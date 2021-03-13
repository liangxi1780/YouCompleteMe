[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) [![CodeStyle](https://img.shields.io/badge/Check%20Style-Google-brightgreen)](https://checkstyle.sourceforge.io/google_style.html) [![Pinpoint Satellite](https://img.shields.io/endpoint?url=https%3A%2F%2Fscan.sbrella.com%2Fadmin%2Fapi%2Fv1%2Fpinpoint%2Fshield%2FFederatedAI%2FFATE)](https://github.com/mmyjona/FATE-Serving/pulls) [![Style](https://img.shields.io/badge/Check%20Style-Black-black)](https://checkstyle.sourceforge.io/google_style.html) [![Build Status](https://travis-ci.org/FederatedAI/FATE.svg?branch=master)](https://travis-ci.org/FederatedAI/FATE)
[![codecov](https://codecov.io/gh/FederatedAI/FATE/branch/master/graph/badge.svg)](https://codecov.io/gh/FederatedAI/FATE)

 
   
 

[DOC](./doc) | [Quick Start](./examples/federatedml-1.x-examples) | [中文](./README_zh.md)

FATE (Federated AI Technology Enabler) is an open-source project initiated by Webank's AI Department to provide a secure computing framework to support the federated AI ecosystem. It implements secure computation protocols based on homomorphic encryption and multi-party computation (MPC). It supports federated learning architectures and secure computation of various machine learning algorithms, including logistic regression, tree-based algorithms, deep learning and transfer learning.

 


## Federated Learning Algorithms In FATE
FATE already supports a number of federated learning algorithms, including vertical federated learning, horizontal federated learning, and federated transfer learning. More details are available in [federatedml](./federatedml).


## Install

FATE can be installed on Linux or Mac. Now, FATE can support：

* Native installation: standalone and cluster deployments;

* KubeFATE installation:

	- Multipal parties deployment by docker-compose, which for devolopment and test purpose;

	- Cluster (multi-node) deployment by Kubernetes

### Native installation: 
Software environment :jdk1.8+、Python3.6、python virtualenv、mysql5.6+、redis-5.0.2

##### Standalone
FATE provides Standalone runtime architecture for developers. It can help developers quickly test FATE. Standalone support two types of deployment: Docker version and Manual version. Please refer to Standalone deployment guide: [standalone-deploy](./standalone-deploy/)

##### Cluster
FATE also provides a distributed runtime architecture for Big Data scenario. Migration from standalone to cluster requires configuration change only. No algorithm change is needed. 

To deploy FATE on a cluster, please refer to cluster deployment guide: [cluster-deploy](./cluster-deploy).


### KubeFATE installation:
Using KubeFATE, FATE can be deployed by either docker-compose or Kubernetes:

* For development or testing purposes, docker-compose is recommended. It only requires Docker enviroment. For more detail, please refer to [Deployment by Docker Compose](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046efa07f3fe5b1e8e72cbc43f250ba0b4867d8765a997a6ef251dad227bcfffe3fbf6fa517c72a86fd9178aa39bf76f2a45ea6e110cbaea4cda044ad5196b46069 

* For a production or a large scale deployment, Kubernetes is recommended as an underlying infrastructure to manage FATE system. For more detail, please refer to [Deployment on Kubernetes](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046efa07f3fe5b1e8e72cbc43f250ba0b4880fe29792be64002e6a7486b9b28346ad6db7ccbdb893a19994afd03cd944144 

More instructions can be found in [KubeFATE](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046efa07f3fe5b1e8e72cbc43f250ba0b48a77db1798aa03fe2b735593ab8f4874d 

## Running Tests

A script to run all the unittests has been provided in ./federatedml/test folder. 

Once FATE is installed, tests can be run using:

> sh ./federatedml/test/run_test.sh

All the unittests shall pass if FATE is installed properly. 

## Example Programs

### Quick Start

We have provided a python script for quick starting modeling task. This scrip is located at ["examples/federatedml-1.x-examples"](./examples/federatedml-1.x-examples)

###  Obtain Model and Check Out Results
We provided functions such as tracking component output models or logs etc. through a tool called fate-flow. The deployment and usage of fate-flow can be found [here](./fate_flow/README.md)


## Doc
### API doc
FATE provides some API documents in [doc-api](./doc/api/), including federatedml, eggroll, federation.
### Develop Guide doc
How to develop your federated learning algorithm using FATE? you can see FATE develop guide document in [develop-guide](./doc/develop_guide.md)
### Other doc
FATE also provides many other documents in [doc](./doc/). These documents can help you understand FATE better.

## Getting Involved

*  Join our maillist [Fate-FedAI Group IO](http://u.720life.cn/g/2c8f087431e9603ac25d2b7f742746904528900b3dba5e220cde44ce38a0a42a  You can ask questions and participate in the development discussion.

*  For any frequently asked questions, you can check in [FAQ](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462cbba887109d1760fa51a6cf8656336adf78183d51368ec21d5563cec26ac35b 

*  Please report bugs by submitting [issues](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462cbba887109d1760fa51a6cf8656336a65714c04391ef75127bf0f4130aadb4d  

*  Submit contributions using [pull requests](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462cbba887109d1760fa51a6cf8656336afacdc7c4f301b953dfd6c796215fb3c8) 


### License
[Apache License 2.0](LICENSE)




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)