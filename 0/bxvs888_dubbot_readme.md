 
## 项目介绍
   
随着微服务的流行，不管是企业级应用还是互联网应用都在向微服务架构转变，我们在享用微服务给我们带来价值的同时，也发现了传统的开发模式上微服务给我们带来的管理、部署的问题，比如新增或扩展provider后，consumer需要重新引用provider的API，或者后端服务做升级更新后，前端调用端一般也要跟着升级。本项目就是为了解决此类问题。





特点：
1. consumer不需要引入provider的api包便可实现RPC调用
2. 这里是列表文本模拟SpringMvc的参数接受方式，支持按属性名赋值参数
3. 这里是列表文本.本项目是在dubbo上的扩展，在符合dubbo规则的基础上通过配置的方式实现的，自定义filter兼容普通的RPC调用模式
4. 基于fastjson提供数据传输转换，所以理论上讲支持任意参数类型的传参调用
5. 完全继承dubbo特性


原理：

1. 重新编排dubbo的过滤器
2. 注入自定义过滤器

团队参与成员：林懂、张富、陈月峰

#### 使用说明

    服务提供者配置
    @Configuration
    public class RpcService extends DubboProviderConfig {
    }
    消费者配置
    @Configuration
    public class ReferenceDubbo extends DubboConsumerConfig {
    @Bean
    public GenericService dubbo()
    {
        return  new DubboService();
    }
    }
    消费者调用示例：
    @Autowired GenericService gen;
      public static void main(String[] args) {
                Map  obj=new HashMap<>();
        obj.put("name","HelloWorld");
        genericService.$invoke("com.provider.test.HelloWorld","1.0.0",
                "getTest",obj);
        }





#### 参与贡献

1. [Dubbox 基本特性之泛化调用](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79ded38e0ab63965d59e9e9eaa2125a79301217695f8c9e291dd84149ce20da197e4abad8dfee1c229745cdac4f3cac66a497) 
2. [dubbo 服务发现序列图](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79ded38e0ab63965d59e9e9eaa2125a79301295684d2d26d92e5da89b8bcd58a835c384605f579a475be6d344a545a511f1fa) 
3. [Dubbo Filter详解](http://u.720life.cn/g/76d6b4b287ed79b2a1b660f9d1dea15e076a10dcb5f395506a8423a1f0bdcc5d16ff4d2da943b8a418fedcc0da95edf9acf1b580e08d697a4e409ea610b4fa16) 




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)