bitcore-crown
=============

This package is under development. It may be unstable, or not work as expected.

Prerequisites
=============

Currently, it can be only run on Ubuntu.

You need to have ZeroMQ and tools, nvm, Node.js and npm installed.

ZeroMQ and Tools
----------------

```bash
sudo apt-get update
sudo apt-get install libzmq3-dev build-essential
```

Also make sure the commands `python` and `curl` are installed.

nvm, Node.js and npm
--------------------

Install [nvm](https://github.com/creationix/nvm).

Use `nvm` command to install Node.js v4 and the latest npm:

```bash
nvm install 4
nvm install-latest-npm
```

Installation
============

```bash
npm install bitcore-crown -g --global-style
```

Note: Do not use `sudo`. To get rid of `sudo`, Node.js and npm must be installed via `nvm`.

Usage
=====

```bash
bitcored-crown
```

It will start a Crown node and Insight service. The blockchain data will be downloaded to `~/.bitcore-crown`. Insight can be visited via "http://localhost:3001/insight/".

Configurations can be changed in `~/.bitcore-crown/bitcore-node-crown.json`. But don't modify the `servicesConfig.bitcoind.spawn.exec` property. Unlike the original Bitcore, modifying the binary file path will have no effect, as it will be automatically adjusted on every start if needed. This is by design to avoid conflicts between the testing environment and production environment. In the future this may be changed.

If you want the root path "/" rather than the default "/insight" to hold the Insight website, and "/api" rather than the default "/insight-api-crown" to hold the Insight API website, add 2 fields to `servicesConfig` in the config file:

```
{
  ...
  ...
  "servicesConfig": {
    ...
    ...
    "insight-ui-crown": {
      "routePrefix": "",
      "apiPrefix": "api"
    },
    "insight-api-crown": {
      "routePrefix": "api"
    }
  }
}
```

If you think the data is broken, the last way is to delete `~/.bitcore-crown` and start the program to redownload the data.

There's another command `bitcore-crown-adv` for advanced operations. This maps to the `bitcore` command in the original Bitcore. The original Bitcore manual is [here](https://bitcore.io/). We added the `-adv` suffix to avoid confusion with `bitcored-crown`.

Contributing
============

See `CONTRIBUTING.md` file.

License
=======

See `LICENSE` file.
