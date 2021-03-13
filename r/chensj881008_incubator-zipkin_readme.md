[![Gitter chat](http://img.shields.io/badge/gitter-join%20chat%20%E2%86%92-brightgreen.svg)](https://gitter.im/openzipkin/zipkin)
[![Build Status](https://img.shields.io/jenkins/s/https/builds.apache.org/job/incubator-zipkin.svg)](https://builds.apache.org/blue/organizations/jenkins/incubator-zipkin)
[![Maven Central](https://img.shields.io/maven-central/v/org.apache.zipkin/zipkin-server.svg)](https://search.maven.org/search?q=g:org.apache.zipkin%20AND%20a:zipkin-server)

# zipkin
[Zipkin](http://u.720life.cn/g/17c5ce8e0ecb6066a2f15a2cc8f8cf8d)  is a distributed tracing system. It helps gather timing data needed to troubleshoot latency problems in microservice architectures. It manages both the collection and lookup of this data. Zipkin’s design is based on the [Google Dapper paper](http://u.720life.cn/g/34e2e041e0a09d204ff62d1d75406c00309c65f46aac80b52bb829aec40806fbf91cb5e733d40a6be179220511af3db4 

This project includes a dependency-free library and a [spring-boot](http://u.720life.cn/g/e0845233bf5cae93142c4c8e1c8864d4e670a90f87afc2ad04fb4c1d1899c07f92f1cd313affd115e19808b7bfd858ec)  server. Storage options include in-memory, JDBC (mysql), Cassandra, and Elasticsearch.

## Quick-start

The quickest way to get started is to fetch the [latest released server](http://u.720life.cn/g/96ed47473b0145f8df365f77c67cbdd826a6be446775885ca5adf65a64c6b96a8ba689ed0c49e9085e1628a4a0e54bb0b5e6a8c405c582f35f92a101741276d278b8ccf0ecf394a2ba4719d09769a50fe0ffb4b01186c2c6abd753c7788415f4)  as a self-contained executable jar. Note that the Zipkin server requires minimum JRE 8. For example:

```bash
curl -sSL https://zipkin.io/quickstart.sh | bash -s
java -jar zipkin.jar
```

You can also start Zipkin via Docker.
```bash
docker run -d -p 9411:9411 openzipkin/zipkin
```

Once the server is running, you can view traces with the Zipkin UI at `http://your_host:9411/zipkin/`.

If your applications aren't sending traces, yet, configure them with [Zipkin instrumentation](http://u.720life.cn/g/cf45ebab08d11246d3cf0ea3448323830367a0c9e65d18abec66ae426dadf435bcb48555c5d0b7302349d310fdb63fc1)  or try one of our [examples](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304693f07f94b5d3bfcfd7c70522bed9395283ef25a02ed6f5cbf54489671f3a597f711c7cdefd7cf5d68a36ac20be7fb66a 

Check out the [`zipkin-server`](/zipkin-server) documentation for configuration details, or [`docker-zipkin`](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e4da780ee2a704c8408a3f1628ae467799743a9a026637524c691e5babd9d6f2)  for how to use docker-compose.

## Core Library
The [core library](zipkin2/src/main/java/zipkin2) is used by both Zipkin instrumentation and the Zipkin server. Its minimum Java language level is 6, in efforts to support those writing agent instrumentation.

This includes built-in codec for Zipkin's v1 and v2 json formats. A direct dependency on gson (json library) is avoided by minifying and repackaging classes used. The result is a 155k jar which won't conflict with any library you use.

Ex.
```java
// All data are recorded against the same endpoint, associated with your service graph
localEndpoint = Endpoint.newBuilder().serviceName("tweetie").ip("192.168.0.1").build()
span = Span.newBuilder()
    .traceId("d3d200866a77cc59")
    .id("d3d200866a77cc59")
    .name("targz")
    .localEndpoint(localEndpoint)
    .timestamp(epochMicros())
    .duration(durationInMicros)
    .putTag("compression.level", "9");

// Now, you can encode it as json
bytes = SpanBytesEncoder.JSON_V2.encode(span);
```

Note: The above is just an example, most likely you'll want to use an existing tracing library like [Brave](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304627097d68610c56d6d509e6b29b670875eff8ef36831e8b6e277a0b0ffe0b3133) 

## Storage Component
Zipkin includes a [StorageComponent](zipkin/src/main/java/zipkin2/storage/StorageComponent.java), used to store and query spans and
dependency links. This is used by the server and those making custom
servers, collectors, or span reporters. For this reason, storage
components have minimal dependencies, but most require Java 8+

Ex.
```java
// this won't create network connections
storage = ElasticsearchStorage.newBuilder()
                              .hosts(asList("http://myelastic:9200")).build();

// prepare a call
traceCall = storage.spanStore().getTrace("d3d200866a77cc59");

// execute it synchronously or asynchronously
trace = traceCall.execute();

// clean up any sessions, etc
storage.close();
```

### In-Memory
The [InMemoryStorage](zipkin2/src/main/java/zipkin2/storage/InMemoryStorage.java) component is packaged in zipkin's core library. It
is neither persistent, nor viable for realistic work loads. Its purpose
is for testing, for example starting a server on your laptop without any
database needed.

### Cassandra
The [Cassandra](zipkin-storage/cassandra) component is tested against
Cassandra 3.11.3+. It stores spans using UDTs, such that they appear like
the v2 Zipkin model in cqlsh. It is designed for scale. For example, it
uses a combination of SASI and manually implemented indexes to make
querying larger data more performant.

Note: This store requires a [spark job](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463f08d0770dfdbffebf3b8e18c3420ce5c54edf3460a763e1a01364b731a2020fcf88988a2353839b83c52ac3387205b8)  to aggregate dependency links.

### Elasticsearch
The [Elasticsearch](zipkin-storage/elasticsearch) component is tested against Elasticsearch 2-6.x.
It stores spans as json and has been designed for larger scale.

Note: This store requires a [spark job](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463f08d0770dfdbffebf3b8e18c3420ce5c54edf3460a763e1a01364b731a2020fcf88988a2353839b83c52ac3387205b8)  to aggregate dependency links.

### Disabling search
The following API endpoints provide search features, and are enabled by
default. Search primarily allows the trace list screen of the UI operate.
* `GET /services` - Distinct Span.localServiceName
* `GET /remoteServices?serviceName=X` - Distinct Span.remoteServiceName by Span.localServiceName
* `GET /spans?serviceName=X` - Distinct Span.name by Span.localServiceName
* `GET /autocompleteKeys` - Distinct keys of Span.tags subject to configurable whitelist
* `GET /autocompleteValues?key=X` - Distinct values of Span.tags by key
* `GET /traces` - Traces matching a query possibly including the above criteria


When search is disabled, traces can only be retrieved by ID
(`GET /trace/{traceId}`). Disabling search is only viable when there is
an alternative way to find trace IDs, such as logs. Disabling search can
reduce storage costs or increase write throughput.

`StorageComponent.Builder.searchEnabled(false)` is implied when a zipkin
is run with the env variable `SEARCH_ENABLED=false`.

### Legacy (v1) components
The following components are no longer encouraged, but exist to help aid
transition to supported ones. These are indicated as "v1" as they use
data layouts based on Zipkin's V1 Thrift model, as opposed to the
simpler v2 data model currently used.

#### MySQL
The [MySQL v1](zipkin-storage/mysql-v1) component currently is only
tested with MySQL 5.6-7. It is designed to be easy to understand, and
get started with. For example, it deconstructs spans into columns, so
you can perform ad-hoc queries using SQL. However, this component has
[known performance issues](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c0001bca31ae58bae1a9ea2d5840c8aa1be86ff0ffe00b1aa2790940765b38c3f367c28c1b54c7aebf85ffab3410c77e  queries will eventually take seconds to return
if you put a lot of data into it.

#### Cassandra
The [Cassandra v1](zipkin-storage/cassandra-v1) component is tested
against Cassandra 2.2+. It stores spans as opaque thrifts which means
you can't read them in cqlsh. However, it is designed for scale. For
example, it has manually implemented indexes to make querying larger
data more performant. This store requires a [spark job](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463f08d0770dfdbffebf3b8e18c3420ce5c54edf3460a763e1a01364b731a2020fcf88988a2353839b83c52ac3387205b8)  to aggregate
dependency links.

## Running the server from source
The [Zipkin server](zipkin-server) receives spans via HTTP POST and respond to queries
from its UI. It can also run collectors, such as RabbitMQ or Kafka.

To run the server from the currently checked out source, enter the
following. JDK 8 is required.
```bash
# Build the server and also make its dependencies
$ ./mvnw -DskipTests --also-make -pl zipkin-server clean install
# Run the server
$ java -jar ./zipkin-server/target/zipkin-server-*exec.jar
```

## Artifacts
Server artifacts are under the maven group id `org.apache.zipkin`
Library artifacts are under the maven group id `org.apache.zipkin.zipkin2`
### Source Releases
Source Releases are uploaded to [Apache](http://u.720life.cn/g/531b4004ef880dee4e9176f85fce89d22ee58c820b137b28bdff2105f2de5b301ce412f2560b3b4b705b15d8e281de410c93c0e51dc5532e4d46a0d840a3acc543f1ee7057fe3fc1ca14d1f54dec21a5) 
### Binary Releases
Binary Releases are uploaded to [Apache](http://u.720life.cn/g/4c86c7768832f9860ee70c4b92b737942ed8b8d0a5c0d415f051e0e2277d9d125493756ad5f63d58d9d47da3cbc33b7e85a3d4b6c27384abfbadcf4bf062afd7569816e0165680dc2cbd3753726d90c0)  and synchronized to [Maven Central](http://u.720life.cn/g/686169b320f6084fa4aea25a9bdaff1c54fff8d070e2826c25013b3d9a2991ae1b09eefe96f02c97b17ddb2e16814aac0b339b45597ae41874d0a3a4a8fa15d8c2dbcf64861d349f64e9cccd172641f6) 
### Binary Snapshots
Binary Snapshots are uploaded to [Apache](http://u.720life.cn/g/4c86c7768832f9860ee70c4b92b73794541b4b9c79da1614fb7519f21d1aea2f769d596da5a51bb75176653e295ede8d434441b2a713e90f3b29c0a0e33385e7)  after commits to master.




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)