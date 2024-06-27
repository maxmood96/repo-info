## `hylang:0-python3.8-alpine3.20`

```console
$ docker pull hylang@sha256:3058d0b1a775b253d0c21e09acaf26995c32732b5cac31ec3506c4fd2e18db07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `hylang:0-python3.8-alpine3.20` - linux; amd64

```console
$ docker pull hylang@sha256:51f931039d994b6a02e1a9fa71c09ccf29773fa29153fd358af38a7399d39ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22055781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff8b1b763d5e3c89f75a8108c7a2b9d920aab75e3f5649e95ec5ff9b393e45c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 May 2024 12:26:30 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Wed, 22 May 2024 12:26:30 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:26:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:26:30 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_VERSION=3.8.19
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075914deb6673cbed6679691ebcc1eb74f3c65168291eff96a63c2dac7f9e96e`  
		Last Modified: Thu, 27 Jun 2024 00:12:44 GMT  
		Size: 463.2 KB (463221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5c0813429c30ca91b7b9b9ad6284b42cf4f732b5f9e3a33bcff7c73d2486bd`  
		Last Modified: Thu, 27 Jun 2024 00:12:44 GMT  
		Size: 11.4 MB (11360982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc46ea10a9d9bff6d2f189a03ffbc51f06e60695eb69b3ad03856744b4706e56`  
		Last Modified: Thu, 27 Jun 2024 00:12:43 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d36688b7a1d6e9660c4ee106f90b55837e6f7520d2bd9c1de403429546030ba`  
		Last Modified: Thu, 27 Jun 2024 00:12:44 GMT  
		Size: 2.9 MB (2851807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a0dd7a09c22e4e9f14e9c29a48936be1ed9d1bbfed8f28357fd44ad513f721`  
		Last Modified: Thu, 27 Jun 2024 00:59:56 GMT  
		Size: 3.8 MB (3755697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:a2888a2029f0e702c54493af5aa2c0b9a0715d208a739f8f94d9e52dcb672125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.0 KB (659965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36cdee5cb6c95fb10f67b46c0ae2b90595cc1537a64c8d2ca37c0ddc250d041`

```dockerfile
```

-	Layers:
	-	`sha256:fa087512edfcb1f7846f81eb3d702de9c8af257817c1d4861e1388cb769e5f06`  
		Last Modified: Thu, 27 Jun 2024 00:59:56 GMT  
		Size: 651.5 KB (651465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1a8a9de1d01b3505ac7ff3252601bdb79efabd2dbbced98629904f62fa25c31`  
		Last Modified: Thu, 27 Jun 2024 00:59:56 GMT  
		Size: 8.5 KB (8500 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.8-alpine3.20` - linux; arm variant v6

```console
$ docker pull hylang@sha256:b54572a9f108b9e6975940a248e4e20ac1daff9f12a11a947d840ba6b46f7e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 MB (21473899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cf74956809937efbc0932816c7375e88a3281d5a42e46d02728966fa417f13`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 May 2024 12:26:30 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Wed, 22 May 2024 12:26:30 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:26:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:26:30 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_VERSION=3.8.19
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
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
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1690c05b67bd96f09afbaf8ed50bd1d5ce45e8ce028ec45d793a1932e33c9f9d`  
		Last Modified: Thu, 27 Jun 2024 00:58:57 GMT  
		Size: 463.9 KB (463884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b7628e954398fc8401a33195ffe0439a794eef86a728d8b5f3789606ad3c5b`  
		Last Modified: Thu, 27 Jun 2024 02:26:34 GMT  
		Size: 11.0 MB (11034668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627234b61cc2bd4c3f5ce80c9b816603a195b54d09a81006e8bf61cc58cecf90`  
		Last Modified: Thu, 27 Jun 2024 02:26:33 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc50285b25d8d17b9c0ca6072c8c293d66e7710d7137947e3449f64787d70a`  
		Last Modified: Thu, 27 Jun 2024 02:26:34 GMT  
		Size: 2.9 MB (2851835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bc7dffa3337eb5da13c85800f3db7a6aec020a054469a1ce4bcf218cf2e71b`  
		Last Modified: Thu, 27 Jun 2024 02:54:00 GMT  
		Size: 3.8 MB (3756129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:7f59b2d6c01828b5959876f105b5210ed05f1edeeaa97f2c42e5667f33078ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 KB (8367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be914d19a59cd57679e13e3ea304a3b67f1e2c9644b0ec320bd9d1a686e6b57`

```dockerfile
```

-	Layers:
	-	`sha256:b98cb66b37272443b1d97077a7a9a3ec84b600a6efc8dc666f38e4f07040bde5`  
		Last Modified: Thu, 27 Jun 2024 02:53:54 GMT  
		Size: 8.4 KB (8367 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.8-alpine3.20` - linux; arm variant v7

```console
$ docker pull hylang@sha256:43ec7ea3af3a71b5fbb8957b4181eb1f5de55efb8a837f5821e23d712fb84550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20812985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc13ad4892e27e0dbf91c1fe1014d8e448806a29b155711320cb595ba0522d3`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:26:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:26:30 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_VERSION=3.8.19
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
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
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c708927d89b7745e9f553175dbb9d585894c9c0f2cd91946e4c0e12199a4f89f`  
		Last Modified: Thu, 20 Jun 2024 22:54:46 GMT  
		Size: 463.1 KB (463099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd6e1190b8c0488d854fdeb08eed46161e7ba3f254f05aa52ec878ec8576632`  
		Last Modified: Thu, 20 Jun 2024 22:56:40 GMT  
		Size: 10.6 MB (10646939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717958af5400b009c999d045e20b0f1eb2e82e3820abe78ac6328fc14fadccc2`  
		Last Modified: Thu, 20 Jun 2024 22:56:38 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542750b80f61dccd88eab3ef54a0462c8c06e87ca9308a37c4b2ab50ad781a75`  
		Last Modified: Thu, 20 Jun 2024 22:56:39 GMT  
		Size: 2.9 MB (2851850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da33f4497712cf6cd80507b3a6d42399081729c2a79b8bf84a9d1ed51466e72`  
		Last Modified: Fri, 21 Jun 2024 12:18:13 GMT  
		Size: 3.8 MB (3755999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:6a1ab646b4813c5db4630cdf776fc871b131371be5455f0e9ceb16ae0b024178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.5 KB (662516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca02c0f1b0b8131044af04fbf65a0e62c3dd3c34068377ceff8bb0eef459187`

```dockerfile
```

-	Layers:
	-	`sha256:e8caab4c92bb4ce61b5b9f232b3078a3f22130d480cd934769a8ea4ee82c08d7`  
		Last Modified: Fri, 21 Jun 2024 12:18:13 GMT  
		Size: 654.1 KB (654079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:046ebb3d4b65805c53f0c15bd6a08df109ead5792297d0c52d379b5374d4b391`  
		Last Modified: Fri, 21 Jun 2024 12:18:13 GMT  
		Size: 8.4 KB (8437 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.8-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:1224358784095aff81eadcef5b5b08f98331c9658a712b15b1b012e9b7b33359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22621684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0f2e93939a85e0d9717a77498c5c9cd323c3cfb35a00d0741c3ee70a062bc2`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:26:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:26:30 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_VERSION=3.8.19
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e0a54ce1bdfb371b942c96830ed8a81f953669f02f93cbf826a148112789ee`  
		Last Modified: Thu, 20 Jun 2024 22:33:07 GMT  
		Size: 465.5 KB (465483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b61dbae143968274f2b6a8c6f453c6e813cc166d66fb3ecfb251e7482d29b4`  
		Last Modified: Thu, 20 Jun 2024 22:35:01 GMT  
		Size: 11.5 MB (11459235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cad5d74d26a650d8a3d678ed8ec4d0f8387050a8798f3f07bf65636003cafb`  
		Last Modified: Thu, 20 Jun 2024 22:35:00 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb85500127eab5f765b7e6a55790deff38e98edd293d2dce87c3afc94f7459ce`  
		Last Modified: Thu, 20 Jun 2024 22:35:00 GMT  
		Size: 2.9 MB (2851870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a321e29a0c032fb16d9a4b596944d5d7d7c084cfadec4b48af14e680fffd788e`  
		Last Modified: Fri, 21 Jun 2024 15:33:27 GMT  
		Size: 3.8 MB (3756053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:7aa25940c1819b1631a6fdd538355f43dc86bd537a6a98cc4604d8fc1520eb31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.2 KB (660198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c2ec9cf6b9912e6f15e8406d32a3ea734cea916d67310f27039a5ff0728232`

```dockerfile
```

-	Layers:
	-	`sha256:6a002e1de11c51f4099b96b4d2cb46682c45c9baedc96448c63cdce5e2608e2d`  
		Last Modified: Fri, 21 Jun 2024 15:33:27 GMT  
		Size: 651.5 KB (651521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d8ebae1d2a2dffe115b962cd5e0ce10e845116c1e83d5caa3b35357b5a607b`  
		Last Modified: Fri, 21 Jun 2024 15:33:27 GMT  
		Size: 8.7 KB (8677 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.8-alpine3.20` - linux; 386

```console
$ docker pull hylang@sha256:2cb6a3d1004dcd274ecd1f4655fc3878fbc3529daca49902b819426f2ccc6efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22135348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e109a08ab962ac475b5df5db770329fa04d35ec3936169b1945a0b4f211330`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 May 2024 12:26:30 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Wed, 22 May 2024 12:26:30 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:26:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:26:30 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_VERSION=3.8.19
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
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
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e600b48577056ebf1bf8110a8500d68b5045218fd4fc1bf8c66bcbbfc2d7cd6`  
		Last Modified: Thu, 27 Jun 2024 00:13:43 GMT  
		Size: 463.6 KB (463621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3bfe28c1b8b56834278101d9f5d1389ce4813a3ed91650d2a21d0ad0f6465e`  
		Last Modified: Thu, 27 Jun 2024 00:13:44 GMT  
		Size: 11.6 MB (11594289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacc7595f6a0ee78cdec7cb0194ff123da7f3b4cf75caa4c7e64483c307c1648`  
		Last Modified: Thu, 27 Jun 2024 00:13:43 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0d32d33965522ecf9446ffa9f25a2204d8521ee9758644e81c5d3ef5f48757`  
		Last Modified: Thu, 27 Jun 2024 00:13:43 GMT  
		Size: 2.9 MB (2851828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a893c027439733ebdab163566997ae6c0ae1f1aff4f22abdd112c0ff8bf416ee`  
		Last Modified: Thu, 27 Jun 2024 01:00:54 GMT  
		Size: 3.8 MB (3755911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:662dba732431cde92d7a9ae3efed016981a739b65cf8ed3582230db459ac33a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.9 KB (659908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699dafd0a7f6fd628f7b88e68fc23ee2c76d36d91d120de4477426bd1f063386`

```dockerfile
```

-	Layers:
	-	`sha256:d975a5cb314fd72e184e9a6a333fad2e992021ed9a6679a3333bdd00bfc34a6f`  
		Last Modified: Thu, 27 Jun 2024 01:00:54 GMT  
		Size: 651.4 KB (651440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37eebca16d1f89e07f0ae0eaa3a582bdce5f52e0220e9203b792c525cfa55482`  
		Last Modified: Thu, 27 Jun 2024 01:00:53 GMT  
		Size: 8.5 KB (8468 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.8-alpine3.20` - linux; ppc64le

```console
$ docker pull hylang@sha256:bb280a8057158c88cb04cb9d2568ef88a5362a91c04ccfb570805b26ee6b77f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22488826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d006257b60ff91f1a58dcc9d46597b70da75c6158e21a0621df13be3bb284fa6`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:26:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:26:30 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_VERSION=3.8.19
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
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
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd453c8be5405b60b60e6f4ed670d0b55e922008cf221fce0ac80e3689940f`  
		Last Modified: Thu, 20 Jun 2024 23:19:38 GMT  
		Size: 465.8 KB (465849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12bf8631e91e7c3a22acf076b7e04022cab7e1303104880b6f02b28e8af7430`  
		Last Modified: Thu, 20 Jun 2024 23:21:29 GMT  
		Size: 11.8 MB (11843204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf08a593dab947f628ec06c242824b55b8919124fa6034f0ea99812437bc7608`  
		Last Modified: Thu, 20 Jun 2024 23:21:27 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae375e8ed82d4259e9acb1c5a35f7b3328a9bafc0dc56fce866f31659dee95dd`  
		Last Modified: Thu, 20 Jun 2024 23:21:28 GMT  
		Size: 2.9 MB (2851869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa49da292e2b9227f43f4aecfc9bd0bcea0ab49d563419776b410b0e940b2fb4`  
		Last Modified: Fri, 21 Jun 2024 06:05:38 GMT  
		Size: 3.8 MB (3755962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:d85689c35b19f82c3fe5b66f9d3b0e3338afbe3e5765967755e17c8a57812d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.0 KB (657950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ddb294d42e72fae8572d06e1f607af51cfefe4a40bef2b9899ef0b58cac60d1`

```dockerfile
```

-	Layers:
	-	`sha256:146a91d0c7c99409beb700055ea8f23142f2eff710a948b6d3e68ea0a9103dde`  
		Last Modified: Fri, 21 Jun 2024 06:05:37 GMT  
		Size: 649.5 KB (649545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffae0aed2e0cb807099f29dd0daf21d14171ffed42de283b07fe62af1a60facc`  
		Last Modified: Fri, 21 Jun 2024 06:05:36 GMT  
		Size: 8.4 KB (8405 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.8-alpine3.20` - linux; riscv64

```console
$ docker pull hylang@sha256:1fe8a6b9cfbd808517823e95afe07d5c67a5dfe1555e84d499332165632332a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21785228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0140448ed677653621e92954f6cc4b2218f1ff4aad74fb1e84de6afe7c98b1`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:26:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:26:30 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_VERSION=3.8.19
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
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
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0657d7ddfcd1bf5fa61b078b84800526e4806ad59081e611ded32e218cc39fdc`  
		Last Modified: Sun, 26 May 2024 05:38:38 GMT  
		Size: 463.8 KB (463841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22fa1fc6d8475ec58250fa16214c43740665663ffb292e661f50b8fb48b835a`  
		Last Modified: Sun, 26 May 2024 05:39:13 GMT  
		Size: 11.3 MB (11343536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbfa5e91b612f400c0d2afc33c33f7fbed845dd2b56a2e15696c7085fbce660`  
		Last Modified: Sun, 26 May 2024 05:39:04 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047e82234d6fb147638765d9677a5c257ea7af9c835b291fedebbf35eaf79773`  
		Last Modified: Sun, 26 May 2024 05:39:07 GMT  
		Size: 2.9 MB (2851925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7d9cc2c26069c8eb9633590e030e73236c802a7e48f2966f729e6ed8a05b3b`  
		Last Modified: Thu, 30 May 2024 21:03:34 GMT  
		Size: 3.8 MB (3757123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:1a9b29a0dc65d9e231e0b1ebb8b7371d5576bbb1ca061ce9cb12deb634ed430d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.8 KB (654771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc5619fa6e028a2498e3ad5a79e984c904ab8242f8a1389ef814eab293d559d`

```dockerfile
```

-	Layers:
	-	`sha256:fbd01638744b1dbb7fc36ee67fa8c193be16c8a8f4a49b459659939d697d9a79`  
		Last Modified: Thu, 30 May 2024 21:03:33 GMT  
		Size: 646.4 KB (646415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70320898c0cb87e8be587e6a9a0ea5fe076015bf152fdb3862b7e40c8e4a968`  
		Last Modified: Thu, 30 May 2024 21:03:33 GMT  
		Size: 8.4 KB (8356 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.8-alpine3.20` - linux; s390x

```console
$ docker pull hylang@sha256:4baa45372e105d08c1a652cc3917d9d3935105719fd5df6c2b567da4d13f8ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.2 MB (22178965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8446f85aa698a9312e81e450f5ef024e4355ec53ce50b022ddde867ecf68ab`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:26:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:26:30 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_VERSION=3.8.19
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
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
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54731744988f9706a5f3a112bf8ec682a61504506e23cc6c16a1b475a945b5b0`  
		Last Modified: Thu, 23 May 2024 00:50:28 GMT  
		Size: 464.2 KB (464183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd5cc2193a5009c348177734663b860e2271349c9fd0734ee445179da80b3fe`  
		Last Modified: Thu, 23 May 2024 00:51:45 GMT  
		Size: 11.6 MB (11646194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb6932b98467e9f34feb8a957e1e32f5b16e299c78fdc5b4ea07e77f31d01ee`  
		Last Modified: Thu, 23 May 2024 00:51:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67df318bbeb1708c595017f25298b26c37ddca27a61f55e8ea925a9ae4cd7d32`  
		Last Modified: Thu, 23 May 2024 00:51:44 GMT  
		Size: 2.9 MB (2852077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd7c3a45a1a80b643476b13d40ec8cfa19177619a1394bd2203adb676a92c37`  
		Last Modified: Thu, 30 May 2024 00:58:55 GMT  
		Size: 3.8 MB (3755931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:f20574ec6e06ec233bc37983343e73d4d31f1c292c2efe9304e69737385054a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.7 KB (654703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68f3dc0b5c72ecd309ddc5080640730089ad90a89383358f8499036ddcd5fc1`

```dockerfile
```

-	Layers:
	-	`sha256:d7d7d205b4289b46a5cfbf3dab2b3eea3bb8f8c66b8486ccd3bdf9240eafab37`  
		Last Modified: Thu, 30 May 2024 00:58:54 GMT  
		Size: 646.4 KB (646385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3522666ba4d56c16952acd0106df49279d963e94d0e1e5da9893735ae013fb76`  
		Last Modified: Thu, 30 May 2024 00:58:54 GMT  
		Size: 8.3 KB (8318 bytes)  
		MIME: application/vnd.in-toto+json
