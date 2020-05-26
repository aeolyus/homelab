# Homelab
Ansible playbook to terraform and configure some apps on my homelab.

## Roles
```
bitwarden    > password manager
caddy        > webserver, reverse proxy, ssl termination, with automatic tls
docker       > container management tool
firewalld    > firewall management tool
grafana      > analytics and graph composer
letsencrypt  > open certificate authority
pihole       > DNS sinkhole for adblocking
prometheus   > monitoring system
ssh          > convert ssh port 22 -> 222
swap         > add some swap
watchtower   > automated docker container base image updates

# Deprecating...
letsencrypt  > open certificate authority
nginx        > webserver, reverse proxy, ssl termination (with Let's Encrypt)
```
