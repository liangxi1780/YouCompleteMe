Apache Isis
===========

*[Apache Isis]http://isis.apache.org)™ software is a framework for rapidly developing domain-driven apps in Java.  Write your business logic in entities, domain services and repositories, and the framework dynamically generates a representation of that domain model as a webapp or a RESTful API.*

To see Isis in action, watch these [screencasts](http://u.720life.cn/g/53affa211c84853afb8c600893f0673d811e7310aec78b58bf16552c024cc8f2596377a3892050619864ba63ba3edbec226bd08e7f1ba93717cf5aaceaca6507 

Get started yourself using the [Maven archetype](http://u.720life.cn/g/53affa211c84853afb8c600893f0673dffa0c7c175ad33dffcecfc4c5a5d213c12594e7868cb2b5036fd2a11d98e90b00456d372b373410c22b68bb68e2e8d556d1eaf7b0972f0c679f5f8a7c0fa0180 

For help and support, join the [mailing lists](http://u.720life.cn/g/53affa211c84853afb8c600893f0673dc308b556b444b5acdee8510082c8ae3e19d2b46a88932ea0c5b869c096d5e721   

## Screenshots

Isis automatically generates the UI from the domain classes.  The following are taken from the [screenshots](http://u.720life.cn/g/53affa211c84853afb8c600893f0673d5fea0168ee14c61e618e3b2a53f47dd93bc420077747b1d44ebe252e7b0df171b7f1028091bcbc1beb1db600717945650e0b18d78453cfca8264f7dd8b09c2e7)  page on the Isis website.  The corresponding domain classes from which this UI was built can be found [here](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ce49333d2cc4bbeffcd1541ee36e7c4f160636bb3b182151cdbc216d80dd24763705aa98023f06e211d4027a80b378d74c93e1088aa8e7d310cbd05b39dea5e3694f826906bc5162bbd4b1748b996ccd4ce3514348e2e655d7c78dab7233ac03b28b52cedd6f100956ef3491e074c471 

A list of objects returned from a domain service action:

![](http://isis.apache.org/images/screenshots/08-collection-action.png)

A domain object:

![](http://isis.apache.org/images/screenshots/11-todo-entity.png)

Invoking an action:

![](http://isis.apache.org/images/screenshots/18-invoke-action-args.png)

The REST API for a domain object:

![](http://isis.apache.org/images/screenshots/screenshot-34-restful-entity.png)

## Extensions

The Wicket viewer is extensible; a number of extensions (hosted on github) are available integrating [google maps](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304640ddd7f535dcb32ddda5ef0e7fdfba16b2232288804c5a663d4c21b4ff3687bcfaa1aa9433996406de999e06c653381c  [charting](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304640ddd7f535dcb32ddda5ef0e7fdfba164500d3309b5332c1b3f9385ea989c121f7e821dce0741266f9f7385c631a500d  and also a [calendar](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304640ddd7f535dcb32ddda5ef0e7fdfba162014ff015a9c8a18a6b81930a0b39635ebea6b916fbec1d076b9ca00d4e47d98)  and [excel download](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304640ddd7f535dcb32ddda5ef0e7fdfba163bb5cdfe8bc780bb337fca5d10907a843ba38536bde4a7867e8a308fc437be77 

#### Google maps v3 integration

Standalone collection:

 

Parented collection:

 


#### Calendar integration

Standalone collection:

 


Parented collection in a custom dashboard view model

 


Parented collection in a regular entity:

 

#### Excel integration

The extension renders a new tab (highlighted): 

 

Clicking the tab provides a download link:

 

The downloaded file can be opened in Excel:

 


#### Wicked Charts integration

Summary chart for a collection with `BigDecimal` properties:

 

... renders the returned chart with associated summary data:

 


Scalar chart, being the result of an action to analyze `ToDoItem`s by their category:

 

A scalar chart is simply a wrapper around a [WickedChart](http://u.720life.cn/g/738704681c531f76765d4dc4a33351930dcc2da3c45bbd92c4dd5adf0965bd76e225df07a40ce3283895005f6041cfb6 
s




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)