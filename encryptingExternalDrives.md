# My Notes For Encrypting External Drives

## Wipe current data on drive
```bash
sudo dd if=/dev/zero of=/dev/sda
```
My drive is at `/dev/sda` but if your is somewhere else you need to change the path after `of=` on the `dd` command.

## Encrypt Drive with LUKS
```bash
sudo cryptsetup luksFormat /dev/sda
```
Again you might need to change the path of the drive.

## Now put a file system on the drive
```bash
sudo mkfs.exfat -L <name for drive> /dev/sda
```

## To Mount
### Decrypt the Drive
```bash
sudo cryptsetup open /dev/sda vault
```
Here I am decrypting drive `/dev/sda` to location `/dev/mapper/vault`

### Mount it
```bash
sudo mount /dev/mapper/vault <path>
```
