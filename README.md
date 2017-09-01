Btccore Blockchain APIs
======

[![NPM Package](https://img.shields.io/npm/v/btccore-explorers.svg?style=flat-square)](https://www.npmjs.org/package/btccore-explorers)
[![Build Status](https://img.shields.io/travis/owstack/btccore-explorers.svg?branch=master&style=flat-square)](https://travis-ci.org/owstack/btccore-explorers)
[![Coverage Status](https://img.shields.io/coveralls/owstack/btccore-explorers.svg?style=flat-square)](https://coveralls.io/r/owstack/btccore-explorers)

A module for [btccore](https://github.com/owstack/btccore) that implements HTTP requests to different Web APIs to query the state of the blockchain.

## Attribution

This repository was created by copy forking [bitcore-explorers commit 1f1334f](https://github.com/bitpay/bitcore-explorers/commit/1f1334f7ea7f75ed80f62d379613a961a66403f2).

## Getting started

Be careful! When using this module, the information retrieved from remote servers may be compromised and not reflect the actual state of the blockchain.

```sh
npm install btccore-explorers
bower install btccore-explorers
```

At the moment, only Explorer is supported, and only getting the UTXOs for an address and broadcasting a transaction.

```javascript
var explorers = require('btccore-explorers');
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

See [CONTRIBUTING.md](https://github.com/owstack/btccore/blob/master/CONTRIBUTING.md) on the main btccore repo for information about how to contribute.

## License

Code released under [the MIT license](https://github.com/owstack/btccore/blob/master/LICENSE).

Copyright 2017 Open Wallet Stack. Btccore is a trademark maintained by Open Wallet Stack.

[btccore]: http://github.com/owstack/btccore-explorers
