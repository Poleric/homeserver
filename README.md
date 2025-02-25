Homeserver
==========

#### A collection of the services I used for my homeserver.

Repo holds the Ansible configuration for deploying and running the services.

## Services used

All of the services are dockerized.

- [Pi-hole](https://pi-hole.net/) - Ad blocking and custom DNS
- [Samba](https://www.samba.org/) - File sharing
- [ddclient](https://ddclient.net/) - IP updates
- [Caddy](https://caddyserver.com/) - Reverse proxy
- [Deluge](https://deluge-torrent.org/) - BitTorrent client
- [Jellyfin](https://jellyfin.org/) - Media server
- [Vaultwarden](https://github.com/dani-garcia/vaultwarden) - Password manager
- [Homepage](https://gethomepage.dev/) - Home server homepage
- [Wireguard + wg-easy](https://github.com/wg-easy/wg-easy) - VPN Server + GUI

## Setup

1. Install Ansible and requirements.
   ```bash
   pip install -r requirements.txt
   ```
   
2. Install requirements.
   ```bash
   ansible-galaxy install -r requirements.yml
   ```
   
3. Configure the variables in `./group_vars/all` and `./inventory`.

   > ~~Read [group_vars/README.md](group_vars/README.md) and [inventory/README.md](inventory/README.md) for documentation
   on the usage and description of each of the variables.~~
   > TODO lol.

4. Run the playbook.
   ```bash
   ansible-playbook main.yml -i inventory/<your_custom_group>/production.yml
   ```
