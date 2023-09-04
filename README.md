# Learn-Jenkins

[Jenkins](https://www.jenkins.io/doc/book/installing/linux/)https://www.jenkins.io/doc/book/installing/linux/)
## Install Jenkins on Linux 

### Dependencies 
```
sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo

sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key

sudo dnf upgrade

# Add required dependencies for the jenkins package
sudo dnf install java-17-openjdk
sudo dnf install jenkins
sudo systemctl daemon-reload
```

### Jenkins 
```
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null

echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt-get update

sudo apt-get install jenkins
```

### Commands 

- You can enable the Jenkins service to start at boot with the command:
```
sudo systemctl enable jenkins
```
- You can start the Jenkins service with the command:
```
sudo systemctl start jenkins
```
- You can check the status of the Jenkins service using the command:
```
sudo systemctl status jenkins
```
- Accessing jenkins
```
192.168.1.4:8080
