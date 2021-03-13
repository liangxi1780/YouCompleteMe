 
   
     
   
 

 Ant Design 

 

An enterprise-class UI design language and React implementation.

[![Build Status](https://dev.azure.com/ant-design/ant-design/_apis/build/status/ant-design.ant-design?branchName=master)](https://dev.azure.com/ant-design/ant-design/_build/latest?definitionId=2?branchName=master)
[![CircleCI branch](https://img.shields.io/circleci/project/github/ant-design/ant-design/master.svg?style=flat-square)](https://circleci.com/gh/ant-design/ant-design)
[![Codecov](https://img.shields.io/codecov/c/github/ant-design/ant-design/master.svg?style=flat-square)](https://codecov.io/gh/ant-design/ant-design/branch/master)
[![npm package](https://img.shields.io/npm/v/antd.svg?style=flat-square)](https://www.npmjs.org/package/antd)
[![NPM downloads](http://img.shields.io/npm/dm/antd.svg?style=flat-square)](http://npmjs.com/antd)

[![Dependencies](https://img.shields.io/david/ant-design/ant-design.svg?style=flat-square)](https://david-dm.org/ant-design/ant-design)
[![DevDependencies](https://img.shields.io/david/dev/ant-design/ant-design.svg?style=flat-square)](https://david-dm.org/ant-design/ant-design?type=dev)
[![Total alerts](https://flat.badgen.net/lgtm/alerts/g/ant-design/ant-design)](https://lgtm.com/projects/g/ant-design/ant-design/alerts/)
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fant-design%2Fant-design.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2Fant-design%2Fant-design?ref=badge_shield)
[![Issues need help](https://flat.badgen.net/github/label-issues/ant-design/ant-design/help%20wanted/open)](https://github.com/ant-design/ant-design/issues?q=is%3Aopen+is%3Aissue+label%3A%22help+wanted%22)

[![](https://img.shields.io/twitter/follow/AntDesignUI.svg?label=Ant%20Design&style=social)](https://twitter.com/AntDesignUI)
[![Gitter](https://img.shields.io/gitter/room/ant-design/ant-design-english.svg?style=flat-square&logoWidth=20&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4NCjxzdmcgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluayIgd2lkdGg9IjEyMzUiIGhlaWdodD0iNjUwIiB2aWV3Qm94PSIwIDAgNzQxMCAzOTAwIj4NCjxyZWN0IHdpZHRoPSI3NDEwIiBoZWlnaHQ9IjM5MDAiIGZpbGw9IiNiMjIyMzQiLz4NCjxwYXRoIGQ9Ik0wLDQ1MEg3NDEwbTAsNjAwSDBtMCw2MDBINzQxMG0wLDYwMEgwbTAsNjAwSDc0MTBtMCw2MDBIMCIgc3Ryb2tlPSIjZmZmIiBzdHJva2Utd2lkdGg9IjMwMCIvPg0KPHJlY3Qgd2lkdGg9IjI5NjQiIGhlaWdodD0iMjEwMCIgZmlsbD0iIzNjM2I2ZSIvPg0KPGcgZmlsbD0iI2ZmZiI%2BDQo8ZyBpZD0iczE4Ij4NCjxnIGlkPSJzOSI%2BDQo8ZyBpZD0iczUiPg0KPGcgaWQ9InM0Ij4NCjxwYXRoIGlkPSJzIiBkPSJNMjQ3LDkwIDMxNy41MzQyMzAsMzA3LjA4MjAzOSAxMzIuODczMjE4LDE3Mi45MTc5NjFIMzYxLjEyNjc4MkwxNzYuNDY1NzcwLDMwNy4wODIwMzl6Ii8%2BDQo8dXNlIHhsaW5rOmhyZWY9IiNzIiB5PSI0MjAiLz4NCjx1c2UgeGxpbms6aHJlZj0iI3MiIHk9Ijg0MCIvPg0KPHVzZSB4bGluazpocmVmPSIjcyIgeT0iMTI2MCIvPg0KPC9nPg0KPHVzZSB4bGluazpocmVmPSIjcyIgeT0iMTY4MCIvPg0KPC9nPg0KPHVzZSB4bGluazpocmVmPSIjczQiIHg9IjI0NyIgeT0iMjEwIi8%2BDQo8L2c%2BDQo8dXNlIHhsaW5rOmhyZWY9IiNzOSIgeD0iNDk0Ii8%2BDQo8L2c%2BDQo8dXNlIHhsaW5rOmhyZWY9IiNzMTgiIHg9Ijk4OCIvPg0KPHVzZSB4bGluazpocmVmPSIjczkiIHg9IjE5NzYiLz4NCjx1c2UgeGxpbms6aHJlZj0iI3M1IiB4PSIyNDcwIi8%2BDQo8L2c%2BDQo8L3N2Zz4%3D)](https://gitter.im/ant-design/ant-design-english?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)
[![Join the chat at https://gitter.im/ant-design/ant-design](https://img.shields.io/gitter/room/ant-design/ant-design.svg?style=flat-square&logoWidth=20&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4NCjxzdmcgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluayIgd2lkdGg9IjkwMCIgaGVpZ2h0PSI2MDAiIHZpZXdCb3g9IjAgMCAzMCAyMCI%2BDQo8ZGVmcz4NCjxwYXRoIGlkPSJzIiBkPSJNMCwtMSAwLjU4Nzc4NSwwLjgwOTAxNyAtMC45NTEwNTcsLTAuMzA5MDE3SDAuOTUxMDU3TC0wLjU4Nzc4NSwwLjgwOTAxN3oiIGZpbGw9IiNmZmRlMDAiLz4NCjwvZGVmcz4NCjxyZWN0IHdpZHRoPSIzMCIgaGVpZ2h0PSIyMCIgZmlsbD0iI2RlMjkxMCIvPg0KPHVzZSB4bGluazpocmVmPSIjcyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoNSw1KSBzY2FsZSgzKSIvPg0KPHVzZSB4bGluazpocmVmPSIjcyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTAsMikgcm90YXRlKDIzLjAzNjI0MykiLz4NCjx1c2UgeGxpbms6aHJlZj0iI3MiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEyLDQpIHJvdGF0ZSg0NS44Njk4OTgpIi8%2BDQo8dXNlIHhsaW5rOmhyZWY9IiNzIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxMiw3KSByb3RhdGUoNjkuOTQ1Mzk2KSIvPg0KPHVzZSB4bGluazpocmVmPSIjcyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTAsOSkgcm90YXRlKDIwLjY1OTgwOCkiLz4NCjwvc3ZnPg%3D%3D)](https://gitter.im/ant-design/ant-design?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

 

[![](https://cdn-images-1.medium.com/max/2000/1*NIlj0-TdLMbo_hzSBP8tmg.png)](http://ant.design)

English | [简体中文](./README-zh_CN.md)

## ✨ Features

- An enterprise-class UI design system for web applications.
- A set of high-quality React components out of the box.
- Written in TypeScript with predictable static types.
- The whole package of development and design resources and tools.

## 🖥 Environment Support

* Modern browsers and Internet Explorer 9+ (with [polyfills](http://u.720life.cn/g/19f81165ca0412019ffde45bafddc8e5b63ec2a50e1fe55a4873c18d8e3aa452ec7133dbc5cf363ace37e76673a8dd96195783a27165ae3f09687095c1949f7b) 
* Server-side Rendering
* [Electron](http://u.720life.cn/g/a9277b299dd7df8002122334f158f1b6cd41d5e12563f9be7c35b02b4f610ce3) 

| [ ](http://u.720life.cn/g/e8e63e9d56ec68b803322c46733da50e250bafa89bf75b6fa300450a04e79d004a89ee4f068d6e1f9b40f65bb657f76f)  IE / Edge | [ ](http://u.720life.cn/g/e8e63e9d56ec68b803322c46733da50e250bafa89bf75b6fa300450a04e79d004a89ee4f068d6e1f9b40f65bb657f76f)  Firefox | [ ](http://u.720life.cn/g/e8e63e9d56ec68b803322c46733da50e250bafa89bf75b6fa300450a04e79d004a89ee4f068d6e1f9b40f65bb657f76f)  Chrome | [ ](http://u.720life.cn/g/e8e63e9d56ec68b803322c46733da50e250bafa89bf75b6fa300450a04e79d004a89ee4f068d6e1f9b40f65bb657f76f)  Safari | [ ](http://u.720life.cn/g/e8e63e9d56ec68b803322c46733da50e250bafa89bf75b6fa300450a04e79d004a89ee4f068d6e1f9b40f65bb657f76f)  Opera | [ ](http://godban.github.io/browsers-support-badges/) Electron |
| --------- | --------- | --------- | --------- | --------- | --------- |
| IE9, IE10, IE11, Edge| last 2 versions| last 2 versions| last 2 versions| last 2 versions| last 2 versions

## 📦 Install

```bash
npm install antd
```

```bash
yarn add antd
```

## 🔨 Usage

```jsx
import { DatePicker } from 'antd';
ReactDOM.render( , mountNode);
```

And import style manually:

```jsx
import 'antd/dist/antd.css';  // or 'antd/dist/antd.less'
```

Or [import components on demand](http://u.720life.cn/g/19f81165ca0412019ffde45bafddc8e5b63ec2a50e1fe55a4873c18d8e3aa4528c335530d2e02f0d8a81840ee0ea603dc998f90ccdabc90bf6f88e0a26aea00e 

### TypeScript

See [Use in TypeScript](http://u.720life.cn/g/19f81165ca0412019ffde45bafddc8e50ac72de83e871fd00e63eb73bd88269a93a3df142b49f4d9f5285d9c0c7898ea25b08da641077e701ce580450188e3ea 

## 🌍 Internationalization

See [i18n](http://u.720life.cn/g/19b5814021e529520410bff849e8e0c8093bb97e7e4521a6f5e76e781b42caef291dc19f503d781849273d49db127521 

## 🔗 Links

- [Home page](http://u.720life.cn/g/19b5814021e529520410bff849e8e0c8faeae6b70ccef46636b50470ea9caf2d) 
- [Components](http://u.720life.cn/g/19b5814021e529520410bff849e8e0c843f1b2180fbb912311c53a8c34c315f3b6dc99c2fc61588f71a0b3e07dafb22c) 
- [Ant Design Pro](http://u.720life.cn/g/af16116c8afdc6f3c6def5f669313ae41b793a6cfc3ccd215998d7df35ff2905) 
- [Change Log](CHANGELOG.en-US.md)
- [rc-components](http://u.720life.cn/g/2319b00587ca4f603809a09965816da5ed9d810aaa3ed53487ff4f1623bb0d61f4b94bd0fa5a1a723d635fd159a3327b) 
- [Mobile UI](http://u.720life.cn/g/76b4223e691710012ddcc92b7a239de307848a81d1b466161ef90fd73eb19181) 
- [Landing Pages](http://u.720life.cn/g/11c8090d2f4445715052cc074770ace435f20bebd65dab6813557305b7d39e1c) 
- [Motion](http://u.720life.cn/g/5a4d19a3a4855c71d9c3ca94a0ab62e5be9e2337eb0e81f6a1236da0b05b7ee7) 
- [Scaffold Market](http://u.720life.cn/g/e0fc2dd6d96e64d38afbb712cd7a30f4410e5079b8274f9409d5df9116202f53) 
- [Developer Instruction](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465c720367d5be3d9a9eebaaaacc01f8f6996e800524b092d98185c6c33d7aab09094a188bbdde39074f1c9c06ddab720f) 
- [Versioning Release Note](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465c720367d5be3d9a9eebaaaacc01f8f61b28226e3157b748e8f9cbd1f8685325f191d97b4634346352d08536518b06d9244ec8cadfa6b7bcede4430e841eaa735db4c1fe2c823189d5113082528977175488750812ba993a08a9b98f3dd0596d13a2bad546fb1b9d10f897730c5a8721e6d8430f6a3ef212c584aa790c09b69833e6a8a1da6635993c14b66927fd835d) 
- [FAQ](http://u.720life.cn/g/19f81165ca0412019ffde45bafddc8e584b912e0aba6653c3c56f1d6769289f9c3875440d54596b92a5d1e46d36c4673) 
- [CodeSandbox Template](http://u.720life.cn/g/d27f7c08ac52c469a424f68173fd730e51a3c19641cf6d451f3025aa13872c0e4a2694234dbbe7720d961429f3045e25)  for bug reports
- [Awesome Ant Design](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046404ec3b3936d51370b1d6dfee677f44394838cab39575a6301b73ad1dd5ea0ea9131c35bbea41504757be580ea201387) 
- [Customize Theme](http://u.720life.cn/g/19b5814021e529520410bff849e8e0c82e940be840a53119760f65580f85c6d534eacd19549f66610e553c623dd6eb47) 

## ⌨️ Development

Use Gitpod, a free online dev environment for GitHub.

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/ant-design/ant-design)

Or clone locally:

```bash
$ git clone git@github.com:ant-design/ant-design.git
$ cd ant-design
$ npm install
$ npm start
```

Open your browser and visit http://127.0.0.1:8001 , see more at [Development](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465c720367d5be3d9a9eebaaaacc01f8f6996e800524b092d98185c6c33d7aab09261389e131fffed17cf3bea3d17b3d02 

## 🤝 Contributing [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

Read our [contributing guide](http://u.720life.cn/g/19f81165ca0412019ffde45bafddc8e54e28761ae4ccb0e9e844722399829739620d6774af0e2a867ce1e0a108229a51)  and let's build a better antd together.

We welcome all contributions. Please read our [CONTRIBUTING.md](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465c720367d5be3d9a9eebaaaacc01f8f6f072607d2a276f49fbc3f88545a92abd33c196db41fe2158b3fa59afea195cc91a7c43b16f4a536e631176cedd15f886)  first. You can submit any ideas as [pull requests](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465c720367d5be3d9a9eebaaaacc01f8f6bd721d7ab332e46e0c3edbefdcf8b1a1)  or as [GitHub issues](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465c720367d5be3d9a9eebaaaacc01f8f66c4f1712b59456fd96467a9454652cbb33b04f20cd84bc37c1b8c7e0526ee3a7  If you'd like to improve code, check out the [Development Instructions](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465c720367d5be3d9a9eebaaaacc01f8f6996e800524b092d98185c6c33d7aab09094a188bbdde39074f1c9c06ddab720f)  and have a good time! :)

If you are a collaborator, please follow our [Pull Request principle](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465c720367d5be3d9a9eebaaaacc01f8f6ad5a5f8a9aed56d224724f68cbf678fae5db687ad30a0ba156d4fb1a1ec55070)  to create a Pull Request by [collaborator template](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465c720367d5be3d9a9eebaaaacc01f8f6306b55b6159d756c631a38063ca1bd09f1ace557e55dac8f636f0285f4baaec6adfc68c8b0ad80758db1c021f5b517163085bdf4d1f567c23a16c727ca4fb102 

[![Let's fund issues in this repository](https://issuehunt.io/static/embed/issuehunt-button-v1.svg)](https://issuehunt.io/repos/34526884)



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)