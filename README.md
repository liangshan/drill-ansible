Drill ansible
=============

Ansible playbook which deploy shadowsocksr(aka SSR) and kcptun on Ubuntu 16.04.

## Prepare

+ ansible > 1.8

## NOTICE

This will disable password login after executed, please make sure the cloud can deploy your ssh key automatically when create a new server.

## Usage

Change the IP address in `hosts` which want to deploy, then just run with your password.

The following is an example:

	$ ansible-playbook -i hosts site.yml --extra-vars '{"hosts":"DO-SG", "password":"yourpassword"}'

## SSR client

+ Mac: https://github.com/qinyuhang/ShadowsocksX-NG-R/releases
+ iOS (available in US market): https://itunes.apple.com/us/app/potatso-lite/id1239860606?mt=8

## Earn $10 on DigitalOcean

DigitalOcean is awesome. If this repo is helpful to you, just click [here](https://www.digitalocean.com/?refcode=c07abab931c2) to create your first VPS and earn $10 with my discount code.
