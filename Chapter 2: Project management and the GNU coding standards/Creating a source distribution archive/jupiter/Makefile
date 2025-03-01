# The global Makefile of the jupiter project
#
# Copyright 2008 John Calcote <http://freesoftwaremagazine.com/authors/John%20Calcote>
# Copyright 2025 林博仁(Buo-ren Lin) <buo.ren.lin@gmail.com>
# SPDX-License-Identifier: WTFPL
package = jupiter
version = 1.0
tarname = $(package)
distdir = $(tarname)-$(version)

all clean jupiter:
	$(MAKE) -C src $@

dist: $(distdir).tar.gz

$(distdir).tar.gz: $(distdir)
	tar chof - $(distdir) |\
		gzip -9 -c >$(distdir).tar.gz
	rm -rf $(distdir)

$(distdir):
	mkdir -p $(distdir)/src
	cp Makefile $(distdir)
	cp src/Makefile $(distdir)/src
	cp src/main.c $(distdir)/src

.PHONY: all clean dist
