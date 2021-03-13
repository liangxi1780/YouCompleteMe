# ECharts

 
     
 

ECharts is a free, powerful charting and visualization library offering an easy way of adding intuitive, interactive, and highly customizable charts to your commercial products. It is written in pure JavaScript and based on  zrender , which is a whole new lightweight canvas library.

Now ECharts is an incubator project of Apache Software Foundation.
Please check its incubator status [here](http://u.720life.cn/g/5e65441f2e917d1bc2465898fdb20764997c82bfc46c4cfe1cf7176c5000415c2c257040dbaf9d823f37a89a12cd8f3ff93bcbc336daa4ed66f0f55a5036b104) 

**[中文官网](http://u.720life.cn/g/7fc119b723a6022f4292f1a804c142c4264f286319f5d35755c114896f5589956b8e798036160793739133e37b43b8e4  | **[ENGLISH HOMEPAGE](http://u.720life.cn/g/7fc119b723a6022f4292f1a804c142c44c09a7dd2a97502a34bd7b28e8e1fec191093d70b140a3de9776f85064dde681 

[![Build Status](https://travis-ci.org/apache/incubator-echarts.svg?branch=master)](https://travis-ci.org/apache/incubator-echarts) [![](https://img.shields.io/npm/dw/echarts.svg?label=npm%20downloads&style=flat)](https://www.npmjs.com/package/echarts) [![Last npm release](https://img.shields.io/npm/v/echarts)](https://www.npmjs.com/package/echarts)

## Get ECharts

You may choose one of the following methods:

+ Download from Official Website in [中文下载页](http://u.720life.cn/g/7fc119b723a6022f4292f1a804c142c4367d55558d96e3ef99d062d1f358b022251d7e9ade08ba8ceb46451672979216) 
+ Download from Official Website in [English](http://u.720life.cn/g/7fc119b723a6022f4292f1a804c142c408cca8ba9bb7127c90d7a3800437126732f8911a5a43027f6da8da1fdac3f5c7) 
+ `npm install echarts --save`
+ CDN: [jsDelivr CDN](http://u.720life.cn/g/ab55b18e77c71bdb182f9d2fc257c44231ec3ae516a24f4ebca8e2e40ef9d79328ab560bc31d648302dd175fef3dabbbaecaa85ad077a86eeab9692a190481ff) 

## Docs

+ Tutorial
    + [中文](http://u.720life.cn/g/7fc119b723a6022f4292f1a804c142c44ceec2eb83c3a00b38f06931e83f9285f7ae4fca7e109114ffab8a7742c8d11e) 
    + [English](http://u.720life.cn/g/7fc119b723a6022f4292f1a804c142c4f6e5412fa99e89403111a5d7776a3aa16b6613b049a35f4b38a9ea45e2c2ab1c) 

+ API
    + [中文](http://u.720life.cn/g/7fc119b723a6022f4292f1a804c142c4a1473467674d59562a6b85af5fcd6f62b0cb9e15b177ccfff4ff981dae07e8d3) 
    + [English](http://u.720life.cn/g/7fc119b723a6022f4292f1a804c142c4dbb32a6c74a48ded580fda314b98f720dc915424f99c3ecdf95b1ba9609b3b18) 

+ Option Manual
    + [中文](http://u.720life.cn/g/7fc119b723a6022f4292f1a804c142c4e560ac9e2f8f64fa8e5fbdd992fa9c4e16aaef7ed40898e98fbb0d0b0ffc4064) 
    + [English](http://u.720life.cn/g/7fc119b723a6022f4292f1a804c142c4a970739ddf7b1d1e0f06d8a124bc0c26ecac3af1505b9405fdd7e96ac76a13b7) 

## Get Help

+ [GitHub Issues](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c0001bca31ae58bae1a9ea2d5840c8aa3393543c9093f50dce1700b510e38e782b658742922955844dc8a4ab94b82ce6)  for bug report and feature requests
+ Email [dev@echarts.apache.org](dev@echarts.apache.org) for general questions
+ Subscribe [mailing list](http://u.720life.cn/g/7fc119b723a6022f4292f1a804c142c4dd43b8248ccb5a62f1e9b90afa8685d541c60fabbe63ac1ffa416e564fac5c8e)  to get updated with the project

## Build

Build echarts source code:

Execute the instructions in the root directory of the echarts:
([Node.js](http://u.720life.cn/g/6dd25ec2eceebbb6348ad519a7343cbc27be38d93fa976be8774feadbfe55aca)  is required)

```shell
# Install the dependencies from NPM:
npm install

# If intending to build and get all types of the "production" files:
npm run release
# The same as `node build/build.js --release`

# If only intending to get `dist/echarts.js`, which is usually
# enough in dev or running the tests:
npm run build
# The same as `node build/build.js`

# Get the same "production" files as `node build/build.js`, while
# watching the editing of the source code. Usually used in dev.
npm run watch
# The same as `node build/build.js -w`

# Check the manual:
npm run help
# The same as `node build/build.js --help`
```

Then the "production" files are generated in the `dist` directory.

More custom build approaches can be checked in this tutorial: [Create Custom Build of ECharts](http://u.720life.cn/g/7fc119b723a6022f4292f1a804c142c4f6e5412fa99e89403111a5d7776a3aa1696d744228135b79841e8988e99280a72e4c69fb4f9288cdbf5f5acc8e1370e5e276097bc2cad0e19ed32069096e3ca24eb7bea1d5b6c9ce794b2638a98a4350)  please.

## Contribution

If you wish to debug locally or make pull requests, please refer to [contributing](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c0001bca31ae58bae1a9ea2d5840c8aa3d235fc0ed20fc0c27b4e2a7d8ba9a31c608686ff0d34561ee056c4e866b66f0ef92f09062bbe13e8f75e205726228a4)  document.

## Resources

### Awesome ECharts

[https://github.com/ecomfe/awesome-echarts](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046435efbac5694cd7f2ff66c31218684de81bcf9bce22dc49900937d16cc5d3d82) 

### Extensions

+ [ECharts GL](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b33777698bfd897ade1a3dcb86b43058bc1bddb9fd1c5253989ae5bbf3ad2cb7)  An extension pack of ECharts, which provides 3D plots, globe visualization, and WebGL acceleration.

+ [Liquidfill 水球图](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b33777698bfd897ade1a3dcb86b430587f4bde6f13d2edd113d3e2488f8ec049) 

+ [Wordcloud 字符云](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b33777698bfd897ade1a3dcb86b4305888ce2319f6fc4ab4e1f78e2cf1867ec3) 

+ [Extension for Baidu Map 百度地图扩展](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c0001bca31ae58bae1a9ea2d5840c8aa2710fe6f78697bc78e01ce3af30d224ecd2ceddb7ed1f95a8148b87f3f83270fe63e91bf61831ef352879108cb7bf1aa)  An extension provides a wrapper of Baidu Map Service SDK. 

+ [vue-echarts](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046491af1049fddcbd07d6890e7df9641db226633d46dc81bab07a3527335e08c3d)  ECharts component for Vue.js

+ [echarts-stat](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b33777698bfd897ade1a3dcb86b4305899d11eaa52ec96ec8dc7a73cded6ff01)  Statistics tool for ECharts

## License

ECharts is available under the Apache License V2.

## Code of Conduct

Please refer to [Apache Code of Conduct](http://u.720life.cn/g/9504ecfd7de2b26345fb4a78087ff8e37f78cc0f2053227f9d93f5e8e73024a836398680749b456ce4269304d8fc249aa770b8357c15788b47a8b7a099c1f29c 

## Paper

Deqing Li, Honghui Mei, Yi Shen, Shuang Su, Wenli Zhang, Junting Wang, Ming Zu, Wei Chen.
[ECharts: A Declarative Framework for Rapid Construction of Web-based Visualization](http://u.720life.cn/g/2d854640d85bbffc76f1e33e215ebf541ebef430f13c2be296c70e613993c43fe98a98df0a77097dce9c8f3b65ea655241bae1a97f6549ab9a1e31b0cb89f3946d5ae403ea80a38fe72119ffa1877dd1 
Visual Informatics, 2018.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)