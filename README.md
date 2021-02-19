# srv
All commads and sample conf needed frequently


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

# iptables:
```
iptables -nvL
iptables -D INPUT -j REJECT --reject-with icmp-host-prohibited
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





