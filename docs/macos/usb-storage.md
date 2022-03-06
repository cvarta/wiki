# Hidden Fork Files on Mass Storage Devices 
The resource fork is a fork or section of a file on Apple's classic Mac OS operating system, which was also carried over to the modern macOS for compatibility. It's used to store structured data along with the unstructured data stored within the data fork.

On Mac file systems (i.e., MFS, HFS, and HFS+), the actual data file and its resource fork are seen as one file. Copying a Mac file to other volumes can cause the data and the resource fork to be split into different files.

For just a particular mounted volume - like a flash drive called yourUSBstick, the following example - will remove existing cruft, stop Spotlight indexing now and in the future, stop the related fsevents logging, and disable the Trash feature.

```shell
mdutil -i off /Volumes/yourUSBstick
cd /Volumes/yourUSBstick
rm -rf .{,_.}{fseventsd,Spotlight-V*,Trashes}
mkdir .fseventsd
touch .fseventsd/no_log .metadata_never_index .Trashes
cd -
```
