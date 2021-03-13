 
    
   
   PearPlayer.js 
   
   
 

 一个支持多协议、多源、混合P2P-CDN的流媒体播放器 
 
     
      
    
 
 

**[English](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d59af9d2ceff0c52e49fd9f41ec75a59301016f64c223f2f857304809aa2d46ae418b924617f9689af5fa89bf4eb77f6797269ebe710a12bea781875e48919f4 

PearPlayer（梨享播放器）**[[Demo](http://u.720life.cn/g/0d406972bdd47fdfcbfbf1f0fed6323ee2b9778746fb3e57b35a371516b51230ccccd1c5b7e61a7ea881844d7cbf7efd  是完全用JavaScript写的开源HTML5流媒体播放框架，实现了融合HTTP（包含HTTPS、HTTP2）、WebRTC的多协议、多源、低延迟、高带宽利用率的无插件Web端流媒体加速能力。基于H5的MSE技术(Media Source Extension)将来自多个源节点的Buffer分块喂给播放器，再加上精心设计的算法来达到最优的调度策略及对各种异常情况的处理，Pear Player能在保证用户流畅视频体验的前提下最大化P2P率。

![PearPlayer](fig/PearPlayer.png)
 
 
![multisources](fig/fogvdn_multisources.png)

只需将`pear-player.min.js`通过` `标签导入到HTML就可以使用。 参考以下[代码示例](#快速开始)，也可以查看[`/examples/player-test.html`](/examples/player-test.html)来了解使用方法。
参考[get-started](docs/get-started.md)来了解基本使用方法。 

## 特性

- P2P能力基于**WebRTC**，无须安装任何插件
- 多协议(HTTP、HTTPS、WebRTC)、多源
- 自研的调度算法，在保证用户流畅视频体验的前提下最大化P2P率
- 默认无需填参数（内部根据视频码率等作自适应），高级使用模式可自行调整算法和参数
- 默认不会无限制缓冲，尽可能为CP用户节省带宽/流量
- 支持Chrome、Firefox、Opera、腾讯微信、X5/TBS等主流浏览器，不久将支持Safari11
- 可选接入低成本、高可用的Pear [Fog CDN](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c589cdc73cb2d623edd501f8eb6157b5dd38dc318c1d792516be94191d3140e7) 
- 协议默认通过TLS/DTLS全加密，无DPI特征；并可通过Pear Fog组件的动态端口映射进一步消除统计学特征
- 像使用HTML5 ` `标签一样简单，并容易与[video.js]https://github.com/videojs/video.js)等流行播放框架集成
- 具备Browser P2P能力（基于WebTorrent）

![bitmap](fig/bitmap_cn.png)

## 快速开始
将以下代码拷贝到HTML5代码中，打开网页，见证奇迹的时刻到了！
```html
  
  
 
  var player = new PearPlayer('#video', { src: 'https://qq.webrtc.win/tv/Pear-Demo-Yosemite_National_Park.mp4' });
 
```

## 使用方法

### 导入js文件并绑定video标签
首先通过script标签导入pear-player.min.js：
```html
  
```
或者使用CDN：
```html
  
```
假设用video标签播放如下视频，HTML如下所示：
```html
 
```
只需要如下几行代码，即可将PearPlayer绑定到video标签：
```html
 
  /**
  * 第一个参数为video标签的id或class
  * opts是可选的参数配置
  */
  if (PearPlayer.isMSESupported()) {
    var player = new PearPlayer('#pearvideo', opts);
  }
 
```
恭喜您，您的播放器已经具备P2P能力了，而且无须任何插件！

### 如何为自己的视频加速？
示例中的视频是已经分发过的，那么如何为任意视频加速呢？很简单，只需在[视频分发系统]https://oss.webrtc.win/)中添加您的视频URL，即可利用Pear的海量节点为您的视频加速！具体教程请点击[这里]https://manual.webrtc.win/oss/)（目前仅支持分发`MP4`格式，视频的名字需要加上`Pear-Demo`前缀，如`Pear-Demo-movie.mp4`）

## 谁在用我们的产品？

+ [Pear Limited](http://u.720life.cn/g/90edb4c9588f81e751444f32af10bc99) 
+ [Lenovo China](http://u.720life.cn/g/7377d71212b3ba32ca8b81c6d177dc38fe58e9a07ab1ff0e9de57e87dd2dc304) 
+ [Newifi xCloud](http://u.720life.cn/g/3ad0a892c5e62819447318fadbff1cef5ab730132d3b4aa0b3e164bce072a326) 
+ [FastWeb](http://u.720life.cn/g/6a3f76e99ab644db915c1a1398f4c33f6beef596384c431ac9de7c6710be7a09) 
+ [UCloud](http://u.720life.cn/g/ed15d0866a635f3c641cd3ed32d102fbef447f3aafc721f3e5fbc071112ba13a) 
+ [Tencent Cloud](http://u.720life.cn/g/a03719b0e8a2b62305a42f930eb40debe65901b6ac754413e0bc6308c0d16770) 
+ [Tencent X5/TBS](http://u.720life.cn/g/79f766d8f9268e18ac5099c815a991a83d27973e63f2bf54b09bc288d718ca68) 
+ [Tencent APD](http://u.720life.cn/g/3aed19dcc5710abe443b0c755a5a99070506dae135624ab4ed90e0c215475a66125c25c925219c8e8b397fc5ebdeeac5ac9159777274ecfbd93592cdddcdf2de) 

## Pear Player 文档
- **[阅读get-started文档](docs/get-started.md)**
- **[阅读API文档](docs/api.md)**

## 致谢
特别感谢以下项目，为本项目提供了部分灵感来源以及API设计参考：

- [WebTorrent](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463a1044b30dd894b08466f4a0787bcfa5f32ade679b1ddafd591e7fbaf8925e61) 
- [Peer5](http://u.720life.cn/g/0925233fb00971932b1b60ce5127b3cf68f6afac91118798a879a706adb86c39) 

## 演讲与媒体报道

- 2017.11.24 （金色财经） - [谛听科技正式进军区块链领域，战略投资梨享计算](http://u.720life.cn/g/6fb822b0e87db3b532ef7372da60f3d916aad67f7111b49ce1a5e5f2e64044f034227442434b904f22b948a17dccf98b) 
- 2017.09.01 （未来网络开放社区联盟） - [继云计算之后，雾计算再起 —— 谈谈 P2P CDN](http://u.720life.cn/g/408fb60b53d11d245635ad5e8e8cd6972a4a97d99ab198b91b6706047eb2ad50ce63bfdc1f40e5f7b5ab2f99301d24991838c8042fdc198b052f1252f8759bb5)   
- 2017.08.18 （IT大咖说） - [WebRTC会成主流吗？众包CDN时代到了！](http://u.720life.cn/g/ecc7d42b8e4205e5d387aa616e7cff785aa8e0cb4e39f00c3f57350ee57b4e0dd908f8d8d108aa632a883342bb830a6e) 
- 2017.07.11 （OSChina开源中国） - [PearPlayer.js —— 混合P2P-CDN的流媒体播放器](http://u.720life.cn/g/1dbc517b01e71dde51eaf55b6f5fa833ede2541a71733bdbd270d29eccded8b7c372a362ebe41f7e6cf4d2ea3b19afea) 
- 2017.06.24 （腾讯Web前端大会） - [基于WebRTC的P2P-CDN流媒体加速](http://u.720life.cn/g/d5ae4af44884bbe8965e6c5bd2c8989acf3b51f0435180e3c7dc4e4f477266329b9d3ab51c79b2d25d83b2a21f673589) 
- 2017.05.17 （南方科技大学） - Edge Computing and Shared Fog Streaming
- 2017.05.08 （台湾逢甲大学） - A Cooler Fruit Venture: Scaling up a Network from Cloud to Fog with Crowdsourcing
- 2016.08.17 （香港科技大学） - From Cloud to Fog: Scaling up a Network with Crowdsourcing

## License

MIT. Copyright (c) [Pear Limited](http://u.720life.cn/g/90edb4c9588f81e751444f32af10bc99)  and [snowinszu](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b9b231a18620a158a586c034213e0baf 

## 帮助与支持
E-mail:  ；用户QQ群：`373594967`；[CP/CDN接入、OEM与其他商务合作](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c589cdc73cb2d623edd501f8eb6157b5dd38dc318c1d792516be94191d3140e7) 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)