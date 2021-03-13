
# EOSIO - The Most Powerful Infrastructure for Decentralized Applications

[![Build status](https://badge.buildkite.com/370fe5c79410f7d695e4e34c500b4e86e3ac021c6b1f739e20.svg?branch=master)](https://buildkite.com/EOSIO/eosio)

Welcome to the EOSIO source code repository! This software enables businesses to rapidly build and deploy high-performance and high-security blockchain-based applications.

Some of the groundbreaking features of EOSIO include:

1. Free Rate Limited Transactions
1. Low Latency Block confirmation (0.5 seconds)
1. Low-overhead Byzantine Fault Tolerant Finality
1. Designed for optional high-overhead, low-latency BFT finality
1. Smart contract platform powered by WebAssembly
1. Designed for Sparse Header Light Client Validation
1. Scheduled Recurring Transactions
1. Time Delay Security
1. Hierarchical Role Based Permissions
1. Support for Biometric Hardware Secured Keys (e.g. Apple Secure Enclave)
1. Designed for Parallel Execution of Context Free Validation Logic
1. Designed for Inter Blockchain Communication

EOSIO is released under the open source MIT license and is offered “AS IS” without warranty of any kind, express or implied. Any security provided by the EOSIO software depends in part on how it is used, configured, and deployed. EOSIO is built upon many third-party libraries such as WABT (Apache License) and WAVM (BSD 3-clause) which are also provided “AS IS” without warranty of any kind. Without limiting the generality of the foregoing, Block.one makes no representation or guarantee that EOSIO or any third-party libraries will perform as intended or will be free of errors, bugs or faulty code. Both may fail in large or small ways that could completely or partially limit functionality or compromise computer systems. If you use or implement EOSIO, you do so at your own risk. In no event will Block.one be liable to any party for any damages whatsoever, even if it had been advised of the possibility of damage.  

Block.one is neither launching nor operating any initial public blockchains based upon the EOSIO software. This release refers only to version 1.0 of our open source software. We caution those who wish to use blockchains built on EOSIO to carefully vet the companies and organizations launching blockchains based on EOSIO before disclosing any private keys to their derivative software.

There is no public testnet running currently.

---

**If you used our build scripts to install eosio, [please be sure to uninstall](#build-script-uninstall) before using our packages.**

---

#### Mac OS X Brew Install
```sh
$ brew tap eosio/eosio
$ brew install eosio
```
#### Mac OS X Brew Uninstall
```sh
$ brew remove eosio
```

#### Ubuntu 18.04 Package Install
```sh
$ wget https://github.com/eosio/eos/releases/download/v1.8.1/eosio_1.8.1-1-ubuntu-18.04_amd64.deb
$ sudo apt install ./eosio_1.8.1-1-ubuntu-18.04_amd64.deb
```
#### Ubuntu 16.04 Package Install
```sh
$ wget https://github.com/eosio/eos/releases/download/v1.8.1/eosio_1.8.1-1-ubuntu-16.04_amd64.deb
$ sudo apt install ./eosio_1.8.1-1-ubuntu-16.04_amd64.deb
```
#### Ubuntu Package Uninstall
```sh
$ sudo apt remove eosio
```
#### Centos RPM Package Install
```sh
$ wget https://github.com/eosio/eos/releases/download/v1.8.1/eosio-1.8.1-1.el7.x86_64.rpm
$ sudo yum install ./eosio-1.8.1-1.el7.x86_64.rpm
```
#### Centos RPM Package Uninstall
```sh
$ sudo yum remove eosio
```

#### Build Script Uninstall

If you have previously installed EOSIO using build scripts, you can execute `eosio_uninstall.sh` to uninstall.
- Passing `-y` will answer yes to all prompts (does not remove data directories)
- Passing `-f` will remove data directories (be very careful with this)
- Passing in `-i` allows you to specify where your eosio installation is located

## Supported Operating Systems
EOSIO currently supports the following operating systems:  
1. Amazon Linux 2
2. CentOS 7
3. Ubuntu 16.04
4. Ubuntu 18.04
5. MacOS 10.14 (Mojave)

## Resources
1. [Website](http://u.720life.cn/g/0ef657bf7e0bc0b2203e39a999dc8a6f) 
1. [Blog](http://u.720life.cn/g/ce19288caac4b59057ec565c52ba1b36ff685215c3d299ea38ea69096599972c) 
1. [Developer Portal](http://u.720life.cn/g/a69e8f5dba5b4106ccc3875c547b1484625ea3937b73e66dbffe8d98caff1fce) 
1. [StackExchange for Q&A](http://u.720life.cn/g/d5a7751c676d02404c76978be09926e243462a9b8242effbb78d8c45c8ba95a2) 
1. [Community Telegram Group](http://u.720life.cn/g/8b4beb361516fe4e666235cce7acd947977a45f949fb80f3dca655185b2fe6a7) 
1. [Developer Telegram Group](http://u.720life.cn/g/1da30d8db3607fa9f1133fa65e71caa63152bc9e732991ba30b6c4aceb5efffa5389f1486631512effd4934c9f452018) 
1. [White Paper](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046adb17191900aae0e2e65def3ab04981b93050dca43b1deb9616556ee3a6d27db23cb8aea52fadde94db655609caf80b2cc83edbeb9b45cf97acebe96058f26b2) 
1. [Roadmap](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046adb17191900aae0e2e65def3ab04981b93050dca43b1deb9616556ee3a6d27db213249a71075185c32b50cba35e17217) 

  
## Getting Started
Instructions detailing the process of getting the software, building it, running a simple test network that produces blocks, account creation and uploading a sample contract to the blockchain can be found in [Getting Started](http://u.720life.cn/g/a69e8f5dba5b4106ccc3875c547b1484cc6ee0ebaf8744d4f52717ef1e1764b654e83bddbabf00ba42f8333ff91d763f)  on the [EOSIO Developer Portal](http://u.720life.cn/g/a69e8f5dba5b4106ccc3875c547b148487c81f4bef755a92d991c2bf32f31505 

## Contributing

[Contributing Guide](./CONTRIBUTING.md)

[Code of Conduct](./CONTRIBUTING.md#conduct)

## License

[MIT](./LICENSE)

## Important

See LICENSE for copyright and license terms.  Block.one makes its contribution on a voluntary basis as a member of the EOSIO community and is not responsible for ensuring the overall performance of the software or any related applications.  We make no representation, warranty, guarantee or undertaking in respect of the software or any related documentation, whether expressed or implied, including but not limited to the warranties or merchantability, fitness for a particular purpose and noninfringement. In no event shall we be liable for any claim, damages or other liability, whether in an action of contract, tort or otherwise, arising from, out of or in connection with the software or documentation or the use or other dealings in the software or documentation.  Any test results or performance figures are indicative and will not reflect performance under all conditions.  Any reference to any third party or third-party product, service or other resource is not an endorsement or recommendation by Block.one.  We are not responsible, and disclaim any and all responsibility and liability, for your use of or reliance on any of these resources. Third-party resources may be updated, changed or terminated at any time, so the information here may be out of date or inaccurate.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)