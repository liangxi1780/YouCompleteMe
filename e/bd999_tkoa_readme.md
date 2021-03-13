![tkoa logo](https://raw.githubusercontent.com/tkoajs/tkoa/master/source/logo.png)

🌈 Tkoa is a Koa web app framework written in typescript. ![typescript logo](https://raw.githubusercontent.com/tkoajs/tkoa/master/source/ts%20logo.png)

Although written in typescript, you can still use the nodejs framework and koa middleware.

Not only that, you can also enjoy the type checking and convenient testing with typescript!

## Installation
TKoa requires **>= typescript v3.1.0** and **node v7.6.0** for ES2015 and async function support.

```shell
$ npm install tkoa
```

### Hello T-koa

```typescript
import tKoa = require('tkoa');

interface ctx {
    res: {
        end: Function
    }
}

const app = new tKoa();

// response
app.use((ctx: ctx) => {
    ctx.res.end('Hello T-koa!');
});

app.listen(3000);
```

### Middleware
Tkoa is a middleware framework that can take two different kinds of functions as middleware:

- async function
- common function

Here is an example of logger middleware with each of the different functions:

#### async functions (node v7.6+):

```typescript
interface ctx {
  method: string,
  url: string
}

app.use(async (ctx: ctx, next: Function) => {
  const start = Date.now();
  await next();
  const ms = Date.now() - start;
  console.log(`${ctx.method} ${ctx.url} - ${ms}ms`);
});
```

#### Common function
```typescript
// Middleware normally takes two parameters (ctx, next), ctx is the context for one request,
// next is a function that is invoked to execute the downstream middleware. It returns a Promise with a then function for running code after completion.

interface ctx {
  method: string,
  url: string
}

app.use((ctx: ctx, next: Function) => {
  const start = Date.now();
  return next().then(() => {
    const ms = Date.now() - start;
    console.log(`${ctx.method} ${ctx.url} - ${ms}ms`);
  });
});
```

## Getting started
- [Tkoa - wiki](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046055371308892d88e241cf8047a34fe72c1aa5495d7c744200bd2ae537d4e6453) 
- [zhcn - 中文文档](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d4908dc68ad90b44c5ab16e295021e8cec896dca60aa64a79f004bbdff7873df9374d54d8d4f114f71bd63d36fa6e985) 
- [Gitter](http://u.720life.cn/g/11e95d0ed8d2826912e12fe1dc3f3421f8db58f888b058cab87d79f80fc6196b64c17ad742c4640d46211e437f5c48be) 

## Support
### TypeScript
- Higher than version v3.1
### Node.js
- Higher than version v7.6.0

## License
[MIT](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d4908dc68ad90b44c5ab16e295021e8c56953e288bf2cc78a2270ef1d6124ac527d4bcf1eee800b08b825b8776beea9a) 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)