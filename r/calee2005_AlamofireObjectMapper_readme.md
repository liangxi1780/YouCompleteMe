AlamofireObjectMapper
============
[![Build Status](https://travis-ci.org/tristanhimmelman/AlamofireObjectMapper.svg?branch=master)](https://travis-ci.org/tristanhimmelman/AlamofireObjectMapper)
[![CocoaPods](https://img.shields.io/cocoapods/v/AlamofireObjectMapper.svg)](https://github.com/tristanhimmelman/AlamofireObjectMapper)
[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)


An extension to [Alamofire](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046fb6a364d1412ea6493936c0a3aa36a0e167c86976af07cbfbf7ddaee8319777c)  which automatically converts JSON response data into swift objects using [ObjectMapper](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c55f1fb85da0c7d7738f42f736509bf6e09c5cbd628d397690f99d19919209d6  

# Usage

Given a URL which returns weather data in the following form:
```
{
    "location": "Toronto, Canada",    
    "three_day_forecast": [
        { 
            "conditions": "Partly cloudy",
            "day" : "Monday",
            "temperature": 20 
        },
        { 
            "conditions": "Showers",
            "day" : "Tuesday",
            "temperature": 22 
        },
        { 
            "conditions": "Sunny",
            "day" : "Wednesday",
            "temperature": 28 
        }
    ]
}
```

You can use the extension as the follows:
```swift
import AlamofireObjectMapper

let URL = "https://raw.githubusercontent.com/tristanhimmelman/AlamofireObjectMapper/d8bb95982be8a11a2308e779bb9a9707ebe42ede/sample_json"
Alamofire.request(URL).responseObject { (response: DataResponse ) in

    let weatherResponse = response.result.value
    print(weatherResponse?.location)
    
    if let threeDayForecast = weatherResponse?.threeDayForecast {
        for forecast in threeDayForecast {
            print(forecast.day)
            print(forecast.temperature)           
        }
    }
}
```

The `WeatherResponse` object in the completion handler is a custom object which you define. The only requirement is that the object must conform to [ObjectMapper's](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c55f1fb85da0c7d7738f42f736509bf60a6693888a7012836ad97dce5958cf9a)  `Mappable` protocol. In the above example, the `WeatherResponse` object looks like the following:

```swift
import ObjectMapper

class WeatherResponse: Mappable {
    var location: String?
    var threeDayForecast: [Forecast]?
    
	required init?(map: Map){

	}
    
    func mapping(map: Map) {
        location  (queue: DispatchQueue? = nil, keyPath: String? = nil, mapToObject object: T? = nil, context: MapContext? = nil, completionHandler: @escaping (DataResponse ) -> Void) -> Self
```
The `responseObject` function has 4 optional parameters and a required completionHandler:
- `queue`: The queue on which the completion handler is dispatched.
- `keyPath`: The key path of the JSON where object mapping should be performed.
- `mapToObject`: An object to perform the mapping on to.
- `context`: A [context object](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c55f1fb85da0c7d7738f42f736509bf62ab6db6436d03505828f4fb4c785274f1f38048de0a7e5c759de37f60880d10a)  that is passed to the mapping function.
- `completionHandler`: A closure to be executed once the request has finished and the data has been mapped by ObjectMapper.

### Easy Mapping of Nested Objects

AlamofireObjectMapper supports dot notation within keys for easy mapping of nested objects. Given the following JSON String:
```json
"distance" : {
     "text" : "102 ft",
     "value" : 31
}
```
You can access the nested objects as follows:
```swift
func mapping(map: Map) {
    distance  ) in
    expectation.fulfill()
    
    let weatherResponse = response.result.value
    print(weatherResponse?.location)
    
    if let threeDayForecast = weatherResponse?.threeDayForecast {
        for forecast in threeDayForecast {
            print(forecast.day)
            print(forecast.temperature)           
        }
    }
}
```

# Array Responses
If you have an endpoint that returns data in `Array` form you can map it with the following function:
```swift
public func responseArray (queue queue: dispatch_queue_t? = nil, keyPath: String? = nil, completionHandler: DataResponse  -> Void) -> Self
```

For example, if your endpoint returns the following:
```
[
    { 
        "conditions": "Partly cloudy",
        "day" : "Monday",
        "temperature": 20 
    },
    { 
        "conditions": "Showers",
        "day" : "Tuesday",
        "temperature": 22 
    },
    { 
        "conditions": "Sunny",
        "day" : "Wednesday",
        "temperature": 28 
    }
]
```
You can request and map it as follows:
```swift
let URL = "https://raw.githubusercontent.com/tristanhimmelman/AlamofireObjectMapper/f583be1121dbc5e9b0381b3017718a70c31054f7/sample_array_json"
Alamofire.request(URL).responseArray { (response: DataResponse ) in

    let forecastArray = response.result.value
    
    if let forecastArray = forecastArray {
        for forecast in forecastArray {
            print(forecast.day)
            print(forecast.temperature)           
        }
    }
}

```

# Installation
AlamofireObjectMapper can be added to your project using [CocoaPods](http://u.720life.cn/g/77a38086ed44384e91ae28cd5ee2cdc972334dacf1a469b699593e9e5c3357dc)  by adding the following line to your Podfile:
```
pod 'AlamofireObjectMapper', '~> 5.2'
```

If you're using [Carthage](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f8566d4c7bb2e79d97422e59628e897058997b6aacadc9ac11b35bdee60840f2)  you can add a dependency on AlamofireObjectMapper by adding it to your Cartfile:
```
github "tristanhimmelman/AlamofireObjectMapper" ~> 5.2
```



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)