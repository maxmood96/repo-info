## `python:alpine3.19`

```console
$ docker pull python@sha256:17a0bb21c0b146f0de3b9b3c1e31b0b2394b16bc7c47ebdaf34aa15466b05eec
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

### `python:alpine3.19` - linux; amd64

```console
$ docker pull python@sha256:102cdc81570e87ed12daa25a8242923f1cf46116783455f0eef4d4ebef21e26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20826654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4bac40fae0ed2f89d229eb9b4e69ec561d159e2ceb7398146bb8515eac930d`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:04 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 20 Jun 2024 20:17:04 GMT
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
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2a14695d73b34735496f9cfd2e8edf6a3bcc407334d6babb695317c8863ab8`  
		Last Modified: Wed, 10 Jul 2024 19:15:44 GMT  
		Size: 627.9 KB (627921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbf42e206ed506ddbf65757d6f8862810dcb8539b5cf71d531e89bae96e8a7f`  
		Last Modified: Wed, 10 Jul 2024 19:15:45 GMT  
		Size: 14.0 MB (13984383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee6f8cace97e5b6a89f70ade88015b0beeff69fa1de870fdb833122f545f49b`  
		Last Modified: Wed, 10 Jul 2024 19:15:44 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ead4d50ec0da3b3ffd27703eced84396e48736798c8814a8a046e70d7932fb2`  
		Last Modified: Wed, 10 Jul 2024 19:15:45 GMT  
		Size: 2.8 MB (2796789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.19` - unknown; unknown

```console
$ docker pull python@sha256:ccf81b07f40b8a40d6b299b1be9aa87cc7bf6b9e22d9305d7e61edf48383fe00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1044617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea5cda9849c4c1ec3a383e29770d7f396184413937f66bc8a14133c4f7ea6ca8`

```dockerfile
```

-	Layers:
	-	`sha256:6570b8ae73e571ac23a119f860c863607b445c2a47a810df7baf09ae2c609795`  
		Last Modified: Wed, 10 Jul 2024 19:15:44 GMT  
		Size: 1.0 MB (1020507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87fce7c5d5815c38029929f19b128361f44cb6a155639d71d85159529e74cb45`  
		Last Modified: Wed, 10 Jul 2024 19:15:44 GMT  
		Size: 24.1 KB (24110 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.19` - linux; arm variant v6

```console
$ docker pull python@sha256:745e73ac63d5ed4cd60012019c69c3c805c2737e80a01c2ff01edce5dfaf672c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 MB (19835627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c99533ed512485f3f72f0f7b61c4e0d0c2c45ccdb9d6d04ba74cb988f51a94`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
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
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2154630478e0a6a1f4cf7bce6cd6fb1ee147d334f82bde6e6fd701389f098f`  
		Last Modified: Wed, 10 Jul 2024 20:18:50 GMT  
		Size: 628.8 KB (628799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392d5ffecd0d124f90d61629e1e210ed9e3199ac9b480e4cb1a99d311b875572`  
		Last Modified: Wed, 10 Jul 2024 20:18:51 GMT  
		Size: 13.2 MB (13235921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6315a06bf8230a51829f98213038d4b01e77acafd072a37081b9d2befbbf88e1`  
		Last Modified: Wed, 10 Jul 2024 20:18:50 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c5b2882c5fae0d07efe54460cc9721e3ce96839b3ce209c693861fc1c7cc34`  
		Last Modified: Wed, 10 Jul 2024 20:18:51 GMT  
		Size: 2.8 MB (2796769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.19` - unknown; unknown

```console
$ docker pull python@sha256:b006268b75f5b3fd896611913c8a41c68bb57d7e16a8d6af9fb06c18f804b236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 KB (23999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ae490783febbdede4554cb43f974621d34b1ffb384d9dfb931d49a1a3048e0`

```dockerfile
```

-	Layers:
	-	`sha256:24dabef08f92cfd00e108664fcc00600356abfc65708185322b0aaa74f857ed5`  
		Last Modified: Wed, 10 Jul 2024 20:18:50 GMT  
		Size: 24.0 KB (23999 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.19` - linux; arm variant v7

```console
$ docker pull python@sha256:204d0c9c767375850a5108d337b0a53a79538fa6a262727331c4d0fda07e6986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19044845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3104f6c94e64ebaee2a7e843e99e0444190057a8fb4ad020ca511f9f27153404`
-	Default Command: `["python3"]`

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

### `python:alpine3.19` - unknown; unknown

```console
$ docker pull python@sha256:2e53889094c2fd2b10e9393176bff3b6d51e65827feb8047e0647f7df4d65915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1047340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c960decff15dd5db08fc0daddd0f2651acff85476d246135f76ec29cc7676948`

```dockerfile
```

-	Layers:
	-	`sha256:718261f18a77f793615812886537c2da0ab21594e3127b87f7edcc45d6e33d5d`  
		Last Modified: Wed, 10 Jul 2024 19:11:04 GMT  
		Size: 1.0 MB (1023121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c3337afe0e24bcfd74141dc5ae103ab49c930ae9fbd719707d254833f69da2e`  
		Last Modified: Wed, 10 Jul 2024 19:11:03 GMT  
		Size: 24.2 KB (24219 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull python@sha256:b76be4bc8f0e2d04094aceec461ef90b70e63e62988ef9064f17b3c8caea1ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20720984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216d0525f1974fda921f67d2ac2c0cf0c99962f35198e64452d9bbd03cffed84`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
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
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b05c22b072e3de5c24584e2c71e9c33fae53127874260bd3188217fffddb9e`  
		Last Modified: Wed, 03 Jul 2024 05:55:23 GMT  
		Size: 630.4 KB (630360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af03ad8590b86ced5c10da8f19019c727cf585acf00392f93d1abced4c5df0cc`  
		Last Modified: Wed, 03 Jul 2024 05:55:24 GMT  
		Size: 13.9 MB (13936440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d9d9dad39fefdfb8d3aa0fb610e802c656ef6310ac8df5acec3f9e370cdfe9`  
		Last Modified: Wed, 03 Jul 2024 05:55:23 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581763910f9d3e1281b7cd15c684b2f23a00df08034d4ab0849040dd8a46cda7`  
		Last Modified: Wed, 10 Jul 2024 19:08:34 GMT  
		Size: 2.8 MB (2796750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.19` - unknown; unknown

```console
$ docker pull python@sha256:1bd6fa141e146ef931f90a82a11d352f2d5b759b0108ccb51860527ca1856792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1044973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4669879a24bd76f2c87506b23cf86a2b5fd3634119dbd4f53e03e49bd44b558b`

```dockerfile
```

-	Layers:
	-	`sha256:6186ed9573b5eb583323a1ae5a276b1def7fc2964b9f082703401901566ebc2e`  
		Last Modified: Wed, 10 Jul 2024 19:08:33 GMT  
		Size: 1.0 MB (1020563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea50d462f181b21874f741523b3aa6d5ea7e2ced9178ce1534d2edbc81189a9c`  
		Last Modified: Wed, 10 Jul 2024 19:08:34 GMT  
		Size: 24.4 KB (24410 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.19` - linux; 386

```console
$ docker pull python@sha256:34c66510d3e3763428b7a37a24e00ecd5ddc72d455357a504ff20a388218c472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20672401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d032d3bf2c59ada537788d73e5d0e1bc4504fa97e8dcfa63f93a72ab2caf45d`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:29 GMT
ADD file:fef5870f3bb90ed437c0331d7e65e52da6728b66d231aea95a605935fef056d7 in / 
# Thu, 20 Jun 2024 17:38:29 GMT
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
	-	`sha256:e9c6bf0d8f3154c26ee87ffe9feb02c91666069b8cbe0668cfae10922ad80c49`  
		Last Modified: Thu, 20 Jun 2024 17:39:06 GMT  
		Size: 3.3 MB (3250890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc3372d72e50ea2589722532c032841d9b8ab8b9eaa1fda8fa7a3775aa688d2`  
		Last Modified: Wed, 10 Jul 2024 19:17:14 GMT  
		Size: 628.4 KB (628431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1ab870e2b4aed9312f5c42e74d1cf161be8f28eebcd82ef594c36f3c542fdf`  
		Last Modified: Wed, 10 Jul 2024 19:17:15 GMT  
		Size: 14.0 MB (13996065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145ac04472732580a045eb5ef3e3ef64271a07d91d489c71574d363a01dbe860`  
		Last Modified: Wed, 10 Jul 2024 19:17:14 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949be9e4a7f47ef382d8c5a533b86f0f781d748d171df512017f1e3ecc02e48d`  
		Last Modified: Wed, 10 Jul 2024 19:17:14 GMT  
		Size: 2.8 MB (2796787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine3.19` - unknown; unknown

```console
$ docker pull python@sha256:865bf33df9964d203842b925fda44d423fab85a4911299a8428cea7f4d16efb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1044557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e64cb5075cb94f4727b3d6874c5a18ee564fe2655288fb9daf2868ca18a51a`

```dockerfile
```

-	Layers:
	-	`sha256:c492d9d5898c74e7eaa59b85174ec714de683f74504237c68564b79b22bc8a11`  
		Last Modified: Wed, 10 Jul 2024 19:17:14 GMT  
		Size: 1.0 MB (1020482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7bdc45653f78d1a9aaade7decd628e33af3fdd9c90fddd34014c3a47c01932`  
		Last Modified: Wed, 10 Jul 2024 19:17:14 GMT  
		Size: 24.1 KB (24075 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.19` - linux; ppc64le

```console
$ docker pull python@sha256:672915783a7a8c88675b1a2b3504e18d760b91946bc1da96df87b3539360b20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21138862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71bc172fe12788797f013fe48d6c284dc50627390d3d405ad290ab81d4d8a736`
-	Default Command: `["python3"]`

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

### `python:alpine3.19` - unknown; unknown

```console
$ docker pull python@sha256:e9b8c3f3815d9409feae95c359b653ce77aed02879d258be03eb936b42b0ae92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1042741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffe2cce28509f728e0ef854d7aff39436de36e4664e97f66db9ae0ee3046701`

```dockerfile
```

-	Layers:
	-	`sha256:7bdc153e8e7ff9e71781e91110a0918416700e271394784cb87f3ebc07065464`  
		Last Modified: Wed, 10 Jul 2024 22:15:19 GMT  
		Size: 1.0 MB (1018587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68ec119b46ee12f0f02c1c25dbb5998f6870832e843d973b8511edaccaa9af47`  
		Last Modified: Wed, 10 Jul 2024 22:15:19 GMT  
		Size: 24.2 KB (24154 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine3.19` - linux; s390x

```console
$ docker pull python@sha256:6153c6c8cc55121482430923f263af1ba5f16a94a65c6f7dfd722b07c59f63b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20757741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d043c79afb9e6746b9b3c96401e03efbfa222a6c2dbd7fbcd4c27b2e7de70c`
-	Default Command: `["python3"]`

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

### `python:alpine3.19` - unknown; unknown

```console
$ docker pull python@sha256:b98092742add5faf1ee79fc9605c7cf2effda179e920c85161a3942e76a28ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1042663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f09552fc4249c79821b5d50a920cda0aee83ba4d87b1dd78cb39f2395ad7e7`

```dockerfile
```

-	Layers:
	-	`sha256:3a7ad108789405bfc2a44f57bf97229c994300990e82fa1e6bed10b868595246`  
		Last Modified: Wed, 10 Jul 2024 19:11:26 GMT  
		Size: 1.0 MB (1018553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b61fc4c27bbd275c56ebaa3db58eb6f150b02d4767b415a26087e89ce4ee92e`  
		Last Modified: Wed, 10 Jul 2024 19:11:26 GMT  
		Size: 24.1 KB (24110 bytes)  
		MIME: application/vnd.in-toto+json
