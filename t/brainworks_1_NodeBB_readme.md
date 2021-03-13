#  

[![Build Status](https://travis-ci.org/NodeBB/NodeBB.svg?branch=master)](https://travis-ci.org/NodeBB/NodeBB)
[![Coverage Status](https://coveralls.io/repos/github/NodeBB/NodeBB/badge.svg?branch=master)](https://coveralls.io/github/NodeBB/NodeBB?branch=master)
[![Dependency Status](https://david-dm.org/nodebb/nodebb.svg?path=install)](https://david-dm.org/nodebb/nodebb?path=install)
[![Code Climate](https://codeclimate.com/github/NodeBB/NodeBB/badges/gpa.svg)](https://codeclimate.com/github/NodeBB/NodeBB)

[**NodeBB Forum Software**](http://u.720life.cn/g/b746f0d7093fd9016eedcc8040d22156afc28c82e69868c19b312db4b9c9b175)  is powered by Node.js and built on either a Redis or MongoDB database. It utilizes web sockets for instant interactions and real-time notifications. NodeBB has many modern features out of the box such as social network integration and streaming discussions, while still making sure to be compatible with older browsers.

Additional functionality is enabled through the use of third-party plugins.

* [Demo & Meta Discussion](http://u.720life.cn/g/7132cf8bf192881e782e683bce80a19d7144fd5bd0ae32e81c81c10deb8e8707) 
* [Documentation & Installation Instructions](http://u.720life.cn/g/0bf22c506b9f749128bb8225d899231468c4280673016e20b855f18420e2d1fd) 
* [Help translate NodeBB](http://u.720life.cn/g/187a633cc93501bb91ac0a975d230ba5b687eb929cb4b0ea88d3e8de82a8adb617ad09072c22de1e7835186f6fb467d8) 
* [NodeBB Blog](http://u.720life.cn/g/d1e66e6ed3af3fff0c6def4187597921bbd43ddf274994e20006d0dbd97dde4d) 
* [Premium Hosting for NodeBB](http://u.720life.cn/g/6ad85a6f868cdd66756a9a787a10cbdf92c1e1f9f4bc8b979d1777920d2617f8  "NodeBB")
* [Follow us on Twitter](http://u.720life.cn/g/55c28302c8d6b2a51d2f0facda80b1a8bca7eb47e3fef9f35df355f1f610f686  "NodeBB Twitter")
* [Like us on Facebook](http://u.720life.cn/g/cac60526a5b26e496dc98eb4bac45b69951e18dc2c89e1ca9ffbda25d2d4f0ce  "NodeBB Facebook")

## Screenshots

NodeBB's theming engine is highly flexible and does not restrict your design choices. Check out some themed installs in these screenshots below:

[![](http://i.imgur.com/VCoOFyqb.png)](http://i.imgur.com/VCoOFyq.png)
[![](http://i.imgur.com/FLOUuIqb.png)](http://i.imgur.com/FLOUuIq.png)
[![](http://i.imgur.com/Ud1LrfIb.png)](http://i.imgur.com/Ud1LrfI.png)
[![](http://i.imgur.com/h6yZ66sb.png)](http://i.imgur.com/h6yZ66s.png)
[![](http://i.imgur.com/o90kVPib.png)](http://i.imgur.com/o90kVPi.png)
[![](http://i.imgur.com/AaRRrU2b.png)](http://i.imgur.com/AaRRrU2.png)
[![](http://i.imgur.com/LmHtPhob.png)](http://i.imgur.com/LmHtPho.png)
[![](http://i.imgur.com/paiJPJkb.jpg)](http://i.imgur.com/paiJPJk.jpg)

Our minimalist "Persona" theme gets you going right away, no coding experience required.

[![](http://i.imgur.com/HwNEXGu.png)](http://i.imgur.com/HwNEXGu.png)
[![](http://i.imgur.com/II1byYs.png)](http://i.imgur.com/II1byYs.png)



## How can I follow along/contribute?

* If you are a developer, feel free to check out the source and submit pull requests. We also have a wide array of [plugins](http://u.720life.cn/g/7132cf8bf192881e782e683bce80a19d770ea0f286e93095f2e7546fca3bf4361c1aaf49c0935a9bea70d4327598bf1ec37c33d7066435aab8a144a9ee5a1426)  which would be a great starting point for learning the codebase.
* If you are a designer, [NodeBB needs themes](http://u.720life.cn/g/7132cf8bf192881e782e683bce80a19d770ea0f286e93095f2e7546fca3bf436ccece3a92d59f4c8d609237039b3d65779198ab7a167fcd75c89c1e8bd5d0808  NodeBB's theming system allows extension of the base templates as well as styling via LESS or CSS. NodeBB's base theme utilizes [Bootstrap 3](http://u.720life.cn/g/e23be2821e5181a1a46a005bc6e93d9dc1c8dad0ef41593aa593e12a30fc455b)  but themes can choose to use a different framework altogether.
* If you know languages other than English you can help us translate NodeBB. We use [Transifex](http://u.720life.cn/g/187a633cc93501bb91ac0a975d230ba5b687eb929cb4b0ea88d3e8de82a8adb617ad09072c22de1e7835186f6fb467d8)  for internationalization.
* Please don't forget to **like**, **follow**, and **star our repo**! Join our growing [community](http://u.720life.cn/g/7132cf8bf192881e782e683bce80a19d7144fd5bd0ae32e81c81c10deb8e8707)  to keep up to date with the latest NodeBB development.

## Requirements

NodeBB requires the following software to be installed:

* A version of Node.js at least 8 or greater ([installation/upgrade instructions](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467b3900daee26c58ca60df61f7414599c750558a8a209bacd1ce1f11ebc19f23e) 
* Redis, version 2.8.9 or greater **or** MongoDB, version 2.6 or greater
* nginx, version 1.3.13 or greater (**only if** intending to use nginx to proxy requests to a NodeBB)

## Installation

[Please refer to platform-specific installation documentation](http://u.720life.cn/g/7b1dd46fb087802e93209d784dc17ba6d5f7e00a5dda900b94b46b16bd248f5b0cf4d48097126b60b8928a25a8772ae6) 

## Securing NodeBB

It is important to ensure that your NodeBB and database servers are secured. Bear these points in mind:

1. While some distributions set up Redis with a more restrictive configuration, Redis by default listens to all interfaces, which is especially dangerous when a server is open to the public. Some suggestions:
    * Set `bind_address` to `127.0.0.1` so as to restrict access  to the local machine only
    * Use `requirepass` to secure Redis behind a password (preferably a long one)
    * Familiarise yourself with [Redis Security](http://u.720life.cn/g/f4afcc2808cb8f2d18b502aeb587da1986a4549b5352d7a94700d11112debb58) 
2. Use `iptables` to secure your server from unintended open ports. In Ubuntu, `ufw` provides a friendlier interface to working with `iptables`.
    * e.g. If your NodeBB is proxied, no ports should be open except 80 (and possibly 22, for SSH access)

## Upgrading NodeBB

Detailed upgrade instructions are listed in [Upgrading NodeBB](http://u.720life.cn/g/7b1dd46fb087802e93209d784dc17ba68bacdf986bce687300d607bcd7f3a20b50537de10f54fd8aff72915122d6f79c) 

## License

NodeBB is licensed under the **GNU General Public License v3 (GPL-3)** (http://u.720life.cn/g/0faf03d8167674bee364b61e9b7d6858de092c730901b66e45ef02da10ec874d077884d917824d3c1bdee2485aa4fdcf 

Interested in a sublicense agreement for use of NodeBB in a non-free/restrictive environment? Contact us at sales@nodebb.org.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)