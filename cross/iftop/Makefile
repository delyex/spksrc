PKG_NAME = iftop
PKG_VERS = 0.17
PKG_EXT = tar.gz
PKG_DIST_NAME = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = http://www.ex-parrot.com/pdw/iftop/download/
PKG_DIR = $(PKG_NAME)-$(PKG_VERS)

DEPENDS = cross/libpcap cross/ncurses

HOMEPAGE = http://ex-parrot.com/pdw/iftop/
COMMENT  = Display bandwidth usage on an interface.
LICENSE  = GNU General Public License

GNU_CONFIGURE = 1
CONFIGURE_ARGS = 

include ../../mk/spksrc.cross-cc.mk
