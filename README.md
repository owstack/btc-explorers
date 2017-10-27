Btc Blockchain APIs
======

[![NPM Package](https://img.shields.io/npm/v/btc-explorers.svg?style=flat-square)](https://www.npmjs.org/package/btc-explorers)
[![Build Status](https://img.shields.io/travis/owstack/btc-explorers.svg?branch=master&style=flat-square)](https://travis-ci.org/owstack/btc-explorers)
[![Coverage Status](https://img.shields.io/coveralls/owstack/btc-explorers.svg?style=flat-square)](https://coveralls.io/r/owstack/btc-explorers)

A module for [btc](https://github.com/owstack/btc) that implements HTTP requests to different Web APIs to query the state of the blockchain.

## Attribution

This repository was created by copy forking [bitcore-explorers commit 1f1334f](https://github.com/bitpay/bitcore-explorers/commit/1f1334f7ea7f75ed80f62d379613a961a66403f2).

## Getting started

Be careful! When using this module, the information retrieved from remote servers may be compromised and not reflect the actual state of the blockchain.

```sh
npm install btc-explorers
bower install btc-explorers
```

At the moment, only Explorer is supported, and only getting the UTXOs for an address and broadcasting a transaction.

```javascript
var explorers = require('@owstack/btc-explorers');
var explorer = new explorers.Explorer();

explorer.getUtxos('1Bitcoin...', function(err, utxos) {
  if (err) {
    // Handle errors...
  } else {
    // Maybe use the UTXOs to create a transaction
  }
});
```

## Contributing

See [CONTRIBUTING.md](https://github.com/owstack/btc/blob/master/CONTRIBUTING.md) on the main btc repo for information about how to contribute.

## License

Code released under [the MIT license](https://github.com/owstack/btc/blob/master/LICENSE).

Copyright 2017 Open Wallet Stack.

[btc]: http://github.com/owstack/btc-explorers
