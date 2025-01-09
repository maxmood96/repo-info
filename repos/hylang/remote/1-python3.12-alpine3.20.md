## `hylang:1-python3.12-alpine3.20`

```console
$ docker pull hylang@sha256:8a61ca03b63e569c112b601514af7435f06fd754f12e12aff6679b8e98483205
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

### `hylang:1-python3.12-alpine3.20` - linux; amd64

```console
$ docker pull hylang@sha256:c427d3384c2388519bd8b6308663658218206b9a030512fd58f058f09feeae2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23225760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebc54523fdda00868d79a9ff8f2299c8c072d2cfaaf42f6a5f30b229af8ee58`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 00:36:05 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c526301b8513ae30801649155e36023ffe515e0159496e41c2eb775f0d6f99f7`  
		Last Modified: Wed, 08 Jan 2025 18:22:57 GMT  
		Size: 458.4 KB (458430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d041061154af6a5ac74c4544edc87cf4e72024e9ec42b3ed88034753fa93c7`  
		Last Modified: Wed, 08 Jan 2025 18:22:57 GMT  
		Size: 13.5 MB (13533298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd9613e12e6c3b10e188f96bdc7fe8477d200c8f25c31eda720a6ccbaec3ce4`  
		Last Modified: Wed, 08 Jan 2025 18:22:57 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fc3c3866f653e003b5fdcc79eee0309c6c95ec34413df234e512f06795b760`  
		Last Modified: Wed, 08 Jan 2025 19:16:30 GMT  
		Size: 5.6 MB (5607523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:39828b33e6065f7fa4193a8746ac32527c2c48ca112abbdb3061604da0ed8ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.5 KB (661456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e1bea4b19bb6c37228de24ade9ecf856e253f8ebb942b8fcbba440c61a93e6`

```dockerfile
```

-	Layers:
	-	`sha256:6cb5621a793fb033cbbcb122a82760702b090b2b0cab226d867cbf33a2890668`  
		Last Modified: Wed, 08 Jan 2025 19:16:30 GMT  
		Size: 653.4 KB (653419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dd6b5907b44077051286464381a187ae7852b1a06a2fbe22dfa63b96d7bb0d8`  
		Last Modified: Wed, 08 Jan 2025 19:16:30 GMT  
		Size: 8.0 KB (8037 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine3.20` - linux; arm variant v6

```console
$ docker pull hylang@sha256:0d8e2325f77cac307f1e6679f9d2b5fc64c33ab7a3996cf0d8e2d3309f036a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22520694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f5e1ed515d32e1a4c790504444b29382dd5df2884dc142e04cd067fbd69b88`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 00:36:05 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
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
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06475ab9ef588959bc9af33c0c0abe5db6fa1ce5288e003553a7a069a5c7f05`  
		Last Modified: Thu, 09 Jan 2025 07:55:21 GMT  
		Size: 459.2 KB (459192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e529945388dafb6ed36a3eaaba6a5e9dca6e16d80229427f5fc84fc0205ed52`  
		Last Modified: Thu, 09 Jan 2025 07:55:22 GMT  
		Size: 13.1 MB (13082354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6666033a65d4b48e934cd178d99a0ef88c5c88933b13535a1bb948395a9f513b`  
		Last Modified: Thu, 09 Jan 2025 07:55:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436a45481f351dfb564b2f9a98afe6b7dda97015dfb30b9ef57890d329def1cf`  
		Last Modified: Thu, 09 Jan 2025 10:10:48 GMT  
		Size: 5.6 MB (5607426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:0a0c14de8de81ddaf3ae6403a398f9a00b49d20c2350dfbf92988f1c44bfa6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38af4c3c31fbb1003322d8b5e2f943ff42da081831a5c2e55d1c9155f6092f2c`

```dockerfile
```

-	Layers:
	-	`sha256:fc247a82ec5679c74813d370be3a0a49443aeadd25f158843faa72036c0d217a`  
		Last Modified: Thu, 09 Jan 2025 10:10:48 GMT  
		Size: 7.9 KB (7896 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine3.20` - linux; arm variant v7

```console
$ docker pull hylang@sha256:3cf442d9888d2a2df497d222803946b31dea5f903ffbbb4275c3c37cc901ebf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21800062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65dbd0152fddf88d379eb024ae73fb4c8fdaf0ae275641bf905bc72644ceaecd`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 00:36:05 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
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
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00677b9f0ccf08ba448502cbc7e51e586ebd7ad9c38fa403a46937628843d8cb`  
		Last Modified: Tue, 07 Jan 2025 16:54:22 GMT  
		Size: 443.9 KB (443934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366fdfee4ab666bbe9694acb25004d40fa1e5daa5b5ba4e3ca4678f91a0207ca`  
		Last Modified: Tue, 07 Jan 2025 16:54:22 GMT  
		Size: 12.7 MB (12662281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8049756989802bc6d8f0a9f40553466abf5e0a30efe270233510706f1d7ae4`  
		Last Modified: Tue, 07 Jan 2025 16:54:21 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7af355c3617638607d0f823a0359efc69363a5519fdad46b5d8d6836d4e03d`  
		Last Modified: Tue, 07 Jan 2025 19:50:57 GMT  
		Size: 5.6 MB (5602309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:c968589f51dbb0a927bf14cea4683f3e2bae878b520707bafe4631143679a3dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.6 KB (658551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85412487f44bc0104a42d1066392b363f734bc2420533ef4d0d300d78f29dd4`

```dockerfile
```

-	Layers:
	-	`sha256:71857af4d1cd92d5165b5bea8203e11399abc7861e290425b7204a5b6e7cbbd7`  
		Last Modified: Tue, 07 Jan 2025 19:50:56 GMT  
		Size: 650.4 KB (650438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf21795a766684053dde3a620d6b63139003c9ce866017137c2b9dddab1fc6f`  
		Last Modified: Tue, 07 Jan 2025 19:50:56 GMT  
		Size: 8.1 KB (8113 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:877ab25873bceff8b5a35a740dd264648dbdf9aa8cd220b774c1a053619124cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23781313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29bc0f1752567182f8cfc8a6a9ca9e83b4197130a122a3875cfbac1cbd3c06d6`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 00:36:05 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcd6e0cbc06e1fbb5ab80cef8d41b8775ebcc00733d4f1f30773085b1216524`  
		Last Modified: Thu, 09 Jan 2025 04:46:01 GMT  
		Size: 460.6 KB (460581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b7f5bad9d75005f8afde55ea70447cf2c115a5b368a9ee2a31f26f4778d22b`  
		Last Modified: Thu, 09 Jan 2025 04:46:01 GMT  
		Size: 13.6 MB (13622202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48af7e4abc74cf9b5833de88034dff367622a39b78319f218f8873ca5fdd526a`  
		Last Modified: Thu, 09 Jan 2025 04:46:01 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843a80493d15295c258fa06b9c91f7f7ee3507a7c8071bbc4c8e486d2b9f6d3e`  
		Last Modified: Thu, 09 Jan 2025 08:22:36 GMT  
		Size: 5.6 MB (5607512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:30fc2ae8375382d791a82f01ad9688b28c9f280607766d7bc0f3fb84356e13f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.6 KB (661616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3bebe759b09c777e6e6682dab24dccd7e02c628530500c484197df311e6155b`

```dockerfile
```

-	Layers:
	-	`sha256:d23e310d84b9032293b5cb8a0ad436a946087f144cdef294fe40d9f2417e5c99`  
		Last Modified: Thu, 09 Jan 2025 08:22:36 GMT  
		Size: 653.5 KB (653475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bffea3162cc7eb934eea2ed9eb3bea48b8a03a802559efe9e1b1693533cc5e2c`  
		Last Modified: Thu, 09 Jan 2025 08:22:36 GMT  
		Size: 8.1 KB (8141 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine3.20` - linux; 386

```console
$ docker pull hylang@sha256:20a2fd43f1c5816fb9696a5f0c7c101dca6af452709c961b4835c0a441dbb316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23307598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4710e43d8b7364f97e6c3fad9be50fd48c362bb0c4b535f50c1e9a1da4985235`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 00:36:05 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
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
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622098b9e185fbd9a8e7e51d872b9b8085dbb89deec30e9273523840a39e6a67`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 458.8 KB (458846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70acae4c910c035b88f3e89628753dea791a3938a479abd55d14a1931838154`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 13.8 MB (13770054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fef38e3aadf455e5f707c4c13cf7947837693058416df8cbb3977d8cf95bb1a`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0d9e72b50140537475949b2a28fca2439a97767e98412bcc92a80ec71ff688`  
		Last Modified: Wed, 08 Jan 2025 19:17:22 GMT  
		Size: 5.6 MB (5607480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:d42cd47a18195860116cd8d27139a7affd4976fb03bbf530e2f151418d219cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.4 KB (661399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f97c19fad01e9dd04331ec369847b1df39bb3cf5e1f476c2184e2878be69149`

```dockerfile
```

-	Layers:
	-	`sha256:444f49af0997184cf857217a7f0e0c8300e123573d0bc7e894023a0731bcea63`  
		Last Modified: Wed, 08 Jan 2025 19:17:22 GMT  
		Size: 653.4 KB (653394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e84aa21ff1ba1093e8f9d8b3c7549660eb838edb395178bf890ca4ed57c9e7b`  
		Last Modified: Wed, 08 Jan 2025 19:17:22 GMT  
		Size: 8.0 KB (8005 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine3.20` - linux; ppc64le

```console
$ docker pull hylang@sha256:99ee09dcf0309f2b0afec769ea5821e8b79a2f1aa90094f73f450eeec0b96854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23912141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5372a432a3b1dc4b13a55320adaeed54762571ed2b0148f6dc8309f76576a83`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 00:36:05 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
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
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236c49b59f7bc6253ef66b11876ac777a6ca1e7bd5b4685cbf246e81c6b11613`  
		Last Modified: Wed, 08 Jan 2025 23:47:09 GMT  
		Size: 461.0 KB (460965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdff7f1851d64064df8ac9b9a1ed6153b1118e93457e277ebc9681c719be2c22`  
		Last Modified: Wed, 08 Jan 2025 23:47:09 GMT  
		Size: 14.3 MB (14269010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8843138bf0d31dacc4f28b6b2674719fd9403837ff139271f6d10e7838a3e41f`  
		Last Modified: Wed, 08 Jan 2025 23:47:09 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9e3c17f6acb64c1e7f2d1b73a776f3673434d7282df6a1cb2cf7bd7639174f`  
		Last Modified: Thu, 09 Jan 2025 03:49:16 GMT  
		Size: 5.6 MB (5607511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:bb4e85b714b7d22e947d675713156c51e897c72973f1a25f6d15d9935e87c801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.6 KB (659583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f83508312f7447d1987bdb8926f88bd9e9d21b850a8c74d8a3ccbb022f7eff`

```dockerfile
```

-	Layers:
	-	`sha256:a4ef44ccf981071d79c29f238939c6e798afcdac9b1221c925a85cce5b11127a`  
		Last Modified: Thu, 09 Jan 2025 03:49:16 GMT  
		Size: 651.5 KB (651502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f6aa2e740a9d9b15046d51f67d5bdc749ac1c41cdce1709119c42c2c46a5d5b`  
		Last Modified: Thu, 09 Jan 2025 03:49:15 GMT  
		Size: 8.1 KB (8081 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine3.20` - linux; s390x

```console
$ docker pull hylang@sha256:6df0e40eb077fda788b3f85427186b6039decf80ef218f9fda697bdf23b04de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23548190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fba2e05fef8d3c4d94a25d81a4b8741e130b0910bde65aa40ef91ed336c87a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 00:36:05 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
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
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Wed, 08 Jan 2025 17:25:57 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985cab1b685e8021d8265573dee27e7d43bce4b069c5b582887d01978fffc36b`  
		Last Modified: Thu, 09 Jan 2025 06:00:40 GMT  
		Size: 459.4 KB (459369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cadc390a6c7c1dfafddf2e3a8b8d6b952b297a6f1ca6695f81ee6c765ff9d4a`  
		Last Modified: Thu, 09 Jan 2025 06:00:40 GMT  
		Size: 14.0 MB (14017816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c9691c8de434c07cc2c6cf8d0dfbd0857eef687349de4dd836fdc88ce13cb7`  
		Last Modified: Thu, 09 Jan 2025 06:00:40 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf50297fa55fe08fd283d68eee0f9787c2b7507abb8ac168fc46ede27026aea`  
		Last Modified: Thu, 09 Jan 2025 09:13:16 GMT  
		Size: 5.6 MB (5607433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:1c1e3ccbcef27b2d6297d227d653ece99169079df288732e33e82c6626066408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.5 KB (659505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b66fa0e3e262b32f66b69bd3279ab415240c0cd2293c097fb5f35cde89eec43`

```dockerfile
```

-	Layers:
	-	`sha256:079372fe0a0e396bdc10d2db0c59bae41f542890c12b989e3a40c62f6ccf9b44`  
		Last Modified: Thu, 09 Jan 2025 09:13:16 GMT  
		Size: 651.5 KB (651468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32b88ce5f35f3e8feb9bcb6d98b8bb5fbcaa9598e4571bcfb8a0885e5e681d25`  
		Last Modified: Thu, 09 Jan 2025 09:13:15 GMT  
		Size: 8.0 KB (8037 bytes)  
		MIME: application/vnd.in-toto+json
