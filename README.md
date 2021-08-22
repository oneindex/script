# script
script

## DD.sh  
```
bash <(wget --no-check-certificate -qO- 'https://git.io/dd.sh') -d 10 -v 64 -p "自定义root密码" -port "自定义ssh端口"
```
  
  
## 开机改密： 
```
#!/bin/bash
echo root:Vicer |sudo chpasswd root
sudo sed -i 's/^#\?PermitRootLogin.*/PermitRootLogin yes/g' /etc/ssh/sshd_config;
sudo sed -i 's/^#\?PasswordAuthentication.*/PasswordAuthentication yes/g' /etc/ssh/sshd_config;
sudo reboot
```
