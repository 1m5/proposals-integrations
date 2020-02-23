---
layout: en
title: Evaluation for Censorship Resistance with 1M5 Integration
author: ObjectOrange
date: March 2020
amount: 75
milestones:
  - name: Integration Evaluation with Plan and Design Document Deliverable
    funds: 75
    done:
    status: unfinished
payouts:
  - date:
    amount:
  - date:
    amount:
---

# Evaluation for Censorship Resistance with 1M5 Integration
Proposal to evaluate Monero Network for Censorship Resistance by integrating [1M5](https://1m5.io) into its communication stack, inter-node and when accessing public nodes.

## Issue
[Censorship](https://en.wikipedia.org/wiki/Censorship) is the suppression of speech, public communication, or other information, on the basis that such material is considered objectionable, harmful, sensitive, politically incorrect or "inconvenient" as determined by government authorities or by community consensus. Monero, by providing a private decentralized crypto-currency not registered in any jurisdiction, is likely to come under attack by jurisdictions that consider it illegal.

Monero currently uses the clearnet to communicate internode although there have been attempts to integrate I2P and some do set it up to use TOR. TOR can be censored, [as is done in China](https://en.wikipedia.org/wiki/Internet_censorship_in_China#Using_Tor_and_DPI-resistant_tools), by discovering entry nodes and blocking them by IP. To block 2000 entry nodes is easy work as they are provided publicly and it's not a large list. Bridges do help, but have still remained an unreliable option. VPNs themselves are also targeted and blocked. But TOR is the ideal method to connect to public nodes (e.g. for pricing) as they normally are ran in the clear via the internet.

## Opportunities
The [Invisible Internet Project (I2P)](https://geti2p.net/en/) is much less known and thus less targeted. It works somewhat similarly to TOR with a few differences. Where TOR shines when accessing clearnet sites privately, I2P shines accessing other nodes running I2P, e.g. peer-to-peer networking apps like messaging. I2P doesn't have entry nodes, every node is a potential entry node and there are roughly 65,000 I2P peers (all I2P peers by default are contributors to the network). I2P, like any application, has its vulnerabilities, but they are an active team working to constantly improve it. There is no known attempts to block the I2P network globally although when cellular towers are turned off or the user is behind a severely restrictive firewall (e.g. corporate), even I2P will not work as it requires internet access. This is where Bluetooth and WiFi Direct have become helpful.

[Bluetooth](https://en.m.wikipedia.org/wiki/Bluetooth) and [WiFi Direct](https://en.wikipedia.org/wiki/Wi-Fi_Direct) support sending messages to nearby peers to share information. This has been used successfully in demonstrations in Hong Kong among others. But what they do not do is propagate out until a peer with internet access is available and use that peer to complete a request for an internet resource. Bluetooth and WiFi Direct are implemented using low-powered radios in phones and PCs and they're easily jammed (WiFi more so than Bluetooth). When in this position, shortwave communications is necessary.

Using the full [radio spectrum](https://en.wikipedia.org/wiki/Radio_spectrum) is the next major advancement in commercial radio communications and 1M5 is working with radio engineers globally to make this a reality. Adding [anti-jamming](https://en.wikipedia.org/wiki/Electronic_counter-countermeasure) capabilities additionally will enhance censorship resistance further. But what happens when you're under serious jamming? LiFi is the next battlefield.

[LiFi](https://en.wikipedia.org/wiki/Li-Fi) is short for Light Fidelity. It is basically wireless light communications. A dongle with a LiFi transceiver can send/receive light as data to/from another LiFi transceiver and the only method for blocking it is to physically block the light. Line-of-sight is required although some bouncing can be supported with degraded bandwidth and range and the frequency can be changed so that it is invisible to the human eye - it can be used in the dark without seeing any visible light.

## Proposal
Routing around blocks using TOR, I2P, Bluetooth, WiFi Direct, Full Spectrum Radio, and LiFi to ensure censorship resistance is the primary mission behind 1M5 - Invisible Matrix Services. It's designed to support additional future networks like Nym if/when they prove to be helpful. When integrated with Monero, 1M5 would ensure each node can find each other and maintain communications regardless how attacked, even with a national or global internet shutdown. It would also ensure the same level of censorship-resistance when accessing remote public nodes like price nodes...any public node.

Development would require integration with 1M5 as a proxy, testing the integration on testnet, then documenting it. In addition, a 1M5 Operator/Admin Role would be recommended to monitor and report on 1M5 effectiveness fixing any bugs that come up while providing an expected level of support.

1M5 is open source under the Unlicense 'license' and free to use.

1M5 currently uses TOR, I2P, and Bluetooth. Additional networks will be integrated in the future.

Currently, it is not known how best to do this so this project is just to evaluate the network stack, what it would take to integrate 1M5, and how it would be accomplished resulting in a second proposal with project breakdown.

## Notes
* The best timing for this integration is now. 
* Censorship of TOR is growing and I2P support in Monero appears to be a very unlikely event based on history. 
* Monero is known for its privacy. Let's make it know for censorship-resistance too.

### Resources
* [1M5 Site](https://1m5.io/)
* [1M5 GitHub](https://github.com/1m5)
* [1M5 Info Deck](https://1m5.io/assets/pdf/1m5-info-deck.pdf)
* [1M5 Whitepaper](https://1m5.io/assets/pdf/1m5-wp.pdf)
* [1M5 Docs](https://github.com/1m5/1m5-docs)
* [ObjectOrange GitHub](https://github.com/objectorange)
* [ObjectOrange LinkedIn](https://www.linkedin.com/in/decentralizationarchitect/)

