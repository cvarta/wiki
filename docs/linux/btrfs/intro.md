# Butter FS Introduction
Btrfs is a modern copy on write (CoW) filesystem for Linux aimed at implementing advanced features while also focusing on fault tolerance, repair and easy administration. Jointly developed at multiple companies, Btrfs is licensed under the GPL and open for contribution from anyone. Not too many companies have said that they are using Btrfs in production, but we welcome those who can say so on the production users page.

# Why use Btrfs
BtrFS filesystem in Linux provides the following Features and Capabilities

* Built-in copy on write
* Powerful snapshot capabilities
* Built-in volume management with subvolumes
* Massive Scalability upto 16 Exabytes
* Built-in data integrity (checksums)
* SSD optimization
* Compression capabilities
* RAID built in BtrFS
* Manual defragmentation
* Online filesystem management
* Data and metadata integrity
* In-place conversion from ext2/3/4 and ReiserFS
* Quota groups
* Online expansion and reduction of filesystem size
* Object level RAID
* Seeding devices
* Support for multiple devices

# Installation
## Check Kernel Support
Btrfs filesystem has been integrated into the kernel. To check currently supported filesystems by the kernel

```shell
# cat /proc/filesystems 
nodev   sysfs
nodev   rootfs
..............
   btrfs
   ext3
   ext2
   ext4
   vfat
   xfs
   fuseblk
nodev   fuse
nodev   fusectl
```
## Install Btrfs Userspace Utilities
In order to create / format btrfs volumes the `btrfs-progs` needs to be installed. On Ubuntu 20.04 LTS: Open Terminal
```shell
sudo apt install btrfs-progs
```
