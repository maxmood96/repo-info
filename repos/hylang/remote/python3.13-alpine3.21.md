## `hylang:python3.13-alpine3.21`

```console
$ docker pull hylang@sha256:9fdfb5a4b016789152b259e0b837bf2c42a0c162379464a6d8c7e7f2419ca805
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

### `hylang:python3.13-alpine3.21` - linux; amd64

```console
$ docker pull hylang@sha256:668e005404d398f624840ea93e0be0e3ae1b339e30d48c65b4c09946153872ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22327241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca6501c0ad069f7028d18bf339c255326b99b711d98ed7d0c2f4d9942ed67aa`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 Jan 2025 19:41:06 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYTHON_VERSION=3.13.2
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a507b793f9af8c58adcae308a17d0d4c2e8074a530b01b6abec958e9b7476cbb`  
		Last Modified: Fri, 14 Feb 2025 20:39:31 GMT  
		Size: 458.6 KB (458609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85be7329d6c2da132d82c42a32407595e174c5d8452d99a78201e96a553f1ed0`  
		Last Modified: Fri, 14 Feb 2025 20:39:32 GMT  
		Size: 12.5 MB (12534099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d8a12effa95e69eeae00f331cd5c50b0d9c8ed631b6e681fbe08a5902971ff`  
		Last Modified: Fri, 14 Feb 2025 20:39:31 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3337504136f288bc05a4700b37a994cc7fad51ee0c24cd5ab8b1c10587f63392`  
		Last Modified: Sat, 15 Feb 2025 20:13:01 GMT  
		Size: 5.7 MB (5692037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:aff83827f31dd24fd3f8603455f89bc0bc6eafcec4db8845d46439a568de45c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.3 KB (643270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863107d210c837d939c7a8958e586b6d1945ee11c0fc1eb24364ea4647e8fbad`

```dockerfile
```

-	Layers:
	-	`sha256:d824a7098cb1eccf70830d52df45cd1a70cc717b16f4f865c0fa7aca8a22ecea`  
		Last Modified: Sat, 15 Feb 2025 00:17:22 GMT  
		Size: 631.5 KB (631480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbffe0d076d34264b28bba70087b23b389ffd2c1478324b4fd83f887c8c5c314`  
		Last Modified: Sat, 15 Feb 2025 00:17:22 GMT  
		Size: 11.8 KB (11790 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.21` - linux; arm variant v6

```console
$ docker pull hylang@sha256:7b2447636eef184ab0750678fd20190f41ef7bd5449944fc9ed8c8b3e1f97d59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 MB (21670156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149ad0bd63a2a2a686a8388923c34d832a6767d6d0a81b9b7caa4cde33aa4db4`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 Jan 2025 19:41:06 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYTHON_VERSION=3.13.2
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4fe5d1b18dd307aed3d54fd3454d75bb46ed387a745a0d9d8a94a2e2b1f3ce`  
		Last Modified: Sat, 15 Feb 2025 10:06:38 GMT  
		Size: 459.4 KB (459437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f805e38f3bb6629a66c376bdf0dabd7e9fe8524d5424d4d97aebb9ea8ba8fefd`  
		Last Modified: Sat, 15 Feb 2025 10:06:38 GMT  
		Size: 12.2 MB (12153686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf76bd959f8d96cfc677bac2fd7b4155962f532bdfe24a816934c63ca5a1237`  
		Last Modified: Sat, 15 Feb 2025 10:06:38 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8833fd28390113000a21192cd19cf60380ddebd4317ed001a38d0d773559073e`  
		Last Modified: Sat, 15 Feb 2025 12:17:42 GMT  
		Size: 5.7 MB (5692053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:40c14193866704d5849a2a197c9d9659edae2d43a8e45fe2db99ac494571f31f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 KB (11747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e7391b07740398154b3fcc600549baccaf76774c5027d37eeb837c441e7766`

```dockerfile
```

-	Layers:
	-	`sha256:c9ce25a6c9138a11b9265ac1e89bdbd51d77d5a55a2bf6495126463dc19ee33f`  
		Last Modified: Sat, 15 Feb 2025 12:17:27 GMT  
		Size: 11.7 KB (11747 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.21` - linux; arm variant v7

```console
$ docker pull hylang@sha256:b6c99bda84031e617d8708e1e7c1abf9eebd82b17c7bd402f132802564d31134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21084036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59aad7af83f5b8d7e9473e9d4bcea7dfd3f90e59f4b43107ab46a35cc9bad052`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 Jan 2025 19:41:06 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYTHON_VERSION=3.13.2
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df285caa3e30b294f67bdffabbfdfc7493bf29d73a6d35fde7824f35e36c502`  
		Last Modified: Sat, 15 Feb 2025 10:15:20 GMT  
		Size: 458.6 KB (458625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dacfa9ad6f664f48289ca4e5060f821b6a830bfcd83f98dfd0346cf880fe669`  
		Last Modified: Sat, 15 Feb 2025 10:15:23 GMT  
		Size: 11.8 MB (11834905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb5c3b3fa23b55cc259aaf7076a23e78110c73158136a11e06d018d3f5f9ad4`  
		Last Modified: Sat, 15 Feb 2025 10:15:26 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0449d8f11b65042ebafca3775259683cdb5b25399839fa9b297cde9be90a4c`  
		Last Modified: Sat, 15 Feb 2025 17:49:46 GMT  
		Size: 5.7 MB (5692133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:f87dbc5c8dc6472e53c2bfe1a016356d08adf66ef71905d33f1957ecc22951ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.4 KB (646387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad96979211837571872cd5117e275ba0e69aeaf2c996887869d4189f56401b00`

```dockerfile
```

-	Layers:
	-	`sha256:e3f03ba4519641ad023eb4f8226f794b54740a27e649249f8c656d5711ac63c8`  
		Last Modified: Sat, 15 Feb 2025 18:17:23 GMT  
		Size: 634.4 KB (634425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00e1af545ac0f5ef6b327e26a0292c1ecbe2eec7f018ed898e49fb63c344da82`  
		Last Modified: Sat, 15 Feb 2025 18:17:23 GMT  
		Size: 12.0 KB (11962 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:0f0246b47dc407ca0c8d577c0ce0ba71c3cdcfc6f48cb8b21d355bcc996a1e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22701093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19def57992e48abba673226ab73e7479ea50a18449874148a36cdd334757a739`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 Jan 2025 19:41:06 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYTHON_VERSION=3.13.2
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88e0568d87b596e629b407d2f22c4e20b5dce80986bc791b904d483dbbd4cf4`  
		Last Modified: Sat, 15 Feb 2025 07:07:43 GMT  
		Size: 460.7 KB (460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ccf01a8316429709d1331ece64e7b35914d4a4a3b866d25e8f185e846eb2e7`  
		Last Modified: Sat, 15 Feb 2025 07:07:51 GMT  
		Size: 12.6 MB (12555109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f200fdec1553fc788c1f79427c6a028d72f528cd95094275a4d43bde42eba99`  
		Last Modified: Sat, 15 Feb 2025 07:07:40 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdd44f3b524b71030b2396d26cb9b67cef95814907b4d93786e6140337a4057`  
		Last Modified: Sat, 15 Feb 2025 20:13:21 GMT  
		Size: 5.7 MB (5691981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:e7412a80c1f12f416bd195e43552f2d9b50699ceb388b3f61b51ed32b4764525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.7 KB (643718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca284f6187e2990d98b2ce0de611408a386fefd8665cc3f2348162469de52c6a`

```dockerfile
```

-	Layers:
	-	`sha256:5a144793cde01485efb742ec959a0600320aa0e2a8b2f98a221eacee7922a083`  
		Last Modified: Sat, 15 Feb 2025 12:17:30 GMT  
		Size: 631.7 KB (631680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1a48b4ef6a6e1271a9a6a517bf37718b8363121913346131c7360aec0975ce0`  
		Last Modified: Sat, 15 Feb 2025 12:17:30 GMT  
		Size: 12.0 KB (12038 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.21` - linux; 386

```console
$ docker pull hylang@sha256:b8abdf82ea2b00f012b8f83da5e5d59e72feb667959a790836b8ed8c82d16086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.4 MB (22400937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a3550ef571bf79061a0c01062b31804f4f2f13a2fabb5ccb1a443eb6dd36d1`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 Jan 2025 19:41:06 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYTHON_VERSION=3.13.2
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64abd4c7c10f136ba8dea3df2024aa005d1abf43154c566df5a1c178c3b0ce`  
		Last Modified: Fri, 14 Feb 2025 21:13:33 GMT  
		Size: 459.1 KB (459070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70103b764a44b0b8dd5a1d71c44e3f510e9ef6f42222276d44dbfbf57f25b916`  
		Last Modified: Fri, 14 Feb 2025 21:13:34 GMT  
		Size: 12.8 MB (12785985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2c8820961677bd8c94c821630d2b84ff342afaa85f6631ced3d398b7272069`  
		Last Modified: Fri, 14 Feb 2025 21:13:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cc6f3b3828491621eb2c6301d624738be8237815e27eb992df053dd3bb3cdf`  
		Last Modified: Fri, 14 Feb 2025 21:14:01 GMT  
		Size: 5.7 MB (5692010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:cb71d501598305703198a2231b46ecf827ca1ebff66907349934c30419722303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.1 KB (643091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d16dcdf9d6122e17c7342f67bc788dca94a56b8e408b5c66b8111ddf83934d`

```dockerfile
```

-	Layers:
	-	`sha256:5021d181dedd72954bbe7419debc23276ead5e071dc95979f3c98021a0646d35`  
		Last Modified: Sat, 15 Feb 2025 00:17:28 GMT  
		Size: 631.4 KB (631395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b2ef81e22049b842e37cffe6e69e862b1c3c9a35168c8355814428e1685d89a`  
		Last Modified: Sat, 15 Feb 2025 00:17:28 GMT  
		Size: 11.7 KB (11696 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.21` - linux; ppc64le

```console
$ docker pull hylang@sha256:438123991cc9e4f5be58157c33ddd3be1317806431338ef5dd8a98121233a96e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (22989186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a349d542a7c7187d1320c0a9772c3e9431a8c50d4c514d51e6b01240aafcc15`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 Jan 2025 19:41:06 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYTHON_VERSION=3.13.2
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b017289e140b338bd7f3a7aa45c900780a4b77c5838095d57eedddf2ef89ad50`  
		Last Modified: Sat, 15 Feb 2025 01:13:13 GMT  
		Size: 461.2 KB (461178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6291a44a7781cba77e0d69478279c2e30ba51312cd8e34cb3e8a76a451d79d`  
		Last Modified: Sat, 15 Feb 2025 01:13:15 GMT  
		Size: 13.3 MB (13261027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8272ee5d2f00fd3f5cd817ce6df26066ffea813903944e72d9a9ec07e56097`  
		Last Modified: Sat, 15 Feb 2025 01:13:13 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05632780c8a1bf3116ca678db5bc00e27a5f5e6130e32d2c7dd7267fbf53fa82`  
		Last Modified: Sat, 15 Feb 2025 04:15:02 GMT  
		Size: 5.7 MB (5692386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:ea5b30a113bc5b546e39ee5cb27c3cae2df99f9118d07fc338f112f0676e32cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.5 KB (641540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c75e9228e9e7495d7c6105ed06e197001532f76e875fd7e3c9ab6e1a89673ed`

```dockerfile
```

-	Layers:
	-	`sha256:c3026ea854534046c788bc8c441a3cf23511d957425e5b76024f97b6572082b9`  
		Last Modified: Sat, 15 Feb 2025 06:17:27 GMT  
		Size: 629.6 KB (629635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25c217ce1c4c3cc21ccd306ef89e305e5be1e1413ca5c4afd3c4fa5abcce5a20`  
		Last Modified: Sat, 15 Feb 2025 06:17:27 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.21` - linux; s390x

```console
$ docker pull hylang@sha256:e992e2f83848eb62f80f2647847c6cdcd334dfd53e4e3b00f2ab22057258aa00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22615949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5bdb9796f9c8a4465d66ad1c091eb7f5e16d3fba97aa2cc680a58337663de4`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 Jan 2025 19:41:06 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYTHON_VERSION=3.13.2
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2087dc574cd4f9926799c31e0eff251e53c7a3f8a2568ea28edecde8f59eca63`  
		Last Modified: Sat, 15 Feb 2025 07:15:20 GMT  
		Size: 459.6 KB (459579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225c026fcca38dd5bfe2f68339dbf9ec5366f7ad9a5a9a2b3f5713e22f201340`  
		Last Modified: Sat, 15 Feb 2025 07:15:22 GMT  
		Size: 13.0 MB (12996551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d649318dd47fdfae9bc8a62457529c4775b15097ac3974113a9a5dfa7173cb`  
		Last Modified: Sat, 15 Feb 2025 07:15:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a76eaee02faa1c3f3d091dc124282c955ce31320f2e334ab7535ce7b34bfc7`  
		Last Modified: Sat, 15 Feb 2025 10:29:20 GMT  
		Size: 5.7 MB (5692005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:3b8fbe7b5e687fdc64523f207c9e7d5225a727723ea533b64b322f7b641b861f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.3 KB (641319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ab6ce3935bf045d45d809d563305666f6e416b0cb4b88db731870d15df2c6df`

```dockerfile
```

-	Layers:
	-	`sha256:ea725867670ce44e87e312fa5376621c0b507ed7235102fe3025a861260f821d`  
		Last Modified: Sat, 15 Feb 2025 12:17:34 GMT  
		Size: 629.5 KB (629529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05cc468b57cb2aba10319e5ae360e8ba7e7d88dbefd2053dbfdfbbcb0ca50ad9`  
		Last Modified: Sat, 15 Feb 2025 12:17:34 GMT  
		Size: 11.8 KB (11790 bytes)  
		MIME: application/vnd.in-toto+json
