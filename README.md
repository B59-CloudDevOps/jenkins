# jenkins

Jenkins is a CI/CD Framework which plays a very important role in software industry.

    Using jenkins and with UI we will use this to run our jobs or to schedule our jobs.

Installing Linux:
    > https://www.jenkins.io/doc/book/installing/linux/
    > https://www.jenkins.io/doc/book/installing/linux/#red-hat-centos

Server Requirements:
    > t3.medium, spot , 30gb storage

```
sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
sudo yum upgrade -y 
# Add required dependencies for the jenkins package
sudo yum install fontconfig java-17-openjdk -y
sudo yum install jenkins -y
sudo systemctl daemon-reload
```