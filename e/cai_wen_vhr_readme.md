扫码加微信（微信ID：**a_java_boy2**），备注微人事，进群讨论。

![微信ID：a_java_boy2](https://user-images.githubusercontent.com/6023444/75459026-ba70d500-59b9-11ea-8cbd-3d5889f356c4.png)

## 项目介绍

微人事是一个前后端分离的人力资源管理系统，项目采用 SpringBoot+Vue 开发，项目加入常见的企业级应用所涉及到的技术点，例如 Redis、RabbitMQ 等。


- 项目地址：[https://github.com/lenve/vhr](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046cc4a2959ca8b572dad07ab9fe52718fe)  
- [项目部署视频教程（旧版）](http://u.720life.cn/g/408fb60b53d11d245635ad5e8e8cd697f615213c104cc2d5f1852040f1118d53f1947a8f31698ad6abfc04fc0ba65009aca66d02fe6ce664c77d54161852ba59) 
- [项目部署视频教程（新版）](http://u.720life.cn/g/408fb60b53d11d245635ad5e8e8cd69775c61557bb1115a47eb481be4c1929bc5ea9f58ee9ee95737eaee5aa393aceec7c62d1aa1f42bfb3d244abc35a5fc678) 

### 项目技术栈

#### 后端技术栈

1. Spring Boot
2. Spring Security
3. MyBatis
4. MySQL
5. Redis
6. RabbitMQ
7. Spring Cache
8. WebSocket
9. ...

#### 前端技术栈

1. Vue
2. ElementUI
3. axios
4. vue-router
5. Vuex
6. WebSocket
7. vue-cli4
8. ...

### 项目效果图

首先，不同的用户在登录成功之后，根据不同的角色，会看到不同的系统菜单，完整菜单如下：

![p278](https://raw.githubusercontent.com/wiki/lenve/vhr/doc/p278.png)

不同用户登录上来之后，可能看到的会有差异，如下：

![p279](https://raw.githubusercontent.com/wiki/lenve/vhr/doc/p279.png)

每个用户的角色是由系统管理员进行分配的，系统管理员给用户分配角色的页面如下：

![p280](https://raw.githubusercontent.com/wiki/lenve/vhr/doc/p280.png)

系统管理员也可以管理不同角色可以操作的资源，页面如下：

![p281](https://raw.githubusercontent.com/wiki/lenve/vhr/doc/p281.png)

## 快速部署

1. clone 项目到本地 `git@github.com:lenve/vhr.git`
2. 数据库脚本使用 Flyway 管理，**不需要手动导入数据库脚本**，只需要提前在本地 MySQL 中创建一个空的数据库 vhr，并修改项目中关于数据的配置（resources 目录下的 application.properties 文件中）即可
3. 提前准备好 Redis，在 项目的 application.properties 文件中，将 Redis 配置改为自己的
4. 提前准备好 RabbitMQ，在项目的 application.properties 文件中将 RabbitMQ 的配置改为自己的（**注意，RabbitMQ 需要分别修改 mailserver 和 vhrserver 的配置文件**）
5. 在 IntelliJ IDEA 中打开 vhr 项目，启动 mailserver 模块
6. 运行 vhrserver 中的 vhr-web 模块

**OK，至此，服务端就启动成功了，此时我们直接在地址栏输入 `http://localhost:8081/index.html` 即可访问我们的项目，如果要做二次开发，请继续看第七、八步。**

7. 进入到vuehr目录中，在命令行依次输入如下命令：

```
# 安装依赖
npm install

# 在 localhost:8080 启动项目
npm run serve
```

由于我在 vuehr 项目中已经配置了端口转发，将数据转发到 Spring Boot 上，因此项目启动之后，在浏览器中输入 `http://localhost:8080` 就可以访问我们的前端项目了，所有的请求通过端口转发将数据传到 Spring Boot 中（注意此时不要关闭 Sprin gBoot 项目）。

8. 最后可以用 WebStorm 等工具打开 vuehr 项目，继续开发，开发完成后，当项目要上线时，依然进入到 vuehr 目录，然后执行如下命令：

```
npm run build
```

该命令执行成功之后，vuehr 目录下生成一个 dist 文件夹，将该文件夹中的两个文件 static 和 index.html 拷贝到 Spring Boot 项目中 resources/static/ 目录下，然后就可以像第 6 步那样直接访问了（关于前后端分离部署，大家也可以参考这个[使用 Nginx 部署前后端分离项目，解决跨域问题]https://mp.weixin.qq.com/s/C7PIck3SIPPTcA3NX3ELoQ)）。


**步骤 7 中需要大家对 NodeJS、NPM 等有一定的使用经验，不熟悉的小伙伴可以先自行搜索学习下，推荐 [Vue 官方教程]https://cn.vuejs.org/v2/guide/)。**

## 文档

文档是对项目开发过程中遇到的一些问题的详细记录，主要是为了帮助没有基础的小伙伴快速理解这个项目。

1. [权限数据库设计](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f25ffcf72c1ee0e1ca7c4efffc035f1ff4935289eedf239ffd1f89ef10c8f0dfaecdbf018638a3762bb7c30ec7a5ee26208946b69ce0dc9a19cfb007c6aeb07748f8c152b20d30cc40305dbcacb8bf9da) 
2. [服务端环境搭建](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572fb939a43ab01ef527ea35bad44c205cc25ecf9f5d44bb3e2c8074275cf5522e36e5f9369f20cc87ed1f0d2765d1a38683cc6ffb4f127515c731245220c297213dc8e6eb6772d61678931c27bb89ee6b7c) 
3. [动态处理角色和资源的关系](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f25ca788af4e17a09865491f100b80ff1eb62c0a18d8c923ec5c25ab37c1a15f618ce67731eb1e1cae27357be422979c1e7c5f907b1d60b048d39e40b216da6c7fa1f123bbc0e0a2f6359ae13fa3f148a812c1a8a1f13a31b746efb93cc347c2e4cc4d1a86eb273825434a5f4a07b5866) 
4. [密码加密并加盐](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f36d9fbc978266a1c4beb9541ba61954423c361ffa1e94c26abfc23042a42d1d84b2c18dd228b9d8e0d7fa2d397b56198bedfbad08054902ba882dc7bfbf4052fb19d3bdfa333f6710e86b7815b89d492) 
5. [服务端异常的统一处理](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572fa3667e7bdd90dbb57e4de5f24cc1069fc28ce192158480e50be0127de471aaf59ede43519ce219552f00db529ce1bd94276f4ab31da0962144fb13259f4dab6d991e718f4235929fae8753523f077a7e66cfdb7de2235d58340d4fd88200ab42) 
6. [axios 请求封装,请求异常统一处理](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f482216558c4340716e42378a45a96c68398be042aea1b300b48b29d3e154478bcf4750e30d70c0612dadb1708bd2b9015c6657136cfa58721331a165efce431d0614d7cd49ad7322cd88bea2e34b9280d9eb8a9800f7c283446a7a79e3cfda81924f3e8ff07140e321c53279d0af2962e53ee959e57b4f0ef5b1c65e18a40f87) 
7. [将请求方法挂到Vue上](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f626f9f53d2ae102741aa9b5425579e67c17f4e07beec203276e913c567896409c2ad9744c45cb92ae90c149f3271bdb75f74b8d0e88451f15910a1fdea08240a67326f4d31710a961de022f6c46a4086) 
8. [登录状态的保存](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572fe8b52469e9814af9bf18fa8cdbb8da55328323dc7e1e29c0766b1499700dd344bfa8080043cc176858bbccffd1ee7068ee3b1021cbcf0840f45fda50ba39bad28162d3ef2b984ca858b01235ccb062c5) 
9. [登录成功后动态加载组件](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f3cff5bed2ccbcb4774b2b1f2deaf2b379343d49b65bff8a6598d71c1ecf39259f0538904e40b547dd7bed15e2d8bd0a59b721fa899f363f76bf804fc2795dea96d682affe038a11ce34f5187f7d364a28bad580d8f587fe7e015a9756de83c03aa35508ed2eecd81e5869c96e7404532) 
10. [角色资源关系管理](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f06f8b717ee40f9199a64887b40df9c95c6b9a951f88b751d8ba2e6646ac1be492e5aa6dba4239b03f68df7267426844421ea4a30c78d643d69fd03715040893b1290e3e016baa73349e4ce257914de6c) 
11. [用户角色关系管理](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572fc761a253b482f7e4b23b034b6f79808057530a33a12a256630d14648833a2b1bdd1c57743c74d686d64f640573b5079ba004ab3eb47b20e712959a783e6c4a40c6239ef02a87502ce44963a71c39f2bb) 


### 更新记录

### 2018.1.10 更新

本次更新版本：v20180110

本次更新完成了部门管理功能，页面在 **[系统管理->基础信息设置->部门管理]**

>本次更新也更新了数据库脚本，小伙伴们需要重新下载数据库脚本执行。

#### 相关文档：

12. [部门数据库设计与存储过程编写](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f5e3a7497365adf27894e27f14e3561d1d2e07f3c99a6635ffc658aafc61e0dc3c78f6ea57c12606729e5ff661a848a592d8cd8d70e158decd675405de58553dd7c3c251260c2c2a48252259487ff8e856f3f1724420615ed2702e7ea3b0a6695073ceedd80e6282892f6de526b49ba7896653706c1e4ee541a9033925b0aa760d8786aa4ac46d545230d570e1097db83) 
13. [递归查询与存储过程调用](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f5ff969bf7467672edf231b1531aa33cc717e58285844fdef4a9abe75468dc8cb303aad8b2f7e45ad550be30c789256253c66f7f79f32fd9810795c7de0aae60c3675f65133983a195c041b0d4854d45b9eda011af5a37bb283cab40de858204f0c6291a5ff7bb8d1e116146e5ecce904) 
14. [Tree 树形控件使用要点](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572fa71484a1a19def0d0cfe0956da91d008e5f35a56bee28fca938a090ea4b33f3ee4309f55c8b8ec2f2e7d39fb71acbbdca376ef819c26fd1173ebf08ef381f7d493b95b1b599944dc4904ea83e66d1a2b098b6a2da6e5b71e8f6d0ba7cf390b90) 

### 2018.1.12 更新

本次更新版本：v20180112

本次更新完成了职称管理和职位管理，页面在 **[系统管理->基础信息设置->职位管理]** 和 **[系统管理->基础信息设置->职称管理]** 

>本次更新也更新了数据库脚本，小伙伴们需要重新下载数据库脚本执行。

#### 相关文档：

15. [职位管理和职称管理功能介绍](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f8c93184c783e72f44a1794a1ff5a5e74421bcda4ced4d2a0f019b08e2d6b9b051958decc61b489a23a0f3bf42d2121355aa346184109805944abc207b441e33b63fd28888bf24f857524fcf611110fa387f25a9e7f174ca6237e13b6a803b2a5bc87a76edc04f4ac014a85ee061d6b426578883dd48adf6915685663fba2cf42) 
16. [组件复用](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572fe91642a96e8c52526cdd652ae0d658cb9df4061f8eac763994b05472ecca45d5d29e59f0761ee54e6a27266a2bbc55e0) 
17. [[题外话]利用 git 标签回退至任意版本](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572fc9fb9f99fa7c1739d58af17eb0a03dbcbb5bbd7d2ca9c62456aac92b99962689c6f1ff4b5e0176828e68fb1d225d8b565ff9290787bcbe68d3898b003545fb34ebaf9878f9d39c457d0701e08991afcdadb5f6518d100576a5d36ab15ae77a4d8d460841e98ec499e3125467d51478e58e88334b1797bf5cf14e71ded06022f84fe2e7938683b039c6e0b1479804ac14) 

### 2018.1.15 更新

本次更新版本：v20180115

本次更新完成了员工基本信息管理，页面在 **[员工资料->基本资料]**

>本次更新也更新了数据库脚本，小伙伴们需要重新下载数据库脚本执行。

#### 相关文档：

18. [员工基本信息管理功能介绍](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f56b7795b163911e7ce3c0c1bddd74d7bd29b88b5c593b494dd9f0016896ea18849984198ddbbaf7473972d850975741320732d3f6ede219e52beff6935af4495a9e431f90b8c878f9b06c14d7f00065d4991ffb45825bbabc14c100aa191727ad9569e1b857d037c10edd3be5e08afc271471310b1e8436652006d6c5d51eea8) 
19. [Spring Boot 中自定义参数绑定](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572fdc7b90160d4e8ee28d1b2c350f85b671e9ebced77888b3b20cd0993cb788eaad599b183ce6d58f6689971fc7d94364e3379ec06407a180089e498625e5eefa9ed0291a9facf3ec0bc57881cbe3e9ada1e7182667f8580f73069b3a81882e2075) 

### 2018.1.16 更新

本次更新版本：v20180116

本次更新完成了员工的高级搜索功能，页面在 **[员工资料->基本资料]**

#### 相关文档：

20. [高级搜索功能介绍](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f3fe0c0f8b4b9bd5b0759a4a89f5b2b753052903cf4c6b959f19aed8fbbf90f1bd5667b64c733a932d04a6628ddc2f83e8ac1c31bb586e3d008932a1a99fd8eca239776d7f3f0b2a719eca52d49282aa1) 

### 2018.1.17 更新

本次更新版本：v20180117

本次更新完成了员工数据的导入导出功能，即可将员工数据导出为Excel，也可以将外部Excel导入到员工数据表中，页面在 **[员工资料->基本资料]**

#### 相关文档：

21. [Excel 导入导出效果图](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f631bf8c9f1143cd7242affcc41658fd0f0ef1e0d18ef60ead6f0a224fcb55ea9bd513773cc637b2577f6b686ea698cb6c122dffc9fd20c5ed88914b01dacb6756d91abfdccf17b32b9b9d92443da4e76) 
22. [SpringMVC 文件下载的两种方式](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f806756c509b0c11fb3fc9299c427a36650a4e90b35d768dc407f381e10fd87198bfef98b86e95e693044bcb0eee521bd0a24054f605cf0f532e751dfa0b92feee8d7abe8467e6b05ffa417e93f7710a478e073eb1c4dddc4dd1ff1a200b29f88) 
23. [POI 生成 Excel](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f78e5eabf3c51b47673360ef117740afff88d8d17348960bd693a5bd67046f3fe) 
24. [axios 下载文件](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572fc03189ad1fd3056eca776b4f85d5b964a556964c95ed3abce9fb1b9f4721a9450479ebe856923a6604dbc3c044a2ae6f) 
25. [使用 POI 实现 Excel 导入](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f2f0572fa54d22a4f39a1eb193e8ae1f90fad413277d054935d812f0df1f4616fc5c34bc7e671c31307b13cf555e95aff55ba2866c1046131d9bf3819c65e0e9b8ab525eb0d18c385fd40bca0c2b4602a) 

### 2018.1.19 更新

本次更新版本：v20180119

本次更新主要实现了当管理员添加一个用户时，添加成功后，会根据该用户的邮箱自动向用户发送一封欢迎入职邮件，页面在 **[员工资料->基本资料->添加员工]** 详情可以参考下面的文档。 **注意：邮件发送需要小伙伴小伙伴自己配置授权码，配置方式参考下面的文档，配置文件在[src/main/java/org/sang/common/EmailRunnable.java](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046624dc879ba83f417ac3c2af05ca4481319d0e3ad3c183ba8fb8de6f181e21212f247731d3f7452853548e6f8a5c455ae732e33775ee7135c0da3262da7792ad69ee3ec947e8cd07c5e3dfd7182c82aa619c6e9164e831f435a15aec313f2d0a6  

#### 相关文档：

26. [Spring Boot 中使用 Freemarker 邮件模板生成邮件](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f2e627fa3b19b29a8f7e7027a79f8531dbe69b8dbfa51b10132ae487910cc0cf13cc3f6e66a575f5adb66ab55b7e3535debaa81addaab44e79c11b79623e8b38de3b6121343fda12dbddbb18c57b561b455f2a484a6650c2e715370b6395d7c0160713fd87240cb64d45ec7021491aeb492228898cc5bb5ce4e7e51a2d639bed8) 
27. [Java 中邮件的发送](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f1b61891d43358e1559e9db4414ec2c5f052f264bede1890850c61e0fccf41d01d1a5bfcc165c6d55a97b028f3827269997822264aa76cda2f7cf754f12a29cff) 
28. [Spring Boot 中使用新线程发送邮件](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f17f6f97a3448508b1fc418d7602b774e32983d02a8030d515bcc177c96308178041ecac2d4e52d83a012e54b4c79b8b34fe31a032f7f83e2ffa4a6c49556d1c5f951198ae966dc9d68ff8f6925c65ac7a3af11d76b31662164bbee9e573a5759581a274009e00db6784a935f99b8dcf4) 

### 2018.1.25 更新

本次更新版本：v20180125

本次更新主要完成了工资账套管理功能，页面在 **[薪资管理->工资账套管理]**

>本次更新也更新了数据库脚本，小伙伴们需要重新下载数据库脚本执行。

#### 相关文档：

29. [工资账套管理功能介绍](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f92ceda195eb15a7959bd8ab906c7ed894429ffcf159704287c8fe26099d045eadda2889deac14c54c7cef0d8227e4795107b43ec2dfd52b91edd11e9157098b833168f7d2aa0640e7e24e39e018e5c51dc4c3cd2cf98dbbdcf387a4440a8c92b) 

### 2018.1.26 更新

本次更新版本：v20180126

本次更新主要完成了员工账套设置功能，页面在 **[薪资管理->员工账套设置]**

>本次更新也更新了数据库脚本，小伙伴们需要重新下载数据库脚本执行。

#### 相关文档：

30. [员工账套设置功能介绍](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f9feb79291f93409116dabe095be7d7abde11fa571a912783fb0e306ea5a5a32ec57e14be6147b9eabe9854dc7df0dd31444dc786ee71d46b05bfcef541266de35b283bda715d609e95a5fd6ea62a10c0f48f0495727fb05d32cc388c7142bcf8) 

### 2018.2.2 更新

本次更新版本：v20180202

本次更新完成了HR在线聊天功能，页面在 **[Home页->右上角铃铛->好友聊天]**

#### 相关文档：

31. [在线聊天功能介绍](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f8506a6a718626a78652e914e15f3251fb03309321b741325109cc6a77d7392826f6e5b12cac6bf53312b02f2ca9d5c3f7972ac3a353bb3e42c9ad331d64100aef8ca9783b1545561865cb14701a8baad) 
32. [在线聊天功能实现](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f16723ca5eb5949183f0275c782922012e056880367a41bbc3182c4d065fbd21c30d40cefdda01154406024ff94b53653a058caa6359fb5044e1db2b26e0a58d3359c89512190eeef48ee54e7231bfab0) 

### 2018.2.5 更新

本次更新版本：v20180205

本次更新完成了管理员发送系统通知功能，页面在 **[Home页->右上角铃铛->系统通知]**

>本次更新也更新了数据库脚本，小伙伴们需要重新下载数据库脚本执行。

#### 相关文档：

33. [系统通知功能实现](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463605c4e1a30eae3ae8eba1073bd5572f3677c45786ff2cb2a59cb3da69123817be9289f895a7d2766cac2b695f9b87befe54485386d3bf38c07210154823b34f4f82b61683a6f4179d0cd0eaa4cc0d6848e7fe6e3f3f83a5fd4161ba17686aab) 

### 2019.12.22 更新

本次更新版本：v20191222

本次更新是一次规模较大的更新，整个项目的版本得到升级，同时引入了多模块、RabbitMQ 等技术栈。

#### 相关文档

34. [两年了，微人事项目迎来了一次重大更新](http://u.720life.cn/g/408fb60b53d11d245635ad5e8e8cd69785401e7ada4e463f461562aa24a27f060057b3f894097e45e3e8c2a9436fd7eaaf5b1f2f20e490fdddace68606eff37e) 

## 其他资料

关注公众号**江南一点雨**，专注于 Spring Boot+微服务，定期视频教程分享，关注后回复 2TB ，领取松哥为你精心准备的超 2TB 免费 Java 学习资源。

![公众号二维码](http://www.javaboy.org/images/sb/javaboy.jpg)

## 参考

- [vue-chat](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464fb1a8d1a9123c924235ed864317605b8380e58c7505e7e16b8de9b865e28bd4) 

## License

    Copyright 2018 王松

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
 


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)