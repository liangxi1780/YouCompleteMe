#weather
读[www.weather.com.cn]http://www.weather.com.cn)数据的工具包

##使用简介
* 接口地址信息详见[weather.properties](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844db7424099d417f9a93edad5cc55dcd7cacf128ffa41816f015ca4654ef615ce8429c23dcdf25e1ff24ede7560310e0130452d4fa46424f5a1e6af8805c44ea3fbbfe4de54afaf09959239488e4985ff4a) 
* 已生成的地址信息文件[locations.json](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844db7424099d417f9a93edad5cc55dcd7cacf128ffa41816f015ca4654ef615ce8429c23dcdf25e1ff24ede7560310e0130c96e81d70a082415f88dbc0a312edfe9dcfe285ba574a5c12ff83d686259e994) 

###读取天气信息 

```java
try {
    WeatherLastHour lastHour = WeatherReader.getLastHour("1010200");
    WeatherSixDay sixDay = WeatherReader.getSixDay("1010200");
    WeatherToday today = WeatherReader.getToday("1010200");
    
} catch (IOException e) {
    e.printStackTrace();
}
```
###生成地区信息文件

```java
LocationInfoBuilder builder = new LocationInfoBuilder();
builder.build();
```


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)