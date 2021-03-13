[![Build Status](https://travis-ci.org/ReactiveX/rxjs.svg?branch=master)](https://travis-ci.org/ReactiveX/rxjs)
[![Coverage Status](https://coveralls.io/repos/github/ReactiveX/rxjs/badge.svg?branch=master)](https://coveralls.io/github/ReactiveX/rxjs?branch=master)
[![npm version](https://badge.fury.io/js/%40reactivex%2Frxjs.svg)](http://badge.fury.io/js/%40reactivex%2Frxjs)
[![Join the chat at https://gitter.im/Reactive-Extensions/RxJS](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/Reactive-Extensions/RxJS?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

[![Selenium Test Status](https://saucelabs.com/browser-matrix/rxjs5.svg)](https://saucelabs.com/u/rxjs5)

# RxJS 5 (beta)

Reactive Extensions Library for JavaScript. This is a rewrite of [Reactive-Extensions/RxJS](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046125b952034ae75a43a8307f470de6200432db6b8087ad7b2d231401d87517f12)  and is intended to supersede it once this is ready. This rewrite is meant to have better performance, better modularity, better debuggable call stacks, while staying mostly backwards compatible, with some breaking changes that reduce the API surface.

[Apache 2.0 License](LICENSE.txt)

- [Code of Conduct](CODE_OF_CONDUCT.md)
- [Contribution Guidelines](CONTRIBUTING.md)
- [Maintainer Guidelines](doc/maintainer-guidelines.md)
- [Creating Operators](doc/operator-creation.md)
- [Migrating From RxJS 4 to RxJS 5](MIGRATION.md)
- [API Documentation (WIP)](http://u.720life.cn/g/3c6d873642c48d33a3825c200ca38831599ea7be4f6f9baefd2750479bdad3b9) 

## Important

By contributing or commenting on issues in this repository, whether you've read them or not, you're agreeing to the [Contributor Code of Conduct](CODE_OF_CONDUCT.md). Much like traffic laws, ignorance doesn't grant you immunity.

## Installation and Usage

### ES6 via npm

```sh
npm install rxjs-es
```

To import the entire core set of functionality:

```js
import Rx from 'rxjs/Rx';

Rx.Observable.of(1,2,3)
```

To import only what you need by patching (this is useful for size-sensitive bundling):

```js
import { Observable } from 'rxjs/Observable';
import 'rxjs/add/operator/map';

Observable.of(1,2,3).map(x => x + '!!!'); // etc
```

To import what you need and use it with proposed [bind operator](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046460af53d8b401b051690f5830d6601d98b2f2299529fe31ee9f144fa3134c4bd 

> Note: This additional syntax requires [transpiler support](http://u.720life.cn/g/4b3f91bf9d47cd6e779f43a558035b5bc9ab9cf3ad6f7ea9c6eb20e16605de6134deac48849963c73ee3fda39c25a7b8262303eda1b826338853bb737b07455a)  and this syntax may be completely withdrawn from TC39 without notice! Use at your own risk.

```js
import { Observable } from 'rxjs/Observable';
import { of } from 'rxjs/observable/of';
import { map } from 'rxjs/operator/map';

Observable::of(1,2,3)::map(x => x + '!!!'); // etc
```

### CommonJS via npm

```sh
npm install rxjs
```

Import all core functionality:

```js
var Rx = require('rxjs/Rx');

Rx.Observable.of(1,2,3); // etc
```

Import only what you need and patch Observable (this is useful in size-sensitive bundling scenarios):

```js
var Observable = require('rxjs/Observable').Observable;
// patch Observable with appropriate methods
require('rxjs/add/operator/map');

Observable.of(1,2,3).map(function (x) { return x + '!!!'; }); // etc
```

Import operators and use them _manually_ you can do the following (this is also useful for bundling):

```js
var Observable = require('rxjs/Observable').Observable;
var map = require('rxjs/operator/map').map;

map.call(Observable.of(1,2,3), function (x) { return x + '!!!'; });
```

You can also use the above method to build your own Observable and export it from your own module.


### All Module Types (CJS/ES6/AMD/TypeScript) via npm

To install this library via [npm](http://u.720life.cn/g/920c024f0b8c5aa5e32c4f88af4e6c96e1ac4c199acb8ebb78caf10d83a4d0e4)  **version 3**, use the following command:

```sh
npm install @reactivex/rxjs
```

If you are using npm **version 2** before this library has achieved a stable version, you need to specify the library version explicitly:

```sh
npm install @reactivex/rxjs@5.0.0-beta.1
```

### CDN

For CDN, you can use [unpkg](http://u.720life.cn/g/a37a61a440aa343e38eba02fa2d29d2b276ae04f93213bc34bf20494a3bdf0a6 

5.0.0-beta.1 - 5.0.0-beta.11:

https://unpkg.com/@reactivex/rxjs/dist/global/Rx.umd.js


5.0.0-beta.12 or higher:

https://unpkg.com/@reactivex/rxjs/dist/global/Rx.js

#### Node.js Usage:

```js
var Rx = require('@reactivex/rxjs');

Rx.Observable.of('hello world')
  .subscribe(function(x) { console.log(x); });
```

## Goals

- Provide better performance than preceding versions of RxJS
- To model/follow the [Observable Spec Proposal](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304649191629772c5c4e03ec1b25bbb7580a28c5d7cb002a1c06b611948e3826b651)  to the observable.
- Provide more modular file structure in a variety of formats
- Provide more debuggable call stacks than preceding versions of RxJS

## Building/Testing

The build and test structure is fairly primitive at the moment. There are various npm scripts that can be run:

- build_es6: Transpiles the TypeScript files from `src/` to `dist/es6`
- build_cjs: Transpiles the ES6 files from `dist/es6` to `dist/cjs`
- build_amd: Transpiles the ES6 files from `dist/es6` to `dist/amd`
- build_global: Transpiles/Bundles the CommonJS files from `dist/cjs` to `dist/global/Rx.js`
- build_all: Performs all of the above in the proper order.
- build_test: builds ES6, then CommonJS, then runs the tests with `jasmine`
- build_perf: builds ES6, CommonJS, then global, then runs the performance tests with `protractor`
- build_docs: generates API documentation from `dist/es6` to `dist/docs`
- build_cover: runs `istanbul` code coverage against test cases
- test: runs tests with `jasmine`, must have built prior to running.
- tests2png: generates PNG marble diagrams from test cases.

`npm run info` will list available script.

### Example

```sh
# build all the things!
npm run build_all
```

## Performance Tests

Run `npm run build_perf` or `npm run perf` to run the performance tests with `protractor`.
Run `npm run perf_micro` to run micro performance test benchmarking operator.

## Adding documentation
RxNext uses [ESDoc](http://u.720life.cn/g/07beed3e88e57209b069e60990cdcab46be3261e3e8d3bc538630535f116e714)  to generate API documentation. Refer to ESDoc's documentation for syntax. Run `npm run build_docs` to generate.

## Generating PNG marble diagrams

The script `npm run tests2png` requires some native packages installed locally: `imagemagick`, `graphicsmagick`, and `ghostscript`.

For Mac OS X with [Homebrew](http://u.720life.cn/g/af2cb7974ba29ffbfd8647e25db79703528c9f567a52cb33c4691927e0428678 

- `brew install imagemagick`
- `brew install graphicsmagick`
- `brew install ghostscript`

For Debian Linux:

- `sudo add-apt-repository ppa:dhor/myway`
- `apt-get install imagemagick`
- `apt-get install graphicsmagick`
- `apt-get install ghostscript`

For Windows and other Operating Systems, check the download instructions here:

- http://imagemagick.org
- http://www.graphicsmagick.org
- http://www.ghostscript.com/



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)