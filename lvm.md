# My Notes On LVM
## LVM
`LVM` stands for `Logical Volume Management`

## Physical Volumes
To initialize a drive as a `physical volume` we use the `pvcreate` command. For example if you have the drive `/dev/sdX` you could use the command.
```bash
sudo pvcreate /dev/sdX
```
You can view your physical volumes and info about them with
```bash
sudo pvdisplay
```
You can view your physical volumes with
```bash
pvs
```
You also might to resize physical volume after resizing a partition, this can be done with the `pvresize`.
```bash
sudo pvresize /dev/sdX
```

## Volume Groups
To create a volume group use the command
```bash
sudo vgcreate bucket /dev/sdX /dev/example
```
Here I am calling the volume group `bucket`. And I am using some physical volumes to create it.

You can view and see info about you `Volume Groups` with the command
```bash
sudo vgdisplay
```

You can also view them with
```bash
sudo vgs
```

To remove a volume group, you can use the command
```bash
sudo vgremove bucket
```

## Logical Volumes

To create a `Logical Volume` use the command.
```bash
sudo lvcreate -L 15G -n bit bucket
```
