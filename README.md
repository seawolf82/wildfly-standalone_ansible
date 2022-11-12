# wildfly-standalone_ansible
wildfly-standalone_ansible

This script install wildfly in standalone mode on remote machine through ansible and enabling management console to manage it

Tested with openjdk17 on Almalinux8-9 RockyLinux8-9

Tested with openjdk18 on Centos7

Tested with:

- 2.9 Ansible version

To install wildfly run:

ansible-playbook -vv -i hosts site.yaml

To uninstall wildfly run:

ansible-playbook -vv -i hosts deprovision.yaml

Adding Tags to permit run only specific task of playbook

Tags:

upgrade
package
selinux
ntp
wildfly
epel

For example, to launch only task regarding upgrade os, run:
 
ansible-playbook -vv --tags "upgrade" -i hosts site.yaml
