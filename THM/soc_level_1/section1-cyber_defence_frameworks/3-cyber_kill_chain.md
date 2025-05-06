* The kill chain is a military concept related to the structure of an attack.
* Lockheed Martin established the Cyber Kill Chain framework for the cybersecurity.
* The framework defines the steps used by adversaries or malicious actors in cyberspace.
    - Reconnissance
    - Weaponization
    - Delivery
    - Exploitation
    - Installation
    - Command & Control
    - Actions on Objective

## Reconnaissance

* Reconnaissance is discovering and collecting information on the system and the victim. 
    - OSINT
    - Email harvesting

## Weaponization

* combines malware and exploit into a deliverable payload.

**Malware** - Malicious software designed to damage, disrupt and gain unauthorized access.

**Exploit** - Program or code that take advantage of vulnerability. its purpose is to deliver malware and other malicious activity.

**Payload** - is a malicious code that the attacker runs on the system.

## Delivery

* eg of delivery option
    - Phishing email
    - USB baiting
    - Watering hole attack

## Exploitation

* After gaining access to the system, the malicious actor could exploit software, system, or server-based vulnerabilities to escalate the privileges or move laterally through the network.

**Lateral movement** - techniques that a malicious actor uses after gaining initial access to the victim's machine to move deeper into a network to obtain sensitive data. 

* eg of how attacker carries out exploitation
    - Phishing (malicious link clicked)
    - zero-day exploit
    - An attacker triggers the exploit for server based vulnerability.

## Installation

* the backdoor lets an attacker bypass security measures and hide the access.

* Once the attacker gets access to the system, he would want to reaccess the system if he loses the connection to it or if he got detected and got the initial access removed, or if the system is later patched. He will no longer have access to it. That is when the attacker needs to install a persistent backdoor. A persistent backdoor will let the attacker access the system he compromised in the past.

* The persistence can be achieved through eg.
    * Installing a **web shell** on the webserver. (web shell is a malicious script written in web dev programming language like js php which can be difficult to detect)
    * Installing backdoor via **Metepreter**. (metepreter is metasploit framework payload) 
    * Adding entry to the **run keys**. (payload will execute each time the user logs in).

> Timestomping - The Timestomping technique lets an attacker modify the file's timestamps, including the modify, access, create and change times. 

## Command & Control

 C&C or C2 Beaconing as a type of malicious communication between a C&C server and malware on the infected host.

* most common C2 channels used by adversaries nowdays
    - http and https on port 80 and 443 for bypass the firewall.
    - DNS for **DNS tunneling**(where the victim makes regular DNS requests to a DNS server and domain which belong to an attacker. )

## Action on objective

With keyboard access. The attacker can achieve.
* Collect credentials
* perform privilege escalation
* Lateral movement
* Exfiltrate sensitive data
* Deleting and overwrite data

> shadow copy - is a microsoft technology that can create backup copies, snapshot of computer files.
