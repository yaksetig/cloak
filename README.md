# Cloak
In this document, we describe our grant application for building the Cloak Wallet.


## Project description

Cloak is a novel state-of-the-art wallet design that integrates different components not present in any wallet to date. Concretely, the use of quantum-secure fallbacks from [ W-OTS(+) up my Sleeve](https://eprint.iacr.org/2021/872), which can be considered a variant of a proof of complete knowledge as introduced by Kelkar, Babel, Daian, Austgen, Buterin, and Ari Juels, along with simple ECDSA fail-stop signatures from [here](https://eprint.iacr.org/2024/473).

This work would also feature a first implementation (besides SPHINCS+) of **WOTS-TW**, a simpler secure one-time hash-based signature scheme used specifically for the quantum-secure fallbacks.

A quantum secure fallback is the ability of a user to provide a proof of ownership of a wallet even when the secret key is compromised (for example, in the case of a quantum computer breaking the ECDLP). This is also applicable in a setting where a hacker or a malicious adversary is able to gain access to the secret key. Both scenarios are effectively equivalent from the perspective of the user. The secret key is compromised in both settings. 



Expected use cases:

* **More secure voting** (provide stronger coercion resistance via proof of complete knowledge)

* **ZK Vault** functionality (users can lock valuable assets inside a smart contract vault that only gets unlocked with an additional zero-knowledge (i.e., ZK-SNARKs) proof of knowledge. 

* **Quantum-secure fallback** (users can provide a proof of ownership of a wallet in case it's compromised) and a **quantum-secure vault** (users can lock valuable funds inside a quantum-secure vault that uses a different quantum-secure key pair to be unlocked). This is an even stronger variant than the previously mentioned ZK Vault. 

* **Potential insurance use cases** against wallet hacks (users can produce a proof-of-ownership to trigger a "theft alert", similar to a credit card dispute). This was not possible in traditional wallets. 

* **(Simple) Fail-stop signatures** (ability for a user to prove that a signature is correctly formed and potentially prove against hacks). Combined with covenants, this is a particularly interesting protection for the different funds of users. 

(Goals) - This project aims at closing the gap between the strong theoretical work done in the cryptography space and the actual primitives that see adoption in the real-world crypto(currency) space. We want to bring better cryptography to the masses and make it more usable in this process. 
 
(Benefits for ecosystem) - Further security for all the users in general, mitigation of phishing attacks (via ZK vault), long-term quantum security embedded in any wallet in the ecosystem.  This design allows for the incorporation of any quantum-secure key pair within any regular wallet. Our system is very flexible and, therefore, compatibility with any post-quantum signature scheme is possible within the quantum-secure fallback primitive. 


## Roadmap

Q4 2024:

* Set up of public open-source Github repo 

* Initial paper describing the design and its properties

* Integration of the double mnemonic system (regular + quantum-fallback)

* Initial implementation of the proof of complete knowledge addresses on chain (via ZK Proofs)

Q1 2025:

* ZK vault(s) where a smart contract locks funds and can unlock funds when a particular ZK proof of complete knowledge is provided. 

* Quantum-secure vault(s) where users can lock assets, which can only be unlocked when a post-quantum signature is provided. This is particularly useful for high-value funds and prevent phishing attacks

Q2 2025:

* Initial UI/UX App implementing all the above features and ready to be used

Q3 2025:

* Final App ready to be downloaded by users

* ZK & Smart Contract Audit

## Budget & milestones

We are requesting a total of $165,000. We believe this to be a project of medium-scale due to the intrinsically challenging primitives involved in this wallet design. Funds will be allocated completely to cover for the development of the software over a period of 12 months. 

* Milestone I ($20,000): Kick-off payment to begin the project and fund the team for an initial development.

* Milestone II ($15,000): Paper describing the wallet protocol, along with the cryptographic primitives and its properties

* Milestone III ($15,000): Proof of complete knowledge addresses, where an owner publishes a proof of knowledge of the secret key of the wallet.

* Milestone IV ($25,000): Smart Contract ZK Vault

* Milestone V ($30,000): Quantum-secure smart contract vault

* Milestone VI ($35,000): UI/UX visual app

* Milestone VII ($25,000): Audit of the smart contract(s) and ZK Circuits

## KPIs
The key performance indicators for such a project are:


* Number of users

* Number of complete knowledge addresses

* TVL in smart-contract vaults

* Usability of the wallet app

We believe this is the most straightforward and tangible way to measure the success, traction, and growth of the project. 

## Team

[Mario Yaksetig](https://scholar.google.com/citations?user=deXRtJwAAAAJ) - Applied cryptographer who worked with David Chaum, the creator of e-cash and online anonymous communications, on the design of novel protocols for the blockchain space. Mario's L2 work has been cited by Vitalik Buterin and is one of the creators of the quantum secure fallback primitive. Mario also wrote a [paper](https://eprint.iacr.org/2024/552.pdf) on how the Avalanche architecture is great for a blockchain-powered metaverse. 

[Alexander Havlin](https://scholar.google.com/citations?user=QRBlsTIAAAAJ) - Cryptography engineer who co-authored an attack against a hash-based threshold signature scheme created by Vitalik Buterin. This work was published at [ACM CCS](https://www.sigsac.org/ccs/CCS2023/) as a [poster](https://dl.acm.org/doi/10.1145/3576915.3624393) in 2023. Alex uses Circom to develop ZK circuits and is proficient in Solidity. 

UI/UX Specialist - The team will recruit a specialist in the user interface field to help execute on the user front and ensure that the app is usable and can compete with other wallets in the different ecosystems. 

Feasibility of the proposal: The team is experienced in the design and development of new cryptographic protocols, the UI element is the one to be outsourced. Therefore, the main risk of execution lies on having a very usable UI/UX at the highest level. 

Additional remarks: The team is based in Cayman Islands, a crypto friendly jurisdiction. The team members are originally from Portugal and Cayman and are not in an OFAC sanctioned jurisdiction. This should result in a smooth KYC process. 

## Contact details
Telegram: @myaksetig
Email: myaksetig@gmail.com
