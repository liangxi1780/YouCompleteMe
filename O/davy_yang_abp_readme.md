# ABP

![build and test](https://github.com/abpframework/abp/workflows/build%20and%20test/badge.svg)
[![NuGet](https://img.shields.io/nuget/v/Volo.Abp.Core.svg?style=flat-square)](https://www.nuget.org/packages/Volo.Abp.Core)
[![MyGet (with prereleases)](https://img.shields.io/myget/abp-nightly/vpre/Volo.Abp.svg?style=flat-square)](https://docs.abp.io/en/abp/latest/Nightly-Builds)
[![NuGet Download](https://img.shields.io/nuget/dt/Volo.Abp.Core.svg?style=flat-square)](https://www.nuget.org/packages/Volo.Abp.Core)

This project is the next generation of the [ASP.NET Boilerplate](http://u.720life.cn/g/bf9d60cc47899993c4e10bb18073a29c3ecedf873a98c41a235efdd010ef6b85)  web application framework. See [the announcement](http://u.720life.cn/g/35bf74d78eb3b0e699ea41663670febd46d704de7a053e4a6df74334ba6ec2457df0bb8381148e38f6180ce35e246f67 

See the official [web site (abp.io)](http://u.720life.cn/g/e901e3eb8d56200361a16d9f3ae9fbbc)  for more information.

### Documentation

See the  documentation .

### Development

#### Pre Requirements

- Visual Studio 2019 16.4.0+

#### Framework

Framework solution is located under the `framework` folder. It has no external dependency.

#### Modules/Templates

[Modules](modules/) and [Templates](templates/) have their own solutions and have **local references** to the framework and each other.

Visual Studio can not work properly with the local references out of the solution folder. When you open a module/sample solution in the Visual Studio, you may get some errors related to the dependencies. In this case, run the `dotnet restore` on the command prompt for the related solution's folder. You need to run it after you first open the solution or change a dependency.

### Contribution

ABP is an open source platform. Check [the contribution guide](docs/en/Contribution/Index.md) if you want to contribute to the project.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)