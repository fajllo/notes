## Signature-based detections
Signature-based detections are what is thought about for traditional security operations. Platforms such as antivirus (yes, it's still a thing), Intrusion Detection/Prevention Systems (IDS/IPS), and firewall blocks are examples of signature-based detections. While these are table-stakes (love or hate that term) for security operations, they block a smaller and smaller percentage of threats because they rely on previously identified threats being analyzed and rules/signatures being created from a "known bad."


## Behavior-based detections
Behavior-based detections are things that are either a derivative of "known bad" or leverage known good binaries/trusts/processes to perform malicious operations. Some examples of behavior-based detections are the following: • Authenticating from two different locations at the same time • Authentications occurring closely chronologically, but over a large geographic distance (such as an authentication from San Francisco, CA, USA and then another authentication from Paris, France 1 hour later) • Network connections originating from a program that doesn't require a network connection (notepad.exe, vi, or textEdit) One of the most powerful tools in behavior-based detection is YARA, which as described earlier, is a pattern-matching framework for files. To create YARA rules, analysts and operators analyze malicious files to identify strings that can be grouped into conditions to identify that known-bad file as well as derivative files that are similar.

## "Living Off the Land" binaries (LOLBins)
As we've mentioned before, it's an "arms race" between attackers and defenders. As defenders have gotten better at detecting malicious files, attackers have started working hard to blend into the environment. One of the ways they've done that is by using LOLBins. LOLBins are legitimate programs that are present on many systems. While these programs have authorized uses and purposes, they can be used to perform nefarious functions. The fact that they can be used legitimately makes it very difficult to detect when they are being abused.

• At.exe – This program can be used to schedule tasks, but also to maintain persistence.
• pip – This program can be used to install Python packages, but it can also be used to upload and download files or even spawn interactive shells.
• Powershell.exe – This program is an automation and scripting framework, but it can also be used to load and build malware directly onto a compromised system.


![[Pasted image 20220701133328.png]]