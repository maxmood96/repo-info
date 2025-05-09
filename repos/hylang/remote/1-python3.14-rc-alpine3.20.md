## `hylang:1-python3.14-rc-alpine3.20`

```console
$ docker pull hylang@sha256:d1210b98a369ea1dd2efcb6f7d244eb58987210eb77eaf2d11c9b86399098137
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `hylang:1-python3.14-rc-alpine3.20` - linux; amd64

```console
$ docker pull hylang@sha256:7ccce609f8ae88a2892e1e27daf81d21ae5cef9fd72da5c624d69f8c61a7ba10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22730858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2c7b8c5256a037c6943de13950e15f0c1685d97706328e43991a9b5f671738`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 07 May 2025 15:49:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 May 2025 15:49:39 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 May 2025 15:49:39 GMT
ENV PYTHON_VERSION=3.14.0b1
# Wed, 07 May 2025 15:49:39 GMT
ENV PYTHON_SHA256=2ddd30a77c9f62e065ce648664a254b9b0c011bcdaa8c1c2787087e644cbeb39
# Wed, 07 May 2025 15:49:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 07 May 2025 15:49:39 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 May 2025 15:49:39 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e21e571d5bab62b1c66edf0bb76d413890a255e28ecdde9789158011740f94`  
		Last Modified: Thu, 08 May 2025 21:06:45 GMT  
		Size: 459.8 KB (459808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0568ca7f10b95c1099f23f12cd0e7a36493fefc19411f7347a64a1e78528b3f2`  
		Last Modified: Thu, 08 May 2025 21:06:45 GMT  
		Size: 12.8 MB (12795080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378bc159a37873d540f98a55378f999549b416acfd99cd877eaf90114b3e69fe`  
		Last Modified: Thu, 08 May 2025 21:06:44 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df74f591d9ff0912f962cefd4c05b6a2272ba6edd71f3d04d52606d9f5c2404`  
		Last Modified: Fri, 09 May 2025 17:38:07 GMT  
		Size: 5.8 MB (5848825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:19abc409643f313893896033f66a1a73634010d26beda053086e03a420dd3274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.4 KB (631416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a660f0b6f95edfc0377363830789f9afac71d57ed6c8e7fade8bb27b82dc4d1e`

```dockerfile
```

-	Layers:
	-	`sha256:5c0221e4e92d0fe6d90fe04210af78d0db7c91d10879b8680b9d1c63b5673036`  
		Last Modified: Fri, 09 May 2025 17:38:07 GMT  
		Size: 623.4 KB (623406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbd50c16cf801eedab3978ba739233c2fd6306a1a3ae3bf7c066da193e105bd5`  
		Last Modified: Fri, 09 May 2025 17:38:07 GMT  
		Size: 8.0 KB (8010 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-alpine3.20` - linux; arm variant v6

```console
$ docker pull hylang@sha256:776f08ae1f0334f42d714f7f93161ba796d7b944f3e8280d0b6320dfddd4f52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22139185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d7ea74f73be67b8778ec004f1d2cfd461b2373e44f1c459d1518f3a22d5bc9`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 07 May 2025 15:49:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 May 2025 15:49:39 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 May 2025 15:49:39 GMT
ENV PYTHON_VERSION=3.14.0b1
# Wed, 07 May 2025 15:49:39 GMT
ENV PYTHON_SHA256=2ddd30a77c9f62e065ce648664a254b9b0c011bcdaa8c1c2787087e644cbeb39
# Wed, 07 May 2025 15:49:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 07 May 2025 15:49:39 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 May 2025 15:49:39 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 18:28:14 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5eeb73306243b2db6ad0c79827275ba9524583cce792f88030997d7639b84b7`  
		Last Modified: Sat, 15 Feb 2025 08:05:03 GMT  
		Size: 459.1 KB (459059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cb1a3eacea3918d0165c691056ef6470edb29008fda837de2705baa2e8b64f`  
		Last Modified: Thu, 08 May 2025 21:11:12 GMT  
		Size: 12.5 MB (12458150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bf5fb05eaa6317e2151aae3064f052db8752884c5d41620c1d4b29b6e06207`  
		Last Modified: Thu, 08 May 2025 21:11:11 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b72f988d7e740e21ef5bced205a191116c01ceaac2b17d2ee3609ede8fd6008`  
		Last Modified: Fri, 09 May 2025 18:05:51 GMT  
		Size: 5.8 MB (5849197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:9daf3b46a8d52583ea507c09af792b8ae76ecddcce4ffd4d8cd4e6f83d1259bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314aadb873ad15bbdeb9820c78df4f56be06ff5a15f271d3436e53ff9a177e0b`

```dockerfile
```

-	Layers:
	-	`sha256:f3e5169a8fcbcdac515a08b5e505989117e5bf59577f4320ca695fb26213dd50`  
		Last Modified: Fri, 09 May 2025 18:05:50 GMT  
		Size: 7.9 KB (7871 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-alpine3.20` - linux; arm variant v7

```console
$ docker pull hylang@sha256:c0f69d212358220022c8c74b4f40530f4701e1fa51449549dbf551184119eaa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 MB (21502280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4900d1627bfb7908969d6bdbb8bb01a537ae3723616676ab95dc66e786752858`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 07 May 2025 15:49:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 May 2025 15:49:39 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 May 2025 15:49:39 GMT
ENV PYTHON_VERSION=3.14.0b1
# Wed, 07 May 2025 15:49:39 GMT
ENV PYTHON_SHA256=2ddd30a77c9f62e065ce648664a254b9b0c011bcdaa8c1c2787087e644cbeb39
# Wed, 07 May 2025 15:49:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 07 May 2025 15:49:39 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 May 2025 15:49:39 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d336ce3c8ea720a9be2cf80f08a4af7cb894e0c720ed9f7c1d8ec5208b5bb4d1`  
		Last Modified: Fri, 09 May 2025 02:36:19 GMT  
		Size: 459.9 KB (459885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d20c90ffbc946e06c91b9f0c57271e5edb42c7a0b7a0bec425a3cc79f1baed2`  
		Last Modified: Fri, 09 May 2025 02:36:20 GMT  
		Size: 12.1 MB (12097183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2de30a1d8d54ce9e0c1e704315f15f4a11bec9cd3565fbfb75ff2b17c6a40d`  
		Last Modified: Fri, 09 May 2025 02:36:19 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed433f85895f0cdd85504b1cc3f55c67553bfdb96de8a52fac3dc53c320daa0`  
		Last Modified: Fri, 09 May 2025 18:51:01 GMT  
		Size: 5.8 MB (5848995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:6ffb8e6880c5784a88229d6675d787e0723d999033b52b562b9465f531fc6d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.4 KB (634389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e5be58953f7893f63b739e66285e255d31821f999be8bc36cef95574288aeb`

```dockerfile
```

-	Layers:
	-	`sha256:cb2d46f3885e80dfa671533450483229bb00d334336c62d0b76dab79d529a6c0`  
		Last Modified: Fri, 09 May 2025 18:51:01 GMT  
		Size: 626.3 KB (626303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eccb19e326c2fe6e677ba16a20cb11937e6018d67739b7593757bb678cde7ec9`  
		Last Modified: Fri, 09 May 2025 18:51:01 GMT  
		Size: 8.1 KB (8086 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:d955dde0419f26db946141d6e52b9a987df5ec788e3a33249ee6015a020586c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23231856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:672fcbafe7ae06ef1c1eff1df2f044cea64762de0265ef5ab8b8800777c96291`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 07 May 2025 15:49:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 May 2025 15:49:39 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 May 2025 15:49:39 GMT
ENV PYTHON_VERSION=3.14.0b1
# Wed, 07 May 2025 15:49:39 GMT
ENV PYTHON_SHA256=2ddd30a77c9f62e065ce648664a254b9b0c011bcdaa8c1c2787087e644cbeb39
# Wed, 07 May 2025 15:49:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 07 May 2025 15:49:39 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 May 2025 15:49:39 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba6c0e9fdb3d4689a04cf8e5a24314a8f4b926b3939d90b4e94e35567df677b`  
		Last Modified: Thu, 08 May 2025 22:03:28 GMT  
		Size: 461.8 KB (461849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acd0cca292f6c88ee77707baf8ebb7cefbea3d46dedb8784b47c77d39e0eb9c`  
		Last Modified: Thu, 08 May 2025 22:03:29 GMT  
		Size: 12.8 MB (12829582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69e59f47ed610ea8cf7fc9edb5b7b594f5bb68f42a902b909f8e8cb09b68d01`  
		Last Modified: Thu, 08 May 2025 22:03:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13271f392a7868a2eea1ef9889d22bfeffb6d3087ae74a314e8e60162c7c3a3`  
		Last Modified: Fri, 09 May 2025 19:01:49 GMT  
		Size: 5.8 MB (5849013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:0bbd5d3a90f3f3f12dbd35c30ec9bc5d5bb090afb72a95d11b84629e6637cb23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.6 KB (631576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20548633df1d24ee1ab32659d0436f88288318f7b64de7e309aa9b858d9bb9c`

```dockerfile
```

-	Layers:
	-	`sha256:8ca336255eb4463d73d0363a1f64cf2156c739b5422f1109646f34514df241c0`  
		Last Modified: Fri, 09 May 2025 19:01:48 GMT  
		Size: 623.5 KB (623462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56ac29751765be59671945639bea12ad20f4eb8db2178e737d2f18ca3e262069`  
		Last Modified: Fri, 09 May 2025 19:01:48 GMT  
		Size: 8.1 KB (8114 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-alpine3.20` - linux; 386

```console
$ docker pull hylang@sha256:14b87db4c94fcd6dbf4e17211e6854c53a0838cabee311512d6cfbb412b54ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22874898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dec6f6e1fd5e0bc910a86a6cc2838957b3b234a39c131e8e7bb00f57364fe94`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 07 May 2025 15:49:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 May 2025 15:49:39 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 May 2025 15:49:39 GMT
ENV PYTHON_VERSION=3.14.0b1
# Wed, 07 May 2025 15:49:39 GMT
ENV PYTHON_SHA256=2ddd30a77c9f62e065ce648664a254b9b0c011bcdaa8c1c2787087e644cbeb39
# Wed, 07 May 2025 15:49:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 07 May 2025 15:49:39 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 May 2025 15:49:39 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7b4fe26cc7795e970db2ccb5d4e9fc58a505e23a52cc34c444620afb14590`  
		Last Modified: Thu, 08 May 2025 21:07:08 GMT  
		Size: 460.3 KB (460300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e9b12fc6c691b73ab8f6463ef52546706407a1e93464018df5ff2a1f6534c2`  
		Last Modified: Thu, 08 May 2025 21:07:09 GMT  
		Size: 13.1 MB (13093581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb37eb05a452ecb0f36fcad0a1466aee20726932bb2eea094d2b9f189f57ae9`  
		Last Modified: Thu, 08 May 2025 21:07:08 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf305bdaf0af932679c7632b06216a3a4100438870945e0bb234002baf355b1`  
		Last Modified: Fri, 09 May 2025 17:36:10 GMT  
		Size: 5.8 MB (5849100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:b56c57c0368b1af4986add7c01e16e9123b3c2da4d23c63c88d791f77a89382e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.4 KB (631359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05eb5e3f36f3bece4f645b6ae460023ba80f4a788adff89b1b30cc2230212b3f`

```dockerfile
```

-	Layers:
	-	`sha256:08a38ea836f08656fbaf3af356b2add8fc49fd27e589b84a66522b6c0560ead3`  
		Last Modified: Fri, 09 May 2025 17:36:10 GMT  
		Size: 623.4 KB (623381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5b0a4e8cd420ad70f14446362b61bcb44d147a9f28dd61a4a0fa992ae7e5da6`  
		Last Modified: Fri, 09 May 2025 17:36:10 GMT  
		Size: 8.0 KB (7978 bytes)  
		MIME: application/vnd.in-toto+json
