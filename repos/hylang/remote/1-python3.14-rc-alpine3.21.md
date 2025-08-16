## `hylang:1-python3.14-rc-alpine3.21`

```console
$ docker pull hylang@sha256:affb71ad03a4af0b64895d5752785d7ec02c6651d138615362adc62543ca0bd2
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
$ docker pull hylang@sha256:a6f06d1cd3f8fed64f96b5867f9cd35c9eb7a87fbbc037ae52379e893beaaa8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22657189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca044bef50c005de09c7573511f3f08c4ec9fba881d947dd2fc2acb52d88c4f`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.14.0rc2
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=bc62854cf232345bd22c9091a68464e01e056c6473a3fffa84572c8a342da656
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["python3"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HY_VERSION=1.1.0
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 13 Aug 2025 21:03:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c56160a63e3e4a1871a67fcc0be714a321174029f92e341d36e0d37b32d5c3b`  
		Last Modified: Fri, 15 Aug 2025 22:10:10 GMT  
		Size: 447.7 KB (447713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b664b57fae8f878f23c08ea1c039941b76da5bc08db3f529db744449a12cb3ee`  
		Last Modified: Fri, 15 Aug 2025 22:10:11 GMT  
		Size: 12.8 MB (12805721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93c075d129f952bb297ad41c5e799729bbd76c3b9e0ff0c32c63084f81209d4`  
		Last Modified: Fri, 15 Aug 2025 22:10:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d2f4aa6bb06162f88ea6dacb0dc71fe6e98b3c00fecfd76cd8ee418f77abc5`  
		Last Modified: Fri, 15 Aug 2025 23:08:37 GMT  
		Size: 5.8 MB (5765938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:307d5feca9b74332a8551dbc516c15d5113678a03ba9d01d4e0a939dcb392aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.0 KB (625960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea976e0cf5712a5a861d39dca6d33f84bc7219da98d3fd6affc23ef0306a3193`

```dockerfile
```

-	Layers:
	-	`sha256:edc4597840247a1ee5dcea2a89c7dc1388768c57b3b66343c911777ff82eea34`  
		Last Modified: Sat, 16 Aug 2025 02:20:02 GMT  
		Size: 618.0 KB (617950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f9aec4d18535c0bddbc83dd70cf57d8a927182e22703cea81ba74f5baca65d`  
		Last Modified: Sat, 16 Aug 2025 02:20:02 GMT  
		Size: 8.0 KB (8010 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-alpine3.21` - linux; arm variant v6

```console
$ docker pull hylang@sha256:4f763e106e12722239d36b0be56cf33f68d48af768c79c3c630831b42a14217a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (21993545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8039a3aa84a19b85caacbc4d9fbf10740733da499b76e931b3e2e792f4c16cef`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.14.0rc2
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=bc62854cf232345bd22c9091a68464e01e056c6473a3fffa84572c8a342da656
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["python3"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HY_VERSION=1.1.0
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 13 Aug 2025 21:03:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ca0c331561564c536ffa9246944bb50ac21d3fb11fe66c38baad97fdd1f05719`  
		Last Modified: Tue, 15 Jul 2025 18:59:41 GMT  
		Size: 3.4 MB (3363814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1534a8707a68f4fce6b9fe16893dd0db5bca9683c969e7fe0dc7e2d7724fd5`  
		Last Modified: Wed, 16 Jul 2025 01:59:19 GMT  
		Size: 448.2 KB (448250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c54fc56caa77d10ee007922fdfad6c67c82fca10e30023dd4849373f0205e2`  
		Last Modified: Fri, 15 Aug 2025 22:15:34 GMT  
		Size: 12.4 MB (12415418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576aa37eed932d7579ef0186902cb6b52b6979714af6876c3e001a64ceb02941`  
		Last Modified: Fri, 15 Aug 2025 22:15:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39b88d8823146128208a1b993bff3820babde4b329b11a4b3eadaf280c1055a`  
		Last Modified: Fri, 15 Aug 2025 23:09:15 GMT  
		Size: 5.8 MB (5765814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:6cb7e8836fc8d5da1ee319d085cacc3a43648d0ae4dd55a97afa6c12c28383d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9a163211131c707e7ae3182efcac261f13643bdfc038e91eafe1de8582f1a6`

```dockerfile
```

-	Layers:
	-	`sha256:15098accb5c4c2e1263277a0e56a2511b15ec1a58446cc2750e1f164ded7169f`  
		Last Modified: Sat, 16 Aug 2025 02:20:06 GMT  
		Size: 7.9 KB (7872 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-alpine3.21` - linux; arm variant v7

```console
$ docker pull hylang@sha256:f97ab314a44977471d7444e753fdeedd53c6e0a69825aac27740d05f27e1d9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21631695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d87784e6cd7800b62b8329dc7947927cf1a28ed3b31ded17789e504fe6f5a6a`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_VERSION=3.14.0rc1
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_SHA256=8707780ae9f19c5bf5b9f27827181ba11cdad7bb292ea49cad5424331e40ee8b
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
CMD ["python3"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HY_VERSION=1.1.0
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 13 Aug 2025 21:03:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da9037be1902aaf669202bff8b749a3924a202174258d4ae8285c9b2b60f16d`  
		Last Modified: Wed, 16 Jul 2025 02:06:03 GMT  
		Size: 447.5 KB (447520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4c9c3aca2dc3af3e807a753207411925c95fcff91fa03d1789b1f26a3dd793`  
		Last Modified: Wed, 13 Aug 2025 09:20:55 GMT  
		Size: 12.2 MB (12229547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c08487219bf0159f81441c03b7426a61be2933d6eb2bf75612994eaa50b9f9`  
		Last Modified: Wed, 13 Aug 2025 08:15:27 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ff0f3f4a0134fbaececdd403ce9798a07e0cec963a4ee323092651860b770c`  
		Last Modified: Wed, 13 Aug 2025 16:05:10 GMT  
		Size: 5.9 MB (5857508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:ad4a270611820921fc41870c441e025e86711a0a0ee397df48d38ad3ba493821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.1 KB (629071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37dadec884f3893fe2c28da1fe493efc2998b9ab29d60a5dd4d7da5add075cc`

```dockerfile
```

-	Layers:
	-	`sha256:ed53cede471f7dbe3b99e8630f1dec21dc7ddab7b2e43eaee90cddbefa6312ac`  
		Last Modified: Thu, 14 Aug 2025 08:21:20 GMT  
		Size: 621.0 KB (620986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8f47a571b053c812627f1f9744ad2e6eefe787ceab3f24998ca39dcdbb2ce2`  
		Last Modified: Thu, 14 Aug 2025 08:21:21 GMT  
		Size: 8.1 KB (8085 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:9c3c98015c06be996ed445b2af02ce4b2e43fa5c272153142af34f2c3de630f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23003388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf8a20d70895aca2eb5a28418e95a4262c339a1e71f5395eb1946ec6023b5a8`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.14.0rc2
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=bc62854cf232345bd22c9091a68464e01e056c6473a3fffa84572c8a342da656
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["python3"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HY_VERSION=1.1.0
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 13 Aug 2025 21:03:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f11a8844724efb4750e826dae81f9f6efb2391f1e346bf78a1796ef5df145a`  
		Last Modified: Fri, 15 Aug 2025 22:49:31 GMT  
		Size: 449.5 KB (449517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1ded2660c368e1e02e8f387eb9f1180674f3872e5be8a51c941209f67ef028`  
		Last Modified: Fri, 15 Aug 2025 22:49:32 GMT  
		Size: 12.8 MB (12800802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b8aa5e2abdcdacefaa07ef56e57d88bf61a15f7615d503e2562a2f0c3c46f4`  
		Last Modified: Fri, 15 Aug 2025 22:49:31 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9584ea240c8120d6f653f2b8664b80e815647ad58c69d7d1dea95ec759e0f18`  
		Last Modified: Fri, 15 Aug 2025 23:54:55 GMT  
		Size: 5.8 MB (5765881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:fd61301b4172465b994dafa54f0d7ba3844f2a8f05139fffe1df295cd786be99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.1 KB (626121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8561c80275b2522c80329ac77f70d8384065d22ea39c5b8628545b02b64684`

```dockerfile
```

-	Layers:
	-	`sha256:e5fbf550d120f5692022e47220e4367696021f9b834dd88c14cef915a9e37975`  
		Last Modified: Sat, 16 Aug 2025 02:20:12 GMT  
		Size: 618.0 KB (618006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fdf4201b89e5a50885673c1aa3ca0af8ca1d528b43e929180ab27013a1d08dc`  
		Last Modified: Sat, 16 Aug 2025 02:20:12 GMT  
		Size: 8.1 KB (8115 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-alpine3.21` - linux; 386

```console
$ docker pull hylang@sha256:81477238e4a6061a0c4272e8b58671835ee447d9530342f9cfeb8c5b05b96c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22757480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052296b673b278e72ce8ba78fbdbe841d6ac3bd05d6b1d0c7fb5b978ee3161ac`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.14.0rc2
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=bc62854cf232345bd22c9091a68464e01e056c6473a3fffa84572c8a342da656
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["python3"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HY_VERSION=1.1.0
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 13 Aug 2025 21:03:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91f886bcb6b32d94799c923d8b5d7890f61fde7031b57af3113e96375bb04ce`  
		Last Modified: Fri, 15 Aug 2025 22:10:23 GMT  
		Size: 448.0 KB (448007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84895dd6557b0186043414f10c3d2f9060872d73e24383c44fc97bd2abd5b1ab`  
		Last Modified: Fri, 15 Aug 2025 22:10:25 GMT  
		Size: 13.1 MB (13082642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054e92e9a76a4e9ee901745d8ac5747378fbdb426ae1333b78e4bfe216eaab45`  
		Last Modified: Fri, 15 Aug 2025 22:10:23 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc63b4ab98b76ea5745d151699d5151658af4ed2c28e27431ed17e4907ad4903`  
		Last Modified: Fri, 15 Aug 2025 23:08:30 GMT  
		Size: 5.8 MB (5765857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:a7a49296d3cc678c0fbf2e3e260d9b3091c29a341fa9e24ca2ac3367d7a43bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.9 KB (625904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037bb7cdaf5ec3e4599aec14816941154920054c0e4fe934f277be8a4cb4d500`

```dockerfile
```

-	Layers:
	-	`sha256:85d87548c80957eabe97132655e0fc7208bf69b2652a45d03626a02b7d0b3b14`  
		Last Modified: Sat, 16 Aug 2025 02:20:16 GMT  
		Size: 617.9 KB (617925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19d733cefd4d0c40cb80ee236d8821c6007d6c1bf41d2ae9c1fac009eead258f`  
		Last Modified: Sat, 16 Aug 2025 02:20:17 GMT  
		Size: 8.0 KB (7979 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-alpine3.21` - linux; ppc64le

```console
$ docker pull hylang@sha256:254d0251007499fa6233387cb1de2b45b13f37de75245d3b5f8f0895472f2a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23595343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ce79548ca0a3705dd07627571226df1e1ae5b596cc808acf9c108f7d262186`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_VERSION=3.14.0rc1
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_SHA256=8707780ae9f19c5bf5b9f27827181ba11cdad7bb292ea49cad5424331e40ee8b
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
CMD ["python3"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HY_VERSION=1.1.0
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 13 Aug 2025 21:03:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73f2cf29982170ce714ef4c6c2034f1d5f3b7dec88ba87c78379716a93d7076`  
		Last Modified: Tue, 15 Jul 2025 23:44:40 GMT  
		Size: 449.9 KB (449913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd8156689093f605737036e605717b94b0ea9655e71f977018ce22db31a08b5`  
		Last Modified: Wed, 13 Aug 2025 01:48:10 GMT  
		Size: 13.7 MB (13718302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35294a486f76fd96e72841061cb150c3504833b864f20d83a70ee3260c7e4451`  
		Last Modified: Wed, 13 Aug 2025 01:48:09 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ba74801ed8c6c2d9753ffba8cb79d3de666c51abeb8cd30a0a71e2a91be608`  
		Last Modified: Wed, 13 Aug 2025 20:45:15 GMT  
		Size: 5.9 MB (5857754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:1792f161030116148d7db6b83e49b8280f1528beb93568b182724d60c1b97159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.1 KB (624098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c99ed1cb414bbed52a03f17ca1680188d0ad419fca45bc0ff023bfd027104d5`

```dockerfile
```

-	Layers:
	-	`sha256:62eccbcd68eac28be9742de41e7bb76ee95d59cb31d3bd4c4717dd8b20faea20`  
		Last Modified: Thu, 14 Aug 2025 08:21:29 GMT  
		Size: 616.0 KB (616043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eec1e08ed49e2fa0502a314b71c00b6bc5da153f5d6ba4efa844bbb7fd8ea34`  
		Last Modified: Thu, 14 Aug 2025 08:21:30 GMT  
		Size: 8.1 KB (8055 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-alpine3.21` - linux; riscv64

```console
$ docker pull hylang@sha256:b9748c5e120f893083edc20f38627a836088a3f0feff40cc32f25c3e8bc78adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22721243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25fe948bb4e84ccd3904811072326b6a34caa5bf3509df317074e58fed660803`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Jul 2025 16:37:15 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 08 Jul 2025 16:37:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 16:37:15 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Jul 2025 16:37:15 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Jul 2025 16:37:15 GMT
ENV PYTHON_VERSION=3.14.0rc1
# Tue, 08 Jul 2025 16:37:15 GMT
ENV PYTHON_SHA256=8707780ae9f19c5bf5b9f27827181ba11cdad7bb292ea49cad5424331e40ee8b
# Tue, 08 Jul 2025 16:37:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Jul 2025 16:37:15 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Jul 2025 16:37:15 GMT
CMD ["python3"]
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 16:37:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Jul 2025 16:37:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd5d8cf2baeb2d4cd2df019cff24aac486fe1e5e3cd2de997cac6035bc1ef01`  
		Last Modified: Thu, 17 Jul 2025 17:35:23 GMT  
		Size: 448.0 KB (448014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2d7ffcac3e62bad14e5b636c72ce2a02637be3010b18f02caa5cc006f1a66b`  
		Last Modified: Wed, 23 Jul 2025 23:23:07 GMT  
		Size: 13.1 MB (13065834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46df9bbac83fb2ff44f87588a82a03e8c44894f477f4cd22f25020ee272889c0`  
		Last Modified: Wed, 23 Jul 2025 23:23:06 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffff08cb2133f58e9c0f389ecd8038c50ab886aadfe25a3ccdbf5d1e48b565ac`  
		Last Modified: Thu, 24 Jul 2025 00:13:04 GMT  
		Size: 5.9 MB (5858053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:5351104885fe3accd48f35f055781a251a2ba9c3022abffc6678bc400bc9d7eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.1 KB (624093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acaf7080c3cfa0f587c37403773d0f372443c62609e775384484d779284ec500`

```dockerfile
```

-	Layers:
	-	`sha256:8ee7e5197300ca7de0e3930af32f402040aafe5a52231c750274033e1a305167`  
		Last Modified: Thu, 24 Jul 2025 02:18:45 GMT  
		Size: 616.0 KB (616039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dd29e0979a10f29c455e7eb32447ad7c072f7a7825400826338aa6bb15930b0`  
		Last Modified: Thu, 24 Jul 2025 02:18:45 GMT  
		Size: 8.1 KB (8054 bytes)  
		MIME: application/vnd.in-toto+json
