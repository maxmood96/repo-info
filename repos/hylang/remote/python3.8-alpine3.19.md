## `hylang:python3.8-alpine3.19`

```console
$ docker pull hylang@sha256:bbb01e86936fe2dcc70ca835f46f5354a0861c456822f2b2074b84ca73dab239
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

### `hylang:python3.8-alpine3.19` - linux; amd64

```console
$ docker pull hylang@sha256:955f03c6f58545887618efa2f7276409c3cdcf6f86d625f87a61bb7d7971948f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21861399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365febe41ca548a46903cc5ad5e6dc675e336e40aff87329e247c9863fdddea6`
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
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.8.19
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:e9cd1ac1ad1fe67e69a59e74b065662acbd701ee490886e4ff9633fc26197339`  
		Last Modified: Fri, 06 Sep 2024 23:25:27 GMT  
		Size: 627.9 KB (627901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebc28bdf09a46397cc6f590728079757cec3bf276e68c3ddee955d321c1c8ed`  
		Last Modified: Fri, 06 Sep 2024 23:25:27 GMT  
		Size: 11.4 MB (11362399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edac6bd123f530de6e5d74fae519a1725af8b237d31b972b29e8f5d2c0e4d66e`  
		Last Modified: Fri, 06 Sep 2024 23:25:27 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db46b9a5aaae53468786502d23edf914deb283826be15ebbb40bb048f8f00e8`  
		Last Modified: Fri, 06 Sep 2024 23:25:27 GMT  
		Size: 2.7 MB (2698328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ae5c4384f967bad179c9a19da444d0473f92c101f712808ba05976a3c9aa00`  
		Last Modified: Sat, 07 Sep 2024 00:11:36 GMT  
		Size: 3.8 MB (3752837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:810475bcc800d9e5706c4aeee8b3f22cff808c85d8523ba7d3d49a0a46af9d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1047151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fafc1e11245b541cfe2fa2c8c26872cec331ae548e5e35f28e7146a643ad5681`

```dockerfile
```

-	Layers:
	-	`sha256:447249f92586a9caf9e1d50f5f81942ca63594d4054988391ea882403d7e4e5b`  
		Last Modified: Sat, 07 Sep 2024 00:11:36 GMT  
		Size: 1.0 MB (1038651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d397ff1d5999987d3fc810288574b428e0a6aaf61d4d4312b0dfc8cdbbbbef0`  
		Last Modified: Sat, 07 Sep 2024 00:11:36 GMT  
		Size: 8.5 KB (8500 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.19` - linux; arm variant v6

```console
$ docker pull hylang@sha256:f28a1cf19114b144a51a90c5255261273f5216ffc0f9aed4b6b74e953a8b28fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21287808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b548714dd559c5df360f7848172001c9ec06944c2a45fcadcc5452e8ae20c621`
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
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.8.19
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:5681f1cc399dd14805971700f4f77eb6f39177291c612dcb3f5a79facb376b54`  
		Last Modified: Sat, 07 Sep 2024 11:59:31 GMT  
		Size: 11.0 MB (11030970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bd4b2f3c4c8cc915a1ab1d6541a2af7fdff4985c692ab9f3f0507bb5e11b64`  
		Last Modified: Sat, 07 Sep 2024 11:59:30 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c5d1f93f5028f81b0e1b7aaafc5c4deb62e85e4c99e777ec34d6770455459f`  
		Last Modified: Sat, 07 Sep 2024 11:59:31 GMT  
		Size: 2.7 MB (2698328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e189ceccd240c0bffdcb79ee78698f4e4052a92aade6b8d22f27d5f33b8d98b`  
		Last Modified: Sat, 07 Sep 2024 13:50:39 GMT  
		Size: 3.8 MB (3753069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:49fed7cb4e668332e0bb631d3031ad58cdc85990b715ddf1ffe111d1bf69c8e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 KB (8369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a812710cedcaf8f9f879f9d77a10437875e449aeae2bfe59fe273d02da44671`

```dockerfile
```

-	Layers:
	-	`sha256:beb96d0383e0fb4ec61a0e07a59bf50bdbdb4aa77421a508d562f6fa1a0b833d`  
		Last Modified: Sat, 07 Sep 2024 13:50:39 GMT  
		Size: 8.4 KB (8369 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.19` - linux; arm variant v7

```console
$ docker pull hylang@sha256:8e410fa0ce5c011b3981425b837d89e8e0b1f2725f8960723350e6076f58d083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20652252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aec3b18e832884b5a1a419996151d191a300f8b74e7c66db00af35cc615263b`
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
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.8.19
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:0a632fa72482e5be9a7bf695c41a699bebf162145d1ff2de75ee20a1903fe350`  
		Last Modified: Sat, 07 Sep 2024 12:19:26 GMT  
		Size: 10.6 MB (10645194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81c71c855dc7e95fa4321223e99d9810b9eb2cc8be87d3e548d6eb8a0c707d2`  
		Last Modified: Sat, 07 Sep 2024 12:19:25 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca8afd523aa818f3a6009935ec44e040db4d611d29b7146bd16fc4d17d89c9c`  
		Last Modified: Sat, 07 Sep 2024 12:19:26 GMT  
		Size: 2.7 MB (2698349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc39a485ef135a5eb3ef05a9380096c4e6dbb9f685b59484f06f5b454b90971`  
		Last Modified: Sat, 07 Sep 2024 14:26:29 GMT  
		Size: 3.8 MB (3752843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:6a0272a4ada6ffd80481c63c85e07d23d858dec5e51dd2cf28efdd935fbf5f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1050138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1633c54673f9121891652fc86be919a759ad6dd4819548ce57b6032641fdc663`

```dockerfile
```

-	Layers:
	-	`sha256:f55c4897ba781a724e26ebcdd5465f25537e5954b3e243cab4926f639e1a5db8`  
		Last Modified: Sat, 07 Sep 2024 14:26:28 GMT  
		Size: 1.0 MB (1041551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:350653fca0fd8ec261070e8fbe519dd86d0b32b82c84ed43cee70a8767e62748`  
		Last Modified: Sat, 07 Sep 2024 14:26:28 GMT  
		Size: 8.6 KB (8587 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:8bd16fd0ed4699b268a0fccd190ecdfe13419bcbd1816c426a44fc8d4bd8efc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21889532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c4d5a7caa85c0aff47a4d09b8f2f71b3d26ae90847d7d71dee67a5b815550d`
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
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.8.19
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:f7588c45bcdd3114fd89cabb23b7b0f0f3e6c88a33846bb1ce85cf8543663e73`  
		Last Modified: Sat, 07 Sep 2024 11:17:20 GMT  
		Size: 11.4 MB (11448612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa66a90cac79f6b54901f112babc1b509787dc1ede97d0a43d43beb90f003a7`  
		Last Modified: Sat, 07 Sep 2024 11:17:19 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7509752e651eec07d8e1da36cbba6836eeb7f2bff81211c70bfd371ec755dbb0`  
		Last Modified: Sat, 07 Sep 2024 11:17:20 GMT  
		Size: 2.7 MB (2698310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25023ba95acb186c8f738fc77b346377bb2fe38b786f9dc8fb55a6793f1bfcc6`  
		Last Modified: Sat, 07 Sep 2024 13:58:55 GMT  
		Size: 3.8 MB (3752943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:4255cf156494532b2bda98a1cacbe9d931586cd8524b660f091883fc817aa080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1047604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9e4736896d5765ee7dcf5f81a420e6ae090a120090ab6ade5a53984d9d95e7`

```dockerfile
```

-	Layers:
	-	`sha256:fff066b1adae12877ba922045ebd921732f7b51e3ab2da59ec05ec090ed9a750`  
		Last Modified: Sat, 07 Sep 2024 13:58:55 GMT  
		Size: 1.0 MB (1038707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2457c20eafc92ae9f1545ce6dede558d15dbcb2a3d237990f7e8419cd35d0d12`  
		Last Modified: Sat, 07 Sep 2024 13:58:55 GMT  
		Size: 8.9 KB (8897 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.19` - linux; 386

```console
$ docker pull hylang@sha256:9d300e7180fa5db45ce9c6e9bb6098355ef207596eeb034ea96bbaa9118a7f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21920027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cf8d4c839e5dbdd2a1e885ab0e55e569d535c7a54c44f9574446ad666c3adb`
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
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.8.19
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:c6d3d56ac31ccdd932f71ad9b0ca3fc9b80d339085b79efd7a34c05673d7a04c`  
		Last Modified: Fri, 06 Sep 2024 23:25:40 GMT  
		Size: 628.4 KB (628408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a1933e1962885484888fb4e2fb00766c577817db2866ea6119910ac6a7bc13`  
		Last Modified: Fri, 06 Sep 2024 23:25:41 GMT  
		Size: 11.6 MB (11586693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1383f985fc78114eedea5d950e4ea0e4b63c4439bbdaebdc20f52e2bda5834c`  
		Last Modified: Fri, 06 Sep 2024 23:25:40 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd56747d014c6eabe68315aff111782b108206b9b505d8fac1d8e12cdbed913`  
		Last Modified: Fri, 06 Sep 2024 23:25:40 GMT  
		Size: 2.7 MB (2698330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfc91e043e992f5e74eb29c40dd964b623a9971dcee70ee38ab104d3797e0ac`  
		Last Modified: Sat, 07 Sep 2024 00:11:37 GMT  
		Size: 3.8 MB (3752762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:59df9ff58102bffa1c1351191a1961f38f29c7f3265de974397c652dac43a4c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1047092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42733470e8dbde7c7938f2a3a4ce1e9cc09cb35723c6bd25a84bd891479a435b`

```dockerfile
```

-	Layers:
	-	`sha256:6cd9edb0dad633f2c2bc4094fd0b5b77f7e6e7f4dc8a6a58614b19fc88663fc4`  
		Last Modified: Sat, 07 Sep 2024 00:11:37 GMT  
		Size: 1.0 MB (1038626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37715da07e7da351651879475ecbf2ae4c7c8498123b05f69b49bbc3cd2e54cf`  
		Last Modified: Sat, 07 Sep 2024 00:11:37 GMT  
		Size: 8.5 KB (8466 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.19` - linux; ppc64le

```console
$ docker pull hylang@sha256:18802865e492929c413c112f19b9efb6dae54aadbbb3f6ea7ce1988916e72ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22283084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d12e2a3c67ae587bebdeaaa38c397813e884db38f453d8bac28e056049a097`
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
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.8.19
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:2aa560c7a3a3d83414b1599e321a687fadfbbc979834f7959890a50f7711f531`  
		Last Modified: Sat, 07 Sep 2024 11:09:42 GMT  
		Size: 11.8 MB (11835970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdfed2669695d46b58c28aee55e283954c57b290e022cd243e4c30101fb3e66`  
		Last Modified: Sat, 07 Sep 2024 11:09:41 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be1095c2bc7a1c6460e3e28848180e70f63073d819e836eb390d0e81f515bde`  
		Last Modified: Sat, 07 Sep 2024 11:09:42 GMT  
		Size: 2.7 MB (2698313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dc24026a4e04eb089d6db6545d532452aeb20880027dea9af8fc9a8d48ef07`  
		Last Modified: Sat, 07 Sep 2024 14:02:32 GMT  
		Size: 3.8 MB (3753267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:eb962ea30121ac80188a0ce4df1e8938b95c857d5c33f0fe2f557ea328ae545e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1045287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d28c1499ea7f6000ed9e645900c625c93675b8f11b6e3292e296fdaae92dec`

```dockerfile
```

-	Layers:
	-	`sha256:f4b110e4a65970ba1c3b1b38705c7e60ab7c3d34d96df51eaa73e2563c4e5bb7`  
		Last Modified: Sat, 07 Sep 2024 14:02:32 GMT  
		Size: 1.0 MB (1036731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b424b23640577e50a53cdafe110e0b1a71b18e6dbd82e48698b1cc23340a0624`  
		Last Modified: Sat, 07 Sep 2024 14:02:31 GMT  
		Size: 8.6 KB (8556 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.19` - linux; s390x

```console
$ docker pull hylang@sha256:30a0772d4534ffa34116ea9da3d48b9c64725c21db568e205a1caa3523027b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (21974546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74a20ff1244887bb062b407ac649cbcfa14b2e1fc9ea52180a5b4a7f462ce3d`
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
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.8.19
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:5db953551721676e9edfe0f4a99c60466c694137bba6bbd8989a2dd03540c3a9`  
		Last Modified: Sat, 07 Sep 2024 10:12:05 GMT  
		Size: 11.6 MB (11640906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f72e2665a40be232da43808f0c3a95355c8cfcdf3b5357a213970bb6aed119`  
		Last Modified: Sat, 07 Sep 2024 10:12:05 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346a4131c3ad3537c77c10d9eb465e69aec329654fed3aa3e0a700753f13a235`  
		Last Modified: Sat, 07 Sep 2024 10:12:05 GMT  
		Size: 2.7 MB (2698322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fad72257083449e81d35b2ba42024d77fbd1e9b6eb4524c951ee9b06e16fc8`  
		Last Modified: Sat, 07 Sep 2024 11:55:03 GMT  
		Size: 3.8 MB (3752733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:e781ab5e00e1868f577bbc622e8080abbd924d5d98fcbaa041e14136c6a2bf16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1045209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9411136a11ae73c6a1b5ec02367e0967b48991b18fe29e6f6e6edd09eb71cc4f`

```dockerfile
```

-	Layers:
	-	`sha256:445e99d4fa178e064baca0088f9e14a0dbb0afd23c83ccc8c7a93c09f198b019`  
		Last Modified: Sat, 07 Sep 2024 11:55:03 GMT  
		Size: 1.0 MB (1036697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c4f15a1b59bb393fc9b26b0b4dead85e1f6bd1189e207b7533dd49c70fe45a8`  
		Last Modified: Sat, 07 Sep 2024 11:55:03 GMT  
		Size: 8.5 KB (8512 bytes)  
		MIME: application/vnd.in-toto+json
