## `hylang:python3.14-alpine3.21`

```console
$ docker pull hylang@sha256:d93f3253a47a51a50157425e684833bad6316bd95996701ed58be6747bd2c455
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

### `hylang:python3.14-alpine3.21` - linux; amd64

```console
$ docker pull hylang@sha256:4a140c7c28e6ae0d246a896b7847b307671464f9cf21bed77a28622bb50eef00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23103640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d8a7bc5893229cf44150edd7f5d90ade7d918014be6f05b941ef9fb081f8d2`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 01:06:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Dec 2025 01:06:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 03 Dec 2025 01:06:00 GMT
ENV PYTHON_VERSION=3.14.1
# Wed, 03 Dec 2025 01:06:00 GMT
ENV PYTHON_SHA256=8dfa08b1959d9d15838a1c2dab77dc8d8ff4a553a1ed046dfacbc8095c6d42fc
# Wed, 03 Dec 2025 01:08:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Dec 2025 01:08:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Dec 2025 01:08:40 GMT
CMD ["python3"]
# Wed, 03 Dec 2025 02:13:09 GMT
ENV HY_VERSION=1.1.0
# Wed, 03 Dec 2025 02:13:09 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 03 Dec 2025 02:13:09 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 03 Dec 2025 02:13:09 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1bda70e359377fb9cf9d41560ace52f414a124ed1f330fee6c70b2a8fd542e`  
		Last Modified: Wed, 03 Dec 2025 01:09:02 GMT  
		Size: 456.9 KB (456887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5041f7dbd249bb38f5145b62e7e0e5de0e9ec4a48d9e2c973d9249feab81de84`  
		Last Modified: Wed, 03 Dec 2025 01:09:03 GMT  
		Size: 13.3 MB (13288606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cae13779ee91b584c404ad8ed545503eb1f39fe4fa45afbe97c433e2f2c7749`  
		Last Modified: Wed, 03 Dec 2025 01:09:02 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5066a7d4b26998d0244c332641d019d32a8ecb2cf958a335c0f5af22bc464c4d`  
		Last Modified: Wed, 03 Dec 2025 02:13:22 GMT  
		Size: 5.7 MB (5715330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:11b80c90f6cdd21a1264e9f5b0a70b3a4f58a9ce556063c87ad5ab8f8e8ed960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.4 KB (633377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b2f2d905e76516059fbfef71b747fa47e56d6bdb4ae5308de2cc8ab4c85dc3`

```dockerfile
```

-	Layers:
	-	`sha256:1e53ca303a1a6e11d3bba8c801cc76cff197791c1ba082c9cebbf813499b1007`  
		Last Modified: Wed, 03 Dec 2025 03:18:16 GMT  
		Size: 624.1 KB (624093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51695ac3cb41e99f8573f5d60272eb651293e3ea8fdb892037c396447982cc27`  
		Last Modified: Wed, 03 Dec 2025 03:18:17 GMT  
		Size: 9.3 KB (9284 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.21` - linux; arm variant v6

```console
$ docker pull hylang@sha256:37d239574a4f862c26e8b15aa4be0435af8109c730067aa1b87a6922679bf1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.4 MB (22424306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f206e43ab09fe79a9770fbf6124dfcb2b49a90deea87f511a3454b67a09a77ea`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 01:07:32 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Dec 2025 01:07:32 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 03 Dec 2025 01:07:32 GMT
ENV PYTHON_VERSION=3.14.1
# Wed, 03 Dec 2025 01:07:32 GMT
ENV PYTHON_SHA256=8dfa08b1959d9d15838a1c2dab77dc8d8ff4a553a1ed046dfacbc8095c6d42fc
# Wed, 03 Dec 2025 01:10:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Dec 2025 01:10:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Dec 2025 01:10:29 GMT
CMD ["python3"]
# Wed, 03 Dec 2025 02:12:25 GMT
ENV HY_VERSION=1.1.0
# Wed, 03 Dec 2025 02:12:25 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 03 Dec 2025 02:12:25 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 03 Dec 2025 02:12:25 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a365463a776cd382c44d265a9310b8bf4bb854065f61dfa850b0e9c1cda999f`  
		Last Modified: Wed, 03 Dec 2025 01:10:41 GMT  
		Size: 457.7 KB (457692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae31a6d105c3552e5b6c1a73680598353fc7df55447f8a186581649dc670b9c`  
		Last Modified: Wed, 03 Dec 2025 01:10:43 GMT  
		Size: 12.9 MB (12885581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e5a5e9643a88093e28f8dc0175b508fd2c1541d124aa9df49c83fffaaf0a39`  
		Last Modified: Wed, 03 Dec 2025 01:10:41 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ca271264e36c54820293b7852de98e986d352f798530decc547aeab6914b9a`  
		Last Modified: Wed, 03 Dec 2025 02:12:34 GMT  
		Size: 5.7 MB (5715315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:861365299ff57830d28e410dee4dabd7d2decc075bb7a69258faa5dbc1d75671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a4f81e30d10fc4a50bcddd1e7353d600a917901e734c1cb9069daf3f07fc51`

```dockerfile
```

-	Layers:
	-	`sha256:70fc75837ed4daa8a47ce685ded394761a3db2a77e19aa59fa6922bdf2f8796f`  
		Last Modified: Wed, 03 Dec 2025 03:18:20 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.21` - linux; arm variant v7

```console
$ docker pull hylang@sha256:59a7a50b704b1d567bada3bd0813b594edab4fd220d5af1008d8cb0cf73aca26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21768007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22975643eb9cb8a3b9adee24b1785988290af1fefc2b3095a01d7e51253d3d48`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 01:25:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Dec 2025 01:25:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 03 Dec 2025 01:25:59 GMT
ENV PYTHON_VERSION=3.14.1
# Wed, 03 Dec 2025 01:25:59 GMT
ENV PYTHON_SHA256=8dfa08b1959d9d15838a1c2dab77dc8d8ff4a553a1ed046dfacbc8095c6d42fc
# Wed, 03 Dec 2025 01:28:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Dec 2025 01:28:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Dec 2025 01:28:55 GMT
CMD ["python3"]
# Wed, 03 Dec 2025 02:12:34 GMT
ENV HY_VERSION=1.1.0
# Wed, 03 Dec 2025 02:12:34 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 03 Dec 2025 02:12:34 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 03 Dec 2025 02:12:34 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83532e9f9634560ece3fdbf67e32d9dadb35571c8b6fcca4fecb7f75ce9652f7`  
		Last Modified: Wed, 03 Dec 2025 01:29:11 GMT  
		Size: 456.9 KB (456890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c1f4853882535259f349ba4cf75ac15944607ec78dd26e9a0ed61ae9b60ab9`  
		Last Modified: Wed, 03 Dec 2025 01:29:15 GMT  
		Size: 12.5 MB (12496988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0ebc0a444453490bc49a91b2fc0419f77de9cd04c051fddb2e3ab4e30f2dd1`  
		Last Modified: Wed, 03 Dec 2025 01:29:12 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785d6d972cc1e9b08a76662b2c49a47d30745bb2da97c515ba9208178d59dcb`  
		Last Modified: Wed, 03 Dec 2025 02:12:47 GMT  
		Size: 5.7 MB (5715271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:fbc6c862266200de2e37220ff13105a83f9ae31b686068c25f2e911c07b85f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.5 KB (636547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818583eddfd16628061972c7426724fa34534e5e2a46506f0834bfe44bf82cff`

```dockerfile
```

-	Layers:
	-	`sha256:ac246bb856cdf62183a850a5f2729d4152e2ca2bdc380cdf6b04a97ee2649875`  
		Last Modified: Wed, 03 Dec 2025 03:18:24 GMT  
		Size: 627.2 KB (627151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c6d8e174b3d62d536e4b04cbc759affd7b526c0de8d3c5c4d20ec40a50981c5`  
		Last Modified: Wed, 03 Dec 2025 03:18:24 GMT  
		Size: 9.4 KB (9396 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:18e9e0f232dd39d9a039c0e5422305a3492ed0e81fc098db8a4cd3fd0edadc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23437238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f882ceab02bff41265761c6ec239b35c230817737684564bd83ff253db96d1f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 01:04:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Dec 2025 01:04:49 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 03 Dec 2025 01:04:49 GMT
ENV PYTHON_VERSION=3.14.1
# Wed, 03 Dec 2025 01:04:49 GMT
ENV PYTHON_SHA256=8dfa08b1959d9d15838a1c2dab77dc8d8ff4a553a1ed046dfacbc8095c6d42fc
# Wed, 03 Dec 2025 01:07:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Dec 2025 01:07:12 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Dec 2025 01:07:12 GMT
CMD ["python3"]
# Wed, 03 Dec 2025 02:11:48 GMT
ENV HY_VERSION=1.1.0
# Wed, 03 Dec 2025 02:11:48 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 03 Dec 2025 02:11:48 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 03 Dec 2025 02:11:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c087d71e6855bc7c502b77093d848e716647582b3d0319a4f6a26dfb688f8faa`  
		Last Modified: Wed, 03 Dec 2025 01:07:38 GMT  
		Size: 459.0 KB (458988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f05ca2d101b6edb6f21fedeb013bc1c0c8317d32ae7b06a5af84ee051038ca`  
		Last Modified: Wed, 03 Dec 2025 01:07:40 GMT  
		Size: 13.3 MB (13270432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db283d08b4ea086bac3e2987bb8eb3c66352e9fd3792e308b33a10ae4394906`  
		Last Modified: Wed, 03 Dec 2025 01:07:39 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f585ea71000a593582216bcdcbdbb56af7b97cfef86a0e8702284f697fbfc293`  
		Last Modified: Wed, 03 Dec 2025 02:12:01 GMT  
		Size: 5.7 MB (5715214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:88da33149c41a4f26b57546084393ef8376b9da35cf87ddaec0acd00fade7890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.6 KB (633633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61734b78529e6228f2c8ab1043d1f4d64a194485cba5a3ad42990d5af158f36d`

```dockerfile
```

-	Layers:
	-	`sha256:1b8806a79638764c38089084a599a21706cb8120330d4764c1e7bd23eb01131d`  
		Last Modified: Wed, 03 Dec 2025 03:18:28 GMT  
		Size: 624.2 KB (624197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65a945c28d4bd7bfc670527ca2f19c96898092423ef1fc68eae8a25313b6ac93`  
		Last Modified: Wed, 03 Dec 2025 03:18:28 GMT  
		Size: 9.4 KB (9436 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.21` - linux; 386

```console
$ docker pull hylang@sha256:75e3155a81053669983b992aba0788c76e0f600d21434b476ac3d543af03f4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23184915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e856241767a1f5f4f6ff936e6e730d25effedff4ce52a98162e35e9c227de1b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 01:06:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Dec 2025 01:06:39 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 03 Dec 2025 01:06:39 GMT
ENV PYTHON_VERSION=3.14.1
# Wed, 03 Dec 2025 01:06:39 GMT
ENV PYTHON_SHA256=8dfa08b1959d9d15838a1c2dab77dc8d8ff4a553a1ed046dfacbc8095c6d42fc
# Wed, 03 Dec 2025 01:09:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Dec 2025 01:09:32 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Dec 2025 01:09:32 GMT
CMD ["python3"]
# Wed, 03 Dec 2025 02:11:23 GMT
ENV HY_VERSION=1.1.0
# Wed, 03 Dec 2025 02:11:23 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 03 Dec 2025 02:11:23 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 03 Dec 2025 02:11:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca33e93081eeb51265b7c7d8091b9611206390fdb4992aca6d90c9a48eb795b`  
		Last Modified: Wed, 03 Dec 2025 01:09:45 GMT  
		Size: 457.4 KB (457352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147e75faf28899a8efd8a097a1050d7db2f388bbc43a2316af4ac28cf2b910f0`  
		Last Modified: Wed, 03 Dec 2025 01:09:46 GMT  
		Size: 13.5 MB (13547277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7041b72837bcb13f4b97c76ad303ba4be110d18a9fcb6441dd97056df381ec62`  
		Last Modified: Wed, 03 Dec 2025 01:09:45 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d72104b928ff4ba6e702baca023df6726da51697b9ad1b3205425e3b8af2ad`  
		Last Modified: Wed, 03 Dec 2025 02:11:36 GMT  
		Size: 5.7 MB (5715333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:4200c1004b3fb00ed5b4cbed9daedfee0b956e7dbf65294df9869e57fb1737a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.3 KB (633279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f97fc20325292a998037b60551cd076581225c4781962a418f469efd58c67b`

```dockerfile
```

-	Layers:
	-	`sha256:1432a02975b95665eae7324061fe6fee42fc80b0adb033dc5ce9399aa1de469e`  
		Last Modified: Wed, 03 Dec 2025 03:18:32 GMT  
		Size: 624.0 KB (624048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c56f7070077f5e8a5d120fce3628254cabede5f6fcfa024ff7f2e4231f604582`  
		Last Modified: Wed, 03 Dec 2025 03:18:33 GMT  
		Size: 9.2 KB (9231 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.21` - linux; ppc64le

```console
$ docker pull hylang@sha256:e461e9103c7265753b3464fa37b297e0204a72eaadb3f7c4dba5254e40e120a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23819648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065ebce7dad8d0f121c8d93d53885917dd41e4639a28ffddbd68893f408ab79d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 01:41:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Dec 2025 01:41:02 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 03 Dec 2025 01:41:02 GMT
ENV PYTHON_VERSION=3.14.1
# Wed, 03 Dec 2025 01:41:02 GMT
ENV PYTHON_SHA256=8dfa08b1959d9d15838a1c2dab77dc8d8ff4a553a1ed046dfacbc8095c6d42fc
# Wed, 03 Dec 2025 01:43:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Dec 2025 01:43:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Dec 2025 01:43:41 GMT
CMD ["python3"]
# Wed, 03 Dec 2025 04:16:06 GMT
ENV HY_VERSION=1.1.0
# Wed, 03 Dec 2025 04:16:06 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 03 Dec 2025 04:16:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 03 Dec 2025 04:16:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283cffed9550cb8a1104c4085abd886a974b98e6d50016411b7dcbd9e06ce4b2`  
		Last Modified: Wed, 03 Dec 2025 01:44:07 GMT  
		Size: 459.4 KB (459404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3ea4111ff4d58c81eea0bf791c8eb91f49160b52bb35c808c4b2ef185c48c3`  
		Last Modified: Wed, 03 Dec 2025 01:44:08 GMT  
		Size: 14.1 MB (14070488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeb06c710a765fec02cfa7bbd71fba1d5d90b1050ef8f414d00545048198bd1`  
		Last Modified: Wed, 03 Dec 2025 01:44:06 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e73e596fa0de51b670cc929000c799de291df207e1c13ca3e0df9fa0a796de9`  
		Last Modified: Wed, 03 Dec 2025 04:16:25 GMT  
		Size: 5.7 MB (5715431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:12dce1579ac6a9deb3710aa071cb24b0cdd820439e66c901c78138da6f683304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.6 KB (631552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3c3d9a782b01a926968837eaaa1889bcc47a5d1dab7cf2d21e354b16436e13`

```dockerfile
```

-	Layers:
	-	`sha256:0798dae105a49d4db1d7b7637092119253f269f445536dbb6d4b7be4785368dc`  
		Last Modified: Wed, 03 Dec 2025 06:17:42 GMT  
		Size: 622.2 KB (622200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4962eae8bb80409ecf3040aafb2a5a2537f7b759d5edd06fec8bd2afda155d0c`  
		Last Modified: Wed, 03 Dec 2025 06:17:42 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.21` - linux; riscv64

```console
$ docker pull hylang@sha256:bac59037c7bf05d0dc29531a5a78cffbe69613c1329facf84ee1b99a1533e7f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22907131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d12b73f3b0959e4de7309f20f4c930463afb9cbb933958ceb7995bb9cf000cc`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.14.0
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Sat, 22 Nov 2025 22:37:46 GMT
ENV HY_VERSION=1.1.0
# Sat, 22 Nov 2025 22:37:46 GMT
ENV HYRULE_VERSION=1.0.1
# Sat, 22 Nov 2025 22:37:46 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 22 Nov 2025 22:37:46 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f874295bfcd01a87ee99265d45f0786d35242cd9d53bc2744cb330bf3be277f5`  
		Last Modified: Wed, 08 Oct 2025 21:19:05 GMT  
		Size: 3.4 MB (3351001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d6f0ef7935c8394b7aa736e2595da7669db080ca4e2940fd0393e48cabf7f1`  
		Last Modified: Sat, 11 Oct 2025 02:17:38 GMT  
		Size: 457.2 KB (457229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc830ef2858f93b567ddc4a853cebd8437bb747a495881486c905e170fdccb6`  
		Last Modified: Sat, 11 Oct 2025 02:17:39 GMT  
		Size: 13.4 MB (13381225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff306c398b65926f9c6c9812f1b559b49db1eed0342053c01e478331bbc2c53e`  
		Last Modified: Sat, 11 Oct 2025 02:17:38 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a5238e9a4e56575f8d4a966c308279889addcc05c692ff46c573f5d29dc46c`  
		Last Modified: Sat, 22 Nov 2025 22:38:31 GMT  
		Size: 5.7 MB (5717426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:1291c8f33ea7a758855d54395be04883f9810b1b4e945a628370e87e4940bce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.3 KB (632289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2819f15490dce276fab2726d9c4d14b4eb807e5f5dc76397bc1e15845a2f26ed`

```dockerfile
```

-	Layers:
	-	`sha256:acf88bc3e26de5ea0620991271d1d5174fc6973c07f014e366f933cb4a2e3999`  
		Last Modified: Sun, 23 Nov 2025 00:17:52 GMT  
		Size: 622.9 KB (622937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c90ff84c6ffb0d567cbbc9d8c5cfd9cea869236c0cfcca273931e5e82b6c4dd7`  
		Last Modified: Sun, 23 Nov 2025 00:17:53 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.21` - linux; s390x

```console
$ docker pull hylang@sha256:da4210a3f5ff9c7e01c7ef7457b54d87cb30733cd6cc2a010eada3652fbd1168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23444654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569c64e5800bb777a4c093823a74f58e5094d91475d23c40775b0a25edf06973`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 01:19:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Dec 2025 01:19:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 03 Dec 2025 01:19:55 GMT
ENV PYTHON_VERSION=3.14.1
# Wed, 03 Dec 2025 01:19:55 GMT
ENV PYTHON_SHA256=8dfa08b1959d9d15838a1c2dab77dc8d8ff4a553a1ed046dfacbc8095c6d42fc
# Wed, 03 Dec 2025 01:25:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Dec 2025 01:25:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Dec 2025 01:25:05 GMT
CMD ["python3"]
# Wed, 03 Dec 2025 02:10:03 GMT
ENV HY_VERSION=1.1.0
# Wed, 03 Dec 2025 02:10:03 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 03 Dec 2025 02:10:03 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 03 Dec 2025 02:10:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Wed, 08 Oct 2025 16:25:19 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a1949b13cd6d0549261659c0460788901027ab5c94d5e2a0187fb3e3fc911e`  
		Last Modified: Wed, 03 Dec 2025 01:25:24 GMT  
		Size: 457.9 KB (457873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27438edc6fbcba865da11ab9a04bcca8d3782f39eb7ea3351f3daee4ae97c1ca`  
		Last Modified: Wed, 03 Dec 2025 01:25:25 GMT  
		Size: 13.8 MB (13804655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d9c90b5951cd27a96f492e1818b81d8cacdd6eff5a2ab9c4101a551b9002c4`  
		Last Modified: Wed, 03 Dec 2025 01:25:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4206d5be0cc3fb667b678f1bda5b7ef42106d23400ac31d72ab3e77f6d1e9808`  
		Last Modified: Wed, 03 Dec 2025 02:10:27 GMT  
		Size: 5.7 MB (5715445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:753f773f1e077206eafc91365af347fe4ac5da8ba5e9a74c68eb1eec3142ca51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.4 KB (631426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b11fed771dd3e00f91fdc5dd1b0402f561a4287c5901a43d7e9bdff67bf13b`

```dockerfile
```

-	Layers:
	-	`sha256:11e5a9f9436419facd6fae2849fccf61c5ea5e963cc7967d92957e25250f8704`  
		Last Modified: Wed, 03 Dec 2025 03:18:42 GMT  
		Size: 622.1 KB (622142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df06a9a4ba38f9c6ddb4243104c1393f1da881507f24fe1347043c0883abd78a`  
		Last Modified: Wed, 03 Dec 2025 03:18:43 GMT  
		Size: 9.3 KB (9284 bytes)  
		MIME: application/vnd.in-toto+json
