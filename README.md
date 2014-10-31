Drill ansible
=============

Ansible playbook which deploy pptpd and squid on Ubuntu 14.04 only.

## Prepare
+ ansible 1.8

## Usage

Change the IP address in `hosts` which want to deploy, then just run with your real username and password.

The following is an example:

	$ ansible-playbook -i hosts site.yml --extra-vars '{"hosts":"DO-SGP","username":"yourusername","password":"yourpassword"}'

## configure your Mac or iPhone

Now you have an PPTP server and a http proxy (squid), use them with a powerful combination.

Mac, for example, after connected to your PPTP VPN, http proxy is available at `192.168.23.1:3128`, just set the browser proxy (usually managed by a browser plugin) to it.

Configuring iPhone is quite similar to Mac, setup PPTP VPN and also a http proxy at the same time.

