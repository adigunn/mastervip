Install Node JS 14
Write npm install at terminal in bots folder
Setup .env file in the folder with this explanation :

WBNB_CONTRACT=0xbb4cdb9cbd36b01bd1cbaebf2de08d9173bc095c 
~ WBNB contract for buy the token //Dont Change because the bots will using WBNB for snipe the tokens

YOUR_ADDRESS=   
~ Your BSC (BEP20) address from trustwallet or another wallet.

YOUR_PRIVATEKEY=
~ You can get the private key of your wallet by following this guide:
https://metamask.zendesk.com/hc/en-us/articles/360015289632-How-to-Export-an-Account-Private-Key

TARGET_TOKEN=
~ Put the token address of the token you want to snipe here.

AMOUNT_WBNB=
~Amount Of WBNB you want the bot to snipe with. 1=1 WBNB. You need to have WBNB in your wallet and makesure already approved

SPAMBUY=
~Total Amount of SpammingBuy you want
Example if you put 5 , the bots will trying to purchase token you targetting for 5 times , Write false , to deactivate spambuy feature

LATEST_NONCE=
~Your Latest Nonce Transaction in your address , to get your latest nonce , visit https://bscscan.com/address/youraddress , and click at latest txn Hash
see this screenshot to know your latest_nonce at txn Hash: https://prnt.sc/16f91hx

SPAM_INTERVAL=
~ your interval in every spambuy in millisecond
Example 1000 = 1 second , recomended 250-500 ms

FACTORY=0xcA143Ce32Fe78f1f7019d7d551a6402fC5350c73 
~ Pancake Factory contract to get function of buy //Dont Change

ROUTER=0x10ED43C718714eb63d5aA57B78B54704E256024E 
~ Pancake Factory contract to process function of buy //Dont Change

SLIPPAGE_SETTING=5  
~ The slippage you want the bot to handle specially for selling. Can be set from 1 to 100%.
Slippage is the expected % difference between these quoted and executed prices. Low Liquidity can also cause increased slippage, which is why larger orders then ot face higher slippage.

GWEI_SETTING=5
~ The amount of GWEI you want to use for a trade. Remember to keep this 10-15 (when bsc is not the usual 5 GWEI) for testing. But for sniping much higher.
How Much higher depens on the token (how much people are going to snipe), The fastest snipes use the highest GWEI and are only worth it when you play with a lot of WBNB.

GAS_LIMIT=650000
~ Please set this at 650000, so an order will never fail because you didn't accept a higher gas

MINIMUM_LIQUIDITY=3
~ Set how much minimum liquidity added in pair address that you want to buy. set in BNB. (eg : 2, 4, 7).
  2 mean 2 BNB liquidity added.
  
PERCENT_PROFIT=20
~ Provide in percent, the amount of profit you want to have, and want to sell for. This is not the profit that you are going to make, there is still slippage fee.

AMOUNT_OF_SELL=50
~ Provide in percent, that mean you will sell 50% amount of token you have.

LIQUIDITY_CHECKER=true
~ true if you want check global liquidity until the token you snipe its received the liquidity , false if you dont want to check global liquidity

ATTEMPTS=0
~ How many attempts to try again if transaction error.






Common Errors

Fail with error TransferHelper: 'TRANSFER_FROM_FAILED'
'max gas' was too low. please set the max-gas at 650k to be sure it never fails because of that.
or 
You were a victim of a honeypot contract (please google what it is ). 
The maker of the token was able to sell, and you were not due the contract the owner deployed.
