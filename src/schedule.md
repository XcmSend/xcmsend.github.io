# Schedule transactions on Polkadot


> Note this feature is still in development and can be accessed by: using the 'scheduler' branch in the main app repo.  


### Intro:  
If you select Polkadot as the source chain, you will be prompted for a block delay option.  
The block delay will delay your transaction with the amount of blocks you enter. If you eeneter 0, your transaction will not be scheduled.


![](/img/schedule.png)

##### Tech specs:  
The transaction is delayed using the scheduler pallet and delays it the amount of blocks the user has set.  




![](/img/schedule_tx.png)

### Supported direction:  
-  Polkadot > Assethub  
-  Polkadot > HydraDX 




