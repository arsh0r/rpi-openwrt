include $(TOPDIR)/rules.mk

PKG_NAME:=rpi-userland
PKG_REV:=350dfd09b0b1f0b8fe0bd52192fecdd25f64993c
PKG_VERSION:=20140104
PKG_RELEASE:=1
PKG_SOURCE:=$(PKG_REV).tar.gz
PKG_SOURCE_URL:=https://github.com/raspberrypi/userland/archive/
PKG_MD5SUM:=d0d156b1d8d0575e5ff5860b6cec618f

PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)/userland-$(PKG_REV)

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/rpi-userland
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=rpi-userland utilities
  URL:=https://github.com/raspberrypi/userland
  DEPENDS:=+libpthread +librt +ldconfig
endef

define Package/rpi-userland/description
This repository contains the source code for the ARM side libraries used on Raspberry Pi. These typically are installed in /opt/vc/lib and includes source for the ARM side code to interface to: EGL, mmal, GLESv2, vcos, openmaxil, vchiq_arm, bcm_host, WFC, OpenVG.
endef

define Package/rpi-userland/install
	$(INSTALL_DIR) $(1)/opt/vc/bin
	$(INSTALL_DIR) $(1)/opt/vc/lib
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/build/bin/* $(1)/opt/vc/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/build/lib/* $(1)/opt/vc/lib
endef

$(eval $(call BuildPackage,rpi-userland))
