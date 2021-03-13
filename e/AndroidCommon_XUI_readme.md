 
   
 

# XUI
[![](https://jitpack.io/v/xuexiangjys/XUI.svg)](https://jitpack.io/#xuexiangjys/XUI)
[![api](https://img.shields.io/badge/API-17+-brightgreen.svg)](https://android-arsenal.com/api?level=17)
[![Issue](https://img.shields.io/github/issues/xuexiangjys/XUI.svg)](https://github.com/xuexiangjys/XUI/issues)
[![Star](https://img.shields.io/github/stars/xuexiangjys/XUI.svg)](https://github.com/xuexiangjys/XUI)

一个简洁而又优雅的Android原生UI框架，解放你的双手！还不赶紧点击[使用说明文档]https://github.com/xuexiangjys/XUI/wiki)，体验一下吧！

> 涵盖绝大部分的UI组件：TextView、Button、EditText、ImageView、Spinner、Picker、Dialog、PopupWindow、ProgressBar、LoadingView、StateLayout、FlowLayout、Switch、Actionbar、TabBar、Banner、GuideView、BadgeView、MarqueeView、WebView、SearchView等一系列的组件和丰富多彩的样式主题。

在提issue前，请先阅读[【提问的智慧】]https://xuexiangjys.blog.csdn.net/article/details/83344235)，并严格按照[issue模板]https://github.com/xuexiangjys/XUI/issues/new/choose)进行填写，节约大家的时间。

在使用前，请一定要仔细阅读[使用说明文档]https://github.com/xuexiangjys/XUI/wiki),重要的事情说三遍！！！

在使用前，请一定要仔细阅读[使用说明文档]https://github.com/xuexiangjys/XUI/wiki),重要的事情说三遍！！！

在使用前，请一定要仔细阅读[使用说明文档]https://github.com/xuexiangjys/XUI/wiki),重要的事情说三遍！！！

## 关于我

[![github](https://img.shields.io/badge/GitHub-xuexiangjys-blue.svg)](https://github.com/xuexiangjys)   [![csdn](https://img.shields.io/badge/CSDN-xuexiangjys-green.svg)](http://blog.csdn.net/xuexiangjys)   [![简书](https://img.shields.io/badge/简书-xuexiangjys-red.svg)](https://www.jianshu.com/u/6bf605575337)   [![掘金](https://img.shields.io/badge/掘金-xuexiangjys-brightgreen.svg)](https://juejin.im/user/598feef55188257d592e56ed)   [![知乎](https://img.shields.io/badge/知乎-xuexiangjys-violet.svg)](https://www.zhihu.com/people/xuexiangjys) 

## X系列库快速集成

为了方便大家快速集成X系列框架库，我提供了一个空壳模版供大家参考使用: [https://github.com/xuexiangjys/TemplateAppProject](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ac2a2c7b3ae308edf4e3efeb4e59e0838ef424774a22ae746f936a8c2536680dc9faf07aa7396c6bf55b668c2c24fd32) 

除此之外，我还特别制作了几期[视频教程]https://space.bilibili.com/483850585/channel/detail?cid=104998)供大家学习参考.

----

## 特征

* 简洁优雅，尽可能少得引用资源文件的数量，项目库整体大小不足1M(打包后大约644k）
* 组件丰富，提供了绝大多数我们在开发者常用的功能组件。
* 使用简单，为方便快速开发，提高开发效率，对api进行了优化，提供一键式接入。
* 样式统一，框架提供了一系列统一的样式，使UI整体看上去美观和谐。
* 兼容性高，框架还提供了3种不同尺寸设备的样式（4.5英寸、7英寸和10英寸），并且最低兼容到Android 17, 让UI兼容性更强。
* 扩展性强，各组件提供了丰富的属性和样式API，可以通过设置不同的样式属性，构建不同风格的UI。

----

## 如何使用

> 在决定使用XUI前，你必须明确的一点是，此框架给出的是一整套UI的整体解决方案，如果你只是想使用其中的几个控件，那大可不必引入如此庞大的一个UI库，Github上会有更好的组件库。如果你是想拥有一套可以定制的、统一的UI整体解决方案的话，那么你就继续往下看吧！

### 添加Gradle依赖

1.先在项目根目录的 build.gradle 的 repositories 添加:
```
allprojects {
     repositories {
        ...
        maven { url "https://jitpack.io" }
    }
}
```

2.然后在dependencies添加:

```
dependencies {
  ...
  //androidx项目
  implementation 'com.github.xuexiangjys:XUI:1.1.4'

  implementation 'androidx.appcompat:appcompat:1.1.0'
  implementation 'androidx.recyclerview:recyclerview:1.1.0'
  implementation 'com.google.android.material:material:1.1.0'
  implementation 'com.github.bumptech.glide:glide:4.11.0'
}
```

【注意】如果你的项目目前还未使用androidx，请使用如下配置：

```
dependencies {
  ...
  //support项目
  implementation 'com.github.xuexiangjys:XUI:1.0.9-support'

  implementation 'com.android.support:appcompat-v7:28.0.0'
  implementation 'com.android.support:recyclerview-v7:28.0.0'
  implementation 'com.android.support:design:28.0.0'
  implementation 'com.github.bumptech.glide:glide:4.8.0'
}
```

### 初始化XUI设置

1.在Application最顶部初始化设置（必须）

```
XUI.init(this); //初始化UI框架
XUI.debug(true);  //开启UI框架调试日志

```

2.调整应用的基础主题（必须）

> 必须设置应用的基础主题，否则组件将无法正常使用！必须保证所有用到XUI组件的窗口的主题都为XUITheme的子类，这非常重要！！！

基础主题类型：

* 大平板(10英寸, 240dpi, 1920*1200）：XUITheme.Tablet.Big

* 小平板(7英寸, 320dpi, 1920*1200）：XUITheme.Tablet.Small

* 手机（4.5英寸, 320dpi, 720*1280）：XUITheme.Phone

```
 
       
     @color/colorPrimary 
     @color/colorPrimaryDark 
     @color/colorAccent 
  

```
当然也可以在Activity刚开始时调用如下代码动态设置主题

```
@Override
protected void onCreate(Bundle savedInstanceState) {
    XUI.initTheme(this);
    super.onCreate(savedInstanceState);
    ...
}
```

3.调整字体库（对字体无要求的可省略）

（1）设置你需要修改的字体库路径（assets下）
```
//设置默认字体为华文行楷，这里写你的字体库
XUI.getInstance().initFontStyle("fonts/hwxk.ttf");
```

（2）在项目的基础Activity中加入如下代码注入字体.

注意：1.1.4版本之后使用如下设置注入
```
@Override
protected void attachBaseContext(Context newBase) {
    //注入字体
    super.attachBaseContext(ViewPumpContextWrapper.wrap(newBase));
}
```

注意：1.1.3版本及之前的版本使用如下设置注入
```
@Override
protected void attachBaseContext(Context newBase) {
    //注入字体
    super.attachBaseContext(CalligraphyContextWrapper.wrap(newBase));
}
```

## 混淆配置

```
-keep class com.xuexiang.xui.widget.edittext.materialedittext.** { *; }

```

----

## 演示（请star支持）

### 演示程序截图

![](./art/1_splash.png) &emsp; ![](./art/2_main.png) &emsp; ![](./art/3_about.png) &emsp; ![](./art/4_menu.png)

![](./art/5_dialog.png) &emsp; ![](./art/6_bottom_dialog.png) &emsp; ![](./art/7_picker.png) &emsp; ![](./art/8_webview.png)

![](./art/9_flowlayout.png) &emsp; ![](./art/10_ninegrid.png) &emsp; ![](./art/11_radius_imageview.png) &emsp; ![](./art/12_badge_view.png)

![](./art/13_tabview.png) &emsp; ![](./art/14_citypicker.png) &emsp; ![](./art/15_refresh_layout.png) &emsp; ![](./art/16_spinner.png) &emsp;

### Demo下载

> 演示程序大概18M（主要是demo中集成了一个小视频拍摄的库比较大，大约13M左右，而XUI库目前只有644k大小），项目比较大，推荐使用蒲公英下载。

![](./art/xui_size.png)

#### 蒲公英下载

> 蒲公英下载的密码: xuexiangjys

[![蒲公英](https://img.shields.io/badge/downloads-蒲公英-blue.svg)](https://www.pgyer.com/XUIDemo)

![](./art/download_pugongying.png)

#### Github下载

[![Github](https://img.shields.io/badge/downloads-Github-blue.svg)](https://github.com/xuexiangjys/XUI/blob/master/apk/xuidemo.apk?raw=true)

![](./art/download_github.png)

## 特别感谢

* [QMUI_Android](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046616a54f950c74ea029f0c5e3dfb5ff9a8056c02f765899aca9bd098952add614) 
* [AgentWeb](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468cc166dccc66b72124fb584eb957f8c72a6a21d2a8ea338b25c377068fde6c97) 
* [Android-Iconics](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e3a05b03f6ce6935b2541e74061e0c9c922c501f62f249d0c28e2c4f2e2037db) 
* [Android-PickerView](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c5999ffcc5154870de1483c465aee838334c0ccc86c8fff616bb849a5e14bfcb) 
* [CityPicker](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469f8cfc5547387c2fb5d8caaa87f7ab62f11fd29f5e0ea53a338085b6755a045d) 
* [ELinkageScroll](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d6fe199e93f8d3d950c004446b1b15641ff12e2d3407a56e278ad9d2b4f9823a) 
* [FlycoBanner_Master](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c53c2247f7d96c31b730aee22ae9691fba730311d84e47eca0633cd74c563abd) 
* [Linkage-RecyclerView](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046297776f42839ab1d5bb267576309f3c5750fa8ee7f2fed475c2bdcd4c3530d96) 
* [MaterialEditText](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046810c1ba3189d4b09c3f88466c20dffaad5cb94b4090a2c00e7f931fe11b5d344) 
* [MaterialSpinner](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469e470e20c70351b391cee3cc2e74ec58785ce9a0fc8ce64c2d55c9942780ed0f) 
* [MaterialProgressBar](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046905ba87364c8eaee83d87367bc90635fb47ead6764dbafa952c432bc6a907a5ff8f6e39304c8d15e947b52df343d75ad) 
* [MPAndroidChart](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469a7ab35b5782ffa26df2295b70e3a96af1d786d87e97cbec04d7b001b2248820) 
* [PictureSelector](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e74580f150ab0d143d3e528746a837b5ce9561d0066b86e4d963a612113f5d60) 
* [SmartRefreshLayout](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046db62ac84945c3734293cab6a6c4fa895680c1a01646be29253fb4ee8568a5cdb) 
* [SlideBack](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b020142a4fd1a919e0010d60f35d7b069f632d428a61d98e59440fcfac550125) 
* [SwipeRecyclerView](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468fb670a0eb175388c5206dde9a38b3b84ff542057534655b562b450321696bb6) 


## 如果觉得项目还不错，可以考虑打赏一波

> 你的打赏是我维护的动力，我将会列出所有打赏人员的清单在下方作为凭证，打赏前请留下打赏项目的备注！

![](./art/alipay.jpeg) &emsp; ![](./art/weixinpay.jpeg)

感谢下面小伙伴的打赏：

姓名 | 金额 | 方式
:-|:-|:-
C*y | 1￥ | 微信
*流 | 1￥ | 微信
*声 | 50￥ | 微信
*宇涛 | 5￥ | 支付宝
*事 | 10￥ | 微信
优*1 | 168￥ | 微信
*、 | 20￥ | 微信
*钰晗 | 6￥ | 支付宝
*娜 | 3￥ | 微信
*米 | 20￥ | 微信
*忘 | 10￥ | 微信
*清红 | 1￥ | 支付宝
*口 | 5￥ | 微信
\* | 10.24￥ | 微信
*俊耀 | 100￥ | 支付宝
*俊杰 | 1￥ | 支付宝
*鸥 | 10.24￥ | 微信
*云 | 20.21￥ | 支付宝
*钰晗 | 66￥ | 支付宝
*杰柱 | 10￥ | 支付宝
*毛 | 6.66￥ | 微信
*凯 | 10￥ | 微信
r*o | 8.88￥ | 微信
T*8 | 7.77￥ | 微信
v*d | 20￥ | 微信
B*G | 1￥ | 微信
*舞 | 10￥ | 微信
*肉 | 2￥ | 微信
*拖 | 12.12￥ | 微信

## 联系方式

[![](https://img.shields.io/badge/XUI开源交流群-695048677-blue.svg)](http://shang.qq.com/wpa/qunwpa?idkey=a2ab505862c81f1528416b585832022e835ce0abe28eefa4b0d53f8094a5691d)
[![](https://img.shields.io/badge/XUI开源交流2群-700246750-blue.svg)](http://shang.qq.com/wpa/qunwpa?idkey=39497f13d5e456d219be785361a282d2d9c8cd9ba7745f6170def9d90643e164)

![](./art/xui_qq.jpg)



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)