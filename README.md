# Linux-SWAP
Linux一键设置SWAP大小，优化SWAP参数

使用方法：

      curl https://raw.githubusercontent.com/john8911/Linux-SWAP/master/swap.sh -o swap.sh && chmod +x swap.sh && bash swap.sh
      
      

# Linux-SSH
Linux-SSH端口一键修改脚本

使用方法：

      curl https://raw.githubusercontent.com/john8911/Linux-SWAP/master/sshport.sh -o sshport.sh && chmod +x sshport.sh && bash sshport.sh
      
输入端口确认。再打开防火墙端口：

# 如果防火墙使用的iptables（Centos 6），修改端口为8080
```
iptables -I INPUT -p tcp --dport 8080 -j ACCEPT
service iptables save
service iptables restart
```
# 如果使用的是firewall（CentOS 7）
```
firewall-cmd --zone=public --add-port=8080/tcp --permanent 
firewall-cmd --reload
```

最后重启ssh生效：
```
#CentOS系统
service sshd restart
#Debian/Ubuntu系统
service ssh restart      
```
