AM_CFLAGS = $(PYTHON_INCLUDE) $(PACKAGE_CFLAGS) -I$(top_srcdir)/include

lib_LTLIBRARIES = libbabeltrace-python-plugin-provider.la

libbabeltrace_python_plugin_provider_la_SOURCES = \
	python-plugin-provider.c logging.c logging.h
libbabeltrace_python_plugin_provider_la_LDFLAGS = \
	$(LT_NO_UNDEFINED) \
	-version-info $(BABELTRACE_LIBRARY_VERSION) \
	$(PYTHON_LIBS)

libbabeltrace_python_plugin_provider_la_LIBADD =

if !BUILT_IN_PLUGINS
libbabeltrace_python_plugin_provider_la_LIBADD += \
	$(top_builddir)/logging/libbabeltrace-logging.la \
	$(top_builddir)/common/libbabeltrace-common.la
endif
