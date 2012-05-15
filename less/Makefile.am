bootstrap: $(srcdir)/*.less
	${RECESS} --compile $(srcdir)/bootstrap.less > \
		$(builddir)/bootstrap.css
	${RECESS} --compress $(srcdir)/bootstrap.less > \
		$(builddir)/bootstrap.min.css
	${RECESS} --compile $(srcdir)/bootstrap-responsive.less > \
		$(builddir)/bootstrap-responsive.css
	${RECESS} --compress $(srcdir)/bootstrap-responsive.less > \
		$(builddir)/bootstrap-responsive.min.css

clean-local:
	rm -rf $(builddir)/bootstrap.css
	rm -rf $(builddir)/bootstrap.min.css
	rm -rf $(builddir)/bootstrap-responsive.css
	rm -rf $(builddir)/bootstrap-responsive.min.css

all-local: bootstrap
