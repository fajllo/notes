useradd -m [user name] -G [group name] -s [shell type]

passwd Gus

su [user name – that you want to switch to]


To learn the capabilities of the current user with the sudo command, you need to execute sudo ‐l to get the correct information:
sudo -l

To view the current user information, use the id command:
id

To list the currently logged on users, use w or who
w or who

userdel [user name – that you want to delete]

To list the last logged in users in the Kali system, use the last command:


roupadd [new group name]

To join a user (which is Gus for this example) to the hackers group that we created earlier, execute the usermod command:
- [ ] usermod -aG [group name]  [user name]

![[Pasted image 20220714144859.png]]


**Manipulating Files in Kali**
touch [new file]
file [file name]
cp [source file path]  [destination file path]
mv [source file path]  [destination file path]


**Searching for Files**
There are multiple ways to search for files in Kali; the three common ones are the locate , find , and which commands.

First, you will need to update the database for the locate command using the updatedb command: updatedb

locate	[file	name]

To find an application path, use the which command.
which [application name]
find 
![[Pasted image 20220714145547.png]]


