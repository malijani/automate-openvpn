This repo contains some openvpn profiles which created by Chauffeur with love.

**Use prepared script to use this profiles**

*via curl :* 
 
`sh -c "$(curl -fsSL https://raw.githubusercontent.com/virtualdemon/chauffeur-vpn/master/initialize)"`

*via wget :*

`sh -c "$(wget  https://raw.githubusercontent.com/virtualdemon/chauffeur-vpn/master/initialize -O - )"`

**Usage :**

just run : `sudo $HOME/OpenVPN/start.exp`

by default US.ovpn profile is in use. you can comment US.ovpn and uncomment DE.ovpn in $HOME/OpenVPN/start.exp file to use DE.ovpn.
