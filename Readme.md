# Ansible 


### Install Ansible v2.3.1 with python pip. Report details where ansible has been installed.
<img src="/pictures/8.png">
<img src="/pictures/9.png">


### Create ansible inventory file (name: inventory) with remote host connection details:

- Remote VM hostname/ip/port
- Remote ssh login username
- Connection type

<img src="/pictures/1.png">

### Test ansible connectivity to the VM with ad-hoc command: 

Find out host details:
Number of CPUs
Host name
Host IP(s)
Total RAM

Create info.yml file with 4 tasks 
<img src="/pictures/2.png">
<img src="/pictures/3.png">



### Develop a playbook (name: tomcat_provision.yml) which is supposed to run against any host (specified in inventory)

Software installation requirements:
- Tomcat AS should be installed from sources (tar.gz) – download from the official site (http://archive.apache.org/dist/tomcat/).
- Tomcat AS should be owned (and run) by user tomcat_as:tomcat_as_group
- Tomcat AS version should be 8.x
- Tomcat installation folder (CATALINA_HOME) is /opt/tomcat/$version, where $version is the version of tomcat defined in playbook
- Java can be installed from CentOS Repositories

<img src="/pictures/5.png">
<img src="/pictures/6.png">
<img src="/pictures/7.png">
<img src="/pictures/4.png">



### 3 different checks

- systemctl status tomcat
<img src="/pictures/10.png">
- curl -l http://192.168.56.10:8080 or curl -l http://localhost:8080
<img src="/pictures/11.png">
- wget http://192.168.56.10:8080 or wget -l http://localhost:8080
<img src="/pictures/12.png">

