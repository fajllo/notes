# Module 01: Footprinting and Reconnaissance

## Scenario

Reconnaissance refers to collecting information about a target, which is the first step in any attack on a system. It has its roots in military operations, where the term refers to the mission of collecting information about an enemy. Reconnaissance helps attackers narrow down the scope of their efforts and aids in the selection of weapons of attack. Attackers use the gathered information to create a blueprint, or “footprint,” of the organization, which helps them select the most effective strategy to compromise the system and network security.

Similarly, the security assessment of a system or network starts with the reconnaissance and footprinting of the target. Ethical hackers and penetration (pen) testers must collect enough information about the target of the evaluation before initiating assessments. Ethical hackers and pen testers should simulate all the steps that an attacker usually follows to obtain a fair idea of the security posture of the target organization. In this scenario, you work as an ethical hacker with a large organization. Your organization is alarmed at the news stories concerning new attack vectors plaguing large organizations around the world. Furthermore, your organization was the target of a major security breach in the past where the personal data of several of its customers were exposed to social networking sites.

You have been asked by senior managers to perform a proactive security assessment of the company. Before you can start any assessment, you should discuss and define the scope with management; the scope of the assessment identifies the systems, network, policies and procedures, human resources, and any other component of the system that requires security evaluation. You should also agree with management on rules of engagement (RoE)—the “do’s and don’ts” of assessment. Once you have the necessary approvals to perform ethical hacking, you should start gathering information about the target organization. Once you methodologically begin the footprinting process, you will obtain a blueprint of the security profile of the target organization. The term “blueprint” refers to the unique system profile of the target organization as the result of footprinting.

The labs in this module will give you a real-time experience in collecting a variety of information about the target organization from various open or publicly accessible sources.

## Objective

The objective of the lab is to extract information about the target organization that includes, but is not limited to:

-   **Organization Information** Employee details, addresses and contact details, partner details, weblinks, web technologies, patents, trademarks, etc.
    
-   **Network Information** Domains, sub-domains, network blocks, network topologies, trusted routers, firewalls, IP addresses of the reachable systems, the Whois record, DNS records, and other related information
    
-   **System Information** Operating systems, web server OSes, location of web servers, user accounts and passwords, etc.
    

## Overview of Footprinting

Footprinting refers to the process of collecting information about a target network and its environment, which helps in evaluating the security posture of the target organization’s IT infrastructure. It also helps to identify the level of risk associated with the organization’s publicly accessible information.

Footprinting can be categorized into passive footprinting and active footprinting:

-   **Passive Footprinting**: Involves gathering information without direct interaction. This type of footprinting is principally useful when there is a requirement that the information-gathering activities are not to be detected by the target.
    
-   **Active Footprinting**: Involves gathering information with direct interaction. In active footprinting, the target may recognize the ongoing information gathering process, as we overtly interact with the target network.
    

## **Lab Tasks**

Ethical hackers or pen testers use numerous tools and techniques to collect information about the target. Recommended labs that will assist you in learning various footprinting techniques include:

1.  Perform footprinting through search engines
    
    -   Gather information using advanced Google hacking techniques
    -   Gather information from video search engines
    -   Gather information from FTP search engines
    -   Gather information from IoT search engines
2.  Perform footprinting through web services
    
    -   Find the company’s domains and sub-domains using Netcraft
    -   Gather personal information using PeekYou online people search service
    -   Gather an email list using theHarvester
    -   Gather information using deep and dark web searching
    -   Determine target OS through passive footprinting
3.  Perform footprinting through social networking sites
    
    -   Gather employees’ information from LinkedIn using theHarvester
    -   Gather personal information from various social networking sites using Sherlock
    -   Gather information using Followerwonk
4.  Perform website footprinting
    
    -   Gather information about a target website using ping command line utility
    -   Gather information about a target website using Photon
    -   Gather information about a target website using Central Ops
    -   Extract a company’s data using Web Data Extractor
    -   Mirror a target website using HTTrack Web Site Copier
    -   Gather information about a target website using GRecon
    -   Gather a wordlist from the target website using CeWL
5.  Perform email footprinting
    
    -   Gather information about a target by tracing emails using eMailTrackerPro
6.  Perform Whois footprinting
    
    -   Perform Whois lookup using DomainTools
7.  Perform DNS footprinting
    
    -   Gather DNS information using nslookup command line utility and online tool
    -   Perform reverse DNS lookup using reverse IP domain check and DNSRecon
    -   Gather information of subdomain and DNS records using SecurityTrails
8.  Perform network footprinting
    
    -   Locate the network range
    -   Perform network tracerouting in Windows and Linux Machines
9.  Perform footprinting using various footprinting tools
    
    -   Footprinting a target using Recon-ng
    -   Footprinting a target using Maltego
    -   Footprinting a target using OSRFramework
    -   Footprinting a target using FOCA
    -   Footprinting a target using BillCipher
    -   Footprinting a target using OSINT Framework