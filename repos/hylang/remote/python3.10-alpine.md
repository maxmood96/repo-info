## `hylang:python3.10-alpine`

```console
$ docker pull hylang@sha256:d224a63b81e7bfa1d599fb3cb65f1230845e5c970d603d06d619a4d32f4a2791
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

### `hylang:python3.10-alpine` - linux; amd64

```console
$ docker pull hylang@sha256:095ff72afcd165068a83ee3668042f4d377b91b977fe7c45ff641754633db966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24948619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade97a8181205e8dd5dbebb3587fd08f8c31c840e490d24dae8215b9b054e668`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:25:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:25:30 GMT
ENV LANG=C.UTF-8
# Wed, 04 Feb 2026 20:25:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:25:30 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Feb 2026 20:25:30 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 04 Feb 2026 20:25:30 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 04 Feb 2026 20:28:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:28:19 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:28:19 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:12:45 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:12:45 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:12:45 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:12:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da64b14f7f39dea599f6d3757a6a5d6f0aa9162935a57b8e3d8a568a5671a08`  
		Last Modified: Wed, 04 Feb 2026 20:28:26 GMT  
		Size: 460.9 KB (460941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29329a0f50c2873fda59a29f7be832f4d9fafb50d04e754e7bc7f1522b23e01`  
		Last Modified: Wed, 04 Feb 2026 20:28:27 GMT  
		Size: 15.5 MB (15450763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77714a77750d747be2c7b56948eeaee8d479fb025508101952fc2da6ba2d4811`  
		Last Modified: Wed, 04 Feb 2026 20:28:26 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713bc13a04b31ef2de999c7b1a9a4fe1b4fe7a4b31922c90c2a6132910a8a111`  
		Last Modified: Wed, 04 Feb 2026 21:12:51 GMT  
		Size: 5.2 MB (5174845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:f791e48945bc445f95c7d1698d39b8f40451c16cb35b3243f62b68b9f0441c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.4 KB (709373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceacd999e3162e5d6d4ee9cdacff3a5cf74f50229c0f06fb959c1e6a3ee039b0`

```dockerfile
```

-	Layers:
	-	`sha256:ddc2dee7f7c78888c1734e0a2afc182ba630e87c8bc6ef99c3124da829491f09`  
		Last Modified: Wed, 04 Feb 2026 21:12:51 GMT  
		Size: 700.0 KB (699966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4cca572687af1fba58b806059f2bd9a9568758f03ca742a427546155e65aaf4`  
		Last Modified: Wed, 04 Feb 2026 21:12:51 GMT  
		Size: 9.4 KB (9407 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine` - linux; arm variant v6

```console
$ docker pull hylang@sha256:12cb8102da73b70afbd0faaeb0e9a2567c1709845590e39f6328084cf085ec9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 MB (24250742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c631eb421b284b76cfa2e865522e0603943eb60e11b85192a290b9bd2f41e4b5`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:34:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:34:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 03:34:11 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 03:34:11 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 28 Jan 2026 03:34:11 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 28 Jan 2026 03:34:11 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 28 Jan 2026 03:38:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 03:38:17 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 03:38:17 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 04:46:50 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 04:46:50 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 04:46:50 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 04:46:50 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eac78b997b078aa42871b50cc93d24cd4c51adc8ab6ebb76ff44aacb4947c45`  
		Last Modified: Wed, 28 Jan 2026 03:38:22 GMT  
		Size: 461.4 KB (461449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e476f6818f08c913ee1d117bfae9151c5435dfbdb13eca3043d4dd3b43a41d7f`  
		Last Modified: Wed, 28 Jan 2026 03:38:23 GMT  
		Size: 15.0 MB (15044656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d30ae6954ee24385afdc2dc8da7ba02b51404fb1cc776b2c6621765b309f53`  
		Last Modified: Wed, 28 Jan 2026 03:38:22 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e6c0a595a6d0e552f1c7301ec70edd670262e8f99a93008687cedb21729794`  
		Last Modified: Wed, 28 Jan 2026 04:46:55 GMT  
		Size: 5.2 MB (5174567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:2c5c1cda582681b172e9802f0d1f6e038ef039e35a8fcfe317649c2ee418664c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1816ab984e8adf763553fe2be13d746da88f42573f71b49b05c7cccfb97ee1`

```dockerfile
```

-	Layers:
	-	`sha256:165ed56acee72e1c62d1c5e9941b84e8ffc724ec584b266177037fd132cd0f33`  
		Last Modified: Wed, 28 Jan 2026 04:46:54 GMT  
		Size: 9.3 KB (9304 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine` - linux; arm variant v7

```console
$ docker pull hylang@sha256:ba1f5cb80d7062e5cc5f033d3e324a62ab1ca2c7ddf4a526298e4e38b52ad852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23547107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805dcefe99a698d0c93be75044aa4f94c669b3a961b08cdefc86d627eb460924`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:35:46 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:35:46 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 03:35:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 03:35:46 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 28 Jan 2026 03:35:46 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 28 Jan 2026 03:35:46 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 28 Jan 2026 03:39:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 03:39:50 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 03:39:50 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 04:31:02 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 04:31:02 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 04:31:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 04:31:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8db001219f62b74094b37f645cfdd83c3dab747aa61c38ba4a14aa4284664fa`  
		Last Modified: Wed, 28 Jan 2026 03:39:56 GMT  
		Size: 460.7 KB (460727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f29414c3817fcc30171e6a07b77b62b5d062b1f8980c55d0200134c8725211`  
		Last Modified: Wed, 28 Jan 2026 03:39:57 GMT  
		Size: 14.6 MB (14629941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b940833cbfaae74d17738fc6f7347d3943f0ce412657d7db8b85573999c1dd`  
		Last Modified: Wed, 28 Jan 2026 03:39:56 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5306a666b93ee13548e746dcffb8749882cbc4a8ee6987955e50356595534fe6`  
		Last Modified: Wed, 28 Jan 2026 04:31:08 GMT  
		Size: 5.2 MB (5174465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:9773320351578dc73b4f67516e6c0e5fe86b53e4575faa5458f21dcd332f091e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **711.9 KB (711893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e54773f5d3875297211c98576c3397b293f033b8f810fc576214c38c8ad16f1`

```dockerfile
```

-	Layers:
	-	`sha256:2a7a1c2e416681059cb0506df6b64458ff1ad84638d623d079aed2f731e49046`  
		Last Modified: Wed, 28 Jan 2026 04:31:08 GMT  
		Size: 702.4 KB (702374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb3298a817347d3ed24e0f64961e7661441138146cbbb064713b5117974f384d`  
		Last Modified: Wed, 28 Jan 2026 04:31:08 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:e3373d0e369439514a36e1508510b3d8e3a5228ade93cb9f91ce0d1db1ce3ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25463445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aea282291feab7ab34348f7edc05e3caafc378b36a8dfd04254c1c56b807d55`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:18:56 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:18:56 GMT
ENV LANG=C.UTF-8
# Wed, 04 Feb 2026 20:18:56 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:18:56 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Feb 2026 20:18:56 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 04 Feb 2026 20:18:56 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 04 Feb 2026 20:36:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:36:42 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:36:42 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:10:59 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:10:59 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:10:59 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:10:59 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c746ec0a997c7069e8a770a91558b284d554ad0bb7f70df91910d5d79979db0b`  
		Last Modified: Wed, 04 Feb 2026 20:26:00 GMT  
		Size: 463.0 KB (463008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f7870f87eacd58f48e97af9cdc0f7c8466a5b2eaee753bc6f1bd2bde7167d2`  
		Last Modified: Wed, 04 Feb 2026 20:36:50 GMT  
		Size: 15.6 MB (15628236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93462647c68155e0f94e26782bea713491b3d7bbe2f5b7b1f5e8acbd4b6232fa`  
		Last Modified: Wed, 04 Feb 2026 20:36:49 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5736e555729fb62a52576fd47370358641c70d1acae9cdb9e036a5275d435188`  
		Last Modified: Wed, 04 Feb 2026 21:11:05 GMT  
		Size: 5.2 MB (5174862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:b8da30faf3bbf73dc84768a905664c3d89dabcd30f47aa534e846c0ecc426a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.0 KB (708979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc0a431c1255fd830491b36dceec6864c2882d13c18a3f3e1da823c1bca3b05`

```dockerfile
```

-	Layers:
	-	`sha256:081d71dfee808fa667028751111388efa048cafb81b67ae15b112f8088dbb6f5`  
		Last Modified: Wed, 04 Feb 2026 21:11:05 GMT  
		Size: 699.4 KB (699420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea5723e18066509606dc98b089326593400eeaa71dba0f15b2e5104955e2b129`  
		Last Modified: Wed, 04 Feb 2026 21:11:04 GMT  
		Size: 9.6 KB (9559 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine` - linux; 386

```console
$ docker pull hylang@sha256:6cfb175cbf6d909fc3897f09450261807ccde33afb4745c136559e9252832e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (25002398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707f760cd0d8d9e6b749c58f9eaed81f1d60a65afd776e8cc54856f28eba742f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:29:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:29:06 GMT
ENV LANG=C.UTF-8
# Wed, 04 Feb 2026 20:29:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:29:06 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Feb 2026 20:29:06 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 04 Feb 2026 20:29:06 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 04 Feb 2026 20:32:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:32:31 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:32:31 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:07:06 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:07:06 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:07:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:07:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1806f5cb048d291e21dd99ad4346d3e67ab06ece7ba07527bc8961e29e1e1041`  
		Last Modified: Wed, 04 Feb 2026 20:32:37 GMT  
		Size: 461.2 KB (461235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3784ee3ed80dab2295ac16575c57fe5b123fb8e431547bff1abe1d08e74292d`  
		Last Modified: Wed, 04 Feb 2026 20:32:38 GMT  
		Size: 15.7 MB (15678897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f48dac4757c9ac4a55267ce3462a89b39b18c8f08255234289abcf21afdf4f`  
		Last Modified: Wed, 04 Feb 2026 20:32:37 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36c45bdc43b5becc9afa07061305f14d0327e5d5076cd94abc0780482951ebc`  
		Last Modified: Wed, 04 Feb 2026 21:07:12 GMT  
		Size: 5.2 MB (5175019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:6914cd00cc5794b631ae97c9a0cd1392e1ca6a8ae279ad05ce449b2e6b508a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.3 KB (709276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c42cc77745314c5f50504c013e03c0639e4bb33a2fe22a511d20a39e60007a`

```dockerfile
```

-	Layers:
	-	`sha256:dba94b3d179efb458e0f21846cb232e8642bb0970aef4b15b7d56796b8d634ab`  
		Last Modified: Wed, 04 Feb 2026 21:07:11 GMT  
		Size: 699.9 KB (699921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967e2134fec2d56b157182b2bd8046124611c4fa6cf976bd63f34c8c24f16333`  
		Last Modified: Wed, 04 Feb 2026 21:07:11 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine` - linux; ppc64le

```console
$ docker pull hylang@sha256:2f3a5d97a78f846567742b7984325c5b50e10f0d3b25b58e4c7f804b074a74e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25722674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f0c7c6722327bb73d0f37838c166c306bbe6b2d3d9d37f65d19f588f8a973e`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:59:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 04:59:53 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:59:53 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 04:59:53 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 28 Jan 2026 04:59:53 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 28 Jan 2026 04:59:53 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 28 Jan 2026 05:24:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 05:24:17 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 05:24:17 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 07:09:17 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 07:09:17 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 07:09:17 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 07:09:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88aafecdf803f0bda53169e0b4516ebe803ec0a6efe23323aab9048a5a31b23`  
		Last Modified: Wed, 28 Jan 2026 05:09:03 GMT  
		Size: 463.5 KB (463504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3369a31d3fba293daa5e13c16532e54a7dcdaab572813519d5fb2b8a54141ee`  
		Last Modified: Wed, 28 Jan 2026 05:24:38 GMT  
		Size: 16.3 MB (16254649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1314f3318ed6f5195607e49a6649c465ef7b4f7bf24818085e794c85a26db477`  
		Last Modified: Wed, 28 Jan 2026 05:24:37 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f409216fa2b7a985eae2f718689978c0c85003f4a09a9db23a3d231cf09999c4`  
		Last Modified: Wed, 28 Jan 2026 07:09:31 GMT  
		Size: 5.2 MB (5174630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:0f85bb7b3953a87893114e5384a2feea088894d47d6cab885985709973ace120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.8 KB (708848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3e454252139a714b078d8940577dbe3f7a27ba12c071ac37edee4f1733ed9f`

```dockerfile
```

-	Layers:
	-	`sha256:00a78c8d07a83f29c6940101b67e3b70bb2eb2be29623b796c100deee01a18d9`  
		Last Modified: Wed, 28 Jan 2026 07:09:31 GMT  
		Size: 699.4 KB (699373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3443de4bf4f2d11addd02138e3507aea902c62b0b81c53731ba1105e4f4c16a8`  
		Last Modified: Wed, 28 Jan 2026 07:09:31 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine` - linux; riscv64

```console
$ docker pull hylang@sha256:92d1a3a4521ee2585dd007ae12cd1a89e04f274fce67ec3de924d838656138fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24632467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0abdcf7f3492eec74bd0b29fd1e960e152bbed3cab4a9ae0c3b6c6e5dc920b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 23:27:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 23:27:38 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 23:27:38 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Jan 2026 23:27:38 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 29 Jan 2026 23:27:38 GMT
ENV PYTHON_VERSION=3.10.19
# Thu, 29 Jan 2026 23:27:38 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Fri, 30 Jan 2026 02:08:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 30 Jan 2026 02:08:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 30 Jan 2026 02:08:07 GMT
CMD ["python3"]
# Sun, 01 Feb 2026 06:24:36 GMT
ENV HY_VERSION=1.2.0
# Sun, 01 Feb 2026 06:24:36 GMT
ENV HYRULE_VERSION=1.0.1
# Sun, 01 Feb 2026 06:24:36 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 01 Feb 2026 06:24:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a24d3312840a658b2b4b8edfb5495fcefd5c5898b617c59e7367d3e6b834e59`  
		Last Modified: Fri, 30 Jan 2026 00:02:56 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e886439328d87a3af08c5b88f1e9926010423060b7ce27a8d29d567bdbbf067e`  
		Last Modified: Fri, 30 Jan 2026 02:08:58 GMT  
		Size: 15.4 MB (15409698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933588e7000f0a121475f36f371b8d37a5e9a7be9bbc4f2b94179af5fde56dcb`  
		Last Modified: Fri, 30 Jan 2026 02:08:56 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe616cab7c93add9f5595c42b5d8c8d1f94d79e669b7755aefe81a87adc260b`  
		Last Modified: Sun, 01 Feb 2026 06:25:17 GMT  
		Size: 5.2 MB (5176042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:6d72e2a012bc2aaa8670e62aabb964443d40ddb0cac03722d4f35cbd4dbe3831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.8 KB (708844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a50cb036321c0bf0632addf85e394d539ca207697b34623e9dede32258ed4c3`

```dockerfile
```

-	Layers:
	-	`sha256:ad41bfba95beb65457d4a79b23d8248664d01e8b6af093eae10cd86a18d5dee0`  
		Last Modified: Sun, 01 Feb 2026 06:25:17 GMT  
		Size: 699.4 KB (699369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24c8e9a12f118a07375d019b51cfc14d6458f664382d29eab926ef8289bf0340`  
		Last Modified: Sun, 01 Feb 2026 06:25:16 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine` - linux; s390x

```console
$ docker pull hylang@sha256:72fb1eb55756e06244e98a55cb2cf962ac2f4c448274fa3f3b48618818b2d41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25178524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fe3c6a68ba63deb58fa47290d45c9a0ca4da8c23447cbca91b3b7f1851fa89`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:43:32 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 06:43:32 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 06:43:32 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 06:43:32 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 28 Jan 2026 06:43:32 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 28 Jan 2026 06:43:32 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 28 Jan 2026 06:47:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 06:47:18 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 06:47:18 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 07:29:15 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 07:29:15 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 07:29:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 07:29:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b83181b5a3b5dcb8438a9172fc8afa1728c9d95c28167ff79e8a214b8d378c`  
		Last Modified: Wed, 28 Jan 2026 06:47:28 GMT  
		Size: 461.7 KB (461738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c153e90789720e10b45bf1a201522ca86018b2282d40b3598a595d1aeb3bbc`  
		Last Modified: Wed, 28 Jan 2026 06:47:28 GMT  
		Size: 15.8 MB (15816797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2da795ee61471a2d3335b64069133a7f90749990a3808b949b3e0fe1360695`  
		Last Modified: Wed, 28 Jan 2026 06:47:28 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89328ef9e6d8dee00bb8d83a7868fd4f74b3dfa0d320677a6598dd814d08fa0`  
		Last Modified: Wed, 28 Jan 2026 07:29:26 GMT  
		Size: 5.2 MB (5174406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:edc728ee4a6c742a1d935ab9a5e34a4b95bed0f1c7cb11a8d57f625fee0762ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.7 KB (708722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d64ba9735214270861294570b3be4d3115978012eeef10fbf308bbc24b3122b`

```dockerfile
```

-	Layers:
	-	`sha256:38ebc18cdd9b36a9c118993d27c64d1da951f2b73705342f207c6b9b9ed0f47f`  
		Last Modified: Wed, 28 Jan 2026 07:29:25 GMT  
		Size: 699.3 KB (699315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcf1bf700e5786e18510de176a1605c2691d928ae8e1ecd110bdf734b603a940`  
		Last Modified: Wed, 28 Jan 2026 07:29:25 GMT  
		Size: 9.4 KB (9407 bytes)  
		MIME: application/vnd.in-toto+json
