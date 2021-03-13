 

   
     
     

   
     
       
     
     
       
     
     
       
     
   
   
     
       
     
     
       
     
     
       
     
     
       
     
     
       
     
   

   A glib-like cross-platform C library 
 

## Introduction ([中文](/README_zh.md))

TBOX is a glib-like cross-platform C library that is simple to use yet powerful in nature.

The project focuses on making C development easier and provides many modules (.e.g stream, coroutine, regex, container, algorithm ...), 
so that any developer can quickly pick it up and enjoy the productivity boost when developing in C language.

It supports the following platforms:

- Windows
- Macosx
- Linux
- Android
- iOS

And it provides many compiling options using [xmake](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304686d020c7eedf15e0fde31b8d1df57a871f012ff64f346d283d53280e6581fdc4 

* Release: Disable debug information, assertion, memory checking and enable optimization.
* Debug: Enable debug information, assertion, memory checking and disable optimization.
* Small: Disable all extensional modules and enable space optimization.
* Micro: compiling micro library (~64K) for the embed system.

If you want to know more, please refer to:

* [HomePage](http://u.720life.cn/g/75a639d0ee98d7a448ed2dfa4621e70b6242cb21f61d3efae26fdcf3d3a8c999) 
* [Documents](http://u.720life.cn/g/a67a193113c300343644bb41a9d13d577ae3f178d9f0ef788f20b67a262b298cd5b25c951fdd2b330533ec6664959b71) 
* [Github](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304657d8efa05c681e2a08f08f2bae66e5cd) 
* [Gitee](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e174a006e3529030e8b9e7fbbe7cabc1e) 

## Features

#### The stream library

- Supports file, data, http and socket source
- Supports the stream filter for gzip, charset and...
- Implements stream transfer
- Implements the static buffer stream for parsing data
- Supports coroutine and implements asynchronous operation

#### The coroutine library 

- Provides high-performance coroutine switch
- Supports arm, arm64, x86, x86_64 ..
- Provides channel interfaces
- Provides semaphore and lock interfaces
- Supports io socket and stream operation in coroutine
- Provides some io servers (http ..) using coroutine
- Provides stackfull and stackless coroutines
- Support epoll, kqueue, poll, select and IOCP
- Support to wait pipe, socket and process in coroutine and poller at same time

#### The database library

- Supports mysql and sqlite3 database and enumerates data using the iterator mode

#### The xml parser library

- Supports DOM and SAX mode and Supports xpath

#### The serialization and deserialization library

- Supports xml, json, bplist, xplist, binary formats

#### The memory library

- Implements some memory pools for optimizing memory
- Supports fast memory error detecting. it can detect the following types of bugs for the debug mode:
  - out-of-bounds accesses to heap and globals
  - use-after-free
  - double-free, invalid free
  - memory leaks

#### The container library

- Implements hash table, single list, double list, vector, stack, queue
  and min/max heap. Supports iterator mode for algorithm

#### The algorithm library

- Uses the iterator mode
- Implements find, binary find and reverse find algorithm
- Implements sort, bubble sort, quick sort, heap sort and insert sort algorithm
- Implements count, walk items, reverse walk items, for_all and rfor_all

#### The network library

- Implements dns(cached)
- Implements ssl(openssl, polarssl, mbedtls)
- Implements http
- Implements cookies
- Supports ipv4, ipv6
- Supports coroutine

#### The platform library

- Implements timer, fast and low precision timer
- Implements atomic and atomic64 operation
- Implements spinlock, mutex, event, semaphore, thread and thread pool 
- Implements file, socket operation
- Implements poller using epoll, poll, select, kqueue ...
- Implements switch context interfaces for coroutine

#### The charset library

- Supports utf8, utf16, gbk, gb2312, uc2 and uc4
- Supports big endian and little endian mode

#### The zip library

- Supports gzip, zlibraw, zlib formats using the zlib library if exists
- Implements lzsw, lz77 and rlc algorithm

#### The utils library

- Implements base32, base64 encoder and decoder
- Implements assert and trace output for the debug mode
- Implements bits operation for parsing u8, u16, u32, u64 data

#### The math library

- Implements random generator
- Implements fast fixed-point calculation, Supports 6-bits, 16-bits, 30-bits fixed-point number

#### The libc library

- Implements lightweight libc library interfaces, the interface name contains `tb_xxx` prefix for avoiding conflict
- Implements strixxx strrxxx wcsixxx wcsrxxx interface extension
- Optimizes some frequently-used interface, .e.g. memset, memcpy, strcpy ... 
- Implements `memset_u16`, `memset_u32`, `memset_u64` extension interfaces

#### The libm library

- Implements lightweight libm library interfaces, the interface name contains `tb_xxx` prefix for avoiding conflict
- Supports float and double type

#### The regex library

- Supports match and replace
- Supports global/multiline/caseless mode
- Uses pcre, pcre2 and posix regex modules

#### The hash library

- Implements crc32, adler32, md5 and sha1 hash algorithm
- Implements some string hash algorithms (.e.g bkdr, fnv32, fnv64, sdbm, djb2, rshash, aphash ...)
- Implements uuid generator

## Projects

Some projects using tbox:

* [gbox](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466424aa5b40cf746504b4ea5c47c23c9d) 
* [vm86](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a592dbb566eb4e33ab545a174182d754) 
* [xmake](http://u.720life.cn/g/81388e611fe593863c440490cca8c5ca999e2dfe6a800ee4a26a178ba12d9dea) 
* [itrace](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f0e4a5d2c276da7dc1e4a69f9ee53985) 
* [more](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460d44b0b9b02705ead36ae477d0620eabe00c7284c07129b7df3468e2ec2ec164) 

## Build

Please install xmake first: [xmake](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304686d020c7eedf15e0fde31b8d1df57a875c1c3c733825798e96ec7cd6d9a7465b) 

```console
# build for the host platform
$ cd ./tbox
$ xmake

# build for the mingw platform
$ cd ./tbox
$ xmake f -p mingw --sdk=/home/mingwsdk 
$ xmake

# build for the iphoneos platform
$ cd ./tbox
$ xmake f -p iphoneos 
$ xmake

# build for the android platform
$ cd ./tbox
$ xmake f -p android --ndk=xxxxx
$ xmake

# build for the linux cross-platform
$ cd ./tbox
$ xmake f -p linux --sdk=/home/sdk # --bin=/home/sdk/bin
$ xmake
```
    
## Example

```c
#include "tbox/tbox.h"

int main(int argc, char** argv)
{
    // init tbox
    if (!tb_init(tb_null, tb_null)) return 0;

    // trace
    tb_trace_i("hello tbox");

    // init vector
    tb_vector_ref_t vector = tb_vector_init(0, tb_element_cstr(tb_true));
    if (vector)
    {
        // insert item
        tb_vector_insert_tail(vector, "hello");
        tb_vector_insert_tail(vector, "tbox");

        // dump all items
        tb_for_all (tb_char_t const*, cstr, vector)
        {
            // trace
            tb_trace_i("%s", cstr);
        }

        // exit vector
        tb_vector_exit(vector);
    }

    // init stream
    tb_stream_ref_t stream = tb_stream_init_from_url("http://www.xxx.com/file.txt");
    if (stream)
    {
        // open stream
        if (tb_stream_open(stream))
        {
            // read line
            tb_long_t size = 0;
            tb_char_t line[TB_STREAM_BLOCK_MAXN];
            while ((size = tb_stream_bread_line(stream, line, sizeof(line))) >= 0)
            {
                // trace
                tb_trace_i("line: %s", line);
            }
        }

        // exit stream
        tb_stream_exit(stream);
    }

    // wait 
    tb_getchar();

    // exit tbox
    tb_exit();
    return 0;
}
```

## Contacts

* Email：[waruqi@gmail.com](mailto:waruqi@gmail.com)
* Homepage：[tboox.org](http://u.720life.cn/g/75a639d0ee98d7a448ed2dfa4621e70b6242cb21f61d3efae26fdcf3d3a8c999) 
* Community：[/r/tboox on reddit](http://u.720life.cn/g/c0dd3a2651b78798f89b1013814805623f1a63a6d905c15df72e472aa578981e) 
* ChatRoom：[Char on telegram](http://u.720life.cn/g/81b3001eda94fccf5f7753bb8378abc1c14544ef12aef5cc493612fa30a7737e  [Chat on gitter](http://u.720life.cn/g/11e95d0ed8d2826912e12fe1dc3f34213d053b7442ea437e8b47413e3457277d000d09d75a2b772c5816d6481f2d12ab86e9cc0202de789836269a74804e7434e4cbc98a75c1b924ec462db53c440da0c31d568070b9860bb1d51047347f379bad8b60e37e43c96c50a4aadddad62766) 
* QQ Group: 343118190(full), 662147501
* Wechat Public: tboox-os

## Backers

Thank you to all our backers! 🙏 [[Become a backer](http://u.720life.cn/g/df0d0b49c04f66c9033e4268d2ee0e122716ad212b50d73e016ecc2275a50272a06f1909bd65490eb380da03a43cf809 

   

## Sponsors

Support this project by becoming a sponsor. Your logo will show up here with a link to your website. [[Become a sponsor](http://u.720life.cn/g/df0d0b49c04f66c9033e4268d2ee0e122716ad212b50d73e016ecc2275a50272a3354575b156d2ec99e524b2aa01471f 

   
   
   
   
   
   
   
   
   
   




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)