## `hylang:1-alpine3.21`

```console
$ docker pull hylang@sha256:f001ec10fc599e689a8e38af6c79501079dfe388f29528782f5a5ec818ae792a
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

### `hylang:1-alpine3.21` - linux; amd64

```console
$ docker pull hylang@sha256:d28cefbcbb89caec08352b47189567ae4c569546ee61cee850acb49aef23e528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22340025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0a0eba0b1e4fd28e13991be0eebd28583b669687072c9941ccb278adc5d987`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.13.3
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
CMD ["python3"]
# Fri, 30 May 2025 23:29:22 GMT
ENV HY_VERSION=1.1.0
# Fri, 30 May 2025 23:29:22 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 30 May 2025 23:29:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 30 May 2025 23:29:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ce495d870ad5aeb412759e4489eccbc21273ba10edb98a577014cd18253b19`  
		Last Modified: Fri, 09 May 2025 23:46:36 GMT  
		Size: 460.2 KB (460196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a1aa7cc8f77514969eea9c393c8f91f363e54a3aac298c1c35e6b56bb19f12`  
		Last Modified: Fri, 09 May 2025 23:46:36 GMT  
		Size: 12.6 MB (12555215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e8c8c0750e39af85fa6beb079e0cd5832a67f3d764965e689cec29c77ba31a`  
		Last Modified: Fri, 09 May 2025 23:46:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c51abcbdce9171ac464b89179e8899306fb353c24c6cd44c5587a032051d30a`  
		Last Modified: Mon, 02 Jun 2025 17:47:13 GMT  
		Size: 5.7 MB (5682118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:8a90faff3e97c5a5111c98814342d8bd4b9493e9fd6ec4d7fed24baf82130d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.7 KB (641684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5634403cda0fccb50b18f190e285e31c384effdd9a8f1f24a8a274c73ab3232c`

```dockerfile
```

-	Layers:
	-	`sha256:9b0635a5708b09129187cd85fc5af154a6df831934e9f1a5a011bb6ea59217de`  
		Last Modified: Mon, 02 Jun 2025 17:47:13 GMT  
		Size: 632.4 KB (632414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:401039ceff3391c4a4719026eb99fd6feffae5f0e6ea7c5eb3576036c66d9121`  
		Last Modified: Mon, 02 Jun 2025 17:47:13 GMT  
		Size: 9.3 KB (9270 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.21` - linux; arm variant v6

```console
$ docker pull hylang@sha256:44e054a5fb7cd44731aa195ad38d1cafbd7d7aaae931eb1c1e1677c37204f3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 MB (21675030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83526226a920bfe1aac7e64795a7b8f42c650bc89f4cf1591f4556b41bf0858f`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.13.3
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
CMD ["python3"]
# Fri, 30 May 2025 23:29:22 GMT
ENV HY_VERSION=1.1.0
# Fri, 30 May 2025 23:29:22 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 30 May 2025 23:29:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 30 May 2025 23:29:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4fe5d1b18dd307aed3d54fd3454d75bb46ed387a745a0d9d8a94a2e2b1f3ce`  
		Last Modified: Sat, 15 Feb 2025 07:57:45 GMT  
		Size: 459.4 KB (459437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b579fb66e2a6a2e9d0c5b18ad9d8558727409914f4f505b9a3c9752f99f5777`  
		Last Modified: Fri, 09 May 2025 23:59:40 GMT  
		Size: 12.2 MB (12169564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6f9a98eafdd37289ea7c4b18840320a93b07549e4383a5d4962d64a1dd6ac7`  
		Last Modified: Fri, 09 May 2025 23:59:39 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae610da4c96b5d0523b1466215c7cd9473c03d1b053157cf8504712a3228d88`  
		Last Modified: Sat, 10 May 2025 01:00:43 GMT  
		Size: 5.7 MB (5681049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:a084089471882fedfa6acb2bae27ee5f7f5e73fa2c5c1ce20b952c2590548980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4a2e63a7e6c94df0d230be4e5b416787f5fa7d6fe331a05700ffd92e8ee5e7`

```dockerfile
```

-	Layers:
	-	`sha256:9d9c96cfdf1f05388d5654d6a8e8e73c1813d7211bcd3972a9bf4e9e9868d1f0`  
		Last Modified: Mon, 02 Jun 2025 17:58:32 GMT  
		Size: 9.2 KB (9163 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.21` - linux; arm variant v7

```console
$ docker pull hylang@sha256:b49cd17188c571756246a4ae3c0750e83d80b7b6e3dd8af0be2cf761c08056d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21095891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1221d05004b8b632f488ff47642695c0bceb376fa5fbbf16a6d4ca723154755`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.13.3
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
CMD ["python3"]
# Fri, 30 May 2025 23:29:22 GMT
ENV HY_VERSION=1.1.0
# Fri, 30 May 2025 23:29:22 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 30 May 2025 23:29:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 30 May 2025 23:29:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ecc85683812d0585b9ad9a25a17e496c376367d442aade30005099b80d8495`  
		Last Modified: Fri, 09 May 2025 02:30:16 GMT  
		Size: 460.2 KB (460203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506dea0fe4a3652936aca4aa9fc85e52bb99281167dbb941e79cd67cdf7d3efd`  
		Last Modified: Sat, 10 May 2025 03:23:36 GMT  
		Size: 11.9 MB (11854726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bb57e78f9e6f5bb73cb08d62057a237fdc4a6bd1d4d8bd71140f82a6623874`  
		Last Modified: Sat, 10 May 2025 03:23:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21310e98e298a1157ac4ceee81ad410828bd9c27c752ae8e1825c16d9f30f5c3`  
		Last Modified: Fri, 30 May 2025 18:03:56 GMT  
		Size: 5.7 MB (5682593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:aa5fa4585eb013355b2a1646a6dd5ed1c263e845ff2d638a3d039acc3fd3caf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.9 KB (644850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de21ee7857d6012b5878b8b5558240f02f499477661a5b4e431e99a3963a2bfd`

```dockerfile
```

-	Layers:
	-	`sha256:30ab59165d464fcf9cf5a1520ca088c0f643b0aeb6babe1a55559b5e29581a1d`  
		Last Modified: Mon, 02 Jun 2025 18:08:18 GMT  
		Size: 635.5 KB (635472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4485d35c1e70edb38431467b9a1d5bab0151264caa1b91c7cb902e651875e601`  
		Last Modified: Mon, 02 Jun 2025 18:08:18 GMT  
		Size: 9.4 KB (9378 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:90f73fe1d094a71d924a508592f95ed317f4e5c18b0711574e4abd0533a26ab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22710870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d4bab7515999dff9b596301b756d36dfc7c68cd8046ed6a8d28424e60cdde4`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.13.3
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
CMD ["python3"]
# Fri, 30 May 2025 23:29:22 GMT
ENV HY_VERSION=1.1.0
# Fri, 30 May 2025 23:29:22 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 30 May 2025 23:29:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 30 May 2025 23:29:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd04ed000f543fe0ebfb48e4ae3e8b61f32da8fce708f53358e4b17a8b443aa`  
		Last Modified: Thu, 08 May 2025 22:00:52 GMT  
		Size: 462.1 KB (462084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1523497d2ae8957f7959baf05c1e9073ad839a1fec0b6a5c7b5dab5714f6b4`  
		Last Modified: Sat, 10 May 2025 01:40:20 GMT  
		Size: 12.6 MB (12573065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e61d3b32586cc2f96d667d85ea804f8a911ff06f5fccbf77723e29a24327a14`  
		Last Modified: Sat, 10 May 2025 01:40:19 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ae81edfbd26c396f22e80bf9e814a76d1a8f132d63799f9b821d6d7750a258`  
		Last Modified: Fri, 30 May 2025 18:03:32 GMT  
		Size: 5.7 MB (5682442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:b3beb318072c7585814ee2bc17c0a9e2f4278813d37720c12d613164361e3e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.9 KB (641940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6806c412915b85e2215683390dcb5a954578107a67679174c3203493fcc1516c`

```dockerfile
```

-	Layers:
	-	`sha256:bb2d9c5d29f77d4da6e48e322f1603f5692036b3c850bfab8b3c7883f6b26000`  
		Last Modified: Mon, 02 Jun 2025 19:53:14 GMT  
		Size: 632.5 KB (632518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1162cd9baab357038afbfb26d152f14def00670392a4e505168d7e598a23bb44`  
		Last Modified: Mon, 02 Jun 2025 19:53:14 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.21` - linux; 386

```console
$ docker pull hylang@sha256:629f9ddc863392d8ac5dd62dcc03dea0ba00848fa8a05381461a6e3fc00b0bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.4 MB (22415717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585e3d5abd832df9d86bb6fd6138eb71c4a8ff5da105d7d231c9d4bf364c9418`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.13.3
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
CMD ["python3"]
# Fri, 30 May 2025 23:29:22 GMT
ENV HY_VERSION=1.1.0
# Fri, 30 May 2025 23:29:22 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 30 May 2025 23:29:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 30 May 2025 23:29:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a25f20c99820126b5d2e14a34bbf9734543fa1f7e205c0403a3bd4da9c88dc9`  
		Last Modified: Fri, 09 May 2025 23:47:29 GMT  
		Size: 460.6 KB (460631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163ca479eab9e15cf61286da5806468be44ddd1ac250259036e4ae00fa63e398`  
		Last Modified: Fri, 09 May 2025 23:47:29 GMT  
		Size: 12.8 MB (12808988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17735d3713d53d8fc01822499195f57020c7d5efe99e6c0442c0e7a2302d3882`  
		Last Modified: Fri, 09 May 2025 23:47:29 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131f7965f3f8f215932ad2165ed6b799edd4033112459d2c460e24c42f644a0a`  
		Last Modified: Mon, 02 Jun 2025 17:48:20 GMT  
		Size: 5.7 MB (5682227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:b10a978b0c6baa93949c553de9c07b140e5cfb93903a72de743e78abae83e737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 KB (641586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926b6cf9e91c6232f37f83ffef07372e598da95d97a19ace1300279657ace626`

```dockerfile
```

-	Layers:
	-	`sha256:9707e71cb7aa2800b54de6724cc3397dbc5af6b062674bca93a08aa2a1fd7822`  
		Last Modified: Mon, 02 Jun 2025 17:48:20 GMT  
		Size: 632.4 KB (632369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7dc2c72a4e3a508cf2b021c729ce43a8408e9440012ca466642b85cd537ce6c`  
		Last Modified: Mon, 02 Jun 2025 17:48:20 GMT  
		Size: 9.2 KB (9217 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.21` - linux; ppc64le

```console
$ docker pull hylang@sha256:578cc1a44175becd75d8b9a01399a9dbec84a409cde888a1eb65cdf02f8dfcaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (22999310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7f800fd4b5f010b87b7ded1faae4ef69439913e879f1a8fd7e5596d06c904e`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.13.3
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
CMD ["python3"]
# Fri, 30 May 2025 23:29:22 GMT
ENV HY_VERSION=1.1.0
# Fri, 30 May 2025 23:29:22 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 30 May 2025 23:29:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 30 May 2025 23:29:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2a209ef4b40c4d2cca337e07efac631483c4d7b6386c631a08daa122ab2c07`  
		Last Modified: Thu, 08 May 2025 21:42:31 GMT  
		Size: 462.6 KB (462564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af8173e27cd526a9e585ddf4baaa7fce5b9daec4e461dd258147fd947d15167`  
		Last Modified: Sat, 10 May 2025 01:07:36 GMT  
		Size: 13.3 MB (13279802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5a3f4d96bd9e37bfb71652d1690f44358a4985aabda6608b89f81128ffbedc`  
		Last Modified: Sat, 10 May 2025 01:07:35 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0833fb443cbc448137ed53c54f27f2c20d1fa1e6084892cf8e9b15e726fa1b4b`  
		Last Modified: Fri, 30 May 2025 18:02:57 GMT  
		Size: 5.7 MB (5682349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:b37b98e937024ec3731f748f3c9a168afc4a9473a17d80f42fba67f6e6adad8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.9 KB (639859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0eb821eefb68c277326dfa1921a563f2aff03cc078a6169ca3d86951f67c85`

```dockerfile
```

-	Layers:
	-	`sha256:3c3fa19074ee7757312f175675f44036c9f85fe2d7991d4d0f0b385717da8f95`  
		Last Modified: Mon, 02 Jun 2025 19:43:59 GMT  
		Size: 630.5 KB (630521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:119c9b0fcd7e7451205afeec75afc2bc6d9c4a802f337f7afaf3055741fc0126`  
		Last Modified: Mon, 02 Jun 2025 19:43:58 GMT  
		Size: 9.3 KB (9338 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.21` - linux; riscv64

```console
$ docker pull hylang@sha256:3c5e6fedca7b8459cff0219c1ab31957fbfb03d4941034940b0458ffca683461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22121010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51203cce36980f29201b58463b00a17800a752a2b83fa5e20c4062a917db7a4`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.13.3
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
CMD ["python3"]
# Fri, 30 May 2025 23:29:22 GMT
ENV HY_VERSION=1.1.0
# Fri, 30 May 2025 23:29:22 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 30 May 2025 23:29:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 30 May 2025 23:29:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdd0fd69c6a32066ab97e740dd2a3c694b5914634fa4558c362a817bc0be197`  
		Last Modified: Sat, 10 May 2025 04:02:08 GMT  
		Size: 460.5 KB (460536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78b73007713a9135cdb9d07d2a164fbe724b00fd2c4c11eb202db49078302e2`  
		Last Modified: Sat, 10 May 2025 05:17:39 GMT  
		Size: 12.6 MB (12625504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9452e8261d8146655e3b2baa89405781d6fe5b7dd2aa072a82fd9a9260ff934`  
		Last Modified: Sat, 10 May 2025 05:17:37 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87d1111fe17cc9342e8e083df026b609f8c23a5356359288fbfd305b3832ea7`  
		Last Modified: Fri, 30 May 2025 18:07:12 GMT  
		Size: 5.7 MB (5683280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:e97f17b8c712f7c5f241f8e615a415cb0481b84471d19223bb24d981f98300fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.9 KB (639855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6682f1e6f92417daadbc7da25636998b789fa8ba90c65f2634093647d330efe3`

```dockerfile
```

-	Layers:
	-	`sha256:f513de53e0be401c0f275d60ecd1735785b8b83ae432cdb5b743078356a478c0`  
		Last Modified: Tue, 03 Jun 2025 01:44:01 GMT  
		Size: 630.5 KB (630517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7775da9adfe47bad16d71afbb9dbe8e287bdd412cbc26fe3a647f61f238cb1be`  
		Last Modified: Tue, 03 Jun 2025 01:44:00 GMT  
		Size: 9.3 KB (9338 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.21` - linux; s390x

```console
$ docker pull hylang@sha256:6f3f4b93bb4057c62fde0241ed5a47384a7187be22aeec0acacb1491035a2b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22630846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa3f5252289008b63fdfcc8507f64fe5bbd078585f793d3907f119ac2dfc9ca`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.13.3
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
CMD ["python3"]
# Fri, 30 May 2025 23:29:22 GMT
ENV HY_VERSION=1.1.0
# Fri, 30 May 2025 23:29:22 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 30 May 2025 23:29:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 30 May 2025 23:29:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49aa20b448d7b4eb02fc23dd7c98263e303ee064ea08d34aa98637446940c90`  
		Last Modified: Sat, 10 May 2025 00:38:39 GMT  
		Size: 461.2 KB (461151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6b0464d5a03f1c265048e8ccaf202deefa86858d5ff448045d0776d27d4b9b`  
		Last Modified: Sat, 10 May 2025 00:38:39 GMT  
		Size: 13.0 MB (13019647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd070869b8c50bd815c4054c63a6d32f682332e7273602b969b0aaea6b2dee9`  
		Last Modified: Sat, 10 May 2025 00:38:39 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce26be70ff49999cfb215ac7bb7bf2bbae35dcfb1bddeb19d89e5c25fe897dba`  
		Last Modified: Fri, 30 May 2025 18:03:45 GMT  
		Size: 5.7 MB (5682234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:b6fb9f795123c10e8313b445c1f3215efe75f93a7aaaec4b0ffa06e863eebead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.7 KB (639733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2af699f0ea0724b39a61a52931d82fd6431e1f3e9a1d6253bb471bc61dcac7c`

```dockerfile
```

-	Layers:
	-	`sha256:43ccfc246efe667275678fdc8cb4be57e6123ae34d09c46d2954b9872e6866f5`  
		Last Modified: Mon, 02 Jun 2025 19:13:33 GMT  
		Size: 630.5 KB (630463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cb9a080846d2819e7b9c2ce3005154d12f3f260fbdb6794a4663f25b2c7cde1`  
		Last Modified: Mon, 02 Jun 2025 19:13:33 GMT  
		Size: 9.3 KB (9270 bytes)  
		MIME: application/vnd.in-toto+json
