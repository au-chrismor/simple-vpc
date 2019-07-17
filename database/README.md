# DATABASE

## What it does

database is an example of how to create RDS database instances under Ansible control.

A couple of things to note, which you probably should alter for production:

* The password for the database is stored using Ansible Vault.  You will need to generate your own vault data and update the vars/main.yml file.  Details how to do this are located at:  https://docs.ansible.com/ansible/latest/user_guide/vault.html

* Security groups could be tightened up.  By default, the database instance relies on the main VPC Security Group.  You might want to create another group and grant access only to the specific ports required.

* When you launch the database role out of site.yml, the command line needs to include *'--ask-vault-password'*, or use one of the storage methods (such as *--vault-password-file*) described in the ansible documentation.  NEVER store your passwords in git repos.

