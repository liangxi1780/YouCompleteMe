

![Pinpoint](web/src/main/webapp/images/logo.png)

[![Build Status](https://travis-ci.org/naver/pinpoint.svg?branch=master)](https://travis-ci.org/naver/pinpoint)
[![codecov](https://codecov.io/gh/naver/pinpoint/branch/master/graph/badge.svg)](https://codecov.io/gh/naver/pinpoint)

**Visit [our official web site](http://u.720life.cn/g/de30f15857fd1c9a973e226d01bd8c900f1b8ae07cb8622dcae0b924b123c1c3)  for more information and [Latest updates on Pinpoint](http://u.720life.cn/g/42e71941bd31e4a590c9d906ef6fdabdc42f158869348a8beb9d5d5b1d80adc904030dad7b9cc707e3bc2a0b341443a3   

## Latest Release (2018/08/13)
We're happy to announce the release of Pinpoint v1.8.0-RC1.
Please check the release note at (http://u.720life.cn/g/54145d0471d91890860f7f8463c030465c915df3eccae484d494bb8989515ebf4d652696f44de229580562ee4f20a36e5840d728c7c63d493a5cbe395d105ea0 

The current stable version is [v1.7.3](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465c915df3eccae484d494bb8989515ebf4d652696f44de229580562ee4f20a36e9859d0aef7220f842a6f0af4a122fea9 

**Pinpoint** is an APM (Application Performance Management) tool for large-scale distributed systems written in Java. Inspired by [Dapper](http://u.720life.cn/g/34e2e041e0a09d204ff62d1d75406c00309c65f46aac80b52bb829aec40806fb096d50830fa555a0f1c400f7f1529bba  "Google Dapper"), Pinpoint provides a solution to help analyze the overall structure of the system and how components within them are interconnected by tracing transactions across distributed applications.

You should definitely check **Pinpoint** out If you want to

* understand your *[application topology](http://u.720life.cn/g/42e71941bd31e4a590c9d906ef6fdabdc42f158869348a8beb9d5d5b1d80adc9bf28c6b196b4734e78b619d742027fc985bdb26fcaef64cb45abaff37c865fe4  at a glance
* monitor your application in *Real-Time*
* gain *code-level visibility* to every transaction
* install APM Agents *without changing a single line of code*
* have minimal impact on the performance (approximately 3% increase in resource usage)

## Getting Started
 * [Quick-start guide](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465c915df3eccae484d494bb8989515ebf65f62163005578de223a5ac707e2612f62c03e82f69cc436737656b69618a1c5)  for simple test run of Pinpoint
 * [Installation guide](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465c915df3eccae484d494bb8989515ebfa51af3a5ee79c9bb3566c7693711563ed378b4c416ff730948e2b650c94bece9c10e09fe5dfdd7e5ae17df65a366d97b)  for further instructions.
 
## Overview
Services nowadays often consist of many different components, communicating amongst themselves as well as making API calls to external services. How each and every transaction gets executed is often left as a blackbox. Pinpoint traces transaction flows between these components and provides a clear view to identify problem areas and potential bottlenecks. 
For a more intimate guide, please check out our *[Introduction to Pinpoint](http://u.720life.cn/g/de30f15857fd1c9a973e226d01bd8c900f1b8ae07cb8622dcae0b924b123c1c3dcf2134fc1e72ecf4def4bc61549aaaaa4032e7a47caf93261743137d92d938d  video clip.

* **ServerMap** - Understand the topology of any distributed systems by visualizing how their components are interconnected. Clicking on a node reveals details about the component, such as its current status, and transaction count.
* **Realtime Active Thread Chart** - Monitor active threads inside applications in real-time.
* **Request/Response Scatter Chart** - Visualize request count and response patterns over time to identify potential problems. Transactions can be selected for additional detail by **dragging over the chart**.

  ![Server Map](doc/images/ss_server-map.png)

* **CallStack** - Gain code-level visibility to every transaction in a distributed environment, identifying bottlenecks and points of failure in a single view.

  ![Call Stack](doc/images/ss_call-stack.png)

* **Inspector** - View additional details on the application such as CPU usage, Memory/Garbage Collection, TPS, and JVM arguments.

  ![Inspector](doc/images/ss_inspector.png)

## Supported Modules
* JDK 6+
* Tomcat 6/7/8, [Jetty 8/9](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465c915df3eccae484d494bb8989515ebf29f61af147ffeb9c7b950d3c4f87732d7d50065dd0f0ffe2cc4003ed2585cbdb  [JBoss EAP 6](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465c915df3eccae484d494bb8989515ebf29f61af147ffeb9c7b950d3c4f87732d4399e90099dd6aded0427ea3c984d7f9  [Resin 4](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465c915df3eccae484d494bb8989515ebf29f61af147ffeb9c7b950d3c4f87732d54b7d547308c64848fcf5ce7e24017d9  [Websphere 6/7/8](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465c915df3eccae484d494bb8989515ebf29f61af147ffeb9c7b950d3c4f87732d52767e797b732dad11034584ab7454474d66a9c2f090076f5c43459781af673f  [Vertx 3.3/3.4/3.5](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465c915df3eccae484d494bb8989515ebf29f61af147ffeb9c7b950d3c4f87732d7bcb62a1f7c5d8d9d0e603e11cbe181d) 
* Spring, Spring Boot (Embedded Tomcat, Jetty)
* Apache HTTP Client 3.x/4.x, JDK HttpConnector, GoogleHttpClient, OkHttpClient, NingAsyncHttpClient
* Thrift Client, Thrift Service, DUBBO PROVIDER, DUBBO CONSUMER
* ActiveMQ, RabbitMQ
* MySQL, Oracle, MSSQL, CUBRID,POSTGRESQL, MARIA
* Arcus, Memcached, Redis, CASSANDRA
* iBATIS, MyBatis
* DBCP, DBCP2, HIKARICP
* gson, Jackson, Json Lib
* log4j, Logback

## Compatibility

Java version required to run Pinpoint:

Pinpoint Version | Agent | Collector | Web
---------------- | ----- | --------- | ---
1.0.x | 6-8 | 6+ | 6+
1.1.x | 6-8 | 7+ | 7+
1.5.x | 6-8 | 7+ | 7+
1.6.x | 6-8 | 7+ | 7+
1.7.x | 6-8 | 8+ | 8+
1.8.x | 6-8  9+(Experimental) | 8+ | 8+ 

HBase compatibility table:

Pinpoint Version | HBase 0.94.x | HBase 0.98.x | HBase 1.0.x | HBase 1.1.x | HBase 1.2.x
---------------- | ------------ | ------------ | ----------- | ----------- | -----------
1.0.x | yes | no | no | no | no
1.1.x | no | not tested | yes | not tested | not tested
1.5.x | no | not tested | yes | not tested | not tested
1.6.x | no | not tested | not tested | not tested | yes
1.7.x | no | not tested | not tested | not tested | yes
1.8.x | no | not tested | not tested | not tested | yes

Agent - Collector compatibility table:

Agent Version | Collector 1.0.x | Collector 1.1.x | Collector 1.5.x | Collector 1.6.x | Collector 1.7.x | Collector 1.8.x
------------- | --------------- | --------------- | --------------- | --------------- | --------------- | ---------------
1.0.x | yes | yes | yes | yes | yes | yes
1.1.x | not tested | yes | yes | yes | yes | yes
1.5.x | no | no | yes | yes | yes | yes
1.6.x | no | no | not tested | yes | yes | yes
1.7.x | no | no | no | no | yes | yes
1.8.x | no | no | no | no | no | yes

Flink compatibility table:

Pinpoint Version | flink 1.3.X | flink 1.4.X
---------------- | ----------- | ----------- 
1.7.x | yes | no |

## User Group
For Q/A and discussion [here](http://u.720life.cn/g/941693b557d072bb769494a6a61fcd979ee9fee4d4fd0c2a6b8a30bc68eade2171beab61c77927d277a05f9945bc1ceb60741d400d7320a0958fb6e8f9b69dc0 

## License
Pinpoint is licensed under the Apache License, Version 2.0.
See [LICENSE](LICENSE) for full license text.

```
Copyright 2018 NAVER Corp.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)