# mbc-avalanche

## Due Date

November 25th at Midnight (call it gmt 0 time)

## Task of the Hackathon

## Terms

* Like Horizontal scaling instead of vertical scaling which has limitations

**C-Chain**: Seems like their EVM compatible L1 chain because you can use Solidity for it

Fuji: The Avalanche testnet

Foundry

Forge

Cast

Relayer

AWM Relayer

ERC20 Tokens

BuilderKit

Bridges

ICTT Bridges

AvaCloud

ICM

ICTT


Relayer

## What is Avalanche

* Performant blockchain that supports mulitple L1s on it
* Avalanche validator can be a validator for multiple L1s
* Primary network, the main L1 of Avalanche, all validators are a part of it
* Each L1 is meant to establish customized blockchain use cases

**Subnet Architecture**: Blockchain structure where there is primary network that every validator validates, and subsets of the entire set of validators validate other L1s and other chains, allows you to enable more transactions total on the network

**Cross-Chain Communication**: Idea where different chains can interact with each other by sending messages to each other

* A message in this context just means proof that an event occured
* Message should have authenticity, non-repudiation, and integrity
  * Authenticity: Message sender can be verified
  * Non-repudiation: Once you send a message you cannot unsend it
  * Integrity: Nobody can change the original message made by the sender

**Avalanche Warp Messaging**: Sender speaks to validators for the corresponding chain on publicly available network, then aggregates signatures of all validators for a very small signature instead of a very large list of many signatures

**Teleporter**: Message flow process on Avalanche, teleporters are typically done as smart contracts

* Warp messaging is abstracted away from developer
* You tell teleporter message, amount, receiving address, contract to send the message to
* Receiving dApp has a callback function to handle incoming messages from other teleporters

## Avalanche Consensus Mechanism

**Double spending attack**: You issue multiple transactions for values you don't have total in your wallet to different validators with the goal that different validators will approve your transactions and both will go through and you will spend currency you don't have

**Repeated Subsampling Voting**: Different validators may have preferences for which transactions to include, you ask randomly chosen validators which transaction they prefer and decide based on what they say, the amount of times you ask a random sample is called the decision threshold

* Helps resolve double spending attacks, but if just one transaction happens everyone very quickly agrees with no conflicts

**Time to Finality**: How much time it takes for one transaction to be fully verified and confirmed on the blockchain (like ping), 800ms for avalanche

**Throughput**: How many transactions can be decided on by the consensus mechanism in a certain amount of time (like bandwidth), 2500TPS for avalanche
