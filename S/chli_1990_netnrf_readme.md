# netnrf 响应式框架
> 用于快速开发的响应式框架

> 演示： 

### [更新日志](CHANGELOG.md)

### [文档说明](DOCUMENT.md)

### v2.x
- 前端采用 jQuery + Bootstrap + EasyUI + AceAdmin + fontAwesome
- 后端采用 .NET Core + EF + SQL（SQLServer、MySQL、PostgreSQL、SQLite）
    - 以`.NET Core`版本为主，同步更新`.NET Framework`版本
    - 数据库转换使用的工具：http://www.szmesoft.com/DB2DB
- 数据库脚本放置于 `wwwroot/scripts/`目录下
- Visual Studio 2017+ 运行项目，跨数据库、跨平台支持（在线demo部署在Linux服务器上）

### 项目结构
- Netnr.Core 类库（引用NuGet）
- Netnr.Data 数据访问、仓储
- Netnr.Domain 实体
- Netnr.Fast 常用方法
- Netnr.Func 应用
- Netnr.ResponseFramework Web站点

### 数据表
- 系统用户（SysUser）
- 系统角色、角色权限（SysRole）
- 系统菜单（SysMenu）
- 系统按钮（SysButton）
- 系统日志（SysLog）
- 表配置（SysTableConfig）

### 功能
- 登录：系统账号登录，第三方账号登录（QQ、微博等）
- 权限：角色权限，控制菜单及页面按钮
- 表格：动态配置标题、宽度、排序、对齐方式、格式化、冻结、点击排序等
- 表单：动态生成表单，自定义标题、排序、跨列、类型、必填等，支持多表单生成。
- 查询：动态生成查询面板，自定义哪些字段支持查询
- 日志：访问日志记录
- 工具：数据库表信息展示，一键导出表结构为Excel

### 使用说明
1. 创建表、写字段注释（方便生成表配置）
2. 生成表配置，可以用【工具箱】-【表管理】-【生成表配置】，也可以直接拷贝文件夹`wwwroot/scripts/table-config/`对应的`SQL`脚本运行
3. 修改表配置，表格，表单、查询，调整为需要展示的形式（标题、宽度、排序、输入类型、列格式化、必填、默认值等，根据业务拓展配置项）
4. 修改表配置，输入类型配置，需要配置下拉框、下拉树等，在`Common`控制器写方法，`url`源指向这个方法访问的地址
5. 修改表配置，列格式化配置，比如状态需要格式化为`启用`、`停用`，有常用公共的格式化方法，也可以配置自定义格式化方法`col_custom_字段小写`
6. 创建一个页面，菜单表添加此页面，配置操作按钮
7. 写表对应的查询、保存（新增/修改）、删除方法，参考【系统设置】里面的功能
8. 基于`z.js`封装的表格方法（API与EasyUI保持一致，看EasyUI文档即可），配置查询表的请求地址、表格类型、分页、复选等

----------
> 如果该项目对你有帮助，请你为项目Star，谢谢，这是对我精神上的支持，也是能一直坚持下去的动力。

----------

### 截图

#### 列表 

![列表](https://netnr.gitee.io/gs/2018/05/18/403ce7d002.png)

#### 新增、编辑、查看

![表单](https://netnr.gitee.io/gs/2018/05/18/8d25d345b2.png)

#### 列表配置

![列表配置](https://netnr.gitee.io/gs/2018/05/18/13da6572a3.png)

#### 表单配置

![表单配置](https://netnr.gitee.io/gs/2018/05/18/0c98ee578c.png)

#### 角色权限配置（树）

![角色权限配置](https://netnr.gitee.io/gs/2018/08/16/31a55cac78.png)

### 第三方文档API
- [EasyUI文档](http://u.720life.cn/g/8f8077fe2068979963f633bf75f78589dbc1f3f2a5efcd98b4175b913c7103a889efd289033e7a0de3dfd3cff68bd71f) 
- [jQuery文档](http://u.720life.cn/g/8f8077fe2068979963f633bf75f785898f73715e8686cc3a8f54d52f053acd19088da5c2f9e08032a3008ca81c1d984f) 

### 附
- [联系（打赏）](http://u.720life.cn/g/bb5a4b5d6aadda3c40ba82e1c4878dd285d5a0859f5eacddad94e3b4ed491462) 
- [加入QQ群](http://u.720life.cn/g/2161fefda279a0b09b13f7711dd877f77446b6d2ef583156f958b9e5cec01f00f115e4efded787a74333ef657e35eb5dfd7213654f0355e91d6699fcb65e0701f3ae045ad8797ffe3f4efb2e47833b70) 

### Source
-  
-  


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)