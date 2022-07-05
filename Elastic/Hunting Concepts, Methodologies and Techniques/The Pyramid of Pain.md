This model is more of a roadmap for accomplishing "the D's" we covered previously:

![[Pasted image 20220629181050.png]]

This model highlights the difficulties that adversaries have when different elements of their campaign are discovered and, importantly, shared. Threat hunting can uncover all of these tiers and, through the application of "the D's," we can harass, frustrate, and stress the adversary, which can cause them to move onto easier targets or make mistakes that, as hunters and defenders, we can capitalize on to evict them from the contested network.

#JA3 https://github.com/salesforce/ja3

JA3 is a method for creating SSL/TLS client fingerprints that should be easy to produce on any platform and can be easily shared for threat intelligence.

Fingerprinting these unchanging negotiations allows defenders to identify normal and abnormal TLS sessions

#YARA
YARA is a framework that performs pattern matching on files and can be used to create rules that can use identified tool patterns to ferret out other files used by the adversary

## TTPs Explained

As the name implies, there are three components to be found in the TPS category:

-   **Tactics.** These are the general, beginning-to-end strategies that threat actors use to access valuable systems and information. In other words, this is the “how” of cyberattacks. Hackers might choose to tap into confidential information or intrude into a website to accomplish their aims.
-   **Techniques.** These are the non-specific, intermediate methods or tools that a criminal will use to compromise your information. Phishing via email attachments is just one commonly employed example.
-   **Procedures.** These are the detailed descriptions of how the attacker plans to go about achieving their purpose. In other words, how will the general techniques be carried out in detail?