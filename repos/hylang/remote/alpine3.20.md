## `hylang:alpine3.20`

```console
$ docker pull hylang@sha256:1c1e271d771b23cadb21236912afc28ce6fda50af5cc44268aeba0547ad2b796
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

### `hylang:alpine3.20` - linux; amd64

```console
$ docker pull hylang@sha256:2f9f7f48dc5868976c050959b4b426e087886f94413d896360e00dc9662c5bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.2 MB (22187433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371bb7103e3cbf821f511b5784b83bcc3551d6526e0487bda9083b00d40e0344`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 02:30:19 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_VERSION=3.13.1
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
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
	-	`sha256:d32dad080ed5b77d398ebf763cb4a46e5a207ef46a889b989a4bbf3efa3e2c6c`  
		Last Modified: Wed, 08 Jan 2025 18:23:12 GMT  
		Size: 458.4 KB (458435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157246674d47edb217d2631229bce1cb500dfcdfaeeddd914b540b7b9c1cdfa0`  
		Last Modified: Wed, 08 Jan 2025 18:23:12 GMT  
		Size: 12.4 MB (12411211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea36b2cc71fda40d2b6613eb558bab26086e70d8b8f54b93e8db9dda331bc4c`  
		Last Modified: Wed, 08 Jan 2025 18:23:12 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ae0f1c070744a4bfa85ca84dbd815694ed3c50323484de9dd7ae4669d38583`  
		Last Modified: Wed, 08 Jan 2025 19:16:22 GMT  
		Size: 5.7 MB (5691278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:a0191605b363435ec3bf37ccc2214ba899b9ff688c1538fbcbb3f74df85a9a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.3 KB (633274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54f4e7996c03078bf776f90e383815f4f127a6d98783a9aaf83651dca410476`

```dockerfile
```

-	Layers:
	-	`sha256:a73c134b25902b83f732001cdaa4dfdc454f3c312b0834ce2f82ba203620811d`  
		Last Modified: Wed, 08 Jan 2025 19:16:22 GMT  
		Size: 624.0 KB (624004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cb306119ecef2eaeb5e4069fbf48fd1327daa4b7892bf6d7b92f1f44ab05718`  
		Last Modified: Wed, 08 Jan 2025 19:16:22 GMT  
		Size: 9.3 KB (9270 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.20` - linux; arm variant v6

```console
$ docker pull hylang@sha256:7f8c17b278a78065371953494ebe173f9db11929dc094fdbf3e3546fa98153f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21565560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa80d1810b4d267b9cdd59afa5c014c7c0ace44b422fd43960ffd60f1a7e76f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 02:30:19 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_VERSION=3.13.1
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
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
	-	`sha256:ed580f0fb223eebbd5f6146da5038af16f340acf4313cf018eab71dd6f18652d`  
		Last Modified: Thu, 09 Jan 2025 07:23:54 GMT  
		Size: 459.2 KB (459195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2289cae1664c1b4640d32eefa4f6fd27727d719db4ee05cea2fdc633d8f3e57d`  
		Last Modified: Thu, 09 Jan 2025 07:41:52 GMT  
		Size: 12.0 MB (12043144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609bae9bc5be13c0a69eb37c45d87eb95c0dbf75ee644eadabe46dfc2bf896d1`  
		Last Modified: Thu, 09 Jan 2025 07:41:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76ac25df52c8da3751ecb138c3d4db77e8fdbb24558b79a974ae3e4f9f93841`  
		Last Modified: Thu, 09 Jan 2025 10:09:40 GMT  
		Size: 5.7 MB (5691501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:6c7368864926b8f6f36c770caa115c8bfade119566ce3fae33b41d369dac8fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aba0ff2f1de82ada99c6286214fa984c888bb64f93e8a791f7929b8fa01ec928`

```dockerfile
```

-	Layers:
	-	`sha256:8d60785c4257d194cca833da0a1de98c1013321ac2d76599f37df129dcbb0b1b`  
		Last Modified: Thu, 09 Jan 2025 10:09:39 GMT  
		Size: 9.2 KB (9163 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.20` - linux; arm variant v7

```console
$ docker pull hylang@sha256:406ceee52eb324c8292bc497501930a939f4b6350d34c41e787a9262cb86853f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20933120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3965668d7726ce1d82f85e8b923c7e6bb3b125496ce89d2234a3de0122af9ad2`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 02:30:19 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_VERSION=3.13.1
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
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
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Wed, 08 Jan 2025 17:34:15 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589321ec10dec5e71a8958de767f64ed1bd97c8c89ddfe4475bcb6c38ddb49b7`  
		Last Modified: Thu, 09 Jan 2025 07:57:58 GMT  
		Size: 458.4 KB (458419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce23e55e6f85424d94e741ba6f3fc5f2a3b95a34dc03f391adc5c3d2f336ace`  
		Last Modified: Thu, 09 Jan 2025 08:12:44 GMT  
		Size: 11.7 MB (11687436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdb7973e7924148098a852bd9e3124b7fae15b685eff3a5c5c7cc52622f2560`  
		Last Modified: Thu, 09 Jan 2025 08:12:42 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b1801173eb0af77c315b36bb9e8e14d161d6ef0b40a17e99c14c04b997f5cf`  
		Last Modified: Thu, 09 Jan 2025 12:15:18 GMT  
		Size: 5.7 MB (5691502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:54a8425f726e78c5beef11f4d2997e632b3ca7556edb975ec295ad641b49158d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.3 KB (636311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127d5b751cb5577f74d5e468d6505037bd2627a375639dabd4aa54c41d7522a8`

```dockerfile
```

-	Layers:
	-	`sha256:74c885d68d23c690c06fcdce33ba1e4b3f9c90e855697893419e013ddccfb437`  
		Last Modified: Thu, 09 Jan 2025 12:15:17 GMT  
		Size: 626.9 KB (626933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61b318e1f16af9d88ba517cbf877ae2802b04fe87a796da36e069c8d627cbff0`  
		Last Modified: Thu, 09 Jan 2025 12:15:17 GMT  
		Size: 9.4 KB (9378 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:91eaf60b6eaa4574fa32e607af1be01c4b12a8579226ce62ada9a1407915031f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22688838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c88a0fd362bf697af70f27b56160815bff59b11c2d39f2b49e75e5e9dfa0ff`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 02:30:19 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_VERSION=3.13.1
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
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
	-	`sha256:05da92a201330e11bbf02fe3270176f5a26cdb991915c9409ac910c29b2a875e`  
		Last Modified: Thu, 09 Jan 2025 04:21:30 GMT  
		Size: 460.6 KB (460582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d68a0c4609463aed3ac9b38a18fa77c0d078aedf575230fdd93e902c221aa`  
		Last Modified: Thu, 09 Jan 2025 04:34:13 GMT  
		Size: 12.4 MB (12445799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f340f38ec06a345110d4a59b58302fc8e54e4949acb450410a8248ff2b2ed7`  
		Last Modified: Thu, 09 Jan 2025 04:34:13 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d396dabd7e0874f2c6a1f1dc9324426d23666df870508636d187b499623c3702`  
		Last Modified: Thu, 09 Jan 2025 08:21:33 GMT  
		Size: 5.7 MB (5691440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:b735e8c51842c9fde4c712eaa166d0ec20605014088901b9dee3b4248e2c4996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.5 KB (633529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19ebca3f8bb161b8ba0fb53bace4b19ff7a6e167904380dd9057185f01a1eb5`

```dockerfile
```

-	Layers:
	-	`sha256:c16c1589cea6d004568717c27e10f87e1aebc66cb7a780e8032f2e9877ff3897`  
		Last Modified: Thu, 09 Jan 2025 08:21:33 GMT  
		Size: 624.1 KB (624108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64d50a214e7a8ecad23ebfb2af86e93c63d232ee79e87e111cf3e5331afdf3be`  
		Last Modified: Thu, 09 Jan 2025 08:21:33 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.20` - linux; 386

```console
$ docker pull hylang@sha256:ddd98d6bab6170a8d74607345b295bc892ca645f6ab69363f3ab89caece9a922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22295950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0288ee3e41d61533a779ab32207d9658ac1d0e8f530785d37d01ffc4738c175`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 02:30:19 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_VERSION=3.13.1
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
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
	-	`sha256:268b697aa01c0387f48a204357ca75868a7b059c1b4bfd5ce7e31eafcdecb5b2`  
		Last Modified: Wed, 08 Jan 2025 18:19:11 GMT  
		Size: 458.8 KB (458836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878263cccd3ba8aaa141a2075cb2ecd66fc497184230780a76d869790ab7ec42`  
		Last Modified: Wed, 08 Jan 2025 18:19:12 GMT  
		Size: 12.7 MB (12674537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed54296a909e1381542cf1ef5a4528de189a4c6cd2ed93d90b0c25c903fcc79`  
		Last Modified: Wed, 08 Jan 2025 18:19:11 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774cebc1e89ea127df327e1c13656b7678a0678aff73fb5c8eae66db84e5dbea`  
		Last Modified: Wed, 08 Jan 2025 19:17:24 GMT  
		Size: 5.7 MB (5691359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:df3d24a562b3c036c7afe31c6bfb00992c1d34e9700063170df1898041e12664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.2 KB (633177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c47eeb07904ab3ef1e068f0cf55940895f8ecdbdbfff6c5517588a3d0859f0a`

```dockerfile
```

-	Layers:
	-	`sha256:7dadaf41f4bc30ed218e955f6585b5c5eeb5bd850ef5d8ba4caeca6e627972a0`  
		Last Modified: Wed, 08 Jan 2025 19:17:24 GMT  
		Size: 624.0 KB (623959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4c21cc71bc8a8e4518a9f0b1c862a349b089d024236be8f5455aafab9438616`  
		Last Modified: Wed, 08 Jan 2025 19:17:24 GMT  
		Size: 9.2 KB (9218 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.20` - linux; ppc64le

```console
$ docker pull hylang@sha256:22bb9967e7c6ce0f337229fd7039c6bfe37b1197ad4513e4d09f2041ffd87a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22823355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7234245a08cc7f068661907675e5bf8cd524ef5f3de83c24d66fba78fa00acf6`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 02:30:19 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_VERSION=3.13.1
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
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
	-	`sha256:29780dea8accba52a1c6771449b8be3b1e5429ef7dfffaefd3c7772b6a0a30c9`  
		Last Modified: Wed, 08 Jan 2025 23:15:06 GMT  
		Size: 461.0 KB (460956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add3c6d0180bc1f4f7f4a521769ed68408adb73f77f0187241de728d80256931`  
		Last Modified: Wed, 08 Jan 2025 23:31:38 GMT  
		Size: 13.1 MB (13096327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4820bed491a9104f41c0b30c678a3a6c9294869b96233d9fefbc3337dfd8b2d0`  
		Last Modified: Wed, 08 Jan 2025 23:31:37 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c323012ee8e659c0685c3a1b4230c7b37925f75c8ca4415fe16b4cf22792c41e`  
		Last Modified: Thu, 09 Jan 2025 03:47:20 GMT  
		Size: 5.7 MB (5691415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:248f720dbe21c3d8b2191b65ee47d5262ffe324c684cb3893740ce46e214490a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.4 KB (631449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9deac7aa1b59f605f9badfaf65c4a9e9fd49dbe8cf6da7f037f2b9f306e9c8ec`

```dockerfile
```

-	Layers:
	-	`sha256:a711f0c7279cf88dd9d695ddee11893350dd531204494ada62553999ba7314fe`  
		Last Modified: Thu, 09 Jan 2025 03:47:19 GMT  
		Size: 622.1 KB (622111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:499280aa990d5958509ab990eef7439e95da86073493cd3200485784c917f371`  
		Last Modified: Thu, 09 Jan 2025 03:47:19 GMT  
		Size: 9.3 KB (9338 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.20` - linux; s390x

```console
$ docker pull hylang@sha256:705b31e109f977950f1ce340ee598ae3340be9ca4d418346eadee3d0949a1fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.4 MB (22439074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1437a4569bfa7086495135d0e43bceaafba3a7d387c4bb6e3f86a6910ed4aa7c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 02:30:19 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_VERSION=3.13.1
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
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
	-	`sha256:fb877377d950a6b18989691394ea2132e8f926b68f32bfd49c40345883ebab5b`  
		Last Modified: Thu, 09 Jan 2025 05:31:50 GMT  
		Size: 459.4 KB (459368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa68ea4899179d1bc42e6a5b0999b6cdfdec0577bed976c949a38b8c4f53766`  
		Last Modified: Thu, 09 Jan 2025 05:46:30 GMT  
		Size: 12.8 MB (12824739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15b8745ee92c0558810c613b349aff26c128fdec11d0fcf169016d6b689e626`  
		Last Modified: Thu, 09 Jan 2025 05:46:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c776c65dac3c9929085a691922d43e0dc43015ca1d3daf7d2edbfed4740ecde`  
		Last Modified: Thu, 09 Jan 2025 09:11:17 GMT  
		Size: 5.7 MB (5691396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:1f6b1c4124258ef378728a52622fe13a3f148321e2a60acd367c767e5092b0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.3 KB (631323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc86279e6e3aa7139a8402e0deeee9d08e5a1b1d6fd32d7df5dfd792534d32ce`

```dockerfile
```

-	Layers:
	-	`sha256:02a9f9fe078e4cee53247a8ca585b36383520aa8568d66bbcaab396e58b22668`  
		Last Modified: Thu, 09 Jan 2025 09:11:16 GMT  
		Size: 622.1 KB (622053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:539fe56c6478b3033774e30021620ecfa0abb518ee49711bd107c9272c2b7220`  
		Last Modified: Thu, 09 Jan 2025 09:11:16 GMT  
		Size: 9.3 KB (9270 bytes)  
		MIME: application/vnd.in-toto+json
