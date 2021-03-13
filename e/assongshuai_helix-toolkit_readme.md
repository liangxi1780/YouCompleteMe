 

# Helix Toolkit

**Helix Toolkit is a collection of 3D components for .NET Framework.**

[**HelixToolkit.WPF:**](/Source/HelixToolkit.Wpf) 
Adds variety of functionalities/models on the top of internal WPF 3D models (Media3D namespace). 

[**HelixToolkit.SharpDX.WPF:**](/Source/HelixToolkit.Wpf.SharpDX) 
Custom 3D Engine and XAML/MVVM compatible Scene Graphs based on [SharpDX](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304654675ab9b85f6ccd43c8f1978a52fadf241b8f54c655d7297f94df1270f2a39e  11) for high performance usage.

[**HelixToolkit.UWP:**](/Source/HelixToolkit.UWP) 
Custom 3D Engine and XAML/MVVM compatible Scene Graphs based on [SharpDX](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304654675ab9b85f6ccd43c8f1978a52fadf241b8f54c655d7297f94df1270f2a39e  11) for Universal Windows App.

[**HelixToolkit.SharpDX.Core:**](/Source/HelixToolkit.SharpDX.Core) 
Custom 3D Engine and Scene Graphs based on [SharpDX](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304654675ab9b85f6ccd43c8f1978a52fadf241b8f54c655d7297f94df1270f2a39e  11) for netstandard and .NET Core.

[**HelixToolkit.SharpDX.Assimp:**](/Source/HelixToolkit.Wpf.SharpDX.Assimp) 
[Assimp.Net](http://u.720life.cn/g/72026af82e032ae6e7744b1eb21f3c0814c12e51f98640866c04b8be7a427b4d585d8ba80bc3ff77267b1f67ed68ce2a238f01e692c12a00c5826b75ee36dfc8)  3D model importer/expoter support for HelixToolkit.SharpDX Components.

[**Examples:**](/develop/Source/Examples)
Please download full source code to run examples. Or download [compiled version](http://u.720life.cn/g/134499da667fce84d5b0b80ba6e1ebd79098c3a605934ce27d196f93c34181db32bd5ffc7a22b31e55c4a204a619299e01519791d1ac4b9912d042fbe9613042afa61bd3699de56ba9a5312f7c10671a) 

[![License: MIT](https://img.shields.io/github/license/helix-toolkit/helix-toolkit.svg?style=popout)](https://github.com/helix-toolkit/helix-toolkit/blob/develop/LICENSE)
[![Build status](https://ci.appveyor.com/api/projects/status/tmqafdk9p7o98gw7?svg=true)](https://ci.appveyor.com/project/objorke/helix-toolkit)
[![Release](https://img.shields.io/github/release/helix-toolkit/helix-toolkit.svg?style=popout)](https://www.nuget.org/packages?q=Helix-Toolkit)
[![Chat](https://img.shields.io/gitter/room/helix-toolkit/helix-toolkit.svg)](https://gitter.im/helix-toolkit/helix-toolkit)

Description         | Value
--------------------|-----------------------
Web page            | http://helix-toolkit.github.io/
Wiki                | https://github.com/helix-toolkit/helix-toolkit/wiki
Documentation       | http://helix-toolkit.readthedocs.io/
Chat                | https://gitter.im/helix-toolkit/helix-toolkit
Source repository   | http://github.com/helix-toolkit/helix-toolkit
Latest build        | http://ci.appveyor.com/project/objorke/helix-toolkit
Issue tracker       | http://github.com/helix-toolkit/helix-toolkit/issues
NuGet packages      | http://www.nuget.org/packages?q=HelixToolkit
MyGet feed          | https://www.myget.org/F/helix-toolkit
StackOverflow       | http://stackoverflow.com/questions/tagged/helix-3d-toolkit
Twitter             | https://twitter.com/hashtag/Helix3DToolkit

## Project Build

**Visual Studio 2019. Windows 10 SDK (Min Ver.10.0.17763).**

**Missing `.cso` error during the build?** Windows 10 SDK **Ver.10.0.17763** can be selected and installed using Visual Studio 2019 installer. If you already installed the higher SDK version, please change the target version in **HelixToolkit.Native.ShaderBuilder** property to the version installed on your machine.

## Notes

#### 1. Right-handed Cartesian coordinate system and row major matrix by default
HelixToolkit default is using right-handed Cartesian coordinate system, including Meshbuilder etc. To use left-handed Cartesian coordinate system (Camera.CreateLeftHandedSystem = true), user must manually correct the triangle winding order or IsFrontCounterClockwise in raster state description if using SharpDX. Matrices are row major by default.

#### 2. Performance [Topics](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046bb726820436518c88dc20d9da1167ee14994afb719ce9c4777fc3427834f50fbed389f091677aab3905d462030b9e5ac526b41bd5fdb79a6ca79f362c2bdeed479cc02fb843093f1819d69650c75b5ff0e71c55fcf4f803577d4acf724716272)  for WPF.SharpDX and UWP.

#### 3. Following features are not supported currently on FeatureLevel 10 graphics card:
FXAA, Order Independant Transparent Rendering, Particle system, Tessellation.

#### 4. [Wiki](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046bb726820436518c88dc20d9da1167ee14994afb719ce9c4777fc3427834f50fb247708bbcdde075f01a18dbdf07d060f)  and useful [External Resources](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046bb726820436518c88dc20d9da1167ee14994afb719ce9c4777fc3427834f50fb50c3225c6727bb6b15496d4007295059820ce9cf4310ff2da77163526296d463)  on Computer Graphics.

## Bug Report
Please use the following template to report bugs.

- Version: [Example: 2.11]
- Package: [Example: Helixtoolkit.Wpf]
- Issue: 
- Reproduce Steps:
- Sample Code:

## News

#### 2020-02-08
[v2.11.0](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046bb726820436518c88dc20d9da1167ee166bd069648186eea1a5a48d6913eb0cc39d1ceff99294e77bcec7f1380830087b3bf0d3ce3a30903f8d515dbb6118f3f)  releases are available on nuget. [Release Note](/CHANGELOG.md)
- [WPF](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17ecb3a9c2b2dee4c1de0ced7b508c0cbca81c303618e849df1870993491246a17d) 
- [Core.WPF](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17e4d506f58a54c9f1819511a70de60b10092e8e71501f405794de029dbd90d6266) 
- [WPF.Input](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17e27391d7f38c5af63282ea00be04d42a1a0202599aca0cbbd8abd94e89a34f3e6) 
- [WPF.SharpDX](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17e27391d7f38c5af63282ea00be04d42a1f3488a96aca0eb8c5f15fbacc6e6904e) 
- [UWP](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17eca7704942fb29d26f050abc5a1a9bd5fe43ac51caa3e93b6b248210361111fda) 
- [SharpDX.Core](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17ebfdeec9d5107ea394dab65a06f887eeed92e4fed6d86d6b431507c507e23e77b) 
- [SharpDX.Core.Wpf](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17ebfdeec9d5107ea394dab65a06f887eee06faa0283b647fc7d3933b0b6231b57183a7d540fcffb55101f59a6d1925c1a6) 
- [SharpDX.Assimp](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17ebfdeec9d5107ea394dab65a06f887eee943519299053aaa3a110c08656b1cc15372d456737e56fefda46e0dd66bb470a) 

#### 2019-11-10
[v2.10.0](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046bb726820436518c88dc20d9da1167ee166bd069648186eea1a5a48d6913eb0cc222942630d7a95b6cace011adcc422b819d60b2a151c008881ac1aae9e96c6db)  releases are available on nuget. [Release Note](/CHANGELOG.md)
- [WPF](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17ecb3a9c2b2dee4c1de0ced7b508c0cbca713dd35213e256b8a7160023f33ce8b5) 
- [Core.WPF](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17e4d506f58a54c9f1819511a70de60b1005a8d285063d8a9062365f2e0cdb84ca4) 
- [WPF.Input](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17e27391d7f38c5af63282ea00be04d42a1a44663580e8c1dd38c7d1eb6db44b136) 
- [WPF.SharpDX](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17e27391d7f38c5af63282ea00be04d42a129197e9efa72a445099139118b4d1266) 
- [UWP](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17eca7704942fb29d26f050abc5a1a9bd5fd792d17163253219beed0cd3ad774efa) 
- [SharpDX.Core](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17ebfdeec9d5107ea394dab65a06f887eeea985479fcd2a9111a82af5140e7b911a) 
- [SharpDX.Core.Wpf](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17ebfdeec9d5107ea394dab65a06f887eee06faa0283b647fc7d3933b0b6231b5712259c9a36d638fdea42dacda00b467b3) 
- [SharpDX.Assimp](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17ebfdeec9d5107ea394dab65a06f887eeea2e5485d712e1b8b02a5dfd657d21c0ddb2a5476b4d654f4141eee0b0f56026e) 

#### 2019-08-24
[v2.9.0](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046bb726820436518c88dc20d9da1167ee166bd069648186eea1a5a48d6913eb0cc67ed9818e8909eeb66bd2f9e0d6b893ff7fc49acc91baf6d6686c747df92b453)  releases are available on nuget. [Release Note](/CHANGELOG.md)
- [WPF](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17ecb3a9c2b2dee4c1de0ced7b508c0cbca58f7173abd820d82be6264797c0a499f) 
- [WPF.Input](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17e27391d7f38c5af63282ea00be04d42a1498989da88e7e703005e9552818476f4) 
- [WPF.SharpDX](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17e27391d7f38c5af63282ea00be04d42a12b30ec5e420988652c090099b99ab16e) 
- [UWP](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17eca7704942fb29d26f050abc5a1a9bd5f7cf5457d160da024fb5ce77306313a7f) 
- [SharpDX.Core](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17ebfdeec9d5107ea394dab65a06f887eeec2d6681b8b008df8ec8ab324502012e1) 
- [SharpDX.Assimp](http://u.720life.cn/g/fc22af1986001aaffae545db699770d8ccd0daabc28bf76bb9abe914f4cfe17ebfdeec9d5107ea394dab65a06f887eee051e5ac08112cbd2cb23be2fe662bcc8) 

#### Changes (Please refer to [Release Note](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046bb726820436518c88dc20d9da1167ee187caa6e79efc1fcafe163ba8fdd96fb56a6d2e3f25c7ebfc43db0d98aa048c649ececb5e242d2dc4860fc7b520e5cbad)  for details)

##### Note: 2.0 Breaking changes from version 1.x.x. (HelixToolkit.SharpDX only) see [ChangeLog](/CHANGELOG.md)



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)