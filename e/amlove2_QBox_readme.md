
# ![Qbox logo](http://otwcctfiu.bkt.clouddn.com/logo-blue.png)


> QBox is a convenient manage tool for your [Qiniu](http://u.720life.cn/g/aca7767ed952af2935266b72d4ea39a5c7e8880f7b3f45bc4eebd1934a2fe336)  buckets. It is an open-source software and can be used on `OS X`, `Linux` and `Windows`, and it was generated with [electron-vue](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304665f0ca54dc3ddccd0c4489a7f153719d038ce828418c33b0a65285c359bf9285) 

## Screenshots

#### Bucket Panel

![bucket panel](http://otwcctfiu.bkt.clouddn.com/bucket-panel.png)

#### Manage Panel

![bucket panel](http://otwcctfiu.bkt.clouddn.com/manage-panel.png)

#### Upload Panel

![bucket panel](http://otwcctfiu.bkt.clouddn.com/upload-panel.png)

## Feature

#### Bucket Panel

- [x] Login by setting `accessKey` and `secretKey`.
- [x] Logout by clearing localStorage (include `accessKey` and `secretKey`).
- [x] List all buckets (include private).
- [x] Manage files in a bucket, that will open a new `Manage Panel`.

#### Manage Panel

- [x] List all files in a specified bucket.
- [x] List all files with pagination.
- [x] Sort by `file name`, `file type`, `file size` or `modified time`.
- [x] Preview `image` and `media` file.
- [x] Delete a existing file.
- [x] Delete a batch of files were checked.
- [x] Copy the outer link of a file.
- [x] Refresh the files in the bucket.
- [x] Download a existing file.(this feature will be put in `preview` modal)
- [x] Upload a single file. 
- [x] Search filter.

## TODO

#### MenuBar

- [ ] Set default bucket.
- [ ] Drag to MenuBar icon to upload.

#### Bucket Panel

- [ ] Delete a existing bucket.
- [ ] Create a new bucket.

#### Manage Panel

- [x] Add enter event to search box.
- [ ] Upload mutiple files.
- [ ] Download a batch of files were checked.
- [ ] Rename resouces.

## License

[AGPL](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465cc9f67616ec3ce123e5c60c6c6ff8b03d90b243552f119b0f8a9620687b011ae1791825fbe76e484f2b776d3c494b93) 

## Contribute

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:9080
npm run dev

# build electron application for production
npm run build

# run unit tests (no tests now)
npm test

# lint all JS/Vue component files in `src/`
npm run lint
```

## [中文文档](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465cc9f67616ec3ce123e5c60c6c6ff8b06f29df52cb5ecaf965009ccd0a03660dafb50c8edaa66723a6a6a6c4ad5d5c68) 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)