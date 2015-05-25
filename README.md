# vagrant-lab-environment
This is a vagrant environment to create/make/practice labs of infrastructure elements

## Requirements
- Virtualbox + Vbox Guest Additions
- Vagrant + vagrant-hostmanager plugin
- Powerfull machine to virtualize

## How to do it
Just clone this repo and understand how environment file works

```
git clone https://github.com/padajuan/vagrant-lab-environment.git
cd vagrant-inf-environment
```

This is the environment file:

```
---
gfs01:
  memory: 1024
  cpus: 1
  address: 192.168.33.10
  box: RH7.1
  storage: 5
  storage_port: 0

gfs02:
  memory: 1024
  cpus: 1
  address: 192.168.33.11
  box: RH7.1
  storage: 5
  storage_port: 1
```

Now will wake up 2 VMs with this details, 1CPU, 1024 gb de RAM, the Box name RH7.1 and 5GB of storage on a SCSI port
(I just using SCSI because of many errors with SATA controller of Vbox).
Feel free to modify the Vagrant file as your needs.
