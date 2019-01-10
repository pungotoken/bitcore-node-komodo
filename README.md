![Pungo Token](https://i.ibb.co/T0cFLpx/token-regular-small.png)

# Bitcore Node

A Bitcoin full node for building applications and services with Node.js. Bitcore node is required 
for [Insight-UI](https://github.com/pungotoken/insight-ui-komodo.git). 
To install Insight read [instructions](https://github.com/pungotoken/insight-ui-komodo/blob/master/README.md)
A node is extensible and can be configured to run additional services. At the minimum a node has an interface to 
[Bitcoin Core with additional indexing](https://github.com/bitpay/bitcoin/tree/0.12.1-bitcore) for more 
advanced address queries. Additional services can be enabled to make a node more useful such as exposing new APIs, 
running a block explorer and wallet service.

## Development Resources

- PungoToken Website: [https://pungotoken.com](https://pungotoken.com/)
- PungoToken Blockexplorer: [https://explorer.pungotoken.build](https://explorer.pungotoken.com)
- PungoToken Telegram: [https://t.me/pungotalk](https://t.me/pungotalk)
- PungoToken Node Addresses:  190.114.254.103, 190.114.254.104
- PungoToken Electrum Servers Addresses: agama.komodo.build:10001 agama2.komodo.build:10001

## Getting started

### Minimum requirements

- GNU/Linux x86_32/x86_64, or OSX 64bit *(for bitcoind distributed binaries)*
- Node.js v0.10, v0.12 or v4
- ZeroMQ *(libzmq3-dev for Ubuntu/Debian or zeromq on OSX)*
- ~200GB of disk storage
- ~8GB of RAM

### Dependencies

Before installing Bitcore node you should install NodeJS and NPM manager:

```shell
#The following packages are needed:
sudo apt-get install -yq nodejs=4.2.6~dfsg-1ubuntu4.2 npm
```

### Install

```bash
npm install -g bitcore-node
bitcore-node start
```

Note: For your convenience, we distribute bitcoind binaries for x86_64 Linux and x86_64 Mac OS X. Upon npm install, the binaries for your platform will be downloaded. For more detailed installation instructions, or if you want to compile the project yourself, then please see the Bitcore branch of [Bitcoin Core with additional indexing](https://github.com/bitpay/bitcoin/tree/0.12.1-bitcore).

### Configuration

Bitcore includes a Command Line Interface (CLI) for managing, configuring and interfacing with your Bitcore Node.

```bash
bitcore-node create -d <bitcoin-data-dir> mynode
cd mynode
bitcore-node install <service>
bitcore-node install https://github.com/yourname/helloworld
```

This will create a directory with configuration files for your node and install the necessary dependencies. For more information about (and developing) services, please see the [Service Documentation](docs/services.md).

### Add-on Services

There are several add-on services available to extend the functionality of Bitcore:

- [Insight API](https://github.com/bitpay/insight-api)
- [Insight UI](https://github.com/bitpay/insight-ui)
- [Bitcore Wallet Service](https://github.com/bitpay/bitcore-wallet-service)

### Documentation

- [Upgrade Notes](docs/upgrade.md)
- [Services](docs/services.md)
  - [Bitcoind](docs/services/bitcoind.md) - Interface to Bitcoin Core
  - [Web](docs/services/web.md) - Creates an express application over which services can expose their web/API content
- [Development Environment](docs/development.md) - Guide for setting up a development environment
- [Node](docs/node.md) - Details on the node constructor
- [Bus](docs/bus.md) - Overview of the event bus constructor
- [Release Process](docs/release.md) - Information about verifying a release and the release process.

### Contributing

Please send pull requests for bug fixes, code optimization, and ideas for improvement. For more information on how to contribute, please refer to our [CONTRIBUTING](https://github.com/bitpay/bitcore/blob/master/CONTRIBUTING.md) file.

### License

Code released under [the MIT license](https://github.com/bitpay/bitcore-node/blob/master/LICENSE).

Copyright 2013-2015 BitPay, Inc.

- bitcoin: Copyright (c) 2009-2015 Bitcoin Core Developers (MIT License)
