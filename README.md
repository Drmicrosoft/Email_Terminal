# Email_Terminal


#OpenSSl
change this in next command to your mail server " smtp.office365.com " 

#OpenSSl>> s_client -starttls smtp -connect smtp.office365.com:587 -crlf -ign_eof

to start the server you send it : 

#HELO

then you open the TLS Server by : 

#startTLS

then you start login by using : 

#AUTH LOGIN

using this website :

https://www.base64encode.org/

Send first your Email after encoding it and send it with enter
and then your password after also encoding it and send it with enter

then start send your mail 
by those commands


#mail from:<omar.okasha@gizasystems.com> 
#rcpt to:<omar.prmail@gmail.com>
#rcpt to:<omar@okasha.com>

#data 
This is a test, please do not respond
. 
quit

rcpt to:<omar.okasha@gizasystems.com>





MAIL FROM:<omar.okasha@gizasystems.com>
S: 250 OK
RCPT TO:<omar.prmail@gmail.com>
RCPT TO:<omar.okasha@gizasystems.com>
S: 250 OK
C: RCPT TO:<peggy@mail.com>
S: 250 OK
 
DATA
The DATA command starts the transfer of the message contents (body text, attachments etc). After that the DATA command has been sent to the server from the client, the server will respond with a 354 reply code. After that, the message contents can be transferred to the server. When all message contents have been sent, a single dot (“.”) must be sent in a line by itself. If the message is accepted for delivery, the SMTP server will response with a 250 reply code. Example (the message contents is set to italic in the example below):
 
C: DATA
S: 354 Send message content; end with <CRLF>.<CRLF>
C: Date: Thu, 21 May 2008 05:33:29 -0700
C: From: Okashov <omar.okasha@gizasystems.com>
C: Subject: The Next Meeting
To: omar.prmail@gmail.com
To: omar.okasha@gizasystems.com

C:
C: Hi John,
C: The next meeting will be on Friday.
C: /Anna.
C: .
S: 250 OK
