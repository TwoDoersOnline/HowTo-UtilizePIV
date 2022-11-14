# HowTo-UtilizePIV
Cloud server smartcard integration (DoD focused) with Django + Nginx + Daphne/Gunicorn

Major requirements for project
1. A server (more on this later)
1. Version of Python
1. Smartcard reader
1. Redis, Postgres, Nginx


## Provisioning/installing a server
Feel free to chose either option or try out both if you'd like.
  -Server stability option
    This option is best for as little coupling as possible with your home environment.

1. Spin up a server on any provider some options are:
    digitalocean, vultr, heroku, linode
   
1. Provision (create) a "server" on your provider, it may be called something else
    i.e. digitalocean calls them "droplets" vice vultr calls them "servers"
   
   
## Do it yourself option
1. Spin up a server (not in this HowTo's scope) using an option of:
    spare computer, hypervisor, WSL, or any other Virtual Machine (VM) option. 
    
1. Check out https://ubuntu.com/download/server for installing Ubuntu Server. 
    VM: look to mount the ISO or disc image.
    Physical: Use Balena Etcher to install the ISO as a bootable image onto a flash drive. 
      Be aware on Linux a "live" option means you can't save anything unless you make a "persistent" partition.
      
## Post-install updating and package installation 
1. Linux: use apt, yum, rpm for package repository or download source code for everything yourself.
   Be aware doing this one by one is a huge time burden and can lead to dependancy issues. 
    on Ubuntu: apt-get install python3.11 python3.11-venv ufw redis-server daphne 
   Windows: Download Python at https://www.python.org/downloads/release/python-3110/ the link layout
    should you want a different version change the 3110 say for 3.8.2 is just 382
    
 If for some reason your distro doesn't have the new version you want I would suggest waiting on it for 
 Linux due to how many packages it influences it's easier to just fallback to an earlier vesion.
