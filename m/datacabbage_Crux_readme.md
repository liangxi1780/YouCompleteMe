# Crux

Crux parses Web pages to identify the crux of an article — the very essential points — minus all the
fluff. The library consists of multiple independent APIs. You can pick and choose which ones you
want to use. If you use Crux in an Android app, they are designed to be independent so that Proguard
or other minification tools can strip out the parts you don’t use.

## Article Extraction API

- Rich formatted content available, not just plain text.
- Support for more sites & better parsing overall.
- Support for more metadata formats: OpenGraph, Twitter Cards, Schema.org.
- Small footprint and code size: JSoup is the only required dependency.
- Fewer setters/getters, to keep the method count low (this is important for Android).
- The ability to use HTTP libraries besides the default HttpUrlConnection, such as OkHttp, under
  the hood.
- Cleaner, leaner code (compared to other libraries not optimized for Android)
- First-class support for importing into Android Studio projects via Gradle.
- [![Build Status](https://travis-ci.org/chimbori/crux.svg?branch=master)](https://travis-ci.org/chimbori/crux) Continuous integration with unit tests and golden file tests.  

### Sample Code

In a background thread, make a network request and obtain the `rawHTML` of the page you would like
to analyze.

```java
String url = "https://example.com/article.html";
String rawHTML = "   This is an article   ";

Article article = ArticleExtractor.with(url, rawHTML)
    .extractMetadata()
    .extractContent()  // If you only need metadata, you can skip `.extractContent()`
    .article();
```

On the UI thread:

```java
// Use article.document, article.title, etc.
```

## Image URL Extractor API

From a single DOM Element root, the Image URL API inspects the sub-tree and returns the best
possible image URL candidate available within it. It does this by scanning within the DOM tree
for interesting `src` & `style` tags.

All URLs are resolved as absolute URLs, even if the HTML contained relative URLs.

```java
ImageUrlExtractor.with(url, domElement).findImage().imageUrl();
```

## Anchor Links Extractor API

From a single DOM Element root, the Image URL API inspects the sub-tree and returns the best
possible link URL candidate available within it. It does this by scanning within the DOM tree
for interesting `href` tags.

All URLs are resolved as absolute URLs, even if the HTML contained relative URLs.

```java
LinkUrlExtractor.with(url, domElement).findLink().linkUrl();
```

## URL Heuristics API

This API examines a given URL (without connecting to the server), and returns
heuristically-determined answers to questions such as:

- Is this URL likely a video URL?
- Is this URL likely an image URL?
- Is this URL likely an audio URL?
- Is this URL likely an executable URL?
- Is this URL likely an archive URL?

This API also supports resolving redirects for certain well-known redirectors, with the precondition
that the target URL be available as part of this candidate URL. In other words, this API will
not be able to resolve redirectors that perform a HTTP 301 redirect.

```java
CruxURL cruxUrl = CruxURL.parse("https://example.com/article.html");
cruxUrl.resolveRedirects();
cruxUrl.isLikelyArticle();  // Returns true.
cruxUrl.isLikelyImage();  // Returns false.
```

# Usage

Include Crux in your project, then see sample code for each API provided above.

Crux uses semantic versioning. If the API changes, then the major version will be incremented.
Upgrading from one minor version to the next minor version within the same major version should
not require any client code to be modified.

## Import Crux via Gradle

Project/`build.gradle`:
```groovy
allprojects {
  repositories {
    maven { url "https://jitpack.io" }
  }
}
```

Module/`build.gradle`:

From the [Releases page](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304681511802d15d91f7fc61f9711a94ba637a03a3150da03393bcc355fb69ede246  copy the latest version number
& use it below:

```
dependencies {
  compile 'com.github.chimbori:crux: '
}
```

# History

Crux began as a fork of [Snacktory](http://u.720life.cn/g/f6754e90a70fcffec3c12b5e1e01b2d3a52af5b173efe55324e89f961639c99a83435bff8c02f17c92aea35037ef3087)  with the goal of making
it more performant on Android devices, but it has quickly gained several new features that are not
available in Snacktory.

Snacktory (and thus Crux) borrow ideas and test cases from [Goose](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467a658f5787fecbcd8e6bbd167a901d077834961aa2458f15d7a50591af82e183)  
and [JReadability](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046fe484e2d114f0116f5e400ad113e630db63605bc8308acc61d740caeab5e58d4 

# License

    Copyright 2016, Chimbori, makers of Hermit, the Lite Apps Browser.

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)