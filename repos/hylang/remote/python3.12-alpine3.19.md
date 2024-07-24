## `hylang:python3.12-alpine3.19`

```console
$ docker pull hylang@sha256:a36e5bdff4023c47a21cd2c567c2c22fa424d277c783c4c102c144ef1fb5d0ee
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

### `hylang:python3.12-alpine3.19` - linux; amd64

```console
$ docker pull hylang@sha256:6e49300443251ac692ee94ced2223f09958c1521e96d5aab0c954bba034527d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25511349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04ca8222617493d810fa2e264790f9dcfc92ff4c422c52394d443a42423d4f3`
-	Default Command: `["hy"]`

```dockerfile
# Sun, 07 Jul 2024 23:32:36 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Sun, 07 Jul 2024 23:32:36 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 23:32:36 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_VERSION=3.12.4
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40afeb6137f70ecc3c5571c9c2e7a8f737387ca5f01cc8488a31c1317c96ff7e`  
		Last Modified: Mon, 22 Jul 2024 23:21:11 GMT  
		Size: 627.9 KB (627913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ec0dcc007836e088956242e8c9a71395e89d972494a465c4ef58e10e584903`  
		Last Modified: Mon, 22 Jul 2024 23:21:11 GMT  
		Size: 11.8 MB (11780546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d14df23354eef12d132b87ae2f92e23f5d9bdaa0aff865fe1801f99e1d7bc06`  
		Last Modified: Mon, 22 Jul 2024 23:21:11 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4c105015ad2f14b4c0a09d489514e13667cf600d91d2731c24b5d84839fbc`  
		Last Modified: Mon, 22 Jul 2024 23:21:11 GMT  
		Size: 4.2 MB (4159740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce515f0689382864d812702b02a100dd77d52a0a80d384409bc4622e170680c`  
		Last Modified: Tue, 23 Jul 2024 00:08:36 GMT  
		Size: 5.5 MB (5523880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:74e95ff6e7b3b5da83dfdd38dfc4b24832f08bf8265215b6294867c0233837f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1091660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:944cc04a453ba5e42214e84ae9bc87c2be78b659ee67b72e627b60e56fe3a8ff`

```dockerfile
```

-	Layers:
	-	`sha256:ae0ea6035843ac150cb3721c493b37f5514a36e5c02ad69fd0db6be0e8145f24`  
		Last Modified: Tue, 23 Jul 2024 00:08:36 GMT  
		Size: 1.1 MB (1079406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63f71469e911ab4705dbd2bbb9064af109c70b302506aad20337b65b52a7adf7`  
		Last Modified: Tue, 23 Jul 2024 00:08:36 GMT  
		Size: 12.3 KB (12254 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.19` - linux; arm variant v6

```console
$ docker pull hylang@sha256:7d04379982619de132b8082b0b7a4cdb33895c07dc95911b6af70f48e51907c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24845051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4949621cbc08dab13f3bac244dddd78d5e45cadd5880cf2cb7a5713e7361fd2e`
-	Default Command: `["hy"]`

```dockerfile
# Sun, 07 Jul 2024 23:32:36 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Sun, 07 Jul 2024 23:32:36 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 23:32:36 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_VERSION=3.12.4
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b74e34e590a0380682ae6e51f296cd7fc2d8427cbe99b90a2c5f5559017ad80`  
		Last Modified: Tue, 23 Jul 2024 09:39:32 GMT  
		Size: 628.8 KB (628805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bda94db1fd7d84a94eb7af6dfe2e8e1bf5350fe9c3b315aa937ddb1b7963d4`  
		Last Modified: Tue, 23 Jul 2024 09:39:32 GMT  
		Size: 11.4 MB (11356577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759ecf5d4a5f49eca81d2c98bbcd37899e1925e58b3807326de7c0875fd04397`  
		Last Modified: Tue, 23 Jul 2024 09:39:31 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66beec5fc2780d7ebfe8f8039e96ff77c285a1b8187218e1fd65d2b2acf7b213`  
		Last Modified: Tue, 23 Jul 2024 09:39:32 GMT  
		Size: 4.2 MB (4159807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9af07072927b47ebd57164580c1b93acfc24bb0482c2696456ae7ea388d9690`  
		Last Modified: Tue, 23 Jul 2024 12:58:44 GMT  
		Size: 5.5 MB (5523958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:2999936a8b063356c9031f6efe6209aefd5c22d8178ee5a27c81878b18f55f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 KB (12219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9238027cc524ce506ca9facdb73a306b3ff6e052998f926958868d6b132d2f2`

```dockerfile
```

-	Layers:
	-	`sha256:6a893abcbbf780dc03e7bb318c80cbe6a2257ac661ace2fa457f6a06c3cd33ab`  
		Last Modified: Tue, 23 Jul 2024 12:58:43 GMT  
		Size: 12.2 KB (12219 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.19` - linux; arm variant v7

```console
$ docker pull hylang@sha256:69fa3b81ec8bec3d45d39eb24a0d4b3e56edddb210155cc6ced7ba60d4d4fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24652111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807b2b2cb57d83e3bbcb614bf8ec0775da228e9d02f235fd18f4e552a683b23a`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:32 GMT
ADD file:a79253a22e927307fa2edd1752e7945fd88afbb97c73bbbe771cc99947c0517a in / 
# Thu, 20 Jun 2024 18:00:32 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 23:32:36 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_VERSION=3.12.4
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4007367bb0cf596fd27d2207989b3864272eb2e5caf7429c07e68abc3bd47b0c`  
		Last Modified: Thu, 20 Jun 2024 18:01:06 GMT  
		Size: 2.9 MB (2926498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18da7f9ea4b72174affbaac4fba728f95028c8f23045119084033f40112c77fa`  
		Last Modified: Wed, 03 Jul 2024 07:24:27 GMT  
		Size: 628.0 KB (627994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093f0b868f5358b6ece70d49729b3c50893a7997b0c2351d9cbc05e52309e7aa`  
		Last Modified: Wed, 03 Jul 2024 07:24:27 GMT  
		Size: 12.7 MB (12693346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a157f2935b602d07d862f5bcd17ad348792b793b97b6cb8ede375996c408b0bd`  
		Last Modified: Wed, 03 Jul 2024 07:24:27 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec560426e1f6b8e3c6018cf74d48041d76f5c851261b73cd5e602053a7fd3565`  
		Last Modified: Wed, 10 Jul 2024 19:11:04 GMT  
		Size: 2.8 MB (2796777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6b29e45aafa944d3ee34ecd57b1b7d7060fcb8b068883c14b6fcfb0617ca1f`  
		Last Modified: Wed, 10 Jul 2024 20:07:07 GMT  
		Size: 5.6 MB (5607266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:6c85721818a95a4dbf92c536976e2aba92ecdb3b8b8ad334e4b3aac50756acf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1045834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5e1ff5afdb5cf9c7d2c655bf30f8ba146a96a81b120824e0736dacd7c44e4a`

```dockerfile
```

-	Layers:
	-	`sha256:1db3ee9f8474e32029cb7ad573ef4abfab0ff02c61d935822949541dcfaf18cc`  
		Last Modified: Thu, 11 Jul 2024 16:58:40 GMT  
		Size: 1.0 MB (1033396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0d9e36ea1b8614daac97e9195a0d1d952fba4a269e64dba2f5d93de061e4ac`  
		Last Modified: Thu, 11 Jul 2024 16:58:40 GMT  
		Size: 12.4 KB (12438 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:0c9842760c5b1dc70b3339889ece02e5a6ea76045c696c248a80fe291164402b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25520120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d97f53c62bf1148bc2571a29a27f06877a718421f9b1f8f38030dd6d42cf16`
-	Default Command: `["hy"]`

```dockerfile
# Sun, 07 Jul 2024 23:32:36 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Sun, 07 Jul 2024 23:32:36 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 23:32:36 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_VERSION=3.12.4
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e257f7a74ed4abedae801be4da90ed9a652c40aef959cab80130ac90e1b1d1ea`  
		Last Modified: Wed, 24 Jul 2024 04:40:33 GMT  
		Size: 630.3 KB (630336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e74f8d386611e38bbb7f7bacd24a7a13f68e39195dfdc0b4cf980a31cfa10b3`  
		Last Modified: Wed, 24 Jul 2024 04:40:34 GMT  
		Size: 11.8 MB (11847358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c164db8e736fdaf6d2e180265a02ea3cd57a01cf0b851eee7e2b1cf702314df5`  
		Last Modified: Wed, 24 Jul 2024 04:40:33 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e1c0d3ad9f9bba560c1e96bb67fdeacbdb9108e622b6cf03178b0c3bc7d1f0`  
		Last Modified: Wed, 24 Jul 2024 04:40:34 GMT  
		Size: 4.2 MB (4159660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe258bbe3793cb187ce044143484545ae6d710ad8e1077be3ad008f73a2567e8`  
		Last Modified: Wed, 24 Jul 2024 15:28:59 GMT  
		Size: 5.5 MB (5524078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:550328f668a991ec5c6786c1e754018f3d9d5ac466babc7fb4a56456dae7781f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1092401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50896fe73d2abb62bfdb1ff14d7373a5c5260e7fb8603742de9d518e2bffdc1b`

```dockerfile
```

-	Layers:
	-	`sha256:2e8ecaa9257a85fdabaeea45275b4353132ee47f2dde8fb97a328ede8c5e382a`  
		Last Modified: Wed, 24 Jul 2024 15:28:59 GMT  
		Size: 1.1 MB (1079606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5041e8a657efbc3e216828a92563af9dab4f80279fa27243e6d3c6e35b4c9561`  
		Last Modified: Wed, 24 Jul 2024 15:28:59 GMT  
		Size: 12.8 KB (12795 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.19` - linux; 386

```console
$ docker pull hylang@sha256:b92f1b9c882085483f3610755ecf31e1d4029501a15a6931af34cbf703a73343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25536877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d511382651d87080975232242c537a4608095a58537626297b396c133f97215b`
-	Default Command: `["hy"]`

```dockerfile
# Sun, 07 Jul 2024 23:32:36 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Sun, 07 Jul 2024 23:32:36 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 23:32:36 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_VERSION=3.12.4
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb990260759814a22dd46a3d2e679e2b42c3f9031c9e446554f4c0b6239e0cc9`  
		Last Modified: Mon, 22 Jul 2024 22:28:29 GMT  
		Size: 628.4 KB (628429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345cfcc12208b8f0de2a0522207b8435fc0f2fc845a8945ddab0d07309485a87`  
		Last Modified: Mon, 22 Jul 2024 22:28:29 GMT  
		Size: 12.0 MB (11971798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb52a51935387a673315a5ed53f4bb14c96dd0fced47dd2a995c20304edadba`  
		Last Modified: Mon, 22 Jul 2024 22:28:29 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62aa8a56eceb2081f4b6961f921bb585eca819de2d8d8319810ee30840ba1bce`  
		Last Modified: Mon, 22 Jul 2024 22:28:29 GMT  
		Size: 4.2 MB (4159725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7b7ecf49c76221665222454a4cdeffc1f51258bbf7ead11ffa1b38191abfa6`  
		Last Modified: Mon, 22 Jul 2024 23:08:15 GMT  
		Size: 5.5 MB (5524094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:9aaf1fff511155804050158438e5cf502576f219ec9fbcb05293225076468119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1091482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c081451c25ea4968a82e3af3dc39a177502f264a640656abf83ffa9e7c54f26`

```dockerfile
```

-	Layers:
	-	`sha256:461571ec865ce428b52b20777e066927ca27921b742342355e1f5eb68652026c`  
		Last Modified: Mon, 22 Jul 2024 23:08:14 GMT  
		Size: 1.1 MB (1079321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1241b3cc089c064f2e9b825a5897442471c9ede28635dc541cfc286acc1fad6`  
		Last Modified: Mon, 22 Jul 2024 23:08:14 GMT  
		Size: 12.2 KB (12161 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.19` - linux; ppc64le

```console
$ docker pull hylang@sha256:3e1037de9f441550311eb29c55df8ea692216054029205b2d4440390b61cb8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26746099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76551ea02417b0585d933b982648e114ac68b4e4b0cccec618c602acad022ed`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:27 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Thu, 20 Jun 2024 18:18:28 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 23:32:36 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_VERSION=3.12.4
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a87ce480a1e6b2a211e539793eb8993daec4a7b45a3b284a63476a172be632c2`  
		Last Modified: Thu, 20 Jun 2024 18:19:08 GMT  
		Size: 3.4 MB (3360635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610a000dea67f427739e4253b5c0995030afebc2443f8a05dd9e1c6ce628c5c6`  
		Last Modified: Wed, 03 Jul 2024 13:37:53 GMT  
		Size: 630.8 KB (630830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f724ee540cc933a77396f2aba943e9357c94661b4e553d2352fbf18e836e4b67`  
		Last Modified: Wed, 03 Jul 2024 13:37:54 GMT  
		Size: 14.4 MB (14350360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e50cbef7e000f70305fa18216c713a1dde11b632b224976ac0f689e19e217a`  
		Last Modified: Wed, 03 Jul 2024 13:37:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2e9fcfb45225befee9511ee4594b6416230bb1ae635e9ad665f04dda2d2f6d`  
		Last Modified: Wed, 10 Jul 2024 22:15:19 GMT  
		Size: 2.8 MB (2796810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138e816ad298fc772724d83280dd015d5feaae6de4834c3d78bdb3f589c2bd2c`  
		Last Modified: Wed, 10 Jul 2024 23:16:12 GMT  
		Size: 5.6 MB (5607237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:0d8e6036d31a3731b37cc35cadc91bab0cf5abff216f87cc5b9c7c9b206d02cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1041220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44296a4683489838258cb03c9c3154ad4deb89b7e5208ff0b3ab71d959ea97d6`

```dockerfile
```

-	Layers:
	-	`sha256:2c493593a7d18a74eab53d2367408a1b61dc2e78b7220000494d08a4b3a981ec`  
		Last Modified: Thu, 11 Jul 2024 16:59:34 GMT  
		Size: 1.0 MB (1028838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32694c059ae8184f9dcb8d189573098b21da9157e628d221a8cd5f35c1d9ce78`  
		Last Modified: Thu, 11 Jul 2024 16:59:33 GMT  
		Size: 12.4 KB (12382 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.19` - linux; s390x

```console
$ docker pull hylang@sha256:ec08c8ddad87ba61f7a28f7d713b3229a5d5412105409a425a66c53d545f7953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26364810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caac0ad8987894cbbf9e7a7f71a0ed2fd5196ab64868f3d1aba7bd259dda2266`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:12 GMT
ADD file:4aa205db6913ec3fd53a65bd281586a5f6abde77d41f1ffab554706c04822982 in / 
# Thu, 20 Jun 2024 17:42:12 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 23:32:36 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_VERSION=3.12.4
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:71c2dde42aad09035a9686e376c7507b6e8e2a8ada2c409775f1c1bfb8d928ea`  
		Last Modified: Thu, 20 Jun 2024 17:43:16 GMT  
		Size: 3.3 MB (3252491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fd969fb1447a056625a813142d0136ec2f1a214ec7982823c71fe162da1f81`  
		Last Modified: Wed, 03 Jul 2024 05:25:36 GMT  
		Size: 629.0 KB (628980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ed05ce5fac0e5ae5b113374527faf9f9287b6b0f32816e0875886a4d7d9079`  
		Last Modified: Wed, 03 Jul 2024 05:25:37 GMT  
		Size: 14.1 MB (14079287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441ed6d8233396a9fff24b8eaf6e0b5bb33a65e0c06af1c153942d61c4be7bae`  
		Last Modified: Wed, 03 Jul 2024 05:25:36 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c95ad4392d5c915c3b4f53d699b2d70ee02afd2630ee0fedc79b90e06e6e822`  
		Last Modified: Wed, 10 Jul 2024 19:11:27 GMT  
		Size: 2.8 MB (2796753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53b0d00556529e204904d48d9b75a731c6238caf5b0f8077e804e0b785d0682`  
		Last Modified: Wed, 10 Jul 2024 20:05:52 GMT  
		Size: 5.6 MB (5607069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:cf29cae360263df288e469280f59f11b9a86b5e84505915f8b3e20194dbfaf00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1040997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74059484585fb455c8b587cba5138d37903c3530925a9370b0b989fb417a189a`

```dockerfile
```

-	Layers:
	-	`sha256:01a55640eca4ce2400bf319794f044a3d3650baaa14113faeb3c4f2dee3e19df`  
		Last Modified: Thu, 11 Jul 2024 16:59:22 GMT  
		Size: 1.0 MB (1028732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c9b57b5aadcc7e27736bcd77176d4d57292efc57cf011c6019b3be2e11a4bff`  
		Last Modified: Thu, 11 Jul 2024 16:59:22 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.in-toto+json
