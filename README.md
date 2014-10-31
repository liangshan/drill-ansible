Drill ansible
=============

Ansible playbook which deploy pptpd and squid on Ubuntu 14.04 only.

## Prepare
+ ansible 1.8

## Usage

Change the IP address in `hosts` which want to deploy, then just run with your real username and password.

The following is an example:

	$ ansible-playbook -i hosts site.yml --extra-vars '{"hosts":"DO-SGP","username":"yourusername","password":"yourpassword"}'

