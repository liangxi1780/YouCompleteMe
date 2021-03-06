# vue-monoplasty-slide-verify

> A Vue plugin to slide verify [Demo](http://u.720life.cn/g/ec4011e15016b358d3f952a60c8b14868551dd01f479a57b340e405d50f08b2a8fde934f95aea5675e5866d04b213e0dc1dd1c072d7f055acfe42b211aebd726) 

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```
## Quick Start

###  1. Import vue-monoplasty-slide-verify into your vue.js project.

Using build tools:

```bash
npm install --save vue-monoplasty-slide-verify
```

```js
import Vue from 'vue';
import SlideVerify from 'vue-monoplasty-slide-verify';

Vue.use(SlideVerify);
```

### 2. Now you have it. The simplest usage:

```html
  
 {{msg}} 
```

```js
export default {
        name: 'App',
        data(){
            return {
                msg: '',
            }
        },
        methods: {
            onSuccess(){
                this.msg = 'login success'
            },
            onFail(){
                this.msg = ''
            },
            onRefresh(){
                this.msg = ''
            }
        }
    }
```

## Document
### 内置方法
  - 在父组件里如果需要重置，可以在父组件中调用子组件reset() 方法
  ```html
    
  ```
  ```javascript
  this.$refs.slideblock.reset();
  ```
  - V1.1.0 版本新增属性`imgs`：
    - 当`imgs`不传或者传空数组时，图片库默认使用第三方api提供的图片路径。可能加载缓慢；
    - 当`imgs`传本地路径时，确保图片路径是否正确。建设传cdn上的图片地址。
    - 详情可参考`APP.vue`上的写法。或[在线查看demo地址](http://u.720life.cn/g/ec4011e15016b358d3f952a60c8b14868551dd01f479a57b340e405d50f08b2a8fde934f95aea5675e5866d04b213e0dc1dd1c072d7f055acfe42b211aebd726) 
  - [gitee镜像地址](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e4a13146f58c023e9cd09777a8cecd9aaaae25b217326fecbfe8162904d48cfda1c8e161ff4bbaf28d45f4ed149541925) 
### argument

| Param | Type | Describe |
| :------: | :------: | :------: |
| l | Number | block length |
| r | Number | block circle radius |
| w | Number | canvas width |
| h | Number | canvas height |
| sliderText | String | Slide filled right |
| imgs | Array | picture array |

### callBack

| Event | Type | Describe |
| :------: | :------: | :------: |
| success | Function | success callback |
| fail | Function | fail callback |
| refresh | Function | refresh button callback |


## Log
### V1.0.2
- Mobile terminal touch event support
### V1.0.5
- add slider text
### V1.1.0
- add img array



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)