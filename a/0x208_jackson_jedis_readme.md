[![Build Status](https://travis-ci.org/xetorthio/jedis.png?branch=master)](https://travis-ci.org/xetorthio/jedis)

# Jedis

Jedis is a blazingly small and sane [Redis](http://u.720life.cn/g/f6754e90a70fcffec3c12b5e1e01b2d3fa7400de2fbf5c6f2a2eb33acd6b5337  "Redis") java client.

Jedis was conceived to be EASY to use.

Jedis is fully compatible with redis 2.8.x and 3.0.x.

## Community

Meet us on IRC: ##jedis on freenode.net

Join the mailing-list at [http://groups.google.com/group/jedis_redis](http://u.720life.cn/g/92946f42bc9470f8655236cc83ba3a8d646da254b7a4a95258f2953aeae85ba212130e4590bddc6ecd4612d3d7293dd0) 

## So what can I do with Jedis?
All of the following redis features are supported:

- Sorting
- Connection handling
- Commands operating on any kind of values
- Commands operating on string values
- Commands operating on hashes
- Commands operating on lists
- Commands operating on sets
- Commands operating on sorted sets
- Transactions
- Pipelining
- Publish/Subscribe
- Persistence control commands
- Remote server control commands
- Connection pooling
- Sharding (MD5, MurmurHash)
- Key-tags for sharding
- Sharding with pipelining
- Scripting with pipelining
- Redis Cluster

## How do I use it?

You can download the latest build at: 
    http://github.com/xetorthio/jedis/releases

Or use it as a maven dependency:

```xml
 
     redis.clients 
     jedis 
     2.7.2 
     jar 
     compile 
 
```

To use it just:
    
```java
Jedis jedis = new Jedis("localhost");
jedis.set("foo", "bar");
String value = jedis.get("foo");
```

For more usage examples check the tests.

Please check the [wiki](http://u.720life.cn/g/f6754e90a70fcffec3c12b5e1e01b2d3d048dffa5c53a5373cd2f8b13d7bed363f5cf7e23e412620018a3c5ec0839814  "wiki"). There are lots of cool things you should know, including information about connection pooling.

And you are done!

## Jedis Cluster

Redis cluster [specification](http://u.720life.cn/g/f4afcc2808cb8f2d18b502aeb587da196c6b7b7eeb299ece5b8668192ce338122ac3512fe425339736264e34cc3ad2db)  (still under development) is implemented

```java
Set  jedisClusterNodes = new HashSet ();
//Jedis Cluster will attempt to discover cluster nodes automatically
jedisClusterNodes.add(new HostAndPort("127.0.0.1", 7379));
JedisCluster jc = new JedisCluster(jedisClusterNodes);
jc.set("foo", "bar");
String value = jc.get("foo");
```

## FAQ

- Do you have strange stack traces?
- You're getting errors when running jedis in multi-threaded environments?
- Do you need further instructions about pipelining, transactions or sentinel?

Please check the [WIKI](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046542adf33a02b50d9ea34e04f3739d517054ca6756a217a8547aa152d38a243fc)  for more useful information.


## I want to contribute!

That is great!

Please see CONTRIBUTING.md on project's root directory for follow up how to contribute to Jedis project.

Thanks for helping!

## Sponsorship

YourKit supports open source projects with its full-featured Java Profiler.
YourKit, LLC is the creator of [YourKit Java Profiler](http://u.720life.cn/g/0a07e9efd47949eedbe6db3d68f6daf7aa7fcbfe399fed40e3c6f58e6332950c60654d003f3e3352909570a1f9a425e6)  
and [YourKit .NET Profiler](http://u.720life.cn/g/0a07e9efd47949eedbe6db3d68f6daf763ff8b092a153bb07c14b8c70a628a89dac3a18299bf80e9339c66a1128e04d3 
innovative and intelligent tools for profiling Java and .NET applications.

![YourKit Logo](https://cloud.githubusercontent.com/assets/1317309/4507430/7119527c-4b0c-11e4-9245-d72e751e26ee.png)

## License

Copyright (c) 2011 Jonathan Leibiusky

Permission is hereby granted, free of charge, to any person
obtaining a copy of this software and associated documentation
files (the "Software"), to deal in the Software without
restriction, including without limitation the rights to use,
copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following
conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT
HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)