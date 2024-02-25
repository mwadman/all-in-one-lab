# Overview



# Prerequisites

- [libvirt](https://wiki.archlinux.org/title/libvirt)
- [Vagrant](https://developer.hashicorp.com/vagrant/docs/installation)
- [vagrant-libvirt](https://vagrant-libvirt.github.io/vagrant-libvirt/)

# Environment Creation

## Vagrant Up

```bash
vagrant up
```

## Ansible Setup and Run

```bash
python3 -m venv venv # Create virtual environment if it doesn't already exist
source venv/bin/activate
pip3 install -r requirements.txt
ansible-galaxy install -r requirements.yml
ansible-playbook playbooks/all-in-one.yml -D
```
