# Semaphore Network EthSIM Wallet

### DO NOT USE TO STORE VALUABLES. VERY MUCH A WORK IN PROGRESS

## What?
The Semaphore Network EthSIM Wallet aims to allow anyone to turn ANY cellphone into a secure airgapped hardware wallet for Ethereum transactions.

## TLDR Features:
*  Novel first (afaik) partial raw re-implementation of SIM Toolkit (STK) features, without the sim.*/uicc.* proprieteary API ROM blob
*  allows ANY javacard to be used. NO TELCO GATEKEEPING
*  The ability to display menus, [hidden]inputs and outputs that create a Hardware Wallet UI interface directly on-card.
*  Leverages Secure Element for keygen, signing, PIN etc.

## Future:
- [-] hashing on card.
- [-] tx/rlp generation on card.

## How?
By combining a cheap(~$10) secure element SIM-sized JavaCard/Smarcard and almost ANY cellphone;
The Semaphore Network EthSIM platform enables an extremely low cost, secure and open hardware wallet experience.

<!-- <VIDEO> -->

## Background:
Almost everyone knows about the SIM card that goes in your phone, billions are produced annually and as such are probably one of the most ubiquitious electronic devices in the world. What remains elusively packed away inside that SIM card, is that it runs a subset of a secure computing platform called Javacard.

Javacard is a predominant smartcard and secure element platform used by many manufacturers; if you use a hardware wallet or secure element today chances are that you're using a Javacard at some level. Grid+, Status Keycard, Yubikey(partial? ), Ledger(partial) and Kong all use Javacard secure elements at their core.

So clearly a Javacard, provided the right software can do both **crypto stuff** AND **phone stuff**.
The phone stuff is important to Semaphore Network as we build out a truely decentralized cellular network.
A key differientiator of our network is using self soverign Ethereum cryptographic identity, at the core network layer.
The management of these keys can be cumbersome, especially if the phones of a truely global audience might not even have an app store.

Therefore, we needed a truly universal way to deliver UI to our users, something absent app stores, walled gardens etc.
On our quest give power back to the people, we stumbled across a piece of ancient telco knowledge....

## SIM Toolkit (STK):
A little known protocol for creating simple apps -
something that predates app stores by about a decade -
Ability to display menus, [hidden] input and output built into literally every phone since the mid-90s!

You might remember it from feature phones of yester-year. Maybe on that European trip in 2005 you bought some more minutes through an obscure payment menu embedded deep into your Moto Razr.... That was SIM Toolkit.

So what's the big deal? Until now, the intersections of phone Javacard technology and crypto Javacard technology were out of reach. The SIMToolkit API is proprieteary; you have to be telco adjacent, know a card manufacturer and/or have large MOQ orders AND pay extra to have this feature included in custom Javacards.

Not anymore! we've started a byte level rewrite of this functionality and are sharing it here in our hardware wallet implementation.

## Limitations:
There are many pros cons
