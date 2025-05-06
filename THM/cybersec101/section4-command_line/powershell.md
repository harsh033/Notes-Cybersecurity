## Powershell
* PowerShell is a task automation and configuration management program from Microsoft, consisting of a command-line shell and the associated scripting language.

* developed to overcome the limitation of traditional command line tools like cmd.exe.

### Object
* In programming, an object represents an item with properties (characteristics) and methods (actions). For example, a car object might have properties like Color, Model, and FuelLevel, and methods like Drive(), HonkHorn(), and Refuel().

* Similarly, in PowerShell, objects are fundamental units that encapsulate data and functionality, making it easier to manage and manipulate information. An object in PowerShell can contain file names, usernames or sizes as data (properties), and carry functions (methods) such as copying a file or stopping a process.

### Basic syntax
* powershell commands are known as cmdlets. They are much more powerful than the traditional window commands and allow  for more advanced data manipulation.

* Cmdlets follow a consistent `Verb-Nown` naming convention.
    - `Get-Content` - retrieves(gets) the content of a file and displays it in the console.
    - `Set-Location` - Changes(sets) the current working directory.

#### Basic cmdlets

* **Get-Command** - To list all available cmdlets, functions, aliases, and scripts that can be executed in the current PowerShell session.

* **Get-Help** - It provides detailed information about cmdlets eg `Get-Help Get-Date`

* **Get-Alias** - Lists all aliases available. eg- `dir` is an alias for `Get-ChildItem`, and `cd` is an alias for `Set-Location`.

#### Find and Download Cmdlets

* To search modules we can use `Find-Module`. if we don't know the name of the module then we can use `Name` property and wildcard `*` eg - `Find-Module -Name "PowerShell*"`

* Once identified the module can be install from the repo with `Install-Module` eg- `Install-Module -Name "PowerShellGet"`

## Navigating the File System and Working with Files

* **Get-ChildItem** - lists the files and directories in a location specified with the `-Path`. [`dir`]

* **Set-Location** - To navigate to a different directory. [`ls`]

* **New-Item** - To create an item in PowerShell, we will need to specify the path of the item and its type eg- `New-Item -Path ".\captain-cabin\captain-wardrobe" -ItemType "Directory"`.

* **Remove-Item** - cmdlet removes both directories and files, whereas in Windows CLI we have separate commands `rmdir` and `del`. eg- `Remove-Item -Path ".\captain-cabin\captain-wardrobe"`

* **Copy-Item** - equivalent to `copy`.
* **Move-Item** - equivalent to `move`.

* **Get-Content** - To read and display the contents of a file similar to `type` in command prompt or `cat` in unix-like system.


## Piping, Filtering and Sorting data

* Sort-Object
* Where-Object
* Select-Object
* **Select-String** - eg- `Select-String -Path ".\captain-hat.txt" -Pattern "hat"`

* eg- `Get-ChildItem | Sort-Object Length -Descending | Select-Object -First 1`

## System and Network Information

* `Get-ComputerInfo` -  retrieves comprehensive system information.
* `Get-LocalUser` - List all the local user accounts.
* `Get-NetIPConfiguration` - provides detailed information about the network interfaces on the system, including IP addresses, DNS servers, and gateway configurations.

* Get-NetIPAddress` - show details for all IP addresses configured on the system.

## Real-Time System Analysis

* `Get-Process` - provides a detailed view of all currently running processes.

* `Get-Service` -  information about the status of services on the machine.

* `Get-NetTCPConnection` - display current TCP connections.

* `Get-FileHash` - for generating file hashes.

## Scripting

* Scripting is the process of writing and executing a series of commands contained in a text file, known as a script

* `Invoke-Command` - is essential for executing commands on remote systems.`
