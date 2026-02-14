**Day 13 – Linux Volume Management (LVM)**
Learn LVM to manage storage flexibly – create, extend, and mount volumes.

**ask 1: Check Current Storage**
Run 
-lsblk 
-pvs 
-vgs
-lvs 
-df 
-h
<br></br>
<img width="646" height="533" alt="image" src="https://github.com/user-attachments/assets/98769f6a-51ec-4a29-bd6d-d5b5182f75f7" /><br></br>
<br></br>
**Task 2: Create Physical Volume**
<img width="564" height="241" alt="image" src="https://github.com/user-attachments/assets/5da38aea-383d-4742-bb34-d57fdbf90fb4" /><br></br>
<br></br>
**Task 3: Create Volume Group**
<img width="789" height="111" alt="image" src="https://github.com/user-attachments/assets/d31940de-6691-49f6-b036-2a5dcc401876" /><br></br>
<br></br>
**Task 4: Create Logical Volume**
<img width="896" height="117" alt="image" src="https://github.com/user-attachments/assets/ecd22db8-1f4e-4e5b-82c2-b5a98c0d7c36" /><br></br>
<br></br>
**Task 5: Format and Mount**
<img width="781" height="381" alt="image" src="https://github.com/user-attachments/assets/8d2c8b9a-e09f-4481-bc10-2ce84ee4cd55" /><br></br>
<br></br>
**Task 6: Extend the Volume**
<img width="1090" height="270" alt="image" src="https://github.com/user-attachments/assets/dbde9c32-63da-40ee-87fa-5e36193c9da7" /><br></br>
<br></br>
**Task 7: Mounting PV directly**
<img width="816" height="641" alt="image" src="https://github.com/user-attachments/assets/d84fc9f8-f191-4138-86a6-8dc33f826a71" /><br></br>

#**Commands Used**
-lsblk - List block devices and their mount
-df -h - Show mounted filesystem usage
-pvcreate /dev/sdb - Initialize partition as PV
-pvs - List all PVs
-vgcreate vg_name /dev/sdb - Create a VG from PVs
-vgs - List all VGs
-lvcreate -n lv_name -L 5G vg_name - Create LV of 5GB
-lvextend -L +2G /dev/vg_name/lv_name - Extend LV by 2GB
-lvs - List all LVs
-mkfs.ext4 /dev/vg_name/lv_name - Create ext4 filesystem
-mount /dev/vg_name/lv_name /mnt/data - Mount created LV
-resize2fs /dev/vg_name/lv_name - Resize ext2/3/4 filesystem
-mkfs -t ext4 /dev/sdb /mnt/data - Directly mount PV
