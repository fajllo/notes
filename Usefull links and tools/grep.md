grep search command output for specific word

eg: **grep test**-> will display only output lines witch inclide word 'test'
 excluding words:
 
 *grep -v 'test'* -> will show all lines without test work

we can exclude multiple words with:
*grep -vE 'test|another|thirs'* -> this words will be excluded from the output


###### log noise filter
cat ausearchaudit.txt| grep 192.168.4.155 | grep -vE 'USER_AUTH|USER_LOGIN|CRED_ACQ|USER_ERR|USER_ACCT|USER_END|USER_START' | head

**leaves proctitle tty and execve** -> command and processes run on the machine 

