# System Prerequisites

1. Download and install [Xtreme Download Manager](http://xdman.sourceforge.net/)

    *Note:* XDM will allow faster download of larger files from the Internet

2. Download and install [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
3. Download [Ubuntu 19.10 VirtualBox image](https://sourceforge.net/projects/osboxes/files/v/vb/55-U-u/19.10/U19_10-VB-64bit.7z/download)
4. Extract `Ubuntu 19.10 (64bit).vdi` file from the downloaded zip file (refer step #3, above)
5. Open VirtualBox 
6. Select `Machine` >> `New` 
7. Give a name to your virtual machine, e.g. `Ubuntu 19.10 (64-bit)`

    ![Create a new virtual machine](../image/system_prerequisites/0_createVM.png)

8. Click `Next` and select the memory size.
    
    *Note:* Virtualbox recommends allotting less than half of the total RAM in host machine. For example, if you have a 2 GB RAM you can allot up to 1 GB memory for one virtual machine.

    ![Select memory size](../image/system_prerequisites/0b_selectMemory.png)

9.  Select the option `Use an existing virtual hard disk file` and add the extracted `.vdi` file (refer step #4, above)

    ![Add VDI](../image/system_prerequisites/1_add_vdi.png)

    ![Use an existing virtual hard disk](../image/system_prerequisites/2_use_existing_virtual_hard_disk.png)

10. Click on `Create`

11. Select the newly created virtual machine (VM) `Ubuntu 19.10 (64-bit)` and click on `Start`

    ![Start VM](../image/system_prerequisites/3_startVM.png)

12. Login using the password `osboxes.org`

    ![Login](../image/system_prerequisites/4_login.png)

13. Take a snapshot of your newly created virtual machine 
    1. Select `Snapshots` from the context menu 

        ![Select snapshots](../image/system_prerequisites/14a_VB_snapshot.png)

    2. Click on `Take` icon 
    3. Give a name to your snapshot and click on `OK`
    
        ![Name your snapshot](../image/system_prerequisites/14b_VB_snapshot.png)

    *Note:* We are creating this snapshot to revert to a clean state in case the state of the virtual box gets corrupted at any point.

