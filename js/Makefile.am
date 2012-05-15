JS_SOURCES = $(srcdir)/bootstrap-transition.js $(srcdir)/bootstrap-alert.js \
	$(srcdir)/bootstrap-button.js $(srcdir)/bootstrap-carousel.js \
	$(srcdir)/bootstrap-collapse.js $(srcdir)/bootstrap-dropdown.js \
	$(srcdir)/bootstrap-modal.js $(srcdir)/bootstrap-tooltip.js \
	$(srcdir)/bootstrap-popover.js $(srcdir)/bootstrap-scrollspy.js \
	$(srcdir)/bootstrap-tab.js $(srcdir)/bootstrap-typeahead.js

bootstrap: $(JS_SOURCES)
	cat $(JS_SOURCES) > $(builddir)/bootstrap.js
	${UGLIFYJS} -nc $(builddir)/bootstrap.js > $(builddir)/bootstrap.min.tmp.js
	echo "/*!\n* Bootstrap.js by @fat & @mdo\n* Copyright 2012 Twitter, Inc.\n* http://www.apache.org/licenses/LICENSE-2.0.txt\n*/" > $(builddir)/copyright.js
	cat $(builddir)/copyright.js $(builddir)/bootstrap.min.tmp.js > $(builddir)/bootstrap.min.js
	rm $(builddir)/copyright.js $(builddir)/bootstrap.min.tmp.js

clean-local:
	rm -rf $(builddir)/bootstrap.js $(builddir)/bootstrap.min.js

all-local: bootstrap
