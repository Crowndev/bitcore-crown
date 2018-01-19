bitcore-crown
=============

# This package is under development. Please don't install.

Installation
============

It should finally download Crown Core binaries from the web. But for now it just copies a local file. Make sure there's a file `~/zzz-crown-binaries/crownd`.

Install [nvm](https://github.com/creationix/nvm).

Use `nvm` command to install Node.js v4 and the latest npm.

Then type:

```bash
npm install -g bitcore-crown@next
```

Note: Do not use `sudo` to run the above command. To get rid of `sudo`, we must use `nvm` to install `node` and `npm` beforehand.

Usage
=====

Type:

```bash
bitcored-crown
```

It will start a Crown node and Insight service. The blockchain data will be downloaded to `~/.bitcore-crown`. Insight can be visited via "http://localhost:3001/insight/".

The original Bitcore manual is [here](https://bitcore.io/).

Contributing
============

See `CONTRIBUTING.md` file.

License
=======

See `LICENSE` file.
