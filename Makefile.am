applicationsdir = $(datadir)/applications
waylandsessionsdir = $(datadir)/wayland-sessions

bin_SCRIPTS =
dist_applications_DATA =
dist_waylandsessions_DATA =
dist_pkgdata_DATA = weston.ini
CLEANFILES = $(subst_files)
EXTRA_DIST = waydroid-x11.in waydroid-drm.in

if ENABLE_X11
bin_SCRIPTS += waydroid-x11
dist_applications_DATA += waydroid-x11.desktop
endif

if ENABLE_DRM
bin_SCRIPTS += waydroid-drm
dist_waylandsessions_DATA += waydroid-drm.desktop
endif

do_subst = sed \
	-e 's,[@]pkgdatadir[@],$(pkgdatadir),g'

subst_files = $(bin_SCRIPTS)
$(subst_files): %: %.in Makefile
	$(do_subst) < $< > $@
