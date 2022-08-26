grep search command output for specific word

eg: **grep test**-> will display only output lines witch inclide word 'test'
 excluding words:
 
 *grep -v 'test'* -> will show all lines without test work

we can exclude multiple words with:
*grep -vE 'test|another|thirs'* -> this words will be excluded from the output

use *-A 10* to list addiotional 10 lines


###### log noise filter
cat ausearchaudit.txt| grep 192.168.4.155 | grep -vE 'USER_AUTH|USER_LOGIN|CRED_ACQ|USER_ERR|USER_ACCT|USER_END|USER_START' | head

**leaves proctitle tty and execve** -> command and processes run on the machine 

``` sh
cat access.log| grep /wp-login.php?itsec-hb-token=adminlogin | grep -o -E '[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}' | sort | uniq
```

windows open ssh 
``` sh
cat sshlog.log | grep  192.168.1.17 | grep password | grep Accepted


```
