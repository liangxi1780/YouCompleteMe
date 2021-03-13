
![](./doc/picture/introduction/TencentOS_tiny_log.png)

[![license](http://img.shields.io/badge/license-BSD-blue.svg)](https://github.com/Tencent/TencentOS-tiny/blob/master/LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-blue.svg)](https://github.com/Tencent/TencentOS-tiny/pulls)
[![Build status](https://travis-ci.org/Tencent/TencentOS-tiny.svg?branch=master)](https://travis-ci.org/Tencent/TencentOS-tiny)

[(English Documents Available)](README_en.md)

# 一、TencentOS Tiny 简介

[TencentOS tiny]https://cloud.tencent.com/product/tos-tiny)是腾讯面向物联网领域开发的实时操作系统，具有低功耗，低资源占用，模块化，安全可靠等特点，可有效提升物联网终端产品开发效率。TencentOS tiny 提供精简的 RTOS 内核，内核组件可裁剪可配置，可快速移植到多种主流 MCU (如STM32全系列)及模组芯片上。而且，基于RTOS内核提供了丰富的物联网组件，内部集成主流物联网协议栈（如 CoAP/MQTT/TLS/DTLS/LoRaWAN/NB-IoT 等），可助力物联网终端设备及业务快速接入腾讯云物联网平台。


## 1、TencentOS tiny整体架构

![](./doc/picture/introduction/TencentOS_tiny_Architecture.png)
TencentOS tiny 主体架构图，从下到上主要包括：

**CPU 库** ：TencentOS tiny 支持的 CPU IP 核架构，当前主要支持 ARM Cortex M0/3/4/7。

**驱动管理层** ：包括板级支持包（BSP，主要由 MCU 芯片厂家开发与维护）、硬件抽象（HAL，主要由 TencentOS tiny提供，方便不同芯片的适配与移植）、设备驱动（Drivers，例如 Wi-Fi、GPRS、LoRa 等模块的驱动程序）。

**内核** ：TencentOS tiny 实时内核包括任务管理、实时调度、时间管理、中断管理、内存管理、异常处理、软件定时器、链表、消息队列、信号量、互斥锁、事件标志等模块。

**IoT 协议栈**：TencentOS tiny 提供 lwip、AT Adapter、SAL 层，支持不同的网络硬件，例如以太网、串口 Wi-Fi、GPRS、NB-IoT、4G等通信模块。TCP/IP 网络协议栈上提供常用的物联网协议栈，例如 CoAP、MQTT，支撑终端业务快速接入腾讯云。

**安全框架**：TencentOS tiny 为了确保物联网终端数据传输安全以及设备认证安全，提供了完整的安全解决方案。安全框架提供的 DTLS 和 TLS 安全协议，加固了 COAP 及 MQTT 的传输层，可确保物联网终端在对接腾讯云时实现安全认证和数据加密；另外针对低资源的终端硬件，安全框架还提供与腾讯云 IoTHub 配套的密钥认证方案，确保资源受限设备也能在一定程度上实现设备安全认证。

**组件框架**：TencentOS tiny 提供文件系统、KV 存储、自组网、JS 引擎、低功耗框架、设备框架、OTA、调试工具链等一系列组件，供用户根据业务场景选用。

**开放 API（规划开发中）**：TencentOS tiny 将在协议中间件和框架层上提供开放 API 函数，方便用户调用中间件功能，使用户无需过多关心中间件具体实现，快速对接腾讯云，实现终端业务上云的需求，期望最大程度减少终端物联网产品开发周期，节省开发成本。

**示例应用**：TencentOS tiny 提供的示例代码，模块测试代码等，方便用户参考使用。

## 2、TencentOS tiny优势

### (1).小体积
最小内核：RAM 0.6KB，ROM 1.8KB
典型LoraWAN及传感器应用：RAM 3.3KB，ROM 12KB
### (2).低功耗
休眠最低功耗低至2 uA
支持外设功耗管理框架
### (3).丰富的IoT组件
集成主流IoT协议栈
多种通信模组SAL层适配框架；
支持OTA升级
提供简单易用端云API，加速用户业务接入腾讯云
### (4).可靠的安全框架
多样化的安全分级方案
均衡安全需求&成本控制
### (5).良好的可移植性
内核及IoT组件高度解耦，提供标准适配层
提供自动化移植工具，提升开发效率
### (6).便捷的调试手段
提供云化的最后一屏调试功能
故障现场信息自动上传云平台，方便开发人员调试分析

## 3、TencentOS tiny携手合作伙伴共建IoT生态

![](./doc/picture/introduction/Partners.png)

TencentOS tiny目前支持STM32、NXP、华大半导体、国民技术、GD32、Nordic、TI等主流MCU。当前已完成两套官方定制开发板设计，支持全系列STM32 NUCLEO官方评估板内核移植。TencentOS tiny 将携手合作伙伴为物联网终端厂家提供更优质的IoT终端软件解决方案，方便各种物联网设备快速接入腾讯云，共同扩展IoT生态，更好地支撑智慧城市、智能水表、智能家居、智能穿戴、车联网等多种行业应用。

# 二、TencentOS tiny 代码目录
- [TencentOS tiny代码目录说明](./doc/TencentOS-tiny-代码目录说明.md)

# 三、TencentOS tiny 参考文档
## 1、移植指南
- [TencentOS tiny移植指南（KEIL版本）](./doc/TencentOS-tiny-porting-keil.md)
- [TencentOS tiny移植指南（IAR版本）](./doc/TencentOS-tiny-porting-iar.md)
- [TencentOS tiny移植指南（GCC版本）](./doc/TencentOS-tiny-porting-gcc.md)

## 2、TencentOS tiny 开发指南
- [TencentOS tiny内核开发指南](./doc/4.TencentOS-tiny开发指南.md)
- [TencentOS tiny API参考](./doc/5.TencentOS-tiny-SDK文档.md)
- [TencentOS tiny对接腾讯云IoTHub开发指南](./doc/8.TencentOS-tiny对接腾讯云IoTHub开发指南.md)

# 四、TencentOS tiny 开源协议
* TencentOS tiny 遵循 [BSD-3开源许可协议](LICENSE)


# 五、TencentOS tiny 支持的物联网平台
TencentOS tiny能支持物联网终端设备和业务快速接入[腾讯云物联网平台IoT Explorer]https://cloud.tencent.com/product/iotexplorer)。

TencentOS tiny结合腾讯云物联网开发平台IoT Explorer，已经构筑起连接通讯芯片到云开发的能力，加上已经建设完成的国内最大规模LoRa网络，腾讯彻底打通从芯片通讯开发、网络支撑服务，物理设备定义管理，数据分析和多场景应用开发等全链条IoT云开发服务能力，重新定义了物联网开发模式，助力亿级设备多方式多模式低门槛接入腾讯云服务。作为物联网基础设施建设服务者，腾讯将持续打造开放的物联网生态体系，促进物联网生态良性发展。

# 六、TencentOS tiny 快速入门参考
TencentOS tiny联合合作伙伴(南京厚德物联网)设计了定制开发板，如下图：
![](./doc/picture/introduction/EVB_MX.png)

- [TencentOS tiny定制开发板介绍页]http://www.holdiot.com/product/showproduct.php?id=8)，开发者可以基于定制开发板进行快速入门学习，点击下载参考文档
- [TencentOS-tiny定制开发板入门指南](./doc/TencentOS-tiny定制开发板入门指南.pdf)

# 七、贡献代码
* 1.  在您自己的GitHub账户下Fork TencentOS tiny 开源项目；
* 2.  根据您的需求在本地clone 一份TencentOS tiny 代码；
* 3.  您修改或者新增功能后，push 到您fork的远程分支；
* 4.  创建 pull request，向TencentOS tiny官方开发分支提交合入请求；
* 5.  TencentOS tiny研发团队会定期review代码，通过测试后合入。

# 八、加入TencentOS tiny官方QQ技术交流群

扫码加群，请备注TencentOS tiny开发者，工作人员会根据备注进行审核：

![](./doc/picture/introduction/qq.png)

# 九、第三方开发者评测

感谢CSDN博客专家杰杰的贡献

基于野火stm32f103开发板上移植的TencentOS tiny 例程、源码剖析、视频讲解。

## 简单上手：

- [超详细的 TencentOS tiny 移植到STM32F103全教程](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79dedca56664c39a5acf9782dcf177037ae54012b50e2f35b8961c3447404c52e66b2cc7f397cb9bf8c69c3757a4c1df2dbe9) 

## 深度源码分析：

- [【TencentOS tiny学习】源码分析（1）——task](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79dedca56664c39a5acf9782dcf177037ae54012b50e2f35b8961c3447404c52e66b24a7cb96f721bb2b47c985e9e10b02872) 

- [【TencentOS tiny学习】源码分析（2）——调度器](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79dedca56664c39a5acf9782dcf177037ae54012b50e2f35b8961c3447404c52e66b2ec82d0a709c9c7111d05657e165365e6) 

- [【TencentOS tiny学习】源码分析（3）——队列](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79dedca56664c39a5acf9782dcf177037ae54012b50e2f35b8961c3447404c52e66b21d785e21e58901999ddbd03607a1dbc0) 

- [【TencentOS tiny学习】源码分析（4）——消息队列](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79dedca56664c39a5acf9782dcf177037ae54012b50e2f35b8961c3447404c52e66b2c19d6aa27d0f5d70dedb1453c124fa13) 

- [【TencentOS tiny学习】源码分析（5）——信号量](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79dedca56664c39a5acf9782dcf177037ae54012b50e2f35b8961c3447404c52e66b20d3a0c5ff439bcd1ffdb55250c23e59f) 

- [【TencentOS tiny学习】源码分析（6）——互斥锁](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79dedca56664c39a5acf9782dcf177037ae54012b50e2f35b8961c3447404c52e66b2d5e8852f82d1abb04c1e8299d483d0c2) 

- [【TencentOS tiny学习】源码分析（7）——事件](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79dedca56664c39a5acf9782dcf177037ae54012b50e2f35b8961c3447404c52e66b22cb5a48613ca2ae17b0fae34419a33af) 

- [【TencentOS tiny学习】源码分析（8）——软件定时器](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79dedca56664c39a5acf9782dcf177037ae54012b50e2f35b8961c3447404c52e66b28216ed181b0141c064a48dd7413e78f9) 

## 配套例程：

- [【TencentOS tiny学习】例程（0）——hello world](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304675fa28a52337a8a20807bc483b6495aeddec0c820125c9e3238c41d915b3832091acad89071f1af3faf0ac2316fc23e3c8ffade841bb6cfd18c16fb5d6aa34b0) 

- [【TencentOS tiny学习】例程（1）——task](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304675fa28a52337a8a20807bc483b6495aeddec0c820125c9e3238c41d915b38320d75f81e18ac36af8d073f408dc4cbb10) 

- [【TencentOS tiny学习】例程（2）——队列](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304675fa28a52337a8a20807bc483b6495aeddec0c820125c9e3238c41d915b38320435d00b41e1de717725d38e497656f3e) 

- [【TencentOS tiny学习】例程（3）——消息队列](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304675fa28a52337a8a20807bc483b6495aeddec0c820125c9e3238c41d915b38320660595300f4e265b3d8299da89f69d6e7ec027c1d3977d8c5cf703c670fb1cba) 

- [【TencentOS tiny学习】例程（4）——信号量](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304675fa28a52337a8a20807bc483b6495aeddec0c820125c9e3238c41d915b38320d3ef743517579448189076bfab5a6d03) 

- [【TencentOS tiny学习】例程（5）——互斥锁](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304675fa28a52337a8a20807bc483b6495aeddec0c820125c9e3238c41d915b383201897e2df2b7724f8627055033a7c7b91) 

- [【TencentOS tiny学习】例程（6）——事件](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304675fa28a52337a8a20807bc483b6495aeddec0c820125c9e3238c41d915b383202a952e3bc0a74491da6926001dbb850d) 

- [【TencentOS tiny学习】例程（7）——软件定时器](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304675fa28a52337a8a20807bc483b6495aeddec0c820125c9e3238c41d915b38320a1ea6533f7cc0a6fb349cdea4c65266c) 

- [【TencentOS tiny学习】例程（8）——内存池](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304675fa28a52337a8a20807bc483b6495aeddec0c820125c9e3238c41d915b383204474aa7ac9c8fd77994172102706d3aa) 

- [【TencentOS tiny学习】例程（9）——内存堆](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304675fa28a52337a8a20807bc483b6495aeddec0c820125c9e3238c41d915b38320b391148fd8006916399ccb14d04614560672df99539ffc467c889042fe157534) 


## 视频教程：

- [【TencentOS tiny学习】视频汇总](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a9797873134e94e0e9ea30709471212212326f030636fa8cd816457cedb91f769d0ef854e4c3ef0ceeac61724b2a143aa3d) 
- [【视频】01-初识TencentOS tiny](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a9709f66dcb3649bd153aa958c8e26e87f7) 
- [【视频】02-TencentOS tiny基础知识](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a9734eff4772608efab08b2133c1c22e2d3) 
- [【视频】03-TencentOS tiny移植](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a97cc7fc390fdaf0fa62c3074440e88cb7c) 
- [【视频】04-TencentOS tiny任务-1](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a970532a1134bdf81bb276fd37f8f7684fa) 
- [【视频】05-TencentOS tiny任务-2](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a97b6af9993ae4b9f1ffb9e44536f56ce49) 
- [【视频】06-TencentOS tiny队列-1](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a97fd79426afd5674e7bc4e7959a5420ea4) 
- [【视频】07-TencentOS tiny队列-2](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a97b065f7d23b152ffe5422de8a62c75c05) 
- [【视频】08-TencentOS tiny消息队列](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a97fd81ba613d1d5b1e5c0e13b178793c40) 
- [【视频】09-TencentOS tiny信号量-1](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a9731ecc3ba747a473de8d430532262bf07) 
- [【视频】10-TencentOS tiny信号量-2](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a9756c1ee5452709aa690722a450aa61b53) 
- [【视频】11-TencentOS tiny互斥锁-1](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a97ecda26af2860365667967d9507508073) 
- [【视频】12-TencentOS tiny互斥锁-2](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a97839e7ce55a83bdca0aa31798640d3a41) 
- [【视频】13-TencentOS tiny互斥锁-3](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a97f46aba5f281c7356f38f49ce9d23cfdd) 
- [【视频】14-TencentOS tiny事件-1](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a97cfa859f4bf8ff0913763b64e49251785) 
- [【视频】15-TencentOS tiny事件-2](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a97cbb6fe83a713672434dd71c12e7059b2) 
- [【视频】16-TencentOS tiny软件定时器-1](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a97de6ccae9c6c868cf40d5f7d71c217a6b) 
- [【视频】17-TencentOS tiny软件定时器-2](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a97ecda26af2860365667967d9507508073) 
- [【视频】18-TencentOS tiny软件定时器-3](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a97f8f95399ac196f9a0084edc6299d1c15) 

## 相关PPT资料：
- [【TencentOS tiny学习】视频PPT](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304675fa28a52337a8a20807bc483b6495aeddec0c820125c9e3238c41d915b38320d0198327bf9769fb745bf729eae6ba8c) 





 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)