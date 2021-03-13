# gRPC Spring Boot Starter

[![Build Status](https://travis-ci.org/yidongnan/grpc-spring-boot-starter.svg?branch=master)](https://travis-ci.org/yidongnan/grpc-spring-boot-starter)
[![Maven Central with version prefix filter](https://img.shields.io/maven-central/v/net.devh/grpc-spring-boot-starter.svg)](http://search.maven.org/#search%7Cga%7C1%7Cg%3A%22net.devh%22%20grpc)
[![MIT License](https://img.shields.io/github/license/mashape/apistatus.svg)](LICENSE)

[![Client-Javadoc](https://www.javadoc.io/badge/net.devh/grpc-client-spring-boot-autoconfigure.svg?label=Client-Javadoc)](https://www.javadoc.io/doc/net.devh/grpc-client-spring-boot-autoconfigure)
[![Server-Javadoc](https://www.javadoc.io/badge/net.devh/grpc-server-spring-boot-autoconfigure.svg?label=Server-Javadoc)](https://www.javadoc.io/doc/net.devh/grpc-server-spring-boot-autoconfigure)
[![Common-Javadoc](https://www.javadoc.io/badge/net.devh/grpc-common-spring-boot.svg?label=Common-Javadoc)](https://www.javadoc.io/doc/net.devh/grpc-common-spring-boot)

README: [English](README.md) | [中文](README-zh.md)

## Features

* Auto configures and runs the embedded gRPC server with `@GrpcService`-enabled beans as part of your spring-boot
application

* Automatically creates and manages your grpc channels and stubs with `@GrpcClient`

* Supports [Spring Cloud](http://u.720life.cn/g/c6d1b26d763f49c99d62f7dd7e1f263d74791681f9785d83f6cd6c957366ad1dd6abd36b3d488c22bff8dcabd4ce747f)  (register services to [Consul](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046bb92d12e4c5b020779e917ba40822747fd90e357620a2095258f2b805bfe5100da94ac43a8b264ac09744a8acccf451f)  or [Eureka](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046bb92d12e4c5b020779e917ba40822747640ec59bcfcc304bf2ddf3ff010a55e90c80107bc5d93956230a3b62541aac8e)  and fetch gRPC server information)

* Supports [Spring Sleuth](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046bb92d12e4c5b020779e917ba4082274714604e9d86a8810ad97cd1a30c5933b8f320cabf41554e565a91d8e84618e578)  as distributed tracing solution (If [brave-instrumentation-grpc](http://u.720life.cn/g/7ce2d2ef6590cc535c0771ea8b234faeb326ae1cdebeac2489768a7f46dda1a4fed37fb60d6a508575440bdbf1b89694eded775aab4ccbf4952510ec5e2a3b7357e4f60d1c38340fccbb341f7a326254)  is present)

* Supports global and custom gRPC server/client interceptors

* [Spring-Security](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304611a5405430b6b0aabdafc095c1a5e14d45ba110baaae1f3032857394441a13900934377dbafc342b405d42e59ebbc422)  support

* Automatic metric support ([micrometer](http://u.720life.cn/g/30758ccd9ec903beefadccc833e460443c1ccab0f76c4ec0e1c5823c11b0abaa7ee39ae680a4c37c622872d831b30f2833c1698fc3f6b93b48a95ac23c5b4443094124829a879f795ee80c0e67bd2872ad85dfcad06c05615fb49c7fc20d86da70aaba80a137e0984f16d6c33de0089b74aa069548542e754259d69a82fa3acc268f0c0cb582217a5810fe02ed425ddd)  based)

* Also works with (non-shaded) grpc-netty

## Versions

2.x.x.RELEASE support Spring Boot 2 & Spring Cloud Finchley, Greenwich.

The latest version: ``2.2.1.RELEASE``

1.x.x.RELEASE support Spring Boot 1 & Spring Cloud Edgware, Dalston, Camden.

The latest version: ``1.4.1.RELEASE``

**Note:** This project can also be used without Spring-Boot, however that requires some manual bean configuration.

## Usage

### gRPC server + client

To add a dependency using Maven, use the following:

````xml
 
   net.devh 
   grpc-spring-boot-starter 
   2.2.1.RELEASE 
 
````

To add a dependency using Gradle:

````gradle
dependencies {
  compile 'net.devh:grpc-spring-boot-starter:2.2.1.RELEASE'
}
````

### gRPC server

To add a dependency using Maven, use the following:

````xml
 
   net.devh 
   grpc-server-spring-boot-starter 
   2.2.1.RELEASE 
 
````

To add a dependency using Gradle:

````gradle
dependencies {
  compile 'net.devh:grpc-server-spring-boot-starter:2.2.1.RELEASE'
}
````

Annotate your server interface implementation(s) with ``@GrpcService``

````java
@GrpcService
public class GrpcServerService extends GreeterGrpc.GreeterImplBase {

    @Override
    public void sayHello(HelloRequest req, StreamObserver  responseObserver) {
        HelloReply reply = HelloReply.newBuilder().setMessage("Hello ==> " + req.getName()).build();
        responseObserver.onNext(reply);
        responseObserver.onCompleted();
    }

}
````

By default, the grpc server will listen to port 9090. These and other
[settings](grpc-server-spring-boot-autoconfigure/src/main/java/net/devh/boot/grpc/server/config/GrpcServerProperties.java)
can be changed via Spring's property mechanism. The server uses the `grpc.server.` prefix.

#### Example-Properties

````properties
grpc.server.port=9090
grpc.server.address=0.0.0.0
````

#### Customizing a Server

This library also supports custom changes to the `ServerBuilder` during creation by creating `GrpcServerConfigurer` beans.

````java
@Bean
public GrpcServerConfigurer keepAliveServerConfigurer() {
  return serverBuilder -> {
    if (serverBuilder instanceof NettyServerBuilder) {
      ((NettyServerBuilder) serverBuilder)
          .keepAliveTime(30, TimeUnit.SECONDS)
          .keepAliveTimeout(5, TimeUnit.SECONDS)
          .permitKeepAliveWithoutCalls(true);
    }
  };
}
````

#### Server-Security

This library supports securing the grpc application with Spring-Security. You only have to add Spring-Security (core or
config) to your dependencies and then configure it as needed.

##### First choose an authentication scheme

* **BasicAuth**

  ````java
  @Bean
  AuthenticationManager authenticationManager() {
      final List  providers = new ArrayList<>();
      providers.add(...); // Possibly DaoAuthenticationProvider
      return new ProviderManager(providers);
  }

  @Bean
  GrpcAuthenticationReader authenticationReader() {
      final List  readers = new ArrayList<>();
      readers.add(new BasicGrpcAuthenticationReader());
      return new CompositeGrpcAuthenticationReader(readers);
  }
  ````

* **Bearer Authentication (OAuth2/OpenID-Connect)**

  ````java
  @Bean
  AuthenticationManager authenticationManager() {
      final List  providers = new ArrayList<>();
      providers.add(...); // Possibly JwtAuthenticationProvider
      return new ProviderManager(providers);
  }

  @Bean
  GrpcAuthenticationReader authenticationReader() {
      final List  readers = new ArrayList<>();
      readers.add(new BearerAuthenticationReader(accessToken -> new BearerTokenAuthenticationToken(accessToken)));
      return new CompositeGrpcAuthenticationReader(readers);
  }
  ````

  You might also want to define your own *GrantedAuthoritiesConverter* to map the permissions/roles in the bearer token
  to Spring Security's `GrantedAuthority`s.

* **Certificate Authentication**

  ````java
  @Bean
  AuthenticationManager authenticationManager() {
      final List  providers = new ArrayList<>();
      providers.add(new X509CertificateAuthenticationProvider(userDetailsService()));
      return new ProviderManager(providers);
  }

  @Bean
  GrpcAuthenticationReader authenticationReader() {
      final List  readers = new ArrayList<>();
      readers.add(new SSLContextGrpcAuthenticationReader());
      return new CompositeGrpcAuthenticationReader(readers);
  }
  ````

  and some properties:

  ````properties
  grpc.server.security.enabled=true
  grpc.server.security.certificateChainPath=certificates/server.crt
  grpc.server.security.privateKeyPath=certificates/server.key
  grpc.server.security.trustCertCollectionPath=certificates/trusted-clients-collection
  grpc.server.security.clientAuth=REQUIRE
  ````

* **Chain multiple mechanisms by using the `CompositeGrpcAuthenticationReader` class**
* **Your own authentication mechanism (Implement a `GrpcAuthenticationReader` yourself)**

##### Then decide on how you want to protect the services

* **Via Spring-Security's annotations**

  ````java
  @Configuration
  @EnableGlobalMethodSecurity(proxyTargetClass = true, ...)
  public class SecurityConfiguration {
  ````

  `proxyTargetClass` is required, if you use annotation driven security!
  However, you will receive a warning that MyServiceImpl#bindService() method is final.
  You cannot avoid that warning (without massive amount of work), but it is safe to ignore it.
  The `#bindService()` method uses a reference to `this`, which will be used to invoke the methods.
  If the method is not final it will delegate to the original instance and thus it will bypass any security layer that
  you intend to add, unless you re-implement the `#bindService()` method on the outermost layer (which Spring does not).

* **Via manual configuration**

  ````java
  @Bean
  AccessDecisionManager accessDecisionManager() {
      final List > voters = new ArrayList<>();
      voters.add(new AccessPredicateVoter());
      return new UnanimousBased(voters);
  }

  @Bean
  GrpcSecurityMetadataSource grpcSecurityMetadataSource() {
      final ManualGrpcSecurityMetadataSource source = new ManualGrpcSecurityMetadataSource();
      source.set(MyServiceGrpc.getSecureMethod(), AccessPredicate.hasRole("ROLE_USER"));
      source.setDefault(AccessPredicate.permitAll());
      return source;
  }
  ````

### gRPC client

To add a dependency using Maven, use the following:

````xml
 
   net.devh 
   grpc-client-spring-boot-starter 
   2.2.1.RELEASE 
 
````

To add a dependency using Gradle:

````gradle
dependencies {
  compile 'net.devh:grpc-client-spring-boot-starter:2.2.1.RELEASE'
}
````

There are three ways to get a connection to the gRPC server:

* Use `grpcChannelFactory.createChannel(serverName)` to create a `Channel` and create the grpc stub
  yourself.

  ````java
  @Autowired
  private GrpcChannelFactory grpcChannelFactory;

  private GreeterGrpc.GreeterBlockingStub greeterStub;

  @PostConstruct
  public void init() {
      Channel channel = grpcChannelFactory.createChannel("gRPC server name");
      greeterStub = GreeterGrpc.newBlockingStub(channel);
  }
  ````

* Annotate a field of type `Channel` with `@GrpcClient(serverName)` and create the grpc stub yourself.
  * Do not use in conjunction with `@Autowired` or `@Inject`

  ````java
  @GrpcClient("gRPC server name")
  private Channel channel;

  private GreeterGrpc.GreeterBlockingStub greeterStub;

  @PostConstruct
  public void init() {
      greeterStub = GreeterGrpc.newBlockingStub(channel);
  }
  ````

* Annotate a field of your grpc client stub with `@GrpcClient(serverName)`
  * Do not use in conjunction with `@Autowired` or `@Inject`

  ````java
  @GrpcClient("gRPC server name")
  private GreeterGrpc.GreeterBlockingStub greeterStub;
  ````

**Note:** You can use the same grpc server name for multiple channels and also different stubs (even with different
interceptors).

Then you can send queries to your server just like this:

````java
HelloReply response = stub.sayHello(HelloRequest.newBuilder().setName(name).build());
````

It is possible to configure the target address for each client individually.
However in some cases, you can just rely on the default configuration.
You can customize the default url mapping via `NameResolver.Factory` beans. If you don't configure that bean,
then the default uri will be resolved as followed:

* If a `DiscoveryClient` bean is present, then the client name will be used to search inside the discovery client.
* Otherwise the client assumes that the server runs on `localhost` with port `9090`.

These and other
[settings](grpc-client-spring-boot-autoconfigure/src/main/java/net/devh/boot/grpc/client/config/GrpcChannelProperties.java)
can be changed via Spring's property mechanism. The clients use the `grpc.client.(serverName).` prefix.

It is also possible to list multiple target IP addresses with automatic load balancing like this:

* `static://127.0.0.1:9090,[::1]:9090`

You can also use service discovery based address resolution like this (requires a `DiscoveryClient` bean):

* `discovery:///my-service-name`

Additionally, you can use DNS based address resolution like this:

* `dns:///example.com`

This will automatically read all IP addresses from that domain and use them for load balancing.
Please note that `grpc-java` caches the DNS response for performance reasons.
Read more about these and other natively supported `NameResolverProviders` in the official [grpc-java sources](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046fe94b7b76179efc377526a00a74b2d14f55d3d7d65037b5d32a3f9a84dc0ad1e 

#### Example-Properties

````properties
grpc.client.GLOBAL.enableKeepAlive=true

grpc.client.(gRPC server name).address=static://localhost:9090
# Or
grpc.client.myName.address=static://localhost:9090
````

`GLOBAL` is a special constant that will be used as a fallback for configuration options that are not configured per client.
Order of precedence: Per Client > `GLOBAL` > defaults

#### Customizing a Client

This library also supports custom changes to the `ManagedChannelBuilder` and gRPC client stubs during creation by creating `GrpcChannelConfigurer` and `StubTransformer` beans.

````java
@Bean
public GrpcChannelConfigurer keepAliveClientConfigurer() {
  return (channelBuilder, name) -> {
    if (channelBuilder instanceof NettyChannelBuilder) {
      ((NettyChannelBuilder) channelBuilder)
          .keepAliveTime(15, TimeUnit.SECONDS)
          .keepAliveTimeout(5, TimeUnit.SECONDS);
    }
  };
}

@Bean
public StubTransformer authenticationStubTransformer() {
  return (clientName, stub) -> stub.withCallCredentials(grpcCredentials(clientName));
}
````

#### Client-Authentication

**Note:** The following section only applies, if you use injected stubs. If you inject a channel, or create the stubs
yourself, then you have to configure the credentials yourself. However, you might still be able to benefit from the
provided helper methods.

There are multiple ways for the client to authenticate itself. Simply define a bean of type `CallCredentials` and
it will automatically be used for authentication. Currently the following are supported via helper methods:

* **BasicAuth**

  ````java
  @Bean
  CallCredentials grpcCredentials() {
    return CallCredentialsHelper.basicAuth(username, password);
  }
  ````

* **Bearer Authentication (OAuth2, OpenID-Connect)**

  ````java
  @Bean
  CallCredentials grpcCredentials() {
    return CallCredentialsHelper.bearerAuth(token);
  }
  ````

* **Certificate Authentication**

  Only needs some configuration properties:

  ````properties
  #grpc.client.test.security.authorityOverride=localhost
  #grpc.client.test.security.trustCertCollectionPath=certificates/trusted-servers-collection
  grpc.client.test.security.clientAuthEnabled=true
  grpc.client.test.security.certificateChainPath=certificates/client.crt
  grpc.client.test.security.privateKeyPath=certificates/client.key
  ````

* **Different credentials per client(name)**

  Instead of adding a `CallCredentials` bean to your context you have to define a `StubTransformer` bean:

  ````java
  @Bean
  StubTransformer grpcCredentialsStubTransformer() {
    return CallCredentialsHelper.mappedCredentialsStubTransformer(
        Map.of(
            clientA, callCredentialsAC,
            clientB, callCredentialsB,
            clientC, callCredentialsAC));
  }
  ````

  **Note:** There might be conflicts if you configure exactly one `CallCredentials` in the application context in
  this scenario.

## Running with (non-shaded) grpc-netty

This library supports both `grpc-netty` and `grpc-netty-shaded`.
The later one might prevent conflicts with incompatible grpc-versions or conflicts between libraries that require different versions of netty.

**Note:** If the shaded netty is present on the classpath, then this library will always favor it over the non-shaded grpc-netty one.

You can use it with Maven like this:

````xml
 
     io.grpc 
     grpc-netty 
     ${grpcVersion} 
 

 
 
     net.devh 
     grpc-spring-boot-starter 
     ... 
     
         
             io.grpc 
             grpc-netty-shaded 
         
     
 
 
 
     net.devh 
     grpc-server-spring-boot-starter 
     ... 
     
         
             io.grpc 
             grpc-netty-shaded 
         
     
 
 
 
     net.devh 
     grpc-client-spring-boot-starter 
     ... 
     
         
             io.grpc 
             grpc-netty-shaded 
         
     
 
````

and like this when using Gradle:

````groovy
compile "io.grpc:grpc-netty:${grpcVersion}"

compile 'net.devh:grpc-spring-boot-starter:...' exclude group: 'io.grpc', module: 'grpc-netty-shaded' // For both
compile 'net.devh:grpc-client-spring-boot-starter:...' exclude group: 'io.grpc', module: 'grpc-netty-shaded' // For the client (only)
compile 'net.devh:grpc-server-spring-boot-starter:...' exclude group: 'io.grpc', module: 'grpc-netty-shaded' // For the server (only)
````

## Example-Projects

Read more about our example projects [here](examples).

## Troubleshooting

Before you begin to dive into the details, make sure that the grpc and netty library versions are compatible with each other.
This library brings all necessary dependencies for grpc and netty to work together.
In some cases, however, you may need additional libraries such as tcnative or have other dependencies that require a different version of netty, which may cause conflicts.
To prevent such issues gRPC and us recommend using the grpc-netty-shaded dependency.
If you are using the (non-shaded) grpc-netty, please check the [table](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046fe94b7b76179efc377526a00a74b2d14df093440382fccdec171ec3809a241f72e271a46b354d7adbea4f8bcc1caf48a)  provided by [grpc-java](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046fe94b7b76179efc377526a00a74b2d14c00fa7a6b57a563f070acefaa90d243b  which displays compatible version combinations.

### Issues with SSL in general

* `java.lang.IllegalStateException: Failed to load ApplicationContext`
* `Caused by: org.springframework.context.ApplicationContextException: Failed to start bean 'grpcServerLifecycle'`
* `Caused by: java.lang.IllegalStateException: Could not find TLS ALPN provider; no working netty-tcnative, Conscrypt, or Jetty NPN/ALPN available`

or

* `AbstractMethodError: io.netty.internal.tcnative.SSL.readFromSSL()`

or

* `javax.net.ssl.SSLHandshakeException: General OpenSslEngine problem`

You don't have the (correct) library or version of `netty-tcnative...` in your classpath.

(There is a breaking change between netty 4.1.24.Final -> 4.1.27.Final and netty-tcnative 2.0.8.Final -> 2.0.12.Final and also elsewhere)

See also [grpc-java: Security](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046fe94b7b76179efc377526a00a74b2d14df093440382fccdec171ec3809a241f7633e74ed5af8b947c2e4cd3b2732b7332293e5813defc6cd6d51fe86680d6e66 

### Issues with SSL during tests

By default, the grpc client assumes that the server uses TLS and will try to use a secure connection. During development
and for tests is it unlikely that the required certificates are available thus you have to switch to `PLAINTEXT`
connection mode.

````properties
grpc.client.(gRPC server name).negotiationType=PLAINTEXT
````

**Note:** The grpc protocol and we strongly recommend using `TLS` for production use.

### Server port already in use during tests

Sometimes you just want to launch your application in your test classes to check the interaction between your services.
This will also start the grpc server, however it won't be shut down after each test (class) individually. You can avoid that issue by
adding `@DirtiesContext` to your test classes or methods.

### No name matching XXX found

* `io.grpc.StatusRuntimeException: UNAVAILABLE: io exception`
* `Caused by: javax.net.ssl.SSLHandshakeException: General OpenSslEngine problem`
* `Caused by: java.security.cert.CertificateException: No name matching gRPC server name found`

The name of the `gRPC server name` in the client config does not match the common / alternative name in the server
certificate. You have to configure the `grpc.client.(gRPC server name).security.authorityOverride`
property with a name that is present in the certificate.

## Contributing

Contributions are always welcomed! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

## Show case

https://github.com/yidongnan/grpc-spring-boot-starter/tree/master/examples



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)