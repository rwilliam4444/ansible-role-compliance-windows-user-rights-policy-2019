# Role Name:
- ansible-role-compliance-windows-user-rights-policy-2019

# Description:
This User Rights Policy Role was based off the CIS specs for 2019 servers.   
This role covers the "Credential Validation" CIS section only. There are NO
checks here - just remediation commands.  The remediation commands are for local
settings only. Group Policy settings may override these settings. When the
"remediate" variable is set to "YES", the role will try to remediate the
server's setting(s) accoridng to the CIS standards.  Again, there are NO checks
available on this role - just remediation tasks according to the 2019 CIS
standards.   The defaults/main.yml file can be used to disable specific CIS
items (i.e. "execute_<cis task #>") from executing. The default value in the
defaults/main.yml for these CIS item variables (i.e. "execute_<cis task #>") is
set to "YES". The value "YES" means that the CIS item will execute at run time.
Set the value to "NO" if you want to skip this CIS item in question from
executing.

# Requirements:
Windows Ansible related pre-requisites


# Defaults file for ansible-role-compliance-windows-user-rights-policy-2019:
# Variables
Parameter | Choices/Defaults|Comments
----------|-----------------|--------
__remediate__ |"NO"| variable used to determine whether or not to remediate.


# Example Playbook:
---
 - hosts: [win]
   roles:
   - ansible-role-compliance-windows-user-rights-policy-2019


# Author Information:
Richard M. Williams (williamsitv@yahoo.com)
