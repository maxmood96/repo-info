## `hylang:1-python3.12-alpine3.21`

```console
$ docker pull hylang@sha256:cbe69406776cfe6ac3a7b85d0f53da1de31062b5a8034eb1d5fd5fcc09f63650
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
	-	linux; s390x
	-	unknown; unknown

### `hylang:1-python3.12-alpine3.21` - linux; amd64

```console
$ docker pull hylang@sha256:cf12cf682d3689a72efb7fbea9d9b16722aefb3466c1becdeaac8d282ebb762a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23315576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac33a3d08f2261dd5177f7f99d2ed397ba02ef7905d1e7f720b55aa66b0b31fb`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jan 2025 12:35:53 GMT
ENV LANG=C.UTF-8
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PYTHON_VERSION=3.12.8
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	test "$gnuArch" != 'i686-linux-gnu' && EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd2a30403bed8ce2d8f998b1be5032cb97e2f9f46ec26c039d29bf59b3819c1`  
		Last Modified: Fri, 24 Jan 2025 19:35:12 GMT  
		Size: 458.8 KB (458752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d05111962e5378328cf22c62e3a83da84cf90592539e8248925ec409f87af5`  
		Last Modified: Fri, 24 Jan 2025 19:35:13 GMT  
		Size: 13.6 MB (13607357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8891da8f55682d107f9ba00ba9688a1342a468ee8f1953ef38caae2f042d7`  
		Last Modified: Fri, 24 Jan 2025 19:35:12 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033611f7caa6b8c8ab62931b6e47645c39c2367cbc537ed8f330c7bc5ff46fd2`  
		Last Modified: Fri, 24 Jan 2025 20:08:10 GMT  
		Size: 5.6 MB (5607503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:05dcad12a40bd98243335964669f229fd841048f54a82448f3daacc35dc3da5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.0 KB (669018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19fb46cb01833d15d4c5e3f038a88a5e301b1d54df8bc063a65b888da0466131`

```dockerfile
```

-	Layers:
	-	`sha256:18de1d9e8b558f88669edc7d6a42327122369252a151f672911898c2984950ab`  
		Last Modified: Fri, 24 Jan 2025 20:08:09 GMT  
		Size: 659.7 KB (659677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c70a7a424e961ebcd7b6b9596c968a42dda248f9f95491eb932b277c91477ac`  
		Last Modified: Fri, 24 Jan 2025 20:08:09 GMT  
		Size: 9.3 KB (9341 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine3.21` - linux; arm variant v6

```console
$ docker pull hylang@sha256:5c6de68cf2442748e38c069dc8acbe1598da45527b025c4d8b0e5d2edf520baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22543922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:635b906970d15c1f15e6485fa7823034d299324311d21d653f80d40fb7f56ff0`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
ENV LANG=C.UTF-8
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.12.8
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff0a4077f329734365423e1f7a8f45ea76ac88dda4e38832db6d82d047e001a`  
		Last Modified: Thu, 09 Jan 2025 07:48:46 GMT  
		Size: 459.6 KB (459577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0393a7f008421899966847e217574cd3457d6ac64d29f9051fa68110c1b45972`  
		Last Modified: Thu, 09 Jan 2025 07:48:46 GMT  
		Size: 13.1 MB (13112524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b68f91a2cfa6cb31e2ebf9bc822d709923c519c6bac9f441b453a9186af9193`  
		Last Modified: Thu, 09 Jan 2025 07:48:46 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b3acfa977fea9b1f215816b8ce6c25ab777527769b19dba5e62cedd47292f8`  
		Last Modified: Thu, 23 Jan 2025 01:41:03 GMT  
		Size: 5.6 MB (5607693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:439e1d02a9f9947e0a45ae88850b181b775be5015a4abbcb9cf2169c008afdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8581e7cd95ea6e7816a13bc7a1721076a9052012712c262812ca6c1de24358`

```dockerfile
```

-	Layers:
	-	`sha256:498af53f43761b5315ab09e19ac0d69b7e06c4da6551f4f03af835b9774731ea`  
		Last Modified: Thu, 23 Jan 2025 01:41:02 GMT  
		Size: 9.2 KB (9233 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine3.21` - linux; arm variant v7

```console
$ docker pull hylang@sha256:4d913b283a1141389c52ef8a9b9b73ab5a3199c5c3c7418c539b57d4541d8707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21878481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2c10c13981bd2eecf3090c9409a584b6c33d163399cf6b8ac70b322f3c89a2`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
ENV LANG=C.UTF-8
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.12.8
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a362fe3b52ccb4a43ae3d2e7b9f53bdf4eedb49d7cf54acc45450c89f8e0f9`  
		Last Modified: Thu, 09 Jan 2025 08:19:55 GMT  
		Size: 458.7 KB (458732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebff9b3600121c6ac7919aea8508dc43555f0d3d24e6b4f0c41a79d897fddc8a`  
		Last Modified: Thu, 09 Jan 2025 08:19:56 GMT  
		Size: 12.7 MB (12714636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd4773ee5716588846c0cb38f16596b192bf9c3d7f66d31b99b23eb55ae5289`  
		Last Modified: Thu, 09 Jan 2025 08:19:55 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a56c7a18f141a6b1d454f205ece110e85d2b1ba858af36e0d7c8e75fbd588ce`  
		Last Modified: Thu, 23 Jan 2025 05:12:01 GMT  
		Size: 5.6 MB (5607751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:b1721773dcc9da81fdd2d3e8ee4d7f082de006aa33a2eb52269da00cc2086fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.0 KB (672007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291df27c898bfe9b96182279ed38b8dfbb2b241529b863ca24872ce20d7d93de`

```dockerfile
```

-	Layers:
	-	`sha256:298fa30af543947b17bc39f921be4366a12258cb18b0b5c26a505218709bac76`  
		Last Modified: Thu, 23 Jan 2025 05:12:01 GMT  
		Size: 662.6 KB (662558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dead7d97b68e4f6ee1c83bef98c4ccbe42962fc48f128b0896dbea486a32d2d`  
		Last Modified: Thu, 23 Jan 2025 05:12:00 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:b3e4bac6787e96c97974be9ecbd58b961929b36f6ab67653f226748562fc51d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23714197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cddb251ad8a76519dc018f054d858a02a6b42411fe21db5af5d744b37a39c0e`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jan 2025 12:35:53 GMT
ENV LANG=C.UTF-8
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PYTHON_VERSION=3.12.8
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	test "$gnuArch" != 'i686-linux-gnu' && EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed41066ce5d3bb9c19b6566796bf04431c1dcc625165abd71c61c1816715ee8`  
		Last Modified: Fri, 24 Jan 2025 22:44:50 GMT  
		Size: 460.8 KB (460841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c0ef2e529c6689af9ee98e85584c8795cc4d6051358eb8c705babc6ecec153`  
		Last Modified: Fri, 24 Jan 2025 22:44:51 GMT  
		Size: 13.7 MB (13653183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac04324d7afff7a4625056f264fa703ef31ca26f5619baa09ab2f35489f8a13`  
		Last Modified: Fri, 24 Jan 2025 22:44:50 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acd01ffc317bb419b5af2cce76795301d9710d4b3ce2293021460864aad6b6f`  
		Last Modified: Fri, 24 Jan 2025 23:55:57 GMT  
		Size: 5.6 MB (5607565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:ad9bd427d3341076b9837747307e4ade10e48b6ccbc3a5edceb4a81deda21c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.3 KB (669274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1810c7c00ca76e609a3daa60a2b5d403e6e6d3e70b4881c732dba3edb301e93e`

```dockerfile
```

-	Layers:
	-	`sha256:ac26501ef2da25c5b850f8f7e7c8c852dddfec44527affc01723df58fefa69f6`  
		Last Modified: Fri, 24 Jan 2025 23:55:50 GMT  
		Size: 659.8 KB (659781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aa43d9034521bba55b0aae0a80fc53a63ec82256af2978bd1db9dd47817e685`  
		Last Modified: Fri, 24 Jan 2025 23:55:50 GMT  
		Size: 9.5 KB (9493 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine3.21` - linux; 386

```console
$ docker pull hylang@sha256:bedb8f530f3485b3c99e1e1808f18dfe3361e50f42626bb927f039c4f0a976ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23109993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a67ef1e9ea4871ff937afbf2f4704c8937aa1a26a6ec894ce3c11c7ff555b8a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jan 2025 12:35:53 GMT
ENV LANG=C.UTF-8
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PYTHON_VERSION=3.12.8
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	test "$gnuArch" != 'i686-linux-gnu' && EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f195e63f2c0ffeac8eb5750e14ac43838d64a488b781b41ff48c0091c7cca90`  
		Last Modified: Fri, 24 Jan 2025 19:35:31 GMT  
		Size: 459.2 KB (459180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecac568fcd98c0fc22df58c98d7032982185516160a19e20f8b6de572953594`  
		Last Modified: Fri, 24 Jan 2025 19:35:31 GMT  
		Size: 13.6 MB (13579806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a2840d0d52e92c76298a6e96a6f136f40ad9e3d14ce11f4c18844023eaf86f`  
		Last Modified: Fri, 24 Jan 2025 19:35:31 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a732cd9f7980dbd856a787caaf7395666b93ac20c3a018771f13937ee13407`  
		Last Modified: Fri, 24 Jan 2025 20:08:11 GMT  
		Size: 5.6 MB (5607632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:93faae5d51f3860a9fa0eaf8c783264267761c2dad8ae2a4d9570fe8f2423d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.9 KB (668921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5ab0f816a7919dc549e78ae360dbee4d4a66a360b24cc0c864426daa4501f0`

```dockerfile
```

-	Layers:
	-	`sha256:ba59e996503d5e170ad11f8b88edf9a5541ff4b07e70e9120ec9b8934f33a094`  
		Last Modified: Fri, 24 Jan 2025 20:08:10 GMT  
		Size: 659.6 KB (659632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59f6a3cc194948c8b0eb4dc3360c060e3f6482d7939a090980babc87ec37d315`  
		Last Modified: Fri, 24 Jan 2025 20:08:10 GMT  
		Size: 9.3 KB (9289 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine3.21` - linux; ppc64le

```console
$ docker pull hylang@sha256:e53f30b87cfa81eb03850c5a920271c84aa45bbb6c6cd08f86370213e45e403c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23961832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ae0d86daeef8a129a059a197bd328d7774cddbdcd880e59b5acd7e60cbbdf4`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
ENV LANG=C.UTF-8
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.12.8
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd98bd85d9639dad5088cef5124b34bafc1ef08f075de94ad85e1778cc49e8f`  
		Last Modified: Wed, 08 Jan 2025 23:39:36 GMT  
		Size: 461.3 KB (461300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f25d20a5ac1c51c538314dbaf97cee1f12c9bf2fe6ee8f94a2f96ef3cec7db4`  
		Last Modified: Wed, 08 Jan 2025 23:39:37 GMT  
		Size: 14.3 MB (14318982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0372247ac8dca43b1cde1d6e362254e184bbb540e869b5f92829280a245d4230`  
		Last Modified: Wed, 08 Jan 2025 23:39:36 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7947ba22bc18451a2626d3fa83c0c43f45e0e4f20402416a90d31c63e7af50`  
		Last Modified: Thu, 23 Jan 2025 01:32:45 GMT  
		Size: 5.6 MB (5607699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:3f43b7c94420132f11a0ee16b9ed6c92a02011b7d70e4a0af1d9c4358b50a87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.2 KB (667193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a2d82082cd0849a558b677b3b0e54f828d60316675769216465fdc398d20c6`

```dockerfile
```

-	Layers:
	-	`sha256:ac79e0b02e53b02eac16d2f6760054ba1eb3d38042a15d973ce24fa392aa9bdd`  
		Last Modified: Thu, 23 Jan 2025 01:32:45 GMT  
		Size: 657.8 KB (657784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d3b6d0712a9e4c17dc4da31be5e00f7064179e5c674a99ec74c13b305463b8f`  
		Last Modified: Thu, 23 Jan 2025 01:32:44 GMT  
		Size: 9.4 KB (9409 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine3.21` - linux; s390x

```console
$ docker pull hylang@sha256:8b5fc43358fd3da6a3a0279126548befad128e1096aa37ec9c5311a5f45f1ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23628352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee1497a4e7b0fd42ae56e840b758aeec50e71b8f3d0fa77e257786523f2aab5`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
ENV LANG=C.UTF-8
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.12.8
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b60eaccca3a913528bbaa3a3ec5f33b6f8c613d50a6ce6775926b9ada7c0bc4`  
		Last Modified: Thu, 09 Jan 2025 05:53:42 GMT  
		Size: 459.7 KB (459692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fc348e67a6a3bf609377a69069af5ab938283ab3c0f5bf79b1b4b173744c49`  
		Last Modified: Thu, 09 Jan 2025 05:53:42 GMT  
		Size: 14.1 MB (14093994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4562e47bb9090190bba276b8bd9f01a4f1f79ed82732d84100c36c3f31e4cc`  
		Last Modified: Thu, 09 Jan 2025 05:53:42 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0837a305a499ab122dfd38d2c8ed1c8cdc2c5e480ae11a6617efc28b46ba7440`  
		Last Modified: Thu, 23 Jan 2025 03:05:27 GMT  
		Size: 5.6 MB (5607552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:41f67c41867e5ad5b1a1ead3f9f5111c3065416db2852960739f5cd434c4ad03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.1 KB (667067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0524f8ff098cff76c23907e337b4bd628a54214451aeaeaf25f7ea9870a1e282`

```dockerfile
```

-	Layers:
	-	`sha256:a585d2d01f23df3d1a42e0df00724fcd981ad36954140b4b5723bf5e18abc70d`  
		Last Modified: Thu, 23 Jan 2025 03:05:26 GMT  
		Size: 657.7 KB (657726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1cfcf5cd2f79cf3737545e0ae413e8ced0fe9134b16e4a371345511820546c`  
		Last Modified: Thu, 23 Jan 2025 03:05:26 GMT  
		Size: 9.3 KB (9341 bytes)  
		MIME: application/vnd.in-toto+json
