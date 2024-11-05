# My Notes on selinux

# Basic Commands

## set the status of selinux
``` bash
sestatus
```

## See the mode that it is in
```bash
getenforce
```

## set the mode
To set to enforcing
```bash
sudo setenforce Enforcing
```
To set to permissive
```bash
sudo setenforce Permissive
```
This will not perssist so if you want selinux to stay in a mode even after reboot you need to set it in the config file.
This is file is located at `/etc/selinux/config`.
