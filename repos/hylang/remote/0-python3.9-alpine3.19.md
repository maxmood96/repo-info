## `hylang:0-python3.9-alpine3.19`

```console
$ docker pull hylang@sha256:570ba1024a4fce7a8ab91e3cd493c0d735a5238427f075b9b95bb6dd026b30de
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

### `hylang:0-python3.9-alpine3.19` - linux; amd64

```console
$ docker pull hylang@sha256:588f14f425e3c9356679e903affcdbe3e5022b9fae7cee601710ddf1ad634c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24196075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03b25dd06ba016efd8c44685e42744ab2a7967126427e7c5da3100c6215045a`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:04 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 20 Jun 2024 20:17:04 GMT
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
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f37675a14c476c8654327cac40148fbcf374cfe99d025e32568c3319b18289d`  
		Last Modified: Wed, 10 Jul 2024 19:13:18 GMT  
		Size: 627.9 KB (627907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c5a2db3448578554777cbef439cd3238f3ad7fa16a02951799c62716b48e43`  
		Last Modified: Wed, 10 Jul 2024 19:13:18 GMT  
		Size: 13.8 MB (13804824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52ce6faae58ddee363333ecd33087d29b722a88f534ceb91b160e49a9a30d21`  
		Last Modified: Wed, 10 Jul 2024 19:13:18 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a26c8abad2881275bd8ae24734d82e215ce7bed443cab173df15c9ab87c2919`  
		Last Modified: Wed, 10 Jul 2024 19:13:18 GMT  
		Size: 2.7 MB (2694915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba855c795ea80224088d68bf2c578254fdbe495e88df25a93f00036bc53669b`  
		Last Modified: Thu, 11 Jul 2024 16:58:07 GMT  
		Size: 3.7 MB (3650869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.9-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:6ceb6537382eba18d9404f6956b21efc5b3922a92f027cc08ba226c94fb590ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1038064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd162bf64b581011b26a36c2d8b67a771f7adcbadd7c12c9688c94196ed30a97`

```dockerfile
```

-	Layers:
	-	`sha256:a4fdbf9f71087a1e7225d3ffa06ccdcb37668c949347c5baa0d2a32cb1668191`  
		Last Modified: Thu, 11 Jul 2024 16:58:07 GMT  
		Size: 1.0 MB (1028264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:022a34c08c343f4b113bda1982ed03000467b146621c44e4f5dd096a6a0f7f34`  
		Last Modified: Thu, 11 Jul 2024 16:58:07 GMT  
		Size: 9.8 KB (9800 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.9-alpine3.19` - linux; arm variant v6

```console
$ docker pull hylang@sha256:92b540eeca32a304e58106ff3d381e533e3325f0fdcb7f43075a0fe45cc12583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23274660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4dcc845ca6f6e9d4e4a1f9e45d59c8f5fb807ba234fe1d449e3db34ebbb76a`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
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
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2154630478e0a6a1f4cf7bce6cd6fb1ee147d334f82bde6e6fd701389f098f`  
		Last Modified: Wed, 10 Jul 2024 20:18:50 GMT  
		Size: 628.8 KB (628799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51935de34d2ed4957ece7130a5dca74cee3ecd0383dadd172a13dc1ae908d488`  
		Last Modified: Wed, 10 Jul 2024 21:18:16 GMT  
		Size: 13.1 MB (13125998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e9a88e4988cb80413c5d9e9294907b1487897070406d3c370734a285c3b7d7`  
		Last Modified: Wed, 10 Jul 2024 21:18:15 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382e80f0fb85f60a1fcc13aedc83b735428f6d72306bcbc016a45a96c8a1ed46`  
		Last Modified: Wed, 10 Jul 2024 21:18:16 GMT  
		Size: 2.7 MB (2694902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032236fec051cb8a3f4f7debf891e5188b66ea96d4aa3af873dc41323e5e3ac3`  
		Last Modified: Thu, 11 Jul 2024 17:01:42 GMT  
		Size: 3.7 MB (3650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.9-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:39fe64ed4e891e2cf910b04cab86d3f2821c6713ed8dee9e20cca2e23ea458b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 KB (9689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea27f9edec3074e0ae444bb0330e8e609b2c5d843a0bbffd7082b155a9959b2`

```dockerfile
```

-	Layers:
	-	`sha256:bf38b0d3c47aef9637421e3816e952581556c0201b09d638ebf129c8e10204ff`  
		Last Modified: Thu, 11 Jul 2024 17:01:41 GMT  
		Size: 9.7 KB (9689 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.9-alpine3.19` - linux; arm variant v7

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

### `hylang:0-python3.9-alpine3.19` - unknown; unknown

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

### `hylang:0-python3.9-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:21e8e0bc462f087372484d425b0bd1918e0c74e0d87552443bdc5c6db97e1a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24107463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d26e15b9a7be5cf1352a15d5aed9add124d7d9fed99c1ce1f991f0e4144efc2`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
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
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b05c22b072e3de5c24584e2c71e9c33fae53127874260bd3188217fffddb9e`  
		Last Modified: Wed, 03 Jul 2024 05:55:23 GMT  
		Size: 630.4 KB (630360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0747b307f7cab526d4752387ad8df21da165f38158f38c50d193d633cfe92539`  
		Last Modified: Wed, 03 Jul 2024 06:54:46 GMT  
		Size: 13.8 MB (13773870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ec619035f88b02bcaaec1baaf8690c30d8f7d1a9c90bd599319ac23487bf8e`  
		Last Modified: Wed, 03 Jul 2024 06:54:45 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c418b33f2d40b007e1dee4f25e803c62775835ccca99e982bcc1d5d842e298d`  
		Last Modified: Wed, 10 Jul 2024 19:18:03 GMT  
		Size: 2.7 MB (2694912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060db080b41d96a537464518c8c73ca336caca633cd738ce70b49040f5f5dd5b`  
		Last Modified: Wed, 10 Jul 2024 20:07:45 GMT  
		Size: 3.7 MB (3650890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.9-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:5c37ae525fae89741a7f37a0aaf078a5ed6489f12768ea4af527d4afad54f2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1038613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2f314b9d756059f1fbd477a6875f8b768aeca860998f5d026e44c44c1c78b7`

```dockerfile
```

-	Layers:
	-	`sha256:eca471afef8cfc593c8436e84e324d8709b0b8c616e49673214c4358fa6d3408`  
		Last Modified: Thu, 11 Jul 2024 17:02:34 GMT  
		Size: 1.0 MB (1028368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3df712fc801d17ef610d1b358762610d08f804a2eb2700c8387b5128a2967148`  
		Last Modified: Thu, 11 Jul 2024 17:02:34 GMT  
		Size: 10.2 KB (10245 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.9-alpine3.19` - linux; 386

```console
$ docker pull hylang@sha256:df7054315d3dd3a8e0867d8051ed62d7d94379df7fc4928844a4b1ee199bf07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24091762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248f8f5cbbb2a755ec75da5fb7b52cd17b3d6b7ee9ac3df9117e072a8c212aa5`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:29 GMT
ADD file:fef5870f3bb90ed437c0331d7e65e52da6728b66d231aea95a605935fef056d7 in / 
# Thu, 20 Jun 2024 17:38:29 GMT
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
	-	`sha256:e9c6bf0d8f3154c26ee87ffe9feb02c91666069b8cbe0668cfae10922ad80c49`  
		Last Modified: Thu, 20 Jun 2024 17:39:06 GMT  
		Size: 3.3 MB (3250890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac184a8ffc8508464426cb158076fa703a68739ce6b57b3d8d70fe9bf767ca42`  
		Last Modified: Wed, 10 Jul 2024 19:12:44 GMT  
		Size: 628.4 KB (628421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f42ca492746490c551503bc9b2832df8550a8fae9c63ad7e951f649ed2234c`  
		Last Modified: Wed, 10 Jul 2024 19:12:44 GMT  
		Size: 13.9 MB (13866313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ed5be6436c4888d67876bf21d235c646b632aa85728e33d3ce85832fc46bc7`  
		Last Modified: Wed, 10 Jul 2024 19:12:43 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadde87f66b0d784904b2928ffe74ac94bc510ea0e234a1ecdf76af908bd5eaa`  
		Last Modified: Wed, 10 Jul 2024 19:12:44 GMT  
		Size: 2.7 MB (2694911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b0b72fb7c453f0973e136a0b30b73f12c74bc04963ed20e5c26ee3f2e38b92`  
		Last Modified: Thu, 11 Jul 2024 16:58:19 GMT  
		Size: 3.7 MB (3650998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.9-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:1a0c77b8c19ad5ca5ebb3a586324e7f08f43b5d6c29ce4cde089d07cc0af3e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1037967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bddc1983d1aace42c3438be1f639523aec1d899e154f80d06051abcef5679b1b`

```dockerfile
```

-	Layers:
	-	`sha256:9b2e8df606293b904617300493d27139fa2c7ce18a182b80a465f16bc2d73236`  
		Last Modified: Thu, 11 Jul 2024 16:58:19 GMT  
		Size: 1.0 MB (1028219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01d4b2ded65057a7aad85a0b257e7ca009862bac97ec46256b8f50c1fc513195`  
		Last Modified: Thu, 11 Jul 2024 16:58:19 GMT  
		Size: 9.7 KB (9748 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.9-alpine3.19` - linux; ppc64le

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

### `hylang:0-python3.9-alpine3.19` - unknown; unknown

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

### `hylang:0-python3.9-alpine3.19` - linux; s390x

```console
$ docker pull hylang@sha256:9af2a52c2e2d35be70d4628f9b3207f41498f870ebfc0dd582cbc4d926b9d128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24056294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7a0fbec4eb1ac9b221d7d8dd376943311f6a59a1a347016b3a45bbcbc84cb2`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:12 GMT
ADD file:4aa205db6913ec3fd53a65bd281586a5f6abde77d41f1ffab554706c04822982 in / 
# Thu, 20 Jun 2024 17:42:12 GMT
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
	-	`sha256:71c2dde42aad09035a9686e376c7507b6e8e2a8ada2c409775f1c1bfb8d928ea`  
		Last Modified: Thu, 20 Jun 2024 17:43:16 GMT  
		Size: 3.3 MB (3252491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fd969fb1447a056625a813142d0136ec2f1a214ec7982823c71fe162da1f81`  
		Last Modified: Wed, 03 Jul 2024 05:25:36 GMT  
		Size: 629.0 KB (628980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc251a6aa179c78bee6e6bde3d70fae156f3a944de1c2a7c2f144e0cebc98042`  
		Last Modified: Wed, 03 Jul 2024 06:28:07 GMT  
		Size: 13.8 MB (13828905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4022c782497fa7c112675f84474e97c2e9ede9fd2f71f9c0f28bbb3e54203b33`  
		Last Modified: Wed, 03 Jul 2024 06:28:06 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23b0ba75048cb4230fa3bb7bcf04ec0f26aedc352cfdfc3c0883dee89a207df`  
		Last Modified: Wed, 10 Jul 2024 19:25:01 GMT  
		Size: 2.7 MB (2694898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8f09904c9a84ab0b8dad3dd63a1032037385bef9a3a2adf0122a3fc3e54a39`  
		Last Modified: Wed, 10 Jul 2024 20:15:46 GMT  
		Size: 3.7 MB (3650791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.9-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:db8eef3e050fecde3d22ee1c3eb9997436754e05f32a9fa17ae26cc3bbcdbc5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1036122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33fd023b4635945250a7a98cd2578ad05279d55a246fb36d9abd263450c70d7f`

```dockerfile
```

-	Layers:
	-	`sha256:f1585abbb39d706dd286958f85b1072e367d92628128e12d2fb0119f86e49fda`  
		Last Modified: Thu, 11 Jul 2024 17:06:09 GMT  
		Size: 1.0 MB (1026310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0393fe47609460e048fbca938c3a8233f9c47ef9d656c4cd3ddb2d57302e7460`  
		Last Modified: Thu, 11 Jul 2024 17:06:08 GMT  
		Size: 9.8 KB (9812 bytes)  
		MIME: application/vnd.in-toto+json
