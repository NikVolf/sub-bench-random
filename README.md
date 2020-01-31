# sub-bench-random

You can use this bench routine to run against `substrate --dev` node. No configuration needed!

This sends transfers from around 1000 endowed accounts to _random_ new accounts, thus trying to avoid state cache hits in substrate.

Having your substrate started in `--dev` mode with default websockets config, run here

```
npm install
npx tsc
node dist/index.js
```

or just if already npm-installed & compiled

```
node dist/index.js
```

### some configuration

You can change how long will it spam transactions in bench.config.json:

`processedTransactions = 1000`

replace it with any number to spam more/less

In the same file, you can change how much is spammed per seccond:

`tps = 100`

websockets url is set in `polkadot.bench.config.json`
