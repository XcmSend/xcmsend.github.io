# Api tests


### Build:
```shell
$ git clone https://github.com/XcmSend/api
$ cd api/
$ npm install 
```


### Run tests:
```shell
$ npm run test

> xcmsend-api@1.0.0 test
> ts-node src/api/tests.ts

running api tests
starting connection test
trying to connect to Polkadot
Polkadot connection ok
trying to connect to HydraDX
HydraDX connection ok
trying to connect to Assethub
Assethub connection ok
connection test passed
Testing transaction routing
Checking polkadot > hydradx
route_tx start
polkadot:hydradx
handleTransfer for Polkadot to HydraDx...
cant connect
connect
drafting dot to hydradx
Creating tx
polkadot > hydradx ok
Checking hydradx > assethub
route_tx start
hydradx:assethub
handleTransfer for HydraDx to AssetHub...
hydradx > assethub ok
Checking polkadot > assethub
route_tx start
polkadot:assethub
handleTransfer for Polkadot to AssetHub...
polkadot > assethub ok
Checking hydradx > polkadot
route_tx start
hydradx:polkadot
handleTransfer for HydraDx to Polkadot...
hydradx > polkadot ok
Checking assethub > polkadot
route_tx start
assethub:polkadot
handleTransfer for AssetHub to Polkadot...
assethub > polkadot ok
Checking assethub > hydradx
route_tx start
assethub:hydradx
handleTransfer for AssetHub to HydraDx...
[assethub_to_hydra]
assethub > hydradx ok
transaction routing ok
testing hrmp channels
Checking HydraDX <> Assethub channels
hrmp channel test passed
api tests finished
```

