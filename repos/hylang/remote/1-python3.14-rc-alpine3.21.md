## `hylang:1-python3.14-rc-alpine3.21`

```console
$ docker pull hylang@sha256:4260619ff4441ad39e69e3013cf079f848a8161b187585f5cc8814f5f763708c
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

### `hylang:1-python3.14-rc-alpine3.21` - linux; amd64

```console
$ docker pull hylang@sha256:8177dbe70ac4b51edb94dec210f2f781f9cc1c2207ec6c1d0f8c42947065ea5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22890891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc5b3749c09b0d586774c49b85568b4ad6f41d85f84a417a2d675405fe0c0e8`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 26 May 2025 21:49:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 21:49:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 26 May 2025 21:49:30 GMT
ENV PYTHON_VERSION=3.14.0b2
# Mon, 26 May 2025 21:49:30 GMT
ENV PYTHON_SHA256=7ac9e84844bbc0a5a8f1f79a37a68b3b8caf2a58b4aa5999c49227cb36e70ea6
# Mon, 26 May 2025 21:49:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 26 May 2025 21:49:30 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 26 May 2025 21:49:30 GMT
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
	-	`sha256:262a1b1b1a13aa8d79b1f61781ed4cb795b4abd732222a4f5eb99d646a529318`  
		Last Modified: Tue, 27 May 2025 19:07:41 GMT  
		Size: 460.2 KB (460206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed9633d6fb2b323c1541026239defe3cc245441ba7b77010162da75591ff1f5`  
		Last Modified: Tue, 27 May 2025 19:07:42 GMT  
		Size: 12.9 MB (12934814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485953a595c7ce3147d61d705cf93b0a1dbfe3391a3bd015ebc9891461197cac`  
		Last Modified: Tue, 27 May 2025 19:07:41 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebabdbaf3854ace5a84ca72af72f36aac3d0ca3c8232530477c51f37f9b6e29d`  
		Last Modified: Mon, 02 Jun 2025 17:47:20 GMT  
		Size: 5.9 MB (5853375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:6ac56ea2a011253914f96dfafc68d157f47c700fdaaf1f12f42c4ea64a22a178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 KB (639204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b682d79dde586ebfcda4b826cc04099ece8d7966bc425c0c5b1942bdd911b1`

```dockerfile
```

-	Layers:
	-	`sha256:754ac3461252fb398c05a78b0f4fe328d7d3caadb25771a152f3cc4262a167d6`  
		Last Modified: Mon, 02 Jun 2025 17:47:20 GMT  
		Size: 631.2 KB (631194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58cc424b67c4c6400c2e96e5e41eaade3158d1cf03c761a241e8f9337af8af5a`  
		Last Modified: Mon, 02 Jun 2025 17:47:20 GMT  
		Size: 8.0 KB (8010 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-alpine3.21` - linux; arm variant v6

```console
$ docker pull hylang@sha256:232721c9cee7f57d0e17cbeeb4183c586146e6d6d35755cfbdd9ecd245027e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.2 MB (22216704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa850562e3a2255de4291426342d2b11841fc412902d3b3c756a2fa1bb04da27`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 26 May 2025 21:49:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 21:49:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 26 May 2025 21:49:30 GMT
ENV PYTHON_VERSION=3.14.0b2
# Mon, 26 May 2025 21:49:30 GMT
ENV PYTHON_SHA256=7ac9e84844bbc0a5a8f1f79a37a68b3b8caf2a58b4aa5999c49227cb36e70ea6
# Mon, 26 May 2025 21:49:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 26 May 2025 21:49:30 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 26 May 2025 21:49:30 GMT
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
	-	`sha256:8d778ddefd098ea1f8d8d85528e328cda8004a1941ff540a98078928a7e139fe`  
		Last Modified: Tue, 27 May 2025 19:13:04 GMT  
		Size: 12.5 MB (12538911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09de32b07ca9837323ee46056c2706db5e30d7f482fce2b30641160038479d31`  
		Last Modified: Tue, 27 May 2025 19:13:03 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0318ed2ceac2c56ddf1eadb1b829228bf5dd4ac20ddd44916ef19bd12bfa1c39`  
		Last Modified: Tue, 27 May 2025 20:08:39 GMT  
		Size: 5.9 MB (5853378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:8cb166c5ef3b7ed1a52c59572e757e36960f55c2b3b381e333800887a800ea0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bd8e0966377404c2b3de8bc204f47aa9a5055b763ee6f7c89d0ac4eea1f8dd`

```dockerfile
```

-	Layers:
	-	`sha256:acd3e39bc1acfe51f9990c7e8a861788a9489098cd7522300eadcf1bca6fb067`  
		Last Modified: Mon, 02 Jun 2025 18:02:05 GMT  
		Size: 7.9 KB (7871 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-alpine3.21` - linux; arm variant v7

```console
$ docker pull hylang@sha256:f2588e7cb9927057e42752f10ad68b230f8438f86764c0f4692107ff6c7731a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21607660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f69e2f9017f91882774089570824dc09ad5d884863a1bd987d49f9f322a3651`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 26 May 2025 21:49:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 21:49:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 26 May 2025 21:49:30 GMT
ENV PYTHON_VERSION=3.14.0b2
# Mon, 26 May 2025 21:49:30 GMT
ENV PYTHON_SHA256=7ac9e84844bbc0a5a8f1f79a37a68b3b8caf2a58b4aa5999c49227cb36e70ea6
# Mon, 26 May 2025 21:49:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 26 May 2025 21:49:30 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 26 May 2025 21:49:30 GMT
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
	-	`sha256:250da117450e8b1b6545d67ea6560ce7614013e97ff7d04d64a887d8229dd677`  
		Last Modified: Tue, 27 May 2025 20:50:44 GMT  
		Size: 12.2 MB (12195851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144e21448db202b61fac106d161e4f8c1c6be05d588a575f7e74091bbe265aa9`  
		Last Modified: Tue, 27 May 2025 20:50:44 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdd2b584d5e032a43537a31a66e01d04c52c08270dd46e7d0235871e70c8cfa`  
		Last Modified: Tue, 27 May 2025 21:13:53 GMT  
		Size: 5.9 MB (5853235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:7747f3f4dda68052dc5f8d9e8a050a7fcfff399788266ee8521ca067bb2de7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.3 KB (642306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305c5eb1497f8048ecc8a82d06ceeb135b7b3f1fb627e8bc93fb6db1c5135260`

```dockerfile
```

-	Layers:
	-	`sha256:a4575324b5771af691ec1dab921c6d35143777060360a8a913ad55578dee783a`  
		Last Modified: Mon, 02 Jun 2025 18:15:05 GMT  
		Size: 634.2 KB (634220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b46486a8f2a72dd69459e81a29d53ea891aa1b4fcf80af0d5db762fedca0173`  
		Last Modified: Mon, 02 Jun 2025 18:15:05 GMT  
		Size: 8.1 KB (8086 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:7ad53adb1de8cb550330fa403bc291c2fa4a57832f6965fe323f83fc134c59af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23233917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a4c46fa782f405a5aef74f04463486287e8b2a8bd289a60c4e2adbe9e0d9a9`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 26 May 2025 21:49:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 21:49:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 26 May 2025 21:49:30 GMT
ENV PYTHON_VERSION=3.14.0b2
# Mon, 26 May 2025 21:49:30 GMT
ENV PYTHON_SHA256=7ac9e84844bbc0a5a8f1f79a37a68b3b8caf2a58b4aa5999c49227cb36e70ea6
# Mon, 26 May 2025 21:49:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 26 May 2025 21:49:30 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 26 May 2025 21:49:30 GMT
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
	-	`sha256:aedf05ed5a71c5dad02946b12111f31433d8c5d11ee3e641c35e12e183f1aac0`  
		Last Modified: Tue, 27 May 2025 21:05:59 GMT  
		Size: 462.1 KB (462075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba73bd3b92ffc5a82dd5f16cef8c3a331f722a5aa1c4a1d2092c9893409005e`  
		Last Modified: Tue, 27 May 2025 21:05:59 GMT  
		Size: 12.9 MB (12925371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359a9ee2f260d153f1f2576be194e0b19bb2006b177d9699b705f5ef95d13281`  
		Last Modified: Tue, 27 May 2025 21:05:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcddf191c683321cd473b6fea61176ebc1064d600e2ec6ec796213dc92994a70`  
		Last Modified: Tue, 27 May 2025 21:58:16 GMT  
		Size: 5.9 MB (5853195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:207d7837da37aee0d84f232e6dbb0cf45306addbc73c03fdb388fab483b1648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.4 KB (639364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5354cc3c663e98c460004c89ed425acccfabf980d10305231a5538f740ba1cb2`

```dockerfile
```

-	Layers:
	-	`sha256:d5f8d533b528fe70b334edfd0a1ca5d64696770d0078247c5a344e3cae07efc0`  
		Last Modified: Mon, 02 Jun 2025 19:59:22 GMT  
		Size: 631.2 KB (631250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:961b126be974605cff46d51883fe3b78bb927fc95bf2d0e926b07925b7d9ed27`  
		Last Modified: Mon, 02 Jun 2025 19:59:22 GMT  
		Size: 8.1 KB (8114 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-alpine3.21` - linux; 386

```console
$ docker pull hylang@sha256:6d2c29cd895bb01e9fec960cc11329b10b9e259937c4d21bb9ee4da55d2515ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (22989875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508d2734598e09fb2af663dbd4ae893c88c493ce515a5b7d9c671c8ffe8b7865`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 26 May 2025 21:49:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 21:49:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 26 May 2025 21:49:30 GMT
ENV PYTHON_VERSION=3.14.0b2
# Mon, 26 May 2025 21:49:30 GMT
ENV PYTHON_SHA256=7ac9e84844bbc0a5a8f1f79a37a68b3b8caf2a58b4aa5999c49227cb36e70ea6
# Mon, 26 May 2025 21:49:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 26 May 2025 21:49:30 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 26 May 2025 21:49:30 GMT
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
	-	`sha256:92ade42d1d4d0a70a2108e94e62e3c004281c8091403bdd6d4acc49162c9c7a0`  
		Last Modified: Tue, 27 May 2025 19:07:43 GMT  
		Size: 460.6 KB (460627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38b5c6bf1bfee843603166da6001e48d347083c043fb86999ac959e477cc9fa`  
		Last Modified: Tue, 27 May 2025 19:07:43 GMT  
		Size: 13.2 MB (13211881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb28c04f2dd200260bff97d10332769f84d5419ad14ad2a5dfff937746372e4`  
		Last Modified: Tue, 27 May 2025 19:07:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2095fd7f2c0815f94b581a94a865deeefa487e65a5fb8ab619b950f41c08e80`  
		Last Modified: Mon, 02 Jun 2025 17:47:14 GMT  
		Size: 5.9 MB (5853496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:fbe78338e1e8b0520bf4c5a87ee4575989823c7fd62d17fe3a212c5b7e7c1b49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.1 KB (639147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019be4acb6ea136bcba0aa188bdd1183bc39b5373f61073a08a2fb511dc2d071`

```dockerfile
```

-	Layers:
	-	`sha256:ff7d20e19e80af124f3233fc311a32c9c451536fa381969dd481fbaaaf6c376f`  
		Last Modified: Mon, 02 Jun 2025 17:47:14 GMT  
		Size: 631.2 KB (631169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cbb45c44b19a7b783f6b3d14a200b7bb5f2ce5624aca9acf6a307fcb665d98b`  
		Last Modified: Mon, 02 Jun 2025 17:47:14 GMT  
		Size: 8.0 KB (7978 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-alpine3.21` - linux; ppc64le

```console
$ docker pull hylang@sha256:9e3b7542fa1a92fc55cc21b111d8fe839eaf10a483f151e7cc5c35d12577089c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23573161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d63751f4bf509818207e7b749750669cd8b1863640497eeb3c241c527fbd5e`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 26 May 2025 21:49:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 21:49:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 26 May 2025 21:49:30 GMT
ENV PYTHON_VERSION=3.14.0b2
# Mon, 26 May 2025 21:49:30 GMT
ENV PYTHON_SHA256=7ac9e84844bbc0a5a8f1f79a37a68b3b8caf2a58b4aa5999c49227cb36e70ea6
# Mon, 26 May 2025 21:49:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 26 May 2025 21:49:30 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 26 May 2025 21:49:30 GMT
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
	-	`sha256:ecfb4c01304ef6340f8a80889d64a187e58cc76d5af000daa24fd81116b6efa7`  
		Last Modified: Tue, 27 May 2025 20:24:04 GMT  
		Size: 13.7 MB (13682736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c96561c852f02a75e86a990d3ed3afc98ac910b8b09d754e8fe5c68619c93b2`  
		Last Modified: Tue, 27 May 2025 20:24:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a17b36ced4fe3ecd7ac11883304fe81e3a17d7db89d965202a9cd6ea67eaae3`  
		Last Modified: Tue, 27 May 2025 20:44:27 GMT  
		Size: 5.9 MB (5853268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:37cf5da57ad8c4a95511e21e11ba3ebc8513d22bf767b8cb397cb5d477784cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.3 KB (637331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b991255b771f9b3209dd28d360580eee15e698d5505a613d5ece7c8de8477ff`

```dockerfile
```

-	Layers:
	-	`sha256:1e5dcab9e945d3ed3e62f01c90491f24eafeef3e6d1d3f39869254f1d6837f83`  
		Last Modified: Mon, 02 Jun 2025 19:52:01 GMT  
		Size: 629.3 KB (629277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44308390466f44cc4c327f96f65b20ae540c211ee1164d47445a9b8df6ccbc3e`  
		Last Modified: Mon, 02 Jun 2025 19:52:00 GMT  
		Size: 8.1 KB (8054 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-alpine3.21` - linux; riscv64

```console
$ docker pull hylang@sha256:9b81331b855ea2ea110ef862ec8e005dd0de7215e4748420869962ff245b0854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22692881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7057a99848707780d814f6c13710b41d95b18c1ec3b09e75beb859bf004e06`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 26 May 2025 21:49:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 21:49:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 26 May 2025 21:49:30 GMT
ENV PYTHON_VERSION=3.14.0b2
# Mon, 26 May 2025 21:49:30 GMT
ENV PYTHON_SHA256=7ac9e84844bbc0a5a8f1f79a37a68b3b8caf2a58b4aa5999c49227cb36e70ea6
# Mon, 26 May 2025 21:49:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 26 May 2025 21:49:30 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 26 May 2025 21:49:30 GMT
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
	-	`sha256:49a3b46847989afab71578f477702b931d0863e0cc5c25c4346e6be5470bf857`  
		Last Modified: Tue, 27 May 2025 21:23:42 GMT  
		Size: 13.0 MB (13026632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9d95a6ffb5fb60821b05ff431cc40bc3a3bfa8a5f813acbc8034eeb810f597`  
		Last Modified: Tue, 27 May 2025 21:23:40 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f47b7f7ebe6dec5b91562a3adc1b78a8e08486fe3a643997f36c09aafd7f6c`  
		Last Modified: Tue, 27 May 2025 22:12:23 GMT  
		Size: 5.9 MB (5854023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:5233efa071edb78a14759a94e7dfde6a5b4e12dfbc7855e38259b35e3d4d3cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.3 KB (637327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51afc5029998825aac9f4a7a22c2935954d91c8fa6624a6430916ca804e9abd0`

```dockerfile
```

-	Layers:
	-	`sha256:f52e51c3a2f997689866a90f0d4562fe5c0d0b1712a11d5d7a03cea1b47ba8ca`  
		Last Modified: Tue, 03 Jun 2025 02:13:44 GMT  
		Size: 629.3 KB (629273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b276d6f580964517712ef36a103b1b74a7233b3c4ca851a35772f985c643c7e5`  
		Last Modified: Tue, 03 Jun 2025 02:13:44 GMT  
		Size: 8.1 KB (8054 bytes)  
		MIME: application/vnd.in-toto+json
