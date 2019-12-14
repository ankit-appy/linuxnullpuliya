# GNU/Linux

**GNU** stands for *GNU Not Unix*. It was designed to be an open source *operating system* that is backwards compatible with Unix operating systems. GNU packages are packages designed to be shared, modified and run wherever you want, for whatever purpose.

1. Find out what operating system is running in your machine

        $ uname -o

    ![OS name](../../image/getting_started_with_linux/1_uname_o.png)

2. Print the kernel name

        $ uname -s

    ![Kernel name](../../image/getting_started_with_linux/2_kernel_name.png)

3. Check if kernel is 32-bit or 64-bit

        $ uname -m

    ![Kernel version](../../image/getting_started_with_linux/2b_kernel_version.png)

    *Note:* `x86_64 GNU/Linux` indicates that you’ve a **64-bit** Linux kernel running. If you use see i386/`i486`/`i586`/`i686`, then it is a **32-bit** kernel.
    <br/>

4. Print all system information. Follow [this link](https://stackoverflow.com/questions/6943803/understanding-uname-output) to understand the output.
   
        $ uname -a

    ![Print all system information](../../image/getting_started_with_linux/3_all_sys_info.png)

5. Follow [this link](https://www.geeksforgeeks.org/uname-command-in-linux-with-examples/) and try other available `uname` options.
6. Determine *Linux distribution* and *version* by running the following command

        $ cat /etc/*-release

    ![](../../image/getting_started_with_linux/3b_linux_distro.png)