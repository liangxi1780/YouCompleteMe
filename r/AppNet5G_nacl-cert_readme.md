NaCL Cert System Specification based on TweetNaCL
-------------------------------------------------

NACL Certification System


### Certification file format as JSON consists of description and signature parts

* Description object defined as below

```js
  {  
      // common part or request part  
        "version": string,       // version: '1.0'  
           "type": string,       // type: 'self', 'ca'  
            "tte": Date as ms,   // cert live time to expire from UTC 1970-01-01T00:00:00Z, ms  
             "ca": string        // CA domain name, like appnet.link,  
                                 // in case self-sign it MUST be filled in advance  
      "publickey": byte array,   // NACL Box public key to sign with CA,  
                                 // or Sign public key to sign by self  
          "names": string array, // domain name to ask sign, ignore for self-sign cert  
            "ips": string array, // domain ip address to ask sign, ignore for self-sign cert
           "macs": string array, // domain mac address to ask sign, ignore for self-sign cert  
              
      // append fields when sign  
            "gid": uuid string,  // cert global id: 16 bytes of uuid string  
       "signtime": Date as ms,   // signed time as ms from UTC 1970-01-01T00:00:00Z  
  }
  ```

* Signature object defined as below

```js
  {  
      signature: byte array      // NACL signature  
  }
  ```
  
* Entire cert object defined as below
```js
  {  
      desc: Description object,  
      sign: Signature object  
  }
  ```

### Cert request object defined as Common part of Description

```js
self-signed:  {  
     // common part or request part  
        "version": string,       // version: '1.0'  
           "type": 'self',       // type: 'self'  
            "tte": Date as ms,   // cert live time to expire from UTC 1970-01-01T00:00:00Z, ms  
             "ca": string        // CA domain name, like appnet.link  
      "publickey": byte array,   // NACL Sign public key to sign by self  
  }  
  
ca-signed:  {  
     // common part or request part  
        "version": string,       // version: '1.0'  
           "type": 'ca',         // type: 'ca'  
            "tte": Date as ms,   // cert live time to expire from UTC 1970-01-01T00:00:00Z, ms  
             "ca": string        // CA domain name, like appnet.link  
      "publickey": byte array,   // NACL box public key to sign
        
          "names": string array, // domain name to ask sign, ignore for self-sign cert      
            "ips": string array, // domain ip address to ask sign, ignore for self-sign cert
           "macs": string array, // domain mac address to ask sign, ignore for self-sign cert  
  }
  ```

 


### Reference implementations

* [JS/NodeJS](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468d6f25f24e3bf485ee7a06a60c932cef64ada4526aec263fae588ccb7bf35726) 
* [Java/Android](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468d6f25f24e3bf485ee7a06a60c932cef7622a6329ce62e62909306024de5247a3b515651ecd3569c3a95ebe051991aa312f1d0d0f0d5fc40eadb6f463768363420109795fb3d5da880bd7241f22f7d6c312197438ea7e27374b2ecad9dc395ab) 

### License
(MIT)

Copyright (c) 2014-present Tom Zhou(appnet.link@gmail.com)





 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)