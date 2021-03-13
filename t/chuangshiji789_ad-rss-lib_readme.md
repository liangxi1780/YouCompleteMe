C++ Library for Responsibility Sensitive Safety
=====

[![License](https://img.shields.io/badge/License-LGPL%202.1--Clause-blue.svg)](https://opensource.org/licenses/LGPL-2.1)
![GitHub tag (latest SemVer)](https://img.shields.io/github/tag/intel/ad-rss-lib.svg)
[![Build Status](https://travis-ci.com/intel/ad-rss-lib.svg?branch=master)](https://travis-ci.com/intel/ad-rss-lib)
[![Code Coverage](https://codecov.io/gh/intel/ad-rss-lib/branch/master/graph/badge.svg)](https://codecov.io/gh/intel/ad-rss-lib)


# Table of contents
1. [Introduction](#introduction)
2. [License](#license)
3. [Documentation](#documentation)
4. [Releases](#releases)
   1. [Release 2.x](#release_2)
   2. [Release 1.x](#release_1)
5. [Getting Started](#started)
   1. [Supported Systems](#systems)
6. [Building the library](#building)
7. [Contributing](#contributing)


## Introduction   
This library intends to provide a C++ implementation of the Responsibility Sensitive Safety model (RSS) for Autonomous Vehicles.

RSS is described in the following papers. Potential users of this C++ library are encouraged to read these papers in order to become familiar with the concepts and functions provided by the library.

* On a Formal Model of Safe and Scalable Self-driving Cars, S. Shalev-Shwartz, S. Shammah, A. Shashua, Mobileye, arXiv:1708.06374, [https://arxiv.org/abs/1708.06374](http://u.720life.cn/g/ef50ff7c3b5c85de9d07d6f28fa0575448ca65ff69058372b173a2d62b0d5f18) 
* Implementing the RSS Model on NHTSA Pre-Crash Scenarios, Mobileye, July 2018, [https://www.mobileye.com/responsibility-sensitive-safety/rss_on_nhtsa.pdf](http://u.720life.cn/g/a7eb1f036efe07c8243b0a3a8f6080b566d2bc779619f614c44746ddaf16ffa9b49d75216867d90ffbc4dbbade1e5d3a74ca7890a5574aa4a81c5dfec6268b77554f3e3fd529f5be6d37857f59c75722) 

The RSS module in this library receives (processed) sensor information as input and provides actuator command restrictions as output. The input to the RSS module is an object list, with information about all objects (road agents) in the surrounding environment of the ego vehicle. For each object, the RSS module creates a description of the object-ego vehicle pair and their properties, called a "situation". For each situation, the relevant RSS safety checks are performed and a proper response is calculated. Finally, one overall response is obtained by combining the responses calculated for each object-ego vehicle situation. The resulting actuation command restrictions, in the form of longitudinal and lateral limits on acceleration are provided as output.

This library contains a stand-alone C++ implementation of the RSS module.

* Conversion of AV sensor data to the input object list required by the RSS module is outside the scope of this library. This includes conversion of object location and motion in a Cartesian world coordinate system into a situation based coordinate system.
* Conversion of the output acceleration restrictions to real AV actuation commands (enforcing the restrictions) is outside the scope of this library. This conversion depends strongly on the software and hardware setup of the actual (or simulated)vehicle.

The scope, design and architecture of this C++ library for RSS is described in more detail in the following document packaged with this release. This documentation includes guidance on the usage of the RSS library and its integration into an autonomous driving system. Users of this library are strongly encouraged to read this documentation prior to integration of the library.

### Integrating RSS with automated driving maps
When RSS is to be integrated into a larger system it is usually up to the user implementation to provide the required input into RSS based on the environment information
available within the system. The [*ad_rss_map_integration*](http://u.720life.cn/g/de195d65b4699092fb68205c90c4dfe7344f58b16809d43473a40ebb3ff9ad087ad5e40ba5d7ad7e609319ee0c45fbb0c5613485faedaa7f5a1320fb509d2b40)  library provides a C++ implementation
for integrating RSS with automated driving maps.

### Usage of ad-rss-lib
If you use ad-rss-lib for any publication, please cite the IV'2019 paper:
```
@INPROCEEDINGS{
   title={Towards Standardization of AV Safety: C++ Library for Responsibility Sensitive Safety}
   author={Gassmann, Bernd and Oboril, Fabian and Buerkle, Cornelius and Liu, Shuang and Yan, Shoumeng and Elli, Maria Soledad and Alvarez, Ignacio and Aerrabotu, Naveen and Jaber, Suhel and van Beek, Peter and Iyer, Darshan and Weast, Jack}
   booktitle={2019 IEEE Intelligent Vehicles Symposium (IV)}
   year={2019}
}
```

#### Usage with Python
Starting with Release v1.6, it is possible to use the ad-rss-lib library also with Python.
Please see the [Documentation on the Python binding for ad_rss](http://u.720life.cn/g/de195d65b4699092fb68205c90c4dfe7344f58b16809d43473a40ebb3ff9ad082aba5997bd24ec48a08ce705ec5b29355ae2f128b8c05ce2f380eb19bd1b1e1d7c1da683b0fa334e81801defee13d4b2)  or [ad_rss_map_integration_python](http://u.720life.cn/g/de195d65b4699092fb68205c90c4dfe7344f58b16809d43473a40ebb3ff9ad087ad5e40ba5d7ad7e609319ee0c45fbb0270ff0111cd19fafba84c28d253f625c869114bc4aa9b088e263f77a7b02cf3f84e0156e533bcad868ec0f6b224a91d66ce6cba7134a6e0fba364ba824befe00)  for further information.

#### Usage within CARLA
This library can be used together with the open-source driving simulator [CARLA](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d39f026c27eb059854517312a4769b8d9bf5eb31842337fe47c8ce41cc775c83)  to investigate the behavior of RSS. A first version is shown in the following video sequence:
[![RSS safety sensor in CARLA](https://raw.githubusercontent.com/intel/ad-rss-lib/master/doc/images/carla_integration.png)](https://www.youtube.com/watch?v=UxKPXPT2T8Q)

#### Usage within Baidu Apollo
In addition, the library is already integrated and used in Baidu's [Apollo Open Platform stack](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467f10316befc55b12c9528be4c3bf78af490dc25def2291454bb01a082b3fbd11 

![RSS integration in Apollo](https://raw.githubusercontent.com/intel/ad-rss-lib/master/doc/images/apollo_integration.png)


## License   
This software library is provided under the LGPL-2.1 open-source license: https://opensource.org/licenses/LGPL-2.1.

In addition, the terms in the following apply:
[RELEASE NOTES AND DISCLAIMERS](./RELEASE_NOTES_AND_DISCLAIMERS.md).

## Documentation
Visit the project's [GitHub page](http://u.720life.cn/g/de195d65b4699092fb68205c90c4dfe7344f58b16809d43473a40ebb3ff9ad08a9e49ba5abc37786fda45863647c0f2a)  to access the online version of the full documentation of this library. This includes:

* [Doxygen](http://u.720life.cn/g/de195d65b4699092fb68205c90c4dfe7344f58b16809d43473a40ebb3ff9ad08ee0787237c9a06c6a6bdd594212437ef0e9efea6aa789d4b917e4805ebe171d6) 
* [Background documentation](http://u.720life.cn/g/de195d65b4699092fb68205c90c4dfe7344f58b16809d43473a40ebb3ff9ad08cdf850fa9e64fc134b8d1ba62ea0e2ae25ec90794a4e4e655da222129cbeb126 
* [Integrate RSS with AD map data](http://u.720life.cn/g/de195d65b4699092fb68205c90c4dfe7344f58b16809d43473a40ebb3ff9ad087ad5e40ba5d7ad7e609319ee0c45fbb0c5613485faedaa7f5a1320fb509d2b40)  and respective [Doxygen](http://u.720life.cn/g/de195d65b4699092fb68205c90c4dfe7344f58b16809d43473a40ebb3ff9ad08ee0787237c9a06c6a6bdd594212437ef7eb9898cd97ce3db3981c8be66f8465885a1380e6bb294fa7e319fdfa774e5c3 

If you have any additional question not answered therein, you might find more in the [FAQ](http://u.720life.cn/g/de195d65b4699092fb68205c90c4dfe7344f58b16809d43473a40ebb3ff9ad08cd5c609a49ec9acd9d3e4365f0e68b16744727c469715821940aff9ea7ab724a) 

## Releases   
General release notes and changes can be found in the [Changelog](http://u.720life.cn/g/de195d65b4699092fb68205c90c4dfe7344f58b16809d43473a40ebb3ff9ad0848a99f327f0b1fb82e3a3a18bd60aaec607578ffde16b2cfd452e4c34f328727) 

#### Release 2.x.x   
These releases extend the 1.x version with map integration for extended usability.

#### Release 1.x.x   
The initial release of the C++ software library for RSS implements a subset of the rules and calculations specified in the published RSS paper. This means that this release handles a subset of autonomous driving scenarios, described below. Scenarios other than this subset cannot be handled.

##### Features & Limitations
This release implements the RSS calculations and rules corresponding to the following scenarios:

* Multi-lane roads, i.e. longitudinal and lateral safe distance and proper response determination; and
* Intersections, i.e. two or more routes of different geometry, rules for intersections of routes, with priority/right of way, and longitudinal and lateral proper response determination. However, in the case of intersections, it is assumed that there is always a lateral conflict.

The following parts of RSS are NOT implemented in this release of the library software:

* Unstructured roads, e.g. parking lots and wide round-abouts;
* Pedestrians, bicyclists and other vulnerable road users;
* Occlusions;
* Longitudinal or lateral evasive maneuvers as defined by RSS; and
* Intersections without a lateral conflict.

Note: The RSS module in this library does not initiate evasive manuevers. At the same time, it would not hinder an evasive manuever being executed by the AV driving policy and planning modules, as long as it is compliant with the required RSS proper response.

## Getting started   

#### Installation of dependencies
Currently, the focused operating system is Ubuntu 16.04. Nevertheless, the library should work in a similar way for any other Linux OS.
To install the dependencies for Ubuntu 16.04 execute the following command:
```bash
 user$> sudo apt-get install git build-essential cmake
```

If you want to use doxygen for API documentation, please also install:
```bash
 user$> sudo apt-get install doxygen graphviz
```

#### Get the library
To download the library, you may run:
```bash
 user$> git clone https://github.com/intel/ad-rss-lib.git
 user$> cd ad-rss-lib
```

#### Supported systems   
Besides Ubuntu 16.04 we are currently supporting the following Linux OS and compiler combinations:

|                 | Ubuntu 14.04 | Ubuntu 16.04 | Ubuntu 18.04 |
|:---------------:|:------------:|:------------:|:------------:|
|  Clang 3.4      |   only 1.x   |              |              |
|  Clang 3.8/3.9  |   only 1.x   |       x      |              |
|  Clang 5.0      |              |       x      |              |
|  Clang 6.0      |              |       x      |   only 1.x   |
|   GCC 4.8       |   only 1.x   |              |              |
| GCC 5.4/5.5     |              |       x      |              |
|   GCC 6.0       |              |       x      |              |
|   GCC 7.3       |              |       x      |       x      |

Important: cmake is required to be at least version 3.5!

## Building the library   
See the detailed [Build instructions](http://u.720life.cn/g/de195d65b4699092fb68205c90c4dfe7344f58b16809d43473a40ebb3ff9ad081499aca08deb1bad81096bab01aff9bd9c7344c7f41648b25390d2dcd4697251 

## Contributing   
Contibutions are very welcome!

Before submitting a pull request, please ensure that your code compiles successfully and that the tests run successfully.
Please also check that your code formatting complies to the provided clang style. To do so, you can run:
```bash
ad_rss$> sudo apt-get install clang-format-3.9
ad_rss$> find -iname *.cpp -o -iname *.hpp | xargs clang-format-3.9 -style=file -i
```
This command will automatically update the code formatting to be compliant with our style.

In addition, please perform a static code analysis, if possible.
```bash
ad_rss$> sudo apt-get install clang-tidy
ad_rss$> cmake -DBUILD_STATIC_ANALYSIS=ON
ad_rss$> make clang-tidy
```
This may provide a list of possible improvements that you would like to consider in your pull request.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)