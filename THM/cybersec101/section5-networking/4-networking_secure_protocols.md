## TLS
TLS is a cryptographic protocol operating at the OSI model’s transport layer. It allows secure communication between a client and a server over an insecure network.

### Working
Generally, the server administrator creates a Certificate Signing Request (CSR) and submits it to a Certificate Authority (CA); the CA verifies the CSR and issues a digital certificate. Once the (signed) certificate is received, it can be used to identify the server (or the client) to others, who can confirm the validity of the signature. For a host to confirm the validity of a signed certificate, the certificates of the signing authorities need to be installed on the host.

> A self-signed certificate cannot prove the server’s authenticity as no third party has confirmed it.

## HTTPS
It is basically HTTP over TLS. Consequently, requesting a page over HTTPS will require the following three steps (after resolving the domain name):
1. Establish a TCP three way handshake with the target server.
2. Establish a TLS session.
3. Communicate using HTTP protocol. eg `GET / HTTP/1.1`.

> step 1 and 2 are where the **TLS negotiation and establishment** take place.

## SMTPS, POP3S, and IMAPS
Using these protocols over TLS is no different than using HTTP over TLS; therefore, almost all the points from the HTTPS discussion apply to these protocols.

| Protocol | Default Port |
| -------- | ------------ |
| HTTP     | 80           |
| HTTPS    | 443          |
| SMTP     | 25           |
| SMTPS    | 465 and 587  |
| POP3     | 110          |
| POP3S    | 995          |
| IMAP     | 143          |
| IMAPS    | 993          |

## SSH
SSH is used for secure remote access. OpenBSD developers released OpenSSH, an open-source implementation of SSH. Nowadays, when you use an SSH client, it is most likely based on OpenSSH libraries and source code. SSH server listen on port 22.

OpenSSH offers several benefits like:
* Secure Authentication: besides password based authentication, SSH supports public key and 2FA.
* Confidentiality: provides end-to-end encryption. 
* Integrity: 
* Tunneling: SSH can create a secure "tunnel" to route other protocols through SSH.
* X11 Forwarding: If you connect to a unix like system with GUI. SSH allows you to run graphical application on a remote server.

## SFTP and FTPS
SFTP stands for SSH File Transfer Protocol and allows secure file transfer. It is part of the SSH protocol suite and shares the same port number, 22. If enabled in the OpenSSH server configuration, you can connect using a command such as `sftp username@hostname`. Once logged in, you can issue commands such as `get filename` and `put filename` to download and upload files.

FTPS stands for File Transfer Protocol Secure. it is secured using TLS, just like https. FTP uses port 21, FTPS usually uses port 990.

Setting up an SFTP server is as easy as enabling an option within the OpenSSH server.

## VPN

A VPN connection is usually the perfect option for connecting two company branches.

A VPN (Virtual Private Network) creates a secure, encrypted connection between your device and the internet, masking your IP address and encrypting your data to enhance privacy and security.
