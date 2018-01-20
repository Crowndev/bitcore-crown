bitcore-crown
=============

This package is under development. It may be unstable, or not work as expected.

Prerequisites
=============

You need to have ZeroMQ and tools, nvm, Node.js, npm, and Crown Core on your computer.

ZeroMQ and Tools
----------------

For GNU/Linux distribution such as Debian or Ubuntu:

```bash
sudo apt-get install libzmq3-dev build-essential
```

For Mac OS X:

Install `zeromq` via Brew.

nvm, Node.js and npm
--------------------

Install [nvm](https://github.com/creationix/nvm).

Use `nvm` command to install Node.js v4 and the latest npm.

Crown Core
----------

It should finally download Crown Core binaries from the web. But for now it just copies a local file. So make sure there's a file `~/zzz-crown-binaries/crownd`. We must use a Bitcore-specific `crownd` by cloning the repo "https://github.com/zhanzhenzhen/crowncoin" then build it.

Installation
============

```bash
npm install -g bitcore-crown
```

Note: Do not use `sudo`. To get rid of `sudo`, Node.js and npm must be installed via `nvm`.

Usage
=====

```bash
bitcored-crown
```

It will start a Crown node and Insight service. The blockchain data will be downloaded to `~/.bitcore-crown`. Insight can be visited via "http://localhost:3001/insight/".

There's another command `bitcore-crown-adv` for advanced operations. This maps to the `bitcore` command in the original Bitcore. The original Bitcore manual is [here](https://bitcore.io/). We added the `-adv` suffix to avoid confusion with `bitcored-crown`.

Contributing
============

See `CONTRIBUTING.md` file.

License
=======

See `LICENSE` file.
