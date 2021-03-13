
# LuaIde 
1. author:kangping  
1. **luaIde** 是基于vscode开发的一款用于lua语言开发者使用的插件  
1. 目标:致力于做最好的**跨平台**lua开发工具  
1. 更新:luaide 个人开发者开发持续更新 (**更新频率为一周一更**) 
1. 平台支持:**win**,**mac**  
1. 代码调试:理论上只要支持 **luasocket** 就能调试 如果你的游戏引擎或 lua框架需要调试 请联系我


# LuaIde 更新日志  


1. 2017/6/25 0.3.3-0.37  版本
	1. 方法返回值注释:`--@returnValue [Model.BaseModel]` 修改为 `--@return [Model.BaseModel]`
	2. 将同文件中的变量由只提示方法内的改为 当前文件全局提示
	3. 修复全局变量无法提示bug
	3. 修改某些情况方法返回值无法提示bug
	4. lua文件修改后在不保存的情况下搜索symbol定位错误
	5. 添加用户在线数量显示,可通过 `luaide.showOnLine` 进行关闭  5分钟刷新一次
	
1. 1. 2017/6/15 0.3.2 版本
	1. 修复添加新文件无法 无法在 require 和类型注释中提示的bug
	2. 修复for 循环中的变量错误的解析为全局变量
	3. 修复全局方法返回值 无法提示
	4. 添加注释提示
	5. 添加变量类型注释 `--@valueReference [Model.BaseModel] `  当输入[ 会列出当前文件中所有的文件
	4. 注释路径添加转到定义
	5. 添加写入初始化信息 文件夹权限不足提示
1. 2017/6/8 0.3.0 版本
	2. 增强代码推断能力,与0.2.x 版本用了两套逻辑 所以luaide 版本终结与0.2.1 以后待功能完善后 luaide将更名为luaIdeProfessional 
	3. 增加了 方法返回值 注释 和父类 类型注释
	1. 方法返回值注释:`--@returnValue [Model.BaseModel]`  当输入[ 会列出当前文件中所有的文件
	1. 父类类型注释:`--@parentClass [Model.BaseModel]`  当输入[ 会列出当前文件中所有的文件
	1. 两种注释需要 添加luaide 的配置 "luaide.scriptRoots": ["C:/Users/Administrator/Desktop/t"]

#重要提示
1.  [LuaDebug 下载地址](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a58cccd65a886bc83c4f7eec2a4b4d9c16c37687c0470f4bf9be974749a6b2b59d4b64c644263f139a2aa976204bbd24) 
2.  文档请直接查看[wiki](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a58cccd65a886bc83c4f7eec2a4b4d9c71cbf2b25014aa11aa38cd9b124fb23c) 
3.  qq群 **494653114** 
3.  调试文件为两个 LuaDebug,LuaDebugjit  添加调试文件时确认一下自己运行时选择对应的调试文件
4.  bug 和  问题 请留言 [issues](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a58cccd65a886bc83c4f7eec2a4b4d9ceb011a35b468d6b2840db19ca2bd6b67)   
4.  [调试视频](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a58cccd65a886bc83c4f7eec2a4b4d9c5c232d224255a7082fb7f046c4c8b55cd339d39f3a662745ba9b5b1ff43584757fa31169f3f73edcd486c3f8374c8dce)   
5. [历史版本](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a58cccd65a886bc83c4f7eec2a4b4d9c1d467ab98a82b467b9c9343552c1af54b12dae1827503473930ad3dba3737d1a)  如果当前版本出现bug 可将 win->:\Users\Administrator\.vscode\extensions   和 mac->user/.vscode/extensions 中对应的文件夹删除将历史版本解压重启vscode

#更新记录
1. 0.1.9->0.2.2 
	1. 修复模块方法创建 插入位置错误 修改为插入到当前方法结束后
	2. 方法注释 @desc 无法显示bug
	3. 优化  **require**  时 lua 文件路径提示 兼容 "xxx.xxx.xx" 和 自定义变量 注意如果需要显示"xxx.xxx.xxx" 需要设置 **luaide.scriptRoots** 
	4. 优化二进制lua文件导致的lua解析停止无法进行自动提示bug
	5. 添加最大文件检查限制 **luaide.maxFileSize** 默认为2048KB  
	6. **luaide.moduleFunNestingCheck** 默认值修改为false -->该检测一定几率会检查错误,该问题将在0.2.1 修复  
	7.  添加文件夹右键菜单 **[创建模板文件]**  模板文件配置 请看 [安装](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a58cccd65a886bc83c4f7eec2a4b4d9c2d2b76329c32d94a2870a94c5293b954a4bb468abb4837acdccaf64c3fa5758a)  --> **luaide.luaTemplatesDir**
	8. 修正方法参数无法提示bug
	9. 格式化代码后#与变量名中多出一个空格 修改  
	10. 修复由及时检查代码语法引起的 提示错误
1. 0.1.9->0.2.1 
	1. 添加 输入 **---** 自动生成方法注释 
	2. 优化方法信息提示 区分全局函数和局部函数
	3. 优化  **require**  时 lua 文件路径提示 兼容 "xxx.xxx.xx" 和 自定义变量 注意如果需要显示"xxx.xxx.xxx" 需要设置 **luaide.scriptRoots** 
	4. 优化二进制lua文件导致的lua解析停止无法进行自动提示bug
	5. 添加最大文件检查限制 **luaide.maxFileSize** 默认为2048KB  
	6. **luaide.moduleFunNestingCheck** 默认值修改为false -->该检测一定几率会检查错误,该问题将在0.2.1 修复  
	7.  添加文件夹右键菜单 **[创建模板文件]**  模板文件配置 请看 [安装](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a58cccd65a886bc83c4f7eec2a4b4d9c2d2b76329c32d94a2870a94c5293b954a4bb468abb4837acdccaf64c3fa5758a)  --> **luaide.luaTemplatesDir**
	8. 修正方法参数无法提示bug
	9. 格式化代码后#与变量名中多出一个空格 修改  
	10. 修复由及时检查代码语法引起的 提示错误
1. 0.1.8
	1. 根据 [guoweidong1987](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304628e9e978efd647ed4c3334f019805f72ba56927be68814131835b47633dadf20)  提供的方法修改lua代码格式化
	2. 添加 **luaide.ChangeTextCheck** 代码修改时是否检查lua语法是否正确
	3. 添加模块方法 **luaide.moduleFunNestingCheck**  模块方法嵌套检查,如果在一个方法中出现另外一个模块方法会认为是错误的
	4. 修改**self** 提示bug  无法提示三级和三级以上的代码  如 **self.data.index** 
	5. 添加  **require**  时 lua 文件路径提示
	
1. 0.1.7
	1. 添加显示介绍页面配置 **luaide.isShowDest** 默认为false 只显示一次,如需重复显示修改为true
	2. 修改代码格式化 换行处理 和 " 转义 bug
	3. 修改代码提示  function  方法中 定义的local 变量 无法提示 二级变量 的bug
	4. 添加数据统计接口 统计在线人数, 如果有反感这一行为的请联系我,后期考虑添加配置
	5. 优化debug  将 lua 和luajit 调试文件进行分离 coocs 和unity 如果使用luajit 的调试文件请使用luaDebugjit.lua 文件进行调试  调试文件地址为luadeubg/LuaDebug.lua or luadebug/Luadebugjit.lua
	 

1. 0.1.6 修改代码格式化bug   
1. 将源代码提交至github 


# 捐献      
支持LuaIde的开发 可以通过微信  
![IDE](https://coding.net/u/k0204/p/imgres/git/raw/master/money.png)



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)