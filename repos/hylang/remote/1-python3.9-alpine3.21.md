## `hylang:1-python3.9-alpine3.21`

```console
$ docker pull hylang@sha256:dd95f484e1a8e4e58469ce77dca9efafff56e233f3a50bdee35fff5567da4c76
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

### `hylang:1-python3.9-alpine3.21` - linux; amd64

```console
$ docker pull hylang@sha256:43fb8a9a44e76e37e629cdda355d0c23acf49a80336e59c385ed0326eeb04b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23209754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2611bc769e910b4c4cd654968420fb752f45f333c2db0e73345d6be184c9923f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 23:16:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 23:16:43 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 23:16:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 31 Oct 2025 23:16:43 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 31 Oct 2025 23:16:43 GMT
ENV PYTHON_VERSION=3.9.25
# Fri, 31 Oct 2025 23:16:43 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Fri, 31 Oct 2025 23:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 31 Oct 2025 23:17:54 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 31 Oct 2025 23:17:54 GMT
CMD ["python3"]
# Fri, 31 Oct 2025 23:57:45 GMT
ENV HY_VERSION=1.1.0
# Fri, 31 Oct 2025 23:57:45 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 31 Oct 2025 23:57:45 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 31 Oct 2025 23:57:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9947ceb03627a87c94b1740bae38ca87f0e47e177fd4c8e34317b3d91bea71f9`  
		Last Modified: Fri, 31 Oct 2025 23:18:06 GMT  
		Size: 456.9 KB (456889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67844e24a9fff0bb15b0d9689c6f59e8fb8d7d954c4bb3c3c9bca9b92047bcad`  
		Last Modified: Fri, 31 Oct 2025 23:18:08 GMT  
		Size: 15.4 MB (15386556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610fe38fb40f9e714a28504a11bf6d7be84edaa3c2db14f6b44e3b6e5ae4afde`  
		Last Modified: Fri, 31 Oct 2025 23:18:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb6e52153095b95429990d23a019706d6002c69e6c5776f7bc95018a7b45dc2`  
		Last Modified: Fri, 31 Oct 2025 23:57:56 GMT  
		Size: 3.7 MB (3723493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:c88c2f20687294fe2a166b6780ce5f9d437c4f0b32cd9b130e95b76057cb3338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.2 KB (705160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc81c2968ac3c6cce463bfc3cea04be8b1ea8ae138200d917642404c237dae0f`

```dockerfile
```

-	Layers:
	-	`sha256:822681d343b6576b9c1b3773ea131564c18db473d0974f2a26da18f365e69857`  
		Last Modified: Sat, 01 Nov 2025 02:19:29 GMT  
		Size: 697.1 KB (697070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb282b4fcaac853d529712fb235769ceda0c51752b8dc835c29848330dfc2175`  
		Last Modified: Sat, 01 Nov 2025 02:19:30 GMT  
		Size: 8.1 KB (8090 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-alpine3.21` - linux; arm variant v6

```console
$ docker pull hylang@sha256:fda3a10c538c90c5bc578c9845646102027872e2053ca56efe17c8195712f593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22487150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a957ed1a71db6f4ca068d5f64d827d575fbe922af82f0d61990ecfb0a507f51f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 23:13:48 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 23:13:48 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 23:13:48 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 31 Oct 2025 23:13:48 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 31 Oct 2025 23:13:48 GMT
ENV PYTHON_VERSION=3.9.25
# Fri, 31 Oct 2025 23:13:48 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Fri, 31 Oct 2025 23:15:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 31 Oct 2025 23:15:21 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 31 Oct 2025 23:15:21 GMT
CMD ["python3"]
# Fri, 31 Oct 2025 23:56:54 GMT
ENV HY_VERSION=1.1.0
# Fri, 31 Oct 2025 23:56:54 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 31 Oct 2025 23:56:54 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 31 Oct 2025 23:56:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c680dd4ce2708d9f034a1d5b554626a04e1177a20edf6e949b1908582919372`  
		Last Modified: Fri, 31 Oct 2025 23:15:33 GMT  
		Size: 457.7 KB (457695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4532c98f179efef9f942ee356ea9b2fcc0ec4cbdb83442731952d5b517b7a87d`  
		Last Modified: Fri, 31 Oct 2025 23:15:34 GMT  
		Size: 14.9 MB (14940098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c429a08ea9efe701b08545ae74573221011253ee69bf2d90b882a40c275d74c5`  
		Last Modified: Fri, 31 Oct 2025 23:15:33 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e213121c4648d29bb3c84a9afb2c7955715cc6851722c85d9a63240afc6636`  
		Last Modified: Fri, 31 Oct 2025 23:57:04 GMT  
		Size: 3.7 MB (3723637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:3caf8e12de3a6dd81b66305dd58c88a1be6caa772ef9af662b2a3ce580f52f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 KB (7956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c8237cde7a94f8488f8398855f16e4a5c9b9c76c7492605f4ec96efbb851d4`

```dockerfile
```

-	Layers:
	-	`sha256:555a8f1c58176f6006214ed7c95242fb1451c9c73262929f9125532ba7816084`  
		Last Modified: Sat, 01 Nov 2025 02:19:34 GMT  
		Size: 8.0 KB (7956 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-alpine3.21` - linux; arm variant v7

```console
$ docker pull hylang@sha256:82440e1f7834ce9b0878965bf8bf9b5661920c82014d4bf97136b2e37097e659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21829123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0436b324479d6882bbb795e4c6b22ae96ddfed12cff9c3ba474c3bb71de1de52`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 23:16:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 23:16:31 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 23:16:31 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 31 Oct 2025 23:16:31 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 31 Oct 2025 23:16:31 GMT
ENV PYTHON_VERSION=3.9.25
# Fri, 31 Oct 2025 23:16:31 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Fri, 31 Oct 2025 23:18:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 31 Oct 2025 23:18:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 31 Oct 2025 23:18:07 GMT
CMD ["python3"]
# Fri, 31 Oct 2025 23:57:00 GMT
ENV HY_VERSION=1.1.0
# Fri, 31 Oct 2025 23:57:00 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 31 Oct 2025 23:57:00 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 31 Oct 2025 23:57:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed06d6fd87405dda97798480e32912f5abf9b95bde2f460fc691500248968f4`  
		Last Modified: Fri, 31 Oct 2025 23:18:22 GMT  
		Size: 456.9 KB (456888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a224bbd623e0678e757eda6298d006810c02c9770c751049f1538550e8a3901`  
		Last Modified: Fri, 31 Oct 2025 23:18:24 GMT  
		Size: 14.5 MB (14549744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06f816ffce5177c6c8ef96393b8f8071a66dbdadbdc4224b93fb33c4f7544b7`  
		Last Modified: Fri, 31 Oct 2025 23:18:22 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2e51049ec9112003953390a96afd960e0a2f2c792187644e26c9e0f52a005`  
		Last Modified: Fri, 31 Oct 2025 23:57:11 GMT  
		Size: 3.7 MB (3723631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:8dc2a377cfb4c0b6ce68283388c697e3efdcc0e795c3d921a67fa126da3d068d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.3 KB (708267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5449e986427d4268f3ebc10942d5575ab486f781a949fece9a78a17e9d058e4f`

```dockerfile
```

-	Layers:
	-	`sha256:a7d2810a38b2c57880d3b234c5263ed88c979eb1fca64ff1a2ad76f905fb1927`  
		Last Modified: Sat, 01 Nov 2025 02:19:36 GMT  
		Size: 700.1 KB (700096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a862df3e5894366d7dc62bf0348e0e46e02199f902e83091a72a347cc6e0cd63`  
		Last Modified: Sat, 01 Nov 2025 02:19:37 GMT  
		Size: 8.2 KB (8171 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:7b6c829772ea70100eb6715695696b38979f1fe14adc4e43edbc8e174d63ea59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23630313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f6f3253975d3c52ef287f70e508d215e20928d2d7ad3f3d8bee552bf14598e`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 23:16:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 23:16:39 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 23:16:39 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 31 Oct 2025 23:16:39 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 31 Oct 2025 23:16:39 GMT
ENV PYTHON_VERSION=3.9.25
# Fri, 31 Oct 2025 23:16:39 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Fri, 31 Oct 2025 23:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 31 Oct 2025 23:18:00 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 31 Oct 2025 23:18:00 GMT
CMD ["python3"]
# Fri, 31 Oct 2025 23:55:21 GMT
ENV HY_VERSION=1.1.0
# Fri, 31 Oct 2025 23:55:21 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 31 Oct 2025 23:55:21 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 31 Oct 2025 23:55:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4334047df782d336eb851022260cfda089bbd5191a4faf376edfc3ae6304fc`  
		Last Modified: Fri, 31 Oct 2025 23:18:22 GMT  
		Size: 459.0 KB (458999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca35cae2873f6ce18867f4ed12280de428242d61429e00e1a69939f5eb6d940`  
		Last Modified: Fri, 31 Oct 2025 23:18:23 GMT  
		Size: 15.5 MB (15455006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc164f6e96949997f2132646f4ff512b9df7f088eb3c827195b2654b2cbd854f`  
		Last Modified: Fri, 31 Oct 2025 23:18:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e00b719aff93b1af9ef655bb429aa17dd96a9d7ddd2c6152995596d1dc0b43`  
		Last Modified: Fri, 31 Oct 2025 23:55:33 GMT  
		Size: 3.7 MB (3723707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:84806f5da0ee7be96e731232e38c747ceac9b278ce4cbfd192dc86e4de03f5a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.3 KB (705321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b88b6e7b5dd9bc3b4538b7b77f9eeede35a57b6017fce03e77f59d159aced0`

```dockerfile
```

-	Layers:
	-	`sha256:6ce4f8bc4bbb1aa84a379449de4cdf56f83776af215609d5f8fa78d98e1e7d1e`  
		Last Modified: Sat, 01 Nov 2025 02:19:41 GMT  
		Size: 697.1 KB (697126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f16dc66c675da81ac4707c6ef66754ec66b699a7f57f359ef94d49d8b8d212b5`  
		Last Modified: Sat, 01 Nov 2025 02:19:41 GMT  
		Size: 8.2 KB (8195 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-alpine3.21` - linux; 386

```console
$ docker pull hylang@sha256:aed49a24496bfc15b8a69f296df6dd92bdd257525e37d67b428dc189b6899826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23260762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df77f50dda2e1c5d67096d66c2f9ca8c2d270a595e04e5d7e8da2d1a0dbb76e1`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 23:15:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 23:15:21 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 23:15:21 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 31 Oct 2025 23:15:21 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 31 Oct 2025 23:15:21 GMT
ENV PYTHON_VERSION=3.9.25
# Fri, 31 Oct 2025 23:15:21 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Fri, 31 Oct 2025 23:16:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 31 Oct 2025 23:16:49 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 31 Oct 2025 23:16:49 GMT
CMD ["python3"]
# Fri, 31 Oct 2025 23:57:16 GMT
ENV HY_VERSION=1.1.0
# Fri, 31 Oct 2025 23:57:16 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 31 Oct 2025 23:57:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 31 Oct 2025 23:57:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8323aa7f0701c31da6dc71787b0d9ef58afafe05f229e7b2db66babbad4c11d`  
		Last Modified: Fri, 31 Oct 2025 23:17:01 GMT  
		Size: 457.4 KB (457353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279e1d6685c11b1a023c7b67b49e3b2b3e166eb22cd6bbbc2edf106e7227a589`  
		Last Modified: Fri, 31 Oct 2025 23:17:02 GMT  
		Size: 15.6 MB (15614879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a832bb9fe20a201bc53ad34b4596f1cdffd31fa29d5b57e6594176ccfc3f334`  
		Last Modified: Fri, 31 Oct 2025 23:17:02 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6f2e06a069a4fe824434de002f92494aaabb44414ee0fff500dc04610a65aa`  
		Last Modified: Fri, 31 Oct 2025 23:57:27 GMT  
		Size: 3.7 MB (3723580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:48038d87e9650a9650aa719ecefeaf0733b58ddfc7b19b2d8195f4300014a663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.1 KB (705104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c168cd9c6b211158f9b53df039d53d513af6a13c9cdbde1e82997eea0efdb6`

```dockerfile
```

-	Layers:
	-	`sha256:66812c17baa796225697657daf03af34697fc58544aab4dd5897084e671619b1`  
		Last Modified: Sat, 01 Nov 2025 02:19:45 GMT  
		Size: 697.0 KB (697045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be7168578116b9bce0257998ec5863b3204af2ac08fa2be8c1e0881adf111d09`  
		Last Modified: Sat, 01 Nov 2025 02:19:45 GMT  
		Size: 8.1 KB (8059 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-alpine3.21` - linux; ppc64le

```console
$ docker pull hylang@sha256:7a5cbb27aa57b3d013d1c6a20bbbbad11958050b8bc2c82b68b1b57e93b39350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23843481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d867c69656ea5a64c53b9f0e1e2d062f743a7cc568546b29a6be84e4d72cda`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 08:28:32 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 08:28:32 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 08:28:32 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 09 Oct 2025 08:28:32 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 09 Oct 2025 08:28:32 GMT
ENV PYTHON_VERSION=3.9.25
# Thu, 09 Oct 2025 08:28:32 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Fri, 31 Oct 2025 23:50:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 31 Oct 2025 23:50:45 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 31 Oct 2025 23:50:45 GMT
CMD ["python3"]
# Fri, 31 Oct 2025 23:58:37 GMT
ENV HY_VERSION=1.1.0
# Fri, 31 Oct 2025 23:58:37 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 31 Oct 2025 23:58:37 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 31 Oct 2025 23:58:37 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0026c7dc43c0a7255a1ad9f4da34ccbef2597f65b422a86bda4c70ee1f6cbd4`  
		Last Modified: Thu, 09 Oct 2025 08:37:20 GMT  
		Size: 459.4 KB (459409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a4ba739fe238d7f6c96fa6072177ea89f4c0071a9a23b43f5eb8a40f1bd941`  
		Last Modified: Fri, 31 Oct 2025 23:51:09 GMT  
		Size: 16.1 MB (16085931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334551f2f190f2ea36909eada6ee922b04d30b3583e710b5f401dda8517452bc`  
		Last Modified: Fri, 31 Oct 2025 23:51:08 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15e80f3495061f37e6b577b32c43be4bd6570aaec833793d7ec4626b90d04e4`  
		Last Modified: Fri, 31 Oct 2025 23:58:57 GMT  
		Size: 3.7 MB (3723819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:270e5ee2a53ef8844017854cbb83f895570b75462d03cf2e0eaf13c66fcaf7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.3 KB (703288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f88bcb643ddebcd9633403ec05d22635dad3504db74f6f6d992ed42f7d7d2a`

```dockerfile
```

-	Layers:
	-	`sha256:ceb8acd73dcdae6da83be6503d3132ce35cf4e100ac22054ac97b7f2f4f46d92`  
		Last Modified: Sat, 01 Nov 2025 02:19:49 GMT  
		Size: 695.2 KB (695153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8a43ab896c04d3c07f2f67ffc358be838da51a1d19bf4061475b7bfcdd27002`  
		Last Modified: Sat, 01 Nov 2025 02:19:49 GMT  
		Size: 8.1 KB (8135 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-alpine3.21` - linux; riscv64

```console
$ docker pull hylang@sha256:bd7cd269647f033392ff8bb8d3010346ed309aeabf3f6e4a261282d0e9c4809d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22935595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b3bfc4b21b3ea1930fbd73228ded30b219e67d04ec58b5421ab0f82af5bac1`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 17:54:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 17:54:13 GMT
ENV LANG=C.UTF-8
# Mon, 13 Oct 2025 17:54:13 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 13 Oct 2025 17:54:13 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 13 Oct 2025 17:54:13 GMT
ENV PYTHON_VERSION=3.9.25
# Mon, 13 Oct 2025 17:54:13 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Sat, 01 Nov 2025 03:00:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Sat, 01 Nov 2025 03:00:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 01 Nov 2025 03:00:06 GMT
CMD ["python3"]
# Sat, 01 Nov 2025 03:34:56 GMT
ENV HY_VERSION=1.1.0
# Sat, 01 Nov 2025 03:34:56 GMT
ENV HYRULE_VERSION=1.0.0
# Sat, 01 Nov 2025 03:34:56 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 01 Nov 2025 03:34:56 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f874295bfcd01a87ee99265d45f0786d35242cd9d53bc2744cb330bf3be277f5`  
		Last Modified: Wed, 08 Oct 2025 21:19:05 GMT  
		Size: 3.4 MB (3351001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4666486ae2b3de4262dd119500cb4aed261920d55a1e4598d541bd3462e2414`  
		Last Modified: Mon, 13 Oct 2025 18:26:13 GMT  
		Size: 457.2 KB (457225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720b272a47583e0b355e9f5d2521008b5bfb3f1920ad824888f14fe48a4603b2`  
		Last Modified: Sat, 01 Nov 2025 03:01:06 GMT  
		Size: 15.4 MB (15402489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0138481cee27883158b720d29129903660087463bdf7153b607d4100dfa9f3fa`  
		Last Modified: Sat, 01 Nov 2025 03:01:05 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cdc91396e387c06714d997bc67e03d8f0a8785dbde31010c080c96916bb953`  
		Last Modified: Sat, 01 Nov 2025 03:35:40 GMT  
		Size: 3.7 MB (3724629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:27c66becde9eda999f1eb59f3c1163cacb748192cd630a99d654aa840765f366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.3 KB (703284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29566cc9260e107c555d61bc9734e65ce57031f9b0178845f533bba3c72188d4`

```dockerfile
```

-	Layers:
	-	`sha256:e0ffcbdb466c2a4e50003f3f35fc260b2cc8cf00a177b17f9b9c2c50426c0c9b`  
		Last Modified: Sat, 01 Nov 2025 05:18:45 GMT  
		Size: 695.1 KB (695149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a82b442d6df3d6243849322d7cff539a790ded7ade760df4189020da02bfd55`  
		Last Modified: Sat, 01 Nov 2025 05:18:46 GMT  
		Size: 8.1 KB (8135 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-alpine3.21` - linux; s390x

```console
$ docker pull hylang@sha256:4e997a8e5ec0ba3ab74ca9cb4134b1b43af8c841def5ac390950ce89e53bc43a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23427223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cc34a72dd7f78ec2b5935c533992612cc8ae248bb25fafc3fc68cd2cc112ac`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 12:59:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 12:59:53 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 12:59:53 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 09 Oct 2025 12:59:53 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 09 Oct 2025 12:59:53 GMT
ENV PYTHON_VERSION=3.9.25
# Thu, 09 Oct 2025 12:59:53 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Fri, 31 Oct 2025 23:36:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 31 Oct 2025 23:36:35 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 31 Oct 2025 23:36:35 GMT
CMD ["python3"]
# Fri, 31 Oct 2025 23:57:31 GMT
ENV HY_VERSION=1.1.0
# Fri, 31 Oct 2025 23:57:31 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 31 Oct 2025 23:57:31 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 31 Oct 2025 23:57:31 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Wed, 08 Oct 2025 16:25:19 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d403476d77f3c6d174042f0a35c75c77af9283be8ed3f5fdc93ad0cd153034`  
		Last Modified: Thu, 09 Oct 2025 13:06:21 GMT  
		Size: 457.9 KB (457870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9445343e8d0bedafedd4aa0fa81c2ae1a4922662042ffd764ce618761441657c`  
		Last Modified: Fri, 31 Oct 2025 23:36:53 GMT  
		Size: 15.8 MB (15779047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799bb8aa59b2d1622772a335db06423acf8dce75e3dd272e7a3c8754cdb222fd`  
		Last Modified: Fri, 31 Oct 2025 23:36:52 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af5743d05c1ef0dfb456b4907fc1bc8b697142ff9f611cb3d010ae16b7f17c1`  
		Last Modified: Fri, 31 Oct 2025 23:57:47 GMT  
		Size: 3.7 MB (3723623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:fd33d71ad4f2226bd69add99b4abcc9efd75c21c3a137212493febfc5a329ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.2 KB (703210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a4273bd39a08ed2a0249b58c787f217690c4e056fa10c20221911c82c213df`

```dockerfile
```

-	Layers:
	-	`sha256:ab0385dccf7a0824e8d85b66c172a7154b08e3c95b3df6a7079589bfcf48563f`  
		Last Modified: Sat, 01 Nov 2025 02:19:55 GMT  
		Size: 695.1 KB (695119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef9adbda426fc5a234ce4b03d50f60954e28b0f6ad7755d2c07d75fa824cdda5`  
		Last Modified: Sat, 01 Nov 2025 02:19:56 GMT  
		Size: 8.1 KB (8091 bytes)  
		MIME: application/vnd.in-toto+json
