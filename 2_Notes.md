# on centos
```
sudo su -
yum install python3 -y
python3 -m pip install --upgrade pip
echo "jenkins ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers
yum groupinstall "Development Tools" -y
- normal user
sudo usermod -aG docker jenkins

```