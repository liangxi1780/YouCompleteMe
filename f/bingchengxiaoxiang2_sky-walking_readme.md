Apache SkyWalking | [中文](README_ZH.md)
==========

 

**SkyWalking**: APM (application performance monitor) tool for distributed systems, especially designed for 
microservices, cloud native and container-based (Docker, K8s, Mesos) architectures.
Underlying technology is a distributed tracing system.

[![GitHub stars](https://img.shields.io/github/stars/apache/incubator-skywalking.svg?style=for-the-badge&label=Stars&logo=github)](https://github.com/apache/incubator-skywalking)
[![Twitter Follow](https://img.shields.io/twitter/follow/asfskywalking.svg?style=for-the-badge&label=Follow&logo=twitter)](https://twitter.com/AsfSkyWalking)

[![Build Status](https://travis-ci.org/apache/incubator-skywalking.svg?branch=master)](https://travis-ci.org/apache/incubator-skywalking)
[![Join the chat at https://gitter.im/sky-walking/Lobby](https://badges.gitter.im/openskywalking/Lobby.svg)](https://gitter.im/openskywalking/Lobby)
[![OpenTracing-1.x Badge](https://img.shields.io/badge/OpenTracing--1.x-enabled-blue.svg)](http://opentracing.io)

* Provide Java agent, **no need to CHANGE any application source code**.
  * High performance agent. Only increase extra **10%** cpu cost in 5000+ tps application, even **when collect all traces**.
  * [Supported middlewares, frameworks and libraries](docs/Supported-list.md).
* Manual instrumentation
  * As an [OpenTracing supported tracer](http://u.720life.cn/g/5f14984dfd144c88331f86c5d98ff48a11a287f46e5050460b7560a9e5476e3cb1c5bd122aa4cc9a9416dc930cc5d8b770f15071427d7df20d8dedd06a43c1d9) 
  * Use **@Trace** annotation for any methods you want to trace.
  * Integrate traceId into logs for log4j, log4j2 and logback.
* Pure Java server implementation, provide RESTful and gRPC services. Compatibility with other language agents/SDKs. 
* The UI released on [skywalking-ui](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c0001bca31ae58bae1a9ea2d5840c8aa3249350502098fa87888b8e15a4e5ce7297adfc215228cfaf6a88d797ba8d8f7) 

# Document
[![EN doc](https://img.shields.io/badge/document-English-blue.svg)](docs/README.md) [![cn doc](https://img.shields.io/badge/文档-中文版-blue.svg)](docs/README_ZH.md)

# 5.x Architecture
 

# Code of conduct
This project adheres to the Contributor Covenant [code of conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior to wusheng@apache.org.

# Screenshots
- Discovery topological graph of application clusters automatically.
 

- Trace query.
 

- Span detail.
 

- Instance Overview.
 

- JVM Detail.
 

- Services Dependency Tree.
 

# Test reports
- Automatic integration test reports
  - [Java Agent test report](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462a3cc85fbfbac0e259af0e3e6c2a229d0f13b69738fa0ab0adfec06fea0e8b41f46b5486e75363f4fb192f075034a7dd) 
- Performance test reports
  - [Java Agent test report](http://u.720life.cn/g/24baa8521d1e383b793fb66b5f35acf12d249dd4c315cf22fb9ffcb24ddeaae1c05bd24abdada8d9bfc287c26c4e344df6d5f7b9619e436d9a19fd27db99aa5a) 

# Contact Us
* Submit an issue
* [Gitter](http://u.720life.cn/g/11e95d0ed8d2826912e12fe1dc3f3421ed1d6771376d16283890b4e733ec44057ff17893ae1e32fac8260a7b4cffc965) 
* QQ Group: 392443393

# License
[Apache 2.0 License.](/LICENSE)



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)