## Process this file with automake to produce Makefile.in

scriptsdir = $(pkgdatadir)

dist_scripts = \
	compile \
	depcomp \
	install-sh \
	missing \
	version-sh

version_sh = version-sh


version-sh:
	@echo '#!/bin/sh' > ${version_sh}; \
	echo '' >> ${version_sh}; \
	echo 'umask 133' >> ${version_sh}; \
	echo 'version_string=`git describe --tags`;' >> ${version_sh}; \
	echo 'if [ -n "${version_string}" ]; then' >> ${version_sh}; \
	echo '	echo "${version_string}" > jamrouter-version' >> ${version_sh}; \
	echo 'else' >> ${version_sh}; \
	echo '	version_string=`cat jamrouter-version`' >> ${version_sh}; \
	echo 'fi' >> ${version_sh}; \
	echo 'echo "${version_string}"' >> ${version_sh}; \
	chmod 755 ${version_sh}


install-data-local:


uninstall-hook:


clean-local:


distclean-local:
	rm -f *~

