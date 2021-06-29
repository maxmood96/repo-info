## `python:alpine3.14`

```console
$ docker pull python@sha256:4f73d4c73e745c4622e3c5b2a5a78c314374f2d7110787ff11ee6d33357fdd57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `python:alpine3.14` - linux; amd64

```console
$ docker pull python@sha256:7b7de9ac217104d68fe5c1847e8124867a0a375ff72a5726436d51ebafa163cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17286446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d7d315652743e932c5bf63bced3c9bc082ac37b4060aa8b841a3353996b84f`
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
# Tue, 29 Jun 2021 01:30:49 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 29 Jun 2021 01:30:49 GMT
ENV PYTHON_VERSION=3.9.5
# Tue, 29 Jun 2021 01:37:34 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Tue, 29 Jun 2021 01:37:35 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 29 Jun 2021 01:37:36 GMT
ENV PYTHON_PIP_VERSION=21.1.3
# Tue, 29 Jun 2021 01:37:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a1675ab6c2bd898ed82b1f58c486097f763c74a9/public/get-pip.py
# Tue, 29 Jun 2021 01:37:36 GMT
ENV PYTHON_GET_PIP_SHA256=6665659241292b2147b58922b9ffe11dda66b39d52d8a6f3aa310bc1d60ea6f7
# Tue, 29 Jun 2021 01:37:45 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 29 Jun 2021 01:37:45 GMT
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
	-	`sha256:dbb464156bd73586e055c8dea3805dd73a5ecdfdd219d4aa3736ac6fd684094a`  
		Last Modified: Tue, 29 Jun 2021 02:10:34 GMT  
		Size: 11.5 MB (11469916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb580d0cf6ebfcb6f936f28e8e9ab21d5ba1cf02190b390f453048e93dd6f1b5`  
		Last Modified: Tue, 29 Jun 2021 02:10:31 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c048b1b73dfdaceda9b9f7b26ab664b6bce07b28347d28f24f04f0504db6819d`  
		Last Modified: Tue, 29 Jun 2021 02:10:32 GMT  
		Size: 2.3 MB (2348479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:alpine3.14` - linux; arm variant v6

```console
$ docker pull python@sha256:45a60de6e0fa80ed07bbd139b87f7e81bf3d8747c62178e6902493e594a09676
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16654273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c42837945e3f30c55dde837b41a67df174e4650f08e5ee67091361b4c8064c`
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
# Mon, 28 Jun 2021 21:42:20 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 28 Jun 2021 21:42:21 GMT
ENV PYTHON_VERSION=3.9.5
# Mon, 28 Jun 2021 21:54:17 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Mon, 28 Jun 2021 21:54:19 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 28 Jun 2021 21:54:19 GMT
ENV PYTHON_PIP_VERSION=21.1.3
# Mon, 28 Jun 2021 21:54:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a1675ab6c2bd898ed82b1f58c486097f763c74a9/public/get-pip.py
# Mon, 28 Jun 2021 21:54:20 GMT
ENV PYTHON_GET_PIP_SHA256=6665659241292b2147b58922b9ffe11dda66b39d52d8a6f3aa310bc1d60ea6f7
# Mon, 28 Jun 2021 21:54:37 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 28 Jun 2021 21:54:38 GMT
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
	-	`sha256:4ee6fb9463b85ede07740b2d78eaa5bdf348ab0ba1d8e96d2e2b49e655b2e91c`  
		Last Modified: Mon, 28 Jun 2021 23:37:04 GMT  
		Size: 11.0 MB (11019047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b31d3781c621c3c6db1ecf0db79cf0f7081a7f0205b1993d2ddc849ea7718f`  
		Last Modified: Mon, 28 Jun 2021 23:36:56 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db84bdaad6ac66a449c0df61e7ddb60380a6128fc141c052b3fc2ea7ce8adda8`  
		Last Modified: Mon, 28 Jun 2021 23:36:59 GMT  
		Size: 2.3 MB (2348637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:alpine3.14` - linux; arm variant v7

```console
$ docker pull python@sha256:2e5060abbe21794ed795b721b0b7f1dddb50f745826aa30367f50b9201380159
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15960703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb81e814395926e678902cd69a93742861f0c4f73bece56ba127892eb75ef6e2`
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
# Tue, 29 Jun 2021 01:01:02 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 29 Jun 2021 01:01:03 GMT
ENV PYTHON_VERSION=3.9.5
# Tue, 29 Jun 2021 01:11:48 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Tue, 29 Jun 2021 01:11:50 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 29 Jun 2021 01:11:50 GMT
ENV PYTHON_PIP_VERSION=21.1.3
# Tue, 29 Jun 2021 01:11:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a1675ab6c2bd898ed82b1f58c486097f763c74a9/public/get-pip.py
# Tue, 29 Jun 2021 01:11:51 GMT
ENV PYTHON_GET_PIP_SHA256=6665659241292b2147b58922b9ffe11dda66b39d52d8a6f3aa310bc1d60ea6f7
# Tue, 29 Jun 2021 01:12:08 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 29 Jun 2021 01:12:08 GMT
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
	-	`sha256:9a87484dce9e71fa8b1ecfe700b9c9fc252112718337d3acb3d0c1aa25bc65a0`  
		Last Modified: Tue, 29 Jun 2021 02:09:17 GMT  
		Size: 10.5 MB (10528728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6527c7e605638c93a1a4fd830fec80a567c0d1f184387b9059f423b74def2ecb`  
		Last Modified: Tue, 29 Jun 2021 02:09:10 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4b5838cb99bb2e85b1889ce55acc19762ef710e017a729b4b0f15b1b8eadf2`  
		Last Modified: Tue, 29 Jun 2021 02:09:13 GMT  
		Size: 2.3 MB (2348614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:alpine3.14` - linux; arm64 variant v8

```console
$ docker pull python@sha256:d491ee7ab6ea12b278dd9e8bde32474b157ac03a76d665d39606170fa1833a7e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17233331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e955670326b52d82093bb0f04790b1300620a1af4b1e54e4948c722efc91511`
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
# Mon, 28 Jun 2021 23:41:24 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 28 Jun 2021 23:41:25 GMT
ENV PYTHON_VERSION=3.9.5
# Mon, 28 Jun 2021 23:47:43 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Mon, 28 Jun 2021 23:47:44 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 28 Jun 2021 23:47:44 GMT
ENV PYTHON_PIP_VERSION=21.1.3
# Mon, 28 Jun 2021 23:47:44 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a1675ab6c2bd898ed82b1f58c486097f763c74a9/public/get-pip.py
# Mon, 28 Jun 2021 23:47:44 GMT
ENV PYTHON_GET_PIP_SHA256=6665659241292b2147b58922b9ffe11dda66b39d52d8a6f3aa310bc1d60ea6f7
# Mon, 28 Jun 2021 23:47:52 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 28 Jun 2021 23:47:52 GMT
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
	-	`sha256:bb35478c04a4cc80c0b5d2b7b5bfb03a0316cbd0ae04f39cbd633c5fe10a2aa3`  
		Last Modified: Tue, 29 Jun 2021 00:20:12 GMT  
		Size: 11.5 MB (11516198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232d9f772b7c6256a83ee3e2362ea482bf0e4b19f92a068fbc80274eaf24ecfc`  
		Last Modified: Tue, 29 Jun 2021 00:20:10 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a3f8347299d4b16aa2f618732bbfb18f1225fb6a8e6796fdc21fefbedd1f14`  
		Last Modified: Tue, 29 Jun 2021 00:20:10 GMT  
		Size: 2.3 MB (2348472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:alpine3.14` - linux; 386

```console
$ docker pull python@sha256:2a292f43aa5dd791e1eb229e917c908f719db020b6bd9ad561cb850d3476ba28
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17484434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31eb475321c9fcb96d73cbe8658d1c9d623b6896da8a36e0b4a7904ac728e612`
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
# Tue, 29 Jun 2021 02:28:21 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 29 Jun 2021 02:28:21 GMT
ENV PYTHON_VERSION=3.9.5
# Tue, 29 Jun 2021 02:37:00 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Tue, 29 Jun 2021 02:37:01 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 29 Jun 2021 02:37:01 GMT
ENV PYTHON_PIP_VERSION=21.1.3
# Tue, 29 Jun 2021 02:37:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a1675ab6c2bd898ed82b1f58c486097f763c74a9/public/get-pip.py
# Tue, 29 Jun 2021 02:37:01 GMT
ENV PYTHON_GET_PIP_SHA256=6665659241292b2147b58922b9ffe11dda66b39d52d8a6f3aa310bc1d60ea6f7
# Tue, 29 Jun 2021 02:37:10 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 29 Jun 2021 02:37:10 GMT
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
	-	`sha256:d250d70b4f1b95366dfd6671a4650e7fbd3f602214d2253b8c0041256d719cc8`  
		Last Modified: Tue, 29 Jun 2021 03:13:06 GMT  
		Size: 11.7 MB (11650884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56295a7401f4c7b7bca497fb1cf3639c3467570f58486ae46b130c898089e66`  
		Last Modified: Tue, 29 Jun 2021 03:13:03 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5906f76acf25b55e3517e3969d47f8ac55100a8eea10a3db233cb50fab634a8e`  
		Last Modified: Tue, 29 Jun 2021 03:13:04 GMT  
		Size: 2.3 MB (2348421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
