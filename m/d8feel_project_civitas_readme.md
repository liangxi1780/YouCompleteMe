Civitas
=======

![Main game area](docs/images/civitas3-min.jpg)

Description
===========

Civitas is an empire-building game written in Javascript with the help of the jQuery library.

Features
========

- Over 35 types of buildings, each intertwined in the chain of production.
- Custom climate zone, each with specific buildings.
- Global market, player can trade goods with other settlements.
- Army! Navy! Soldiers! Ships!
- Fame system that allows your city to level up via trades, conquers and special buildings.
- Prestige system that affects diplomacy.
- Each city in the game world is linked via a influence system that needs to be maintained for diplomacy to work.
- Random events that can change your diplomacy status with the other cities, give you coins or
random resources.
- Espionage, subvert cities, destroy buildings, sabotage.
- Ranking screen, where cities get ranked according to their status in the world.
- Declare war, propose alliances and pacts, ask other settlements to join your city, propose cease fire.

![Battles](docs/images/civitas17-min.jpg)

Missing
=======

Check out the [ToDo](TODO.md).

Screenshots
===========

[Intro game](docs/images/civitas1-min.jpg)

[Main game area](docs/images/civitas3-min.jpg)

[Buildings screen](docs/images/civitas6-min.jpg)

[Storage space](docs/images/civitas7-min.jpg)

[Game Menu](docs/images/civitas2-min.jpg)

[World Map](docs/images/civitas15-min.jpg)

[Tavern, heroes and their items](docs/images/civitas4-min.jpg)

[Various buildings, costs, prerequisites](docs/images/civitas5-min.jpg)

[World Market trades](docs/images/civitas8-min.jpg)

[City Council](docs/images/civitas9-min.jpg)

[Diplomacy](docs/images/civitas11-min.jpg), [caravans](docs/images/civitas12-min.jpg), [spies](docs/images/civitas13-min.jpg), [armies and war](docs/images/civitas14-min.jpg)

[Battles](docs/images/civitas16-min.jpg), [more battles](docs/images/civitas17-min.jpg)

![Tavern, heroes and their items](docs/images/civitas4-min.jpg)

Playing
=======

In development, Civitas is using several assets that are copyrighted by Bluebyte, so I cannot redistribute them with the game. You can find a link to the said assets [in this issue](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a11e5c469b606a37458e405379ff104173629b0314b2ca8bcbaca38090c8f7a760ce0acc129d063517fe435b3ca3032e8cea6cde2814003ad7b75646512178ba  All the other game resources are freely distributed under the MIT license, same as the code.


## 1. With Docker

	$ docker build -t civitas .

	$ docker run --name civitas-dev -d -p 10082:80 civitas

And point your browser to `http://localhost:10082`.

## 2. Local

Choose an archive format from the Releases section, download and uncompress it. Point your browser to `index.html`, you don't need a game server to play.

Releases
========

- bleeding edge version - [.zip](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a11e5c469b606a37458e405379ff10414947b1184307ad1b9a7eac57e7d960e80ad862c5c612f52174e7c42ac68dc0a6)  [.tar.gz](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a11e5c469b606a37458e405379ff10414947b1184307ad1b9a7eac57e7d960e813891edc1e04d59012f024cb545e3a0a) 
- 0.2 (April 30, 2017) - [.zip](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a11e5c469b606a37458e405379ff1041e951d97dae14d9b71e98cb931323948103dc5ee78f144d55716f2fc08d196192)  [.tar.gz](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a11e5c469b606a37458e405379ff1041e951d97dae14d9b71e98cb9313239481abcf2f46d53a6b42b05a7a1cfedbacac) 
- 0.1 (January 20, 2017) - [.zip](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a11e5c469b606a37458e405379ff1041e951d97dae14d9b71e98cb93132394815d3969fe4c68a711d800f2b2cd4fda44)  [.tar.gz](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a11e5c469b606a37458e405379ff1041e951d97dae14d9b71e98cb93132394815ebd22752fa73fb837b2614b1dd004a3) 

License
=======

Civitas is written by sizeof(cat)   and distributed under the [MIT license](LICENSE).

Contributing
============

Pull requests are always welcome!

I am always thrilled to receive pull requests, and do my best to process them as fast as possible. Not sure if that typo is worth a pull request? Do it! I will probably appreciate it.

If your pull request is not accepted on the first try, don't be discouraged! If there's a problem with the implementation, hopefully you received feedback on what to improve.

Always sign your commits and make sure you read the [coding style](CODING-STYLE.md).

![World Map and City Council](docs/images/civitas10-min.jpg)

Source code
===========

Civitas is written using Javascript, has ~15000 lines of code, ~250Kb minified and can be [downloaded from GitHub.com](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a11e5c469b606a37458e405379ff10414947b1184307ad1b9a7eac57e7d960e80ad862c5c612f52174e7c42ac68dc0a6)  or by using git to clone the repository:

`git clone git@github.com/sizeofcat/civitas.git`

Dependencies
============

- [jQuery 3.2.1](http://u.720life.cn/g/0a8164b4e54fe9c39d5074c1f90b955107edd69253c714b7b4b0ab058cef2fcb) 
- [jQuery UI 1.11.2](http://u.720life.cn/g/fdde3bf3cb5ff3ec8935c77ffc7dd1ee88f16a85f78060c5ad7dd1dac3b134e1) 
- [jQuery Tipsy 1.0.0a](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d1a805361f12a1efdb14667abf39af3c) 
- [jQuery scrollTo 1.4.14](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046eeae83019f096ecf8690186f99d9696179d1338abde5fbb380811d58f06f1934) 
- [CryptoJS 3.1.9](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a9ab0664b9a5fe463bb331c23febae906d7c0ee6f5e9cbcb57dffc95c94e6234) 

Thanks
======

The `music/track1.mp3` song is named 'Glandula Pinealis' by Shatifax.


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)