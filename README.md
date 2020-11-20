# process-fast

[![NPM](https://img.shields.io/npm/v/process-fast.svg?style=for-the-badge)](https://npm.im/process-fast)
![Downloads](https://img.shields.io/npm/dt/process-fast.svg?style=for-the-badge)
![Dependency status](https://img.shields.io/librariesio/release/npm/process-fast?style=for-the-badge)
[![license](https://img.shields.io/:license-MIT-blue.svg?style=for-the-badge)](https://mvr.mit-license.org)

Fast node `require('process')` for modern browsers.

Inspired by [process](https://npm.im/process) but painfully simple - using`queueMicrotask` to shim `process.nextTick()`.

If you only need to support modern browsers this can speed up many node based modules and dependencies by avoiding slow shims such as `setTimeout()`.


## Install

```shell
$ npm install process-fast
```

## Example
Shim with webpack:

```js
plugins: [
  new webpack.ProvidePlugin({
    process: 'process-fast'
  })
]
```
