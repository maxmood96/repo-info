## `hylang:python3.13-alpine3.22`

```console
$ docker pull hylang@sha256:9fc178de2fd0281b39fa4c961d4fbe106c9c998bb79355f41d968080dea85cd8
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

### `hylang:python3.13-alpine3.22` - linux; amd64

```console
$ docker pull hylang@sha256:e95bb0b602a1ffb0d7941c2c603c555ee8fb40c36157afb4d81bf1691cd11709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.2 MB (22189155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fabce3a5f4e73262a96a49740609151fe174f52a5d8cb02e1c8b39360bff76`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.13.9
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24e45344b415b3025bddd3c7795b3b3f9883beea1dc700ee52587c432184eba`  
		Last Modified: Wed, 15 Oct 2025 17:11:24 GMT  
		Size: 456.9 KB (456923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1a564c7d4a34452712d895e8047635d9a6ba701e9f526f403907ed67d7c780`  
		Last Modified: Wed, 15 Oct 2025 17:11:25 GMT  
		Size: 12.4 MB (12379126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6fa290b4c73bf1d47f30315e9949e2fbfc992ad584f6318856c72555b253db`  
		Last Modified: Wed, 15 Oct 2025 17:11:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7578099c7b0d0b6f999c73004b4b2a4643b1433418dda9dbf3a160d64fe31c2a`  
		Last Modified: Wed, 15 Oct 2025 17:12:34 GMT  
		Size: 5.6 MB (5550406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:8756a0c0a049fb154d008539856d7c6b28983ef65d57a1dba151b1769f950d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.7 KB (632702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e503833f63f06da19cb830e839afdaa0b83bfad4b059682557396bcb4888d3b`

```dockerfile
```

-	Layers:
	-	`sha256:29c08a25a50a27a2a4c6ce6db38698a24175b54b7c2472e1e0592bc631921164`  
		Last Modified: Wed, 15 Oct 2025 20:19:39 GMT  
		Size: 623.4 KB (623376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac752160e2782d00a9d3821165b299e006525efec51120f8006e86ac6a38a609`  
		Last Modified: Wed, 15 Oct 2025 20:19:40 GMT  
		Size: 9.3 KB (9326 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; arm variant v6

```console
$ docker pull hylang@sha256:0cd83c4cc13f52fc1c6be7eb8e1788dc11950cc28da84259c67501330541118d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 MB (21510151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78987afc328159cf75ea192eacafdfed5236816db335cb072a7f8ed9686436d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.13.9
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02e4f3cc3a4565fdc6d682b29ff1086172ec601449ffc64ff35a5ec7180a85`  
		Last Modified: Wed, 15 Oct 2025 16:49:37 GMT  
		Size: 457.7 KB (457746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf2697a8cd57899655b1f12b5240de1679df2f3af8262e1bf9cb246077e1211`  
		Last Modified: Wed, 15 Oct 2025 16:49:38 GMT  
		Size: 12.0 MB (11997565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f5f8f921b37496f0e5be4773922e5634bb1b910bf7be6590e5d04d6fe24e6b`  
		Last Modified: Wed, 15 Oct 2025 16:49:36 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e181699640246843f1fe4d4688a600dc0798a992c37e0524a0d6a13ac060fcf7`  
		Last Modified: Wed, 15 Oct 2025 17:09:27 GMT  
		Size: 5.6 MB (5550512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:bbc556d024bc8781b59fc122746c9968173835c50dab846830bcafaf0b12fc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7852b1333ca5eb7f3686a942fbae55a2d8db3957543f5cad68470c1bb0438e07`

```dockerfile
```

-	Layers:
	-	`sha256:f89776ac9df574b6f009ece1690fb341d5e7aa2a65e61c2e5684246a3e8c039e`  
		Last Modified: Wed, 15 Oct 2025 20:19:43 GMT  
		Size: 9.2 KB (9222 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; arm variant v7

```console
$ docker pull hylang@sha256:1e2094015a77000002a1803eb60e248dab769ff3d6116650ceca3585c403d3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20903302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3f57416b9e1b6ac08d5dcf3280976ba041cb4dd0774aa94448abfcd0844b92`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.13.9
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4dae11c7ce712c3188f32a226f09e34ce659930bb9a74419bf4af9616329f62`  
		Last Modified: Wed, 15 Oct 2025 16:57:32 GMT  
		Size: 456.9 KB (456927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e1e247a2a02da52add9d5e26dc2d2baddf4acada7748fe6a03498ef2d0e41b`  
		Last Modified: Wed, 15 Oct 2025 16:57:33 GMT  
		Size: 11.7 MB (11674057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d314d7266a9f081fdcfbdc2b51e3151abf866e95a4df136913586c3553a44fa7`  
		Last Modified: Wed, 15 Oct 2025 16:57:32 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592e4b40891b0da411e5e01ed140c7211109b584b50ace3fd931daf695f3c428`  
		Last Modified: Wed, 15 Oct 2025 17:09:23 GMT  
		Size: 5.6 MB (5550515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:f12523cc8448a19a62cb966828c028541bbc661e73bf726927d2594643573bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.9 KB (635872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c038c0493778a28a0c14a9c65db211403d954b26e435bb565d10c9058c8a6f7b`

```dockerfile
```

-	Layers:
	-	`sha256:f6c17a5e498ceea31f2e42cf0fd33542eeaa17a8fb86e76274be3e1dee7a0794`  
		Last Modified: Wed, 15 Oct 2025 20:19:46 GMT  
		Size: 626.4 KB (626434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c132aa6f585f76d445924f759518afb21326cedc01f0272777eab685392254f8`  
		Last Modified: Wed, 15 Oct 2025 20:19:47 GMT  
		Size: 9.4 KB (9438 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:e9e10e273f38c7fa7189eafba7806ce53a0a81a312985db7e04739d3e398f653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22541791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3eaf0ff128c63e7d9eac9e9e96aa035d2e6f3cc6c78ccd194ebafb0d857fb1`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.13.9
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71263fa570a63eb3dfff44620561237a401f3196cb998cefa48b23c32c0f4abf`  
		Last Modified: Wed, 15 Oct 2025 16:53:49 GMT  
		Size: 459.0 KB (459011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e82d8615442035e9072f7ebebbfdc82f06194b454d313168e5ff21f02bcb14`  
		Last Modified: Wed, 15 Oct 2025 16:53:50 GMT  
		Size: 12.4 MB (12394016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a365b55c38e78952efffd43d7cd4a850e08c2651eee738ae437bb5e8599df70f`  
		Last Modified: Wed, 15 Oct 2025 16:53:49 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba9a19ce3941a7d1a4ac477b4bccd63724146aadc7c1f2ab003b869944bbd8c`  
		Last Modified: Wed, 15 Oct 2025 17:13:17 GMT  
		Size: 5.6 MB (5550447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:aae23b7f586d8bee365d328f2f6800a13d6451e5a3bff70a487fc529ecaae902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.0 KB (632958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d24f05e09649ed98bedc03f7c79767e71ab6ccbbfe5912f309a98490a31ef1`

```dockerfile
```

-	Layers:
	-	`sha256:c554d9367a2516b201b611db2a818b02294c60c11da9e3ff1eee68fcfcd53a4c`  
		Last Modified: Wed, 15 Oct 2025 20:19:51 GMT  
		Size: 623.5 KB (623480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5adacc9e8bdade7e49b868a2d5819760642717b9dc647414df8417546e0895f`  
		Last Modified: Wed, 15 Oct 2025 20:19:51 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; 386

```console
$ docker pull hylang@sha256:56b36e536b83bdfa1f80b3f02e4beebdd091222a2a1b73aff429e5735633d2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22261593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e360906adec1fb57cf839621383dd0f373de4b50de785a72dbec318893c1c140`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.13.9
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7cf655b6483b0826a9217a18f518ce3f101d68c7d578c33e94c53155341d4e`  
		Last Modified: Wed, 15 Oct 2025 16:51:10 GMT  
		Size: 457.4 KB (457373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d017901a61343661e85de32cc65ee8097bb4ffbc6c26e6fe7db57ca98c02b0`  
		Last Modified: Wed, 15 Oct 2025 16:51:14 GMT  
		Size: 12.6 MB (12634549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8788d4a5dbec5607a987af531f4ea1030e25153c167071eb709b6de3395d488`  
		Last Modified: Wed, 15 Oct 2025 16:51:10 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d69159c2680ef8651c9d7b96118d2baea3e754b833b6bca63814dc51d85f67c`  
		Last Modified: Wed, 15 Oct 2025 17:38:37 GMT  
		Size: 5.6 MB (5550490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:761c20697d5606ea195e23685b4410735a774cd4e1369bd178d77fb6dd2e9d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.6 KB (632605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533f24ab10636f768de1c7037e44abb35749de22eaca5b2947e41b5eda882189`

```dockerfile
```

-	Layers:
	-	`sha256:b8ee0533d427cb8d11ee6f5e7e56eca8013eec4f3df7e8ad21f0911a6d3b1843`  
		Last Modified: Wed, 15 Oct 2025 20:19:55 GMT  
		Size: 623.3 KB (623331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8653b546f96910a7521a6d6c1173777c05e19a37d98128c9a317edd76fe83cfe`  
		Last Modified: Wed, 15 Oct 2025 20:19:56 GMT  
		Size: 9.3 KB (9274 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; ppc64le

```console
$ docker pull hylang@sha256:3e4474b4fffc21b4bc0e6d5713c42151719483a51d57bf66a7e58946c9ca036a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22845532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31cbf80d620d44870460f894e20f5859a7db1430f381cb116f53aa664f502009`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.13.9
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23714c84328ef3f37492a90472403973b73231e81a2513a552b86e56ddd87a77`  
		Last Modified: Thu, 09 Oct 2025 08:00:15 GMT  
		Size: 459.4 KB (459428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb18a53c63bd02893e5f5137cc66f1ec4c8fd6c5486c04a700b762f8564c6a3`  
		Last Modified: Wed, 15 Oct 2025 18:11:15 GMT  
		Size: 13.1 MB (13103071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3d21d6f7e75f52bfcf1ddedad4146ace35b88a4e53485ade69bc15f158e810`  
		Last Modified: Wed, 15 Oct 2025 18:11:14 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320b5a7df66834fcfe524906c8e9c160ea22b562339515dcdd38e6dfe223e870`  
		Last Modified: Wed, 15 Oct 2025 19:11:39 GMT  
		Size: 5.6 MB (5550543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:56c831b3397d9a1e59e73afb32add08049f38ac58e3b433f4d320970e79a8655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.9 KB (630877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48876d27460d4fddeeb762f105b685cc8fa52cb7366918028451149040c713c`

```dockerfile
```

-	Layers:
	-	`sha256:62a1ad09fca89bbd254c6edb66e39e7f2148ef410f6a995827263031eceae47a`  
		Last Modified: Wed, 15 Oct 2025 20:19:59 GMT  
		Size: 621.5 KB (621483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd560a8f046ead983d7b45f3d339057a3bfa1014f65beb69222d0b6afcd0a19e`  
		Last Modified: Wed, 15 Oct 2025 20:19:59 GMT  
		Size: 9.4 KB (9394 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; riscv64

```console
$ docker pull hylang@sha256:cba1b2d7e221c122e06f8c9387bc6b359e9a2eedd3aa2e25cded9606bb87961a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (21970837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ba093e247a293a50b133472087256f5e40323a5ec85ebcbf4b9652dd4df4fc`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.13.9
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3386baf0e035ea4652fc916d5ecaf8b33fd89200acd2da378d80b4cc1fd3ee`  
		Last Modified: Sat, 11 Oct 2025 01:38:25 GMT  
		Size: 457.3 KB (457263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9817292eb1fc9ec1536cf82a879cea516580480c3a4201a6bcc9b4d79af838`  
		Last Modified: Thu, 16 Oct 2025 05:32:13 GMT  
		Size: 12.4 MB (12446747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f0b3d2bf84076c840e7b2c23315ef8b51370c7805efbeb66d2e0416aba27a`  
		Last Modified: Thu, 16 Oct 2025 05:32:12 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb4a211ba53fc2a5d17342d1caa59650e92f4a1c3d9e61086b4404d8b704047`  
		Last Modified: Thu, 16 Oct 2025 11:47:13 GMT  
		Size: 5.6 MB (5551337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:dc5e942c6887a532567d535252d014886dee3e271f1bc415f9c21986eed8f9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.9 KB (630873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646429fc2ab5b5e7d7551c57817da791ee60a576465910787970df042473abad`

```dockerfile
```

-	Layers:
	-	`sha256:83ca8ee1cf59a78514da9d0c5b66684290fd713652fc19bed071f665093ee74d`  
		Last Modified: Thu, 16 Oct 2025 14:18:17 GMT  
		Size: 621.5 KB (621479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3b50f9c3310ef5197a63830c891c27b002b4303accdaea76a3b207b11c9f1f4`  
		Last Modified: Thu, 16 Oct 2025 14:18:18 GMT  
		Size: 9.4 KB (9394 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; s390x

```console
$ docker pull hylang@sha256:30fc8fb4daab99b3ab0bc2d4cb40330c6ccc2735eadad05232dad34bef2acf11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22496607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba51c3d7b9fa77003efeee73492078d9e1afbf098c32cce11aa51d1326080f5`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.13.9
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825710de672f5a5c7768d4c4cf259be1850b49a843e5d8287c4b28ec27b5f190`  
		Last Modified: Thu, 09 Oct 2025 12:34:32 GMT  
		Size: 457.9 KB (457905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec98d65865fba049469fe400b5d69c38e507f010f68d29af057b36553b3be2b7`  
		Last Modified: Wed, 15 Oct 2025 17:46:13 GMT  
		Size: 12.8 MB (12838780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ffb40dcde2104cc8ae4166057fc3ace80f7a0f79c06a790d89d13029b642a8`  
		Last Modified: Wed, 15 Oct 2025 17:46:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22073728620e91fd8b3991d045b2640bbe0c224a52f441ac53b0fcd44e63afb`  
		Last Modified: Wed, 15 Oct 2025 18:25:13 GMT  
		Size: 5.6 MB (5550431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:56f1d2547503695260fe9d048a1dc9a96c2964b050d6f415bc8314481dc215d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.8 KB (630750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1991d97d97e6aec6bfb70247db5f6f05657185178f26b2fa58037a86fe1690af`

```dockerfile
```

-	Layers:
	-	`sha256:a0c7fb161a180864bd30e4006ceefb08e9fc4bef4b400969f20568a3aa6da9b7`  
		Last Modified: Wed, 15 Oct 2025 20:20:05 GMT  
		Size: 621.4 KB (621425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f5376ee407f48c52bf4f0fb197a3586258b4dd12071930a7683fe1de23fab69`  
		Last Modified: Wed, 15 Oct 2025 20:20:06 GMT  
		Size: 9.3 KB (9325 bytes)  
		MIME: application/vnd.in-toto+json
