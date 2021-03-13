
## What is Moquette?

[![Build Status](https://api.travis-ci.org/moquette-io/moquette.svg?branch=master)](https://travis-ci.org/moquette-io/moquette)

* [Documentation reference guide](http://u.720life.cn/g/7ab690d14cb774bc5375c71058a5868a9d69f5648da8ca5eee917e7a0c4f92f9bb0437c362a6ddad1da1b12d75508d48)  Guide on how to use and configure Moquette
* [Google Group](http://u.720life.cn/g/941693b557d072bb769494a6a61fcd979ee9fee4d4fd0c2a6b8a30bc68eade21b1231b7fbeccd20c0334d143a8348f813c3c2e8fbd1d286957a21392cd82a0e1)  Google Group to participate in development discussions.

Moquette aims to be a MQTT compliant broker. The broker supports QoS 0, QoS 1 and QoS 2.

Its designed to be evented, uses Netty for the protocol encoding and decoding part.
 
## Embeddable

[Freedomotic](http://u.720life.cn/g/7f1e0d28f8ce20e4916f5ff7cf1b31516cb223baf1f2643837fdc5d590e62423)  is an home automation framework and uses Moquette embedded to interface with MQTT by a specific [plugin](http://u.720life.cn/g/d6295dcec2dcca2dbc2f5bff7781f9fdbb5c1cd7c5935eb04304959406e33c34942fa9d54909818c10a4d0270d1a6b87fa2cd87c09ee8db6cd6f52949fea2258f53769b14f00a1713ebff6ffd94b0716418e1579a0e9e19203e07f28618afbc8  

Moquette is also used into [Atomize Spin](http://u.720life.cn/g/c950bd935d32875cc77d2f0f14db4119be21e9209b2dcc6a3e6632d9fa854b1e)  a software solution for the logistic field.

Part of moquette are used into the [Vertx MQTT module](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046edef9a54c68d71b516283b50fd5d4afad1fd06b3a83a3e61e6806f6db338bc3c00e0af374b7449819082bfc5e764857c  into [MQTT spy](http://u.720life.cn/g/77b2010e7b7c82494a56e4393a605482b1b9adb07b08d0ec5cc6d8d84ca672a48914c11f82dc9b7c77a01c7b761a847b) 
and into [WSO2 Messge broker](http://u.720life.cn/g/a602471bf2f09d58879d8cdbaf1771b030df9851af110b1a1aef67021358682a15b00d4294a3ded8d691a5a9ce3ae2e15584d6110e69ef5251d32ae68393dea524dc1094b0c3088f9b465514bbad17ec27de0d4804256016c2f4255459075645 

## Try the demo instance

Point your browser to [cloud instance](http://u.720life.cn/g/f128f1d49834b23c96073cbb06b0c38d14367e7ecfc00a85192c9c7dac58c3f6  request an account then use it from your MQTT clients.

## 1 minute set up

Start play with it, download the self distribution tar from [BinTray](http://u.720life.cn/g/30aa4dd72d94f39a9fd13b96c7f343665821b26a1b651f68600fd7615fd57b25246fa28b028b840401bb5ce43c0fbd7b1a246789fbbbbd03ea6b9316a8cb5d7477ba3482617f77d770063c3e019dd458)  ,
the un untar and start the broker listening on `1883` port and enjoy!

```
tar xvf moquette-distribution-0.12.1.tar.gz
cd bin
./moquette.sh
```

Or if you are on Windows shell

```
 cd bin
 .\moquette.bat
```

## Embedding in other projects

To embed Moquette in another maven project is sufficient to include a repository and declare the dependency: 

```
 
   
     bintray 
     https://jcenter.bintray.com 
     
       true 
     
     
       false 
     
   
 
```

Include dependency in your project: 

```
 
       io.moquette 
       moquette-broker 
       0.12.1 
 
```

## Build from sources


After a git clone of the repository, cd into the cloned sources and: `./gradlew clean moquette-distribution:distMoquetteTar` or
`./gradlew clean moquette-distribution:distMoquetteZip`.


In distribution/build directory will be produced the selfcontained file for the broker with all dependencies and a running script. 
  

---

If you like Moquette you can support us by donating.

 
   
 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)