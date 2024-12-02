# My Notes of UFW

## Install UFW
```bash
# on ubuntu & debian
sudo apt update && sudo apt upgrade -y
sudo apt install ufw

# on fedora or rhel based distro
sudo dnf upgrade -y
sudo dnf install ufw

# on Arch Linux
sudo pacman -Syu ufw
```

## Set Default Policies
Here are some sensible default polices
```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```
There are some ports you will want to allow before enabling `ufw`
```bash
# for ssh(if you use a different port enable it)
sudo ufw allow 22/tcp
# if it is a server
sudo ufw allow 80,443/tcp
```

## Enable It
```bash
sudo ufw enable

# sometimes you need to enable it as a systemd service also
sudo systemctl enable ufw.service --now
```

## Stop people form pinging your server
To do this you need to configure `ufw` to drop ICMP codes. To do this you can edit the file `/etc/ufw/before.rules`.

You need to change the line
```
-A ufw-before-input -p icmp --icmp-type echo-request -j ACCEPT
```
To
```
-A ufw-before-input -p icmp --icmp-type echo-request -j DROP
```
Then you need to restart your `ufw` with the command
```bash
sudo ufw reload
```
