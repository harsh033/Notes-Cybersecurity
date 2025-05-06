## SCP
- Secure copy, or SCP, is just that -- a means of securely copying files. Unlike the regular cp command, this command allows you to transfer files between two computers using the SSH protocol to provide both authentication and encryption.

Working on a model of SOURCE and DESTINATION, SCP allows you to:

Copy files & directories from your current system to a remote system
Copy files & directories from a remote system to your current system

eg - `scp important.txt ubuntu@192.168.1.30:/home/ubuntu/transferred.txt`

## Serving files from your host-web
- Ubuntu machines come pre-packaged with python3. Python helpfully provides a lightweight and easy-to-use module called "HTTPServer". This module turns your computer into a quick and easy web server that you can use to serve your own files, where they can then be downloaded by another computing using commands such as curl and wget. Simply, all we need to do is run `python3 -m http.server`. Now use wget to download the file eg- `wget http://10.10.50.80:8000/myfile`.

## another useful commands
- `systemctl [option] [service]`
- `ps aux`
- `fg`

## Automation - execute commands at specific time
- cron
- crontabe -e

## Maintaining you system - package management
> When developers wish to submit software to the community, they will submit it to an  "apt" repository. If approved, their programs and tools will be released into the wild. 

- Additional repositories can be added by using the `add-apt-repository` command 
- **GPG (Gnu Privacy Guard)** - When adding software, the integrity of what we download is guaranteed by the use of what is called GPG (Gnu Privacy Guard) keys. These keys are essentially a safety check from the developers saying, "here's our software". If the keys do not match up to what your system trusts and what the developers used, then the software will not be downloaded.




