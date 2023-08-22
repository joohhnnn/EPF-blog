Hey my name is joohhnnn. Here is my update on EPF4 Week 5.

# Design the architecture of Cost counts optimization

At the beginning of the design, I found that there are many problems at present, for example, the implementation of the current `eth_sendRawTransactionConditional()` is different between ARB or Polygon or OP network. Like, arb only checked when it entered the mempool, and did not validate the userOperation when a new state change was generated later There may be a need for a solution that can be extended to all layer2, but I don't know much about the design and implementation of layer2, I think I need a few weeks to understand most of the design framework of layer2

# Study the architecture of layer2
   This week, I mainly checked TAIKO's client and code structure, as well as his overall design ideas. I just checked some key codes roughly, and I still need some time to study in depth.
*   [Taiko Concepts](https://taiko.xyz/docs/concepts/overview) 
*   [Taiko-mono](https://github.com/taikoxyz/taiko-mono)
*   [Taiko-client](https://github.com/taikoxyz/taiko-client)