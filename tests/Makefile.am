# Copyright © 2015 Broadcom
#
# Permission is hereby granted, free of charge, to any person obtaining a
# copy of this software and associated documentation files (the "Software"),
# to deal in the Software without restriction, including without limitation
# the rights to use, copy, modify, merge, publish, distribute, sublicense,
# and/or sell copies of the Software, and to permit persons to whom the
# Software is furnished to do so, subject to the following conditions:
#
# The above copyright notice and this permission notice (including the next
# paragraph) shall be included in all copies or substantial portions of the
# Software.
#
# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
# IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
# FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.  IN NO EVENT SHALL
# THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
# LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
# FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS
# IN THE SOFTWARE.

AM_CPPFLAGS = \
	-I$(top_srcdir)/include/drm \
	-I$(top_srcdir)/include \
	-I$(srcdir)/lib \
	$()

AM_CFLAGS = $(LIBDRM_CFLAGS) $(CWARNFLAGS)

noinst_LTLIBRARIES = libvc4_test.la

libvc4_test_la_SOURCES = \
	lib/vc4_test.c \
	lib/vc4_test.h \
	lib/vc4_qpu.c \
	lib/vc4_qpu.h \
	$()

noinst_PROGRAMS = \
	shader_map \
	shader_missing_end \
	shader_noop \
	$()

TEST_LIBS = $(LIBDRM_LIBS) libvc4_test.la

shader_map_LDADD = $(TEST_LIBS)
shader_missing_end_LDADD = $(TEST_LIBS)
shader_noop_LDADD = $(TEST_LIBS)

list-tests:
	@echo $(noinst_PROGRAMS)

