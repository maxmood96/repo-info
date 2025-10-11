## `hylang:python3.11-alpine3.21`

```console
$ docker pull hylang@sha256:a46362323fc5c07fae9a8421917f2ed87165a1a8ff3c64ddb017d2922c1cb3c5
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

### `hylang:python3.11-alpine3.21` - linux; amd64

```console
$ docker pull hylang@sha256:17f42f6bc7376e5ad1f68c5060ae62f14c3597616ec002b49d6e36969801f521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25719995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c1968a676bf78d17639bb6e5d94573f7d2b74445c2e5978f5f20b11b970c9e`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.11.14
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
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
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3ebd1ba813a1621555a6bdc18e809b8a5d0796a99ba8c4301bc7360dd33cf5`  
		Last Modified: Thu, 09 Oct 2025 22:43:20 GMT  
		Size: 456.9 KB (456884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785198da0926470a6594d5313507ec774462044ec1bdb979157fe8820e7ae3b5`  
		Last Modified: Thu, 09 Oct 2025 22:43:22 GMT  
		Size: 15.9 MB (15939602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce055d5792e4f0b5502dc6523fefecc00e214f20b6a849d84388d3af87c43e95`  
		Last Modified: Thu, 09 Oct 2025 22:43:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ba07566497fb74c35f2e38174afc303d447da25929dbea7e701adabfed401d`  
		Last Modified: Thu, 09 Oct 2025 23:16:00 GMT  
		Size: 5.7 MB (5680694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:789760571f9a512f61839354fdbb0cec3cf6e5b7237964e82261e16a7f298d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.1 KB (705138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f99936086674cad2a4f205cd4c242df9eb3a25fc0dc6723774232d4475a4a08`

```dockerfile
```

-	Layers:
	-	`sha256:36b7fdf330fb1c5c0039f026174f7e0aa12f578520b5d7c06faa13e9da4a74a7`  
		Last Modified: Fri, 10 Oct 2025 05:19:19 GMT  
		Size: 697.1 KB (697100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:251618a2d3aa3bfef6f053387545368b3affca7aa8cbb00668a2d47cae3dfc2e`  
		Last Modified: Fri, 10 Oct 2025 05:19:20 GMT  
		Size: 8.0 KB (8038 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.21` - linux; arm variant v6

```console
$ docker pull hylang@sha256:5e4f3c673ef72b9ab02f83086773c5b0de6109fa1c9574ba3347db005e7825f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (24984676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b39c5c541c05d71a7b318e426a71037bc53364fd08ad9b5b97dd8a742661f8a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.11.14
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
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
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a354d4eda470b43231cbf360a76cdb7d0ba148fa93e4cf4d4b530e71891d9c`  
		Last Modified: Thu, 09 Oct 2025 22:41:22 GMT  
		Size: 457.7 KB (457683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d8d1c4154262c8a6963f80720f54f36252f17e8e7a20e6db2323f1afdd49a0`  
		Last Modified: Thu, 09 Oct 2025 22:48:13 GMT  
		Size: 15.5 MB (15480534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bba80edf81b3f968dc3b25901f21382e8bec92bf01fbd0511647101184ac6f`  
		Last Modified: Thu, 09 Oct 2025 22:48:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b18b7a1e199eb9a2e08430d3e36ca9de69584f37c784db43c4545a4c0fa8df2`  
		Last Modified: Thu, 09 Oct 2025 23:24:19 GMT  
		Size: 5.7 MB (5680743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:6f972ff69439c132183f735f8b95cca8427ab05b713ea6beba2faed3ad8eb425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37bab3214203def5f175b2b95bf7d6e81cc33718a1a58cebacfb070f99a6616e`

```dockerfile
```

-	Layers:
	-	`sha256:0c0a20d1128056dae38ca5c859957c3e74083c68641fdaaa5eec444525e427ec`  
		Last Modified: Fri, 10 Oct 2025 02:18:01 GMT  
		Size: 7.9 KB (7903 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.21` - linux; arm variant v7

```console
$ docker pull hylang@sha256:5285f02c15fab31d64550552c6e03a622da7931f8a34e8d97cb153bd3e3d1f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 MB (24316117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b04e63ae5c49a9080216ed4a5a5da108c0fafc59eae0a39e1a297254099de3`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.11.14
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
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
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f767143e1a5a9f1fe4b0bb8a4aee64af49886238581e51c8a7942ff60577ce1a`  
		Last Modified: Thu, 09 Oct 2025 23:17:10 GMT  
		Size: 456.9 KB (456884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc14269504a0a54c27439a3f2d849a3b5e9bf36eb14c47ec4b6060822568ba7d`  
		Last Modified: Thu, 09 Oct 2025 23:17:11 GMT  
		Size: 15.1 MB (15079625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69ce804968a85bb40b010d989f742890f00909a86730af7c34830112085a211`  
		Last Modified: Thu, 09 Oct 2025 23:17:10 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313911ffc37a89a3ca4336e55476a05c4bfddbf76c167bcea39fe0db6622f850`  
		Last Modified: Thu, 09 Oct 2025 23:48:01 GMT  
		Size: 5.7 MB (5680749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:a1c6246d88fce59b4d57d4e6f43fa9056dcd517b8465517aa56708a7e1e4a931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.2 KB (708244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157ffd1d3671800e39c6b110eff2390f975d522679d0a8a542e20648343b31d2`

```dockerfile
```

-	Layers:
	-	`sha256:b81ffd832e3b537e40fd73be568af969b5e1843336ada7163a5053818f87d0f8`  
		Last Modified: Fri, 10 Oct 2025 05:19:25 GMT  
		Size: 700.1 KB (700126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2001f2b25b17531f3fa0fd6bbb4c7d543cb162e799310f3b07abb1f4e7cb97b7`  
		Last Modified: Fri, 10 Oct 2025 05:19:26 GMT  
		Size: 8.1 KB (8118 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:7d14a8d82a3786780b79b139194d3b2b4ee770cb3e9f9274c3cbeadd1fff8e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26149442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0bfc39d18f9e656252922765bc4a33471964e6f89842d7f53b3a1dd9f30682`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.11.14
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
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
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8993f3b8a7bfec7a84525bfccc40205867214442502184ea0914489e986a8d3f`  
		Last Modified: Thu, 09 Oct 2025 22:46:07 GMT  
		Size: 459.0 KB (458981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88230c87240f0a21e2a390a275bab932da9ac46e0e362e73e5ca23e882f5d0c1`  
		Last Modified: Thu, 09 Oct 2025 22:46:12 GMT  
		Size: 16.0 MB (16017027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787d785bdfd305b4db5915c306c59e7a62818b720388d879fcfa62276bff03c4`  
		Last Modified: Thu, 09 Oct 2025 22:46:07 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8253c0faa680f57189ec7e96f8d52d28c252a6d5f73af8c8746a06fea1b4fe9a`  
		Last Modified: Thu, 09 Oct 2025 23:16:03 GMT  
		Size: 5.7 MB (5680833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:c8ca3f9c3010fe3615167b8aacb4a7a2c36a829340e7d241e48eda373c41e058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.3 KB (705297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13bbd931e0a05764a5e27ccb11ee8db435fe8f49b31e81530ba519e7f1b5381`

```dockerfile
```

-	Layers:
	-	`sha256:3639f553afb2fb84b74d31cb3671f15b7e52ec6c1ff017a23eee2f42661591f9`  
		Last Modified: Fri, 10 Oct 2025 05:19:29 GMT  
		Size: 697.2 KB (697156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:930207667a4a5bb06af4faf5b34753e233c3323b7e450edfefb5e1fbdd13ae68`  
		Last Modified: Fri, 10 Oct 2025 05:19:30 GMT  
		Size: 8.1 KB (8141 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.21` - linux; 386

```console
$ docker pull hylang@sha256:043c87b08de404e669b451b26a62dd1c974d04ebb3716fdfc6fc67272f933408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25764530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd46f99e89d17c650f4d341c7e61b1e0756e6473ff552cf7ad49aa67c016fd49`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.11.14
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
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
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c65d663be7744df6357a0e4f20b46994d37f846ccbf8bfe2b1a0d3171223ff`  
		Last Modified: Thu, 09 Oct 2025 22:40:59 GMT  
		Size: 457.3 KB (457336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d9973d3b20d9be2631b01b151c44a6a20ff8569d08b55e1e28b46ab528a671`  
		Last Modified: Thu, 09 Oct 2025 23:13:03 GMT  
		Size: 16.2 MB (16161708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4ad72491b2c6026fdda93ef5ad1af31774edeef348d3f8101f8f6f8f196a77`  
		Last Modified: Thu, 09 Oct 2025 22:45:38 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f941d06603667a9edc43deb214ed9cb22064cf9baffe0d2ea62cb5ccd9abe1`  
		Last Modified: Thu, 09 Oct 2025 23:13:25 GMT  
		Size: 5.7 MB (5680531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:587a285b59b9ebd8df5c4a35bb1a0cebc1a4c1844b2e5d13b63960ba044125d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.1 KB (705081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f00b5facf0cffe9e12701e49357ffa9a5783c3b67c5f431cca1c7c412e2b799`

```dockerfile
```

-	Layers:
	-	`sha256:8736dd42ea3aa4edbf9a8ce78c318f182b67e6417634d8802a5f71ae346ca2b1`  
		Last Modified: Fri, 10 Oct 2025 05:19:33 GMT  
		Size: 697.1 KB (697075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91ca7cf0e4ed793e069dce3534da87eca10758ec2ea6b35364067e25344d17e4`  
		Last Modified: Fri, 10 Oct 2025 05:19:34 GMT  
		Size: 8.0 KB (8006 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.21` - linux; ppc64le

```console
$ docker pull hylang@sha256:957a3b33fdddf5633e10116595dac48c753da535455b2bcd9dd5ffaa72f23597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26375420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e45bc7bc895a8012c49e76c9fab48045262fd8599abb9efe819895b0ea85bb1`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.11.14
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
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
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0026c7dc43c0a7255a1ad9f4da34ccbef2597f65b422a86bda4c70ee1f6cbd4`  
		Last Modified: Thu, 09 Oct 2025 08:37:20 GMT  
		Size: 459.4 KB (459409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c467a7cfa1dad0fe6e4044aba238e1625c9bf8c7ee963c91c7d43fa429dba03c`  
		Last Modified: Fri, 10 Oct 2025 02:32:40 GMT  
		Size: 16.7 MB (16660520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bf039aff031686020bba4f77bc1c37ac8b11ef5afe9d00d6500e3a53ba1cee`  
		Last Modified: Fri, 10 Oct 2025 02:32:39 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdd606196bf3a62d66db0fa84533b58386416d9bf831b6bb5785040fb42a220`  
		Last Modified: Fri, 10 Oct 2025 09:10:09 GMT  
		Size: 5.7 MB (5681170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:a71984e4b840e4c14fa2d9e39120c7a81e6d53f7d5b56c152a045096883689d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.3 KB (703265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd146ad29dec872535fd954dc38879aafb2112c8405f4e6d51af891da482810e`

```dockerfile
```

-	Layers:
	-	`sha256:5538b1a4eda7d555e16401140f28ac5495aeb786c61c7049715187aa240cb2ef`  
		Last Modified: Fri, 10 Oct 2025 11:18:29 GMT  
		Size: 695.2 KB (695183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:913fab7519ee804c37d3bb70690cb8d6ed6530f3911d0f735734f9a102a24fec`  
		Last Modified: Fri, 10 Oct 2025 11:18:30 GMT  
		Size: 8.1 KB (8082 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.21` - linux; riscv64

```console
$ docker pull hylang@sha256:a42247833940d7069b7ec1550cd8779bcc9268201261a9c4cc415c6617cd2e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 MB (26169812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155ef58361dd02a48da1b2fb1bf3791bf936aea550556add54ae9a3003c37b1d`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 18:20:34 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_VERSION=3.11.13
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_SHA256=8fb5f9fbc7609fa822cb31549884575db7fd9657cbffb89510b5d7975963a83a
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
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
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Fri, 10 Oct 2025 10:59:07 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab0152f745fe105bd917dd035bf213e5a0afdd2b6b1e0eb9374377da919271d`  
		Last Modified: Thu, 17 Jul 2025 19:53:16 GMT  
		Size: 448.0 KB (448014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28eb6b410a800bb15388f6f435e08a65fc3ef324a0df7a78a3468696949ad49`  
		Last Modified: Wed, 13 Aug 2025 07:52:35 GMT  
		Size: 16.2 MB (16151505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae3e1dfe49cd25b596ed969f9c65cb4ccea840048ce2e0f674460914806e25b`  
		Last Modified: Wed, 13 Aug 2025 07:52:36 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7959f75b4e1de5434878b762a58f668a5a6798cf4ecfe978d6f6d33f51cd006d`  
		Last Modified: Sun, 17 Aug 2025 12:57:09 GMT  
		Size: 6.2 MB (6220953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:89807bb7d7126027e78d0703122cdebc6159c62192a082399090d70e02adc131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.5 KB (660465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9409e858ac349fe2ec563682624c90bde629b71ed57aef96bd645de74eef8b2`

```dockerfile
```

-	Layers:
	-	`sha256:93cfb8f6c77c9a0401e44d5145aee580fdad670663e08091dc96514dd67fe48e`  
		Last Modified: Sun, 17 Aug 2025 14:18:16 GMT  
		Size: 652.4 KB (652383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c020ef5555afda097aa18cd451b1731147ffcf2d6b527a5c8a1f86c135faa53`  
		Last Modified: Sun, 17 Aug 2025 14:18:17 GMT  
		Size: 8.1 KB (8082 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.21` - linux; s390x

```console
$ docker pull hylang@sha256:bbb352df4f4de3d290af04affe1088f0724977ae57992bbe3b86190bbad7d82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26019531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0491b1dc1308d52518a3124011d3d9dbb05ea6a6655777f0744f6334184506d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.11.14
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
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
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Wed, 08 Oct 2025 16:25:19 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d403476d77f3c6d174042f0a35c75c77af9283be8ed3f5fdc93ad0cd153034`  
		Last Modified: Thu, 09 Oct 2025 13:06:21 GMT  
		Size: 457.9 KB (457870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e69ef0aa4288fc8ec4f3a05567b6c2a542f655e8d7a0828c1f8b77c21aa8d6`  
		Last Modified: Fri, 10 Oct 2025 04:16:07 GMT  
		Size: 16.4 MB (16414197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92073bcf16bc3fb561e5036e117313e83e4e1cd6de8be6d1886229ab159b3bf`  
		Last Modified: Fri, 10 Oct 2025 04:16:06 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5c1dc8eee60c986444bfaefed1eb93f0df4ded535613a226ce9b1d22cbc081`  
		Last Modified: Fri, 10 Oct 2025 05:47:31 GMT  
		Size: 5.7 MB (5680782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:f0757482f89e9b042cd75de905fe8cec7c2eddcfe5f19d2cc923408f9cbf5d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.2 KB (703187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea43c1d5fc7a525fd80979a3b64fca8a944a87f17f33bda0c3a5da711089abc`

```dockerfile
```

-	Layers:
	-	`sha256:b3d0836aebbabc626037b6798fb0a65e3eefc01497e851f2f2678688167c29aa`  
		Last Modified: Fri, 10 Oct 2025 08:18:31 GMT  
		Size: 695.1 KB (695149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abd55373237ac4599a2088b4c4d01e7bce1ea1a5e290a8a5ac68774015d2a986`  
		Last Modified: Fri, 10 Oct 2025 08:18:32 GMT  
		Size: 8.0 KB (8038 bytes)  
		MIME: application/vnd.in-toto+json
