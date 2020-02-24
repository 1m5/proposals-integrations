# Evaluation for Censorship Resistance with 1M5 Integration
Proposal to evaluate Monero Network for Censorship Resistance by integrating [1M5](https://1m5.io) into its communication stack, inter-node and when accessing public nodes.

## Issue
[Censorship](https://en.wikipedia.org/wiki/Censorship) is the suppression of speech, public communication, or other information, on the basis that such material is considered objectionable, harmful, sensitive, politically incorrect or "inconvenient" as determined by government authorities or by community consensus. Monero, by providing a private decentralized crypto-currency not registered in any jurisdiction, is likely to come under attack by jurisdictions that consider it illegal.

Monero currently uses the clearnet to communicate internode although there have been attempts to integrate I2P and some do set it up to use TOR. TOR can be censored, [as is done in China](https://en.wikipedia.org/wiki/Internet_censorship_in_China#Using_Tor_and_DPI-resistant_tools), by discovering entry nodes and blocking them by IP. To block 2000 entry nodes is easy work as they are provided publicly and it's not a large list. Bridges do help, but have still remained an unreliable option. VPNs themselves are also targeted and blocked. But TOR is the ideal method to connect to public nodes (e.g. for pricing) as they normally are ran in the clear via the internet.

The latest support in Monero for both TOR and I2P is discussed in this file: https://github.com/monero-project/monero/blob/master/ANONYMITY_NETWORKS.md. It claims that it's still experimental and requires much manual setup of TOR hidden services and I2P. It requires manual TOR hidden service setup and port selection and manual selection of TOR and I2P peers instead of random TOR ports and building up a network of peers through discovery. It does nothing regarding the ability to relay broadcasts through alternative networks when TOR and/or I2P is getting blocked in the local node. The lack of some intelligent routing mechanism between anonymity internet overlay networks, alternative radio networks, and LiFi is the reason for interest in integrating 1M5 into the communication stack. Having a team on this full-time focused solely on censorship-resistance is a necessity if not immediate, it will be with no doubt.

## Opportunities
The [Invisible Internet Project (I2P)](https://geti2p.net/en/) is much less known and thus less targeted. It works somewhat similarly to TOR with a few differences. Where TOR shines when accessing clearnet sites privately, I2P shines accessing other nodes running I2P, e.g. peer-to-peer networking apps like messaging. I2P doesn't have entry nodes, every node is a potential entry node and there are roughly 65,000 I2P peers (all I2P peers by default are contributors to the network). I2P, like any application, has its vulnerabilities, but they are an active team working to constantly improve it. There is no known attempts to block the I2P network globally although when cellular towers are turned off or the user is behind a severely restrictive firewall (e.g. corporate), even I2P will not work as it requires internet access. This is where Bluetooth and WiFi Direct have become helpful.

[Bluetooth](https://en.m.wikipedia.org/wiki/Bluetooth) and [WiFi Direct](https://en.wikipedia.org/wiki/Wi-Fi_Direct) support sending messages to nearby peers to share information. This has been used successfully in demonstrations in Hong Kong among others. But what they do not do is propagate out until a peer with internet access is available and use that peer to complete a request for an internet resource. Bluetooth and WiFi Direct are implemented using low-powered radios in phones and PCs and they're easily jammed (WiFi more so than Bluetooth). When in this position, shortwave communications is necessary.

Using the full [radio spectrum](https://en.wikipedia.org/wiki/Radio_spectrum) is the next major advancement in commercial radio communications and 1M5 is working with radio engineers globally to make this a reality. Adding [anti-jamming](https://en.wikipedia.org/wiki/Electronic_counter-countermeasure) capabilities additionally will enhance censorship resistance further. But what happens when you're under serious jamming? LiFi is the next battlefield.

[LiFi](https://en.wikipedia.org/wiki/Li-Fi) is short for Light Fidelity. It is basically wireless light communications. A dongle with a LiFi transceiver can send/receive light as data to/from another LiFi transceiver and the only method for blocking it is to physically block the light. Line-of-sight is required although some bouncing can be supported with degraded bandwidth and range and the frequency can be changed so that it is invisible to the human eye - it can be used in the dark without seeing any visible light.

## Proposal
Routing around blocks using TOR, I2P, Bluetooth, WiFi Direct, Full Spectrum Radio, and LiFi to ensure censorship resistance is the primary mission behind 1M5 - Invisible Matrix Services. It's designed to support additional future networks like Nym if/when they prove to be helpful. When integrated with Monero, 1M5 would ensure each node can find each other and maintain communications regardless how attacked, even with a national or global internet shutdown. It would also ensure the same level of censorship-resistance when accessing remote public nodes like price nodes...any public node.

Development would require integration with 1M5 as a proxy, testing the integration on testnet, then documenting it. In addition, a 1M5 Operator/Admin Role would be recommended to monitor and report on 1M5 effectiveness fixing any bugs that come up while providing an expected level of support.

1M5 is open source under the Unlicense 'license' and free to use.

1M5 currently uses TOR, I2P, and Bluetooth. WiFi-Direct, Full Spectrum Radio (including Locha Mesh if it works out), and LiFi will be integrated in the future.

Considering TOR and I2P is currently supported by following the directions in this file: https://github.com/monero-project/monero/blob/master/ANONYMITY_NETWORKS.md, it is believed by the author that implementation could be used to change the proxy to 1M5 so that the networks are setup automatically as much as possible, networks are chosen based on their status, while also allowing the end user to constrain which networks are to be used based on their current situation, e.g. a new laws comes out threatening prison time if using Monero yet TOR/I2P are not being physically blocked. Implementation should be as easy as replacing the proxy configuration to this: --proxy 1m5,127.0.0.1:2020,10 and ensuring all communications are able to use the proxy vs just transactions. This will require work in 1M5 to support running its platform daemon as a proxy which hasn't been implemented yet. Initial work will be to just replace the transaction proxy so that it can be a third option for testing out the router. Future work on testing success of tx proxy integration could be to move all comms to the proxy and add options to a Monero GUI for enabling the manual overriding of what networks to use/not use by the end user based on their perceived situational awareness (threats).

The exact amount of work is not known although 75 XMR appeared steep to a member of the community for two weeks work. So I think it might be a good idea too to follow a monthly minimal payout based on progress to show engagement and progress to reduce risk.

March, April, May 2020: 50 XMR (~$4,000) each
Total: 150 XMR

Milestones:

1. EOM March 2020 - Reverse-engineer current TOR/I2P proxies to determine API required to support as a proxy, document, and setup 1M5 project for implementation
2. EOM April 2020 - Implement 1M5 API to support Monero transactions and document
3. EOM May 2020 - Develop and use Test framework to ensure transactions validate correctly using testnet and demo

## Likely Future Proposals

* An Admin Role at minimal monthly expense to maintain and improve on 1M5 for Monero
* Full support of all communications through 1M5 to ensure censorship-resistance of all comms
* Additional sensor testing with Monero as new sensors come on-line
* Addition of manual control over the 1M5 router sensor selection through GUIs

## Progress updates

Updates will be shared as tasks are finished in GitHub (https://github.com/1m5/1m5). Our website (https://1m5.io) will be updated to reflect the work with and support by Monero. Upon successful testing of Monero with 1M5 resisting manual censorship attempts, we will promote the relationship if desired by our main speaker Amin Rafie (https://arafiee.com/) during events.

## Notes
* The best timing for this integration is now. 
* Censorship of TOR is growing and I2P will be next. Automatic dynamic selection of networks routing around blocks while ensuring manual selection is needed.
* Monero is known for its privacy. Let's make it know for censorship-resistance too.

## Resources
* Brian Taylor Email: [brian@resolvingarchitecture.io](mailto:brian@resolvingarchitecture.io) GPG: 2FA3 9B12 DA50 BD7C E43C 3031 A15D FABB 2579 77DC (backed by protonmail)
* ObjectOrange Email: [objectorange@1m5.io](mailto:objectorange@1m5.io) GPG: DD08 8658 5380 C7DF 1B4E 04C2 1849 B798 CF36 E2AF (backed by protonmail)
* [1M5 Site](https://1m5.io/)
* [1M5 GitHub](https://github.com/1m5)
* [1M5 Info Deck](https://1m5.io/assets/pdf/1m5-info-deck.pdf)
* [1M5 Whitepaper](https://1m5.io/assets/pdf/1m5-wp.pdf)
* [1M5 Docs](https://github.com/1m5/1m5-docs)
* [ObjectOrange GitHub](https://github.com/objectorange)
* [ObjectOrange LinkedIn](https://www.linkedin.com/in/decentralizationarchitect/)
