# Deploy Prometheus Stack with Docker Compose

## 项目介绍

Deploy Prometheus Stack with Docker Compose

## 软件架构

![Prometheus Consul Grafana](imgs/PromStack.png)

### Prometheus

[Prometheus](http://u.720life.cn/g/9a9b751b4176dd00a09dcbac56dd9284ef18eb97e63021e13b4bd63c370094bf)  是由 SoundCloud 开源监控告警解决方案，从 2012 年开始编写代码，再到 2015 年 github 上开源以来，已经吸引了 18k+ 关注，以及很多大公司的使用；2016 年 Prometheus 成为继 k8s 后，第二名 CNCF(Cloud Native Computing Foundation) 成员。

CNCF announced the graduation status of Prometheus at the PromCon 2018 conference.

Prometheus, an open-source monitoring system and time series database, has become the second project after Kubernetes to graduate from the Cloud Native Computing Foundation (CNCF).

2018 年 CNCF 在 PromCon 2018 上宣布 Prometheus 从 CNCF Graduated ，这是继 Kubernetes 后第二个 Graduated 的成员。

![prometheus architecture](imgs/prometheus-architecture.png)

#### 它有什么特点？

+ 自定义多维数据模型(时序列数据由metric名和一组key/value标签组成)
+ 在多维度上灵活且强大的查询语言(PromQl)
+ 不依赖分布式存储，支持单主节点工作
+ 通过基于HTTP的pull方式采集时序数据
+ 可以通过push gateway进行时序列数据推送(pushing)
+ 可以通过服务发现或者静态配置去获取要采集的目标服务器
+ 多种可视化图表及仪表盘支持

### Consul

[Consul](http://u.720life.cn/g/93f8ac2267aa71b18ddaa3e2d05eff7dd02683cb51b1568269211bbb6cfbe143)  是一个分布式服务网格（ service mesh ），用于跨任何运行时平台以及公共云 / 私有云连接的服务发现、服务分割和服务配置。

关键概念：

+ `API-Driven` 对服务定义、运行状况检查、服务授权策略、故障转移逻辑等进行编码和自动化。
+ `Run and Connect Anywhere` 跨任何运行时平台和公共云 / 私有云连接服务。将服务从 Kubernetes 连接到 VM （ Kubernetes to VMs ）、容器到无服务器（ Containers to Serverless ）功能。
+ `Extend and Integrate` 在任何基础架构上配置群集，通过代理集成连接到TLS上的服务，使用可插拔证书颁发机构提供TLS证书。

### Grafana

_The open platform for beautiful analytics and monitoring_

[Grafana](http://u.720life.cn/g/b675da847faf899dd7953a9eae0a65acb6dcf30f8d98a4ba9ad0a6e740f2a45a)  是一个领先的时序数据（ time series ）分析开源软件，同时提供通用仪表板和告警功能（ Grafana4.0 及之后版本）作为 Web 应用程序运行。它支持 graphite ， InfluxDB 或 opentsdb 作为后端存储。

## 安装教程

1. 创建目录： 

    + `/usr/local/prometheus`
    + `/usr/local/grafana`
    + `/data/nginx/logs`
    + `/data/nginx/conf/ssl.d`
    + `/data/nginx/conf/stream.d`
    + `/data/nginx/conf/conf.d`

2. 复制配置文件到指定目录，详见 [docker-compose.yml](docker-compose.yml) volume 结构

3. 启动服务：

```
# cd ~/PrometheusStackDockerCompose
# docker-compose up -d
```

4. 卸载服务：

```
# 完全卸载（删除 volumes ）
# cd ~/PrometheusStackDockerCompose
# docker-compose down -v
# 删除容器，保留数据（保留 volumes ）
# cd ~/PrometheusStackDockerCompose
# docker-compose down
```

## 使用说明

1. 配置修改：

    + 修改相应的配置文件
    + 重启 service ： `docker-compose -f ~/PrometheusStackDockerCompose/docker-compose.yml restart  `

2. 注册 Exporter 到 Consul 以供 Prometheus Server 发现并拉取 metrics 数据

比如将

```
curl -X PUT -d '{"id": "host1-node","name": "host1-node","address": " ","port": 9100,"tags": ["node_exporter"],"checks": [{"http": "http:// :9100/","interval": "5s"}]}' http:// :8500/v1/agent/service/register
```

其中 `-d` 参数 `json` 数据内容为：

```
{
  "id": "host1-node",
  "name": "host1-node",
  "address": " ",
  "port": 9100,
  "tags": [
    "node_exporter"
  ],
  "checks": [
    {
      "http": "http:// :9100/",
      "interval": "5s"
    }
  ]
}
```

```
cat temp.json|jq -a
cat temp.json|jq -c
```

3. 将 Exporter 从 Consul 中移除（同时回从 Prometheus Server 中移除对此 Exporter 的 metrics 数据的拉取）

```
# 将 service monitor-node 移除
curl  --request PUT  http://localhost:8500/v1/agent/service/deregister/monitor-node
```

*. 访问 grafana

    + 浏览器访问： https://gf.domain.name
    + dashboard 可以浏览器导入，插件安装具体操作见[官方文档](http://u.720life.cn/g/94cc14904ee11ccad73c1ee672975e3d0cdb3345780c4a72ca9e9eb9009109106dec985ddc18a23d5f456fb5b51b79b8) 

## Supported Exporters

+ [node_exporter v0.15.2](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6eb6f01a1a1d0f5839e118ffb7a6b6134ade959c3029127f1087beabda2cd59c82bbd0cd111111bc51d4ae6ce4839a391a) 
+ [mysqld_exporter 0.10.0](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046dfc24fcfc72acb14eca5ab1056d6407f832763c47088f0c880cf03033d959be1863a66f50392dfe0acc6c26f3ca0403faf899f35ce9f5e36f4c091fb0a13f570) 
+ [redis_exporter v0.21.0](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460b81f4593d96d9e4f2480b304d057e59eca651cb71723682f37aceb967a493095dd7ecd410862c053b3f23bbc4bd1b56) 
+ [nginx_exporter](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046381a044aedc531b481d6350a7c804e81384cf58d68f0058e221c2995cfae9b6d43377ff5306f47b2ae63097b96613216) 
+ [prometheus-pusher](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e3e454eb0880060812e5308048c8422b367b2d1d9d2cb443c97bde8e4a4a3a3e5) 
+ [*_client](http://u.720life.cn/g/9a9b751b4176dd00a09dcbac56dd9284d97499b48e804baa9093181ae824cc639b9db330304c001069dc7a45d3be0701c8251d12c867e3fd0c9c7472c2437e85) 

## 参与贡献

1. Fork 本项目
2. 新建 Feat_xxx 分支
3. 提交代码
4. 新建 Pull Request


## 码云特技

1. 使用 Readme\_XXX.md 来支持不同的语言，例如 Readme\_en.md, Readme\_zh.md
2. 码云官方博客 [blog.gitee.com](http://u.720life.cn/g/4d9d51ba66eeb41dfb9759648c593bf554785fd0e6ab49d2f13e98afcb69bbc7) 
3. 你可以 [https://gitee.com/explore](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ed27d15edf43aa40a6d37a2a10b263e5a)  这个地址来了解码云上的优秀开源项目
4. [GVP](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6eb5ad9b84ebe402667383e4a11c785b2d)  全称是码云最有价值开源项目，是码云综合评定出的优秀开源项目
5. 码云官方提供的使用手册 [http://git.mydoc.io/](http://u.720life.cn/g/76dccab75f320b82352866c6b8b38adf94d437922eb4b9bf86524045dd598681) 
6. 码云封面人物是一档用来展示码云会员风采的栏目 [https://gitee.com/gitee-stars/](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e43c4696b881f436e3c9d0b3d64c264cb) 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)