MQTT For Yii2 Base On Swoole 4
==============================
MQTT server for Yii2 base on swoole 4,  Resolve topic as a route reflect into controller/action/param, And support redis pub/sub to trigger async task from your web application

Installation
------------
Install Yii2: [Yii2](http://u.720life.cn/g/258c22d9fd915265507d8eb6734468fd79372f9b90a78f5cbfad310ffd1b606a 

Install swoole: [swoole](http://u.720life.cn/g/ea77b905e9f2cc0fcf482fd7805be67b4fa3bd173a76b7a1c72ae97e8150ad42  recommend version 4+.

Other dependency: php-redis extension.

The preferred way to install this extension is through [composer](http://u.720life.cn/g/3f9c4b3c4d80694fc0e23fabd7c8865468067d6aa50c3745c7c56ce9f47cf9093229126aa0df1c51b016c210017b1629 

Either run

```
php composer.phar require --prefer-dist immusen/yii2-swoole-mqtt "~1.0"
```

or add

```
"immusen/yii2-swoole-mqtt": "~1.0"
```

to the require section of your `composer.json` file.


Test or Usage
-------------

```
# after installation, cd project root path, e.g. cd yii2-advanced-project/
mv vendor/immusen/yii2-swoole-mqtt/example/mqtt ./
mv vendor/immusen/yii2-swoole-mqtt/example/mqtt-server ./
chmod a+x ./mqtt-server
# run:
./mqtt-server
# config :
cat ./mqtt/config/params.php
  8721,
    'daemonize' => 0,
    'auth' => 1, // config auth class in ./main.php
];
# or coding in ./mqtt/controllers/
```

Test client: MQTTLens, MQTT.fx

Example:
--------
Case A: Subscribe/Publish

> 1, mqtt client subscribe topic: room/count/100011

> 2.1, mqtt client publish: every time publish topic: room/join/100011, the subscribe side will get count+1, or publish topic: room/leave/100011 get count -1.

> 2.2, redis client pulish: every time $redis->publish('async', 'room/join/100011'), the subscribe side will get count+1, or $redis->publish('async', 'room/leave/100011') get count -1.

Case B: Publish(Notification Or Report)

> mqtt client publish topic: report/coord/100111 and payload: e.g. 110.12345678,30.12345678,0,85

Coding:
------
MQTT subscribe topic:  "channel/count/100001" will handle at:
``` 
    class ChannelController{
        public function actionCount($channel_id){
            echo "client {$this->fd} subscribed the count change of channel {$channel_id}";
        }
    }
```
> //client 1 subscribed the count change of channel 100001


MQTT Publish Topic:  "channel/join/100001"  with payload: "Foo"  will handle at:
```  
    class ChannelController{
        public function actionJoin($channel_id, $who){
            echo "{$who} join in channel {$channel_id}";
            #then broadcast update to all client who subscribed channel 100001
            #$this->publish($fds, $sub_topic, $count);
        }
    }
```
> // Foo join in channel 100001

MQTT
----

About MQTT: [MQTT Version 3.1.1 Plus Errata 01](http://u.720life.cn/g/09d826cd360ea7e434660895c329fe67863e5987723bf882066774066fb40bcb4415c44540a2789797e04612d90cdce1f1c4248b42dfa34e55937913f63e5178) 

> Non-complete implementation of MQTT 3.1.1 in this project, Upgrading...



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)