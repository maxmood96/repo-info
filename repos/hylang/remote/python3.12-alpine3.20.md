## `hylang:python3.12-alpine3.20`

```console
$ docker pull hylang@sha256:2d52759042fa2294a343cefbcb31d61729bd3dc35b7d095470b7a6f76abfc6e3
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

### `hylang:python3.12-alpine3.20` - unknown; unknown

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

### `hylang:python3.12-alpine3.20` - linux; arm variant v6

```console
$ docker pull hylang@sha256:60c6fcb5d5e1881f3d052c488e90b786cbb6688977293c2dc07af3576cfba987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22493175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5baedc60eb1519398c967f372884610c2a9f2fe7b9a127e00be2f9734592b82`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 00:36:05 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
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
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a987a8d3b34b4101f1f618e5340eb174b6871d02a5c70353eb79a667003bc8a3`  
		Last Modified: Tue, 07 Jan 2025 17:10:13 GMT  
		Size: 444.8 KB (444782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571bcd4e122a35883c7ea44e4bca85cb3c92577e75d4597509667945dcaeda8a`  
		Last Modified: Tue, 07 Jan 2025 17:10:14 GMT  
		Size: 13.1 MB (13082006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089fd428e014e2697ccc6885a2b1447e8fbad68347f99989a1db628ca97cffc3`  
		Last Modified: Tue, 07 Jan 2025 17:10:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89e7c22dc08cdbca05631c39ebd3b49f822ce7e04130d80b8bad28490228323`  
		Last Modified: Tue, 07 Jan 2025 20:31:26 GMT  
		Size: 5.6 MB (5602196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:8d414358f1cd72a6432d53bd9d96520d41bb9817b06f55fb1a0c0b77a14f9e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36317c1d00836b51056e4a3b33ca8aa90fd87817e9ade2497290148bc14ca3d`

```dockerfile
```

-	Layers:
	-	`sha256:fc7efda15aa4dea963a23811258c28969954d49099f005bf51d8a986950ee9e8`  
		Last Modified: Tue, 07 Jan 2025 20:31:26 GMT  
		Size: 7.9 KB (7898 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.20` - linux; arm variant v7

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

### `hylang:python3.12-alpine3.20` - unknown; unknown

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

### `hylang:python3.12-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:80b789a8003f64356f057de6573ee5784e899f0058c65a94956c3c9aeb6d2c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23756874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011084173ff8290bae2d795a8057684553f14d4f5e9f190792bf94a678884302`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 00:36:05 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721755a35fcbfe0867183d7cb7cd9f5302b052fc3e22ccfe6840442901b14353`  
		Last Modified: Tue, 07 Jan 2025 14:13:18 GMT  
		Size: 446.1 KB (446147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c1a93175611d80677ccd56392faf71e5b9b90d581f288ffc1b87a9239c4a60`  
		Last Modified: Tue, 07 Jan 2025 14:13:18 GMT  
		Size: 13.6 MB (13621598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de93a8b5e7524e83e4f7882aeca1c46389d96e2b768f6e85611f8e787d564ec3`  
		Last Modified: Tue, 07 Jan 2025 14:13:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef14ef2d5e448554e9b9e037b9c5fba6589f7838eb516fb7fa7947224318054d`  
		Last Modified: Tue, 07 Jan 2025 17:40:53 GMT  
		Size: 5.6 MB (5602196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:e70243c5f03e119abd0b3c0485a26a4c1963d937f198394c528672e09a6ca8ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.7 KB (655738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a60e60053c86acc011e0536c1bf51e314f2e3e55ff73c4bf629311f0dfd7551`

```dockerfile
```

-	Layers:
	-	`sha256:bfcc6f6c26b19c01dd9e3d7cd313d68bed7a55f182d026fb3ccf061daa64e177`  
		Last Modified: Tue, 07 Jan 2025 17:40:52 GMT  
		Size: 647.6 KB (647597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2c55b99d3c6b64cb590889a5be39037ca3b58cd248017525abb14511af51274`  
		Last Modified: Tue, 07 Jan 2025 17:40:52 GMT  
		Size: 8.1 KB (8141 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.20` - linux; 386

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

### `hylang:python3.12-alpine3.20` - unknown; unknown

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

### `hylang:python3.12-alpine3.20` - linux; ppc64le

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

### `hylang:python3.12-alpine3.20` - unknown; unknown

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

### `hylang:python3.12-alpine3.20` - linux; s390x

```console
$ docker pull hylang@sha256:d1793948418ba5d15a8bfa39a35949f63c3c1930e93d18c533592304888bd007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23524256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba98ab4ba8ac6538cd46102be0f9c149568ab93fd4f5289e2f0e9a6ee8bc430a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 00:36:05 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
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
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Last Modified: Tue, 07 Jan 2025 02:32:49 GMT  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60331bd144e0dee0bcf228deaa18c9b2bd2cce3f24e2b721d8dfa614550c029b`  
		Last Modified: Tue, 07 Jan 2025 14:22:27 GMT  
		Size: 444.9 KB (444948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48250418b2a3b9985633e78cd3627c99a99f23bc62ecf07f1b5deddd55e0b768`  
		Last Modified: Tue, 07 Jan 2025 14:22:27 GMT  
		Size: 14.0 MB (14017854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74bee9a03d3d7d8ac0ea0c3cfde5be291769ef19509da8e47a296fc1ddc1ddb`  
		Last Modified: Tue, 07 Jan 2025 14:22:27 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21f192b248f6e918f65d959da0c90415c7ab3bcc34a79fd2a3e2e18c3f32e27`  
		Last Modified: Tue, 07 Jan 2025 17:14:47 GMT  
		Size: 5.6 MB (5602022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:7549a559b6edad19b2e84bb4905a99259f9d189a10bfef59fcb702c9ead52c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.6 KB (653627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fbcd107f2a064dd89043b3953b33c6f818be148d19271a54b1bd0c6c484ab2`

```dockerfile
```

-	Layers:
	-	`sha256:473eb63b3cc25606e59d6c55bfd3665cd9f7ab11113786cd3eb0dbb9662a11ba`  
		Last Modified: Tue, 07 Jan 2025 17:14:47 GMT  
		Size: 645.6 KB (645590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe22c1f68edc8bb74b9ff15bc32980b6e5c43b1dedc92083c1564e62751cd35f`  
		Last Modified: Tue, 07 Jan 2025 17:14:47 GMT  
		Size: 8.0 KB (8037 bytes)  
		MIME: application/vnd.in-toto+json
