# Static IP Ubuntu <= 16.04

### /etc/network/interfaces
```
# This file describes the network interfaces available on your system
# and how to activate them. For more information, see interfaces(5).

source /etc/network/interfaces.d/*

# The loopback network interface
auto lo
iface lo inet loopback

# The primary network interface
auto ens160
iface ens160 inet static
address 192.168.1.xx
netmask 255.255.255.0
gateway 192.168.1.1
dns-nameservers xxx.xxx.xxx.xxx xxx.xxx.xxx.xxx
```

# Static IP Ubuntu >= 18.04

### (ToDo - Netplan)

# Enable Repository Updating (Plex & UniFi Controller)

### Plex
https://support.plex.tv/articles/235974187-enable-repository-updating-for-supported-linux-server-distributions/
* plexmediaserver

### UniFi Controller
https://help.ubnt.com/hc/en-us/articles/220066768-UniFi-How-to-Install-Update-via-APT-on-Debian-or-Ubuntu
* Packages
  * openjdk-8-jre-headless
    * required prior to unifi, otherwise an incompatible version will be installed as a dependency
  * unifi

# Generally Required Server Packages
* cifs-utils
  * Common Internet File System utilities
* openssh

# Desktop Packages
* openvpn
* chromium-browser
* iftop
* htop
* open-vm-tools-desktop
