rpi-openwrt
===========

Preparations:

* $ svn co --revision=38972 svn://svn.openwrt.org/openwrt/trunk/
* $ cd trunk
* $ wget https://sites.google.com/site/variousopenwrt/rpi-patch/openwrt-rpi.patch
* $ patch -p1 < openwrt-rpi.patch
* $ scripts/feeds update
* $ scripts/feeds install -a
