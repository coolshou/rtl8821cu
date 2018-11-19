rtl8821cu

Drivers for the rtl8821cu chipset for wireless adapters (D-Link DWA-171 rev C1)

# Install driver
## requirement
    * kernel header

## compile the driver
> cd driver
> make
## test the driver (require cfg80211 loaded in system)
> insmod 8821cu.ko
## install driver
> sudo make install

# auto switch from DISK mode to NIC mode
## requirement (test with ubuntu 18.04):
    1. usb-modeswitch usb-modeswitch-data
    > apt install usb-modeswitch usb-modeswitch-data
    2. udev
    > apt install udev

## install usb-modeswitch setting files
> cd usbswitch
> sudo make install

# UEFI Secure Boot - (boot the kernel with signed)
 if insmod the module it shows error of "Required key not available", you are using a kernel which is signed
 Only signed module can be use in this condition.
