# How to Create Incident Response Plan?
## What is incident response?

  
Incident response is an approach to managing a security incident process. An incident response plan is needed to approach security incidents systematically. A successful incident response plan includes the following 6 stages:

1- Preparation  
2- Identification  
3- Scope  
4- Eradication  
5- Recovery  
6- Lessons Learned

  
  

## 1- Preparation

  
**Creating a Central Registration System**

It is important in terms of saving time that all data can be examined from a single point with a central log collection system that can manage large files.

  
**Time Synchronization**

Enabling [NTP](https://pl.wikipedia.org/wiki/Network_Time_Protocol) on all devices in the network is important for matching the time information of the logs collected.

  
**User Account Management**

The fact that the user names of different accounts belonging to personnel are the same and different from other personnel makes it easy to monitor user activities in the event of an incident.

  
**Management of System and Service Accounts**

The administrators of the services and systems used should be appointed and a document should be created on how to reach these managers if needed.

  
**Asset Management**

Instant access to information such as devices, operating systems, patch versions, and critical status should be available.

  
**Secure Communication**

If necessary, the team may need to communicate independently of the internal network, for such cases mobile phone or secondary emails can be used.

  
**Legal Transactions**

The method of who will initiate the judicial process and in which situations should be determined before the incident occurs.

  
  

## 2- Identification

  
**Review**  
For a potential suspicious incident, preliminary information about the incident should be gathered. Then it must be decided whether the situation is a suspicious event or not.

  
**Assignment**  
The first person to examine the incident must be determined. The person should take notes about the review.

  
**Using the Checklist**  
There should be checklists for the analysis to be made in order to ensure consistent responses to incidents.

  
  

## 3- Scope

  
**Characterize the event**

Since determining the event will determine the actions to be taken, it is important to determine the type of the incoming event. EX: DDoS, malware infection, data leak …

  
**Taking Action**

Action should be taken according to the technique used to intercept the attacker's method quickly. If there is an account that it has captured, simple measures such as account deactivation and IP blocking should be done quickly.

  
**Data collecting**

The image of the volatile memory along with the firewall, network traffic and other logs will be required for the investigation.

  
**Isolation**

Unplugging the compromised system could be a solution, isolating it is a more viable solution.

After the systems affected by the incident are determined, the possibility of the attacker's spread in the network is cut and volatile information is collected, the next step can begin.  
  
  

## 4- Eradication

  
**Identifying the Root Cause**

With the information obtained in the 2nd and 3rd stages, the root cause of the event should be determined. The attacker must then be completely eliminated.

  
**Determining Rootkit Potential**

If rootkits are suspected in the system, the disk should be cleaned and a clean backup installed. After the installation, the latest updates of the existing applications and systems should be installed.

  
**Improve Defense**  
Operating systems, applications used, network, DMZ etc. The deficiencies of defense in areas should be determined and work should be done on how to make improvement.

  
**Vulnerability Scan**

Potential attack points on networks and systems should be identified and corrected by performing vulnerability scans.

When the necessary arrangements are prepared to prevent the event from recurring, the recovery phase can be started.

  
  

## 5- Recovery

  
**Verification**

Verify that logging, systems, applications, databases, and other operations work correctly.

  
**Restore**

At this stage, the restore operation is coordinated.

  
**Monitoring**

Systems should be monitored for recurring events.

When there is no repetitive harmful situation or unusual activity, the next step is taken.

  
  

## 6- Lessons Learned

  
**Writing a Follow-up Report**

The report includes the examinations with the expert and the executive, the stages of good and bad working in the intervention plan, and the recommendations regarding the process. The report should be written in a way that the manager is sure that the event has been closed.
--------------------------------------------------------------------------
# Incident Response Procedure
### How Does the Procedure Proceed?

In a SOC (Security Operation Center) environment, the action taken against an incident is important. Everyone should not use their own method they came up with, but methods that have had their frameworks previously determined should be used so there is consistency and everything proceeds accurately during a time of crisis. In this section, we will talk about how we can keep the base of consistency in response to incidents. This section is important to understand the big picture.

![](https://letsdefend.io/images/academy/pro.png)

##### Alert

After the logs collected through the EDR, IDS, IPS, WAF, and similar security tools that are found in the SOC, rule correlation sets are formed through the SIEM to determine suspicious activity. Thus, in the case of an unwanted situation, a new alert is created.

##### Analyze

In an ideal SOC environment, there are Tier 1 analysts present to conduct the preliminary analysis on alerts that come through the security tools. This analyst analyzes the incoming alert and determines whether it is a false positive or not. For example, an alert can be formed after sending a request to a malicious URL address; however, the URL address is not actually malicious. The Tier 1 analyst controls this procedure and eliminates incoming alerts.

##### Investigate

After it is determined that the incoming alert is not a false positive, the investigation procedure begins, and the source of the attack is investigated. In addition, the amount of progress the attacker has made since the beginning of the attack is investigated.

##### Assess Impact

The systems that have been affected by the attack are determined and the amount of damage present in the current situation is assessed and evaluated. For example, in a system that has been affected by ransomware may not have had all its data encrypted. Determinations similar to this have to be conducted to have an assessment of the current situation.

##### Contain

After determining the systems affected from the attack, it is crucial that the situation is handled with control and prevented from spreading. Thus, the affected devices must immediately be isolated from the network. Let’s continue with the ransomware example. A dangerous ransomware will want to spread itself to other devices. In order to prevent the interaction with the other devices, the device must be isolated from the network.

##### Respond

After all the mentioned steps above are completed, the response process is initiated. At this step, the root cause of the situation is determined, the present dangers are removed, the systems are brought back to a working state, and lessons are made from the situation that has occurred. The main topic of this training will be the details listed under this title. In future topics, we have showed you how to do this with details.
# 3 Important Things
When analyzing a system that has been hacked or believed to have been hacked, regardless of the processing system, there are 3 questions that must be answered. The responses to these questions may change or end the continuation of the analysis.  

  
  
  

![](https://letsdefend.io/images/academy/3important.png)

  
  
  
-   Is there a malware that is actively in the system?
  
-   Is there any suspicious internal or external communication?
  
-   Is there any persistence?

  
  

##### Is there a malware that is actively in the system?

If there is anything malicious that is actively running in the system, you may conduct a backward analysis to investigate how it came there in the first place. The easiest way to do this is conducting a process analysis. We will teach you the details of process analysis in the future. However, to give a short example: a “powershell.exe” childprocess under an “excel.exe” process is suspicious and must be investigated.  
  
  

##### Is there any suspicious internal or external communication?

An attacker must form an interaction with the server in order complete procedures like controlling the system or extracting data from it. This interaction will form network traffic. An anomaly determination can be conducted by analyzing the connections made in that system currently and in the past. For example, in the case of a connection being established with an IP with a bad reputation, or data traffic at rates of large GBs between a certain IP, or connections made between anormal ports can be cases that should be carefully investigated.  
  
  

##### Is there any persistence?

When the actions of the attacker until this day are observed, it can clearly be seen that the attacker aims to be permanently present in the system that has been taken over. The reason behind this can be the fact that the attacker may not have been able to complete a certain transaction quickly and may need to return to complete it later and the thought that he/she should leave an open door because he/she might need it in the future again.

During your analysis, you may not be able to determine an active malicious presence or suspicious traffic. Maybe the attacker has kept a backdoor that can trigger itself once a week. Thus, you must know the procedures used for permanence and you must examine these within the system.

Answering the 3 mentioned questions is important. The responses to these questions may change the continuation of the analysis. To answer these questions, there are certain places you must technically analyze. We will start talking about these in the upcoming chapter.

[Back](https://app.letsdefend.io/training/lesson_detail/incident-response-procedure)
# Free Tools That Can Be Used
# Checklist
#### Tools That Can Be Used

  
-   Process Hacker
  
-   Autoruns
  
-   FullEventLogView
  
-   LastActivityView
  
-   BrowsingHistoryView

  
  

#### Procedures That Must be Conducted for Memory Analysis

  
-   Process Tree
  
-   Web Connections
  
-   Signature Status

  
  

#### Users

  
-   Net user
  
-   Lusrmgr.msc
  
-   Event ID 4720 - A user account was created
  
-   Event ID 4732 - A member was added to a security-enabled local group

  
  

#### Scheduled Tasks

  
-   Autoruns, Event Viewer
  
-   Event ID 4698 - A scheduled task was created
  
-   Event ID 4702 - A scheduled task was updated
  
-   Applications and Services Logs-Microsoft-Windows-TaskScheduler Operational.evtx

  
  

#### Services

  
  

#### Registry Run Keys / Startup Folder

  
-   Event ID 4657: A registry value was modified
  
-   HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run
  
-   HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\RunOnce
  
-   HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\Run
  
-   HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\RunOnce
  
-   HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\UserShellFolders
  
-   HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\ShellFolders
  
-   HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\ShellFolders
  
-   HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\UserShellFolders
  
-   HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\RunServicesOnce
  
-   HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\RunServices
  
-   HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\RunServices
  
-   HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\RunServices
  
-   HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer\Run
  
-   HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer\Run

  
  

#### Files

  
-   AV scan
  
-   Manual Search
