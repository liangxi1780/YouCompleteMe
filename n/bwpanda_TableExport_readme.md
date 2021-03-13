[![TableExport](/Hero.png)](https://tableexport.travismclarke.com)

 
 

[![NPM release](https://img.shields.io/npm/v/tableexport.svg)](https://www.npmjs.com/package/tableexport)
[![Build Status](https://travis-ci.org/clarketm/TableExport.svg?branch=master)](https://travis-ci.org/clarketm/TableExport)
[![Downloads](https://img.shields.io/npm/dt/tableexport.svg)]()
[![License](https://img.shields.io/npm/l/tableexport.svg)]()

## Docs

- [Migrating from **3.x** to **4.x**?](MIGRATING_v3_to_v4.md)
- [Migrating from **4.x** to **5.x**?](MIGRATING_v4_to_v5.md)
- [`v3` docs](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90e1b0c89b2317754fd6fb4e35b3feb3cdd)  and [README](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c474d571170fc6871651af8b56097b1137c6ab05517386d3c6e683d8cd6e80587efeaa9ce97f2b06558662b08d9fcd87e7ef5ca39aed8a3289f212408646eab5 
- [`v4` docs](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cbe6069e5fe4c27022ad30d970cb7e193ae1d96c48a02ea674bb61677ef7a4c3e62768e3e72186020a9b2d0f02f3aec823)  and [README](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c474d571170fc6871651af8b56097b11cf805bb533b0ae353b9e8012ea25c31f3f83c2f62b38d6cfe81092fd9b71af107dc12d8feeedd3fb462d27cd3247e362 
- [`v5` docs](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cbe6069e5fe4c27022ad30d970cb7e193a175607b68798c20ad47b99e34a512da6)  and [README](#getting-started) (below):

## Getting Started

### Install manually using ` ` tags

To use this library, include the [FileSaver.js](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c244f445a95dcba6d626fe75801b1a1471afd55aef5860436303a946c558dd85)  library, and [TableExport](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cbe6069e5fe4c27022ad30d970cb7e193a8bc89012a009c299ce7f2f1eac8c6296)  library before the closing ` ` tag of your HTML document:

```html
  
...
  
```

### Install with Bower

```shell
$ bower install tableexport.js
```

### Install with npm

```shell
$ npm install tableexport
```

### CDN

#### [unpkg](http://u.720life.cn/g/a37a61a440aa343e38eba02fa2d29d2bd71e4957eec33e870863e727d6c5bbcc) 

|            |                         uncompressed                         |                                                                                                                                 compressed                                                                                                                                 |
| :--------: | :----------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|  **CSS**   | [🔗](http://u.720life.cn/g/a37a61a440aa343e38eba02fa2d29d2bf8b75766c14e95a3c31c7f758444e5ce0ab8453e6ad8ec1d2c6c71764cbe6aed2caae926cc847cb40dfecdfbfc3adacc)  |                                                                                                      [🔗](http://u.720life.cn/g/a37a61a440aa343e38eba02fa2d29d2bf8b75766c14e95a3c31c7f758444e5ce0ab8453e6ad8ec1d2c6c71764cbe6aedf7a06a8350dda26f824a3c4175e7cf85)                                                                                                       |
|   **JS**   |  [🔗](http://u.720life.cn/g/a37a61a440aa343e38eba02fa2d29d2bf8b75766c14e95a3c31c7f758444e5ceabe2d35b41fe149b873214665afc27b26036f37dae40a60589a08f1e8468102a)   |                                                                                                       [🔗](http://u.720life.cn/g/a37a61a440aa343e38eba02fa2d29d2bf8b75766c14e95a3c31c7f758444e5ceabe2d35b41fe149b873214665afc27b28e2bb29f9964b62c1fb19fae13f968c0)                                                                                                        |
| **Images** |                           &mdash;                            | [🔗 xlsx ]https://unpkg.com/tableexport/dist/img/xlsx.svg)[🔗 xls ]https://unpkg.com/tableexport/dist/img/xls.svg)[🔗 csv ]https://unpkg.com/tableexport/dist/img/csv.svg)[🔗 txt ](http://u.720life.cn/g/a37a61a440aa343e38eba02fa2d29d2bf8b75766c14e95a3c31c7f758444e5ce21bc9b1f17a5b9374223b5c591de9dfb)  |

### Dependencies

#### Required:

- [FileSaver.js](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c244f445a95dcba6d626fe75801b1a1471afd55aef5860436303a946c558dd85) 

#### Optional:

- [jQuery](http://u.720life.cn/g/0a8164b4e54fe9c39d5074c1f90b955149e6934088f97327625ec6a05c42e2e1)  (1.2.1 or higher)
- [Bootstrap](http://u.720life.cn/g/e23be2821e5181a1a46a005bc6e93d9dabd141426b0b46d74d9ab3d47ead6054a7b62ea8e6c1387d8d6f37e52e4af1a547e39929bf884b975f363086a29fce03)  (3.1.0 or higher)

#### Add-Ons:

In order to provide **Office Open XML SpreadsheetML Format ( `.xlsx` )** support, you must include the following third-party library in your project before both [FileSaver.js](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c244f445a95dcba6d626fe75801b1a1471afd55aef5860436303a946c558dd85)  and [TableExport](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cbe6069e5fe4c27022ad30d970cb7e193ad5665f4ff26fe13d46c1dc8ce88542d7 

- [xlsx.core.js](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460b881e3e6b319519ab1a30be8fde2103f480239f676e04c8643f9e64ea3ba3cb)  by _SheetJS_

> Including `xlsx.core.js` is **NOT** necessary if installing with [`Bower`](#install-with-bower) or [`npm`](#install-with-npm)

```html
  
  
...
  
```

#### Older Browsers:

To support legacy browsers ( **Chrome**   Including `Blob.js` is **NOT** necessary if installing with [`Bower`](#install-with-bower) or [`npm`](#install-with-npm)

```html
  
  
...
  
```

## Usage

### JavaScript

To use this library, simple call the [`TableExport`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cbe6069e5fe4c27022ad30d970cb7e193a8bc89012a009c299ce7f2f1eac8c6296)  constructor:

```js
new TableExport(document.getElementsByTagName("table"));

// OR simply

TableExport(document.getElementsByTagName("table"));

// OR using jQuery

$("table").tableExport();
```

Additional properties can be passed-in to customize the look and feel of your tables, buttons, and exported data.

Notice that by default, TableExport will create export buttons for three different filetypes _`xls`, `csv`, `txt`_. You can choose which buttons to generate by setting the `formats` property to the filetype(s) of your choice.

```js
/* Defaults */
TableExport(document.getElementsByTagName("table"), {
  headers: true,                      // (Boolean), display table headers (th or td elements) in the  , (default: true)
  footers: true,                      // (Boolean), display table footers (th or td elements) in the  , (default: false)
  formats: ["xlsx", "csv", "txt"],    // (String[]), filetype(s) for the export, (default: ['xlsx', 'csv', 'txt'])
  filename: "id",                     // (id, String), filename for the downloaded file, (default: 'id')
  bootstrap: false,                   // (Boolean), style buttons using bootstrap, (default: true)
  exportButtons: true,                // (Boolean), automatically generate the built-in export buttons for each of the specified formats (default: true)
  position: "bottom",                 // (top, bottom), position of the caption element relative to table, (default: 'bottom')
  ignoreRows: null,                   // (Number, Number[]), row indices to exclude from the exported file(s) (default: null)
  ignoreCols: null,                   // (Number, Number[]), column indices to exclude from the exported file(s) (default: null)
  trimWhitespace: true,               // (Boolean), remove all leading/trailing newlines, spaces, and tabs from cell text in the exported file(s) (default: false)
  RTL: false,                         // (Boolean), set direction of the worksheet to right-to-left (default: false)
  sheetname: "id"                     // (id, String), sheet name for the exported spreadsheet, (default: 'id')
});
```

> **Note:** to use the `xlsx` filetype, you must include [js-xlsx](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460b881e3e6b319519ab1a30be8fde2103513b6c8bf091f8c66a588dcf54f72467ef416f2a606157ee74a9fd5e4e8d87a2c8d5ebf053591a29df5fb5cc80b0dcb0  reference the [`Add-Ons`](#add-ons) section.

### Properties

- [`headers`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f402f6e8c03f011439cdee5c994239178d9579952943cb7a312ba91925269d1dee5) 
- [`footers`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f402f6e8c03f011439cdee5c994239178d9579952943cb7a312ba91925269d1dee5) 
- [`formats`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40b4eb621cdafc6f6bd9bde760d324e1254d74df66697ec052677fbf66f2839b51) 
- [`filename`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f4018ff7ece296a22cecbf82cca753fa8ab) 
- [`bootstrap`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40b383e432e2a98cbf99354f75e7a48e0f) 
- [`exportButtons`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40f2284477b75fa02966820237f1dd8916abe5fe29afaa21f5353e06e61672501f) 
- [`position`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40688716b753e6815fefc754d508b8cf94) 
- [`ignoreRows`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40d84f5fc85a7f8e761fcf6eb20caa3bbae5781b153209238b7412684a94eaffff) 
- [`ignoreCols`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40d84f5fc85a7f8e761fcf6eb20caa3bbae5781b153209238b7412684a94eaffff) 
- [`trimWhitespace`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f400d32b122d3888d6c2627b10eedff65cb69833cfd93e0922fb06bad26972b0e80) 
- [`RTL`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40020fad1186fa045a18a0f6ca14cf3bf854ec2c42e48cdc02e7e4706a0572a2fd) 
- [`sheetname`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f407e32727396ed58b0a007312a59b0f63f) 

### Methods

TableExport supports additional methods (**getExportData**, **update**, **reset** and **remove**) to control the [`TableExport`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cbe6069e5fe4c27022ad30d970cb7e193a8bc89012a009c299ce7f2f1eac8c6296)  instance after creation.

```js
/* First, call the `TableExport` constructor and save the return instance to a variable */
var table = TableExport(document.getElementById("export-buttons-table"));
```

#### [`getExportData`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40f2284477b75fa02966820237f1dd8916abe5fe29afaa21f5353e06e61672501f) 

```js
/* get export data */
var exportData = table.getExportData(); // useful for creating custom export buttons, i.e. when (exportButtons: false)

/*****************
 ** exportData ***
 *****************
{
    "export-buttons-table": {
        xls: {
            data: "...",
            fileExtension: ".xls",
            filename: "export-buttons-table",
            mimeType: "application/vnd.ms-excel"
        },
        ...
    }
};
*/
```

#### [`export2file`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40f2284477b75fa02966820237f1dd8916abe5fe29afaa21f5353e06e61672501f) 

```js
/* convert export data to a file for download */
var exportData = table.getExportData(); 
var xlsxData = exportData.table.xlsx; // Replace with the kind of file you want from the exportData
table.export2file(xlsxData.data, xlsxData.mimeType, xlsxData.filename, xlsxData.fileExtension, xlsxData.merges, xlsxData.RTL, xlsxData.sheetname)
```

#### [`getFileSize`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40f2284477b75fa02966820237f1dd8916abe5fe29afaa21f5353e06e61672501f) 

```js
var tableId = "export-buttons-table";
var XLS = table.CONSTANTS.FORMAT.XLS;

/* get export data (see `getExportData` above) */
var exportDataXLS = table.getExportData()[tableId][XLS];

/* get file size (bytes) */
var bytesXLS = table.getFileSize(exportDataXLS.data, exportDataXLS.fileExtension);

/**********************************
 ** bytesXLS (file size in bytes)
 **********************************
352
*/
```

#### [`update`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f400470b64d0657958deb2f6fae2892c06a7ff6e2ee6de271d65e02ee7a30187b08) 

```js
/* update */
table.update({
  filename: "newFile" // pass in a new set of properties
});
```

#### [`reset`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f400470b64d0657958deb2f6fae2892c06a7ff6e2ee6de271d65e02ee7a30187b08) 

```js
/* reset */
table.reset(); // useful for a dynamically altered table
```

#### [`remove`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f400470b64d0657958deb2f6fae2892c06a7ff6e2ee6de271d65e02ee7a30187b08) 

```js
/* remove */
table.remove(); // removes caption and buttons
```

### Settings

Below are some of the popular configurable settings to customize the functionality of the library.

#### [`ignoreCSS`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40d84f5fc85a7f8e761fcf6eb20caa3bbae5781b153209238b7412684a94eaffff) 

```js
/**
 * CSS selector or selector[] to exclude/remove cells (  or  ) from the exported file(s).
 * @type {selector|selector[]}
 * @memberof TableExport.prototype
 */

// selector
TableExport.prototype.ignoreCSS = ".tableexport-ignore";

// selector[]
TableExport.prototype.ignoreCSS = [".tableexport-ignore", ".other-ignore-class"];

// OR using jQuery

// selector
$.fn.tableExport.ignoreCSS = ".tableexport-ignore";

// selector[]
$.fn.tableExport.ignoreCSS = [".tableexport-ignore", ".other-ignore-class"];
```

#### [`emptyCSS`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40d84f5fc85a7f8e761fcf6eb20caa3bbae5781b153209238b7412684a94eaffff) 

```js
/**
 * CSS selector or selector[] to replace cells (  or  ) with an empty string in the exported file(s).
 * @type {selector|selector[]}
 * @memberof TableExport.prototype
 */

// selector
TableExport.prototype.emptyCSS = ".tableexport-empty";

// selector[]
TableExport.prototype.emptyCSS = [".tableexport-empty", ".other-empty-class"];

// OR using jQuery

// selector
$.fn.tableExport.emptyCSS = ".tableexport-empty";

// selector[]
$.fn.tableExport.emptyCSS = [".tableexport-empty", ".other-empty-class"];
```

```js
/* default charset encoding (UTF-8) */
TableExport.prototype.charset = "charset=utf-8";

/* default `filename` property if "id" attribute is unset */
TableExport.prototype.defaultFilename = "myDownload";

/* default class to style buttons when not using Bootstrap or the built-in export buttons, i.e. when (`bootstrap: false` & `exportButtons: true`)  */
TableExport.prototype.defaultButton = "button-default";

/* Bootstrap classes used to style and position the export button, i.e. when (`bootstrap: true` & `exportButtons: true`) */
TableExport.prototype.bootstrapConfig = ["btn", "btn-default", "btn-toolbar"];

/* row delimeter used in all filetypes */
TableExport.prototype.rowDel = "\r\n";
```

```js
/**
 * Format-specific configuration (default class, content, mimeType, etc.)
 * @memberof TableExport.prototype
 */
formatConfig: {
    /**
     * XLSX (Open XML spreadsheet) file extension configuration
     * @memberof TableExport.prototype
     */
    xlsx: {
        defaultClass: 'xlsx',
        buttonContent: 'Export to xlsx',
        mimeType: 'application/vnd.openxmlformats-officedocument.spreadsheetml.sheet',
        fileExtension: '.xlsx'
    },
    xlsm: {
        defaultClass: 'xlsm',
        buttonContent: 'Export to xlsm',
        mimeType: 'application/vnd.ms-excel.sheet.macroEnabled.main+xml',
        fileExtension: '.xlsm'
    },
    xlsb: {
        defaultClass: 'xlsb',
        buttonContent: 'Export to xlsb',
        mimeType: 'application/vnd.ms-excel.sheet.binary.macroEnabled.main',
        fileExtension: '.xlsb'
    },
    /**
     * XLS (Binary spreadsheet) file extension configuration
     * @memberof TableExport.prototype
     */
    xls: {
        defaultClass: 'xls',
        buttonContent: 'Export to xls',
        separator: '\t',
        mimeType: 'application/vnd.ms-excel',
        fileExtension: '.xls',
        enforceStrictRFC4180: false
    },
    /**
     * CSV (Comma Separated Values) file extension configuration
     * @memberof TableExport.prototype
     */
    csv: {
        defaultClass: 'csv',
        buttonContent: 'Export to csv',
        separator: ',',
        mimeType: 'text/csv',
        fileExtension: '.csv',
        enforceStrictRFC4180: true
    },
    /**
     * TXT (Plain Text) file extension configuration
     * @memberof TableExport.prototype
     */
    txt: {
        defaultClass: 'txt',
        buttonContent: 'Export to txt',
        separator: '  ',
        mimeType: 'text/plain',
        fileExtension: '.txt',
        enforceStrictRFC4180: true
    }
},

//////////////////////////////////////////
// Configuration override example
//////////////////////////////////////////

/* Change the CSV (Comma Separated Values) `mimeType` to "application/csv" */
TableExport.prototype.formatConfig.xlsx.mimeType = "application/csv"

```

### CSS

[TableExport](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cbe6069e5fe4c27022ad30d970cb7e193a8bc89012a009c299ce7f2f1eac8c6296)  packages with customized [Bootstrap](http://u.720life.cn/g/e23be2821e5181a1a46a005bc6e93d9dabd141426b0b46d74d9ab3d47ead6054a7b62ea8e6c1387d8d6f37e52e4af1a547e39929bf884b975f363086a29fce03)  CSS stylesheets to deliver enhanced table and button styling. These styles can be _enabled_ by initializing with the `bootstrap` property set to `true`.

```js
TableExport(document.getElementsByTagName("table"), {
  bootstrap: true
});
```

When used alongside Bootstrap, there are four custom classes **`.xlsx`, `.xls`, `.csv`, `.txt`** providing button styling for each of the exportable filetypes.

### Browser Support

|             |  Chrome  | Firefox  |    IE    |  Opera   |  Safari  |
| :---------: | :------: | :------: | :------: | :------: | :------: |
| **Android** | &#10003; | &#10003; |    -     | &#10003; |    -     |
|   **iOS**   | &#10003; |    -     |    -     |    -     | &#10003; |
| **Mac OSX** | &#10003; | &#10003; |    -     | &#10003; | &#10003; |
| **Windows** | &#10003; | &#10003; | &#10003; | &#10003; | &#10003; |

> A full list of [browser support](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c244f445a95dcba6d626fe75801b1a148c1cd81492bc5286bf8b37bc4114e615ff22aa4368156497089251b932a129c7)  can be found in the [FileSaver.js](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c244f445a95dcba6d626fe75801b1a14a2c9b9e788a27dd4f22c17c277cb94ca)  README. Some [legacy browsers](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c244f445a95dcba6d626fe75801b1a148c1cd81492bc5286bf8b37bc4114e615ff22aa4368156497089251b932a129c7)  may require an additional third-party dependency: [Blob.js](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f5f497c95ff628f97084a0f84230ee1f75d4c5ed294a670ca84779038f09dbad) 

### Examples

#### Customizing Properties

- [`headers`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f402f6e8c03f011439cdee5c994239178d9579952943cb7a312ba91925269d1dee5) 
- [`footers`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f402f6e8c03f011439cdee5c994239178d9579952943cb7a312ba91925269d1dee5) 
- [`formats`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40b4eb621cdafc6f6bd9bde760d324e1254d74df66697ec052677fbf66f2839b51) 
- [`filename`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f4018ff7ece296a22cecbf82cca753fa8ab) 
- [`bootstrap`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40b383e432e2a98cbf99354f75e7a48e0f) 
- [`exportButtons`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40f2284477b75fa02966820237f1dd8916abe5fe29afaa21f5353e06e61672501f) 
- [`position`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40688716b753e6815fefc754d508b8cf94) 
- [`ignoreRows`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40d84f5fc85a7f8e761fcf6eb20caa3bbae5781b153209238b7412684a94eaffff) 
- [`ignoreCols`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40d84f5fc85a7f8e761fcf6eb20caa3bbae5781b153209238b7412684a94eaffff) 
- [`trimWhitespace`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f400d32b122d3888d6c2627b10eedff65cb69833cfd93e0922fb06bad26972b0e80) 
- [`RTL`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40020fad1186fa045a18a0f6ca14cf3bf854ec2c42e48cdc02e7e4706a0572a2fd) 
- [`sheetname`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f407e32727396ed58b0a007312a59b0f63f) 

#### Customizing Settings

- [`ignoreCSS`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40d84f5fc85a7f8e761fcf6eb20caa3bbae5781b153209238b7412684a94eaffff) 
- [`emptyCSS`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40d84f5fc85a7f8e761fcf6eb20caa3bbae5781b153209238b7412684a94eaffff) 

#### Miscellaneous

- [`rowspan`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40bbf51c25fc456d57ef063f48392efc8fa30e2387f229dd50ef9357b48e26ee2d) 
- [`colspan`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40bbf51c25fc456d57ef063f48392efc8fa30e2387f229dd50ef9357b48e26ee2d) 
- [`cell data types`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f4035a5771268927e9ef74c444930a8489d704410de6f88ec1a2873a966bcb79c39)  (`string`, `number`, `boolean`, `date`)
- [`emoji`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f4073482079eb7f42d79341923f57ee7f4d9dabc96e25f4d1297c3a4ea085de73d1) 
- [`Arabic`](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cb029e062ef19a7253ea32a6081112b90ed6aaea1048bb3c688a1bfd5b68e79f40e0ac0c8c69f1f0434889744499fc8506a16e4be6046da55a9b8e9d6354a6aad6) 

#### Skeletons

- [TableExport + RequireJS](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f8e9871eecd2fc8c123920e0fa7f923dee2194444b4ab7ed954fa1fd37c80126f0632fc752c474c2c6aa5b8870d5c3f0)  skeleton.
- [TableExport + Flask](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f8e9871eecd2fc8c123920e0fa7f923da8e2dca5b60dfdd0aa798b16f8d53de5ba8708bdbb7750796aacd6899a4839f6)  skeleton.
- [TableExport + Webpack 1](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f8e9871eecd2fc8c123920e0fa7f923da5fe03978a7d4c8e2bfbae4bae6e2aea0dc3e4e14204871ff1bcbb1b5270cd74)  skeleton.
- [TableExport + Angular 4 + Webpack 2](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f8e9871eecd2fc8c123920e0fa7f923dc2fa2de5b17411262ff8e739d538fe4eee4d2c3da452b1499028288338d7bfd9)  skeleton.

### License

[TableExport](http://u.720life.cn/g/d85856f364d9b878e8ac6787842070cbe6069e5fe4c27022ad30d970cb7e193a8bc89012a009c299ce7f2f1eac8c6296)  is licensed under the terms of the [Apache-2.0](http://u.720life.cn/g/c0fe1da5278ca9f6360e901f74721f845e8fe6a63a2e42f1caa9cfc3bfda71640d7e08e8dff8ca14a4a2db069871c2fb)  License

### Going Forward

#### TODOs

- [x] Update JSDocs and TypScript definition file.
- [x] Fix bug with **CSV** and **TXT** `ignoreRows` and `ignoreCols` (rows/cols rendered as empty strings rather than being _removed_).
- [x] Reimplement and test the `update`, `reset`, and `remove` **TableExport** prototype properties without requiring jQuery.
- [x] Make jQuery as _peer dependency_ and ensure proper **TableExport** rendering in browser, AMD, and CommonJS environments.
- [x] Force jQuery to be an optionally loaded module.
- [x] Use the enhanced [SheetJS](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460b881e3e6b319519ab1a30be8fde2103a54f27f6c91b5cf17242f8275d3340698627ec666d7624b5175f75ce2a6abe78)  `xls`, `csv`, and `txt` formats (exposed via `enforceStrictRFC4180` prototype property).
- [x] Allow `ignoreCSS` and `emptyCSS` to work with any `selector|selector[]` instead of solely a single CSS class.
- [x] Ensure (via testing) full consistency and backwards-compatibility for jQuery.
- [ ] Add **Export as PDF** support.

### Credits

Special thanks the the following contributors:

- [SheetJS](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469e9badb43f3166c89cda377abe6cc91a)  - js-xlsx
- [Eli Grey](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f5cdcc86d8ae53d7b945113d4eb3e449)  - FileSaver.js & Blob.js



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)