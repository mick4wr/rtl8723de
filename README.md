# rtl8723de
Realtek RTL8723DE module for Linux kernel version >= 4.11

Install:

    git clone https://github.com/smlinux/rtl8723de.git -b 4.11-up
    dkms add ./rtl8723de
    dkms install rtl8723de/5.1.1.8_21285.20171026_COEX20170111-1414
    depmod -a
    reboot

Uninstall:

    rmmod -f 8723de
    dkms uninstall rtl8723de/5.1.1.8_21285.20171026_COEX20170111-1414
    dkms remove rtl8723de/5.1.1.8_21285.20171026_COEX20170111-1414 --all
    depmod -a
    reboot

This fork attempts to fix the build failure on kernel 4.15. It is highly experimental; regular use is not recommended.
