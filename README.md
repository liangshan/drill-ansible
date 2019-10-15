Drill ansible
=============

Ansible playbook which deploy shadowsocksr(aka SSR) and kcptun on Ubuntu 16.04.

And a proxy service with all the corresponding clients , if you need.

## Prepare

+ ansible > 1.8

## NOTICE

This will disable password login after executed, please make sure the cloud can deploy your ssh key automatically when create a new server.

## Usage

Change the IP address in `hosts` which want to deploy, then just run with your password.

The following is an example:

    $ ansible-playbook -i hosts server.yml --extra-vars '{"hosts":"ALIYUN-SV", "password":"yourpassword"}'

The network woud looks like this now:

![WX20191015-134856](https://user-images.githubusercontent.com/1119114/66803527-6f967980-ef52-11e9-8ad0-eb1f015b6a95.png)

### Optional

If you need a proxy server, which will connect the server for you, just do this:

    $ ansible-playbook -i hosts proxy.yml --extra-vars '{"hosts":"ALIYUN-PROXY", "password":"yourpassword"}'

> NOTICE: same password as first step.

Then you only need to set the system/application's proxy to `PROXY_SERVER:1086` and have fun.

Futher more, if you don't want to make the proxy server go public, just build an OpenVPN server according to the instructions.

+ https://blog.ssdnodes.com/blog/tutorial-installing-openvpn-on-ubuntu-16-04/
+ https://www.digitalocean.com/community/tutorials/how-to-set-up-an-openvpn-server-on-ubuntu-16-04

The network would looks like this finally:

![WechatIMG21512](https://user-images.githubusercontent.com/1119114/66803328-e0896180-ef51-11e9-988b-e4e5759d55cd.png)

## SSR client

+ Mac: https://github.com/qinyuhang/ShadowsocksX-NG-R/releases
+ iOS (available in US market): https://itunes.apple.com/us/app/potatso-lite/id1239860606?mt=8
