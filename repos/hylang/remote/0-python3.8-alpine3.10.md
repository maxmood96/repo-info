## `hylang:0-python3.8-alpine3.10`

```console
$ docker pull hylang@sha256:1b755f675a69be424e9354734f7aabe3c58f61dc641f4dd71d553874ba3488b5
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

### `hylang:0-python3.8-alpine3.10` - linux; amd64

```console
$ docker pull hylang@sha256:94f7f4dc457933629a54dfd87b2a001055fea9d50f65531f0ca4c7cbefee456a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39307627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94703f2170dac2af7d27c4a0863795f4f31a39c53f1994b49336084de121377d`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 01:34:56 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2020 01:34:56 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2020 01:34:58 GMT
RUN apk add --no-cache ca-certificates
# Fri, 24 Apr 2020 01:34:58 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 24 Apr 2020 01:34:59 GMT
ENV PYTHON_VERSION=3.8.2
# Fri, 24 Apr 2020 01:47:03 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Fri, 24 Apr 2020 01:47:04 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 29 Apr 2020 17:38:14 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 29 Apr 2020 17:38:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 29 Apr 2020 17:38:15 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 29 Apr 2020 17:38:21 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 29 Apr 2020 17:38:21 GMT
CMD ["python3"]
# Wed, 29 Apr 2020 18:49:15 GMT
ENV HY_VERSION=0.18.0
# Wed, 29 Apr 2020 18:49:21 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 29 Apr 2020 18:49:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a80d14c35bdcf3182348df62dae02f393b19e47d873d74d008296c54b784602`  
		Last Modified: Fri, 24 Apr 2020 11:13:39 GMT  
		Size: 300.9 KB (300945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e03bd2decbe27776066b08ae567fe3d52c70265efc8756d8942c1c00483e79`  
		Last Modified: Fri, 24 Apr 2020 11:13:46 GMT  
		Size: 31.5 MB (31469567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0fe21a04d0e5275576bf0948486d48df77be96d926afafa35cc6daf7c414eb8`  
		Last Modified: Fri, 24 Apr 2020 11:13:40 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd5ded23bc2d9639c46312e352a7994539712c48339f6aa59a1344e1ef2b486`  
		Last Modified: Wed, 29 Apr 2020 17:44:56 GMT  
		Size: 1.9 MB (1931012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7a0db9e917eb4627c5d8e27d71e97afe24920c3390d58bf12700c8ffd3e69a`  
		Last Modified: Wed, 29 Apr 2020 18:52:08 GMT  
		Size: 2.8 MB (2810290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.8-alpine3.10` - linux; arm variant v6

```console
$ docker pull hylang@sha256:994c3bfbdf9a7d80cdd59231fadd6e0ed87f2639cb330b85c169ac436fb79f2e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36453385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a269d2dc93561e6f06996819a62e38c9d2c4200a99ae735943a51d9ab116d90`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:35 GMT
ADD file:ef75120295e25a8e67c5ef378df2cf4ce9f7b83b44709452fcaf247b54fabd16 in / 
# Thu, 23 Apr 2020 15:51:36 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 20:38:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 20:38:45 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 20:38:48 GMT
RUN apk add --no-cache ca-certificates
# Thu, 23 Apr 2020 20:38:48 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 14 May 2020 19:00:34 GMT
ENV PYTHON_VERSION=3.8.3
# Thu, 14 May 2020 19:09:31 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 14 May 2020 19:09:35 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 14 May 2020 19:09:36 GMT
ENV PYTHON_PIP_VERSION=20.1
# Thu, 14 May 2020 19:09:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Thu, 14 May 2020 19:09:37 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Thu, 14 May 2020 19:09:53 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 14 May 2020 19:09:55 GMT
CMD ["python3"]
# Thu, 14 May 2020 19:29:53 GMT
ENV HY_VERSION=0.18.0
# Thu, 14 May 2020 19:30:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 14 May 2020 19:30:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e745d1dc1c9e0be26166278da7632765ca98fa1be8179a7cc440b3bdc5671860`  
		Last Modified: Thu, 23 Apr 2020 15:52:15 GMT  
		Size: 2.6 MB (2572512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57a40f256a36351da43ee93685238f00bc7c6b0457d57f43b6de40365dc27eb`  
		Last Modified: Thu, 23 Apr 2020 21:58:11 GMT  
		Size: 301.3 KB (301254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd95d78571e5bdd46a75aee8baa70bc1898a7beca4cffe387e764a7f650890e`  
		Last Modified: Thu, 14 May 2020 19:13:14 GMT  
		Size: 28.8 MB (28837212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa2111811bd1623f911d7ed7f4311124f46f5161070c7aad23e7febf349d284`  
		Last Modified: Thu, 14 May 2020 19:13:02 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa02053cd999ff31e8a5ecdb105d92881911a479cf585d01a5db9c52faeda2be`  
		Last Modified: Thu, 14 May 2020 19:13:03 GMT  
		Size: 1.9 MB (1931289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebc9f1b4a141f103dcb5bd1b922827b47acb8910205dfad23cdc5e698b710c7`  
		Last Modified: Thu, 14 May 2020 19:31:59 GMT  
		Size: 2.8 MB (2810886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.8-alpine3.10` - linux; arm variant v7

```console
$ docker pull hylang@sha256:e4ebd7875da67cbc34e567ddf4464e892e6c6c8fe13cef955c3bd40085f7f465
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35681632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51ff98c4224269cb8e3df90d714da7041a3c5e9201884efcfa20fcdb91c0df6`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:44 GMT
ADD file:dabd2c1328a46961a58e93557d1039d6b98775cbdfe48ce875c109bb74615cb1 in / 
# Thu, 23 Apr 2020 22:04:45 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:28:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2020 04:28:07 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2020 04:28:10 GMT
RUN apk add --no-cache ca-certificates
# Fri, 24 Apr 2020 04:28:11 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 24 Apr 2020 04:28:12 GMT
ENV PYTHON_VERSION=3.8.2
# Fri, 24 Apr 2020 04:36:35 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Fri, 24 Apr 2020 04:36:42 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 29 Apr 2020 17:19:40 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 29 Apr 2020 17:19:41 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 29 Apr 2020 17:19:41 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 29 Apr 2020 17:19:55 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 29 Apr 2020 17:19:56 GMT
CMD ["python3"]
# Wed, 29 Apr 2020 18:06:42 GMT
ENV HY_VERSION=0.18.0
# Wed, 29 Apr 2020 18:06:54 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 29 Apr 2020 18:06:56 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ad20c94522902b824bd9ea4e65dc1cba24dca4fdadd5728ed7446c0f4550d1ff`  
		Last Modified: Thu, 23 Apr 2020 22:05:22 GMT  
		Size: 2.4 MB (2378640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce92f9b10e33d2ac10e4a2982e1b92743ef36e12ec1e8ba8ef66ae7a125936a`  
		Last Modified: Fri, 24 Apr 2020 08:30:19 GMT  
		Size: 300.1 KB (300138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d9ac9b3da42cf28e588e49e193a5ba8b1836e611445396ac5d061ea5ed374`  
		Last Modified: Fri, 24 Apr 2020 08:30:28 GMT  
		Size: 28.3 MB (28260735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2602e3ebd92130dc3deb31c1ac39967c4cf4e65f5997e5886375f68e38af3ae`  
		Last Modified: Fri, 24 Apr 2020 08:30:19 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5efabca96d9ae4ea813ec14226ea54c4963c2816034f136beee1051635e3e48`  
		Last Modified: Wed, 29 Apr 2020 17:31:31 GMT  
		Size: 1.9 MB (1931262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f39a17982d5412a498343380e1103ca64cee5861b1fc09ca9858c65336f8f3`  
		Last Modified: Wed, 29 Apr 2020 18:12:53 GMT  
		Size: 2.8 MB (2810626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.8-alpine3.10` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:9673f1e25b0fe1fcbe6141eb37fcd2447b8bc317856fec63a06e43f00255cc6a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38360315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1304b49b558b71ab0d61e3b66e51132ffefff445e970fbecd85603329be760c1`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:52 GMT
ADD file:75529f7e83edb6d0457a3b8bbfe33d4e3a12f339c5ace517d0f52dbedd9a146b in / 
# Fri, 24 Apr 2020 00:14:53 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 07:16:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2020 07:16:39 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2020 07:16:41 GMT
RUN apk add --no-cache ca-certificates
# Fri, 24 Apr 2020 07:16:42 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 24 Apr 2020 07:16:42 GMT
ENV PYTHON_VERSION=3.8.2
# Fri, 24 Apr 2020 07:23:55 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Fri, 24 Apr 2020 07:23:58 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 29 Apr 2020 18:02:37 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 29 Apr 2020 18:02:38 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 29 Apr 2020 18:02:39 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 29 Apr 2020 18:02:57 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 29 Apr 2020 18:02:59 GMT
CMD ["python3"]
# Wed, 29 Apr 2020 19:10:39 GMT
ENV HY_VERSION=0.18.0
# Wed, 29 Apr 2020 19:10:48 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 29 Apr 2020 19:10:49 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b038bcb63e9c8905cc879c957302f686a9b43f24a18dcfc4186ab236ddf04cad`  
		Last Modified: Fri, 24 Apr 2020 00:15:54 GMT  
		Size: 2.7 MB (2718734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00770a9e6c343f414a2bac6b7ff8cb12c89d6b8559f1cb74ed38ea04ff029cd`  
		Last Modified: Fri, 24 Apr 2020 08:25:29 GMT  
		Size: 301.6 KB (301579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4793f9e3ec4a7413756f6194d97709714c7176f857e241445ea8125263044ebb`  
		Last Modified: Fri, 24 Apr 2020 08:25:42 GMT  
		Size: 30.6 MB (30597807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aabb4248cde1815d83231f7f0505cd0083a41ed44995f8f622c23a9371fc0a2`  
		Last Modified: Fri, 24 Apr 2020 08:25:29 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f779fc097d52b48508c98935d3e69395d8b7ccfb4fcdc4e869ae996f7b1a21`  
		Last Modified: Wed, 29 Apr 2020 18:15:57 GMT  
		Size: 1.9 MB (1931272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9be612becb6936281f1f7d9b54a3ccbbdac15e99b9b37f849ec1be9e230e7d`  
		Last Modified: Wed, 29 Apr 2020 19:15:39 GMT  
		Size: 2.8 MB (2810693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.8-alpine3.10` - linux; 386

```console
$ docker pull hylang@sha256:67ec1273c9bdeb6ea818f5d08e8581ac273d517c873fa4fdb1dfae9139ccccdf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37599999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae1ea7e81f0088faaace4b216685bab20184365b5770294cfae913b496ba779`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:11 GMT
ADD file:2e9fb162fdd20e7ac6e9edcb9e1ce9ece750f125c93824c5709a2800ae397f89 in / 
# Thu, 23 Apr 2020 21:16:11 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 21:38:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 21:38:22 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 21:38:24 GMT
RUN apk add --no-cache ca-certificates
# Thu, 23 Apr 2020 21:38:24 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 23 Apr 2020 21:38:24 GMT
ENV PYTHON_VERSION=3.8.2
# Thu, 23 Apr 2020 21:47:05 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Apr 2020 21:47:06 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 29 Apr 2020 18:01:23 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 29 Apr 2020 18:01:23 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 29 Apr 2020 18:01:23 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 29 Apr 2020 18:01:30 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 29 Apr 2020 18:01:30 GMT
CMD ["python3"]
# Wed, 29 Apr 2020 18:24:51 GMT
ENV HY_VERSION=0.18.0
# Wed, 29 Apr 2020 18:24:56 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 29 Apr 2020 18:24:56 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:294658c31053f36b08a64158e37d4fb84478e6fe8f4d5127c51a6334c8a3c36d`  
		Last Modified: Thu, 23 Apr 2020 21:16:37 GMT  
		Size: 2.8 MB (2787128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61cc54eae371e15077a5272fb58cfef3e4a13587edf5fe05700b05ee682c5cd`  
		Last Modified: Thu, 23 Apr 2020 22:44:54 GMT  
		Size: 301.6 KB (301596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49975db90f632e7a85b33c5a47952d4b9c0917bc08955835241deac8bae1ecc`  
		Last Modified: Thu, 23 Apr 2020 22:45:01 GMT  
		Size: 29.8 MB (29769951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22ae841242a322ad19b6cffecc0aafced1d53729ed72470500488f8bc39e449`  
		Last Modified: Thu, 23 Apr 2020 22:44:53 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db5a5e06de8262d469fdb8070acacf7a9433e5de854358af02da7dfbe63e184`  
		Last Modified: Wed, 29 Apr 2020 18:07:22 GMT  
		Size: 1.9 MB (1931035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587ad2b27a3afa1e2652ad46fe3ec2230148225be7c38d154d9d8b27b674b125`  
		Last Modified: Wed, 29 Apr 2020 18:27:52 GMT  
		Size: 2.8 MB (2810058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.8-alpine3.10` - linux; ppc64le

```console
$ docker pull hylang@sha256:e769bb2d53b9975647d1ff598811d0c086e016a9b5ecb02f652063896e216ed7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40233963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad0e70320c0e586db65e00f1be0fec24042c3ffe7027cb1f8b137723ed2de5d`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Apr 2020 20:40:45 GMT
ADD file:2b585d18d1fcebf3ed725468d8f9642d2e6e32af8770f87b36d4601cc3a55316 in / 
# Thu, 23 Apr 2020 20:40:47 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:56:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2020 09:56:06 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2020 09:56:16 GMT
RUN apk add --no-cache ca-certificates
# Fri, 24 Apr 2020 09:56:20 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 24 Apr 2020 09:56:22 GMT
ENV PYTHON_VERSION=3.8.2
# Fri, 24 Apr 2020 10:05:01 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Fri, 24 Apr 2020 10:05:17 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 29 Apr 2020 17:45:41 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 29 Apr 2020 17:45:44 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 29 Apr 2020 17:45:46 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 29 Apr 2020 17:46:10 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 29 Apr 2020 17:46:13 GMT
CMD ["python3"]
# Wed, 29 Apr 2020 19:19:27 GMT
ENV HY_VERSION=0.18.0
# Wed, 29 Apr 2020 19:19:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 29 Apr 2020 19:19:52 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6694fcf3186b2073b4f09e0a2a753df9c8bcd31083e89a8a8f9a7001ad295328`  
		Last Modified: Thu, 23 Apr 2020 20:41:47 GMT  
		Size: 2.8 MB (2809956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36408d0fc6e8604a4840728f6b4d11631e84283c697404c6f7487c1b60518036`  
		Last Modified: Fri, 24 Apr 2020 11:09:27 GMT  
		Size: 303.7 KB (303693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f537c94ea0910bfaa119a4fb6c0744779eac66ad6b90bb1f3d42f8426e2f8a8a`  
		Last Modified: Fri, 24 Apr 2020 11:09:35 GMT  
		Size: 32.4 MB (32377802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76b0a249c62dbd63ff1d87b0e612be6459ee958ad003169a07128460143c29d`  
		Last Modified: Fri, 24 Apr 2020 11:09:26 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b0c3f21922a03297b8bdc3bcf8c1f530fa184ae1cf40f14a19a8f772eda5e8`  
		Last Modified: Wed, 29 Apr 2020 18:08:49 GMT  
		Size: 1.9 MB (1931242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36214599a26fe882da7b30d46dff7af1182f8be5fd0e956d848c40b4c9a37263`  
		Last Modified: Wed, 29 Apr 2020 19:27:31 GMT  
		Size: 2.8 MB (2811039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.8-alpine3.10` - linux; s390x

```console
$ docker pull hylang@sha256:80fd344718d4214ae879942a4ea75ab42b455816eff94634ac1495cf36e3bf41
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38988503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b762364d82f33feaa74def8a1a2662621fae2fc92ba55c204ade4a123afef2d`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Apr 2020 17:51:08 GMT
ADD file:53e1d2e5396547a2d7109e4b73078911bd069ae5d762f816d90e89ec9731ab13 in / 
# Thu, 23 Apr 2020 17:51:08 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 00:08:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2020 00:08:22 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2020 00:08:23 GMT
RUN apk add --no-cache ca-certificates
# Fri, 24 Apr 2020 00:08:24 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 14 May 2020 20:54:46 GMT
ENV PYTHON_VERSION=3.8.3
# Thu, 14 May 2020 20:59:05 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 14 May 2020 20:59:07 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 14 May 2020 20:59:07 GMT
ENV PYTHON_PIP_VERSION=20.1
# Thu, 14 May 2020 20:59:07 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Thu, 14 May 2020 20:59:07 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Thu, 14 May 2020 20:59:14 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 14 May 2020 20:59:14 GMT
CMD ["python3"]
# Fri, 15 May 2020 00:09:22 GMT
ENV HY_VERSION=0.18.0
# Fri, 15 May 2020 00:09:25 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 15 May 2020 00:09:26 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ab92bebeb6027138cd65f1f6658fd3428e21c60c95bdc978e0c57bf0b2a53970`  
		Last Modified: Thu, 23 Apr 2020 17:51:46 GMT  
		Size: 2.6 MB (2574478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9effbbafa6dfb00bba9beef1c64dca1e9ac011970f2065747370e7774a9109a7`  
		Last Modified: Fri, 24 Apr 2020 06:43:43 GMT  
		Size: 301.7 KB (301709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab50268a987292ef62c8521e1182cc375dfc78513812649a726fbf036d068e66`  
		Last Modified: Thu, 14 May 2020 21:02:39 GMT  
		Size: 31.4 MB (31370268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72962290fc1b3e4d562c26a0cce277cad0bb21e20d7d9aaea805c725abdf5226`  
		Last Modified: Thu, 14 May 2020 21:02:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f904d48e09f4dc88898ee58c6105a3d2796f90b7deb1a5fa9c8ef260e96a7d1`  
		Last Modified: Thu, 14 May 2020 21:02:49 GMT  
		Size: 1.9 MB (1931119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b0fc6449398a4b7027258f83c772d0c06c70641c3cf2302e5f6839446948a4`  
		Last Modified: Fri, 15 May 2020 00:12:16 GMT  
		Size: 2.8 MB (2810699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
