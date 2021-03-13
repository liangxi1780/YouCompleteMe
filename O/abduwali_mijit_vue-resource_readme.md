# vue-resource [![Version](https://img.shields.io/npm/v/vue-resource.svg)](https://www.npmjs.com/package/vue-resource) [![License](https://img.shields.io/npm/l/vue-resource.svg)](https://www.npmjs.com/package/vue-resource) [![Downloads](https://img.shields.io/npm/dt/vue-resource.svg)](https://www.npmjs.com/package/vue-resource)

The plugin for [Vue.js](http://u.720life.cn/g/6086d56f21092497791a7b1434038d92)  provides services for making web requests and handle responses using a [XMLHttpRequest](http://u.720life.cn/g/a69e8f5dba5b4106ccc3875c547b14848492c6553bd52bb7c59a8587071dd1267fb2856419993d6af548deecc896cdd18f312befb6d3499fa9758705025f1fa2)  or JSONP.

## Features

- Supports the [Promise](http://u.720life.cn/g/a69e8f5dba5b4106ccc3875c547b14848492c6553bd52bb7c59a8587071dd126fdd1ea40180be86366b781aeb1d69201f77ec2e972b12461f043e3970497679d84a04b97180d73ddb7e07bf239102e6fdef3ef4a51b6cf03f3e5e97d4116cb7f)  API and [URI Templates](http://u.720life.cn/g/b01b15ebd504e7d95a7d009c8f17ce3a386570eaa22a36cca95d0f0934e007a22bf1c4ee4c3ba890dfb22340af7866cd85ca2afb9eecfc13ca63d69a8ed5ec62) 
- Supports [interceptors](docs/http.md#interceptors) for request and response
- Supports latest Firefox, Chrome, Safari, Opera and IE9+
- Compact size 14KB (5.3KB gzipped)

## Installation

### NPM
```
$ npm install vue-resource
```

### Bower
```
$ bower install vue-resource
```

### CDN
Available on [jsdelivr](http://u.720life.cn/g/bb7a93d719a99772080f396520384e5981761a8c4ed4338aeccd1bbc257096b462d3fa4bc88fff556810fec6dadb89021d85c821c930a767564010590049d2e2db6ab64e16e97beb01b285ad9a9d3602  [cdnjs](http://u.720life.cn/g/3614b93d46b9512c39a847457049c70b44a34f00f47364f7da833d3a9b545fea25e622fd25cf53dc6ecc05d2f0d2dc14)  or [unpkg](http://u.720life.cn/g/a37a61a440aa343e38eba02fa2d29d2b17359e56f1a51ccf6a3e123169769760fe78a7cef6c21ee815f9eb086edce866fa12671578cf4cd0f5661877aa9d8579 
```html
  
```

## Example
```js
{
  // GET /someUrl
  this.$http.get('/someUrl').then(response => {

    // get body data
    this.someData = response.body;

  }, response => {
    // error callback
  });
}
```

## Documentation

- [Configuration](docs/config.md)
- [HTTP Requests/Response](docs/http.md)
- [Creating Resources](docs/resource.md)
- [Code Recipes](docs/recipes.md)
- [API Reference](docs/api.md)

## Changelog

Details changes for each release are documented in the [release notes](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f2d401599ecf202547a0fc302d55d5df6cc171a5b8145301bf123d52a01dce39 

## Contribution

If you find a bug or want to contribute to the code or documentation, you can help by submitting an [issue](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f2d401599ecf202547a0fc302d55d5dffd87beca1a6f2a5042bf8879380f9216)  or a [pull request](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f2d401599ecf202547a0fc302d55d5df9f688421f91dd55827950c85420830cc 

## License

[MIT](http://u.720life.cn/g/ba059582536a397f7c573b87c8bea647045b0ef049248233b6f76e909e70200fe7048b25e29c8bab79aeff32ea74556a) 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)