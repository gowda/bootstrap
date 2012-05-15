AC_INIT([bootstrap],[git],[twitter-bootstrap@googlegroups.com],,[https://twitter.github.com/bootstrap])

AM_INIT_AUTOMAKE

if make --help 2>&1 | grep -q no-print-directory; then
   AM_MAKEFLAGS="$AM_MAKEFLAGS --no-print-directory";
fi

if make --help 2>&1 | grep -q quiet; then
   AM_MAKEFLAGS="$AM_MAKEFLAGS --quiet";
fi

AC_CONFIG_FILES([Makefile
	         less/Makefile
		 js/Makefile
		 img/Makefile])

AC_CHECK_TOOL([JSHINT], [jshint])

AC_CHECK_TOOL([RECESS], [recess])

AC_CHECK_TOOL([UGLIFYJS], [uglifyjs])

AC_OUTPUT
