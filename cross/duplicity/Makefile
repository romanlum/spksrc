PKG_NAME = duplicity
PKG_SHORT_VERS = 0.7
PKG_VERS = $(PKG_SHORT_VERS).06
PKG_EXT = tar.gz
PKG_DIST_NAME = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = https://launchpad.net/$(PKG_NAME)/$(PKG_SHORT_VERS)-series/$(PKG_VERS)/+download
PKG_DIR = $(PKG_NAME)-$(PKG_VERS)

DEPENDS = cross/duplicity-amazondrive cross/librsync

HOMEPAGE = http://duplicity.nongnu.org/
COMMENT  = Encrypted bandwidth-efficient backup using the rsync algorithm
LICENSE  = GNU GPLv2

PRE_CONFIGURE_TARGET = dupPostConfigure

dupPostConfigure:
	cp $(STAGING_INSTALL_PREFIX)/share/duplicity-amazondrive/amazondrivebackend.py $(WORK_DIR)/$(PKG_DIR)/duplicity/backends/

include ../../mk/spksrc.python-wheel.mk
