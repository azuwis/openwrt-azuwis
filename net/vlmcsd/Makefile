#
# Copyright (C) 2018 Zhong Jianxin <azuwis@gmail.com>
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#
include $(TOPDIR)/rules.mk

PKG_NAME:=vlmcsd
PKG_VERSION:=svn1111
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/Wind4/vlmcsd.git
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=28a50f7bbaf1f047f6501147ff2a4a80e3f9bc41
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.xz
PKG_MIRROR_HASH:=193fd250d2c3bd51d10255dbaee051745341dfdd30688fc12adf3058cdadf49f

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
