     
   

 Java RAD framework for enterprise web applications 
  
 
   
   
 


 
   
     
      Website
     
      |  
     
      Online Demo
     
      |  
     
      Documentation
     
      |  
     
      Guides
     
      |  
     
      Forum
     
   
 

 
   
   
   
   
 
  
[CUBA Platform](http://u.720life.cn/g/f330c85adbe327e1f61b6405ff6aa86bf72ba17161245388923df482f08a8ab6)  is a high level framework for rapid development of enterprise applications with rich web interface.

The simplest way to start using the platform is to [download](http://u.720life.cn/g/f330c85adbe327e1f61b6405ff6aa86bb4fad68e65f51f28b78c7424462aa8c2539a19ab3c64e1f26ddd3e1978283e94)  CUBA Studio and create a new project in it. A released version of the platform will be downloaded automatically from the artifact repository.

You can also build a snapshot version of the platform from the source code and use it in your project.

To contribute, first refer to [Contributing Code](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304617c39dbbaa10eea47e6c57a7a7b06895bb8a1341dce8b7dd817a52c35efdcdc190858a32b4ee7da1a23ca9e45f524fb890698ceaa120c75d0f9090b3344d868c)  for general instructions and requirements for contributing code to the platform.

## Building from Source

In order to build the platform from source, you need to install the following:
* Java 8 Development Kit (JDK)
* [CUBA Gradle Plugin](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304617c39dbbaa10eea47e6c57a7a7b0689542ea872c10fe15b0100ac9186f55215930f1e8836444aa28dd71a430be0177f6) 

Let's assume that you have cloned CUBA Gradle Plugin and CUBA into the following directories:
```
work/
    cuba/
    cuba-gradle-plugin/
```

Open terminal in the `work` directory and run the following command to build and install the plugin into your local Maven repository (`~/.m2`):
```
cd cuba-gradle-plugin
gradlew install
```

After that, go to the CUBA directory and build and install it with the same command:
```
cd ../cuba
gradlew install
```

## Using Snapshot Version

Edit the `build.gradle` file of your project. Change the `ext.cubaVersion` property and add `mavenLocal()` to the `repositories` section, for example:
```
buildscript {
    ext.cubaVersion = '7.2-SNAPSHOT'
    repositories {
        mavenLocal()
        maven { ...
```
That's all. Now you can build and deploy your application based on the snapshot version of the platform from your local repository:
 ```
 gradlew deploy
 ```

## Third-party dependencies

The platform uses a number of forked third-party libraries. They can be found in the following source code repositories:

* [eclipselink](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304617c39dbbaa10eea47e6c57a7a7b06895e103b6839321c78e1285abe439fb7169) 
* [vaadin](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304617c39dbbaa10eea47e6c57a7a7b06895bd0bbc9eea10fd52694e2904f6d8f496) 
* [vaadin-dragdroplayouts](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304617c39dbbaa10eea47e6c57a7a7b0689557e9517b57cae4277fdd9a56671423b345de35183222807126135c6188403cd3) 
* [vaadin-aceeditor](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304617c39dbbaa10eea47e6c57a7a7b068958ba6270e7424cce976bfd06bdd905bc7717380d6ace7ff90f7929a2c9d6ff00a) 
* [swingx-core](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304617c39dbbaa10eea47e6c57a7a7b06895707c011ea3da3cfb544c09b439d8cd60) 

All dependencies are also located in our artifacts repository, so you don't have to build them from sources in order to build and use the platform.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)