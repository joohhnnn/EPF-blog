Hey my name is joohhnnn. Here is my update on EPF4 Week 4.

# Test eth_sendRawTransactionConditional() with bundler
Testing API with [Bundler](https://github.com/eth-infinitism/bundler)

1. Test the current codebase (geth) without opening conditionalRpc~~ 

2. Test the current codebase (geth) with opening conditionalRpc~~ 

     2.1.  Test with knownAccounts（already implemented by Bundler）—— test fail.

    This error  throw by [`supportsRpcMethod`](https://github.com/eth-infinitism/bundler/blob/d935f2690f19c3e22d30da942479acac92cc3f29/packages/bundler/src/utils.ts#L61)

    ![](https://hackmd.io/_uploads/Syy9M532n.png)

    2.2.  Add other options to bundler and test them.    

    I test the condition with only Geth, will try to help 6450 next step
# Try to help issues bundler test issue 
Try to help issues [6450](https://github.com/ethereum-optimism/optimism/issues/6450) 

1. It's really strange. At the beginning, I added the following flags to the configuration:
--dev \
--rpc.allow-unprotected-txs \
--allow-insecure-unlock,
and then successfully deployed it. However, when I was doing POC (I'm not sure whether it was --dev or --allow-insecure-unlock that made it successful), the deployment failed again, and it was all due to insufficient balance. But when I checked the balance of 0xf39Fd6e51aad88F6F4ce6aB8827279cffFb92266, both l1 and l2 had enough balance. 
2. There's another issue, it seems that the latest commit's devnet cannot be run directly with make devnet-up anymore, and it keeps telling me that the ./devnet addresses.json file is missing. For testing, I used git reset 7168db67c5b421975fef2a090aa6e6ee4e3ff298 --hard to do it.

    ![](https://hackmd.io/_uploads/H1gXXqn33.png)
    ![](https://hackmd.io/_uploads/HyF7X9hn3.png)
    ![](https://hackmd.io/_uploads/BkVEm5n22.png)
    ![](https://hackmd.io/_uploads/S1yrX92h3.png)

# Next week’s schedule
Continue to try to solve issue 6450 and explore the architecture of Cost counts optimization