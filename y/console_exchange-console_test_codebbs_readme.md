[whoami代码论坛(码谈)](http://u.720life.cn/g/216847e15f58d764b0ade510b82c3d040d153ebaff9446ddb909cbfd8882c08f) 
===============
### 资料
[Spring 文档](http://u.720life.cn/g/c6d1b26d763f49c99d62f7dd7e1f263d7fd00d4defa003bbbe5135ab4fb1b2d9)     
[Spring Web](http://u.720life.cn/g/c6d1b26d763f49c99d62f7dd7e1f263d4a51a6e7ce5a0a478ef97900b3fd4287475a68214f57549bca2e08efe03e9b14)   
[菜鸟教程](http://u.720life.cn/g/be6a902dad679c47f4ac36e469c6aaed53e40fc2ff5130b5d5152bdee512ab8c5cbef26fe359a34c79d116c040bbf9d8d49c99aa616d1129c83ce9f41bfcf17a)     

[Spring Dev Tool](http://u.720life.cn/g/a8126de486174bbac1604ce886fda0d3dd4ff778e999be73548ad31b6c319bb05f27b61a921e9adb89b5f82bd64ed6fbd16972172cdadba0d8ce9c1b9d31aa9ad6bf6d6bae7efbf4f54edbc35df10830fd6fad630bf91a38f381aba06b6ec266)   
[Spring MVC官网](http://u.720life.cn/g/a8126de486174bbac1604ce886fda0d33163127cc15a75fd56a7a0b8d7ab0ad77f1ffa585d3f4c610dc5db44868dde39e337cf5c2367ed0810c944d151b11a1a8e1d0a61fd0f41e49ebb3bfa435fa44b0885e0f0bd7459215721593d1ccca2b8b2f980486e2a66f36bfe075147eeea2c22124b636401f9e47a8d1b97ebaa6c0d)   
 
#### BootStrap


#### 工具
[lombok的安装和使用](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79ded5435b7d64c5f19b94971b00183f7595a776c034c95767b1dad8f447c69fdf6c246c19ff3fb2fc75a9e435631864c7b68)     
[Markdown 插件](http://u.720life.cn/g/62ba2c0ec0b5419421d1cb88bcfe78aeb0931761a711b76e738928f0b0cbc685)   
[REST API测试 Chrome插件](http://u.720life.cn/g/4285663a6c4e633a5e7f90182679bfc1de4fcc632eff4999d4ba669f185b37ed6a97e8eea673f6ec56c35162a4d319304ca855a69e287f9637e879d4c24be348) 

码谈介绍(完善中...)
----------------------
#### 界面设计模块
1. 使用bootstrap设计简单的响应式页面
    + 下载bootstrap官方资源包
    + 引入项目所需资源
    + 根据官方文档使用相应的组件
    + [BootStrap](http://u.720life.cn/g/76ce37f2b9c55c77168e215bbd34e832dfdf333e2484d9d21b7e50af634c40afef4b2663aa1eb219c6f3d641d924f8a2)      
    + [栅格系统](http://u.720life.cn/g/76ce37f2b9c55c77168e215bbd34e83224e19e981aa452d070825dbb2fac2ee3) 

#### 登录功能模块
[github官网](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d45c0ae7090bb1b2bd83912ab32555db)      
[github OAuth](http://u.720life.cn/g/a69e8f5dba5b4106ccc3875c547b1484e674244761dae780d00991994723698679cdc7ea90a5ea27998aa3bd7a303d90bb6543f02dfba646be37698d433def48f6f9e48bb4b96d5f5ac4c1b45c3e43d7) 
1. 用户点击登录按钮     
    使用github的登录授权，发送请求，请求调用authorize接口，需要提供的参数
    + client_id：github自动生成
    + redirect_uri：回调接口地址
    + state=1
    + scope=user
1. github自动跳转到设置的callback接口中，并携带参数code
1. 然后调用github提供的access_token接口，需要提供参数，将数据传的参数封装成AccessTokenDTO
    + client_id：github生成
    + client_secret：github生成
    + code: github回调返回的参数
    + redirect_uri：回调接口地址
    + state=1
1. 使用OkHttp所提供的类将请求设为post请求
    + https://github.com/login/oauth/access_token
    ``` java
   Request request = new Request.Builder()
                   .url("https://github.com/login/oauth/access_token")
                   .post(body)
                   .build(); 
   ```
1. 再次将返回的access_token使用get方式请求github提供的user接口
    + https://api.github.com/user?access_token=xxx
    ``` java
   Request request = new Request.Builder()
                   .url("https://api.github.com/user?access_token="+accessToken)
                   .build(); 
   ```
   注：该方法即将弃用，后续更新使用方法
1. 最后返回github用户参数，存入数据库，更新登录状态。

### 论坛发布、修改、分页展示模块
1. 前提条件：已登录用户。
1. 将问题信息封装成QuestionDTO，并添加Lombok支持，减少代码getter/setter等方法的编写。
    ``` java
   @Data
   public class QuestionDTO {
       private Long id;
       private String title;
       private String description;
       ......
   }
    ```
1. 发布问题之前的校验
    ``` java
    //校验输入是否为空
    if (title == null || title.equals("")) {
        model.addAttribute("error","标题不能为空");
        return "publish";
    } 
   //其他校验
   ......
   ```
1. 使用thymeleaf+Bootstrap+Jquery解析数据解析美化发布问题页面
    + [Thymeleaf](http://u.720life.cn/g/38905b16d69edbd3d412c817647c3438f5e980419c3906d6ac3405b43ce94202119dc26dc96ee8f486928d08ed70667431fc914d8569196de76da5786e30e8f0bbd1e501de8897e8e44cfa3d453dea8273741cf7c47c598b7035a2285167876a)     
    + [JQuery](http://u.720life.cn/g/be6a902dad679c47f4ac36e469c6aaed2f6a64a1d56c21d8ea28fa6777cb1f59b68ad793f3fd2180749c21a1e73883569d2cc890f4b87db3d82c2b1d2cec4b23) 
1. 实现我的问题列表以及首页分页展示示例
    + 使用mybatis-generator自动生成代码的插件实现分页等多种功能
    ``` java
   QuestionExample example = new QuestionExample();
           example.createCriteria()
                   .andCreatorEqualTo(userId);
           example.setOrderByClause("gmt_create desc");
           List  questions = questionMapper.selectByExampleWithRowbounds(example, new RowBounds(offset, size)); 
   ```
    + [插件github地址](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304602d75ec6f7ef29bab0759c73f5fdf49997b16c203063ed2ad9d38fb1be612af0)   
    + [使用教程](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79ded0cd3d9dd38e13afe4cb766736c1ec238e5b871be64470a57333fc174c0083f5d0fac8e54f93ef19bef508b26449c688d) 

### 多级回复、浏览数及评论点赞功能
1. 数据表设计采用单表设计
    + 通过type属性指定评论为问题评论还是评论回复
    + 通过parent_id在单表中指定级联关系
1. 问题显示页面
    + 首次进入问题页面应保证效率,仅展示一级评论,即问题的回复
    + 每条评论显示有点赞数及评论数,用户可点击评论查看二级评论,并显示出二级评论窗口
1. 每访问一次问题详情页浏览数+1
    ``` java
   /**
    * 根据id查询到问题，对问题的浏览数+1
    * @param id
    */
    public void incview(Long id) {
        Question question = new Question();
        question.setId(id);
        question.setViewCount(1);
        questionExtMapper.incView(question);
    } 
   ```
1. 将点赞数量保存至Redis数据库中
    ``` java
    //被点赞数+1
    @Override
    public void incrementLikedCount(String likedUserId) {
        redisTemplate.opsForHash().increment(RedisKeyUtil.MAP_KEY_USER_LIKED_COUNT,likedUserId,1);
    } 
   ```

### Tag标签库完善
1. 将所有标签封装成TagCache
2. 不允许提交问题时输入非法标签
    ``` java
   //校验标签的合法性
    String invalid = TagCache.filterInvalid(tag);
    if (StringUtils.isNotBlank(invalid)){
        model.addAttribute("error","输入非法标签"+invalid);
        return "publish";
    }
    ```
3. 焦点移动到标签时，弹出选择标签，用户选择符合自己的标签进行添加
4. 标签与标签之间用逗号分隔

### 通知回复功能模块
1. createNotify(创建通知)
    + 每当有一次评论请求成功时,同时创建一条通知,保存parent_id问题的id,设置状态为未读,在通知页面显示评论内容及评论人
    + 使用Spring事务进行管理,保证评论与通知的原子性
    ``` java
   @Transactional
    public void  insert(Comment comment, User commentator){
   //创建通知
   createNotify(......);
   }
   private void createNotify(Comment comment, ......) { 
   ......
   }
   ```
1. 评论数增加
1. 通知条数及内容展示
    + 使用拦截器查询当前用户在数据库中通知的未读条数,放入Session中
    + 用户请求通知列表，展示所有被评论的信息
    + 用户点击某条通知时，根据parent_id,
    转发请求到question页面并将该通知状态置为已读

### 集成Markdown富文本编辑器
1. 开源在线Markdown编辑器
    + [Markdown](http://u.720life.cn/g/db08e82e8a423dbbc7bd3115b44ffe3193110e9cbd370ca283774323c60717d3730ac23c7f22136005db8474674be57e) 
1. 引入使用编辑器的基本样式及必须资源
1. 示例：
``` html
 
    $(function () {
        var editor = editormd("question-editor", {
            width: "100%",
            height: 350,
            path: "/js/lib/",
            delay: 0,
            syncScrolling : "single",
            placeholder: "请输入问题描述",
            imageUpload: true,
            imageFormats: ["jpg", "jpeg", "gif", "png", "bmp", "webp"],
            imageUploadURL: "/file/upload",
            saveHTMLToTextarea : true
        });
    });
 
```
### 7天最热话题&点赞关系存储
1. 引入定时任务
1. 定时查询和存储Redis数据
### ......


------------------------------------
##### 开发日志  
1. 2020/02/15 完成部署    
1. 2020/02/18 添加动态导航栏    
1. 2020/02/20 完善登录用户名为null的情况   
1. 2020/02/24 添加使用Redis实现点赞功能   
1. ......


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)