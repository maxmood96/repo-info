## `hylang:python3.8-alpine3.14`

```console
$ docker pull hylang@sha256:a1b7d6d01296f1172690b24285ec010339864d30e92e69e43f1b8e05e7c2423d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hylang:python3.8-alpine3.14` - linux; amd64

```console
$ docker pull hylang@sha256:2b3453a676d60a0294c8d3890a648aba7c085ddd73dd9adc56f557471fcf41b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19269750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fe3d750805dc2a0e9dbb71d41999b87c839d077008af6f2211a3313ac33bd0`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 23:58:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 02:36:52 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 04:03:25 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Sat, 13 Nov 2021 04:03:26 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 13 Nov 2021 04:03:26 GMT
ENV PYTHON_VERSION=3.8.12
# Sat, 13 Nov 2021 04:09:32 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Sat, 13 Nov 2021 04:09:33 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 13 Nov 2021 04:09:33 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Sat, 13 Nov 2021 04:09:33 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Sat, 13 Nov 2021 04:09:34 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Sat, 13 Nov 2021 04:09:34 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Sat, 13 Nov 2021 04:09:40 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 13 Nov 2021 04:09:41 GMT
CMD ["python3"]
# Tue, 11 Jan 2022 00:21:08 GMT
ENV HY_VERSION=1.0a4
# Tue, 11 Jan 2022 00:21:08 GMT
ENV HYRULE_VERSION=0.1
# Tue, 11 Jan 2022 00:21:13 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 11 Jan 2022 00:21:13 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1c01f59fcc7f7c93b7819b80102de4622e5b448ebf68120a07bc88366cc08a`  
		Last Modified: Sat, 13 Nov 2021 04:58:31 GMT  
		Size: 282.0 KB (281960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff57dacc9b2e5b45a9520394c6c64071f30bc19f5a2436f8df7eb7916b89b85`  
		Last Modified: Sat, 13 Nov 2021 04:58:34 GMT  
		Size: 11.2 MB (11236960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a883406ff56fddb97ebd1ae0bfad837af6f13cbb11a623636822dc48b57123`  
		Last Modified: Sat, 13 Nov 2021 04:58:31 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48d66fa9d87870657ad21d9c86bd69e614143903657983169300845c0498019`  
		Last Modified: Sat, 13 Nov 2021 04:58:32 GMT  
		Size: 2.3 MB (2349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e96fac5232e0db980410bd60a31398c736b3f569ea9cd61c7cc6c8facd0c6c7`  
		Last Modified: Tue, 11 Jan 2022 00:26:29 GMT  
		Size: 2.6 MB (2578546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8-alpine3.14` - linux; arm variant v6

```console
$ docker pull hylang@sha256:8d8ec985c83656dbea91ea461788ab16641f58f16cdcf953a8a4fdd39db0ca88
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19101582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f54b385b961bdde945a464be0ec9fcc37d5b727fc31a89dd45dd384fa0659f5`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:41:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Nov 2021 18:41:19 GMT
ENV LANG=C.UTF-8
# Fri, 12 Nov 2021 18:41:23 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Fri, 12 Nov 2021 20:33:09 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 29 Jan 2022 03:06:11 GMT
ENV PYTHON_VERSION=3.8.12
# Sat, 29 Jan 2022 03:17:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 	cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 29 Jan 2022 03:17:39 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Sat, 29 Jan 2022 03:17:40 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Sat, 29 Jan 2022 03:17:40 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Sat, 29 Jan 2022 03:17:40 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Sat, 29 Jan 2022 03:17:41 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Sat, 29 Jan 2022 03:17:57 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	; 	rm -f get-pip.py
# Sat, 29 Jan 2022 03:17:57 GMT
CMD ["python3"]
# Sat, 29 Jan 2022 04:49:03 GMT
ENV HY_VERSION=1.0a4
# Sat, 29 Jan 2022 04:49:03 GMT
ENV HYRULE_VERSION=0.1
# Sat, 29 Jan 2022 04:49:11 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Sat, 29 Jan 2022 04:49:11 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f5468f2f6e403f83bd2b163e2371fd5e7ed62ebbe7ea097b54c818e4c65adc`  
		Last Modified: Sat, 13 Nov 2021 00:08:03 GMT  
		Size: 683.0 KB (682987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc31511bcccde19f3457aeff359453a4daecf87f2930d817e99782461f74029`  
		Last Modified: Sat, 29 Jan 2022 04:02:44 GMT  
		Size: 10.9 MB (10855075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fcf34854b8fb3e19f073701fbd889fd316f7c412a3d1da1cb9dd999385dd72`  
		Last Modified: Sat, 29 Jan 2022 04:02:37 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f026539cf7aa34e183776e1de406272bcfc153bf34dad59dd9cffef95ff88e8`  
		Last Modified: Sat, 29 Jan 2022 04:02:39 GMT  
		Size: 2.3 MB (2349231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f97c34d2f77bbd40244b2a0af31389001b97e59e390b07da8b0213ad3c6572`  
		Last Modified: Sat, 29 Jan 2022 04:54:12 GMT  
		Size: 2.6 MB (2578665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8-alpine3.14` - linux; arm variant v7

```console
$ docker pull hylang@sha256:718d2b53adb389aa7990d68fb8b3c7577d238dd64edd90e209e755a41a504954
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17998894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4acbd9854d1f605bea7cd434e61bd89aeb42578bc89129261707f1768bf7e687`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:06:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Nov 2021 21:06:53 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 00:38:11 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Sat, 13 Nov 2021 00:38:11 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 13 Nov 2021 00:38:12 GMT
ENV PYTHON_VERSION=3.8.12
# Sat, 13 Nov 2021 00:48:36 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Sat, 13 Nov 2021 00:48:38 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 13 Nov 2021 00:48:38 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Sat, 13 Nov 2021 00:48:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Sat, 13 Nov 2021 00:48:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Sat, 13 Nov 2021 00:48:40 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Sat, 13 Nov 2021 00:48:55 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 13 Nov 2021 00:48:56 GMT
CMD ["python3"]
# Tue, 11 Jan 2022 01:02:44 GMT
ENV HY_VERSION=1.0a4
# Tue, 11 Jan 2022 01:02:45 GMT
ENV HYRULE_VERSION=0.1
# Tue, 11 Jan 2022 01:02:53 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 11 Jan 2022 01:02:53 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79d0ac51eb5f836fa91faeb9a77f15f4b94debe8d198099a2f699704283c145`  
		Last Modified: Sat, 13 Nov 2021 02:14:01 GMT  
		Size: 281.3 KB (281272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92111eab06955f8d3f634bd17987f44ac75a904d3e1395845011980c2ae8693`  
		Last Modified: Sat, 13 Nov 2021 02:14:07 GMT  
		Size: 10.4 MB (10350900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559515da7be6e62162fe55e84089a354fa234498ded9da052461d8abd9f8ee02`  
		Last Modified: Sat, 13 Nov 2021 02:14:01 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b005d8ad3c81a0dddb086154bf5bc03c599f7fc7d0444a037a29fcbda2b75a1`  
		Last Modified: Sat, 13 Nov 2021 02:14:03 GMT  
		Size: 2.3 MB (2349152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6763d3865944655f08f3edc1815aaf529a465f7c5a4ae72f369ea89b656842ff`  
		Last Modified: Tue, 11 Jan 2022 01:12:19 GMT  
		Size: 2.6 MB (2578720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:30b7d5019ba03043e9a9573bcb972a3b29a53fa11c03cd2aa9441a0470a3dcbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19230151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646ef1515f8cca79065b201017dd01255669204d3047e723e643719a7c0a9859`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:36:28 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Nov 2021 21:36:29 GMT
ENV LANG=C.UTF-8
# Fri, 12 Nov 2021 22:51:25 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Fri, 12 Nov 2021 22:51:26 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 12 Nov 2021 22:51:27 GMT
ENV PYTHON_VERSION=3.8.12
# Fri, 12 Nov 2021 22:56:42 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 12 Nov 2021 22:56:43 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 12 Nov 2021 22:56:43 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Fri, 12 Nov 2021 22:56:44 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Fri, 12 Nov 2021 22:56:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Fri, 12 Nov 2021 22:56:46 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Fri, 12 Nov 2021 22:56:53 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 12 Nov 2021 22:56:54 GMT
CMD ["python3"]
# Tue, 11 Jan 2022 00:42:17 GMT
ENV HY_VERSION=1.0a4
# Tue, 11 Jan 2022 00:42:18 GMT
ENV HYRULE_VERSION=0.1
# Tue, 11 Jan 2022 00:42:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 11 Jan 2022 00:42:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05aeb984f21061c6aea8489e65bd68a3ec292e9cba160566d11a942d487b550d`  
		Last Modified: Fri, 12 Nov 2021 23:39:44 GMT  
		Size: 281.9 KB (281928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6143fbdccc3a89a9a026d9a81a3a34dde138033eef04ed273857548b595ae7`  
		Last Modified: Fri, 12 Nov 2021 23:39:46 GMT  
		Size: 11.3 MB (11301953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df4657a6df88dd63247ff4508ad8bda16501b67f2f97a2a31dcdef51ab74ebd`  
		Last Modified: Fri, 12 Nov 2021 23:39:44 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87e4ff6e8d761e0db691ad452425a6a92dbad9ff27b28ad302af3b3a2294ab6`  
		Last Modified: Fri, 12 Nov 2021 23:39:45 GMT  
		Size: 2.4 MB (2350476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f5c2fca182bc8eb33d684623db7273d1a6a0d72369576a0d9b5400230104bd`  
		Last Modified: Tue, 11 Jan 2022 00:49:08 GMT  
		Size: 2.6 MB (2577862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8-alpine3.14` - linux; 386

```console
$ docker pull hylang@sha256:711dabe05395ee968317d1b0f809e48709e663cfa57b3d156da01ce696ceec58
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19474475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72457801180e85755c45bb8a67de2965327bad5986582426a67151fb35b4f6b`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:35:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Nov 2021 21:35:45 GMT
ENV LANG=C.UTF-8
# Fri, 12 Nov 2021 22:50:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Fri, 12 Nov 2021 22:50:07 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 12 Nov 2021 22:50:08 GMT
ENV PYTHON_VERSION=3.8.12
# Fri, 12 Nov 2021 22:56:46 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 12 Nov 2021 22:56:47 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 12 Nov 2021 22:56:47 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Fri, 12 Nov 2021 22:56:47 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Fri, 12 Nov 2021 22:56:48 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Fri, 12 Nov 2021 22:56:48 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Fri, 12 Nov 2021 22:56:55 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 12 Nov 2021 22:56:55 GMT
CMD ["python3"]
# Tue, 11 Jan 2022 00:40:58 GMT
ENV HY_VERSION=1.0a4
# Tue, 11 Jan 2022 00:40:58 GMT
ENV HYRULE_VERSION=0.1
# Tue, 11 Jan 2022 00:41:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 11 Jan 2022 00:41:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a868b05e11ba9eef9795d57a853d5fc28e2feebfd192b906e0b643a697e8d18`  
		Last Modified: Fri, 12 Nov 2021 23:42:07 GMT  
		Size: 282.5 KB (282489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7251c15efc8aa8928373423d5df85193137950dd22fb28a204d99ee74e42d4`  
		Last Modified: Fri, 12 Nov 2021 23:42:11 GMT  
		Size: 11.4 MB (11433226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d98e1e647fd61d16ccf1df209b0ead70fe2ad989b3d893c4c750f662ec8484`  
		Last Modified: Fri, 12 Nov 2021 23:42:07 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c969876f7518cf7e05043e30d6a6bf1607f06da79fbc1f65a41049983bd1c88`  
		Last Modified: Fri, 12 Nov 2021 23:42:09 GMT  
		Size: 2.3 MB (2348949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f716003b921525ead90195e51a8b44d7139e6a4bf60045ba57b39a7c2d08e4f2`  
		Last Modified: Tue, 11 Jan 2022 00:48:10 GMT  
		Size: 2.6 MB (2578632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8-alpine3.14` - linux; ppc64le

```console
$ docker pull hylang@sha256:918aced416bd9b07d2895488163cd3af558136b8149c15b2647e4ff2cb7bcef8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19568390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd16dbeccd81076e1fd0110304278ee25c5f4f071cf98a77a0cbf1614bb7708`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 12 Nov 2021 21:18:00 GMT
ADD file:4d45063079cb28a34f1e382fddb22f156ac99d5449aa05ed37cb653c1f7b80f2 in / 
# Fri, 12 Nov 2021 21:18:01 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 03:07:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 03:07:59 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 04:47:24 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Sat, 13 Nov 2021 04:47:31 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 13 Nov 2021 04:47:37 GMT
ENV PYTHON_VERSION=3.8.12
# Sat, 13 Nov 2021 04:55:58 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Sat, 13 Nov 2021 04:56:11 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 13 Nov 2021 04:56:16 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Sat, 13 Nov 2021 04:56:21 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Sat, 13 Nov 2021 04:56:25 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Sat, 13 Nov 2021 04:56:29 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Sat, 13 Nov 2021 04:56:51 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 13 Nov 2021 04:56:54 GMT
CMD ["python3"]
# Tue, 11 Jan 2022 00:22:49 GMT
ENV HY_VERSION=1.0a4
# Tue, 11 Jan 2022 00:22:52 GMT
ENV HYRULE_VERSION=0.1
# Tue, 11 Jan 2022 00:23:10 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 11 Jan 2022 00:23:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:72940440c1ab65eca4d38846164719ffde4b147543cc658d041407a925b13368`  
		Last Modified: Fri, 12 Nov 2021 21:19:32 GMT  
		Size: 2.8 MB (2817467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226718af5bcd33590bacccdf63da6c839b8083ede355bff8299fb1b6460acc1f`  
		Last Modified: Sat, 13 Nov 2021 05:56:46 GMT  
		Size: 284.1 KB (284069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8e09b75ba9e0b9a553277c6fd167f915b44089c001c2a88f616e021dcaaa6a`  
		Last Modified: Sat, 13 Nov 2021 05:56:48 GMT  
		Size: 11.5 MB (11538761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7480727dbdca7c3e70dd9039fbd506ffc0689c1b73ecc85d10a0ae42a7962416`  
		Last Modified: Sat, 13 Nov 2021 05:56:46 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e47c244498fbd358b38431be4c61ad2750e3070240651d5c2cffe902aa86a7`  
		Last Modified: Sat, 13 Nov 2021 05:56:46 GMT  
		Size: 2.3 MB (2349132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbc45524238f2fd3369ace99561e029733b1ca63b2c8b16d360dfec8f3fc58f`  
		Last Modified: Tue, 11 Jan 2022 00:30:14 GMT  
		Size: 2.6 MB (2578730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8-alpine3.14` - linux; s390x

```console
$ docker pull hylang@sha256:9a6c9c7827981021d651e76c880d57b95491435893d4a12df44056dbd8d172cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19474658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d689a03d1d02496fcedc5e38404a5e383eb15d79f18175c138ab42dad736af`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:32:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Nov 2021 17:32:13 GMT
ENV LANG=C.UTF-8
# Fri, 12 Nov 2021 17:32:14 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Fri, 12 Nov 2021 18:11:56 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 29 Jan 2022 03:53:24 GMT
ENV PYTHON_VERSION=3.8.12
# Sat, 29 Jan 2022 03:57:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 	cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 29 Jan 2022 03:57:40 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Sat, 29 Jan 2022 03:57:41 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Sat, 29 Jan 2022 03:57:41 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Sat, 29 Jan 2022 03:57:41 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Sat, 29 Jan 2022 03:57:41 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Sat, 29 Jan 2022 03:57:46 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	; 	rm -f get-pip.py
# Sat, 29 Jan 2022 03:57:47 GMT
CMD ["python3"]
# Sat, 29 Jan 2022 04:57:57 GMT
ENV HY_VERSION=1.0a4
# Sat, 29 Jan 2022 04:57:57 GMT
ENV HYRULE_VERSION=0.1
# Sat, 29 Jan 2022 04:58:00 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Sat, 29 Jan 2022 04:58:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f129656592216f3e6d38774b2d5b74c60752c0e42dfc59e2be1e725a9ed9d7e`  
		Last Modified: Fri, 12 Nov 2021 18:58:31 GMT  
		Size: 684.2 KB (684210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6152512d40d28756d2eb7480f1c36ca9bc89b5e4e157eadca1019db319deb8`  
		Last Modified: Sat, 29 Jan 2022 04:39:12 GMT  
		Size: 11.3 MB (11253385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98536c4f9d61b90d467af553dd930093a4fc944bdf976ecdf89692b4f317341d`  
		Last Modified: Sat, 29 Jan 2022 04:39:11 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae777829f134ad401ba2adcc299156b786f356cc139162d4d15f20eb9439a675`  
		Last Modified: Sat, 29 Jan 2022 04:39:11 GMT  
		Size: 2.3 MB (2349075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdb6ff26a4f3fe4c83d7ce39be50b7e4ff7ee5d62be7b885656ee7218f433d6`  
		Last Modified: Sat, 29 Jan 2022 05:02:54 GMT  
		Size: 2.6 MB (2578479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
