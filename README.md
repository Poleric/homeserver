Homeserver
==========

#### A collection of the services I used for my homeserver.

Repo holds the Ansible configuration for deploying and running the services.

## Services used

All of the services are dockerized.

- [x] [Pi-hole](https://pi-hole.net/) - Ad blocking and custom DNS
- [x] [Samba](https://www.samba.org/) - File sharing
- [x] [ddclient](https://ddclient.net/) - IP updates
- [x] [Caddy](https://caddyserver.com/) - Reverse proxy
- [ ] [Deluge](https://deluge-torrent.org/) - BitTorrent client
- [ ] [Jackett](https://github.com/Jackett/Jackett) - Torrent trackers browser
- [ ] [Jellyfin](https://jellyfin.org/) - Media server
- [ ] [Vaultwarden](https://github.com/dani-garcia/vaultwarden) - Password manager
- [ ] [Homer](https://github.com/bastienwirtz/homer) - Home server homepage

## Setup

1. Install Ansible.
   ```bash
   pip install ansible
   ```
2. Install requirements.
   ```bash
   ansible-galaxy install -r requirements.yml
   ```
3. Configure the variables in `./group_vars/all` and `./inventory/production.yml`.
   > Read [group_vars/README.md](group_vars/README.md) and [inventory/README.md](inventory/README.md) for documentation
   on the usage and description of each of the variables.
4. Run the playbook.
   ```bash
   ansible-playbook main.yml -i inventory/production.yml
   ```
