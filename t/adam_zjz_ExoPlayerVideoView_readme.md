# ExoPlayerView
ExoPlayerView is a simple video view based on [ExoPlayer](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046977806ad0a6f64ac9388fbf8efea2879f49fe71eb852667c1742aa545f78d945 

[中文](/README_CN.md).

![brightness](/images/brightness_new.png)
![controller_1](/images/controller_1_new.png)
![fast_forward_rewind](/images/fastforward_rewind_new.png)
![landscape](/images/landscape_new.png)
![portrait](/images/portrait_new.png)
![volume](/images/volume_new.png)

Just add the following to your `build.gradle` file

    compile 'com.jarvanmo:exoplayerview:0.1.0'

ExoPlayerView can play simple video directly, such as mp4,m3u8 and so on.
It's easy to use.
Just declare ExoVideoView in your layout files:
```xml

     
        
```
The ExoVideoView provide 4 modes to resize your video: fit ,  fit_width , fit_height
and none.

The attribute  orientationAuto determines that the orientation of controller should 
be managed by sensor or not.The video view will call this when orientation is changed.
```java
   videoView.setFullScreenListener(new ExoVideoPlaybackControlView.ExoClickListener() {
         @Override
         public void onClick(View view, boolean isPortrait) {
             videoView.changeOrientation();
          }
   });
```
and the parameter(view) will be null if changed by sensor.
NOTE:The video view won't change its orientation by sensor automatically because I
want user to change it by code in current version.That's what I do during my work.
I'll add this function in the future.  


We can play a video just like:
```java
   videoView.play(mediaSource);
```
The ExoVideoView will create SimpleExoPlayer by itself if we play mediaSource.
Actually, you can set a player by yourself;
```java
    videoView.setPlayer(player);
```

We can play from a particular position too:
```java
   videoView.play(mediaSource,where);
```
Note:don't forget to release ExoPlayer:
```java
videoView.releaseSelfPlayer();
```
also we can give a display name:
```java
 mediaSource.setDisplayName("LuYu YouYue");
```
or
```java
 videoView.setDisplayName("LuYu YouYue");
```


There are also some listeners for you :
```java

        videoView.setBackListener(new ExoVideoPlaybackControlView.ExoClickListener() {
            @Override
            public void onClick(View view, boolean isPortrait) {
                if(isPortrait){
                    finish();
                }else {
                    videoView.changeOrientation();
                }
            }
        });

```

```java
        videoView.setFullScreenListener(new ExoVideoPlaybackControlView.ExoClickListener() {
            @Override
            public void onClick(View view, boolean isPortrait) {
                videoView.changeOrientation();
            }
        });
```
Note:The method `changeOrientation()` only determine the style of the 
playback controller view.


Also you can add you view to the controller view when landscape:

```java
       videoView.addViewToControllerWhenLandscape(view);
```
the view you want to add will add into FrameLayout．

The ExoPlayer also support simple gesture action, such as change-volume,
change-brightness and so on.If your target SDK version is 23
or higher, don't forget to request the following permission:
```xml
 
```


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)