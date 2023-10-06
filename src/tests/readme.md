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
$ npx tsx src/tests/run_tests.ts
Running tests
Running Balance tests
Testing assethub balance
assethub balance ok
Checking polkadot balance checks
polkadot native balance check ok
Testing Hydradx asset balance
Hydradx asset balance ok
running transaction tests
[test] Polkadot transfers
Polkadot DOT > assethub OK
Polkadot DOT > hydradx OK
[test] AssetHub transfers
Assethub > hydradx ok
[test] assethub > polkadot
Assethub > Polkadot ok
[test] HydraDx transfers
Hydradx > assethub ok
[test] Hydradx > polkadot
Hydradx > polkadot ok
all transaction tests are constructed ok!
test completed
```

##### The tests will check:   
 -  drafting transactions and checking that they are encoded in the right way    
 -  checking if each chain returns correct asset and native balance    



### Broadcast transactions:  
Edit the `src/tests/run_tests` and set your seed in the `get_test_account` function.  

