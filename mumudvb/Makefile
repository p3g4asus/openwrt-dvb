# 
# Copyright (C) 2009 Brice DUBOST
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/kernel.mk

PKG_NAME:=mumudvb
PKG_VERSION:=2019-01-21
PKG_RELEASE:=2

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/braice/MuMuDVB.git
PKG_SOURCE_DATE:=2019-01-21
PKG_SOURCE_VERSION:=745259ad4e3f5befa06a893e52d5adbf36a16ed1
PKG_MIRROR_HASH:=skip
PKG_FIXUP:=autoreconf


include $(INCLUDE_DIR)/package.mk


define Package/mumudvb
  SECTION:=utils
  CATEGORY:=Utilities
  DEFAULT:=n
  TITLE:=MuMuDVB streaming software
  URL:=http://mumudvb.net/
  DEPENDS:= +libdvbapi +libucsi +libdvben50221
endef

define Package/mumudvb/description
 MuMuDVB streaming software
endef

define Build/Configure
  $(call Build/Configure/Default,--with-linux-headers=$(LINUX_DIR))
endef

define Package/mumudvb/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/src/mumudvb $(1)/usr/bin/mumudvb
endef

$(eval $(call BuildPackage,mumudvb))
