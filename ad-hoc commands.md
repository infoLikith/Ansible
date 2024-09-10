# Ansible Ad-hoc commands
Ansible ad-hoc commands are simple, one-time use commands executed without the need for a playbook. They are mainly used for quick tasks or testing purposes. These commands allow you to perform actions across multiple hosts specified in your inventory file.

## Ad-hoc commands are useful for:

**Gathering information about your hosts**

**Managing files and directories**

**Installing or removing packages**

**Rebooting servers**

**Checking service status**

## Example Ad-hoc Commands:

**1. Ping all hosts**

````
ansible all -m ping
````
This command checks the connectivity with all hosts in the inventory.

**2. Install a package:**

````
ansible web -m dnf -a "name=httpd state=present" --become

````
This installs the httpd package on hosts in the webservers group using the yum module

**3. Start the httpd in the target node from the controller**

````
ansible web -m service -a "name=httpd state=started" --become
````
***Ad-hoc commands are convenient for quick actions but not meant for reusable automation like playbooks.***




