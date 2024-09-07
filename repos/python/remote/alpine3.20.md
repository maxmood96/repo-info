## `python:alpine3.20`

```console
$ docker pull python@sha256:4dae8a34125c839fce52c0b4efa963b1be1ce7e84df8eb1a62136049010916da
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

### `python:alpine3.20` - linux; amd64

```console
$ docker pull python@sha256:03a4136a9c700db1cd105384d0f2e9f5c7eec169db62f56f7c9e7a89d9b3f995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17254749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de975f3f5997fef7d279dd25b8aea9e2abed6e7c2e9a5c4d095dab12db393471`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 29 Aug 2024 23:26:33 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Thu, 29 Aug 2024 23:26:33 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 23:26:33 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_VERSION=3.12.5
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_PIP_VERSION=24.2
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9afd1f50702b9ff2b187430471498298c96d4919de0ed435aa4ecaf72ba6534`  
		Last Modified: Fri, 06 Sep 2024 23:29:45 GMT  
		Size: 455.1 KB (455090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057327fbabf5b9b7038e4d0a243f4362e8ccc878c8e32da2530d9a052378a77f`  
		Last Modified: Fri, 06 Sep 2024 23:31:34 GMT  
		Size: 11.5 MB (11502028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b084f291fbf3323df5fbe8cec0ac91312fc6c4108c274279263f75819fa0033c`  
		Last Modified: Fri, 06 Sep 2024 23:31:34 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964622a07b8dca4a81e4e0274f48ea6fe02af782d6bbcae22e11ba1efc5abd0c`  
		Last Modified: Fri, 06 Sep 2024 23:31:34 GMT  
		Size: 1.7 MB (1673595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.20` - unknown; unknown

```console
$ docker pull python@sha256:caa2322eb9b46fe443d4244b6e6e980a142a9c354a773ea1141fed46cc707d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.7 KB (673721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159f2228724446c279cabe08cd17789c3c96b969344636ad8c3567e49b27e925`

```dockerfile
```

-	Layers:
	-	`sha256:0d3759dc5a18ee1de12e9fa7b1a4eb6d80f9ec7e916e5dddf011099cd109af19`  
		Last Modified: Fri, 06 Sep 2024 23:31:34 GMT  
		Size: 648.2 KB (648224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b0e091c111379ce0e72609e0e49ad585d5d37498e86134f5451130d127d063c`  
		Last Modified: Fri, 06 Sep 2024 23:31:34 GMT  
		Size: 25.5 KB (25497 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.20` - linux; arm variant v6

```console
$ docker pull python@sha256:5636ef2a6ed2a6ac70ecfe5791a23d14090b68df6f5e9c6f9360b3f4dce907f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16576775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0f8a30963157f5cc2bd77be3954256e24fd18f0ea5439c34a23df3fef8559c`
-	Default Command: `["python3"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 23:26:33 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_VERSION=3.12.5
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_PIP_VERSION=24.2
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38d5916d3896eb1d9b31289f1279c077609d768fa196443664651576bbc20cc`  
		Last Modified: Wed, 07 Aug 2024 19:47:36 GMT  
		Size: 462.6 KB (462575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f6771ce62c932b2f851197725d6b7c350c905b2621567cc63e4ae4ba8bd734`  
		Last Modified: Wed, 07 Aug 2024 19:47:36 GMT  
		Size: 11.1 MB (11075198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41f3990b196fb60efd04f17aac0745ab0ede1ba1b439336cdc06e5ca47f31fd`  
		Last Modified: Wed, 07 Aug 2024 19:47:35 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88aa8cd0dd4fa2e5e7c5e3f3181055625236dc2c680ccb86edddf20ec1e52175`  
		Last Modified: Wed, 04 Sep 2024 06:39:41 GMT  
		Size: 1.7 MB (1673583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.20` - unknown; unknown

```console
$ docker pull python@sha256:169433c1d98dea06976a8dd820cbc8d8733d3dd8d18163762f674cd9ddfd5289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22824dba5ced7a214d96c00f55808e0f8aa7fd5e39b7e4c26bc340d92dd02c4`

```dockerfile
```

-	Layers:
	-	`sha256:15e0e356b12ecd99c4894e4ef79cd6caee48b546cf7525eba5bff9102222684f`  
		Last Modified: Wed, 04 Sep 2024 06:39:40 GMT  
		Size: 25.4 KB (25419 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.20` - linux; arm variant v7

```console
$ docker pull python@sha256:9bcb5a4960b058c3ff048e5c58a802452c4deede781d0a3174c8054abbc397c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17819462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a2a8c05f03005e840befb0ac74afdf19db803fb13527b34423edbcf3495eba`
-	Default Command: `["python3"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 23:26:33 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_VERSION=3.12.5
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_PIP_VERSION=24.2
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ef77f3591f9a13a2d038b8d57b659d41ac91d2de7301c4ab9e6c12c44d058c`  
		Last Modified: Wed, 24 Jul 2024 09:43:23 GMT  
		Size: 461.8 KB (461753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8254ff524ae1d56e74788b8ccbfabd73bf8ab959bd61f499c439f7c2789cf19b`  
		Last Modified: Wed, 04 Sep 2024 08:49:37 GMT  
		Size: 12.6 MB (12588913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1a4b335d59f5dc3c242d4d26fb2136663d43982ed7c4d54f97d8531b8d287b`  
		Last Modified: Wed, 04 Sep 2024 08:49:36 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca6d2501c359a67a67c3f88d2332658e4bdad2a022bbb14eaad29d753741676`  
		Last Modified: Wed, 04 Sep 2024 08:49:37 GMT  
		Size: 1.7 MB (1673608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.20` - unknown; unknown

```console
$ docker pull python@sha256:9e5c405a44c792f1a8a9ec34b5ae191bee36e80cf69b6102527a52edc3ca4d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.8 KB (676794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e46cbe1eb9f0e64e87e7d201ee60a0ce2788c8c858e9dbb9eebbd0e48e5b4a8`

```dockerfile
```

-	Layers:
	-	`sha256:42199b8eb4760a656dfc51ddeb0314b61073721b07e5100e6d6f10fc1882d275`  
		Last Modified: Wed, 04 Sep 2024 08:49:36 GMT  
		Size: 651.2 KB (651156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d57dc74254375dc17f63ba9f8d0040297891a32a98cf95adbdb7871f098c231`  
		Last Modified: Wed, 04 Sep 2024 08:49:36 GMT  
		Size: 25.6 KB (25638 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull python@sha256:7e075906c70c45c4ffba435201109fe5ac221a0f77731bae80034d7ce9241b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20622997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927524c80f5e20975d88d118e63f71eae184286801545c7090ff89cffb1b045f`
-	Default Command: `["python3"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 23:26:33 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_VERSION=3.12.5
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_PIP_VERSION=24.2
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa7aa6ad9d5c7fbdfa91631684bd60282df5d9a94099d8535203a5717b03d0a`  
		Last Modified: Wed, 04 Sep 2024 07:15:43 GMT  
		Size: 463.8 KB (463838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292fd645e195b7a208213ef911ad198fc3aca307f7c54bd3a581eeb5c44f869e`  
		Last Modified: Wed, 04 Sep 2024 07:15:44 GMT  
		Size: 14.4 MB (14398397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef367b93c87ccec2c6b7ed4cafe5cbf060fd71cee433b8ad5eb9192a376f5afa`  
		Last Modified: Wed, 04 Sep 2024 07:15:43 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a706c085b2779621b071f6d3824a9ebbf466885e752bec91162ea91805e52e81`  
		Last Modified: Wed, 04 Sep 2024 07:15:44 GMT  
		Size: 1.7 MB (1673598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.20` - unknown; unknown

```console
$ docker pull python@sha256:3c147f8380ab60cbec31732e07f7c9213deddf44155f49585baa9f37f9d89c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.2 KB (674173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac7be4bf20ac56efdb91eecb886f2e8272879e2c1db466fb4a23e3ea4d36019`

```dockerfile
```

-	Layers:
	-	`sha256:aea2735234ce229f93b370661e5072de1c2e74bc74b0ce2aa95849dd1f41cf8c`  
		Last Modified: Wed, 04 Sep 2024 07:15:44 GMT  
		Size: 648.3 KB (648328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd601b119888e9d2695fe862c37f0e0cd2fbe84209facba7dd4a2ee5b3b4b625`  
		Last Modified: Wed, 04 Sep 2024 07:15:43 GMT  
		Size: 25.8 KB (25845 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.20` - linux; 386

```console
$ docker pull python@sha256:e0cdf34ea21a01dbd1fe57bf7e7a808fe36bd279188446746e83e8fe77f76043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17301165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a280a5cf25fa1c09a060f193179e9e8239c68e5fe10142ac941dbf120dc521`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 29 Aug 2024 23:26:33 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Thu, 29 Aug 2024 23:26:33 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 23:26:33 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_VERSION=3.12.5
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_PIP_VERSION=24.2
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96fc95a92a0152441c08d8a3bf8c278766d9886d03101bd5ef418bdad36c45cb`  
		Last Modified: Fri, 06 Sep 2024 23:33:08 GMT  
		Size: 455.6 KB (455555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086462c2bde1170518d22e1bbff619e35f24e1b5a367fc1fb293a92f278063ba`  
		Last Modified: Fri, 06 Sep 2024 23:33:09 GMT  
		Size: 11.7 MB (11702632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263689f745a7b22e3afe9acd3255e8092d7e078b7520809ec403ac5cb8b070da`  
		Last Modified: Fri, 06 Sep 2024 23:33:08 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7728402efceba3a6be337bd443852fe55d5acdb07d4ddfe0f921a5c7d6019e5`  
		Last Modified: Fri, 06 Sep 2024 23:33:08 GMT  
		Size: 1.7 MB (1673583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.20` - unknown; unknown

```console
$ docker pull python@sha256:55c312ddccdae322382989a9f2dda7ca079f15f9ee3db4b7089a5b47327c24b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.6 KB (673621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f4933a4edb8d41924154d40b732057f6d7724db75a8048b5c385bb21b1f960`

```dockerfile
```

-	Layers:
	-	`sha256:6579beaf10394115a4a96d33232ba70aa111d6e0a3a3db60e7f6dce9320a1a52`  
		Last Modified: Fri, 06 Sep 2024 23:33:08 GMT  
		Size: 648.2 KB (648179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4962745bf0e592aceaf50cc07bc3218f2f2a1ccfbb26a73f2c348cdc575f343`  
		Last Modified: Fri, 06 Sep 2024 23:33:08 GMT  
		Size: 25.4 KB (25442 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.20` - linux; ppc64le

```console
$ docker pull python@sha256:0ef75d4ee693936ecfb0bec62ee4e58e8147cca69dfe6d2f184f291f60611e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (20001617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ea8c3df152259c7acb7a1f1bb7804d8f7737eb8b1fc2d2d9ff552ba317eaf0`
-	Default Command: `["python3"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 23:26:33 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_VERSION=3.12.5
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_PIP_VERSION=24.2
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98be566dfd5104c6e58a7ac8bcd83ced66237176a42a2f0d7988feb69814c443`  
		Last Modified: Wed, 04 Sep 2024 07:22:55 GMT  
		Size: 464.2 KB (464221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c0b4229e41c7d452f99f18aec1fd4e68b972f532e91311875987192d186f79`  
		Last Modified: Wed, 04 Sep 2024 10:34:48 GMT  
		Size: 14.3 MB (14292012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda519db8931ddf86b3fc03e57970c5187490a3f6af2b5cae24a161de6f3aaaa`  
		Last Modified: Wed, 04 Sep 2024 10:34:47 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdef8b16b4c4d9ebba52963e586b4b113f010d86a0a4ae6d58599529090d1537`  
		Last Modified: Wed, 04 Sep 2024 10:34:47 GMT  
		Size: 1.7 MB (1673599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.20` - unknown; unknown

```console
$ docker pull python@sha256:785efb36e89ec3123e2d35f16674d0cd2b21504cc61475de28fa4173befe8422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.9 KB (671893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19e51f700271482cb6aab73950e89964898d124430f10d3fa2385151b2ae63a`

```dockerfile
```

-	Layers:
	-	`sha256:7611a388f1f328e162bcea56427b783526f4e333548c1c9c60fae459ca59f5b3`  
		Last Modified: Wed, 04 Sep 2024 10:34:47 GMT  
		Size: 646.3 KB (646328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3ba3394217008e98824092249ed4fe234781d31a9f57032a67804f26f7ad858`  
		Last Modified: Wed, 04 Sep 2024 10:34:47 GMT  
		Size: 25.6 KB (25565 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.20` - linux; s390x

```console
$ docker pull python@sha256:678bca1d04ba7dc10f0d74fcfa4c08f5d0875682d508460bf8eb873a74adb6b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19615667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1620c4d0d1937e6de6a8417b0d7142267ffedd6325185e51f658f9cb54dfdf55`
-	Default Command: `["python3"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 23:26:33 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_VERSION=3.12.5
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_PIP_VERSION=24.2
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973ed613b77f93ae6fd0cdac200eeba5114474b4918834bd582533e622019792`  
		Last Modified: Wed, 04 Sep 2024 07:54:49 GMT  
		Size: 462.7 KB (462728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6710069ecc54a326db93e6b58b02ed7358646ff0e32b6a12b68a9e5b8fddc2d4`  
		Last Modified: Wed, 04 Sep 2024 07:54:49 GMT  
		Size: 14.0 MB (14018058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8034834127209f3928717e997a7d9c1d75bc8ef98d83cbc86628108d77909c`  
		Last Modified: Wed, 04 Sep 2024 07:54:49 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba5d21ec41d9a277489678a3892540015d2c5bbafd919ca980a1ddd49719707`  
		Last Modified: Wed, 04 Sep 2024 07:54:49 GMT  
		Size: 1.7 MB (1673586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.20` - unknown; unknown

```console
$ docker pull python@sha256:22a4168abe5f5fe112f74ec6673529809bea2d3453f16dda38436f914984f857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.8 KB (671767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d36002affbd61c7e74b4ade1f4fda558b9f88f0b5e95d716e525db72f02cc5b`

```dockerfile
```

-	Layers:
	-	`sha256:db144963a4e8f23949530dee2ed750dc703e4425557908ccc3ba056d071f404f`  
		Last Modified: Wed, 04 Sep 2024 07:54:49 GMT  
		Size: 646.3 KB (646270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cf099864166d6685dfc1fbc7ab4e65977665cbbcc34dd0982509ae32521ca53`  
		Last Modified: Wed, 04 Sep 2024 07:54:49 GMT  
		Size: 25.5 KB (25497 bytes)  
		MIME: application/vnd.in-toto+json
