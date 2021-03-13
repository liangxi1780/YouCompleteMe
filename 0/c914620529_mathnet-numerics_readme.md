Math.NET Numerics
=================

Math.NET Numerics is an opensource **numerical library for .Net, Silverlight and Mono**.

Math.NET Numerics is the numerical foundation of the Math.NET initiative, aiming to provide methods and algorithms for numerical computations in science, engineering and every day use. Covered topics include special functions, linear algebra, probability models, random numbers, statistics, interpolation, integration, regression, curve fitting, integral transforms (FFT) and more.

In addition to the core .NET package (which is written entirely in C#), Numerics specifically supports F# with idiomatic extension modules and maintains mathematical data structures like BigRational that originated in the F# PowerPack. If a performance boost is needed, the managed-code provider backing its linear algebra routines and decompositions can be exchanged with wrappers for optimized native implementations such as Intel MKL.

Math.NET Numerics is covered under the terms of the [MIT/X11](LICENSE.md) license. You may therefore link to it and use it in both opensource and proprietary software projects. We accept contributions!

* [**Project Website**](http://u.720life.cn/g/86722a84ff3c79c2e50a9a5ca1053a3eb9de25a7a8ccdc3f91e6b9804060afdf) 
* [Source Code](http://u.720life.cn/g/f6754e90a70fcffec3c12b5e1e01b2d34158fd2ce77675be781e2ff3b4ddbf3c4fc5d57041733b2ee0482f1b5ce3ab5e) 
* [NuGet & Binaries](http://u.720life.cn/g/86722a84ff3c79c2e50a9a5ca1053a3e5ae6f149394e47e77646154039211865bab22f21a6ef08e7f35128ef15926170)  | [Release Notes](http://u.720life.cn/g/86722a84ff3c79c2e50a9a5ca1053a3e6b20c2ce7af3a1285e75fa0b6e3f1f967d1293980a2c8dce0e72998c47a10256) 
* [Documentation](http://u.720life.cn/g/86722a84ff3c79c2e50a9a5ca1053a3eb9de25a7a8ccdc3f91e6b9804060afdf)  | [API Reference](http://u.720life.cn/g/86722a84ff3c79c2e50a9a5ca1053a3eed41602577d228bfb5a564ecbaabed4626dbbc048f18f43fd471d185656990aa) 
* [Issues & Bugs](http://u.720life.cn/g/f6754e90a70fcffec3c12b5e1e01b2d34158fd2ce77675be781e2ff3b4ddbf3cdb23a6b7e96758d042052bd6075dd28cda1524a13b7c15914f66eeb45b1adde5)  | [Ideas](http://u.720life.cn/g/0407e4715a287fb5c21a740ddf0858a8484cc21ef5aa4f82d946f6c35f9253a4b292f611100c15dc56c759759077c8cbe86cf52e16e220daf000fd02e718d57a) 
* [Discussions](http://u.720life.cn/g/a2ad429add0a5c335524d148fee2dc66875c58f0e40fa42afc8424f348341c7d44b49bee99e6743aa180fa47cec9651e)  | [Stack Overflow](http://u.720life.cn/g/ddb1c8aa997182cb1a4af16f7df394520a2863231ad8d7352308cd295ccf0ae903e4a0845ec4a8d324e78f4d1647c3b5ae3fe08f7c00ae457d4763c85d778a6f)  | [Twitter](http://u.720life.cn/g/872672d0e23e2eaceaf26c6fd3ebbc6dfe19b541710130edb36a1403153888f4) 
* [Wikipedia](http://u.720life.cn/g/aace67412d3c40f689b2c469b4f53b5974d863b425d20d5a5f62666c40cd38295eba79cea83617b7e02b364499edf9ac)  | [OpenHUB](http://u.720life.cn/g/fdd5fa93ad411ba171f92856eb15be2157e849680d06efd93a9570f085a4b3f3) 

### Current Version

![Math.NET Numerics Version](http://img.shields.io/nuget/v/MathNet.Numerics.svg?style=flat) Math.NET Numerics  
![Native Providers Version](http://img.shields.io/nuget/v/MathNet.Numerics.MKL.Win-x64.svg?style=flat) Native Providers  
![Data Extensions Version](http://img.shields.io/nuget/v/MathNet.Numerics.Data.Text.svg?style=flat) Data Extensions

Installation Instructions
-------------------------

The recommended way to get Math.NET Numerics is to use NuGet. The following packages are provided and maintained in the public [NuGet Gallery](http://u.720life.cn/g/2d31820d3fd987587cd7805d437edf9a8d6b73f2e4e35c5541db67394a9184cd144458fe23919cc46a104b0a163bd7f4  Alternatively you can also download the binaries in Zip packages, available on [CodePlex](http://u.720life.cn/g/f615266d63ba06afd975437a1eaab8f24d0f821585d2ef6889f306a10ae9bfe704670907593b09cdf265e37245adef78 

Core Package:

- **MathNet.Numerics** - core package, including .Net 4, .Net 3.5 and portable/PCL builds.
- **MathNet.Numerics.FSharp** - optional extensions for a better F# experience. BigRational.
- **MathNet.Numerics.Signed** - strong-named version of the core package *(not recommended)*.
- **MathNet.Numerics.FSharp.Signed** - strong-named version of the F# package *(not recommended)*.

Alternative Provider Packages (optional):

- **MathNet.Numerics.MKL.Win-x86** - Native Intel MKL Linear Algebra provider (Windows/32-bit).
- **MathNet.Numerics.MKL.Win-x64** - Native Intel MKL Linear Algebra provider (Windows/64-bit).

Data/IO Packages for reading and writing data (optional):

- **MathNet.Numerics.Data.Text** - Text-based matrix formats like CSV and MatrixMarket.
- **MathNet.Numerics.Data.Matlab** - MATLAB Level-5 matrix file format.

Platform Support and Dependencies
---------------------------------

Supported Platforms:

- .Net 4.0, .Net 3.5 and Mono: Windows, Linux and Mac.
- PCL Portable Profiles 7, 47, 78, 259 and 328: Windows 8, Silverlight 5, Windows Phone/SL 8, Windows Phone 8.1.
- Xamarin: Android, iOS

For full details, dependencies and platform discrepancies see [Platform Compatibility](http://u.720life.cn/g/86722a84ff3c79c2e50a9a5ca1053a3ec66478cbfa1faa124d19548176888399bc4b40978753df2a3f7d2810f54ace05326b85b1914f585cdb474394fbcc153e 

Building Math.NET Numerics
--------------------------

Windows (.Net): [![AppVeyor build status](https://ci.appveyor.com/api/projects/status/79j22c061saisces/branch/master)](https://ci.appveyor.com/project/cdrnet/mathnet-numerics)  
Linux (Mono): [![Travis Build Status](https://travis-ci.org/mathnet/mathnet-numerics.svg?branch=master)](https://travis-ci.org/mathnet/mathnet-numerics)

You can build Math.NET Numerics with an IDE like VisualStudio or Xamarin,
with MsBuild or with FAKE.

MsBuild/XBuild:

    msbuild MathNet.Numerics.sln

FAKE:

    build.cmd Build    # build from the Windows console with .Net
    ./build.sh Build   # build from Bash, with Mono on Linux/Mac or .Net on Windows
    ./build.sh Test    # build and run unit tests

See [Build & Tools](http://u.720life.cn/g/86722a84ff3c79c2e50a9a5ca1053a3e1e0f9233d7d7b099318c4b59aaed5825b5911366257603fe420e3326ee70bb89)  for full details
on how to build, generate documentation or even create a full release.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)