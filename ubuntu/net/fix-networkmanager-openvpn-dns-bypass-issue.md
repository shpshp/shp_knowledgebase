fix-networkmanager-openvpn-dns-bypass-issue
===========================================

Add two lines of configuration into the *client* openvpn config file:
```bash
#script-security 2
up /etc/openvpn/update-resolv-conf
down /etc/openvpn/update-resolv-conf
```

Also ensure the resolvconf packega is installed on the client because update-resolv-conf script depends on it.

Update: not working???

Next try:

```bash
dhcp-option DNS 77.88.8.8
block-outside-dns
#redirect-gateway
```
