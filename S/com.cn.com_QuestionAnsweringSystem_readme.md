##QuestionAnsweringSystem是一个Java实现的人机问答系统，能够自动分析问题并给出候选答案。IBM人工智能计算机系统"沃森"（Watson）在2011年2月美国热门的电视智力问答节目"危险边缘"（Jeopardy！）中战胜了两位人类冠军选手，QuestionAnsweringSystem就是IBM Watson的Java开源实现。

##使用方法：

    1、安装JDK8和Maven3.3.3
        将JDK的bin目录和Maven的bin目录加入PATH环境变量，确保在命令行能调用java和mvn命令：
        java -version
            java version "1.8.0_60"
        mvn -v
            Apache Maven 3.3.3
            
    2、获取人机问答系统源码
        git clone https://github.com/ysc/QuestionAnsweringSystem.git
        cd QuestionAnsweringSystem
        建议自己注册一个GitHub账号，将项目Fork到自己的账号下，然后再从自己的账号下签出项目源码，
        这样便于使用GitHub的Pull requests功能进行协作开发。
    
    3、运行项目
        unix类操作系统执行：
            chmod +x startup.sh & ./startup.sh
        windows类操作系统执行：
            ./startup.bat

    4、使用系统
        打开浏览器访问：http://localhost:8080/deep-qa-web/index.jsp

##工作原理：

    1、判断问题类型（答案类型），当前使用模式匹配的方法，将来支持更多的方法，如朴素贝叶斯分类器。
    2、提取问题关键词。
    3、利用问题关键词搜索多种数据源，当前的数据源主要是人工标注的语料库、谷歌、百度。
    4、从搜索结果中根据问题类型（答案类型）提取候选答案。
    5、结合问题以及搜索结果对候选答案进行打分。
    6、返回得分最高的TopN项候选答案。
	
##目前支持5种问题类型（答案类型）：

    1、人名 
		如：
		APDPlat的作者是谁？
		APDPlat的发起人是谁？
		谁死后布了七十二疑冢？
		习近平最爱的女人是谁？
	2、地名
		如：
		“海的女儿”是哪个城市的城徽？
		世界上流经国家最多的河流是哪一条？
		世界上最长的河流是什么？
		汉城是哪个国家的首都？
	3、机构团体名
		如：
		BMW是哪个汽车公司制造的？
		长城信用卡是哪家银行发行的？
		美国历史上第一所高等学府是哪个学校？
		前身是红色中华通讯社的是什么？
	4、数字
		如：
		全球表面积有多少平方公里？
		撒哈拉有多少平方公里？
		北京大学占地多少平方米？
		撒哈拉有多少平方公里？
	5、时间
		如：
		哪一年第一次提出“大跃进”的口号？
		大庆油田是哪一年发现的？
		澳门是在哪一年回归祖国怀抱的？
		邓小平在什么时候进行南巡讲话？
		
##API接口：

	调用地址：
		http://127.0.0.1/api/ask?n=1&q=APDPlat的作者是谁？
	参数：
		n表示需要返回的答案的个数
		q表示问题
	编码：
		服务端和客户端均使用UTF-8编码
		服务端需要修改tomcat配置文件conf/server.xml，在相应的Connector中加入配置URIEncoding="UTF-8"
	返回json:
		[
			{
				"answer": "杨尚川",
				"score": 1
			}
		]
			
##使用说明：

1、初始化MySQL数据库(MySQL作为数据缓存区使用，此步骤可选)：   

    在MySQL命令行中执行QuestionAnsweringSystem\deep-qa\src\main\resources\mysql\questionanswer.sql文件中的脚本   
    MySQL编码：UTF-8，
    主机：127.0.0.1
    端口：3306
    数据库：questionanswer
    用户名：root
    密码：root
	
2、构建war文件并部署到tomcat：

    cd QuestionAnsweringSystem   
    mvn install   
    cd deep-qa-web\target
    cp deep-qa-web-1.1.war apache-tomcat-7.0.37/webapps/QuestionAnsweringSystem.war   
    启动tomcat
	
3、打开浏览器访问：

    http://localhost:8080/QuestionAnsweringSystem/
	
[可部署war包下载](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a4125ed946db7d2dd7b36d953c777884bb4) 

##如何在你的应用中集成人机问答系统QuestionAnsweringSystem? 

    QuestionAnsweringSystem提供了两种集成方式，以库的方式嵌入到应用中，以平台的方式独立部署。

    下面说说这两种方式如何做。

    1、以库的方式嵌入到应用中。

    这种方式只支持Java平台，可通过Maven依赖将库加入构建路径，如下所示：

     
         org.apdplat 
         deep-qa 
         1.1 
     

    在应用如何使用呢？示例代码如下：
    
    String questionStr = "APDPlat的作者是谁？";
    Question question = SharedQuestionAnsweringSystem.getInstance().answerQuestion(questionStr);
    if (question != null) {
        List  candidateAnswers = question.getAllCandidateAnswer();
        int i=1;
        for(CandidateAnswer candidateAnswer : candidateAnswers){
            System.out.println((i++)+"、"+candidateAnswer.getAnswer()+":"+candidateAnswer.getScore());
        }
    }

    运行程序后会在当前目录下生成目录deep-qa，目录里面又有两个目录dic和questionTypePatterns。
    dic是中文分词组件依赖的词库，questionTypePatterns是问题类别分析依赖的模式定义，可根据自己的需要修改。

    2、以平台的方式独立部署。

    首先在自己的服务器上如192.168.0.1部署好了，然后就可以通过Json Over HTTP的方式提供服务，使用方法如下所示：

    调用地址：
    http://192.168.0.1/api/ask?n=1&q=APDPlat的作者是谁？
    参数：
    n表示需要返回的答案的个数
    q表示问题
    编码：
    UTF-8编码
    返回json:
    [
        {
            "answer": "杨尚川",
            "score": 1
        }
    ]

##深入了解：

    QuestionAnsweringSystem由2个子项目构成，deep-qa和deep-qa-web。
    deep-qa是核心部分，deep-qa-web提供web界面来和用户交互，同时也提供了Json Over HTTP的访问接口，便于异构系统的集成。
    deep-qa是一个jar包，可通过maven引用：
    
     
         org.apdplat 
         deep-qa 
         1.1 
     

    示例代码如下：

    String questionStr = "APDPlat的作者是谁？";
    Question question = SharedQuestionAnsweringSystem.getInstance().answerQuestion(questionStr);
    if (question != null) {
        List  candidateAnswers = question.getAllCandidateAnswer();
        int i=1;
        for(CandidateAnswer candidateAnswer : candidateAnswers){
            System.out.println((i++)+"、"+candidateAnswer.getAnswer()+":"+candidateAnswer.getScore());
        }
    }

    运行程序后会在当前目录下生成目录deep-qa，目录里面又有两个目录dic和questionTypePatterns。
    dic是中文分词组件依赖的词库，questionTypePatterns是问题类别分析依赖的模式定义，可根据自己的需要修改。

[测试人机问答系统智能性的3760个问题](http://u.720life.cn/g/b56a32676c52deea69b3fa6af7eae602bc0edcffe890e3f5fecb60a43be713deed6ebb119b7aff819ab784a106b6ac09) 

[人机问答系统的前世今生](http://u.720life.cn/g/b56a32676c52deea69b3fa6af7eae602bc0edcffe890e3f5fecb60a43be713de9268d310ba13e59a0f65d3f12aa8b88b) 

[人机问答系统的类别](http://u.720life.cn/g/b56a32676c52deea69b3fa6af7eae602bc0edcffe890e3f5fecb60a43be713dec67903b7ee1ae5db1b8ce3b837b820a1) 

[What is Question Answering?](http://u.720life.cn/g/448b263c15b48cb08a0a28be1ea6ddbebb0eb00010c3bd14408a26b1ee10ba6891ca881603f16225466a5c7910d3202e) 

其他人机问答系统介绍：

1、OpenEphyra（Java开源）

    Ephyra is a modular and extensible framework for open domain question answering (QA). 
    The system retrieves accurate answers to natural language questions from the Web and 
    other sources. 
    
[OpenEphyra主页](http://u.720life.cn/g/482998388336efecc15a00c4972bfca738712126dd86cbfb4e56023abeb198ff) 

2、Watsonsim（Java开源）
    
    Open-domain question answering system from UNCC.
    Watsonsim works using a pipeline of operations on questions, candidate answers, and 
    their supporting passages. 
    In many ways it is similar to IBM's Watson, and Petr's YodaQA. 
    It's not all that similar to more logic based systems like OpenCog or Wolfram Alpha.
    
[Watsonsim主页](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c29153f0350f04a5097ced07fa99ba381f87362a0e861ea7fdb826781bc7109c) 

3、YodaQA（Java开源）

    YodaQA is an open source Question Answering system.
    using on-the-fly Information Extraction from various data sources (mainly enwiki).
    YodaQA stands for "Yet anOther Deep Answering pipeline" and 
    the system is inspired by the DeepQA (IBM Watson) papers. 
    It is built on top of the Apache UIMA.
    
[YodaQA主页](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f84a41b8face67bcb4de89d6bf6d825675c0c1cd391c64eb02ce9bb136930edb) 

4、OpenQA（Java开源）

    OpenQA is an open source question answering framework that unifies approaches from 
    several domain experts. 
    The aim of OpenQA is to provide a common platform that can be used to promote advances 
    by easy integration and measurement of different approaches.
    
[OpenQA主页](http://u.720life.cn/g/4a0d781e6a65844e27cc21baeeb5339858a38fc3c7285c0f704b86d2dafe90d8) 

5、START（商业）

    START, the world's first Web-based question answering system, has been on-line 
    and continuously operating since December, 1993. 
    
    It has been developed by Boris Katz and his associates of the InfoLab Group 
    at the MIT Computer Science and Artificial Intelligence Laboratory. 
    
    Unlike information retrieval systems (e.g., search engines), 
    START aims to supply users with "just the right information" 
    instead of merely providing a list of hits. 
    
    Currently, the system can answer millions of English questions about 
    places (e.g., cities, countries, lakes, coordinates, weather, maps, demographics, 
    political and economic systems), movies (e.g., titles, actors, directors), 
    people (e.g., birth dates, biographies), dictionary definitions, and much, much more.
    
[START主页](http://u.720life.cn/g/5c90e89dbe6c18ef1fc46a0f5e45976f8ae877ee938155855b8e250939bf9081bef1c9ba7c6b6569b334f0c38c80f582) 

6、IBM Watson（商业）

    Watson is built to mirror the same learning process that we have.
    Watson has been learning the language of professions and is trained 
    by experts to work across many different industries. 
        
[IBM Watson主页](http://u.720life.cn/g/f21fa08637b636c027532cc2314161dc8403a744e885a72d80586e416764642926fb47052046b11343ed7338ea89579bcaafbf96084f482a681b8c2c0eaba0ef1f1dbaef11efd6a53d2ccd38e7056249) 
    
7、Siri（商业）

    Siri /ˈsɪri/ is a part of Apple Inc.'s iOS which works as 
    an intelligent personal assistant and knowledge navigator. 
    The feature uses a natural language user interface to 
    answer questions, make recommendations, and perform actions 
    by delegating requests to a set of Web services. 

[Siri主页](http://u.720life.cn/g/c6391381b80c5d4bf11f1dd493dc78ada4a118950869f0740f76303bca2382c8) 

8、Wolfram|Alpha（商业）

    Wolfram|Alpha introduces a fundamentally new way to get knowledge and answers 
    not by searching the web, but by doing dynamic computations based on a vast collection 
    of built-in data, algorithms, and methods.
    
[Wolfram|Alpha主页](http://u.720life.cn/g/84d9d004d875832467eee3b4f8e3f25f08217f630920c471e995ae9f507dee45) 
    
9、Evi（商业）
    
    Evi was founded in August 2005, originally under the name of True Knowledge, with the mission 
    of powering a new kind of search experience where users can access the world's knowledge simply 
    by asking for the information they need in a way that is completely natural.
    
[Evi主页](http://u.720life.cn/g/2ca6aee51a5e0d728bd6d7c83f82c99048f9f141d86f0db0f841c59d8c753286) 

10、微软小冰（商业）

    微软小冰是智能聊天机器人，基于微软搜索引擎和大数据积累，所有数据全部来自于公开的互联网网页信息。
    
[微软小冰主页](http://u.720life.cn/g/f651b8865e983984f19b5ba8eb49e1c3c8710a486642fdbef7859710c7012ed9) 
    
11、Magi Semantic Search（商业）

    Magi is a search engine that gives you answers instead of references. 
    It's designed to be General, Feasible and Useful. 

[Magi Semantic Search主页](http://u.720life.cn/g/a9cdf832a015234c7f4d4574c37d514644d0d9bc37d9dbb6f28ca929691141cd) 
    


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)