## Introduction
* Yara (Yet Another Ridiculous Acronym)
* Yara was developed by Victor M. Alvarez (@plusvic) and @VirusTotal.
* def - "The pattern(textual or binary) matching swiss knife for malware researchers (and everyone else)"
* Yara rules are frequently written to determine if a file is malicious or not, based upon the features - or patterns - it presents.

## Inroduction to YARA rules

syntax command:- `yara myrules.yar myfile`

## Expanding on yara rules

* **Meta**
This section of a Yara rule is reserved for descriptive information by the author of the rule. eg `desc` use for description of rule.

* **Strings**
You can use strings to search for specific text or hexadecimal in files or programs.
```
rule helloworld_check{
    strings:
        $hello_world = "Hello World!"
        
    condition:
        $hello_world
}
```

```
rule helloworld_checker{
	strings:
		$hello_world = "Hello World!"
		$hello_world_lowercase = "hello world"
		$hello_world_uppercase = "HELLO WORLD"

	condition:
		any of them
}
```
or we can use condition operator (`<=, >=, !=`) and keywords (and, or, not)

```
    condition:
        $hello_world and filesize < 10KB
```
## Yara Modules

**cuckoo**
Cuckoo Sandbox is an automated malware analysis environment. This module allows you to generate Yara rules based upon the behaviours discovered from Cuckoo Sandbox.

**PythonPE**
Python's PE module allows you to create Yara rules from the various sections and elements of the Windows Portable Executable (PE) structure.

## Other tools and yara

### YARA tools

**LOKI**
LOKI is a free open-source IOC (Indicator of Compromise) scanner

**THOR**
THOR Lite is Florian's newest multi-platform IOC AND YARA scanner.

**FENRIR**
Simple Bash Script for IOC checker.

## Valhalla
Valhalla boosts your detection capabilities with the power of thousands of hand-crafted high-quality YARA rules.


