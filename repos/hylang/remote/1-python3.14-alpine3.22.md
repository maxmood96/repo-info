## `hylang:1-python3.14-alpine3.22`

```console
$ docker pull hylang@sha256:cf8924e9883f17ded705d59c90b1ce2d5946c7e0e8fbf584814a88d42cfea8c4
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

### `hylang:1-python3.14-alpine3.22` - linux; amd64

```console
$ docker pull hylang@sha256:4472466c650690106cc10e73945d0a936fe78c2814bab87ff385f4aa6ab446fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23160976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b695bb860384f2ce8f417b7ee785de8d4fda3a69cfcb33a92fbd6154477c63b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:04:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:04:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:04:01 GMT
ENV PYTHON_VERSION=3.14.3
# Wed, 04 Feb 2026 20:04:01 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Wed, 04 Feb 2026 20:09:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:09:31 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:09:31 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:12:10 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:12:10 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:12:10 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:12:10 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721411f3124f66c19438187aebf5e433f3863d4f479d6ddde0dde13b5855b487`  
		Last Modified: Wed, 04 Feb 2026 20:06:45 GMT  
		Size: 457.0 KB (457048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1fae1463515589ad88c0082498abcdbdb8fd47d59681f42557be54c64fd34b`  
		Last Modified: Wed, 04 Feb 2026 20:09:37 GMT  
		Size: 13.3 MB (13310552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb035045ac3e7de6827ce89c22e2d5487baa10dd88042b36c05a56de1633a5a8`  
		Last Modified: Wed, 04 Feb 2026 20:09:37 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721c8ec1b9bda9f7408830750d1e51812d0cf63c55fb267fa67f2067ba46ef17`  
		Last Modified: Wed, 04 Feb 2026 21:12:16 GMT  
		Size: 5.6 MB (5588251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:63b44d146dd2436992561bf5f07f12c309059f76a5246a09f5016525138f4198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.9 KB (634916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893aa5bb5d6a61552123a6644727c667cdf39b1f98c34cb3f9d664a2ec555721`

```dockerfile
```

-	Layers:
	-	`sha256:66370a21958d19b96496a0c03b2c09aa059e902425b25d7114bf312086db0e90`  
		Last Modified: Wed, 04 Feb 2026 21:12:16 GMT  
		Size: 625.6 KB (625632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:904c2e3c23fa341f07c840be1048d0b3df3ceb390eff30a2ffdbf9d899b8085c`  
		Last Modified: Wed, 04 Feb 2026 21:12:16 GMT  
		Size: 9.3 KB (9284 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine3.22` - linux; arm variant v6

```console
$ docker pull hylang@sha256:e0f55ae6f6549cb36ef2bd85f4527e274922a9b8c31a7913803d4f4616d2004a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.4 MB (22439221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658f5f98d79cb9486c7bddafcdbac30f1e14ed4ec121ddb5bbd88b424bec4e4b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:06:56 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:06:56 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 03:06:56 GMT
ENV PYTHON_VERSION=3.14.2
# Wed, 28 Jan 2026 03:06:56 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Wed, 28 Jan 2026 03:09:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 03:09:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 03:09:41 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 04:05:56 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 04:05:56 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 04:05:56 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 04:05:56 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbb93456cd9ac6f8ec3d85f3a6d3c4e5e2be3de4f73c485f1546a3a4823de24`  
		Last Modified: Wed, 28 Jan 2026 03:09:47 GMT  
		Size: 457.9 KB (457869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cfacfc54a3da142b4ca9df43a8c45eadb00787a6a996146a146daf8f52b29a`  
		Last Modified: Wed, 28 Jan 2026 03:09:47 GMT  
		Size: 12.9 MB (12889030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392205a34633cf1d20fd6a39386544f994f60da8263bd0118a8d6f1eda72954a`  
		Last Modified: Wed, 28 Jan 2026 03:09:46 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce675e6edf61f064bf277a399b15450397b19e04fe41d74527d403e67161f17`  
		Last Modified: Wed, 28 Jan 2026 04:06:01 GMT  
		Size: 5.6 MB (5587026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:54cb6a99ffdbb5b3a27eaafd2a54ba8415dc01303ebc2115b77d4946eadbdf7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf58bdb4e0c57952e21ce536e935b12bb3e5ff00623d586ce04d4968a54660a`

```dockerfile
```

-	Layers:
	-	`sha256:b07626d8ddd2b43ffa9542324036b7e92e3222cd53d5f267635bf6eb6bfa980f`  
		Last Modified: Wed, 28 Jan 2026 04:06:00 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine3.22` - linux; arm variant v7

```console
$ docker pull hylang@sha256:a837cebc21a412c25baced1bb3e13e404c7a9546a2fd15571c811a41a3f4ccd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21774718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b73b5bd97892d72cbdaba0a04df059a6897f45b80874ba3f3f266d5678bf8ab`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:06:56 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:06:56 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 03:06:56 GMT
ENV PYTHON_VERSION=3.14.2
# Wed, 28 Jan 2026 03:06:56 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Wed, 28 Jan 2026 03:16:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 03:16:36 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 03:16:36 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 04:29:28 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 04:29:28 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 04:29:28 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 04:29:28 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76260369b49c861f79659547d43b9b96c3a9d8d53c49ee765e0783428fc7dc5`  
		Last Modified: Wed, 28 Jan 2026 03:09:48 GMT  
		Size: 457.1 KB (457057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb572fee8e30d641ca6d632e2a36cbce27305c524aec19026a9f252a13f5fd34`  
		Last Modified: Wed, 28 Jan 2026 03:16:42 GMT  
		Size: 12.5 MB (12506713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92315577882a5a3f925460fa6a230d9865ef93e917432ee570d5e688ded9ca88`  
		Last Modified: Wed, 28 Jan 2026 03:16:42 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f35a5ccc427cf4775f4cb4636af3b2ecff1d87cb1c4c37ece5b78a49a5c0875`  
		Last Modified: Wed, 28 Jan 2026 04:29:35 GMT  
		Size: 5.6 MB (5587070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:35dc1f7a1135ae9eaf8619f312628c5e1b16331d11bae17bee47d0bc8ad9d875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.1 KB (638086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac16b79561c02bd6bbd73197fd5198a5481ee4d8552b7bb29b5dad0a0b16798`

```dockerfile
```

-	Layers:
	-	`sha256:78ac38c56452117b4f14369d1fb8b2ece1c1288c96e1ce93a64c46b90d993e82`  
		Last Modified: Wed, 28 Jan 2026 04:29:34 GMT  
		Size: 628.7 KB (628690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a298aff25f6c1d60e2932a746ec61d2bc0395572609ae3db034f94f4d48d45f4`  
		Last Modified: Wed, 28 Jan 2026 04:29:34 GMT  
		Size: 9.4 KB (9396 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:91abbaefa57e4a77f0f2b70266b06433708bb4d31b685819b2ea70c69293ec5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23479776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c84e289a5b4dfdd4bf4d50abcd1a20f3ae6b66358ca21470d4a072ecdd91f2`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:04:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:04:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:04:08 GMT
ENV PYTHON_VERSION=3.14.3
# Wed, 04 Feb 2026 20:04:08 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Wed, 04 Feb 2026 20:09:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:09:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:09:29 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:10:07 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:10:07 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:10:07 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:10:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1a6b74439e8677c9460b5bc6d4c97d29ea7073cb8f640a83602710d484a3db`  
		Last Modified: Wed, 04 Feb 2026 20:06:48 GMT  
		Size: 459.2 KB (459152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ad5cce29c608b70ea8591757c55b123ac98625282a6997b030a699d016a2cd`  
		Last Modified: Wed, 04 Feb 2026 20:09:36 GMT  
		Size: 13.3 MB (13292565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c663bc312c61e55d4cb3ddffe172f4844a63850a3e32e4f3e5301baef853ab`  
		Last Modified: Wed, 04 Feb 2026 20:09:36 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27904bba2c7f6093799936f6d9d0e0806dc45e20e4380b508cd1a7e44795bde8`  
		Last Modified: Wed, 04 Feb 2026 21:10:13 GMT  
		Size: 5.6 MB (5588291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:7826f4fe9e7552ebc839baee6af9a85b30ab04b6003d7a3e2ac194cb5aefa840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.2 KB (635170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8e428f4782ea924d497e557a3bee36877659c313f6ef652b92a845db860ff4`

```dockerfile
```

-	Layers:
	-	`sha256:127468b7313aa1249a5e8afa0e452844ef52d488bb502ddf08e7daae4b257a2d`  
		Last Modified: Wed, 04 Feb 2026 21:10:13 GMT  
		Size: 625.7 KB (625736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9565c0dfeb6866f0f494e8d59bbe8c2c8d9778137df7203de950d4eac2edbea`  
		Last Modified: Wed, 04 Feb 2026 21:10:13 GMT  
		Size: 9.4 KB (9434 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine3.22` - linux; 386

```console
$ docker pull hylang@sha256:2a6031680ecc5e8720b43549b60b9c7ffcef6615b2598032acc8bc292fe8ba29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23255913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077c006eeb658bfa25191c026b36086a8a83ce5c2727ae84ef23dd3df50b1f98`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:07:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:07:09 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:07:09 GMT
ENV PYTHON_VERSION=3.14.3
# Wed, 04 Feb 2026 20:07:09 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Wed, 04 Feb 2026 20:09:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:09:33 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:09:33 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:06:40 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:06:40 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:06:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:06:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8dc36f4e023c67e4ac5ff400f4b7cd6f9e16799be1d85818ef71053e761266`  
		Last Modified: Wed, 04 Feb 2026 20:09:39 GMT  
		Size: 457.5 KB (457509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2d380c6f5618e3fd1fc650b3d6aa679e3459a4495417cff8d617bf093e8d38`  
		Last Modified: Wed, 04 Feb 2026 20:09:39 GMT  
		Size: 13.6 MB (13589139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e181a523de1cee6ea6f28f7076a60a376948871e68fb3105230de0ae847184`  
		Last Modified: Wed, 04 Feb 2026 20:09:39 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fef8fddbddbc74bbd717ab33803149ff8113b41f200da44114cbe86d73f41c`  
		Last Modified: Wed, 04 Feb 2026 21:06:46 GMT  
		Size: 5.6 MB (5588284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:14e9a9881d8c30b50dc508b20515e3033ff0a9c8bcaa29a4968aff045ac866df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.8 KB (634819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66f4bb923029fad624fbca8a8fe2b580742c2a27aa50cbd6ecb8d566b366705`

```dockerfile
```

-	Layers:
	-	`sha256:f459d479161dc8a1fd6ac620277f048313632d08f0dc08d0cf029bb2d2b3818b`  
		Last Modified: Wed, 04 Feb 2026 21:06:46 GMT  
		Size: 625.6 KB (625587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aee4991451d8d808d3c92a9954ea32931f00af63414d93c4687a35c8bc7122d8`  
		Last Modified: Wed, 04 Feb 2026 21:06:46 GMT  
		Size: 9.2 KB (9232 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine3.22` - linux; ppc64le

```console
$ docker pull hylang@sha256:9b06fa7e99fb1fc1868d2927c5d87aa229d9bc4ec4b2bb9188d1b4e39e5dee83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23860820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6efbeeac5da63ddf41bd0690928e8f20e04b9881ba7533b8c0d540001821e25`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:44:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 04:44:31 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 04:44:31 GMT
ENV PYTHON_VERSION=3.14.2
# Wed, 28 Jan 2026 04:44:31 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Wed, 28 Jan 2026 04:50:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 04:50:44 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 04:50:44 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 06:58:55 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 06:58:55 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 06:58:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 06:58:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1c0afa633a3760fd9ab687459d95fd4798539d5a78dcc7093921a89ff5eff`  
		Last Modified: Wed, 28 Jan 2026 04:47:43 GMT  
		Size: 459.6 KB (459568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261b3139204cb1880ba91c1e25f1761e0b623bbda21e3b62510ca332a7d83016`  
		Last Modified: Wed, 28 Jan 2026 04:51:01 GMT  
		Size: 14.1 MB (14079604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917a8d6532ae42d22fcffe3f41aa9307b7aa92ca6e2df39315906893d4ffe603`  
		Last Modified: Wed, 28 Jan 2026 04:51:00 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce87496cf9815d6253e7261c5a55a58fe03e041e9aadff3bc428afac6097878`  
		Last Modified: Wed, 28 Jan 2026 06:59:06 GMT  
		Size: 5.6 MB (5587103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:b06d6cb8a30e5e39a798d43b5d2dc9296fe8c0e05578333f2c4a2fb54422945c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.1 KB (633091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022dbb65fb066be59de296310d563aacafe623fcb41bbdd8746b745f0380fad5`

```dockerfile
```

-	Layers:
	-	`sha256:d784d02d514c60a0f04e1150073047de65bd1ee3ceff535372a007c88d480d4c`  
		Last Modified: Wed, 28 Jan 2026 06:59:05 GMT  
		Size: 623.7 KB (623739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a25aee1e14e4491191767bc79ced43392cfd4057a8fc5fbe3e76f937529f600`  
		Last Modified: Wed, 28 Jan 2026 06:59:05 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine3.22` - linux; riscv64

```console
$ docker pull hylang@sha256:0745520200f0d489b2815fd2857254d7f2c8a291cb1e6ec595920909af95c19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23020090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9211cef45bc8335ee7daca38363e3d60e7c9d17a1b20e31aff787156b4fbbb`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 20:12:03 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 20:12:03 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Jan 2026 20:12:03 GMT
ENV PYTHON_VERSION=3.14.2
# Thu, 29 Jan 2026 20:12:03 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Thu, 29 Jan 2026 22:10:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 29 Jan 2026 22:10:33 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Jan 2026 22:10:33 GMT
CMD ["python3"]
# Sun, 01 Feb 2026 05:57:11 GMT
ENV HY_VERSION=1.2.0
# Sun, 01 Feb 2026 05:57:11 GMT
ENV HYRULE_VERSION=1.0.1
# Sun, 01 Feb 2026 05:57:11 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 01 Feb 2026 05:57:11 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f09c06bcb0cd7a2f20a63c8a8409f2c94c296872976bd8ac6cc3232892a618e`  
		Last Modified: Thu, 29 Jan 2026 20:49:52 GMT  
		Size: 457.4 KB (457400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6ec509f0e99d1489b0a03ae91d2d5485099c5badf646de1bea9df8bd4eea4a`  
		Last Modified: Thu, 29 Jan 2026 22:11:20 GMT  
		Size: 13.5 MB (13457582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615e9412ef6f8b08fae02173dca9ddfdad0b33b427b860c371e0d45f0443d664`  
		Last Modified: Thu, 29 Jan 2026 22:11:17 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcb0c94593c9d8e3a8112c1652266d1810bfdcbfdf1a0f350dd95aa051b4b71`  
		Last Modified: Sun, 01 Feb 2026 05:57:51 GMT  
		Size: 5.6 MB (5587436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:abb098067a4047f1dd84b0a80d494714d8c859379d00f58a9058f5f2a9e64a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.1 KB (633086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b776abe457a1c05a8c9391669ddfcb7752bf3785b8c109b33cc2b5615338b6e2`

```dockerfile
```

-	Layers:
	-	`sha256:9ee22e6979bbec14c27fca3a72ae85033b741b42497310bb729b6e2a60aa7c82`  
		Last Modified: Sun, 01 Feb 2026 05:57:51 GMT  
		Size: 623.7 KB (623735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cb19d833723caed36576c983c57d29ad9dcbded99a929e652e8284fa31a0850`  
		Last Modified: Sun, 01 Feb 2026 05:57:51 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine3.22` - linux; s390x

```console
$ docker pull hylang@sha256:11e611c3982a886b346f9e6430a8a5dd624924759fb1aac0edba3818ec6f6070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23497426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3946989eba528453a9f6abfaa516fabb8dcbac348fb940920081f4ba935d80fe`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:27:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 06:27:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 06:27:54 GMT
ENV PYTHON_VERSION=3.14.2
# Wed, 28 Jan 2026 06:27:54 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Wed, 28 Jan 2026 06:36:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 06:36:14 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 06:36:14 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 07:27:52 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 07:27:52 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 07:27:52 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 07:27:52 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3774a20bd11bb03ab9932bdbf32f75779c80e3db7f10da48aeecbff4bb4662e9`  
		Last Modified: Wed, 28 Jan 2026 06:31:42 GMT  
		Size: 458.0 KB (458037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec46fc739c5f290d2d08b575604704021d91ea24f5db2bc602df6f516db0330`  
		Last Modified: Wed, 28 Jan 2026 06:36:25 GMT  
		Size: 13.8 MB (13801657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f8672c18faa258d3d68034355ccf0057d7c3d28185f2628d3d349f932ba290`  
		Last Modified: Wed, 28 Jan 2026 06:36:24 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135accf2993673a94669e9db886933400828130d315198ba3136939ca9a7468a`  
		Last Modified: Wed, 28 Jan 2026 07:28:01 GMT  
		Size: 5.6 MB (5587049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:b976d1458094801ee85d9927603a5ee57fb0f3af3d5fd3be970b0ba8e51c9119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.0 KB (632965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ebc7c7511bcf0e936c86c6da78457978527b99e7a0f9caf5e0d3df9837c9708`

```dockerfile
```

-	Layers:
	-	`sha256:3b718c58cded2b5649f1b8eeb23949965a2973745298f5da0ddbda5cf1dc3b8d`  
		Last Modified: Wed, 28 Jan 2026 07:28:01 GMT  
		Size: 623.7 KB (623681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c209cf82cc12534a46687542a44f595114003a6ebd5b4e5596483ea5f67d0a6c`  
		Last Modified: Wed, 28 Jan 2026 07:28:01 GMT  
		Size: 9.3 KB (9284 bytes)  
		MIME: application/vnd.in-toto+json
