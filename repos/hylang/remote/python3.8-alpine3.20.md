## `hylang:python3.8-alpine3.20`

```console
$ docker pull hylang@sha256:05a9d4944228572940dfdabcc83f28582b8e24dc6c695c29f7e5f7355118fd12
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

### `hylang:python3.8-alpine3.20` - linux; amd64

```console
$ docker pull hylang@sha256:cb01b13a601fa4233799a7c4a8da6826a0152b947d86627d49e884fb8f8e4f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 MB (24312583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1328659b2581d116223fa1c1233fedbab868517b7234c47aff0a720899ff211d`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cda287a5cb387e5c9903ea9e216dffbc6e6365f652663b98543e033cd4a0988`  
		Last Modified: Wed, 10 Jul 2024 19:12:01 GMT  
		Size: 461.8 KB (461832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d585f28638636cccf3bbcc7ee0cf32ce1c038d740a4836ffc326c45ceae72c2b`  
		Last Modified: Wed, 10 Jul 2024 19:12:01 GMT  
		Size: 13.8 MB (13773305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dd7b899ca49bd8fd144cd95a500f2263a9e2908cc3e075a82b0bd1d98b2b54`  
		Last Modified: Wed, 10 Jul 2024 19:12:00 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293cb43cc7d6092c5cd9be0923c56cfa0ec9024cc159b64b417456fd23c0edad`  
		Last Modified: Wed, 10 Jul 2024 19:12:01 GMT  
		Size: 2.7 MB (2697327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee65fc68ae24331a8b7ba2efe9ef1eddfd1e17841777c63a60da6416b4ae149`  
		Last Modified: Thu, 11 Jul 2024 16:58:21 GMT  
		Size: 3.8 MB (3756045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:73edad86c6760b0906f96f07e269c09a666e8cc1ff1550ea9594322689eaecee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.9 KB (660920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f2f232cb9ce392fbda5ad4ed476646e0d864f383cff441dc30834dde7460ee`

```dockerfile
```

-	Layers:
	-	`sha256:36d99503e5db86d8932d64913ff45c4bf254d3c27f15ff890e922b015440a8b2`  
		Last Modified: Thu, 11 Jul 2024 16:58:20 GMT  
		Size: 652.4 KB (652420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eca39c812d91f06346b16ed31fbfda36d64b40cc891f5365f1a1dd7b69ad2f7c`  
		Last Modified: Thu, 11 Jul 2024 16:58:20 GMT  
		Size: 8.5 KB (8500 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.20` - linux; arm variant v6

```console
$ docker pull hylang@sha256:1e075231abc60ea1a8dc9e8fcf60041dbd3b0b3396f4dbf1a98accf7b4d06aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23394085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d018096734c07dfb761a7250b8467062af54abd125752c61c84d0c52bc7f4f5`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
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
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba80aed40dc0d93565b3fcce19703d79949c65bed2ae051e3cb520c4e577d7a0`  
		Last Modified: Wed, 10 Jul 2024 19:59:42 GMT  
		Size: 462.6 KB (462618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2106f698036c043239df16c91d736ee492e299d3762ef47ed72a3f1da69e056`  
		Last Modified: Wed, 10 Jul 2024 21:20:47 GMT  
		Size: 13.1 MB (13110574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d93c0563537b4d21c34c41228d770215b20df7b15f76db30907b50ad56c449`  
		Last Modified: Wed, 10 Jul 2024 21:20:46 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592a712dac895e9e51b726aaae1f3157d950ab871b8cd69f521f34169a37580c`  
		Last Modified: Wed, 10 Jul 2024 21:20:46 GMT  
		Size: 2.7 MB (2697339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc8acac33231ee0568d21d6167eb727647a2da3632895789ff70c9341bf5750`  
		Last Modified: Thu, 11 Jul 2024 17:02:17 GMT  
		Size: 3.8 MB (3756172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:e35e9a9a3cd6611a9022cd0d04549f9fe1b1c21af92fc0a71aef8d5a6852ba89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 KB (8357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55742b535fce7059f0df30cad5d2fdb83d0080e6abbbc013d817d9ff04172b06`

```dockerfile
```

-	Layers:
	-	`sha256:8018394aedeb9fbdd40deb3c34b0f4f9294cb96bcf9ed33a7079af67ecaeb650`  
		Last Modified: Thu, 11 Jul 2024 17:02:16 GMT  
		Size: 8.4 KB (8357 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.20` - linux; arm variant v7

```console
$ docker pull hylang@sha256:0d8afb5a77df2c674ae219ccd505b16681d5bd9ce2b35dd16711db39ddd74425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22588055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d66c95d6992bedd7cffb2638137b506aacf842ccb859b3fda7e0de851024017`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
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
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67fbf7b03239e69ea5cefa1b3bcbeb41abb2359ce6e7c757b9818b1d72bef20`  
		Last Modified: Wed, 03 Jul 2024 07:06:27 GMT  
		Size: 463.2 KB (463183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4992ad3b4d201d972eb764216ca5e39645df2650140369fed5716ab3533903`  
		Last Modified: Wed, 03 Jul 2024 08:51:12 GMT  
		Size: 12.6 MB (12576235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7051c38e4326780ce9afa08e1336f3547f88ed5c0bfeedf93651e5a160f979`  
		Last Modified: Wed, 03 Jul 2024 08:51:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e0232fe4491d75ee723142cedd2996e8a5796239bcad879eb7bd183fc20c7b`  
		Last Modified: Wed, 10 Jul 2024 19:27:07 GMT  
		Size: 2.7 MB (2697322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456bd0b0d249de18953c3a613fb25c43b59965f3f1ba6439d130d4d559cdca85`  
		Last Modified: Wed, 10 Jul 2024 20:16:24 GMT  
		Size: 3.8 MB (3756231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:8a046d2ce613668a80c3757da2ea4007ec623da3b88f33d18bd1ff69ed2c1836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.7 KB (662667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0bf10333594ffd501daeb13f821937c0e65f60bb917fec43e12cf5ef598b9d6`

```dockerfile
```

-	Layers:
	-	`sha256:867a5e7c47eb8882bd60e74f46ffcc1a4ea79d8acb6aa992d439bf08871083e2`  
		Last Modified: Thu, 11 Jul 2024 17:03:51 GMT  
		Size: 654.1 KB (654079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff0b1dbb036b13982cacc8fb131a6564821a02fac7afe868e75ff13503348a44`  
		Last Modified: Thu, 11 Jul 2024 17:03:51 GMT  
		Size: 8.6 KB (8588 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:10fa16643199c7340d600b7ee9a873b4fb12eeba8ebf2d93cae6edcd9fe091cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25288178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03885107b863c29c646865feadfeb2c48dae07c7935626fb352ca5d69f8a85e`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651520864e37836e5ab990630591892b9d8473fa358c43e86895ef38eabe513f`  
		Last Modified: Wed, 03 Jul 2024 05:38:30 GMT  
		Size: 465.6 KB (465596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a89428f232d6923edfb02507db99f5d47a1e2be1258d625f06bf45fca32d5f`  
		Last Modified: Wed, 03 Jul 2024 06:59:24 GMT  
		Size: 14.3 MB (14280159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de11a9b084b0d9f127fce7de119abb9a2965bc42b1f49a8a65caf23e711b773a`  
		Last Modified: Wed, 03 Jul 2024 06:59:23 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4205dff3e57922ab092107071d5160a4455fe565d1e3985d62d425c7e353dc38`  
		Last Modified: Wed, 10 Jul 2024 19:20:40 GMT  
		Size: 2.7 MB (2697332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26469e3ce9fb1486e09f53cf676ff76d7d244beff2b7450254877e4e2d37cafd`  
		Last Modified: Wed, 10 Jul 2024 20:09:27 GMT  
		Size: 3.8 MB (3756062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:647d825a70f0f3e17f2436fd773f008f62c07e97b4ecc3066c00bd9d5793c057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.4 KB (660418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63bc31a1bf315e38c975de20cf072b417b7098cb32c95316067aabaa47ccb96f`

```dockerfile
```

-	Layers:
	-	`sha256:87f0b90bd63a4de74f6ed821e13797e2c244238e5a2688544d7198de8c7725ae`  
		Last Modified: Thu, 11 Jul 2024 17:03:24 GMT  
		Size: 651.5 KB (651521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77ab15a6753cec7a3a8125a30637160fd67f947548ff4be8c36ab93130f1aae`  
		Last Modified: Thu, 11 Jul 2024 17:03:23 GMT  
		Size: 8.9 KB (8897 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.20` - linux; 386

```console
$ docker pull hylang@sha256:780bda068efddda66df90b381704e9a3e26acfc3589616184054829a015bc889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24224060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62c65ca847333debcf8e186090518f603bdab35fb011b7f42555d8e99d25fad`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:24 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Thu, 20 Jun 2024 17:38:25 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
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
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae71512a57e906d6d3338e15934c8b872616b9e828de39c94a3fc7c4b657771`  
		Last Modified: Wed, 10 Jul 2024 19:13:36 GMT  
		Size: 462.2 KB (462223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df92d691542de12bb58db041a433ddfe70c24d31bb45923d3dae549cdb3acc1c`  
		Last Modified: Wed, 10 Jul 2024 19:13:37 GMT  
		Size: 13.8 MB (13838545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7f385105731438c986749b5d621ad2573171452e4dfb2c946944072ddb82bd`  
		Last Modified: Wed, 10 Jul 2024 19:13:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50398743d95cdd2c37a7bfbe5a5aaf6d18afc7fa51b62e7e0050338b8e77e6a5`  
		Last Modified: Wed, 10 Jul 2024 19:13:37 GMT  
		Size: 2.7 MB (2697319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a37c886de58458affa0421d63a51bdfda8e380f5566d540a71818b223e1f0c`  
		Last Modified: Thu, 11 Jul 2024 16:58:19 GMT  
		Size: 3.8 MB (3756273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:6f1ab66891b3db7cf9d8ac76d4973613ae55b77595b94d21034826672194077f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.9 KB (660861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9607bf7e310b2dd1c49b281959313a24c278ecb109dafccb77b59a264d7ce06`

```dockerfile
```

-	Layers:
	-	`sha256:d8f40e6fdd0f2e35cf61e2d327dd3ef6bfb316fd3b94970b9cdb86befb460711`  
		Last Modified: Thu, 11 Jul 2024 16:58:18 GMT  
		Size: 652.4 KB (652395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:086ce89c1994b1eefc23d723127d4dc1cff17d05c133cfd05fdc89924d6daf87`  
		Last Modified: Thu, 11 Jul 2024 16:58:18 GMT  
		Size: 8.5 KB (8466 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.20` - linux; ppc64le

```console
$ docker pull hylang@sha256:612d80182427f1bdbedb05bace4443d9c1a58f15b372f75b4b98ca951b2f0baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24604532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6418b635df4a4fc591ac15496f5c74aaa25411b1a0cc5ff906cda1edc71cf7ee`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
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
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03dda537e2a89e050c4a6baee145aa8999cb1aeb295d4b29f95940b9351c2e3`  
		Last Modified: Wed, 03 Jul 2024 13:15:42 GMT  
		Size: 466.0 KB (465998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09212bc29ebab8e325b8b8a68dc45c63560693164191e56dab1ee761f5368640`  
		Last Modified: Wed, 03 Jul 2024 16:54:28 GMT  
		Size: 14.1 MB (14113022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f06fe6cd0d968abbb73c9378fb82d23c8616d47ca432e4b1ddc3e9e752d041f`  
		Last Modified: Wed, 03 Jul 2024 16:54:27 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149bce38fde7e4441856bf305fe86171daedfe68569a57812e4f8cafc8bda4fe`  
		Last Modified: Wed, 10 Jul 2024 22:35:03 GMT  
		Size: 2.7 MB (2697312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5850ab7aee3a0c39d88b26946d024f6214a525171ff58c340fabbf8ef8b944e0`  
		Last Modified: Wed, 10 Jul 2024 23:28:23 GMT  
		Size: 3.8 MB (3756271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:64821677f0e141905b598e89cb5c638641a6ae738a7f4a619c894b4a41c2a3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.1 KB (658098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959a5a68c39a18e336e53553eff81285841facbe44dc6e23effd80a77e97d4e0`

```dockerfile
```

-	Layers:
	-	`sha256:a0bd9131b8d5cbbe02e35822c24ec55a22fd8d5726a54524d25063ae3deb372f`  
		Last Modified: Thu, 11 Jul 2024 17:09:18 GMT  
		Size: 649.5 KB (649545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31f416ea5d95eee47b737b9b325a0c48043d9237ef260de00052e097cbbaba81`  
		Last Modified: Thu, 11 Jul 2024 17:09:17 GMT  
		Size: 8.6 KB (8553 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.20` - linux; riscv64

```console
$ docker pull hylang@sha256:d5993533e1eab8b1f4c20ae2d00a349ad4c512b9167c30d12a8368b0eb54d516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23715265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039a56ce357e05c928cd92cb32abb4cb142a427d888fd06d702e84401bf1abbe`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:03 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
# Thu, 20 Jun 2024 18:18:04 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
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
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345891dcc3e2a64fb9a9364c2ac331cbfcd9bac3f7c68e03933d19e027ace86d`  
		Last Modified: Wed, 03 Jul 2024 13:44:08 GMT  
		Size: 464.0 KB (464022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5604d5a6197ef9990241acd8b81e5b8e3abb7f774fa7720018a98d5bdc422a`  
		Last Modified: Wed, 03 Jul 2024 14:57:53 GMT  
		Size: 13.4 MB (13425275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be815405dce52fa0731cc7ccdc619c1d9657864f675df31f48434044b76ecaaa`  
		Last Modified: Wed, 03 Jul 2024 14:57:51 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3472c0ca9b0ec30acad0df3da1ab33ec09f8cec62d6087afdaf15e0f8b4f0bc`  
		Last Modified: Wed, 10 Jul 2024 20:46:21 GMT  
		Size: 2.7 MB (2697422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d837d21c29f5199aa2997ef67bac905755249fc16326cc2509ff7ebd4fd270f3`  
		Last Modified: Wed, 10 Jul 2024 21:19:26 GMT  
		Size: 3.8 MB (3757278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:5a28d1ac36f9126a6434c07a386bb424b7516d81c502fc1cc8e6320b6ed066cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.1 KB (658095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1671533ec6f1dd7528f70f248abe98e7a2ed01048a67e8a1dde6c2ddabed57`

```dockerfile
```

-	Layers:
	-	`sha256:c92555f46ce94c8bfe10e1b92f3c9013b4598af4df1f5c1104e6fb3af302b273`  
		Last Modified: Thu, 11 Jul 2024 17:00:10 GMT  
		Size: 649.5 KB (649541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61c142478056b54544904a69a1a33f6fec87a559773e97f160e1e7042e96a94f`  
		Last Modified: Thu, 11 Jul 2024 17:00:09 GMT  
		Size: 8.6 KB (8554 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.20` - linux; s390x

```console
$ docker pull hylang@sha256:381528998e96db157c8dbe347370a9c323ef8c13b17f0c79142c7289170ac240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24188932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae98d5fa2b0215d42d4213b4f99ae92a2b9fc96f1cc714ad697de02ed07027ff`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
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
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81372ec9eec545e9af2e05c16da4cf7ebcaa676e104e5924b51839f59c80730c`  
		Last Modified: Wed, 03 Jul 2024 05:10:43 GMT  
		Size: 464.2 KB (464153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749b8e71379b6888c52f0ac7161585c2358586b49495a21ce9faa32f053884d1`  
		Last Modified: Wed, 03 Jul 2024 06:35:42 GMT  
		Size: 13.8 MB (13809460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45722d661bf93d4b9228032440d31212d5ba6528581ccbe33ef209f53f407bf`  
		Last Modified: Wed, 03 Jul 2024 06:35:41 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a85e7c2e1a837ed709b0836a2a394310527ffcb4ca5bb4593d25bfc43c1529`  
		Last Modified: Wed, 10 Jul 2024 19:30:54 GMT  
		Size: 2.7 MB (2697208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8601a2023717bddf3690cb4c0a13b86d8265bf4985e92cc1cc1294b8b546f810`  
		Last Modified: Wed, 10 Jul 2024 20:18:23 GMT  
		Size: 3.8 MB (3756025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:de1f0689ae7901109f5e74bb8d12869b58bc449e1cd104e26e9cc664381ff12c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.0 KB (658023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355f6ea297fa766930e2bdbf4e5abf99cbe7ac382892d17ba7d6529520da5eb3`

```dockerfile
```

-	Layers:
	-	`sha256:38473b87412de3cf2ec16fdd912b67e90a339e478fc7e4a20ef0760e7a7562f8`  
		Last Modified: Thu, 11 Jul 2024 17:07:39 GMT  
		Size: 649.5 KB (649511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91cc46de878921013cc6a2884fbb89916d2c1425936007634f806982bca74603`  
		Last Modified: Thu, 11 Jul 2024 17:07:39 GMT  
		Size: 8.5 KB (8512 bytes)  
		MIME: application/vnd.in-toto+json
