# quantisnetcore-message

[![Build Status](https://img.shields.io/travis/quantisnetevo/quantisnetcore-message.svg?branch=master&style=flat-square)](https://travis-ci.org/quantisnetevo/quantisnetcore-message)
[![NPM Package](https://img.shields.io/npm/v/@quantisnetevo/quantisnetcore-message.svg?style=flat-square)](https://www.npmjs.org/package/@quantisnetevo/quantisnetcore-message)

> Message Verification and Signing for quantisnetcore-lib

quantisnetcore-message adds support for verifying and signing quantisnet messages in [Node.js](http://nodejs.org/) and web browsers.

See [the main quantisnetcore-lib repo](https://github.com/quantisnetevo/quantisnetcore-lib) for more information.

## Install

```sh
npm install @quantisnetevo/quantisnetcore-message
```

To sign a message:

```javascript
var bitcore = require('@quantisnetevo/quantisnetcore-lib');
var Message = require('@quantisnetevo/quantisnetcore-message');

var privateKey = bitcore.PrivateKey.fromWIF('cPBn5A4ikZvBTQ8D7NnvHZYCAxzDZ5Z2TSGW2LkyPiLxqYaJPBW4');
var signature = Message('hello, world').sign(privateKey);
```

To verify a message:

```javascript
var address = 'n1ZCYg9YXtB5XCZazLxSmPDa8iwJRZHhGx';
var signature = 'H/DIn8uA1scAuKLlCx+/9LnAcJtwQQ0PmcPrJUq90aboLv3fH5fFvY+vmbfOSFEtGarznYli6ShPr9RXwY9UrIY=';
var verified = Message('hello, world').verify(address, signature);
```

## Contributing

Feel free to dive in! [Open an issue](https://github.com/quantisnetevo/quantisnetcore-message/issues/new) or submit PRs.

Please see [CONTRIBUTING.md](https://github.com/quantisnetpay/quantisnet/blob/master/CONTRIBUTING.md) on the QuantsisnetCore repo for information about how to contribute.

## License

Code released under [the MIT license](LICENSE).
