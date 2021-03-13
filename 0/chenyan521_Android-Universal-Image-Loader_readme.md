# ![Logo](https://github.com/nostra13/Android-Universal-Image-Loader/raw/master/sample/src/main/res/drawable-mdpi/ic_launcher.png) Universal Image Loader [![Build Status](https://travis-ci.org/nostra13/Android-Universal-Image-Loader.svg?branch=master)](https://travis-ci.org/nostra13/Android-Universal-Image-Loader) [![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.nostra13.universalimageloader/universal-image-loader/badge.svg)](https://maven-badges.herokuapp.com/maven-central/com.nostra13.universalimageloader/universal-image-loader)

Android library **[#1]https://www.gitrep.com/search?utf8=✓&omni_search=&public_tags%5B%5D=android&description=&search=true&sort=star_count&commit=Search)** on GitHub.
UIL aims to provide a powerful, flexible and highly customizable instrument for image loading, caching and displaying. It provides a lot of configuration options and good control over the image loading and caching process.

![Screenshot](https://github.com/nostra13/Android-Universal-Image-Loader/raw/master/UniversalImageLoader.png)

## Project News 
 * Really have no time for development... so I stop project maintaining since Nov 27 :(
 * UIL [27.11.2011 - 27.11.2015]
 * Thanks to all developers for your support :)

## Features
 * Multithread image loading (async or sync)
 * Wide customization of ImageLoader's configuration (thread executors, downloader, decoder, memory and disk cache, display image options, etc.)
 * Many customization options for every display image call (stub images, caching switch, decoding options, Bitmap processing and displaying, etc.)
 * Image caching in memory and/or on disk (device's file system or SD card)
 * Listening loading process (including downloading progress)

Android 2.0+ support

## Downloads
 * **[universal-image-loader-1.9.5.jar](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d7b7fecec8c72fdeda13bcc3230f11270723e803153a8fdddcb7ee1b747b8cef2765aba70c651393e10b2135772f78b271e64e962931c8796c0612005aa494f8b190caa1bb6d6ea2e91bdb36f42a4f4fcf02969f28cb2bb8118c35332cc3c2ac3aeba62d7c1eede07ea7c18f2fb4dbe6 
 * [ ](https://play.google.com/store/apps/details?id=com.nostra13.universalimageloader.sample) [![QR Code](https://lh3.ggpht.com/csXEddxiLgQ6FxckefjQnP1PVugbaAYOdcuTa3vVtGV1PlWbFu2dYggoH8rI1w2RdEz1=w50)](http://chart.apis.google.com/chart?chs=300x300&cht=qr&chld=|1&chl=https%3A%2F%2Fplay.google.com%2Fstore%2Fapps%2Fdetails%3Fid%3Dcom.nostra13.universalimageloader.sample) [ ](https://github.com/nostra13/Android-Universal-Image-Loader/raw/master/downloads/universal-image-loader-sample-1.9.5.apk)

## [Documentation](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d7b7fecec8c72fdeda13bcc3230f11270723e803153a8fdddcb7ee1b747b8cefe35440a1daf55d61d55ee689936955a3) 
 * **[Quick Setup](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d7b7fecec8c72fdeda13bcc3230f11270723e803153a8fdddcb7ee1b747b8cef1a3e1f08688d6709e6d8f9758e276156f6d4452ef94579f5aae3e7d02ceb2d78 
 * **[Configuration](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d7b7fecec8c72fdeda13bcc3230f11270723e803153a8fdddcb7ee1b747b8cef1a3e1f08688d6709e6d8f9758e2761566abc4b532b27f601dfc6b0afdffc4391 
 * **[Display Options](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d7b7fecec8c72fdeda13bcc3230f11270723e803153a8fdddcb7ee1b747b8cef1a3e1f08688d6709e6d8f9758e2761566df89c8f2e15d66557a8635b6f104dff6d0330946e50856f35b4842d4cff1a19 
 * [Useful Info](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d7b7fecec8c72fdeda13bcc3230f11270723e803153a8fdddcb7ee1b747b8cef1a3e1f08688d6709e6d8f9758e2761563c9e10a5dcba681e7ed932d054b9550c)  - Read it before asking a question
 * [User Support](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d7b7fecec8c72fdeda13bcc3230f11270723e803153a8fdddcb7ee1b747b8cef1a3e1f08688d6709e6d8f9758e276156888aa4b6c475a1e553ecea1ce3f94710)  - Read it before creating new issue
 * [Sample project](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d7b7fecec8c72fdeda13bcc3230f11270723e803153a8fdddcb7ee1b747b8cef1bb3abf402f6770af4f64b42ef208aac76fa36a0b49e9793011502ecca58e190)  - Learn it to understand the right way of library usage
 * [ChangeLog](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d7b7fecec8c72fdeda13bcc3230f11270723e803153a8fdddcb7ee1b747b8cef51f3385615b82be4c0423796f6bac7f92b9821fbeeb438bc3d866faf41b73bce3ead2de3146dc83a35bb71deb24229b8)  - Info about API changes is here

## Usage

### Acceptable URIs examples
``` java
"http://site.com/image.png" // from Web
"file:///mnt/sdcard/image.png" // from SD card
"file:///mnt/sdcard/video.mp4" // from SD card (video thumbnail)
"content://media/external/images/media/13" // from content provider
"content://media/external/video/media/13" // from content provider (video thumbnail)
"assets://image.png" // from assets
"drawable://" + R.drawable.img // from drawables (non-9patch images)
```
**NOTE:** Use `drawable://` only if you really need it! Always **consider the native way** to load drawables - `ImageView.setImageResource(...)` instead of using of `ImageLoader`.

### Simple
``` java
ImageLoader imageLoader = ImageLoader.getInstance(); // Get singleton instance
```
``` java
// Load image, decode it to Bitmap and display Bitmap in ImageView (or any other view 
//	which implements ImageAware interface)
imageLoader.displayImage(imageUri, imageView);
```
``` java
// Load image, decode it to Bitmap and return Bitmap to callback
imageLoader.loadImage(imageUri, new SimpleImageLoadingListener() {
	@Override
	public void onLoadingComplete(String imageUri, View view, Bitmap loadedImage) {
		// Do whatever you want with Bitmap
	}
});
```
``` java
// Load image, decode it to Bitmap and return Bitmap synchronously
Bitmap bmp = imageLoader.loadImageSync(imageUri);
```

### Complete
``` java
// Load image, decode it to Bitmap and display Bitmap in ImageView (or any other view 
//	which implements ImageAware interface)
imageLoader.displayImage(imageUri, imageView, options, new ImageLoadingListener() {
	@Override
	public void onLoadingStarted(String imageUri, View view) {
		...
	}
	@Override
	public void onLoadingFailed(String imageUri, View view, FailReason failReason) {
		...
	}
	@Override
	public void onLoadingComplete(String imageUri, View view, Bitmap loadedImage) {
		...
	}
	@Override
	public void onLoadingCancelled(String imageUri, View view) {
		...
	}
}, new ImageLoadingProgressListener() {
	@Override
	public void onProgressUpdate(String imageUri, View view, int current, int total) {
		...
	}
});
```
``` java
// Load image, decode it to Bitmap and return Bitmap to callback
ImageSize targetSize = new ImageSize(80, 50); // result Bitmap will be fit to this size
imageLoader.loadImage(imageUri, targetSize, options, new SimpleImageLoadingListener() {
	@Override
	public void onLoadingComplete(String imageUri, View view, Bitmap loadedImage) {
		// Do whatever you want with Bitmap
	}
});
```
``` java
// Load image, decode it to Bitmap and return Bitmap synchronously
ImageSize targetSize = new ImageSize(80, 50); // result Bitmap will be fit to this size
Bitmap bmp = imageLoader.loadImageSync(imageUri, targetSize, options);
```

## Load & Display Task Flow
![Task Flow](https://github.com/nostra13/Android-Universal-Image-Loader/raw/master/wiki/UIL_Flow.png)


## Applications using Universal Image Loader
**[MediaHouse, UPnP/DLNA Browser](http://u.720life.cn/g/b77c9812b4c231c9db5ffbe20c7ac4514598fe0c0eef619f1c2864cffe959e0ac4bfabb522b5eac23c168265b1e7fafa5c43676e91448c49cdd1f5f4de09a3629defb09bb9b7abe14d6b25cac4b31143  | **[Prezzi Benzina (AndroidFuel)](http://u.720life.cn/g/b77c9812b4c231c9db5ffbe20c7ac4514598fe0c0eef619f1c2864cffe959e0ae943753608954931d7f168379124b7680c364385034575aeed906f9f0e9c7ef1891cb147d2edbc74e3be7110e42803b3  | **[ROM Toolbox Lite](http://u.720life.cn/g/b77c9812b4c231c9db5ffbe20c7ac4514598fe0c0eef619f1c2864cffe959e0ac4bfabb522b5eac23c168265b1e7fafa248b75d78b4aa0affd955e993c0d67bf8974c52053ece3e5b6185970ba0da96a  [Pro](http://u.720life.cn/g/b77c9812b4c231c9db5ffbe20c7ac4514598fe0c0eef619f1c2864cffe959e0ac4bfabb522b5eac23c168265b1e7fafa248b75d78b4aa0affd955e993c0d67bf54687d6c4d1ea72b38a75cf2d306bce6)  | [Stadium Astro](http://u.720life.cn/g/b77c9812b4c231c9db5ffbe20c7ac4514598fe0c0eef619f1c2864cffe959e0ac4bfabb522b5eac23c168265b1e7fafa3c36dd224b96dd4290cca79e8e231c1aebc7a491b1c5170a5a81a0987d14500c)  | [Chef Astro](https://play.google.com/store/apps/details?id=com.sencha.test) | [Sporee - Live Soccer Scores](https://play.google.com/store/apps/details?id=com.sporee.android) | **[EyeEm - Photo Filter Camera](https://play.google.com/store/apps/details?id=com.baseapp.eyeem)** | **[Topface - meeting is easy](https://play.google.com/store/apps/details?id=com.topface.topface)** | **[reddit is fun](https://play.google.com/store/apps/details?id=com.andrewshu.android.reddit)** | **[Diaro - personal diary](https://play.google.com/store/apps/details?id=com.pixelcrater.Diaro)** | **[Meetup](https://play.google.com/store/apps/details?id=com.meetup)** | [Vingle - Magazines by Fans](https://play.google.com/store/apps/details?id=com.vingle.android) | [Anime Music Radio](https://play.google.com/store/apps/details?id=com.maxxt.animeradio) | [WidgetLocker Theme Viewer](https://play.google.com/store/apps/details?id=com.companionfree.WLThemeViewer) | [ShortBlogger for Tumblr](https://play.google.com/store/apps/details?id=com.luckydroid.tumblelog) | [SnapDish Food Camera](https://play.google.com/store/apps/details?id=com.vuzz.snapdish) | **[Twitch](https://play.google.com/store/apps/details?id=tv.twitch.android.viewer)** | [TVShow Time, TV show guide](https://play.google.com/store/apps/details?id=com.tozelabs.tvshowtime) | [Planning Center Services](https://play.google.com/store/apps/details?id=com.ministrycentered.PlanningCenter) | **[Lapse It](https://play.google.com/store/apps/details?id=com.ui.LapseIt)** | [My Cloud Player for SoundCloud](https://play.google.com/store/apps/details?id=com.mycloudplayers.mycloudplayer) | **[SoundTracking](https://play.google.com/store/apps/details?id=com.schematiclabs.soundtracking)** | [LoopLR Social Video](https://play.google.com/store/apps/details?id=com.looplr) | [Hír24](https://play.google.com/store/apps/details?id=hu.sanomamedia.hir24) | **[Immobilien Scout24](https://play.google.com/store/apps/details?id=de.is24.android)** | **[Lieferheld - Pizza Pasta Sushi](https://play.google.com/store/apps/details?id=de.lieferheld.android)** | [Loocator: free sex datings](https://play.google.com/store/apps/details?id=com.ivicode.loocator) | [벨팡-개편 이벤트,컬러링,벨소리,무료,최신가요,링투유](https://play.google.com/store/apps/details?id=com.mediahubs.www) | [Streambels AirPlay/DLNA Player](https://play.google.com/store/apps/details?id=com.tuxera.streambels) | [Ship Mate - All Cruise Lines](https://play.google.com/store/apps/details?id=shipmate.carnival) | [Disk & Storage Analyzer](https://play.google.com/store/apps/details?id=com.mobile_infographics_tools.mydrive) | [糗事百科](https://play.google.com/store/apps/details?id=qsbk.app) | [Balance BY](https://play.google.com/store/apps/details?id=com.vladyud.balance) | **[Anti Theft Alarm - Security](https://play.google.com/store/apps/details?id=br.com.verde.alarme)** | **[XiiaLive™ - Internet Radio](https://play.google.com/store/apps/details?id=com.android.DroidLiveLite)** | **[Bandsintown Concerts](https://play.google.com/store/apps/details?id=com.bandsintown)** | **[Save As Web Archive](https://play.google.com/store/apps/details?id=jp.fuukiemonster.webmemo)** | [MCPE STORE -Download MCPE file](https://play.google.com/store/apps/details?id=com.newidea.mcpestore) | **[All-In-One Toolbox (29 Tools)](http://aiotoolbox.com/)** | [Zaim](https://play.google.com/store/apps/details?id=net.zaim.android) | **[Calculator Plus Free](https://play.google.com/store/apps/details?id=com.digitalchemy.calculator.freedecimal)** | [Truedialer by Truecaller](https://play.google.com/store/apps/details?id=com.truecaller.phoneapp) | [DoggCatcher Podcast Player](https://play.google.com/store/apps/details?id=com.snoggdoggler.android.applications.doggcatcher.v1_0) | [PingTools Network Utilities](https://play.google.com/store/apps/details?id=ua.com.streamsoft.pingtools) | [The Traveler](https://play.google.com/store/apps/details?id=edu.bsu.android.apps.traveler) | [minube: travel photo album](https://play.google.com/store/apps/details?id=com.minube.app) | [Wear Store for Wear Apps](https://play.google.com/store/apps/details?id=goko.ws2) | [Cast Store for Chromecast Apps](https://play.google.com/store/apps/details?id=goko.gcs) | [WebMoney Keeper](https://play.google.com/store/apps/details?id=com.webmoney.my)

## Donation
You can support the project and thank the author for his hard work :)

       
* **PayPal** - nostra.uil[at]gmail[dot]com

## Alternative libraries

 * [AndroidQuery : ImageLoading](http://u.720life.cn/g/b1f73db7c3bd88ab3d1af6161318928ebfcfbad3a4f24a8b68f18249a87f44cdc5750c8be8100b34fb7e03bbd5bb843c2e6472d4a41bbb0d8c1ab5b971f75907) 
 * [DroidParts : ImageFetcher](http://u.720life.cn/g/b68f0d2708b359264551bdc91f9932ad74ea5b1fef3036df15a041bb4a243ad89b570f2cf061e11081e03c1106a55f4a) 
 * [Fresco](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469caf98d0c1019e9d782070f925a64620724cbb526881454e454ae62552057ca9) 
 * [Glide](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304651118b5c333a886eda9bc25794653510551309d554f196c3515983f263dd5c9a) 
 * [Picasso](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d3ccc8c26dcb1110678f852b40cf69cf14a09c9af79f6504e149c9409e3c6d2b) 
 * [UrlImageViewHelper](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c052b296d15f2ddfb41b16e0037b34ff0ad511afac46fce327191aa7c4aa46a5) 
 * [Volley : ImageLoader](http://u.720life.cn/g/56e220b236c4ae56c0fa270f62d2a7b3d6d52d2725324e53b0d7f1edb25a1546a0c62b659b2f67c742f30b70e2c94815949f7d8daddd3a7c730f15275ccc70cf) 

## License

    Copyright 2011-2015 Sergey Tarasevich

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)