# CI-CD-PIPELINE-DEMO

This is an example ready-to-deploy java web application built for Tomcat using Maven and webapp-runner.

#Jenkins Repo and key download command:

sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo

sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key

#Maven download command:

wget https://mirrors.gigenet.com/apache/maven/maven-3/3.8.1/binaries/apache-maven-3.8.1-bin.tar.gz

#Sonarqube Download Command:

wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-6.7.7.zip

#Sonarqube scanner download command:

wget https://binaries.sonarsource.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-4.1.0.1829-linux.zip

#TOMCAT download command:

wget https://mirrors.ocf.berkeley.edu/apache/tomcat/tomcat-8/v8.5.69/bin/apache-tomcat-8.5.69.tar.gz

#TOMCAT user details:
  <role rolename="manager-script"/>
  <role rolename="manager-gui"/>
  <user username="tomcat" password="tomcat" roles="manager-script,manager-gui"/>
  
  
#Sample Pipeline Script.

pipeline {
      agent any
      stages {
            stage('clone') {
                  steps {
                        echo 'cloning GITHUB repository'
                    
                  }
            }
            stage('Build') {
                  steps {
                        echo 'Building Maven Project'
                  }
            }
            stage('Deploy') {
                  steps {
                        echo "Deploying the application"
                  }
            }
          
      }
}

#Testing jenkins-ansible integration.
