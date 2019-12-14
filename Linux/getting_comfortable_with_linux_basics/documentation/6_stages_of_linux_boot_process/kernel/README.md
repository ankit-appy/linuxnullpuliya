# 4. Kernel

A linux kernel is responsible for handling Process management, Memory Management, Users, Inter process communication etc. The kernel loads an initial RAM disk (`initrd`) that loads the system drives and then looks for the root file system.

1. Kernel mounts the root file system as specified in the `root=` attribute in `grub.cnf` file. Check your grub configuration file by running following command

        $ cat /boot/grub/grub.cfg | grep root=

    ![Locate root attribute in grub.cfg](../../image/6_stages_of_linux_boot_process/15_grub_configuration_root.png)

2. The kernel image is a compressed image like **zImage** (compressed image, less than 512 KB) or **bzImage** (big compressed image, greater than 512 KB). Can you find your kernel image? Check the contents of `/boot/` folder

    ![Locate kernel image](../../image/6_stages_of_linux_boot_process/16_kernel.png)

3. `initrd` stands for Initial RAM Disk. It is used by the kernel as a **temporary** root file system until kernel is booted and the real root file system is mounted. `initrd` is available in the form of an image similar to the kernel image file. Can you locate the `initrd` image file? Check the contents of `/boot` folder once again

    ![Locate `initrd` image file](../../image/6_stages_of_linux_boot_process/18_initrd.png)

4. Extract *initramfs* content of the kernel by running following command

        $ unmkinitramfs /boot/initrd.img-5.0.0-XX-generic /tmp/initramfs/

    ![Extract initramfs content](../../image/6_stages_of_linux_boot_process/20_unmkinitramfs.png)

5.  View the extracted contents of `initrd` image file
   
        $ ll /tmp/initramfs/main/

    ![](../../image/6_stages_of_linux_boot_process/20b_unmkinitramfs.png)

    *Note:* The `initrd` image file contains folders that are very much similar to our linux directory strucutre. There is `/etc/`, `/lib`, and some necessary commands in `/sbin` etc. Its a small root file system that the kernel loads as a **temporary root file system** before the real root file system is loaded.
