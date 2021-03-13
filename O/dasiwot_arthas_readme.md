## Arthas

![arthas](site/src/site/sphinx/arthas.png)

[![Build Status](https://travis-ci.org/alibaba/arthas.svg?branch=master)](https://travis-ci.org/alibaba/arthas)
[![codecov](https://codecov.io/gh/alibaba/arthas/branch/master/graph/badge.svg)](https://codecov.io/gh/alibaba/arthas)
![maven](https://img.shields.io/maven-central/v/com.taobao.arthas/arthas-packaging.svg)
![license](https://img.shields.io/github/license/alibaba/arthas.svg)
[![Average time to resolve an issue](http://isitmaintained.com/badge/resolution/alibaba/arthas.svg)](http://isitmaintained.com/project/alibaba/arthas "Average time to resolve an issue")
[![Percentage of issues still open](http://isitmaintained.com/badge/open/alibaba/arthas.svg)](http://isitmaintained.com/project/alibaba/arthas "Percentage of issues still open")

`Arthas` is a Java Diagnostic tool open sourced by Alibaba.

Arthas allows developers to troubleshoot production issues for Java applications without modifying code or restarting servers.

[中文说明/Chinese Documentation](README_CN.md)

### Background

Often times, the production system network is inaccessible from the local development environment. If issues are encountered in production systems, it is impossible to use IDEs to debug the application remotely. More importantly, debugging in production environment is unacceptable, as it will suspend all the threads, resulting in the suspension of business services. 

Developers could always try to reproduce the same issue on the test/staging environment. However, this is tricky as some issues cannot be be reproduced easily on a different environment, or even disappear once restarted. 

And if you're thinking of adding some logs to your code to help troubleshoot the issue, you will have to go through the following lifecycle; test, staging, and then to production. Time is money! This approach is inefficient! Besides, the issue may not be reproducible once the JVM is restarted, as described above.

Arthas was built to solve these issues. A developer can troubleshoot your production issues on-the-fly. No JVM restart, no additional code changes. Arthas works as an observer, which will never suspend your existing threads.

### Key features

* Check whether a class is loaded, or where the class is being loaded. (Useful for troubleshooting jar file conflicts)
* Decompile a class to ensure the code is running as expected.
* View classloader statistics, e.g. the number of classloaders, the number of classes loaded per classloader, the classloader hierarchy, possible classloader leaks, etc.
* View the method invocation details, e.g. method parameter, return object, thrown exception, and etc.
* Check the stack trace of specified method invocation. This is useful when a developers wants to know the caller of the said method.
* Trace the method invocation to find slow sub-invocations.
* Monitor method invocation statistics, e.g. qps, rt, success rate and etc.
* Monitor system metrics, thread states and cpu usage, gc statistics, and etc.
* Supports command line interactive mode, with auto-complete feature enabled.
* Supports telnet and websocket, which enables both local and remote diagnostics with command line and browsers.
* Supports JDK 6+.
* Supports Linux/Mac/Windows.


### Online Tutorials(Recommend)

* [Arthas Basics](http://u.720life.cn/g/eff6dbe5c0981d8621a9099c954de83f51965da81f2d4b4e160d341e0dba3b210b22f90f990a93f769160a1696e79faa9fff5ee32259fcac07a7e961bc6d745680783c0eb4e007669ed6851481106258) 
* [Arthas Advanced](http://u.720life.cn/g/eff6dbe5c0981d8621a9099c954de83f51965da81f2d4b4e160d341e0dba3b210b22f90f990a93f769160a1696e79faa9fff5ee32259fcac07a7e961bc6d745663ba92ccaff5acc978c19f95541604b1) 

### Quick start

#### Use `arthas-boot`(Recommend)

Download`arthas-boot.jar`，Start with `java` command:

```bash
wget https://alibaba.github.io/arthas/arthas-boot.jar
java -jar arthas-boot.jar
```

Print usage:

```bash
java -jar arthas-boot.jar -h
```

#### Use `as.sh`

You can install Arthas with one single line command on Linux, Unix, and Mac. Copy the following command and paste it into the command line, then press *Enter* to run:

```bash
curl -L https://alibaba.github.io/arthas/install.sh | sh
```

The command above will download the bootstrap script `as.sh` to the current directory. You can move it the any other place you want, or put its location in `$PATH`.

You can enter its interactive interface by executing `as.sh`, or execute `as.sh -h` for more help information.


### Documentation

* [Online Tutorials(Recommend)](http://u.720life.cn/g/eff6dbe5c0981d8621a9099c954de83f51965da81f2d4b4e160d341e0dba3b210b22f90f990a93f769160a1696e79faa727cd32e143bbdccd189363b857f922a) 
* [User manual](http://u.720life.cn/g/eff6dbe5c0981d8621a9099c954de83f51965da81f2d4b4e160d341e0dba3b211c38a2814f5c3138e515b40f8378f19b) 
* [Installation](http://u.720life.cn/g/eff6dbe5c0981d8621a9099c954de83f51965da81f2d4b4e160d341e0dba3b2137264cba6871b18cfca688a1435db9bd78583feff9a95493c26c231f4e9dcb44) 
* [Quick start](http://u.720life.cn/g/eff6dbe5c0981d8621a9099c954de83f51965da81f2d4b4e160d341e0dba3b21930474f14575736c66df7e672b25689a4040c9078f4a2df3c8a9570de8fbc777) 
* [Advanced usage](http://u.720life.cn/g/eff6dbe5c0981d8621a9099c954de83f51965da81f2d4b4e160d341e0dba3b21e1ffac09c8727c1b60cae3f77eb94bf46725cc30e21c92c477963ae8a8b4b83b) 
* [Commands](http://u.720life.cn/g/eff6dbe5c0981d8621a9099c954de83f51965da81f2d4b4e160d341e0dba3b21997ff2f8ad6e4815fb168f4d816284623ced8fe7310b8addacbc340b63151d5d) 
* [Docker](http://u.720life.cn/g/eff6dbe5c0981d8621a9099c954de83f51965da81f2d4b4e160d341e0dba3b21947f0b52f602550b124f1dd9e20cf0ac) 
* [User cases](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ca7ffc1d62e958cae2f5103f867514ff6e2226ae3709d251a0fe7a447c5bb0d51e83f06d25493b596702683c2e7468a2) 
* [Questions and answers](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ca7ffc1d62e958cae2f5103f867514ff55831642199e49e311a65640e77ee27eb2c7f8993a58c45dd50576f85c2264c7b79e7f3265c7216861106e1fd671eb3330051e0b1e244d72cd4b4de0b8e97f0f) 
* [How to contribute](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ca7ffc1d62e958cae2f5103f867514ffac6b0e4d3831d1e11c94071d5d7efbd10f67795c736e60a4b02d5d47cf16c09c) 
* [Release Notes](http://u.720life.cn/g/eff6dbe5c0981d8621a9099c954de83f51965da81f2d4b4e160d341e0dba3b21d67a80f9d039b72d5d0fad48517d95f1221d045bb103b0f74c3e655275d1b11b) 


### Feature Showcase

#### Dashboard

* https://alibaba.github.io/arthas/en/dashboard

![dashboard](site/src/site/sphinx/_static/dashboard.png)

#### Thread

See what is eating your cpu (ranked by top cpu usage) and what is going on there in one glance:

```bash
$ thread -n 3
"as-command-execute-daemon" Id=29 cpuUsage=75% RUNNABLE
    at sun.management.ThreadImpl.dumpThreads0(Native Method)
    at sun.management.ThreadImpl.getThreadInfo(ThreadImpl.java:440)
    at com.taobao.arthas.core.command.monitor200.ThreadCommand$1.action(ThreadCommand.java:58)
    at com.taobao.arthas.core.command.handler.AbstractCommandHandler.execute(AbstractCommandHandler.java:238)
    at com.taobao.arthas.core.command.handler.DefaultCommandHandler.handleCommand(DefaultCommandHandler.java:67)
    at com.taobao.arthas.core.server.ArthasServer$4.run(ArthasServer.java:276)
    at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1145)
    at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:615)
    at java.lang.Thread.run(Thread.java:745)

    Number of locked synchronizers = 1
    - java.util.concurrent.ThreadPoolExecutor$Worker@6cd0b6f8

"as-session-expire-daemon" Id=25 cpuUsage=24% TIMED_WAITING
    at java.lang.Thread.sleep(Native Method)
    at com.taobao.arthas.core.server.DefaultSessionManager$2.run(DefaultSessionManager.java:85)

"Reference Handler" Id=2 cpuUsage=0% WAITING on java.lang.ref.Reference$Lock@69ba0f27
    at java.lang.Object.wait(Native Method)
    -  waiting on java.lang.ref.Reference$Lock@69ba0f27
    at java.lang.Object.wait(Object.java:503)
    at java.lang.ref.Reference$ReferenceHandler.run(Reference.java:133)
```

#### jad

Decompile your class with one shot:

```java
$ jad javax.servlet.Servlet

ClassLoader:
+-java.net.URLClassLoader@6108b2d7
  +-sun.misc.Launcher$AppClassLoader@18b4aac2
    +-sun.misc.Launcher$ExtClassLoader@1ddf84b8

Location:
/Users/xxx/work/test/lib/servlet-api.jar

/*
 * Decompiled with CFR 0_122.
 */
package javax.servlet;

import java.io.IOException;
import javax.servlet.ServletConfig;
import javax.servlet.ServletException;
import javax.servlet.ServletRequest;
import javax.servlet.ServletResponse;

public interface Servlet {
    public void init(ServletConfig var1) throws ServletException;

    public ServletConfig getServletConfig();

    public void service(ServletRequest var1, ServletResponse var2) throws ServletException, IOException;

    public String getServletInfo();

    public void destroy();
}
```

#### mc

Memory compiler, compiles `.java` files into `.class` files in memory.

```bash
mc /tmp/Test.java
```

#### redefine

Load the external `*.class` files to re-define the loaded classes in JVM.

```bash
redefine /tmp/Test.class
redefine -c 327a647b /tmp/Test.class /tmp/Test\$Inner.class
```

#### sc

Search any loaded class with detailed information.

```bash
$ sc -d org.springframework.web.context.support.XmlWebApplicationContext
 class-info        org.springframework.web.context.support.XmlWebApplicationContext
 code-source       /Users/xxx/work/test/WEB-INF/lib/spring-web-3.2.11.RELEASE.jar
 name              org.springframework.web.context.support.XmlWebApplicationContext
 isInterface       false
 isAnnotation      false
 isEnum            false
 isAnonymousClass  false
 isArray           false
 isLocalClass      false
 isMemberClass     false
 isPrimitive       false
 isSynthetic       false
 simple-name       XmlWebApplicationContext
 modifier          public
 annotation
 interfaces
 super-class       +-org.springframework.web.context.support.AbstractRefreshableWebApplicationContext
                     +-org.springframework.context.support.AbstractRefreshableConfigApplicationContext
                       +-org.springframework.context.support.AbstractRefreshableApplicationContext
                         +-org.springframework.context.support.AbstractApplicationContext
                           +-org.springframework.core.io.DefaultResourceLoader
                             +-java.lang.Object
 class-loader      +-org.apache.catalina.loader.ParallelWebappClassLoader
                     +-java.net.URLClassLoader@6108b2d7
                       +-sun.misc.Launcher$AppClassLoader@18b4aac2
                         +-sun.misc.Launcher$ExtClassLoader@1ddf84b8
 classLoaderHash   25131501

```

#### stack

View the call stack of `test.arthas.TestStack#doGet`:

```bash
$ stack test.arthas.TestStack doGet
Press Ctrl+C to abort.
Affect(class-cnt:1 , method-cnt:1) cost in 286 ms.
ts=2018-09-18 10:11:45;thread_name=http-bio-8080-exec-10;id=d9;is_daemon=true;priority=5;TCCL=org.apache.catalina.loader.ParallelWebappClassLoader@25131501
    @test.arthas.TestStack.doGet()
        at javax.servlet.http.HttpServlet.service(HttpServlet.java:624)
        at javax.servlet.http.HttpServlet.service(HttpServlet.java:731)
        at org.apache.catalina.core.ApplicationFilterChain.internalDoFilter(ApplicationFilterChain.java:303)
        at org.apache.catalina.core.ApplicationFilterChain.doFilter(ApplicationFilterChain.java:208)
        at org.apache.tomcat.websocket.server.WsFilter.doFilter(WsFilter.java:52)
        at org.apache.catalina.core.ApplicationFilterChain.internalDoFilter(ApplicationFilterChain.java:241)
        at org.apache.catalina.core.ApplicationFilterChain.doFilter(ApplicationFilterChain.java:208)
        at org.apache.catalina.core.ApplicationFilterChain.internalDoFilter(ApplicationFilterChain.java:241)
        at org.apache.catalina.core.ApplicationFilterChain.doFilter(ApplicationFilterChain.java:208)
        at org.apache.catalina.core.StandardWrapperValve.invoke(StandardWrapperValve.java:220)
        at org.apache.catalina.core.StandardContextValve.invoke(StandardContextValve.java:110)
        ...
        at org.apache.catalina.core.StandardHostValve.invoke(StandardHostValve.java:169)
        at org.apache.catalina.valves.ErrorReportValve.invoke(ErrorReportValve.java:103)
        at org.apache.catalina.core.StandardEngineValve.invoke(StandardEngineValve.java:116)
        at org.apache.catalina.connector.CoyoteAdapter.service(CoyoteAdapter.java:451)
        at org.apache.coyote.http11.AbstractHttp11Processor.process(AbstractHttp11Processor.java:1121)
        at org.apache.coyote.AbstractProtocol$AbstractConnectionHandler.process(AbstractProtocol.java:637)
        at org.apache.tomcat.util.net.JIoEndpoint$SocketProcessor.run(JIoEndpoint.java:316)
        at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1142)
        at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:617)
        at org.apache.tomcat.util.threads.TaskThread$WrappingRunnable.run(TaskThread.java:61)
        at java.lang.Thread.run(Thread.java:745)
```

#### Trace

See what is slowing down your method invocation with trace command:

![trace](site/src/site/sphinx/_static/trace.png)

#### Watch

Watch the first parameter and thrown exception of `test.arthas.TestWatch#doGet` only if it throws exception.

```bash
$ watch test.arthas.TestWatch doGet {params[0], throwExp} -e
Press Ctrl+C to abort.
Affect(class-cnt:1 , method-cnt:1) cost in 65 ms.
ts=2018-09-18 10:26:28;result=@ArrayList[
    @RequestFacade[org.apache.catalina.connector.RequestFacade@79f922b2],
    @NullPointerException[java.lang.NullPointerException],
]
```

#### Monitor

Monitor a specific method invocation statistics, including total number of invocations, average response time, success rate, and every 5 seconds:

```bash
$ monitor -c 5 org.apache.dubbo.demo.provider.DemoServiceImpl sayHello
Press Ctrl+C to abort.
Affect(class-cnt:1 , method-cnt:1) cost in 109 ms.
 timestamp            class                                           method    total  success  fail  avg-rt(ms)  fail-rate
----------------------------------------------------------------------------------------------------------------------------
 2018-09-20 09:45:32  org.apache.dubbo.demo.provider.DemoServiceImpl  sayHello  5      5        0     0.67        0.00%

 timestamp            class                                           method    total  success  fail  avg-rt(ms)  fail-rate
----------------------------------------------------------------------------------------------------------------------------
 2018-09-20 09:45:37  org.apache.dubbo.demo.provider.DemoServiceImpl  sayHello  5      5        0     1.00        0.00%

 timestamp            class                                           method    total  success  fail  avg-rt(ms)  fail-rate
----------------------------------------------------------------------------------------------------------------------------
 2018-09-20 09:45:42  org.apache.dubbo.demo.provider.DemoServiceImpl  sayHello  5      5        0     0.43        0.00%
```

#### Time Tunnel(tt)

Record method invocation data, so that you can check the method invocation parameters, returned value, and thrown exceptions later. It works as if you could come back and replay the past method invocation via time tunnel.

```bash
$ tt -t org.apache.dubbo.demo.provider.DemoServiceImpl sayHello
Press Ctrl+C to abort.
Affect(class-cnt:1 , method-cnt:1) cost in 75 ms.
 INDEX   TIMESTAMP            COST(ms)  IS-RET  IS-EXP   OBJECT         CLASS                          METHOD
-------------------------------------------------------------------------------------------------------------------------------------
 1000    2018-09-20 09:54:10  1.971195  true    false    0x55965cca     DemoServiceImpl                sayHello
 1001    2018-09-20 09:54:11  0.215685  true    false    0x55965cca     DemoServiceImpl                sayHello
 1002    2018-09-20 09:54:12  0.236303  true    false    0x55965cca     DemoServiceImpl                sayHello
 1003    2018-09-20 09:54:13  0.159598  true    false    0x55965cca     DemoServiceImpl                sayHello
 1004    2018-09-20 09:54:14  0.201982  true    false    0x55965cca     DemoServiceImpl                sayHello
 1005    2018-09-20 09:54:15  0.214205  true    false    0x55965cca     DemoServiceImpl                sayHello
 1006    2018-09-20 09:54:16  0.241863  true    false    0x55965cca     DemoServiceImpl                sayHello
 1007    2018-09-20 09:54:17  0.305747  true    false    0x55965cca     DemoServiceImpl                sayHello
 1008    2018-09-20 09:54:18  0.18468   true    false    0x55965cca     DemoServiceImpl                sayHello
```

#### Classloader

```bash
$ classloader
 name                                                  numberOfInstances  loadedCountTotal
 BootstrapClassLoader                                  1                  3346
 com.taobao.arthas.agent.ArthasClassloader             1                  1262
 java.net.URLClassLoader                               2                  1033
 org.apache.catalina.loader.ParallelWebappClassLoader  1                  628
 sun.reflect.DelegatingClassLoader                     166                166
 sun.misc.Launcher$AppClassLoader                      1                  31
 com.alibaba.fastjson.util.ASMClassLoader              6                  15
 sun.misc.Launcher$ExtClassLoader                      1                  7
 org.jvnet.hk2.internal.DelegatingClassLoader          2                  2
 sun.reflect.misc.MethodUtil                           1                  1
```

#### Web Console

* https://alibaba.github.io/arthas/en/web-console

![web console](site/src/site/sphinx/_static/web-console-local.png)


### Known Users

Welcome to register the company name in this issue: https://github.com/alibaba/arthas/issues/111 (in order of registration)

![Alibaba](static/alibaba.png)
![Alipay](static/alipay.png)
![Aliyun](static/aliyun.png)
![Taobao](static/taobao.png)
![Tmall](static/tmall.png)
![微医](static/weiyi.png)
![卓越教育](static/zhuoyuejiaoyu.png)
![狐狸金服](static/hulijingfu.png)
![三体云](static/santiyun.png)
![证大文化](static/zhengdawenhua.png)
![Acmedcare+](static/acmedcare.png)
![好慷](static/homeking365_log.png)
![来电科技](static/laidian.png)
![四格互联](static/sigehulian.png)
![ICBC](static/icbc.png)
![陆鹰](static/luying.png)
![玩友时代](static/wangyoushidai.png)
![她社区](static/tashequ.png)
![龙腾出行](static/longtengchuxing.png)
![foscam](static/foscam.png)
![二维火](static/2dfire.png)
![lanxum](static/lanxum_com.png)
![纳里健康](static/ngarihealth.png)
![掌门1对1](static/zhangmen.png)
![offcn](static/offcn.png)
![sia](static/sia.png)
![振安资产](static/zhenganzichang.png)
![菠萝](static/bolo.png)
![中通快递](static/zto.png)
![光点科技](static/guangdian.png)
![广州工程技术职业学院](static/gzvtc.jpg)
![mstar](static/mstar.png)
![xwbank](static/xwbank.png)
![imexue](static/imexue.png)
![keking](static/keking.png)
![secoo](static/secoo.jpg)
![viax](static/viax.png)
![yanedu](static/yanedu.png)
![duia](static/duia.png)
![哈啰出行](static/hellobike.png)
![hollycrm](static/hollycrm.png)
![citycloud](static/citycloud.jpg)
![yidianzixun](static/yidianzixun.png)
![神州租车](static/zuche.png)
![天眼查](static/tianyancha.png)
![商脉云](static/anjianyun.png)
![三新文化](static/sanxinbook.png)
![雪球财经](static/xueqiu.png)
![百安居](static/bthome.png)
![安心保险](static/95303.png)
![杭州源诚科技](static/hzyc.png)
![91moxie](static/91moxie.png)
![智慧开源](static/wisdom.png)
![富佳科技](static/fujias.png)
![鼎尖软件](static/dingjiansoft.png)
![广通软件](static/broada.png)

### Credit

#### Contributors

This project exists thanks to all the people who contribute.

   

#### Projects

* [greys-anatomy](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ed08a217d092feecc348638ee5cfb4af643d50594099d5bfd8666bbcd42cf010217a6412d2bd9a2210253901601c5702  The Arthas code base has derived from Greys, we thank for the excellent work done by Greys.
* [termd](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462fd281e41429a8a2d8bd7c957fd35e68  Arthas's terminal implementation is based on termd, an open source library for writing terminal applications in Java.
* [crash](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046134da6f0437ed964e78402c0386b136e6f6e0311141df801397bc71915085451  Arthas's text based user interface rendering is based on codes extracted from [here](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046134da6f0437ed964e78402c0386b136ee28a6993e427f6bca70db1d7db4b0e656546f918ff0ff7b813c8eb79d728f752) 
* [cli](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046008b1d80b36c17fd64c9fd9f304fe6df2c4a25fc5e97555013f58410b99cce4ab5ec054d220066461138b8402e7c4d3dfa5594a69cb5f406fa9649a4d91b71a8abb3bf67b95984833337980b3edd5ee0  Arthas's command line interface implementation is based on cli, open sourced by vert.x
* [compiler](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d5e2b6226cc20c36f60ca3f7bfcf3224fba71050748a3018d6e2d989f3138847f2186686824a10b2c7bdc3a1f6d55927)  Arthas's memory compiler.
* [Apache Commons Net](http://u.720life.cn/g/25b81716ea945ab6a84c5047ae290cf27413bb67d38e36a259445a4a4d6111d74bf3605d3adc3ee60a94908e56c3c1c1)  Arthas's telnet client.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)