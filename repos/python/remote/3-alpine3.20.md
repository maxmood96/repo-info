## `python:3-alpine3.20`

```console
$ docker pull python@sha256:0bd77ae937dce9037e136ab35f41eaf9e012cfd741fc3c8dd4b3e2b63499f12c
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

### `python:3-alpine3.20` - linux; amd64

```console
$ docker pull python@sha256:ebe4166fcf7fd212975cb932440ba69cfd6c27fdb9ab2253f965a1d2d7f1c476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21076180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad3ec94c61cb6bb3b0dd6698b4859a48628d782af7743d7e2e54169b77e910e`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
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
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf61f78292651fa8fadac1ebf3a9a254eed574bd25384e9204913dc10aed830d`  
		Last Modified: Wed, 10 Jul 2024 19:15:42 GMT  
		Size: 461.8 KB (461840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebb9be3b50110b912abc31de5172e43a5a53aa22153cb13742c77fe0b7e1e39`  
		Last Modified: Wed, 10 Jul 2024 19:15:42 GMT  
		Size: 14.2 MB (14193489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79cbbc17282fcc23e91f188b04af8a10b980eb0badc6fdc717bec37463a7cf9`  
		Last Modified: Wed, 10 Jul 2024 19:15:41 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f29a7b2e9bd862d641c02ba520b2409bd181aa8dfccd311dcb3f132f0b0df5e`  
		Last Modified: Wed, 10 Jul 2024 19:15:42 GMT  
		Size: 2.8 MB (2796778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine3.20` - unknown; unknown

```console
$ docker pull python@sha256:b451d97d033dee16af87f520bf7064fe16d79849287caa5accb9df8a1e3a1bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.2 KB (670206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0bee723459df794ae59de5d6b1acce63e7435111c23ec5adb2fedb85f81ceea`

```dockerfile
```

-	Layers:
	-	`sha256:b7f433a75922791410575df43bc784858e93031445fca87cb31f23b8a9632e85`  
		Last Modified: Wed, 10 Jul 2024 19:15:42 GMT  
		Size: 644.9 KB (644876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0e90b67b703b7115a27f3f15c232a713272db06e2475274df5d058ec46577b2`  
		Last Modified: Wed, 10 Jul 2024 19:15:41 GMT  
		Size: 25.3 KB (25330 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine3.20` - linux; arm variant v6

```console
$ docker pull python@sha256:657e2dd8199bd0180b5624885fa760fd4052e532e3bf65db2bfe009c5c80c34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20068147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c0a37576677d607686861fb64c31a3f30b97ded14b7e34fbec4a5496df84ce`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
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
	-	`sha256:7c8eb7954d38312547c265f55642a2ae2f55edec61b3f30924211c60652052da`  
		Last Modified: Wed, 10 Jul 2024 19:59:43 GMT  
		Size: 13.4 MB (13441362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c720dd93cdf015141512ed92c6b758bc1a1a8c207d498e93c10cb391d48b5f20`  
		Last Modified: Wed, 10 Jul 2024 19:59:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fade912e1bea7cdd4e9563c8327d91494cb8146da73b5046ca49112a5e2508`  
		Last Modified: Wed, 10 Jul 2024 19:59:44 GMT  
		Size: 2.8 MB (2796783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine3.20` - unknown; unknown

```console
$ docker pull python@sha256:ff3e55ba4b7f961ee1dc8c00e08835bdad6f2be772af766e64c9f09d724f763e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b1fa41bde09c4bd94c6ecfe970e7c9e73e403ba036a55d29a351892c8f0001`

```dockerfile
```

-	Layers:
	-	`sha256:118001b71d4a943eed79bdc85a46c2c2c47277cc82127b53534a5a7f204da70e`  
		Last Modified: Wed, 10 Jul 2024 19:59:42 GMT  
		Size: 25.3 KB (25252 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine3.20` - linux; arm variant v7

```console
$ docker pull python@sha256:01456063c10891b9ce778d24ae5788df8b06a2e32ddddccc70abfa25aef3fca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19227601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b999abf42744d2be5a186a9e63284b2a16dd32d65eb702c1e9f124696902c158`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
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
	-	`sha256:a71f6fbfd0dc9de3438813b92d7fc9c67a9defdfd51a8a42533c42a1ac73c408`  
		Last Modified: Wed, 03 Jul 2024 07:06:28 GMT  
		Size: 12.9 MB (12872496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f52a81baa128154781aed295352ab1b33f5fdce69412925d29775a39e17b10`  
		Last Modified: Wed, 03 Jul 2024 07:06:27 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1590e867b602bf16b477b961c88956663ebd2063da020f1e0b2cee2d72fae95`  
		Last Modified: Wed, 10 Jul 2024 19:10:35 GMT  
		Size: 2.8 MB (2796836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine3.20` - unknown; unknown

```console
$ docker pull python@sha256:0200bb377ab36e63a8f8527784ed3da2b5590bf403765f5cc410f168755596cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.0 KB (672037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c36f95cea6303ecabbe69ce76ea401f1cea603781174913a63f5e82b700d1e6`

```dockerfile
```

-	Layers:
	-	`sha256:b57eb13d5352a7c0af53c0fa5a04888fdd3f16d224b4d8de1ae1034c6da3d630`  
		Last Modified: Wed, 10 Jul 2024 19:10:35 GMT  
		Size: 646.6 KB (646567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3dbecddc745bc193eb4ca923a51e6137c2d723b53329eee751d1dfd17aa7c8`  
		Last Modified: Wed, 10 Jul 2024 19:10:34 GMT  
		Size: 25.5 KB (25470 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull python@sha256:34d509784411f01550b8b48a373ed99ad2ac9027219188c0db89edebd676610f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (22030710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a082b9c523b59cd05a16e6937c1c73ea8e857d49acc63b4223b9b43f7db8b95c`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
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
	-	`sha256:5412981fd604e1f259b45fb42f0d9091e2e9ac987930c0f30feaa835002faaf9`  
		Last Modified: Wed, 03 Jul 2024 05:38:30 GMT  
		Size: 14.7 MB (14679333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776e7b2cfe3ce113ab1c23ad8c972ceb6032f26c9aedbcdca735b0194aa3c7e6`  
		Last Modified: Wed, 03 Jul 2024 05:38:30 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488056526c3b3dc02eae8a4563547105b0ed64e611816af861e4151675eaaa90`  
		Last Modified: Wed, 10 Jul 2024 19:08:09 GMT  
		Size: 2.8 MB (2796752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine3.20` - unknown; unknown

```console
$ docker pull python@sha256:37b09553a4a59701f015e073d2cd7bf1e031e9501ba500d96a45da5eb11afb17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.7 KB (669703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c2dd4b3e437b7094b1d69303f6e08c0aa544b267e0e2fabec8a3e73a50d97b`

```dockerfile
```

-	Layers:
	-	`sha256:b89faf3a651cf59b87ad86969c64dfbcd6c6296e2cd317c94ca6e7328b24b476`  
		Last Modified: Wed, 10 Jul 2024 19:08:09 GMT  
		Size: 644.0 KB (644025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc0c9d78c7d1f652595406ad917762375cbcfcc25e7355edfa79bfed859a52cc`  
		Last Modified: Wed, 10 Jul 2024 19:08:09 GMT  
		Size: 25.7 KB (25678 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine3.20` - linux; 386

```console
$ docker pull python@sha256:eeb6175120bb7a4bf9aeaa975ea325bbd03651ed2bdf3f8e4f4bd52fd10fd463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 MB (20957137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada3db05d1d11b59d708f6a0aadb49d5f785db01cb50595b36ea0617c73aebcc`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:24 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Thu, 20 Jun 2024 17:38:25 GMT
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
```

-	Layers:
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377344f1f696650b5d9731b7aad53dd89bad186810bbd69facf8e8412795d516`  
		Last Modified: Wed, 10 Jul 2024 19:17:44 GMT  
		Size: 462.2 KB (462208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54293c1567220358d7285e43ed8e0aa436122624eb7dedc78775a19bb7b480cc`  
		Last Modified: Wed, 10 Jul 2024 19:17:44 GMT  
		Size: 14.2 MB (14228419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb78931cde80df9e28a3f4b66ff37c89b3f82c9916b511b5b52c5cf436709149`  
		Last Modified: Wed, 10 Jul 2024 19:17:43 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f351630ac8e90d09a8272ef8f0e50033376cce9eae8916c412605fab4e4513ce`  
		Last Modified: Wed, 10 Jul 2024 19:17:44 GMT  
		Size: 2.8 MB (2796809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine3.20` - unknown; unknown

```console
$ docker pull python@sha256:b732bb999ae24db8a16a0ee91df1e6e67031175655b5cf81ff07cf798e7519e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.1 KB (670106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c415d668168eeb7eecabeedbe14fe9fba4dabd1047ece2684a7c7668146f2a1b`

```dockerfile
```

-	Layers:
	-	`sha256:52998fdec6398a7436e3b4ae08203c686ee9d8259d6271982c48fe1b0bf69686`  
		Last Modified: Wed, 10 Jul 2024 19:17:44 GMT  
		Size: 644.8 KB (644831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75750c7f0f43940e9c64c5261b6288388615da07978bd1e21230f0a89fd5797`  
		Last Modified: Wed, 10 Jul 2024 19:17:44 GMT  
		Size: 25.3 KB (25275 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine3.20` - linux; ppc64le

```console
$ docker pull python@sha256:cb0743a5dcaeac23ac73801c69166a7c3e84b36119e2be6998bf5640e7aa3df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21403418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e7dcf7ecb9693d719bb262deb77937eb0a9c40fc4d7416bbd263bd0518f0da`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
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
	-	`sha256:642cd7b97b957919b180cb487fee432a488cc1cb448865578a5f82fc4500faaa`  
		Last Modified: Wed, 03 Jul 2024 13:15:42 GMT  
		Size: 14.6 MB (14568681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05349c0d99c05bf7228024049a77fd7169f171a35ac8d3913d1bef05ae41bb7f`  
		Last Modified: Wed, 03 Jul 2024 13:15:42 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21011e74179ef784735553d38f8c878cbd52037eaf40bbc1b07f0c715c6e727`  
		Last Modified: Wed, 10 Jul 2024 22:14:42 GMT  
		Size: 2.8 MB (2796809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine3.20` - unknown; unknown

```console
$ docker pull python@sha256:3112b29bea06880070134257594dceb5928cc8044aac4ff34ab43584cd67adf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.4 KB (667423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1ee514a6826d7b38b6618aed391e475838015704670298793ebed8ad32b8af`

```dockerfile
```

-	Layers:
	-	`sha256:de1f8ee6710dc39423645459704650ea5eaba4d59e9469a596ac275bee9373ef`  
		Last Modified: Wed, 10 Jul 2024 22:14:41 GMT  
		Size: 642.0 KB (642025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0511408e6dd063c12f634db6becf8a69799633a34173a4d725bdb81db29ea4e9`  
		Last Modified: Wed, 10 Jul 2024 22:14:41 GMT  
		Size: 25.4 KB (25398 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine3.20` - linux; s390x

```console
$ docker pull python@sha256:f042cecf2c4a587d19703bde50479adf937507d9afce8205dafbe2bcbdec6427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 MB (21021253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f89d191cbe7dbfaa99aa427da066d45443e79caf2be14969a542265868c2db`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
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
	-	`sha256:6db2fe9b43f5b570bd5989235021b72b0051bc8064eca54140ecf137ab4b1ed1`  
		Last Modified: Wed, 03 Jul 2024 05:10:44 GMT  
		Size: 14.3 MB (14298253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53be7a8cddd5eff826c02db857bebf29ba81b03b4af7ebe2f4b8f02bb7760603`  
		Last Modified: Wed, 03 Jul 2024 05:10:43 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f0f3662d9080ffb1ff90e30de1c6f87d45679d43574efb986703e074c7f254`  
		Last Modified: Wed, 10 Jul 2024 19:10:50 GMT  
		Size: 2.8 MB (2796760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine3.20` - unknown; unknown

```console
$ docker pull python@sha256:1cdb15397a6fcdcf4e63e02ea40569774393cb4aa9c47d7c12022f223629e22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.3 KB (667296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3fb782bcbab4e6b46ea00d89a4e8c66a2a56a13225c4f5b1e7e860a4e12151b`

```dockerfile
```

-	Layers:
	-	`sha256:37122670d51c87ee0db994ae563bdf8579745964b14cd9b817b14e9e0f2dcf09`  
		Last Modified: Wed, 10 Jul 2024 19:10:50 GMT  
		Size: 642.0 KB (641967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62b3bfcee31734ab3b59174a226396ad953cd167591a160925e8575e2e6f2798`  
		Last Modified: Wed, 10 Jul 2024 19:10:50 GMT  
		Size: 25.3 KB (25329 bytes)  
		MIME: application/vnd.in-toto+json
