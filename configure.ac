#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([cpdb-backend-file],[1.0.1],[ayushb268@gmail.com],[CPDB - FILE Backend], [https://github.com/ayush268/cpdb-backend-file])
AM_INIT_AUTOMAKE([-Wall foreign])
AC_CONFIG_SRCDIR([src/print_backend_file.c])

: ${CFLAGS=""}
# Check for a C compiler
AC_PROG_CC


# Checks for backend library
PKG_CHECK_MODULES([CPDBBACKEND],[cpdb-libs-backend >= 1])
PKG_CHECK_MODULES([GIO],[gio-2.0])
PKG_CHECK_MODULES([GIOUNIX],[gio-unix-2.0])
PKG_CHECK_MODULES([GLIB],[glib-2.0])

# Checks for header files.
AC_CHECK_HEADERS([stdlib.h string.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_TYPE_SIZE_T

# Checks for library functions
AC_FUNC_MALLOC

# The Dbus service directory
DBUS_SERVICES_DIR="/usr/share/dbus-1/services"
AC_SUBST(DBUS_SERVICES_DIR)

# The info directory which will be read by the frontend
INFO_DIR="/usr/share/print-backends"
AC_SUBST(INFO_DIR)

# The directory for the backend executables
CPDB_BACKEND_DIR="$libdir/print-backends"
AC_SUBST(CPDB_BACKEND_DIR)

AC_OUTPUT([Makefile src/Makefile data/Makefile])
