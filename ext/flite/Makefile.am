plugin_LTLIBRARIES = libgstflite.la

libgstflite_la_SOURCES = gstflite.c gstflitetestsrc.c
libgstflite_la_CFLAGS = \
	$(GST_PLUGINS_BASE_CFLAGS) \
	$(GST_CFLAGS) \
	$(FLITE_CFLAGS)
libgstflite_la_LIBADD = \
	$(GST_PLUGINS_BASE_LIBS) \
	-lgstaudio-@GST_MAJORMINOR@ \
	$(GST_BASE_LIBS) \
	$(GST_LIBS) \
	$(FLITE_LIBS)
libgstflite_la_LDFLAGS = $(GST_PLUGIN_LDFLAGS) $(LIBM)
if !GST_PLUGIN_BUILD_STATIC
libgstflite_la_LIBTOOLFLAGS = --tag=disable-static
endif

