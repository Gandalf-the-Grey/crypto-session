[![NPM version][npm-img]][npm-url]
[![Build status][travis-img]][travis-url]
[![Test coverage][coveralls-img]][coveralls-url]
[![License][license-img]][license-url]
[![Dependency status][david-img]][david-url]

### koa-crypto-session

* Use [koa-session](https://github.com/koajs/session), but aes encrypted.

### Usage

* `options` will pass to [koa-session](https://github.com/koajs/session)

```js
const session = require('koa-crypto-session')
const app = require('koa')()

session(app, {
  crypto_key: new Buffer('exiKdyF+IwRIXJDmtGIl4vWUz4i3eVSISpfZoeYc0s4=', 'base64'),
  algorithm: 'aes-256-cbc'
})
```

Generate a new crypto_key:
```bash
$ node
> crypto.randomBytes(32).toString('base64')
```

### License
MIT

[npm-img]: https://img.shields.io/npm/v/koa-crypto-session.svg?style=flat-square
[npm-url]: https://npmjs.org/package/koa-crypto-session
[travis-img]: https://img.shields.io/travis/onebook/koa-crypto-session.svg?style=flat-square
[travis-url]: https://travis-ci.org/onebook/koa-crypto-session
[coveralls-img]: https://img.shields.io/coveralls/onebook/koa-crypto-session.svg?style=flat-square
[coveralls-url]: https://coveralls.io/r/onebook/koa-crypto-session?branch=master
[license-img]: https://img.shields.io/badge/license-MIT-green.svg?style=flat-square
[license-url]: http://opensource.org/licenses/MIT
[david-img]: https://img.shields.io/david/onebook/koa-crypto-session.svg?style=flat-square
[david-url]: https://david-dm.org/onebook/koa-crypto-session
