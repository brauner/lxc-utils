DIST_SUBDIRS = ja ko

if USE_DOCBOOK2X
SUBDIRS = ja ko
endif

EXTRA_DIST = FAQ.txt

if ENABLE_DOCBOOK
man_MANS = \
	lxc-attach.1 \
	lxc-autostart.1 \
	lxc-cgroup.1 \
	lxc-checkpoint.1 \
	lxc-config.1 \
	lxc-console.1 \
	lxc-copy.1 \
	lxc-create.1 \
	lxc-destroy.1 \
	lxc-device.1 \
	lxc-execute.1 \
	lxc-freeze.1 \
	lxc-info.1 \
	lxc-ls.1 \
	lxc-monitor.1 \
	lxc-snapshot.1 \
	lxc-start.1 \
	lxc-stop.1 \
	lxc-top.1 \
	lxc-unfreeze.1 \
	lxc-unshare.1 \
	lxc-wait.1

if ENABLE_DEPRECATED
    man_MANS += lxc-clone.1
endif

%.1 : %.sgml
	$(db2xman) $<
	test "$(shell basename $@)" != "$@" && mv $(shell basename $@) $@ || true

%.5 : %.sgml
	$(db2xman) $<
	test "$(shell basename $@)" != "$@" && mv $(shell basename $@) $@ || true

%.7 : %.sgml
	$(db2xman) $<
	test "$(shell basename $@)" != "$@" && mv $(shell basename $@) $@ || true

lxc-%.sgml : common_options.sgml see_also.sgml

clean-local:
	$(RM) manpage.* *.7 *.5 *.1 $(man_MANS)
endif
