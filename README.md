# Homelab
Ansible playbook to terraform and configure some apps on my homelab.

## Roles
```
bitwarden    > password manager
caddy        > webserver, reverse proxy, ssl termination, with automatic tls
docker       > container management tool
firewalld    > firewall management tool
grafana      > analytics and graph composer
nextcloud    > file hosting service
minecraft    > sandbox game server
pihole       > DNS sinkhole for adblocking
plex         > media server
prometheus   > monitoring system
swap         > add some swap
tautulli     > monitoring and tracking tool for plex
watchtower   > automated docker container base image updates

# Deprecating...
letsencrypt  > open certificate authority
nginx        > webserver, reverse proxy, ssl termination (with Let's Encrypt)
```

## Usage
Edit the services you want in `site.yml`.
Modify the default variables as desired.
Change the `hosts` file to include the server.
Run the ansible playbook to terraform and configure the server!
```
ansible-playbook site.yml
```

You can also run the playbook on an arbitrary server without specifying it in the `hosts` file.
```
ansible-playbook -i user@server, site.yml
```
