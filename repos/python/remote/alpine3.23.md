## `python:alpine3.23`

```console
$ docker pull python@sha256:14558bb88225c495de95c0796c22de2c708500e48e9a6b84ce6b729d590fcb65
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
$ docker pull python@sha256:581c14606911610c6b61e569714e92a726c1ef2437dd034824f644f6d9df6e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17693963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ed750fc366fa2c049b60ef401b5c8e3c79d2cbc759ec08876b9345ad7b1dc8`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:03:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:03:59 GMT
ENV PYTHON_VERSION=3.14.3
# Wed, 04 Feb 2026 20:03:59 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Wed, 04 Feb 2026 20:09:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:09:04 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:09:04 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0805a1082be0eb6421d4e4ea162883988394d156972333fe3818728bf2e0416f`  
		Last Modified: Wed, 04 Feb 2026 20:06:31 GMT  
		Size: 460.9 KB (460948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3566efde290bd04ef1658d390fe2c17f4a9fdf47499f81e1e52f4ecccec500e6`  
		Last Modified: Wed, 04 Feb 2026 20:09:11 GMT  
		Size: 13.4 MB (13370946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2800a7aef8b136106b41f5cd30530992ed6ad5f3b48b1ce9516084d69ba3cea3`  
		Last Modified: Wed, 04 Feb 2026 20:09:10 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.23` - unknown; unknown

```console
$ docker pull python@sha256:e4599d4a08f9139912c3657949039cc00e70ddc91a56ed222b7be6d00dee8907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.6 KB (640587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0cee7c24f05b5647a9add39ea1e5602c7376d5a0de1b1fdfe06d21e009e338`

```dockerfile
```

-	Layers:
	-	`sha256:c3a1310b263e02360d3e2bdcb16c9f4204fcbb4a9f900f9a7d59b5a0d43d8d90`  
		Last Modified: Wed, 04 Feb 2026 20:09:10 GMT  
		Size: 618.0 KB (617962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed708596bc5fa4ba93245d287b9aa07fcfa60a29a0e18fc0b5cfff8d35b846f4`  
		Last Modified: Wed, 04 Feb 2026 20:09:10 GMT  
		Size: 22.6 KB (22625 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.23` - linux; arm variant v6

```console
$ docker pull python@sha256:e90709365c6d22073ba07613982ddbf509eb7a8ccf43796ea8cb3f9f5294cc10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17028166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b1f2b066ff5adc62caf492eb14a07d24b589b88d6e1d0bcd63e5bb75b66ba6`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:04:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:04:09 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:04:09 GMT
ENV PYTHON_VERSION=3.14.3
# Wed, 04 Feb 2026 20:04:09 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Wed, 04 Feb 2026 20:06:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:06:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:06:53 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9977f97b49c3796bef03e36eb4abf062ed7bab608e2b19b40e89fc57ad40a5b1`  
		Last Modified: Wed, 04 Feb 2026 20:06:58 GMT  
		Size: 461.4 KB (461445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208e4c6b594d4680c9b35bf370634c8b1dc39f3a36ea49209aceff37cb7254a0`  
		Last Modified: Wed, 04 Feb 2026 20:06:58 GMT  
		Size: 13.0 MB (12996652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b2cc5b74b050592c312fadb7eeba492fc78198408e76f1f72d90fc27fc5f6d`  
		Last Modified: Wed, 04 Feb 2026 20:06:58 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.23` - unknown; unknown

```console
$ docker pull python@sha256:8c700ee1ca0d1d70b8f42d99f8f27057e4d1a62f68fe0d158e8d4d8d8c9e1abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 KB (22548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be0c1c0a085ae25651fbc595d24c46f0d2dcf26d24ae197b7fe32868b59a7a9`

```dockerfile
```

-	Layers:
	-	`sha256:ec68b275950525bdc4105c3d5e413a3b3edf3fb669744cce97e49159b0d257fb`  
		Last Modified: Wed, 04 Feb 2026 20:06:58 GMT  
		Size: 22.5 KB (22548 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.23` - linux; arm variant v7

```console
$ docker pull python@sha256:d8ea7c0035deabb1e2b53a829725ce737bcfa8e021897f318d9309bf6d2a36c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16337666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc31a5e4983f6a14586240696f894ae51130352f4b381accc91f707ebbaef1bb`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:04:10 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:04:10 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:04:10 GMT
ENV PYTHON_VERSION=3.14.3
# Wed, 04 Feb 2026 20:04:10 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Wed, 04 Feb 2026 20:16:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:16:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:16:47 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5752e69d1d5fa86afaca63df454d1f70ba5f645caf736730307a775276653c`  
		Last Modified: Wed, 04 Feb 2026 20:16:53 GMT  
		Size: 460.7 KB (460735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4548e0a7e6d97da1835fba9bcce46cfbd0ba442ffe1825f429ec26e5655a9ef7`  
		Last Modified: Wed, 04 Feb 2026 20:16:53 GMT  
		Size: 12.6 MB (12594959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428f787903a5e724edc3dcd748bead1249a6963fed92581f7202965764e43bc7`  
		Last Modified: Wed, 04 Feb 2026 20:16:53 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.23` - unknown; unknown

```console
$ docker pull python@sha256:70a7638b922e5aa72b19c3f5315c68e6c6b6673d83e3c69a3a4ec3650ee64c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.1 KB (643133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419a55d851259857a05db5463406fc47ecf15aebe96568d9feac5b3775a228bc`

```dockerfile
```

-	Layers:
	-	`sha256:e915c8511cde2ba2a5866c6af572f90207917c7d4c57bf18dbe9808b3cdd0db2`  
		Last Modified: Wed, 04 Feb 2026 20:16:53 GMT  
		Size: 620.4 KB (620370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c07ffbf64674644b046f19224706072ab8edcdd16013690da97b29ee65852620`  
		Last Modified: Wed, 04 Feb 2026 20:16:53 GMT  
		Size: 22.8 KB (22763 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull python@sha256:5e5bbef2a0126e926a9116029826a29590b23ee48bd11cda30cfc08606160912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18123680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b7f425ab2eb7c56a9b38a4ddf68825caf4eb6bb8e3fbecb7013af816450715`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:03:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:03:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:03:51 GMT
ENV PYTHON_VERSION=3.14.3
# Wed, 04 Feb 2026 20:03:51 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Wed, 04 Feb 2026 20:09:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:09:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:09:13 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d233c77fc7697acc8330a76ec4404659d8534b1fe00b12be5cabb9a7fde43480`  
		Last Modified: Wed, 04 Feb 2026 20:06:31 GMT  
		Size: 463.0 KB (463015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f8dca9b7ef8a409b52b41bbe861b311fdac3be5c543163585c24946d09c3d4`  
		Last Modified: Wed, 04 Feb 2026 20:09:20 GMT  
		Size: 13.5 MB (13463326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ed0137d8700a790d80689630812c09faf706afb500c8049ad18566c4399c01`  
		Last Modified: Wed, 04 Feb 2026 20:09:20 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.23` - unknown; unknown

```console
$ docker pull python@sha256:ca3d72af8d7cbf27bda40df96209faa66660aee23886a5ea1d9f40b021fd08e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699fa090a922700588b031642f8fd55bf325f557b4b6eb347566078c8bb16d85`

```dockerfile
```

-	Layers:
	-	`sha256:db147184386cd3936360f1a8e7c626b4c08b443b2ab56d00bc77ebbd31c7e84d`  
		Last Modified: Wed, 04 Feb 2026 20:09:20 GMT  
		Size: 617.4 KB (617416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9aff4904eacc4cbc35b326dfb058cd013d44bac19792f73b79fb6d91d5c29c2`  
		Last Modified: Wed, 04 Feb 2026 20:09:20 GMT  
		Size: 22.8 KB (22807 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.23` - linux; 386

```console
$ docker pull python@sha256:0afb7bfc6fefa9987ec771073f82de1dc35c3faaf7e920b2c23ca4b8d8b254a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17772480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89819c93ca7519d27616820a4ea0d07856dce960322056f1de01ef8c8fdf9bda`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:04:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:04:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:04:27 GMT
ENV PYTHON_VERSION=3.14.3
# Wed, 04 Feb 2026 20:04:27 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Wed, 04 Feb 2026 20:06:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:06:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:06:55 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ecc5adc979d1a2402dee93e9ff1a6e4a1e6cf38c22c92891db3719a2138824`  
		Last Modified: Wed, 04 Feb 2026 20:07:02 GMT  
		Size: 461.2 KB (461232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ce63da3caefc63dfb28c720fc7f69eb57fee560d6eb4fb7f55999c18a3aee1`  
		Last Modified: Wed, 04 Feb 2026 20:07:02 GMT  
		Size: 13.6 MB (13624002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8558285f8dfa43d2ffe068bb053f6658bbd4166822a1cfb10c3ecec51331ea15`  
		Last Modified: Wed, 04 Feb 2026 20:07:02 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.23` - unknown; unknown

```console
$ docker pull python@sha256:2257e9d90452e5db92f353ac8bf54b762d663331667bb0e678323d1a2be29b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.5 KB (640486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac57248f8c2fcd30ff71d9d4a8552999f3e3d9444b7d31f1e31d9926535815b`

```dockerfile
```

-	Layers:
	-	`sha256:5eed3aa532a6d0171cf83d008ee1d93fca40f9130d2ec2f9bb52f1b682d58f7f`  
		Last Modified: Wed, 04 Feb 2026 20:07:02 GMT  
		Size: 617.9 KB (617917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfc8d2ad066d83f4174141fc21077038b95e224161ab474b053468e951c45ccf`  
		Last Modified: Wed, 04 Feb 2026 20:07:02 GMT  
		Size: 22.6 KB (22569 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.23` - linux; ppc64le

```console
$ docker pull python@sha256:a4bf20d681cf0e9577f2c0d75327e32a4e1aaf76b1c5c1c1f5c365e2ed5d0d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18545122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e4f61b67a6e83fb5f4300ae8bb37029e274fdbdb8e9cc5e778527dffd590fb`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:40:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:40:44 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:40:44 GMT
ENV PYTHON_VERSION=3.14.3
# Wed, 04 Feb 2026 20:40:44 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Wed, 04 Feb 2026 21:24:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 21:24:50 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 21:24:50 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2192b557a530eeb9753a79cc2bf687d27f9d6c5d97252deb6915a15f66fda1b5`  
		Last Modified: Wed, 04 Feb 2026 21:25:05 GMT  
		Size: 463.7 KB (463656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f067c653fba8430f366243f54442be338605e1f4ca3be76585f7c4a5546d305e`  
		Last Modified: Wed, 04 Feb 2026 21:25:06 GMT  
		Size: 14.3 MB (14251574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4da5cb7468bc8d6eecc24cea792e61094d59b3a07c1d1c42257961d1f1981`  
		Last Modified: Wed, 04 Feb 2026 21:25:05 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.23` - unknown; unknown

```console
$ docker pull python@sha256:363787be6f525a6ad37f7d612a98aa8be75410c0dbd769797559e54335d71df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.1 KB (640066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919bd47494b8483a1d308c6198557e1add17cb8d2066a52231bf9ca75b464918`

```dockerfile
```

-	Layers:
	-	`sha256:969547c6e8035d5bc35a2daa2cf65306c4fe777839c6da67f9656fb74ef81fab`  
		Last Modified: Wed, 04 Feb 2026 21:25:05 GMT  
		Size: 617.4 KB (617369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e1dfedf75eea39f13ee02fd41caa5a83898ee9957ca9b96876988c607fb587`  
		Last Modified: Wed, 04 Feb 2026 21:25:05 GMT  
		Size: 22.7 KB (22697 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.23` - linux; riscv64

```console
$ docker pull python@sha256:31a61ebffa1ea3a0d5f80d1d205334e0c550a902c2865858fbe3aa1f25cec0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17531207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8da4815f2f82a777bf459ad667b23d0ef465b4ad8aaf6eb392748e7b3c6b28`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:30:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 19:30:12 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Jan 2026 19:30:12 GMT
ENV PYTHON_VERSION=3.14.2
# Thu, 29 Jan 2026 19:30:12 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Thu, 29 Jan 2026 21:31:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 29 Jan 2026 21:31:31 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Jan 2026 21:31:31 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35a473f7da969ca6a41bd17bd9ab88790821df528b66a16299f480a4d4a1620`  
		Last Modified: Thu, 29 Jan 2026 20:11:12 GMT  
		Size: 461.2 KB (461185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9ffdd3d9fc33f5d3ee4f9ccd53137b99f2cd6425f851eff321e21ee8477180`  
		Last Modified: Thu, 29 Jan 2026 21:32:18 GMT  
		Size: 13.5 MB (13484484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74fbbb95293da59a992254e5dbbfb92d04f5ea429428ae5cd9f9bcfb4b41c01`  
		Last Modified: Thu, 29 Jan 2026 21:32:15 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.23` - unknown; unknown

```console
$ docker pull python@sha256:5ce6929cbe365dc2c9fba07ad787010bf1e6be6460637d7cfa57e5cc33eb3a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.1 KB (640102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0263d2144d41389f8c409e724bab1037dcf7b55c779a76d1161bf6d594607695`

```dockerfile
```

-	Layers:
	-	`sha256:5760f39183650f61ace35ad3a1252ae848088a8b8500e420390e91db5d197f73`  
		Last Modified: Thu, 29 Jan 2026 21:32:16 GMT  
		Size: 617.4 KB (617365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d31e169aba5c635bf5f691e7546621505596638858ad54ff52f0d8e9280c0af`  
		Last Modified: Thu, 29 Jan 2026 21:32:16 GMT  
		Size: 22.7 KB (22737 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.23` - linux; s390x

```console
$ docker pull python@sha256:047621130e5f69ac1f8a2a8cad395603309ae861adbced4eca8448223e5a6ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18044871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d361745ebbce204cb84ad0b090203cd13a3e8d3b66293381422c6908d75b8d38`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:25:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:25:02 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:25:02 GMT
ENV PYTHON_VERSION=3.14.3
# Wed, 04 Feb 2026 20:25:02 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Wed, 04 Feb 2026 20:28:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:28:18 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:28:18 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e66eff15c11b9fed4f82e03ed072ea35a5208cb6665c11b27c05429100bb2f`  
		Last Modified: Wed, 04 Feb 2026 20:28:28 GMT  
		Size: 461.7 KB (461737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f126732f18fa2ecb89963158602c0855189a771e823856e606e0cca4753b7bdc`  
		Last Modified: Wed, 04 Feb 2026 20:28:28 GMT  
		Size: 13.9 MB (13857552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9c89db7cd69f7bb71b96da615f4315f202d621124a01b1bf47e6141e3976d7`  
		Last Modified: Wed, 04 Feb 2026 20:28:28 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.23` - unknown; unknown

```console
$ docker pull python@sha256:e6416a4a6fa337acc3d1724591b52437e06f47e95b1f8dbc48185ea37b892331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.9 KB (639936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96991fadbb8277133be5f79e63899aacbd765a6ed555cc2d93752afd68fb6786`

```dockerfile
```

-	Layers:
	-	`sha256:22f3b96d0cff278e098a8861bf46040fcd28d55364c58f0c92bfa1480c7929fa`  
		Last Modified: Wed, 04 Feb 2026 20:28:28 GMT  
		Size: 617.3 KB (617311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5ce4937c8c202446013e8faf9a76cf2b322c2336a2a3264202f6666f6d2c4b2`  
		Last Modified: Wed, 04 Feb 2026 20:28:28 GMT  
		Size: 22.6 KB (22625 bytes)  
		MIME: application/vnd.in-toto+json
