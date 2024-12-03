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

## Get Addresses
Net-tools has a cli app called `ip`. With it you can get addresses such as ip, mac addresses, ipv6 addresses. To get these type.
```bash
sudo ip a
```
Here a is short for address.`
