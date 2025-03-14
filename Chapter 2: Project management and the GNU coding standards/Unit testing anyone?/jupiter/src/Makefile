# The Makefile for the src/ sub-directory of the jupiter project
#
# Copyright 2008 John Calcote <http://freesoftwaremagazine.com/authors/John%20Calcote>
# Copyright 2025 林博仁(Buo-ren Lin) <buo.ren.lin@gmail.com>
# SPDX-License-Identifier: WTFPL
all: jupiter

jupiter: main.c
	gcc -g -O0 -o $@ $+

clean:
	-rm jupiter

check: all
	./jupiter | grep "Hello from .*jupiter!"
	@echo "*** ALL TESTS PASSED ***"

.PHONY: all clean check
