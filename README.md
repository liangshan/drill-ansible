Drill ansible
=============

Ansible playbook which deploy a drill on Ubuntu 14.04 only.

## Prepare
+ ansible 1.8

## Usage

Change the IP address in `hosts` which want to deploy, then just run the following:

	$ ansible-playbook -i hosts site.yml --extra-vars "hosts=DO-SGP user=liangshan password=123456"
