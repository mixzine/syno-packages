PKG_NAME = db
PKG_VERS = 4.8.30
PKG_EXT = tar.gz
PKG_DIST_NAME = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = http://download.oracle.com/berkeley-db
PKG_DIR = $(PKG_NAME)-$(PKG_VERS)

DEPENDS = 

HOMEPAGE = http://www.oracle.com/technetwork/products/berkeleydb/overview/index.html
COMMENT  = Berkeley DB enables the development of custom data management solutions, without the overhead traditionally associated with such custom projects.
LICENSE  = Copyright © 1990,2007 Oracle.  All rights reserved. See LICENSE file.

DESTDIR = $(INSTALL_DIR)
CONFIGURE_TARGET = myConfigure
COMPILE_TARGET = myCompile
INSTALL_TARGET = myInstall

include ../../mk/spksrc.cross-cc.mk

.PHONY: myConfigure
myConfigure: 
	$(RUN) ; cd build_unix ; ../dist/configure $(TC_CONFIGURE_ARGS) --enable-cxx --prefix=$(INSTALL_DIR)/$(INSTALL_PREFIX)

.PHONY: myCompile
myCompile: 
	@$(RUN) ; cd build_unix ; $(MAKE)
	
.PHONY: myInstall
myInstall: 
	@$(RUN) ; cd build_unix ; $(MAKE) install

