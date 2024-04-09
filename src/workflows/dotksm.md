# Polkadot to Kusama Transfers

The long awaited Polkadot Assethub <> Kusama Assethub bridge is here and we wanted to be one of the first projects to document DOT transfers to kusama.

In the community forum post Kusama Assethub to Polkadot assethub was shown. We have now figured out how to go from Polkadot Assethub to Kusama Assethub.  

![](/img/dot_ksm.png) 


> We have implemented DOT > kusama assethub transfers with Bagpipes!! You can now drag and drop together a transfer in seconds.   
## Try it here:   
[https://app.xcmsend.com/#/builder](https://app.xcmsend.com/#/builder)   


## Video demo:
[https://drive.google.com/file/d/1iDaMNiZDaUjD95MGOwZqc87KBkl_deYL/view](https://drive.google.com/file/d/1iDaMNiZDaUjD95MGOwZqc87KBkl_deYL/view)    

## Valid extrinsic call data:  
`0x1f08030202090300a10f03000101005400e2f7f5669b26998d8e4d3c1a2c8a2d0a9af827ca54a1cc3509105035c32e0304000100000700c817a8040000000000`

You can check out this call by going to polkadot.js apps and pasting it in the decode field.  [Check it on this link](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Fpolkadot-asset-hub-rpc.polkadot.io#/extrinsics/decode)    

## Broadcasted transaction:    
[polkadot assethub #6021484-2](https://assethub-polkadot.subscan.io/extrinsic/6021484-2)

If all is successful you should be able to see this message on the kusama assethub polkadot.js app explorer     

![](/img/query_foreign.png)

### Check DOT balance on Kusama assethub:  

Go to chainstate and query `foreignAssets` > `account`:   

![](/img/query_ksm.png)


#### Polkadot.js typescript code:  
```typescript
export async function polkadot_assethub_to_kusama_assethub(
  amount: number,
  accountid: string
) {
  const myaccount = getRawAddress(accountid);

  const api = await getApiInstance("assetHub");

  const destination = {
    parents: 2,
    interior: {
      X2: [
        { GlobalConsensus: { Kusama: null } },
        { Parachain: 1000 }, // assethub
      ],
    },
  };

  const account = {
    parents: 0,
    interior: { X1: { AccountId32: { id: myaccount, network: null } } },
  };

  const asset = {
    id: {
      Concrete: {
        parents: 1,
        interior: {
          Here: null,
        },
      },
    },
    fun: { Fungible: amount },
  };

  const tx = api.tx.polkadotXcm.limitedReserveTransferAssets(
    { V3: destination },
    { V3: account },
    { V3: [asset] },
    0,
    { Unlimited: 0 }
  );
  return tx;
}
```


## References:   
[Polkadot Forum thread](https://forum.polkadot.network/t/polkadot-kusama-bridge/2971)   

