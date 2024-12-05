## `hylang:1-python3.11-alpine3.19`

```console
$ docker pull hylang@sha256:eecdd84f3867bd27fc4d59e4410a10c8021eaa20de1868845bbf39865d72e90f
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

### `hylang:1-python3.11-alpine3.19` - linux; amd64

```console
$ docker pull hylang@sha256:9dbc7eac2779f1b3f8d1450bf63c5ed2158c4575067964a579b796c22b5db2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28578152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1dcd94ead09c5fcf59ebde175b16b317c9a8691ade01dfbbb9873bfc47e5e96`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc7acfc3979528917defd79f3d763a45162ccdcac0c48eedbae53229c9aa460`  
		Last Modified: Wed, 04 Dec 2024 20:36:01 GMT  
		Size: 627.9 KB (627932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbdc450a23822fc091c5641a4a7905f54ca26e04c68019d16d815bc489479ea`  
		Last Modified: Wed, 04 Dec 2024 20:36:02 GMT  
		Size: 18.3 MB (18312181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a01739510fb7d2e8262d77a9201ded1e22201ca926e41a3109a1672624b2bfd`  
		Last Modified: Wed, 04 Dec 2024 20:36:01 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1198749f96d55c6a9c065ae46a27fefc56174aede8ab136394abb9852731aafd`  
		Last Modified: Wed, 04 Dec 2024 21:10:18 GMT  
		Size: 6.2 MB (6218062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:e3eaa62d3d8757e8e3376604895e7285675b150b64d2d4bf0ba6c6e37d0746d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1044063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302a6f5550081df415db585f488e3dbb544dc86c5083f7596f6b86e297a4cd97`

```dockerfile
```

-	Layers:
	-	`sha256:9baf31a330f7bd8f088370342d51336c500a860b22bb71f429b318ff0df3a649`  
		Last Modified: Wed, 04 Dec 2024 21:10:17 GMT  
		Size: 1.0 MB (1036026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c847de0271223688e79ddde60f8a8afedf9bee5bed60143fcfe09b1587c8f0da`  
		Last Modified: Wed, 04 Dec 2024 21:10:17 GMT  
		Size: 8.0 KB (8037 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.19` - linux; arm variant v6

```console
$ docker pull hylang@sha256:d4307a013d7351612170cf1cbfad2274bff7ec8745eee6d7890823d863e8b7bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27596701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3453a108944ffe748a4fa93bf6b1aaf6c5def1248f05b474e3360e2b0ffd81`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2431344f9ef4c8213d672cda2b6e387e95583c1e88274bffbb69202bfcc5ffc7`  
		Last Modified: Tue, 12 Nov 2024 14:28:12 GMT  
		Size: 628.8 KB (628823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac27cdb810c9a60aa54fbce11117e787d4ea2de81b768a3f096a971b1ffde1c2`  
		Last Modified: Wed, 04 Dec 2024 21:12:31 GMT  
		Size: 17.6 MB (17573063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e5d789dc27bfb18d3221165234cfdff0dbe39e91fd7ce0c463a3adb8a5b49f`  
		Last Modified: Wed, 04 Dec 2024 21:12:29 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08d7d00c797ec36fbd88cd9cb9189f3d0b66a014cf70779f46273f86294a8e6`  
		Last Modified: Wed, 04 Dec 2024 22:08:02 GMT  
		Size: 6.2 MB (6218132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:4d052c09bb9c78e4d31566addf33bdd6933a066e86a8cf6861ce0e96fd06284b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ed8e02861064285ab288ef8997796a7f05ba7d0e3a58d7beab0bc8e46dc51d`

```dockerfile
```

-	Layers:
	-	`sha256:e7a04dbed8616b1b86d2a738bae728d821c8b410057c8d45e1911282078533b8`  
		Last Modified: Wed, 04 Dec 2024 22:08:01 GMT  
		Size: 7.9 KB (7899 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.19` - linux; arm variant v7

```console
$ docker pull hylang@sha256:8da6ab2c3d3ad96deb3520c45c72749609778df6fa9eea3599e3ab4e8a0b5c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26804938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dadeca2300da885d45c18ec58de7788c3bfb04ab1c16df6bbc4cb4a11595088`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:02dfd5e2e7e47e8d8f9020a0d7f4d8240d6646afc6a52b168c0899bc0c3d06a3`  
		Last Modified: Mon, 09 Sep 2024 07:03:23 GMT  
		Size: 2.9 MB (2927731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c2f9787048526330ac7cda8db975c894470c98d98a1f85506dcce30d2b788d`  
		Last Modified: Wed, 04 Dec 2024 23:50:18 GMT  
		Size: 628.0 KB (627971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67f42b0ff6780c1d12054ff842d726158928965688137e3b0c93d2491bdf5cc`  
		Last Modified: Thu, 05 Dec 2024 01:18:58 GMT  
		Size: 17.0 MB (17030850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713eb644fabbbc60f7748c5e3b96fe120a9ab6580790fdaaf23db15a23776dea`  
		Last Modified: Thu, 05 Dec 2024 01:18:57 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389ec2c8a80c08a1e49a8c8ad7395b35eb702a8762f18509dfbacfba2e7cab43`  
		Last Modified: Thu, 05 Dec 2024 03:08:47 GMT  
		Size: 6.2 MB (6218137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:e9d4006bfcd5a38759ed12ebc44175c5dc16ca0ab9be0d5a4a7601c2afdfd0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1047040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff3eabf839905f0962d7c399346f6e8cf270a31c3af4ef6bca70da89857157a`

```dockerfile
```

-	Layers:
	-	`sha256:70500cc785911b4226fa660fc0eeb35528aea2ffe4483fe2940433bcffce6df2`  
		Last Modified: Thu, 05 Dec 2024 03:08:47 GMT  
		Size: 1.0 MB (1038926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78ca358dbf6cfd5c20c86a37da19110e943a819a862f77b1686ce7ed1fcd91f3`  
		Last Modified: Thu, 05 Dec 2024 03:08:46 GMT  
		Size: 8.1 KB (8114 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:7f42ff28fcb05377462245497e3b8069984b2cb7493007fb3102daae34298e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28532031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8acafcd6688d3075f6531d4d2b09872992d97ac63fc8c0beacac103bf8bbe36`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8807c905fe7992682192bc630b9c68d1ca8b7b640529650c9556b2c63601bac1`  
		Last Modified: Wed, 04 Dec 2024 22:54:27 GMT  
		Size: 630.3 KB (630347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d374e7163d6fba55ea15507862a4dd09bf89dd1a221a912f5dc85d6ef39cb2`  
		Last Modified: Wed, 04 Dec 2024 23:52:31 GMT  
		Size: 18.3 MB (18324127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a616418df1c34eb61b49ac60099774a594d94d988a23a25a517b4cf1b40faca`  
		Last Modified: Wed, 04 Dec 2024 23:52:30 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385eb6cd78d8f9b97d0355532f65786f438ce46628382e3b2340b0b47d086c8f`  
		Last Modified: Thu, 05 Dec 2024 01:13:47 GMT  
		Size: 6.2 MB (6218061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:b986c878260fe8c20e54fe9b10e4b769172c1598fbb4796b8b80bb055cc7c9a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1044224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:853f26c1a6c5c51311907318d28716ade0fe3ac08de506f28c121594e90ff101`

```dockerfile
```

-	Layers:
	-	`sha256:6d39ebc31597dc52cba61883eb7e92bf2b99e3daf447206c321e8114e711c245`  
		Last Modified: Thu, 05 Dec 2024 01:13:46 GMT  
		Size: 1.0 MB (1036082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7d58b63d6d2fb21f4403f17dd6d20d2e0add861e7bcedb5edbdd1c537b5422`  
		Last Modified: Thu, 05 Dec 2024 01:13:46 GMT  
		Size: 8.1 KB (8142 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.19` - linux; 386

```console
$ docker pull hylang@sha256:7413231906cf2fd624024085e0358140c81a303d2f5cf5e09fdc21f98d85cb8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28459109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ef8a403368a26b5ab7d2d54e61dd56009b4395728be0233e7d3929be0d8c13`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c986bb5c208d405125b114af8105cd1e2f09af7807dbecb699f912963f37f4f`  
		Last Modified: Wed, 04 Dec 2024 20:36:40 GMT  
		Size: 628.4 KB (628416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0250929f27e126a157abff9f8dfaabc600c93de38836a2f5db1f24c69d668ffa`  
		Last Modified: Wed, 04 Dec 2024 20:36:41 GMT  
		Size: 18.4 MB (18358636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bef989402a1664af5e172567dbb91c6145119023946a2930ecb24b5d54187d3`  
		Last Modified: Wed, 04 Dec 2024 20:36:40 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50826e38375e5cb8d9a423861db69b13e79453e1fdf4617de4b8105fb5177705`  
		Last Modified: Wed, 04 Dec 2024 21:10:19 GMT  
		Size: 6.2 MB (6218139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:0f1a97b48d322590396a8207727fb0bd3b22b35ecbdca2e74633e7b1eec111f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1044007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b42c7d46341840a5d8ae84dc39f6bd5436439b3777d0e81b6eabb4e73961cc`

```dockerfile
```

-	Layers:
	-	`sha256:73bbbd950f6d1406344d8224437f5b3731ea966a5b349824bb2baa24766aff75`  
		Last Modified: Wed, 04 Dec 2024 21:10:19 GMT  
		Size: 1.0 MB (1036001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5bf10b80b92736bcad2fc4cfd86dc52f060b6c527e2572ae279743c87d9777`  
		Last Modified: Wed, 04 Dec 2024 21:10:19 GMT  
		Size: 8.0 KB (8006 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.19` - linux; ppc64le

```console
$ docker pull hylang@sha256:5735f9bf158f47d8032006650eb5545e7c6a02709cfce69736347d93ec795e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29113352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226873a922fcda1d778f7e6ae9c411ffc8492a4ec788a5624b04b10b2882ef93`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a3b208fb93d4b6ab11a15715a17ef854a2307e9102b287f01460c628f471ab`  
		Last Modified: Wed, 04 Dec 2024 22:06:33 GMT  
		Size: 630.8 KB (630823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437f11b017c84b259ebb168a64cbb05c12537ca0be2639f27c5439338eba003e`  
		Last Modified: Wed, 04 Dec 2024 22:54:19 GMT  
		Size: 18.9 MB (18899724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c1c7eeacb34c5b8da95bd301343784cab24b96dfdb022a40b5fbe5166fdcce`  
		Last Modified: Wed, 04 Dec 2024 22:54:15 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5be6b39047295cb1d61b0b62efb5882c69806f713a2ea25067f238d46001ea`  
		Last Modified: Thu, 05 Dec 2024 00:09:39 GMT  
		Size: 6.2 MB (6218057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:e8aa632dada97ff3d8c15f678a746d2a11b1692be638c8e8ed4689c7a0cf34d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1042188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9600cd5ebe9b0c66381d97bb971f8941d9255da3686a21f59c37eb2967195870`

```dockerfile
```

-	Layers:
	-	`sha256:2db09adfcfa5d63b3d029dc7d20ae048fabf40daa920a6bfaf07a627b94572ba`  
		Last Modified: Thu, 05 Dec 2024 00:09:39 GMT  
		Size: 1.0 MB (1034106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7e5a0f2345d030c16a13a0b9ba0ee7dbb17d182be6f634cdb8cc0e87de3521e`  
		Last Modified: Thu, 05 Dec 2024 00:09:38 GMT  
		Size: 8.1 KB (8082 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.19` - linux; s390x

```console
$ docker pull hylang@sha256:aa2d6b6ecdcdcc356a9cff2380f49e2bbd2d91ee2f54af6ec29bb605fe8b0bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28635181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49900fb8a6570109305be2a29f584bcc0265c12607c610f471676c8c3675f194`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958d33515d223f7b57730bc71831734e07e677ed82e4f416a0ad37a98d1e7fee`  
		Last Modified: Wed, 04 Dec 2024 21:56:21 GMT  
		Size: 629.0 KB (628997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cb0048cc75730097ad2717b7ea40853a4ebee14b4960c4cb886ec56ec2a7c6`  
		Last Modified: Wed, 04 Dec 2024 22:38:46 GMT  
		Size: 18.5 MB (18534428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3f9ffc740f74eedd47dd08918e7dd59ca2eee9ec46517fe1e8f0fac8997bfc`  
		Last Modified: Wed, 04 Dec 2024 22:38:45 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fcedf3507d619d6557ab1310d0deaf4e900907f00d76b49d3b3b9cc5495596`  
		Last Modified: Wed, 04 Dec 2024 23:48:46 GMT  
		Size: 6.2 MB (6218111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:1d799569322b8d844f4a7ef0ede3843bf6dfb47b3745384d5f511e701877bf33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1042110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec2a464d7a913f4dee870257787844c4e396f3d53372a55665b74cfef9642c7`

```dockerfile
```

-	Layers:
	-	`sha256:edadb815dedc8ab30d03d86243c0f244cb3a701af24f95dd355ac97860b1c158`  
		Last Modified: Wed, 04 Dec 2024 23:48:45 GMT  
		Size: 1.0 MB (1034072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b9971d25fe0ecb79311f906a69dccb7bb45b79501e55aca1e6600b5f41d11a2`  
		Last Modified: Wed, 04 Dec 2024 23:48:45 GMT  
		Size: 8.0 KB (8038 bytes)  
		MIME: application/vnd.in-toto+json
