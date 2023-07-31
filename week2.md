Here is my update on EPF4 Week 2.

Last week, my work mainly revolved around three parts:
## Research
1. I delved into the specifics of EIP-4337 and corrected some of my previous misconceptions. 
2. I had a discussion with Mark about how to test the current API implementation for the sequencer. Mark pointed out that we should have a single commit in geth that we can simply apply to op-geth. This would allow bundlers to run on either L1 or L2. 
3. I looked into another task mentioned last week, which was about rpcclient. However, as I delved deeper into the current task, it seemed that there was more to implement than I initially thought, so I didn't explore it in depth.


## Coding 
Completed the 'complete regarding errors' task from last week's to-do list. The code is complete, and I conducted some simple manual test cases.
https://github.com/tynes/go-ethereum/compare/eip4337...joohhnnn:go-ethereum:eip4337Help
![](https://hackmd.io/_uploads/BJsgjUBoh.jpg)


## Testing
I realized that simple manual tests are not sufficient. Therefore, I started to explore 
1. hive: https://github.com/ethereum/hive
2. rpctestgen: https://github.com/lightclient/rpctestgen
3. execute-api: https://github.com/ethereum/execution-apis

aiming to implement standardized testing code using these tools.

## Outstanding issues
1. Mark raised an issue for support. I conducted some simple tests, but they were for geth. However, it seems that this issue requires a deeper understanding of opstack. I need more time to understand it. https://github.com/ethereum-optimism/optimism/issues/6450
2. This test suite only contains cases for successful outcomes. I'm uncertain if it's fitting to incorporate tests for erroneous conditions here.

## Next week’s schedule

Understand this test suite. Complete compliant tests. If there's still time, I might work on completing other cases.