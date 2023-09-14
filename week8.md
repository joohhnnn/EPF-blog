Hey my name is joohhnnn. Here is my update on EPF4 Week 8.

### Week 8 Project Progress Report

#### Work Completed This Week

1. **Addressing the Lingering Issue - Issue 6450**

   This week, I continued to tackle the lingering issue, specifically the [Issue 6450 in the Ethereum Optimism project](https://github.com/ethereum-optimism/optimism/issues/6450). After a deep dive, I pinpointed the issues to the following aspects:

   - **Environment Setup**: I managed to run the bundler smoothly in my fresh Ubuntu 22.04 setup. Ensure you initiate the devnet correctly. I recommend installing geth by executing `make install-geth` in the optimism mono.
   
   - **Successful Launch**: Following the steps mentioned, I successfully launched the bundler on port 3000 and ensured it was bound to port 9545.
   
   - **Removing ChainID Validation**: To tailor to a specific network setting, I removed the ChainID validation found in `./bundler/packages/bundler/deploy/2-deploy-entrypoint.ts`.
   
   - **Port Adjustment**: I altered the port number to 9545 in both `./bundler/packages/bundler/hardhat.config.ts` and `./bundler/packages/bundler/localconfig/bundler.config.json`.
   
   - **Shell Script Update**: I revised the `./optimism/ops-bedrock/entrypoint-l2.sh` script to accommodate the new configurations and environmental variables.
   
   - **Funds Deployment**: Utilizing port 9545, I transferred 1 ETH to the address `0x3fab184622dc19b6109349b94811493bf2a45362`.

2. **Developing an Auto-Configuration Middleware**

   Stemming from the issue mentioned above, I [crafted an auto-configuration middleware](https://github.com/joohhnnn/OPBundlerAutoConfig) to streamline the configuration process and mitigate potential issues in the future.

3. **Exploring the Underlying Code of Optimism**

   I initiated a journey into the underlying code of Optimism, getting a preliminary understanding of the directory structure and some non-core parts of the code, such as `op-bindings` and `op-bootnode`.

#### Plans for Next Week

- Delve deeper into the core sections of the Optimism underlying code.
- Prepare to share my experiences and solutions from addressing Issue 6450 with the community.

