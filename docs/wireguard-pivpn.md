# Remote access: WireGuard via PiVPN

WireGuard gives me secure access to my home LAN from anywhere. It is installed on the application host with [PiVPN](https://www.pivpn.io/), not in Docker.

## How it works

- A DuckDNS hostname follows my home IP (updated by a cron job every 5 minutes).
- The router forwards one UDP port to the application host.
- Each device (phone, laptop) has its own WireGuard profile created with PiVPN.
- Once connected, I can reach LAN services and use Pi-hole for DNS.

## Managing clients

    pivpn add        # create a client profile
    pivpn -qr        # show a QR code to scan with the WireGuard mobile app
    pivpn list       # list clients
    pivpn remove     # revoke a client

## Security notes

- One profile per device, so a lost device can be revoked without affecting the others.
- Only the WireGuard UDP port is forwarded; everything else stays internal.
- Client configs and keys are never committed (`wg*.conf` is git-ignored).

## Not the same as the `vpn` stack

The [`vpn` stack](../stacks/vpn/) is a separate VPN client (Private Internet Access) that routes torrent traffic. It has nothing to do with remote access.
