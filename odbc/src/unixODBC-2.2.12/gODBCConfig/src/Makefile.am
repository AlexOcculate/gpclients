## Process this file with automake to produce Makefile.in

bin_PROGRAMS = gODBCConfig
lib_LTLIBRARIES = libgtkodbcconfig.la

include_HEADERS = odbcconfig.h

INCLUDES = \
	-I@top_srcdir@/include \
	-I@top_srcdir@/../include \
	-I$(top_srcdir)/intl \
	-I@top_srcdir@/libltdl \
	-DUNIXODBC_SOURCE \
	$(GNOME_INCLUDEDIR)

gODBCConfig_SOURCES = \
	main.c 

libgtkodbcconfig_la_SOURCES = \
	odbcconfig.c odbcconfig.h \
	support.c support.h \
	interface.h \
	callbacks.c callbacks.h

gODBCConfig_DEPENDENCIES = libgtkodbcconfig.la ../../ini/libinilc.la

gODBCConfig_LDADD = $(GNOME_LIBDIR) \
		$(GNOMEUI_LIBS) \
		$(INTLLIBS) \
		-L$(ODBCLIBS) $(ODBCLIB) \
		libgtkodbcconfig.la \
		../../odbcinst/libodbcinst.la \
		../../ini/libinilc.la
