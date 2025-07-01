applicationsdir = $(datadir)/applications
waylandsessionsdir = $(datadir)/wayland-sessions

bin_SCRIPTS =
man_MANS =
dist_applications_DATA =
dist_waylandsessions_DATA =
dist_pkgdata_DATA = waydroid-x11.ini waydroid-drm.ini
CLEANFILES = $(subst_files)
EXTRA_DIST = \
	waydroid-x11.in waydroid-x11.1.in \
	waydroid-drm.in waydroid-drm.1.in

if ENABLE_X11
bin_SCRIPTS += waydroid-x11
man_MANS += waydroid-x11.1
dist_applications_DATA += waydroid-x11.desktop
endif

if ENABLE_DRM
bin_SCRIPTS += waydroid-drm
man_MANS += waydroid-drm.1
dist_waylandsessions_DATA += waydroid-drm.desktop
endif

do_subst = sed \
	-e 's,[@]PACKAGE_NAME[@],$(PACKAGE_NAME),g' \
	-e 's,[@]PACKAGE_VERSION[@],$(PACKAGE_VERSION),g' \
	-e 's,[@]pkgdatadir[@],$(pkgdatadir),g'

subst_files = $(bin_SCRIPTS) $(man_MANS)
$(subst_files): %: %.in Makefile
	$(do_subst) < $< > $@
