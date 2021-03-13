EasyExcel
======================
[![Build Status](https://travis-ci.org/alibaba/easyexcel.svg?branch=master)](https://travis-ci.org/alibaba/easyexcel)
[![Maven central](https://maven-badges.herokuapp.com/maven-central/com.alibaba/easyexcel/badge.svg)](https://maven-badges.herokuapp.com/maven-central/com.alibaba/easyexcel)
[![License](http://img.shields.io/:license-apache-brightgreen.svg)](http://www.apache.org/licenses/LICENSE-2.0.html)

[QQ群: 662022184](//shang.qq.com/wpa/qunwpa?idkey=53d9d821b0833e3c14670f007488a61e300f00ff4f1b81fd950590d90dd80f80)
[钉钉群: 21960511](http://u.720life.cn/g/f4cacde5dcb7e13d8784a8a69e169ce4f7521c8c01cc47de4ae1c48a340147eb22d87959ab18800fd6d425e13e26cd03f60ae025047e5e822b723d5041430818899ef75e81d86a25f7cb9d7a95c7c95cc2974126e45ff942a464c6d8cc912ce2104d1a6807cdb6c9de3d492bf5a045eb30ce60579d35ee8e0710f550388b82cd) 

[官方网站: https://yuque.com/easyexcel](http://u.720life.cn/g/794be49a28e6f6b6aa755de579be43d973c4d3addf1b87dd75f1e70a9ac2722c22e239e9a29404e0d8fd37caeca7eedf) 

[常见问题](http://u.720life.cn/g/794be49a28e6f6b6aa755de579be43d973c4d3addf1b87dd75f1e70a9ac2722ce584279f244268839cc7c23973fd3cf6) 
#### 因为公司不方便用QQ，所以建议加钉钉群

# JAVA解析Excel工具EasyExcel
Java解析、生成Excel比较有名的框架有Apache poi、jxl。但他们都存在一个严重的问题就是非常的耗内存，poi有一套SAX模式的API可以一定程度的解决一些内存溢出的问题，但POI还是有一些缺陷，比如07版Excel解压缩以及解压后存储都是在内存中完成的，内存消耗依然很大。easyexcel重写了poi对07版Excel的解析，能够原本一个3M的excel用POI sax依然需要100M左右内存降低到几M，并且再大的excel不会出现内存溢出，03版依赖POI的sax模式。在上层做了模型转换的封装，让使用者更加简单方便

## 64M内存1分钟内读取75M(46W行25列)的Excel
当然还有急速模式能更快，但是内存占用会在100M多一点
![img](img/readme/large.png)

## 相关文档
* [快速开始](http://u.720life.cn/g/794be49a28e6f6b6aa755de579be43d973c4d3addf1b87dd75f1e70a9ac2722c22e239e9a29404e0d8fd37caeca7eedf) 
* [关于软件](/abouteasyexcel.md)
* [更新记事](/update.md)
* [贡献代码](http://u.720life.cn/g/794be49a28e6f6b6aa755de579be43d973c4d3addf1b87dd75f1e70a9ac2722c6a47853be5c0783a01f28f46409a3436) 

## 维护者
玉霄、庄家钜、怀宇
## 快速开始
### 读Excel
DEMO代码地址：[https://github.com/alibaba/easyexcel/blob/master/src/test/java/com/alibaba/easyexcel/demo/read/ReadTest.java](/src/test/java/com/alibaba/easyexcel/test/demo/read/ReadTest.java)

```java
    /**
     * 最简单的读
     *  1. 创建excel对应的实体对象 参照{@link DemoData}
     *  2. 由于默认一行行的读取excel，所以需要创建excel一行一行的回调监听器，参照{@link DemoDataListener}
     *  3. 直接读即可
     */
    @Test
    public void simpleRead() {
        String fileName = TestFileUtil.getPath() + "demo" + File.separator + "demo.xlsx";
        // 这里 需要指定读用哪个class去读，然后读取第一个sheet 文件流会自动关闭
        EasyExcel.read(fileName, DemoData.class, new DemoDataListener()).sheet().doRead();
    }
```

### 写Excel
DEMO代码地址：[https://github.com/alibaba/easyexcel/blob/master/src/test/java/com/alibaba/easyexcel/test/demo/write/WriteTest.java](/src/test/java/com/alibaba/easyexcel/test/demo/write/WriteTest.java)
```java
    /**
     * 最简单的写
     *  1. 创建excel对应的实体对象 参照{@link com.alibaba.easyexcel.test.demo.write.DemoData}
     *  2. 直接写即可
     */
    @Test
    public void simpleWrite() {
        String fileName = TestFileUtil.getPath() + "write" + System.currentTimeMillis() + ".xlsx";
        // 这里 需要指定写用哪个class去读，然后写到第一个sheet，名字为模板 然后文件流会自动关闭
        // 如果这里想使用03 则 传入excelType参数即可
        EasyExcel.write(fileName, DemoData.class).sheet("模板").doWrite(data());
    }
```

### web上传、下载
DEMO代码地址：[https://github.com/alibaba/easyexcel/blob/master/src/test/java/com/alibaba/easyexcel/test/demo/web/WebTest.java](/src/test/java/com/alibaba/easyexcel/test/demo/web/WebTest.java)
```java
 /**
     * 文件下载（失败了会返回一个有部分数据的Excel）
     *  1. 创建excel对应的实体对象 参照{@link DownloadData}
     *  2. 设置返回的 参数
     *  3. 直接写，这里注意，finish的时候会自动关闭OutputStream,当然你外面再关闭流问题不大
     */
    @GetMapping("download")
    public void download(HttpServletResponse response) throws IOException {
        // 这里注意 有同学反应使用swagger 会导致各种问题，请直接用浏览器或者用postman
        response.setContentType("application/vnd.ms-excel");
        response.setCharacterEncoding("utf-8");
        // 这里URLEncoder.encode可以防止中文乱码 当然和easyexcel没有关系
        String fileName = URLEncoder.encode("测试", "UTF-8");
        response.setHeader("Content-disposition", "attachment;filename=" + fileName + ".xlsx");
        EasyExcel.write(response.getOutputStream(), DownloadData.class).sheet("模板").doWrite(data());
    }

    /**
     * 文件上传
     *  1. 创建excel对应的实体对象 参照{@link UploadData}
     *  2. 由于默认一行行的读取excel，所以需要创建excel一行一行的回调监听器，参照{@link UploadDataListener}
     *  3. 直接读即可
     */
    @PostMapping("upload")
    @ResponseBody
    public String upload(MultipartFile file) throws IOException {
        EasyExcel.read(file.getInputStream(), UploadData.class, new UploadDataListener(uploadDAO)).sheet().doRead();
        return "success";
    }
```
### 联系我们
有问题阿里同事可以通过钉钉找到我，阿里外同学可以通过git留言。其他技术非技术相关的也欢迎一起探讨。
### 招聘&交流
阿里巴巴新零售事业部--诚招JAVA资深开发、技术专家。有意向可以微信联系，简历可以发我邮箱jipengfei.jpf@alibaba-inc.com



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)