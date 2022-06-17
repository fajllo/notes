[[pytania moje]]
1. wprowanie od kuby 
2. przywitanie - dzien dobry jestem ktośt  i co bede pokazywac 
3.  czym jest nesus i różnice między tenablem 
4. Host discovery -> zeby był dobry scna musimy wiedzieć jakie mamy hosty w siecie 
	1. postwaiuć wiecej VM i pokazac co odkrył
	2.  A simple scan to discover live hosts and open ports

6. po wykonaniu skanu mamy odkryte hosty w dzisiejszej prezentacji skupimy się na jedenym konkretnym hoscie który dokładniej omówimy 
7. Pokazac basic netwok scan i omówic poszczególne opcje 
	1.  general - omówić każde pole 
	2. schedule
	3.  notyfication -> czas skanowania może być długi wiec można ustwić powiadomie o zakończonym skanie 
		1. result filter -> Filter or search the notifications to narrow results in the notifications table.
	2. Discovery 
		1. scan type - omówić opcje portów 
			1. common port -> najpopularniejsz porty 
			2. all ports -> skanowanie wszystiego (653 2....) około 65k
			3. custom
				1.  ping remote host -> jeżeli ta opcja jest włczona ale np firewall blokuje pakiety ICMP nessus może nie wykryć hosta pomimo jego obecności w sieci
				2. fragile devices
				3. wake-on LAN - przy właczonej opcji Wake on lan nessus może wybodzić uśpionego host z dostępnej mu listy mac addresów
			4. Port scanning 
				1. Ports - można ustawić które porty ma skanować domyślnie przeskanuje common porty
				2. locla port enumeration 
					1.  Nessus was able to run 'netstat' on the remote host to enumerate the open ports. -> mozna zrobić enumeracje lokalnych portow filtrujc po danych protokołach
				2. network port scaner 
					1.  przejrzeć pokój na tryhack me nmap i coś tu dopisać 
			5. Service discovery - > Attempts to map each open port with the service that is running on that port. Note that in some rare cases, this might disrupt some services and cause unforeseen side effects
			6. Assesment -> nessus może być zastosowany nie tylko do skanu sieci ale również do skanowania aplikacji webowych, w zakładce assesmen możemy dostosować preferncje sknowania, pokaza web app scan i ze to tam jest już zdefinowane 
				1. General-> to olac 
				2. Brutr force-> pozwala na atak słownikowy przy użyci Hydry, możemy użyć własnego  słownika 
				3. web app -> pominać 
				4. windows -> jest kilka metod enumeracji 
					1. omówic jedna metode 
					2. ![[Pasted image 20220518103314.png]]
			5. Database -> When enabled, if at least one host credential and one Oracle database credential are configured, the scanner authenticates to scan targets using the host credentials, and then attempts to detect Oracle System IDs (SIDs) locally. The scanner then attempts to authenticate using the specified Oracle database credentials and the detected SIDs. **opcjonalnie** 
			6. Reportnig-> nessus ma wbudowaną możliwośc raportownaia i tutaj możemy sobie ustawić co chcemy wyświetlić na raporcie 
			7. Advance-> mamy domyślne 2 typy skanów
				1. low bandwith -> aby nie przeciążać siec które skanujemy możemy wybrac tą opcje , porównac performance options 				2. 
	2. Plugins ->
		1. As information about new vulnerabilities is discovered and released into the general public domain, Tenable Research designs programs to detect them. These programs are named plugins and are written in the Nessus Attack Scripting Language (NASL). The plugins contain vulnerability information, a simplified set of remediation actions and the algorithm to test for the presence of the security issue. Tenable Research has published 171415 plugins, covering 69234 CVE IDs and 30940 Bugtraq IDs.**trzeba to skrócić**
		
		3. Kolejny basic network z credentialimy
			1. omówić SSH
				1. jakie metody uwierzytelniania możemy wybrać 
				2. zrobić setup tego scanu 
				3. omówić różnice miedzy scanem z credentialmi i bez 
		4. team z tenabla i nessusa tworzy templtki skanów adrusiujące aktualne zagrożenia np log4shell
	5. omówić różce miedzy agentem a nessusem 

			
 