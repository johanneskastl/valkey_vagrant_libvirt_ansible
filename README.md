# valkey_vagrant_libvirt_ansible

This Vagrant setup creates a VM and installs
[Valkey](https://github.com/valkey-io/valkey) on it.

It configures a `vagrant-libvirt` instance of Valkey and starts it up.

Default OS is openSUSE Tumbleweed. Although that can be changed in the
Vagrantfile, please beware that this will break the Ansible provisioning.

## Vagrant

1. You need vagrant obviously. And ansible. And git...
1. Fetch the box, per default this is `opensuse/Tumbleweed.x86_64`, using
   `vagrant box add opensuse/Tumbleweed.x86_64`.
1. Make sure the git submodules are fully working by issuing `git submodule init
   && git submodule update`
1. Run `vagrant up`
1. Run `vagrant ssh` to log into the VM.
1. Run `sudo systemctl status valkey@vagrant-libvirt` to check the service's
   status.
1. Run `sudo valkey-cli ping` and you should get a `PONG` back.
1. Party!

## Cleaning up

The VMs can be torn down after playing around using `vagrant destroy`.

## License

BSD-3-Clause

## Author Information

I am Johannes Kastl, reachable via git@johannes-kastl.de
