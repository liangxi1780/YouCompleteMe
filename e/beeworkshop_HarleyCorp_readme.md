# open api demo (java ver.)
java version "1.7.0_75"

## Getting Started

1..将工程clone到本地：```git clone https://github.com/ddtalk/HarleyCorp.git```，导入到IDE中，比如eclipse点击```File->import```导入到eclipse中

2.打开工程的Env.java文件，填入企业的CORP_ID和SECRET（CORP_ID和SECRET可以在企业OA后台找到）
```
    public static final String CORP_ID = "your CORP_ID";
    
    public static final String CORP_SECRET = "your CORP_SECRET";
```

 

3.部署工程

4.OA后台创建微应用，并把工程的首页地址填到微应用首页中。
[如何创建微应用？]http://ddtalk.github.io/dingTalkDoc/#step-2-创建微应用
 


###本DEMO具体实现

1.jsapi权限验证配置流程

请查看[文档]http://ddtalk.github.io/dingTalkDoc/#页面引入js文件
- 前端文件:WebContent/index.jsp，WebContent/javascripts/demo.js
- 后端文件:[链接](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ac21b50dc96432c7c3c3c23cad1e24768d5338403e656f18ad1cbcbf2434a053dc4ad2cdf4d71e01e191d7f205a3a551801a0b75f431248b1bbd56f0ff48a895b011605ccb8ed73d360a5b6512f85f6af64ef32a62260734b4aadebce8f36b1b8127afe0ec2243a6bdab31ac2e919242) 

2.免登流程

请查看[文档]http://ddtalk.github.io/dingTalkDoc/#手机客户端微应用中调用免登
- 前端文件:WebContent/javascripts/demo.js和
- 后端文件:[链接](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ac21b50dc96432c7c3c3c23cad1e24768d5338403e656f18ad1cbcbf2434a053dc4ad2cdf4d71e01e191d7f205a3a551801a0b75f431248b1bbd56f0ff48a895d794bb4516d69858b81606d6c38bbafec0a90fbb1f51d5f9807503290623a7618fbd9108dae36e34fea07cb135ae7ee6) 


3.部门的操作
请查看[文档]http://ddtalk.github.io/dingTalkDoc/#管理通讯录
- 后端文件：[链接](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ac21b50dc96432c7c3c3c23cad1e24768d5338403e656f18ad1cbcbf2434a053dc4ad2cdf4d71e01e191d7f205a3a551801a0b75f431248b1bbd56f0ff48a89509cf6588852f2d01b3b6347d971907c9b929242347d4040383e6a6702f5ad93c) 

4.员工的操作
请查看[文档]http://ddtalk.github.io/dingTalkDoc/#管理通讯录
- 后端文件：[链接](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ac21b50dc96432c7c3c3c23cad1e24768d5338403e656f18ad1cbcbf2434a053dc4ad2cdf4d71e01e191d7f205a3a551801a0b75f431248b1bbd56f0ff48a895cea6f92f4d4ae9e9ced83f661b0e4bd104bc237ee9c260c8b0239f0f7d796bc0) 

5.通讯录事件（比如用户的离职，部门的删除）回调
请查看[文档]http://ddtalk.github.io/dingTalkDoc/#通讯录及群会话变更事件回调接口
- 后端文件：[链接](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ac21b50dc96432c7c3c3c23cad1e24768d5338403e656f18ad1cbcbf2434a053dc4ad2cdf4d71e01e191d7f205a3a551801a0b75f431248b1bbd56f0ff48a895d794bb4516d69858b81606d6c38bbafec1573e8bea145163b840d23d2efbeca7b5de2dfa3a469fcd4817d1051be0cc91) 

6.发送消息
请查看[文档](http://u.720life.cn/g/0e3fbaf759f115341edbcd9f12d052c7ff38043c551533e12613c6a40c32466b332e4ea1401781c28a430afb088d7b6167a7e17fd5135b6ac812bbe0a079f386) 
- 后端文件：[链接](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ac21b50dc96432c7c3c3c23cad1e24768d5338403e656f18ad1cbcbf2434a053dc4ad2cdf4d71e01e191d7f205a3a551801a0b75f431248b1bbd56f0ff48a895783e620b6d8b3b058d5224d6b1d8042f9d6a1b8da19cf56c2cffba45d532e0d9) 




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)