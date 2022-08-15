1. Chceck event logs if there is anythig suspicious
2. Chceck for new useres and groups
3. Check members of Administrators group
4. Check scheduled tasks
5. Check Strut Up item
6. Check network information 
7. Check arp -a and netstat -ano
8. check host file c:Windows\System32\Drivers\etc\hosts
9. View running servieces
10. Verify File Signatures -> sigverif
11. Identify Recently Added Files ->**dir /a/o-d/p %SystemRoot%\System32\**
12. Perform Static Analysis on File -> in this case with Strings tool
13. Check Virus Total

MiTeC Windows Registry Recovery is one of many tools that can be used by computer forensic examiners to view registry values. The MiTeC Windows Registry Recovery uses a button system to allow you to view some of the most important registry key values.

The SYSTEM, SECURITY, SAM, and SOFTWARE are the registry files that contain many of these key system configuration values. These registry files are located in the Windows\System32\config directory and provide a wealth of information about the configuration of a Windows system. Some of the values we examined in this final section include the following:

-   Installation Date
-   TCP/IP Settings
-   User accounts
-   User SIDs
-   Services
-   Startup items

#Registry - > A database within the Windows operating system that records settings related on the machine’s users, installed programs, and other system settings.

#WRR -> Windows Registry Recovery, automatically parses some of the most pertinent information from the Windows registry files.

#SAM -> The Security Accounts Manager file of Windows.

#SYSTEM -> A Windows file that has information about computer profile settings, including services.

#Autopsy -> A free program that can be used to analyze forensic images.

There are many places to look for evidence of an intrusion on a Windows system, including the following:

-   Log files
-   Event viewer files
-   Registry files
-   Startup folder
-   Folders in the path, C:\Windows, C:\Windows\System32
-   Scheduled Tasks folder