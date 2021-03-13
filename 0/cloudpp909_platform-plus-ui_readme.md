## 介绍
- platform-plus-ui基于vue、element-ui构建开发，实现platform-plus后台管理前端功能。
- 封装富文本编辑器组件，并且支持使用v-model双向绑定富文本数据。简单到像使用input一样。
```
  
...
data () {
      return {
        msg: '  Vue + UEditor + v-model双向绑定 '
      }
```
- 后台地址：https://gitee.com/fuyang_lipengjun/platform-plus

## 实现功能
```
- 系统管理
    - 菜单管理
    - 组织机构
    - 系统参数
    - 字典管理
    - 文件上传
    - 系统日志
- 权限管理
    - 管理员列表
    - 角色管理
- 短信平台
    - 短信配置
- 任务调度
    - 定时任务
- 开发工具
    - 在线用户管理
    - 缓存信息
    - SQL监控
    - 接口文档
    - 代码生成器
```

# 技术栈
你需要在本地安装 nodejs。

- [nodejs](http://u.720life.cn/g/c47729c1c499a00d6e30af9fa18eaddd7b41ca24e187ea438549a271175cdbab) 
- [ES6](http://u.720life.cn/g/c7e32d8c72c7a7f0f5b5c90906d5840147fbfe912e3ee75f7d82e51ef33921c3) 
- [vue-cli](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046521cadb82ab6b46bcadb5dbc00f05b7e) 
- [vue](http://u.720life.cn/g/1eea7f654038e3466b5f7afd82540e02e09a9b8aabfa84663bde4b4d0da42395) 
- [vue-router](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304606fb5995514a592d0358d69de03eba11587624a2443f25b40b14ec7210b1c182) 
- [vuex](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304619f8490e119a6e120fe5c95321103894) 
- [axios](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304638015ac6a54b1cadf0934b8a0d5637d0) 
- [vue-cookie](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046cf5367c3e23b8e3d51a389b6a998c787fbcef539ad570f6d17ab0c71bab5dbd4) 
- [element-ui](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461c3385d2c6442447210a4c3d1baebf5188ca4979686fe7db89246207127fdadd) 
- [iconfont](http://u.720life.cn/g/2d8f53acd5e6641c0a10dfd2b41ddcfda6f0e50ce7730b021f4582854a637a81) 

# 目录结构
本项目已经通过vue-cli脚手架为你生产完整的开发框架（有根据业务需求做调整修改），下面是整个项目的目录结构。
```bash
├── build                      // 构建相关  
├── config                     // 构建配置相关
├── dist                       // 构建打包生成部署文件
│   ├── 1902151513             // 静态资源（19年02月15日15时13分）
│   ├── config                 // 配置
│   ├── index.html             // index.html入口
├── src                        // 源代码
│   ├── assets                 // 静态资源
│   ├── components             // 全局公用组件
│   ├── element-ui             // element-ui组件配置
│   ├── element-ui-theme       // element-ui组件主题配置
│   ├── icons                  // 所有 svg icons
│   ├── router                 // 路由
│   ├── store                  // 全局 store管理
│   ├── utils                  // 全局公用方法
│   ├── views                  // view
│   ├── App.vue                // 入口组件
│   ├── main.js                // 入口
├── static                      // 第三方不打包资源
│   ├── config                 // 全局变量配置
│   ├── img                    // favicon图标
│   ├── plugins                // 插件
├── .babelrc                   // babel-loader 配置
├── eslintrc.js                // eslint 配置项
├── .gitignore                 // git 忽略项
├── index.html                 // html模板
└── package.json               // package.json
```

# 安装
```bash
# 安装依赖
npm install

# 启动服务
npm run dev
```

安装过程中，可能会出现安装过慢、报错等情况，请尝试以下方式：
```bash
npm install -g cnpm --registry=https://registry.npm.taobao.org

cnpm install

# 启动服务
npm run dev
```
启动完成后会自动打开浏览器访问 [http://localhost:8000]()。

# 打包部署
```
修改
/static/config/index-[prod].js文件中  
window.SITE_CONFIG['baseUrl'] = 'http://47.93.215.16/platform-plus'// 后台接口请求地址
window.SITE_CONFIG['domain'] = '静态资源cdn地址';  

# 构建生产环境(默认)
npm run build

```
# 部署Nginx配置参考
```
  location / {
        # 指向我们打包后上传的前端文件
        root /usr/local/nginx/dist;
        index index.html;
    }
    location /platform-plus {
        # 转发请求到后端
        proxy_pass                         http://localhost:8888;
        proxy_set_header  Host             $host;
        proxy_set_header  X-Real-IP        $remote_addr;
        proxy_set_header  X-Forwarded-For  $proxy_add_x_forwarded_for;
    }
```

**项目演示**
- 演示地址：http://fly2you.cn/platform-plus/#/login
- 账号密码：
  - admin/admin
  - test/888888
  - test1/888888
  - test2/888888
  - test3/888888
  - test4/888888
  - test5/888888
  - test6/888888
  - test7/888888
  - test8/888888
  - test9/888888
  - test10/888888

**效果图：**
- 菜单管理
![https://platform-wxmall.oss-cn-beijing.aliyuncs.com/upload/platform-plus/platform-plus.jpg](https://platform-wxmall.oss-cn-beijing.aliyuncs.com/upload/platform-plus/platform-plus.jpg "菜单管理")
- 字典管理
![https://platform-wxmall.oss-cn-beijing.aliyuncs.com/upload/platform-plus/dict.png](https://platform-wxmall.oss-cn-beijing.aliyuncs.com/upload/platform-plus/dict.png "字典管理")
- 在线人数
![https://platform-wxmall.oss-cn-beijing.aliyuncs.com/upload/platform-plus/users.png](https://platform-wxmall.oss-cn-beijing.aliyuncs.com/upload/platform-plus/users.png "在线人数")
- 缓存数据
![https://platform-wxmall.oss-cn-beijing.aliyuncs.com/upload/platform-plus/doc.png](https://platform-wxmall.oss-cn-beijing.aliyuncs.com/upload/platform-plus/redis.png "缓存数据")
- 接口文档
![https://platform-wxmall.oss-cn-beijing.aliyuncs.com/upload/platform-plus/doc.png](https://platform-wxmall.oss-cn-beijing.aliyuncs.com/upload/platform-plus/doc.png "接口文档")

#### 提交反馈
1. 欢迎提交 issue，请写清楚遇到问题的原因，开发环境，复显步骤。
2. 不接受`功能请求`的 issue，功能请求可能会被直接关闭。  
3. 代码修改请遵循指定的 `ESLint` 规则，`PR` 之前请先执行 `npm run lint` 进行代码风格检测，大部分语法细节可以通过 `npm run fix` 修正。
4. 官方QQ群：
-    
-    
-    

#### 常用API
- [Vue](http://u.720life.cn/g/1eea7f654038e3466b5f7afd82540e020a870f4a4185f17a1941814df81fc9db) 
- [element-ui](http://u.720life.cn/g/99b90101e0edb43e4fb6c26272a617e68663cc65b086687fa23d692ae5a71460f46c41bd5e556a5c80e1411639f231fc61da3a12304b84df873a8ab63ca1c524) 
- [echarts](http://u.720life.cn/g/f989f483b7470966b008e44ccf371b7e4eede3e8f28b2bde8d388515915df9fe7b24b63d91dd897cf2e028448cfb039b) 
- [iconfont](http://u.720life.cn/g/e78198cbca568641bd2625675a127257b1162ff841e727fd60de3d703ac776265c1dba52c7c6016c9e481db3396322f3) 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)