docker-oracle-xe-11g
============================

Oracle Express Edition 11g Release 2 on Ubuntu 14.04.1 LTS

This **Dockerfile** is a [trusted build](http://u.720life.cn/g/9b9572a53e8f8aa37f1a576edb6fe3af90a6f0eec0678d1f099f1ad35bd1b6974d0b28e7a0a5ec5720efab3dae0ab208e1b7bf77bde6dcd3a499ef58f58d86ee)  of [Docker Registry](http://u.720life.cn/g/9b9572a53e8f8aa37f1a576edb6fe3af90a6f0eec0678d1f099f1ad35bd1b6979f7199afa5b5f64bb33aac22043aac94 

### Installation
```
docker pull wnameless/oracle-xe-11g
```

Run with 22 and 1521 ports opened:
```
docker run -d -p 49160:22 -p 49161:1521 wnameless/oracle-xe-11g
```

Connect database with following setting:
```
hostname: localhost
port: 49161
sid: xe
username: system
password: oracle
```

Password for SYS & SYSTEM
```
oracle
```

Login by SSH
```
ssh root@localhost -p 49160
password: admin
```



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)