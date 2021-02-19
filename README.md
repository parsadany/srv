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


