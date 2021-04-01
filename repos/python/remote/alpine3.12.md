## `python:alpine3.12`

```console
$ docker pull python@sha256:cd1da17f18a7c441914db33f6911dd3d40cffc07596e01eb217d30273623ac1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `python:alpine3.12` - linux; amd64

```console
$ docker pull python@sha256:09b6d6a27fcf4f74ae83ede0b6da3e38cdf87e71a5dc360d44b5e057178d8d73
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17181133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b7a45b22042fbab7ec3935f079039b1be5941f9bbdaca251b5b84871986bb7`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 06:05:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Mar 2021 08:30:50 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 08:30:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Fri, 26 Mar 2021 08:43:09 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 26 Mar 2021 08:43:09 GMT
ENV PYTHON_VERSION=3.9.2
# Fri, 26 Mar 2021 08:48:33 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 26 Mar 2021 08:48:34 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 26 Mar 2021 08:48:34 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Fri, 26 Mar 2021 08:48:34 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Fri, 26 Mar 2021 08:48:34 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Fri, 26 Mar 2021 08:48:40 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 26 Mar 2021 08:48:41 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ff1337a9b05c41170477142045cba8c1eaf914d390ef365168e1b15f4077c3`  
		Last Modified: Fri, 26 Mar 2021 09:27:47 GMT  
		Size: 655.7 KB (655736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fede5250f32e1895bc91b2761b1ba9cdedb24da95b2c54e5248f00cd60950d87`  
		Last Modified: Fri, 26 Mar 2021 09:28:36 GMT  
		Size: 11.6 MB (11560790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be52bd57dbf33e8aefd57a741d924af4aba2f48c02b48812967bf0d8ee027704`  
		Last Modified: Fri, 26 Mar 2021 09:28:35 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1408072aad56401a2608a65ad045066145319d22e267397fae9d65369f2d2ab4`  
		Last Modified: Fri, 26 Mar 2021 09:28:35 GMT  
		Size: 2.2 MB (2164613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:alpine3.12` - linux; arm variant v6

```console
$ docker pull python@sha256:fde9ef1e1652cae1b10ef925c7a0c70b6a9cf992574881af2f82ca8bd59653a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16636908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702f55f307d03eb5909b4f3dca7045e136a02b93cad843e3c79d0276cebe4024`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:11 GMT
ADD file:00ac3d0df16779e7564cda9cbf94eef90ffa8043778a867272ff0135a1fb537f in / 
# Wed, 31 Mar 2021 17:19:12 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 00:58:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Apr 2021 00:58:53 GMT
ENV LANG=C.UTF-8
# Thu, 01 Apr 2021 00:59:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Thu, 01 Apr 2021 01:25:21 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 01 Apr 2021 01:25:22 GMT
ENV PYTHON_VERSION=3.9.2
# Thu, 01 Apr 2021 01:35:48 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Thu, 01 Apr 2021 01:35:59 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 01 Apr 2021 01:36:01 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Thu, 01 Apr 2021 01:36:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Thu, 01 Apr 2021 01:36:03 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Thu, 01 Apr 2021 01:36:22 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 01 Apr 2021 01:36:24 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:66e54586dae0889b30da12f7a66838d9b86511b58696c83c3b9166ff1a534bbe`  
		Last Modified: Wed, 31 Mar 2021 17:20:05 GMT  
		Size: 2.6 MB (2604658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e885fa1462cc76046f40a60875e7e349242ddca81f0d1d983fd93c4722404f`  
		Last Modified: Thu, 01 Apr 2021 02:54:27 GMT  
		Size: 659.6 KB (659603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371856c5c5b81c7ca8a6289deae66d4611a259c605c750377f1c890440e02808`  
		Last Modified: Thu, 01 Apr 2021 02:55:04 GMT  
		Size: 11.2 MB (11207798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e08c59b99b2936430a8f062e7b125840fd38b7343f8b3431b19f6233e193b6`  
		Last Modified: Thu, 01 Apr 2021 02:55:00 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba161fda88fae5152f215a1bbac895fa393186ed529a22cb7dbc1e343aac636`  
		Last Modified: Thu, 01 Apr 2021 02:55:01 GMT  
		Size: 2.2 MB (2164617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:alpine3.12` - linux; arm variant v7

```console
$ docker pull python@sha256:b6e713103d5717282353b87786cc83691f495c71f20b83945ab5d5056743506e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15485166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc0a90353a926ed7c6b1cefb4eccde07061afdb32e28fffbf28efb2c0aa1d68`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 25 Mar 2021 22:06:14 GMT
ADD file:09312e8d8073093cdfa852f8a73713903ec5022b963fe0413feb08af5c98721b in / 
# Thu, 25 Mar 2021 22:06:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:35:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Mar 2021 02:35:22 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 02:35:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Fri, 26 Mar 2021 02:54:07 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 26 Mar 2021 02:54:10 GMT
ENV PYTHON_VERSION=3.9.2
# Fri, 26 Mar 2021 03:00:05 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 26 Mar 2021 03:00:09 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 26 Mar 2021 03:00:10 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Fri, 26 Mar 2021 03:00:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Fri, 26 Mar 2021 03:00:12 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Fri, 26 Mar 2021 03:00:25 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 26 Mar 2021 03:00:26 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:1d60ece6104ddbfa31c28af7c5c9c14957b3b271ea6f7edac14f84f4cd8c5fa9`  
		Last Modified: Thu, 25 Mar 2021 22:07:33 GMT  
		Size: 2.4 MB (2408322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5b39bda0b9b48c1f5a25a1a0df0a63e3df4482b69e0e31746dcb2ddbaf51b9`  
		Last Modified: Fri, 26 Mar 2021 04:01:05 GMT  
		Size: 652.0 KB (651968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874f537d7918652a83b6449cb29e1b4b6037f61e5e1c616434ecca2466a8a90c`  
		Last Modified: Fri, 26 Mar 2021 04:01:42 GMT  
		Size: 10.3 MB (10260010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecf59ba83fb79a3618b13636870fe447e8adf273d046c2f063ec4fd685d8207`  
		Last Modified: Fri, 26 Mar 2021 04:01:39 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3dee47c08cb6a3a9be05ed2ffaa807db419ee7ff0190591166b83dc7f5c07ab`  
		Last Modified: Fri, 26 Mar 2021 04:01:40 GMT  
		Size: 2.2 MB (2164633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:alpine3.12` - linux; arm64 variant v8

```console
$ docker pull python@sha256:56e1675469566adef759b66eafeb5da31d1c69e981cadf7a4be22e81ab23fad0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17175637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde75e69b5df396615bc83f26dad1efa00d47f6f0a93c97379284e5c697a1b26`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:00 GMT
ADD file:97aac29a9ffbba2c76441891035010395614dc3115c4710d58932205b604308f in / 
# Thu, 25 Mar 2021 22:41:10 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 06:29:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Mar 2021 06:29:58 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 06:30:03 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Fri, 26 Mar 2021 06:49:03 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 26 Mar 2021 06:49:03 GMT
ENV PYTHON_VERSION=3.9.2
# Fri, 26 Mar 2021 06:56:28 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 26 Mar 2021 06:56:30 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 26 Mar 2021 06:56:31 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Fri, 26 Mar 2021 06:56:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Fri, 26 Mar 2021 06:56:33 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Fri, 26 Mar 2021 06:56:45 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 26 Mar 2021 06:56:47 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:95dec6db372224fc1909f0d0c0a9a9d5767ec6b78d066ff6a7d5723160037828`  
		Last Modified: Thu, 25 Mar 2021 22:45:23 GMT  
		Size: 2.7 MB (2709692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51dc3cd6da4908dddd85717b07bb66f875180ea01ea9f955da1696efd72001c`  
		Last Modified: Fri, 26 Mar 2021 08:05:16 GMT  
		Size: 658.3 KB (658324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86267ba792b87b9e17520c602276d0706a678b2bf672dee183b7727620899be2`  
		Last Modified: Fri, 26 Mar 2021 08:05:56 GMT  
		Size: 11.6 MB (11642682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5156e58bcbb00947479039792d40bae63c2d07316f6078099a86893b99544b`  
		Last Modified: Fri, 26 Mar 2021 08:05:53 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8df6b8488e3d8f646def1407cb1b2e8cdf25cdefb9183a814342b3c2c26f7e`  
		Last Modified: Fri, 26 Mar 2021 08:05:54 GMT  
		Size: 2.2 MB (2164706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:alpine3.12` - linux; 386

```console
$ docker pull python@sha256:0dacf1e14007ad59f243a126e05b108e53ec75976bf30adc824b29ad6ec105bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17419545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00a14f5a3e9f82a168828b1f91d86070070a7dc3e37f01c3333a5abdcfafdc6`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 31 Mar 2021 17:43:08 GMT
ADD file:053c3a6154e80758106cbf0fec936c3b41dabf24a9f5eda36416caa90556810c in / 
# Wed, 31 Mar 2021 17:43:09 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 18:26:03 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Mar 2021 18:26:04 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 18:26:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 31 Mar 2021 18:51:52 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 31 Mar 2021 18:51:53 GMT
ENV PYTHON_VERSION=3.9.2
# Wed, 31 Mar 2021 19:04:58 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Wed, 31 Mar 2021 19:05:00 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 31 Mar 2021 19:05:01 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Wed, 31 Mar 2021 19:05:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Wed, 31 Mar 2021 19:05:01 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Wed, 31 Mar 2021 19:05:14 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 31 Mar 2021 19:05:14 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:8eca83e4805e4c5e7b071425a4603bc4b02885b817aa7c1bba9605bd2cb9125a`  
		Last Modified: Wed, 31 Mar 2021 17:44:26 GMT  
		Size: 2.8 MB (2794977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a813350c9b3f77536bb61a126c653043c86c80899ab67885400971a4c2bb19d6`  
		Last Modified: Wed, 31 Mar 2021 23:07:22 GMT  
		Size: 661.8 KB (661847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40588503dd112c24b33d026d70c6b515b8ac3b3d967955ea5ef30db096d87b10`  
		Last Modified: Wed, 31 Mar 2021 23:08:45 GMT  
		Size: 11.8 MB (11797827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456ea90f2fa55d7828d7998f9c4e18d3d5160a818e680cd015e0fadede0e7338`  
		Last Modified: Wed, 31 Mar 2021 23:08:39 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20ebee5bddc42ad3badebf38bc328526fd8adca06db45bf7f502f54893bd404`  
		Last Modified: Wed, 31 Mar 2021 23:08:44 GMT  
		Size: 2.2 MB (2164662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:alpine3.12` - linux; ppc64le

```console
$ docker pull python@sha256:b61036f07b46b93a971ec97a7717559d1f08832b69bf66bac3d0648b8083df84
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17971094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e294527511b193a3d9c12364f5d89e04318c7b17ab06b542a42700730a1eeadc`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 25 Mar 2021 22:22:44 GMT
ADD file:fa3152db8e0ad493ea5fe137f9b6210cabbda6e880fc18f1935b8ef1dae5e5b7 in / 
# Thu, 25 Mar 2021 22:22:50 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:40:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Mar 2021 02:40:12 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 02:40:48 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Fri, 26 Mar 2021 05:16:41 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 26 Mar 2021 05:16:46 GMT
ENV PYTHON_VERSION=3.9.2
# Fri, 26 Mar 2021 22:10:32 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 26 Mar 2021 22:10:54 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 26 Mar 2021 22:11:00 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Fri, 26 Mar 2021 22:11:03 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Fri, 26 Mar 2021 22:11:08 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Fri, 26 Mar 2021 22:11:34 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 26 Mar 2021 22:11:41 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:d9d64eb18374b2d527a335e2362041eba1adef6c7376c1347f45cbd1df5239c1`  
		Last Modified: Thu, 25 Mar 2021 22:24:26 GMT  
		Size: 2.8 MB (2805974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb17582c0d351b4c346f6c16a229bca2ceae304ec0266b0e13267823856cf5a`  
		Last Modified: Sat, 27 Mar 2021 00:57:01 GMT  
		Size: 664.6 KB (664642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa82e625095a67299ccbd71e2fe877f1d9a3e82e002b2187049ee66b6566cff`  
		Last Modified: Sat, 27 Mar 2021 00:58:29 GMT  
		Size: 12.3 MB (12335543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c4770a731c458e6b404365b4cab6ee78f31a2f9d989ad8ff3e03c9a00fca02`  
		Last Modified: Sat, 27 Mar 2021 00:58:26 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffd1f4be1f59429ef88904124293d35fc7e7ff363daba4ec7e8b5c3286f33bc`  
		Last Modified: Sat, 27 Mar 2021 00:58:27 GMT  
		Size: 2.2 MB (2164703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:alpine3.12` - linux; s390x

```console
$ docker pull python@sha256:89549c574171c9442e365855ec86e756ad488d84beb4526da0c9237a8901e631
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16958699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55460baff9afe00550fab631f6f0b23091a8aeaee3deb96feda2ac4727863f8b`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 31 Mar 2021 17:15:04 GMT
ADD file:1f37b92ea1f573c4810b1d056dc4880cf4035e143451d9b2b76fac1e3b462248 in / 
# Wed, 31 Mar 2021 17:15:04 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 02:59:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Apr 2021 02:59:12 GMT
ENV LANG=C.UTF-8
# Thu, 01 Apr 2021 02:59:14 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Thu, 01 Apr 2021 03:12:12 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 01 Apr 2021 03:12:12 GMT
ENV PYTHON_VERSION=3.9.2
# Thu, 01 Apr 2021 03:17:08 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Thu, 01 Apr 2021 03:17:10 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 01 Apr 2021 03:17:10 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Thu, 01 Apr 2021 03:17:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Thu, 01 Apr 2021 03:17:11 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Thu, 01 Apr 2021 03:17:17 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 01 Apr 2021 03:17:18 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:38ca5430c9af12b6b6dee7c10eb6b1eb0e4eb4f5f02a97890579c4b049d00233`  
		Last Modified: Wed, 31 Mar 2021 17:15:46 GMT  
		Size: 2.6 MB (2567453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073b469b782714ffb46c1c65d073b7ee0112f6cc67ead08bc30a9f10a071ba3a`  
		Last Modified: Thu, 01 Apr 2021 03:53:45 GMT  
		Size: 660.5 KB (660527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c283958982c3d99a07c0cfce45db7f49a4f09a64d817924a58e25931220bc9`  
		Last Modified: Thu, 01 Apr 2021 03:54:19 GMT  
		Size: 11.6 MB (11565958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d21d5f4e95b11fbe9501b83393fd18ce7b63f5311d875bcea9d0186b59a665`  
		Last Modified: Thu, 01 Apr 2021 03:54:17 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42da8a776eee2e3dea817f81160ef1ddcb8887e449adbb834e4b4bdd54f4160`  
		Last Modified: Thu, 01 Apr 2021 03:54:18 GMT  
		Size: 2.2 MB (2164532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
