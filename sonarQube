# SonarQube
===================

Installing the Java-1.11 or Java 11:
------------------------------------

Step:1 Install using the command as below
$ sudo yum list | grep java 
$ yum -y install java-11-openjdk-devel.x86_64

Step:2 Check the Java Version.
$ java -version

--------------------- 

SonarQube Server  Installation Commands:
========================================

# Login as a root user.
$ sudo su -

$ sudo cd /opt
$ sudo wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.8.0.42792.zip
$ sudo unzip sonarqube-8.8.0.42792.zip 
$ ls 
$ sonarqube-8.8.0.42792  sonarqube-8.8.0.42792.zip

#  As a good security practice, SonarQube Server is not advised to run sonar service as a root user, so create a new user called "sonar" and grant sudo access to manager "sonar" service as follows.

$ useradd sonar 
$ passwd sonar

# give the sudo access to that user "sonar"
$ sudo visudo
$ se nu [ line number 100]

# Go to Line No: 100 ; If you don't want to get password all the "sonar" user Always
sonar   ALL=(ALL)	NOPASSWD:ALL
:wq!   --> Save it

# Now $ ls -l    -> The sonarqube-7.9.1  directory running by root user and group.
So change it. Change the ownership from root to sonar.
 $ chown -R sonar:sonar /opt/softwares//sonarqube-7.9.1

# Now change as a sonar user from root for starting the software.
$ su - sonar

$ pwd 
# Now you are in /home/sonar
# Go to the   from sonar user    /opt/softwares/sonarqube-7.9.1  This is SonarQube Home Directory. 
$  ls
bin  conf  COPYING  data  elasticsearch  extensions  lib  logs  temp  web
Note: These above Cement colors are Directories

# Give the  permissions for that directory. 
$ chmod -R 775 /opt/softwares/sonarqube-7.9.1

# Go to bin Directory in SonarQube Home Directory.  Go to 64-bit architecture OS.
$ cd linux-x86-64 
lib  sonar.sh  wrapper

# start the Server and Pause the Argument as "start"
$  ./sonar.sh  start   OR   $ sh sonar.sh start

# check whether the sonarqube started or Not.
$  ./sonar.sh  status   OR   $ sh sonar.sh status

# To stop the sonar server
$ sh sonar.sh stop
