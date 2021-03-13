# QtScrcpy 

![build state](https://img.shields.io/badge/build-passing-brightgreen.svg)
![license](https://img.shields.io/badge/license-Apache2.0-blue.svg)
![release](https://img.shields.io/badge/release-v1.0.1-brightgreen.svg)

[中文介绍](README_zh.md)

QtScrcpy can connect to Android devices via USB (or via TCP/IP) for display and control. No root privileges are required.

A single application can support up to 16 Android devices to connect at the same time.

Supports three major desktop platforms, GNU/Linux, Windows and MacOS.

![win](screenshot/win.png)

![mac](screenshot/mac.jpg)

![linux](screenshot/ubuntu.png)

## Custom keymap（only windows enable）
You can write your own script to map the PC keyboard keys to the touch and click of the mobile phone according to your needs. [Here](docs/按键映射说明.md) are the rules.

By default, it has its own mapping script for key and mouse mapping of "Game for peace" mobile games. When enabled, you can use key and mouse to play "Game for peace" mobile games like PC games. You can also write mapping files of other games according to [writing rules](docs/按键映射说明.md). The default key mapping is as follows:

![game](screenshot/game.jpg)

[Here is a video demonstration of playing "Game for peace"](http://u.720life.cn/g/ecc7d42b8e4205e5d387aa616e7cff786315a54a0172f57fb205a477c948a9c065cb5d029620f6c35557e639d47686c1875137018257f87aa8a17a9f525a4a4d2046a9cb881b0b6cf1901b8e0a626d410741e95602ffd54ec7dd66a3d650be28c978ce1365c9a869af00e4977fa395167d6a1ba24be4073058dedf2213395125a5382dda052839e95637de0c6bd1120a7ac35ddb8606891d5e444c420d61d5eb676cf515785eb48db1fc150d06675b675a71c2b3be9ffa79b800b190c06000939770d439cf4434981c85f1aebfa4d046a41d173b9b7ab487211136bd3b12f636d5e989b24eb62c56e18f45702400c3e1c0745a94f937bb3d2f2ceaf2680d8730f16056bf79f9fec08143eb7274ee480b5bc70a374bb421ac06cf0bcaf71ef921a8be217e35379587bf2f1c691ef8e9eb238663a959dc9af023581382c466e2f5365c170ec9b0518a77f8037599f2aba39f32ddfb7b2505bc1e6a4cde86df6a5f23b42c1be0d8683dcef34beee5cd9548ace02a6d5d26ec8fe98fcf83fbe6ba50) 

The operation method of custom key mapping is as follows：
- Write a custom script and put it in the keymap directory
- Check the custom mapping option and select the custom mapping script before starting the service
- Enter the game scene after connecting the mobile phone
- Press the ~ key (left side of the number key 1) to switch to the game mapping mode to experience (what key to press depends on the switchkey defined by your key script)
- Press the ~ key again to switch to normal control mode
- To start the WASD control car, remember to set it to single rocker mode in vehicle settings.

## Thanks

QtScrcpy is based on [Genymobile's](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d7fd888f79f10269569747fc324e5ed9)  [scrcpy](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046182fc10086ed8dfcf20aef2c3a6da432ab341c4fe984a6d70998f7fbd55604ad)  project and is very grateful to him.

The difference between QtScrcpy and the original scrcpy is as follows:

keys|scrcpy|QtScrcpy
--|:--:|:--:
ui|sdl|qt
video decode|ffmpeg|ffmpeg
video render|sdl|opengl
base tool|c++|Qt
language|C|C++
style|sync|asyn
build|meson+gradle|Qt Creator

- It's very easy to customize your interface with Qt
- Asynchronous programming of Qt-based signal slot mechanism improves performance
- Easy for novices to learn
- Add multi touch support


## Learn

If you are interested in it and want to learn how it works and feel that you can't get started, you can choose to purchase my recorded video lessons.
It details the development architecture and development process of the entire software, and takes you to develop QtScrcpy from scratch.：

course introduction：[https://blog.csdn.net/rankun1/article/details/87970523](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79ded00cfce5007324447cf873a663e2fb2770fc135724290bd18f5cd248f7f387f80421d528055666479c922f2ac3d9b66fb) 

Or you can join my QtScrcpy qq group and exchange ideas with like-minded friends.：

QQ Group number：901736468


## Requirements
The Android part requires at least API 21 (Android 5.0).

Make sure you enabled [adb debugging][enable-adb] on your device(s).

[enable-adb]: https://developer.android.com/studio/command-line/adb.html#Enabling


## Download

[gitee-download]: https://gitee.com/Barryda/QtScrcpy/releases
[github-download]: https://github.com/barry-ran/QtScrcpy/releases

### Windows
For Windows, for simplicity, prebuilt archives with all the dependencies (including adb) are available:

 - [`QtScrcpy`][github-download]

or you can [build it by yourself](#Build)

### Mac OS
For Mac OS, for simplicity, prebuilt archives with all the dependencies (including adb) are available:

- [`QtScrcpy`][github-download]

or you can [build it by yourself](#Build)

### Linux
you can [build it by yourself](#Build)(just ubuntu test)


## Run

Connect to your Android device on your computer, then run the program and click the button below to connect to the Android device.

![run](screenshot/run.png)

### Wireless connection steps (ensure that the mobile phone and computer are in the same LAN):
1. Enable USB debugging in developer options on Android mobile terminal
2. Connect Android phone to computer via USB
3. Click update device, and you will see that the device number is updated.
4. Click get ip
5. Click start adbd
6. Click wireless connect
7. Click update device again, and another device with IP address beginning is found. Select this device.
8. Click start service

## Interface button introduction：

- Startup configuration: function parameter settings before starting the service    

    You can set the bit rate, resolution, recording format, and video save path of the local recorded video.

    - Recording only in the background: Starting the service is not realistic, just recording the Android device screen
    - Window Top: Android device video window top display
    - Close screen: automatically turn off the Android device screen to save power after starting the service
    - Use reverse: service startup mode, service startup failure error more than one device can remove this check to try to connect
    

- Refresh device list: Refresh the currently connected device
- Start the service: connect to the Android device
- Stop service: disconnect from Android device
- Stop all services: disconnect all connected Android devices
- Get device ip: Get the IP address of the Android device and update it to the "Wireless" area for easy wireless connection.
- Start adbd: Start the adbd service of the Android device, you must start it before the wireless connection.
- Wireless connection: Connect to Android devices wirelessly
- Wireless disconnect: Disconnect wirelessly connected Android devices
- adb command line: convenient to execute custom adb commands (currently does not support blocking commands, such as shell)


## The main function
- Display Android device screens in real time
Real-time mouse and keyboard control Android device
- Screen recording
- Wireless connections
- Supports up to 16 device connections (can be added if PC performance allows, you need to compile it yourself)
- full-screen display
- Window topping
- Install apk: drag and drop apk to the video window to install
- Transfer files: Drag files to the video window to send files to Android devices
- Background recording: record only, no display interface

## TODO
[TODO](docs/TODO.md)

## FAQ
[FAQ](docs/FAQ.md)

## Why develop QtScrcpy?
There are several reasons for this, and the proportions are arranged from large to small:
1. In the process of learning Qt, you need a project to combat
2. It has audio and video related skills and is very interested in audio and video.
3. It has Android development skills, it’s a bit rusty for a long time, you need to consolidate it.
4. Found scrcpy, decided to re-entamrate with the new technology stack (C++ + Qt + Opengl + ffmpeg)


## Build
Try to provide all the dependencies and make it easy to compile.

### PC client
1. Set up the Qt development environment on the target platform (Qt >= 5.9.7, vs >= 2015 (not support mingw))
2. Clone the project
3. Open the project root directory all.pro with QtCreator
4. Compile and run

### Android (If you do not need to modify the requirements, you can use the built-in scrcpy-server.jar directly)
1. Set up an Android development environment on the target platform
2. Open the server project in the project root directory using Android Studio
3. Build it
4. After compiling apk, rename it to scrcpy-server.jar and replace third_party/scrcpy-server.jar.

## Licence
Since it is based on scrcpy, respect its Licence

    Copyright (C) 2018 Genymobile

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

## About the author

[Barry CSDN](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79ded464c066891ee903c822dbfe34be5ea6d) 

An ordinary programmer, working mainly in C++ for desktop client development, graduated from Shandong for more than a year of steel simulation education software, and later moved to Shanghai to work in security, online education related fields, familiar with audio and video. I have an understanding of audio and video fields such as voice calls, live education, video conferencing and other related solutions. At the same time have android, linux server and other development experience.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)