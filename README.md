WireGuard Auto-Script Installer
Easily set up a dual-stack WireGuard VPN on a Linux server. See the issues for the WIP.

Requirements
Supported distributions:
Ubuntu 18.04 LTS
Debian 9
Fedora
CentOS 7
Arch Linux
I recommend these cheap cloud providers for your VPN server:
Vultr: Worldwide locations, IPv6 support,
PulseHeberg: France, unlimited bandwidth,
Digital Ocean: Worldwide locations, IPv6 support,


How to install :

1. Create a fresh VPS server then login the credentials using Bitvise --> CLICK HERE TO DOWNLOAD <---
2. Then just run the script bellow and reboot the vps afer installation.
Command link bellow
https://www.phcracker.net/threads/8335/

3. Run the script to create a config
Then run it :
./wireguard-install.sh
4. Copy the file /root/client-wg0.conf from a remote server to your local PC path /etc/wireguard/wg0.conf and run sudo systemctl start wg-quick@wg0.service

To show VPN status, run sudo wg show.

Options
The script can be configured by setting the following environment variables:

INTERACTIVE - if set to "no", the script will not prompt for user input
PRIVATE_SUBNET - private subnet configuration, "10.9.0.0/24" by default
SERVER_HOST - public IP address, detected by default
SERVER_PORT - listening port, picked random by default
CLIENT_DNS - comma separated DNS servers to use by the client


Credits
Inspired by Nyr's openvpn-install.
Reply
Select for moderation
