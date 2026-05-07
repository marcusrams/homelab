# Proxmox Install Notes
 
**Date:** 07.05.2025
 
---
 
## Before installing
 
**Documentation:** [Proxmox Wiki](https://pve.proxmox.com/wiki/Installation)
 
**Hardware**
 
| Component | Spec |
|-----------|------|
| Machine | Dell Optiplex 3080 SFF |
| RAM | 16GB |
| Storage A | 256GB M.2 SSD |
| Storage B | 1TB HDD |
 
**Plan:** SSD for the OS and VMs (speed). HDD for ISOs and backups (space).
 
---
 
## Decisions made
 
**Repo swap**
Deleted the enterprise repo and added the no-subscription one.
> To get updates without a paid license.
 
**HDD setup**
Formatted as a Directory with Ext4.
> Keeping it simple. ZFS uses too much RAM and 16GB needs to be saved for the actual VMs.
 
**SSH keys**
Generated an Ed25519 key on my PC and pasted it into Proxmox.
> Typing passwords every time I want to manage the host is slow and less secure.
 
---
 
## Questions
 
- **Storage:** If I wipe the SSD later, how do I tell a new Proxmox install that the HDD already has my files on it?
- **Networking:** How does the single Ethernet port on the Dell handle multiple VMs having their own IP addresses?
---
 
## Problems and fixes
 
**Problem:** `ssh-copy-id` doesn't work on Windows.
**Fix:** Used `mkdir -p ~/.ssh` on the host, then used `nano` to paste the public key into `~/.ssh/authorized_keys`.
 
---
 
**Problem:** Permissions on the SSH files were too open.
**Fix:** Ran `chmod 700` on the folder and `chmod 600` on the file so the SSH service would accept the key.
