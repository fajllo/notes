This phase is when an initial payload is delivered as a result of the exploitation of the weaponized object that was delivered to the target. Installation generally has multiple sub-phases, such as loading multiple tools/droppers onto the target that will assist in maintaining a good foothold onto the system, to avoid the adversary losing a valuable piece of malware (or other malicious logic) to a lucky anti-virus detection.

As an example, the exploit may be to get a user to open a document that loads a remote template that includes a macro. When the document is opened, the remote template is loaded and brings the macro with it over TLS. Using this example, the email with the attachment looked like normal correspondence and the adversary didn't have to risk losing a valuable macro-enabled document to an email or anti-virus scanner: 
![[Pasted image 20220617112014.png]]



In the preceding snippet, we can see a normal Microsoft Word document template. Specifically take note of the Target="file:///" section, which defines the local template (GoodTemplate.dotm). In the following snippet, an adversary, using the same Target= syntax, is loading a remote template that includes malicious macros. This process of loading remote templates is allowed within the document standards, which makes it a prime candidate for abuse:
![[Pasted image 20220617112037.png]]

This can go on for several phases, each iteration being more and more difficult to track, using encryption and obfuscation to hide the actual payload that will finally give the adversary sufficient cover and access to proceed without concern for detection.

As a real-world example, during an incident, I observed an adversary use an encoded PowerShell script to download another encoded PowerShell script from the internet, decode it, and that script then downloaded another encoded PowerShell script, and so on, to eventually download five encoded PowerShell scripts, at which point the adversary believed they weren't being tracked (spoiler: they were).