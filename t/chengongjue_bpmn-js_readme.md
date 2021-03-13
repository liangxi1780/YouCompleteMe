# bpmn-js - BPMN 2.0 for the web

[![Build Status](https://travis-ci.org/bpmn-io/bpmn-js.svg?branch=develop)](https://travis-ci.org/bpmn-io/bpmn-js)

View and edit BPMN 2.0 diagrams in the browser.

[![bpmn-js screencast](./resources/screencast.gif "bpmn-js in action")](http://demo.bpmn.io/s/start)


## Installation

Use the library [pre-packaged](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046756a4ada46c114f6ee808048942b96d646a8b8f5094f7fc7fd79bd433a6bd5cf7e7838be0b671d075474a04f5a82004d6c6fca5dc2bb18f05227039799ef0e40) 
or include it [via npm](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046756a4ada46c114f6ee808048942b96d646a8b8f5094f7fc7fd79bd433a6bd5cfbeb33aea7172b561068ac7deb5c8fea4) 
into your node-style web-application.

## Usage

To get started, create a [bpmn-js](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046756a4ada46c114f6ee808048942b96d69948b6badd8f8a437381bec91f0768db)  instance
and render [BPMN 2.0 diagrams](http://u.720life.cn/g/c8f67a445e18719f39c501bafe36deca6cb75fc796eebbef361dadba16bfef2dddc749b0b68055a0461757eed3ddb9c2)  in the browser:

```javascript
var xml; // my BPMN 2.0 xml
var viewer = new BpmnJS({
  container: 'body'
});

viewer.importXML(xml, function(err) {

  if (err) {
    console.log('error rendering', err);
  } else {
    console.log('rendered');
  }
});
```

Checkout our [examples](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046756a4ada46c114f6ee808048942b96d63b87cc6465a3eac8965183210810ab1c)  for many
more supported usage scenarios.


### Dynamic Attach/Detach

You may attach or detach the viewer dynamically to any element on the page, too:

```javascript
var viewer = new BpmnJS();

// attach it to some element
viewer.attachTo('#container');

// detach the panel
viewer.detach();
```


## Resources

* [Demo](http://u.720life.cn/g/fd9bc20ab6a6ed07a517f811edf03cf717c39645bb5268facf76362f96e0e884) 
* [Issues](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046756a4ada46c114f6ee808048942b96d6963de8d2df74224cfc4693c894463dad) 
* [Examples](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046756a4ada46c114f6ee808048942b96d63b87cc6465a3eac8965183210810ab1c) 
* [Forum](http://u.720life.cn/g/49e85c50d6d15dc55361d9d026006d98bbcd9de2a625f69687afb88208db6c10) 
* [Changelog](./CHANGELOG.md)


## Building the Project

Perform the following steps to build the library, including running all tests:

```
cd bpmn-js
npm install
npm run all
```

You may need to perform [additional project setup](./docs/project/SETUP.md) when
building the latest development snapshot.

Please checkout our [contributing guidelines](./.github/CONTRIBUTING.md) if you plan to
file an issue or pull request.


## Related

bpmn-js builds on top of a few powerful tools:

* [bpmn-moddle](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046756a4ada46c114f6ee808048942b96d6dc14096246b45319eb15dfd2be9f2e6a  Read / write support for BPMN 2.0 XML in the browsers
* [diagram-js](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467eb01a8f48a1ed77c067a99019a46bb1a7455e035774debd61aec6a9b5e4f390  Diagram rendering and editing toolkit


## License

Use under the terms of the [bpmn.io license](http://u.720life.cn/g/543574664f4e343509e0e69ccc77d84182a3061cc98c1a477c86f2916e14812d 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)