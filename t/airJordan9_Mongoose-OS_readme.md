[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)  [![Gitter](https://badges.gitter.im/cesanta/mongoose-os.svg)](https://gitter.im/cesanta/mongoose-os?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

# Mongoose OS - an IoT Firmware Development Framework

- Over-The-Air firmware updates and remote management - reliable updates with rollback on failures, remote device access infrastructure
- Security - 	built in flash encryption, crypto chip support, ARM mbedTLS optimized for small memory footprint
- [Device management dashboard service](http://u.720life.cn/g/b673fdb4dcf8996bd3f4d61d037e85a71aaa2afb6505aeb1d46881fb0c854f84) 
- Supported microcontrollers: CC3220, CC3200, ESP32, ESP8266, STM32F4, STM32L4, STM32F7
- Recommended dev kits: [ESP32-DevKitC for AWS IoT](http://u.720life.cn/g/17ca4bf30fedad22be68a8d56ffa3982f589e9ba2a2b7bea2f3ef6b5bd41c0aaae21c39550fc322d7fd660379f343ce1  [ESP32 Kit for Google IoT Core](http://u.720life.cn/g/17ca4bf30fedad22be68a8d56ffa3982dc3bbfb939b0cfcaedd2be1a55a7b169) 
- Built-in integration for AWS IoT, Google IoT Core, Microsoft Azure, Adafruit IO, generic MQTT servers
- Code in C or JavaScript
- Ready to go Apps and Libraries
- [Embedded JavaScript engine - mJS](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b12c1fbabfc2588b295d08b7e67ef37e) 


Trusted and Recommended By:
- Amazon AWS - [Amazon AWS Technology Partner](http://u.720life.cn/g/27820330f4d197042ec05c336c0aab24d06da5674896fe642f98089ba2d9498349fc19d6b7a63116acaf22c98fc6bbaa89eb0633e45f0c16d7383abffdc6d0317335f0db3f410fd337fd90ecd97ec0e4) 
- Google IoT Core - [Mongoose OS is a Google Cloud IoT Core Partner](http://u.720life.cn/g/bc2b69ab4567718d93479b15660de06d0d5562898dd263716f504f0af71320db446abfee62efb46b0eb368685e5a5a58) 
- IBM Watson IoT - [Mongoose OS is a Ready for IBM Watson IoT validated solution](http://u.720life.cn/g/9b7f7d2ea6a0416797ecaf87021cb45d54d0ccb1be9ddb5cf7a8eec4436ec3d3d6fb8b6a812620e40b3ed9c5c8a7f765431db06d1ad5dde8a9caecb9a054ababc174ff2d6afb13a7c69f50cc81d75366557b737ec8f3ba0c510037b58320e7c5) 
- Microsoft Azure IoT - [Mongoose OS is recommended by Microsoft Azure IoT](http://u.720life.cn/g/08a23d9c242a0aac3f1ee3afc4f56dc2b637f5c1ea256c314d24e12037ad3958562f34b9cd8e7be65dcdfa46486cb5a8423eeb574156a06e24421b97eb81caeb52f2539c3919ba7d1ec805bfb9cfbd77822d482f8e1aa88d2afb1f9d25e671716efbc18abede90b5306011142c02a907475b8a5317037ce66b7cfedec2f67874) 
- Texas Instruments - [an official partner of Texas Instruments](http://u.720life.cn/g/379ed56e1e5c77b2311cb0bc39cd29e2ec5faa5b36c9d607213a0387ad9f60e9a816432a8917d778d5afbdbc9d82ebb0c4c50da667fff5356b1e81ebdaf7964c685d94e0a361e3fb4435a016afc1b2b9) 
- STMicroelectronics - [an official partner of STMicroelectronics](http://u.720life.cn/g/d53d2da185d62ac3818cddc9996de744352beb361c726deca692ae2b7af739990978d552efba822c08598aedbe8b5d3fb2d624109520cd743a856ea201925c2075aaaad88912b7328e50ab099415b57db32d035133988a58e9ef4261ccb5b985) 
- Espressif Systems - [an official partner of Espressif Systems](http://u.720life.cn/g/28d5d24a0db702b871bf379e3e4c7e0bec93f4049d6065eb8695ade917af7957f062c1b393b6f2a68090ab867644b7b7) 



# Docs, Support
- [Mongoose OS Documentation](http://u.720life.cn/g/17ca4bf30fedad22be68a8d56ffa3982b25638f9c551e7718abc9ad62cc1e7653614c7e01a2953b1e74f84a9b91ec0984fedb773338974b2375d0060053b6005) 
- [Support Forum - ask your technical questions here](http://u.720life.cn/g/1486213a66d08c740744c61ea7141c4b6c84ebbc54db93acf8a9fe67de330465) 
- [Video tutorials](http://u.720life.cn/g/2bc656cc69a0e9056dae2ced9f817b90e4824d906f042ec069e1bc943de38830f895e7a55c362a98ea0f85f28e526befcc7fe8dfe21ac26b395e4c90f87043d6043306cede332b65ac8eac1d56b645f6) 
- [Commercial licensing](http://u.720life.cn/g/17ca4bf30fedad22be68a8d56ffa39824e09f8ea28dbdd5f00cc9481f47848cab5d5b5ba6f111e426617d08ee79245ad)  and [support available](http://u.720life.cn/g/17ca4bf30fedad22be68a8d56ffa398291017b82394a0c1623b14111174c6cfc0b106a500a1a381c5d5acecef10649c1) 

# Licensing

Mongoose OS is Open Source and dual-licensed:

- **Mongoose OS Community Edition** - Apache License Version 2.0
- **Mongoose OS Enterprise Edition** - Commercial License


## Community vs Enterprise Edition

|              |  Community Edition |  Enterprise Edition  |
| -------------| ------------------ | -------------------- |
| License | [Apache 2.0](http://u.720life.cn/g/9504ecfd7de2b26345fb4a78087ff8e39017fae1e889f3875d0fa1b09af9991c7f4e79f930ebc375207fc3a69c8ee78e)  | Commercial - [contact us](http://u.720life.cn/g/17ca4bf30fedad22be68a8d56ffa3982168a051fd43f46fbe0d5eac5a67c8655527c8fcde1252cc26769b13f8aaae721)  |
| Allows to close end-product's source code  | Yes | Yes  |
| Price  | Free | Paid, see [details](http://u.720life.cn/g/17ca4bf30fedad22be68a8d56ffa39820d3650cb49177884538bd02780023ec4659906ca86a903ed90e2602a75642ec8)  |
| Source code & functionality  | [Limited](http://u.720life.cn/g/17ca4bf30fedad22be68a8d56ffa3982b25638f9c551e7718abc9ad62cc1e765f87d15c5bcd62ada931f959737ff7fc6f29e9ad18202d4cdadfb168d237596b6)  | Full |
| Technical support  | Community support via [Forum](http://u.720life.cn/g/e2ac435176eea8bde97ff89a30b84dae71a06facb5db49f3ae98e7777ea7d675)  and [Chat](http://u.720life.cn/g/11e95d0ed8d2826912e12fe1dc3f3421222421fc1bd2ade5d2396c6282e9abbfd933cc8aeda6386b3ca45727ad595c4d)  | Commercial support by Mongoose OS development team, see [details](http://u.720life.cn/g/17ca4bf30fedad22be68a8d56ffa398291017b82394a0c1623b14111174c6cfc0b106a500a1a381c5d5acecef10649c1)  |


# How to contribute

- If you have not done it already, sign [Cesanta CLA](http://u.720life.cn/g/7828605c5820ef8fd66723aec50e04c3779ab15e9ea14e186b84f72d155b8c03) 
and send GitHub pull request.
- Make a Pull Request (PR) against this repo. Please follow
  [Google Coding Style](http://u.720life.cn/g/3ea36103fea3c16ffeedd28e5902a1cc480b0a136f4ffba7cea9eb0bdd9074740eedd4895f404237cf77fbb358d2a4c108b1b4c25fe148354f711cb6ce711a12 
  Send PR to one of the core team member:
   * [pimvanpelt](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e4839274529b0c845146570a8eea0a0b) 
   * [nliviu](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460a4d9af8c8cbe220cc1b27affdcc51b9) 
   * [DrBomb](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d4a45ca4c29d07ab99a8cf82b64c441d) 
   * [kzyapkov](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046392aca66321fd85cc2d9bab25cf6a4d6) 
   * [rojer](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046bce4befd4df8616b487bd4efe3adb87f) 
   * [cpq](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046470882b12286b7c3b526aebfed733395) 
- Responsibilities of the core team members:
   * Review and merge PR submissions
   * Create new repos in the https://github.com/mongoose-os-apps and
   https://github.com/mongoose-os-libs organisations for new app/library
   contributions
   * Create Mongoose OS releases



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)