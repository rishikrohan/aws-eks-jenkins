# aws-eks-jenkins


## aws-eks-jenkins

### Install Java 

### Install AWS CLI 

### Install Jenkins Server

### Install Maven

```shell


yum install wget
wget https://mirror.lyrahosting.com/apache/maven/maven-3/3.8.1/binaries/apache-maven-3.8.1-bin.tar.gz
tar -xvzf apache-maven-3.8.1-bin.tar.gz
export M2_HOME=/opt/apache-maven-3.8.1
export M2=$M2_HOME/bin
PATH=$PATH:$M2

```

### Install Docker

```shell

yum install docker
systemctl start docker
systemctl enable docker

```

### provide permissions to jenkins user in jenkins server to access docker

```shell

  cat /etc/group | grep -i docker

  sudo groupadd docker
  sudo usermod -aG docker jenkins
  sudo chmod 777 /var/run/docker.sock

  ```

### add Jenkins user into sudoers file to get sudo access

```shell

vi /etc/sudoers
jenkins ALL=(ALL) NOPASSWD: ALL

```




