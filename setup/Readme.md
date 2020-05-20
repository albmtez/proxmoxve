# Proxmox VE hosts setup for deploying infrastructure with Ansible

## Short version

Add hostnames and/or ip addresses of all nodes in `nodes` file.

Execute: `ansible-playbook -i nodes --ask-pass setup.yml`

## Configuration description

In order to use `proxmox` and `proxmox_kvm` ansible plugins we have to make a basic configuration in Proxmox VE hosts.

The following system pip packages are installed:

```text
python-apt
python-pip
python-dev
build-essential
```

Proxmox packages repository switched to community repo: `http://download.proxmox.com/debian/pve buster pve-no-subscription`

All packages are updated to their latest version.

Finally, we pip install the needed dependencies:

```text
virtualven
proxmoxer
```
