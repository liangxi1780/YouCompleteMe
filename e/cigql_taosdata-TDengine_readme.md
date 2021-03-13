[![Build Status](https://travis-ci.org/taosdata/TDengine.svg?branch=develop)](https://travis-ci.org/taosdata/TDengine)
[![Build status](https://ci.appveyor.com/api/projects/status/kf3pwh2or5afsgl9/branch/develop?svg=true)](https://ci.appveyor.com/project/sangshuduo/tdengine-2n8ge/branch/develop)


[![TDengine](TDenginelogo.png)](https://www.taosdata.com)

# What is TDengine？

TDengine is an open-sourced big data platform under [GNU AGPL v3.0](http://u.720life.cn/g/0faf03d8167674bee364b61e9b7d6858faa547366fa4dc74b7ddcdf6fc488b81c1f1df709715ce8b45075eaf99dd155c  designed and optimized for the Internet of Things (IoT), Connected Cars, Industrial IoT, and IT Infrastructure and Application Monitoring. Besides the 10x faster time-series database, it provides caching, stream computing, message queuing and other functionalities to reduce the complexity and cost of development and operation.

- **10x Faster on Insert/Query Speeds**: Through the innovative design on storage, on a single-core machine, over 20K requests can be processed, millions of data points can be ingested, and over 10 million data points can be retrieved in a second. It is 10 times faster than other databases.

- **1/5 Hardware/Cloud Service Costs**: Compared with typical big data solutions, less than 1/5 of computing resources are required. Via column-based storage and tuned compression algorithms for different data types, less than 1/10 of storage space is needed.

- **Full Stack for Time-Series Data**: By integrating a database with message queuing, caching, and stream computing features together, it is no longer necessary to integrate Kafka/Redis/HBase/Spark or other software. It makes the system architecture much simpler and more robust.

- **Powerful Data Analysis**: Whether it is 10 years or one minute ago, data can be queried just by specifying the time range. Data can be aggregated over time, multiple time streams or both. Ad Hoc queries or analyses can be executed via TDengine shell, Python, R or Matlab.

- **Seamless Integration with Other Tools**: Telegraf, Grafana, Matlab, R, and other tools can be integrated with TDengine without a line of code. MQTT, OPC, Hadoop, Spark, and many others will be integrated soon.

- **Zero Management, No Learning Curve**: It takes only seconds to download, install, and run it successfully; there are no other dependencies. Automatic partitioning on tables or DBs. Standard SQL is used, with C/C++, Python, JDBC, Go and RESTful connectors.

# Documentation
For user manual, system design and architecture, engineering blogs, refer to [TDengine Documentation](http://u.720life.cn/g/38479dcb4cee8c7863a4fe77e7e96c5d064354ed9a124b31892aa5aba11653087f35a04d3736abcfd60e8431b6f9049a) 
 for details. The documentation from our website can also be downloaded locally from *documentation/tdenginedocs-en* or *documentation/tdenginedocs-cn*.

# Building
At the moment, TDengine only supports building and running on Linux systems. You can choose to [install from packages](http://u.720life.cn/g/38479dcb4cee8c7863a4fe77e7e96c5dbccfb8ee626ce45f05fab8d0ba8ed10c63841f3641df7d5f9991025402fec94f8bc5c12e349a059ac6519210250bdaff878d31e686e0ea49ebcbac477d17754f)  or from the source code. This quick guide is for installation from the source only.

To build TDengine, use [CMake](http://u.720life.cn/g/a75d52cde9c3226230e6270162b9978ed4e33551b0ccc52c9de11de3d76ae1bf)  2.8 or higher versions in the project directory. Install CMake for example on Ubuntu:
```
sudo apt-get install -y cmake build-essential
```

To compile and package the JDBC driver source code, you should have a Java jdk-8 or higher and Apache Maven 2.7 or higher installed. 
To install openjdk-8 on Ubuntu:
```
sudo apt-get install openjdk-8-jdk
```
To install Apache Maven on Ubuntu:
```
sudo apt-get install maven
```

Build TDengine:

```
mkdir build && cd build
cmake .. && cmake --build .
```

To compile on an ARM processor (aarch64 or aarch32), please add option CPUTYPE as below:

aarch64:
```cmd
cmake .. -DCPUTYPE=aarch64 && cmake --build .
```

aarch32:
```cmd
cmake .. -DCPUTYPE=aarch32 && cmake --build .
```

# Quick Run
To quickly start a TDengine server after building, run the command below in terminal:
```cmd
./build/bin/taosd -c test/cfg
```
In another terminal, use the TDengine shell to connect the server:
```
./build/bin/taos -c test/cfg
```
option "-c test/cfg" specifies the system configuration file directory. 

# Installing
After building successfully, TDengine can be installed by:
```cmd
make install
```
Users can find more information about directories installed on the system in the [directory and files](http://u.720life.cn/g/38479dcb4cee8c7863a4fe77e7e96c5d064354ed9a124b31892aa5aba11653084f5e39550423ea39e93c07c42f72ea9508e14436a8ac63999674190160df862fd2ec1f81435634f840cd860f36316d45)  section. It should be noted that installing from source code does not configure service management for TDengine.
Users can also choose to [install from packages](http://u.720life.cn/g/38479dcb4cee8c7863a4fe77e7e96c5dbccfb8ee626ce45f05fab8d0ba8ed10c63841f3641df7d5f9991025402fec94f8bc5c12e349a059ac6519210250bdaff878d31e686e0ea49ebcbac477d17754f)  for it.

To start the service after installation, in a terminal, use:
```cmd
taosd
```

Then users can use the [TDengine shell](http://u.720life.cn/g/38479dcb4cee8c7863a4fe77e7e96c5dbccfb8ee626ce45f05fab8d0ba8ed10c3bad39de3025cd72c1330b9a864095bd6ad4aa345df8735a0016541540cdcfc8)  to connect the TDengine server. In a terminal, use:
```cmd
taos
```

If TDengine shell connects the server successfully, welcome messages and version info are printed. Otherwise, an error message is shown.

# Try TDengine
It is easy to run SQL commands from TDengine shell which is the same as other SQL databases.
```sql
create database db;
use db;
create table t (ts timestamp, a int);
insert into t values ('2019-07-15 00:00:00', 1);
insert into t values ('2019-07-15 01:00:00', 2);
select * from t;
drop database db;
```

# Developing with TDengine
### Official Connectors

TDengine provides abundant developing tools for users to develop on TDengine. Follow the links below to find your desired connectors and relevant documentation.

- [Java](http://u.720life.cn/g/38479dcb4cee8c7863a4fe77e7e96c5d064354ed9a124b31892aa5aba116530821fa954914066aa5a033990b817efaafd3685fe053ad6ec5e5be56d7a32c74d4174e0cd86031c0d4ce799987a8f7b7e3) 
- [C/C++](http://u.720life.cn/g/38479dcb4cee8c7863a4fe77e7e96c5d064354ed9a124b31892aa5aba116530821fa954914066aa5a033990b817efaaf7f253916fa7ac7eb42e5eca43063ebc523c6c20eda5789e05b46e99294afde82) 
- [Python](http://u.720life.cn/g/38479dcb4cee8c7863a4fe77e7e96c5d064354ed9a124b31892aa5aba116530821fa954914066aa5a033990b817efaaf795ec3d69dbb94f3b407754699588e1d6a290c74ca2e5e8d9afd399a30e0c16f) 
- [Go](http://u.720life.cn/g/38479dcb4cee8c7863a4fe77e7e96c5d064354ed9a124b31892aa5aba116530821fa954914066aa5a033990b817efaaf8a068c7e4fcece023dab585c54d715868e7b04b42419d51f1a88dd49f6bbcdb0) 
- [RESTful API](http://u.720life.cn/g/38479dcb4cee8c7863a4fe77e7e96c5d064354ed9a124b31892aa5aba116530821fa954914066aa5a033990b817efaaff1ece4e5b220ff709b20007d72141912e891ea231859ba9bc5c9179130a917a9) 
- [Node.js](http://u.720life.cn/g/38479dcb4cee8c7863a4fe77e7e96c5d064354ed9a124b31892aa5aba116530821fa954914066aa5a033990b817efaaf4f76b6cac970905ef0a1b2c5ba3495002b714906c64f857b9b052714ffe407a6) 

### Third Party Connectors

The TDengine community has also kindly built some of their own connectors! Follow the links below to find the source code for them.

- [Rust Connector](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304691cf5badcd683fbc0e28945b224fe3aa875b5730421c1a4d232466bdfaf9432ba9544c0167749de4927442ddbb8f57a509859b253087bae58d8f0ef059bd8e27) 
- [.Net Core Connector](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046eda225c43b1882bedd446e1b57ebd7ab1e70980474e4e8262c9d466fc8d9993283af6ab8761d1a8528c543d2ba84dfec) 

# TDengine Roadmap
- Support event-driven stream computing
- Support user defined functions
- Support MQTT connection
- Support OPC connection
- Support Hadoop, Spark connections
- Support Tableau and other BI tools

# Contribute to TDengine

Please follow the [contribution guidelines](CONTRIBUTING.md) to contribute to the project.

# Join TDengine WeChat Group

Add WeChat “tdengine” to join the group，you can communicate with other users.




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)