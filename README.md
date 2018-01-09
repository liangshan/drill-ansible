Drill ansible
=============

Ansible playbook which deploy pptpd, shadowsocksr(aka SSR) on Ubuntu 14.04 and 16.04.

## Prepare

+ ansible > 1.8

## NOTICE

This will disable password login after executed, please make sure the cloud can deploy your ssh key automatically when create a new server.

## Usage

Change the IP address in `hosts` which want to deploy, then just run with your real username and password.

The following is an example:

	$ ansible-playbook -i hosts site.yml --extra-vars '{"hosts":"DO-SG","username":"yourusername","password":"yourpassword"}'

And [here](https://opensourcehacker.com/2015/04/12/almost-free-netflix-vpn-on-amazon-ec2-set-up-in-30-minutes-using-ansible/) is an article about how to use this playbook with EC2. 

## configure PPTP client

Now you have a PPTP server, use them with a powerful combination.

Mac, for example, after connected to your PPTP VPN, HTTP proxy is available at `192.168.23.1:3128`, just set the browser proxy (usually managed by a browser plugin) to it.

## SSR client for Mac

https://github.com/qinyuhang/ShadowsocksX-NG-R/releases

## Earn $10 on DigitalOcean

DigitalOcean is awesome. If this repo is helpful to you, just click [here](https://www.digitalocean.com/?refcode=c07abab931c2) to create your first VPS and earn $10 with my discount code.
