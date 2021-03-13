
# QUANTAXIS 量化金融策略框架

------------------


## QUANTAXIS 新版本客户端/手机终端 5月即将发布 


![pypidownloads](https://img.shields.io/pypi/dm/quantaxis.svg)
![pypidownloads](https://img.shields.io/pypi/dw/quantaxis.svg)
[![Backers on Open Collective](https://opencollective.com/QUANTAXIS/backers/badge.svg)](#backers) [![Sponsors on Open Collective](https://opencollective.com/QUANTAXIS/sponsors/badge.svg)](#sponsors) 

[![Github workers](https://img.shields.io/github/watchers/quantaxis/quantaxis.svg?style=social&label=Watchers&)](https://github.com/quantaxis/quantaxis/watchers)
[![GitHub stars](https://img.shields.io/github/stars/quantaxis/quantaxis.svg?style=social&label=Star&)](https://github.com/quantaxis/quantaxis/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/quantaxis/quantaxis.svg?style=social&label=Fork&)](https://github.com/quantaxis/quantaxis/fork)

[点击右上角Star和Watch来跟踪项目进展! 点击Fork来创建属于你的QUANTAXIS!]

![QUANTAXIS_LOGO_LAST_small.jpg](http://pic.yutiansut.com/Fn0TPEcwu_uhraf58_93Ul5yfvAz)

![gvp](http://pic.yutiansut.com/gvp.jpg)

Quantitative Financial FrameWork

从数据爬取-清洗存储-分析回测-可视化-交易复盘的本地一站式解决方案







QUANTAXIS 项目从2017年开始  已经从一个写毕业论文时没有框架  到现在实际在私募中稳定运行的项目了 因此QUANTAXIS对于刚接触的人会感觉较为庞大和无从入手, 在经历了群里的同学和一些实际企业的部署以后 , 我们希望你可以从以下方式逐步入手和了解QUANTAXIS



## QUANTAXIS提供什么

简单的讲 QUANTAXIS 提供的是一个从0到一个完整的可以上实盘的支持多市场多周期多策略的框架, 支持局域网/互联网远程部署

- 投研分析

  - 全市场数据(日线/分钟线/tick)
  - 财务数据
  - 股票/期货/期权/港股/美股/(以及自定义数据源)
  - 为多品种优化的数据结构QADataStruct
  - 为大批量指标计算优化的QAIndicator [支持和通达信/同花顺指标无缝切换]
  - 基于docker提供远程的投研环境
  - 自动数据运维

- 回测

  - 纯本地部署/开源
  - 全市场(股票/期货/自定义市场[需要按规则配置])
  - 多账户(不限制账户个数, 不限制组合个数)
  - 多品种(QADataStruct原生为多品种场景进行了优化)
  - 跨周期(基于动态的resample机制)
  - 多周期(日线/周线/月线/1min/5min/15min/30min/60min/tick)
  - 可视化(提供可视化界面)
  - 自定义的风控分析/绩效分析

- 模拟

  - 支持股票/期货的实时模拟(不限制账户)
  - 支持定向推送/全市场推送
  - 支持多周期实时推送/ 跨周期推送
  - 模拟和回测一套代码
  - 模拟和实盘一套代码
  - 可视化界面
  - 提供微信通知模版

- 实盘

  - 支持股票(需要自行对接)
  - 支持期货(支持CTP接口)
  - 和模拟一套代码
  - 不限制账户数量
  - 基于策略实现条件单/风控单等
  - 可视化界面
  - 提供微信通知模版

- 终端

  - 提供mac/windows的可安装版本(QACommunity)
  - 提供全平台可用的web界面
  - 提供手机客户端(ios/andriod)  [内测中]

  



## QUANTAXIS如何部署/使用

因为QUANTAXIS和其相关联的项目约有19个之多, 包括了从本地账户系统到数据收集, 数据分发, 数据存储, 实时的消息分发, 策略挂载, 可视化, 投研环境 等大量内容, 因此 不推荐用户在不熟悉的情况下进行本地部署, 我们推荐的路径(也是我们在私募中实际使用也是)是docker模式



### 部署

docker可以理解为一个高效的虚拟机环境(性能损失不到2%), 每个虚拟机包含了一部分独立的代码内容, 因此我们通过类似叠积木的形式就可以将我们所需要的环境一个一个搭建起来

我们推荐:

| Win10 企业版/教育版 | 路径                                                  |      |
| ------------------- | ----------------------------------------------------- | ---- |
| Win10 企业版/教育版 | 通过docker-desktop                                    |      |
| Win10 家庭版/Win7   | 推荐升级系统至win10企业版, 或者使用docker-toolbox部署 |      |
| Linux用户           | 支持一键部署脚本, 快速拉起docker                      |      |
| Mac用户             | 通过docker-desktop                                    |      |
| 强行需要代码部署    | 19个项目 8个服务需要自行手动开启                      |      |

### 使用

对于初学者, 我们推荐直接上手```QAStrategy```来直接编写回测/模拟/实盘


    QAStrategy传送门: 
    
    [QAStrategy]https://github.com/yutiansut/QAStrategy）

PS: 除了可视化的桌面端/网页端 QACommunity(内置在docker/ 群文件自行下载) 以外,  QAStrategy专属的APP也即将上架, 支持自定义的服务器后端连接, 实时的实盘账户手动干预, 行情处理, 持仓管理以及多策略的运行调整等 



### QUANTAXIS的结构



![QUANTAXIS 2019.png](http://pic.yutiansut.com/FnRlMW2LQpFBrsdRv7E_uJ9RvzHt)

技术栈: python/nodejs/vue/mongodb/rabbitmq/c++

### 核心工具链(生产环境在用)

![QQ图片20191029223640.png](http://pic.yutiansut.com/FuVrzcbWJUBNrj4Wa0zlRl-YlBY_)

#### 已开源

> 数据存储/数据分析/回测

- [QUANTAXIS](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461fd6ed1c8757ea34675ede980caf5325d236ecef7b9ed3591805c7a890076b68)  QUANTAXIS的核心部分

> WEB相关, http/websocket/开放数据接口

- [QUANTAXIS_WEBSERVER](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461fd6ed1c8757ea34675ede980caf53251251eebb7033f6e9da3c2bac48e5c274)  基于tornado的web api/ websocket

> 分布式相关, 任务异步执行, 跨进程分布式消息订阅分发

- [QUANTAXIS_RUN](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a506b4cb0b5b8e4837ca9c72de673379a00d16663f005ec0f9beb0c6f03a42d1)  基于rabbitmq/celery的分布式任务部署
- [QUANTAXIS_PUBSUB](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304697c112862c6959f21f340e8261a60d9c839bb52e09c025ccbc4f9db6c8b3e2da)  基于RABBITMQ的消息分发订阅

> 接口相关: 交易账户/ 期货接口封装/ Trader实例
- [QUANTAXIS OTGBROKER](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304675f0cac9fb75e0b84189fb595aab2e7c28e9b2faed319e522917f2a7bccc22d3)  基于OPEN_TRADE_GATEWAY的接口封装
- [QUANTAXIS CTPBEEBROKER](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ba7365b6582e006d1c46f50c207c0dc60b1135b35684d27e5b581c6959df08ea)  基于CTPBee的接口封装
- [QUANTAXIS_ATBROKER](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b34ccc911fffda81a72784c583bbbf3794f7fe167cd22dac5479a2a886ea529a)  基于海风at的接口封装
- [QUANTAXIS TRADER](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046892eb7b89475cb4cd44304ddc22369257ad443093ab7077bfe757a7a9852d416)  一个开源的websocket版本的期货交易实例

> 策略相关 
- [QASTRATEGY101](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b5b52ceaf407511710702b1e4e8d264e8912358806330bdeb9edea22d7c03902)  101个基础策略[逐步更新中...]

> 行情相关: 主推行情实现/ 基于OU过程的模拟行情
- [QUNATAXIS MARKETCOLLECTOR](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304697cb12c6a10cd262b63ead0954ef7995f4987d80ac6216cd91fffe777ee6c09c2e7b3f8b4f2921fd85ca6d8557920533)  全市场订阅分发的行情推送
- [QUANTAXIS_RandomPrice](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304697cb12c6a10cd262b63ead0954ef79950ad64fa3a81fbd11a8acd6d8dbd392d131dd88814dd84b43473e0df37ac5c894)  基于OU过程的随机行情模拟

> 账户协议

- [QIFI](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ad498cad092b0b7d76d70af5d1468067cbaa0bd7e742e2ee81c4f24f2d7b4ba5)  一个基于快期DIFF协议的QA实时账户协议
- [QIFIAccount](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e66ab84e44faff05d915de1a3239aaf92a71230e4f730f4a48879ca4fc3b35e2)  一个基于QIFI协议的多市场兼容的 实时账户实现
- [QAStrategy](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c848721150621cbc600bd6ab8411b59e7c7a3a2ae836d3792fdc959654d12a05)  一个完整的 支持 模拟/回测/实盘一键切换的策略基类

> 多语言实现

- [qatrader-rs](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467fe79db041dc30c3277767eb3fadd2c49532eb864c5c5a2b3f95c4f78797d128)  一个rust实现的qatrader
- [qamarket-rs](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463b2d5b999755def49dd43d3eada2b9f1b2c417f3a823d375528a957bd14cc610)   一个rust实现的期货全市场行情多周期采样分发



#### 未开源

未开源部分为 目前私募自用部分, 因此暂时不开源 一些相关的项目会经过选取和完善后逐步开源

> 实时交易解决方案/ 无人值守/状态汇报/实时账户评估/多账户/策略账户拆分/事件流风控/PB系统/CEP引擎/多系统终端

- [QUANTAXIS_REALTIME_RESOLUTION](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304697cb12c6a10cd262b63ead0954ef79952b76c74593846c5e2cb03ecaf1adcea3aa8d8c787500cc90cc783aa4e5dbdbf2)  实时交易/部署解决方案(未开源)
- [QUANTAXIS UNICORN](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304630d3de49212189a85c8d24ba23c98a38a7f9eca729b72967f9ec213bf936f8a5)  QUANTAXIS 策略托管, 交易监控解决方案(未开源)
- [QUANTAXIS_RANK](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b14aeba26f02e9ae7ba006f520a65bcb2e7f9701f1c243badcce0421b75cfad7)  QUANTAXIS实时账户评估
- [QUANTAXIS_CEPEngine](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ae2c5d614cc858876d9e3f55643edb1561a6007d4459463d0eb039fc2bef72ea)  QUANTAXIS 复杂事件处理引擎
- [QUANTAXIS_PBSystem](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465f2906b544ced04a6da2831ed3d552dad4daed7693d4cd029a0e14677f11f5d3)  QUANTAXIS PB系统
- [QUANTAXIS_QARISKPRO](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b14aeba26f02e9ae7ba006f520a65bcb8d92a51a18ede749d75b2fc19292de56)  QUANTAXIS 多市场多账户集成的实时风控系统
- [QUANTAXIS QADESKPRO](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046bf5fc81e82060250bd5ad45162de3d9dbe95d8ceb006f45d121b818137e27e8a)  新版本客户端网页(部分开源)
- [QUANTAXIS PMS](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465f2906b544ced04a6da2831ed3d552dab337a44b4788fbef616fe2f27cb11f98)  一个轻量级的纯python实现的  兼容QIFI协议的账户/仓位管理系统

> tick回测

- [QUANTAXIS TICKBacktest](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046892eb7b89475cb4cd44304ddc2236925c296aa0a4c3ef7be9b685859dae20477)  tick回测 支持真实tick/仿真tick

> jupyterhub 定制(多人编辑)

- [QUANTAXIS JUPYTERHUB](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046407080abcf57b54312352e13744ac6f05ea6056184356accc4a96390b65ff641) 

> docker cluster

- [QUANTAXIS PROCluster](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465f2906b544ced04a6da2831ed3d552dabb981e6182fd7f01753111672ea103f6)  一键部署的docker集群, 2地3中心的高可用灾备投研/交易环境


### 社区提供的工具链

- [QUANTAXIS_MONITOR_GUI](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461fd6ed1c8757ea34675ede980caf5325d4bab153a5592856185cb5d0e64956a5672364f8e03911755c9e18003fb4c44a)  基于QT的python监控
- (目前废弃)[QUANTAXIS_DESKTOP](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f11818e37c47d227c7010840b4a1d413f639506df9c892d732ba80a9cdff87c8)  基于VUE.js/ ELECTRON的 桌面终端
- [portable_QA](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467d9bd6a534cdfef88c2145ca3f0c81301d7c54051fdc11282cf5a72caa052a38)  一个独立的python环境,免配置
- [QUANTAXIS_CRAWLY](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461fd6ed1c8757ea34675ede980caf5325dda6dbb97694cfb8624bb5fb0413b3e8)  爬虫部分

## 社区/项目捐赠

### github

QUANTAXIS 是一个开放的项目, 在开源的3年中有大量的小伙伴加入了我, 并提交了相关的代码, 感谢以下的同学们

   



许多问题 可以在 [GITHUB ISSUE]https://github.com/QUANTAXIS/QUANTAXIS/issues)中找到, 你可以提出新的issue



### QQ群

欢迎加群讨论: 563280067 [群链接](http://u.720life.cn/g/55fcd4cfb32e35fc063cde71dfc8708f6dfac4862855c04eecbf6b86ad7d9dc9c0ef6657c15c9ca579ee0756b5e93f2a)  

DISCORD 社区  https://discord.gg/mkk5RgN

QUANATXIS 前端开发群: 983499694 [群链接](http://u.720life.cn/g/55fcd4cfb32e35fc063cde71dfc8708fdef04e15024a63ea72e26bcd340a5c2a8dab3d5116fa3971e6a1527b8c3ffc17) 

QUANATXIS 研报阅读/ 事件驱动分析群: 1045723486 [群链接](http://u.720life.cn/g/55fcd4cfb32e35fc063cde71dfc8708fc4e2e4020045b3841d0702d1fac4e33c69e99d125d843a20cf4e28994a9233bc) 

QUANTAXIS 开发群: 773602202 (如果想要贡献代码 请加这个群 需要备注你的GITHUB ID)

QUANTAXIS 期货实盘多账户的本地部署群 (请勿浪费群资源 没有本地多账户部署的请勿加): 945822690

### 公共号

欢迎关注公众号: ![公众号](http://data.yutiansut.com/qrcode_for_gh_bbb47e0550f7_258.jpg)

QAPRO公共号免费提供了下单推送接口, 关注公共号回复trade即可使用

### 论坛 QACLUB

QUANTAXIS 内测版论坛 [QUANTAXISCLUB上线](http://u.720life.cn/g/9bf6a474ee7d851d7a1cda0fd67e48df252bfa433992c6d9d8c748dcc8808acd) 

http://www.yutiansut.com:3000

凡通过论坛进行提问的 均有最高的回复优先级

### 文档

全新文档界面 [QUANTAXISDocs](http://u.720life.cn/g/c3a7cdfaedc2068d3101d182ff80b4b5968274226f0939cd8423c0244e7dd3c4) 

http://doc.yutiansut.com

 ### 捐赠

写代码不易...请作者喝杯咖啡呗?


![](http://pic.yutiansut.com/alipay.png)

(PS: 支付的时候 请带上你的名字/昵称呀 会维护一个赞助列表~ )

[捐赠列表](CONTRIBUTING.md)



##  QUANTAXIS 桌面级产品(全平台 WIN/MAC/LINUX)




首页

![image.png](http://pic.yutiansut.com/FnGCyLQ8nRLFOYX8elP4PhJ7IQuq)

登陆

![image.png](http://pic.yutiansut.com/FmDc4ZPxHeNncZICoMr9dqz46h78)

行情/键盘精灵

![image.png](http://pic.yutiansut.com/FhiN_asx158UobclVpCY00e61pjr)

lab 投研

![image.png](http://pic.yutiansut.com/FlkJTKu7iG-FD7Rz2DwUhvs2Cy3j)

回测/组合

![image.png](http://pic.yutiansut.com/FuB_dC5vX5Y1_Z8At0MiMRXcE5ZT)
![image.png](http://pic.yutiansut.com/Fqvh8m1ka4jdmwYwBn8MAHixpZOm)

模拟实盘多账户管理
![image.png](http://pic.yutiansut.com/Fh0fZzqORNRmY5txaXYgHWJUCPqw)
![](http://pic.yutiansut.com/QQ%E6%88%AA%E5%9B%BE20190311015440.png)
![](http://pic.yutiansut.com/QQ%E6%88%AA%E5%9B%BE20190311015451.png)
![](http://pic.yutiansut.com/QQ%E6%88%AA%E5%9B%BE20190311015550.png)
![](http://pic.yutiansut.com/QQ%E6%88%AA%E5%9B%BE20190311015537.png)




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)