# GitLab

[![Build status](https://gitlab.com/gitlab-org/gitlab-ce/badges/master/build.svg)](https://gitlab.com/gitlab-org/gitlab-ce/commits/master)
[![Overall test coverage](https://gitlab.com/gitlab-org/gitlab-ce/badges/master/coverage.svg)](https://gitlab.com/gitlab-org/gitlab-ce/pipelines)
[![Code Climate](https://codeclimate.com/github/gitlabhq/gitlabhq.svg)](https://codeclimate.com/github/gitlabhq/gitlabhq)
[![Core Infrastructure Initiative Best Practices](https://bestpractices.coreinfrastructure.org/projects/42/badge)](https://bestpractices.coreinfrastructure.org/projects/42)
[![Gitter](https://badges.gitter.im/gitlabhq/gitlabhq.svg)](https://gitter.im/gitlabhq/gitlabhq?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

## Test coverage

- [![Ruby coverage](https://gitlab.com/gitlab-org/gitlab-ce/badges/master/coverage.svg?job=coverage)](https://gitlab-org.gitlab.io/gitlab-ce/coverage-ruby) Ruby
- [![JavaScript coverage](https://gitlab.com/gitlab-org/gitlab-ce/badges/master/coverage.svg?job=rake+karma)](https://gitlab-org.gitlab.io/gitlab-ce/coverage-javascript) JavaScript

## Canonical source

The canonical source of GitLab Community Edition is [hosted on GitLab.com](http://u.720life.cn/g/bb98acc2cd3ff8b4e4d1deaad062bca23547a837c4db41c31d8b12993d00752d10f67d5d443890510cc06fdbc1c52a39 

## Open source software to collaborate on code

To see how GitLab looks please see the [features page on our website](http://u.720life.cn/g/9c860e2d3718475e314159dbec867d66a84bc62f5cadf92df76bda3c6f02393acc7fb88f930f9be89d605e1e587c86e5 

- Manage Git repositories with fine grained access controls that keep your code secure
- Perform code reviews and enhance collaboration with merge requests
- Complete continuous integration (CI) and CD pipelines to builds, test, and deploy your applications
- Each project can also have an issue tracker, issue board, and a wiki
- Used by more than 100,000 organizations, GitLab is the most popular solution to manage Git repositories on-premises
- Completely free and open source (MIT Expat license)

## Hiring

We're hiring developers, support people, and production engineers all the time, please see our [jobs page](http://u.720life.cn/g/9c860e2d3718475e314159dbec867d666c00073739489a5a2b3fe5b9737ae4d1 

## Editions

There are two editions of GitLab:

- GitLab Community Edition (CE) is available freely under the MIT Expat license.
- GitLab Enterprise Edition (EE) includes [extra features](http://u.720life.cn/g/9c860e2d3718475e314159dbec867d668a3074803715d62eb6eb981087fcf7ef4b3de12ebc3bf67456ffc14462a07703b7cf9261b64592947ebd760a0227f8e3)  that are more useful for organizations with more than 100 users. To use EE and get official support please [become a subscriber](http://u.720life.cn/g/9c860e2d3718475e314159dbec867d668a3074803715d62eb6eb981087fcf7ef7f8164b761f950ad4757bfb33bf9f726 

## Website

On [about.gitlab.com](http://u.720life.cn/g/9c860e2d3718475e314159dbec867d665713f8eb94260b42696059f4c28c7f6e)  you can find more information about:

- [Subscriptions](http://u.720life.cn/g/9c860e2d3718475e314159dbec867d6644161ed13c35e20d63abfad04203e674fb7913a957f2d3d274572b3ac269c62b) 
- [Consultancy](http://u.720life.cn/g/9c860e2d3718475e314159dbec867d668ba444a46934c6722ad2bc0e1717f3d34e28640a93b5dcec9a2feb45b59e1411) 
- [Community](http://u.720life.cn/g/9c860e2d3718475e314159dbec867d662d5ee8e8b9d87688a25cf2ed97b52bfd6814d7bc97dfce44b1335aba4c741fca) 
- [Hosted GitLab.com](http://u.720life.cn/g/9c860e2d3718475e314159dbec867d668f987cd36a92627af4073d911d167b5c8ea34cef717e1bb5fb630dacdec01186)  use GitLab as a free service
- [GitLab Enterprise Edition](http://u.720life.cn/g/9c860e2d3718475e314159dbec867d66a84bc62f5cadf92df76bda3c6f02393a942d7945b5c6ceb8ed3f3430e6d2633e)  with additional features aimed at larger organizations.
- [GitLab CI](http://u.720life.cn/g/9c860e2d3718475e314159dbec867d668f987cd36a92627af4073d911d167b5ccc9d3452a86060818535d61834c5d9b8)  a continuous integration (CI) server that is easy to integrate with GitLab.

## Requirements

Please see the [requirements documentation](doc/install/requirements.md) for system requirements and more information about the supported operating systems.

## Installation

The recommended way to install GitLab is with the [Omnibus packages](http://u.720life.cn/g/9c860e2d3718475e314159dbec867d6620bafe508a56d01383bd763717061949a6ec9fe5a94122303152e5f44f68fcf6)  on our package server.
Compared to an installation from source, this is faster and less error prone.
Just select your operating system, download the respective package (Debian or RPM) and install it using the system's package manager.

There are various other options to install GitLab, please refer to the [installation page on the GitLab website](http://u.720life.cn/g/9c860e2d3718475e314159dbec867d660eb2e70e8aba5757aa9348dc2119a69ded3724053438317c6ca099cd852964ce)  for more information.

You can access a new installation with the login **`root`** and password **`5iveL!fe`**, after login you are required to set a unique password.

## Contributing

GitLab is an open source project and we are very happy to accept community contributions. Please refer to [CONTRIBUTING.md](/CONTRIBUTING.md) for details.

## Install a development environment

To work on GitLab itself, we recommend setting up your development environment with [the GitLab Development Kit](http://u.720life.cn/g/bb98acc2cd3ff8b4e4d1deaad062bca23547a837c4db41c31d8b12993d00752d45d7e0bd6d20bee1d5fa09620b8d99eb492158ed963ea1195635204f35812647 
If you do not use the GitLab Development Kit you need to install and setup all the dependencies yourself, this is a lot of work and error prone.
One small thing you also have to do when installing it yourself is to copy the example development unicorn configuration file:

    cp config/unicorn.rb.example.development config/unicorn.rb

Instructions on how to start GitLab and how to run the tests can be found in the [getting started section of the GitLab Development Kit](http://u.720life.cn/g/bb98acc2cd3ff8b4e4d1deaad062bca23547a837c4db41c31d8b12993d00752d45d7e0bd6d20bee1d5fa09620b8d99eb2a0d3d949af52855fa03460d421d1f26b6749790e554ac3816c2b357355a24d9 

## Software stack

GitLab is a Ruby on Rails application that runs on the following software:

- Ubuntu/Debian/CentOS/RHEL/OpenSUSE
- Ruby (MRI) 2.3
- Git 2.8.4+
- Redis 2.8+
- PostgreSQL (preferred) or MySQL

For more information please see the [architecture documentation](http://u.720life.cn/g/bf8e39dfdcedc32aaa1a3ff4fe053dc597c139dafaecb6908acc8843bb0774663ecb64fba0b12bd10cd04599fe7bb317793e89413e01466ffb2d96d67e1ca145 

## UX design

Please adhere to the [UX Guide](doc/development/ux_guide/index.md) when creating designs and implementing code.

## Third-party applications

There are a lot of [third-party applications integrating with GitLab](http://u.720life.cn/g/9c860e2d3718475e314159dbec867d66ffc82a38da44f11db6a713638e9f157396584f33ef12b442b371d0b6a2e0c09a  These include GUI Git clients, mobile applications and API wrappers for various languages.

## GitLab release cycle

For more information about the release process see the [release documentation](http://u.720life.cn/g/bb98acc2cd3ff8b4e4d1deaad062bca2f7591bc7439e3c5256ff8b472b7fcf0e9efa1028d196b78162d975babbc317c2df4ebe52cf8f2c3c5362390838b63adbaa81ee20ac84c179fc7fa27ffb065624 

## Upgrading

For upgrading information please see our [update page](http://u.720life.cn/g/9c860e2d3718475e314159dbec867d66d4649ca30d990f3899c8081e5fb06cb12b5be1d454c3b3f9d6df163b9d00834d 

## Documentation

All documentation can be found on [docs.gitlab.com/ce/](http://u.720life.cn/g/bf8e39dfdcedc32aaa1a3ff4fe053dc513712c08e0ddb092ba25e16dc3fba858 

## Getting help

Please see [Getting help for GitLab](http://u.720life.cn/g/9c860e2d3718475e314159dbec867d662f32b1e736b90af6b600bd21037fd770237519d1979cfbb03e8e70cc137d0385)  on our website for the many options to get help.

## Is it any good?

[Yes](http://u.720life.cn/g/ba4d8a79018dd07fd6fda7781ab5d426327cb003394fbb5e75316994544d6a2eabc420711cf37c90f52c30497f2b1564) 

## Is it awesome?

Thanks for [asking this question](http://u.720life.cn/g/5ea88169c4a0fbd169233d52478d54fe4bff8ad744945c8bab5c97b27addc135c5028b0ee6f0608578f8da0504fbe7d8a3101b20a478182f72cbbf505d3fe434)  Joshua.
[These people](http://u.720life.cn/g/5ea88169c4a0fbd169233d52478d54fe241123710239bf1c0d7cc946849c99c1)  seem to like it.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)