[![JetBrains incubator project](http://jb.gg/badges/official.svg)](https://confluence.jetbrains.com/display/ALL/JetBrains+on+GitHub) 

# Kotlin Spinner Game

Simple spinner-like game intended to demonstrate capabilities of Kotlin/Native software stack

## How to play

*   Download and install the mobile application for [Android](http://u.720life.cn/g/b77c9812b4c231c9db5ffbe20c7ac4514598fe0c0eef619f1c2864cffe959e0ac4bfabb522b5eac23c168265b1e7fafa296263d98aef779af4245a2e738ea8ecac34e86f3857e544323d53538dec970f)  or [iOS](http://u.720life.cn/g/691fbefe595b3d5ed0d2fd14e433ba9869258af0e1b040bde26bfe15dc6eb359960edea0503712d7e99629de9f7c985854212aa5111a3ba533fc69b7668efbbb124ece4bd0288d78952dad2931a4b501) 
*   The system will automatically assign you to a random team. Each team has a unique colour
*   Spin the Kotlin logo using your fingers, or alternatively shake your phone
*   Each two full rotations (i.e. 720 degrees) will increment your team's score
*   The team with the highest score wins

## Technical details
The entire application is implemented using [Kotlin/Native](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046126f1c80255df7a7084842247b9fdff671a075320a96319766dc3887f6673d94) 

### Server-Side

[Server side](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046126f1c80255df7a7084842247b9fdff6b4a401525616a59f671ad2b267a894d7e61122698a038f0e558c81da3499a76354e20cc623460c6f4b99ee8d15fe3aeb1252e851fe73769e5b7c2ddfaffefb92bbff85a5859c221d1e400f7304808a740d5ac0e966ae59779cca698329b12221f57c27dc95f22714ff5a544502e2a02f)  runs on a linux server and is implemented using:

*   [microHTTPD](http://u.720life.cn/g/80aceec34af2d650b057d93ea119d365c43a6e12b86b39375e14fb36a64060e2c1e92e02c45cf2e6f923f0aaf57f643d)  HTTP server library
*   [SQLite](http://u.720life.cn/g/835011cc069504b6245036337ae92d7e35e412b4c7432e14e5398b52a7d96cf7)  for the database, storing score
*   [Jansson](http://u.720life.cn/g/526a219f04c3e777915078fd2c5f396eef02e511cb63d08e2b8c970899bf5d05)  for JSON serialization and client/server communication

### Client-Side 

#### Android 

[Client side](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046126f1c80255df7a7084842247b9fdff6b4a401525616a59f671ad2b267a894d7e61122698a038f0e558c81da3499a76354e20cc623460c6f4b99ee8d15fe3aeb66e29548cf85570a516786443c7e2431b32208a3093f4dc66c11893bf2c604eae48e3d50c46edf086cc1715deff3ec230a3ef525bb7de3c95dbd16c5a20e8a14)  for Android is implemented in pure Kotlin/Native, as a Native Activity using:
*   [GLES version 3](http://u.720life.cn/g/a69e8f5dba5b4106ccc3875c547b1484e144945f286474f4370907a7f2d6bec72089bb3f64ad0c94f1d10824ef9e1e553edacb91ea2dbd9b0de0f7cf4a143990)  interop for 3D rendering
*   [NDK input handling](http://u.720life.cn/g/a69e8f5dba5b4106ccc3875c547b1484eaf99cc757b48fc96f74f685776e5c823be2fca4e8dcacf0712f7c62a0d1d8c66b302d938da4d4039455ad3f5ee5e7b5)  for input processing
*   [Open AL](http://u.720life.cn/g/25c6ec599554e791edfb864b96d06126fb9a193486166e5c405779503f8fcd5b)  interop for sound playback
*   [Sensors native API](http://u.720life.cn/g/a69e8f5dba5b4106ccc3875c547b1484eaf99cc757b48fc96f74f685776e5c823be2fca4e8dcacf0712f7c62a0d1d8c6478c58a13527a69748bcc3da86ca203c) 
*   [libcurl](http://u.720life.cn/g/c9fa89c66db4bfd512eaa45e319ce993b0bfebd3be3e728570507ac414af3f21)  file transfer library as HTTP client

#### iOS

[Client side](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046126f1c80255df7a7084842247b9fdff6b4a401525616a59f671ad2b267a894d7e61122698a038f0e558c81da3499a76354e20cc623460c6f4b99ee8d15fe3aeb66e29548cf85570a516786443c7e2431d5e778860f2235e93a24481ea6c09b92)  for iOS is implemented in pure Kotlin/Native using:
*   [GLES version 3 framework](http://u.720life.cn/g/a69e8f5dba5b4106ccc3875c547b148492cfec17ef8bb528fa0fc50595a3da38d60fe12c39cf3730a19d5eb3eb101489448ae9ad465d4adf0704438f39746d72)  for 3D rendering
*   [UIKit framework](http://u.720life.cn/g/a69e8f5dba5b4106ccc3875c547b148492cfec17ef8bb528fa0fc50595a3da38b1c3a57c411886b0cf3498a3f23ddc8f)  for windows and views
*   [CoreMotion framework](http://u.720life.cn/g/a69e8f5dba5b4106ccc3875c547b148492cfec17ef8bb528fa0fc50595a3da38df5a24b1776415f2d51fe79cf5d5f8be3c08d1aefe7591f059093cf83c1303cb)  for sensors access
*   [OpenAL framework](http://u.720life.cn/g/a69e8f5dba5b4106ccc3875c547b14842223b7aa17cd72ce46480dd6e45bc974e548f160b450787daee71e5df5729ef90e5cbd6b7d11527c0844e7669c07093bb4a10323c6be9b098eee6d98f6fb1511712116c8dd8ff8ee539b281c4595e4d14909b02e7b570a0f28de9a768e9cd1bfa0f35b62ac4dab17dd3089e2b7761f06be83e2a3fd6b56c4eddb0b31767cea2c368a1b9129c28210ebbfc8a2ca042cb80193d56cf9a8d29a7462a0efe86dbed0)  for audio playback

### Implementation details

*   Most graphical code, sound playback and user input reaction is [shared](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046126f1c80255df7a7084842247b9fdff6b4a401525616a59f671ad2b267a894d7c6e78ed138f80ce12eefead705563b68c8c1461273914dac2701525e4d4e882c96714b4d7b3bbcc144128a7957fc43ff2e4ff7522478f9212cbec2ffce1f1fa1012f1bd4428e2d79b3450154d724e054)  between Android and iOS
*   Server interaction on Android is [asynchronous](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046126f1c80255df7a7084842247b9fdff6b4a401525616a59f671ad2b267a894d7e61122698a038f0e558c81da3499a76354e20cc623460c6f4b99ee8d15fe3aeb66e29548cf85570a516786443c7e2431b32208a3093f4dc66c11893bf2c604eaac966e8961c395749d2b90bcf28cd520f09b6c225c4f732101fb98e02e8ab723711929f9738a55b2b698f7b910c0c6da)  from the UI thread, using [workers](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046126f1c80255df7a7084842247b9fdff62267212aa001c5fc28be4b78501bb4bb0169eabc47a2c67780df306887f8ea5ff36621ab1e5cafd1f0b67c6dce34a46f) 
*   HTTP server works in multithreaded mode, state sharing between sessions performed via SQLite DB access
*   Android app is split into separate [loader](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046126f1c80255df7a7084842247b9fdff6b4a401525616a59f671ad2b267a894d7e61122698a038f0e558c81da3499a76354e20cc623460c6f4b99ee8d15fe3aeb66e29548cf85570a516786443c7e2431b32208a3093f4dc66c11893bf2c604eab727986111f062eb5db957d6d378b5e308659ab36ec02914dfa16c38270b15af)  and application code, so that dynamic library (libopenal.so) included with application can be used on older Androids
*   [WebAssembly frontend](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046126f1c80255df7a7084842247b9fdff6b4a401525616a59f671ad2b267a894d7c6e78ed138f80ce12eefead705563b68c8c1461273914dac2701525e4d4e882c96714b4d7b3bbcc144128a7957fc43ff5bea4528018bcc073a32b0bfcca5042b)  can fetch and render stats in the browser

### Project Sources

Use JDK1.8, for Android compatibility, i.e.:
    export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_161.jdk/Contents/Home

To use microhttpd  (HTTP server) install it, i.e.:

    port install libmicrohttpd
    apt install libmicrohttpd-dev

To use jansson (JSON library) install it, i.e.:

    port install jansson
    apt install libjansson-dev

To use sqlite (embedded SQL server) install it:

    port install sqlite3
    apt install libsqlite3-dev

To use curl (HTTP client) install it:

    port install curl
    apt install libcurl3-nss



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)