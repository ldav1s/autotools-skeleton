auxdir                  = $(top_srcdir)/auxd

# These are generated by autotools
HELPER_PROGS            = $(auxdir)/config.guess \
                          $(auxdir)/config.sub \
                          $(auxdir)/depcomp \
                          $(auxdir)/install-sh \
                          $(auxdir)/ltmain.sh \
                          $(auxdir)/missing

# These are generated by autotools
GEN_MACROS              = $(top_srcdir)/m4/libtool.m4 \
			  $(top_srcdir)/m4/ltoptions.m4 \
			  $(top_srcdir)/m4/ltsugar.m4 \
			  $(top_srcdir)/m4/ltversion.m4 \
			  $(top_srcdir)/m4/lt~obsolete.m4
ACLOCAL_AMFLAGS         = -I m4
MOSTLYCLEANFILES        =
CLEANFILES              =
EXTRA_DIST              = $(top_srcdir)/bootstrap.sh

# This cleans aggressively, to the bare repo almost
MAINTAINERCLEANFILES    = $(top_builddir)/Makefile.in \
			  $(top_builddir)/configure \
			  $(top_builddir)/aclocal.m4 \
			  $(HELPER_PROGS) $(GEN_MACROS)

# These are set this way to allow conditionals to append later
# (when added) instead of just setting them to a list of targets
bin_PROGRAMS =
lib_LTLIBRARIES =

bin_PROGRAMS += skel

skel_SOURCES = $(top_srcdir)/src/main.c

# make sure libtool gets updated
libtool: $(LIBTOOL_DEPS)
	$(SHELL) ./config.status --recheck
