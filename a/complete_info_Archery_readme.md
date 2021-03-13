 

#  Archery  

[![Build Status](https://travis-ci.org/hhyo/Archery.svg?branch=master)](https://travis-ci.org/hhyo/Archery)
[![Release](https://img.shields.io/github/release/hhyo/archery.svg)](https://github.com/hhyo/archery/releases/)
[![codecov](https://codecov.io/gh/hhyo/archery/branch/master/graph/badge.svg)](https://codecov.io/gh/hhyo/archery)
[![version](https://img.shields.io/badge/python-3.6.5-blue.svg)](https://www.python.org/downloads/release/python-365/)
[![version](https://img.shields.io/badge/django-2.0-brightgreen.svg)](https://docs.djangoproject.com/zh-hans/2.0/)
[![docker_pulls](https://img.shields.io/docker/pulls/hhyo/archery.svg)](https://hub.docker.com/r/hhyo/archery/)
[![HitCount](http://hits.dwyl.io/hhyo/hhyo/Archery.svg)](http://hits.dwyl.io/hhyo/hhyo/Archery)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](http://github.com/hhyo/archery/blob/master/LICENSE)
[![996.icu](https://img.shields.io/badge/link-996.icu-red.svg)](https://996.icu)

[文档](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466e64231d9d5bb681f75da8467f516962ce9556b71f9d9fad3d6fc9b87750a58a)  | [FAQ](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466e64231d9d5bb681f75da8467f5169625b4ff89f608cfdea1cb521067d4d6530)  | [Releases](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466e64231d9d5bb681f75da8467f5169623cd82d92d1a38bc4fb661a2a941c3514) 

 


介绍
============
Archery是[archer]https://github.com/jly8866/archer的分支项目，定位于SQL审核查询平台，附加部分DB运维功能，所有功能都兼容手机端操作，[功能列表]https://github.com/hhyo/Archery/wiki/功能列表

开发计划
==============
https://github.com/hhyo/archery/projects   

快速开始
===============
### 系统体验
[在线体验](http://u.720life.cn/g/8bafced76569f2e962730d25e9b78c465d8472e12b5a6a9518f2dd2d23f8d3b2)  
  
| 账号 | 密码 |
| --- | --- |
| archer | archer |

### Docker
#### 准备运行配置
具体可参考：https://github.com/hhyo/Archery/tree/master/src/docker-compose

#### 启动
进入docker-compose文件夹

```bash
#启动
docker-compose -f docker-compose.yml up -d

#表结构初始化
docker exec -ti archery /bin/bash
cd /opt/archery
source /opt/venv4archery/bin/activate
python3 manage.py makemigrations sql  
python3 manage.py migrate

#数据初始化
python3 manage.py loaddata initial_data.json

#创建管理用户
python3 manage.py createsuperuser

#重启服务
docker restart archery

#日志查看和问题排查
docker logs archery -f --tail=10
/downloads/log/archery.log
```

#### 访问
http://127.0.0.1:9123/

手动安装
===============
[部署说明]https://github.com/hhyo/archery/wiki/部署#手动部署

运行测试
===============
```
python manage.py test -v 3
```

依赖清单
===============
### 框架
- [Django](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304631317e99b10ba61ff8f183f112f4ff05) 
- [Bootstrap](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465a8160a390414e5887ea7b27f65f8894df8a88b45f3cfc9c4098552eeb42db05) 
- [jQuery](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463ed6ba350bf5845433cef188b94c91ed) 
### 前端组件
- 菜单栏 [metisMenu](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468ca112927ad45fa04b8c486dad7d4d20f8866dc3e98c6d018c2fd86214ad37fd) 
- 主题 [sb-admin-2](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304668462bdfb0faad9952aec6b9e539f845d55f3d82f6a711e0d2f61674f669cc12f5a44356123a67a650d94cbea1bb2dbc) 
- 编辑器 [ace](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464793796175e00e929d950d0bfd744319) 
- SQL美化 [sql-formatter](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466a20804f98cfbb4005f9dc3c3ef354abba08e02df5cea0e567d4ea6ac6ccf4aa) 
- 表格  [bootstrap-table](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f2f423513f085635331b1265a6816cdb36af265fd434a72654ac1ef575ab42cc) 
- 表格编辑  [bootstrap-editable](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464a5338df28a2cb1838f5389ea29c9012b1d86b289cb1d729ed92e2e6c7f9a77c) 
- 下拉菜单 [bootstrap-select](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046107f2a1b1a1c6ecace1ae33895cc5b7bcad9b7ed8184775e73fbf164a45558916dbf3d6e31cb530f691224017464b0a1) 
- 文件上传 [bootstrap-fileinput](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460b83579f878ca7cbf41bc62cbc2cc8c5829694a69bc5084a4b8e178ab210b639) 
- 时间选择  [bootstrap-datetimepicker](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304660dd6aa3deb0486e17d8b0e50a4089b527352afbc0d8b5e221d41a546e91d1ee06254f3c9a4496fd878a292b9ae09f4e) 
- 日期选择  [daterangepicker](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304613a2b7d720261b0eadb225528e6ba1d5687a6820b6fdeadc7750326d132c3b76) 
- 开关  [bootstrap-switch](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304608328e195dc45405070a683c9ea8a9c5b911f6fd9006154da9fbd92fa1abdf7f) 
- Markdown展示  [marked](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460d08562e45ca9708e77b12bcfd2c92231a8beafc447934987406c1d5d8caa713) 
### 服务端
- 队列任务 [django-q](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e39022b11daaf57f88682b997a4858c2cc0250fa3859aec952cde190c08c48a5) 
- MySQL Connector [mysqlclient-python](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304674bc30234c2ddcee33128527ff668e7b3730e1e03ab5780bf1a5ddf2dff23de8) 
- MsSQL Connector [pyodbc](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b4b788506065127bdc308837a57c49a53a9c499c1edcb5e87f1aed06d5fa386b) 
- Redis Connector [redis-py](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304660a26e47bdcb5a9ca4de5bcbc1b21b4911ea8b94b07c18904675deca68716aaf) 
- PostgreSQL Connector [psycopg2](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463fbc2afdff6a4dc1ab02d4aa45c15df596189ae80cbae564679b9a0ac38e9132) 
- Oracle Connector [cx_Oracle](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304682d6ce39357b920610862684a8a4c0f052f940901d11170e4fe98a7b90da9cec) 
- SQL解析/切分/类型判断 [sqlparse](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465a7ede01d754525a74c5e1018657690cc7fcf9ae1056c6bbf4c212c22a135bcc) 
- MySQL Binlog解析/回滚 [python-mysql-replication](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466668b30ec86a32e800d9b712bc3418df12bbd171dec64f2729712e2c23cb11381a376fee1a92718555d456bfa7bd7af8) 
- LDAP [django-auth-ldap](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464b276f96cc06b35d08f700f38c19b0c7b641058b588ea4e4afadc5104833307209bd049ed2ea4028c9e79fe4e0e802a6) 
- 序列化 [simplejson](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468514921e81bbc07e0c1322e6e54041ea22dad69dda416a1cfc53815a5d4deec3) 
- 时间处理 [python-dateutil](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d77cde5806c82f58d65c4c6cea0f6ac33e4e39c0e6faf89394635c6e6ad75963) 
### 功能依赖
- 可视化 [pyecharts](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304615d0c13b82f18f669c2056ed8e8bc2b4037829517cf95f6d9940b61363d55938) 
- MySQL审核/执行/备份 [goInception](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467b14419cab778a72503c8a89786468ab7198e313e0bd6b98ff0535d05f38483b9ae187991731b2052142de49c23ac9e2106b12da97cca38ff205915b638716619a7af97d50801a08363293db9c1c475a) 
- 数据库审核 [Themis](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466a38f5fd0a0e7b88c23679293a289e16fc31b21dc208047137cbc9dc530283a8) 
- MySQL索引优化 [SQLAdvisor](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b789abeb984c455150cb582c6aebce4fe8f64a3c1b2a158cec3d0b4a14be327b) 
- SQL优化/压缩 [SOAR](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d8acf43e8c5c05ca18cafe0e48526656) 
- Binlog2SQL [binlog2sql](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046560c51dcfd42ebaa9ec1d98099ece4e71d8dc7f5502f732fd0530faa3b9299e4) 
- 表结构同步 [SchemaSync](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304676edc4096b476f97ec2757c8941d57970b1d2eb0a7be39ab5035b573d6d3fc34) 
- 慢日志解析展示 [pt-query-digest](http://u.720life.cn/g/6e6d6140da0b4f68f288d6ba7592ad81b3f6ab03143418ef0794692de0662732485f9d600b64a7a8876d8e1ca7055026bce17bf4eee1bdd9be28485255713c5c5c7700a09bf3a04137e9a17a46ea3163624ceeec1641f96be18c74075cde767770658ce58b83bef7040b394cf3408ca92b70bf46aeb369a1c89a68969a8109f5) 
- 大表DDL [gh-ost](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468f3b4c771ae89c849cbc917a52941008f35a2a824cf7dee020deed6c06b03b8c13b8411b7070b73d8634a80f9a8115143c62930ba044e894acde06f2045b9c8ab775afd963e4a572d32c370a2f5b01ddf20cd7cf8e480bf49051627e9d8253615506f925b184336de0a7441f8b0ffd29bd5c6a797d3cab38a4f9062a74c7960b) 
- MyBatis XML解析 [mybatis-mapper2sql](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304638dcf02578c3eb7bd04fbeaa454cfd1cd34725e9ec34601a26eae489bb1133d4) 
- RDS管理 [aliyun-openapi-python-sdk](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463acc10ac40ebe392ae83d014e0e2b286a3077b1d19a38d5e6264ee831c4b5191ce6d9580325d38534fe3a99eec110150) 

贡献者
===============
[![](https://sourcerer.io/fame/hhyo/hhyo/archery/images/0)](https://sourcerer.io/fame/hhyo/hhyo/archery/links/0)[![](https://sourcerer.io/fame/hhyo/hhyo/archery/images/1)](https://sourcerer.io/fame/hhyo/hhyo/archery/links/1)[![](https://sourcerer.io/fame/hhyo/hhyo/archery/images/2)](https://sourcerer.io/fame/hhyo/hhyo/archery/links/2)[![](https://sourcerer.io/fame/hhyo/hhyo/archery/images/3)](https://sourcerer.io/fame/hhyo/hhyo/archery/links/3)[![](https://sourcerer.io/fame/hhyo/hhyo/archery/images/4)](https://sourcerer.io/fame/hhyo/hhyo/archery/links/4)[![](https://sourcerer.io/fame/hhyo/hhyo/archery/images/5)](https://sourcerer.io/fame/hhyo/hhyo/archery/links/5)[![](https://sourcerer.io/fame/hhyo/hhyo/archery/images/6)](https://sourcerer.io/fame/hhyo/hhyo/archery/links/6)[![](https://sourcerer.io/fame/hhyo/hhyo/archery/images/7)](https://sourcerer.io/fame/hhyo/hhyo/archery/links/7)

贡献代码
===============
可查阅主页的开发计划以及依赖清单，在对应issues中回复，或者直接提交PR  
贡献包括但不限于以下方式：
- Wiki文档（开放编辑）
- Bug修复
- 新功能提交
- 代码优化
- 测试用例完善

问题反馈
===============
[Issues]https://github.com/hhyo/archery/issues)是本项目唯一的沟通渠道，如果在使用过程中遇到问题，请先查阅文档，如果仍无法解决，请查看相关日志，保存截图信息，给我们提交[Issues]https://github.com/hhyo/archery/issues)，请按照模板提供相关信息，否则会被直接关闭，感谢理解



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)