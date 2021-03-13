 
      
     
 
 
     
 
 A Vue.js 2.0 Mobile UI at YouZan 

[![Build Status](https://travis-ci.org/youzan/vant.svg?branch=master)](https://travis-ci.org/youzan/vant) [![Coverage Status](https://img.shields.io/codecov/c/github/youzan/vant/dev.svg)](https://codecov.io/github/youzan/vant?branch=dev) [![npm version](https://img.shields.io/npm/v/vant.svg?style=flat)](https://www.npmjs.com/package/vant) [![downloads](https://img.shields.io/npm/dt/vant.svg)](https://www.npmjs.com/package/vant) 
 
[访问中文版](./README.zh-CN.md)

## Install

```shell
npm i -S vant
```
 
## Usage

### Use [babel-plugin-import](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462aaced1fa5f947db3914dcd309b60a3e71c4b60d088e736628077dab47444f64478b22ac59d0b3daf92a0f1c947dc8de)  (Recommended)

   ```js
   // .babelrc or babel-loader option
   {
     "plugins": [
       ["import", { "libraryName": "vant", "style": true }]
     ]
   }
   ```

   Then you can import components from vant, equivalent to import manually below.

   ```js
   // import js and css modularly, parsed by babel-plugin-import
   import { Button } from 'vant';
   ```

### Manually import

   ```jsx
   import { Button } from 'vant';
   import 'vant/lib/vant-css/button.css';
   ```
 
 
### Import all components
 
```javascript
import Vue from 'vue';
import vant from 'vant';
import 'vant/lib/vant-css/index.css';

Vue.use(vant);
```
 
## Development

### Add a new component

```shell
make init componentName
```

### Start coding

Start development mode:

```shell
npm run dev
```

Visit [http://localhost:8080](http://u.720life.cn/g/e71094f6077cb9592da5b56893f0ad140b42b73eea3c0cdc72b4d749f85d5d96)  to see an example of all components.

## Preview

You can scan the following QR code to access the demo：

![zanui_vue_mobile_qrcode](https://img.yzcdn.cn/v2/image/youzanyun/zanui/pc/zanui_vue_mobile_preview_03.png)
 
## LICENSE

[MIT](http://u.720life.cn/g/fa1db2c4a526903522dec7b8417f89d15f847589016765e3143cbb68cadbc104b1c4e151f2bc0d5bdecbcbaec8e9f53f6911e682a15e2223b2e88a1c1a85af42) 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)