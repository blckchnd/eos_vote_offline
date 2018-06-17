# EOS VOTE OFFLINE

## Rationale

It is in the best interest of the entire EOS community to select block producers (a.k.a witnesses) sooner rather than later. The network will not be fully activated until at least 15% of tokens will have voted. And without fully activated network, no transfers or smart-contracts will be possible. At the same time we expect that many bad actors will try to exploit inexperienced users by providing fake voting tools aimed to steal their private keys and then access their EOS tokens.

## Why off-line?

Having the above situation in mind, [Tokenika](https://tokenika.io/) has decided to release a tool offering the possibility of **OFF-LINE** voting for block producers. Contrary to the on-line equivalent, with off-line voting, if done properly, at no point in time is your EOS private key exposed to the outside world. Thus the risk of being hacked is substantially reduced.

## How it works?
The main idea is to generate a voting transaction while being completely off-line and make sure the private key is used only for signing the transaction and is never exposed afterwards. The actual signing and key handling process uses only official EOSIO unmodified codebase. Thus the [eosjs](https://github.com/EOSIO/eosjs) library is the only external dependency, while the rest of the code is pretty short and simple.

## Three steps

The process of off-line voting is divided into three simple steps, each of them in the form of an HTML page served from the `https://eos.blckchnd.com` domain:

1. ON-LINE: [Fetch information about the network](https://eos.blckchnd.com/vote_offline/1_get_blockchain_data.html)
2. **OFF-LINE**: [Generate and sign transaction with your private key](https://eos.blckchnd.com/vote_offline/2_generate_transaction.html) 
3. ON-LINE: [Push the transaction to the network](https://eos.blckchnd.com/vote_offline/3_push_transaction.html)

**NOTE:** Please make sure the URL always starts with `https://tokenika.github.io/secure-bp-voting`.

**NOTE:** Step 2 is to be done **OFF-LINE**, ideally on a computer which has never been connected to the Internet.

## Text manual

[On russian](https://golos.io/eos/@on0tole/eos-zapushen-chto-dalshe)

## About

*EOS BLCKCHND VOTE OFFLINE* is an open-source software based on created by [Tokenika](https://tokenika.io/) service  [Secure EOS Block Producer Voting](https://github.com/tokenika/secure-bp-voting) created by [blockchained](https://eos.blckchnd.com)
an EOS block producer candidate. The source code is available at [https://github.com/blckchnd/secure-bp-voting/tree/russian](https://github.com/blckchnd/secure-bp-voting/tree/russian) on [MIT Licence](https://github.com/blckchnd/secure-bp-voting/blob/russian/LICENSE). 


## Feedback is welcome

We encourage the EOS community to audit our code and help us improve it. The source code is quite concise, so for anyone qualified it should not pose a problem to go through it. We would appreciate your comments if you find anything that needs our attention. 

## Legal disclaimer

The code in this repository is offered to the EOS community for peer review. Tokenika takes no responsibility for the execution and the results of the execution of this code. This code is provided as is, under [MIT Licence](https://github.com/tokenika/secure-bp-voting/blob/master/LICENSE).
