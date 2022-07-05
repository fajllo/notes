**Filters and Coloring**
#DNS

**DNS analyzing**
DNS is UDP trafic -> if we want to check how many diffrent convesations we hahe go to statistics-> conversation-> UDP -> and count port 53 requests

Check how much DNS response we have dns.flags.response ==1 -> if we do dns.flags.response  == 0 we will check for dns queries

Check for external DNS Queries dns.flags.response == 0 and !(ip.dst ==10.0.0.0/24)

#TCP 
**TCP Analyz**
TCP Syn scan (tcp.flags.syn == 1) && (tcp.flags.ack == 0) also you can use tcp.flags.reset == 1 
TCP Xmas scan tcp.flags.urg == 0) && (tcp.flags.push == 0)) && (tcp.flags.fin == 0)

#SSH 
tcp.port ==22 this is ssh trafic you can add  ! ip.src == 10.0.1.0/24(our trusted subnet ) you can identify this trafic as suspected 


#exe
search for exe files 
http.request.uri matches "/*.exe"* when we use matches we can use regex exp
another way tcp/ http contains DOS
MZ -begininig of the file header for binary file or executable 

#non-standard-ports

