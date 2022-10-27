---
permalink: /
---

# Ruggability - know the risks before it's too late

## Motivation

The combined factors of anonymity, 6+ figures of cash and transaction finality provide unprecedented incentives for scammers of all sorts to run away with your money. There's therefore no surprise that every week we [witness](https://web3isgoinggreat.com/?theme=rugPull) new massive rug pulls.

This website is an attempt to uncover the different centralization and permission threats that exist in different Web3 projects. Armed with knowledge, investors and speculators can choose where to pour their funds fully understanding the risks involved.

## Format

Each project will be described using several metrics:

1.  Anonymity - are key project members anonymous?
2.  Contract upgradeability - How easily can the project "change the rules" by upgrading proxy contracts
3.  Asset risk - are special addresses permitted to handle user's assets?
4.  Multisig - Is the owner address a multisig smart wallet? Only applicable to dangerous operations
5.  Timelock - Is there a lock time period before any dangerous protocol operation?
6.  Additional - Threats not handled by the above metrics go here. For example, for stablecoins, is the backing strategy adequate? What are possible pitfalls?

## Disclaimer

Users are 100% responsible for any use of the information contained on this website. We do not guarantee any of the provided information is correct, up-to-date, or reliable. DYOR.

## Contribution

Any contribution to the Ruggability database is more than welcome. Please open an ISSUE or a PULL REQUEST and we'll make sure to include it and add your name to the contributors list.

# The Ruggability Database

## Holograph - Globally unique NFT platform

|     |     |
| --- | --- |
| Anonymous | Yes |
| Contract upgradeability | Yes. Can attach new addresses to the [Holograph](https://github.com/holographxyz/holograph-protocol/blob/c4_audit/contracts/Holograph.sol) entry point |
| Asset risk | Owner can [forge](https://github.com/holographxyz/holograph-protocol/blob/b39a61ca53f97fcae8a39f92c2285d6b57a16de0/contracts/module/LayerZeroModule.sol#L190) any bridging in message from another chain, by changing the registered Layer Zero approved sender. |
| Multisig | No  |
| Timelock | No  |
| Additional |     |

## The Graph ETH <-> Arbitrum GRPH token bridge

|     |     |
| --- | --- |
| Anonymous | No  |
| Contract upgradeability | Yes. Can attach new addresses to the [Holograph](https://github.com/holographxyz/holograph-protocol/blob/c4_audit/contracts/Holograph.sol) entry point |
| Asset risk | Governor can [approve](https://github.com/graphprotocol/contracts/blob/7b383140ba5430a564d3caecb1074b31f5497bab/contracts/gateway/BridgeEscrow.sol#L28) bridge tokens held in escrow to any address. |
| Multisig | On chain governance |
| Timelock | -   |
| Additional |     |

## OpenSea - Leading NFT marketplace

|     |     |
| --- | --- |
| Anonymous | No  |
| Contract upgradeability | No  |
| Asset risk | No  |
| Multisig | N/A |
| Timelock | N/A |
| Additional | Owner can pause marketplace |

## Iron Bank - Lending platform

|     |     |
| --- | --- |
| Anonymous | Yes |
| Contract upgradeability | Unitroller (key logic contract) and vaults can be [upgraded](https://docs.ib.xyz/#protocol-contract) |
| Asset risk | Vaults can be [upgraded](https://etherscan.io/address/0x41c84c0e2ee0b740cf0d31f63f3b6f627dc6b393#readContract) with multisig, no timelock |
| Multisig | [Yes](https://docs.ib.xyz/governance) |
| Timelock | 2 Days. No timelock for emptying [reserve](https://docs.ib.xyz/governance) |
| Additional |     |

## Fringe Finance - Lending platform

|     |     |
| --- | --- |
| Anonymous | Yes |
| Contract upgradeability | Yes |
| Asset risk | Yes |
| Multisig | No  |
| Timelock | 7 days for [upgrades](https://etherscan.io/address/0xfb872a364e63950f9847a39202bb4d1c07534466#readContract) by ProxyAdmin |
| Additional | Normal admin can add new project token, fake high value using rogue oracle, use it as collateral to steal entire [vault](https://etherscan.io/address/0x9fD0928A09E8661945767E75576C912023bA384D?utm_source=immunefi#readProxyContract#F5). |
