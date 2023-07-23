Here is my update on EPF4 Week 1.
## Further understanding of tasks
This week, I mainly focused on gaining a deeper understanding of the OP bundler. Although I still couldn't get in touch with my mentor from last week, I managed to contact Mark, the developer currently responsible for the implementation. He shared his current repository with me, and after thoroughly reviewing it, I engaged in a series of discussions with him.

Mark’s repo: https://github.com/ethereum/go-ethereum/compare/master...tynes:go-ethereum:eip4337

## Results obtained
During my exploration of Mark's repository and the discussions with him, I gathered some valuable insights and came up with a to-do list for the project. ⬇️⬇️

> #### [External] 4337 Endpoint Work
> 
> ### TODO List
> 
> 
> - [ ]  complete regarding errors
> - [ ]  cost counts optimization
> 
> ### other thoughts
> 
> 
> #####  about validation
> 
> *Currently, we perform multiple validations at different stages. For local transactions, we validate them in SendRawTransactionConditional, then in txpool, and finally in the worker. For remote transactions, we also need to perform sorting twice.*
> 
> *Perhaps we can explore adding subscriptions for the stateChange event and the blockgenerate event to facilitate sorting all the TxOptions. However, we should conduct a proof-of-value analysis to determine which approach is more efficient.*
> 
> *By the way, the txpool is not currently checking the options like blockNumberMin...*

## Other areas of learning.
1. This week, while dealing with some details, I realized that I was not very familiar with certain features of Golang. So, I spent time going through the materials that I had previously overlooked.

2. regularly browsed through the issues and pull requests on the Geth repository.

## The problems I encountered during Week 1
It seems that this task requires in-depth communication with the current developers to proceed further. There are many changes that need to be evaluated by them before I can proceed with the development. Therefore, this task is more of a concrete development and involves less research. Most of my time is spent on drafting and waiting for their responses.

## Next week’s schedule

1. I will further study the previously overlooked features of Golang. 
2. Additionally, I will explore other areas to see if there are any topics that interest me. This way, I can make the most of my time while waiting for responses and reviews.