Welcome\! This repository contains the source code for:

  - Windows Terminal
  - The Windows console host (`conhost.exe`)
  - Components shared between the two projects
  - [ColorTool](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046dd40ae045c96902af50a41bdb40c13e469efa426cd2e0a1e97b1b3fec39fa931e3701116af7aba64c116206a759c0bcfab2cc29ec74f85a4c3ab03056f4960f0) 
  - [Sample projects](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046dd40ae045c96902af50a41bdb40c13e469efa426cd2e0a1e97b1b3fec39fa9311a404c7a5f8adff713062abc3cceb146)  that show how to consume the Windows Console APIs

### Build Status

Project|Build Status
---|---
Terminal|[![Build Status](https://dev.azure.com/ms/Terminal/_apis/build/status/Terminal%20CI?branchName=master)](https://dev.azure.com/ms/Terminal/_build?definitionId=136)
ColorTool|![](https://microsoft.visualstudio.com/_apis/public/build/definitions/c93e867a-8815-43c1-92c4-e7dd5404f1e1/17023/badge)

# Terminal & Console Overview

Please take a few minutes to review the overview below before diving into the code:

## Windows Terminal

Windows Terminal is a new, modern, feature-rich, productive terminal application for command-line users. It includes many of the features most frequently requested by the Windows command-line community including support for tabs, rich text, globalization, configurability, theming & styling, and more.

The Terminal will also need to meet our goals and measures to ensure it remains fast, and efficient, and doesn't consume vast amounts of memory or power.

## The Windows console host

The Windows console host, `conhost.exe`, is Windows' original command-line user experience. It implements Windows' command-line infrastructure, and is responsible for hosting the Windows Console API, input engine, rendering engine, and user preferences. The console host code in this repository is the actual source from which the `conhost.exe` in Windows itself is built.

Console's primary goal is to remain backwards-compatible with existing console subsystem applications.

Since assuming ownership of the Windows command-line in 2014, the team has added several new features to the Console, including window transparency, line-based selection, support for [ANSI / Virtual Terminal sequences](http://u.720life.cn/g/dbf1195f8a53209e138d24666db066369e30537899bba9d4ad13f58106103ffa1592ca88b9cc88bcdde215d85f94abcc  [24-bit color](http://u.720life.cn/g/0eb7ef68e3710af1364fb22f7dd3f03521037eb6e50464e25fd37352ca4f56c3ead80e1c9818053fcc720943620dd983fe4ff7b06c1078db4b13f740ba9d05816658411c489d5ba869966b304a87c84ab70a8f62c0f6d2d6bddb0029503447cc  a [Pseudoconsole ("ConPTY")](http://u.720life.cn/g/0eb7ef68e3710af1364fb22f7dd3f03521037eb6e50464e25fd37352ca4f56c354b5dadf1c5d8b456d3dbe8178e6d609697dd027879386235285a0efeb58bb253a7c15fc1015a02efffc934265c0f83e46d6f162c405ab35c5345a2130957a0a8d08cfbbeafc4241980e39103d7e5fab  and more.

However, because the Console's primary goal is to maintain backward compatibility, we've been unable to add many of the features the community has been asking for, and which we've been wanting to add for the last several years--like tabs!

These limitations led us to create the new Windows Terminal.

## Shared Components

While overhauling the Console, we've modernized its codebase considerably. We've cleanly separated logical entities into modules and classes, introduced some key extensibility points, replaced several old, home-grown collections and containers with safer, more efficient [STL containers](http://u.720life.cn/g/7f9564e5f558bc72a27cbe45da89f3838e2cd6dc01b92e58e0e861ee33282c2348d843ed086d5b5ccebc64decf82dd3a5390d4f080379ee3cb7e5628c2a70bc7fd4df41d03468d8d9f2ea7b905d793ce0201eea296c2e9c561d823bbc1962366  and made the code simpler and safer by using Microsoft's [WIL](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466d912ca50d660695c1eedcf46cde5c7e)  header library.

This overhaul work resulted in the creation of several key components that would be useful for any terminal implementation on Windows, including a new DirectWrite-based text layout and rendering engine, a text buffer capable of storing both UTF-16 and UTF-8, and a VT parser/emitter.

## Building a new terminal

When we started building the new terminal application, we explored and evaluated several approaches and technology stacks. We ultimately decided that our goals would be best met by sticking with C++ and sharing the aforementioned modernized components, placing them atop the modern Windows application platform and UI framework.

Further, we realized that this would allow us to build the terminal's renderer and input stack as a reusable Windows UI control that others can incorporate into their applications.

# FAQ

## Where can I download Windows Terminal?

### There are no binaries to download quite yet. 

The Windows Terminal is in the _very early_ alpha stage, and not ready for the general public quite yet. If you want to jump in early, you can try building it yourself from source. 

Otherwise, you'll need to wait until Mid-June for an official preview build to drop.

## I built and ran the new Terminal, but it looks just like the old console! What gives?

Firstly, make sure you're building & deploying `CascadiaPackage` in Visual Studio, _NOT_ `Host.EXE`. `OpenConsole.exe` is just `conhost.exe`, the same old console you know and love. `opencon.cmd` will launch `openconsole.exe`, and unfortunately, `openterm.cmd` is currently broken.

Secondly, try pressing Ctrl+t. The tabs are hidden when you only have one tab by default. In the future, the UI will be dramatically different, but for now, the defaults are _supposed_ to look like the console defaults.

## I tried running WindowsTerminal.exe and it crashes!

* Don't try to run it unpackaged. Make sure to build & deploy `CascadiaPackage` from Visual Studio, and run the Windows Terminal (Preview) app.
* Make sure you're on the right version of Windows. You'll need to be on Insider's builds, or wait for the 1903 release, as the Windows Terminal **REQUIRES** features from the latest Windows release.

# Getting Started

## Prerequisites

* You must be running Windows 1903 (build >= 10.0.18362.0) or above in order to run Windows Terminal
* You must have the [1903 SDK](http://u.720life.cn/g/a69e8f5dba5b4106ccc3875c547b1484ca582ccb97b1edef8e165c477581401b21de6ef1886a471ec085a00de55a0c208336fcff8b90f1159df5bdb5375f1cfa212326a526f4e7e1939e06a5770e1edc)  (build 10.0.18362.0) installed
* You will need at least [VS 2017](http://u.720life.cn/g/820904a611da240c9864c98b312d88b8c07726139b7dc45e0ef6d2903f520b6f818e5751f49374ba4ff35410e5128419)  installed
* You will need to install both the following packages in VS ("Workloads" tab in Visual Studio Installer) :
  - "Desktop Development with C++"
  - "Universal Windows Platform Development"
  - If you're running VS2019, you'll also need to install the "v141 Toolset" and "Visual C++ ATL for x86 and x64"
* You will also need to enable Developer Mode in the Settings app to enable installing the Terminal app for running locally.

## Contributing

We are excited to work alongside you, our amazing community, to build and enhance Windows Terminal\!

We ask that **before you start work on a feature that you would like to contribute,  please file an issue  describing your proposed change**: We will be happy to work with you to figure out the best approach, provide guidance and mentorship throughout feature development, and help avoid any wasted or duplicate effort.

> 👉 **Remember\!** Your contributions may be incorporated into future versions of Windows\! Because of this, all pull requests will be subject to the same level of scrutiny for quality, coding standards, performance, globalization, accessibility, and compatibility as those of our internal contributors.

> ⚠ **Note**: The Command-Line Team is actively working out of this repository and will be periodically re-structuring the code to make it easier to comprehend, navigate, build, test, and contribute to, so **DO expect significant changes to code layout on a regular basis**.

## Communicating with the Team

The easiest way to communicate with the team is via GitHub issues. Please file new issues, feature requests and suggestions, but **DO search for similar open/closed pre-existing issues before you do**.

Please help us keep this repository clean, inclusive, and fun\! We will not tolerate any abusive, rude, disrespectful or inappropriate behavior. Read our [Code of Conduct](http://u.720life.cn/g/22e7b067064505b0b066921a690bc00f40fc6818092ae136d535683f62b36971e7b295096e982152791c6cc0acadce74)  for more details.

If you would like to ask a question that you feel doesn't warrant an issue (yet), please reach out to us via Twitter:

  - Rich Turner, Program Manager: [@richturn\_ms](http://u.720life.cn/g/5ea88169c4a0fbd169233d52478d54fe007ef5d4e19102305bd9dda982ed9d9e) 

  - Dustin Howett, Engineering Lead: [@dhowett](http://u.720life.cn/g/5ea88169c4a0fbd169233d52478d54fe015cb5aa091c27a255ded3201b1cac04) 

  - Michael Niksa, Senior Developer: [@michaelniksa](http://u.720life.cn/g/5ea88169c4a0fbd169233d52478d54fe227ea51e2d29a8cdbdd0dd0a2387edb0) 

  - Kayla Cinnamon, Program Manager (especially for UX issues): [@cinnamon\_msft](http://u.720life.cn/g/5ea88169c4a0fbd169233d52478d54fef7f3fdf610fb30b1e31b551e5ee25cf53c7a310c75ecf2c1dded9d99720dff31) 

# Developer Guidance

## Building the Code

This repository uses [git submodules](http://u.720life.cn/g/0699e533b96232c5e210af6ab5668134af9e5b446fffe54eb720e923db98d7716b1856c762ff07df656cb67af39b81f9867ce21b19d9e1ddbacfbcfdb6070cf4)  for some of its dependencies. To make sure submodules are restored or updated, be sure to run the following prior to building:

```shell
git submodule update --init --recursive
```

OpenConsole.sln may be built from within Visual Studio or from the command-line using MSBuild. To build from the command line:

```shell
.\tools\razzle.cmd
bcz
```

We've provided a set of convenience scripts as well as [README](./tools/README.md) in the **/tools** directory to help automate the process of building and running tests.

## Coding Guidance

Please review these brief docs below relating to our coding standards etc.

> 👉 If you find something missing from these docs, feel free to contribute to any of our documentation files anywhere in the repository (or make some new ones\!)

This is a work in progress as we learn what we'll need to provide people in order to be effective contributors to our project.

  - [Coding Style](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046dd40ae045c96902af50a41bdb40c13e4a6368e632e1fc9e6839993fa497c9b3c5501501c073f1fca9d46db29b2c49daf) 
  - [Code Organization](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046dd40ae045c96902af50a41bdb40c13e4a6368e632e1fc9e6839993fa497c9b3c4b130aa8af5e16b89199708f66dd25b4bfd4c12958cc12db644dd923c7687600) 
  - [Exceptions in our legacy codebase](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046dd40ae045c96902af50a41bdb40c13e4a6368e632e1fc9e6839993fa497c9b3c2679a0a0255e7b31a8edb29023143dc4beb5d9df972d92549b219338e6ddc577) 
  - [Helpful smart pointers and macros for interfacing with Windows in WIL](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046dd40ae045c96902af50a41bdb40c13e4a6368e632e1fc9e6839993fa497c9b3c06ee1fac029eb8278bf75fd388795a7b) 

# Code of Conduct

This project has adopted the [Microsoft Open Source Code of Conduct][conduct-code].
For more information see the [Code of Conduct FAQ][conduct-FAQ] or contact [opencode@microsoft.com][conduct-email] with any additional questions or comments.

[conduct-code]: https://opensource.microsoft.com/codeofconduct/
[conduct-FAQ]: https://opensource.microsoft.com/codeofconduct/faq/
[conduct-email]: mailto:opencode@microsoft.com



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)