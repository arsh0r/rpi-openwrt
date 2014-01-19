rpi-openwrt
===========

Preparations:

* $ git clone git://git.openwrt.org/openwrt.git
* $ git log --grep=r39286
* $ cd openwrt
* $ wget https://sites.google.com/site/variousopenwrt/rpi-patch/openwrt-rpi-kernel-3.12.7y.patch
* $ patch -p1 < openwrt-rpi-kernel-3.12.7y.patch
* $ scripts/feeds update
* $ scripts/feeds install -a
