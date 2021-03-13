AppleBacklightFixup
===================

Lilu plugin for enabling support for backlight using RehabMan's patches

### Downloads

RehabMan pre-built is on bitbucket: https://bitbucket.org/RehabMan/applebacklightfixup/downloads/

### Features
- No need Clover patch and `AppleBacklightInjector.kext`
- Work in Recovery and Installation

### Instruction
- Install this kext using your favorite method (Clover, /L/E, etc.) and put `SSDT-PNLF.aml` to `/EFI/CLOVER/ACPI/patched`

### Boot-args
- `-applbkloff` disables kext loading
- `-applbkldbg` turns on debugging output
- `-applbklbeta` enables loading on unsupported osx

### Downloads
Available on the [releases](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046db86701fcd5ff765aaae78b8bc353844b5ab88ce3029d8686ec2b5ee0f2eb6fe79ef0142035ef803508b0677e4c5774d)  page.

#### Credits
- [Apple](http://u.720life.cn/g/391435ab90081af20739ca58fedafecab222142164016e0547ba847e79d4affd)  for macOS  
- [vit9696](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464d2c0f7fd3d4971fb1ede1da0452081e)  for [Lilu](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468b862bf1404b00f06951f5a0ddb433a5569b262cd10cf1e763a92f46788a5a65) 
- [RehabMan](http://u.720life.cn/g/769799622d2b5ae55d616089cd1241a3ed47393efccd9399b58f7cc5db10958def612b4b8a82145e4cbb115aeacca30fd8a21c3ae3051cc4621a144a6f0eceea)  for [the patch](http://u.720life.cn/g/769799622d2b5ae55d616089cd1241a3741c12b436ea2a780f21baf7e9348b123b0a126a5d0b44825b40bd6bc1b59c5dabeddc3c3d2f1907f5afcb02415949b8f5520d1abcd2533f2b93f654b8d0e316d1bb7ac4e27abd766feddc12bf0332193b0128a3452c18a33c6028afede6088a) 
- [hieplpvip](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463d184e81d471348b16ec2c0b4bc1271f)  for writing the software and maintaining it



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)