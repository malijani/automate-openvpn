This repository contains some openvpn profiles which created by Chauffeur with love.

**Use prepared script to use this profiles!**

*via curl :* 
 
`sh -c "$(curl -fsSL https://raw.githubusercontent.com/virtualdemon/chauffeur-vpn/master/initialize)"`

*via wget :*

`sh -c "$(wget  https://raw.githubusercontent.com/virtualdemon/chauffeur-vpn/master/initialize -O - )"`

**Usage :**

Just run : `sudo $HOME/OpenVPN/start.exp`

By default US.ovpn profile is in use. You can comment US.ovpn and uncomment DE.ovpn in "*$HOME/OpenVPN/start.exp*" file to use DE.ovpn.

**Telegram channel : [@ipctux](https://t.me/ipctux)**

## common problems!?

> dns problem

In case you may have dns problem(you can't open censored sites)! you should check systemd-resolved service , NetworkManager configuration and resolv.conf to fix the problem! for temporary dns change you can use this command : 

`sudo bash -c 'echo -e "nameserver 1.1.1.1\nnameserver 1.0.0.1" > /etc/resolv.conf'`

for fixing this problem permanently  do follow these instructions : 

 1. disable 'systemd-resolved' service (you doin' it wrong systemd :D ) : 
	`sudo systemctl stop systemd-resolved`
	`sudo systemctl disable systemd-resolved`
	
 2. add 'dns=none' in /etc/NetworkManager/NetworkManager.conf under [main] section :
	`sudo nano /etc/NetworkManager/NetworkManager.conf`
	**[main]
	      dns=none**
	      
 3. add your dns to /etc/resolv.conf :
	`sudo nano /etc/resolv.conf`
	**nameserver 1.1.1.1
	      nameserver 1.0.0.1**
 
 4. restart NetworkManager service :  	      
	*debian based distros :*
	`sudo systemctl restart network-manager`
	*other distros :*
	`sudo systemctl restart NetworkManager`
	
if you want script to do this just tell me :) 

