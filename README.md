This is a kernel module for block device called MyDisk which allocates 512KB Of space in the memory and simulate that as a separate block device and partition into 3 Primary and 3 logical partitions.

Block driver can read and write into this virtual disk.

Procedure :

> Download the repository from github
> In the command line opened from the directory containing these files, type make all
> This should generate .ko files
> push the module to kernel using command sudo insmod main.ko
> To write into the device, goto the root mode and type this command $ cat > /dev/mydisk4
> To read the data present in the device, type this command $ xxd /dev/mydisk4
> To see the partitions type $ sudo fdisk -l


