# plugindir is set in configure

plugin_LTLIBRARIES = libgstkate.la

# sources used to compile this plug-in
libgstkate_la_SOURCES = gstkate.c gstkatedec.c gstkateenc.c gstkateparse.c gstkatetag.c gstkateutil.c gstkatespu.c
if USE_TIGER
libgstkate_la_SOURCES += gstkatetiger.c
endif

# flags used to compile this plugin
libgstkate_la_CFLAGS = $(GST_CFLAGS) $(GST_PLUGINS_BASE_CFLAGS) $(TIGER_CFLAGS) $(KATE_CFLAGS)
libgstkate_la_LIBADD = $(GST_PLUGINS_BASE_LIBS) -lgstvideo-$(GST_MAJORMINOR) -lgsttag-$(GST_MAJORMINOR) $(GST_LIBS) $(TIGER_LIBS) $(KATE_LIBS)
libgstkate_la_LDFLAGS = $(GST_PLUGIN_LDFLAGS)
if !GST_PLUGIN_BUILD_STATIC
libgstkate_la_LIBTOOLFLAGS = --tag=disable-static
endif

# headers we need but don't want installed
noinst_HEADERS = gstkate.h gstkatedec.h gstkateenc.h gstkateparse.h gstkatetag.h gstkateutil.h gstkatespu.h gstkatetiger.h

EXTRA_DIST=README
