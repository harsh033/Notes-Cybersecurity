## Window domains
- Window domain is a group of users and computers under the administration of a given business.

**Active directory** - Active Directory is a centraized repository or database for store credentials and information about objects within a network.

**Domain Controller** - The server that runs the Active Directory services is known as a doman controller.

- main advantage of having a configured windows domain are;
    + Centralised identity management
    + Managing security policies

### Object types on active directory
- Users
    + They can be authenticated by the domain and can be assigned privileges over resurces
    + users can be people(eg employees) or services(eg IIS or MSSQL)Every single service requires a user to run, but service users are different from regular users as they will only have the privileges needed to run their specific service.
    
- Machines
    + for every computer that joins the Active Directory domain, a machine object will be created. (eg DC01$).

- Security Groups 
    + you can define user groups to assign access rights to files or other resources to entire groups

### Organizational Units
-  These objects are organised in Organizational Units (OUs) which are container objects that allow you to classify users and machines. OUs are mainly used to define sets of users with similar policing requirements. (eg IT, sales, marketing)

> **Delegation** - give specific users some control over some OUs without needing a Domain Administrator to step in.

## Group Policy
- the main idea behind this is to be able to deploy different policies for each OU individually.

- To configure GPOs, you can use the **Group Policy Management** tool

## Authentication methods
- Two protocols can be used for network authentication in windows domains:
    * Kerberos
    * NetNTLM

> Kerberos - Kerberos is a computer network authentication protocol that operates based on tickets, allowing nodes to securely prove their identity to one another over a non-secure network. It primarily aims at a client-server model and provides mutual authentication, where the user and the server verify each other's identity. The Kerberos protocol messages are protected against eavesdropping and replay attacks, and it builds on symmetric-key cryptography, requiring a trusted third party.

## Trees, Forest and Trust

