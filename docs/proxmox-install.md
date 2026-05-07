Proxmox Install Notes

Date: 07.05.2025

Before installing

Documentation: Proxmox Wiki



Hardware: Dell Optiplex 3080 SFF



16GB RAM



256GB M.2 SSD



1TB HDD



Plan: SSD for the OS and VMs (speed). HDD for ISOs and backups (space).



Decisions made

Repo Swap: Deleted the enterprise repo and added the "no-subscription" one.



Why: To get updates without a paid license.



HDD Setup: Formatted as a Directory with Ext4.



Why: Keeping it simple. ZFS uses too much RAM, and 16GB needs to be saved for the actual VMs.



SSH Keys: Generated an Ed25519 key on my PC and pasted it into Proxmox.



Why: Typing passwords every time I want to manage the host is slow and less secure.



Questions I have

Storage: If I wipe the SSD later, how do I tell a new Proxmox install that the HDD already has my files on it?



Networking: How does the single Ethernet port on the Dell handle multiple VMs having their own IP addresses?



Problems and fixes

Problem: ssh-copy-id doesn't work on Windows.



Fix: Used mkdir -p \~/.ssh on the host, then used nano to paste my public key into \~/.ssh/authorized\_keys.



Problem: Permissions on the SSH files.



Fix: Ran chmod 700 on the folder and chmod 600 on the file so the SSH service wouldn't reject the key for being "too open."

