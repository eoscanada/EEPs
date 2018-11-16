---
eep: <to be assigned>
Title: Distribution of EOS Inflation Back to Voters That Have Voted For At Least 21 Block Producers
Author: Adam Zientarski <adam@eosdetroit.io>, Rob Konsdorf <rob@eosdetroit.io>, Santhosh Kumaraswamy, Angelo Laub, Matias Romeo
discussions-to: https://github.com/eoscanada/EEPs/issues/26
status: Draft
Type: Standard Track
category Interface
created: 2018-11-16
---

## Simple Summary
The consensus algorithm behind EOS, Delegated Proof of Stake, is more secure when more EOS tokens are being used to vote for block producers. This is due to the fact that a larger voter turnout reduces the influence of any one voting entity, making it less likely for individual voters or coalitions to unilaterally choose the top block producers.

This EEP puts forth a change to allocation of EOS’ 5% inflation in the following manner: 
 - 1% to block producers
 - 2% to voter rewards
 - 2% to the worker proposal system

The new 2% voter rewards pool will be distributed on a regular basis to accounts who vote for at least 21 block producers or proxy their vote to an account who votes for at least 21 block producers. This creates a direct incentive to vote on block producers, in order to increase voter turnout and demand for the EOS token.

## Abstract
This EEP was devised to create a direct incentive for EOS token holders to activate their stake via approval voting for at least 21 block producers. Today, voter turnout is about 40% of the total EOS tokens. Of that, only a fraction are voting for at least 21 block producers. Token holders who are voting need to consider the security of their account keys, and which block producers to vote for, both of which can be time consuming processes depending on their level of knowledge. By creating an incentive to do this work, more token holders will activate their stake and participate in the voting process, improving the overall security and health of the network.

## Motivation
Creative ways to combat voter apathy and improve the security of the network are vital for the success of EOS. Some ideas have been discussed and are being implemented, such as the REX. This EEP is meant to be complementary to the REX incentives.

## Specification
The technical specification should describe the syntax and semantics of any new feature. The specification should be detailed enough to allow competing, interoperable implementations for any of the current EOS platforms.

## Rationale
The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.

## Backwards Compatibility
All EEPs that introduce backwards incompatibilities must include a section describing these incompatibilities and their severity. The EEP must explain how the author proposes to deal with these incompatibilities. EEP submissions without a sufficient backwards compatibility treatise may be rejected outright.

## Test Cases
Test cases for an implementation are mandatory for EEPs that are affecting consensus changes. Other EEPs can choose to include links to test cases if applicable.

## Implementation
The implementations must be completed before any EEP is given status "Final", but it need not be completed before the EEP is accepted. While there is merit to the approach of reaching consensus on the specification and rationale before writing code, the principle of "rough consensus and running code" is still useful when it comes to resolving many discussions of API details.

## References

[Initial prototype work by Angelo Laub](https://github.com/angelol/eosio.contracts/commits/master)

## Copyright
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).