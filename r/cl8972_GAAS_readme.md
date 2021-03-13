 
     
 

# Generalized Autonomy Aviation System

:star: Star us on GitHub — it helps!

[![Join the chat at https://gitter.im/GAAStalk/community](https://badges.gitter.im/GAAStalk/community.svg)](https://gitter.im/GAAStalk/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
  [![Join Facebook Group at https://www.facebook.com/groups/300340454189266/?ref=bookmarks](https://img.shields.io/badge/Group-Facebook-blue.svg)](https://www.facebook.com/groups/300340454189266/?ref=bookmarks) [![twitter](https://img.shields.io/twitter/follow/GAAS_ooo.svg?style=social)](https://twitter.com/GAAS_ooo)   [![Follow Medium at https://medium.com/generalized-intelligence](https://img.shields.io/badge/Medium-Blogs-black.svg)](https://medium.com/generalized-intelligence)
  
  
[ ](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ada5f7b074cbae54b1f0fc72adcb1c5aac888edda6230256a7ba8a1ffa1512faa275a1a43d3cefc728a826ea7a20632c553eafa7609188e171408f595add9827) 
---
[ ](http://u.720life.cn/g/5610af61c96015b9358fd65f1e2d86c0dba3e5bf02894692c1f8cd207ae5f99d69dadaa4e266d877994be3c6bcd471f2) 

[ ](http://u.720life.cn/g/f586abf4f7831ab6b4c32c258231018b109523fd1ec1e9d6e81cd72a43bd3920f6cacb6250855c01d239c1e4fb31030252ee183a06ed9e1a0eb4f7b5eac87162  ](http://u.720life.cn/g/ab0b3dc59e6a87263f3b7d98d443126fe47063ad0e62b41697b952defd6a4f40  ](http://u.720life.cn/g/f2a7d7b12e1fc16eaafd863db538a18319a992b51c06cf04bdc817de31b5c2a6) 
 

[Progress Report 2019.08.01-2019.08.28](http://u.720life.cn/g/d1b0ac7a88e1099f652a21684ea0eda7b24bbf04f15caf4319587a3881c3469a0b4374a855f94e217acd039f52a3e6828ec9656fa254fd7826ceb410230340826a2265f0b6fa2a799bd5e775f95cb009) 

- [What is GAAS?](#what-is-gaas)
  * [Tutorial for GAAS](#tutorial-for-gaas)
  * [Installation](#installation)
  * [Overview](#overview)
  * [Contribute](#contribute)
  * [Meta](#meta)
  * [Special Thanks](#special-thanks)
  * [中文 readme.md](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ada5f7b074cbae54b1f0fc72adcb1c5aac888edda6230256a7ba8a1ffa1512fad10609cd8b8dfa8c9acdf24affe12fe8147a908074658a6b77a78b6feba03f16) 

# What is GAAS?

 

> GAAS (Generalized Autonomy Aviation System) is an open source software platform for autonomous drones and VTOLs. GAAS was built to provide a common infrastructure for computer-vision based drone intelligence. In the long term, GAAS aims to accelerate the coming of autonomous VTOLs. Being a BSD-licensed product, GAAS makes it easy for enterprises, researches, and drone enthusiasts to modify the code to suit specific use cases. 

> Our long-term vision is to implement GAAS in autonomous passenger carrying VTOLs (or "flying cars"). The first step of this vision is to make Unmanned Aerial Vehicles truly "unmanned", and thus make drones ubiquitous. We currently support manned and unmanned multi-rotor drones and helicopters. Our next step is to support VTOLs and eVTOLs.

## Tutorial for GAAS
See the [repo](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ada5f7b074cbae54b1f0fc72adcb1c5aac888edda6230256a7ba8a1ffa1512fab94319b002f8506284d55f52a680fe23406233dd510c342f25199c1cc3dcdb63)  and the [documentation](http://u.720life.cn/g/886cce3806b396aa4f0b83f44f04db126752a2ca5d524548194dcebad74c247c) 


## Installation
Please see [Setup.md](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ada5f7b074cbae54b1f0fc72adcb1c5aac888edda6230256a7ba8a1ffa1512fadb2342aa54d8411c8c75824bea7d76a9fc6ea639689dd0643425cac6a37fa1b7) 


## Overview
Currently the project provides the following ten funcitons, some of which may need to be further optimized: 

NOTE: This is a beta version of the software. Please re-ensure the stability of each feature before implementing on real drones.

 
 
    
    VISION BASED POLE AVOIDANCE BY GAAS
 

1. Details about automatic taking off and landing can be found in: ```software/px4_mavros_scripts```;
2. Navigation in GPS denied environment can be found in: ```software/SLAM/ygz_slam_ros```, currently we are using stereo optical flow;
3. Obstacle avoidance based on stereo vision can be found in: ```software/Obstacle_Map```;
4. Path planning can be found in ```software/Navigator```;
5. Scene recoginition, given an image, recover its position in terms of given environment, details can be found in algorithms/scene_retrieving;
6. 3D modeling, details can be found in ```algorithms/sfm```;
7. [Object tracking](http://u.720life.cn/g/e890eb7ffa84f9513a1cd28c3149c56b5afb2ded3a02fe5075bfd0193a551ce4  details can be found in ```algorithms/object_trace_tracking```;
8. Object detection, details can be found in ```algorithms/image_detection```;
9. Instance segmentation, details can be found in ```algorithms/image_detection```;
10. A list of control API based on MAVROS, and a series of tutorials can be found in ```GAAS/demo```;
11. A list of hardware that we use is at ```GAAS/hardware```.

 
 
 

## Contribute
### I just want to build an autonomous drone
You have come to the right place!

If this is your first time building an autonomous aviation system, check out our [first Tutorial](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ada5f7b074cbae54b1f0fc72adcb1c5aac888edda6230256a7ba8a1ffa1512fab94319b002f8506284d55f52a680fe2312c5369ad83b5407c8cf9314e1f9cdc9  You will get a basic understanding of what MavROS, PX4 and Gazebo are, which are fundamental for the success of your autonomous drone.

If you are stuck with configuration, you may:
1. Google the error messages and see if someone else has solved a similar problem.
2. Visit the [Issues Page](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ada5f7b074cbae54b1f0fc72adcb1c5aac888edda6230256a7ba8a1ffa1512fac3a95758a379414acc111debdeb5a0a0)  to see if others have provided solutions for a similar problem.
3. If neither Step 1 or Step 2 were able to help you, submit an issue to let the community know that you need help. 

If you are an advanced user, feel free to help others to get started, contribute by solving issues, or share with us about your project on our [Gitter group chat](http://u.720life.cn/g/11e95d0ed8d2826912e12fe1dc3f34214f67f75f870e47b9708a7265ae95a402d497e4ee23326abab680d835276a4b1de82563089224362c9c7683ddf0b27e5d919132dda77541ab0173eed0f7830ecf39d697d3b7fcb52722c706c2cee83faeaf0543158c424f8d4c17f15b3ca7d20b  

### I want to contribute

We are so grateful for your interest in contributing!

To start contributing, you need to become familiar with PX4 and MavROS, as well as the workflow of [GitHub](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468ce00409999e7d7eec2a9685f23ba8ebe21c9c7af25b3384792409ff874475d23fdbbc3114ea359539fb0eb15bc25072a22c36b3795ba37b7887fd6bb0014b64  

A good place to start is to look at the [open issues](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ada5f7b074cbae54b1f0fc72adcb1c5aac888edda6230256a7ba8a1ffa1512fadc18091b5741433bc2c76943f2aef0de  From there, you may choose one that interests you to tackle, or open an issue of your own to communicate with other developers. 

PS: One of the best ways to contribute is to help others to kick off their autonomous drone journey. Pay attention to the “Configuration” label in issues page to help others get started.
For more details, please follow [CONTRIBUTING.md](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ada5f7b074cbae54b1f0fc72adcb1c5aac888edda6230256a7ba8a1ffa1512faa7575c5ff5d58178099a6f77d62b8c5c858a095f7b60571823638fd2d9c24bf2) 

## Meta

Project initialized by Generalized Intelligence

Distributed under the BSD 3-Clause license. See ``LICENSE`` for more information.

## Special Thanks

It is worth mentioning that we did not build everything from scratch, but on top of the solid foundations built by pioneers in the field. We would like to thank communities such as [PX4](http://u.720life.cn/g/25260e5e09659994d67262077265f241)  and [Dronecode](http://u.720life.cn/g/f74b0fc30c3c2b7c7185cfd781f0f556d0046efbba8f6f1c84b1cf586f1878aa)  for constantly pushing the industry foward. What they have built are what allowed us to build GAAS!

We are also very grateful for our contributors. You may be able to find them at [AUTHORS.md](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ada5f7b074cbae54b1f0fc72adcb1c5aac888edda6230256a7ba8a1ffa1512fa6ac46a2159f05e3bd54aa319d93cd58910234ec9eda9d84ba0219b7dfef9b0d4 

Il Vole



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)