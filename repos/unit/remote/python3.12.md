## `unit:python3.12`

```console
$ docker pull unit@sha256:7c1a786f552b2872158ad721eec334e6f4c8b3f05c237ad48b1218e8be5fdf7b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `unit:python3.12` - linux; amd64

```console
$ docker pull unit@sha256:e22aef5c1a256d1854e0b2e2e80290c7177fa2ff1ebc522bcbba476428f0acd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.7 MB (361742881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a201ad8b637438f174a18568152d9b65d01f33aac66e21f95e97589f51125cbf`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Tue, 26 Mar 2024 13:57:15 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 26 Mar 2024 13:57:15 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Mar 2024 13:57:15 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:57:15 GMT
ENV LANG=C.UTF-8
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 26 Mar 2024 13:57:15 GMT
ENV PYTHON_VERSION=3.12.4
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
ENV PYTHON_PIP_VERSION=24.0
# Tue, 26 Mar 2024 13:57:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Tue, 26 Mar 2024 13:57:15 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
CMD ["python3"]
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.title=Unit (python3.12)
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.version=1.32.1
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.32.1-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure python --config=/usr/local/bin/python3-config     && make -j $NCPU python3-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure python --config=/usr/local/bin/python3-config     && make -j $NCPU python3-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
STOPSIGNAL SIGTERM
# Tue, 26 Mar 2024 13:57:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 13:57:15 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Mar 2024 13:57:15 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a305f523084f0a28b5daf532a5216d9be05d863c6bd3f5bd2969965eb7e9a27`  
		Last Modified: Tue, 02 Jul 2024 02:01:21 GMT  
		Size: 15.8 MB (15764174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da238dd9d1f579bf4f3cd6589e3ab75747f8ea35be2bf50403f8f3fafa942eea`  
		Last Modified: Tue, 02 Jul 2024 02:01:35 GMT  
		Size: 54.6 MB (54588637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414da18c1936c380bc310a14aa9627a150fd6e6393e752068962869f27d2907c`  
		Last Modified: Tue, 02 Jul 2024 02:02:06 GMT  
		Size: 197.0 MB (197018307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db327cb5d518edab7990bc21871f629d8b92d6ea4e941403e1848ac9f0b67af1`  
		Last Modified: Wed, 10 Jul 2024 19:08:56 GMT  
		Size: 6.1 MB (6051065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9835e50bd47c9363c0efb540b5960f4d377c225f4f7cbae8da786d2e5414895`  
		Last Modified: Wed, 10 Jul 2024 19:08:56 GMT  
		Size: 23.2 MB (23153645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a5eaf0b1ca7b382e4a16ccdf8a549c8f8006094baaab9b1459788285297e65`  
		Last Modified: Wed, 10 Jul 2024 19:08:41 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f97980791357edf351608843b4e3a4596b238e94d0c145e7acfacc8f42bf29e`  
		Last Modified: Wed, 10 Jul 2024 19:08:55 GMT  
		Size: 2.8 MB (2797122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f22c57de2edb3d620604a8b8091d837d4894fb3e65e5d579887b6259182e7c`  
		Last Modified: Wed, 10 Jul 2024 19:56:17 GMT  
		Size: 7.3 MB (7285622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ecf3be1628adb25761b555f7f4334fd9a559998a15403645dc70511036360a`  
		Last Modified: Wed, 10 Jul 2024 19:56:17 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83402fe8c3fab780a0bae6268d151cf5c1adf01e38a15040331c53fe6b5bcae7`  
		Last Modified: Wed, 10 Jul 2024 19:56:17 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:python3.12` - unknown; unknown

```console
$ docker pull unit@sha256:b0954ef7989eb3526372074ecf5d52e80ef89eae6b1ccb39ae8d0f55688a722a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 KB (25724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295b90e895799b867f66918436cca78a1ca2d92fcfa179f87d8c1c82596536a9`

```dockerfile
```

-	Layers:
	-	`sha256:decb142058352fc64ba25147b255756791011b9e317d607b148ae51a7d4f3693`  
		Last Modified: Wed, 10 Jul 2024 19:56:17 GMT  
		Size: 25.7 KB (25724 bytes)  
		MIME: application/vnd.in-toto+json

### `unit:python3.12` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:3dc42ac45e3759e8360bbebf29e028af8b5f5ba01a96ec24a4f66fd228b7900a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.1 MB (353139297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c69148d316633a1f96880840154255a9bf9c6cf4001944c1b04610f3c79a2e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Tue, 26 Mar 2024 13:57:15 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Tue, 26 Mar 2024 13:57:15 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Mar 2024 13:57:15 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:57:15 GMT
ENV LANG=C.UTF-8
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 26 Mar 2024 13:57:15 GMT
ENV PYTHON_VERSION=3.12.4
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
ENV PYTHON_PIP_VERSION=24.0
# Tue, 26 Mar 2024 13:57:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Tue, 26 Mar 2024 13:57:15 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
CMD ["python3"]
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.title=Unit (python3.12)
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.version=1.32.1
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.32.1-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure python --config=/usr/local/bin/python3-config     && make -j $NCPU python3-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure python --config=/usr/local/bin/python3-config     && make -j $NCPU python3-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
STOPSIGNAL SIGTERM
# Tue, 26 Mar 2024 13:57:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 13:57:15 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Mar 2024 13:57:15 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d9ac7785741df545f96a8744d3a9a5c29f75a171fb8de0a0bae196294ad50`  
		Last Modified: Tue, 02 Jul 2024 04:02:37 GMT  
		Size: 15.7 MB (15749565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eeecfcb7b2ee9a8806953208440dbffd4b9110e5d2950924c7395e7ea3c070`  
		Last Modified: Tue, 02 Jul 2024 04:02:51 GMT  
		Size: 54.7 MB (54695057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c75f0ece8974d005f2532701f9fffb099d09a9bd1a53465b796982e4c2f594c`  
		Last Modified: Tue, 02 Jul 2024 04:03:16 GMT  
		Size: 189.9 MB (189935947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b835256a972db611db1dc22447abc4e61151696587fa8f12c3e8425854519ab5`  
		Last Modified: Tue, 02 Jul 2024 21:10:26 GMT  
		Size: 6.2 MB (6163663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65d3b86b487297cef6764548695672b2f7810e2699590dd63ef462817080bc1`  
		Last Modified: Tue, 02 Jul 2024 21:10:26 GMT  
		Size: 22.9 MB (22914552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987170d32e9712f4b8ac42b346609abcaa11245b9d7d399120e6855fed519e4f`  
		Last Modified: Wed, 03 Jul 2024 05:22:43 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c276c65e38d739bae4f95c03df333c1a22903e4d3a04c3db65ce84b8ccf4dac`  
		Last Modified: Wed, 10 Jul 2024 19:07:14 GMT  
		Size: 2.8 MB (2797105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cff42012d66fc0292a185d4ffb3101984e494d77888971b9d8ed33e6008313`  
		Last Modified: Wed, 10 Jul 2024 19:58:10 GMT  
		Size: 7.2 MB (7158811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c3402d712feb32af25a0f010b228d1e151c5844006584ff90b91c19d415951`  
		Last Modified: Wed, 10 Jul 2024 19:58:10 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c86e039b069b48c2b51a02bbb2e4f7bfeb89846ef7b439ae0642ce2481afb7e`  
		Last Modified: Wed, 10 Jul 2024 19:58:10 GMT  
		Size: 1.5 KB (1453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:python3.12` - unknown; unknown

```console
$ docker pull unit@sha256:3efe704238a80a7ca88d22b52fa9b1b6f725e044b1d2e6ccf8df4b4c413ce059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc583c36db20b60dc12849ae8aaf30c302ecc4d74d0ddd8b3e2576e5b1765370`

```dockerfile
```

-	Layers:
	-	`sha256:99ba5511755ff20cbb4e92360b3410d321a2c30548da5df374d23935286d5bbe`  
		Last Modified: Wed, 10 Jul 2024 19:58:09 GMT  
		Size: 26.2 KB (26204 bytes)  
		MIME: application/vnd.in-toto+json
