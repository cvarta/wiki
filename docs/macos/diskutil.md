# Formatting a Compact Flash Card
Format a Compact Flash drive to the older FAT 16 (required for come older hardware), using Mac OS X and the terminal application.

Open the Terminal, and type `diskutil` list to list the connected devices.

```shell
$ diskutil list
/dev/disk2 (external, physical):
   #:                       TYPE NAME                    SIZE       IDENTIFIER
   0:                            NONAME                 *1.0 GB     disk2   <- this one!
```
Identify the external drive, and use its 'device identifier' in the following command:
`diskutil partitiondisk /dev/disk2 1 MBR "MS-DOS FAT16" "NONAME" 0B`

**The arguments are as follows:**

| Argument     | Description |
|--------------|-------------|
| /dev/disk2   | disk device to be partitioned, found with 'diskutil list' |
| 1            | number of partitions, optional, but if given must match  |
| MBR          | partition Scheme (eg, DOS=MBR, Unix=GPT)                 |
| MS-DOS FAT16 | partition type (or fat32                                 |
| NONAME       | partition name                                           |
| 0B           | partition size (0B=maximum)                              |


CAUTION! This procedure refers to disk2, but your device identifier can be different. Check it first!



**For example:**
```shell
$ diskutil partitionDisk /dev/disk2 MBR "MS-DOS FAT16" "NONAME" 0B
Started partitioning on disk2
Unmounting disk
Creating the partition map
Waiting for partitions to activate
Formatting disk2s1 as MS-DOS (FAT16) with name NONAME
512 bytes per physical sector
/dev/rdisk2s1: 994304 sectors in 62144 FAT16 clusters (8192 bytes/cluster)
bps=512 spc=16 res=1 nft=2 rde=512 mid=0xf8 spf=243 spt=32 hds=54 hid=63 drv=0x80 bsec=994833
Mounting disk
Finished partitioning on disk2
/dev/disk2 (external, physical):
   #:                       TYPE NAME                    SIZE       IDENTIFIER
   0:     FDisk_partition_scheme                        *509.4 MB   disk2
   1:                 DOS_FAT_16 NONAME                  509.4 MB   disk2s1
$ diskutil info /dev/disk2s1
```
----
# A specific size:
To create a specific size drive, eg 64 Meg:

### Two partitions, NONAME1 (64meg) and NONAME2 (all remaining space)
`diskutil partitionDisk /dev/disk3 MBR "MS-DOS FAT16" "NONAME1" 64M "MS-DOS FAT16" "NONAME2" 0B`
### One 64meg partition, the remainder as free space (free space still requires a name in quotes)
`diskutil partitionDisk /dev/disk3 MBR "MS-DOS FAT16" NONAME 64M free "" 0B`

Though "MS-DOS FAT16" is shown, change this string to "MS-DOS FAT32" to create a FAT32 partition. 
 - list the supported partition types with the command: `diskutil listFilesystems`

----
# Display the partition scheme
Use diskutil list to display the partition scheme:

```shell
chris$ diskutil list
/dev/disk2 (external, physical):
   #:                       TYPE NAME                    SIZE       IDENTIFIER
   0:     FDisk_partition_scheme                        *509.4 MB   disk2
   1:                 DOS_FAT_16 NONAME                  509.4 MB   disk2s1

```
Disk2 refers to the entire disk, whereas disk2s1 refers to partition 1 on disk 2. The letter 's' means 'slice' (partition).

 
When finished, unmount and remove the disk (or "eject" it in the finder):
```shell
chris $ diskutil unmountdisk disk2
```
Unmount of all volumes on disk2 was successful

----
# Alternate Method
Unmount the disk, and use the following command to reformat the first partition:
```shell
sudo newfs_msdos -F 16 /dev/disk3s1
```
The F option specifies the FAT type, which can be 12, 16, or 32. Type man newfs_msdos for other option details.