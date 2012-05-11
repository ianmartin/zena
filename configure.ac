#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ(2.59)
AC_INIT([zena], [0.5.0], [jdesbonnet@gmail.com])
AC_CONFIG_SRCDIR([zena.c])
AC_CONFIG_HEADER([config.h])

AM_INIT_AUTOMAKE([-Wall foreign subdir-objects])
m4_ifdef([AM_SILENT_RULES], [AM_SILENT_RULES([yes])])

# Checks for programs.
AC_PROG_CC
AM_PROG_CC_C_O

# Checks for libraries.
AC_SEARCH_LIBS([clock_gettime], [rt])
PKG_CHECK_MODULES(LIBUSB, libusb-1.0 >= 1.0.0)

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
