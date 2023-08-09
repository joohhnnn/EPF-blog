Hey my name is joohhnnn. Here is my update on EPF4 Week 3.

## Add local test case for new error message

[Add test cases code](https://github.com/joohhnnn/go-ethereum/commit/9392ab777105aa8706100dea79ecd85bd448293c) 

It took me so long. I was stuck for a few days, thinking about using the execution-api and hive method to test errors, especially since there were few error tests case before in the geth codebase. But after some research and chatting with a friend, I realized that errors don't fall under the openrpc category. Also, trying to unify common errors across different clients like Erigon, Besu, and Nethermind would be pretty complicated. But I'm not too down about it, as the stuff I've learned over the past few days will come in handy when adding API Specification testing later on.

## Familiarized myself with the testing framework

1. generate test fixture by [rpctestgen](https://github.com/joohhnnn/rpctestgen)

    [link-to-code](https://github.com/lightclient/rpctestgen/compare/main...joohhnnn:rpctestgen:main)

 2. add test fixture to [execution-apis](https://github.com/ethereum/execution-apis) 

    [link-to-code](https://github.com/ethereum/execution-apis/compare/main...joohhnnn:execution-apis:main)

 3. test API with [hive](https://github.com/ethereum/hive)

    [link-to-code](https://github.com/ethereum/hive/compare/master...joohhnnn:hive:eip4337)

    (change the dockerfile’s path to the eip4337 patch)
    
    ![](https://hackmd.io/_uploads/B18nfXZhh.png)

## Next week’s schedule

test `eth_sendRawTransactionConditional()` with bundler and help with issue [6450](https://github.com/ethereum-optimism/optimism/issues/6450) 