![[Pasted image 20220805122332.png]]
#FTKimager #Redline 

#### The Digital Forensic Process
![[Pasted image 20220809122323.png]]
Digital evidence includes some of the following:
-   E-mails
-   User accounts
-   Digital videos, audio, and photos
-   Instant messages (IM)
-   Web browsing history
-   Files
-   An image of RAM
-   Registry
-   Backups
-   Logs
-   Video recordings

### Process breake down
#collection
Identify, label, record, and acquire the data from relevant sources to be used by investigators. Care must be taken to preserve the integrity of the evidence for chain-of-custody reasons. The data custodian must document every step to preserve chain-of-custody.

#examination
Use forensically sound ways to collect data to help support the investigation. Again, preserving the integrity of evidence is critical here.

#analysis
Analysis is the result of the investigation using legally justifiable methods and techniques. The computer forensic examiner documents every step to preserve chain of custody.

#reporting
Reporting is the documentation of the examination and analysis of the investigation which includes explanation of the use of tools, description of the analysis of the different data sources, issues and vulnerabilities identified, and recommendations. The examiner will document every step to preserve chain of custody.


Imaging the system:
eather we can use gui tool ftkimager or install dd on windows (is unix native tool)
'dd if=\\.\e: of="h:\image.dd" --progress bs=1024'



<div class="rich-link-card-container"><a class="rich-link-card" href="https://superuser.com/questions/355310/dd-rescue-vs-dcfldd-vs-dd" target="_blank">
	<div class="rich-link-image-container">
		<div class="rich-link-image" style="background-image: url('https://cdn.sstatic.net/Sites/superuser/Img/apple-touch-icon@2.png?v=e869e4459439')">
	</div>
	</div>
	<div class="rich-link-card-text">
		<h1 class="rich-link-card-title">dd_rescue vs dcfldd vs dd</h1>
		<p class="rich-link-card-description">
		What are the main differences between dd_rescue, dcfldd, and dd? In what situations would you use one over the other? Why are there three different yet simliar programs?
		</p>
		<p class="rich-link-href">
		https://superuser.com/questions/355310/dd-rescue-vs-dcfldd-vs-dd
		</p>
	</div>
</a></div>

![[Pasted image 20220809132525.png]]
