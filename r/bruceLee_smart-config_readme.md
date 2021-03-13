#smart-config
基于smart-boot构建的配置中心系统，以Redis作为数据持久化

##系统依赖
1. Redis
2. NodeJs(本人的node版本为5)
3. Java8

##项目部署
1. 修改application-dev.properties,配置(redis地址`spring.redis.host`)、(redis密码`spring.redis.password`)、(缓存名`redis.cacheName`)
2. 运行Bootstrap.java启动服务端
3. 目录切换至htdocs,并执行readme.md文件内的命令
4. 在htdocs目录下执行gulp start,打开浏览器访问http://localhost:3000/build/tenant.html
![键值对](kv.png)

![租户](tenant.png)
##推荐项目
- [smart-socket](http://u.720life.cn/g/3e7e8f170da15d1979f4c6b1321cc36bfd030e1b2558231b27bd05e4906159079c81dea6217c5d7843eaab09acad458c) 
- [smart-sosa](http://u.720life.cn/g/3e7e8f170da15d1979f4c6b1321cc36bfd030e1b2558231b27bd05e490615907c67702e7e2457c522a7e112800983fc2) 
- [maven-mybatisdalgen-plugin](http://u.720life.cn/g/3e7e8f170da15d1979f4c6b1321cc36bfd030e1b2558231b27bd05e490615907e8bb0e140cba03427f78e8618ef490adee8f6f1944e75f246eb6c6353cf9d6e0) 
- [smart-boot](http://u.720life.cn/g/3e7e8f170da15d1979f4c6b1321cc36bfd030e1b2558231b27bd05e490615907b14d4e30d5cb1432f67a5ce85d016f0a) 

##关于作者
Edit By [Seer](http://u.720life.cn/g/b1220a2a2f52f62e970b7e94fba7e966f1e27694fc29b34ffcdbdc016148415e8d45a497bb4b76ecd0930b0244cd9b33)   
E-mail:zhengjunweimail@163.com  
QQ:504166636 
Update Date: 2016-06-03

##捐赠
![微信捐赠](wx.png)


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)