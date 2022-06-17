**Agent Scans**

Nessus Agent scans use lightweight, low-footprint programs that you install locally on hosts. Nessus Agents collect vulnerability, compliance, and system data, and report that information back to Nessus Manager or Tenable.io for analysis. Nessus Agents are designed to have minimal impact on the system and the network, giving you the benefit of direct access to all hosts without disrupting your end users.
**Benefits:**
	- Provides extended scan coverage and continuous security
		- Can deploy where it’s not practical or possible to run network-based scans
		- Can assess off-network assets and endpoints that intermittently connect to the internet (such as laptops). Nessus Agents can scan the devices regardless of network location and report results back to the manager.
	- Eliminates the need for credential management
		- Doesn't require host credentials to run, so you don't need to manually update credentials in scan configurations when credentials change, or share credentials among administrators, scanning teams, or organizations
		- Can deploy where remote credentialed access is undesirable, such as Domain Controllers, DMZs, or Certificate Authority (CA) networks
	-  Efficient:
	    -   Can reduce your overall network scanning overhead.
	    -   Relies on local host resources, where performance overhead is minimal.
	    -   Reduces network bandwidth need, which is important for remote facilities connected by slow networks.
	    -   Removes the challenge of scanning systems over segmented or complex networks.
	    -   Minimizes maintenance, because Nessus Agents can update automatically without a reboot or end-user interaction.
	    -   Large-scale concurrent agent scans can run with little network impact.
	-Easy deployment and installation
		-  You can install and operate Nessus Agents on all major operating systems.
		-   You can install Nessus Agents anywhere, including transient endpoints like laptops.
			-   You can deploy Nessus Agents using software management systems such as Microsoft’s System Center Configuration Manager (SCCM).
**Limitations:**
	-   Network checks—Agents are not designed to perform network checks, so certain plugins items cannot be checked or obtained if you deploy only agent scans. Combining traditional scans with agent-based scanning eliminates this gap.
	-  Remote connectivity—Agents miss things that can only be performed through remote connectivity, such as logging into a DB server, trying default credentials (brute force), traffic-related enumeration, etc.