**Package	Management**
The first thing that you need to know before you update your Kali Linux system is that the configuration file for the Kali repository is located at /etc/apt/sources.list :

To fully upgrade from one release to another, execute the full‐upgrade command along with the update command.
$apt update && apt full-upgrade -y

Now, to list all the installed software packages on Kali Linux, you'll have to use the dpkg command:
dpkg -l

What	about	installing	a	new	software	(package)	on	Kali?	There	are	two	common
ways	that	I	use	most	of	the	time.	The	first	one	is	the	apt	install	command,	and
the second one is dpkg (I use the latter only when I download a file that ends with .deb extension). $apt install [package name] -y $dpkg -i [filename.deb]

In some software packages, they will require you to use the configure / make installation way, if that's the case, then use the following commands (you must be inside the application directory):

$./configure && make && make install