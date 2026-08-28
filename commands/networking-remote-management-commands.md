# Networking & Remote Management

> **Section:** 14  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `ifconfig` | Configure network interfaces. | Source | Legacy; prefer ip. |
| `ip addr` | Show IP addresses. | Source |  |
| `ip link` | Show or manipulate network interfaces. | Source |  |
| `ip route` | Show or manipulate routing tables. | Source |  |
| `ss` | Display socket statistics. | Source |  |
| `nmap` | Network exploration and security-auditing tool. | Source |  |
| `telnet HOST PORT` | Connect using TELNET. | Source | Plain telnet is insecure; commonly used only for simple connectivity tests. |
| `nc -l -p 1234` | Listen on TCP port 1234 using netcat. | Source |  |
| `nc HOST PORT` | Connect to a host and port using netcat. | Source |  |
| `iptables` | Administer legacy IPv4 packet filtering and NAT rules. | Source |  |
| `firewalld` | Firewall management service used by several RPM-based distributions. | Source |  |
| `ufw enable` | Enable UFW firewall. | Source |  |
| `ufw allow PORT` | Allow traffic to a port using UFW. | Source |  |
| `tcpdump` | Capture and analyze packets from the command line. | Source |  |
| `curl` | Transfer data using HTTP and other protocols. | Source |  |
| `wget` | Download content over HTTP/HTTPS/FTP. | Source |  |
| `scp FILE USER@HOST:/PATH/` | Copy a file to a remote server over SSH. | Source |  |
| `rsync -avz LOCAL/ HOST:/REMOTE/` | Synchronize directories to a remote host. | Source |  |
| `ssh -i KEY USER@HOST` | Connect using a specific SSH private key. | Added |  |
| `ssh -J BASTION TARGET` | Connect to a target through a jump host. | Added |  |
| `ssh -L 8080:REMOTE:80 USER@HOST` | Create a local SSH port forward. | Added |  |
| `sftp USER@HOST` | Open an interactive secure file-transfer session. | Added |  |
| `rsync -a --info=progress2 -e ssh SOURCE/ USER@HOST:/DEST/` | Synchronize with aggregate progress over SSH. | Added |  |
| `nft list ruleset` | Display nftables firewall rules. | Added |  |
| `firewall-cmd --list-all` | Show firewalld configuration for the active zone. | Added |  |
| `ufw status verbose` | Show UFW rules and status. | Added |  |
| `tcpdump -i any port 443` | Capture traffic to/from TCP/UDP port 443 on all interfaces. | Added |  |
| `openssl s_client -connect HOST:443 -servername HOST` | Inspect a TLS connection and certificate chain. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
