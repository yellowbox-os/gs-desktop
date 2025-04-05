# Makefile

check_root:
	@if [ $$(id -u) -ne 0 ]; then \
		echo "This Makefile must be run as root or with sudo."; \
		exit 1; \
	fi

install: system local

system: check_root
	WORKDIR=`pwd`; \
	mkdir -p /System/Library; \
	cp -R Library/* /System/Library; \
	. /System/Library/Preferences/GNUstep.conf; \
	CPUS=`nproc`; \
	export GNUSTEP_INSTALLATION_DOMAIN="LOCAL"; \
	echo "CPUS is set to: $$CPUS"; \
	echo "GNUSTEP_INSTALLATION_DOMAIN is set to: $$GNUSTEP_INSTALLATION_DOMAIN"; \
	echo "WORKDIR is set to: $$WORKDIR"; \
	cd $$WORKDIR/Addresses && gmake -j"${CPUS}" || exit 1 || exit 1 && gmake install && gmake clean; \
	cd $$WORKDIR/Affiche && gmake -j"${CPUS}" || exit 1 || exit 1 && gmake install && gmake clean; \
	cd $$WORKDIR/Calculator && gmake -j"${CPUS}" || exit 1 || exit 1 && gmake install && gmake clean; \
	cd $$WORKDIR/DefaultsManager && gmake -j"${CPUS}" || exit 1 || exit 1 && gmake install && gmake clean; \
	cd $$WORKDIR/DictionaryReader && gmake -j"${CPUS}" || exit 1 || exit 1 && gmake install && gmake clean; \
	cd $$WORKDIR/FTP && gmake -j"${CPUS}" || exit 1 || exit 1 && gmake install && gmake clean; \
	cd $$WORKDIR/InnerSpace && gmake -j"${CPUS}" || exit 1 || exit 1 && gmake install && gmake clean; \
	cd $$WORKDIR/OpenUp && gmake -j"${CPUS}" || exit 1 || exit 1 && gmake install && gmake clean; \
	cd $$WORKDIR/RemoteView && gmake -j"${CPUS}" || exit 1 || exit 1 && gmake install && gmake clean; \
	cd $$WORKDIR/ScanImage && gmake -j"${CPUS}" || exit 1 || exit 1 && gmake install && gmake clean; \
	cd $$WORKDIR/Sketch && gmake -j"${CPUS}" || exit 1 || exit 1 && gmake install && gmake clean; \

	fi;
