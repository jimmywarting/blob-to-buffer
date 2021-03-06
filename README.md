# blob-to-buffer [![travis][travis-image]][travis-url] [![npm][npm-image]][npm-url] [![downloads][downloads-image]][downloads-url] [![javascript style guide][standard-image]][standard-url]

[travis-image]: https://img.shields.io/travis/feross/blob-to-buffer/master.svg
[travis-url]: https://travis-ci.org/feross/blob-to-buffer
[npm-image]: https://img.shields.io/npm/v/blob-to-buffer.svg
[npm-url]: https://npmjs.org/package/blob-to-buffer
[downloads-image]: https://img.shields.io/npm/dm/blob-to-buffer.svg
[downloads-url]: https://npmjs.org/package/blob-to-buffer
[standard-image]: https://img.shields.io/badge/code_style-standard-brightgreen.svg
[standard-url]: https://standardjs.com

#### Convert a Blob to a [Buffer](https://github.com/feross/buffer).

[![Sauce Test Status](https://saucelabs.com/browser-matrix/blob-to-buffer.svg)](https://saucelabs.com/u/blob-to-buffer)

Say you're using the ['buffer'](https://github.com/feross/buffer) module on npm, or
[browserify](http://browserify.org/) and you're working with lots of binary data.

How do you convert it to a `Buffer`?

***Simply use this module!***

Works in the browser. This module is used by [WebTorrent](http://webtorrent.io)!

### install

```
npm install blob-to-buffer
```

### usage

```js
const toBuffer = require('blob-to-buffer')

// Get a Blob somehow...
const blob = new Blob([ new Uint8Array([1, 2, 3]) ])

toBuffer(blob).then(buffer => {
  buffer[0] // => 1
  buffer.readUInt8(1) // => 2
})
```

### license

MIT. Copyright (c) [Feross Aboukhadijeh](http://feross.org).
