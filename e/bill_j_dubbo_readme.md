# Apache Dubbo Project

[![Build Status](https://travis-ci.org/apache/dubbo.svg?branch=master)](https://travis-ci.org/apache/dubbo)
[![codecov](https://codecov.io/gh/apache/dubbo/branch/master/graph/badge.svg)](https://codecov.io/gh/apache/dubbo)
![maven](https://img.shields.io/maven-central/v/org.apache.dubbo/dubbo.svg)
![license](https://img.shields.io/github/license/alibaba/dubbo.svg)
[![Average time to resolve an issue](http://isitmaintained.com/badge/resolution/apache/dubbo.svg)](http://isitmaintained.com/project/apache/dubbo "Average time to resolve an issue")
[![Percentage of issues still open](http://isitmaintained.com/badge/open/apache/dubbo.svg)](http://isitmaintained.com/project/apache/dubbo "Percentage of issues still open")
[![Tweet](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)](https://twitter.com/intent/tweet?text=Apache%20Dubbo%20is%20a%20high-performance%2C%20java%20based%2C%20open%20source%20RPC%20framework.&url=http://dubbo.apache.org/&via=ApacheDubbo&hashtags=rpc,java,dubbo,micro-service)
[![](https://img.shields.io/twitter/follow/ApacheDubbo.svg?label=Follow&style=social&logoWidth=0)](https://twitter.com/intent/follow?screen_name=ApacheDubbo)
[![Gitter](https://badges.gitter.im/alibaba/dubbo.svg)](https://gitter.im/alibaba/dubbo?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

Apache Dubbo is a high-performance, Java based open source RPC framework. Please visit [official site](http://u.720life.cn/g/d01e1e84c56b9ce2c8f8c95cb6c6ddc79a43753092211076172485a24a5b6b4e)  for quick start and documentations, as well as [Wiki](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdb15e9787d9f61eedac52dbabac0e834b457bc7a7b36cba6d8a87f1105f57)  for news, FAQ, and release notes.

We are now collecting dubbo user info in order to help us to improve Dubbo better, pls. kindly help us by providing yours on [issue#1012: Wanted: who's using dubbo](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdb15e9787d9f61eedac52dbabac0e4683a38d757b25342e98cac6930af33a  thanks :)

## Architecture

![Architecture](http://dubbo.apache.org/img/architecture.png)

## Features

* Transparent interface based RPC
* Intelligent load balancing
* Automatic service registration and discovery
* High extensibility
* Runtime traffic routing
* Visualized service governance

## Getting started

The following code snippet comes from [Dubbo Samples](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304621966f7a4da201eaa2cd01924b2e22ecaab07284fe56cca00b1d19c92f7786b8b282a48fce3183759ff59720cf1474363280745ad263533965474e3fa364c580  You may clone the sample project and step into `dubbo-samples-api` sub directory before read on.

```bash
# git clone https://github.com/apache/dubbo-samples.git
# cd dubbo-samples/java/dubbo-samples-api
```

There's a [README](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304621966f7a4da201eaa2cd01924b2e22ecaab07284fe56cca00b1d19c92f7786b8b282a48fce3183759ff59720cf1474367f738d004ab8f8025204cbcf54a1ec0388216974ac82ea57bf0813f62e539feb)  file under `dubbo-samples-api` directory. Read it and try this sample out by following the instructions.

### Maven dependency

```xml
 
     2.7.7 
 
    
 
     
         org.apache.dubbo 
         dubbo 
         ${dubbo.version} 
     
     
         org.apache.dubbo 
         dubbo-dependencies-zookeeper 
         ${dubbo.version} 
         pom 
     
 
```

### Define service interfaces

```java
package org.apache.dubbo.samples.api;

public interface GreetingService {
    String sayHi(String name);
}
```

*See [api/GreetingService.java](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304621966f7a4da201eaa2cd01924b2e22ec178ca8226ff928386e0c54beb9f7ea1a7528dead789126da983b3cbce492fa274e539860a1ff0b3875a92c2bae3c09ea1391fe4c9408bea6977e87759718aabdff0297236e95bd148193fc54f390a59174cf8dbc6bc99789626c7af2daa417a35b0f0d072c3d951a51bb4dc15918ca7b)  on GitHub.*

### Implement service interface for the provider

```java
package org.apache.dubbo.samples.provider;

import org.apache.dubbo.samples.api.GreetingsService;

public class GreetingsServiceImpl implements GreetingsService {
    @Override
    public String sayHi(String name) {
        return "hi, " + name;
    }
}
```

*See [provider/GreetingServiceImpl.java](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304621966f7a4da201eaa2cd01924b2e22ec178ca8226ff928386e0c54beb9f7ea1a7528dead789126da983b3cbce492fa274e539860a1ff0b3875a92c2bae3c09ea1391fe4c9408bea6977e87759718aabdff0297236e95bd148193fc54f390a591f03dbcaccff185ebdfe48c173dd9f311706b9403c64ed1b4b7b8ebb57ba246f69e67d775e5f22c2e4009ea1e20ffa8f5)  on GitHub.*

### Start service provider

```java
package org.apache.dubbo.samples.provider;


import org.apache.dubbo.config.ApplicationConfig;
import org.apache.dubbo.config.RegistryConfig;
import org.apache.dubbo.config.ServiceConfig;
import org.apache.dubbo.samples.api.GreetingsService;

import java.util.concurrent.CountDownLatch;

public class Application {
    private static String zookeeperHost = System.getProperty("zookeeper.address", "127.0.0.1");

    public static void main(String[] args) throws Exception {
        ServiceConfig  service = new ServiceConfig<>();
        service.setApplication(new ApplicationConfig("first-dubbo-provider"));
        service.setRegistry(new RegistryConfig("zookeeper://" + zookeeperHost + ":2181"));
        service.setInterface(GreetingsService.class);
        service.setRef(new GreetingsServiceImpl());
        service.export();

        System.out.println("dubbo service started");
        new CountDownLatch(1).await();
    }
}
```

*See [provider/Application.java](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304621966f7a4da201eaa2cd01924b2e22ec178ca8226ff928386e0c54beb9f7ea1a7528dead789126da983b3cbce492fa274e539860a1ff0b3875a92c2bae3c09ea1391fe4c9408bea6977e87759718aabdff0297236e95bd148193fc54f390a591b0d94ced51d035e06925c72ac1d9c2f9734b0db91eb8d8a173e8b079d74b3eee)  on GitHub.*

### Build and run the provider

```bash
# mvn clean package
# mvn -Djava.net.preferIPv4Stack=true -Dexec.mainClass=org.apache.dubbo.samples.provider.Application exec:java
```

### Call remote service in consumer

```java
package org.apache.dubbo.samples.client;


import org.apache.dubbo.config.ApplicationConfig;
import org.apache.dubbo.config.ReferenceConfig;
import org.apache.dubbo.config.RegistryConfig;
import org.apache.dubbo.samples.api.GreetingsService;

public class Application {
    private static String zookeeperHost = System.getProperty("zookeeper.address", "127.0.0.1");

    public static void main(String[] args) {
        ReferenceConfig  reference = new ReferenceConfig<>();
        reference.setApplication(new ApplicationConfig("first-dubbo-consumer"));
        reference.setRegistry(new RegistryConfig("zookeeper://" + zookeeperHost + ":2181"));
        reference.setInterface(GreetingsService.class);
        GreetingsService service = reference.get();
        String message = service.sayHi("dubbo");
        System.out.println(message);
    }
}
```
*See [consumer/Application.java](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304621966f7a4da201eaa2cd01924b2e22ec178ca8226ff928386e0c54beb9f7ea1a7528dead789126da983b3cbce492fa274e539860a1ff0b3875a92c2bae3c09ea1391fe4c9408bea6977e87759718aabdff0297236e95bd148193fc54f390a5914c2c990a749e92375a0963a3ff64f7cecc1829ca591cd4f578faf425fdb4559d)  on GitHub.*

### Build and run the consumer

```bash
# mvn clean package
# mvn -Djava.net.preferIPv4Stack=true -Dexec.mainClass=org.apache.dubbo.samples.client.Application exec:java
```

The consumer will print out `hi, dubbo` on the screen.


### Next steps

* [Your first Dubbo application](http://u.720life.cn/g/d01e1e84c56b9ce2c8f8c95cb6c6ddc7aae89ad7fadb2d531368d02abfa2066fb6854d3516ac9fa730a25478f2c03270923e05e71546142cc6b42ac65a711bc9)  - A 101 tutorial to reveal more details, with the same code above.
* [Dubbo user manual](http://u.720life.cn/g/d01e1e84c56b9ce2c8f8c95cb6c6ddc7c165b329b07ea011ca5a314b194234174c4252712b8191d97d5f7868d6c4b5a0103387e0903f970a7799ca12ed4328d0)  - How to use Dubbo and all its features.
* [Dubbo developer guide](http://u.720life.cn/g/d01e1e84c56b9ce2c8f8c95cb6c6ddc7c165b329b07ea011ca5a314b19423417e33d41d21aa90b8d00d828509a47ac2b711f37b1bfc84bd9c7a38f5908e81c5f)  - How to involve in Dubbo development.
* [Dubbo admin manual](http://u.720life.cn/g/d01e1e84c56b9ce2c8f8c95cb6c6ddc7c165b329b07ea011ca5a314b19423417ef9a416a0a31527a27342ea5eba56265c09bfd8e8a9b4a312735817986da5b1babb19bf7542a19ccd075f2e3457a7110)  - How to admin and manage Dubbo services.

## Building

If you want to try out the cutting-edge features, you can build with the following commands. (Java 1.8 is required to build the master branch)

```
  mvn clean install
```

## Contact

* Mailing list: 
  * dev list: for dev/user discussion. [subscribe](mailto:dev-subscribe@dubbo.apache.org), [unsubscribe](mailto:dev-unsubscribe@dubbo.apache.org), [archive](http://u.720life.cn/g/cffa11baa100334c83b876d057edfab04a40abb61f522fc35129b5e0c2672ce47f43b25287c7c5c14058d80c02058f187e647bfbbec35326763ef1c195719fdf   [guide](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdb15e9787d9f61eedac52dbabac0ea5e0bf67ad15d703401ffff7e5b35d27da226633b4e47460347a9a9b72560134823675005c003d2a6f6b37ed88418629) 
  
* Bugs: [Issues](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdb15e9787d9f61eedac52dbabac0e4afa5223cf13a7dfbea22b5b2fc4c240ce968aea021f12e351536157ed168cf41278dc1a21baeb81b79b46c994c48c31962399457eeb7c80a305b79849e96b35) 
* Gitter: [Gitter channel](http://u.720life.cn/g/11e95d0ed8d2826912e12fe1dc3f3421ec405df47ecc508b3dacbc5916c9471b)  
* Twitter: [@ApacheDubbo](http://u.720life.cn/g/5ea88169c4a0fbd169233d52478d54fea35dc4661b1417b0757ab7dbf8340330) 

## Contributing

See [CONTRIBUTING](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdb15e9787d9f61eedac52dbabac0e5d2971689814c1dd6d3821ee3a3a189abbf002a907292e58fd450ebd35390bc3)  for details on submitting patches and the contribution workflow.

### How can I contribute?

* Take a look at issues with tag called [`Good first issue`](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdb15e9787d9f61eedac52dbabac0e40b84c470ae7facf0aec90acf4039050788a881220ddeeff47d131ef767435cddb2ba667c9a6ffa064b6ba3f7cd655967df8e6585d4b5c81bc614ad4efb0b17c)  or [`Help wanted`](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdb15e9787d9f61eedac52dbabac0e40b84c470ae7facf0aec90acf4039050788a881220ddeeff47d131ef767435cd9671626ebcb03f9979ffc9c5b3db0544b24b24a1b2be59da8a57690689363378 
* Join the discussion on mailing list, subscription [guide](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdb15e9787d9f61eedac52dbabac0ea5e0bf67ad15d703401ffff7e5b35d27da226633b4e47460347a9a9b7256013461e58da80896b4849d2432596c05861f 
* Answer questions on [issues](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdb15e9787d9f61eedac52dbabac0eeb4849e846ab98b749dbda4b9ca2d970 
* Fix bugs reported on [issues](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdb15e9787d9f61eedac52dbabac0eaeda8ab13b35182622cc23541c6b751c  and send us pull request.
* Review the existing [pull request](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdb15e9787d9f61eedac52dbabac0e13f1e70511c39ddf7463c51b2bcafa26 
* Improve the [website](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304621966f7a4da201eaa2cd01924b2e22ec38f138e1a423659c148e9972bec2e024  typically we need
  * blog post
  * translation on documentation
  * use cases about how Dubbo is being used in enterprise system.
* Improve the [dubbo-admin/dubbo-monitor](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304621966f7a4da201eaa2cd01924b2e22ecee5798fed3310d32076fb6f3725e719a 
* Contribute to the projects listed in [ecosystem](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304609a03ecf7f297f5bcb1a2a855fbeaa81 
* Any form of contribution that is not mentioned above.
* If you would like to contribute, please send an email to dev@dubbo.apache.org to let us know!

## Reporting bugs

Please follow the [template](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdb15e9787d9f61eedac52dbabac0e4afa5223cf13a7dfbea22b5b2fc4c240ce968aea021f12e351536157ed168cf41278dc1a21baeb81b79b46c994c48c31962399457eeb7c80a305b79849e96b35)  for reporting any issues.

## Reporting a security vulnerability

Please report security vulnerability to [us](mailto:security@dubbo.apache.org) privately.

## Dubbo ecosystem

* [Dubbo Ecosystem Entry](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046513a8fc8e7ca3f6ff321e8bc0a0d73554cc0550182ec490eac7c98997a1d51227da11f00b86d17ad5f760d7afcb182b4)  - A GitHub group `dubbo` to gather all Dubbo relevant projects not appropriate in [apache](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d2e0c73bbd71d24c9b75d5caf7908b71)  group yet
* [Dubbo Website](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304621966f7a4da201eaa2cd01924b2e22ec0b7fed59bea7ffeba4e0089258d83ca0)  - Apache Dubbo official website
* [Dubbo Samples](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304621966f7a4da201eaa2cd01924b2e22ec07308fbfdb1270e2b86e253b9f1c8291)  - samples for Apache Dubbo
* [Dubbo Spring Boot](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304621966f7a4da201eaa2cd01924b2e22ecee7882af8930914f3b09636cfad6386a796bd8c220df1a11987fc2261aca6502)  - Spring Boot Project for Dubbo
* [Dubbo Admin](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304621966f7a4da201eaa2cd01924b2e22ec3bfac69b0f2fb24e5f69cc9ef61ed1e9)  - The reference implementation for Dubbo admin
* [Dubbo Awesome](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304621966f7a4da201eaa2cd01924b2e22ec580db729cd208ed1b9f2d20227bb5b9a)  - Dubbo's slides and video links in Meetup

#### Language

* [Node.js](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304621966f7a4da201eaa2cd01924b2e22ec436eb4b3e6daded0a5a9af30b4f99b8c) 
* [Python](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e030edc4066bd22a08c22b47c6a1c6558dbee444e80913559650431089698b1c5f94c4ae82d51f733712de4f31999ac1) 
* [PHP](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304621966f7a4da201eaa2cd01924b2e22ec8e1d5b85d603015763d3735b6dcba075) 
* [Go](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463aa9eb58521f3b6e7d3c4d1c2a3192fc0bdfb061bc30a78156765c4d948296a7) 
* [Erlang](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304621966f7a4da201eaa2cd01924b2e22ecd23a650e829aa9e727f306373cda7f51) 

## License

Apache Dubbo is under the Apache 2.0 license. See the [LICENSE](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdb15e9787d9f61eedac52dbabac0e30975ba11ebb29e1b518a79cb547a0cc3695e13c86b80e7c4763b2ad097b8824)  file for details.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)