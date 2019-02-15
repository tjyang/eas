##############################################################################
# rpm making automation for CentOS/RHEL.

ARCH ?= $(shell arch)
ifeq ($(ARCH),x86_64)
RPM_ARCH := x86_64
else
    ifeq ($(ARCH),i686)
RPM_ARCH := i386
    else
$(error Unknown arch "$(ARCH)".)
    endif
endif

MWD=/tmp


clean:
	@(sudo rm -f ../eas-2.0.0.tgz *.rpm *~ ../*~)
#	@(sudo rm -f ../sudosh.1 ../sudosh-replay.8 ../sudosh.conf.5 ../config.h ../stamp-h1 ../config.log) 
#	@(sudo rm -rf ../autom4te.cache ../config.guess ../config.sub ../config.status ../Makefile)
rpm:
	# create eas tar ball.
	@(cd ..;rm -f eas-2.0.0.tar.gz)
	@(cd ..;make dist)
	# build the rpm using rpmbuild from ./rmbuild as topdir
	@sudo rm -rf *.rpm ${MWD}/rpmbuild && mkdir -p ${MWD}/rpmbuild/{BUILD,RPMS,SOURCES,SPECS,SRPMS}
	@cp  ../eas-2.0.0.tar.gz ${MWD}/rpmbuild/SOURCES/eas-2.0.0.tar.gz
	@sudo rpmbuild -ba --define "_topdir ${MWD}/rpmbuild"   ./eas.spec
	@sudo mv ${MWD}/rpmbuild/RPMS/$(RPM_ARCH)/*.rpm .
	@ls -l *.rpm
