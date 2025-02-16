## `hylang:python3.9-alpine`

```console
$ docker pull hylang@sha256:477c8d00b06b787e571d512606c673ab3a513da25ea86053f93419323ff5dfe2
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

### `hylang:python3.9-alpine` - linux; amd64

```console
$ docker pull hylang@sha256:684c3b7e49004abcfec21339ea892e384ded2453f21056ac63c00256a6821693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22638614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5cffe01bf1887f4763746fd71838a309b093ceab01b706f35edb24147cf221`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
ENV LANG=C.UTF-8
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.9.21
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efc7c91101bd06c8dfbc2c0cf770afd96b5168c833323a8c93c10545537a5be`  
		Last Modified: Fri, 14 Feb 2025 20:36:02 GMT  
		Size: 458.6 KB (458622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9948e85d045a6a02a32794cfac4ba5d9f271f65aed76114458b1bb124fd4ea3`  
		Last Modified: Fri, 14 Feb 2025 20:36:13 GMT  
		Size: 14.9 MB (14867628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e323708b3d96d783ff338254085ca725fb5d3c1a8603100dc474063ca4aaf192`  
		Last Modified: Fri, 14 Feb 2025 20:36:01 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b812b9c2d400cf30a7ab07849f2cc38ba9ba4ae50e130719e6172fbc0793a6d7`  
		Last Modified: Sun, 16 Feb 2025 05:01:01 GMT  
		Size: 3.7 MB (3669869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:8a1add9305a9d89295557e9d065138151ae39dbfbf5d64bfd7b640157bf3cd06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.8 KB (673777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e8a755fa26eb916674fbc83290c5dd95583b06fd1dca18e15814e722c68c32`

```dockerfile
```

-	Layers:
	-	`sha256:07f1cd558ec1cc36fa09752ee18eb7b235d61728c7725053c932e03c88e81364`  
		Last Modified: Sat, 15 Feb 2025 00:19:00 GMT  
		Size: 664.5 KB (664455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c2d2346f3f2b5e56220ff408013b36b681ac034fa9c3cbe1680428121c3be85`  
		Last Modified: Sat, 15 Feb 2025 00:19:00 GMT  
		Size: 9.3 KB (9322 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine` - linux; arm variant v6

```console
$ docker pull hylang@sha256:36009e44c7fcd3352fb693ee20d00f4f6062f51def3d690a61936d4847d1512d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21915802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c816e2d21ddfe0777f47cd0191984f4d351edb44b054b5dbc42728a8952e74`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
ENV LANG=C.UTF-8
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.9.21
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a5fbd377f634bd200cb3834402a3cfe9d57ac6cb9dd5cf9fe3147bb665960d`  
		Last Modified: Sat, 15 Feb 2025 10:07:08 GMT  
		Size: 459.4 KB (459436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3f6901f709b67e92253583aae34b54fb2ec9e6c946cffd9a01e51502677650`  
		Last Modified: Sat, 15 Feb 2025 10:10:05 GMT  
		Size: 14.4 MB (14421569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473a856dae8f82a76e3b5d694db9765cc8620b35f17326e1130c3153326387b7`  
		Last Modified: Sat, 15 Feb 2025 10:10:04 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9674343815ba7e23dd1a2f174e032d3219c581347db6b4ae6e7e16fa429a829`  
		Last Modified: Sat, 15 Feb 2025 12:19:45 GMT  
		Size: 3.7 MB (3669818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:6e6c74dff2fdec31821f507de34f16f40de10c3b6d23cc9908f3e92a212a5c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2ba248d6d99e75b1b770e2657602c75f1160197b3eb96907aaafecbcc28a40`

```dockerfile
```

-	Layers:
	-	`sha256:51196efee0b7172252557a853876c57a075d963346a1b1820858bf41bbfcffac`  
		Last Modified: Sat, 15 Feb 2025 12:19:28 GMT  
		Size: 9.2 KB (9215 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine` - linux; arm variant v7

```console
$ docker pull hylang@sha256:4eefd8e531d25a1fbed2c955ca1372e37255c13530dd206a5cafd7e045631306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21257808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383b032fd4f4782a7d3f3705b54e625e5e92cd0666ba3973457dd945ee13770d`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
ENV LANG=C.UTF-8
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.9.21
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be29710354556f0f0df673704b6b540828d1087963ffd820135dfcb597033328`  
		Last Modified: Sat, 15 Feb 2025 10:09:41 GMT  
		Size: 458.6 KB (458622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e191b0947c91e4551cce9ddf9afb2d4be6c140560fbc632a7f34110a5bd50d10`  
		Last Modified: Sat, 15 Feb 2025 13:15:39 GMT  
		Size: 14.0 MB (14030900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dca530d4408f102aab3c320816f87e17528b1bfd2b2b29284c0550307d304f`  
		Last Modified: Sat, 15 Feb 2025 13:15:43 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfba3b655553079d11221487042f74f230917e7caddf68d7bd23a440afacbbe`  
		Last Modified: Sat, 15 Feb 2025 18:52:09 GMT  
		Size: 3.7 MB (3669914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:3f9a9a667b0028d0dad74daabeee79c92cd37a07de0282857691890d12078d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.8 KB (676766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2774d806796ad1ae90a9f97a623f55f8a44626968be2015a142d9aad0e73f0f`

```dockerfile
```

-	Layers:
	-	`sha256:2815123633be88dbd05709206a6e6214b3f04b6c0f9a2505b8496509b87179bc`  
		Last Modified: Sat, 15 Feb 2025 21:18:18 GMT  
		Size: 667.3 KB (667336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f06b301fdbeed8a836e96d9cae45e6f7a73e8ca606bc9e68203908ded6e346a1`  
		Last Modified: Sat, 15 Feb 2025 21:18:19 GMT  
		Size: 9.4 KB (9430 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:1d5d34da2c0027fd10b06ddddc9f2c9658359ab2687e66196a2256fcf8c72fe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23063581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c864090065bf6d7f95a2bc783e983eb76aa98214b4d4f63e385297a84555f959`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
ENV LANG=C.UTF-8
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.9.21
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60a29b5b2911d5b8ee9dcdb5f3a38f98e46d2b43ff40db6f826f5497a01cab4`  
		Last Modified: Sat, 15 Feb 2025 07:08:10 GMT  
		Size: 460.7 KB (460730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d9d160c09632a5224405e883e2dc0e371917e9288bd5beefb8195936cf21bc`  
		Last Modified: Sat, 15 Feb 2025 07:18:27 GMT  
		Size: 14.9 MB (14939700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2173f8b432fef3874d90f72331d57c37695e358027436c4a2fb7df379799f7eb`  
		Last Modified: Sat, 15 Feb 2025 07:18:16 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c25b3adebf6d6773064cee9c3994f9306f02886d03f94dadc9f32d66d73b50`  
		Last Modified: Sun, 16 Feb 2025 08:26:23 GMT  
		Size: 3.7 MB (3669872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:f2d6302e9fe3105b163b2321b3992146baa9915ba8dd5b136801a1510f49d5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.0 KB (674033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eec611a5936405877a0f37141b223394901300d8a565479607f49fa7d4329eb`

```dockerfile
```

-	Layers:
	-	`sha256:657a22e63375fced4ba2ca240ff7895b0a203017b6f1e412e42f7f93fa071443`  
		Last Modified: Sat, 15 Feb 2025 12:19:31 GMT  
		Size: 664.6 KB (664559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66a17b2016ee81a91c167aa1d4753e9353c6c17fb90b71f8398f78fa8df85830`  
		Last Modified: Sat, 15 Feb 2025 12:19:31 GMT  
		Size: 9.5 KB (9474 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine` - linux; 386

```console
$ docker pull hylang@sha256:53142e0389e9b97e63f270881e188d08fe8fe4d3e21a92fd732917ed650047ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22685251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e517ab457b239be8aa2374d9c7ab7996886771846ffd11f05ce6f1422cd22ea5`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
ENV LANG=C.UTF-8
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.9.21
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9404552efcfe261823d6f1c449c1e6f9d80b7d98b8fe759fabe74e2fb5378a6`  
		Last Modified: Fri, 14 Feb 2025 20:34:52 GMT  
		Size: 459.1 KB (459062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8db275dd076baee447f689b12af5a2e96a6479031f585035c85be7a00bf58`  
		Last Modified: Fri, 14 Feb 2025 20:34:53 GMT  
		Size: 15.1 MB (15092522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8930df28427a84751d3b4bec46ee27c2d11e096643ce66caa8b7a7e91b7f84d`  
		Last Modified: Fri, 14 Feb 2025 20:34:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f4cfbd96259ba20bb766acc2bbcb97d666863b5c895c24182a8ed440578f8a`  
		Last Modified: Fri, 14 Feb 2025 20:35:15 GMT  
		Size: 3.7 MB (3669795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:586f0fa9f1ae61864386ee7043daf597b9c0aab43f44a660263ae5558891bb03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.7 KB (673680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebae398f3a5c0d24de4f6983dc335e68d23964ed3d0f93633ae2166de1b4ed2`

```dockerfile
```

-	Layers:
	-	`sha256:fa913e3e3aa5a5b19e7fbb37cc35d866ad1ca4b9cb093e412b6d82c64426533e`  
		Last Modified: Sat, 15 Feb 2025 00:19:09 GMT  
		Size: 664.4 KB (664410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd127c162376b56d569214de6e919d1e1d9785e2342b9dd9c16895f335dd58c`  
		Last Modified: Sat, 15 Feb 2025 00:19:10 GMT  
		Size: 9.3 KB (9270 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine` - linux; ppc64le

```console
$ docker pull hylang@sha256:e82cb8f20fbb93a4d22376364a8da68b1fedaecc3b2a8d1a4862250076b3f1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23274662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9c1a0b4a290fee1f7e74d4e2b71f81a7077f34a6356ce38077419798717778`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
ENV LANG=C.UTF-8
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.9.21
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde1b426b09d99aed3ee9095c2aa945af40570fa93947d87e310bf08c98a9391`  
		Last Modified: Sat, 15 Feb 2025 01:12:17 GMT  
		Size: 461.2 KB (461167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d5f8f5fe1d2dc67171a9bc4cb512dd47946831d575e7e66c5cc4dc061aefdf`  
		Last Modified: Sat, 15 Feb 2025 01:14:01 GMT  
		Size: 15.6 MB (15568781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140c0cf41d74a1f990a36b3c75908f3bff81c48181d5c402816b6694d79ab574`  
		Last Modified: Sat, 15 Feb 2025 01:14:00 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70a474ee654b5a424a3955f06832608c6e857309430fe83a566835c7c3d9c4e`  
		Last Modified: Sat, 15 Feb 2025 04:23:04 GMT  
		Size: 3.7 MB (3670119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:94a344070bdb95b8e7ce02a7d9bf6a05a8a04d08034e6a4e43723c3b5d607d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.0 KB (671952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c787959a20865c99743882ba160014e424c5d4e0dead0c0196679c9a1543fa`

```dockerfile
```

-	Layers:
	-	`sha256:ff951bc3d123a45d5102e5198b0cf9acc12f118c13447d842528e6ff5f693f89`  
		Last Modified: Sat, 15 Feb 2025 06:18:45 GMT  
		Size: 662.6 KB (662562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5f7b4afcdef5e5830966fe11ae8485d331f93f4bac363d13c597550e963867c`  
		Last Modified: Sat, 15 Feb 2025 06:18:45 GMT  
		Size: 9.4 KB (9390 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine` - linux; riscv64

```console
$ docker pull hylang@sha256:d8ded34269897bb1472877796e7decf9f4a63133f876927d11953fa480b562d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22329771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74068f8855910db3b06492a87c567c4b51576d9968d753dc20702e82ed2e1813`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
ENV LANG=C.UTF-8
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.9.21
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b980028893d58ec8fc066f4e0114bbcda459daae354590bda3a186f1b39a1a`  
		Last Modified: Wed, 22 Jan 2025 12:02:48 GMT  
		Size: 459.1 KB (459121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1ca70bc4bf6d15a6bafaa5124345d73e90ccdffa8b68c4e3e58a5e175a272d`  
		Last Modified: Wed, 05 Feb 2025 14:00:55 GMT  
		Size: 14.8 MB (14849023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a974d8837665e78e7055367f7fbe832cc191775b61f1115ce8af9b04a97179`  
		Last Modified: Thu, 13 Feb 2025 11:01:11 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed603903ee89164366b9e2c09ed37855e54a8115c763cf52029ffe75d60bcb75`  
		Last Modified: Thu, 23 Jan 2025 01:43:28 GMT  
		Size: 3.7 MB (3671120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:f5b4ad9497583303ff4e190e40729418f776ddebc915760f4d0061168b374d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.9 KB (671942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585576f2dcb790df576545994bb500489ee9e55cd05d5d7f4368727d42c70ead`

```dockerfile
```

-	Layers:
	-	`sha256:644d5009f5c36bbcf9ba3a3c0d88a132a52da4dbd824e227af734f9cdf887760`  
		Last Modified: Sat, 15 Feb 2025 00:19:14 GMT  
		Size: 662.6 KB (662552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed27508a138d7553a75bd6b97e8592ed66ea669546cf81a59cfcad66f22808e`  
		Last Modified: Sat, 15 Feb 2025 00:19:14 GMT  
		Size: 9.4 KB (9390 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine` - linux; s390x

```console
$ docker pull hylang@sha256:8487f8e11fcb6c0aa7e0a1b4fb848a8e4bcbb814544570e7292ba545d2ca4a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22855547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:242fd8b329f786617a244fc7aa0bdefd0c096f8c36f9525029c974d471a2db24`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
ENV LANG=C.UTF-8
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.9.21
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b235a0851abb555863d26c3d5c5de5319d2090f8e05fe647e5d2a1b7441a02f8`  
		Last Modified: Sat, 15 Feb 2025 07:18:30 GMT  
		Size: 459.6 KB (459578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d928c0768333357b1f31490403c76621a2db404c81d79bd8dac2ccda83b4f004`  
		Last Modified: Sat, 15 Feb 2025 07:18:33 GMT  
		Size: 15.3 MB (15258406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec878b8883f51e825f035f3691af0a164df726426565066fa96f7bf9fb541e9`  
		Last Modified: Sat, 15 Feb 2025 07:18:36 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7431b8509e8b9b6848ac4fb441fbae8e7324e6f8fc5437996a60482d8b7cea`  
		Last Modified: Sat, 15 Feb 2025 10:36:12 GMT  
		Size: 3.7 MB (3669748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:784e5ec30cfdd82591c6e38ffb3e4b3d9847276a7a995c7295bd7b2f32fe89fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.8 KB (671826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b908371a7023f2362ccd44e5c69bcdc2d9dc62d72ea8bb49c0893287052b37c`

```dockerfile
```

-	Layers:
	-	`sha256:1c87153a9d05dcf5fc1760216eef5dc1fe557b95592ad3a9c108f4fe7695d109`  
		Last Modified: Sat, 15 Feb 2025 12:19:36 GMT  
		Size: 662.5 KB (662504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e6dc31ec76a5b265c0c9faa595c3c34079c99ead5ac0ea5a71c10f663fc84f`  
		Last Modified: Sat, 15 Feb 2025 12:19:37 GMT  
		Size: 9.3 KB (9322 bytes)  
		MIME: application/vnd.in-toto+json
