# srv
All commads and sample conf needed frequently


# SSH: 

##ssh config:
```
 /etc/ssh/ssh_config
```
##sshd config:
```
/etc/ssh/sshd_config
```
##generate new key:
```
ssh-keygen
```
##copy key to server:
```
ssh-copy-id -i ~/.ssh/id_rsa.pub root@host
```

#iptables:
```
iptables -nvL
iptables -D INPUT -j REJECT --reject-with icmp-host-prohibited
```

#Python:
## ftp address:
```https://www.python.org/ftp/python/```
## Download and install:
```
makdir tmp && cd tmp
```
### py37
```
wget https://www.python.org/ftp/python/3.7.9/Python-3.7.9.tar.xz
tar xf Python-3.7.9.tar.xz
cd ./Python-3.7.3 
```
### py38
```
wget https://www.python.org/ftp/python/3.8.7/Python-3.8.7.tar.xz
tar xf Python-3.8.7.tar.xz 
cd Python-3.8.7/
```
###install:
todo: add pattern of configure options.
```
./configure
make
make install
```



