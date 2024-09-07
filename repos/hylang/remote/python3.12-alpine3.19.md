## `hylang:python3.12-alpine3.19`

```console
$ docker pull hylang@sha256:f70ffad4e7d1f73c7b18bb9133d743080a6eb2d4c81f97f279dbaeca268b562e
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
$ docker pull hylang@sha256:b399e8aa086abc844654fe4969a47cc3ae1c4f7b995bc37f29898e3681822783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22824737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fc01a6942562a67e7bae408ef2d60a00aaa06ad2ee048d4f0deef1edfab89d`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.12.5
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=24.2
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fe8821d8e937f4d18d66ed6c01512319f6369e39501aa040d545cddb26c012`  
		Last Modified: Fri, 06 Sep 2024 23:31:42 GMT  
		Size: 627.9 KB (627915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e73abbe668f9cf00602e624892cee4209b2bea1a95102c68b2057c7e0b3c57`  
		Last Modified: Fri, 06 Sep 2024 23:31:43 GMT  
		Size: 11.5 MB (11499904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd37ef32dbcc8362c68d13269033880dde7e11c41e37de2144c7489fe84d588`  
		Last Modified: Fri, 06 Sep 2024 23:31:42 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e183bebb85d6d6db6d0223f702bb07cfdb79b7f435fb9c1d0e43fb9022370a9`  
		Last Modified: Fri, 06 Sep 2024 23:31:43 GMT  
		Size: 1.7 MB (1673601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d947a596db30de6a062e515fcd3e04ba4d2d6550989e0727d181609a471ec40`  
		Last Modified: Sat, 07 Sep 2024 00:10:51 GMT  
		Size: 5.6 MB (5603382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:b2fd82f7567c67338be071652b228c45e7bea201eaf0b3eec06653d39c562c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1042906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4619692ab4436d0c423a9b0ef0f1fd5594da49513abce41f36101e46ebbdedf8`

```dockerfile
```

-	Layers:
	-	`sha256:eb5fb58e5a5428858667aa7d9febbe1e0aad56d9614ae8b4badc0b9784aceedf`  
		Last Modified: Sat, 07 Sep 2024 00:10:50 GMT  
		Size: 1.0 MB (1033180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6782c62c108f74ff291d05c55d320459d4219efb0ae4bf6365da73ef928790f`  
		Last Modified: Sat, 07 Sep 2024 00:10:50 GMT  
		Size: 9.7 KB (9726 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.19` - linux; arm variant v6

```console
$ docker pull hylang@sha256:d794599f9e7fd745374c47a49562e76994767289954b4eb92e7865315907c3aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.2 MB (22159892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d976215c8361cfea5f3c049c1cd0787a2926d7fe2bace0336ba8f9045b9b1cf`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.12.5
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=24.2
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a39bdf9d326d55be66a6472913d0bdbe3b64af11a3fa17f368b4581b594e62`  
		Last Modified: Sat, 07 Sep 2024 10:50:50 GMT  
		Size: 628.8 KB (628820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145bfd8b63ae851ec721f6cb0f78de10ddb2efa84a3c9dff6b80f92e65d78d10`  
		Last Modified: Sat, 07 Sep 2024 10:50:50 GMT  
		Size: 11.1 MB (11077321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57665f15901fb5632cfe104fb47d90add7073fdbc06b590801bf691f3a5cf0c2`  
		Last Modified: Sat, 07 Sep 2024 10:50:49 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c353c0fce85966384a1d68011fc643cf531557c7226622680bb791c6d4dddc5`  
		Last Modified: Sat, 07 Sep 2024 10:50:50 GMT  
		Size: 1.7 MB (1673577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e1191dc161fa996e91cf23b956db5a46947fcd6b502cfea51c887d07bbcf64`  
		Last Modified: Sat, 07 Sep 2024 13:39:18 GMT  
		Size: 5.6 MB (5603553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:54b5715faf743ad0b7563044f5a8247aaee71c3071ef41eb417ae50739408664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93079eebde60e243dd7a66be29009bd2fcdb6b9fd243cc7d64a38887d8f203c2`

```dockerfile
```

-	Layers:
	-	`sha256:99af62b64b6caf94072dccc479fdeed970ed433ef6cbbdd4f1f9da6ef9c6bb91`  
		Last Modified: Sat, 07 Sep 2024 13:39:17 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.19` - linux; arm variant v7

```console
$ docker pull hylang@sha256:3565066601694349cab691fa7511d4b8778056745205549d69b169d82eb28997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 MB (21488111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afd0a54d816fa51128a986716804924cb54452c7fd18270a39862157f218d3c`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.12.5
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=24.2
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2773a0915bfcbc78e079faa18251ac0d879f0f82697ee83220c411ab06dd1bb`  
		Last Modified: Sat, 07 Sep 2024 11:07:13 GMT  
		Size: 628.0 KB (627974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c851b91fbfc005b0a492ea0a7d23bd4bf980acc455dd9f80e26c81a4953045`  
		Last Modified: Sat, 07 Sep 2024 11:07:13 GMT  
		Size: 10.7 MB (10655570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d199e7d86a5f221207db423ae86ac3c10acff885da75a03e94ee2a3fea0b70b8`  
		Last Modified: Sat, 07 Sep 2024 11:07:12 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d2ae683e3bb34d89ce4c615fc82a17c7b5e6bd23129a6c3db33538f7e4932e`  
		Last Modified: Sat, 07 Sep 2024 11:07:13 GMT  
		Size: 1.7 MB (1673608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9948ca10fb78736881826f6dbab1a0c3ae1f4e834d788807ea54ed93751e9f6f`  
		Last Modified: Sat, 07 Sep 2024 14:21:48 GMT  
		Size: 5.6 MB (5603066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:7bb10d9249f27a46fabcdfd97fc78e2208c49890ff2feab449b2f207af4aaf0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1045958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06479177ea3239718882a28b0e1048d1448fe62bde24f219c40aa64e479714fe`

```dockerfile
```

-	Layers:
	-	`sha256:1bcdd146c7d611918c821167945ccba14d2f7974f69c39fe1e9829ecf3d9bd9f`  
		Last Modified: Sat, 07 Sep 2024 14:21:48 GMT  
		Size: 1.0 MB (1036112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0e7e3d0d520deb53c8ee622204b62093554bbb8d102ccf33e8bd2f22df360fa`  
		Last Modified: Sat, 07 Sep 2024 14:21:47 GMT  
		Size: 9.8 KB (9846 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:153dea94856323bfc377a3ae480ab0b3ec3eb4244b5e13f8aebcbf975668853f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22831087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34fb5af5334c90d9ac84962d757f3efc3ca2212d704affee75f4ac3c0f53ea01`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.12.5
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=24.2
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf2f2790992c8c78211ff5181c3fb0eb2710f0d4ab4c29278770b838db532c2`  
		Last Modified: Sat, 07 Sep 2024 10:20:39 GMT  
		Size: 630.3 KB (630335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad091d9089c0ac44dc812383b48f68f30b44a82724a2a9f49133ac83e7ec460`  
		Last Modified: Sat, 07 Sep 2024 10:20:39 GMT  
		Size: 11.6 MB (11564577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298b95195cdb65e24539d3b94f010c699bdbc25bbc0fc08f8878fe5dcd52c8c0`  
		Last Modified: Sat, 07 Sep 2024 10:20:38 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63241a4ca26a8c3eb5148f85985b2f3cc4dde120752230a23d1d7bee978ef891`  
		Last Modified: Sat, 07 Sep 2024 10:20:39 GMT  
		Size: 1.7 MB (1673584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10decf1c5f902c2992381bfb01a8abf485f335a63cead1fecead68720979a84e`  
		Last Modified: Sat, 07 Sep 2024 13:54:42 GMT  
		Size: 5.6 MB (5603259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:a97601095133bbf81fadf9ed4df96f8c10da81283fff8df3efd5ea3b65771945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1043454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc9e64fb7ede89ec0cbf78396b023a26575fd5a8ffbde2db18806a54a768d65`

```dockerfile
```

-	Layers:
	-	`sha256:26996e095868e040cba97df4d24e0a9a7eff6d1ef1a417c4fb7e7acfdfb84b87`  
		Last Modified: Sat, 07 Sep 2024 13:54:41 GMT  
		Size: 1.0 MB (1033284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2925bc9a3b558848137a192c5701dc439ad86cef14adba41c13ada9d0583583`  
		Last Modified: Sat, 07 Sep 2024 13:54:41 GMT  
		Size: 10.2 KB (10170 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.19` - linux; 386

```console
$ docker pull hylang@sha256:e641a2bbb74800513b978469f96a4f5f262eeea019304abbe7b318c23feac66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22852168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46ac3a713cea51067d263ecf99b8726ca428c3c21979dc159882f04d89943e3`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.12.5
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=24.2
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b2801d1a66d8eb7d37ef8c9bd01ed316e098fb58aca389c7038cf904ab7229`  
		Last Modified: Fri, 06 Sep 2024 23:33:12 GMT  
		Size: 628.4 KB (628417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e8a05a75efec89d800448cf9a90e1fd959a798b05a8f51e395555b1d05c35f`  
		Last Modified: Fri, 06 Sep 2024 23:33:13 GMT  
		Size: 11.7 MB (11692995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5711feaa7d3d84fb482e82165b47257f80cf1c7983ba93ce546895b7d9e28f21`  
		Last Modified: Fri, 06 Sep 2024 23:33:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daa8fc3a87001de1178cb86c2f3a5fb7e0c2b59f148e985334303b078cc6b13`  
		Last Modified: Fri, 06 Sep 2024 23:33:13 GMT  
		Size: 1.7 MB (1673606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06beda1aab180f255d764390d760bfcdbc3966b302bd08e46bcd2047715b7701`  
		Last Modified: Sat, 07 Sep 2024 00:10:56 GMT  
		Size: 5.6 MB (5603315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:831764bf74591f5a68574f63ef8d71c351a47f82fd9fd7d0e4aa9fa4a11379d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1042809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c934319f500487e648dfab671147eaf639182ea094243b09e78066915558ee36`

```dockerfile
```

-	Layers:
	-	`sha256:a8e43033e1dc8af09f5eeaf9ae75dc388cb2d5df71eaf4dc623b86b15d356b35`  
		Last Modified: Sat, 07 Sep 2024 00:10:55 GMT  
		Size: 1.0 MB (1033135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:067dd462bc5d31e87f1e59ea49f04e038fb4332015cfd9fbb870dafca8c45f42`  
		Last Modified: Sat, 07 Sep 2024 00:10:55 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.19` - linux; ppc64le

```console
$ docker pull hylang@sha256:12f0e9342c0a1702348fc7d9789135ff03c7e7ad5d6071521bab19a7521c1163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23279233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe834a533c1b8db05628b7b24d9d92c7723f71da1266a0c9d2042cf524da2ad3`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.12.5
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=24.2
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5749dced5c3ea885609ac4ce0f87b1f345b6e9df997e9a8b0aaceac5eaaa6e3f`  
		Last Modified: Sat, 07 Sep 2024 09:58:37 GMT  
		Size: 630.8 KB (630837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426cd415c55992db06a26a1ed7bd25ae340566940cb6b178398e5471c3e1b95d`  
		Last Modified: Sat, 07 Sep 2024 09:58:38 GMT  
		Size: 12.0 MB (12006638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b06f62338efedc26e0b5ff8c2d9585691e0620c327d156b7da1677b41f53b58`  
		Last Modified: Sat, 07 Sep 2024 09:58:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bbf543dbb062c5901a7043cf5ddfd477c30350d9ab299e7de9d446206bd4ce`  
		Last Modified: Sat, 07 Sep 2024 09:58:37 GMT  
		Size: 1.7 MB (1673636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b63a7fc7765940e1feec184011bae24fb08d6af76d04932175ff43cae07b99d`  
		Last Modified: Sat, 07 Sep 2024 13:55:48 GMT  
		Size: 5.6 MB (5603425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:bda532135117a8957ed7ed64af5d59fe3ac5724f5804b1a28a2ba1af793f4286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1041090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4df80d5300fa3fdd5791fa1856d2fda0486569c792edbc45856d203049affe`

```dockerfile
```

-	Layers:
	-	`sha256:b4b288d414546a15fd74a60be074733c2a3bff9fde2750509ca277ed4618073a`  
		Last Modified: Sat, 07 Sep 2024 13:55:48 GMT  
		Size: 1.0 MB (1031284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f777d74240f3500c1f4249f9dfe765bf8f2a63a2eb2de3855fe9b1aa20ff61de`  
		Last Modified: Sat, 07 Sep 2024 13:55:47 GMT  
		Size: 9.8 KB (9806 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.19` - linux; s390x

```console
$ docker pull hylang@sha256:b9535f7dd121d950415628c8fb6732f89a4c55a1e3b18187d82c2dcae0ad207b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23008309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ea5fc929e04b184c651d5d285fd30d14fa05032a5dbfc83ee256b504f1878f`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.12.5
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=24.2
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf180b200a9685ef5f8a9f8ba267cdaf8e59fe28f3b974eee5118a914d262ab`  
		Last Modified: Sat, 07 Sep 2024 09:10:44 GMT  
		Size: 629.0 KB (628993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfff035c94cd65ed1f69179dc629b447cdc4f1eaa2a283222d5efca71604d42`  
		Last Modified: Sat, 07 Sep 2024 09:10:45 GMT  
		Size: 11.8 MB (11849166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52398e64804d7565253504cbb36cac16882bac5cf162472e2fadcbafcc4e78f`  
		Last Modified: Sat, 07 Sep 2024 09:10:44 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72f6e7b1d0d69b1e8873414b89f35cb8fb6a4b98d781b02a0500a57877ddf1f`  
		Last Modified: Sat, 07 Sep 2024 09:10:44 GMT  
		Size: 1.7 MB (1673596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b5be22cbdb29bc963c109a4f2efc324062137d0fa4e6f6d90a63d128031785`  
		Last Modified: Sat, 07 Sep 2024 11:49:52 GMT  
		Size: 5.6 MB (5602968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:09fe1b51ff6e9b5be39f297ea84eabd82705ad9669c26022f7d98c1f86bb479f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1040964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e43d99107878c36a0eb3946badd1f51ef02f7f72edea895be1cc5df63d9ef2`

```dockerfile
```

-	Layers:
	-	`sha256:e491e1d260a00e9f13357000a8f658bb4425fb2fe1c1c64fb401b3ec11cbb428`  
		Last Modified: Sat, 07 Sep 2024 11:49:52 GMT  
		Size: 1.0 MB (1031226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7661163c151e07f07d1b26511017a09f83d25b19e96564bff543f760c067eca0`  
		Last Modified: Sat, 07 Sep 2024 11:49:52 GMT  
		Size: 9.7 KB (9738 bytes)  
		MIME: application/vnd.in-toto+json
