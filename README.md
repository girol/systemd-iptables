# iptables/ip6tables systemd configuration

Example of a persistent firewall based on systemd for Debian Jessie.

Based on some forks over the internet and the original author

### Install Steps

```sh
cp -r etc/firewall /etc/firewall
cp -r etc/systemd/system/firewall.service /etc/systemd/system/
cp -r etc/systemd/system/ip6firewall.service /etc/systemd/system/

# Loads the new service files
systemctl daemon-reload

# Enables the service in startup
systemctl enable firewall.service
systemctl enable ip6firewall.service

# Starts the service
systemctl start firewall.service
systemctl start ip6firewall.service
```

