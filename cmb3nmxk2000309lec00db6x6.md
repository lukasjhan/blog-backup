---
title: "Time for Credential-Based Authentication"
datePublished: Sun May 25 2025 12:48:35 GMT+0000 (Coordinated Universal Time)
cuid: cmb3nmxk2000309lec00db6x6
slug: time-for-credential-based-authentication
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/o0kPG3RirHs/upload/1b6a54eea96d385a1a1840d4ad10afae.jpeg
tags: hacking, digital-identity, cybersecurity-1

---

In April 2024, a massive hacking incident at SK Telecom, South Korea's largest mobile carrier, exposed fundamental vulnerabilities in our digital authentication systems. This incident provides a crucial opportunity to examine why we must transition to a credential-based authentication paradigm.

## What Was Compromised?

SK Telecom's core server, the HSS (Home Subscriber Server), was infected with sophisticated malware called BPFDoor, leading to the mass theft of the following information:

* **IMSI (International Mobile Subscriber Identity)**: International mobile subscriber identification numbers
    
* **IMEI (International Mobile Equipment Identity)**: Device unique identifiers (uncertain if compromised)
    
* **Authentication Keys**: Core information used for SIM authentication
    
* **MSISDN**: Phone numbers
    
* **Personal Information**: Names, dates of birth, etc.
    

Approximately 27 million IMSI records were confirmed compromised, meaning that information for most SKT subscribers was exposed. What's particularly concerning is that this information doesn't exist in isolation—it forms complete communication profiles when connected together.

## What Attacks Became Possible?

### The Threat of SIM Swapping and USIM Cloning

The most immediate threat enabled by this breach is SIM swapping attacks. Attackers can transfer a victim's phone number to their own SIM card, intercepting text-based authentication to access financial services or social media accounts.

More seriously, USIM cloning attacks became possible. Particularly when USIM cloning is combined with IMEI spoofing, it becomes extremely difficult for carriers to distinguish between legitimate users and attackers. While SKT claims to have strengthened their FDS (Fraud Detection System), this provides only probabilistic defense and cannot guarantee complete protection.

In practice, attackers can combine sophisticated social engineering attacks, such as impersonating government agencies to request device reboots, then attempting SIM swaps during those brief moments. Against such complex attacks, individual users find it nearly impossible to protect themselves.

## Fundamental Limitations of the Current System

### The Disaster of Centralized Architecture

The current carrier-centric authentication system inherently relies on a centralized structure. Having all subscriber core information concentrated in a single HSS server represents an enormous security risk in itself. This incident demonstrates the realization of such structural vulnerabilities.

The bigger problem is that this information is static. Once generated, IMSI or authentication keys remain the same unless the SIM is replaced. Therefore, once compromised, they can be continuously exploited with no fundamental way to prevent it. This is why SKT decided to replace all customers' SIM cards.

However, SIM replacement cannot be a fundamental solution. If new SIMs are issued using the same structure and methods, the same problems can recur with another hack at any time. It's like replacing only the lock on a broken house while leaving the fence and security system unchanged.

## Credential-Based Authentication: A New Paradigm

### The Era of Self-Sovereign Identity

We need an entirely new approach. Credential-based authentication is based on the concept of Self-Sovereign Identity, where users directly manage their own digital identities. This represents not just a technical change, but a philosophical shift in how we manage identity in the digital age.

An ID Wallet is a digital wallet securely stored on a user's device, containing Verifiable Credentials. These credentials have dynamic characteristics—they can be created, used, and revoked as needed. Even if someone steals a credential, it's likely already expired or restricted to work only under specific conditions.

### Combining Device Binding with Multi-Factor Authentication

Device Binding is a crucial element of this system. It's not simply about software-level information, but binding identity to devices at the hardware level. Using hardware security modules like TPM (Trusted Platform Module) or Secure Elements makes it virtually impossible to clone authentication information without physically stealing the device.

Combining this with various authentication factors—biometrics, PINs—creates even stronger security. Even if attackers steal some information, they cannot succeed in authentication without the remaining factors. This provides a fundamentally different security level compared to the current single-factor (SIM) dependent system.

Additionally, credential-based systems enable 'Selective Disclosure.' For example, when accessing age-restricted services, instead of providing your entire resident registration number, you can present a credential that only proves "I am over 19 years old." This innovative approach simultaneously enhances both privacy protection and security.

## Conclusion: A Transition We Can No Longer Delay

The SKT hacking incident is not just a security breach—it reveals the structural limitations of our current digital authentication system. A system where 27 million people's information can be compromised at once is no longer sustainable.

The transition to credential-based authentication has already reached a technologically feasible level. W3C's DID (Decentralized Identifiers) and Verifiable Credentials standards are established, and notably, the W3C Verifiable Credentials Data Model 2.0 was officially published in May, 2025, providing an even stronger standards foundation. Many countries and companies are already conducting pilot projects based on these standards. What we need is not technology, but the will to accept and implement change.

Carriers must prepare to transform their role from managers of all authentication information to trusted authentication service providers. Governments must establish the legal and institutional frameworks to support new authentication systems. And we all must renew our understanding of what digital identity means and how it should be protected.

In the wake of the SKT incident, it's time to accelerate the transition to a safer, more user-centric digital authentication system. Before the next hack occurs, we must begin fundamental change.

---

*This article was written reflecting on the future of digital authentication following the SKT SIM hacking incident. Everyone's attention and participation are needed for a safer digital environment.*