gRPC - An RPC library and framework
===================================

gRPC is a modern, open source, high-performance remote procedure call (RPC) framework that can run anywhere. gRPC enables client and server applications to communicate transparently, and simplifies the building of connected systems.

 
   
      Homepage:  
      grpc.io  
   
   
      Mailing List:  
      grpc-io@googlegroups.com  
   
 

[![Join the chat at https://gitter.im/grpc/grpc](https://badges.gitter.im/grpc/grpc.svg)](https://gitter.im/grpc/grpc?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

# To start using gRPC

To maximize usability, gRPC supports the standard method for adding dependencies to a user's chosen language (if there is one).
In most languages, the gRPC runtime comes as a package available in a user's language package manager.

For instructions on how to use the language-specific gRPC runtime for a project, please refer to these documents

 * [C++](src/cpp): follow the instructions under the `src/cpp` directory
 * [C#](src/csharp): NuGet package `Grpc`
 * [Dart](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046452a5f71350a6e416acbc579b192225c3f280b6338c9411931d63f8eec6c6dea  pub package `grpc`
 * [Go](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469fed61561597a350b519ecd1c1deb5526edb2f99c90fe901b391d573d775ab20  `go get google.golang.org/grpc`
 * [Java](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046fe94b7b76179efc377526a00a74b2d1473a9ca2191e4e4dc970e0e0540e189d0  Use JARs from Maven Central Repository
 * [Node](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046cf6c8bd9700cc68bd070f30add00eff184d73ede72dd404eabd473f3353bcec1  `npm install grpc`
 * [Objective-C](src/objective-c): Add `gRPC-ProtoRPC` dependency to podspec
 * [PHP](src/php): `pecl install grpc`
 * [Python](src/python/grpcio): `pip install grpcio`
 * [Ruby](src/ruby): `gem install grpc`
 * [WebJS](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046824bb0c537864079177f89f257c703623e3ccfc85681ad19dce82d1615d1dbc9  follow the grpc-web instructions

Per-language quickstart guides and tutorials can be found in the [documentation section on the grpc.io website](http://u.720life.cn/g/8c024964a090786d506fe3e8c05197243d93a3f6e679ba21eed25394fbaeea6a  Code examples are available in the [examples](examples) directory.

Precompiled bleeding-edge package builds of gRPC `master` branch's `HEAD` are uploaded daily to [packages.grpc.io](http://u.720life.cn/g/ef290e076b81ef97791a042cd15959d4abf4f610230e7d413d1819e588f3b584 

# To start developing gRPC

Contributions are welcome!

Please read [How to contribute](CONTRIBUTING.md) which will guide you through the entire workflow of how to build the source code, how to run the tests, and how to contribute changes to
the gRPC codebase.
The "How to contribute" document also contains info on how the contribution process works and contains best practices for creating contributions.

# Troubleshooting

Sometimes things go wrong. Please check out the [Troubleshooting guide](TROUBLESHOOTING.md) if you are experiencing issues with gRPC.

# Performance 

See the [Performance dashboard](http://u.720life.cn/g/d23f3545585c60292e26e40cb4882fd97672652ee55ffdae2ace4d5c21c297807908bcd06fb9875e0724ccdff50f58e5806ef346b4e36009f8c0457eb18d1cc2c3bba7ba5eff3d4c2fdff52766e06f15ee6d7dad8fbbaecb966937f19eb6c3d3)  for performance numbers of the latest released version.

# Concepts

See [gRPC Concepts](CONCEPTS.md)

# About This Repository

This repository contains source code for gRPC libraries implemented in multiple languages written on top of a shared C core library [src/core](src/core).

Libraries in different languages may be in various states of development. We are seeking contributions for all of these libraries:

| Language                | Source                              |
|-------------------------|-------------------------------------|
| Shared C [core library] | [src/core](src/core)                |
| C++                     | [src/cpp](src/cpp)                  |
| Ruby                    | [src/ruby](src/ruby)                |
| Python                  | [src/python](src/python)            |
| PHP                     | [src/php](src/php)                  |
| C# (core library based) | [src/csharp](src/csharp)            |
| Objective-C             | [src/objective-c](src/objective-c)  |

| Language                | Source repo                                          |
|-------------------------|------------------------------------------------------|
| Java                    | [grpc-java](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046fe94b7b76179efc377526a00a74b2d146ebf4a00eb18bd7079c6f2113046b3bb)         |
| Go                      | [grpc-go](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ce49d951bfe6c5c3f8b5a647381454de)             |
| NodeJS                  | [grpc-node](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046cf6c8bd9700cc68bd070f30add00eff1de9a0e88603a60347be11a86c0b27115)        |
| WebJS                   | [grpc-web](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046824bb0c537864079177f89f257c70362)          |
| Dart                    | [grpc-dart](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046452a5f71350a6e416acbc579b192225c330a8d3ffd2e95682c2f7ac42eff181e)        |
| .NET (pure C# impl.)    | [grpc-dotnet](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e1f51a01b3ca1a7dc91cbe904c2aec43eefe513d49fded135184b0ba9ad8e6ef)    |



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)