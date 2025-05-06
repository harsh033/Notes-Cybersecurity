## Basic system information
* `set` - check your path from the command line

* `ver` - Determining the operating system version

* `systeminfo` - list various information about the system.

## Network troubleshooting

* `ipconfig` - check network information.

* `ipconfig /all` - for more information

* `ping target_name` - checking if the server can access a particular server on the Internet.

* `tracert target_name` - traces the network route traversed to reach the target.

* `nslookup` -  It looks up a host or domain and returns its IP address. 

* `netstat` - This command displays the current network connections and listening ports.

## File and disk management

* `dir` - view child directories
    - `dir /a` - display hidden directories
    - `dir /s` - display files in the current directory and all subdirectories.

* `tree` - visually represent the child directories.

* we can delete a file using `del` or `erase`.

* `type` - to display the textfile contents.

* use wildcard character to refer multiple files `copy *.md c:\Markdown`

## Task and Process management

* You must be familiar with MS Windows Task Manager and might be familiar with killing non-responsive processes. Let’s discover how to achieve a similar functionality using the command line.

* we can list the running processes using `tasklist`

* we can also filter the output eg. `tasklist /FI "imagename eq sshd.exe"`

* we can terminate any task using `taskkill /PID target_pid`

## Conclusion

* some advance commands
    - `chkdsk` - checks the file system and disk vilumes for errors and bad sectors.
    - `driverquery` - display a list of installed drivers.
    - `sfc /scannow - scans system files for corruption and repairs them if possible.
