#
# Copyright (C) 2011 OpenWrt.org
# Copyright (C) 2017 Tomasz Maciej Nowak <tomek_n@o2.pl>
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#
include $(TOPDIR)/rules.mk

PKG_NAME := w-scan2
PKG_VERSION:=2019-03-14
PKG_RELEASE:=2

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/stefantalpalaru/w_scan2.git
PKG_SOURCE_DATE:=2019-03-14
PKG_SOURCE_VERSION:=e55d718a9166e7a91f32abe0c1c89689c2ef2c23
PKG_MIRROR_HASH:=skip

PKG_LICENSE := GPL-2.0
PKG_LICENSE_FILE := COPYING

PKG_MAINTAINER := Tomasz Maciej Nowak <tomek_n@o2.pl>
PKG_FIXUP:=autoreconf

include $(INCLUDE_DIR)/package.mk

define Package/w-scan2
  SECTION := utils
  CATEGORY := Utilities
  TITLE := w_scan performs frequency scans for DVB and ATSC
  URL := http://wirbel.htpc-forum.de/w_scan/index2.html
endef

define Package/w-scan2/description
 w_scan is a small command line utility used to perform frequency scans for
 DVB and ATSC transmissions. It is capable of creating channels.conf files
 (in different output formats !) as well as initial tuning data for scan.
 It's based on the utility scan from linuxtv-dvb-apps, but meanwhile it was
  heavily changed and has different features:
 1. no need for "initial transponders", and such no need for a config file
 2. w_scan finds automatically the best matching dvb card
 3. complete different command line options
 4. a different default output format as well as bunch of output formats.
 This package does not include the script file "w_scan_start.sh".
endef


define Package/w-scan2/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/w_scan2 $(1)/usr/bin
endef

$(eval $(call BuildPackage,w-scan2))
