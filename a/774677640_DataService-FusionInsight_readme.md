# DataService-FusionInsight

#### 项目介绍
基于华为大数据平台FusionInsight的流数据处理服务。
使用Flume组件采集系统日志，并将采集到的日志存放到Kafka消息队列，供SparkStreaming程序消费使用。软件的目的是实现日志文件的实时采集，并实时加工处理到数据库，供其他服务程序使用。

#### 软件架构
项目基于FusionInsight HD V100R002C70SPC200平台，依赖以下组件：  
1. Java: 1.8  
2. Scala: 2.10.4
3. Flume: 1.6.0
4. Kafka: 0.8.2.1 / 0.10.0.0
5. Spark: 1.5.1

软件结构如下：  
DataService-FusionInsight 项目根目录  
+ commons：公共功能模块，提供配置文件读取、数据库连接、日志打印、工具类等公共功能，以供其他模块调用。  
+ kafka-streams：主题数据过滤模块，Kafka自带的流处理功能，业务系统记录的日志如果包含了大量的：程序异常日志、数据库操作日志、调试日志等日志信息，而采集的数据只需要日志文件中的特定数据的日志记录，那么对于我们采集到的日志来说，可能会有90%以上的日志都是垃圾数据，但是Flume组件没有提供日志过滤功能，而Spark程序又不应该消费这些数据。这时就需要提供一个中间层，将Flume采集到的Topic1的日志中满足条件的数据筛选出来放到Topic2中，Spark程序只需要消费Topic2的数据即可，过滤条件按照正则表达式进行配置。这样Spark消费Topic2的数据都是我们需要的数据，并且我们可以及时的清理掉Topic1的数据以释放空间。
+ spark-kafka：Spark程序处理模块，通过SparkStreaming程序，准实时消费Kafka中的数据，经过字段数据解析、码值标准化处理等操作后，落地到DB中，供其他程序、服务使用。

#### 功能扩展
目前，软件实现了Flume数据采集、Kafka主题数据过滤、SparkStreaming实时数据处理。但是SparkStreaming的数据处理只实现了代码值标准化等基础功能。并且，目前默认支持的采集日志格式只有两种：分隔符分隔字段的数据、JSON格式的数据。  
功能扩展可以从两个方面进行：
1. SparkStreaming程序扩展，可以继续增加程序处理功能，完成更复杂的数据处理，比如：指标加工、客户行为分析、客户画像等
2. 日志格式扩展，目前只开发了支持两种类型的日志格式，可以自定义类实现com.service.data.spark.streaming.process.TopicValueProcess接口，以实现其他格式的日志内容的解析。自定义实现类后，需要在spark-kafka模块的resources/META-INF/services/com.service.data.spark.streaming.process.TopicValueProcess文件中添加一行记录类名称，并且在使用过程中将其配置到数据库中即可。

#### 使用说明
数据端配置工具：[数据端配置工具.xlsx](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e2e94194b9900d75288f0ec78e2fcb314cafb92b3bf0f9dd5a1ea6dfde533ca28fe3dea76651313456e7d4120f8fd1103f15e95f592fdfba5af6613280f09fad6a728f4992e22b6c927f3bb57df91a46923e7e0522f195fca873cc88f13f1ca019af8020c3a6aff3d99620ff7404f48e248101cc6b9ea3264781f2c8f970fdeee)  [[下载](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e2e94194b9900d75288f0ec78e2fcb314cafb92b3bf0f9dd5a1ea6dfde533ca283926c33ccfe638fb0cb8d07be76572df873a84b62c7d4761574e143a5f788d2e4b706f197eff032809df41f216cad10e571937361eecc83f699c6c35eec5ad47dcb540c91678628df7988a3c60a2b848acfb17c3d4025f19ec9cdbf357710843   
环境搭建部署文档：[环境搭建部署文档.docx]https://gitee.com/hy-wux/DataService-FusionInsight/blob/master/works/docs/%E7%8E%AF%E5%A2%83%E6%90%AD%E5%BB%BA%E9%83%A8%E7%BD%B2%E6%96%87%E6%A1%A3.docx)[[下载]https://gitee.com/hy-wux/DataService-FusionInsight/raw/master/works/docs/%E7%8E%AF%E5%A2%83%E6%90%AD%E5%BB%BA%E9%83%A8%E7%BD%B2%E6%96%87%E6%A1%A3.docx)]  
软件开发打包文档：[软件开发打包文档.docx](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e2e94194b9900d75288f0ec78e2fcb314cafb92b3bf0f9dd5a1ea6dfde533ca28fe3dea76651313456e7d4120f8fd11035cff2c98b179e023323c6d45fdeabc79ac20a91a6acf7d33a4d4a0683e7feeac8c843bb4eec5d67cb65294b181809425ae60827746bddd6e194d190768f9a46db1c7d5f2c0aab988745dd7af053a3911a8da4da8b566e8226c6d5c58204ae44d)  [[下载](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e2e94194b9900d75288f0ec78e2fcb314cafb92b3bf0f9dd5a1ea6dfde533ca283926c33ccfe638fb0cb8d07be76572df8afa919acddb9d5a1ad500da7badebb73e9b5d637a3fd0f6f7312de4dc8785fcf8803954f288e52ad8383180657b1ea630dbe13b8bdf3936c93a56d4a6d7758936bcf7d4c61ef06af104ae749fbea3f7a5f01f6908600527103a36d843bd5ab9   

#### 部分截图
Flume服务端配置文件下载
![](https://gitee.com/hy-wux/DataService-FusionInsight/raw/master/works/images/007.png)  
Flume服务端配置文件上传
![](https://gitee.com/hy-wux/DataService-FusionInsight/raw/master/works/images/008.png)  
Flume服务端配置文件生效
![](https://gitee.com/hy-wux/DataService-FusionInsight/raw/master/works/images/012.png)  
Flume客户端软件下载
![](https://gitee.com/hy-wux/DataService-FusionInsight/raw/master/works/images/003.png)  
Flume客户端采集配置
![](https://gitee.com/hy-wux/DataService-FusionInsight/raw/master/works/images/013.png)  
Kafka Topic监控
![](https://gitee.com/hy-wux/DataService-FusionInsight/raw/master/works/images/015.png)  
数据库配置项配置
![](https://gitee.com/hy-wux/DataService-FusionInsight/raw/master/works/images/020.png)  
表结构配置
![](https://gitee.com/hy-wux/DataService-FusionInsight/raw/master/works/images/022.png)  
Spark on Yarn 监控
![](https://gitee.com/hy-wux/DataService-FusionInsight/raw/master/works/images/019.png)  
产生分隔符分隔的数据
![](https://gitee.com/hy-wux/DataService-FusionInsight/raw/master/works/images/024.png)  
产生JSON格式数据
![](https://gitee.com/hy-wux/DataService-FusionInsight/raw/master/works/images/025.png)  
数据处理结果验证
![](https://gitee.com/hy-wux/DataService-FusionInsight/raw/master/works/images/026.png)  

#### 安装教程

1. xxxx
2. xxxx
3. xxxx

#### 参与贡献

1. Fork 本项目
2. 新建 Feat_xxx 分支
3. 提交代码
4. 新建 Pull Request


#### 码云特技

1. 使用 Readme\_XXX.md 来支持不同的语言，例如 Readme\_en.md, Readme\_zh.md
2. 码云官方博客 [blog.gitee.com](http://u.720life.cn/g/4d9d51ba66eeb41dfb9759648c593bf554785fd0e6ab49d2f13e98afcb69bbc7) 
3. 你可以 [https://gitee.com/explore](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ed27d15edf43aa40a6d37a2a10b263e5a)  这个地址来了解码云上的优秀开源项目
4. [GVP](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6eb5ad9b84ebe402667383e4a11c785b2d)  全称是码云最有价值开源项目，是码云综合评定出的优秀开源项目
5. 码云官方提供的使用手册 [https://gitee.com/help](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ebbaab544314b1a4bd89bdd984a12bd00) 
6. 码云封面人物是一档用来展示码云会员风采的栏目 [https://gitee.com/gitee-stars/](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e43c4696b881f436e3c9d0b3d64c264cb) 


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)