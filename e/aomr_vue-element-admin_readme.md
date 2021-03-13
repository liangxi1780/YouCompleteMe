 
   
 

 
   
     
   
   
     
   
   
     
   
   
     
   
   
     
   
 

English | [简体中文](./README.zh-CN.md)

## Introduction

[vue-element-admin](http://u.720life.cn/g/fe66c81bb3beaaa729d5c40a4b27d2dccd4bd354013c5583da7a7933e04955629608bb4f22741984912ae6a81efbe29f)  is a front-end management background integration solution. It based on [vue](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a66c77cd0911e5527fb3fc591bfc25f5)  and use the UI Toolkit [element](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461c3385d2c6442447210a4c3d1baebf51b4c3a2e2c9b33f1317d09abb948fab82 

It is a magical vue admin based on the newest development stack of vue, built-in i18n solution, typical templates for enterprise applications, lots of awesome features. It helps you build a large complex Single-Page Applications. I believe whatever your needs are, this project will help you.

- [Preview](http://u.720life.cn/g/fe66c81bb3beaaa729d5c40a4b27d2dccd4bd354013c5583da7a7933e04955629608bb4f22741984912ae6a81efbe29f) 

- [Documentation](http://u.720life.cn/g/41d6770a8ffafe7688694282c8a2e655bf3c6de28ae62da3938ff25d74873215eb4557e911c10522557c395f4527b3ae15a44b777d6d46c48fa0ec135bd3f963) 

- [Gitter](http://u.720life.cn/g/11e95d0ed8d2826912e12fe1dc3f34212d27e5689b604252209daca17f7256f8dc5b4f00c1131fd04b28b3f5b47d25ab) 

- [Wiki](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304603c6efa7d0c1ce77680f5b6f938bd6ce1dbfd9825dd43b2faae6e4bf617322f73d2f0d2a8a66dbd10f1d93cca579c837) 

- [Donate](http://u.720life.cn/g/41d6770a8ffafe7688694282c8a2e655bf3c6de28ae62da3938ff25d74873215eb4557e911c10522557c395f4527b3ae8f77a970562f3b94dd5f0125601eaaab) 

- [Gitee](http://u.720life.cn/g/41d6770a8ffafe7688694282c8a2e6556b9a9ba08c7856b8b73cae36d0c3455315f2582e41805bf0c6b42d1a1ad0df29)  国内用户可访问该地址在线预览

**This project is positioned as a background integration solution and is not suitable for secondary development as a basic template.**

 - Base template recommends using: [vueAdmin-template](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304603c6efa7d0c1ce77680f5b6f938bd6ced0f57b73745494f998016a2069c21e8a)   
 - Desktop: [electron-vue-admin](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046dd88aac115d6b4bf24ce86891d3d788cf9775745fef1b25a2dc49f4ebda19deb) 

## Preparation

You need to install [node](http://u.720life.cn/g/c47729c1c499a00d6e30af9fa18eaddd7b41ca24e187ea438549a271175cdbab)  and [git](http://u.720life.cn/g/0699e533b96232c5e210af6ab5668134e6f26f1fc99a343a9eacc50fbfcb0e97)  locally. The project is based on [ES2015+](http://u.720life.cn/g/c7e32d8c72c7a7f0f5b5c90906d584013b2798962de04a3375474bff3b5a2b2f  [vue](http://u.720life.cn/g/1eea7f654038e3466b5f7afd82540e02402fb3b54bb29bc02feef21ccbff11fe23da4fdeac1d0e3348d1d168e5ea79c6  [vuex](http://u.720life.cn/g/acea3f53396a46112876052cae0a3648a301c768c1c6a891b90c7c1c05e9a591  [vue-router](https://router.vuejs.org/zh-cn/), [axios](https://github.com/axios/axios) and [element-ui](https://github.com/ElemeFE/element), all request data is simulated using [Mock.js](https://github.com/nuysoft/Mock).
 Understanding and learning this knowledge in advance will greatly help the use of this project.

 **This project does not support low version browsers (e.g. IE). Please add polyfill yourself if you need them.**

 **Note: This project uses element-ui@2.3.0+ version, so the minimum compatible vue@2.5.0+**

  
   
 

## Features
```
- Login / Logout

- Permission Authentication
  - Page permission
  - Directive permission
  - Two-step login

- Multi-environment build
  - dev sit stage prod

- Global Features
  - I18n
  - Multiple dynamic themes
  - Dynamic sidebar (supports multi-level routing)
  - Dynamic breadcrumb
  - Tags-view(Tab page Support right-click operation)
  - Svg Sprite
  - Mock data
  - Screenfull
  - Responsive Sidebar

- Editor
  - Rich Text Editor
  - Markdown Editor
  - JSON Editor

- Excel
  - Export Excel
  - Export zip
  - Upload Excel
  - Visualization Excel

- Table
  - Dynamic Table
  - Drag And Drop Table
  - Tree Table
  - Inline Edit Table

- Error Page
  - 401
  - 404

- Components
  - Avatar Upload
  - Back To Top
  - Drag Dialog
  - Drag Kanban
  - Drag List
  - SplitPane
  - Dropzone
  - Sticky
  - CountTo

- Advanced Example
- Error Log
- Dashboard
- Guide Page
- Echarts
- Clipboard
- Markdown to html
```

## Getting started

```bash
# clone the project
git clone https://github.com/PanJiaChen/vue-element-admin.git

# install dependency
npm install

# develop
npm run dev
```

This will automatically open http://localhost:9527.

## Build
```bash
# build for test environment
npm run build:sit

# build for production environment
npm run build:prod
```

## Advanced
```bash
# --report to build with bundle size analytics
npm run build:prod --report

# --preview to start a server in local to preview
npm run build:prod --preview

# lint code
npm run lint

# auto fix
npm run lint -- --fix
```

Refer to [Documentation](http://u.720life.cn/g/41d6770a8ffafe7688694282c8a2e655bf3c6de28ae62da3938ff25d74873215eb4557e911c10522557c395f4527b3aef3eb2d6ddfba6c7fc6e108170574b0940907860fc0f3cc5e65f50e9779d6a51e)  for more information

## Changelog
Detailed changes for each release are documented in the [release notes](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304603c6efa7d0c1ce77680f5b6f938bd6ce1dbfd9825dd43b2faae6e4bf617322f748328e04ad80f3e2053789595bae7ce0 

## Online Demo
[Preview](http://u.720life.cn/g/fe66c81bb3beaaa729d5c40a4b27d2dccd4bd354013c5583da7a7933e04955629608bb4f22741984912ae6a81efbe29f) 

## Donate
If you find this project useful, you can buy author a glass of juice :tropical_drink:

![donate](https://wpimg.wallstcn.com/bd273f0d-83a0-4ef2-92e1-9ac8ed3746b9.png)

[Paypal Me](http://u.720life.cn/g/a273b252b999cb4afe707ebbed9aa55c68ac128a62d915a21f3b518e9ca3ed00) 

[Buy me a coffee](http://u.720life.cn/g/19a47102c7b29855acf1483539b95ed1c492d6714cd47f2560d0186add9ea4b7) 

## License

[MIT](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304603c6efa7d0c1ce77680f5b6f938bd6ce1dbfd9825dd43b2faae6e4bf617322f7675d0503adf737229a77e5cc04f20d40bf3051f7a3a176f714d0d73236755ac0) 

Copyright (c) 2017-present PanJiaChen



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)