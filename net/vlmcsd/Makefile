#
# Copyright (C) 2018 Zhong Jianxin <azuwis@gmail.com>
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#
include $(TOPDIR)/rules.mk

PKG_NAME:=vlmcsd
PKG_VERSION:=1113
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/Wind4/vlmcsd.git
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=70e03572b254688b8c3557f898e7ebd765d29ae1
PKG_SOURCE:=$(PKG_SOURCE_SUBDIR).tar.xz
PKG_HASH:=fcc8357b3ef8b523deb5d61280fc6bce56e9a191cf7839bc29426aecc3c1d085

PKG_MAINTAINER:=Zhong Jianxin <azuwis@gmail.com>

PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

define Package/vlmcsd
  TITLE:=KMS Emulator
  SECTION:=net
  CATEGORY:=Network
  URL:=https://github.com/Wind4/vlmcsd
endef

define Package/vlmcsd/install
	$(INSTALL_DIR) \
		$(1)/usr/bin \
		$(1)/etc/init.d

	$(INSTALL_BIN) $(PKG_BUILD_DIR)/bin/vlmcsd $(1)/usr/bin/
	$(INSTALL_BIN) files/vlmcsd.init $(1)/etc/init.d/vlmcsd
endef

$(eval $(call BuildPackage,vlmcsd))
