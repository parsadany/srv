# Server Config:
All commads and sample conf needed frequently

In the words of mine:
> Don't forget to reboot your server as its first time boot!
> 
> Allways keep your OS up to date.
> 
> Allways write what you did on it somewhere! (if you have about 6 or 7 servers just like me, you will forget all of em!)
> 
> I strongly recommend that forget old OS versions and use almost up-to-date versions. (If you hate troubles, leave the centos7 or debian9 or ubuntu16)
> 
> Debian is almost more stable than Ubuntu. But if you need everything be up-to-date you are forced to use Ubuntu!
> 
> RHEL dists are more better (more secure and lightweight) than Debian dists.
> 
> Use Arch if and only if you are an Arch master!
> 
> DO NOT install subprocess.run via pip! you can simply import it by default.



# SSH: 

## ssh config:
```
/etc/ssh/ssh_config
```
## sshd config:
```
/etc/ssh/sshd_config
```
## generate new key:
```
ssh-keygen
```
## copy key to server:
```
ssh-copy-id -i ~/.ssh/id_rsa.pub root@host
```
# mosh

## mosh installing:
### REHL:

```
yum install mosh
```

### Debian-Based:

```
apt-get install mosh

apt install mosh
```

## mosh iptables:

```
iptables -I INPUT 1 -p udp --dport 60000:60002 -j ACCEPT

iptables-saveiptables-save > /etc/iptables/rules.v4 
```

# iptables:
```
iptables -nvL
iptables -D INPUT -j REJECT --reject-with icmp-host-prohibited
nft delete rule inet firewalld filter_INPUT handle 105
nft delete rule inet firewalld filter_INPUT handle 98

```

# Python on debian baseds:
## Dev Tools:
```
apt update
apt install build-essential
apt install build-essential libssl-dev libffi-dev python3-dev
apt install -y python3-pip
apt install -y python3-venv
```
## ftp address:
```https://www.python.org/ftp/python/```
## Download:
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
## install:
todo: add pattern of configure options.
```
./configure --enable-optimizations 
make
make install
```
## Updating path on debian baseds:
```
update-alternatives --install /usr/bin/python python /usr/local/bin/python3.7 10
update-alternatives --install /usr/bin/python python /usr/local/bin/python3.8 10
```
## Fixing and Updating Pip:
```
ln -s /usr/share/pyshared/lsb_release.py /usr/local/lib/python3.7/site-packages/lsb_release.py

ln -s /usr/share/pyshared/lsb_release.py /usr/local/lib/python3.8/site-packages/lsb_release.py

pip3 install --upgrade pip
```
## Specific version VirtualEnv:
```
python3.5 -m venv my_env_path
```

# Self-signed SSL:
```
https://www.digitalocean.com/community/tutorials/how-to-create-a-self-signed-ssl-certificate-for-nginx-on-centos-7
```




