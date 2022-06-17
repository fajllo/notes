#Wireshark  #LinuxCLI #Volatility2

https://www.youtube.com/watch?v=IcH4N9-Qx6k

1. start with window memory image ->you can get the list of all processes that ware running on the machine 
	1. volatility -f WINADMIN.raw --profile=Win7SP1x86 pslist
	2. w procesach znajsujemy powershella -> który uruchamia kolejnego powershela
2. Sprawdzamy ID porcesus powerhella (3888) w logach z SYSMONA
	1. ten process powstał po pobraniu zainfekowanego pliku hta
	2. uruchamia w ukryty oknie zaszyfrowana komende powershell
	3. możemy ja odszyfrowac uzywajac base64 --decode  