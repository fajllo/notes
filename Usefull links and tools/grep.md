grep search command output for specific word

eg: **grep test**-> will display only output lines witch inclide word 'test'
 excluding words:
 
 *grep -v 'test'* -> will show all lines without test work

we can exclude multiple words with:
*grep -vE 'test|another|thirs'* -> this words will be excluded from the output
