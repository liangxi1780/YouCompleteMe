
# Arduino ThingsBoard SDK

[![Build Status](https://travis-ci.org/thingsboard/ThingsBoard-Arduino-MQTT-SDK.svg?branch=master)](https://travis-ci.org/thingsboard/ThingsBoard-Arduino-MQTT-SDK)

This library provides access to ThingsBoard platform over MQTT protocol.

## Examples

The SDK comes with a number of example sketches. See File > Examples > ThingsBoard within the Arduino application.
Please review the complete guide for ESP32 Pico Kit GPIO control and DHT22 sensor monitoring available [here](http://u.720life.cn/g/e9ef43ba5ca95f567a3a96171ad805a1cc15991583cde03fe838cf008c26e921aa11a0581bb0802e3ef165f123c98b0e6a6c3848655a2d6b01c2af0b2aebabc4941b6c5b1158f37b54ce179aeba6e1c2 

## Installation

ThingsBoard SDK can be installed directly from the Arduino Library manager.
Following dependencies must be installed, too:

 - [MQTT PubSub Client](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462034da00bcf3eaf637cf7a46e561b2d4a3c4ec5e031e79adea2fa621d4b8af32)  — for interacting with MQTT.
 - [ArduinoJSON](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463ab07e8e0e0cb65e8aba5f1a43762936923eb57a5b950671e7d73f3a1446a169)  — for dealing with JSON files.
 - [Arduino Http Client](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461c92e351f0a96417d6aa865d540e6a77853bb158c8eb91cb03c4cb7b7c927e8872de0f2a08f87e20b55a7fb19196d07b)  — for interacting with ThingsBoard using HTTP.

## Supported ThingsBoard Features

 - [Telemetry data upload](http://u.720life.cn/g/e9ef43ba5ca95f567a3a96171ad805a10e7bef71ec7cbd0f97cefc9447a947f13f36e7ded675571ada957f87e0b5915c05cc28d16cab3d5d45d8d59d233285e1c6e245b0e6bdb50e05a9087e7a6fc7c2) 
 - [Device attribute publish](http://u.720life.cn/g/e9ef43ba5ca95f567a3a96171ad805a10e7bef71ec7cbd0f97cefc9447a947f13f36e7ded675571ada957f87e0b5915c3040dd36376b49a77b2dd9e333482182bef394c214ca9a963ad68b9cc32c5d31a57932bb498f3ef9087dfdf41d2d1b5a) 
 - [Server-side RPC](http://u.720life.cn/g/e9ef43ba5ca95f567a3a96171ad805a10e7bef71ec7cbd0f97cefc9447a947f13f36e7ded675571ada957f87e0b5915cd67a0639a2da3d278ea08930b429f607) 

## Troubleshooting

### Not enough space for JSON serialization

The buffer size for the serialized JSON is fixed to 64 bytes. The SDK will reject a data, if there is more data to be sent. Respective logs in the "Serial Monitor" window will indicate the condition:

```
[TB] too small buffer for JSON data
```

If that's a case, the buffer size for serialization should be increased. To do so, `ThingsBoardSized` class can be used in place of `ThingsBoard` as illustrated below:

```cpp
// For the sake of example
WiFiEspClient espClient;

// The SDK setup with 64 bytes for JSON buffer
// ThingsBoard tb(espClient);

// The SDK setup with 128 bytes for JSON buffer
ThingsBoardSized  tb(espClient);
```

### Too much data fields must be serialized

A buffer allocated internally by ArduinoJson library is fixed and is capable for processing not more than 8 fields. If you are trying to send more than that, you will get an error in the "Serial Monitor" window of the Arduino IDE:

```
[TB] too much JSON fields passed
```

The solution is to use `ThingsBoardSized` class instead of `ThingsBoard`. **Note that the serialized JSON buffer size must be specified explicitly, as described [here](#not-enough-space-for-json-serialization).**

```cpp
// For the sake of example
WiFiEspClient espClient;

// The SDK setup with 8 fields for JSON object
// ThingsBoard tb(espClient);

// The SDK setup with 128 bytes for JSON payload and 32 fields for JSON object.
ThingsBoardSized  tb(espClient);
```

## Tips and Tricks
To use your own logger you have to create a class and pass it as third parameter Logger to your `ThingsBoardSized` class instance.

For example:

```cpp
class CustomLogger {
public:
  static void log(const char *error) {
    Serial.print("[Custom Logger] ");
    Serial.println(error);
  }
};
```
Your class must have method `log` with the same prototype as in the example. It will be called if some error occurs.

After that, you can use it in place of regular `ThingsBoard` class. **Note that the serialized JSON buffer size must be specified explicitly, as described [here](#too-much-data-fields-must-be-serialized).**

```cpp
// For the sake of example
WiFiEspClient espClient;

// The SDK setup with 8 fields for JSON object
// ThingsBoard tb(espClient);

// The SDK setup with 128 bytes for JSON payload and 32 fields for JSON object.
ThingsBoardSized  tb(espClient);
```

## Have a question or proposal?

You are welcomed in our [issues](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046dcf082d384f53c2262ad778ba0031870bc25b8551724ddf3d94544673431a72a5eeb42e090b7e3b412746a3e13f17be0b007c5f4597de021d463c5b127489d42)  and [Q&A forum](http://u.720life.cn/g/941693b557d072bb769494a6a61fcd979ee9fee4d4fd0c2a6b8a30bc68eade2104af9ac4326a5602cba7b5b6884aacbbacc036fc6845b0532ea777d9b9d1680c 

## License

This code is released under the MIT License.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)