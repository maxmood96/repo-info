## `hylang:python3.14-rc-alpine3.21`

```console
$ docker pull hylang@sha256:749de7bae4c791a29415ffba867dfed086cb1269664fb57a9cac0d7d2340afd4
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
	-	linux; riscv64
	-	unknown; unknown

### `hylang:python3.14-rc-alpine3.21` - linux; amd64

```console
$ docker pull hylang@sha256:e0e3b6979b6e0ef7ec74eda3335d91907b83d8fa903e51ae26c799568b1c4134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22925824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a0f726f4ee3734cc947236e4d4b0113ef5586f38344e7dbbc873de465d3465`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_VERSION=3.14.0b3
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_SHA256=c6f48bf51f01f50d87007a445dd7afe4a4c7a87ab482570be924c1ddfd0d3682
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedcd48ace0804819c54a9f53229322566ad132e9cf77d26187da7d8e1e25e49`  
		Last Modified: Wed, 18 Jun 2025 16:41:38 GMT  
		Size: 460.2 KB (460211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af33837790512108af6ea5936d90f82076f7061f33dc11c77dbf041b29d803e0`  
		Last Modified: Wed, 18 Jun 2025 16:41:41 GMT  
		Size: 13.0 MB (12966342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb04fe98265ea08e06e79d77d31426202300ce6f07db52520980ae3a365645e9`  
		Last Modified: Wed, 18 Jun 2025 16:41:39 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e32d9b65d7672c19a5183c5f68229900b2edffdf24bc3076e67c84e0472383b`  
		Last Modified: Wed, 18 Jun 2025 17:08:39 GMT  
		Size: 5.9 MB (5856775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:9dc07c62160ebacb83b7fd50d7a19494d6604c074ddf96d9d863e8b9b9733340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.5 KB (630510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec1d3dda8c6bcbc7e8f14816b242b62def526f2e9fd1b15ab6c9b4e9e0e194e`

```dockerfile
```

-	Layers:
	-	`sha256:d1eea1c2fe9e1d136cce4154d8fa06dcbd62833e0bb5f3e5e0247c5f2f3843b6`  
		Last Modified: Wed, 18 Jun 2025 20:19:13 GMT  
		Size: 622.5 KB (622500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4af3df8c56047e01073615df6fba52dfc8a953e47d1c46d91ee4bbc2a4e0b73`  
		Last Modified: Wed, 18 Jun 2025 20:19:14 GMT  
		Size: 8.0 KB (8010 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-alpine3.21` - linux; arm variant v6

```console
$ docker pull hylang@sha256:becfaa2029596e33981a36651adf529cf518178fd4af0eeb11fa47bb8b4459ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22256662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7e4a9093a27eb812e134de47dd0bb2cd0516d4ded263b63bf4956a5cdc7307`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_VERSION=3.14.0b3
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_SHA256=c6f48bf51f01f50d87007a445dd7afe4a4c7a87ab482570be924c1ddfd0d3682
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4fe5d1b18dd307aed3d54fd3454d75bb46ed387a745a0d9d8a94a2e2b1f3ce`  
		Last Modified: Sat, 15 Feb 2025 10:06:38 GMT  
		Size: 459.4 KB (459437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec55cf2080fbc8e734dc9b043df0cc5549205ba14276a0b5075d1cc54668864`  
		Last Modified: Wed, 18 Jun 2025 18:09:47 GMT  
		Size: 12.6 MB (12575248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5b1432c5b31f678451e9808e6ae9ffd9f81a82588244799e42bbff7fd64ebb`  
		Last Modified: Wed, 18 Jun 2025 16:53:25 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c6b4ea688cd83864fe40a02b90b6c88cbcab4a8cda8b233216d9629e8d1bbb`  
		Last Modified: Wed, 18 Jun 2025 20:20:06 GMT  
		Size: 5.9 MB (5856992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:932390d39def910e28a6f7dd80220daf2ab576b5bc0614cf317824b4f66f8309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f72cbdb3c042fcc0511aba034eae2cb14c980ada5b06b14cca5b40129cae3ff`

```dockerfile
```

-	Layers:
	-	`sha256:e4c8f96a96546b12385ddbc1d5d9d3aa9886581eeea3ed91027ba653b8a95828`  
		Last Modified: Wed, 18 Jun 2025 20:19:18 GMT  
		Size: 7.9 KB (7871 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-alpine3.21` - linux; arm variant v7

```console
$ docker pull hylang@sha256:c282d874e7b8e00192f3b370d4c60566b89bad95d28680ac9089cec5eafd61f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21640183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7cdb6fc23651d21d8140cbf2174ef0e22fed046a95ec2411ebda71a0e29d4c`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_VERSION=3.14.0b3
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_SHA256=c6f48bf51f01f50d87007a445dd7afe4a4c7a87ab482570be924c1ddfd0d3682
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ecc85683812d0585b9ad9a25a17e496c376367d442aade30005099b80d8495`  
		Last Modified: Fri, 09 May 2025 02:30:45 GMT  
		Size: 460.2 KB (460203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee74158dae7b3fa05daf7dd3a00aadd23f250152638f2b199f97ca9e6531cd28`  
		Last Modified: Wed, 18 Jun 2025 20:20:08 GMT  
		Size: 12.2 MB (12224866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75530237de6ac95eb4dab89c487f0b8b12722fb083bec593d28c6f3394ce3bd`  
		Last Modified: Wed, 18 Jun 2025 20:20:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787154d42b55fba03f9db2e5d7696a986dc790a628d68ddfdb38210c763b7bb1`  
		Last Modified: Wed, 18 Jun 2025 19:08:55 GMT  
		Size: 5.9 MB (5856742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:bdda34dd5db858a808cdacea839fe8a2805e918c82d77bd4fe97d604db490f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.6 KB (633612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d6d95f3a9a14c2d4b4acf3fc96e464949bba4ca9d1f20675782256fae6a537`

```dockerfile
```

-	Layers:
	-	`sha256:2b2932d7876e1d3e2d7ac47119fa147324c947733fbf5d89f24d5bb1616d21b1`  
		Last Modified: Wed, 18 Jun 2025 20:19:27 GMT  
		Size: 625.5 KB (625526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9154dc461960d01c979e92ab29cfe5e981ee0c1b097b0fc219591f95ba8ebeb`  
		Last Modified: Wed, 18 Jun 2025 20:19:28 GMT  
		Size: 8.1 KB (8086 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:98a56cd02c5abc0befd4c43b66a3e473e7913192ea73d1fb7181858b2f500dac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23269994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08248955537eae83ca0564f62c7f3913698695e02774ccff6d03177c1ff7322f`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_VERSION=3.14.0b3
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_SHA256=c6f48bf51f01f50d87007a445dd7afe4a4c7a87ab482570be924c1ddfd0d3682
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b28441aad6a5ce614544be397191306e05569c156d01bbd230edeb43a5c9a1`  
		Last Modified: Fri, 13 Jun 2025 01:48:40 GMT  
		Size: 462.1 KB (462077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406ed888af90a0fb82dcd03ae449752614abf2987cb040e06fc79029c3d5ce46`  
		Last Modified: Wed, 18 Jun 2025 18:12:43 GMT  
		Size: 13.0 MB (12957779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa8e37f97c28599753439b3baa2272b1ed0bbf1d89ff3f8fa08f06db84e4062`  
		Last Modified: Wed, 18 Jun 2025 17:45:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e816869bd852f484ed66b844e6ff484d7ebb7941f48d43e71e4d3e2307a056b9`  
		Last Modified: Wed, 18 Jun 2025 18:09:41 GMT  
		Size: 5.9 MB (5856861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:ff89c91b342864b62e85e3cfeb10e5852d2b1d69a76e88219c79f3a77361ac51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.7 KB (630670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8254e02e9b4a0ad75953d3e2370fc77244a969c33b45c155162cb4d9e5af802e`

```dockerfile
```

-	Layers:
	-	`sha256:6dd136ffe84c4c25a00124e8bc616bebf75273ca67bb731247bfbf826150026e`  
		Last Modified: Wed, 18 Jun 2025 20:19:32 GMT  
		Size: 622.6 KB (622556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6fc2c4e4f238d0492215dfa567a791da828eade128ca6b68c506bb27b1cef3c`  
		Last Modified: Wed, 18 Jun 2025 20:19:33 GMT  
		Size: 8.1 KB (8114 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-alpine3.21` - linux; 386

```console
$ docker pull hylang@sha256:f6446b4852554f4c84f01196de82efd44905e060ecc78797e7355a689eb3ed77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23027200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d1f1b25c80eb22b47ad1cd7d4ae72920d18b2f97075a390fa2f9c30dd26481d`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_VERSION=3.14.0b3
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_SHA256=c6f48bf51f01f50d87007a445dd7afe4a4c7a87ab482570be924c1ddfd0d3682
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642817bb8a5616c3744bf92bcb84ee3cf674b0b2ecb97b5905b25bce8f180441`  
		Last Modified: Wed, 18 Jun 2025 16:42:01 GMT  
		Size: 460.6 KB (460627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d3cfc8d0352dccd166edd12053386992a22c359582f314d474758056e75407`  
		Last Modified: Wed, 18 Jun 2025 16:42:04 GMT  
		Size: 13.2 MB (13245787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c14b320825efb99f42d7410c2b0151d7718d79877ee688953458a82ca4fa734`  
		Last Modified: Wed, 18 Jun 2025 16:42:02 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e131d210f868c6004793c48705933f762e4e65b4164b554cc6d489be50e84e`  
		Last Modified: Wed, 18 Jun 2025 17:08:05 GMT  
		Size: 5.9 MB (5856915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:0bff6a8b1650a2bb2d3b79346a2b8e2215ecddb95a94ff17b25b45b623500f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.5 KB (630453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820b2f6da16a030fdb2b9c10b89ba6c059c7a14042a430e67cb62f220b258f37`

```dockerfile
```

-	Layers:
	-	`sha256:2a8925a4bd2f9028344d849b35e90af3b4c98d61a8d3e6a784b7d077e5a6eebd`  
		Last Modified: Wed, 18 Jun 2025 20:19:36 GMT  
		Size: 622.5 KB (622475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c41fdd32820ec47aff562e9fc31badaba7bb4f72a6f9377312d12ee5303602e3`  
		Last Modified: Wed, 18 Jun 2025 20:19:37 GMT  
		Size: 8.0 KB (7978 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-alpine3.21` - linux; ppc64le

```console
$ docker pull hylang@sha256:1485ebb9ca058c9d342154af9de4be8d823691e77b98b38f86a743e6d5043d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23609654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de090ac19ed1c134e0bf9425679cf2c12d105ae82be131df15a92fb9d47be9ed`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_VERSION=3.14.0b3
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_SHA256=c6f48bf51f01f50d87007a445dd7afe4a4c7a87ab482570be924c1ddfd0d3682
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2a209ef4b40c4d2cca337e07efac631483c4d7b6386c631a08daa122ab2c07`  
		Last Modified: Thu, 08 May 2025 21:42:59 GMT  
		Size: 462.6 KB (462564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da7b2572346c26c886385ee7cc5a64c78acc9b189bfebf98712b287d68c3a2c`  
		Last Modified: Wed, 18 Jun 2025 18:20:06 GMT  
		Size: 13.7 MB (13715308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e013547698e6c965fd1d477fe57d7e48b477dab42963910d468d20c199c3e27`  
		Last Modified: Wed, 18 Jun 2025 18:19:52 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111898777654bddc0c103d00ab5b0bc1b0e27aca4cbd67aea30d65fb1db172e`  
		Last Modified: Wed, 18 Jun 2025 18:11:42 GMT  
		Size: 5.9 MB (5857187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:7c926747205da08081990f9d620ca1bcded7c8c0aa2ec399021547648d6bfe46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.6 KB (628637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5984fe75dfd602aafc21013a5ffc02825769b7b002bd003e4e03f86e2de57312`

```dockerfile
```

-	Layers:
	-	`sha256:25263cfaacca4c723c2679b00b24489e2cd342832b9a391d0d733602cc326e82`  
		Last Modified: Wed, 18 Jun 2025 20:19:47 GMT  
		Size: 620.6 KB (620583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d31c60b6ed249366d5821cc7c29357ed0ac0ccfe3cc8465f35b650ebfd4951a6`  
		Last Modified: Wed, 18 Jun 2025 20:19:48 GMT  
		Size: 8.1 KB (8054 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-alpine3.21` - linux; riscv64

```console
$ docker pull hylang@sha256:25cacbb9d31c64afb1db10a21783373983081d6f5dcf80e194a98a79adaeb537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22730253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8caf7ca805d20ab909bc883d5e429a7a7136c5a4851c4386054a8b962e8154fe`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_VERSION=3.14.0b3
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_SHA256=c6f48bf51f01f50d87007a445dd7afe4a4c7a87ab482570be924c1ddfd0d3682
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdd0fd69c6a32066ab97e740dd2a3c694b5914634fa4558c362a817bc0be197`  
		Last Modified: Fri, 16 May 2025 17:38:44 GMT  
		Size: 460.5 KB (460536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5bb8d88d25ab62e51fc406ee15e625f15df25575556c11f3054edb2820b0fe`  
		Last Modified: Wed, 18 Jun 2025 17:55:18 GMT  
		Size: 13.1 MB (13060472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca90e305371438ac4d0140451af82a5545c1b00d3f5b1c7e2e7e3e7c9227df3d`  
		Last Modified: Wed, 18 Jun 2025 17:55:16 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15b65c26445c9bae236ca288e2306397821d35c98bdb015854911e0015c88aa`  
		Last Modified: Wed, 18 Jun 2025 18:21:18 GMT  
		Size: 5.9 MB (5857555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:2daaba209ab7ba70dcd0d66c4585b923d8c15902af97ce8189645e36afff00c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.6 KB (628632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0db6a788045c917cd4eebc5a3ab662c98e1f536c464f972e11509db95d45eb`

```dockerfile
```

-	Layers:
	-	`sha256:575922f80351e2e04f7c9c52ee6317ec134d1d850835f060c22b7a708ffa362e`  
		Last Modified: Wed, 18 Jun 2025 20:19:52 GMT  
		Size: 620.6 KB (620579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb77c56c16fb13381ca245da71a8b4a3376457ab14a4d7f7bc9192253862cfcb`  
		Last Modified: Wed, 18 Jun 2025 20:19:52 GMT  
		Size: 8.1 KB (8053 bytes)  
		MIME: application/vnd.in-toto+json
