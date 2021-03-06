# Vagrant and Virtual Box 101

This repo setup a simple ubuntu machine.


## What is Vagrant?

Allows us to manage and provision Virtual Machines.

It also allows us to pull images of VM from it's marketplace.

## What is Virtual Box?

Is the SW that does the heavy lifting of creating said machines.


## Find out basic Vagrant commands

`vagrant init` - Creates the vagrant file.

`vagrant up` - Downloads the VM and starts it via VirtualBox

`vagrant halt` - Stops the vagrant file

`vagrant destroy` - Destroys the vagrant file

`vagrant ssh` - start using vagrant from terminal

`vagrant reload` - reloads vagrant whilst keeping the files


## Create a ubuntu 18.04 server
using vagrant open the vagrant file and input
```ruby
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/bionic64"

end
```
To configure an internal IP add:
```ruby
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/bionic64"
  config.vm.network "private_network", ip:'192.168.10.100'


end
```
## Installing package manager.

- `sudo apt-get update`
- `sudo apt-get install nginx`

### to check if nginx is installed use
`sudo systemctl start nginx`


`ps aux | grep nginx`
