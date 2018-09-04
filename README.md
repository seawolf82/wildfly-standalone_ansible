# wildfly13-standalone_ansible
wildfly13-standalone_ansible

This script install wildfly13 in standalone mode on remote machine through ansible and enabling management console to manage it

N.B. 

Oracle Jdk it is not installed. The user will have to install it through rpm package or tar.gz and afterwards setting JAVA_HOME


However this installation of wildfly is tested with Oracle Jdk 10.1

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
