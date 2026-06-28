# Setup Peripherals on Linux

https://forum.level1techs.com/t/mchose-a7-ultra-linux-review/232734

## Commands (requires setting write flag on usb device)
        lsusb
> Output

        Bus 007 Device 003: ID 3837:100b RealTek MCHOSE A7 V2 Ultra
        Bus 007 Device 004: ID 41e4:2114 MCHOSE Ace68-I
> Edit mchose.rules

        sudo nano /etc/udev/rules.d/mchose.rules
> Rules

        KERNEL=="hidraw*", ATTRS{idVendor}=="3837", ATTRS{idProduct}=="100b", MODE="0666", TAG+="uaccess"
        KERNEL=="hidraw*", ATTRS{idVendor}=="41e4", ATTRS{idProduct}=="2114", MODE="0666", TAG+="uaccess"
> Reload

        sudo udevadm control --reload-rules
        sudo udevadm trigger