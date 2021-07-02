# Local Setup

### Virtual Box Installation

Download Virtual Box to play/work/Hands-On with Multiple Operating System.
https://www.virtualbox.org/wiki/Downloads

#### Windows Installation
You can [download](https://download.virtualbox.org/virtualbox/6.1.22/VirtualBox-6.1.22-144080-Win.exe) for Windows Machine. 


There are Multiple ways to install OS on Virtual Box. I use vagrant for Local dev Environment setup.

### Vagrant
This Tutorial is about using Vagrant with VirtualBox. Because it is free and can work with many other providers.
For more details ["Why Vagrant?"](https://www.vagrantup.com/intro/index)

##### Install Vagrant

##### Windows Installation
You can Download the Vagrant Binary for windows 64-bit from [here](https://releases.hashicorp.com/vagrant/2.2.16/vagrant_2.2.16_x86_64.msi). For others, https://www.vagrantup.com/downloads

Installation via Command Line. Open Powershell as Administrator,

```
.\vagrant_2.2.16_x86_64.msi 
```

This above command will install the vagrant or Double the msi file to install via GUI.

Once, the Vagrant is Installed. To play with Multiple Providers, Create a New Project Directory.

```
mkdir Vagrant_ubuntu
cd Vagrant_ubuntu
ls 
```
under the Newly Created Directory, you wont find any files,Now, to install ubuntu,

```
vagrant init ubuntu/trusty64
ls
```

Now you will see a file, `Vagrant` file. A new ubuntu/Trusty file has been initialized, Lets spin up the new Ubuntu machine. Similary you can Download any OS from [Vagrant Cloud](https://app.vagrantup.com/)

```
Vagrant up  
```
The Above command, will start the fresh new Environment. This may take time, because it has to download the ubuntu image from the vagrant Cloud and install the Ubuntu on your
local machine.

```
-> % vagrant status
Current machine states:

default                   running (virtualbox)

The VM is running. To stop this VM, you can run `vagrant halt` to
shut it down forcefully, or you can run `vagrant suspend` to simply
suspend the virtual machine. In either case, to restart it again,
simply run `vagrant up`.
```

will show the current status of the OS,(i.e stopped, running, etcc..), if the status is running, ssh in to the machine,

```
vagrant ssh 
Welcome to Ubuntu 14.04.6 LTS (GNU/Linux 3.13.0-170-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Thu Jul  1 18:03:13 UTC 2021

  System load:  0.0               Processes:           74
  Usage of /:   3.6% of 39.34GB   Users logged in:     0
  Memory usage: 25%               IP address for eth0: 10.0.2.15
  Swap usage:   0%

  Graph this data and manage this system at:
    https://landscape.canonical.com/

UA Infrastructure Extended Security Maintenance (ESM) is not enabled.

0 updates can be installed immediately.
0 of these updates are security updates.

Enable UA Infrastructure ESM to receive 64 additional security updates.
See https://ubuntu.com/advantage or run: sudo ua status

New release '16.04.7 LTS' available.
Run 'do-release-upgrade' to upgrade to it.


Last login: Thu Jul  1 18:03:14 2021 from 10.0.2.2
vagrant@vagrant-ubuntu-trusty-64:~$ 
vagrant@vagrant-ubuntu-trusty-64:~$ cat /etc/issue
Ubuntu 14.04.6 LTS \n \l
```

The above command will ssh in to the newly created ubuntu machine.

#### More Vagrant Commands

# Starting a VM
- `vagrant up`                  -- starts vagrant environment (also provisions only on the FIRST vagrant up)
- `vagrant resume`              -- resume a suspended machine (vagrant up works just fine for this as well)
- `vagrant provision`           -- forces reprovisioning of the vagrant machine
- `vagrant reload`              -- restarts vagrant machine, loads new Vagrantfile configuration
- `vagrant reload --provision`  -- restart the virtual machine and force provisioning

# Getting into a VM
- `vagrant ssh`           -- connects to machine via SSH
- `vagrant ssh <boxname>` -- If you give your box a name in your Vagrantfile, you can ssh into it with boxname. Works from any directory.

# Stopping a VM
- `vagrant halt`        -- stops the vagrant machine
- `vagrant suspend`     -- suspends a virtual machine (remembers state)

# Cleaning Up a VM
- `vagrant destroy`     -- stops and deletes all traces of the vagrant machine
- `vagrant destroy -f`   -- same as above, without confirmation

- `Vagrant Status` -- Status of the current machine. 

More Info: [Cheat Sheet](https://gist.github.com/wpscholar/a49594e2e2b918f4d0c4#file-vagrant-cheat-sheet-md)
