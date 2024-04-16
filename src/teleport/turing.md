# Turing Kusama Parachain


#### Turing > Moonriver 

![](/img/turing2moonriver.png)   

We recommend that you connect talisman wallet and select your evm(0x) address as the destination address.  

 
Link to template:  
[https://app.xcmsend.com/#/create/?diagramData=k-2EaAM3l](https://app.xcmsend.com/#/create/?diagramData=k-2EaAM3l)   


#### Moonriver > Turing  

![](/img/moonriver2turing_xcm.png)

Select Moonriver as the source chain and turing as destination, after you press the green button and sign it. Press broadcast, once you get the transaction in a notification popup, copy the transaction and use the moonriver subscan block explorer linked below. 

We use the substrate interface (xtokens pallet) to send Asset from Moonriver to other parachains.


Link to template:  
[https://app.xcmsend.com/#/create/?diagramData=m4BcNtaWd](http://localhost:5173/#/create/?diagramData=m4BcNtaWd})   



#### Turing > MangataX  

![](/img/turing2mangatax.png)


Due to MangataX's transaction signing, we at the moment only support turing to mangatax transfers. If you have funds on MangataX and want to XCM them somewhere else we recommend that you use [https://app.mangata.finance](https://app.mangata.finance/).  



Link to template:  
[https://app.xcmsend.com/#/create/?diagramData=H4jA_C5vt](https://app.xcmsend.com/#/create/?diagramData=H4jA_C5vt)

#### Check the transactions:  
For turing we recommend that you copy the finalized hash and look it up here:
[https://turing.subscan.io/](https://turing.subscan.io/)

When your sending from Moonriver use this:   
![](/img/moonriverturingtx.png)     
[https://moonriver.subscan.io/](https://moonriver.subscan.io/)


### Use Turing with our api:  

```shell  
$ git clone https://github.com/XcmSend/api/   
$ cd api/ && npm install -f && npm run build 
$ npm run api
$ curl -X POST -H "Content-Type: application/json" -d '{"source_chain": "turing", "dest_chain": "moonriver", "destination_address": "0xA68db75204262BFC29aaC76CD546E2500Ba2AcBd", "amount": 100, "assetid": 0}' http://localhost:8080/create/scenario 

$ {"result":"SFdcb77BY"}


$ curl -X POST -H "Content-Type: application/json" -d '{"id": "SFdcb77BY"}' http://localhost:8080/scenario/info/full

$ {"result":{"tx":"0xa8042c0103000101000921009101030102009d1f0300a68db75204262bfc29aac76cd546e2500ba2acbd00","summary":"turing > xTransfer > moonriver","asset":"0","amount":"100","source_chain":"turing","dest_chain":"moonriver","txtype":"xTransfer"}}
```



### Read more about Turing:  
[https://oak.tech/turing/home/](https://oak.tech/turing/home/)   
[https://app.oak.tech/](https://app.oak.tech/)   


### Notes:  
We used Talisman browser wallet to test all these features.    


Turing transfers where enabled in the following version of Bagpipes:
`@bagpipes/xcm-send@0.1.1`

