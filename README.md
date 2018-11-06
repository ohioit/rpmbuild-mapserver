# MapServer RPM Build

MapServer is an Open Source platform for publishing spatial data and interactive mapping applications to the web.
There are not a lot of readily available and regularly updated RPM packages currently available. The sole purpose
of this repo is to facilitate the creation and maintenace of MapServer RPMs.

## Requirements

- Vagrant <https://www.vagrantup.com/>
- VirtualBox <https://www.virtualbox.org/>
- Ansible <https://www.ansible.com/>

## Vagrant/Ansible Usage

```shell
git clone https://github.com/ohioit/rpmbuild-mapserver.git mapserver
cd mapserver
cp vars.yml local.yml
# Modify local.yml as needed, i.e. MapServer CMake Options
vagrant up
```

If everything works properly you should end up with a freshly cut RPM in the 'out' directory.
You can simply run `vagrant destroy -f` at this point if you like. All you need is the new
RPM file which can be distributed to your servers.
