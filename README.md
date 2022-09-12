# cephify
Simplified Ceph Deployment

Minimum setup: 3 monitor nodes, 3 manager nodes, 3 OSD nodes (at least *2* parent OSD to prevent degraded pgs)

# Prerequisite
## Setup node01 [master] as root
  - Create .ssh/config
```
Host node01
  Hostname 10.158.1.220
  User root
  Port 22
  
Host node02
  Hostname 10.158.1.221
  User root
  Port 22
```

 - Generate public/private rsa key pair on root using `ssh-keygen` on node01-master
 - Copy public rsa key to all nodes manually(recommended) or by using `ssh-copy-id`(might need to enable `PermitRootLogin` in `/etc/ssh/sshd_config` and root password) 

# Usage
cephify *command* *node*
