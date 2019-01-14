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

## `new NETWORK.Identity()`

```javascript
const box = new WHS.Box({
  geometry: {
    width: 2,
    height: 2,
    depth: 2
  },
  
  modules: [
    new NETWORK.Identity()
  ],
  
  material: new THREE.MeshBasicMaterial({color: 0xff0000})
});

box.addTo(app);
```

## `new NETWORK.Transform()`

```javascript
const box = new WHS.Box({
  geometry: {
    width: 2,
    height: 2,
    depth: 4
  },
  
  modules: [
    new NETWORK.Transform({
      position: true,
      rotation: true,
      scale: false,
      animation: true
    })
  ],
  
  material: new THREE.MeshBasicMaterial({color: 0xff0000})
});

box.addTo(app);
```

## `new NETWORK.Event()`
You can use this to allow for special events to be fired on objects. This is easy to do, and allows for great control over different objects.

```javascript
const box = new WHS.Box({
  geometry: {
    width: 2,
    height: 2,
    depth: 4
  },
  
  modules: [
    new NETWORK.Event({
      name: 'myCustomEvent'
      id: 0,
      handler: (data) => {
        doSomething();
      };
    })
  ],
  
  material: new THREE.MeshBasicMaterial({color: 0xff0000})
});

box.addTo(app);
```
