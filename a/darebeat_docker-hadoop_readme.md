# docker-hadoop

## 准备软件包
1. [jdk1.7.0_60下载](http://u.720life.cn/g/91c0921eef61dd6be4a6bbe4a298a51e01aa854127de490c9b42a9b4ffb0a36dd82c1b3bdf013e927e58c3d3463dcd4e040d3d5fcb2e9392cb976287422cdebb) 
2. [hadoop-2.7.2下载](http://u.720life.cn/g/53129a24016149f29552d9e08488adb8dd71f6888b48c7d7ca8fa5e7ab5d4f6565fc3a3f31a237c4ffffd26058bc0660c4e4cf5fd77ef49978646f2256f179e3901263bdb7464831b103b622dac034ca) 


## 生成镜像
```sh
cd .
# 如果上面文件下载到工程目录，使用本地源生成镜像
# 本地源生成镜像
bin/build.sh local

# 在线生成镜像
bin/build.sh
```

## 部署容器
```sh
# 启动hadoop集群
bin/hadoop-cluster.sh start 3

# 卸载hadoop集群
bin/hadoop-cluster.sh stop 3
```

## 启动/关闭hadoop集群
```sh
$HADOOP_HOME/sbin/start-all.sh -y
$HADOOP_HOME/sbin/stop-all.sh

# 验证服务是否启动
$JAVA_HOME/bin/jps -l
```

## 网页管理地址
+ NameNode: [http://localhost:8088](http://u.720life.cn/g/e71094f6077cb9592da5b56893f0ad14f329ad135f5cccc4fbc590950bd80b37) 
+ ResourceManager: [http://localhost:50070](http://u.720life.cn/g/e71094f6077cb9592da5b56893f0ad144e2418ce71d68866c3276cce634bdc6d) 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)