#
# Copyright (C) 2017 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-lirc
PKG_VERSION:=0.10.1
PKG_RELEASE:=2

PKG_LICENSE:=MIT
PKG_BUILD_DEPENDS:=lirc
PKG_SOURCE:=lirc-$(PKG_VERSION).tar.bz2
PKG_SOURCE_URL:=@SF/lirc
PKG_MD5SUM:=skip

include $(INCLUDE_DIR)/package.mk
include ../../packages/lang/python/python3-package.mk
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)
PKG_BUILD_DIR_TEMP:=$(BUILD_DIR)/_$(PKG_NAME)-$(PKG_VERSION)

define Package/python3-lirc
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=python3-lirc
  DEPENDS:=+python3-light +lirc
  VARIANT:=python3
endef

define Build/Prepare
	$(INSTALL_DIR) $(PKG_BUILD_DIR)
	$(PKG_UNPACK)
	mv $(BUILD_DIR)/lirc-$(PKG_VERSION)/python-pkg/* $(PKG_BUILD_DIR)/
	ls -l $(PKG_BUILD_DIR)
endef

$(eval $(call Py3Package,python3-lirc))
$(eval $(call BuildPackage,python3-lirc))
$(eval $(call BuildPackage,python3-lirc-src))

