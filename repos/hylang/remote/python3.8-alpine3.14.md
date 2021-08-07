## `hylang:python3.8-alpine3.14`

```console
$ docker pull hylang@sha256:594eb29f1da669e3ce3a96230217bb52476f143a2de89bb72b7e86f09c7fb2ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `hylang:python3.8-alpine3.14` - linux; amd64

```console
$ docker pull hylang@sha256:c4dd92ce0c41bfd6ba88f5efba8ce1d0cb9aca1b9577605e824c66f998a18d88
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 MB (19811357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd97814201c1451614e86a5244a9801845926562e746f84d3171ea4e743b8aad`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Aug 2021 17:19:45 GMT
ADD file:34eb5c40aa00028921a224d1764ae1b1f3ef710d191e4dfc7df55e0594aa7217 in / 
# Fri, 06 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:37:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 21:11:33 GMT
ENV LANG=C.UTF-8
# Fri, 06 Aug 2021 21:30:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Fri, 06 Aug 2021 21:30:58 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 06 Aug 2021 21:30:58 GMT
ENV PYTHON_VERSION=3.8.11
# Fri, 06 Aug 2021 21:37:04 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 06 Aug 2021 21:37:05 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 06 Aug 2021 21:37:05 GMT
ENV PYTHON_PIP_VERSION=21.2.3
# Fri, 06 Aug 2021 21:37:05 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c20b0cfd643cd4a19246ccf204e2997af70f6b21/public/get-pip.py
# Fri, 06 Aug 2021 21:37:05 GMT
ENV PYTHON_GET_PIP_SHA256=fa6f3fb93cce234cd4e8dd2beb54a51ab9c247653b52855a48dd44e6b21ff28b
# Fri, 06 Aug 2021 21:37:12 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 06 Aug 2021 21:37:12 GMT
CMD ["python3"]
# Sat, 07 Aug 2021 02:31:59 GMT
ENV HY_VERSION=1.0a3
# Sat, 07 Aug 2021 02:32:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 07 Aug 2021 02:32:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:29291e31a76a7e560b9b7ad3cada56e8c18d50a96cca8a2573e4f4689d7aca77`  
		Last Modified: Thu, 05 Aug 2021 15:56:25 GMT  
		Size: 2.8 MB (2813006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3626a090061d56f9d6eaa946c29f4a7600401e2bca3f7b517369d0da709bf6d3`  
		Last Modified: Fri, 06 Aug 2021 22:03:22 GMT  
		Size: 281.5 KB (281505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab7c3958d02c548f8a01137383d178a982079695cda15bda551d17fde69092`  
		Last Modified: Fri, 06 Aug 2021 22:03:25 GMT  
		Size: 11.2 MB (11244323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d9978a71b93404de628d3705cbf22d6b284b0264c244c84a0ba170ce640cb7`  
		Last Modified: Fri, 06 Aug 2021 22:03:22 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e93103535260c51fbb6da1174085bd794ca3be8324fa69cabebe1df938391e0`  
		Last Modified: Fri, 06 Aug 2021 22:03:23 GMT  
		Size: 2.4 MB (2355097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8bb867fcafb2279aa96b3a17f3147eda52c216d41e85d1420b0f9357ed4ac7`  
		Last Modified: Sat, 07 Aug 2021 02:36:33 GMT  
		Size: 3.1 MB (3117189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8-alpine3.14` - linux; arm variant v6

```console
$ docker pull hylang@sha256:7e5eb88ed4ef12245b3f706bfc4f763ee32a5db17c3d5e92d01373f2864fafe1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19208578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa17ee7e8b4d447b3d037a815736d6512bc4ba994f13e0e1f4a4026bdd6bdc67`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Aug 2021 17:49:32 GMT
ADD file:7f2c7deda009eabdcbbdccb11e854043d32c498e64e7e1ca02165d7bb4261d39 in / 
# Fri, 06 Aug 2021 17:49:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 22:10:56 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 22:10:56 GMT
ENV LANG=C.UTF-8
# Fri, 06 Aug 2021 22:40:35 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Fri, 06 Aug 2021 22:40:36 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 06 Aug 2021 22:40:37 GMT
ENV PYTHON_VERSION=3.8.11
# Fri, 06 Aug 2021 22:53:28 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 06 Aug 2021 22:53:29 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 06 Aug 2021 22:53:30 GMT
ENV PYTHON_PIP_VERSION=21.2.3
# Fri, 06 Aug 2021 22:53:30 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c20b0cfd643cd4a19246ccf204e2997af70f6b21/public/get-pip.py
# Fri, 06 Aug 2021 22:53:31 GMT
ENV PYTHON_GET_PIP_SHA256=fa6f3fb93cce234cd4e8dd2beb54a51ab9c247653b52855a48dd44e6b21ff28b
# Fri, 06 Aug 2021 22:53:46 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 06 Aug 2021 22:53:47 GMT
CMD ["python3"]
# Sat, 07 Aug 2021 03:31:38 GMT
ENV HY_VERSION=1.0a3
# Sat, 07 Aug 2021 03:31:49 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 07 Aug 2021 03:31:50 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f465bb3e9fcd0c42f936ecc566c6e40353c00f3089b2b2c2ea1663c30f89d3ab`  
		Last Modified: Fri, 06 Aug 2021 17:51:00 GMT  
		Size: 2.6 MB (2626350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fce632e670bccbc0903da70add2d72568a9c2b703cbe9aa1a968f6d0bfb7673`  
		Last Modified: Fri, 06 Aug 2021 23:31:33 GMT  
		Size: 281.7 KB (281674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d4f66268ec3e17e61e9e6e91bcbacea5fc85d0ea6f77132eb749e238f75d71`  
		Last Modified: Fri, 06 Aug 2021 23:31:39 GMT  
		Size: 10.8 MB (10827493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5d2f94b7fc6ae598dcf5b448ed7b645be05a981c081747beb52027deda0da9`  
		Last Modified: Fri, 06 Aug 2021 23:31:32 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2756aa4d1badba0e523c99e90593b3e57d35ad18df1796cd1835c70983b834e`  
		Last Modified: Fri, 06 Aug 2021 23:31:34 GMT  
		Size: 2.4 MB (2355217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791dff201a5b7049d7cd8e6bfcf5860dc34eb9447f5c8c1b7c5e8c8989ab2961`  
		Last Modified: Sat, 07 Aug 2021 03:38:35 GMT  
		Size: 3.1 MB (3117615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8-alpine3.14` - linux; arm variant v7

```console
$ docker pull hylang@sha256:9142af46693210167ca47af560c29a4544055e6c65cadec96d39142bdc66707d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18530598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68646dcba11d816da1a7696bd8514f54f639a8e6205fef1ef7c3f8529db8e82`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:19 GMT
ADD file:416a8b507abdc6bdcb22997a4be0a4170796c3f9f77e315b2dbff2b0a212bc68 in / 
# Fri, 30 Jul 2021 18:36:20 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 04:09:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 31 Jul 2021 04:09:55 GMT
ENV LANG=C.UTF-8
# Sat, 31 Jul 2021 04:58:03 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Sat, 31 Jul 2021 04:58:04 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 31 Jul 2021 04:58:04 GMT
ENV PYTHON_VERSION=3.8.11
# Sat, 31 Jul 2021 05:08:29 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Sat, 31 Jul 2021 05:08:31 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 02 Aug 2021 19:15:04 GMT
ENV PYTHON_PIP_VERSION=21.2.2
# Mon, 02 Aug 2021 19:15:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a1675ab6c2bd898ed82b1f58c486097f763c74a9/public/get-pip.py
# Mon, 02 Aug 2021 19:15:05 GMT
ENV PYTHON_GET_PIP_SHA256=6665659241292b2147b58922b9ffe11dda66b39d52d8a6f3aa310bc1d60ea6f7
# Mon, 02 Aug 2021 19:15:19 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 02 Aug 2021 19:15:19 GMT
CMD ["python3"]
# Mon, 02 Aug 2021 20:25:28 GMT
ENV HY_VERSION=1.0a3
# Mon, 02 Aug 2021 20:25:39 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Mon, 02 Aug 2021 20:25:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:136482bf81d1fa351b424ebb8c7e34d15f2c5ed3fc0b66b544b8312bda3d52d9`  
		Last Modified: Tue, 15 Jun 2021 23:16:40 GMT  
		Size: 2.4 MB (2427917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4061aa28c86910cd42eea4d762e0cf0e61a27140de7175219cf4e9364597f4f3`  
		Last Modified: Sat, 31 Jul 2021 06:28:49 GMT  
		Size: 280.8 KB (280826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd391f78e38ed39de7e5861567242f0d5c615ea69f8148125324d33384880fcb`  
		Last Modified: Sat, 31 Jul 2021 06:28:55 GMT  
		Size: 10.3 MB (10349380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293fb3804fecc38aa3765c392fee5a73c5da3686a2b5bca7fa443a22168f9ef8`  
		Last Modified: Sat, 31 Jul 2021 06:28:49 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1462e8b303c89ce8d5925b30fff806a3ba307872fa4a91c1650de2c580e9a6a4`  
		Last Modified: Mon, 02 Aug 2021 19:33:26 GMT  
		Size: 2.4 MB (2355869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f620c2bb8889178cca22bf50f4c1897da3aa540a97c8c1031f77a721f335255`  
		Last Modified: Mon, 02 Aug 2021 20:36:29 GMT  
		Size: 3.1 MB (3116374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:5d4e2888e9863139402cf032932735345a265433c923a602fd7bee231715f6a8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 MB (19767209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3203a20240f1d20b731aed7c46bbfb96f808ce5f161f238ab9dfe6138305b7`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Aug 2021 17:39:26 GMT
ADD file:1a8fd1066485e1261462e689c1a072f010c1d3be904b73ef2b84128fac652951 in / 
# Fri, 06 Aug 2021 17:39:27 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:48:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 23:28:08 GMT
ENV LANG=C.UTF-8
# Fri, 06 Aug 2021 23:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Fri, 06 Aug 2021 23:43:27 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 06 Aug 2021 23:43:28 GMT
ENV PYTHON_VERSION=3.8.11
# Fri, 06 Aug 2021 23:49:18 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 06 Aug 2021 23:49:19 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 06 Aug 2021 23:49:19 GMT
ENV PYTHON_PIP_VERSION=21.2.3
# Fri, 06 Aug 2021 23:49:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c20b0cfd643cd4a19246ccf204e2997af70f6b21/public/get-pip.py
# Fri, 06 Aug 2021 23:49:20 GMT
ENV PYTHON_GET_PIP_SHA256=fa6f3fb93cce234cd4e8dd2beb54a51ab9c247653b52855a48dd44e6b21ff28b
# Fri, 06 Aug 2021 23:49:26 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 06 Aug 2021 23:49:26 GMT
CMD ["python3"]
# Sat, 07 Aug 2021 04:09:02 GMT
ENV HY_VERSION=1.0a3
# Sat, 07 Aug 2021 04:09:07 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 07 Aug 2021 04:09:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:fd3acdcea5682abced546ec19fb6ebee725c5184e5d91614c469c0a79e67f2d0`  
		Last Modified: Fri, 06 Aug 2021 17:40:12 GMT  
		Size: 2.7 MB (2710613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd496dba037efd04fc4937dd16b10cb87ae37d722c8751ef5f9adbfd57f4f116`  
		Last Modified: Sat, 07 Aug 2021 00:15:12 GMT  
		Size: 281.7 KB (281684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda0ce65f112f2e6ab6630c071313b585c0847c3907a8ac344aa3805af1f73d8`  
		Last Modified: Sat, 07 Aug 2021 00:15:13 GMT  
		Size: 11.3 MB (11302197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecac5d64d22c7436ce090e68d6c2d58d2f472c10188a57e2843380dbca3b55dc`  
		Last Modified: Sat, 07 Aug 2021 00:15:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a97cc82a5390d15e7e3d382e8c173027f342ab5d60a72aadf2b41b5642dd732`  
		Last Modified: Sat, 07 Aug 2021 00:15:12 GMT  
		Size: 2.4 MB (2355244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d011512c7a91875104563f0fa5c0b6ed8ac919d5284e324f68c2b008e5d21c`  
		Last Modified: Sat, 07 Aug 2021 04:15:19 GMT  
		Size: 3.1 MB (3117241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8-alpine3.14` - linux; 386

```console
$ docker pull hylang@sha256:fbafc0447b4d7848e306192d42d38dfb2eda67202bf8528574c0a86f5f7e4468
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (20007692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ac562e224807c607ebca5f792837edca9216e6c5f440fa5259ccdd8ac0fa93`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 15 Jun 2021 21:38:30 GMT
ADD file:3b0fe1454491bb05e218b090fd461f2fd39546aa4a53eb3f953ee8eae149ac57 in / 
# Tue, 15 Jun 2021 21:38:30 GMT
CMD ["/bin/sh"]
# Tue, 29 Jun 2021 02:07:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Jun 2021 02:07:54 GMT
ENV LANG=C.UTF-8
# Tue, 29 Jun 2021 02:38:14 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Tue, 29 Jun 2021 02:38:14 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 29 Jun 2021 20:42:35 GMT
ENV PYTHON_VERSION=3.8.11
# Tue, 29 Jun 2021 20:51:04 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Tue, 29 Jun 2021 20:51:05 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 02 Aug 2021 19:47:52 GMT
ENV PYTHON_PIP_VERSION=21.2.2
# Mon, 02 Aug 2021 19:47:52 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a1675ab6c2bd898ed82b1f58c486097f763c74a9/public/get-pip.py
# Mon, 02 Aug 2021 19:47:52 GMT
ENV PYTHON_GET_PIP_SHA256=6665659241292b2147b58922b9ffe11dda66b39d52d8a6f3aa310bc1d60ea6f7
# Mon, 02 Aug 2021 19:47:59 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 02 Aug 2021 19:48:00 GMT
CMD ["python3"]
# Mon, 02 Aug 2021 20:19:11 GMT
ENV HY_VERSION=1.0a3
# Mon, 02 Aug 2021 20:19:17 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Mon, 02 Aug 2021 20:19:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:be21df321efb39c5daf3151073ebff7688e15ea6cd5158878bc9559a5db76ac6`  
		Last Modified: Tue, 15 Jun 2021 21:39:16 GMT  
		Size: 2.8 MB (2820718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4375b97fa1be50b8c21c45aa9ec86dfcc7e105ac701ed497d224f69b456c5d3`  
		Last Modified: Tue, 29 Jun 2021 03:14:30 GMT  
		Size: 282.1 KB (282050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a096ddb1f55700003253d1f3f33ecfc93121b8bd8d75b963b6d8c475f0b3a69b`  
		Last Modified: Tue, 29 Jun 2021 22:59:13 GMT  
		Size: 11.4 MB (11432825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e56c2c05ac7d571352c6fdd5a0534cf03cea39b9d6c452255799e22c168945`  
		Last Modified: Tue, 29 Jun 2021 22:59:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02156ecb7d2cc3c076a8242f1a42f2a55bff3ff8136af6d17f46a8068f4c3c7`  
		Last Modified: Mon, 02 Aug 2021 19:59:07 GMT  
		Size: 2.4 MB (2355740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93343cc3b0b815a5d67f7bff00a20459173c117b68cb03d3961f9736d44e471f`  
		Last Modified: Mon, 02 Aug 2021 20:25:46 GMT  
		Size: 3.1 MB (3116129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8-alpine3.14` - linux; ppc64le

```console
$ docker pull hylang@sha256:a8773466a54f54be4d275f236792642f64bf5bb08bc894d6dd7f5fce092ccad5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20106023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4480818649388ac8a2c23dfd9531216e68414fd32c5dc13f6d150876e714ba8a`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:34:32 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Aug 2021 18:34:35 GMT
ENV LANG=C.UTF-8
# Fri, 06 Aug 2021 19:06:10 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	;
# Fri, 06 Aug 2021 19:06:14 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 06 Aug 2021 19:06:17 GMT
ENV PYTHON_VERSION=3.8.11
# Fri, 06 Aug 2021 19:14:23 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Fri, 06 Aug 2021 19:14:37 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 06 Aug 2021 19:14:41 GMT
ENV PYTHON_PIP_VERSION=21.2.3
# Fri, 06 Aug 2021 19:14:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c20b0cfd643cd4a19246ccf204e2997af70f6b21/public/get-pip.py
# Fri, 06 Aug 2021 19:14:47 GMT
ENV PYTHON_GET_PIP_SHA256=fa6f3fb93cce234cd4e8dd2beb54a51ab9c247653b52855a48dd44e6b21ff28b
# Fri, 06 Aug 2021 19:15:05 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 06 Aug 2021 19:15:10 GMT
CMD ["python3"]
# Sat, 07 Aug 2021 03:42:18 GMT
ENV HY_VERSION=1.0a3
# Sat, 07 Aug 2021 03:42:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 07 Aug 2021 03:42:53 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8479c3e0d7fec98095b4beac83f9d91b5eb0795b66b61644662edddb55f1ab7`  
		Last Modified: Fri, 06 Aug 2021 19:53:50 GMT  
		Size: 283.6 KB (283636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd00c6b7f8be2d488a85f3f400565c742712995e13465b5cd562e467e2297c1`  
		Last Modified: Fri, 06 Aug 2021 19:53:52 GMT  
		Size: 11.5 MB (11538309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cf673c9a800fb0c3a01c50e8e181475f75dc25e5b27631f04b218227151342`  
		Last Modified: Fri, 06 Aug 2021 19:53:49 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7670981af5066182c98bf431ebc83d7bad203971ee7f926722bcf4c6041323`  
		Last Modified: Fri, 06 Aug 2021 19:53:50 GMT  
		Size: 2.4 MB (2355249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8e694c5544fc24a31493c019eb96200f2def2b7f7be380b69b3ed4bef65fed`  
		Last Modified: Sat, 07 Aug 2021 03:59:40 GMT  
		Size: 3.1 MB (3117448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
