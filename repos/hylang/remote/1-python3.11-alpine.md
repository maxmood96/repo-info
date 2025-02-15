## `hylang:1-python3.11-alpine`

```console
$ docker pull hylang@sha256:4e5d38c937ec70dbc444f14278bf1ebe37b3faf7916893ce077ea55f77345b19
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

### `hylang:1-python3.11-alpine` - linux; amd64

```console
$ docker pull hylang@sha256:34b3cd771e253a350aed68bad0fae669cc3b48089a799d9e1657b7f52c3b7c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26528211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0660ecc4d9617aa171b2fcac243355c04b1bbd12de5d4a18dd771096d47987a0`
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
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.11.11
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:4bf0423a57b10233f485650edf888de41db5d8d25f63a1635c1e869fb2fd0162`  
		Last Modified: Fri, 14 Feb 2025 20:35:48 GMT  
		Size: 458.6 KB (458620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3746672e3ddae3ce820ad4aa209ea746304e5b6561da73486d5d01489f66d76`  
		Last Modified: Fri, 14 Feb 2025 20:35:49 GMT  
		Size: 16.2 MB (16209049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aad0d33617a1b09816fdedc13afa40a6d83ba70759183d162989213061fd836`  
		Last Modified: Fri, 14 Feb 2025 20:35:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce1d1156d47190649c3b9f2144a1df146075c37f537de301a39ad59a2c23014`  
		Last Modified: Sat, 15 Feb 2025 09:22:35 GMT  
		Size: 6.2 MB (6218045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:5d1d425a1db83d10a21406dc0caa8dce4ff65b9d868c78f9c25ff8dd7d9a8296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.8 KB (673823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b104162df86d2d62e70755f968c28a592be8e1ce7ebab61a5b0d2aa63f7df662`

```dockerfile
```

-	Layers:
	-	`sha256:c98c870541642d2450ca9af612c27764a0d5777a80813c120820ed3efce1a015`  
		Last Modified: Sat, 15 Feb 2025 00:18:09 GMT  
		Size: 664.5 KB (664481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9e1aef577bc774b2f9fe7cd765acbdae2f9b4b27eaf1c9ec4b360d9a5946eb`  
		Last Modified: Sat, 15 Feb 2025 00:18:09 GMT  
		Size: 9.3 KB (9342 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine` - linux; arm variant v6

```console
$ docker pull hylang@sha256:487d290538ed9e651f63f1623d7bb4b7cf9c84365077f8e50eb415c9a598f945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25795194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e91229111dc01f6698a82fa1adf972ed30241f2a31440483777ea6643284aed`
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
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.11.11
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:d9f54796b1fcef7fb649d4c39a3f3f10e64b7f916cfb37df951a2de2131ec7a7`  
		Last Modified: Sat, 15 Feb 2025 10:07:42 GMT  
		Size: 15.8 MB (15752840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ccbcc200ac357890fb893f49d8d89203c01de9e158967965c0fb44cd88da67`  
		Last Modified: Sat, 15 Feb 2025 10:07:42 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6610c6590c4215346a8104ee009e2125631eb23ad3f1d06ffbb2798be5bef8`  
		Last Modified: Sat, 15 Feb 2025 12:18:42 GMT  
		Size: 6.2 MB (6217939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:9d3a39a9aa83dc58e1b76d4a2963d11798760a9dfdeeb65ac89913da2cc081c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8142fd1abd9612415839105fb33ffb848ad3aeecb85b3714992064dec0ec54b4`

```dockerfile
```

-	Layers:
	-	`sha256:478a2f3e0aae32e239aa0a8495874a4436a78a550d23286e9aee4204433e923d`  
		Last Modified: Sat, 15 Feb 2025 12:18:26 GMT  
		Size: 9.2 KB (9235 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine` - linux; arm variant v7

```console
$ docker pull hylang@sha256:e429a2bb959f464538dca19de0aa7f084c59a87471888367aba0a70370a1f1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25128679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d810b054e896100aff6d575c62dcd31c48340ae8e75c26287b999ebbda0889ea`
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
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.11.11
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:81f488142981fd0ce3340d9080e3a8dd0c0239067cc4d56f0c6d6c477c88ec45`  
		Last Modified: Sat, 15 Feb 2025 10:18:13 GMT  
		Size: 15.4 MB (15353662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a18dd6624541d401428b3692a4a179a96e34b169981ea27f971e7b45c3e5048`  
		Last Modified: Sat, 15 Feb 2025 10:18:12 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de15eea399f5cd6e48135fab382778c239cec2d36e4504048f11a30c570552de`  
		Last Modified: Sat, 15 Feb 2025 17:52:43 GMT  
		Size: 6.2 MB (6218021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:407846e6d65a822607006e78bdefc42e7631911d66988ad0e8e507a6cc0f0182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.8 KB (676812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1def9687545aaa22957884ddc0238c4db4896590599dfa50b10b26c0682c3307`

```dockerfile
```

-	Layers:
	-	`sha256:7a9014720cd3be48e6c85b963743996f7a45c6573185cfbc90f2887f13c789e3`  
		Last Modified: Sat, 15 Feb 2025 18:17:52 GMT  
		Size: 667.4 KB (667362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a44540354641fadfef3b5e689ba29cdb0e1c4d2fe12e1920c8325b61ef153cc`  
		Last Modified: Sat, 15 Feb 2025 18:17:52 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:a34001ee1588c1fe1347f32f37d357e2df2b73ef9bcf762103f8c6611087ee2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26959123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b381c0daacddd74bd5a28b29a992cfb5b0a1a5f23f4ede2f6b0b54ad813a5ad`
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
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.11.11
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:9d6ae32e6d0ca0eea4a50b13d3f13b38a4a9dbe96c017f4e0a0b7f5c4332bb5c`  
		Last Modified: Sat, 15 Feb 2025 07:08:57 GMT  
		Size: 16.3 MB (16287338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2040399d367885280bf056dac30a300e402199411e61436220db403496a0d709`  
		Last Modified: Sat, 15 Feb 2025 07:08:55 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7590855920d8e4e6a0ddc2d54413ecdc361d64157ded4ea2ac30fdc2966824ef`  
		Last Modified: Sat, 15 Feb 2025 20:16:40 GMT  
		Size: 6.2 MB (6217777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:0ee426ca8a805c6e5115a5eb1b747d9ddc4a6e9731d1d784d4e13c2775c4b811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.1 KB (674079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfff4d6993ed20e923c400b088b97e6b29bcb4f0a6de10b5df0a2469cbd6b5e1`

```dockerfile
```

-	Layers:
	-	`sha256:20ab60a1dd8c4a95652bc54f5d1ca740b927ad6ab6810ab242d9ba3f530b8b50`  
		Last Modified: Sat, 15 Feb 2025 12:18:29 GMT  
		Size: 664.6 KB (664585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e167b63c7d2055ba332aacab3109bfaabdc09008a27c28cd84f2ad6ef612a54`  
		Last Modified: Sat, 15 Feb 2025 12:18:30 GMT  
		Size: 9.5 KB (9494 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine` - linux; 386

```console
$ docker pull hylang@sha256:4b35da2a086815b1ce78a8bd0ab8d73ff7d06945903271bc42f3ee23134d845c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26570482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efab35b5b8d6126eed7846f5a13f13cde73c6ccef25ab50fbf4a471ad6858634`
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
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.11.11
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:b4145c24f6708864107c5d7ba89c67d4ca7193381fe495ddeb0e456f30b8f466`  
		Last Modified: Fri, 14 Feb 2025 20:34:46 GMT  
		Size: 459.1 KB (459059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a24997bdb815a531a5a012192e54373679851e6b3b15862dad9e895fa79ed5`  
		Last Modified: Fri, 14 Feb 2025 20:34:47 GMT  
		Size: 16.4 MB (16429492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22be7a65a274c2259c59847fc37a9e1a329dac222ee3be3822a77f040e7aedbc`  
		Last Modified: Fri, 14 Feb 2025 20:34:46 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82896f4d01ebdbf60da41559a8c8002f4e7e9eec5c49002d373d6715c86dd243`  
		Last Modified: Fri, 14 Feb 2025 20:35:10 GMT  
		Size: 6.2 MB (6218058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:7171257e4d132a6cea7402a9591b731d4e5c42e8376e36b5c3cafbb84c529411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.7 KB (673726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d67c02a677a6cc3569af357668e124f5130db736d9393a3c6e97a183659387`

```dockerfile
```

-	Layers:
	-	`sha256:4ea531a41e3e1b4631e6f4a4c0a32aa564c2c980070bd9467b5394c2c7b0deaa`  
		Last Modified: Sat, 15 Feb 2025 00:18:14 GMT  
		Size: 664.4 KB (664436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c91d127c6fddd948fafeee251f260089620df8621edb651213bb125d74bf38a`  
		Last Modified: Sat, 15 Feb 2025 00:18:15 GMT  
		Size: 9.3 KB (9290 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine` - linux; ppc64le

```console
$ docker pull hylang@sha256:f1771530de93013d30286bbe02fadb18caa420447532eca9b7e1e8b28dc256cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27186988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c581871948dc01c1b5c10dcf319e98cede636903deac910fa732c058e481286f`
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
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.11.11
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:2c7c13dc10d3dfcbdea3dda5e73d74a95bbf2007465c66d0d5ceee0a36fc7dbc`  
		Last Modified: Sat, 15 Feb 2025 01:12:48 GMT  
		Size: 16.9 MB (16932941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c16f178ebb8e13b2e299cb3fb8940d99e8a9e462a759076c9c4828212ca8db`  
		Last Modified: Sat, 15 Feb 2025 01:12:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c17d81e248cfffd5348a09f9cf466e5da884d628344cc4412bd33978d431ce`  
		Last Modified: Sat, 15 Feb 2025 04:19:28 GMT  
		Size: 6.2 MB (6218288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:c3f66ba0b39941f39bfaffacf33281a1121a34b7ec8704888c87a3dfff3dfe2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.0 KB (671997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:841e8a3924a74032357b90bbf08426bb06167d4937864ae64f841070eb4d6d78`

```dockerfile
```

-	Layers:
	-	`sha256:3ccfd60fbfc95b692f37c1fc3b1b6568867aa7a7db3a7ff4dcaa2acaeacf33fb`  
		Last Modified: Sat, 15 Feb 2025 06:18:03 GMT  
		Size: 662.6 KB (662588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:794035e2bdeceb62261df818dd7570e8648d3fc52011ce91efae6be4555aca82`  
		Last Modified: Sat, 15 Feb 2025 06:18:03 GMT  
		Size: 9.4 KB (9409 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine` - linux; s390x

```console
$ docker pull hylang@sha256:4f191b3b47bc35c636b95a0067af94cf104dee3047a3a553957bbb88d0e989fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26831295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930cda5c367169fc3a7dec0b78d6b79ce91afa3feb1c7152470198a2828e5528`
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
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.11.11
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
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
	-	`sha256:50bdd432499852d71732543a75fdfcffde844ab355a6a666c4ade2e314c6366a`  
		Last Modified: Sat, 15 Feb 2025 10:33:24 GMT  
		Size: 16.7 MB (16685901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c9ae7ba7bfdf37a8a627590736135000628c194f3e90007ffbaa3a008d0794`  
		Last Modified: Sat, 15 Feb 2025 10:33:28 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535856b05bac921ced289aa3019e1b2468feb599540fcc515a04358ae1d0c13c`  
		Last Modified: Sat, 15 Feb 2025 10:32:55 GMT  
		Size: 6.2 MB (6217999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:7c987f14ef4c76bd284317b529d3e56873aff2e1fb0ab2fe47e1b78d426758d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.9 KB (671872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3ade73c7276189db0a34d3b9e9b3f319ebd25fcc6ca08086af414b986cf012`

```dockerfile
```

-	Layers:
	-	`sha256:fef38ac0cab054840adaeb2b13bb63688e159804af57613cd4a946865082c6d1`  
		Last Modified: Sat, 15 Feb 2025 12:18:34 GMT  
		Size: 662.5 KB (662530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d094d5d0a1aeffb1125690c18feb52859f74b1ac29720fbef0309eaa47f5e574`  
		Last Modified: Sat, 15 Feb 2025 12:18:34 GMT  
		Size: 9.3 KB (9342 bytes)  
		MIME: application/vnd.in-toto+json
