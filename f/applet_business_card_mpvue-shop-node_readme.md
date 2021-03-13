# 本项目使用的是腾讯提供的小程序node解决方案 #

## [ Wafer2 Node.js Demo](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f6a831212fae483416fddc4798a6cdc8e5a45aea976460e8bf3a2ce85af6942f240c52ba69acb7a4c1153369c721f4f5)  ##

## 下载源码
    git clone git@github.com:heyushuo/mpvue-shop-node.git


## 开始使用

#### 安装依赖
    npm install

#### 启动项目
    npm run dev
# 需要注意的地方 #
### 1.项目开始前创建数据库nodemysql并导入项目根目录下的nodemysql.sql ##
### 2.项目根目录有一个config.js文件在这里可以配置数据相关,还有本地开发环境配置 ##
  	mysql: {
		host: 'localhost',
		port: 3306,
		user: 'root',   
		db: 'nodemysql',  //数据库名字
		pass: '123456',   //数据库密码
		char: 'utf8mb4'
    };


## 3.腾讯官方也提供的详细的搭建本地开发配置说明 ##

[点击进入](http://u.720life.cn/g/573ff6a91b3af551e410311df33cdee52e098986dc45287cab71b0e0b5408d4f9ef59e5d2175dd6aeaad40b87ecf3e4c020b8c3d4c9d5a9f8cf7cb0b51cace4cc99582e87706eec8f75ad0950ec6691ef80217c23b9fa37d963e2647b030434874cf3f77d7281d19fb746a15e435d16141bc8e2d6a1c7202fc08eaeecc2790edc0f7573e45dc00575fdc8f4bc612f7ca) 

# 项目目录结构 #
本项目所有的业务逻辑都在**controllers**文件夹中  
本项目所有的接口都写在**router文件夹下的index.js**里边
    
    //首页数据
    //1.首页
    router.get('/index/index', controllers.home.index)
    //2.首页品牌制造商直供的详情内的列表数据
    router.get('/brand/listaction', controllers.brand.index.listAction)
    //3.首页品牌制造商直供的详情数据
    router.get('/brand/detailaction', controllers.brand.index.detailAction)
    
    
    /**
     *  分类
     */
    //1.分类和子类
    router.get('/category/indexaction', controllers.category.index.indexAction)
    //2.通过分类的id来查询子类接口
    router.get('/category/currentaction', controllers.category.index.currentAction)
    //3.获取导航数据
    router.get('/category/categoryNav', controllers.category.index.categoryNav)
    
    
    /**
     *  商品相关接口
     */
    //1.商品详情接口
    router.get('/goods/detailaction', controllers.goods.index.detailAction)
    //2.获取商品列表
    router.get('/goods/goodsList', controllers.goods.index.goodsList)
    
    
    /**
     *  专题接口
     */
    //1.列表
    router.get('/topic/listaction', controllers.topic.index.listAction)
    //2.详情加下方四个专题推荐
    router.get('/topic/detailaction', controllers.topic.index.detailAction)
    
    
    /**
     * 搜索相关接口
     */
    //1.关键词和搜索历史接口
    router.get('/search/indexaction', controllers.search.index.indexAction)
    //2.搜索提示接口
    router.get('/search/helperaction', controllers.search.index.helperAction)
    //3.搜索的关键词添加到数据库
    router.post('/search/addhistoryaction', controllers.search.index.addHistoryAction)
    //4.清空搜索历史
    router.post('/search/clearhistoryAction', controllers.search.index.clearhistoryAction)
    
    
    /**
     *  收藏相关接口
     */
    //1.添加收藏
    router.post('/collect/addcollect', controllers.collect.index.addCollect)
    //2.获取收藏列表
    router.get('/collect/listAction', controllers.collect.index.listAction)
    //2.获取收藏列表
    router.get('/collect/deleteCollect', controllers.collect.index.deleteCollect)
    
    /**
     *  购物车相关接口
     */
    //1.添加购物车
    router.post('/cart/addCart', controllers.cart.index.addCart)
    //2.购物车列表
    router.get('/cart/cartList', controllers.cart.index.cartList)
    //3.删除商品
    router.get('/cart/deleteAction', controllers.cart.index.deleteAction)
    
    
    /**
     *  订单相关
     */
    router.post('/order/submitAction', controllers.order.index.submitAction)
    
    router.get('/order/detailAction', controllers.order.index.detailAction)
    /**
     *  收货地址相关接口
     */
    //1.保存和跟新收货地址
    router.post('/address/saveAction', controllers.address.index.saveAction)
    //2.获取收货地址列表
    router.get('/address/getListAction', controllers.address.index.getListAction)
    //3.获取收货地址详情
    router.get('/address/detailAction', controllers.address.index.detailAction)
    //4.删除收货地址
    router.get('/address/deleteAction', controllers.address.index.deleteAction)
    
    
    /**
     *  意见反馈
     */
    router.post('/feedback/submitAction', controllers.feedback.index.submitAction)

# 下方为微信小程序效果展示 #
### 1.首页展示和专题页效果
![](https://user-gold-cdn.xitu.io/2018/8/27/165793588dd8808f?w=323&h=571&f=gif&s=3649872)
![](https://user-gold-cdn.xitu.io/2018/8/25/165717735a9e3c60?w=327&h=573&f=gif&s=3983502)
### 2、分类页面，分类子页面以及搜索功能、搜索列表、历史记录、模糊搜索提示
![](https://user-gold-cdn.xitu.io/2018/8/25/1657185090f5d3cd?w=327&h=573&f=gif&s=884918)
![](https://user-gold-cdn.xitu.io/2018/8/25/1657188bf2746d85?w=327&h=573&f=gif&s=585295)
### 3、购物车功能添加购物车,单选多选,删除和商品收藏功能
![](https://user-gold-cdn.xitu.io/2018/8/25/165719656d9bdb5b?w=327&h=573&f=gif&s=1979300)
![](https://user-gold-cdn.xitu.io/2018/8/25/165719e76bd00f05?w=327&h=573&f=gif&s=1770550)
### 4、地址管理
![](https://user-gold-cdn.xitu.io/2018/8/25/165719e2d9b28ee1?w=327&h=573&f=gif&s=611343)

# 小程序端传送门 [点击进入小程序地址](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304635f3f4b6199beb4576667014dcdcd04d701f3bba727c9d7a477b1046d2e55e35) 
# 最后 #
- 喜欢的记得点个start,鼓励一下谢谢哈!!
- 微信号 hys838723
- qq群号 647099996


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)