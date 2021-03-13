# el-form-renderer

[![Build Status](https://badgen.net/travis/FEMessage/el-form-renderer/master)](https://travis-ci.com/FEMessage/el-form-renderer)
[![NPM Download](https://badgen.net/npm/dm/@femessage/el-form-renderer)](https://www.npmjs.com/package/@femessage/el-form-renderer)
[![NPM Version](https://badgen.net/npm/v/@femessage/el-form-renderer)](https://www.npmjs.com/package/@femessage/el-form-renderer)
[![NPM License](https://badgen.net/npm/license/@femessage/el-form-renderer)](https://github.com/FEMessage/el-form-renderer/blob/master/LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/FEMessage/el-form-renderer/pulls)
[![Automated Release Notes by gren](https://img.shields.io/badge/%F0%9F%A4%96-release%20notes-00B2EE.svg)](https://github-tools.github.io/github-release-notes/)

![](https://i.loli.net/2019/11/14/Nz6n9l7KixqIHsa.png)

[中文文档](./README-zh.md)

## Table of Contents

- [Introduction](#introduction)
  - [WHAT](#what)
  - [WHY](#why)
- [Features](#features)
- [Links](#links)
- [Quick Start](#quick-start)
- [Inspiration](#inspiration)
- [Contributing](#contributing)
- [Contributors](#contributors)
- [License](#license)

## Introduction

### WHAT

`el-form-renderer` is based on [element-ui](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461c3385d2c6442447210a4c3d1baebf512f976766af05deae047ab3ac564f7275  but not limited [element-ui](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461c3385d2c6442447210a4c3d1baebf5188ca4979686fe7db89246207127fdadd)  components. On the basis of completely inheriting the form attribute of element-ui, extension is made. Some non-form components or custom components, such as picture uploading and rich text editor, can also be integrated, thus, users can render a complete form by using a piece of json.

### WHY

In our daily development, there are lots page with form, and usually the form structure is similar, the logic is repeated. el-form-renderer does not have complicated logic. It only convert JSON to render form item, save time and energy to write business logic, and reduce duplicate code.

## Features

- Render form with json
- Support integrate with custom components
- Support batch update form data with updateForm method
- Support setOptions method, dynamically change select options
- Content support `inputFormat` , `outputFormat` , `trim` to process component's input and output values

[⬆Back to Top](#table-of-contents)

## Links

- [Docs](http://u.720life.cn/g/a919183390e89760212c1bca8de9a518bbc461894bffce8db306d672e09bc0add0a52484949ca8df03efb26b5efb5f62) 
- [Guide to developing custom component](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e338e50bd0ef75daed2abd1ededd4a085f367ef803ac2f1354248432a8971e87ba1123d410091114d0810195b9c00d285b31790741a439c778141ecbe3e2bbfac67080bcbce513160d01f03fba71c90f) 
- [Setting validation rules in custom component](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466dc62a7036e7731b92df3e433cf01992eb5717f56db7c211a6e8ef5756a9f758d958409d1627d93ee68bafa740e17d840cfcb2809453ed7ab9b75c6e86207618cf27fd7a1cdd1262a39c7d9ef775d0557ed3ef08f2108d179f9d99757b4d44cd) 
- [fem-vscode-helper](http://u.720life.cn/g/61df49c8dfe6497e1d755535043d5993f084ad4bb2562a93ce813aeeb8e143e31ce529a8f29bba55ad86d25d141343883237056c2a23ef53c8e9cb52e47dc2de9d38274d8bc08bef1bd5fef55170dbf5) 

[⬆Back to Top](#table-of-contents)

## Quick Start

```sh
yarn add @femessage/el-form-renderer
```

```html
 
    
 
 
  import ElFormRenderer from '@femessage/el-form-renderer'
  export default {
    components: {
      ElFormRenderer
    },
    data() {
      return {
        content: []
      }
    }
  }
 
```

[⬆Back to Top](#table-of-contents)

## Inspiration

thanks to [element-patch](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046675c70dc20b735606e9a87aa606d16a698f838a0ffc3a22f081b7fc2e0dadada) 

## Contributing

For those who are interested in contributing to this project, such as:

- report a bug
- request new feature
- fix a bug
- implement a new feature

Please refer to our [contributing guide](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046656a9e9989586d748994a34c8fbc481e4fa5594a54acb3020f42f7d5991d87772b0ab9502424f6dfc3fa50713d9900e94a75d88a7a9558ac88e8d121cd98553a 

[⬆ Back to Top](#table-of-contents)

## Contributors

Thanks goes to these wonderful people ([emoji key](http://u.720life.cn/g/35776c78de41d6d71a059102a9e8e921fbcd61937cbbcc740ca267e8187d18bb8e1a7afd55cb0fd03caabcaf74535dc1 

 
 
        Alvin     💻   👀   🐛   📝   🤔        levy     👀   🚇   🤔        EVILLT     💻   🐛   📝   🤔        Donald Shen     💻   📖   💡   📝        ColMugX     💻   ⚠️   📖        OuZuYu     🐛        Han     💻   📖    

 

This project follows the [all-contributors](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046af6463814647b757f017863e54c8640ab5da9f69ecb42c4faae0ea71740deab2df695a72bddabfa7ec20f6631d043550)  specification. Contributions of any kind welcome!

## License

[MIT](./LICENSE)

[⬆ Back to Top](#table-of-contents)



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)