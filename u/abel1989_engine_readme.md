 
     
 
 
     
         
     
     
         
     
     
         
     
     
         
     
     
         
     
 

# Cocos Creator

![image](https://user-images.githubusercontent.com/1503156/50451713-97d7cc00-0970-11e9-89f8-ccdd8b2cc5cb.png)

Cocos Creator is a complete package of game development tools and workflow, including a game engine, resource management, scene editing, game preview, debug and publish one project to multiple platforms. Cocos Creator focused on content creation, which has realized features like thorough scriptability, componentization and data driven, etc. on the basis of Cocos2d-x. With JavaScript, you can scripting your component in no time. The editor and engine extension is also made with JavaScript so you can make games and refine your tool in a single programming language. Cocos Creator is an provides an innovative, easy to use toolset such as the UI system and Animation editor. The toolset will be expanding continuously and quickly, thanks to the open editor extension system.

This repo is the engine framework for Cocos Creator. Cocos Creator's in-editor scene view and web runtime share the same framework, which is the content of this repo. It's originally forked from [Cocos2d-html5](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046db77290c8b3fa3c71213f7d3f622f28adfc39d216b6fea927dedf2c60f78eb98  we build up an Entity Component architecture on it to meet the needs of Cocos Creator. 

This framework is a cross-platform game engine written in JavaScript and licensed under MIT. It supports major desktop and mobile browsers, it's also compatible with [Cocos2d Javascript Binding engine](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304649b1bd187d85162badc2de51f7843681edc7856807f02784d7bf69e6a2ef8776)  to support native platforms like iOS, Android, Win32, macOS.

The framework is naturally integrated with Cocos Creator, so it's not designed to be used independently.

## Developer

### Prerequisite

- Install [node.js v8.0.0+](http://u.720life.cn/g/6dd25ec2eceebbb6348ad519a7343cbc690041c96fefc0320d9aace915151649) 
- Install [gulp-cli v3.9.0+](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462d9ea9e61ffe1cc55f7ff0b90a018135aeb6480caae8f9f3c961929b7bc72634dc70dc97137a44f3d5751df0e4b61b0e869f1bd6c3a403625022bc98993a194e) 

### Install

In cloned project folder, run the following command to setup dev environment:

```bash
# Initialize gulp task dependencies
# npm is a builtin CLI when you install Node.js
npm install
```

This is all you have to do to set engine development environment.

### Build

```bash
gulp build
```

If the compilation process encounters a "JavaScript heap out memory" warning, you can use the following command line

```bash
gulp build --max-old-space-size=8192
```

### Test

#### Prerequisite

 - Install [express](http://u.720life.cn/g/7e435bb7ea8b678eb5a90145f8db35585a9d4b668ee2d3b5780858d809b0b655  `npm install express`
 - Install gulp-qunit: `npm install gulp-qunit`

#### Unit Test

##### Test in CLI

```bash
npm test
```

##### Test in browser

1. Build for testing.  

    ```bash
    gulp build-test
    ```

2. Start express in cloned project folder.

    ```
    node test/qunit/server.js
    ```

3. Open [http://localhost:8511/bin/qunit-runner.html](http://u.720life.cn/g/e71094f6077cb9592da5b56893f0ad146d2ebdb135230c61d7aed12091008a9c5de356219ebc157537dcadc1825e73bd)  in your browser.

### DebugInfos

View [EngineErrorMap.md](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304649b1bd187d85162badc2de51f7843681c678fbe7064922bf31eb13b89b26c5891e7767545dc8f15f22fa1d804ba4225f9063d26994b1551c1e10bae144e7713b)   
All the debug infos are defined in file EngineErrorMap.md.  
The file DebugInfos.json will be generated based on EngineErrorMap.md, when run gulp build* command.

For details below:

1. Define log in EngineErrorMap.md 

    example
    ```
    ### 1001  
      
    cocos2d: removeAction: Target not found
          
    ```

2. Define deprecated log in EngineErrorMap.md 
   The log should be marked as DEPRECATED when then logId is no longer referenced in the project.

    example
    ```
    ### 1000
      
     
    cc.ActionManager.addAction(): action must be non-null  
    
    ```

## Useful links

* [Official site](http://u.720life.cn/g/7504c84cf53604cb729da7a2b71638454b534351d3c9b5f108653d5d1992eacf) 
* [Download](http://u.720life.cn/g/7504c84cf53604cb729da7a2b7163845fa7319773d91357a731c30a11408bb3f) 
* [Documentation](http://u.720life.cn/g/fa4f999ae3ad37d8f7fb22a96b742762c33de4d99158524341b18e6f55da4d3925d23ce8870e4c51a9b255ee43e2a9f6) 
* [API References](http://u.720life.cn/g/fa4f999ae3ad37d8f7fb22a96b742762c33de4d99158524341b18e6f55da4d396f65fa53ef280e1f5e25f1ab2836563c) 
* [Forum](http://u.720life.cn/g/255826a2d93edb3dacc552364063ec9c6f6be183806e62c57c5282124e826c73be14ffa9b716339948cec313ef8ab547) 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)