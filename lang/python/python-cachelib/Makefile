# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=cachelib
PKG_VERSION:=0.1
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://files.pythonhosted.org/packages/source/c/cachelib
PKG_HASH:=8b889b509d372095357b8705966e1282d40835c4126d7c2b07fd414514d8ae8d

PKG_MAINTAINER:=Daniel Golle <daniel@makrotopia.org>
PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=python3
PKG_BUILD_DIR:=$(BUILD_DIR)/$(BUILD_VARIANT)-$(PKG_NAME)-$(PKG_VERSION)
PKG_UNPACK=$(HOST_TAR) -C $(PKG_BUILD_DIR) --strip-components=1 -xzf $(DL_DIR)/$(PKG_SOURCE)

include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-cachelib
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  URL:=https://github.com/pallets/cachelib
  TITLE:=python3-cachelib
  DEPENDS:=+python3-light
  VARIANT:=python3
endef

define Package/python3-cachelib/description
cachelib

A collection of cache libraries in the same API interface. Extracted from werkzeug.
endef

$(eval $(call Py3Package,python3-cachelib))
$(eval $(call BuildPackage,python3-cachelib))
$(eval $(call BuildPackage,python3-cachelib-src))
