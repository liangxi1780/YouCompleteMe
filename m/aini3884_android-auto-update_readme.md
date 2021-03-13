Android应用自动更新库(android-auto-update)
===================


该library项目实现了软件版本检查，apk文件下载，软件安装（Android app update checker,download and install apk）支持API 8+


#### 1.导入library项目 ####

提供2种版本检查方式,在你的项目中添加以下代码即可

- 使用Dialog
   
    	`UpdateChecker.checkForDialog(this);`

- 使用Notification

	`UpdateChecker.checkForNotification(this);`



#### 2.添加权限 ####

- 添加访问网络的权限

	` `

- 添加写SDCard权限（可选，非必须）

	如果添加这个权限 apk下载在sdcard中的Android/data/包名/cache目录下 否则下载到 内存中的 /data/data/包名/cache中

	` `

#### 3.截图 ####
![screenshot](https://raw.github.com/feicien/android-auto-update/master/screenshots/sample.png)
![screenshot](https://raw.github.com/feicien/android-auto-update/master/screenshots/sample_htc.png)
![screenshot](https://raw.github.com/feicien/android-auto-update/master/screenshots/dialog.png)
![screenshot](https://raw.github.com/feicien/android-auto-update/master/screenshots/dialog_htc.png)
![screenshot](https://raw.github.com/feicien/android-auto-update/master/screenshots/notification.png)
![screenshot](https://raw.github.com/feicien/android-auto-update/master/screenshots/notification_avd.png)
![screenshot](https://raw.github.com/feicien/android-auto-update/master/screenshots/downloading.png)
![screenshot](https://raw.github.com/feicien/android-auto-update/master/screenshots/downloading_avd.png)


#### 4.使用与参考的开源项目 ####



1. [android-styled-dialogs](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461edb8c83cf32151501a402ca14fb395836239a40834ecb350eb3875259c07415  "https://github.com/inmite/android-styled-dialogs") 使用该项目，可以在api 8+上显示 holo 风格的对话框，其它选择
，当然你也可以使用其它的开源项目比如：[ActionBarSherlock](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462fc1dc3ddec2d78b2e26e64aa23f69d693916e6ada7aa8d3e884f1fc36de733d  "https://github.com/JakeWharton/ActionBarSherlock") 和 [HoloEverywhere](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304624e4b148520d08b4b560241219688472a8639bac76e863e34f1fbfd11022487e  "https://github.com/Prototik/HoloEverywhere")


2. [UpdateChecker](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046374e301f245c260c091b3f03a1ca3eac9cd7a141f5a5a29ddcafd70c865ef551  "https://github.com/rampo/UpdateChecker") 该项目检查的是google play上的应用，如果有更新打开google Play,不提供下载apk的功能

 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)