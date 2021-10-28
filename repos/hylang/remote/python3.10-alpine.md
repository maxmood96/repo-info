## `hylang:python3.10-alpine`

```console
$ docker pull hylang@sha256:9a1d0f60505acd2c832d71ab968f69acc4e063edbfe11275dfbfc047bededa91
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

### `hylang:python3.10-alpine` - linux; amd64

```console
$ docker pull hylang@sha256:adc4ae98df7eed329b2e5d6cbc07e89bf78bbddf403e59b3524fef6838c39dc4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20800577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb524d778475d67332fc46536d7a62ef3219e2a0a29a6771f9777ad1f0273f21`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 19:27:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 23:31:48 GMT
ENV LANG=C.UTF-8
# Fri, 27 Aug 2021 23:31:50 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Fri, 27 Aug 2021 23:31:50 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 06 Oct 2021 00:10:08 GMT
ENV PYTHON_VERSION=3.10.0
# Tue, 26 Oct 2021 23:25:36 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Tue, 26 Oct 2021 23:25:38 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 26 Oct 2021 23:25:39 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Tue, 26 Oct 2021 23:25:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 26 Oct 2021 23:25:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Tue, 26 Oct 2021 23:25:39 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Tue, 26 Oct 2021 23:25:50 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 26 Oct 2021 23:25:50 GMT
CMD ["python3"]
# Wed, 27 Oct 2021 00:40:02 GMT
ENV HY_VERSION=1.0a3
# Wed, 27 Oct 2021 00:40:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 27 Oct 2021 00:40:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba51967de001c6e85f574865082c7306be70f40d685b22a82fb7577a67506548`  
		Last Modified: Sat, 28 Aug 2021 00:15:43 GMT  
		Size: 656.4 KB (656378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57f56899fb203f8ea3a83c23ce5bfdfd4156c6e4d41bcccd6a1f5b6867fc514`  
		Last Modified: Tue, 26 Oct 2021 23:57:30 GMT  
		Size: 11.7 MB (11715513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5429bbf616883af130d83202ba6c3c51c4f761f34549ba4b6801527cff31e2d1`  
		Last Modified: Tue, 26 Oct 2021 23:57:28 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60d7396f087dfaf92df3b00852c74a82a0e039ee43a5bd29ef7b1c4569b507a`  
		Last Modified: Tue, 26 Oct 2021 23:57:28 GMT  
		Size: 2.3 MB (2349106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3d9f3416f6f86bd124fbd0b79dc4d353f48da7b35592663c9a7c6d8962b7f3`  
		Last Modified: Wed, 27 Oct 2021 00:45:28 GMT  
		Size: 3.3 MB (3264905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-alpine` - linux; arm variant v6

```console
$ docker pull hylang@sha256:95b4abc09c6221c59ced239dfad452c5e71073128e56689fceb36168ee1f7412
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20236780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efdd4df0125329382491fea2d9bc9556880f2a98dffcc7bb9aaf3c7aeb3474d2`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 22:42:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 22:42:06 GMT
ENV LANG=C.UTF-8
# Fri, 27 Aug 2021 22:42:09 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Fri, 27 Aug 2021 22:42:10 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 06 Oct 2021 00:23:08 GMT
ENV PYTHON_VERSION=3.10.0
# Tue, 26 Oct 2021 23:07:42 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Tue, 26 Oct 2021 23:07:43 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 26 Oct 2021 23:07:44 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Tue, 26 Oct 2021 23:07:44 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 26 Oct 2021 23:07:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Tue, 26 Oct 2021 23:07:45 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Tue, 26 Oct 2021 23:08:03 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 26 Oct 2021 23:08:03 GMT
CMD ["python3"]
# Thu, 28 Oct 2021 01:07:32 GMT
ENV HY_VERSION=1.0a3
# Thu, 28 Oct 2021 01:07:45 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 28 Oct 2021 01:07:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0df3b40b41b9404f3740196daed308df754540b0bda6b97a3b9ed271f41b9c2`  
		Last Modified: Fri, 27 Aug 2021 23:55:02 GMT  
		Size: 661.9 KB (661947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d55702ef00da99d380752549139559c36d4aa8305c719c6ead3fc39a5e7fd1b`  
		Last Modified: Tue, 26 Oct 2021 23:47:10 GMT  
		Size: 11.3 MB (11332690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d98ea8f43909eb707a7ce6578045fd21122ff905de31505fcbadf428a5ebcab`  
		Last Modified: Tue, 26 Oct 2021 23:47:00 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67e41da875685a4d9ac2b7e010bde8b277086013260db45c41af3b5b22e48e6`  
		Last Modified: Tue, 26 Oct 2021 23:47:02 GMT  
		Size: 2.3 MB (2349115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2588709486c9a9f3d1512eaf276c457c226dca0b542e9ee10a13c075d9d7b2a5`  
		Last Modified: Thu, 28 Oct 2021 01:14:28 GMT  
		Size: 3.3 MB (3265346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-alpine` - linux; arm variant v7

```console
$ docker pull hylang@sha256:798f15bef6c2c335d6fdb97ce03f030d8aa7f8baeb8b8fd9f69c7a8aa185e97e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19496790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59f9c4aa5c46e627b2ca8d984b76585ec3bdedbc6e895c908396ce8b0273d4d`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:49:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Aug 2021 00:49:03 GMT
ENV LANG=C.UTF-8
# Sat, 28 Aug 2021 00:49:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 28 Aug 2021 00:49:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 06 Oct 2021 03:41:34 GMT
ENV PYTHON_VERSION=3.10.0
# Wed, 27 Oct 2021 03:05:44 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Wed, 27 Oct 2021 03:05:46 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 27 Oct 2021 03:05:46 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Wed, 27 Oct 2021 03:05:47 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 27 Oct 2021 03:05:47 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Wed, 27 Oct 2021 03:05:47 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Wed, 27 Oct 2021 03:06:02 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 27 Oct 2021 03:06:03 GMT
CMD ["python3"]
# Thu, 28 Oct 2021 02:58:33 GMT
ENV HY_VERSION=1.0a3
# Thu, 28 Oct 2021 02:58:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 28 Oct 2021 02:58:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28fc9ef3efbcdce63be287b234cbd79e8246e453b5abb728ff29e3fe56a283c`  
		Last Modified: Sat, 28 Aug 2021 02:03:32 GMT  
		Size: 655.2 KB (655216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e3150862f6a0717ccf8be19303072bd030d2bb4c11806c8e5f3b1c8243ebf7`  
		Last Modified: Wed, 27 Oct 2021 04:00:39 GMT  
		Size: 10.8 MB (10796731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b361308f44412a0b1ee5d5cf6d4547778d493cb9e7415a23b9f14aa05977754`  
		Last Modified: Wed, 27 Oct 2021 04:00:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e82bd8de7ff9cf82eb4f29180b0857ad5aeef7d3f5af6e7690a375be44e0a6e`  
		Last Modified: Wed, 27 Oct 2021 04:00:34 GMT  
		Size: 2.3 MB (2349101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd76c09cad41ac07ec834be4a9a6d3434b967b6c9eabe71090cc73171862c9c`  
		Last Modified: Thu, 28 Oct 2021 03:11:36 GMT  
		Size: 3.3 MB (3265093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-alpine` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:1d4e8fe3b57da5cfef120ff0fdbb21179c59a17c397c9f098db88fe187be28df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20828810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd8efac336caa8e2ab3b041ef26c1740be26432be5edc69ea86092861ac145a`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Tue, 12 Oct 2021 20:18:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 18:29:00 GMT
ENV LANG=C.UTF-8
# Wed, 13 Oct 2021 18:29:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 13 Oct 2021 18:29:02 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 13 Oct 2021 18:56:36 GMT
ENV PYTHON_VERSION=3.10.0
# Wed, 27 Oct 2021 00:09:16 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Wed, 27 Oct 2021 00:09:16 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 27 Oct 2021 00:09:17 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Wed, 27 Oct 2021 00:09:18 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 27 Oct 2021 00:09:19 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Wed, 27 Oct 2021 00:09:20 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Wed, 27 Oct 2021 00:09:27 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 27 Oct 2021 00:09:28 GMT
CMD ["python3"]
# Wed, 27 Oct 2021 01:09:42 GMT
ENV HY_VERSION=1.0a3
# Wed, 27 Oct 2021 01:09:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 27 Oct 2021 01:09:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e41ad7c31f908109dc305802a72de4a02faf0f46b22f5fadd98430098be7a30`  
		Last Modified: Thu, 14 Oct 2021 05:25:18 GMT  
		Size: 679.5 KB (679461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bb49234ac4664cac8734e1f13b0eee487100039414520bb9209114f6007655`  
		Last Modified: Wed, 27 Oct 2021 00:36:40 GMT  
		Size: 11.8 MB (11823436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a39243d7698a600783797217fa88ffaf2fdd9b87105f28910a652b59b8e771`  
		Last Modified: Wed, 27 Oct 2021 00:36:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222389e8e52c36f005d1deba8191d55b48b531fdd484a8a61b5dd5f89896e672`  
		Last Modified: Wed, 27 Oct 2021 00:36:39 GMT  
		Size: 2.4 MB (2350316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdeb0830818255a51119b93ed840d5aa2a1c315d2f3ec77f80fb13bb3dff27e4`  
		Last Modified: Wed, 27 Oct 2021 01:16:33 GMT  
		Size: 3.3 MB (3263540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-alpine` - linux; 386

```console
$ docker pull hylang@sha256:63ab136243eb642ecdadf527866f36234cbd2b5b5290e29cf149fda37942a5ef
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 MB (21031862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b181ed171a7bc336e36d4afc1c59cf0d783f49f377415c0396e7854716544186`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 27 Aug 2021 17:38:29 GMT
ADD file:42a7bc5a08b546b47049dd0f89ae4e7a8c86342f87000f39ade3ff52916a6c2e in / 
# Fri, 27 Aug 2021 17:38:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 22:56:18 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 22:56:19 GMT
ENV LANG=C.UTF-8
# Fri, 27 Aug 2021 22:56:22 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Fri, 27 Aug 2021 22:56:23 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 06 Oct 2021 00:40:02 GMT
ENV PYTHON_VERSION=3.10.0
# Wed, 27 Oct 2021 01:12:12 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Wed, 27 Oct 2021 01:12:13 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 27 Oct 2021 01:12:14 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Wed, 27 Oct 2021 01:12:14 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 27 Oct 2021 01:12:14 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Wed, 27 Oct 2021 01:12:14 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Wed, 27 Oct 2021 01:12:23 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 27 Oct 2021 01:12:23 GMT
CMD ["python3"]
# Wed, 27 Oct 2021 02:27:44 GMT
ENV HY_VERSION=1.0a3
# Wed, 27 Oct 2021 02:27:49 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 27 Oct 2021 02:27:49 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b11ae9fc5d8a106cfed3a6f6c75e5b5b5797c566fac4411622b4055df6541286`  
		Last Modified: Fri, 27 Aug 2021 17:39:18 GMT  
		Size: 2.8 MB (2822857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb4567e65e64ef30b59e4919454b0e63fd4d1fcf32d86b9f7d9591ce16d23d0`  
		Last Modified: Sat, 28 Aug 2021 00:01:04 GMT  
		Size: 664.2 KB (664205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c758e3b2a81542aac12672310cca7f2662d97b6be6434b75b61fc21c21c47b`  
		Last Modified: Wed, 27 Oct 2021 01:42:40 GMT  
		Size: 11.9 MB (11930598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bc768e6ae4dd86453a373c003ab755a09c52aec2f1089ee581563c3e93255f`  
		Last Modified: Wed, 27 Oct 2021 01:42:38 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b25b5524ec34ba5307722bcccb9cf0729fbc9d1267a8d5717abdb71fc52850`  
		Last Modified: Wed, 27 Oct 2021 01:42:38 GMT  
		Size: 2.3 MB (2349072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c5e8d1da52c1812762cb773877ea161bc2d8053d771a0c5264f239e2280e13`  
		Last Modified: Wed, 27 Oct 2021 02:34:56 GMT  
		Size: 3.3 MB (3264901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-alpine` - linux; ppc64le

```console
$ docker pull hylang@sha256:1314bcda04793f95cf6936511a55cb061c3e5f3d9c581c748882ab1d61605aab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21128783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a63ab130ce3db830b85ca81aa22d647dec8905681a80b6b4cec38117c30be9d`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 01:50:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Aug 2021 01:50:49 GMT
ENV LANG=C.UTF-8
# Sat, 28 Aug 2021 01:50:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 28 Aug 2021 01:51:03 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 07 Oct 2021 02:08:37 GMT
ENV PYTHON_VERSION=3.10.0
# Wed, 27 Oct 2021 03:14:27 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Wed, 27 Oct 2021 03:14:35 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 27 Oct 2021 03:14:37 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Wed, 27 Oct 2021 03:14:38 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 27 Oct 2021 03:14:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Wed, 27 Oct 2021 03:14:40 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Wed, 27 Oct 2021 03:14:54 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 27 Oct 2021 03:14:55 GMT
CMD ["python3"]
# Wed, 27 Oct 2021 07:34:09 GMT
ENV HY_VERSION=1.0a3
# Wed, 27 Oct 2021 07:34:39 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 27 Oct 2021 07:34:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46c7118504c13453ce5a720933b0d109d0da0e556351e697aef027b405284f8`  
		Last Modified: Sat, 28 Aug 2021 02:49:49 GMT  
		Size: 665.0 KB (665029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeaf5081641d4939b023d3d287c106a88aa483cfa97bdcef1645e883985713b5`  
		Last Modified: Wed, 27 Oct 2021 04:01:04 GMT  
		Size: 12.0 MB (12036684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ba710c3e05c32f99fe655ad00a005be3ccebb83ba2935bf8c42ee341287fd7`  
		Last Modified: Wed, 27 Oct 2021 04:01:02 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313d7ac0c3b99a8ed6697739361e0680ef08d4093fa66f3c130aa19118d233db`  
		Last Modified: Wed, 27 Oct 2021 04:01:03 GMT  
		Size: 2.3 MB (2349098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63ae1e7ff2c99e5aa8b75c3bdf28f91dd15711149a1d5122b7dc500c49e2b66`  
		Last Modified: Wed, 27 Oct 2021 07:49:17 GMT  
		Size: 3.3 MB (3265457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-alpine` - linux; s390x

```console
$ docker pull hylang@sha256:3948347401f863cf8578b479ead5e8e7a3dc057273d48f687fccf4423e35b701
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20570306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78b1a29885c9ac4c80363d5a47e3b7c3f69551e1c0a1ed185d1e010abcf8a2d`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 21:01:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Aug 2021 21:01:53 GMT
ENV LANG=C.UTF-8
# Fri, 27 Aug 2021 21:01:56 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Fri, 27 Aug 2021 21:01:56 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 06 Oct 2021 00:11:26 GMT
ENV PYTHON_VERSION=3.10.0
# Tue, 26 Oct 2021 23:32:36 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Tue, 26 Oct 2021 23:32:37 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 26 Oct 2021 23:32:37 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Tue, 26 Oct 2021 23:32:38 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 26 Oct 2021 23:32:38 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Tue, 26 Oct 2021 23:32:38 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Tue, 26 Oct 2021 23:32:43 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 26 Oct 2021 23:32:44 GMT
CMD ["python3"]
# Wed, 27 Oct 2021 01:02:43 GMT
ENV HY_VERSION=1.0a3
# Wed, 27 Oct 2021 01:02:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 27 Oct 2021 01:02:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798844f2ac3ce333d49075582ab558b00ab44e20965b95f5c483dba412e5c678`  
		Last Modified: Sat, 28 Aug 2021 00:38:45 GMT  
		Size: 661.8 KB (661822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d742eb4c4f7f999825c1aa2c507fb4a2fba36ed97b28851bcc07f8835623f8e2`  
		Last Modified: Wed, 27 Oct 2021 00:10:01 GMT  
		Size: 11.7 MB (11691005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898834fff494885dfdc8d9ca364def52dc5d8d257ec561173cece81b6d9d30d6`  
		Last Modified: Wed, 27 Oct 2021 00:09:59 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0bb109473522935429de04067ec4f89b9efb548f03a6052c1a5723ec5c748c`  
		Last Modified: Wed, 27 Oct 2021 00:09:59 GMT  
		Size: 2.3 MB (2348971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c582e57ec5c73c63f7bc28a8792dd30073cee5b5a431ecb80d04ece089c8ac3f`  
		Last Modified: Wed, 27 Oct 2021 01:08:49 GMT  
		Size: 3.3 MB (3264813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
