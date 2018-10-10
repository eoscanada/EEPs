---
eip: 2
title: EOS Verificatoin of Web Properties
author: Josh Kauffman <josh@eoscanada.com>
status: Draft
type: Informational EEP
category: N/A
created: 2018-10-10
---

## Rationale

There is currently no trusted mechanism by which an EOS account owner can have their account verified. By adopting a structure 
similar to [Keybase's](https://keybase.io) verification system, an EOS user will be able to link their account to multiple 
web properties that they are in control of. This can be used to increase trust of an account, so that another user will 
be more or less inclined to enter into a transaction with them. 

The goal is to introduce increased trust into the ecosystem. We envision that Block Explorers will be able to scrape
data from this mechanism to display verified properties. 

## Specification

1. A user controlling an EOS account who wishes to have their web property verified will push a transaction towards 
the EOS account `accountsjson` which exists on the EOS mainnet 
(chain ID: aca376f206b8fc25a6ed44dbdc66547c36c6c33e3a119ffbeaef943642f0e906)
2. The transaction should include a json string that contains the information which they wish to link to their account.
3. A user can update the information by sending a new transaction. The most recent transaction will be the only one
that the system uses.

## Proposed JSON:
```
owner {account_name}
json:
{
“website”: “https://example.com/about_eos”
“twitter”: “https://twitter.com/{twitter_handle}/status/{tweet_ID}”
“telegram”: {telegram_handle}
“facebook”: “https://www.facebook.com/{account_name}/about?lst={ID}&section=bio”
“reddit”: “https://www.reddit.com/r/EOSAccountProofs/comments/{ID}/{owner}/”
“github”: https://gist.github.com/{github_handle}/{ID}
“source_contractname”: 
“nextsource_contractname”: 
“updateproposal_contractname”: 
}
```

## Breakdown

*Owner* - The account name that is looking to be verified

*Website* - The URL that an account wants to be associated to. It will need to have a file within the top-level called
{account_name}.txt that contains nothing other than the account name within.

*Twitter* - The URL of the tweet where a user posts "I am the owner of the EOS account {account_name}."

*Telegram* - The Telegram handle that an account wants to be associated to. Within the bio of the account, a user will
have to enter #eosproof {account_name}.

*Facebook* - The URL of the 'About/Details About You' section, where the user will have to enter #eosproof {account_name}.

*Reddit* - The URL of the post titled {account_name} that a user creates within the subreddit /r/EOSAccountProofs in which they enter
I am the owner of the EOS account {account_name}.

*GitHub* - The URL of the gist with the filename eosproof.md containing the text I am the owner of the EOS account 
{account_name}.


### Implementation

