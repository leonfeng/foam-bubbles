# WSL Troubleshooting

## WSL2 and WireGuard : WireGuard

Clipped from: https://www.reddit.com/r/WireGuard/comments/rp48lr/wsl2_and_wireguard/

> Maybe dns problem, try vpn and change the dns setting in wsl in /etc/resolv.conf, add nameserver 8.8.8.8 to the end. This change is not persist though. Change /etc/wsl.conf or creat that file, fill with in the end

```ini
[network]
generateResolvConf = false
```
