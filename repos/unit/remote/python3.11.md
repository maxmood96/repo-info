## `unit:python3.11`

```console
$ docker pull unit@sha256:3cad897c7f9bff0a905aa06d15945fcd1c6f21d2ecfdf97fd41fa2a3b6a0ff75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `unit:python3.11` - linux; amd64

```console
$ docker pull unit@sha256:209263daecc56261322ada37664f389314175996605e1b8aa554d52204962c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.7 MB (385663726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be96738f94c950ade07b3c87fc5886f774e285df1c2e7eec46916e4dbcf9308e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Mon, 09 Sep 2024 17:16:05 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.11.10
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.title=Unit (python3.11)
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.version=1.33.0
# Tue, 17 Sep 2024 21:10:58 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.33.0-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure python --config=/usr/local/bin/python3-config     && make -j $NCPU python3-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure python --config=/usr/local/bin/python3-config     && make -j $NCPU python3-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Tue, 17 Sep 2024 21:10:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 21:10:58 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Tue, 17 Sep 2024 21:10:58 GMT
STOPSIGNAL SIGTERM
# Tue, 17 Sep 2024 21:10:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 17 Sep 2024 21:10:58 GMT
EXPOSE map[80/tcp:{}]
# Tue, 17 Sep 2024 21:10:58 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5f3b3f727e71a2c8e2d282f958aa488342e7a0edc7c26d994f1dbbb88c88d`  
		Last Modified: Thu, 17 Oct 2024 01:09:47 GMT  
		Size: 24.1 MB (24053088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba0b3d08b81baa192d30dbb2257b8227f2a4eab719c79ef1c419e3a07b39dbc`  
		Last Modified: Thu, 17 Oct 2024 01:10:04 GMT  
		Size: 64.4 MB (64393080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bc85537ac7c401eea9ed38d4a75fddbe5d75d5570921f1c435a8342b3cef15`  
		Last Modified: Thu, 17 Oct 2024 01:10:40 GMT  
		Size: 211.3 MB (211281151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6c177f22dfcd57ee63453f952efdd59e8df03bb97a6c98d04adce4631a61af`  
		Last Modified: Thu, 17 Oct 2024 03:04:54 GMT  
		Size: 6.2 MB (6161671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad5f8f8c5217c851888f627c64e4cc5098e6b693d194598c8a516f6d4a4c526`  
		Last Modified: Thu, 17 Oct 2024 03:04:54 GMT  
		Size: 23.0 MB (22970186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041c0e254e0a3c3d98f3dec24580507f64886960310ddea600b9b20c45a1ca95`  
		Last Modified: Thu, 17 Oct 2024 03:04:53 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df003cc40ba5b8f54887f5e1a94714030240dac48b72c203203d5969d00ea6d1`  
		Last Modified: Thu, 17 Oct 2024 03:54:56 GMT  
		Size: 7.2 MB (7246566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bf5c3b039bc3027ed2c09b5b9f39a5a07c05ca8cdde771908a9908132d18f2`  
		Last Modified: Thu, 17 Oct 2024 03:54:55 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc64c1384c22bb2930a02651a50eb70d83107fde63d0bb496739068342becc4`  
		Last Modified: Thu, 17 Oct 2024 03:54:55 GMT  
		Size: 1.5 KB (1451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:python3.11` - unknown; unknown

```console
$ docker pull unit@sha256:6710b7dc9395573529f197ad304743385250a78621aabbfbdef214aff911a492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 KB (24310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1519f8c6cb9a5cc87eed412aaad39395de613aa45decb4b76b44fe4321ba66f5`

```dockerfile
```

-	Layers:
	-	`sha256:33bea16500d7cffc35721277859c387184fca387692d3042636f09cb123d513f`  
		Last Modified: Thu, 17 Oct 2024 03:54:55 GMT  
		Size: 24.3 KB (24310 bytes)  
		MIME: application/vnd.in-toto+json

### `unit:python3.11` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:7a1e4e17065bcd2b1cd876cf5362f7cd1a6716910592c37e9f287874371bb38c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.2 MB (376212614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e570b393974444428fcd73cb277a6c6d0bf0f4c171e417f168591ee6806b25c1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Mon, 09 Sep 2024 17:16:05 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.11.10
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.title=Unit (python3.11)
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.version=1.33.0
# Tue, 17 Sep 2024 21:10:58 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.33.0-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure python --config=/usr/local/bin/python3-config     && make -j $NCPU python3-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure python --config=/usr/local/bin/python3-config     && make -j $NCPU python3-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Tue, 17 Sep 2024 21:10:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 21:10:58 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Tue, 17 Sep 2024 21:10:58 GMT
STOPSIGNAL SIGTERM
# Tue, 17 Sep 2024 21:10:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 17 Sep 2024 21:10:58 GMT
EXPOSE map[80/tcp:{}]
# Tue, 17 Sep 2024 21:10:58 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71ace0e8bbdcfcf795b836e24a37a6ed0054100e14d6aa6e5a63f7e162ba729`  
		Last Modified: Fri, 27 Sep 2024 05:25:40 GMT  
		Size: 202.7 MB (202651718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d992156d02900e3e9b3a86877cba5b4e759b6c14a78da7bf223a2588bb4474`  
		Last Modified: Fri, 27 Sep 2024 20:25:51 GMT  
		Size: 6.2 MB (6239190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f9ca32b9611bd04b19b7519b801a1865b4b7dc5af434df65f8eaf6354f8bf`  
		Last Modified: Fri, 27 Sep 2024 21:08:13 GMT  
		Size: 22.6 MB (22623752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff88331bae54594b92d8bde7195f0a144a5cc94e1a9370e247b2fcd43d58fe9`  
		Last Modified: Fri, 27 Sep 2024 21:08:12 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7afde374aca0d1bfdade0eb98259b6f1d18f06f0c6b82605ebac0b4609fed7b`  
		Last Modified: Sat, 28 Sep 2024 01:12:53 GMT  
		Size: 7.2 MB (7166367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475fd85ac4cad01421c3623153fc6f7fce5e86bfd98b4fc23701acde94162f3e`  
		Last Modified: Sat, 28 Sep 2024 01:12:52 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd6084850e10121385703c8c41a253b6f7b5fe2e662bc8466407aeb027a2a07`  
		Last Modified: Sat, 28 Sep 2024 01:12:52 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:python3.11` - unknown; unknown

```console
$ docker pull unit@sha256:410c9e5a180e93497605a3da0ea0d3754d79ff6de215d45665a31441de3de7bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e453cc0ae95c3935ef2f6c4d250f43169dcc5b6bf4ad3a6dc4382687ddbdb7a2`

```dockerfile
```

-	Layers:
	-	`sha256:df8069253c0ad6b1cf7aca1af54c9bf726d19cf3e370b0381acb892655557d54`  
		Last Modified: Sat, 28 Sep 2024 01:12:52 GMT  
		Size: 24.7 KB (24728 bytes)  
		MIME: application/vnd.in-toto+json
