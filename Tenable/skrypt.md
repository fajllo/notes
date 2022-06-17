[[prezentacja skrypt]]

1. Wprowadzenie od kuby...
2. Hello and welcome in the port of the presentation dedicated to Nessus
3. What is nessus and how Tenable.io utilize it:
	1. On the begining I would like explain the difrence between #Nessus and #Tenable.io. Nessus is a proprietary vulnerability scanner developed by Tenable. It it often used during vulnerability assessments and penetration testing engagements. Nessus can detect software flaws, missing patches, malware and misconfiguration errors across a wide range of operating systems.
	2. On the other hand Tenable.io is fully featured vulnerability management platform that  provide network and web vulnerability assessments using Nessus technology
5. You can perform two types of scans using Nessus : _discovery scans_ and _assessment scans_. Tenable recommends performing discovery scans to get an accurate picture of the assets on the  network and assessment scans to understand the vulnerabilities on your assets.
6. To create new host discovery scan we need to clicnk "new scan" and them select host discovery. Host discovery is a simple scan to discover live hosts and open ports.
	1. *pokazać jak się ustawia taki skan *
		2. to configure host discorery scan we have to fill all the required field
	
		4. **General:** *tutaj każde pole jest jasne* ->  in this case the required field are #Name of our scan and list of #Target hosts
			1. You can specify the targets of a scan using a number of different formats, inculding:
				1. An single IPv4 or IPv6 address
				2.  IPv4 range with a start and end address
				3. An IPv4 subnet with CIDR or netmask notation
				4. Or FQDN name
				
		6. **Schedule:** if we enable this option we can select frequency and tiem when our scan will be lanched. 
		7. **Notyfiaction:** When we scan large enterprise network scanning can take even couple of hours to complete, here we can fill **Email Recipipent** filed and we will automaticaly get email notification after  scan is done. 
		8. To adjust our discovery methods we can use #Discovery section:
			1. #Discovery here we can pick type of scan we would like to setp up. We have 5 options to choose from: #host_enumeration, #OS_identyfication,  #common_port_scan, #all_ports_scan and #custom
				1.  #custom let us select all setting mannaully.
			1. **Host discover** 
				1. Here we can enable or disable **Pinging the remote host** using #ICMP / #TCP / #UDP / #ARP protocol. If this metthot is ON and for example firewall has the rule that will block all ICMP packets Nassus may not scan targeted hosts, it will assume it's down or not reachable.
				2.  Another interestion setting is **wake-on LAN** option. If targeted host is in sleep mode Nessus can  "wake up" that  host and permorm scanning.
			2. **Port scanning**
				1. In this section we can configure custome **port scan range** 
				2. And select what type of scaner we wont to use: #TCP, #SYN and #UDP 
					1. We can use #TCP  and #SYN  scanners to identify open TCP port. Main diference between them is that #TCP trys to find open ports using full TCP three way handshake and #SYN scanner sensd **SYN** packet to the port and wiats for **SYN-ACK** reply and determines the port state based on a response or lack of response
					2. We can #UDP is used to identyfy open #UDP ports
	2. *pokazać wyniki i wybrac hosta na którym będziemy się skupiać *
	3. I already have my network scaned so let's see how the results looks like -> 
		1. Nassus discoverd six live hosts in my network and succesfully detected OS and open ports information about three of them. 
	4. **during this presentation we will focue on ubuntu versio 12 (192.168.113.131 )host**
   
4. After Host discovery scan is done and we have selected our tareget host we can move on to assesment scan. 
	1. We have many predifined options to choose from but for the purpose of this presentation lest focus on #Basic_Network_Scan 
	2. We won't go throuhg #Basic and #Discovery section again as they are the same as in host discovery scan template with one small diffrence. 
	3. In #Discovery section there is one additionall setting called **Service Discovery**
		1.  **Service Discovery** section includes settings that attempt to map each open port with the service that is running on that port.
		
	4. Nessus can be used not only to scan #network but also it is capable to perform web application scanning, in the **Assessment** section we can configure how a scan identifies vulnerabilities. By default Nessus won't scan for web #vulnerabilities, to enable that we have to eiter scelect predifined web application scan setting or enable it here.
		1. If you select the **Custom** preconfigured setting option, or if you are using a scanner template that does not include preconfigured assessment settings, you can manually configure **Assessment** settings.
			1. In the **General** category there is an options to **adjust scanner accurray**, if we wish to gather as much information as possible about scaned host we can turn on "show potential false alarm" option. Nassus in scan result will display more information but some of them will be generated based on guesswork
				1. Enabling **Perform (trow ) thorough tests** can provide better scan results but can inpact scan speed and disturb network. 
			2. Nessus is capable to perfomr **Brute Force** attack againt remote host, it means that Nessus can test default account and known default password to gain access to the device we are scanning. It can be very usefull during penetration test assesment but I recoment to leave this option turned off while performing  #vulnerability #management #assesments because it may cause account lock.
			3. I will not go into details about #Webapplication, #window and #databeses sections.
				1. Important thinks to know is that Nessus i capable of performing #Webapplication scanning and crawling, advance user enumeration on windows based host and detection of Oracle System IDs
	5. Moving on to the Reporting. I think that this section is self explainatory. Here we can select  what we want to display in the report after scan is completed. 
	6. I mentioned before that we can set up Nessus to **Perform (trow) thorough tests** that can disturb network. We can also select scan type to **scan low bandwitch links**. this option is very usefull when we are worknig with frigele network and we don't want cause ane distrptions. If we  set scan type to custome we can manually configure **Advanced** settings in the following categories:  General Settings. Performance options and Debuge settings.The **Advanced** settings provide increased control over scan efficiency and the operations of a scan, as well as the ability to enable plugin debugging.
	8. Ok, and thats complet the Setting tab but 
		1. before we switch to #Credentials tab you need to know that Asessment scan can by diviede on credential and non credential scan.
		2. 3. Both credentials and non credential scans has it owns #benefits and #limitation:
	9. [[traditional no creds]] for exaample non  credential scans are perfect for large-scale assessments in traditional enterprise environments, Discovers vulnerabilities that an outside attacker can use to compromise your network (provides a malicious adversary's point of view). One of the limitation ot this scan is that it misses client-side vulnerabilities such as detailed patch information. another limitation is that it can sometimes have a negative effect on the network, device, or application you are testing.
	10. [[traditional with creds]] Credential scan can  Provides more accurate results—a complete enumeration of software and patches installed on the host and Consumes  less resources than non-credentialed scanning because the scan executes on hosts themselves rather than across the network. Biggest limitation of credential scans is credential management. 
	11.  In #Tenable.io we have third option to perform scanning. To conduct our #vulnerability #management  assesment we can utilze **Nessus Agent**
		1. Nessus Agent scans use lightweight, low-footprint programs that you install locally on hosts. Nessus Agents collect vulnerability, compliance, and system data, and report that information back to Tenable.io
1. If we wish to set up credentia scan here we need to select authentication methode and specyfi credential nessus will use to log in to the remote host. 
	1. For windows machinse we have 4 methods to choose from: Kerberos, LM Hash, NTLM HASH and password.
	2.  For Unix based host we also have 4 option to authenticate but slightly diferent then on windows. We can choos among autehenticating use certfication, publi key, Kerberos or password.
	3. For purpose of this presentation I will select password authentication. Additionally we have to fill required fields and now we can save our scan as a template and lanch it.
2. In order not to waste time waiting for the results of the scans, I allowed myself to run the scans earlier and now I we can compare results. let's take a look at the credential scan first.
	1. on the first page wa get the overviwe of all hosts we have scaned. In this example we launch the scan againt only one host. Next to the host IP we can see graph with all #vulnerabilities categorized by severity. Serverity is assigned base on Common Vulnerability Scoring System. As you can see nessus found 17 critical and 89 high severity #vulnerabilities  
	2. If we switch to the #vulnerabilities tab we can see that Nessus categorizes #vulnerabilities by Family.
	3. We can click on each  #vulnerability to find out more information
		1. All #vulnerabilities have description how nessus was able to find it and proposed solution how to remediate it. 
		2. on the right we can see  information about #vulnerability  risk factor, cvss score or even if there is exploit available.
		3. on the very bottom of the page we can find reference information with the links that can help us in further investigation.
		4. after we investigate #vulnerability  we can assign our own score to it
		5. In the result tab we can find  agregated information how to remediate each #vulnerability 
		6. 
		




		
	   




	
		   
		