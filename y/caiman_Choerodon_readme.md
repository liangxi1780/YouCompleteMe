# Choerodon

![](img/choerodon-community.png)

Choerodon is an open source enterprise service platform based on container orchestration and management capabilities of [Kubernetes](http://u.720life.cn/g/a71d35e8f2866b1c793c4c27d2959365dd7045b9407ddde93f2ff9f9329e582c  It integrates the tool chain of DevOps, microservices, and mobile application framework to help companies achieve Scrum application delivery and automated operations management, and provide business components such as IoT, payment, data, smart insight, and enterprise application market to help companies focus on business and accelerate digital transformation.

Choerodon provides:

- A comprehensive tool chain supporting DevOps best practices, supporting Scrum management from planning, programming, building, testing, publishing, and operations.

- A suite of Spring Cloud-based microservice application frameworks to help companies become faster and more efficient for microservice development.
    
## The feature of Choerodon 
  
- **Agile** - Choerodon provides a set of tools to help users manage the flow of user value in an agile manner which consists of story map, user story, sprint, kanban.

- [**Development Pipeline**](http://u.720life.cn/g/8e0aac0efc6ea2c26ba2df94a029365ffca4e14ed1ebb76de5376f5c70db25a33b928323084d1bed18e9ecb98b3d7f3d04983d96f73bd396c136dd5edf2d34f2)  - Guided by the concept of DevOps, using Gitlab-CI as a continuous integration tool, combined with the Gitflow branch management model to provide continuous integration of the pipeline.
 
- [**Deployment Pipeline**](http://u.720life.cn/g/8e0aac0efc6ea2c26ba2df94a029365ffca4e14ed1ebb76de5376f5c70db25a34b1f88593b34bf549648549e0f4dc402)  - With the help of the Choerodon, users can easily manage a variety of application services that use the development and deployment of Choerodon.

- [**Operation Management**](http://u.720life.cn/g/8e0aac0efc6ea2c26ba2df94a029365ffca4e14ed1ebb76de5376f5c70db25a3a945bbf9a33e98520e403a9e5c2ef5e3d1df727f2d50bb37fb0a504c88237375)  - Choerodon provides a complete set of operational management tools to monitor development indicators, server logs, application system logs, and micro service call chains.

- [**Microservice Development**](http://u.720life.cn/g/8e0aac0efc6ea2c26ba2df94a029365f982dc38d0015510a33607707e81d58022e2913b8831f80f92164be1a974153a7)  - Choerodon provides a complete microservice development framework of Spring Cloud-based,with this development framework user can easily build application services.

Also, you can view the [screenshots of Choerodon](SCREENSHOT.md) to have a most intuitive understanding of Choerodon, and you can visit the website of Choerodon [choerodon.io](http://u.720life.cn/g/8e0aac0efc6ea2c26ba2df94a029365f5ffd6882c983cc8f86acf30389d45374) 

## Installation
 
Please follow [the documentation of installation](http://u.720life.cn/g/8e0aac0efc6ea2c26ba2df94a029365f0c3b8d4bf71de27e1064f6a5e637ebfc8db9b39291aec070201bed901261edc9e339bb8b9179715042bedc58d3517c40)  to install Choerodon.

## To start using Choerodon

To get started with Choerodon, please read the [Quick Start Guide](http://u.720life.cn/g/8e0aac0efc6ea2c26ba2df94a029365f716ef952f2472e42478f9242a7dd3a6892e7a2676db8e747e3b2b47651c7e5a5 

For operation manual, please read the documentation [choerodon.io](http://u.720life.cn/g/8e0aac0efc6ea2c26ba2df94a029365ffca4e14ed1ebb76de5376f5c70db25a394ad52076f51f8d5b9efe5d1c79a1c4c 

## To start developing with Choerodon

There are two parties, **microservice backend** and **frontend**, in Choerodon microservice development framework.


If you want to develop microservice backend, please refer to the   [microservices developer's documentation](http://u.720life.cn/g/8e0aac0efc6ea2c26ba2df94a029365f982dc38d0015510a33607707e81d5802d393b42c38c702fe5c50a9c1c91bbd350c0853e6c40ecd20c6957d3d413bf0d6 


Also, with the help of [frontend developer's documentation](http://u.720life.cn/g/8e0aac0efc6ea2c26ba2df94a029365f982dc38d0015510a33607707e81d5802e998fe9b1b02a00cd3b1bfe10572e710c4b2b5ef85af9ca15d89b9f42c802a59)  , you can use the Choerodon`s frontend style.

## The components of Choerodon

This repository contains the source code for Choerodon documentation. If you're looking for individual components, they live in their own repositories.

- [choerodon-starter](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdd76ad5579285ec92738d61cb860b7990506f36351f2543f5da73bb53dfaf15dc271393a8fd5db7a1092ade27461c)  - The is the toolkit developed by Choerodon and provides some basic dependency for use in the development process.
- [choerodon-framework](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdd76ad5579285ec92738d61cb860bea5b0c6d43cf8e8c83eeb63a7e38e24dff2832544c28ba2d326ae79d8ee18114)  - The is the Choerodon Microservices Framework.
- [go-register-server](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463948aef6e288adead988b88848dedd720f71e9455090dca23121bf8f8b95ef770b8dfd1cc1a642dbcbbebfbd554a92d6)  - The microservice registration center is implemented in the go language, by tightly integrating the kubinertes, the microservice registration is implemented by monitoring the state changes of the k8s pod, and pull the interface in the spring cloud eureka client service list.
- [api-gateway](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465d3eac7e2b3697585db52b01776c607acab298e2c6d823d615263cdf0de7c850)  - Choerodon's gateway service is responsible for routing requests to real services. 
- [register-server](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463948aef6e288adead988b88848dedd720f71e9455090dca23121bf8f8b95ef770b8dfd1cc1a642dbcbbebfbd554a92d6)   - The microservice registration is implemented by monitoring the state changes of the k8s pod, and pull the interface in the spring cloud eureka client service list.
- [config-server](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304643e753b25a8bbb0f16e3792880261990589a37439c3fa0594833338563e4a9b1)  - Choerodon's configuration service is the configuration center for unified management of service configuration files.
- [manager-service](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462d68035cff6b39abcb59b65bbf44cd6fc4d735f39cad0b10db531e186392ddb4)  - This service is the management center of the choerodon microservices framework. Its main functions include configuration management, route management, and swagger management.
- [gateway-helper](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046cb9b07b15035951c6a62fa016de9fce233ef03401a95326e93d336219cefa308)  - Authenticating and limiting the requests from api-gateway, create JWT and return to api-gateway.
- [oauth-server](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304640d6185684dff4839c229a8ba1ca7dc292e53e561efb6124d5c5465b6c485d6e)  - This service is the authorized authentication center of the choerodon microservices framework and is mainly responsible for user privilege and authorization.
- [eureka-server](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046bae92da5059798f50af2a9dea494ff62e11da0abcfd83717dfcb6a983936214a)  - Locally initiated registration services. Eureka registration center, for local testing only, please using go-register-server if you are online. The API send the message of server starting to "register-server" topic of kafka, after receiving the message, manager-service do the corresponding processing, such as refresh permissions.
- [iam-service](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b1e62f63bbc742b460fc9f6cb322576ac440075a21b834ffbc1f9e944e8aa40d)  - With management functions of user, role, permission, organization, project, password policy, fast code, client, menu, icon, multi-language , and support for importing third-party users through idap.
- [event-store-service](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469630318df22e44e080a095d5096fed500d4b90a46bdab49f9223700603b3e4660e28b6f08ff74658233bba6c5e3f8248)  - Event-store-service for data consistency support. It is necessary to cooperate with choerodon-starter-event-producer and choerodon-starter-event-consumer to implement data consistency. Currently, the message queue kafka is supported.
- [file-service](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b73cc7da32a5403f9ab5e11285b2fec122a54d86f0f7998726e03d2b2491c860)  - The file service is built on minio server, we can use minio client to upload and delete files.
- [hystrix-turbine](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b7624da25d3e4e4fdd6619a857c899c3aa1b282f1b8fcb26505ec99b5782a1a1)  - Hystrix Turbine integrates each service's data of Hystrix Dashboard. The use of Hystrix Turbine is very simple and requires only the introduction of appropriate dependencies, annotations and configurations.
- [hystrix-dashboard](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b7624da25d3e4e4fdd6619a857c899c35d60ea569c24469050011a7ffe0f024aeea93f15494e92af0b9f4fedf77130f4)  - Hystrix Dashboard is a dashboard component of Hystrix. It is mainly used to monitor Hystrix's index information in real time. Information fed back through the interface can quickly discover problems in the system.
- [choerodon-ui](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdd76ad5579285ec92738d61cb860b6ecea8aa65e98641102f01289843a1f1)  - An enterprise-class UI design language and React-based implementation.
- [choerodon-front](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdd76ad5579285ec92738d61cb860bcec60566e830e904a843faebc6aa4fde)  - The project is an overall front-end project that combines Choerodon iam and Choerodon devops.
- [choerodon-front-boot](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdd76ad5579285ec92738d61cb860bc100792d9d4f2d1bac5698b58cdbbe280677cd52d3ad2af1f8e638540a48041c)  - Front end package management, startup, compilation.
- [choerodon-front-iam](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdd76ad5579285ec92738d61cb860b0052bac36f5f08ba55cbfb6f621b42e4a6c510d7ee9f5ad360cf4ff42b6c7d78)  - The project is an overall front-end project that combines Choerodon Boot and Choerodon iam.
- [choerodon-front-devops](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdd76ad5579285ec92738d61cb860b98b1974cdbf6e8e782b24336ceb1dc6654f9567c642308d7c90d9d305ec16c77)  - DevOps Front is the core front service of Choerodon. The service is responsible for all front pages of continuous delivery and providing users with a better user experience through rich display.
- [devops-service](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c6514ccfa86319143fe7674296e962bc6c7fd77364c9577cea3806efca5cf8a6)  - DevOps Service is the core service of Choerodon. Integrated several open source tools to automate the process of planning, coding, building, testing, and deployment, operation, monitoring.
- [gitlab-service](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304660164982a777f952093487e71859637ce0d38f14a11aa4fd76878929033b9386)  - Gitlab Service is responsible for establishing communication with GitLab, handling GitLab related logic and forwarding it to other services.
- [choerodon-agent](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdd76ad5579285ec92738d61cb860b8094aed1aa100bdd282143430daf8270)  - The environment client connects to the choerodon platform through websocket.

- [zipkin-ui](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460d93545dc8c2f812c1f9729174de7c4868799e8a5ba08bb8910f57e785028d5f)  - zipkin UI Application.
- [zipkin-collector](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460d93545dc8c2f812c1f9729174de7c48bbd53074c776c134b099a9be72a57e12146cf4d6df401804969fca634b0654ff)  - Zipkin Call chain collector. Read the Zipkin call information from the Kafka, store the call information in the Elasticsearch, and facilitate the Zipkin front-end display.



## Contribute

We welcome your input! If you have feedback, please [submit an issue](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610fdd76ad5579285ec92738d61cb860bfdb04c8d9d887546420d70c00612af67  If you'd like to participate in development, please read the [documentation of contribution](CONTRIBUTING.md) and submit a pull request.

## Support

If you have any questions and need our support, [reach out to us one way or another](http://u.720life.cn/g/8e0aac0efc6ea2c26ba2df94a029365f2a4bde326c092f1ff0753f6d5a2bf45c81a028325cf00188b29ae5060615407d 




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)