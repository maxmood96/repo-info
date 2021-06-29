## `python:rc-alpine3.14`

```console
$ docker pull python@sha256:bc49603b87a1e418b7c59a66730bddd593e53c8640836139e7915bfe30a4a166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `python:rc-alpine3.14` - linux; amd64

```console
$ docker pull python@sha256:c6a56def5839f2d070eacb8b74a6f1e9dbb8f9bcf1132cf37203fc127a22a868
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17402927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6da5629b1149e080390d1833c03d7f17f6dbc4f25bfb72eedf24bcf2ea52ca3`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 15 Jun 2021 22:19:37 GMT
ADD file:f278386b0cef68136129f5f58c52445590a417b624d62bca158d4dc926c340df in / 
# Tue, 15 Jun 2021 22:19:37 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 18:20:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Jun 2021 01:15:24 GMT
ENV LANG=C.UTF-8
# Tue, 29 Jun 2021 01:15:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 29 Jun 2021 01:15:26 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 29 Jun 2021 01:15:26 GMT
ENV PYTHON_VERSION=3.10.0b3
# Tue, 29 Jun 2021 01:22:31 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Tue, 29 Jun 2021 01:22:32 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 29 Jun 2021 01:22:32 GMT
ENV PYTHON_PIP_VERSION=21.1.3
# Tue, 29 Jun 2021 01:22:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a1675ab6c2bd898ed82b1f58c486097f763c74a9/public/get-pip.py
# Tue, 29 Jun 2021 01:22:32 GMT
ENV PYTHON_GET_PIP_SHA256=6665659241292b2147b58922b9ffe11dda66b39d52d8a6f3aa310bc1d60ea6f7
# Tue, 29 Jun 2021 01:22:40 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 29 Jun 2021 01:22:40 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:5843afab387455b37944e709ee8c78d7520df80f8d01cf7f861aae63beeddb6b`  
		Last Modified: Tue, 15 Jun 2021 22:20:04 GMT  
		Size: 2.8 MB (2811478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dfaacf7024eb3bb4c2e67a960e5c65425a95a09a7a4929884e4f49417dea92f`  
		Last Modified: Tue, 29 Jun 2021 02:09:02 GMT  
		Size: 656.3 KB (656343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a914db1f3d3e5088075bd10d3f32a325c2327e9b860da91d2b1933c9406b53`  
		Last Modified: Tue, 29 Jun 2021 02:09:04 GMT  
		Size: 11.6 MB (11586416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b322088c594cc22ec51e87b91589a6cbee644d5d538aa12c708f81a8ac15896`  
		Last Modified: Tue, 29 Jun 2021 02:09:01 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c287c60cc570554e44b394238a821ffce44f138e8c4377e8c23b2c9f68c3b859`  
		Last Modified: Tue, 29 Jun 2021 02:09:02 GMT  
		Size: 2.3 MB (2348462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:rc-alpine3.14` - linux; arm variant v6

```console
$ docker pull python@sha256:0c59bd46222d9357ce700a09cd0fc5d87a7fd042918a543c921d3940ac523298
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16772433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8216f06b0a8988c984b3bdf4bb1af7a08afaf4d6b8961f331c334811d461a7`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:26 GMT
ADD file:c80bc2b093cbc0fc466582ef21cbed377de9fa874aedbf320079525ddacd1200 in / 
# Tue, 15 Jun 2021 22:57:26 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 21:14:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Jun 2021 21:14:57 GMT
ENV LANG=C.UTF-8
# Mon, 28 Jun 2021 21:15:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Mon, 28 Jun 2021 21:15:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Mon, 28 Jun 2021 21:15:02 GMT
ENV PYTHON_VERSION=3.10.0b3
# Mon, 28 Jun 2021 21:27:44 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Mon, 28 Jun 2021 21:27:45 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 28 Jun 2021 21:27:46 GMT
ENV PYTHON_PIP_VERSION=21.1.3
# Mon, 28 Jun 2021 21:27:46 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a1675ab6c2bd898ed82b1f58c486097f763c74a9/public/get-pip.py
# Mon, 28 Jun 2021 21:27:47 GMT
ENV PYTHON_GET_PIP_SHA256=6665659241292b2147b58922b9ffe11dda66b39d52d8a6f3aa310bc1d60ea6f7
# Mon, 28 Jun 2021 21:28:06 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 28 Jun 2021 21:28:06 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:b4c9a0924271af3466de27804af26420eb58da1466e7eaaba127d178b380fea3`  
		Last Modified: Tue, 15 Jun 2021 22:58:47 GMT  
		Size: 2.6 MB (2624382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8caffa5605e88c080b0168edcfe2bd7ab31024027b3ea2ee059bbcb646775175`  
		Last Modified: Mon, 28 Jun 2021 23:35:58 GMT  
		Size: 662.0 KB (661975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0f345b420cdf165ea5ceaeb90d54a5e6635d8955420c82940a19dda390b024`  
		Last Modified: Mon, 28 Jun 2021 23:36:05 GMT  
		Size: 11.1 MB (11137241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd65b0a71b0fc7c063be27e902fef07671350d98ee8d9d73c474759a3c4f50ac`  
		Last Modified: Mon, 28 Jun 2021 23:35:58 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501cc2c4ce0479fee4ad93543d23ea78d5a271b22857dba6e6e58ce7bc071f6b`  
		Last Modified: Mon, 28 Jun 2021 23:36:00 GMT  
		Size: 2.3 MB (2348603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:rc-alpine3.14` - linux; arm variant v7

```console
$ docker pull python@sha256:e2a629eff5b5035a87ebbb4d53edb1609a91661d123622b644d23be6c8e540b5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16062882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7d334cdf37ebf1518b59ba08b73028be6e754cd464c456c0e376833baac906`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 15 Jun 2021 23:15:05 GMT
ADD file:416a8b507abdc6bdcb22997a4be0a4170796c3f9f77e315b2dbff2b0a212bc68 in / 
# Tue, 15 Jun 2021 23:15:06 GMT
CMD ["/bin/sh"]
# Tue, 29 Jun 2021 00:35:48 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Jun 2021 00:35:48 GMT
ENV LANG=C.UTF-8
# Tue, 29 Jun 2021 00:35:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 29 Jun 2021 00:35:52 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 29 Jun 2021 00:35:52 GMT
ENV PYTHON_VERSION=3.10.0b3
# Tue, 29 Jun 2021 00:47:04 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Tue, 29 Jun 2021 00:47:05 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 29 Jun 2021 00:47:06 GMT
ENV PYTHON_PIP_VERSION=21.1.3
# Tue, 29 Jun 2021 00:47:06 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a1675ab6c2bd898ed82b1f58c486097f763c74a9/public/get-pip.py
# Tue, 29 Jun 2021 00:47:07 GMT
ENV PYTHON_GET_PIP_SHA256=6665659241292b2147b58922b9ffe11dda66b39d52d8a6f3aa310bc1d60ea6f7
# Tue, 29 Jun 2021 00:47:23 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 29 Jun 2021 00:47:24 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:136482bf81d1fa351b424ebb8c7e34d15f2c5ed3fc0b66b544b8312bda3d52d9`  
		Last Modified: Tue, 15 Jun 2021 23:16:40 GMT  
		Size: 2.4 MB (2427917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f0e1b5b2e6a115612e84d82e54c15fc4e2b9b37881a91026682d9d1e446db4`  
		Last Modified: Tue, 29 Jun 2021 02:07:10 GMT  
		Size: 655.2 KB (655211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a38dcb3d27a152fd9ff75b62dbe750c98f4f33477740d09b620551d9bf794f`  
		Last Modified: Tue, 29 Jun 2021 02:07:16 GMT  
		Size: 10.6 MB (10630860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be7b46d915288485fd216adb8839af9a933a3d34ebbe944ff9ceda42a942126`  
		Last Modified: Tue, 29 Jun 2021 02:07:09 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb80c2c84c3057ea74439ad6b7c3f0fefc117ad804c5cf34931bc11ebcd157d`  
		Last Modified: Tue, 29 Jun 2021 02:07:12 GMT  
		Size: 2.3 MB (2348663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:rc-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull python@sha256:4ba1f2091f9fadd48bce69212098c1c60a0f874151ab17aaeb3cc488e4c3258d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17362891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76faf705032987a95fff9a62a2e1d2cb5dc732b868f5713c31994634b5ab04e4`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 15 Jun 2021 21:44:56 GMT
ADD file:6797caacbfe41bfe44000b39ed017016c6fcc492b3d6557cdaba88536df6c876 in / 
# Tue, 15 Jun 2021 21:44:56 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 17:40:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Jun 2021 23:26:44 GMT
ENV LANG=C.UTF-8
# Mon, 28 Jun 2021 23:26:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Mon, 28 Jun 2021 23:26:46 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Mon, 28 Jun 2021 23:26:46 GMT
ENV PYTHON_VERSION=3.10.0b3
# Mon, 28 Jun 2021 23:33:20 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Mon, 28 Jun 2021 23:33:21 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 28 Jun 2021 23:33:21 GMT
ENV PYTHON_PIP_VERSION=21.1.3
# Mon, 28 Jun 2021 23:33:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a1675ab6c2bd898ed82b1f58c486097f763c74a9/public/get-pip.py
# Mon, 28 Jun 2021 23:33:21 GMT
ENV PYTHON_GET_PIP_SHA256=6665659241292b2147b58922b9ffe11dda66b39d52d8a6f3aa310bc1d60ea6f7
# Mon, 28 Jun 2021 23:33:29 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 28 Jun 2021 23:33:29 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:58ab47519297212468320b23b8100fc1b2b96e8d342040806ae509a778a0a07a`  
		Last Modified: Tue, 15 Jun 2021 21:46:03 GMT  
		Size: 2.7 MB (2709626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409d7880206affd555ff2c4a576ce3459104c96cb861a846872ed67fcf2f86ad`  
		Last Modified: Tue, 29 Jun 2021 00:18:36 GMT  
		Size: 658.8 KB (658803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf597ae3924875fdb842a66be6cb19512c59c31d3d1dfe81abb6087efe258c1`  
		Last Modified: Tue, 29 Jun 2021 00:18:37 GMT  
		Size: 11.6 MB (11645736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3071f51100ffc2dc2398403ddabe4c99cf0c95efd9dbcda8b52f6d8e5dc3696c`  
		Last Modified: Tue, 29 Jun 2021 00:18:35 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821935b6302753a5d532132d82ee37b32cb6e85ca98c9b0c564f9d14b4e48ffb`  
		Last Modified: Tue, 29 Jun 2021 00:18:36 GMT  
		Size: 2.3 MB (2348490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:rc-alpine3.14` - linux; 386

```console
$ docker pull python@sha256:6acc03a5c4b0ac9552e8dbfbd98d7cb01214da41754b919ae6ecfa26d0d24b1a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17628967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bd89c4e85d139f8de5824bc0243fc4259f75f5b55e999ab10f66af1eddce2b`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 15 Jun 2021 21:38:30 GMT
ADD file:3b0fe1454491bb05e218b090fd461f2fd39546aa4a53eb3f953ee8eae149ac57 in / 
# Tue, 15 Jun 2021 21:38:30 GMT
CMD ["/bin/sh"]
# Tue, 29 Jun 2021 02:07:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Jun 2021 02:07:54 GMT
ENV LANG=C.UTF-8
# Tue, 29 Jun 2021 02:07:56 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 29 Jun 2021 02:07:56 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 29 Jun 2021 02:07:56 GMT
ENV PYTHON_VERSION=3.10.0b3
# Tue, 29 Jun 2021 02:15:49 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Tue, 29 Jun 2021 02:15:51 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 29 Jun 2021 02:15:51 GMT
ENV PYTHON_PIP_VERSION=21.1.3
# Tue, 29 Jun 2021 02:15:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a1675ab6c2bd898ed82b1f58c486097f763c74a9/public/get-pip.py
# Tue, 29 Jun 2021 02:15:51 GMT
ENV PYTHON_GET_PIP_SHA256=6665659241292b2147b58922b9ffe11dda66b39d52d8a6f3aa310bc1d60ea6f7
# Tue, 29 Jun 2021 02:16:00 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 29 Jun 2021 02:16:00 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:be21df321efb39c5daf3151073ebff7688e15ea6cd5158878bc9559a5db76ac6`  
		Last Modified: Tue, 15 Jun 2021 21:39:16 GMT  
		Size: 2.8 MB (2820718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8415547edc1a6e485a29438531abcddce560a324a068165bb96f98eaf1f22838`  
		Last Modified: Tue, 29 Jun 2021 03:11:24 GMT  
		Size: 664.2 KB (664180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e927028dd328a3da5eb970e84502e2ca2d78d9950eb1815bc3f63dfc9aa5c4ef`  
		Last Modified: Tue, 29 Jun 2021 03:11:27 GMT  
		Size: 11.8 MB (11795304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3092b471e1bd24fe11cbbe112380884903fe95d61aaf2044171fa469a6fcf3a4`  
		Last Modified: Tue, 29 Jun 2021 03:11:24 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e40b91a74120603966ff9f5ca68b4b404aba033e3e0dcf9cb9ccd893785509`  
		Last Modified: Tue, 29 Jun 2021 03:11:25 GMT  
		Size: 2.3 MB (2348534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
