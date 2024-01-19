## `hylang:python3.11-alpine3.18`

```console
$ docker pull hylang@sha256:567f86f47d8817f02d791018cc6e014eca9a2689821947004ca6d3cc87ca7e76
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

### `hylang:python3.11-alpine3.18` - linux; amd64

```console
$ docker pull hylang@sha256:c1c42774fb155e34e8ed30dafb0b2ebd730b14d7f2e3cea8a6ce20461e8ca902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25714792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86736e2bf45a147dfcfe8120c16f45252161f3b0031774cdf55e7d0d25230c1a`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Wed, 20 Dec 2023 02:14:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 02:14:05 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 02:14:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 20 Dec 2023 02:14:05 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 20 Dec 2023 02:14:05 GMT
ENV PYTHON_VERSION=3.11.7
# Wed, 20 Dec 2023 02:14:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 20 Dec 2023 02:14:05 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 Dec 2023 02:14:05 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Wed, 20 Dec 2023 02:14:05 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Wed, 20 Dec 2023 02:14:05 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Wed, 20 Dec 2023 02:14:05 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Wed, 20 Dec 2023 02:14:05 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 20 Dec 2023 02:14:05 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5363d7c7ad3a7983ab3c7d72572f8e9abe624da19a7d1f5047d5896858545b35`  
		Last Modified: Tue, 05 Dec 2023 19:53:56 GMT  
		Size: 622.3 KB (622321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998ab7321685b9e7c68462621b44832ae567fb83a1ddbda39f86f7ec1984f790`  
		Last Modified: Tue, 05 Dec 2023 19:53:58 GMT  
		Size: 12.5 MB (12468641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73b243238ed1351ffdc05634708dd335ae0489473a20546e9bd107e05a7f03a`  
		Last Modified: Tue, 05 Dec 2023 19:53:56 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649cfdc33bb3fb55d2cc34881a4f4057ba4c2d84640bf96f073d5908a4afccd2`  
		Last Modified: Fri, 19 Jan 2024 00:11:24 GMT  
		Size: 3.1 MB (3109703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0eb54e2dd3415d45249aa40bd3a3e11108efaa47118767b3d1ea4b21730673`  
		Last Modified: Fri, 19 Jan 2024 00:50:58 GMT  
		Size: 6.1 MB (6111464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:7eb6d4d64c1da3c1189f15b8f4121dbe76b9a06fc41a9fcaf3243177cdc63fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **870.2 KB (870212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7ef7261d4e9e624a8d3a47918e1f8ad9fafe09b804993e32274194039b0447`

```dockerfile
```

-	Layers:
	-	`sha256:253804d9947dcd137f1a6ded16de2d5502faca592fb4311c3d72d2822dd37be5`  
		Last Modified: Fri, 19 Jan 2024 00:50:58 GMT  
		Size: 861.1 KB (861066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8be9043e9c64859330edc562c420e9134b9959294c032f238b17499858a8e3f`  
		Last Modified: Fri, 19 Jan 2024 00:50:58 GMT  
		Size: 9.1 KB (9146 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.18` - linux; arm variant v6

```console
$ docker pull hylang@sha256:c075d9f159ab57996684d245a6997bd10c7c73c307e385af2a840e24bc9bc21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25102374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51aaade2eb80976df1c302772326d1f210f47cc26d882163bcf9f183f77c5be`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Dec 2023 22:49:21 GMT
ENV LANG=C.UTF-8
# Mon, 04 Dec 2023 22:49:21 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 04 Dec 2023 22:49:21 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PYTHON_VERSION=3.11.7
# Mon, 04 Dec 2023 22:49:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 04 Dec 2023 22:49:21 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Mon, 04 Dec 2023 22:49:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 04 Dec 2023 22:49:21 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279ddce74df1089fd8408c1df4817404bf1429d5e1c26eba71dbe75693396243`  
		Last Modified: Tue, 05 Dec 2023 18:23:57 GMT  
		Size: 622.7 KB (622711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c7ecd45229db25459bb8ec9639cea114d89d19494fe51010ac09ecc18b2734`  
		Last Modified: Tue, 05 Dec 2023 18:23:59 GMT  
		Size: 12.1 MB (12111719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7643c1d7e20cc99bb70e5aa1e24297701ebab3994102998e0e6809e2559b424`  
		Last Modified: Tue, 05 Dec 2023 18:23:56 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caacffca49ae8668e2618afdb4ffc68b47d217aba3bfab53f6e5bcee1e0c89dc`  
		Last Modified: Tue, 05 Dec 2023 18:23:57 GMT  
		Size: 3.1 MB (3109663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3de7d054fd6e6687ca0c4abb6229307318123439a6d19b242f36625bb4ba52`  
		Last Modified: Mon, 08 Jan 2024 20:09:05 GMT  
		Size: 6.1 MB (6111170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:731adbc29e16291a22cd2d88374d15f0db608ebbb4084221b41f80ffcbd606dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 KB (9001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c815b62a0ed94e115ca5006b17310956848a577ff725b7117aec55aa0e02db`

```dockerfile
```

-	Layers:
	-	`sha256:9977c3a6fda13d72ba186f0618aaf0ea0238d22227293b347d5b266ee374ea4d`  
		Last Modified: Mon, 08 Jan 2024 20:09:04 GMT  
		Size: 9.0 KB (9001 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.18` - linux; arm variant v7

```console
$ docker pull hylang@sha256:101e5032ece44f99de02fb98f4e78e5b127ce3eaa9e55b863ab8dfb2abc0b230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24390325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfc85e8204191fd914c77d3ffa5993c18c836ecd637804b22c8e5cbb9c6f56e`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Dec 2023 22:49:21 GMT
ENV LANG=C.UTF-8
# Mon, 04 Dec 2023 22:49:21 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 04 Dec 2023 22:49:21 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PYTHON_VERSION=3.11.7
# Mon, 04 Dec 2023 22:49:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 04 Dec 2023 22:49:21 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Mon, 04 Dec 2023 22:49:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 04 Dec 2023 22:49:21 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6a3a8c72a8c1864813c622206dfebfe27ffe4515ca4764f1a5863c084c385a`  
		Last Modified: Tue, 05 Dec 2023 19:30:47 GMT  
		Size: 621.8 KB (621783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b650cfbc852e0ae95c647dff29dc3ef52b19edb1ace2759ca5cc4a0e1e6c96`  
		Last Modified: Tue, 05 Dec 2023 19:30:50 GMT  
		Size: 11.6 MB (11646294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a27edfddcd73765220aa0c41fc2a7ee38a743319240c9c32b1249b7c37b8ff`  
		Last Modified: Tue, 05 Dec 2023 19:30:47 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6ca41561d8c05200c53c1e71d72eb875b77e7e6be9c03d8224186610a882fa`  
		Last Modified: Tue, 05 Dec 2023 19:30:48 GMT  
		Size: 3.1 MB (3109657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e6fc365897e19eb1cb7676dc95ab729dc3cb01a9c82cf2aa33386557ea016e`  
		Last Modified: Sat, 06 Jan 2024 04:44:51 GMT  
		Size: 6.1 MB (6111345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:be0b74e762d2467ef38f42e5baaf272dedc751e80f7c6ff1743af4f85b7e6aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **872.0 KB (871968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e3f0a3bf7cbff71a023cbb093e324838556b8a9ddd05214024d9fb1ea27674`

```dockerfile
```

-	Layers:
	-	`sha256:fd171cebae5d6a7bd7fc190b2b23802452f7e8aac6dbc992490fc8d560456d18`  
		Last Modified: Sat, 06 Jan 2024 04:44:51 GMT  
		Size: 863.6 KB (863570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57bc3f7c0bc2fd94284eea5a595ae9eca59b287c9aa6a3aa9ebfd9ed851d20ce`  
		Last Modified: Sat, 06 Jan 2024 04:44:50 GMT  
		Size: 8.4 KB (8398 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:51b284057afb5bc19033095decf2773e83b167679c9091f2fb3ce9498b23ad1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25739684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ec626e835c06f7842cf6577c4aff658d0c32783c837ddba7474eafc4dfd93e`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Dec 2023 22:49:21 GMT
ENV LANG=C.UTF-8
# Mon, 04 Dec 2023 22:49:21 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 04 Dec 2023 22:49:21 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PYTHON_VERSION=3.11.7
# Mon, 04 Dec 2023 22:49:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 04 Dec 2023 22:49:21 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Mon, 04 Dec 2023 22:49:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 04 Dec 2023 22:49:21 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7687c947765812cb62b6294a5779d27f0df3310e38c77b4524b2be89bd39260`  
		Last Modified: Tue, 05 Dec 2023 18:58:51 GMT  
		Size: 624.5 KB (624520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04496bdb510c96ff8bdfeaf5b75d3e57e58979ce419a8c36b5eb7f3f1f7895e7`  
		Last Modified: Tue, 05 Dec 2023 18:58:52 GMT  
		Size: 12.6 MB (12560955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2e1ad49051d0bba087acad529ad15132f0dc4f7b818527c6c3c0c0e77dd13e`  
		Last Modified: Tue, 05 Dec 2023 18:58:51 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314673dfe8912c60db5b9b0430250a65edf3082505c959964cf7679f6b5a326b`  
		Last Modified: Tue, 05 Dec 2023 18:58:51 GMT  
		Size: 3.1 MB (3109674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb60bad2efc29aab1a30a4ac349c8910b301c2858c0da16d377f192a4a78274`  
		Last Modified: Sat, 06 Jan 2024 00:37:19 GMT  
		Size: 6.1 MB (6111259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:036b726c703409fe240dac8e05465c0151dea9978f372eb3ce4addf01afad352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **869.4 KB (869407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6d13406ae82865f226b8e44ad276c5fa8ddc99065aff5bb95959fea8e54c80`

```dockerfile
```

-	Layers:
	-	`sha256:b6c5f2117b20d38f6bbd836dcfc914fb5241f8e5e996d82fc64fff9f9ae4e4dc`  
		Last Modified: Sat, 06 Jan 2024 00:37:19 GMT  
		Size: 861.1 KB (861069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da9479268c0dcc3348dda5506812a3dc72dec06ae4a149a895df7f0b95081d83`  
		Last Modified: Sat, 06 Jan 2024 00:37:18 GMT  
		Size: 8.3 KB (8338 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.18` - linux; 386

```console
$ docker pull hylang@sha256:262bcec7808b11058dd591e86a49d6b34d60ba0ca74098a471152fd5566e218c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25641762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22df95fdec25dd8b392a94f087e0d05b50108e221f8157a1bbf742c8bd9306da`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 01 Dec 2023 02:03:44 GMT
ADD file:92902088cd15ed8f5dca2f7fc6570fb4e4824fac8b09e091c88e96bbd0ca814b in / 
# Fri, 01 Dec 2023 02:03:44 GMT
CMD ["/bin/sh"]
# Wed, 20 Dec 2023 02:14:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 02:14:05 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 02:14:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 20 Dec 2023 02:14:05 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 20 Dec 2023 02:14:05 GMT
ENV PYTHON_VERSION=3.11.7
# Wed, 20 Dec 2023 02:14:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 20 Dec 2023 02:14:05 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 Dec 2023 02:14:05 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Wed, 20 Dec 2023 02:14:05 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Wed, 20 Dec 2023 02:14:05 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Wed, 20 Dec 2023 02:14:05 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Wed, 20 Dec 2023 02:14:05 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 20 Dec 2023 02:14:05 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4966a8bd129b0a6adf93dc295a8fbe8f665d3194a684a5ce199c1c3596dbf3d9`  
		Last Modified: Fri, 01 Dec 2023 02:04:18 GMT  
		Size: 3.2 MB (3238831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffea944196344a71c68c27de834d0fcdc5eec752152b9f6fc6497ce5b6747f8f`  
		Last Modified: Tue, 05 Dec 2023 19:39:13 GMT  
		Size: 622.2 KB (622214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fa07015dd9f04071a465e21cc59d139c05828be1072170be1b91c455bb188f`  
		Last Modified: Tue, 05 Dec 2023 19:39:15 GMT  
		Size: 12.6 MB (12559525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28bffb848167d4c1fe89dcf56253d923477c0fa99a3d884a6b0da7633e1c4430`  
		Last Modified: Tue, 05 Dec 2023 19:39:12 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0874f73603bddaca7ad983af92b33c3031e4f0f9a203c978ccec673f906c7a5c`  
		Last Modified: Fri, 19 Jan 2024 01:23:00 GMT  
		Size: 3.1 MB (3109682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e586b86aff2ec1b46397ba64435d44ac72b7fa06226779124137dbc182769d`  
		Last Modified: Fri, 19 Jan 2024 01:50:48 GMT  
		Size: 6.1 MB (6111270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:816bd6af4dde3a0f555857908563231dd847d1ba21eccc90f05f8443ab4bc88a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **870.2 KB (870158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089aaf291016669b73c37aac7178a27daa87e51c426b82ceabfa4ab1138033e2`

```dockerfile
```

-	Layers:
	-	`sha256:80351ed7c92ded1a54dfca46b5ad7e845938cfb229f77b725fd75317b259b785`  
		Last Modified: Fri, 19 Jan 2024 01:50:48 GMT  
		Size: 861.0 KB (861041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37bb41c8418c66ffea9393edbd7ba87c21741d4f4ea9cc766ee55eefc715e9f6`  
		Last Modified: Fri, 19 Jan 2024 01:50:48 GMT  
		Size: 9.1 KB (9117 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.18` - linux; ppc64le

```console
$ docker pull hylang@sha256:c3012c4f29349e5b2775de71bce16e0459697836834c9dce2bb18608bdfa6f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26048800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e48b3894581be1a05ac547bbe0efafbdd8b9170988465498d25213e027b68a48`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Wed, 20 Dec 2023 02:14:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 02:14:05 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 02:14:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 20 Dec 2023 02:14:05 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 20 Dec 2023 02:14:05 GMT
ENV PYTHON_VERSION=3.11.7
# Wed, 20 Dec 2023 02:14:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 20 Dec 2023 02:14:05 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 Dec 2023 02:14:05 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Wed, 20 Dec 2023 02:14:05 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Wed, 20 Dec 2023 02:14:05 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Wed, 20 Dec 2023 02:14:05 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Wed, 20 Dec 2023 02:14:05 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 20 Dec 2023 02:14:05 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c450107b1f651e0d5357ddca15f10b7fe2195f41771b1c55d96c62001069b127`  
		Last Modified: Tue, 05 Dec 2023 20:02:45 GMT  
		Size: 624.9 KB (624906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95f71dbc2cd11ed25d7657207629bf6ca70ceb997bfebae5560311f24fd6f6b`  
		Last Modified: Tue, 05 Dec 2023 20:02:47 GMT  
		Size: 12.9 MB (12853970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa003173fe12683d8230021648e735b278448adf54aba4c3bb6a764574536f71`  
		Last Modified: Tue, 05 Dec 2023 20:02:44 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd34b23e9a15aec7f164e15255608c3300d0655949e79aaedc9276874a6d9b49`  
		Last Modified: Fri, 19 Jan 2024 00:37:49 GMT  
		Size: 3.1 MB (3109712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8deda2a6a49e5ea08a1a04654559f46be882b62ff1d6729c76e7726d480c7991`  
		Last Modified: Fri, 19 Jan 2024 02:27:05 GMT  
		Size: 6.1 MB (6111648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:deabe2bc1c32758609ea74a9d87ae610f941816926dca30fb85661f56e2e275b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **868.6 KB (868648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55545a8cf19d7142f3c6a5c12aaa39f88a8fde8e4a82aaf3031a26fb4e45dace`

```dockerfile
```

-	Layers:
	-	`sha256:aac3338f02dd4d7a21325765d8189cbc0a637c990a5e8b2fe0f01c253e360faf`  
		Last Modified: Fri, 19 Jan 2024 02:27:05 GMT  
		Size: 859.5 KB (859464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:745648ecd1795e1fe2f751311f910d52556fc530b2a353bf7793eaa33728282a`  
		Last Modified: Fri, 19 Jan 2024 02:27:05 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.18` - linux; s390x

```console
$ docker pull hylang@sha256:ec063be5336451b30f21b367897c81277614308b8b6771047a311554a5e64d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25622500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1016e2130a7a85246f74f93e07bab5370d8a883d38d8162a2f9c314c9add51b`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Dec 2023 22:49:21 GMT
ENV LANG=C.UTF-8
# Mon, 04 Dec 2023 22:49:21 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 04 Dec 2023 22:49:21 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PYTHON_VERSION=3.11.7
# Mon, 04 Dec 2023 22:49:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 04 Dec 2023 22:49:21 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Mon, 04 Dec 2023 22:49:21 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Mon, 04 Dec 2023 22:49:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 04 Dec 2023 22:49:21 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607af03b9a228e95db0cdffe1efee657c6cfa8771fb312b60948c7b142bfb77a`  
		Last Modified: Tue, 05 Dec 2023 19:11:08 GMT  
		Size: 622.8 KB (622835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aca7aca3c6b20ceb33417d0f93d6faba28397b85c100887737bc969f39cd1e1`  
		Last Modified: Tue, 05 Dec 2023 19:11:10 GMT  
		Size: 12.6 MB (12561001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04798476fa60c3e2dfcbc6cac3042ad08e0c93fffbfb88cc96038edc0a4e2aa`  
		Last Modified: Tue, 05 Dec 2023 19:11:08 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6da3a6e9567aadf812ce6844402d7934d2f1ecb32f05e7761baac45014aad02`  
		Last Modified: Tue, 05 Dec 2023 19:11:10 GMT  
		Size: 3.1 MB (3109667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3133a7f876c1557583aec40e6e324fceb9e4d08f5e4ccc6ed2adf5ac20832817`  
		Last Modified: Sat, 06 Jan 2024 00:25:51 GMT  
		Size: 6.1 MB (6111300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:9fa80fbc8f7fa33f2632a8b743d58a467fa2acdbc42e9f0e44f6e59608a8c641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.8 KB (867750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abed6437892ccf4424006a17108424bbf891f0bff2b6b547414db20e679ec0e8`

```dockerfile
```

-	Layers:
	-	`sha256:4023a2070c3c107e031c28863e4c8fa6b89d001b6e489b9f0ea9931e9f1d468a`  
		Last Modified: Sat, 06 Jan 2024 00:25:50 GMT  
		Size: 859.4 KB (859422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:644d6a8860b9a1e8c5c1f7464069e23e632635d8614c6639a628f26af854bdd4`  
		Last Modified: Sat, 06 Jan 2024 00:25:51 GMT  
		Size: 8.3 KB (8328 bytes)  
		MIME: application/vnd.in-toto+json
