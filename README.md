# Packer/Azure-Chroot
Based on Packer v1.4.5
Follow command will create a Packer Temp file.

```bash
git clone https://github.com/bedro96/chroot.git
cd chroot
sudo apt install -y unzip
unzip packer_1.4.5_linux_amd64.zip
chmod +x packer
sudo cp packer /usr/bin
sudo su
source ./init_chroot.sh
packer build exampleNetPlanSan_Daniel_Sol.json
```

Please note that in line 18 of exampleNetPlanSan_Daniel_Sol.json, "temporary_os_disk_name": "PackerTemp" is where you setup the name of packer temp disk and line 19 of exampleNetPlanSan_Daniel_Sol.json, "os_disk_skip_cleanup": "true" must set to "true", which will not delete the packer temp disk. 
