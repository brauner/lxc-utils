# Makefile.am

ACLOCAL_AMFLAGS = -I config

LIBTOOL_DEPS = @LIBTOOL_DEPS@
SUBDIRS = config src doc
DIST_SUBDIRS = config src doc
EXTRA_DIST = \
	autogen.sh \
	CONTRIBUTING \
	MAINTAINERS

libtool: $(LIBTOOL_DEPS)
	$(SHELL) ./config.status libtool

install-data-local:
	$(MKDIR_P) $(DESTDIR)$(LXCPATH)
	$(MKDIR_P) $(DESTDIR)$(localstatedir)/cache/lxc

ChangeLog::
	@touch ChangeLog
