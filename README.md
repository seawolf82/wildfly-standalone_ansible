# wildfly13-standalone_ansible
wildfly13-standalone_ansible

This script install wildfly13 in standalone mode on remote machine through ansible and enabling management console to manage it

N.B. 

Oracle Jdk it is not installed. The user will have to install it through rpm package ora tar.gz ans afterwards setting JAVA_HOME

To launch ansible script use:

ansible-playbook -vv -i hosts site.yaml
