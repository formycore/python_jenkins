# on centos
```
sudo su -
yum install python3 -y
python3 -m pip install --upgrade pip
echo "jenkins ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers
yum install make -y
yum groupinstall "Development Tools" -y
- normal user
sudo usermod -aG docker jenkins
docker images 

jenkins plugins
- docker 
- docker pipeline
- docker-build-step
- cloudbees docker build and publish
```