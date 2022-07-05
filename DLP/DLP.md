Malicious Data loss
1. Hacking 
2. Malware
3. credential Theft

Accidental
1. Miscofiguration
2. Data Copying 
3. Phisical Loss

Threat Modeling 
![[Pasted image 20220628102201.png]]

Azure compliance tools 
Security center
Compliance Manager 
Policies


Azure Data Privacy 

Azure information protection -> 
## Klasyfikowanie danych na podstawie ich poufności

Konfiguruj zasady do klasyfikowania, etykietowania i ochrony danych na podstawie ich poufności. Klasyfikacja za pomocą usługi Azure Information Protection jest w pełni automatyczna, sterowana przez użytkowników lub oparta na zaleceniach.

## Ochrona danych przez cały czas

Dodaj do danych klasyfikację i ochronę informacji w celu zapewnienia im podróżującej wraz z nimi trwałej ochrony. Dzięki temu będą one chronione niezależnie od tego, gdzie są przechowywane ani komu zostały udostępnione

## Dodaj widoczność i kontrolę

Śledź działania dotyczące udostępnionych danych i w razie potrzeby odwołuj dostęp. Zespół informatyczny może monitorować oraz analizować dane i podejmować dotyczące ich decyzje, korzystając z zaawansowanych narzędzi do rejestrowania i raportowania.

## Bezpieczniejsza współpraca z innymi

Bezpiecznie udostępniaj dane współpracownikom, klientom i partnerom. Definiuj to, kto może uzyskać dostęp do danych i co może z nimi zrobić — na przykład zezwalając na wyświetlanie i edytowanie plików, ale nie na ich drukowanie ani przesyłanie dalej.

## Azure secures your data at rest and in transit

With state-of-the-art encryption, Azure protects your data both at rest and in transit. Azure secures your data using various encryption methods, protocols, and algorithms, including [double encryption](https://docs.microsoft.com/en-gb/azure/security/fundamentals/double-encryption).

## Lifecycle of data
1)** Identify/Classify/Tag **
2) a. In this phase, we identify the data that needs to be protected. There are two types of data in an organization. Structured and unstructured. 
3) b. Data that resides in a database can be classified as structured. Data that resides on the servers and user systems can be classified as unstructured. We identify the unstructured data
4)  c. Then we classify the data. Simple classification could be Public data which is non-personal and non-confidential. Likewise we could have confidential data. 
5) d. Then we need to tag the data 
6) 
7) 2) **Share and Protect**
8)  a. Once the data is classified and tagged, we encrypt the data. We could either use cloud key or we could use our own keys 
9) b. Then we grant or revoke access to the data. We could grant viewing/ editing permissions to different groups as needed 
10) 
11) 3) **Usage tracking **
12) a. With RMS (azure right management ), we could track the usage of data
13)  b. We can see who accessed the data from which location and when 
14) c. We can grant or deny access 
15) 
16) 4) Revoke access
17)  a. Once we revoke the access to the data, the users who had access before cannot access the same data going forward.

![[Pasted image 20220628131957.png]]