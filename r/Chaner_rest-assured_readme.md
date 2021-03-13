![REST Assured](rest-assured-logo-green.png)

[![Build Status](https://travis-ci.org/rest-assured/rest-assured.svg)](https://travis-ci.org/rest-assured/rest-assured)
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/io.rest-assured/rest-assured/badge.svg)](https://maven-badges.herokuapp.com/maven-central/io.rest-assured/rest-assured)
[![Javadoc](https://javadoc-emblem.rhcloud.com/doc/io.rest-assured/rest-assured/badge.svg)](http://www.javadoc.io/doc/io.rest-assured/rest-assured)


Testing and validation of REST services in Java is harder than in dynamic languages 
such as Ruby and Groovy. REST Assured brings the simplicity of using these 
languages into the Java domain.


## News 
* 2016-09-21: REST Assured [3.0.1](http://u.720life.cn/g/66fe33f71a905208b0f27a8e0cde79b378a1dcd393c0ee87bbf7c722544b824910d72ac0b272efcbcccce4ada477791827160e370c87bb92ce4eb2b5f5ac3d47a14ea851fad01b742e86986a10494a35)  is released. This is a maintence release with several bug fixes. See [change log](http://u.720life.cn/g/bb9e19de933fd87f05600116164183c0b3ddd62d3854e3432c88c12f9e59c662a39a02e42b638ab352d330617eb59f6f745d800927cb88dc28df8a15217a0b2e45c42abb359d1a1bdc8852c6e8573bd9)  for details.
* 2016-06-03: REST Assured [3.0.0](http://u.720life.cn/g/66fe33f71a905208b0f27a8e0cde79b378a1dcd393c0ee87bbf7c722544b824910d72ac0b272efcbcccce4ada47779189f1384e007508c14ad40871209fd60d2de8be449507cc3173f2d64e87b6c0124)  is released. This is a new major release with lots of updates and new features such as the ability to use [any HTTP method](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f952d77627253406ced29e56a99c6d0032380d70c9e931a5056256988120153f5c1919aae988c8848369888417f24cc6f145263d73ab7fa16b64e8ec6f48da521f0edf847d09085db4b4d7ab75249d24  all HTTP methods now supports multipart uploads, improved error messages, improved JsonPath etc. **Note** The package name has changed to `io.restassured` and the groupId has changed to `io.rest-assured`. Please see [release notes](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f952d77627253406ced29e56a99c6d0032380d70c9e931a5056256988120153f4778745f93b2eacb717c7b22c57d3242)  and [getting started guide](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f952d77627253406ced29e56a99c6d0032380d70c9e931a5056256988120153feaa5e25c66df64d5806fcb9b9ec375aa)  for more details.

[Older News](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f952d77627253406ced29e56a99c6d0032380d70c9e931a5056256988120153f7587c559010eaedf21035d04a3130109) 


## Examples
Here's an example of how to make a GET request and validate the JSON or XML response:

```java
get("/lotto").then().assertThat().body("lotto.lottoId", equalTo(5));
```

Get and verify all winner ids:

```java
get("/lotto").then().assertThat().body("lotto.winners.winnerId", hasItems(23, 54));
```

Using parameters:

```java
given().
    param("key1", "value1").
    param("key2", "value2").
when().
    post("/somewhere").
then().
    body(containsString("OK"));
```

Using X-Path (XML only):

```java
given().
    params("firstName", "John", "lastName", "Doe").
when().
    post("/greetMe").
then().
    body(hasXPath("/greeting/firstName[text()='John']")).
```

Need authentication? REST Assured provides several authentication mechanisms:

```java
given().auth().basic(username, password).when().get("/secured").then().statusCode(200);
```

Getting and parsing a response body:

```java
// Example with JsonPath
String json = get("/lotto").asString()
List  winnderIds = from(json).get("lotto.winners.winnerId");
    
// Example with XmlPath
String xml = post("/shopping").andReturn().body().asString()
Node category = from(xml).get("shopping.category[0]");
```

REST Assured supports any HTTP method but has explicit support for *POST*, *GET*, *PUT*, *DELETE*, *OPTIONS*, *PATCH* and *HEAD* and includes specifying and validating e.g. parameters, headers, cookies and body easily.


## Documentation

* [Getting started](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f952d77627253406ced29e56a99c6d0032380d70c9e931a5056256988120153feaa5e25c66df64d5806fcb9b9ec375aa) 
* [Downloads](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f952d77627253406ced29e56a99c6d0032380d70c9e931a5056256988120153f3820ede55558ee532b16bbb6ee194635) 
* [Usage Guide](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f952d77627253406ced29e56a99c6d0032380d70c9e931a5056256988120153fe171350e531e1d385263f2b11ba739b9)  (click [here](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f952d77627253406ced29e56a99c6d0032380d70c9e931a5056256988120153fd2f9847030c16a0f2aa7ebbe758bcd67)  for legacy documentation)
* [Javadoc](http://u.720life.cn/g/baf7e84b21007bd05c28b6a31e2d24d9ef49c1487e4526b0774289287c1c8d3ad3d53614314f8b1c9414070f93d4e2a25d437d15c7efd85fc83d0d666434c402) 
* [Rest Assured Javadoc](http://u.720life.cn/g/a53fd5eac14a3b6d1d78cbeb251e801ce696fa94a25f8d049ea4ee8a707f748cbfcb416ef24c5be906745687fb9d52fc17a6da9a9d480228ff2749f1473888ccb0abcab2a8cb3bb0d10513071ab4b97f4a9111b5d3f43ef4c15e45abc37b45a4) 
* [Rest AssuredMockMvc Javadoc](http://u.720life.cn/g/a53fd5eac14a3b6d1d78cbeb251e801ce696fa94a25f8d049ea4ee8a707f748ca20deec4694a92250190f4edd2323789122284b7aa5472e645b169b04f1fec3c050f50941f3fbc996a84e60692599d341c34825477d0b2510f8168e378be7639091b5e3ac81cafb7a3e7a65f24527b874f81c2c06ccb2da2c6fcdb0d497ea382) 
* [XmlPath Javadoc](http://u.720life.cn/g/a53fd5eac14a3b6d1d78cbeb251e801ce696fa94a25f8d049ea4ee8a707f748c99c85c077835826071009362d1c719036397374097a517304659695cf2b85c9c550aefea8e406f0680eb55390f4fb868e6909c967266f7917a8689c6209ad91e) 
* [JsonPath Javadoc](http://u.720life.cn/g/a53fd5eac14a3b6d1d78cbeb251e801ce696fa94a25f8d049ea4ee8a707f748c214a5ca810fc5811d3ca206a267a7d09aadeef8c371d3b507365cf5478e787da95e4d9dbfd03cbd5d11de0ec5106eb030efc5a9e26ed7cc3927483b595dc5e13) 
* [Release Notes](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f952d77627253406ced29e56a99c6d0032380d70c9e931a5056256988120153ff7d16e9844b6d5ee449427fc77015bd1) 
* [FAQ](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f952d77627253406ced29e56a99c6d0032380d70c9e931a5056256988120153f291d2a60147172f0f9a11d504ced6f2e) 

## Support and discussion
Join the mailing list at our [Google group](http://u.720life.cn/g/92946f42bc9470f8655236cc83ba3a8dcf7f64856d615a4f1daa5252b1379d8f98267e31b3390f30f7e368bee6f3a5e6  

## Links
* [Change log](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f952d77627253406ced29e56a99c6d00a85397b67b848a696c8757bd1b6c2adae895a619fdc01e3e60dcc882c95d779f76b45b455ebcaa5ffb6783bc8f488ad4) 
* REST Assured on [Ohloh](http://u.720life.cn/g/fdd5fa93ad411ba171f92856eb15be2119af69bc9c1d620d3a2dd3bd384cc0dabf8b6865a19b99a83cd947f5275aea36) 
* [Mailing list](http://u.720life.cn/g/92946f42bc9470f8655236cc83ba3a8dcf7f64856d615a4f1daa5252b1379d8f83c4b2c0a7af62fd42502ef19dd890f1)  for questions and support



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)