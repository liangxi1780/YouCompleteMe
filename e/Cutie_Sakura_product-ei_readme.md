
![WSO2 Enterprise Integrator](gh-docs/images/wso2-integration-logo.png?raw=true)

[![Build Status][badge-travis-image]][badge-travis-url]
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://github.com/wso2/product-ei/blob/master/LICENSE)
[ ](http://u.720life.cn/g/ba16f9aac2448ab9a7db13f9be9132bd1603ec0e57dfa693b29ca2336f880a2a) 
[![Twitter](https://img.shields.io/twitter/follow/wso2.svg?style=social&label=Follow)](https://twitter.com/intent/follow?screen_name=wso2)

# WSO2 Enterprise Integrator

WSO2 Enterprise Integrator is an open source, fast, cloud native and scalable integration solution that is the core of 
WSO2 Integration Agile Platform. It enables enterprise integration developers to build sophisticated integration 
solutions to achieve digital agility. As a mature integration product since 2005, *(branded as WSO2 ESB at the time)*, it 
continues to be the most sophisticated and extensible open source enterprise integration solution available.

Actively maintained, with commercial support from WSO2 Inc, WSO2 Enterprise Integrator is widely used in production at 
companies around the globe starting from startups to fortune 500 companies in the fields of government, healthcare, 
banking, education, communication, etc.

[Installation](http://u.720life.cn/g/2e31f53e981d9e519174a6ca612639de8d7903dae717238d177eaa0979e2065a3fbd52877af9eb7fe791138d778f7594a5de08b1e9f2a06b03c8bdbb3020387e)  | 
[Documentation](http://u.720life.cn/g/2e31f53e981d9e519174a6ca612639de8d7903dae717238d177eaa0979e2065a6ee2a8913f211581419c9c44086a5b12)  | 
[Mailing Lists](http://u.720life.cn/g/9e610d5e36505d0cb67f287b8d6f8398d56c19892484bdeec462908b2bb59bca)  | 
[Blog](http://u.720life.cn/g/9e610d5e36505d0cb67f287b8d6f839887907c101c33121fd9e46c4a07950093678c2ec3cc8eebf30c1a5f20611823f7)  | 
[Support](http://u.720life.cn/g/9e610d5e36505d0cb67f287b8d6f8398a38826e2632dc6772c4fb59a667dec7a)  | 
[Nightly Builds](http://u.720life.cn/g/85a77d410b1c5793daa1101a6bf2e9a46cd7f6796a5117e42202411f02315ffa3c6301806bb5ac5be1765c020fca05afd86b40592b69b578f85b3c1b9112093fe0998559e3b2aa18d827b8ab18cb9391) 


## Outline 

- [**Why WSO2 Enterprise Integrator?**](#Why-WSO2-Enterprise-Integrator)
- [**Features**](#Features)
- [**Distributions**](#Distributions)
- [**Installation and Run**](#Installation-and-Run)
- [**Artifact Development**](#Artifact-Development)
- [**Building from Source**](#Building-from-Source)
- [**Enterprise Support**](#Enterprise-Support)
- [**Licence**](#License)


## Why WSO2 Enterprise Integrator

WSO2 Enterprise Integrator is an open source, hybrid integration platform. It is comprised of profiles that address different
parts of a complete integration story. 

**Enterprise Service Bus profile**: If you are trying to interconnect your enterprise applications on-premise, legacy 
  or cloud, WSO2 EI can act as a Service Bus. It can help transforming messages 
  to different formats, standards, use different protocols to communicate and mediating messages across the applications. 
  With 100+ ready made cloud connectors, intuitive tooling,  analytic capabilities WSO2 EI provides a greater agility to 
  meet growing and changing enterprise demands. It can also accelerate bringing your enterprise data to the screen by 
  exposing them as services, APIs.
 
**Message Broker profile**: This allows for queueing of messages (using the AMQP protocol) where you do not require an 
  immediate response to continue processing. WSO2 EI acts as a Message Broker server.  

**Business-process profile**: If your integration story contains human interactions (i.e., approval process) or stateful 
  integration/orchestration, WSO2 EI provides BPEL/BPMN and human task capabilities to develop work-flows.

**Analytics profile**: Provides time-based/count-based analytics, stats, and monetization capability at different points of 
  your integration flow implemented by combining the above profiles.    
  
All above aspects are seamlessly cross-supportive and, together, makes WSO2 EI a complete powerful middleware solution that
helps you to digitalize your business with more agility.

WSO2 EI has a **cloud native offering** as well named **[WSO2 Micro Integrator](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e0fa5f0948d3ed2982bfe9a271ff82fe68b6c7e58749954459fd06fcf8039bc6  that
enables developers implement composite microservices and integrate them. It contains a microservices friendly 
implementation of Enterprise Service Bus profile.

[![WSO2 Enterprise Integrator](gh-docs/images/wso2-ei-overview.png?raw=true "WSO2 Enterprise Integrator")](https://wso2.com/integration/features/)


## Features


- **Support for all EIP Patterns**: Integrate applications following 
  [standard enterprise integration patterns](http://u.720life.cn/g/dbf1195f8a53209e138d24666db06636fc9da0b92b63f16dad8a29f169e77d4ae8be3200107c597c22908549080e4560f371c0ebf66f1fa0298065e4fa88e250)  
- **Faster message mediation**: [Passthrough HTTP Transport](http://u.720life.cn/g/9e610d5e36505d0cb67f287b8d6f8398051b51a3defacba92e407cabdc0311d34f56f9e38569b104f3c4119a04211a07153ca0a0b4c0b0fc8c5206c3267bc8acbd4eadac954a0f81358c5970b8f2c77f23a60d74860f0d3bf78679910783f765)  
  for faster message mediation through WSO2 EI
- **Supports multiple transports/messaging standards**: Interconnect applications that support different 
  protocols (i.e., HTTP and JMS)
- **Supports numerous formats and protocols**: Interconnect applications that work with different message 
  formats (i.e., XML and Json)
- **As a gateway** : Front operations within the operations as a managed, secured proxy services/APIs.  
- **Offer QOS to services/APis**: Supports throttling, caching responses for faster mediation, circuit breaking, 
  applying security 
- **Secure enterprise**: Apply Oauth 2.0, Saml SSO, Keberos for services/APIs. WS-security support for proxy services 
- **Service orchestration**: Enable to interconnect a set of APIs and web services and expose them as a single API or 
  a web service 
- **Database integration**: Enable to expose data as services and APIs, stream data and listen for data changes and 
  trigger events 
- **Handle many concurrent HTTP(S) connections**: Ability to serve multiple HTTP connections concurrently using 
  reactor pattern and Java NIO
- **Event publishing, logging and auditing**: Server logs, audit logs, trace logs with information of executions within 
  server to different levels and ability to integrate with popular log analytic software 
- **185+ connectors**: Connecting Web APIs / Cloud services with on-premise enterprise applications
- **Expose enterprise data as APIs/Services**: Use data services to expose queries/stored procedures as  APIs/Services. 
  Transactions supported. 
- **Visual data mapping**: Map input data formats to output data formats visually, flexibility to change 
  message structure within enterprise is never made easier
- **Guaranteed delivery of messages**: WSO2 EI is configurable with message broker profile (OOB) and with any JMS 
  broker to construct asynchronous messaging patterns with GD.  
- **Periodic task execution**: Execute a periodic task, invoke a message flow periodically, handle a bulk load at 
  off peak time. 
- **Connecting with Packaged applications**: Integration with systems like SAP
- **Business processes and human tasks**: Ability to handle message flows those involves a human 
  interaction, approval process in a standard manner.
- **Data analytic, monetization capabilities**: Ability to measure number of hits to APIs/proxies, geographic 
  information, know what is used most by your users. 

For more about WSO2 EI extension points visit [here](http://u.720life.cn/g/9e610d5e36505d0cb67f287b8d6f8398051b51a3defacba92e407cabdc0311d3405c02c717469ce9c1b01d2e84c054373f3f6a153f9a3cf6094259699f769dda41bd8c416b42d7da25aed0fb64b8d6965df4ed8d0dd12566c83b49bce8ed94e55ecb43b1689d407ff1e86730b40a3fe564e1d1110a7672c4b37e1031f9c60d96  Please 
find the full available connectors at [WSO2 Store](http://u.720life.cn/g/b94a0cf0570d56d769174c6ebd3136b52c4037fefc8f0672a38e597688da8ea7861b61bef6f8096d7396b4aee1c997ef142c01ad3ee0405b954ee67cc8683f76 


## Distributions

WSO2 EI is packaged in several forms for different platforms and environments. However, the bare metal form is the Binary Zip file:

- [WSO2 EI Zip](http://u.720life.cn/g/9e610d5e36505d0cb67f287b8d6f8398da30dbd3ef61d6c0b0bc095fa49c6c218d49b1617a5b62639aa4855a66047438  Works on any platform, just unzip and run 


|Platform                 |  OS                  | Infrastructure Mgt  |
|-------------------------|----------------------|---------------------|
|[WSO2 EI AWS CloudFormation](http://u.720life.cn/g/9e610d5e36505d0cb67f287b8d6f8398da30dbd3ef61d6c0b0bc095fa49c6c21edabcc8448ee50c7021b22c06a9715a532daf6bf43861a428cecf854dad84b2c)  |[WSO2 EI installer](http://u.720life.cn/g/9e610d5e36505d0cb67f287b8d6f8398da30dbd3ef61d6c0b0bc095fa49c6c21f770332b204c4ca665acd5e4dce97e38692d693d1b93a61dcec09a4e5e9bbdce)  for Windows  |[WSO2 EI Puppet Install](http://u.720life.cn/g/9e610d5e36505d0cb67f287b8d6f8398da30dbd3ef61d6c0b0bc095fa49c6c214e74e583a53358f4845f045f7f88868e)    |
|[WSO2 EI Kubernetes](http://u.720life.cn/g/9e610d5e36505d0cb67f287b8d6f8398da30dbd3ef61d6c0b0bc095fa49c6c214de8da5e0d0aa97532cd0ff8b5f8a1733ed45d82ccd557e5d49f6c71bc945195486434f2085e0b9ec2bf5b236439bd04)   |[WSO2 EI installer](http://u.720life.cn/g/9e610d5e36505d0cb67f287b8d6f8398da30dbd3ef61d6c0b0bc095fa49c6c21f770332b204c4ca665acd5e4dce97e388ccb900a690232af97a720b18580b29c)  for Mac        |[WSO2 EI Ansible Install](http://u.720life.cn/g/9e610d5e36505d0cb67f287b8d6f8398da30dbd3ef61d6c0b0bc095fa49c6c2187b70dd92b25a24354c5775666e74bf7)  |
|[WSO2 EI Docker](http://u.720life.cn/g/9e610d5e36505d0cb67f287b8d6f8398da30dbd3ef61d6c0b0bc095fa49c6c219b3c05eaf632678a30995248d97519e4516e3e396f297c5d23c90ef0685c88137353d158d5150acde51c4be0059b4127)           |[WSO2 EI installer](http://u.720life.cn/g/9e610d5e36505d0cb67f287b8d6f8398da30dbd3ef61d6c0b0bc095fa49c6c21f770332b204c4ca665acd5e4dce97e3882228fb009aa856eb562058fecc8a08d)  for Ubuntu  |   |
|[WSO2 EI Vagrant](http://u.720life.cn/g/9e610d5e36505d0cb67f287b8d6f8398da30dbd3ef61d6c0b0bc095fa49c6c2182faaa012517300eb874eb8ffb56cc786260fe2c1f5c7a537900af64697263e154d65ffb138b377f17ef5f6705c81725)         |[WSO2 EI installer](http://u.720life.cn/g/9e610d5e36505d0cb67f287b8d6f8398da30dbd3ef61d6c0b0bc095fa49c6c21f770332b204c4ca665acd5e4dce97e387a602a9bb36df1d7376a71adfe1179a2)  for CentOS  |   |
|[WSO2 EI Helm](http://u.720life.cn/g/9e610d5e36505d0cb67f287b8d6f8398da30dbd3ef61d6c0b0bc095fa49c6c210b15a9a5604dd25568ee2117f8d8f5db08f27bed1a9b5b2426438a47a5bdd61d)               |   |   |
|[WSO2 EI YUM Install](http://u.720life.cn/g/9e610d5e36505d0cb67f287b8d6f8398da30dbd3ef61d6c0b0bc095fa49c6c2190cfb38f47be637b5cc45a8006030453c8591b23351fa123361dba6cb462a595)                     |   |   |
|[WSO2 EI Brew Install](http://u.720life.cn/g/9e610d5e36505d0cb67f287b8d6f8398da30dbd3ef61d6c0b0bc095fa49c6c21fd99b04bbc7612c8056dca0e854dfe40c0ee771ea270818d3cb40c5fd8f04e3f)                   |   |   |
|[WSO2 EI Apt Install](http://u.720life.cn/g/9e610d5e36505d0cb67f287b8d6f8398da30dbd3ef61d6c0b0bc095fa49c6c212715bc17c69d4fa6b185fc7ae4383b8ac26313b09161909241bece9719750caf)                     |   |   |

- [WSO2 Micro Integrator](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e0fa5f0948d3ed2982bfe9a271ff82fe7c71f4c6a8efd3b2e5ce13fdeca54f96)  is the cloud-native offering of WSO2 EI. It is a 
  configuration driven runtime that helps developers implement composite microservices. 

## Installation and Run

Extract wso2ei-x.x.x.zip and navigate to extracted directory/bin. From there, start the preferred profile. 
After started, Management console will be accessible for the profile started. 
Use username:*admin* and password:*admin* to access the console.

| Profile            | Web Console Url                       |
| ------------------ | --------------------------------------|
| `Integrator (ESB)` | https://localhost:9443/carbon         |
| `Broker`           | https://localhost:9446/carbon         |
| `Business process` | https://localhost:9445/carbon         |
| `Analytics`        | https://localhost:9643/portal         |

All open issues pertaining to WSO2 Enterprise Integrator are reported at the following location: 
[known issues](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461bed72f7784e16e04f9333f5aee10103e032054e93eccb80dddbc9dd9605a859) 


## Artifact Development

Use WSO2 EI tooling for artifact development to be deployed and run on WSO2 EI. It is a powerful, visual editor for 
developing WSO2 EI integration artifacts that enables you to structure the whole enterprise integration solution to a 
single project and export it as a single deployable unit. A team can push the project on GitHub and collaboratively 
work on developing integration flows. 

Read on how to develop integration artifacts with EI tooling [here](http://u.720life.cn/g/2e31f53e981d9e519174a6ca612639de8d7903dae717238d177eaa0979e2065a27f70115f28ddb64a7e30b5c9566eb981b70eaedba2e121f53c53c25d13141f5 

#### Test Artifacts in the Enterprise Integrator
WSO2 Enterprise Integrator allows you to execute unit tests against your integration artifacts by using [Synapse Unit Testing Framework](gh-docs/synapse-unit-testing-framework/synapse-unit-testing-framework.md). 

## Building from Source

If you intend to build the project from the source you can do that with or without building the dependent projects. 
Here is an outline how the dependent project are structured. If you build with dependencies, you need to do it from 
bottom to top in the hierarchy.

![WSO2 EI-Repositories](gh-docs/images/ei-repo-structure.png?raw=true)

Repositories referred above

- [product EI](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461bed72f7784e16e04f9333f5aee10103a02163b2f84368dc14332904bb338a6c  contains product EI packaging. 
- [carbon-mediation](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a1457ca5080c349497866db0935383cf26616c726deb7a04ae50cbb50ba6cfb6  mediation features related to WSO2 ESB are developed in this repository. 
- [carbon-data](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465697e51f44ffbe15769385ff1ca904decc316341ef225e11c3710c3695793363  contains features related to data services. 
- [wso2-synapse](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467bbbb823b6d93071b232895ad1b6c0b4d59cb881804ed1c644c84a43f029d136  source of messaging engine used by the WSO2 EI runtime. 
- [carbon-business-messaging](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f68a34aeaee23c5b25adde836c45587e7a8983da513fed6a585805f88412fff1cb76063aa0f3396d642b6be16f958aec  features related to WSO2 Message Broker profile. 
- [andes](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469ea8d2cdfeb0ddd97bdf0dd7e6ef39f8  implementation of messaging core of WSO2 Message Broker profile. 
- [carbon-business-process](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f68a34aeaee23c5b25adde836c45587e2eac1679223834b1638658a9a9eebbece48fbcc0d5f505918e68a575c86123e5  contains the modules implementing BPEL , 
  WS-Human Tasks and BPMN support for WSO2 EI's business process profile.
- [wso2-ode](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c7a80f835700fc0240d26dba6afd91224fca04e14b16c013970cb5616d1c402e  WS-BPEL compliant web services orchestration engine.
- [carbon Commons](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e03d434f52abd3e2301994a70dda17bcc2b936de6f6b832470b053ed2f116fe8  contains the common components to Carbon (i.e., cluster mgt, logging, ntask). 
- [WSO2 Axis2 Transports](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046dd6562473d4051e92025eddb085087d08ca15ea0361fdd285ace6703d954da1c  includes the axis2 based transport 
  implementations (i.e., JMS, Mail, message builders, formatters). 
- [carbon Kernel (4.x.x)](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304662504f57ea3e02ec5b5aa82bc4b6878d876cf51aa45dac4941c7ca09e234e172c62089e41401ed47f268fc017deb9898  lean, modular, OSGi-based platform. 
  This is the base of the WSO2 Carbon platform and is a server software development platform. 
- [wso2-axis2](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046dd6562473d4051e92025eddb085087d001b0865d99d4313af406f77f4e657b26  is a Web Services / SOAP / WSDL engine. Forked from [Apache Axis2](http://u.720life.cn/g/211f3b37683d68ec0f60d14fcce77fcce11fa1272af90b67a100d2c06bb94d425ae4ad77fc5c199e447e422b3efd8490  
- [carbon Analytics](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466a095dcd08585cd941d187c99f8be2c0ef49f2855987754d2b47e6c71c4df8c5  contains components related to WSO2 Stream Processor. 
- [carbon event processing](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467ad14d03d10a562e6bc1b3ee7b3004adbca2e3893b636ceaf49c3b1cd75689da0909455be276ad572acd3f4c855753e4  realtime event processing functionalities 
  used in WSO2 analytics platform. 
- [carbon analytics](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466a095dcd08585cd941d187c99f8be2c0ef49f2855987754d2b47e6c71c4df8c5  common functionalities used in WSO2 analytics platform. 
- [carbon dashboards](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465697e51f44ffbe15769385ff1ca904dea371dd354cc55323c94e3cc1f1ae7a3b  APIs and UI components related to analytic dashboards. 
- [carbon analytics commons](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466a095dcd08585cd941d187c99f8be2c07486d89d64b6ca10bd7d62f63c07ff2e33dd4632ff13ffb440fc30f6ca1ec497  implements common functionalities used 
  in WSO2 analytics platform. 
- [siddhi-io.*  repos](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e73eea740dd7d1f1a31b6ca7fc13a1ed651f01c30d92984bd5561bed0a2a1bfb  contains repos that contribute to transport layer of analytics. 
- [carbon Kernel (5.x.x)](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304662504f57ea3e02ec5b5aa82bc4b6878d4a7ee839f87bf8650dd0c9835e3c8acb  

## Enterprise Support

Enterprise support for WSO2 EI is provided by WSO2. Learn more [here](http://u.720life.cn/g/9e610d5e36505d0cb67f287b8d6f83987adc2174de47d8e1967958e38c3c8331 

## License

```
Copyright (c) 2019, WSO2 Inc. (http://u.720life.cn/g/5c06be2823532e2a5d601695704055042cad7fb43dca46a3ef10596b75860c59)  All Rights Reserved.

WSO2 Inc. licenses this file to you under the Apache License,
Version 2.0 (the "License"); you may not use this file except
in compliance with the License.
You may obtain a copy of the License at

  http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an
"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
KIND, either express or implied. See the License for the
specific language governing permissions and limitations
under the License.
```
 
[badge-travis-image]: https://wso2.org/jenkins/job/products/job/product-ei/badge/icon
[badge-travis-url]: https://wso2.org/jenkins/job/products/job/product-ei
















 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)