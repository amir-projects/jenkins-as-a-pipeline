# jenkins-as-a-pipeline
Creating Jenkins pipeline and configuration.
The purpose of this guide is to write installation process step by step on ubuntu 22.04 LTS

# Setup process
#!/bin/bash
sudo apt update
sudo apt install openjdk-8-jdk -y
sudo apt install maven -y 
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
