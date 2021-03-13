# Azure RTOS LevelX

LevelX provides NAND and NOR flash wear leveling facilities to embedded applications. Since both NAND and NOR flash memory can only be erased a finite number of times, it’s critical to distribute the flash memory use evenly. This is typically called “wear leveling” and is the purpose behind LevelX. LevelX presents to the user an array of logical sectors that are mapped to physical flash memory inside of LevelX. Applications may use LevelX in conjunction with FileX or may read/write logical sectors directly. LevelX is designed for fault tolerance. Flash updates are performed in a multiple-step process that can be interrupted in each step. LevelX automatically recovers to the optimal state during the next operation.

## Documentation

Documentation for this library can be found here: http://docs.microsoft.com/azure/rtos/levelx

# Understanding inter-component dependencies

The main components of Azure RTOS are each provided in their own repository, but there are dependencies between them--shown in the following graph--that are important to understand when setting up your builds.

![dependency graph](docs/deps.png)

# Building and using the library

## Prerequisites

Install the following tools:

* [CMake](http://u.720life.cn/g/a75d52cde9c3226230e6270162b9978e4289275ddb318c75375ef56dc75bb47a)  version 3.0 or later
* [GCC compilers for arm-none-eabi](http://u.720life.cn/g/a69e8f5dba5b4106ccc3875c547b1484947bab7f1df436f5d8aedf1534052d3347a6372e2974625b72c74abb36761c41cec7badbf980db0f46ccb245264387f498f37c793a865bb75add58c5598cc9d84c2c0e3888156ddcba266eed37c670c9ca5a3a1780bd6b44c276a2fa627bad63) 
* [Ninja](http://u.720life.cn/g/89745e0265f2e936993296700045dd170be34bb1c79b3be61aa80d559bdace47) 

## Cloning the repo

```bash
$ git clone https://github.com/azure-rtos/levelx.git
```

## Building as a static library

Each component of Azure RTOS comes with a composible CMake-based build system that supports many different MCUs and host systems. Integrating any of these components into your device app code is as simple as adding a git submodule and then including it in your build using the CMake command `add_subdirectory()`.

While the typical usage pattern is to include threadx into your device code source tree to be built & linked with your code, you can compile this project as a standalone static library to confirm your build is set up correctly.

```bash
$ cmake -Bbuild -DCMAKE_TOOLCHAIN_FILE=cmake/cortex_m4.cmake -GNinja .

$ cmake --build ./build
```

NOTE: You will have to take the dependency graph above into account when building anything other than threadx itself.

# Repository Structure and Usage

## Branches & Releases

The master branch has the most recent code with all new features and bug fixes. It does not represent the latest General Availability (GA) release of the library.

## Releases

Each official release (preview or GA) will be tagged to mark the commit and push it into the Github releases tab, e.g. `v6.0-rel`.

## Directory layout

```
- cmake
- common
  - inc
  - src
- samples
```

# Security

Azure RTOS provides OEMs with components to secure communication and to create code and data isolation using underlying MCU/MPU hardware protection mechanisms. It is ultimately the responsibility of the device builder to ensure the device fully meets the evolving security requirements associated with its specific use case.

# Contribution, feedback and issues

If you encounter any bugs, have suggestions for new features or if you would like to become an active contributor to this project please follow the instructions provided in the contribution guideline for the corresponding repo.

For general support, please post a question to [Stack Overflow](http://u.720life.cn/g/ddb1c8aa997182cb1a4af16f7df394520a2863231ad8d7352308cd295ccf0ae9a477f6a00ad50549643e0302391c59e687033897cf935aeb708defd70ea4889b)  using the `threadx` and `azure-rtos` tags.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)