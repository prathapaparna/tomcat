# tomcat

Tomcat:
--------
How to create users in tomcat

default port for tomcat - 8080
allow port in security group 

<role rolename="manager-gui"/>
<role rolename="manager-script"/>
<role rolename="manager-jmx"/>
<role rolename="manager-status"/>
<role rolename="admin-gui"/>
<user username="tomcat" password="s3cret" roles="manager-gui,manager-script,manager-jmx,manager-status"/>
<user username="admin" password="admin1" roles="admin-gui"/>

Active Directory / Open LDAP
-----------------------------
Users and Groups

Developers not required deployments
Devops require deployment

Developmenet - doesn't have manager/hostmanager access	
Devops		 - he can get manager access
Admin		 - Hostmanager and manager access


If you want to copy files from one server to other server
1. Setup passwordless authentication between two server
2. use scp command

public key
private key

server1  -->  from	--> build
	ssh-keygen
server2  -->  to	--> tomcat

scp <src> <user>@<ip>:<dest>

tomcat  --> we can give full access on this user
deploy  --> Group

chown root:deploy /opt/tomcat/webapp 
