# 分层的定时任务系统

## 使用技术
- 使用 .net Core 开发； 
- roncoo-adminlte 后台界面
- Quartz.net 做定时；
- nlog日志。

## 原理
设定需要定时触发任务的请求地址，请求的cron，处理成功判定结果，告警Email（sms方式需要自己实现）。
定时触发相应任务，判断是否处理成功，根据结果进行告警。

## 配置文件解析：
配置文件的配置说明请参考：[使用说明](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844de5d59641d111e2fcb58bbc90810c0160770e00e2eb89cdab876efd71e41658f8ad8aa6a5a29fc6e3d0227471349939d897b57ecff4bf8bb4bca0be8cda3d2ee8066f9f855aeca863893caf54295f096d) 

## nlog配置
详情见 _nlog.config_ 








 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)