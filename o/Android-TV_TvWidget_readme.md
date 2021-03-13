# TvWidget

TV常用效果控件，包括焦点、边框处理等。qq群:537960195


# 截图

 

 

 

# 使用
```java
//基本用法
BorderView border=new BorderView(this);
border.setBackgroundResource(R.drawable.item_highlight);
RelativeLayout main= (RelativeLayout) findViewById(R.id.main);
border.attachTo(main);

//自定义布局        
BorderView borderView = new BorderView (this,R.layout.custom_item);

//设置放大倍数1.2
borderView.getEffect().setScale(1.2);
```
```xml
//圆角布局 app:radius 为圆角大小
 
       
       
  
```       

# 项目捐赠

![喜欢就支持一下](https://github.com/evilbinary/myblog/raw/master/data/s.png)
# Developed By


* evilbinary   
* 个人博客 [http://evilbinary.org](http://u.720life.cn/g/61eb9fbc3e55f92e14ae6a88b879eee3b09194aa1d943a61a20bf1598091cd9b) 

#项目主页
* [https://github.com/evilbinary/TvWidget](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046bef6eaf1b3b9c1057ca32497a0f46ef2d3b1d1049350e0ea60ef30c77695dbf2) 

# License

Copyright 2016 evilbinary

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