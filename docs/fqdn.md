# Fqdn
## FQDN = Fully Qualified Domain Names

A fully qualified domain name (FQDN) is the complete domain name for a specific computer, or host, on the internet. 

The FQDN consists of two parts: the hostname and the domain name. For example, an FQDN for a hypothetical mail server might be mymail.somecollege.edu. 
The hostname is mymail, and the host is located within the domain somecollege.edu.

### Ssh client ?
When connecting to a host (using an SSH client, for example)
 * You must specify the FQDN. 
 * The DNS server then resolves the hostname to its IP address by looking at its DNS table. 
 * The host is contacted and you receive a login prompt.
