AM_CPPFLAGS =						\
	$(GDKPIXBUF_CFLAGS)				\
	$(GLIB_CFLAGS)					\
	$(GTK_CFLAGS)					\
	$(LIBARCHIVE_CFLAGS)				\
	$(SOUP_CFLAGS)					\
	$(RPM_CFLAGS)					\
	$(FREETYPE_CFLAGS)				\
	-I$(top_srcdir)/libappstream-glib		\
	-I$(top_builddir)/libappstream-glib		\
	-I$(top_srcdir)/libappstream-builder		\
	-I$(top_builddir)/libappstream-builder		\
	-DG_LOG_DOMAIN=\"Asb\"

plugindir = $(libdir)/asb-plugins-$(AS_PLUGIN_VERSION)
plugin_LTLIBRARIES =					\
	libasb_plugin_absorb.la				\
	libasb_plugin_appdata.la			\
	libasb_plugin_desktop.la			\
	libasb_plugin_gettext.la			\
	libasb_plugin_hardcoded.la

if HAVE_FONTS
plugin_LTLIBRARIES +=					\
	libasb_plugin_font.la
endif

libasb_plugin_absorb_la_SOURCES = asb-plugin-absorb.c
libasb_plugin_absorb_la_LIBADD = $(GLIB_LIBS)
libasb_plugin_absorb_la_LDFLAGS = -module -avoid-version
libasb_plugin_absorb_la_CFLAGS = $(GLIB_CFLAGS) $(WARNINGFLAGS_C)

libasb_plugin_gettext_la_SOURCES = asb-plugin-gettext.c
libasb_plugin_gettext_la_LIBADD = $(GLIB_LIBS)
libasb_plugin_gettext_la_LDFLAGS = -module -avoid-version
libasb_plugin_gettext_la_CFLAGS = $(GLIB_CFLAGS) $(WARNINGFLAGS_C)

libasb_plugin_hardcoded_la_SOURCES = asb-plugin-hardcoded.c
libasb_plugin_hardcoded_la_LIBADD = $(GLIB_LIBS)
libasb_plugin_hardcoded_la_LDFLAGS = -module -avoid-version
libasb_plugin_hardcoded_la_CFLAGS = $(GLIB_CFLAGS) $(WARNINGFLAGS_C)

libasb_plugin_desktop_la_SOURCES = asb-plugin-desktop.c
libasb_plugin_desktop_la_LIBADD = $(GLIB_LIBS) $(GDKPIXBUF_LIBS)
libasb_plugin_desktop_la_LDFLAGS = -module -avoid-version
libasb_plugin_desktop_la_CFLAGS = $(GLIB_CFLAGS) $(WARNINGFLAGS_C)

libasb_plugin_appdata_la_SOURCES = asb-plugin-appdata.c
libasb_plugin_appdata_la_LIBADD = $(GLIB_LIBS) $(GDKPIXBUF_LIBS)
libasb_plugin_appdata_la_LDFLAGS = -module -avoid-version
libasb_plugin_appdata_la_CFLAGS = $(GLIB_CFLAGS) $(WARNINGFLAGS_C)

if HAVE_FONTS
libasb_plugin_font_la_SOURCES = asb-plugin-font.c
libasb_plugin_font_la_LIBADD = $(GLIB_LIBS) $(FREETYPE_LIBS) $(GDKPIXBUF_LIBS) $(GTK_LIBS)
libasb_plugin_font_la_LDFLAGS = -module -avoid-version
libasb_plugin_font_la_CFLAGS = $(GLIB_CFLAGS) $(GTK_CFLAGS) $(WARNINGFLAGS_C)
endif

-include $(top_srcdir)/git.mk
