## `hylang:python3.10-alpine`

```console
$ docker pull hylang@sha256:957c8d43abe5e1f8f07fae02833ab3d26b8909f78448825d5b514b597af353f0
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

### `hylang:python3.10-alpine` - linux; amd64

```console
$ docker pull hylang@sha256:ffaf993dbab3d53292bdedc3562baeb511689f39d3ebd0800d0f3a13bc8fcd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23514557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537b5cbaebac5da2d32d30306de39c68f584f4c8486529152e22e13403a8e110`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["/bin/sh"]
# Sat, 25 May 2024 09:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 May 2024 09:33:51 GMT
ENV LANG=C.UTF-8
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.10.14
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7706d1ed1c88b3f8a6210f7c1809234dd754b3632581293a38145731311c25`  
		Last Modified: Thu, 27 Jun 2024 00:09:53 GMT  
		Size: 627.9 KB (627925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98a9d0ca2e40597044ed7310853b7e173fd3187ccee1f609e6866653e48a155`  
		Last Modified: Thu, 27 Jun 2024 00:09:53 GMT  
		Size: 12.2 MB (12215718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f949ad24b2e6b0a44ff3dd6e6f83135aff6b5f79a39974140e133ecd554edb6f`  
		Last Modified: Thu, 27 Jun 2024 00:09:53 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ea833230fa9cd5a956692d26082c217015b3cfb9a859e6c75398f48790d643`  
		Last Modified: Thu, 27 Jun 2024 00:09:53 GMT  
		Size: 3.1 MB (3080760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca89e93ad8c660f9fb6eb4e7f33ab57c9a0f2178d4e6145f2b1ea44ffaf514a`  
		Last Modified: Thu, 27 Jun 2024 00:59:50 GMT  
		Size: 4.2 MB (4172594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:a0f655598b84ae9bcf2f5d50d2cc945315c8e52156a0698589726084652764e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1038122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118574376958f9ff99ad3731767d22838ab8aff5dbb4c7f3a03165136827fa56`

```dockerfile
```

-	Layers:
	-	`sha256:51552f8889432e8a8d20e543efb9ec8cafa6760fcde7767c3715e0744e6c4750`  
		Last Modified: Thu, 27 Jun 2024 00:59:50 GMT  
		Size: 1.0 MB (1028302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89fc35173f55a61aa960aa1318aa319919a826aee55317d4a414598f72350734`  
		Last Modified: Thu, 27 Jun 2024 00:59:50 GMT  
		Size: 9.8 KB (9820 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine` - linux; arm variant v6

```console
$ docker pull hylang@sha256:16f7c3997eee034297bfa15462190f9bee0d7615d9ef1e99e9c1b366711cabe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22922547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcb621ad825b6c045922d4d604e2dc92c1e9fd680f6c4bab67086b4f9f4ca98`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["/bin/sh"]
# Sat, 25 May 2024 09:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 May 2024 09:33:51 GMT
ENV LANG=C.UTF-8
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.10.14
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb75463cb2f814fafbefd18a71f21272200c6eee771dacda867ce1677a06f4e2`  
		Last Modified: Thu, 27 Jun 2024 01:18:19 GMT  
		Size: 628.8 KB (628799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27f83f1d1b652061ad11d60b576583346fc01e3ae79c613689349e109d3378a`  
		Last Modified: Thu, 27 Jun 2024 02:16:44 GMT  
		Size: 11.9 MB (11866114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13008885524c3ea23885764db2c6d0c5fa4099060d4d7894b92412967a075724`  
		Last Modified: Thu, 27 Jun 2024 02:16:43 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0fef639489d9897248add8c8c39cc8c2bfe6fb70f827f0aca3715a0786bf94`  
		Last Modified: Thu, 27 Jun 2024 02:16:44 GMT  
		Size: 3.1 MB (3080727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85f7b9dac1effccb0d8d79d5c09f1b2bc8c60983268b0c9c5a2771935cf5afa`  
		Last Modified: Thu, 27 Jun 2024 02:52:24 GMT  
		Size: 4.2 MB (4172770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:43c43e8d653b4fd3e3728f29485f4d22f91baa0fa82a01595709abaac39c9733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 KB (9721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1852780731936602674838b72dc36aecac55679f3b1f5c828f2eb3289b4af4df`

```dockerfile
```

-	Layers:
	-	`sha256:cde3bedb7ced02f610f179313d4349afb7d3a0f2e8caee11b8d95055158b2dab`  
		Last Modified: Thu, 27 Jun 2024 02:52:23 GMT  
		Size: 9.7 KB (9721 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine` - linux; arm variant v7

```console
$ docker pull hylang@sha256:80d5ae1045573bd07f070b84866ca0c5caf53ffd6eced0b286f4107500a2f5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22256285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3eb8dde91fcc01bf576fdf01aea499eaeb7ae22de6dfdc92971587c84a2042`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:a79253a22e927307fa2edd1752e7945fd88afbb97c73bbbe771cc99947c0517a in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["/bin/sh"]
# Sat, 25 May 2024 09:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 May 2024 09:33:51 GMT
ENV LANG=C.UTF-8
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.10.14
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4007367bb0cf596fd27d2207989b3864272eb2e5caf7429c07e68abc3bd47b0c`  
		Last Modified: Thu, 20 Jun 2024 18:01:06 GMT  
		Size: 2.9 MB (2926498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a929d693636b4a1b2ba82565afa7476ad0e7472b92d5385d556fb9479edd5535`  
		Last Modified: Thu, 20 Jun 2024 22:55:06 GMT  
		Size: 627.8 KB (627761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46237e78394c9d25edebfd00d3d2b51fe44837cfa767d7df9642ea871a4544da`  
		Last Modified: Thu, 20 Jun 2024 22:56:00 GMT  
		Size: 11.4 MB (11448177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652f28790af8c31744a98f0d16cfe3bc6ae17410304a68a990ba6271d739ba5f`  
		Last Modified: Thu, 20 Jun 2024 22:55:58 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85aeb39345076e62f122b76e7e711e3ad6cad59645c29c7a79bdd8bb8421bf9`  
		Last Modified: Thu, 20 Jun 2024 22:56:02 GMT  
		Size: 3.1 MB (3080807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdba66c9aa9eede51a15213439d675f514b6dd51ae9e8cd3afeeba74bba056d`  
		Last Modified: Fri, 21 Jun 2024 12:16:23 GMT  
		Size: 4.2 MB (4172799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:5f005dc0c53ba47ee045a1f79bdb883ab19ac5e7c17e88a0bfe292e7662a2ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1040740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e931b8f1edf8a87a755336fb54351edc5411279b70bfc1599963c3f91c5394`

```dockerfile
```

-	Layers:
	-	`sha256:a173dadfb768dd44e48993afd3378cd88c79d3300dea9754884f3224cc0ec838`  
		Last Modified: Fri, 21 Jun 2024 12:16:22 GMT  
		Size: 1.0 MB (1030948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd7a04bddaebf70417854f4796b8fa64c0335f4d4d22b866fa86cd0e118209ba`  
		Last Modified: Fri, 21 Jun 2024 12:16:22 GMT  
		Size: 9.8 KB (9792 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:e2db5eeb4297ac0990decd21d6db9b1e4fead1bf4a36b5c76ce11eb90ea81ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23531272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd70be1c3a745e32a502663427a6cccc74cb73bfac36e10a1db457bc5aaf1d0e`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["/bin/sh"]
# Sat, 25 May 2024 09:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 May 2024 09:33:51 GMT
ENV LANG=C.UTF-8
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.10.14
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261f98b4ecbbc00ba6e9ea779792f6581861d82157a72200e0025c955fd376f0`  
		Last Modified: Thu, 20 Jun 2024 22:33:26 GMT  
		Size: 630.1 KB (630125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f867c9f1a5db0703837e987f901b4c771d40ad64dd18ad9d0253f5fb42cf4cc`  
		Last Modified: Thu, 20 Jun 2024 22:34:23 GMT  
		Size: 12.3 MB (12290316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f843d371de23dcac55138658539b57363f3505cc25d03a55a767212cb5c977`  
		Last Modified: Thu, 20 Jun 2024 22:34:21 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cd7bfb60a8ac518d4345183be6b9f066f7450685172d299f64795582e48784`  
		Last Modified: Thu, 20 Jun 2024 22:34:22 GMT  
		Size: 3.1 MB (3080774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b2652747ae4a0b036e672f20d7bdd4c318873ab9950c3406f1808794290b8c`  
		Last Modified: Fri, 21 Jun 2024 15:31:22 GMT  
		Size: 4.2 MB (4172614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:0637595d65a5b9507c018bfcfb8aaa8bd85546ed393b8d34a5383917db58e3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1038455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781d032a19217107ee3e1d630f40ca9309498bdcc09a6b5287a2454e4c570ed8`

```dockerfile
```

-	Layers:
	-	`sha256:eed41836a7adebb7cdacc6cf2577d2c97a471ccfb2233da5a1ed2e8f41c153fb`  
		Last Modified: Fri, 21 Jun 2024 15:31:21 GMT  
		Size: 1.0 MB (1028406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c247470d6156fdc74e82f3d8b5f3198431cc5b53144f98afc5e0ed131fa69189`  
		Last Modified: Fri, 21 Jun 2024 15:31:21 GMT  
		Size: 10.0 KB (10049 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine` - linux; 386

```console
$ docker pull hylang@sha256:586d1f83e9c3c0836c02f6b2e7a6b6afef636c3aaea5cb045e29ea3d90a1cfb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23573387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a30b800086e9a193c5dfa2651c38a6df793306a179043d44be8c02bd3d033`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:fef5870f3bb90ed437c0331d7e65e52da6728b66d231aea95a605935fef056d7 in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["/bin/sh"]
# Sat, 25 May 2024 09:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 May 2024 09:33:51 GMT
ENV LANG=C.UTF-8
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.10.14
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e9c6bf0d8f3154c26ee87ffe9feb02c91666069b8cbe0668cfae10922ad80c49`  
		Last Modified: Thu, 20 Jun 2024 17:39:06 GMT  
		Size: 3.3 MB (3250890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192a209625e4817ddb4755fca89eb14f88e939bdbf2d1910869aedc74fbbd369`  
		Last Modified: Thu, 27 Jun 2024 00:10:52 GMT  
		Size: 628.4 KB (628428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ec6d668c2ab0ca632ae350856561c77f1bbb61d32b3e82b1b537c79685b1e9`  
		Last Modified: Thu, 27 Jun 2024 00:10:52 GMT  
		Size: 12.4 MB (12440636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e70401e5ac0871415fe5524238cf2835d2f82c499b0d2bd283c7422eadaa2e9`  
		Last Modified: Thu, 27 Jun 2024 00:10:52 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea11ded3e90336f9b7c7fbe24711c96f33167e1993c48f4bb91eb8f9ca1b40e`  
		Last Modified: Thu, 27 Jun 2024 00:10:52 GMT  
		Size: 3.1 MB (3080705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a1b0343f7b02960a316c29073a15e51f2dd0e70b166a0051bdb40505cbbc39`  
		Last Modified: Thu, 27 Jun 2024 00:59:41 GMT  
		Size: 4.2 MB (4172500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:c2b0b6c2524aa0bdea1ad6340cabc61d24bc4c646a6b88fe6d5eb6f830387351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1038025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015ca7b5b9d9eb72d2080d36e2dedd311d807b2db784d4ade0614b1244b6c8c4`

```dockerfile
```

-	Layers:
	-	`sha256:6c28fbfdec13870eb6f04e888c2bdba5f3a5d55e7743e800448b8f91ee8f57db`  
		Last Modified: Thu, 27 Jun 2024 00:59:40 GMT  
		Size: 1.0 MB (1028257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cfdc99b5eb0b2e8257973539468d86172b6d2fab25871d4137a537e49b6c052`  
		Last Modified: Thu, 27 Jun 2024 00:59:40 GMT  
		Size: 9.8 KB (9768 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine` - linux; ppc64le

```console
$ docker pull hylang@sha256:48ef3d8772b98c41322014e169887262daa5b7ed82f53b0c70a3fc0aacd05550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23966688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a6db628e5c571c0c7d09b5a97f93f371d27f8bb87578854b9b40613e1635ed`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["/bin/sh"]
# Sat, 25 May 2024 09:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 May 2024 09:33:51 GMT
ENV LANG=C.UTF-8
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.10.14
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a87ce480a1e6b2a211e539793eb8993daec4a7b45a3b284a63476a172be632c2`  
		Last Modified: Thu, 20 Jun 2024 18:19:08 GMT  
		Size: 3.4 MB (3360635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f5cedf692e9918ff60fa01f223ad0b5496678de46222513cdb0d0c24288c60`  
		Last Modified: Thu, 20 Jun 2024 23:19:57 GMT  
		Size: 630.6 KB (630572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c604c77d70e356b6f17d6a1a4154a1f8a16612837d3db63674d2a44c41a63d`  
		Last Modified: Thu, 20 Jun 2024 23:20:52 GMT  
		Size: 12.7 MB (12721858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa311e6ba2952b3e3660123ccc5a0c3b22349104f5b9c2aca51270b60ca61a8`  
		Last Modified: Thu, 20 Jun 2024 23:20:50 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66db0462029c94657a309106ed890bc3e86741948720036e4a8ae82d5800c254`  
		Last Modified: Thu, 20 Jun 2024 23:20:51 GMT  
		Size: 3.1 MB (3080810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb836570aff7e76a3b9ddab93bc2f291542ecd10d6a2f02cba71f81d057331be`  
		Last Modified: Fri, 21 Jun 2024 06:03:04 GMT  
		Size: 4.2 MB (4172570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:91e9c2765190456ece7786018c78d07fc43f9b0e88845ec792036454be403b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1036158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22bed888d0a9f7947306d26bf3403a3d20ea65e69fdbcc4b43ad27d3b1180578`

```dockerfile
```

-	Layers:
	-	`sha256:a86290f9f37be30b912314e174cc62988f9af8eb575e983820ae5a535de973bb`  
		Last Modified: Fri, 21 Jun 2024 06:03:03 GMT  
		Size: 1.0 MB (1026406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a55e2b192b976e207e3e35c76904dd28b0a1b84d467bd9139ea706d931b1b8e7`  
		Last Modified: Fri, 21 Jun 2024 06:03:03 GMT  
		Size: 9.8 KB (9752 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine` - linux; s390x

```console
$ docker pull hylang@sha256:10214a1c8256c6f620dc7d63860cb4158b5224892ad32120cc07d463c2f41706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25563276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b093d6592fc79e17484880b7414e7ef6f26ce7073204faaed57fcddc7600a50d`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 25 May 2024 09:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 May 2024 09:33:51 GMT
ENV LANG=C.UTF-8
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.10.14
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9169c179722862a77ad681551b5243bc093a2f27f3446dc08f68809bcc6c2f0b`  
		Last Modified: Fri, 07 Jun 2024 22:32:07 GMT  
		Size: 628.8 KB (628808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7a13f9f5bef3bb0a543333162cbab76538f4dde0dc330761a4cc55723de459`  
		Last Modified: Fri, 14 Jun 2024 19:29:52 GMT  
		Size: 14.4 MB (14438253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b473a672ab11388a2b59d4d897f964c046c1d2f2a6e39dc4982a76fad8a23df8`  
		Last Modified: Fri, 14 Jun 2024 19:29:50 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870e793acf1dfd12905077e4338e2b1e4ace92b787b85728f6657c01c5d3c17`  
		Last Modified: Fri, 14 Jun 2024 19:29:51 GMT  
		Size: 3.1 MB (3080748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd972d6a99a60e34eb3d6682cf53af341b282f660306c15a1f553db44b357d66`  
		Last Modified: Fri, 14 Jun 2024 20:06:53 GMT  
		Size: 4.2 MB (4172590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:71267654ea1ad44fda857fe5439ee8f57545e3935f53cbd42a0d54ef0b460a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1036978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8fed8cd33319029ec1290747103a86b5ec475094085d3835b2de088fcc3508`

```dockerfile
```

-	Layers:
	-	`sha256:36810f8dfb9be65ecaaf6dd9df79e24fed36c7d5c203b2afb1131e28ac7d77ce`  
		Last Modified: Fri, 14 Jun 2024 20:06:53 GMT  
		Size: 1.0 MB (1027288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c5c5fe4f8df76e53edbf3fd048b8f1653c879eaf9f618f4da12cba6ed61c8ac`  
		Last Modified: Fri, 14 Jun 2024 20:06:53 GMT  
		Size: 9.7 KB (9690 bytes)  
		MIME: application/vnd.in-toto+json
