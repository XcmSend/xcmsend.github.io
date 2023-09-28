# Testing Guide


XCMSend comes prepackaged with test that dry run the functionality. 


## Run tests:  
```shell
$ git clone https://github.com/XcmSend/app-v0.0.1.git  
$ cd app-v0.0.1/
$ yarn run test
```

```
$ yarn run test
yarn run v1.22.19
$ npx tsx  src/tests/run_tests.ts
Running tests
Running Balance tests
running transaction tests
[test] Polkadot transfers
Polkadot DOT > assethub OK
[dotTohydraDx] tx created!
[dotTohydraDx] tx to hex 0xec04630803000100c91f030001010068de6e1566e333753df02b2446f24e1cc2b796cfdf954dc0f39753c578e02a40030400000000e5140000000000
Polkadot DOT > hydradx OK
[test] AssetHub transfers
Assethub > hydradx ok
Assethub > Polkadot ok
[test] HydraDx transfers
Hydradx > assethub ok
Hydradx > polkadot ok
all transaction tests are ok!
test completed
```

