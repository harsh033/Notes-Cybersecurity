* IOC(indicator of compromise) - are observable evidence that suggest sign of a potential security incident.

* **Pyramid of Pain** captures the relationship beween IOC and the level of difficulaty that malicious actor experience when IOC are blocked by security teams.

## Hash Values (Trivial)

most common hashing algoritms.
* MD5 (message digest)
    - create 128-bit hash values.
    - not considered as cryptographically secure. (hash collision and other attacks possible).

* SHA-1 (Secure Hash Algorithm-1)
    - Invented by NSA in 1995.
    - Produces 160-bit hash value string as a 40 digit hexadecimal number.
    - NIST deprecated the use of SHA-1 in 2011.
    - susceptible to brute-force attacks

* SHA-2 (Secure Hashing Algorithm-2)
    - Designed by NIST and NSA in 2001.
    - Most common variant of sha-2 is SHA-256 which returns a hash value of 256-bits as a 64 digit hexadecimal number.

> A hash is not considered to be cryptographically secure if two files have the same hash value or digest.

## IP Addresses (Easy)

**Fast Flux** - Fast Flux is a DNS technique used by botnets to hide phishing, web proxying, malware delivery and malware communication activities behind compromised hosts acting as proxies.
- Purpose of using Fast Flux network is to make the communication between malware and its command and control server(C&C) challenging to be discovered by security professional.
- Fast Flux network is having multiple IP addresses associated with a domain name, which is constantly changing.

## Domain Names (Simple)

* Punycode attack
    - Fuzzy hashing is also a strong weapon against the attacker's tools. Fuzzy hashing helps you to perform similarity analysis - match two files with minor differences based on the fuzzy hash values. rPunycode attack used by the attackers to redirect users to a malicious domain that seems legitimate at first glance.

## Host Artifacts (Annoying)

* Host artifacts are the traces or observables that attackers leave on the system, such as registry values, suspicious process execution, attack patterns or IOCs (Indicators of Compromise), files dropped by malicious applications, or anything exclusive to the current threat.

## Network Artifacts (Annoying)

* A network artifact can be a user-agent string, C2 information, or URI patterns followed by the HTTP POST requests.An attacker might use a User-Agent string that hasn’t been observed in your environment before or seems out of the ordinary.

## Tools (Challenging)

* Fuzzy hashing is also a strong weapon against the attacker's tools. Fuzzy hashing helps you to perform similarity analysis - match two files with minor differences based on the fuzzy hash values. 

## TTPs (Tough)

* TTPs - TTPs stands for Tactics, Techniques & Procedures. This includes the whole MITRE ATT&CK Matrix, which means all the steps taken by an adversary to achieve his goal, starting from phishing attempts to persistence and data exfiltration. 

* If you can detect and respond to the TTPs quickly, you leave the adversaries almost no chance to fight back.
