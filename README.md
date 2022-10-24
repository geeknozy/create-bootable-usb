# create-bootable-usb
This is how you can create a bootable USB on Linux operating systems to boot Linux Operating systems<br>

## Note: The Data on USB will be completely lost!<br>

Step 1: Format the USB completely with the help of disk utility like Gparted or Gnome-Disk-utility and do not create any partition on the disk. 

Step 2: Open terminal and get into sudo user mode and type.<br>
```
sudo su
```
<br>       
Step 3: type 
```
lsblk
```
<br>
Step 4: Now check and make note of which disk is your USB, eg: ```/dev/sdX``` where X might be a,b,c etc.<br>

Step 5: go to the folder where the ISO image is present on terminal<br>

Step 6: now type
```
dd bs=4M if=image-name.iso of=/dev/sdX conv=fsync oflag=direct status=progress
```
<br>
Note: <br>
1. here image-name.iso is name of the iso in the folder which you want to burn to the USB.<br>
2. /dev/sdX, here X is the device mount point of USB from step 4.<br>
        
Wait till the progress is completed and you get the temrinal prompt.<br>
