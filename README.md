# Analysis-of-the-Disk-Structure-using-Sleuth-Kit
## AIM:
To analyze the disk structure of a given disk image using Sleuth Kit tools in Kali Linux.

## DESIGN STEPS:
### Step 1:
Obtain or create a disk image file (e.g., disk.dd) to analyze. Open the terminal in Kali Linux.

### Step 2:
Use Sleuth Kit tools like mmls, fsstat, and fls to examine the partition layout, file system details, and file listing.

### Step 3:
Interpret the output of the tools to understand the disk structure, including partitions, sectors, and files.

## PROGRAM:
Sleuth Kit Disk Analysis Commands

✅ Option 1: Create a Sample Disk Image (for Testing)

Let’s create a 10MB blank disk image and simulate file system activity:

```bash
cd ~/Downloads

# Step 1: Create an empty disk image
dd if=/dev/zero of=disk.dd bs=1M count=10

# Step 2: Format it with a file system (like FAT32)
mkfs.vfat disk.dd
```

## OUTPUT:

<img width="400" alt="image" src=https://github.com/user-attachments/assets/4f545328-b501-4ddb-ab2c-ffe82b8d945c>

### Create Disk
<img width="400" alt="image" src=https://github.com/user-attachments/assets/24be8486-72b4-401b-8354-d3d56586e66b>

### mmls 
```bash
mmls disk.dd
```
### fls
```bash
fls -f fat -o 0 disk.dd
```
<img width="350" alt="image" src=https://github.com/user-attachments/assets/8b2fcd71-e995-4f69-9b62-8026bc46d749>


<img width="350" alt="image" src=https://github.com/user-attachments/assets/f4767f8a-2a5a-4764-8c63-4f548f416c32>


<img width="350" alt="image" src=https://github.com/user-attachments/assets/d0ffa9f1-d2a6-4900-be5c-e7a5edd2d535>


## RESULT:
The analysis was performed successfully using Sleuth Kit, and the disk structure was understood in detail.
