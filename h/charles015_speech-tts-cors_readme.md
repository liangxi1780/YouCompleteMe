# 百度语音合成浏览器跨域访问示例

1. 本项目包含一个调用库baidu\_tts\_cors.js文件，以及一个demo.html示例文件，demo.html示例文件已经引入了调用库; 并且项目不依赖其他第三方库。
2. 项目的跨域依赖于XHR2，[CORS跨域控制]http://u.720life.cn/g/bee1b7066881d1d2e496511a41bafc0d649f55a957f8e7a075bfd77d38bb1e4dc1d3adbe0a44c9becb0d4a46397b6c0fedc055072952b703243a1391a56a1fa0788972f4faf638a9ce40e9e227d07a51) 
3. 使用前请确保了解百度AI开发平台授权，百度AI语音合成RESTful接口相关概念。[百度语音合成RESTful接口文档]http://u.720life.cn/g/ef809b9980abae1893394e82a815c1b06ba648cffc2bc80afaf70c62e76e828433a953cbac7f421b20ca9c06dd5e4bbc)  [鉴权机制文档]http://u.720life.cn/g/ef809b9980abae1893394e82a815c1b0fc20a4c6027867eaa1c7c9ac2e86ce0aa24412d80f61075cfaa1f1021739fa69) 
4. 项目为初期版本，后续版本实现和接口调用方式可能会有较大变动。

## 兼容性说明

1. 浏览器对于自动播放特性的支持情况有差异，因此没有添加自动播放的功能，也不建议自行添加自动播放属性。
2. demo已经在主流浏览器下测试通过，非主流浏览器可能存在不支持的情况，包括微信小程序，各种hybrid框架等。

## 如何获取tok参数

首先在您创建的应用中查找Api Key 和 SecretKey。访问https://openapi.baidu.com/oauth/2.0/token 换取 token


**访问如下网址， 可用浏览器测试**

```
// appKey = Va5yQRHl********LT0vuXV4
// appSecret = 0rDSjzQ20XUj5i********PQSzr5pVw2

https://openapi.baidu.com/oauth/2.0/token?grant_type=client_credentials&client_id=Va5yQRHl********LT0vuXV4&client_secret=0rDSjzQ20XUj5i********PQSzr5pVw2
```

**可以获取如下结果**

```json
{
"access_token": "1.a6b7dbd428f731035f771b8d********.86400.1292922000-2346678-124328",
"expires_in": 86400,
"refresh_token": "2.385d55f8615fdfd9edb7c4b********.604800.1293440400-2346678-124328",
"scope": "public",
"session_key": "ANXxSNjwQDugf8615Onqeik********CdlLxn",
"session_secret": "248APxvxjCZ0VEC********aK4oZExMB",
}
```

在结果中可以看见 token = 1.a6b7dbd428f731035f771b8d********.86400.1292922000-2346678-124328，在86400秒后过期。

## 调用示例

您的项目只需引入baidu\_tts\_cors.js文件，即可使用全局函数btts。

```
// 调用语音合成接口
// 参数含义请参考 https://ai.baidu.com/docs#/TTS-API/41ac79a6
btts({
    tex: '百度语音合成',
    tok: '请参照上一章节说明获取的access_token',
    spd: 5,
    pit: 5,
    vol: 15,
    per: 4
}, {
    volume: 0.3,
    autoDestory: true,
    timeout: 10000,
    hidden: false,
    onInit: function (htmlAudioElement) {

    },
    onSuccess: function(htmlAudioElement) {

    },
    onError: function(errorText) {
    },
    onTimeout: function () {
    }
});
}
```

btts全局函数参数说明

    浏览器调用语音合成接口
    @param {Object} param 百度语音合成接口参数
            请参考 https://ai.baidu.com/docs#/TTS-API/41ac79a6

    @param {Object} options 跨域调用api参数
            timeout {number} 超时时间 默认不设置为60秒
            volume {number} audio控件音量，范围 0-1
            hidden {boolean} 是否隐藏audio控件
            autoDestory {boolean} 播放音频完毕后是否自动删除控件
            onInit {Function} 创建完audio控件后调用
            onSuccess {Function} 远程语音合成完成，并且返回音频文件后调用
            onError {Function}  远程语音合成完成，并且返回错误字符串后调用
            onTimeout {Function} 超时后调用，默认超时时间为60秒


*** 具体调用方法和参考示例  demo.html  文件 ***



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)