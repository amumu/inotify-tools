bin_PROGRAMS = inotifywait inotifywatch
inotifywait_SOURCES = inotifywait.c common.c common.h
inotifywatch_SOURCES = inotifywatch.c common.c common.h

AM_CFLAGS = -std=c99 -I../libinotifytools/src -L../libinotifytools/src
LDADD = ../libinotifytools/src/libinotifytools.la

if STATIC_BINARY_ENABLE
AM_LDFLAGS = -static-libtool-libs
endif

dist-hook:
	touch -d '2 days ago' $(distdir)/*
