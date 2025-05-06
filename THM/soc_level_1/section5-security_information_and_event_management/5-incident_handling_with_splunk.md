## Incident Handling - Life Cycle

### 1. Preparation
The preparation phase covers the readiness of an organization against an attack. That means documenting the requirements, defining the policies, incorporating the security controls to monitor like EDR / SIEM / IDS / IPS, etc. It also includes hiring/training the staff.

### 2. Detection and Analysis
This phase covers getting alerts from the security controls like SIEM/EDR investigating the alert to find the root cause. This phase also covers hunting for the unknown threat within the organization.

### 3. Containment, Eradication, and Recovery
This phase covers the actions needed to prevent the incident from spreading and securing the network. ie. isolating the infected host, clearing the network from the infection tracesm and gaining control back from the attack.

### 4. Post-Incident Activity / Lessons Learnt
The steps involve identifying weaknesses that led to the attack, adding detection rules so that similar breach does not happen again, and most importantly, training the staff if required.

## Reconnaissance Phase

Search query: `index=botsv1 imreallynotbatman.com`
explanation: look for the event log in the index "botsv1" which contains the term "imreallynotbatman.com".

## Exploitation Phase
count
* To see the number of counts by each source IP against the webserver.
* search query: `index=botsv1 imreallynotbatman.com sourcetype=stream* | stats count(src_ip) as Requests by src_ip | sort - Requests`
* query explanation: This query uses the stats function to display the count of the IP addresses in the field src_ip.

we can also create different visualization to show the result.

* we can use in query ` | table _time uri src_ip dest_ip form_data` for create a table containing the important fields.

`rex` - specifies a perl regular expression named groups to extract fields while you search eg `...| rex field=_raw "Form:(?<form>.*) to: (?<to>.*)"`

* To extract the **passwd** values we can use ` | rex field=form_data "passwd=(?<creds>\w+)"  | table src_ip creds` 

## Installation Phase

`index=botsv1 sourcetype=stream:http dest_ip="192.168.250.70" *.exe`
* find out who execute the executable file

## Action on Objectives
As the website was defaced due to a successful attack by the adversary, it would be helpful to understand better what ended up on the website that caused defacement.

* find the interesting files, traffic, attack, which rule is triggered in firewall etc.

## Command and Control Phase

identified the suspicious domain as a Command and Control Server, which the attacker contacted after gaining control of the server.

## Weaponization Phase

In the weaponization phase, the adversaries would:
    * Create malware / malicious document to gain initial access / evade detection etc.
    * Establish domains similar to the target domain to trick users.
    * Create a command and control server for post-exploitation communication/activity etc.

### Robtex:
Robtex is a Threat Intel site that provides information about IP addresses, domain names etc.

### Virustotal

### otx.alienvault.com

## Delivery Phase

use the information we have about the adversary and use various Threat Hunting platforms and OSINT sites to find any malware linked with the adversary.

### OSINT Sites
* virustotal 
* ThreatMiner
* Hybrid-Analysis


> LOLBAS - Living Off The Land Binaries, Script and Libraries


