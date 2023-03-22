# Amazon S3

---
# CentOS
rsync= checks all the info in two directories and update if there is any change 
sync a folder or a file with another directory; a= exactly all the file, v= verbose
```
rsync -avz /home/ /mnt
```

```/etc/fstab```

```
xfs noexec,defaults 0 0
```


shows the logs in ```var/log/secure```


s= source; g= file path
```
sed -i 's/SELINUX=enforcing/SELINUX=disabled/g' /etc/selinux/config
```
Set timezone to Asia-Kolkata
```
timedatectl set-timezone Asia/Kolkata
```

Bind Mariadb Server with loopback IP or localhost or lo or 127.0.0.1 ```vi /etc/my.cnf.d/server.cnf``` or ```vi /etc/my.cnf```

edit it
```
bind-address=127.0.0.1
```

# REDHAT

Changes in ```cat /etc/sysconfig/network-scripts/ifcfg-ens3``` [ens3=ETHERNET] for making dhcp address to static address

We have to add IPADDR variable by outselves and insert the new IP address
```
BOOTPROTO
ONBOOT YES
IPADDR
GATEWAY
DNS
NETMASK
```
Example:-
```
IPADDR=192.168.10.101
GATEWAY=192.168.10.1
DNS=192.168.10.254
NETMASK=255.255.255.0
```
command for checking the destination, gateway, genmask,
```
route -n
```

---

