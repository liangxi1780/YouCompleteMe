# ![logo][] PowerShell

Welcome to the PowerShell GitHub Community!
PowerShell Core is a cross-platform (Windows, Linux, and macOS) automation and configuration tool/framework that works well with your existing tools and is optimized
for dealing with structured data (e.g. JSON, CSV, XML, etc.), REST APIs, and object models.
It includes a command-line shell, an associated scripting language and a framework for processing cmdlets.

[logo]: https://raw.githubusercontent.com/PowerShell/PowerShell/master/assets/ps_black_64.svg?sanitize=true

## Windows PowerShell vs. PowerShell Core

Although this repository started as a fork of the Windows PowerShell code base, changes made in this repository do not make their way back to Windows PowerShell 5.1 automatically.
This also means that [issues tracked here][issues] are only for PowerShell Core 6 and higher.
Windows PowerShell specific issues should be opened on [UserVoice][].

[issues]: https://github.com/PowerShell/PowerShell/issues
[UserVoice]: https://windowsserver.uservoice.com/forums/301869-powershell

## New to PowerShell?

If you are new to PowerShell and would like to learn more, we recommend reviewing the [getting started][] documentation.

[getting started]: https://github.com/PowerShell/PowerShell/tree/master/docs/learning-powershell

## Get PowerShell

You can download and install a PowerShell package for any of the following platforms.

| Supported Platform                         | Download (LTS)          | Downloads (stable)      | Downloads (preview)   | How to Install                |
| -------------------------------------------| ------------------------| ------------------------| ----------------------| ------------------------------|
| [Windows (x64)][corefx-win]                | [.msi][rl-windows-64]   | [.msi][rl-windows-64]   | [.msi][pv-windows-64] | [Instructions][in-windows]    |
| [Windows (x86)][corefx-win]                | [.msi][rl-windows-86]   | [.msi][rl-windows-86]   | [.msi][pv-windows-86] | [Instructions][in-windows]    |
| [Ubuntu 18.04][corefx-linux]               | [.deb][lts-ubuntu18]    | [.deb][rl-ubuntu18]     | [.deb][pv-ubuntu18]   | [Instructions][in-ubuntu18]   |
| [Ubuntu 16.04][corefx-linux]               | [.deb][lts-ubuntu16]    | [.deb][rl-ubuntu16]     | [.deb][pv-ubuntu16]   | [Instructions][in-ubuntu16]   |
| [Debian 9][corefx-linux]                   | [.deb][lts-debian9]     | [.deb][rl-debian9]      | [.deb][pv-debian9]    | [Instructions][in-deb9]       |
| [Debian 10][corefx-linux]                  | [.deb][lts-debian10]    | [.deb][rl-debian10]     | [.deb][pv-debian10]   |                               |
| [CentOS 7][corefx-linux]                   | [.rpm][lts-centos]      | [.rpm][rl-centos]       | [.rpm][pv-centos]     | [Instructions][in-centos]     |
| [CentOS 8][corefx-linux]                   | [.rpm][lts-centos8]     | [.rpm][rl-centos8]      | [.rpm][pv-centos8]    |                               |
| [Red Hat Enterprise Linux 7][corefx-linux] | [.rpm][lts-centos]      | [.rpm][rl-centos]       | [.rpm][pv-centos]     | [Instructions][in-rhel7]      |
| [openSUSE 42.3][corefx-linux]              | [.rpm][lts-centos]      | [.rpm][rl-centos]       | [.rpm][pv-centos]     | [Instructions][in-opensuse]   |
| [Fedora 30][corefx-linux]                  | [.rpm][lts-centos]      | [.rpm][rl-centos]       | [.rpm][pv-centos]     | [Instructions][in-fedora]     |
| [macOS 10.13+][corefx-macos]               | [.pkg][lts-macos]       | [.pkg][rl-macos]        | [.pkg][pv-macos]      | [Instructions][in-macos]      |
| Docker                                     |                         |                         |                       | [Instructions][in-docker]     |

You can download and install a PowerShell package for any of the following platforms, **which are supported by the community.**

| Platform                 | Downloads (stable)      | Downloads (preview)           | How to Install                |
| -------------------------| ------------------------| ----------------------------- | ------------------------------|
| Arch Linux               |                         |                               | [Instructions][in-archlinux]  |
| Kali Linux               | [.deb][rl-ubuntu16]     | [.deb][pv-ubuntu16]           | [Instructions][in-kali]       |
| Many Linux distributions | [Snapcraft][rl-snap]    | [Snapcraft][pv-snap]          |                               |

You can also download the PowerShell binary archives for Windows, macOS and Linux.

| Platform                            | Downloads (stable)                               | Downloads (preview)                             | How to Install                                 |
| ------------------------------------| ------------------------------------------------ | ------------------------------------------------| -----------------------------------------------|
| Windows                             | [32-bit][rl-winx86-zip]/[64-bit][rl-winx64-zip]  | [32-bit][pv-winx86-zip]/[64-bit][pv-winx64-zip] | [Instructions][in-windows-zip]                 |
| macOS                               | [64-bit][rl-macos-tar]                           | [64-bit][pv-macos-tar]                          | [Instructions][in-tar-macos]                   |
| Linux                               | [64-bit][rl-linux-tar]                           | [64-bit][pv-linux-tar]                          | [Instructions][in-tar-linux]                   |
| Windows (arm) **Experimental**      | [32-bit][rl-winarm]/[64-bit][rl-winarm64]        | [32-bit][pv-winarm]/[64-bit][pv-winarm64]       | [Instructions][in-arm]                         |
| Raspbian (Stretch) **Experimental** | [32-bit][rl-arm32]/[64-bit][rl-arm64]    | [32-bit][pv-arm32]/[64-bit][pv-arm64]           | [Instructions][in-raspbian]                    |

[lts-ubuntu18]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/powershell-lts_7.0.0-1.ubuntu.18.04_amd64.deb
[lts-ubuntu16]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/powershell-lts_7.0.0-1.ubuntu.16.04_amd64.deb
[lts-debian9]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/powershell-lts_7.0.0-1.debian.9_amd64.deb
[lts-debian10]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/powershell-lts_7.0.0-1.debian.10_amd64.deb
[lts-centos]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/powershell-lts-7.0.0-1.rhel.7.x86_64.rpm
[lts-centos8]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/powershell-lts-7.0.0-1.centos.8.x86_64.rpm
[lts-macos]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/powershell-lts-7.0.0-osx-x64.pkg

[rl-windows-64]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/PowerShell-7.0.0-win-x64.msi
[rl-windows-86]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/PowerShell-7.0.0-win-x86.msi
[rl-ubuntu18]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/powershell_7.0.0-1.ubuntu.18.04_amd64.deb
[rl-ubuntu16]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/powershell_7.0.0-1.ubuntu.16.04_amd64.deb
[rl-debian9]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/powershell_7.0.0-1.debian.9_amd64.deb
[rl-debian10]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/powershell_7.0.0-1.debian.10_amd64.deb
[rl-centos]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/powershell-7.0.0-1.rhel.7.x86_64.rpm
[rl-centos8]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/powershell-7.0.0-1.centos.8.x86_64.rpm
[rl-macos]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/powershell-7.0.0-osx-x64.pkg
[rl-winarm]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/PowerShell-7.0.0-win-arm32.zip
[rl-winarm64]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/PowerShell-7.0.0-win-arm64.zip
[rl-winx86-zip]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/PowerShell-7.0.0-win-x86.zip
[rl-winx64-zip]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/PowerShell-7.0.0-win-x64.zip
[rl-macos-tar]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/powershell-7.0.0-osx-x64.tar.gz
[rl-linux-tar]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/powershell-7.0.0-linux-x64.tar.gz
[rl-arm32]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/powershell-7.0.0-linux-arm32.tar.gz
[rl-arm64]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0/powershell-7.0.0-linux-arm64.tar.gz
[rl-snap]: https://snapcraft.io/powershell

[pv-windows-64]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0-rc.3/PowerShell-7.0.0-rc.3-win-x64.msi
[pv-windows-86]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0-rc.3/PowerShell-7.0.0-rc.3-win-x86.msi
[pv-ubuntu18]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0-rc.3/powershell-preview_7.0.0-rc.3-1.ubuntu.18.04_amd64.deb
[pv-ubuntu16]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0-rc.3/powershell-preview_7.0.0-rc.3-1.ubuntu.16.04_amd64.deb
[pv-debian9]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0-rc.3/powershell-preview_7.0.0-rc.3-1.debian.9_amd64.deb
[pv-debian10]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0-rc.3/powershell-preview_7.0.0-rc.3-1.debian.10_amd64.deb
[pv-centos]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0-rc.3/powershell-preview-7.0.0_rc.3-1.rhel.7.x86_64.rpm
[pv-centos8]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0-rc.3/powershell-preview-7.0.0_rc.3-1.centos.8.x86_64.rpm
[pv-macos]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0-rc.3/powershell-7.0.0-rc.3-osx-x64.pkg
[pv-winarm]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0-rc.3/PowerShell-7.0.0-rc.3-win-arm32.zip
[pv-winarm64]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0-rc.3/PowerShell-7.0.0-rc.3-win-arm64.zip
[pv-winx86-zip]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0-rc.3/PowerShell-7.0.0-rc.3-win-x86.zip
[pv-winx64-zip]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0-rc.3/PowerShell-7.0.0-rc.3-win-x64.zip
[pv-macos-tar]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0-rc.3/powershell-7.0.0-rc.3-osx-x64.tar.gz
[pv-linux-tar]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0-rc.3/powershell-7.0.0-rc.3-linux-x64.tar.gz
[pv-arm32]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0-rc.3/powershell-7.0.0-rc.3-linux-arm32.tar.gz
[pv-arm64]: https://github.com/PowerShell/PowerShell/releases/download/v7.0.0-rc.3/powershell-7.0.0-rc.3-linux-arm64.tar.gz
[pv-snap]: https://snapcraft.io/powershell-preview

[in-windows]: https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-7
[in-ubuntu14]: https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-linux?view=powershell-7#ubuntu-1404
[in-ubuntu16]: https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-linux?view=powershell-7#ubuntu-1604
[in-ubuntu18]: https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-linux?view=powershell-7#ubuntu-1804
[in-deb9]: https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-linux?view=powershell-7#debian-9
[in-centos]: https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-linux?view=powershell-7#centos-7
[in-rhel7]: https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-linux?view=powershell-7#red-hat-enterprise-linux-rhel-7
[in-opensuse]: https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-linux?view=powershell-7#opensuse
[in-fedora]: https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-linux?view=powershell-7#fedora
[in-archlinux]: https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-linux?view=powershell-7#arch-linux
[in-macos]: https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-macos?view=powershell-7
[in-docker]: https://github.com/PowerShell/PowerShell-Docker
[in-kali]: https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-linux?view=powershell-7#kali
[in-windows-zip]: https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-7#zip
[in-tar-linux]: https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-linux?view=powershell-7#binary-archives
[in-tar-macos]: https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-macos?view=powershell-7#binary-archives
[in-raspbian]: https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-linux?view=powershell-7#raspbian
[in-arm]: https://docs.microsoft.com/powershell/scripting/install/powershell-core-on-arm?view=powershell-7
[corefx-win]:https://github.com/dotnet/core/blob/master/release-notes/3.0/3.0-supported-os.md#windows
[corefx-linux]:https://github.com/dotnet/core/blob/master/release-notes/3.0/3.0-supported-os.md#linux
[corefx-macos]:https://github.com/dotnet/core/blob/master/release-notes/3.0/3.0-supported-os.md#macos

To install a specific version, visit [releases](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462f993ce68d5a966df7ec32fd7b10ae370bd78b438217eddd0c4f8cfa08d4f80c6d1b3136b8b8bd75390d246ff9bfa7e8 

## Community Dashboard

[Dashboard](http://u.720life.cn/g/ed703529f87faf7c77b9081c3c5759f363c78b937210440d4645291251e143a0)  with visualizations for community contributions and project status using PowerShell, Azure, and PowerBI.

For more information on how and why we built this dashboard, check out this [blog post](http://u.720life.cn/g/b4daa60d3d059fb4c6303e4a19d951a8de9da263685c64db5d83fd0458b29594a86d0fd39f111af55a1fb8350b34a31523c4c5a0b63a921265025c75baf92e751da88fc2972dca993e6570bcb1768e582612a2063af5e1cb057bc88697ddf83f4e002e5f88cc65c2905753a39d281a5a 

## Chat Room

Want to chat with other members of the PowerShell community?

We have a Gitter Room which you can join below.

[![Join the chat](https://img.shields.io/static/v1.svg?label=chat&message=on%20gitter&color=informational&logo=gitter)](https://gitter.im/PowerShell/PowerShell?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

There is also the community driven PowerShell Slack Team which you can sign up for at [Slack].

[Slack]: http://slack.poshcode.org

## Add-ons and libraries

[Awesome PowerShell](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463446c5786447b0de6060fd8d86aa216a4fb15b899f9d2bc98c71e4dda0d59581e3acf31c12d0a11277a4ac8dc0571a1f)  has a great curated list of add-ons and resources.

## Building the Repository

| Linux                    | Windows                    | macOS                   |
|--------------------------|----------------------------|------------------------|
| [Instructions][bd-linux] | [Instructions][bd-windows] | [Instructions][bd-macOS] |

If you have any problems building, please consult the developer [FAQ][].

### Build status of nightly builds

| Azure CI (Windows)                       | Azure CI (Linux)                               | Azure CI (macOS)                               | Code Coverage Status     | CodeFactor Grade         |
|:-----------------------------------------|:-----------------------------------------------|:-----------------------------------------------|:-------------------------|:-------------------------|
| [![windows-nightly-image][]][windows-nightly-site] | [![linux-nightly-image][]][linux-nightly-site] | [![macOS-nightly-image][]][macos-nightly-site] | [![cc-image][]][cc-site] | [![cf-image][]][cf-site] |

[bd-linux]: https://github.com/PowerShell/PowerShell/tree/master/docs/building/linux.md
[bd-windows]: https://github.com/PowerShell/PowerShell/tree/master/docs/building/windows-core.md
[bd-macOS]: https://github.com/PowerShell/PowerShell/tree/master/docs/building/macos.md

[FAQ]: https://github.com/PowerShell/PowerShell/tree/master/docs/FAQ.md

[az-windows-image]: https://powershell.visualstudio.com/PowerShell/_apis/build/status/PowerShell-CI-windows?branchName=master
[az-windows-site]: https://powershell.visualstudio.com/PowerShell/_build?definitionId=19
[az-linux-image]: https://powershell.visualstudio.com/PowerShell/_apis/build/status/PowerShell-CI-linux?branchName=master
[az-linux-site]: https://powershell.visualstudio.com/PowerShell/_build?definitionId=17
[az-macos-image]: https://powershell.visualstudio.com/PowerShell/_apis/build/status/PowerShell-CI-macos?branchName=master
[az-macos-site]: https://powershell.visualstudio.com/PowerShell/_build?definitionId=14
[az-spell-image]: https://powershell.visualstudio.com/PowerShell/_apis/build/status/PowerShell-CI-static-analysis?branchName=master
[az-spell-site]: https://powershell.visualstudio.com/PowerShell/_build?definitionId=22
[windows-nightly-site]: https://powershell.visualstudio.com/PowerShell/_build/latest?definitionId=32
[linux-nightly-site]: https://powershell.visualstudio.com/PowerShell/_build?definitionId=23
[macos-nightly-site]: https://powershell.visualstudio.com/PowerShell/_build?definitionId=24
[windows-nightly-image]: https://powershell.visualstudio.com/PowerShell/_apis/build/status/PowerShell-CI-Windows-daily
[linux-nightly-image]: https://powershell.visualstudio.com/PowerShell/_apis/build/status/PowerShell-CI-linux-daily?branchName=master
[macOS-nightly-image]: https://powershell.visualstudio.com/PowerShell/_apis/build/status/PowerShell-CI-macos-daily?branchName=master
[cc-site]: https://codecov.io/gh/PowerShell/PowerShell
[cc-image]: https://codecov.io/gh/PowerShell/PowerShell/branch/master/graph/badge.svg
[cf-site]: https://www.codefactor.io/repository/github/powershell/powershell
[cf-image]: https://www.codefactor.io/repository/github/powershell/powershell/badge

## Downloading the Source Code

You can just clone the repository:

```sh
git clone https://github.com/PowerShell/PowerShell.git
```

See [working with the PowerShell repository](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462f993ce68d5a966df7ec32fd7b10ae37c4d075d08ff159baaae19d181ddeb674b24730d8696715aa0d3278b3ce4aee47)  for more information.

## Developing and Contributing

Please see the [Contribution Guide][] for how to develop and contribute.
If you are developing .NET Core C# applications targeting PowerShell Core, please [check out our FAQ][] to learn more about the PowerShell SDK NuGet package.

Also, make sure to check out our [PowerShell-RFC repository](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046102781f4e05857e014173e03017085eb69e8fe16a30efc16b8f76269c5773238)  for request-for-comments (RFC) documents to submit and give comments on proposed and future designs.

[Contribution Guide]: https://github.com/PowerShell/PowerShell/blob/master/.github/CONTRIBUTING.md
[check out our FAQ]: https://github.com/PowerShell/PowerShell/tree/master/docs/FAQ.md#where-do-i-get-the-powershell-core-sdk-package

## Support

For support, please see the [Support Section][].

[Support Section]: https://github.com/PowerShell/PowerShell/tree/master/.github/SUPPORT.md

## Legal and Licensing

PowerShell is licensed under the [MIT license][].

[MIT license]: https://github.com/PowerShell/PowerShell/tree/master/LICENSE.txt

### Windows Docker Files and Images

License: By requesting and using the Container OS Image for Windows containers, you acknowledge, understand, and consent to the Supplemental License Terms available on Docker Hub:

- [Windows Server Core](http://u.720life.cn/g/ce46a7789a867c84732a8edd85365befb041ef69e7d6a531ab522ea8c28e54b503b9db33a54f5943e06cbb1b4f5c11bcf94b20027e62b531258cfd789be929a9) 
- [Nano Server](http://u.720life.cn/g/ce46a7789a867c84732a8edd85365befb041ef69e7d6a531ab522ea8c28e54b50b9c8a11f7040552773958538b932548) 

### Telemetry

By default, PowerShell collects the OS description and the version of PowerShell (equivalent to `$PSVersionTable.OS` and `$PSVersionTable.GitCommitId`) using [Application Insights](http://u.720life.cn/g/08a23d9c242a0aac3f1ee3afc4f56dc2ff56e5885ae798259f160030ec1ead55bcc252656dd5b122947f00c1742a9c968a65661f02c843b8d5d7f5d55b58cecf 
To opt-out of sending telemetry, create an environment variable called `POWERSHELL_TELEMETRY_OPTOUT` set to a value of `1` before starting PowerShell from the installed location.
The telemetry we collect falls under the [Microsoft Privacy Statement](http://u.720life.cn/g/904d0eda6c4951f2fe4847311f92d3edb8f97c6112d351d11397305efa8a77ea3e3daf5bd9a2e3998f493b36bb7486a4797fa8b2e9d96aed9a749a2f6b175897 

## Governance

Governance policy for PowerShell project is described [here][].

[here]: https://github.com/PowerShell/PowerShell/blob/master/docs/community/governance.md

## [Code of Conduct][conduct-md]

This project has adopted the [Microsoft Open Source Code of Conduct][conduct-code].
For more information see the [Code of Conduct FAQ][conduct-FAQ] or contact [opencode@microsoft.com][conduct-email] with any additional questions or comments.

[conduct-code]: https://opensource.microsoft.com/codeofconduct/
[conduct-FAQ]: https://opensource.microsoft.com/codeofconduct/faq/
[conduct-email]: mailto:opencode@microsoft.com
[conduct-md]: https://github.com/PowerShell/PowerShell/tree/master/CODE_OF_CONDUCT.md



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)