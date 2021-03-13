# chinese-poetry: 最全中文诗歌古典文集数据库.

[![Build Status](https://travis-ci.org/chinese-poetry/chinese-poetry.svg?branch=master)](https://travis-ci.org/chinese-poetry/chinese-poetry)
[![License](http://img.shields.io/badge/license-mit-blue.svg?style=flat-square)](https://github.com/jackeyGao/chinese-poetry/blob/master/LICENSE)
[![](https://img.shields.io/github/contributors/chinese-poetry/chinese-poetry.svg)](https://github.com/chinese-poetry/chinese-poetry/graphs/contributors)

[中文诗歌主页]https://shici.store)是一个基于浏览器的诗词网站， 包含唐诗三百首、宋词三百首等文集.

最全的中华古典文集数据库, 包含5.5万首唐诗、26万首宋诗和2.1万首宋词. 唐宋两朝近1.4万古诗人, 和两宋时期1.5K词人. 数据来源于互联网. 

**为什么要做这个仓库?** 古诗是中华民族乃至全世界的瑰宝, 我们应该传承下去, 虽然有古典文集, 但大多数人并没有拥有这些书籍. 从某种意义上来说, 这些庞大的文集离我们是有一定距离的。而电子版方便拷贝, 所以此开源数据库诞生了. 你可以用此数据做任何有益的事情， 甚至我也可以帮助你.

古诗采集没有记录过程， 因为古诗数据庞大，目标网站有限制, 采集过程经常中断超过了一个星期.2017年新加入全宋词, [全宋词爬取过程及数据分析](http://u.720life.cn/g/7de18dc4c2de7673a272a1e9f49d3063d80ec1195dd5d668291561563e979894a16a3b60973b413e18c973e9b04be873 


## 数据分析

一些简单的高频分析

|唐诗高频词|唐诗作者作品榜|
| :---: | :---: |
| ![唐诗高频词](https://raw.githubusercontent.com/jackeygao/chinese-poetry/master/images/tang_text_topK.png "唐诗高频词")| ![唐诗作者作品榜](https://raw.githubusercontent.com/jackeygao/chinese-poetry/master/images/tang_author_topK.png "唐诗作者作品榜")|
|宋诗高频词|宋诗作者作品榜|
| ![宋诗高频词](https://raw.githubusercontent.com/jackeygao/chinese-poetry/master/images/song_text_topK.png "宋诗高频词" )| ![宋诗作者作品榜](https://raw.githubusercontent.com/jackeygao/chinese-poetry/master/images/song_author_topK.png "宋诗作者作品榜")|
|宋词高频词|宋词作者作品榜|
| ![宋词高频词](https://raw.githubusercontent.com/jackeygao/chinese-poetry/master/images/ci_words_topK.png "宋词高频词")  |![宋词作者作品榜](https://raw.githubusercontent.com/jackeygao/chinese-poetry/master/images/ci_author_topK.png "宋词作者作品榜") |

|两宋喜欢的词牌名|
| :---: |
|![两宋喜欢的词牌名](https://raw.githubusercontent.com/jackeygao/chinese-poetry/master/images/ci_rhythmic_topK.png)|

## 数据集合

- 全唐诗 [json](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460c8a4fcdbf82382184ad588680f84fa47399779aab8e80f655511f9bebc91cf1a2e6948a399f699d2cd1b6d53b681e31fbf55fd88e2951596fc25980c3fa728e) 
- 全宋诗 [json](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460c8a4fcdbf82382184ad588680f84fa47399779aab8e80f655511f9bebc91cf1a2e6948a399f699d2cd1b6d53b681e31fbf55fd88e2951596fc25980c3fa728e) 
- 全宋词 [ci](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460c8a4fcdbf82382184ad588680f84fa47399779aab8e80f655511f9bebc91cf1506fcf65dfc50aa6d9bc3178b8241f74) 
- 五代·花间集 [wudai](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460c8a4fcdbf82382184ad588680f84fa47399779aab8e80f655511f9bebc91cf13a003fcdc39143e4d3246e502d0b766b7c09bf753e21897c18fefa00ef1a6176ef8d1125a4271510e5d98ed94ccee0a6) 
- 五代·南唐二主词 [wudai](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460c8a4fcdbf82382184ad588680f84fa47399779aab8e80f655511f9bebc91cf13a003fcdc39143e4d3246e502d0b766be83469b5bb6525d3fe1a0b4c5db034063fc3ec5a8ef402fe278d3609140dfe12cdce1551f37bfc0a76fdc428dc171ce4) 
- 论语 [lunyu](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460c8a4fcdbf82382184ad588680f84fa47399779aab8e80f655511f9bebc91cf1e7dc1da036d2b7121e6ed323a350e07d853d5dcd86c9e2a5b152741b7417aae8) 
- 诗经 [shijing](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460c8a4fcdbf82382184ad588680f84fa47399779aab8e80f655511f9bebc91cf10d70c861ddb71af5a623292ee0c4ac10bba620df891d3bef952a9514b67b931a) 
- 幽梦影 [youmengying](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460c8a4fcdbf82382184ad588680f84fa47399779aab8e80f655511f9bebc91cf10b1b04a54faaf75366118a0d88e2b7dceeb14d07da530eb8560182c477f8f209) 
- 四书五经 [sishuwujing](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460c8a4fcdbf82382184ad588680f84fa47399779aab8e80f655511f9bebc91cf1e345002b6a3409ab22574cd4f78c23b9a7353d21741a13ef7eae6d6a19ce5262) 

**待补充**

- 清代诗词 
- 元曲

## 案例展示

- [animalize](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464cab5cf4b66b24f0179b53f8c4f43aef)  **/** [QuanTangshi](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046210ea9e04931bd93049c9f0a8d883cbc0fd6c7374bef927733e0ef2726de2df6)   *离线全唐诗 Android*
- [justdark](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469f3336c7eb4c5a440745f87e773b2514)  **/** [pytorch-poetry-gen](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304646efdf76deaf588de1e4f4a51c60bc94362405e88d336b773f5532c0023e96d9)   *a char-RNN based on pytorch*
- [Clover27](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d6735aa2b413f0e06a1ccf22d9976ce1)  **/** [ancient-Chinese-poem-generator](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465b7e06787059f910f5aaae302bcec044ee7205c15aa34c46f9dd4ba1b567ea22bf4bf2a6e6e257fdfa26141f8a49a088)   *Ancient-Chinese-Poem-Generator*
- [chinese-poetry](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460c8a4fcdbf82382184ad588680f84fa467087fecd759189da97e5ac13544ae39)  **/** [poetry-calendar](http://u.720life.cn/g/316a46458c589e9c2742c868826abc6f8a38060ab42977bd3e853c0b49dda27938bd98a9364c2748fee5c4b837ccea25)   *诗词周历*
- [chenyuntc](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f0245a7edc8aaee05125de2e1e1ae023)  **/** [pytorch-book]https://github.com/chenyuntc/pytorch-book/blob/master/chapter9-神经网络写诗CharRNN/ *简体唐诗生成(char-RNN), 可生成藏头诗,自定义诗歌意境,前缀等*
- [okcy1016](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460b1ea5d17fcff26f97b516fbdacf2b30)  **/** [poetry-desktop](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046802daf78b7412ee0a4aea2ed5d604eec0c8a720b84af13f75fd762a2ece33523)  *诗词桌面*
- [huangjianke](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462c8c2955722735e9b6da10fc79cf3268)  **/** [weapp-poem](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304683377be1610338d7e01d0e9cc47ec5cad1adf4b8167556f823e95461ab4e2660)  *诗词墨客 小程序版*


## 贡献&讨论

 
 
 


提交PR或者通过issue讨论来优化完善此数据库, 你也可以联系我的邮箱 gaojunqi@outlook.com

创建和维护`chinese-poetry`需要花费很多的时间和资源. 如果此数据库对您有很大的帮助, 请酌情考虑[打赏作者](http://u.720life.cn/g/fe7064e7eada543391e1b189c45f3da189e547ec524f025ac17be470261154de126f49d852654a75df8ec5ad35f022ae 

 


## License

[MIT](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460c8a4fcdbf82382184ad588680f84fa47399779aab8e80f655511f9bebc91cf1756f129b6d1bae0ecb553ebbaa7dd7c5ef5de975be412257f704a42f58c9a02a)  许可证. 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)