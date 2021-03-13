# JsonCpp

[![badge](https://img.shields.io/badge/conan.io-jsoncpp%2F1.8.0-green.svg?logo=data:image/png;base64%2CiVBORw0KGgoAAAANSUhEUgAAAA4AAAAOCAMAAAAolt3jAAAA1VBMVEUAAABhlctjlstkl8tlmMtlmMxlmcxmmcxnmsxpnMxpnM1qnc1sn85voM91oM11oc1xotB2oc56pNF6pNJ2ptJ8ptJ8ptN9ptN8p9N5qNJ9p9N9p9R8qtOBqdSAqtOAqtR%2BrNSCrNJ/rdWDrNWCsNWCsNaJs9eLs9iRvNuVvdyVv9yXwd2Zwt6axN6dxt%2Bfx%2BChyeGiyuGjyuCjyuGly%2BGlzOKmzOGozuKoz%2BKqz%2BOq0OOv1OWw1OWw1eWx1eWy1uay1%2Baz1%2Baz1%2Bez2Oe02Oe12ee22ujUGwH3AAAAAXRSTlMAQObYZgAAAAFiS0dEAIgFHUgAAAAJcEhZcwAACxMAAAsTAQCanBgAAAAHdElNRQfgBQkREyOxFIh/AAAAiklEQVQI12NgAAMbOwY4sLZ2NtQ1coVKWNvoc/Eq8XDr2wB5Ig62ekza9vaOqpK2TpoMzOxaFtwqZua2Bm4makIM7OzMAjoaCqYuxooSUqJALjs7o4yVpbowvzSUy87KqSwmxQfnsrPISyFzWeWAXCkpMaBVIC4bmCsOdgiUKwh3JojLgAQ4ZCE0AMm2D29tZwe6AAAAAElFTkSuQmCC)](https://bintray.com/theirix/conan-repo/jsoncpp%3Atheirix)
[![badge](https://img.shields.io/badge/license-MIT-blue)](https://github.com/open-source-parsers/jsoncpp/blob/master/LICENSE)
[![badge](https://img.shields.io/badge/document-doxygen-brightgreen)](http://open-source-parsers.github.io/jsoncpp-docs/doxygen/index.html)
[![Coverage Status](https://coveralls.io/repos/github/open-source-parsers/jsoncpp/badge.svg?branch=master)](https://coveralls.io/github/open-source-parsers/jsoncpp?branch=master)


[JSON][json-org] is a lightweight data-interchange format. It can represent
numbers, strings, ordered sequences of values, and collections of name/value
pairs.

[json-org]: http://json.org/

JsonCpp is a C++ library that allows manipulating JSON values, including
serialization and deserialization to and from strings. It can also preserve
existing comment in unserialization/serialization steps, making it a convenient
format to store user input files.


## Documentation

[JsonCpp documentation][JsonCpp-documentation] is generated using [Doxygen][].

[JsonCpp-documentation]: http://open-source-parsers.github.io/jsoncpp-docs/doxygen/index.html
[Doxygen]: http://www.doxygen.org


## A note on backward-compatibility

* `1.y.z` is built with C++11.
* `0.y.z` can be used with older compilers.
* `00.11.z` can be used both in old and new compilers.
* Major versions maintain binary-compatibility.

### Special note
The branch `00.11.z`is a new branch, its major version number `00` is to show that it is
different from `0.y.z` and `1.y.z`, the main purpose of this branch is to make a balance
between the other two branches. Thus, users can use some new features in this new branch
that introduced in 1.y.z, but can hardly applied into 0.y.z.

## Using JsonCpp in your project

### The vcpkg dependency manager
You can download and install JsonCpp using the [vcpkg](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466924ae96cacdadd6412a45fd836c5d0a8f05c4413460259e1d5d476e2b1fb731)  dependency manager:

    git clone https://github.com/Microsoft/vcpkg.git
    cd vcpkg
    ./bootstrap-vcpkg.sh
    ./vcpkg integrate install
    ./vcpkg install jsoncpp

The JsonCpp port in vcpkg is kept up to date by Microsoft team members and community contributors. If the version is out of date, please [create an issue or pull request](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466924ae96cacdadd6412a45fd836c5d0a013254843412120db8b708f68faedafd)  on the vcpkg repository.

### Amalgamated source
https://github.com/open-source-parsers/jsoncpp/wiki/Amalgamated-(Possibly-outdated)

### The Meson Build System
If you are using the [Meson Build System](http://u.720life.cn/g/e4001369c670c248c2f4ca52b191348e5cbaefead9be5f15c678d93b03f7f5ea  then you can get a wrap file by downloading it from [Meson WrapDB](http://u.720life.cn/g/d9b966c89be6cb128eee89140fb722a45217b987130cfb99ae77c083de7ae11e6379966b4d939bccbb3d74f6b3daec1c  or simply use `meson wrap install jsoncpp`.

### Other ways
If you have trouble, see the [Wiki](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a03e7f134bbe1a72f4e0627dfc5ba9f5dd94231b24be16c2e13ea386dba433268c636bbc52850be0bed9dcd91cc47dde  or post a question as an Issue.

## License

See the `LICENSE` file for details. In summary, JsonCpp is licensed under the
MIT license, or public domain if desired and recognized in your jurisdiction.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)