noinst_HEADERS = arguments.h \
		 list.h \
		 utils.h

if IS_BIONIC
noinst_HEADERS += include/ifaddrs.h
endif

if !HAVE_GETLINE
if HAVE_FGETLN
noinst_HEADERS += include/getline.h
endif
endif

if !HAVE_GETSUBOPT
noinst_HEADERS += include/getsubopt.h
endif

AM_CFLAGS=-DLIBEXECDIR=\"$(LIBEXECDIR)\" \
	  -DLXCTEMPLATEDIR=\"$(LXCTEMPLATEDIR)\" \
	  -DRUNTIME_PATH=\"$(RUNTIME_PATH)\"

bin_PROGRAMS = lxc-attach \
	       lxc-autostart \
	       lxc-cgroup \
	       lxc-checkpoint \
	       lxc-copy \
	       lxc-config \
	       lxc-console \
	       lxc-create \
	       lxc-destroy \
	       lxc-device \
	       lxc-execute \
	       lxc-freeze \
	       lxc-info \
	       lxc-ls \
	       lxc-monitor \
	       lxc-snapshot \
	       lxc-start \
	       lxc-stop \
	       lxc-top \
	       lxc-unfreeze \
	       lxc-unshare \
	       lxc-wait

if ENABLE_DEPRECATED
bin_PROGRAMS += lxc-clone
endif

AM_LDFLAGS = -Wl,-E
if ENABLE_RPATH
AM_LDFLAGS += -Wl,-rpath -Wl,$(libdir)
endif
LDADD = -llxc

lxc_attach_SOURCES = lxc_attach.c \
		     arguments.c \
		     arguments.h \
		     list.h \
		     utils.c \
		     utils.h
lxc_autostart_SOURCES = lxc_autostart.c \
			arguments.c \
			arguments.h \
			list.h \
			utils.c \
			utils.h
lxc_cgroup_SOURCES = lxc_cgroup.c \
		     arguments.c \
		     arguments.h \
		     list.h \
		     utils.c \
		     utils.h
lxc_checkpoint_SOURCES = lxc_checkpoint.c \
			 arguments.c \
			 arguments.h \
			 list.h \
			 utils.c \
			 utils.h
lxc_config_SOURCES = lxc_config.c \
		     arguments.c \
		     arguments.h \
		     list.h \
		     utils.c \
		     utils.h
lxc_console_SOURCES = lxc_console.c \
		      arguments.c \
		      arguments.h \
		      list.h \
		      utils.c \
		      utils.h
lxc_copy_SOURCES = lxc_copy.c \
		   arguments.c \
		   arguments.h \
		   list.h \
		   utils.c \
		   utils.h
lxc_create_SOURCES = lxc_create.c \
		     arguments.c \
		     arguments.h \
		     list.h \
		     utils.c \
		     utils.h
lxc_destroy_SOURCES = lxc_destroy.c \
		      arguments.c \
		      arguments.h \
		      list.h \
		      utils.c \
		      utils.h
lxc_device_SOURCES = lxc_device.c \
		     arguments.c \
		     arguments.h \
		     list.h \
		     utils.c \
		     utils.h
lxc_execute_SOURCES = lxc_execute.c \
		      arguments.c \
		      arguments.h \
		      list.h \
		      utils.c \
		      utils.h
lxc_freeze_SOURCES = lxc_freeze.c \
		     arguments.c \
		     arguments.h \
		     list.h \
		     utils.c \
		     utils.h
lxc_info_SOURCES = lxc_info.c \
		   arguments.c \
		   arguments.h \
		   list.h \
		   utils.c \
		   utils.h
lxc_ls_SOURCES = lxc_ls.c \
		 arguments.c \
		 arguments.h \
		 list.h \
		 utils.c \
		 utils.h
lxc_monitor_SOURCES = lxc_monitor.c \
		      arguments.c \
		      arguments.h \
		      list.h \
		      utils.c \
		      utils.h
lxc_snapshot_SOURCES = lxc_snapshot.c \
		       arguments.c \
		       arguments.h \
		       list.h \
		       utils.c \
		       utils.h
lxc_start_SOURCES = lxc_start.c \
		    arguments.c \
		    arguments.h \
		    list.h \
		    utils.c \
		    utils.h
lxc_stop_SOURCES = lxc_stop.c \
		   arguments.c \
		   arguments.h \
		   list.h \
		   utils.c \
		   utils.h
lxc_top_SOURCES = lxc_top.c \
		  arguments.c \
		  arguments.h \
		  list.h \
		  utils.c \
		  utils.h
lxc_unfreeze_SOURCES = lxc_unfreeze.c \
		       arguments.c \
		       arguments.h \
		       list.h \
		       utils.c \
		       utils.h
lxc_unshare_SOURCES = lxc_unshare.c \
		      arguments.c \
		      arguments.h \
		      list.h \
		      utils.c \
		      utils.h
lxc_wait_SOURCES = lxc_wait.c \
		   arguments.c \
		   arguments.h \
		   list.h \
		   utils.c \
		   utils.h

if ENABLE_DEPRECATED
lxc_clone_SOURCES = lxc_clone.c \
		    arguments.c \
		    arguments.h \
		    list.h \
		    utils.c \
		    utils.h
endif

if !HAVE_GETSUBOPT
lxc_copy_SOURCES += include/getsubopt.c \
		    include/getsubopt.h
endif
