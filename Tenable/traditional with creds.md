**Traditional Active Scans (Credentialed)**
A traditional active credentialed scan provides a deeper insight than a non-credentialed scan. The scan uses credentials to log into systems and applications and can provide a definitive list of required patches and misconfigurations 
**credentialed scan looks directly at the installed software, including at the version numbers, it can assess items such as:**
	- Identifying vulnerabilities in the software
	- Evaluating password policies.
	- Enumerating USB devices
	- Checking anti-virus software configurations

**Benefits:**
	- Consumes far fewer resources than non-credentialed scanning because the scan executes on hosts themselves rather than across the network.
	-  does not have a negative effect on the network, device, or application you are testing
	- Provides more accurate results—a complete enumeration of software and patches installed on the host.
	- Uncovers client-side software vulnerabilities
**Limitations:**
	- Requires credentials management for each scanned host
		- Large organizations can potentially struggle with creating service accounts with the proper rights and access needed to safely conduct a credentialed scan
		- Password rotation requirements can add to management complexity
	- Misses transient devices that are not always connected to the network