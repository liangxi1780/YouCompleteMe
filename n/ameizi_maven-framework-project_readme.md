# maven-framework-project

[![Build Status](https://travis-ci.org/v5developer/maven-framework-project.svg?branch=master)](https://travis-ci.org/v5developer/maven-framework-project)

这里不仅生产代码，还搬运代码


# 项目描述


较上个*[maven-framework-project]https://github.com/sxyx2008/maven-framework-project)*过去已经一年多了，在上个*[maven-framework-project]https://github.com/sxyx2008/maven-framework-project)*中，由于没有采用maven的继承和聚合。在介绍各种框架时配置杂乱、不易梳理。故再次有了这个示例项目。同时也意味着*[maven-framework-project]https://github.com/sxyx2008/maven-framework-project)*将不再继续下去。

因之前帐号已经存在*[maven-framework-project]https://github.com/sxyx2008/maven-framework-project)*，且这年头github上也流行`Organizations`，故抢注了`v5developer`这个组织名。该组织下目前有三名成员*[v5china]https://github.com/v5china)*、*[ios8]https://github.com/ios8)*、*[sxyx2008]https://github.com/sxyx2008)*)当然都是我啦。如果您有什么意见和建议，欢迎您的加入。

该示例仅仅只是一系列教程集(不仅限于Java)，不做一个完整的项目。不会像*[springside4]https://github.com/springside/springside4)*那样强大。当然如果有你的加入，我想她也许会的。

该项目将长期维护下去，也算是从业以来经验和知识的积累。

这里不仅生产代码，还搬运代码。欢迎*[fork]https://github.com/v5developer/maven-framework-project/fork)*和*[star]https://github.com/v5developer/maven-framework-project/stargazers)*

如果你有好的示例项目或教程可与我联系。我会以`git submodule`的方式添加进来，一来是尊重原作者的劳动成果，二来实时与原作者库同步，保持最新。


# 项目托管


*[https://github.com/v5developer/maven-framework-project](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c0a90a6909160e90c88913f1e244da7e5f965d49fde703e5c96d86abe682003808c754f1667681e28acc77d88a58f445 

*[https://git.oschina.net/sxyx2008/maven-framework-project](http://u.720life.cn/g/3e7e8f170da15d1979f4c6b1321cc36b9ee036aaf3cad460a2944f2c6fdc905b66cf713218ded85eb1cff9f8cc32dd19165e362921d514a83cc5418b77eb07be 

*[https://github.com/sxyx2008/maven-framework-project](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046fe1283520ce804726afce1a0eac98538ccfede3931e3a80b0730d0e523d1d705128f1ea780276705ea572f85f89d4d2e  *较早版本(已不再更新维护)*


# 克隆到本地


该项目争取做到每一个示例项目都可以直接运行。各示例项目之间不相互依赖。由于提交了一些参考书籍*[reference]https://github.com/v5developer/maven-framework-project/tree/master/reference)*导致目前体积较大。因此克隆时间较长，请您耐心等待。

项目使用了`git submodule`，因此克隆后需要执行下面的操作(在项目根目录中，与.gitmodules同一目录下)。

```
git submodule init

git submodule update
```

具体用法参照*[http://git-scm.com/book/zh/](http://u.720life.cn/g/8cc9dac74485932e01bea76468c18214b755e8b836f468e49629c234ce265d7b 



# 酷站分享


该部分内容主要分享一些本人收集的与Java有关的站点。主要包括Maven Repository、Maven Plugins、Java Tutorials。欢迎补充!


## Maven Repository

*[http://mvnrepository.com/](http://u.720life.cn/g/74ab557d7a5541b23b23229f8a92929d3e9404528c9d80590eb9306431a69b62 

*[http://search.maven.org/#browse](http://u.720life.cn/g/686169b320f6084fa4aea25a9bdaff1c9baee8d0f25ec6441d6b9237fb51ef89dd63b06e08c30c96a9309abd960a5809 

*[http://mojo.codehaus.org/](http://u.720life.cn/g/e16d7a53f6bcae8206388f89a07b64e81ed52f1a0f43817ff9d6380a49653a7c 

*[http://dev.nightlabs.org/maven-repository/repo/](http://u.720life.cn/g/3d7d621754a903cf07c0ccab9e1a06c0118e579500e457e01ed81a39f0849083966d1957547cf2d4589117b8bd96e3f34e0cf1280b06541f3b78f94a37dc907e 

*[http://opensource.kantega.no/nexus/content/groups/public/](http://u.720life.cn/g/ba059582536a397f7c573b87c8bea6477992ce3b7260df8bced4b6868061527cd5f71af07c08b3b8478e60c7cd7f9b5a747fff34b12255d7483b8e6aaf8482d0 

*[http://nexus.betaconceptframework.org/nexus/content/groups/public/](http://u.720life.cn/g/4a2a35141f9202171c3dc17da732081bd859852913bd618582af07535e1acb39bf8a91774c3341c13fa2d83a2f2b7b346fdbd56555a6afe9ea1be129105c0dd4cbe635c2472b066433533bde79826769 

*[https://app.camunda.com/nexus/content/groups/public/](http://u.720life.cn/g/4a61c58b7b60082166f9b1a0f5f19728aa5dd0be9f205c3ea15be47695750e2c0359ed1c044376742e848a19ad7770ab3d35bf49cb91999c8fe8e5f4dd7c3e65 

*[http://repo1.maven.org/maven/mule/dependencies/maven2/](http://u.720life.cn/g/dbe7e997259d1c03ff78b9040174184d6bd4bdcd798cbc8ed5f172233a4284bf69913581801396dfef716ca170dd8a52149526f611c7ab545f71f8b81151ee0c 

*[https://maven-us.nuxeo.org/nexus/content/groups/public/](http://u.720life.cn/g/2cbb4e995d646063fd6720dc3e5374278a5282a9350b7403038a645a299fc82c5d6e2a7e55293d8854be54bffa611fe3913a142cebbc87a32a187344db0e78cf 

*[http://repo.yongtai.com.cn/nexus/content/repositories/public/](http://u.720life.cn/g/53368294a69970660b4824eabd43e6e5b46f2c245fc3f90df4c48be123284055dc6861e461df2eb9a0c5b3a0c964ef447048f5bb0b7e591138c9709967421821 

*[https://maven.alfresco.com/nexus/content/repositories/public/](http://u.720life.cn/g/b3662bfecfb8f4ddee6ceb91c7e925c05b72749c65ac18859a90eb68847772ccb0a35e70ba5461fa2d41328f230c2f98465be37d47e7ebe28ef3b9ab41c07508 

*[https://repository.jboss.org/nexus/content/repositories/public/](http://u.720life.cn/g/4c86c7768832f9860ee70c4b92b737940638b4c990a3b721374c7f839d571baa5874257c96b80f0383da9d41f63a418db548cff13380868e7564de0617d475b21a36c880af09422bf9da4c51dcab9f0f 

*[http://mirrors.ibiblio.org/maven/mule/dependencies/maven2/](http://u.720life.cn/g/877fad5ef1a48b04879ac42ba419e3123dcbc7db1e83fa2b61ff1a8e85d96d3de6f7e95d2c7e31b8b9cb65fad5e0c2fbeb3f31d98787061bee8e5bc83583b509 

*[http://repo.squashtest.org/maven2/releases/](http://u.720life.cn/g/5b958053155d07bd061d7df1a5a0b93d160934c7aa8bc381b08c9d2f49eb1ee35674b51004cbe41560fde243814372b7 

*[https://repository.jboss.org/nexus/content/repositories/thirdparty-releases/](http://u.720life.cn/g/4c86c7768832f9860ee70c4b92b737940638b4c990a3b721374c7f839d571baa5874257c96b80f0383da9d41f63a418d6d721e981dde410030242bd06cc58f30d2763fd397c234be9dd6b69290107748 

*[http://repo.spring.io/milestone/](http://u.720life.cn/g/3db1a62541b2bab91d57310ae86c35fce83593fbdfa93060f950096418160788bee9d6c1572de398ff1ef5aada8496f9 

*[http://repo.spring.io/snapshot/](http://u.720life.cn/g/3db1a62541b2bab91d57310ae86c35fca22dba305920156e51a73ca3960b1f0b982ece74fb208ddb61b8a1ebad6f6a99 

*[https://oss.sonatype.org/content/repositories/sourceforge-releases/](http://u.720life.cn/g/bf36fb3cc39acf1dafaeb17e7325b567221904f4def9871c162f0c7f256ff3de7c95680a588e8cb84d8cb7911b9e89e90ffd73e2ec62f2a73ac2000acbefc8546adf0162be57a51bd6be954aebece921 

*[http://maven.in.softeu.cz/nexus/content/repositories/public/](http://u.720life.cn/g/8fbb8311a6a1acf0a18544f50d8b65184a2fe6f16ca60438e26f86e41740507dce8527e40e902b4d364272f8249bfa2805330f0fbc1298a25540d22cfe870e25 

*[http://maven.oschina.net/content/groups/public/](http://u.720life.cn/g/d0811b5e924932d6c7275580d9e0603e40900d14678188c8a6cd1484e9fec3520786df5b4bdd8f19b033949c9641c1e83ee1a1e616735a6b1a1271f95affaac4 

*[http://maven.kaifazhe.me/content/groups/public/](http://u.720life.cn/g/11c109c15f569a1803c075f909ed00155d61461d16acb61401b1965472d14af903af248bd4984ebc924c21d87cfb08dfed204326211b2e95249467ae7c788960 

*[http://repo.spring.io/release/](http://u.720life.cn/g/3db1a62541b2bab91d57310ae86c35fc7040608773738b5d5c0aede96a6c443e 

*[http://mirrors.ibiblio.org/maven2/](http://u.720life.cn/g/877fad5ef1a48b04879ac42ba419e3123dcbc7db1e83fa2b61ff1a8e85d96d3db5f7900febf43edc6bd8ba483cc4ff0e 


*欢迎补充*


## Maven Plugins

*[http://mojo.codehaus.org/](http://u.720life.cn/g/e16d7a53f6bcae8206388f89a07b64e81ed52f1a0f43817ff9d6380a49653a7c 

*[http://tomcat.apache.org/maven-plugin-2.1/](http://u.720life.cn/g/27381b9b9aecbc3251722641d01ac5ed97fa90651b6a921e479334a713015733e658bb85b9f98d157b163534c69f154f 

*[http://maven.apache.org/plugins/index.html](http://u.720life.cn/g/bc840264f6cc23df0a8935b6f2922fec1ac8a16d8d5968e321b58b4e968dc4df0b3014d9bf99c30c4abadfa7f9285aa5 

*[http://docs.codehaus.org/display/JETTY/Maven+Jetty+Plugin](http://u.720life.cn/g/2088ca8750dd43b513063734e5a11f9b4f028451d979ef3dfe051ad7cf80aa9dee604d32339baa01289e5b40a9f8d3b28d31d653e0ea74c6e08a60ffb6ce86d8 

*[https://docs.jboss.org/jbossas/7/plugins/maven/](http://u.720life.cn/g/9846651c171764a753f089891ac0431ae0b0a6ceb3699a8f9c60a26457931dd269ab400c8a04a5177c5c600b868f069d80ea85e7addc7d32f7f51586a5539c77 

*[http://mojo.codehaus.org/jboss-maven-plugin/](http://u.720life.cn/g/e16d7a53f6bcae8206388f89a07b64e8528aa8aa9f78374bc91f5d573e7eb787b175ab412a4d0a0d17a62efbeb81780f 

*[https://maven.apache.org/plugins/index.html](http://u.720life.cn/g/8757c0ea56dfb5a954fb8252a8aa377bce9f16c09af59a9472f6ef4c2dabc1e33e06c6fd9fe1a6653595018a68d5b92b 

*[https://code.google.com/p/maven-db-plugin/](http://u.720life.cn/g/b1f73db7c3bd88ab3d1af6161318928ee8e0cf1dff16747fc53981bb5336611b67a69f6c01fdec4cb74c28887cf1d65d 


*欢迎补充*


## Java Tutorials

*[http://www.mkyong.com/](http://u.720life.cn/g/992bae0e6343f71f1df8216197a653ba9c1bc187ae3559bcef4c703ae96cad4f 

*[http://www.dzone.com/tutorials/java](http://u.720life.cn/g/749c641cc4b3864b701ef5132e52d5be613bdccd9454a74180054725f15e598110ab4b698cda071311092957a292fba5 

*[http://viralpatel.net/blogs/](http://u.720life.cn/g/5b4ced8bceda0ed0748b9066f01670e0323aee163a2bb227902912c858316a77 

*[http://www.hascode.com/](http://u.720life.cn/g/6deec11294fb9ee9f359a5a54606d4bc7566034943d3c3435aa6ddcab119f02b 

*[http://www.journaldev.com/](http://u.720life.cn/g/da80745ba081d53027cc349beeca5b6d051088a9cc00f519489da65949a0ac35 

*[http://verylearning.com/](http://u.720life.cn/g/da8d39b417ad6b02157cd0eda1428cd59afca6302f5635408f545c3b41876f50 

*[http://www.roseindia.net/](http://u.720life.cn/g/f5fc263a3306dc9bc3e1d167febf6d36cc10026d102e0081e01c9106ff5c9eea 

*[http://docs.oracle.com/javaee/5/tutorial/doc/docinfo.html](http://u.720life.cn/g/93f16c577429ee5ee9d7562025a6bc74f8b1f90cd233df2c7a80fed6ca6d96a78f5b94d50aed063eadd4cc74391d8de260b23a508ceaf935f1a8348d39dd8ec6 

*[http://www.mastertheboss.com/index.php](http://u.720life.cn/g/8002fe6a9fd2aa89c2fb393ac9bc944cbcfc6a4a572ac3d5d170e87a2796cf732e53853bce3fa7614e1f884671198cfc 

*[http://www.vogella.com/](http://u.720life.cn/g/868d4a1f5e1b043a2fc7e46582fd0eb55e81117979898119258f9f35e48b8ead 

*[http://www.solrtutorial.com/index.html](http://u.720life.cn/g/527ef4e8af4d87917d8ba0f1548df8953960313dfc4ec302f33b2f7a2e8552dcdaa9f73cf494188b9d9719066c44b040 

*[http://refcardz.dzone.com/](http://u.720life.cn/g/45c6f3c68b481e43935ab3020661d75e92e4c893924184df9fb427a8dbc8e10a 

*[http://www.springbyexample.org/](http://u.720life.cn/g/a50b704f804c379c2fdcea5b9d5061efe3ccc2016ad9cc1e0f263d8bdfa7409931cb2bbb59c7b9d38ad8ca01212adfc8 

*[http://www.coreservlets.com/](http://u.720life.cn/g/343f786a6d8a206d0e14380b95512bf21fdb7c11ba6c7b6064f50eadd3ad1e96 

*[http://www.programcreek.com/](http://u.720life.cn/g/2ad90f05597d3a3bcb7c2fe384a8b178fda2a139682d14de771f22ab99c5a494 

*[http://www.mortardata.com/](http://u.720life.cn/g/6543e95afbd5a988cdc6bed4f735666681e12368e04708f320fc7773ad4fc2ba 

*[http://www.pluralsight.com/training/](http://u.720life.cn/g/a3e60e366918a41fdd4a0f31b233313b31dc8ff5d1f1859c3d6d55b28f635d218aa6f3bbb5f36098e730df01c2589707 

*[https://tutsplus.com/](http://u.720life.cn/g/5c00c0e455aa638c072c6c76b2028772c46a5266eab49b7f29ed14d3c229a4ac 

*[http://www.mossle.com/docs/activiti/](http://u.720life.cn/g/4afd0ef7492f8f79aea45d525fb01d1975b8d94d8a3126d9704dd248358edba07fc0bb47608ff8567ca4d2aacac075de 

*[http://blog.sae.sina.com.cn/](http://u.720life.cn/g/214c14e105523267f0e8a6ae9eceb2f08ace0ee6eeca5568b456a6def44065c9 

*[http://www.baeldung.com/](http://u.720life.cn/g/7fef8247dbca153f4bd73eca189b9efd5eab2c11ea3ff19cf4c1e0cd84585cbd 

*[http://www.javacodegeeks.com/tutorials/java-tutorials/enterprise-java-tutorials/](http://u.720life.cn/g/607f810a2571cbcac0df36454ac513a1a0384f9977e3339484c534bffb9922986306aae442565ee9fcd377359e6f6b9e6b92a3d5268f88b26b4c9f7c893fe3e2d674373a5a5807f734090c2963aff7c0ad4bcac21c71e724020c37e04ae85e60 

*[http://www.tutorialspoint.com/](http://u.720life.cn/g/14e508125ebaea3e2870690ce4084e3d13a3f137365513ad4ec7f1f8c94c5e76 

*[http://www.javaworld.com/](http://u.720life.cn/g/e3bc52bb11bb86b4641bf13db969810438bc2c5dd597b9da731ce7a7d0dbfe45 

*[http://www.codejava.net/](http://u.720life.cn/g/3ebd8e36254dd5f7aecb16c855200777bb02b4ea640450b239490f6e9f718f7c 

*[http://www.javatips.net/](http://u.720life.cn/g/cf053264547635984d2e7c7493232faecf331db194005612115b09cae0026d62 

*[http://www.codesuggestions.com/java/apache-commons-dbutils-tutorial/](http://u.720life.cn/g/93fbcec597e5d6f992d638e5137b875452e1222bed8b2a42aa6427b58ba1d3f1948977f1672e9c605566636d7a6dd9ee342127e4417db460496aea2c879ac87fbfadb0aee1d3f0eb8e1e554e9148abc9 

*[http://www.javatips.net/blog/2014/03/apache-dbutils-tutorial](http://u.720life.cn/g/cf053264547635984d2e7c7493232fae47cc08cb0bf0cae7dba5e689737d4119d607715d63d79136dfaa724225289ab71fe016857659af3f3604e6230a25ea63 

*[http://www.javabeat.net/](http://u.720life.cn/g/190698060ffa7ea6d4568839295e64258cce3ce20b184847c10e79da6eea2339 

*[http://www.concretepage.com/](http://u.720life.cn/g/fa679b022086784fbe5345241bb7a55d5dbd8b407faf1ff79e474679f45e77d0 

*[http://www.petrikainulainen.net/programming/spring-framework/spring-data-jpa-tutorial-part-two-crud/](http://u.720life.cn/g/ea839c90ad670c12865ccf94b0baed7a69e1ab1f501107cf002f5b5c20037c86df5ca72415d27499c43d9789c78fc633cc30eff6a421fb3577c7806f21023894a04b290255b490f7e85258eb0e7a4be260a7d51dd7fdb3ffe6b1614724849ab4ce376dccd35932214798b857c9e9acdf 

*[http://fruzenshtein.com/spring-jpa-data-hibernate-mysql/](http://u.720life.cn/g/188796177ce5fbe15b9bcd88e67e71849205972a1e9d97ca58c6292796cafaa32d41887f33d1d27e1c41a98c24f0d43876da1f80d7349ec8b9cc5093aad46a67 

*[http://howtodoinjava.com/](http://u.720life.cn/g/ab2871ea366f9008a62d5ed70483545f7f0dc6a43535b371eedc4982a456b268 


*欢迎补充*



# 与我联系

* QQ:*184675420*

* Email:*sxyx2008#gmail.com*(#替换为@)

* HomePage:*[aimeizi.net](http://u.720life.cn/g/0b46c123f120d0047f3d1e028e1ae8ed338f6a1e150a1e7e9dd4086ee568cb0b 

* Weibo:*[http://weibo.com/qq184675420]http://weibo.com/qq184675420*荧星诉语

* Twitter:*[https://twitter.com/sxyx2008](http://u.720life.cn/g/5ea88169c4a0fbd169233d52478d54fe3fc4d55b6adfad32d905933a3cde1f7a 



# License

MIT

Copyright (c) 2014 雪山飞鹄



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)