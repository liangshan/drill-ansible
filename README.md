Drill ansible
=============

Ansible playbook which deploy pptpd and squid on Ubuntu 14.04 only.

## Prepare
+ ansible 1.8

## Usage

Change the IP address in `hosts` which want to deploy, then just run the following:

	$ ansible-playbook -i hosts site.yml --extra-vars '{"hosts":"DO-SGP","username":"yourusername","password":"123456"}'
