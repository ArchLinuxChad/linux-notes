# My Notes On LVM
## LVM
`LVM` stands for `Logical Volume Management`

## Physical Volumes
To initialize a drive as a `physical volume` we use the `pvcreate` command. For example if you have the drive `/dev/sdX` you could use the command.
```bash
sudo pvcreate /dev/sdX
```
You can view your physical volumes with
```bash
sudo pvdisplay
```
You also might to resize physical volume after resizing a partition, this can be done with the `pvresize`.
```bash
sudo pvresize /dev/sdX
```
