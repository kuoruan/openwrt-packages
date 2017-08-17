#
# Copyright (C) 2017 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=ariang
PKG_SOURCE_DATE:=2017-07-08
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/mayswind/AriaNg-DailyBuild
PKG_SOURCE_VERSION:=bd8d1db49f0b6d2f14f73af2815446419d6ee85f

PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE
PKG_MAINTAINER:=Hsing-Wang Liao <kuoruan@gmail.com>

include $(INCLUDE_DIR)/package.mk

define Package/ariang
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=Download Manager
  DEPENDS:=
  TITLE:=AriaNg, a modern web frontend making aria2 easier to use.
  URL:=https://github.com/mayswind/AriaNg
  PKGARCH:=all
endef

define Package/ariang/description
  AriaNg is written in pure html & javascript, thus it does not
  need any compilers or runtime environment. You can just put
  AriaNg in your web server and open it in your browser. AriaNg
  uses responsive layout, and supports any desktop or mobile devices.
endef

define Build/Compile
endef

define Package/ariang/install
	$(INSTALL_DIR) \
		$(1)/www/ariang

	$(CP) \
		$(PKG_BUILD_DIR)/{css,fonts,js,langs} \
		$(PKG_BUILD_DIR)/index.html \
		$(PKG_BUILD_DIR)/robots.txt \
		$(PKG_BUILD_DIR)/LICENSE \
		$(1)/www/ariang
endef

$(eval $(call BuildPackage,ariang))
