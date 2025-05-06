## DNS
 responsible for properly mapping a domain name to an IP address. There are many types of DNS records. The main four are:

* **A record** - The A(Address) record maps a hostname to one or more IPv4 addresses.
* **AAAA record** - similar to A record but it is for IPv6.
* **CNAME record** - The CNAME(Canonical Name) records maps a domain name to another domain name. for example `www.example.com` can be mapped to `example.com` or can be `example.org`.
* **MX record** - The MX(Mail Exchanger) record specifies the mail server responsible for handling emails for a domain.

## WHOIS
WHOIS record provides information about the entity that registered a domain name, including name, phone number, email, and address.

## HTTP / HTTPS
This protocol relies on TCP. It use port 80 and 443 and defines how your web browser communicates with the web servers. common methods are GET, POST, PUT, DELETE.

## FTP: Transfering files
File Transfer Protocol (FTP) is designed to transfer files.

example commads defined by the FTP protocol are:
    * `USER` is used to input the username.
    * `PASS` is used to enter the password.
    * `RETR` is used ot retrieve or download the file from the FTP server to the client.
    * `STOR` is used to upload a file from the client to the FTP server.

## SMTP: Sending Email
Simple Mail Transfer Protocol (SMTP) defines how a mail client talks with a mail server and how a mail server talks with another. The SMTP server listen on port 25.

ome of the commands used by your mail client when it transfers an email to an SMTP server:
* `HELO` OR `EHLO`initiates an SMTP session.
* `MAIL FROM` specifies the sender's email address.
* `RCPT TO` specifies the recipient's email address.
* `DATA` indicates that the client will begin sending the content to the email message.
* `.` is sent on a line by itself to indicate the end of the email message.

> There is a lab on this page for understanding the smtp commands using telnet.

## POP3: Receiving Email
You’ve received an email and want to download it to your local mail client. The Post Office Protocol version 3 (POP3) is designed to allow the client to communicate with a mail server and retrieve email messages. POP3 server listens on TCP port 110 by default.

An email client sends its messages by relying on SMTP and retrieves them using POP3.

Some common POP3 commands are:
* `USER <username>` identifies the user.
* `PASS <password>` provides the user's password.
* `STAT` request the number of messages and total size.
* `LIST` lists all messages and their sizes.
* `RETR <message_number>` retrieves the specified message.
* `DELE <message_number>` marks a message for deletion.
* `QUIT` ends the POP3 session applying changes, such as deletions.

## IMAP: Synchronizing Email

IMAP (Internet Message Access Protocol) is used for maintaining a synchronized mailbox across multiple devices. It allows sycchronizing read, moved, and deleted messages. IMAP server listens on TCP port 143 by default.

The IMAP protocol commands.
* `LOGIN <username> <password>` autheticate.
* `SELECT <mailbox> selects the mailbox folder to work with.
* `FETCH <mail_number> <data_item_name> Example `fetch 3 body[]` to fetch message number 3, header and body.
* `MOVE <sequence_set> <mailbox>` moves the specified message to another mailbox.
* `COPY <sequence_set> <mailbox>` copies the specified message to another mailbox.
* `LOGOUT` logs out.
* In IMAP commands we use tags in starting `A`, `B` etc for identify which command the server is responding.


