# Spring Cloud Alibaba

[![CircleCI](https://circleci.com/gh/alibaba/spring-cloud-alibaba/tree/master.svg?style=svg)](https://circleci.com/gh/alibaba/spring-cloud-alibaba/tree/master)
[![Maven Central](https://img.shields.io/maven-central/v/com.alibaba.cloud/spring-cloud-alibaba-dependencies.svg?label=Maven%20Central)](https://search.maven.org/search?q=g:com.alibaba.cloud%20AND%20a:spring-cloud-alibaba-dependencies)
[![Codecov](https://codecov.io/gh/alibaba/spring-cloud-alibaba/branch/master/graph/badge.svg)](https://codecov.io/gh/alibaba/spring-cloud-alibaba)
[![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)

A project maintained by Alibaba.

See the [中文文档](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460e6a7dcd7c5d55e4e87daf4d62e47dcd144510e6e429065021f36ed65b79b2a92c73a7512a400c58b4000ac512e702c4e46f4fc08d6ca6699e448f901b5f911d)  for Chinese readme.

Spring Cloud Alibaba provides a one-stop solution for distributed application development. It contains all the components required to develop distributed applications, making it easy for you to develop your applications using Spring Cloud.

With Spring Cloud Alibaba, you only need to add some annotations and a small amount of configurations to connect Spring Cloud applications to the distributed solutions of Alibaba, and build a distributed application system with Alibaba middleware.


## Features

* **Flow control and service degradation**：Flow control for HTTP services is supported by default. You can also customize flow control and service degradation rules using annotations. The rules can be changed dynamically.
* **Service registration and discovery**：Service can be registered and clients can discover the instances using Spring-managed beans, auto integration Ribbon.
* **Distributed configuration**：support for externalized configuration in a distributed system, auto refresh when configuration changes.
* **Event-driven**：support for building highly scalable event-driven microservices connected with shared messaging systems.
* **Distributed Transaction**：support for distributed transaction solution with high performance and ease of use.
* **Alibaba Cloud Object Storage**：massive, secure, low-cost, and highly reliable cloud storage services. Support for storing and accessing any type of data in any application, anytime, anywhere.
* **Alibaba Cloud SchedulerX**：accurate, highly reliable, and highly available scheduled job scheduling services with response time within seconds.
* **Alibaba Cloud SMS**： A messaging service that covers the globe, Alibaba SMS provides convenient, efficient, and intelligent communication capabilities that help businesses quickly contact their customers.

For more features, please refer to [Roadmap](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460e6a7dcd7c5d55e4e87daf4d62e47dcd144510e6e429065021f36ed65b79b2a99642a17e262ae791fca39ad230285217d0c71d8fc98c6a900efb490e055e8ab4 

## Components

**[Sentinel](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c089fd6330326c1ada4902057b5192ed7ef3f3ad4843123253a191d5ea80172f  Sentinel takes "traffic flow" as the breakthrough point, and provides solutions in areas such as flow control, concurrency, circuit breaking, and load protection to protect service stability.

**[Nacos](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464ab8bd4ffa2989824d7cb8e96d7b7c73929f04fcba15a8dce8a5820ebb7b4d7b  An easy-to-use dynamic service discovery, configuration and service management platform for building cloud native applications.

**[RocketMQ]https://rocketmq.apache.org/)**：A distributed messaging and streaming platform with low latency, high performance and reliability, trillion-level capacity and flexible scalability.

**[Dubbo]https://github.com/apache/dubbo)**：A high-performance, Java based open source RPC framework.

**[Seata]https://github.com/seata/seata)**：A distributed transaction solution with high performance and ease of use for microservices architecture.

**[Alibaba Cloud ACM]https://www.aliyun.com/product/acm)**：An application configuration center that enables you to centralize the management of application configurations, and accomplish real-time configuration push in a distributed environment.

**[Alibaba Cloud OSS](http://u.720life.cn/g/cc176fdce68265104b8a4a80987ffe393f0578af68b131e06d5e5b3778fa057efd3e2aae70c17e49c58a4d53c0ce2aa2  An encrypted and secure cloud storage service which stores, processes and accesses massive amounts of data from anywhere in the world.

**[Alibaba Cloud SMS](http://u.720life.cn/g/cc176fdce68265104b8a4a80987ffe399575b8120e840863f8a65ff87858b67bf1d46fb705b65c10dfde84ae44965e3b  A messaging service that covers the globe, Alibaba SMS provides convenient, efficient, and intelligent communication capabilities that help businesses quickly contact their customers.

**[Alibaba Cloud SchedulerX](http://u.720life.cn/g/cc176fdce68265104b8a4a80987ffe397a69a8b83a6518b831f6566e94ce9aef86036b87d14854033d7b78bcc78ed53a44b3af36611bec850a35364772454b7a  highly reliable, and highly available scheduled job scheduling services with response time within seconds..

For more features please refer to [Roadmap](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460e6a7dcd7c5d55e4e87daf4d62e47dcd144510e6e429065021f36ed65b79b2a99642a17e262ae791fca39ad230285217d0c71d8fc98c6a900efb490e055e8ab4 

## How to build

* **master branch**: Corresponds to Spring Cloud Greenwich & Spring Boot 2.x. JDK 1.8 or later versions are supported.
* **finchley branch**: Corresponds to Spring Cloud Finchley & Spring Boot 2.x. JDK 1.8 or later versions are supported.
* **1.x branch**: Corresponds to Spring Cloud Edgware & Spring Boot 1.x, JDK 1.7 or later versions are supported.

Spring Cloud uses Maven for most build-related activities, and you should be able to get off the ground quite quickly by cloning the project you are interested in and typing:

	./mvnw install


## How to Use

### Add maven dependency 

These artifacts are available from Maven Central and Spring Release repository via BOM:

	 
         
             
                 com.alibaba.cloud 
                 spring-cloud-alibaba-dependencies 
                 2.2.1.RELEASE 
                 pom 
                 import 
             
         
     

add the module in  `dependencies`.


### Reference Doc

[Contents](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460e6a7dcd7c5d55e4e87daf4d62e47dcd144510e6e429065021f36ed65b79b2a91714b65fc2880b4c2ca522c8a5e24d7a08dc2c3bedeff2867eedd9ce29e71289832c99a61d399c4675cef529a032f9abc14058f747ea09811d9dcbe907eccdf1d85354a77a239e582f85742518985e0e2d74b28ff78d49e95e65daa305b32a87) 

[Nacos Config](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460e6a7dcd7c5d55e4e87daf4d62e47dcd144510e6e429065021f36ed65b79b2a91714b65fc2880b4c2ca522c8a5e24d7a08dc2c3bedeff2867eedd9ce29e71289832c99a61d399c4675cef529a032f9abf230d01956f91425f734578bc26932b24374cd6166618bc78028e0b25e1a5bc1) 

[Nacos Discovery](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460e6a7dcd7c5d55e4e87daf4d62e47dcd144510e6e429065021f36ed65b79b2a91714b65fc2880b4c2ca522c8a5e24d7a08dc2c3bedeff2867eedd9ce29e71289832c99a61d399c4675cef529a032f9abf230d01956f91425f734578bc26932b2877c4d4d7f5a61422af03deebd231914) 

[ACM](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460e6a7dcd7c5d55e4e87daf4d62e47dcd144510e6e429065021f36ed65b79b2a91714b65fc2880b4c2ca522c8a5e24d7a08dc2c3bedeff2867eedd9ce29e71289832c99a61d399c4675cef529a032f9abe7a98334ccd4692104e0fc58ac40871eb3e97fab5abbfa0f7f22edd94c52a0f1) 


## Examples

A `spring-cloud-alibaba-examples` module is included in our project for you to get started with Spring Cloud Alibaba quickly. It contains an example, and you can refer to the readme file in the example project for a quick walkthrough.

Examples：

[Sentinel Example](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460e6a7dcd7c5d55e4e87daf4d62e47dcd144510e6e429065021f36ed65b79b2a9fb196d4e41a80ea80aa1f81e80d78a40acb358719618084937783acccdb32436cac531d627063e7d32a8dec83d93d645c8c7ab7d71def20d92fb1442fba865a20d36e1122d77ed5b6fe7e8f2bbea7a392faef4f7ac65f23a296b891a9b1b24aa) 

[Nacos Config Example](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460e6a7dcd7c5d55e4e87daf4d62e47dcd144510e6e429065021f36ed65b79b2a91714b65fc2880b4c2ca522c8a5e24d7a08dc2c3bedeff2867eedd9ce29e71289899f1cb8f3b33d03ba05433486a84de63ed3d1ffffdb41a32b748c343ee0c63806f9bf9ac7f649a8afd274f2cff11e36a2d3d5e0a92012ce1759d00072e17181) 

[Nacos Discovery Example](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460e6a7dcd7c5d55e4e87daf4d62e47dcd144510e6e429065021f36ed65b79b2a91714b65fc2880b4c2ca522c8a5e24d7a08dc2c3bedeff2867eedd9ce29e71289899f1cb8f3b33d03ba05433486a84de607e993e2767019868efa5b1e4a09c439fc5a90f544dd9b1a991aea58f172b7d127ae3328c2749f728c925937d49b9cfa) 

[RocketMQ Example](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460e6a7dcd7c5d55e4e87daf4d62e47dcd144510e6e429065021f36ed65b79b2a91714b65fc2880b4c2ca522c8a5e24d7a08dc2c3bedeff2867eedd9ce29e71289116938282903b864d096efc901da7ff717190c2d7034f9296dcbf2cfe65f90902567de40d815288542017d76b2888bb6) 

[Alibaba Cloud OSS Example](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460e6a7dcd7c5d55e4e87daf4d62e47dcd144510e6e429065021f36ed65b79b2a91714b65fc2880b4c2ca522c8a5e24d7a08dc2c3bedeff2867eedd9ce29e7128912b3af158c80ab0a4e58b79aee981a3fc69cf8cafe3d2cdbf505e9b2b6259277) 

[Dubbo Spring Cloud Example](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460e6a7dcd7c5d55e4e87daf4d62e47dcd144510e6e429065021f36ed65b79b2a91714b65fc2880b4c2ca522c8a5e24d7a08dc2c3bedeff2867eedd9ce29e7128957aaeea02775a7589efa8dcfa8105a5d7fd084d58f3c10f86066ebdf1490f8f013f67a228ad233c434ebd25eed94be37b8231f512adff5fae7324fea64db089d) 

## Version control guidelines
The version number of the project is in the form of x.x.x, where x is a number, starting from 0, and is not limited to the range 0~9. When the project is in the incubator phase, the version number is 0.x.x.

As the interfaces and annotations of Spring Boot 1 and Spring Boot 2 have been changed significantly in the Actuator module, and spring-cloud-commons is also changed quite a lot from 1.x.x to 2.0.0, we take the same version rule as SpringBoot version number.

* 1.5.x for Spring Boot 1.5.x
* 2.0.x for Spring Boot 2.0.x
* 2.1.x for Spring Boot 2.1.x
* 2.2.x for Spring Boot 2.2.x

## Code of Conduct
This project is a sub-project of Spring Cloud, it adheres to the Contributor Covenant [code of conduct](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046bb92d12e4c5b020779e917ba40822747bc61c8c995471a53eda6c434af2805dd6dbf543bf67eba0d1e1f6d4886a0d86e10d7c2ff1a513fe7d6aab4d8bdae270faed9374f3d7a7a2b6cead353ad4196382700dbe6a2ec98dd9f20c5791a4f76d4  By participating, you are expected to uphold this code. Please report unacceptable behavior to spring-code-of-conduct@pivotal.io.

## Code Conventions and Housekeeping
None of these is essential for a pull request, but they will all help. They can also be added after the original pull request but before a merge.

Use the Spring Framework code format conventions. If you use Eclipse you can import formatter settings using the eclipse-code-formatter.xml file from the Spring Cloud Build project. If using IntelliJ, you can use the Eclipse Code Formatter Plugin to import the same file.

Make sure all new .java files to have a simple Javadoc class comment with at least an @author tag identifying you, and preferably at least a paragraph on what the class is for.

Add the ASF license header comment to all new .java files (copy from existing files in the project)

Add yourself as an @author to the .java files that you modify substantially (more than cosmetic changes).

Add some Javadocs and, if you change the namespace, some XSD doc elements.

A few unit tests would help a lot as well — someone has to do it.

If no-one else is using your branch, please rebase it against the current master (or other target branch in the main project).

When writing a commit message please follow these conventions, if you are fixing an existing issue please add Fixes gh-XXXX at the end of the commit message (where XXXX is the issue number).

## Contact Us
Mailing list is recommended for discussing almost anything related to spring-cloud-alibaba. 

spring-cloud-alibaba@googlegroups.com:You can ask questions here if you encounter any problem when using or developing spring-cloud-alibaba.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)