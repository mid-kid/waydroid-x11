AC_INIT([waydroid-x11], [1.0])
AC_CONFIG_AUX_DIR([build-aux])
AM_INIT_AUTOMAKE([foreign])
AC_ARG_ENABLE([x11], [AS_HELP_STRING([--disable-x11],
    [Don't install waydroid-x11 wrapper])])
AM_CONDITIONAL([ENABLE_X11], [test x$enable_x11 != xno])
AC_ARG_ENABLE([drm], [AS_HELP_STRING([--disable-drm],
    [Don't install waydroid-drm wrapper])])
AM_CONDITIONAL([ENABLE_DRM], [test x$enable_drm != xno])
AC_CONFIG_FILES([Makefile])
AC_OUTPUT
