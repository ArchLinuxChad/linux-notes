# My Notes on Net-Tools

## Installing it
Most Distros will already have it installed but if you don't the command is
```bash
# for ubuntu & debian
sudo apt update && sudo apt upgrade -y
sudo apt install net-tools -y

# fedora & RHEL based Distros
sudo dnf upgrade -y
sudo dnf install net-tools -y

# For Arch Linux
sudo pacman -Syu net-tools
```

## Note
For these commands I have to use sudo because I use the fish shell. But if you use another shell you can ignore the sudo command.
## Get Addresses
Net-tools has a cli app called `ip`. With it you can get addresses such as ip, mac addresses, ipv6 addresses. To get these type.
```bash
sudo ip a
```
Here `a` is short for `address`.

## Get Routes 
To see all of your routes type.
```bash
sudo ip r
```

## Get Neighbours
To get your arp(Address solution Protocol) type.
```
sudo ip n
```

## Using NMCLI
`nmcli` is another net-tools cli program.

## General
to get a general connectivity and status of your network interface type.
```bash
nmcli g
```
`g` is short for `general`.

## Connection
To see all of your connections type.
```bash
nmcli c
```

## Other commands
There are lots of other options. You can check these out with the command.
```bash
nmcli --help
```

## Network Manager config file
`nmcli` stands for `Network Manager Command Line Interface`
you can also make some configurations through the config file which is located at `/etc/NetworkManager/NetworkManager.conf`. There also other config files at `/etc/NetworkManager/`.
