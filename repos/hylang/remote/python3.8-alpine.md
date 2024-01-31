## `hylang:python3.8-alpine`

```console
$ docker pull hylang@sha256:606453bd343d26f2aeff660441cc52113e31cc5d508f64549d8d2e8032658692
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

### `hylang:python3.8-alpine` - linux; amd64

```console
$ docker pull hylang@sha256:96ac17e8654304cc5ecb0eea01a66b9d4bf7afaa42818d6e7d49473b8fbb297e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (24036464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e740bb99981e35a2ce0645c1274d641bf375f88f9d6c090ee5a72c2d4e4ff1`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 19:34:36 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_VERSION=3.8.18
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca80dc46cecdd1a97787a1dd6f74263b9d2f7b0dd3e2e15c109f5e34848c932`  
		Last Modified: Sat, 27 Jan 2024 07:51:02 GMT  
		Size: 622.1 KB (622150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78523e2d4ecf2059c351f33624cbbcdd021b3018a661901b2ef0b1720f664d0e`  
		Last Modified: Sat, 27 Jan 2024 07:53:31 GMT  
		Size: 13.4 MB (13430006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd1224e940a20c4284895be4f8469fbe65686ce190a16ca655d9da396df6c6c`  
		Last Modified: Sat, 27 Jan 2024 07:53:29 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b96e5275f5f7bd58de7dc8e2cde562bc790fa1544bbe3fdccab96efc37e6b5`  
		Last Modified: Sat, 27 Jan 2024 07:53:30 GMT  
		Size: 2.9 MB (2851686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bdce4e59676a86428b1d9ab391e11596db140204a61cc675da841c3f5dc9cd`  
		Last Modified: Sat, 27 Jan 2024 08:53:43 GMT  
		Size: 3.7 MB (3723653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:c9ba73e84268d62f37800a7d8fa3f5db2a332ac646ec5f8b54d135912c034ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.0 KB (874956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d19533ab03d26540d4979be754eac5c44e21cb13cad2aba21fba32865419767`

```dockerfile
```

-	Layers:
	-	`sha256:7facfa511cf0eaf677012d7e3c10dc639fbd28b0a49b378593133e20aac5f459`  
		Last Modified: Sat, 27 Jan 2024 08:53:42 GMT  
		Size: 864.5 KB (864524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16a8307fb6ae9da71a76a243da87dfd18059b37003a76743325b59db8adad0d8`  
		Last Modified: Sat, 27 Jan 2024 08:53:42 GMT  
		Size: 10.4 KB (10432 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine` - linux; arm variant v6

```console
$ docker pull hylang@sha256:b09f7f21eb234dff8490b32dc9a0ce4ecad50cc9d88d3e903506508cb2344e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23464729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb5b7cf0a982d0fe654757d4bbe7abfc2c1dae497fed9ea4c9c5e1be6ce05bf`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 19:34:36 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_VERSION=3.8.18
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b53c3012ed72d5fef495f1a028562840d96a9a8f213ee53ccafb5f5ac2f66f`  
		Last Modified: Sat, 27 Jan 2024 09:09:07 GMT  
		Size: 623.4 KB (623370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3742bb044a0106ec2cee7953fe2273326c025983b0104a672986105c372afd6`  
		Last Modified: Sat, 27 Jan 2024 09:11:26 GMT  
		Size: 13.1 MB (13100195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5111cb01d9bdc8680ef1ae476418cb672b1eacda2f51f76fe0c8792895405b`  
		Last Modified: Sat, 27 Jan 2024 09:11:24 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca58466bb88d849f80e48b94da3e21d9c28b012249c73a729ef91c7ff3cc11a`  
		Last Modified: Sat, 27 Jan 2024 09:11:25 GMT  
		Size: 2.9 MB (2851688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a561a762a39ecd49c4fe206916c2a1754c89e9f0d9844991f1b1dc91e2da6f6d`  
		Last Modified: Tue, 30 Jan 2024 23:10:33 GMT  
		Size: 3.7 MB (3723837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:e7485efebc1ebc3ab31bd82d00219a6a7de2f19d49176ddeb5697e03d3700215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 KB (10319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9eb96bb106152c2fe1292884f1a251a02864c82f8a90012dbf1bf0e8707fea`

```dockerfile
```

-	Layers:
	-	`sha256:a952c3277adf1a042c8868116f49412895f5d4d897b1cad52699293479abef0c`  
		Last Modified: Tue, 30 Jan 2024 23:10:33 GMT  
		Size: 10.3 KB (10319 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine` - linux; arm variant v7

```console
$ docker pull hylang@sha256:6c346f8e941a0e1ee0ed0dd044b2e1784f70735ca2be37225bec435be106fcc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22830885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef43b0f794b7aa577afdc2499fe4b358f5e1cf6542aa9b0d1f8e9d14c6c7b04`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 19:34:36 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_VERSION=3.8.18
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0196bec49f2a69fdcb2616601ab1de1723d29440f95d478ab8ca13b3fa59c6`  
		Last Modified: Sat, 09 Dec 2023 02:18:07 GMT  
		Size: 621.9 KB (621916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80ea8e00e537f80edde08d4b40df67d17e631ca4afe44c8e89e3babf7fea49a`  
		Last Modified: Sat, 09 Dec 2023 02:21:14 GMT  
		Size: 12.7 MB (12714347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc548bcece79b41aaee84d415ca0aa430391fb1f634d0986fd9eb5a4ce393926`  
		Last Modified: Sat, 09 Dec 2023 02:21:12 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f835f5de5d4fc426ca5140dfd2406452749bfdfef3df0a298b834064bb94c30c`  
		Last Modified: Fri, 19 Jan 2024 04:12:18 GMT  
		Size: 2.9 MB (2851680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79641c5c96538364d5f67508498f4b038716fc29180a07f448ba39e2724b7658`  
		Last Modified: Fri, 19 Jan 2024 10:28:56 GMT  
		Size: 3.7 MB (3723998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:3a80e609c22fe0793a4d9ddcc115711aae4495f35d2661921969593e167f5034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **877.6 KB (877592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbabe34090d664a669f435e4519d152c32b0afc86d3152788ae8f7dc316c6f57`

```dockerfile
```

-	Layers:
	-	`sha256:26a2b12cafeeba69a7d979f779594ab0568c35c50603e7af72dae5c0885e16ef`  
		Last Modified: Fri, 19 Jan 2024 10:28:55 GMT  
		Size: 867.1 KB (867058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf7be9ff419a52906a4cebf3bb33ba96d66677e12e26184125628432bab409e5`  
		Last Modified: Fri, 19 Jan 2024 10:28:55 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:a17c97f27a8d2892f8969b03beb1c4b9bcdcf2dcda825625c4fd77bdc4229c45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24067013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44de39e8bb391dd4001884406984c600b507a40b5f4bca3610ccef3aab742220`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 19:34:36 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_VERSION=3.8.18
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190fa4880b84a89cd734aeddf7f4553ca139e4d53722c41c54d930662c13fec8`  
		Last Modified: Sat, 27 Jan 2024 07:25:43 GMT  
		Size: 625.2 KB (625198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ad13f9bdbcca7d421a8a92938bdde56ec293307482d9473cbcc473f1997d74`  
		Last Modified: Sat, 27 Jan 2024 07:28:04 GMT  
		Size: 13.5 MB (13518470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20135ae4668df90a7eaa18068eafedbb3535c4972372f94c91e748887edf88a`  
		Last Modified: Sat, 27 Jan 2024 07:28:02 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df913f771e805f7bc7199c9a7181505009014a8f8736d74ed4872474da741986`  
		Last Modified: Sat, 27 Jan 2024 07:28:03 GMT  
		Size: 2.9 MB (2851678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba8286f220e67502825760e1046679bdcba659276be188b6dceb50b4f9ff3ee`  
		Last Modified: Sun, 28 Jan 2024 00:30:04 GMT  
		Size: 3.7 MB (3723712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:cde44d24f4270a148e5f53f9787162e48af5081ea3271b8808f1709852975557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.0 KB (874993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f35e5e19b5f246f2b7e35f86fbbf01e38672476a78115c70dc25f047f37503`

```dockerfile
```

-	Layers:
	-	`sha256:4d540c36afd1d4b1d7fd4fc5f40fbeb23b3bde5036d06b66282124490444070e`  
		Last Modified: Sun, 28 Jan 2024 00:30:04 GMT  
		Size: 864.5 KB (864543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:835c1fb68ddfe1bd7849d52acc946e7b2f98f2199af7a26ec85c79e8ef62f1f2`  
		Last Modified: Sun, 28 Jan 2024 00:30:03 GMT  
		Size: 10.4 KB (10450 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine` - linux; 386

```console
$ docker pull hylang@sha256:92c91968b08e63c8a95640d54b4217d6135f4dc29fb7d34f759221303b6f7fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24096894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f85c2a6ad24c279ca1ba6725b6f7bce0f1e4caacb31905673c22b7cfedf41eb`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 19:34:36 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_VERSION=3.8.18
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7840a0a3a40a6b02ee9c509f8552e6bb70f9a8fb94398de1cfd742dc05d6050`  
		Last Modified: Sat, 27 Jan 2024 04:20:57 GMT  
		Size: 622.8 KB (622802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89aa1e3fbbf3d9c62866fd97592d6cdae2ba1cb06b57ff04c16e0b107f5a3dc`  
		Last Modified: Sat, 27 Jan 2024 04:23:44 GMT  
		Size: 13.7 MB (13654443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d681a853f947cc502fe7d26f8cea3f87bcba3c36642a3b7fa071ef3b9efecaa5`  
		Last Modified: Sat, 27 Jan 2024 04:23:41 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05aea78ce11b38db4f7b1c71bf52c70cd390caf73a0e235f5cc756a9461501be`  
		Last Modified: Sat, 27 Jan 2024 04:23:42 GMT  
		Size: 2.9 MB (2851678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cc4d8227a3b482ea4cd4c4fab7c4c76a5c53bee94ca920ddd16de5242f7aff`  
		Last Modified: Sat, 27 Jan 2024 04:52:01 GMT  
		Size: 3.7 MB (3723641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:e92d446d3951af35cf24e402a902f749dc1be0fee9fd49cac9b419e9962a54a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **874.9 KB (874862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1061a8705d2456c28f481c59b9aba18c888df2042147ff14762d739875b0c6c5`

```dockerfile
```

-	Layers:
	-	`sha256:4d542387e6d4fd5a3bec6c3d41ed3f03ece40f5923101866f300020de8fc3a72`  
		Last Modified: Sat, 27 Jan 2024 04:52:01 GMT  
		Size: 864.5 KB (864479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a8ebb46ff1abb98f2c5402fbc4681cdb6cb7220233d4fb0ade4204d08a9e258`  
		Last Modified: Sat, 27 Jan 2024 04:52:00 GMT  
		Size: 10.4 KB (10383 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine` - linux; ppc64le

```console
$ docker pull hylang@sha256:3c6148dbc50d290b84f09c86c02fb34f8e8e9aa80eab32b07be2a7ca8c86ae20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24462762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac95367f06ab11c2c57a09925a4357dc424058b652b9b59157ddb66d92eb0c25`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 19:34:36 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_VERSION=3.8.18
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d49a9cfe46131ab86b7a184f64865c97ae9d291935002bc7c38567ff27bc73`  
		Last Modified: Sat, 27 Jan 2024 06:51:52 GMT  
		Size: 625.6 KB (625581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86b95c77b7fde95f53ee81eaa59cd5a19e63eafc6338cc082c6142a9b9b692c`  
		Last Modified: Sat, 27 Jan 2024 06:54:40 GMT  
		Size: 13.9 MB (13903172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797f256c0786ef15d476762c1325c3f7d4b5247b3f813d4d4e3b5b1bb0767af4`  
		Last Modified: Sat, 27 Jan 2024 06:54:37 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e32f4436422499e17888ea6118ef3a36a9d454b9ab7c30695536e2be901ba4`  
		Last Modified: Sat, 27 Jan 2024 06:54:38 GMT  
		Size: 2.9 MB (2851669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437347df14c76697c50324f989bdf33c1beea08d38561519741ac8e536336e33`  
		Last Modified: Tue, 30 Jan 2024 04:10:21 GMT  
		Size: 3.7 MB (3723744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:6e890b4d84e78a07cc5fd5c3cdc9d57f7ada57b24ba64a1a9fed91743859d34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.4 KB (873440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0ddd1ad3e94cc62ea63c997eb2cfe6bf073cf68a15083d8cfbc65ab1278473`

```dockerfile
```

-	Layers:
	-	`sha256:848dceac4d0cfadd6fc48ecb17b79c0586b9f6de8ecc92d747ac2513bdaf80da`  
		Last Modified: Tue, 30 Jan 2024 04:10:21 GMT  
		Size: 862.9 KB (862946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6e6269f81022127baba4ef375f9097b01ff4f9621026a4b202b6b850bb483da`  
		Last Modified: Tue, 30 Jan 2024 04:10:20 GMT  
		Size: 10.5 KB (10494 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine` - linux; s390x

```console
$ docker pull hylang@sha256:037fc31505746f823a6b2dd617d74c9ba93b89c655600ea5b0c0f6e64c79831f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24152094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beef405b372cc35e2bc0d4843d3dc236ab5900c2d2dd576deb85c8a67176169d`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 19:34:36 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_VERSION=3.8.18
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0eaf7e0e09cbe2facbd632f110314332d4c2ef4f1f78231439620b76f1b07a`  
		Last Modified: Sat, 27 Jan 2024 04:06:00 GMT  
		Size: 623.4 KB (623391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d51f0376bc6193a813b52e5b70bee946ed7002683fa088303504d289109657c`  
		Last Modified: Sat, 27 Jan 2024 04:08:09 GMT  
		Size: 13.7 MB (13710445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd55d36e3f81a22923d9ac7113e301c143d1d2e74de1fad840d32d73deb5101`  
		Last Modified: Sat, 27 Jan 2024 04:08:06 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4febedfacbbd5349b46412e6adff2c5f6f56bdcdec81eebb06632bf2909f138a`  
		Last Modified: Sat, 27 Jan 2024 04:08:07 GMT  
		Size: 2.9 MB (2851690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd34d615e14ed478c8743b592b29f48aa50236eba56fe56e3fa930fa118d8be`  
		Last Modified: Mon, 29 Jan 2024 00:59:44 GMT  
		Size: 3.7 MB (3723690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:78d6f2509bb33a5a02ea37d1a3bb547086f365bb905883a7a0168a553c2608de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.3 KB (873320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39b7c70a1f4ef3db7d0a316c06898e89b926ce3e3e49c3a0187765f62c3dc2e`

```dockerfile
```

-	Layers:
	-	`sha256:50c7c12d18b67cd491779b38e45a1323916071697048327c3e15343669f1b80f`  
		Last Modified: Mon, 29 Jan 2024 00:59:44 GMT  
		Size: 862.9 KB (862888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdb2995eb3e55d705a6dfbcbbaad8c3234017dce6f8c4a6d77878ef3c66835a7`  
		Last Modified: Mon, 29 Jan 2024 00:59:44 GMT  
		Size: 10.4 KB (10432 bytes)  
		MIME: application/vnd.in-toto+json
