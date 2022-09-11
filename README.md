# cephify
Simplified Ceph Deployment

# Prerequisite
## Setup node01 [master] as root
Create .ssh/config
```
Host node01
  Hostname 10.158.1.220
  User root
  Port 80
  
Host node02
  Hostname 10.158.1.221
  User root
  Port 80
```

# Usage
cephify <command> <node>
