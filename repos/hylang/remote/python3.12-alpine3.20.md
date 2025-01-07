## `hylang:python3.12-alpine3.20`

```console
$ docker pull hylang@sha256:c42b5a6c9e6a4769b2534e37c55cf394db1a82de0b6e9733dc0682d0796204a1
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

### `hylang:python3.12-alpine3.20` - linux; amd64

```console
$ docker pull hylang@sha256:da6ac3287a2afb4e33570645970272c60adbe2f8ea11a258b7288dcb6c453c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23193834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67607660f0fc0f57f37d7c1c92c069666780bfab3b6bea0287e000b8602aef8`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 00:36:05 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 00:36:05 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_VERSION=3.12.8
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc529c814d5595ceff32432397b7f87bab4f63c0ee510156c5aefe063c172ed`  
		Last Modified: Tue, 07 Jan 2025 03:22:39 GMT  
		Size: 443.9 KB (443910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29961897717789797c3e28102fa55a7c89f76ce7577c3f4f1b34de0e4a57713`  
		Last Modified: Tue, 07 Jan 2025 03:22:40 GMT  
		Size: 13.5 MB (13533297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddcb051137bfbcc3b9fb6b36e8ddd20b1df506b2fb96432de7e800577229515`  
		Last Modified: Tue, 07 Jan 2025 03:22:39 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecec0168044fc675ccaa77987e177bd13a56927f6dcdb3fff255e4dbd4a885e8`  
		Last Modified: Tue, 07 Jan 2025 04:24:00 GMT  
		Size: 5.6 MB (5602379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:b737d3b9ccdd5afbe931f9c47b841a9d022bfc396cd70a1c76fdc493075515cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.6 KB (655578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de171371be47b618a0420d673e74d11a368d6f47a81f7a0f8d7a4f986fa95842`

```dockerfile
```

-	Layers:
	-	`sha256:79256c9b33c57879ed01163de27560f5aa7016d9db4790b9df3d83630b6b5fa7`  
		Last Modified: Tue, 07 Jan 2025 04:24:00 GMT  
		Size: 647.5 KB (647541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e94ce930098ea425f13403338f81fd98492bc94ef3a44f68e8b164d644a7928d`  
		Last Modified: Tue, 07 Jan 2025 04:24:00 GMT  
		Size: 8.0 KB (8037 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.20` - linux; arm variant v6

```console
$ docker pull hylang@sha256:91a447654866d60b5f7d543516420d67c0e9176cde98295af556cdeca67e3a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24591961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab0ba2e6dd5e150303f08886b78c17c50cbcaaab416059746962208489c7a14`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 00:36:05 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_VERSION=3.12.8
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9be0ab417dbcb0046d0ccc0e89ca0760a1be6e19d9dd44bd3985a517723442`  
		Last Modified: Tue, 12 Nov 2024 14:21:21 GMT  
		Size: 456.0 KB (456017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699fee07362a706a0a1f021b6c5172b83b7dc676761fc0e3303d559c096e20c4`  
		Last Modified: Wed, 04 Dec 2024 20:52:08 GMT  
		Size: 15.2 MB (15166836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42788117321a820f115a7e84c7fcf2e4f125c84b54d69b15ecf80efc5c6384ce`  
		Last Modified: Wed, 04 Dec 2024 20:52:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241d659f794d40ea52684dd099205628df4b29620478d41b2823383eaafb9bef`  
		Last Modified: Wed, 04 Dec 2024 21:26:57 GMT  
		Size: 5.6 MB (5602263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:0e2548a2e416e11fec1529ea68135cdfe5351bc5b9865c9945e1a14cfc4860ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d219c8f81043d018ee1dbc87f917bce9719315f96e57829ce3d9170c6a9702b`

```dockerfile
```

-	Layers:
	-	`sha256:04cc13acc0f4a40c2be03b2125d6bca624064b0d29da674e7f3d9f0668d07753`  
		Last Modified: Wed, 11 Dec 2024 19:31:16 GMT  
		Size: 7.9 KB (7898 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.20` - linux; arm variant v7

```console
$ docker pull hylang@sha256:49e93cdfab17f76e6b53374d36ccca55a4879e71a71378dc4dd2f0e83b4f2a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23743645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e2547d5286dca6186e85309cfe8fb4cca7906ccb38c234e135bdca8433504e`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 00:36:05 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_VERSION=3.12.8
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a7b3f0e95844a9d728ec36cd0a6d3a25cde46780e99640722e89eb89868dde`  
		Last Modified: Wed, 04 Dec 2024 23:43:27 GMT  
		Size: 455.2 KB (455165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726f57af11edb897b55f3b3cf03be12eaede2536e4c5acc2fa03235ec60c46e2`  
		Last Modified: Wed, 04 Dec 2024 23:43:28 GMT  
		Size: 14.6 MB (14590125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d28a296e86f1043115569e869acf12d75fa3039bedfcffcbcb4bfb14766f8d`  
		Last Modified: Wed, 04 Dec 2024 23:43:27 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42febebd886db51cee3dc83d9291118ef55e07c3fea85ed7896aef45b1321713`  
		Last Modified: Wed, 11 Dec 2024 19:31:02 GMT  
		Size: 5.6 MB (5602621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:dde50d6f7564ccc81c29d6753f59468f419a032ed5185443e51437da9ed25280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.2 KB (664159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51bc812c0a94a6cf14472408430cb443426350176e5edbcfe7738190764bc68c`

```dockerfile
```

-	Layers:
	-	`sha256:5d9d4c32d8ff7405d39891de992f74fc30e4fe96fa614aa2444422dcdd900b43`  
		Last Modified: Wed, 11 Dec 2024 19:31:01 GMT  
		Size: 656.0 KB (656047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06569ce87523dc9b91e43f039e7bed84bc04fd8117388f71ddd0105646dd09eb`  
		Last Modified: Wed, 11 Dec 2024 19:31:01 GMT  
		Size: 8.1 KB (8112 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:741286a17f11d8f6fa2f8ce31ca2968367a9b83f0a5c00195104c71d03fe4944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26592490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c8c8d64b9ee180bb9251663575fa5f821e9d9ac442de6c790f463296598de5`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 00:36:05 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_VERSION=3.12.8
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de61e223e3d6667838145ce293b86882fe701b04ea3217154c9de4814e37e838`  
		Last Modified: Wed, 04 Dec 2024 22:48:34 GMT  
		Size: 457.5 KB (457466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef13442fd552f1aad03f22d18a0bc51bdda770a98935cf57802cc14b624ea45b`  
		Last Modified: Wed, 04 Dec 2024 22:48:34 GMT  
		Size: 16.4 MB (16444532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3aeb98072cb2ce256c2e6fe55db32dbef1cbf3df1398b04e4610cbe1ee30a6`  
		Last Modified: Wed, 04 Dec 2024 22:48:33 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8491a039e5843fc60a3825c2d2c54b90a9428742df734ba0210c12d364b3ec8`  
		Last Modified: Wed, 11 Dec 2024 19:31:14 GMT  
		Size: 5.6 MB (5602516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:e65482e2c6a63b3e0098d2077aa355f31e203a7a1785d1a7e7ca5eab2bd5d42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.3 KB (661344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7e39f5665d5bdf877a5c626e8824cbf78a8a0e6120c594c0bca4de6fec7655`

```dockerfile
```

-	Layers:
	-	`sha256:b53b0e0a47868f25f9b620696446e2fb6e475b4cd87b1fdf7a473bd488b2b6cf`  
		Last Modified: Wed, 11 Dec 2024 19:31:14 GMT  
		Size: 653.2 KB (653203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d134863c3764ea56b754a8c8dc9288de7036f07e7758a81091965b9cce9d8967`  
		Last Modified: Wed, 11 Dec 2024 19:31:13 GMT  
		Size: 8.1 KB (8141 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.20` - linux; 386

```console
$ docker pull hylang@sha256:0565f853973b2f709d8205aad09ef5543a3b135dbc769bac7d519eec87a984ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23280212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f43b49aaa68fe54b3ac34ee33104497b03c173cc3f4cd10ad86d47ff1f6760b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 00:36:05 GMT
ADD alpine-minirootfs-3.20.4-x86.tar.gz / # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 00:36:05 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_VERSION=3.12.8
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a48310298946cd9150f3929f2f8cebe3709f1c7ecd0e99ff2b0c9b6502172586`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3463189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59143cf7bcc3acc73d98b75aa04cf126c045c292a215118fa279abca112443cc`  
		Last Modified: Tue, 07 Jan 2025 03:23:03 GMT  
		Size: 444.4 KB (444366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5aa7d943fe3c43ac512c72b7b7a2c4d31fc725eca71648fdeb50ca4e32c1126`  
		Last Modified: Tue, 07 Jan 2025 03:23:04 GMT  
		Size: 13.8 MB (13770095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8496b980bb73dd259bb14a7f3f7f5c31d51e66676cf802c8bca2a992c5a952`  
		Last Modified: Tue, 07 Jan 2025 03:23:02 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e6e2f500c3ecc9ef3ed3a0fae387eef26cb377a90fb036d543ab63c58036f`  
		Last Modified: Tue, 07 Jan 2025 04:22:33 GMT  
		Size: 5.6 MB (5602307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:8c1d9888db216dddb6990ef0409225b40b3312254cf504bfa4da76e851166d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.5 KB (655521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9025d479dfc97fdef69f5876322b9d8d8de75c307599fe22a30bd51e2071daaf`

```dockerfile
```

-	Layers:
	-	`sha256:d6a56bb6145dc55fa63241bee15d0b7c1d9c95feafe0e99397db6ebcdd57d11c`  
		Last Modified: Tue, 07 Jan 2025 04:22:33 GMT  
		Size: 647.5 KB (647516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b008a26207b6f7566761ee44b068235e892f9f1c3d86ac8c4c7959d6a1dcf2fc`  
		Last Modified: Tue, 07 Jan 2025 04:22:32 GMT  
		Size: 8.0 KB (8005 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.20` - linux; ppc64le

```console
$ docker pull hylang@sha256:c1274e069d14074f0e3c75aa90985a062cadc4c65ec861fa5381da4bda26b1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23885894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4047a93732df184050db0a1495c8624c1f227b55e2aca2c91e1f4c9af233bc79`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 00:36:05 GMT
ADD alpine-minirootfs-3.20.4-ppc64le.tar.gz / # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 00:36:05 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_VERSION=3.12.8
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c96bc34ea0111931eae2007b7db67b205ebd3c8a096d711e1be59e48f25006a3`  
		Last Modified: Tue, 07 Jan 2025 02:32:24 GMT  
		Size: 3.6 MB (3568727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5874797fd4d5c5516c705b7850433463089259824f2b1147ed89224c9b8ac04c`  
		Last Modified: Tue, 07 Jan 2025 08:30:48 GMT  
		Size: 446.5 KB (446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcb5d705f4ad084f3cd5c75d8e25706bff70d4212f7f4be0e1bf0db94edf337`  
		Last Modified: Tue, 07 Jan 2025 08:30:49 GMT  
		Size: 14.3 MB (14268249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acefb8484ddd7c7795927e19611b07176fa7caa0421e67380d778d61e739dfbb`  
		Last Modified: Tue, 07 Jan 2025 08:30:48 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254e60c2c5107d5d10865873fe9c753c242a25956e18a9e229708c03117b5601`  
		Last Modified: Tue, 07 Jan 2025 11:40:06 GMT  
		Size: 5.6 MB (5602147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:e4044bdcbe655bfc19a0277ff1df9c049fdf017210a1f3c7299916b6fbe51b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.7 KB (653705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4314ce5d9f13afd5bf442163a1c3b16055e83e8220407d600505673bf8dd95be`

```dockerfile
```

-	Layers:
	-	`sha256:fc1db6bb0d51647b044bc1a1cd6ee15a0bb682053a5b830c1c49494163ca81d0`  
		Last Modified: Tue, 07 Jan 2025 11:40:05 GMT  
		Size: 645.6 KB (645624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebce064168fbe3941ccd342714081a27202f5bc3be03e7eec0cc9463e8c8a85f`  
		Last Modified: Tue, 07 Jan 2025 11:40:05 GMT  
		Size: 8.1 KB (8081 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.20` - linux; s390x

```console
$ docker pull hylang@sha256:cc3ef7bf26517b653ac6ab24b736aae08158780609b0e7aaf1bfbf8152318900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25698312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390fc67d0a62dbca46bb25f10e60475a5aa68ca51b6f4055f8073a4f2276c192`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 00:36:05 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_VERSION=3.12.8
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886581440a7387e35ae0982554985be4e50cddce78417dd941ff973243ed63d3`  
		Last Modified: Wed, 04 Dec 2024 21:48:53 GMT  
		Size: 456.1 KB (456137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3369a5583da6c7edb8c90effd8c09424a0aebacccc03771bbc4aaa63cc655677`  
		Last Modified: Wed, 04 Dec 2024 21:48:53 GMT  
		Size: 16.2 MB (16177981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42caea76093770fc026cbbd13fd12327e96b480f20b8e09e8c631a5bb7083575`  
		Last Modified: Wed, 04 Dec 2024 21:48:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68b99f7821ef29de3b41f532ebb08911f244e454731a19e36e4038088e52063`  
		Last Modified: Wed, 11 Dec 2024 19:33:06 GMT  
		Size: 5.6 MB (5602337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:a78d7a3487e6ca927a704209539a362ded185d4dbeccb57a41f1de97b2859540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.2 KB (659230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e09a9083d88c79df67d02fd7cf86c97e7f4b0286a592ab68abbe12fb8a71435`

```dockerfile
```

-	Layers:
	-	`sha256:cef51f8f8d00db287de5bfd4110de3e77ac66aacc05a1e5e7cef92369c946e87`  
		Last Modified: Wed, 11 Dec 2024 19:33:06 GMT  
		Size: 651.2 KB (651193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b10ee6d82f64c4666c6c504a8e0dbbf6a7f523bd89ded079245bcb412683256f`  
		Last Modified: Wed, 11 Dec 2024 19:33:06 GMT  
		Size: 8.0 KB (8037 bytes)  
		MIME: application/vnd.in-toto+json
