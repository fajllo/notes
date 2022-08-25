### Process Management
The process is the functioning units of the commands/programs running on the operating system. While performing a live Linux host review, mainly processes are examined. Examination and analysis of memory essentially mean the analysis of processes. In Linux, each process has its own identification number. This identification number is called "Process ID" (PID). This identification number is used in the operations of the processes.

use *ps* to list running processes 



htop 
![[Pasted image 20220715101207.png]]

Another way to get the list of currently running processes is by using the ps command: $ps -Au -A: To select all the processes (if you want to list only the processes that belongs to the current user then use the -x option instead) -u: shows more info (e.g., CPU, MEM, etc) than the default output To kill a process, you will need to identify its PID first; then you can use the kill command to get the job done: $kill [PID] If the system doesn't allow you to kill it, then you must force it to close using the ‐9 switch: $kill -9 [PID]