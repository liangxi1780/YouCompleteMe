![NovalIDE](noval/tool/bmp_source/logo.png)

简介
----------------------------------

NovalIDE是一款开源，跨平台，而且免费的国产多功能，轻便的Python IDE，大小才12M

- 有出色的语法高亮功能,支持多种语言,python,c/c++,html,javascript,xml,css等
- 自动检测，并加载Python解释器，允许用户自由添加删除解释器，并选择相应的解释器运行脚本
- 支持函数智能提示和代码自动完成
- 支持新建NovalIDE工程和从现有代码创建工程，新建工程类型将包括应用程序，Django,Flask,wxPython,Py2exe,Win32,GTK，控制台程序等
- 自动智能分析解释器系统路径下模块文件，并生成智能提示使用的数据文件
- 类VS风格的可停靠窗口，多文档切换模式
- 各种复杂的编辑功能，支持高级编辑功能
- 可以调试以及模拟真实环境的终端方式运行python脚本
- 自动模拟Python解释器环境，并内嵌解释器，不用安装任何python环境，即可运行python程序
- 可以断点调试，单步调试python代码，并能监视，查看变量以及堆栈变化，以及添加，删除，管理断点等
- 可以自由终止，重启以及运行调试环境
- 支持运行多个解释器版本，并在不同版本之间进行切换
- 支持中英文多个语言版本
- 灵活的高扩展性，提供开放式接口支持程序员开发自定义插件
- 强大的包管理器，通过pip一键式安装卸载Python包
- 支持python2.6,2.7版本以及python3.x版本,2.6以前版本未实测

官方网址：[http://www.novalide.com](http://u.720life.cn/g/d2078a13222f7db8b31235f5bb34dfeaf971562c43029bd95811ca9c1f019755) 

相关文章:

- [对一款优秀国产Python IDE---NovalIDE的体验](http://u.720life.cn/g/a88615b97db01a1ba3d626afe31cb1731fbe70265b5ce846ebdcf65a78506efc6385824a36859e9f45dc6cede5c83f83) 
- [Linux如何安装NovalIDE](http://u.720life.cn/g/a88615b97db01a1ba3d626afe31cb1731fbe70265b5ce846ebdcf65a78506efc7f432a5e8bf44042266e93b40a891dc4) 

软件概貌: ![NovalIDE_Screen](noval/tool/bmp_source/images/banner_01.png)

编译
----------------------------------

### 源码依赖包

- Python2.7.11 [Windows下载地址](http://u.720life.cn/g/74e7b7c595201f48e3f4da7562c1a8264f53fd76f34576b971d1a711bbed1ad55e645ed6c8d8513983dc5ca16555dac3f1b23e59cd053dce75b0cc3f8ca40c2f) 
- wxPython(3.0.2) [Windows下载地址](http://u.720life.cn/g/7d644d22d4b2c2395524a3cba003a2d812054fc82bcc98f2ee919ca2cc1559b11cb3202c4caf41d49d1d4b4d714f17fff2d8591692d6d46e70d236c93241d46bf850db0d36265df3c218aab51f742274cc2811a82ef3b1e1632f3c25de7cea602e6d9ca4bcb8cdca035fbdc55fca0b81) 
- pywin32(only windows) [Windows下载地址](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304636cd03e0dc6b12d235ee74e49c7e790a4735cda71f759c6895ddfe76c30ce7ee35ca41e23cb6201b95d29264580db16002c7855a7da087f4b89aad5cc6c0cc01226cd7055fb4148f19b212fff5b94fae) 
- py2exe(only windows) [Windows下载地址](http://u.720life.cn/g/7d644d22d4b2c2395524a3cba003a2d812054fc82bcc98f2ee919ca2cc1559b1211548170127f0ca4b42c1582330637dd071a792c2283431ae1004f1fd5343dcd3bd6ddcff913ee8a4d5e98cef07fbfee6de8a44af194ed4af153d3a66b69ef7) 
- wmi(only windows)
- psutil
- watchdog
- chardet
- pyperclip
- requests

### Windows编译

- **源码运行**

```
下载Python2.7，以及wxPython3.0.2，pywin32，py2exe安装包，下载地址见上。
git clone https://gitee.com/wekay/NovalIDE.git
cd NovalIDE

pip install psutil
pip install watchdog
pip install chardet
pip install pyperclip
pip install wmi
pip install requests

运行Python NovalIDE.py
```

- **源码打包**

```
运行python buildide或者python setup.py py2exe
生成dist目录下运行NovalIDE.exe
```

### Linux编译

- **Ubuntu**

sudo apt-get install python-wxtools

- **Centos**

sudo yum install wxPython-devel

- **编译步骤**

```
git clone https://gitee.com/wekay/NovalIDE.git
cd Noval
运行python setup.py install，权限不够请用sudo
最后运行Python NovalIDE.py或者直接运行NovalIDE命令
```

安装
----------------------------------

### Windows安装

从官网：[http://www.novalide.com]http://www.novalide.com/下载[Windows版本]http://www.novalide.com/member/download_app?lang=zh_cn&os_name=win32

点击NovalIDE_Setup.exe并依次按安装向导安装，直到完成。

![NovalIDE_WINDOWS_INSTALL](noval/tool/bmp_source/images/windows_insall.png)

### Linux安装
从官网：[http://www.novalide.com]http://www.novalide.com/)下载[Linux版本]http://www.novalide.com/member/download_app?lang=zh_cn&os_name=linux)并解压 

- **Ubuntu**

sudo apt-get install python-wxtools

- **Centos**

sudo yum install wxPython-devel

- **安装步骤**

```
运行解压命令:tar -xvf NovalIDE.tar.gz解压安装包:NovalIDE.tar.gz
cd NovalIDE-x.x.x
运行sudo python setup.py install
最后输入命令NovalIDE来运行IDE。
```

功能截图
----------------------------------

- 智能提示
![CodeTip1](noval/tool/bmp_source/images/banner_02.png)
![CodeTip2](noval/tool/bmp_source/images/banner_03.png)
![CodeTip3](noval/tool/bmp_source/images/banner_04.png)

- 解释器配置
![InterpreterManage](noval/tool/bmp_source/images/banner_06.png)

- 包管理器
![PipManage](noval/tool/bmp_source/images/banner_07.png)

- 中英文切换
![Zh_En](noval/tool/bmp_source/images/zh_en.png)

- 单元测试
![UnitTest](noval/tool/bmp_source/images/banner_08.png)

- 新建工程
![NewProject](noval/tool/bmp_source/images/project.png)

- 自动加载解释器
![LoadInterpreter](noval/tool/bmp_source/images/interpreter.png)

特别感谢
----------------------------------

- 感谢欢夏女士帮助制作官网特效
- 感谢回想之后同学提供官网域名以及参与制作官网页面



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)