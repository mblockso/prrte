#
# Copyright (c) 2016-2020 Intel, Inc.  All rights reserved.
# Copyright (c) 2017      IBM Corporation.  All rights reserved.
# Copyright (c) 2019      Research Organization for Information Science
#                         and Technology (RIST).  All rights reserved.
# Copyright (c) 2020      Cisco Systems, Inc.  All rights reserved
# $COPYRIGHT$
#
# Additional copyrights may follow
#
# $HEADER$
#

sources = \
          schizo_singularity_component.c \
          schizo_singularity.h \
          schizo_singularity.c

# Make the output library in this directory, and name it either
# mca_<type>_<name>.la (for DSO builds) or libmca_<type>_<name>.la
# (for static builds).

if MCA_BUILD_prte_schizo_singularity_DSO
component_noinst =
component_install = mca_schizo_singularity.la
else
component_noinst = libmca_schizo_singularity.la
component_install =
endif

mcacomponentdir = $(prtelibdir)
mcacomponent_LTLIBRARIES = $(component_install)
mca_schizo_singularity_la_SOURCES = $(sources)
mca_schizo_singularity_la_LDFLAGS = -module -avoid-version
mca_schizo_singularity_la_LIBADD = $(top_builddir)/src/libprrte.la

noinst_LTLIBRARIES = $(component_noinst)
libmca_schizo_singularity_la_SOURCES = $(sources)
libmca_schizo_singularity_la_LDFLAGS = -module -avoid-version

