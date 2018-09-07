# OpenVPN Firewall Rules

Source: https://wiki.archlinux.org/index.php/OpenVPN

```
# Default Policies
ufw default deny incoming
ufw default deny outgoing

# Openvpn Interface
ufw allow in on tun0
ufw allow out on tun0

# Local Network
ufw allow in on ens160 from 192.168.1.0/24
ufw allow out on ens160 to 192.168.1.0/24

# OpenVPN
ufw allow out on ens160 to any port 443
ufw allow in on ens160 from any port 443
```

# Useful UFW commands

```
ufw disable
ufw enable
ufw reset
ufw status
ufw status verbose
ufw status numbered
```
