## `hylang:python3.9-alpine3.19`

```console
$ docker pull hylang@sha256:b722f64a4bebfd7d18b11dfd7a20eb936236c0dcd206630e00bc78b3c34ec84f
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

### `hylang:python3.9-alpine3.19` - linux; amd64

```console
$ docker pull hylang@sha256:5900498f514a722b5a6160aa4864e87370a437dd11461d3b92c4efe8d599165b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (21999917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c731ae6482741ebb62ed7739e6091864657b3fc87c55b8fa4e14ce59adcba173`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Jul 2024 02:10:08 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 08 Jul 2024 02:10:08 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 02:10:08 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_VERSION=3.9.19
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
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
	-	`sha256:bf984979439cac12d817c677dcb9f5fa394f2f5f4b7c64d6077dd72ab47f4b5d`  
		Last Modified: Mon, 22 Jul 2024 23:10:26 GMT  
		Size: 627.9 KB (627934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7971cf674b8dbdde520840a4aea144040c225f6df49401ecdd95d64368e8c2ea`  
		Last Modified: Mon, 22 Jul 2024 23:10:26 GMT  
		Size: 11.6 MB (11607061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffd89a304debd533d9a2bb420e88d89138ba82c5fb3646981e934de52f2c449`  
		Last Modified: Mon, 22 Jul 2024 23:10:25 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868562c8ba21744c87a76847294f875d3c062e3012aa8dc21a601817d3e8b31d`  
		Last Modified: Mon, 22 Jul 2024 23:10:26 GMT  
		Size: 2.7 MB (2694907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b85ce50b120a274261a52059bba113a24a3c2f9df95e53d9cf76d5de3010f3`  
		Last Modified: Tue, 23 Jul 2024 00:08:27 GMT  
		Size: 3.7 MB (3650746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:30f75f27b8e78f7867bf731a8462ee8191a08ad6b07f2d1a64a7c076c7fa4ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1047301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b69ac2086a2846059b3dcc29f081f18671ad21de054f0325847cc1c8213834`

```dockerfile
```

-	Layers:
	-	`sha256:bf759408b8bbe9f1bb086443876f08c357c201eec3f48bb0d9f47b33fea93abf`  
		Last Modified: Tue, 23 Jul 2024 00:08:27 GMT  
		Size: 1.0 MB (1037501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cee729b6f073edce5e629d93ca32aef6205578d978ebc19d84d8233f245e12db`  
		Last Modified: Tue, 23 Jul 2024 00:08:27 GMT  
		Size: 9.8 KB (9800 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine3.19` - linux; arm variant v6

```console
$ docker pull hylang@sha256:23adcd38e17da873b0ce44f5b2ee25a692fb39a46be7cce1de0a42ba4d4752ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21396075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb18caf8009c99468aa4d2793f2727ff24353c5855e00a4b7eec8a748c0191ad`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Jul 2024 02:10:08 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Mon, 08 Jul 2024 02:10:08 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 02:10:08 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_VERSION=3.9.19
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
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
	-	`sha256:a2c88bae6d1febf32c357980b09fd0b6799e12791538e2d1c4dcb28303ebc1fe`  
		Last Modified: Tue, 23 Jul 2024 10:18:55 GMT  
		Size: 628.8 KB (628801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b4e8c4166f65f82d9884aff23a33dc6d220295f24457c9027ba13aada18c7`  
		Last Modified: Tue, 23 Jul 2024 10:45:00 GMT  
		Size: 11.2 MB (11245563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d2dae28626e110f1a6a3e6f496d509046fbabff28af00b042f823b917feef6`  
		Last Modified: Tue, 23 Jul 2024 10:44:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6789c4b6ebc8b8edd84acf29ada066647dfaac74fe34e536623d19acbc9d2cf`  
		Last Modified: Tue, 23 Jul 2024 10:44:59 GMT  
		Size: 2.7 MB (2694748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8091a689d972ab3d8fff0e3773f64dbc5db5e542934f507ebd76ae9d5322acc`  
		Last Modified: Tue, 23 Jul 2024 13:02:08 GMT  
		Size: 3.7 MB (3651062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:e483c57b4dbc51441385dd32252b3abeccb35fcd1a8d3f5d020fb97ecb295fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 KB (9701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d0ca6eafcfc6c65d51a3444e78c9c53df36bd034d67685983ea1abefadbbd7`

```dockerfile
```

-	Layers:
	-	`sha256:027d74c84baf776a27c9fc448c42da1510c120a47e1de869aef606f888f2a5af`  
		Last Modified: Tue, 23 Jul 2024 13:02:08 GMT  
		Size: 9.7 KB (9701 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine3.19` - linux; arm variant v7

```console
$ docker pull hylang@sha256:fa8876b0bc0a3411566abcfd1038ef6445fdc6376eb1a2f6abbd8aac05e59d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22505209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28397a17065e2da13976ae8be01f3bdca84440c0eef160699bc6bab9fc97d951`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:32 GMT
ADD file:a79253a22e927307fa2edd1752e7945fd88afbb97c73bbbe771cc99947c0517a in / 
# Thu, 20 Jun 2024 18:00:32 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 02:10:08 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_VERSION=3.9.19
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
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
	-	`sha256:981248633f1cddd0e975edc0ecffbf23a8f1b5737627984e2c968b8d9a9c1ec4`  
		Last Modified: Wed, 03 Jul 2024 08:37:22 GMT  
		Size: 12.6 MB (12604425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133f9e2912d741cfde5dea9cd3183b52df61633a44d3c30bcacba58a4633c9fa`  
		Last Modified: Wed, 03 Jul 2024 08:37:21 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c8e9d4fca296c067e2f373c5ba68ad454460efa1bb15aeae884e52391b8183`  
		Last Modified: Wed, 10 Jul 2024 19:23:35 GMT  
		Size: 2.7 MB (2694939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083a118084e3e83c1d82ed1b6f28c67c3ab1257805fb930491fa4d76f7a88bc6`  
		Last Modified: Wed, 10 Jul 2024 20:14:29 GMT  
		Size: 3.7 MB (3651123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:558e197e1f156d97c4c49368c30b556b5b7cc3d76b76c3da191299de626f8049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1040830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d489a30487c3358e98b705bec2c1deb69af1737baba04e57508ad8e535ee587`

```dockerfile
```

-	Layers:
	-	`sha256:5e4a7b0ac59f1ef9a0e29158acd0d0e5ab4669f3ded4bf015c83451f818465b1`  
		Last Modified: Thu, 11 Jul 2024 17:02:52 GMT  
		Size: 1.0 MB (1030910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fb13e020f09326854c7a32e5634c5aaa3408206b560ed88a5aa68abd333ae18`  
		Last Modified: Thu, 11 Jul 2024 17:02:52 GMT  
		Size: 9.9 KB (9920 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:98df911b912b954ada0f47beb938b1e579048f4f5f98492766dd406bd779d16c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (22020990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0094bd385479394372949d3aa14e42c5fa8faaf853753c56d77a11be7c24528f`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Jul 2024 02:10:08 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 08 Jul 2024 02:10:08 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 02:10:08 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_VERSION=3.9.19
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
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
	-	`sha256:dbda74155d56c4eed22fadc32b3e0741a3939ab93f4011ec4e9c3f7b6283247f`  
		Last Modified: Wed, 24 Jul 2024 06:41:59 GMT  
		Size: 11.7 MB (11686128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e605affe908578c0bc344e3a4480141aab75fb70b36ea73a951dd46afaa5b1`  
		Last Modified: Wed, 24 Jul 2024 06:41:58 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fed7b778136c5b07b2b80e7a0bba43c485a0ec82838dcc4c2a7395c19df6f4`  
		Last Modified: Wed, 24 Jul 2024 06:41:59 GMT  
		Size: 2.7 MB (2694884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac9b338aa64a6c6f44f55f1c8ddd1651972f87d5369f2de8801ec0350e623db`  
		Last Modified: Wed, 24 Jul 2024 15:35:34 GMT  
		Size: 3.7 MB (3650954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:06ecaf11073284e573863890e49231193449f32542987b6ac678169c9adb92fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1047850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e8356b7daf672753374dcf5fd5a35757a5a1af0547f16781474fd0b99f7c44`

```dockerfile
```

-	Layers:
	-	`sha256:992defb843b426cc0868a596c93d67a37d0033fbdc2dc65e3b726646eebb5291`  
		Last Modified: Wed, 24 Jul 2024 15:35:34 GMT  
		Size: 1.0 MB (1037605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd5f3ce066ed02bb3e0876d7c3a5ed683e215dbe650fc08ac55f42afe4eaafdc`  
		Last Modified: Wed, 24 Jul 2024 15:35:33 GMT  
		Size: 10.2 KB (10245 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine3.19` - linux; 386

```console
$ docker pull hylang@sha256:f1d8be03d126c8e98b0f5926bc223a27e821e76f7df9a0d9d424cf9c0e5f61df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22070032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0603c01e669cb506a8a1bd8f352066dcfe67ea37d7e79eefd3a2f909fc30865`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Jul 2024 02:10:08 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Mon, 08 Jul 2024 02:10:08 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 02:10:08 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_VERSION=3.9.19
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
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
	-	`sha256:10c9893213e4f29f3e2298a71664d1b3b534877ba7a2aec574cfd71369163afa`  
		Last Modified: Mon, 22 Jul 2024 22:11:24 GMT  
		Size: 628.4 KB (628428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f8a992b36a33f0d4a30127f7fe3462ab6d2d8b9d3c6c21760184fca7764d3f`  
		Last Modified: Mon, 22 Jul 2024 22:11:24 GMT  
		Size: 11.8 MB (11842931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b25fe62019ead0860864eeb13bbb44ff657c8b148bd8093d391e5a67b43c3c`  
		Last Modified: Mon, 22 Jul 2024 22:11:23 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040afc3dbf0a6e510836a244ce3c88aafb435d622c4995b49bef2d8300658de8`  
		Last Modified: Mon, 22 Jul 2024 22:11:24 GMT  
		Size: 2.7 MB (2694924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2dc5481c7ae0fd705031189590e78fa9d254ba05d66f02c889bca65f3d9fab`  
		Last Modified: Mon, 22 Jul 2024 23:08:39 GMT  
		Size: 3.7 MB (3650916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:d1674d5d18fd14be8bfd4aada0da40c7db8611d3d820059b125cee9dba0b0b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1047204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e695f4a66edea39669a8cf1634295f126fad4b5045863a210eb30b3b30d8f1`

```dockerfile
```

-	Layers:
	-	`sha256:cb4259e55f6fea50252cd188387146824a4bf976fe30eecd54e966019d36f1a1`  
		Last Modified: Mon, 22 Jul 2024 23:08:38 GMT  
		Size: 1.0 MB (1037456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eac85fb212732a779195c28bd0516a5f3e19cd4680f18bf7301c5b6da5f7fdb1`  
		Last Modified: Mon, 22 Jul 2024 23:08:38 GMT  
		Size: 9.7 KB (9748 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine3.19` - linux; ppc64le

```console
$ docker pull hylang@sha256:8c5f1485a73c0da2fde5377bc6e2f1a7237da06f31619585f137690669c91e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24482801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ccc975d129d3592bcf4bc0f638bfd9bff4c30487500ad5c728a7e2ddd4edcf`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:27 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Thu, 20 Jun 2024 18:18:28 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 02:10:08 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_VERSION=3.9.19
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
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
	-	`sha256:6519467af49b00b1f4c5979de85a570f526f412f4c4e7296e18dd55d963e8083`  
		Last Modified: Wed, 03 Jul 2024 16:39:02 GMT  
		Size: 14.1 MB (14145168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0fc8b921031d21c13adb284286f038da0c58f674f1934dd69cb6c3d6287bd3`  
		Last Modified: Wed, 03 Jul 2024 16:39:02 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4828e5dfed7d4b1772a479141d1ad2f8afd625a46a13929fa96de4f14d2a12d0`  
		Last Modified: Wed, 10 Jul 2024 22:30:35 GMT  
		Size: 2.7 MB (2694924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ff019dda086667e08e7d5198776da29fb8b5ec6d3ced083e5223bc84bcc9f1`  
		Last Modified: Wed, 10 Jul 2024 23:25:40 GMT  
		Size: 3.7 MB (3651016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:7c6a131c9d286266212a7db16de1446a92383f1d551010084dcdffe9324d9cb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1036248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b0b41c022ebf8fadc844910bb206e4a0becfc181285add9ecedd7295ff4a54`

```dockerfile
```

-	Layers:
	-	`sha256:a3f9999cff3c44a785f556efd3c6b26ea4d48439033f1a25d1ac54ede215fec1`  
		Last Modified: Thu, 11 Jul 2024 17:07:56 GMT  
		Size: 1.0 MB (1026368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c57e1ac703af4ffe991557edca0deed2c55191acc3f3da00847babee25e02b53`  
		Last Modified: Thu, 11 Jul 2024 17:07:56 GMT  
		Size: 9.9 KB (9880 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine3.19` - linux; s390x

```console
$ docker pull hylang@sha256:dafe0373ebd7c9ad421e7ba1e51486aa7ee84a144a6a2853125b355c5b643b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22104663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51786578d31e7507fd638d4a3cecac98ae10d1329e32f7aac7bf95bd56e9b5b2`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Jul 2024 02:10:08 GMT
ADD file:b52033eb72014ee086783e139c55b353697322576013415769016a48fd4f4342 in / 
# Mon, 08 Jul 2024 02:10:08 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 02:10:08 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_VERSION=3.9.19
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 02:10:08 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 02:10:08 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 02:10:08 GMT
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
	-	`sha256:1f544ad804b60fa6fc54acddfe2c176a2b22e7079fedbf238b2c2bb51b8d0dfa`  
		Last Modified: Mon, 22 Jul 2024 21:51:15 GMT  
		Size: 3.3 MB (3253076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a739e3e169fda0f1b9cc4d6f91afe85f7a222d36be7cc6e35447cc2a89c553d`  
		Last Modified: Wed, 24 Jul 2024 06:02:11 GMT  
		Size: 629.0 KB (628994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15474a585e66c12c84fa6af775ec1b8df4ae73411107bd3a9e78d18638dc8445`  
		Last Modified: Wed, 24 Jul 2024 08:11:58 GMT  
		Size: 11.9 MB (11876412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd484a6bcb8ed5a028064c619c923eee28cb9ed953d5c568c45bc6df70355b5b`  
		Last Modified: Wed, 24 Jul 2024 08:11:58 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e51c353355045c1ae50f284ad7fea2525631e1123f3d3e8972afc0084bd06d`  
		Last Modified: Wed, 24 Jul 2024 08:11:58 GMT  
		Size: 2.7 MB (2694888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc07a7e0d97ef18cf5a16096f4a33cd1fbe7625e82319c9ec20f1ffd726c69b5`  
		Last Modified: Wed, 24 Jul 2024 16:41:25 GMT  
		Size: 3.7 MB (3651059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:63726f868c2ec4d2b010b6d642af473011c7ce8986634ac491bc3ead0d4ff0d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1045359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9f2675c5d8eaef84da945552c64a3cba5fe64cc79fceb04d28f27ca0dfd307`

```dockerfile
```

-	Layers:
	-	`sha256:6efb0677747731c03044351947ac0f678fecf455e55183abdd8e20b8fc2afb09`  
		Last Modified: Wed, 24 Jul 2024 16:41:25 GMT  
		Size: 1.0 MB (1035547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967b76a751eac83ada205e90b7f2a79801329ec96678cb6f7ac1b49872b19227`  
		Last Modified: Wed, 24 Jul 2024 16:41:25 GMT  
		Size: 9.8 KB (9812 bytes)  
		MIME: application/vnd.in-toto+json
