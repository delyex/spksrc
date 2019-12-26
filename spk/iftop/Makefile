SPK_NAME = iftop
SPK_VERS = 0.17
SPK_REV = 1

DEPENDS = cross/libpcap cross/ncurses cross/$(SPK_NAME)

MAINTAINER = delyex
DESCRIPTION = Display bandwidth
RELOAD_UI = yes
STARTABLE = yes
DISPLAY_NAME = iftop
CHANGELOG = "None."

HOMEPAGE = http://www.ex-parrot.com/
LICENSE  = GNU

WIZARDS_DIR  = src/wizard/

SERVICE_USER = auto
SERVICE_WIZARD_SHARE = wizard_download_dir
SERVICE_SETUP = src/service-setup.sh
SERVICE_PORT = 9091
SERVICE_PORT_TITLE = $(DISPLAY_NAME)

# Admin link for in DSM UI
ADMIN_PORT = $(SERVICE_PORT)

POST_STRIP_TARGET = transmission_extra_install

BUSYBOX_CONFIG = usrmng
ENV += BUSYBOX_CONFIG="$(BUSYBOX_CONFIG)"

include ../../mk/spksrc.spk.mk

.PHONY: transmission_extra_install
transmission_extra_install:
	install -m 755 -d $(STAGING_DIR)/var
	install -m 644 src/settings.json $(STAGING_DIR)/var/settings.json
