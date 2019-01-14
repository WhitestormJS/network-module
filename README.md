# network-module [![NPM Version](https://img.shields.io/npm/v/physics-module-ammonext.svg?style=flat-square)](https://www.npmjs.com/package/network-module)
Networking module for Whitestorm.js [Alpha]

> Go to [WhitestormJS/whitestorm.js](https://github.com/WhitestormJS/whitestorm.js)

![physics module](http://i.imgur.com/ZdMhDwb.png)

# Modules List

## `new NETWORK.Connection()`

```javascript
const app = new WHS.App({
  // ...
  new NETWORK.Connection({
    host: 'localhost',
    port: 3000,
    protocol: 'http'
  })
});

app.start();
```
