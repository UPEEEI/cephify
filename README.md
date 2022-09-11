# cephify
Simplified Ceph Deployment

Minimum setup: 3 monitor nodes, 3 manager nodes, 3 OSD nodes

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

 - Permit root SSH login in `/etc/ssh/sshd`
 - Generate public/private rsa key pair on root using `ssh-keygen`
 - Set root password
 - Copy public rsa to all nodes using `ssh-copy-id` 

# Usage
cephify *command* *node*
