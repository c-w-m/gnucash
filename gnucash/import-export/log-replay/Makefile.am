SUBDIRS = .

pkglib_LTLIBRARIES=libgncmod-log-replay.la

libgncmod_log_replay_la_SOURCES = \
  gnc-log-replay.c \
  gnc-plugin-log-replay.c \
  gncmod-log-replay.c

noinst_HEADERS = \
  gnc-log-replay.h \
  gnc-plugin-log-replay.h

libgncmod_log_replay_la_LDFLAGS = -avoid-version

libgncmod_log_replay_la_LIBADD = \
  ${top_builddir}/gnucash/gnome-utils/libgncmod-gnome-utils.la \
  ${top_builddir}/libgnucash/app-utils/libgncmod-app-utils.la \
  ${top_builddir}/libgnucash/engine/libgncmod-engine.la \
  ${top_builddir}/libgnucash/core-utils/libgnc-core-utils.la \
  ${top_builddir}/libgnucash/gnc-module/libgnc-module.la \
  ${GTK_LIBS} \
  ${GLIB_LIBS}

AM_CPPFLAGS = \
  -I${top_srcdir}/common \
  -I${top_srcdir}/libgnucash/core-utils \
  -I${top_srcdir}/libgnucash/engine \
  -I${top_srcdir}/libgnucash/gnc-module \
  -I${top_srcdir}/libgnucash/app-utils \
  -I${top_srcdir}/gnucash/gnome \
  -I${top_srcdir}/gnucash/gnome-utils \
  -I${top_srcdir}/gnucash/import-export \
  ${GTK_CFLAGS} \
  ${GLIB_CFLAGS}

uidir = $(GNC_UI_DIR)
dist_ui_DATA = \
	gnc-plugin-log-replay-ui.xml

AM_CPPFLAGS += -DG_LOG_DOMAIN=\"gnc.import.log-replay\"

EXTRA_DIST = CMakeLists.txt
