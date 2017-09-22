dnl Process this file with autoconf to produce a configure script.

dnl Copyright (C) 2017 Dynare Team
dnl
dnl This file is part of Dynare.
dnl
dnl Dynare is free software: you can redistribute it and/or modify
dnl it under the terms of the GNU General Public License as published by
dnl the Free Software Foundation, either version 3 of the License, or
dnl (at your option) any later version.
dnl
dnl Dynare is distributed in the hope that it will be useful,
dnl but WITHOUT ANY WARRANTY; without even the implied warranty of
dnl MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
dnl GNU General Public License for more details.
dnl
dnl You should have received a copy of the GNU General Public License
dnl along with Dynare.  If not, see <http://www.gnu.org/licenses/>.

AC_PREREQ([2.62])
AC_INIT([userguide], [1.0])
AC_CONFIG_SRCDIR([configure.ac])
AM_INIT_AUTOMAKE([1.11 foreign])

AC_CHECK_PROG([PDFLATEX], [pdflatex], [pdflatex])
AM_CONDITIONAL([HAVE_PDFLATEX], [test "x$PDFLATEX" != "x"])

AC_CHECK_PROG([BIBTEX], [bibtex], [bibtex])
AM_CONDITIONAL([HAVE_BIBTEX], [test "x$BIBTEX" != "x"])

if test "x$PDFLATEX" != "x" -a "x$BIBTEX" != "x"; then
  BUILD_DYNARE_USERGUIDE="yes"
else
  BUILD_DYNARE_USERGUIDE="no (missing one of: pdflatex, bibtex)"
fi

AC_CONFIG_FILES([Makefile
                 doc/Makefile
])

AC_MSG_NOTICE([

 Build the Dynare user guide: $BUILD_DYNARE_USERGUIDE

])

AC_OUTPUT
