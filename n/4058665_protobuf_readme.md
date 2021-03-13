# Go support for Protocol Buffers

[![GoDev](https://img.shields.io/static/v1?label=godev&message=reference&color=00add8)](https://pkg.go.dev/mod/github.com/golang/protobuf)
[![Build Status](https://travis-ci.org/golang/protobuf.svg?branch=master)](https://travis-ci.org/golang/protobuf)

This module
([`github.com/golang/protobuf`](http://u.720life.cn/g/b8dd2b158752e0f2fe1709927c2f52459a396c1cc27f5615214f444cc2c2336f015727d7e3e50fe9a715252e09bacc3721ccb4760e87155137e5c8e4b15a8e25) 
contains Go bindings for protocol buffers.

It has been superseded by the
[`google.golang.org/protobuf`](http://u.720life.cn/g/b8dd2b158752e0f2fe1709927c2f5245112eb410c63e7191d96c58123e69764d4f89d5b320bec1ecadaf34ffc72ec0a196e4d7ec808c97cac20bbf8684549b2a) 
module, which contains an updated and simplified API,
support for protobuf reflection, and many other improvements.
We recommend that new code use the `google.golang.org/protobuf` module.

Versions v1.4 and later of `github.com/golang/protobuf` are implemented
in terms of `google.golang.org/protobuf`.
Programs which use both modules must use at least version v1.4 of this one.

See the
[developer guide for protocol buffers in Go](http://u.720life.cn/g/a69e8f5dba5b4106ccc3875c547b1484120e1b6e143b62a1baf04add452c89904c84868b2b683c1ee4b0558b9f1894935481b60cd5abe65798e8e1ae3ef1ffaf) 
for a general guide for how to get started using protobufs in Go.

See
[release note documentation](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464dcd23893803aecc02130a4671260c2d27290ccc2a2ee071826b27b1de029d96) 
for more information about individual releases of this project.

See
[documentation for the next major revision](http://u.720life.cn/g/b8dd2b158752e0f2fe1709927c2f5245112eb410c63e7191d96c58123e69764d4f89d5b320bec1ecadaf34ffc72ec0a196e4d7ec808c97cac20bbf8684549b2a) 
for more information about the purpose, usage, and history of this project.

## Package index

Summary of the packages provided by this module:

*   [`proto`](http://u.720life.cn/g/b8dd2b158752e0f2fe1709927c2f5245ffa8b572c633cb27e0c1fe81a118baf90a80af5d67619f963999a55a305c70fe9656d84ed62633d26bea18f15eec900e  Package
    `proto` provides functions operating on protobuf messages such as cloning,
    merging, and checking equality, as well as binary serialization and text
    serialization.
*   [`jsonpb`](http://u.720life.cn/g/b8dd2b158752e0f2fe1709927c2f5245ffa8b572c633cb27e0c1fe81a118baf92570da330e60f4bdf5b5b7d9563a0a328707c88cadc90a93d96dad94e8a360a5  Package
    `jsonpb` serializes protobuf messages as JSON.
*   [`ptypes`](http://u.720life.cn/g/b8dd2b158752e0f2fe1709927c2f5245ffa8b572c633cb27e0c1fe81a118baf919d0354b1ef8629e916219bb29fe6a19c9c30e14de9c296859f6142df0de0c80  Package
    `ptypes` provides helper functionality for protobuf well-known types.
*   [`ptypes/any`](http://u.720life.cn/g/b8dd2b158752e0f2fe1709927c2f5245ffa8b572c633cb27e0c1fe81a118baf919d0354b1ef8629e916219bb29fe6a196a9a4593323f73f98f86bb651dc909b1 
    Package `any` is the generated package for `google/protobuf/any.proto`.
*   [`ptypes/empty`](http://u.720life.cn/g/b8dd2b158752e0f2fe1709927c2f5245ffa8b572c633cb27e0c1fe81a118baf919d0354b1ef8629e916219bb29fe6a19650c7b281a6cb0c8c322230da01b6b11 
    Package `empty` is the generated package for `google/protobuf/empty.proto`.
*   [`ptypes/timestamp`](http://u.720life.cn/g/b8dd2b158752e0f2fe1709927c2f5245ffa8b572c633cb27e0c1fe81a118baf919d0354b1ef8629e916219bb29fe6a19e616af843d2704aa68f04a19ca051d1b 
    Package `timestamp` is the generated package for
    `google/protobuf/timestamp.proto`.
*   [`ptypes/duration`](http://u.720life.cn/g/b8dd2b158752e0f2fe1709927c2f5245ffa8b572c633cb27e0c1fe81a118baf919d0354b1ef8629e916219bb29fe6a19331a0d136297e96d5ac386cec9485857 
    Package `duration` is the generated package for
    `google/protobuf/duration.proto`.
*   [`ptypes/wrappers`](http://u.720life.cn/g/b8dd2b158752e0f2fe1709927c2f5245ffa8b572c633cb27e0c1fe81a118baf919d0354b1ef8629e916219bb29fe6a191ad64ecd0ef3aaac85e1909f3594fc39 
    Package `wrappers` is the generated package for
    `google/protobuf/wrappers.proto`.
*   [`ptypes/struct`](http://u.720life.cn/g/b8dd2b158752e0f2fe1709927c2f5245ffa8b572c633cb27e0c1fe81a118baf919d0354b1ef8629e916219bb29fe6a193d27874cf11f320b28f8f7b2d92d5799 
    Package `structpb` is the generated package for
    `google/protobuf/struct.proto`.
*   [`protoc-gen-go/descriptor`](http://u.720life.cn/g/b8dd2b158752e0f2fe1709927c2f5245ffa8b572c633cb27e0c1fe81a118baf90a80af5d67619f963999a55a305c70fecc188ee811d97ed94df21e244ba7ca5f4ed9e39cde17090b2cdcdd628899faf5 
    Package `descriptor` is the generated package for
    `google/protobuf/descriptor.proto`.
*   [`protoc-gen-go/plugin`](http://u.720life.cn/g/b8dd2b158752e0f2fe1709927c2f5245ffa8b572c633cb27e0c1fe81a118baf90a80af5d67619f963999a55a305c70febb6751963c8c0dcb6cce98ee03149fa10c17da4185192418ac11711e7c78a9ba 
    Package `plugin` is the generated package for
    `google/protobuf/compiler/plugin.proto`.
*   [`protoc-gen-go`](http://u.720life.cn/g/b8dd2b158752e0f2fe1709927c2f5245ffa8b572c633cb27e0c1fe81a118baf90a80af5d67619f963999a55a305c70fec8c9f4a43b1449830971d45155f23a42 
    The `protoc-gen-go` binary is a protoc plugin to generate a Go protocol
    buffer package.

## Reporting issues

The issue tracker for this project
[is located here](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464dcd23893803aecc02130a4671260c2d2bcc068744e2e63bb6d181dfc7bcc34e 

Please report any issues with a sufficient description of the bug or feature
request. Bug reports should ideally be accompanied by a minimal reproduction of
the issue. Irreproducible bugs are difficult to diagnose and fix (and likely to
be closed after some period of time). Bug reports must specify the version of
the
[Go protocol buffer module](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e23171da61222ff06a858c32899f5eacd334028bc8565bfe344e3314889226b68e52446f6350dba64fe3d46c02d4244a) 
and also the version of the
[protocol buffer toolchain](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e23171da61222ff06a858c32899f5eac048192d20ed7150dfa66c4fd11121a031a9cbb1200e825daa27e89852347c4a4) 
being used.

## Contributing

This project is open-source and accepts contributions. See the
[contribution guide](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464dcd23893803aecc02130a4671260c2ddb649efc8169a5292e60b4e7d0652e1bf6346ce2d381d3ec620b3025c87fafea) 
for more information.

## Compatibility

This module and the generated code are expected to be stable over time. However,
we reserve the right to make breaking changes without notice for the following
reasons:

*   **Security:** A security issue in the specification or implementation may
    come to light whose resolution requires breaking compatibility. We reserve
    the right to address such issues.
*   **Unspecified behavior:** There are some aspects of the protocol buffer
    specification that are undefined. Programs that depend on unspecified
    behavior may break in future releases.
*   **Specification changes:** It may become necessary to address an
    inconsistency, incompleteness, or change in the protocol buffer
    specification, which may affect the behavior of existing programs. We
    reserve the right to address such changes.
*   **Bugs:** If a package has a bug that violates correctness, a program
    depending on the buggy behavior may break if the bug is fixed. We reserve
    the right to fix such bugs.
*   **Generated additions**: We reserve the right to add new declarations to
    generated Go packages of `.proto` files. This includes declared constants,
    variables, functions, types, fields in structs, and methods on types. This
    may break attempts at injecting additional code on top of what is generated
    by `protoc-gen-go`. Such practice is not supported by this project.
*   **Internal changes**: We reserve the right to add, modify, and remove
    internal code, which includes all unexported declarations, the
    [`generator`](http://u.720life.cn/g/b8dd2b158752e0f2fe1709927c2f5245ffa8b572c633cb27e0c1fe81a118baf90a80af5d67619f963999a55a305c70fe6957dc284bd238af77ed6e778723a7c8cb5f2e8f87c9e48d6978255c987f0d8f) 
    package, and all packages under
    [`internal`](http://u.720life.cn/g/b8dd2b158752e0f2fe1709927c2f5245ffa8b572c633cb27e0c1fe81a118baf90d34de9e8ff3ffae00d414dc7223abad71358d0eac3af0c07f92d4a9bea5284a 

Any breaking changes outside of these will be announced 6 months in advance to
[protobuf@googlegroups.com](http://u.720life.cn/g/941693b557d072bb769494a6a61fcd979ee9fee4d4fd0c2a6b8a30bc68eade214e13a20b018ccc41bdcf3e0564dccb3fa1170a00ca57cde6ef0dfc3b100c145e 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)