## `python:alpine3.23`

```console
$ docker pull python@sha256:7af51ebeb83610fb69d633d5c61a2efb87efa4caf66b59862d624bb6ef788345
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

### `python:alpine3.23` - linux; amd64

```console
$ docker pull python@sha256:079b889b270e730f38bdbabf505362538db449a216895c2c45664b1538bd34d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17683805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34693fd53e5f9735174e27709412ddf62ead2616c5ce4d0a0a3f687f03e1fbd0`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:39:50 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:39:50 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 18 Dec 2025 00:39:50 GMT
ENV PYTHON_VERSION=3.14.2
# Thu, 18 Dec 2025 00:39:50 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Thu, 18 Dec 2025 00:42:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 18 Dec 2025 00:42:10 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 18 Dec 2025 00:42:10 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7852f7f4030ee1cb8e32bef7b36b61aa578b5519a4f2bbdbf38695af8350e0f5`  
		Last Modified: Thu, 18 Dec 2025 00:42:21 GMT  
		Size: 460.9 KB (460947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a26977b06f4aec5f8567df9de4b8fe5e1ae0d29dc340f71fbbe6c9a839eb789`  
		Last Modified: Thu, 18 Dec 2025 00:42:16 GMT  
		Size: 13.4 MB (13362505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8c8024fc8955bfe8ee0423d199034a44138f3173ec68934f461aa6d7f41fa3`  
		Last Modified: Thu, 18 Dec 2025 00:42:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.23` - unknown; unknown

```console
$ docker pull python@sha256:e22c351eaf5c67df55ef87b8552cabf440790f9427b6fcf31b62443921f38a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.6 KB (640627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f325125c23065d731346ba917061741cff8eb79dede4a365d9db6c8038badc76`

```dockerfile
```

-	Layers:
	-	`sha256:edf0ef368440144a284353e253efb73cb4f19bc21bf526cb2a4f07e835d6a921`  
		Last Modified: Thu, 18 Dec 2025 03:19:01 GMT  
		Size: 618.0 KB (617962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5deade82ea8119536d4db95a611ef3975d4728458695dbadb34cc2b32f16462`  
		Last Modified: Thu, 18 Dec 2025 03:19:02 GMT  
		Size: 22.7 KB (22665 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.23` - linux; arm variant v6

```console
$ docker pull python@sha256:c0ab0a7dbd3817518a4128bbbb6a2672fd3b83c6b4b7a09b871a3c11528cb13a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17015187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627ff1edab77c6f4d531c7e08eb8f050aad0aed0af9219cf7b350b71f4362243`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:51:18 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:51:18 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 18 Dec 2025 00:51:18 GMT
ENV PYTHON_VERSION=3.14.2
# Thu, 18 Dec 2025 00:51:18 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Thu, 18 Dec 2025 00:54:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 18 Dec 2025 00:54:00 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 18 Dec 2025 00:54:00 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a1f6eb85ed699d3da92435e4b6bf0488a0de3e83e3ca4fe39ee65129be380b`  
		Last Modified: Thu, 18 Dec 2025 00:54:05 GMT  
		Size: 461.4 KB (461435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf560cf070e0b54409a05124b58bf352c1d33c11ac214efefa330cfddb0b35d`  
		Last Modified: Thu, 18 Dec 2025 00:54:06 GMT  
		Size: 13.0 MB (12985073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb705225fe50818778bac4b591f83ee2400c2ba490eada68900341986f9c02`  
		Last Modified: Thu, 18 Dec 2025 00:54:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.23` - unknown; unknown

```console
$ docker pull python@sha256:698cebeb9f55d55cc7ce4a8c03f043b50922fcda1fe74eff4e65a5006e0f3ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 KB (22588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d42da6346cdda390532c32978d1a703768c69376e7d04a14280c64a07d69377`

```dockerfile
```

-	Layers:
	-	`sha256:c1fac2fac1d8a9b58e4ce68584f06b84d8c6f20d07ee72bb5784970a8bbe4287`  
		Last Modified: Thu, 18 Dec 2025 00:54:05 GMT  
		Size: 22.6 KB (22588 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.23` - linux; arm variant v7

```console
$ docker pull python@sha256:8af21e9d62fec5d2e3930d22e5ca1405d6f90b83912999cd4ba2cc5a435df787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16328452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1be20aa56c071f9a9286f284098210f2a689eafbd3b4bfbce9df4a990cba2d`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:51:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:51:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 18 Dec 2025 00:51:30 GMT
ENV PYTHON_VERSION=3.14.2
# Thu, 18 Dec 2025 00:51:30 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Thu, 18 Dec 2025 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 18 Dec 2025 00:54:12 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 18 Dec 2025 00:54:12 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816af132b3f4e3b6967dd0e0160397b0bfffd42b9d3a8e1c7544db2025a01c18`  
		Last Modified: Thu, 18 Dec 2025 00:54:18 GMT  
		Size: 460.7 KB (460735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0b3373dc2488dde3d99d022976ece03183f246763d74ef4f01e9366290db98`  
		Last Modified: Thu, 18 Dec 2025 00:54:19 GMT  
		Size: 12.6 MB (12588081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc384662348fdcba9b7a3b98187b40dd5d8f9935e54d2748de355f3c1ad16411`  
		Last Modified: Thu, 18 Dec 2025 00:54:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.23` - unknown; unknown

```console
$ docker pull python@sha256:17f4ad0a315e4736814b049631119990fee2cc0d9cc646850c68cd53761d3de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.2 KB (643173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7962b3847d6366fbadbe5098267d0a494639827439c7eac30cde6340b594e70`

```dockerfile
```

-	Layers:
	-	`sha256:1e671e2face6baa469cabb73869a13d31837d5460887cf5f2be606829cdbca5c`  
		Last Modified: Thu, 18 Dec 2025 00:54:18 GMT  
		Size: 620.4 KB (620370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa797a0a11664380c1ad2e8c8dd95c08d404f302774ec96bc055dc5529f4b25d`  
		Last Modified: Thu, 18 Dec 2025 00:54:18 GMT  
		Size: 22.8 KB (22803 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull python@sha256:d7ce2729f5f4d1716be99bc2376a7ea2906d293543c4bcd31693e569e6c04fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18110670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6eaca30cf8f88d713fd5040661cefa076b0e809dc27a52e38863c567531379`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:40:35 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:40:35 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 18 Dec 2025 00:40:35 GMT
ENV PYTHON_VERSION=3.14.2
# Thu, 18 Dec 2025 00:40:35 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Thu, 18 Dec 2025 00:43:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 18 Dec 2025 00:43:08 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 18 Dec 2025 00:43:08 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230ee060cedf91a53b1c6f3c40330140e282f461eec439abeee70c77f0ed6ead`  
		Last Modified: Thu, 18 Dec 2025 00:43:15 GMT  
		Size: 463.0 KB (463016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8ad93b1a6cfb42f20dbce20bb518a9576de26808885bea9e9feaca382f0984`  
		Last Modified: Thu, 18 Dec 2025 00:43:23 GMT  
		Size: 13.5 MB (13451666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd65fd9f19f58489ad910135803d1d89928927820d73110adefa161932cd335a`  
		Last Modified: Thu, 18 Dec 2025 00:43:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.23` - unknown; unknown

```console
$ docker pull python@sha256:a32c11523607f2efadaf728f168a85c3e6ac5800fa886460dc3578e2f4389f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.3 KB (640263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6ee0f13ec6ea916bb72187f79cd69e84d62fe1115ae30067e53acb8e94b5ce`

```dockerfile
```

-	Layers:
	-	`sha256:1184c21552811f5c4d881b307950f6ff335daaea723120e0f6fc440fe8365580`  
		Last Modified: Thu, 18 Dec 2025 03:18:56 GMT  
		Size: 617.4 KB (617416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e8a9e24a16f169d561516da48120f4c89e4c66f3815dbf2440e25af47cd3f75`  
		Last Modified: Thu, 18 Dec 2025 00:43:15 GMT  
		Size: 22.8 KB (22847 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.23` - linux; 386

```console
$ docker pull python@sha256:13581a8ce73b217595e17ad3d592f1e28ba7e2000ed1b9ddfe7b0380b3dfb2c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17763074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3163eb3dab6cd70f2d19ab8e434212ac9c4004aaaf2eb6a8ee7797f2a9bb973`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:39:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:39:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 18 Dec 2025 00:39:59 GMT
ENV PYTHON_VERSION=3.14.2
# Thu, 18 Dec 2025 00:39:59 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Thu, 18 Dec 2025 00:42:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 18 Dec 2025 00:42:48 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 18 Dec 2025 00:42:48 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525a4a216346fb0072f57313721593297c53421be7effa83f1517d0f5b3c5dc8`  
		Last Modified: Thu, 18 Dec 2025 00:42:55 GMT  
		Size: 461.2 KB (461228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed6d4da45500258614e447c9a2863dfb0feffb4a997bc73536dec86bf679eca`  
		Last Modified: Thu, 18 Dec 2025 00:42:55 GMT  
		Size: 13.6 MB (13615498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b69c21401cd011d3c9ac35b95f48a03a7675c0ab20f2dc2bbf8b8737d8b823`  
		Last Modified: Thu, 18 Dec 2025 00:42:54 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.23` - unknown; unknown

```console
$ docker pull python@sha256:90f009311d52e59a45bcb9ebf0fefa1c88f67b51e344c1ecc5fa5d1310cc2f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.5 KB (640526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000d2b376e41e685b36375871b3361ebabccb49cd2eb20f6dd2be326cfc5024`

```dockerfile
```

-	Layers:
	-	`sha256:f607991fd1de5e3473ff11ea6d403c3ac443390e7fb27d21dc05646774bf577a`  
		Last Modified: Thu, 18 Dec 2025 03:19:08 GMT  
		Size: 617.9 KB (617917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb2a9ce8ce1bbbeb100c54456d55900bb11d9c4d0cb97ef9debe7477cff9d1de`  
		Last Modified: Thu, 18 Dec 2025 03:19:09 GMT  
		Size: 22.6 KB (22609 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.23` - linux; ppc64le

```console
$ docker pull python@sha256:66c28878504c044816edb8d0080eeb3f03339f716b4822ba5352efd4751f1c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18531376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64218f357b6f59731fac5719b43e958c8f3a290292a13da938f79e47827a17aa`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:40:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:40:16 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 18 Dec 2025 01:40:16 GMT
ENV PYTHON_VERSION=3.14.2
# Thu, 18 Dec 2025 01:40:16 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Thu, 18 Dec 2025 01:46:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 18 Dec 2025 01:46:16 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 18 Dec 2025 01:46:16 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:42 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a546da2393a036672bb1492f778abae140eef4dce74fd37f306e27278d756b`  
		Last Modified: Thu, 18 Dec 2025 01:46:36 GMT  
		Size: 463.5 KB (463467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f40cd26b429fca0a714033b011665cb27d07ac508df8e316d237ce0b82dd3d`  
		Last Modified: Thu, 18 Dec 2025 01:46:31 GMT  
		Size: 14.2 MB (14239904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b63a45a70420035ac5741091d22c5aa30dd6b3da44fcdb4431029440e799b45`  
		Last Modified: Thu, 18 Dec 2025 01:46:36 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.23` - unknown; unknown

```console
$ docker pull python@sha256:95b90fad7bc28f98b1dfd5e1967f531167f4da6ec86040db1d84af215ef58443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.1 KB (640105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9d25f76c9cac3a3e08eab1f96d0bdebdd019fe060651f289eb22c412bd5f87`

```dockerfile
```

-	Layers:
	-	`sha256:aaa26306783f9c2be13fd929c4f4f666686df8d6939fe0682a7bb87a5d99855d`  
		Last Modified: Thu, 18 Dec 2025 01:46:30 GMT  
		Size: 617.4 KB (617369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23f218ff8c6f2a1b23d4b0850c34f8e00ecd987f3f33c9b5e052e18942e49af2`  
		Last Modified: Thu, 18 Dec 2025 01:46:30 GMT  
		Size: 22.7 KB (22736 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.23` - linux; riscv64

```console
$ docker pull python@sha256:403046ef91f7cc62a19595e47edce80de469dd2a4c7c81d656de57acb7d43111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17528974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6e23ceb02fbdc3f29a3aa3b5c637674687f0a1413e802566ee5d130d68fb09`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:56:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Dec 2025 05:56:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 19 Dec 2025 05:56:43 GMT
ENV PYTHON_VERSION=3.14.2
# Fri, 19 Dec 2025 05:56:43 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Fri, 19 Dec 2025 07:19:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 19 Dec 2025 07:19:58 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 19 Dec 2025 07:19:58 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c1297d0b47f8cc996fa306111fc37eee4492b207584fc90d6151f5b00513f5`  
		Last Modified: Fri, 19 Dec 2025 06:38:01 GMT  
		Size: 461.2 KB (461189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac744c1eb54ba37619f7bf7648e886af8c31a724a7422d7c56c63dd25c48da59`  
		Last Modified: Fri, 19 Dec 2025 07:20:53 GMT  
		Size: 13.5 MB (13483595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cb6cdfe6728bc08af8b708a5e430c8483cc08e4b7c47f4e5e41c8e8664caa5`  
		Last Modified: Fri, 19 Dec 2025 07:20:42 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.23` - unknown; unknown

```console
$ docker pull python@sha256:3647126b771967498a49facbd6b7e0e6d26f7ee4fde4e145f7800b579023da6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.1 KB (640102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39cb51d118e44721509aba7898c8e5bc507939e98872ffaeaca454533fc03950`

```dockerfile
```

-	Layers:
	-	`sha256:62523b6850e0402bd6823463ef403a97a5fe353f892d8dd3ed6f97f16d43cffc`  
		Last Modified: Fri, 19 Dec 2025 10:07:03 GMT  
		Size: 617.4 KB (617365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2ff63d23e31b115aa04922010c47050f7f89aa4202c398208f754f35756bb84`  
		Last Modified: Fri, 19 Dec 2025 10:07:03 GMT  
		Size: 22.7 KB (22737 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.23` - linux; s390x

```console
$ docker pull python@sha256:1793e10627303794a46534ab2c2dc72e7de9465538dd7926cee3c0dc81c83bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18034527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a70c52b6ea7828d3ce3d96559aa96f115a7c0f1caa61336927cd9cde61203f`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 02:45:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 02:45:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 18 Dec 2025 02:45:06 GMT
ENV PYTHON_VERSION=3.14.2
# Thu, 18 Dec 2025 02:45:06 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Thu, 18 Dec 2025 03:04:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 18 Dec 2025 03:04:03 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 18 Dec 2025 03:04:03 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:04 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4b1699aa656b23eebe8081f75dec9a272ed29e847d1ea394e07fd40420d6c4`  
		Last Modified: Thu, 18 Dec 2025 02:54:46 GMT  
		Size: 461.7 KB (461734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9accacf7a821986d4fda2a0fea3ae7ebe664f2fc9b277edbe9a0888e6082e8`  
		Last Modified: Thu, 18 Dec 2025 03:04:34 GMT  
		Size: 13.8 MB (13848232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31477603734b9badbcbde1fcc36e9d08bee6a50006d2ac7d1933f95addcb1bf2`  
		Last Modified: Thu, 18 Dec 2025 03:04:28 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.23` - unknown; unknown

```console
$ docker pull python@sha256:210b7507727d1bb39c8d10a95c3b5759b922902a761ea61bc34262edd9562bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 KB (639976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308ab683c5b1a3ed37bb3f39c00d4ad864dfb53266462489069682ed287f28ec`

```dockerfile
```

-	Layers:
	-	`sha256:9c4ae6fa11d5dd0fb9477f074d60a54b341d6015e93ef7ee752ae9296d3f229e`  
		Last Modified: Thu, 18 Dec 2025 04:06:55 GMT  
		Size: 617.3 KB (617311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a30a8dee995141441b785c482d595aa5502cfe90fc87a67fd9fb3ee9982921b`  
		Last Modified: Thu, 18 Dec 2025 04:06:56 GMT  
		Size: 22.7 KB (22665 bytes)  
		MIME: application/vnd.in-toto+json
