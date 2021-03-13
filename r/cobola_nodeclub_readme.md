Nodeclub
=

[![build status][travis-image]][travis-url]
[![codecov.io][codecov-image]][codecov-url]
[![David deps][david-image]][david-url]
[![node version][node-image]][node-url]

[travis-image]: https://img.shields.io/travis/cnodejs/nodeclub/master.svg?style=flat-square
[travis-url]: https://travis-ci.org/cnodejs/nodeclub
[codecov-image]: https://img.shields.io/codecov/c/github/cnodejs/nodeclub/master.svg?style=flat-square
[codecov-url]: https://codecov.io/github/cnodejs/nodeclub?branch=master
[david-image]: https://img.shields.io/david/cnodejs/nodeclub.svg?style=flat-square
[david-url]: https://david-dm.org/cnodejs/nodeclub
[node-image]: https://img.shields.io/badge/node.js-%3E=_4.2-green.svg?style=flat-square
[node-url]: http://nodejs.org/download/

## 介绍

Nodeclub 是使用 **Node.js** 和 **MongoDB** 开发的社区系统，界面优雅，功能丰富，小巧迅速，
已在Node.js 中文技术社区 [CNode(http://u.720life.cn/g/2433032ec1d3e480fde855f96cb7f76c82e0e167d4872371c8761ee1264f5b9d9213fc0e28896557f67ba5f8fef15a1f)  得到应用，但你完全可以用它搭建自己的社区。

## 安装部署

*不保证 Windows 系统的兼容性*

线上跑的是 [io.js](http://u.720life.cn/g/5281e776604544bdc4b27e692d4f3b53)  v2.3.3，[MongoDB](http://u.720life.cn/g/5b6081b126093fbb42e8289314c4c63ef11d05f801624758de9349edb7974f2a)  是 v2.6，[Redis](http://u.720life.cn/g/e43ded0dc5fea7f24cfd27806818885e)  是 v2.8.9。

```
1. 安装 `Node.js/io.js[必须]` `MongoDB[必须]` `Redis[必须]`
2. 启动 MongoDB 和 Redis
3. `$ make install` 安装 Nodeclub 的依赖包
4. `cp config.default.js config.js` 请根据需要修改配置文件
5. `$ make test` 确保各项服务都正常
6. `$ node app.js`
7. visit `http://localhost:3000`
8. done!
```

## 测试

跑测试

```bash
$ make test
```

跑覆盖率测试

```bash
$ make test-cov
```

## 贡献

有任何意见或建议都欢迎提 issue，或者直接提给 [@alsotang](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463c733a0f262f649564ae6f223c8b9c98) 

## License

MIT



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)