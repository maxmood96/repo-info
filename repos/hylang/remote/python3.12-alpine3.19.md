## `hylang:python3.12-alpine3.19`

```console
$ docker pull hylang@sha256:ca7e05261061880a5ce613ae3293ee54ea1ed435a35664985bf0c32dbfa13522
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `hylang:python3.12-alpine3.19` - linux; amd64

```console
$ docker pull hylang@sha256:43237735fc58a454ec0fbf15d66919e606eff2fff4c0c69675ec8c05228a05d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25383074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44077a2bdeea9e676d7a10055f54cf5d040f3a699596916e8cf535fad86b8703`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.12.8
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea565e07506c73142edb3ec06823e48cdabb5e16842b95f117eda5e634ac768`  
		Last Modified: Wed, 04 Dec 2024 20:36:20 GMT  
		Size: 627.9 KB (627928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca4cf76217bf89264f874579af5a0383779ed3bc9e122f72637aff5dfd85baa`  
		Last Modified: Wed, 04 Dec 2024 20:36:20 GMT  
		Size: 15.7 MB (15732855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159747cf9921b0f5849aa0f2f4e78a784812cf2904a7d84cead77ce13a5e9e39`  
		Last Modified: Wed, 04 Dec 2024 20:36:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b675c4dc2c46d4d644efc474896d4e999fa140d28bc19249bb89e5bca166c00`  
		Last Modified: Wed, 04 Dec 2024 21:10:08 GMT  
		Size: 5.6 MB (5602316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:3fe16dbc95310be7b82de1a1362bfde1e92319873b8bb1b2952762298f393fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1039280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66232a88570057f5a15c01b1f91412c7b84d1db2d0d5abd5c1b4b392da57509f`

```dockerfile
```

-	Layers:
	-	`sha256:4eae58502ecea70113694801fc412734cdd84a6681f9de7791fcf5fad96490e2`  
		Last Modified: Wed, 04 Dec 2024 21:10:08 GMT  
		Size: 1.0 MB (1031243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb1cdc38f7bc27fe81dca680dcc949eca5fd32f57eb292f68aba02758ed678c7`  
		Last Modified: Wed, 04 Dec 2024 21:10:08 GMT  
		Size: 8.0 KB (8037 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.19` - linux; arm variant v6

```console
$ docker pull hylang@sha256:ac4e94378bad930c5d61f905aa34bb2e9b3ad4c036748d90e02c6454627e0012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24365016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ee0efb35b3ae00fc7ecafb7e7159419eddd6f03cd48350459512774fc5e76e`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.12.8
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2431344f9ef4c8213d672cda2b6e387e95583c1e88274bffbb69202bfcc5ffc7`  
		Last Modified: Tue, 12 Nov 2024 14:28:12 GMT  
		Size: 628.8 KB (628823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09832e4a834ff6bbf31dd2e4fe01f3686af5954182e0674c5f116cc754b6d6f`  
		Last Modified: Wed, 04 Dec 2024 20:58:56 GMT  
		Size: 15.0 MB (14957211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692234045e762802d53d972e50a8d3a7fb8e84373cb47325519d7c50fd3b9edf`  
		Last Modified: Wed, 04 Dec 2024 20:58:55 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4e51e654b65f31b4a61389d9a7fb829c98558c92e36e343882bf247bb2b4dd`  
		Last Modified: Wed, 04 Dec 2024 21:27:29 GMT  
		Size: 5.6 MB (5602301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:60967fbdbf02a4849043314d72ced94b8a604cdab34c8ed56609f48de7b8dab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f4f71aa22ecba3850aba8b09be20b61d6000eff949818c5d80c20ba5e9910d`

```dockerfile
```

-	Layers:
	-	`sha256:2dae0c2f70cf31a7d48d9965a3d0f4fdc0024567f1448b4c32cc28264a00d0ce`  
		Last Modified: Wed, 04 Dec 2024 21:27:28 GMT  
		Size: 7.9 KB (7898 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.19` - linux; arm variant v7

```console
$ docker pull hylang@sha256:a0fad4251d9e3f0565c805b88292e86682eb5d2b6a9194224fdbf75eb4c75c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23569558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c160558666343ef5f7ab84ec6fc98c3a0ebc7c0c5f5c4af6c82549f62b5cb9`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.12.8
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:02dfd5e2e7e47e8d8f9020a0d7f4d8240d6646afc6a52b168c0899bc0c3d06a3`  
		Last Modified: Mon, 09 Sep 2024 07:03:23 GMT  
		Size: 2.9 MB (2927731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c2f9787048526330ac7cda8db975c894470c98d98a1f85506dcce30d2b788d`  
		Last Modified: Wed, 04 Dec 2024 23:50:18 GMT  
		Size: 628.0 KB (627971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1833f01b4aa9e24234417bb6f3f314c15e67045dd89b12a7668b0d3e0626c2a`  
		Last Modified: Wed, 04 Dec 2024 23:50:18 GMT  
		Size: 14.4 MB (14411253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f3b4be9fde2778058a774648d4100bac336a06aee0e1fdbfff49ba4dccd8e2`  
		Last Modified: Wed, 04 Dec 2024 23:50:18 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bd0970fdb556f5c8b445b2230eda07fe9e720484849d3321522bea42c99fd9`  
		Last Modified: Thu, 05 Dec 2024 03:06:49 GMT  
		Size: 5.6 MB (5602354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:4ec18e517cf2d3a849a6e061e656d66f83f8e03847719bc974f6054d700b7f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1042256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf92ed751286b85ef409896df3a70298a6986e5555d8ef735e7125371f5c51c`

```dockerfile
```

-	Layers:
	-	`sha256:b7c1bd2afde9dbdf517f05e6c34a86728f5d746af13ba96f4a35b61ec7ba01c3`  
		Last Modified: Thu, 05 Dec 2024 03:06:48 GMT  
		Size: 1.0 MB (1034143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8fc98e87230a4c86e2b0dfccc8de1a54994fc08164ed54c5cf0308ecce2864`  
		Last Modified: Thu, 05 Dec 2024 03:06:48 GMT  
		Size: 8.1 KB (8113 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:77f1d06a6ed5c1eee9f7dd408bb55feeb72df157b643364248b4b32a32f58841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25291074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6a98b91e4fdf96a3ab2a25d9d3133f462538631331b2e89a39db35b0a08e11`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.12.8
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8807c905fe7992682192bc630b9c68d1ca8b7b640529650c9556b2c63601bac1`  
		Last Modified: Wed, 04 Dec 2024 22:54:27 GMT  
		Size: 630.3 KB (630347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d77cd4355c56e3192c408cb3482fd33833015e11edaf089f2ffed3f6261954d`  
		Last Modified: Wed, 04 Dec 2024 22:54:27 GMT  
		Size: 15.7 MB (15698778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad024009b6286e208d083d433a66fdeb1c60d704cf1db46b53caba041767784`  
		Last Modified: Wed, 04 Dec 2024 22:54:27 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4684627e4e440fa10fe4fa067bee29f2a17802b94f2f563d2c81f89e71e4d8d2`  
		Last Modified: Thu, 05 Dec 2024 01:11:57 GMT  
		Size: 5.6 MB (5602453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:83ac8b20e82b3a373d5c6362f04d7477aa9d2c87e073e42f9a504d6f1019cedf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1039440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd7707c36f52ba3ae9a7d8b57f3a2f9248726a738bbb949032a795736ad6a84`

```dockerfile
```

-	Layers:
	-	`sha256:cb79b90dd9848de7e66e9108d8094b03b5991079fc0dbeab5871d180cf8fa8d7`  
		Last Modified: Thu, 05 Dec 2024 01:11:57 GMT  
		Size: 1.0 MB (1031299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3c68de99dd4c27207aad3de3390306790a9ea3ded74233b641a02304b011c53`  
		Last Modified: Thu, 05 Dec 2024 01:11:56 GMT  
		Size: 8.1 KB (8141 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.19` - linux; 386

```console
$ docker pull hylang@sha256:7804799132e70a2da0aecc7a9b96d88591033d93bd87517836fcfa9789947566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25261523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca4bd513c2ce7e1552f59eb74bf029eaaedcb6fd9d8d8d9f7ebbbcfc4633119`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.12.8
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daf1a4c11c7b1b580ed2ef786451f308d833ba96d4c90d8e6be3e04e714c6ff`  
		Last Modified: Wed, 04 Dec 2024 20:36:05 GMT  
		Size: 628.4 KB (628431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8380b9123acd58c4c48d915a6c35d2de4a7feb46d8fcdc548af31ca529e09f8c`  
		Last Modified: Wed, 04 Dec 2024 20:36:05 GMT  
		Size: 15.8 MB (15776926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1389e1156cc1d1ce4645585706123b13c8a9e056d8fb395c85e846505782fec2`  
		Last Modified: Wed, 04 Dec 2024 20:36:05 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5622c784a690661a46112d38f79e57c0966989165c5c25f6720ea51d089924b6`  
		Last Modified: Wed, 04 Dec 2024 21:10:19 GMT  
		Size: 5.6 MB (5602252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:77960ae3705fe0d82d7b03feacc5f5f086d393ebb4ee479e6b498c372888d062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1039222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6bd2c6f172b1419bb40f6bd718cd74f07ed90fccf5c5fc8a41d569ff09c6323`

```dockerfile
```

-	Layers:
	-	`sha256:3ab894ba6a55e376fbad9852ec6f655d564523144ac7f872e716d0d15955e43e`  
		Last Modified: Wed, 04 Dec 2024 21:10:18 GMT  
		Size: 1.0 MB (1031218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a98cc87a0915a9a16069a4838e64b74c188eb394f6f120240b089ec5fbf3c0d`  
		Last Modified: Wed, 04 Dec 2024 21:10:18 GMT  
		Size: 8.0 KB (8004 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.19` - linux; ppc64le

```console
$ docker pull hylang@sha256:8e004a87cd4ded216c9dd786be3d83b1e1df17262246caed64d0742648abe042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 MB (25924883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7874e5d4dfa8323daa52ff991d377e0365e67ae48a6aed697cd256d89c54a3`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.12.8
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a3b208fb93d4b6ab11a15715a17ef854a2307e9102b287f01460c628f471ab`  
		Last Modified: Wed, 04 Dec 2024 22:06:33 GMT  
		Size: 630.8 KB (630823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371ce61e2b49802d476c2d6733f80c727544cfcf086cf45d917604a52ee3bf43`  
		Last Modified: Wed, 04 Dec 2024 22:06:34 GMT  
		Size: 16.3 MB (16326908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d8b2c78f5f4b815c2b26e3592f1a1e42175477bf37a09f98065a528149c70b`  
		Last Modified: Wed, 04 Dec 2024 22:06:33 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419f1b6ee1e1a7820f5a0bcb3adfc011e7b63fa8505006c0a3e44802904eb427`  
		Last Modified: Thu, 05 Dec 2024 00:07:19 GMT  
		Size: 5.6 MB (5602405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:af7432e070c2b96d4c872ce56e01819dd9c52a04eb2f3a51d2797a63e9385aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1037403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df07bc3791cf31d3de87a7cedc5e2aec44f921f47aa479c64b2f35842736b312`

```dockerfile
```

-	Layers:
	-	`sha256:94672844b4bc05c7ee3329ab3a7fdb31a70e9d1b3f35fd4016d96377e25d3aae`  
		Last Modified: Thu, 05 Dec 2024 00:07:19 GMT  
		Size: 1.0 MB (1029323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a725b7a062ca736f38277f1b6b32f4a3e365916a1cf12fac4661df868b3df41e`  
		Last Modified: Thu, 05 Dec 2024 00:07:18 GMT  
		Size: 8.1 KB (8080 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.19` - linux; s390x

```console
$ docker pull hylang@sha256:4205dcc1255dd47b248f62da94ee3567f479dc644b69908ed345aaf4ff79a342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25447535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194cb18c9563ca6bc87042f452089ce8da555e557963cb208d975b293e889a5d`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.12.8
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958d33515d223f7b57730bc71831734e07e677ed82e4f416a0ad37a98d1e7fee`  
		Last Modified: Wed, 04 Dec 2024 21:56:21 GMT  
		Size: 629.0 KB (628997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbbb2421176711b0fffacecf76ef525cb6243f12d75a32edcfbe49cb820df3d`  
		Last Modified: Wed, 04 Dec 2024 21:56:22 GMT  
		Size: 16.0 MB (15962620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c964a2945b94c875eed61dcf52e8318cc8845d7de68242bf6b244123bd45c37a`  
		Last Modified: Wed, 04 Dec 2024 21:56:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e1098215ea9bfc74de2b8d3da65c0d33ebafa7d2c29f9f4d818e6d398c8592`  
		Last Modified: Wed, 04 Dec 2024 23:45:58 GMT  
		Size: 5.6 MB (5602273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:1326e575b76188a92a3e2af9d5047a018546c5282761cd3222eba21f831b3340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1037326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805a43ffb085ae028f4008836d7e2237117e1b81dd7493e5f013cf8deda5c6a2`

```dockerfile
```

-	Layers:
	-	`sha256:4cd9ee1685c648e79b723988c5ba33ac451b2ed152a03aff5f56bd0fdcf42e5e`  
		Last Modified: Wed, 04 Dec 2024 23:45:58 GMT  
		Size: 1.0 MB (1029289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff5bc7f56a423403c12270568541fdd537469e524555cbdd6ca658fe54b8744c`  
		Last Modified: Wed, 04 Dec 2024 23:45:58 GMT  
		Size: 8.0 KB (8037 bytes)  
		MIME: application/vnd.in-toto+json
