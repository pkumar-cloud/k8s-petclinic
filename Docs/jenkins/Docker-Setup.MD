## Install Docker
```sh
yum install -y docker
systemctl start docker
systemctl enable docker

OR
service docker status
service docker start
chkconfig docker on
```

## provide permissions to jenkins user in jenkins server to access docker
```sh
  Not needed: sudo groupadd docker
  # When docker is installed, docker group is created.
  cat /etc/group | grep -i docker
  sudo usermod -aG docker jenkins
  sudo chmod 777 /var/run/docker.sock
```
## Add Jenkins user into sudoers file to get sudo access
```sh
   # To execute the helm commands, jenkins user needs sudo access
   vi /etc/sudoers
   jenkins ALL=(ALL) NOPASSWD: ALL
   # #Add under: Allow root to run commands anywhere
```   
   

