#this is my third project installing sonarqube on centos7
#!/bin/bash
#Description: Installation of sonarqube on centos7
#Author: Temitope Ojelade Atiku
echo "installation of sonarque in progress"
echo
sleep 1
yum update -y
echo
sleep 1
echo
yum install java-11-openjdk-devel -y
sleep 1
echo
yum install java-11-openjdk -y
sleep 1
echo
cd /opt
sleep 1
echo
yum install wget -y 
sleep 1
echo
wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.3.0.51899.zip
sleep 1
echo
yum install wget -y
sleep 1 
echo
unzip /opt/sonarqube-9.3.0.51899.zip
sleep 1
echo
chown -R vagrant:vagrant /opt/sonarqube-9.3.0.51899
sleep 1
echo
cd /opt/sonarqube-9.3.0.51899/bin/linux-x86-64
sleep 1
echo
./sonar.sh start
