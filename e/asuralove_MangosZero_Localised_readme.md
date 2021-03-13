# MangosZero Localisation Project

This is a culmination of over a years work to generate a full localisation process and files for Mangos.

### Features

Rather than an all or nothing system for localisation, the languages can be chosen individually

Current support will include the following:
* Korean
* French
* German
* Spanish
* Spanish (Sourth American)
* Chinese
* Taiwanese
* Russian

Plus the following, even though the client does not natively support it (See "Using the Translated Locale on a different language client than the Locale" below):
* Italian

### How to use it

Eventually it will become part of the main install database scripts, but for now it's a case of manually applying the updates.

1) run the following SQL script:

    `1_LocaleTablePrepare.sql`

This will populate the localised tables with empty entries ready for the language pack.

2) Import the language pack you want from \Translations\ 

The language pack currently consists of 6 files:

     _Creature.sql
     _Gameobject.sql
     _GossipMenu.sql
     _Items.sql
     _PageText.sql
     _Quest.sql


The 6 files ending in `_missing.sql` are entries that need to be translated.

### Using the Translated Locale on a different language client than the Locale

1) If you wish to run the localised text in a different language client i.e. Italian Locale using an English client, run these scripts in order:

    `1_LocaleTablePrepare.sql`
    `2_Add_NewLocalisationFields.sql`
    `3_InitialSaveEnglish.sql`

2) Then Import the language pack you want from \Translations\ 

The language pack currently consists of 6 files:

     _Creature.sql
     _Gameobject.sql
     _GossipMenu.sql
     _Items.sql
     _PageText.sql
     _Quest.sql
    
3) Then run the remaining script
    `A_replace_BaseEnglish_with_ .sql`

3a) Should you want to revent the changes, just run:
    `B_replace_BaseEnglish_with_English.sql`

**Official Websites**
----

* [**Official MaNGOS Site**](http://u.720life.cn/g/f18b9182108aa0821f46732170354045141636c3f86d0780fb8e8d91b474b4bd)   
* [**Official MaNGOS Community Forum**](http://u.720life.cn/g/a96299286e8d164d88d108ed4e2a627591acacd3ce9b033de8cf7c7d8ab398bdb9f72994751f0242409638bd62bcfb4b)   

**Main Wiki**
----
For browsing the Wiki, it is located at the following location:

* [**Wiki Home**](http://u.720life.cn/g/009baf6fd125444d1537353f1026a12db91122edc430c44c0656c1dc9273c942)   

---
Proudly brought to you by:
 
[![getMaNGOS](https://www.getmangos.eu/!assets_mangos/logo.png)](http://getmangos.eu)

We would like to acknowledge the work of the following groups who have helped source some of the translations used:

* GMDB (German Mangos Database project)
* YTDB (non-mangos compatible Database)
* MA-WOWEE (Spanish database project)
* UDBFR (French Database Project)

Not to mention a number of people from the Mangos Community who have submitted corrections and updates:

* mpfans
* talendrys
* salja
* AzoG
* D3thw0lf
* bdebaere



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)