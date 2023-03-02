# Hyperspace Testnet

Hyperspace launched on Jan 16, 2023 and upgraded on Feb 27, 2023.

Meta info about the Hyperspace testnet for Filecoin developers

![hyperspace-testnet-image](images/hyperspace-testnet-image.png)

&nbsp;

## Overview

The Filecoin Hyperspace testnet is a stable testnet with fewer resets intended for developers' longer-term testing efforts.

- As of Jan 16, Hyperspace will support the penultimate FEVM release, and will be upgraded to the the final FEVM release on Feb 2. ([List of FEVM releases](https://github.com/filecoin-project/ref-fvm/issues/692))
- Hyperspace supports `512 MiB`, `32 GiB`, and `64 GiB` storage sectors with 2 miners auto-accepting new deals from developers (see [Resources](#resources) - Hyperspace Storage Providers below).
- A comparison of Filecoin's various testnets is available in [FIP #544](https://github.com/filecoin-project/FIPs/discussions/544).


&nbsp;

## Quickstart

1. Add the Hyperspace testnet to your wallet (e.g. MetaMask).
    - Go to https://chainlist.org/chain/3141
    - Click on "Connect wallet"
2. Create a new account in MetaMask to use with Filecoin.
3. Use https://hyperspace.yoga/#faucet to request funds to your Ethereum address (it will be converted behind the scenes to a Filecoin f4 address)
4. Follow the transaction in one of the recommended Hyperspace testnet explorers:
    - https://hyperspace.filfox.info/en 
    - https://beryx.zondax.ch 
    - https://explorer.glif.io/?network=hyperspace 
5. Your account is now funded and can be used in Ethereum tools such as Hardhat, Foundry, Remix, etc.

## Technical details

**Maintainer:** @f8-fil-ops

#### **Genesis**:

- CAR File: `Qmbu9g75GMjbokCNHPQPXAyKZoY8NqVYtkY4PQT7Zvp2T6`
- Reset Timestamp: `2023-01-16T6:00:00Z`
- Genesis Block CID: `bafy2bzacebqfpeylmrl4h3pq4ofbdj2bfbw2i45fuy6qm4wxcyebpsxhrpqhu`
- sha1 Digest: `52d82b6fcad138a726477152ff2543a91f2b83f8`

#### **Network parameters**:

- Supported Sector Sizes: `512 MiB` and `32 GiB` and `64 GiB`
- Consensus Miner Min Power: `16 GiB`
- Epoch Duration Seconds: `30`
- Expected Leaders per Epoch: `5`
- WindowPoSt Proving Period: `2880`
- WindowPoSt Challenge Window: `60`
- WindowPoSt Period Deadlines: `48`
- Pre-Commit Challenge Delay: `10`

#### **Bootstrap peers**:

```
/dns4/de0.bootstrap.hyperspace.yoga/tcp/31000/p2p/12D3KooWRiwg6EHAJMR5w3DZTgpS5W4ncWPSVP2Mr1o4ey1RYSQo
/dns4/de1.bootstrap.hyperspace.yoga/tcp/31000/p2p/12D3KooWM9HZsp1bh5jNu2m9FBSbkKSeSWUPPuDBQiiMfPDBAK3U
/dns4/au0.bootstrap.hyperspace.yoga/tcp/31000/p2p/12D3KooWLup1gTdG9ipt3bSUyPCmM4CT86p9nNe12oqrCX8Zo8Na
/dns4/ca0.bootstrap.hyperspace.yoga/tcp/31000/p2p/12D3KooWNJ4evKioh6gexD4fyvyeFecNtp2oTEPTyp3jtSQ3pWaP
/dns4/sg0.bootstrap.hyperspace.yoga/tcp/31000/p2p/12D3KooWCENec46HHByaJKzbjSqz9TqVdSxSAdi9FKNwdMvfw3vp
```


#### **FVM release**:

- [FVM M2.1 Carbonado.3 (rr12) - Final FVM release!](https://github.com/filecoin-project/ref-fvm/issues/1372)
- Lotus commit: [cf152e19bda7be289fd531be689279aa5f598899](https://github.com/filecoin-project/lotus/commit/cf152e19bda7be289fd531be689279aa5f598899)
- [List of FVM releases](https://github.com/filecoin-project/ref-fvm/issues/692)

#### **Resources**:

- Slack Channel for Updates: [#fil-net-hyperspace-discuss](https://filecoinproject.slack.com/archives/C04JEJB82RY)

- **Network Status**: https://status.filecoin.io/
- **Hyperspace Docs**: [https://kb.factor8.io/en/docs/filecoin/testnets/hyperspace](https://kb.factor8.io/en/docs/filecoin/testnets/hyperspace)
- **Faucets**: 
  - https://hyperspace.yoga/#faucet
    - The faucet currently emits 5 tFIL per request with a max of 5 requests / wallet (to prevent draining attacks).
    - _Setting up a miner?_ You may need more tFIL than this - reach out to us for more or you could try a 2nd or 3rd address.
  - https://beryx.zondax.ch/faucet
- **Block Explorers**:
  - Filfox - [https://hyperspace.filfox.info/en](https://hyperspace.filfox.info/en)
  - Beryx - [https://beryx.zondax.ch](https://beryx.zondax.ch)
  - Glif Explorer - [https://explorer.glif.io/?network=hyperspace](https://explorer.glif.io/?network=hyperspace)
  - Starboard - [https://fvm.starboard.ventures/](https://fvm.starboard.ventures/)
  - Filscan - [https://hyperspace.filscan.io/](https://hyperspace.filscan.io/)
- **RPC - Public Endpoints**:
  - These endpoints are limited to all read-only Filecoin JSON RPC API calls + `MPoolPush` (for sending already signed messages)
  - **Glif Nodes RPC:**
    - https://api.hyperspace.node.glif.io/rpc/v1
    - web socket endpoint: wss://wss.hyperspace.node.glif.io/apigw/lotus/rpc/v1
    - For Lotus Lite use `FULLNODE_API_INFO=wss://wss.hyperspace.node.glif.io/apigw/lotus lotus daemon --lite`
  - **ChainStack RPC:**
    - https://filecoin-hyperspace.chainstacklabs.com/rpc/v0
    - web socket endpoint: wss://ws-filecoin-hyperspace.chainstacklabs.com/rpc/v0
    - Info page: https://chainstack.com/labs/#filecoin
  - **Ankr RPC:**
    - https://rpc.ankr.com/filecoin_testnet
- **Hyperspace Fil+ Data Cap Requests**
  - Apply for Data Cap: https://hyperspace.yoga/#notary 
    - (for Hyperspace only, on mainnet this is handled by https://filplus.storage/apply)
  - Check Data Cap allocations: https://hyperspace.yoga/#dc-check
  - [Fil+ Data Cap Dashboard for Hyperspace](https://hyperspace.filplus.d.interplanetary.one/notaries/t01227)
    - [API reference](https://documenter.getpostman.com/view/131998/Tzsim4NU#introhttps://documenter.getpostman.com/view/131998/Tzsim4NU#intro) but use http://api.hyperspace.filplus.d.interplanetary.one
- **Hyperspace Storage Providers (miners) auto-accepting storage deals / simulating faults:**
  - See [Support Miners - Hyperspace Docs](https://kb.factor8.io/en/docs/filecoin/testnets/hyperspace/support-miners)
- **SP Reputation Systems**
  - https://hyperspace.filrep.io/ - info about deals and sectors is currently being updated
     - API example: https://api.hyperspace.filrep.io/api/v1/miners?region=Europe
- **Filecoin CID Checker**:
  - [https://hyperspace.filecoin.tools/](https://hyperspace.filecoin.tools/) - check your deal or piece CID’s storage status
- **Zondax Filecoin Solidity Libs**
  - https://www.npmjs.com/package/@zondax/filecoin-solidity
  - https://github.com/Zondax/filecoin-solidity
  - https://github.com/Zondax/fevm-solidity-precompiles
- **Hyperspace Chain Index APIs**
  - https://beryx.zondax.ch/ 
    - API Docs: https://docs.zondax.ch/Beryx
    - GraphQL UI: https://docs.zondax.ch/beryx/graphql
- **MetaMask** (HowTo):
  - Open MetaMask and add a new network:
    - Name: Filecoin Hyperspace
    - RPC URL: https://api.hyperspace.node.glif.io/rpc/v1
    - ChainID: [**3141**](https://github.com/ethereum-lists/chains/blob/master/_data/chains/eip155-3141.json) (Filecoin - Hyperspace testnet)
    - Currency symbol: tFIL (Test FIL).
  - Create a new account in MetaMask to use with Filecoin.
  - (OPTIONAL - the faucet accepts 0x style addresses now) Go to https://explorer.glif.io/ethereum/, and select the account to see its f4 address.
  - Use the [faucet](https://hyperspace.yoga/#faucet) to draw funds to your f4 (0x style addresses are translated automatically to f4's in the backend) or alternatively use `lotus send` to transfer funds to the f4 address.
  - Wait until the transaction process, and verify that the funds appear in MetaMask.
  - Create another new account in MetaMask, (optional) obtain its f4 address again.
  - Use MetaMask to send funds from your first account to your second account.
  - **Notes on MM**
    - Note that you may need to increase the gas limit manually because there's something strange going on with gas estimation at the moment.
  - **Note on GLIF**:
    - The GLIF explorer seems to have some problems with f4 addresses right now, please refer to the #fil-net-hyperspace-discuss for questions/solutions
- **Docs and Developer Tools**:
  - [Space Warp Hackathon Schedule](https://ethglobal.com/events/spacewarp#schedule)
  - [Space Warp Developer Cheat Sheet](https://docs.google.com/document/d/1EecX8XOqOF6MNaouXL0qZAuCEK1WF5UWA5LMSlWe3RI/edit#)
  - [FEVM Hardhat Kit, Filecoin Solidity library and Data DAO example](https://docs.filecoin.io/developers/smart-contracts/hardhat/)
  - [Space Warp Developer Resources](https://spacewarp.fvm.dev/#resources)
- **Snapshots**
  - [Latest chain snapshot (pruned)](https://snapshots.hyperspace.yoga/hyperspace-latest-pruned.car)
  - [Latest chain snapshot (full)](https://snapshots.hyperspace.yoga/hyperspace-latest-full.car)

<hr>

:warning: [TODO - SAMPLE INFO BELOW] :warning:


- [Status page and incidents](https://filecoin.statuspage.io/)
- [Stats dashboard](https://stats.filecoin.io/)
- [Block explorer: Filscan](https://filscan.io/)

:warning: [TODO - SAMPLE INFO ABOVE] :warning:
