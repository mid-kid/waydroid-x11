applicationsdir = $(datadir)/applications
waylandsessionsdir = $(datadir)/wayland-sessions

bin_SCRIPTS = waydroid-x11 waydroid-drm
dist_pkgdata_DATA = weston.ini
dist_applications_DATA = waydroid-x11.desktop
dist_waylandsessions_DATA = waydroid-drm.desktop
CLEANFILES = $(subst_files)
EXTRA_DIST = waydroid-x11.in waydroid-drm.in

do_subst = sed \
	-e 's,[@]pkgdatadir[@],$(pkgdatadir),g'

subst_files = $(bin_SCRIPTS)
$(subst_files): %: %.in Makefile
	$(do_subst) < $< > $@
