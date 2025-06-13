## `hylang:alpine3.21`

```console
$ docker pull hylang@sha256:fe61940bcddcd1f06678eda3f1213d21b34bae28266a5545333fbde8864ec249
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

### `hylang:alpine3.21` - linux; amd64

```console
$ docker pull hylang@sha256:49baeee40f5430644409d08cde207a88feb7b377285f2c1161709d183f3919bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22260864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e615dfd47d7669be2b42bb59c2ea05bcf21f48483a661f3b6752adee46ed5261`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_VERSION=3.13.5
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_SHA256=93e583f243454e6e9e4588ca2c2662206ad961659863277afcdb96801647d640
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84470aa48fb783fccd1be9fa7306105db87bc127f10fb938a280a3aa1f77b55d`  
		Last Modified: Thu, 12 Jun 2025 22:44:47 GMT  
		Size: 460.2 KB (460212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc45a8055a8bb9c2244a321d520089247f7798e0c7e854380828de8d12797acc`  
		Last Modified: Thu, 12 Jun 2025 22:44:47 GMT  
		Size: 12.5 MB (12530944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc934c9fbaf660956c6cf1956149eba5944d69c40f0d03e919d469a633bec26`  
		Last Modified: Thu, 12 Jun 2025 22:44:47 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e028539f2d1b73610e27f0fb4d7bfb1cc4e93621963535190b9bfba1ea8462`  
		Last Modified: Thu, 12 Jun 2025 22:52:26 GMT  
		Size: 5.6 MB (5627214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:c4dcf829a85e512ac8e0e25041e55546fa781d9acae645452a2e2b48b9ce8f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.0 KB (632988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d5dabd92d007c4fdd852e7fed1848646d00f5c602cd34c3de3e8fb39045daf8`

```dockerfile
```

-	Layers:
	-	`sha256:21873fa9b19338faeb8b02684a2fd8c7f50b35a6c0ffa1b2d83d24475882638b`  
		Last Modified: Thu, 12 Jun 2025 23:17:46 GMT  
		Size: 623.7 KB (623720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb299e21986fc646cc427464d879babe517ced9267f670e39ead3da447bf91c2`  
		Last Modified: Thu, 12 Jun 2025 23:17:46 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.21` - linux; arm variant v6

```console
$ docker pull hylang@sha256:13b0f6e57d8cfe4aadc5a69bc7056558ec3aadabe54e828738e05c0ff654ec58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21605427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494775b6c8fb49f4268f8949b62221f188b3aa34a108396f583ee53a01d5d867`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_VERSION=3.13.5
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_SHA256=93e583f243454e6e9e4588ca2c2662206ad961659863277afcdb96801647d640
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
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
	-	`sha256:7e290a10df9fa58cfc8e15bc7d3ee56d64f5610ba2154b6241547a56b26d13e4`  
		Last Modified: Fri, 13 Jun 2025 00:07:22 GMT  
		Size: 12.2 MB (12153283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4535b00d4fdf6352784dd8fe6cec802c0f5fdff6b2c014f540c703ba5c605ae`  
		Last Modified: Thu, 12 Jun 2025 23:10:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ccef23358d3d08ec7873dd0ff623ebecef399cb994cf9f85305c9a6f0589c4`  
		Last Modified: Fri, 13 Jun 2025 02:18:21 GMT  
		Size: 5.6 MB (5627727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:4b4599744a0ebb41a52f9d17d367f958607d1451282f9bc87c634e27e9efb8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6164471c789ae719424c9d34512b5e70938499d102fd61d6ba586ea95e4d011a`

```dockerfile
```

-	Layers:
	-	`sha256:3421176444bb63269a984f4fa95223c37ddd03a5539d0c1b253baa6c75221a1e`  
		Last Modified: Fri, 13 Jun 2025 02:17:51 GMT  
		Size: 9.2 KB (9163 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.21` - linux; arm variant v7

```console
$ docker pull hylang@sha256:b54e816d9a790d93a244525758c63b4782061f8faf8fceebb2b035c3ae319bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 MB (21016672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b31e3f183eb68ed80dc6fc69c105967aa387c62139f28e0f48b84f0a572e8b1`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_VERSION=3.13.5
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_SHA256=93e583f243454e6e9e4588ca2c2662206ad961659863277afcdb96801647d640
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ecc85683812d0585b9ad9a25a17e496c376367d442aade30005099b80d8495`  
		Last Modified: Fri, 09 May 2025 02:30:45 GMT  
		Size: 460.2 KB (460203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3659a221ff2d3d05def6a9fe182d60739e1be935e6e0fbfb263e1fb454c5a251`  
		Last Modified: Fri, 13 Jun 2025 03:00:19 GMT  
		Size: 11.8 MB (11830277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b3620b05fdf5a661e8d9fef8978a587f1e88a42a1ba5e67483bed3b10792b0`  
		Last Modified: Fri, 13 Jun 2025 03:00:18 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc146541bd9a6a4add321b28a2c6fc3c21c561afd897d0a35c4dd01f20d368cd`  
		Last Modified: Fri, 13 Jun 2025 06:25:52 GMT  
		Size: 5.6 MB (5627821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:0436f24822832287528f945543e482514bea8f5bee286545cb275bbed10f6407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.2 KB (636156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ae1435024a05495caadb9cf090d1e1449aea011be45212a290c6b49f2e1fc4`

```dockerfile
```

-	Layers:
	-	`sha256:b18aeedb8ddd176357018243672f9ac9a6305121d98c995eddc7bc442f7f44f4`  
		Last Modified: Fri, 13 Jun 2025 08:17:37 GMT  
		Size: 626.8 KB (626778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7384c45c9084ee6d7f678fc0d04fbed3637f5e3fd630bcb48724b1a1c8b0ac9`  
		Last Modified: Fri, 13 Jun 2025 08:17:37 GMT  
		Size: 9.4 KB (9378 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:a7367f714cb8cf838933af5187e0376a4e64b37864ff2aeaa20bb48ed2a0e8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22633945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd195bf676eb9e50d71fc16f4a310acb3fec36c6659e1a58232c9e3444d2448c`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_VERSION=3.13.5
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_SHA256=93e583f243454e6e9e4588ca2c2662206ad961659863277afcdb96801647d640
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b28441aad6a5ce614544be397191306e05569c156d01bbd230edeb43a5c9a1`  
		Last Modified: Fri, 13 Jun 2025 01:48:40 GMT  
		Size: 462.1 KB (462077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8bc26ba9b079a4db18b4a86cae38db27e58bcf6e93e943d212c646862524b0`  
		Last Modified: Fri, 13 Jun 2025 01:48:42 GMT  
		Size: 12.6 MB (12550739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fedfc369cd46322fd45d91c717a1f31488f590db78f611caf0f4302549eb80fb`  
		Last Modified: Fri, 13 Jun 2025 01:48:42 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfceb3896c9ac442d4a083b710417be506f91cd8392e661012c7edb58db41c3`  
		Last Modified: Fri, 13 Jun 2025 04:34:28 GMT  
		Size: 5.6 MB (5627851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:ee6cb07501cf5e27c3f761f63a2798ce2931737eb99600567b848a4da10bf444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.2 KB (633246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a486a9ca0fbdbc07d9af6b4aef4a53b0368d331ce348fbf991a3b2115473d6`

```dockerfile
```

-	Layers:
	-	`sha256:c877911c3eb2d77abd9f2213fb88a66920445945417ef7cf79403ac3741f705b`  
		Last Modified: Fri, 13 Jun 2025 05:17:47 GMT  
		Size: 623.8 KB (623824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90023a0109e0d640a789b672f4fc1d9582acdf621632d3d5e8a10afc65c77d46`  
		Last Modified: Fri, 13 Jun 2025 05:17:48 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.21` - linux; 386

```console
$ docker pull hylang@sha256:f530be54d81133dc3b60a11ad6924c21fe86f777d5070c8f9da38374588372ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22341333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20cea130d1ffd4638d8f9c723d8d9b14b01cdb95277b6536d8dd4381fa79c874`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_VERSION=3.13.5
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_SHA256=93e583f243454e6e9e4588ca2c2662206ad961659863277afcdb96801647d640
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c291da62b123903c7c351b7fd9b5f130d00cf1661adf8f413ad79944e44473ea`  
		Last Modified: Thu, 12 Jun 2025 22:45:16 GMT  
		Size: 460.6 KB (460638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e379b979b097488c42fd88121e7706220efab2f2eea4860253ee1691f914975`  
		Last Modified: Thu, 12 Jun 2025 22:45:17 GMT  
		Size: 12.8 MB (12789150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d258111c13c19a2d08aadb4dc17f53c2559c730b23173c63f11ed964ff90ec3f`  
		Last Modified: Thu, 12 Jun 2025 22:45:16 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b657a6cbf3c92deb01f8cf010028ce84e87f2e102a6343a78a9f029de7842b88`  
		Last Modified: Thu, 12 Jun 2025 22:52:15 GMT  
		Size: 5.6 MB (5627673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:87b4d18f46cb4a042091c1bbf5966c1bf29269eefaeaa62962d87efb3abce69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.9 KB (632893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07e0410a86d34cf1e8647903af6aefdaaf4b666d7655dd5e5220f54993df870`

```dockerfile
```

-	Layers:
	-	`sha256:07d94dd812e0542f93004b2a9503057db824baa01e6fc030c8812806a7fa5b4a`  
		Last Modified: Thu, 12 Jun 2025 23:18:05 GMT  
		Size: 623.7 KB (623675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71a9b2042dea7634ae8ea504155f22f9e487aafdaef50b293931066e56344475`  
		Last Modified: Thu, 12 Jun 2025 23:18:06 GMT  
		Size: 9.2 KB (9218 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.21` - linux; ppc64le

```console
$ docker pull hylang@sha256:aeeaa2b23235f2e3098f21d08cad00a4e991645f1c9687b10c3685c714bd327d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22921296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b12c10bd03dbfba0ee6dc2de99f0851cc9826da76a486eb845deb52ee7dba8`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_VERSION=3.13.5
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_SHA256=93e583f243454e6e9e4588ca2c2662206ad961659863277afcdb96801647d640
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2a209ef4b40c4d2cca337e07efac631483c4d7b6386c631a08daa122ab2c07`  
		Last Modified: Thu, 08 May 2025 21:42:59 GMT  
		Size: 462.6 KB (462564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b320efae3e5b96fe033c8a1588079c28c3f7c00c8574b73bd016b061ed6b41ef`  
		Last Modified: Thu, 12 Jun 2025 23:31:33 GMT  
		Size: 13.3 MB (13256448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6922dcd012054746e2dc1c359dd34a10e0a38dc191403f7744589e4d9226c31d`  
		Last Modified: Thu, 12 Jun 2025 23:31:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfc217be54574b53c6b3a1e80e67a4df22b5c6f6e036b7a2679fb757ce96d81`  
		Last Modified: Fri, 13 Jun 2025 01:13:49 GMT  
		Size: 5.6 MB (5627690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:717af9ee255f768fa237fd6c6606d26c49fc9080e04950e79d8f9a6a8df31876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.2 KB (631165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756e70e72b3e0e4798ef3346f319920a26180005d4a83e2c70be48f48b5a840a`

```dockerfile
```

-	Layers:
	-	`sha256:de64aff97edc25758eef48874a55d34ae2a80aaa209dde478d779a21d3c9ec63`  
		Last Modified: Fri, 13 Jun 2025 02:18:02 GMT  
		Size: 621.8 KB (621827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dfe342ab4fd5e1d2f1f0e447bd44cf419986bc8f973e8a9b0d45a6e8bd8ecca`  
		Last Modified: Fri, 13 Jun 2025 02:18:02 GMT  
		Size: 9.3 KB (9338 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.21` - linux; riscv64

```console
$ docker pull hylang@sha256:01e9a5ffc132d647d4d3462235d130cd1abba07ddc4583694543f53651bd9454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (22044076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab67752ccaa5369667d2466874a7f6291ea604a0335a260617a9ba4b8c79470`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_VERSION=3.13.5
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_SHA256=93e583f243454e6e9e4588ca2c2662206ad961659863277afcdb96801647d640
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdd0fd69c6a32066ab97e740dd2a3c694b5914634fa4558c362a817bc0be197`  
		Last Modified: Fri, 16 May 2025 17:38:44 GMT  
		Size: 460.5 KB (460536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec787b1500d865f97b43261c9eb0f9856901ae4bf286e73ecd573c504d4fe0c3`  
		Last Modified: Thu, 12 Jun 2025 23:54:49 GMT  
		Size: 12.6 MB (12603341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63404d8e7531442a08c3f850adfbf67323776b192cd52a6b53d78d455e4d0b6c`  
		Last Modified: Thu, 12 Jun 2025 23:54:48 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dba2d157c57a2fce7131d07af98344d393548b942169c037ceac81db3c986c3`  
		Last Modified: Fri, 13 Jun 2025 00:17:49 GMT  
		Size: 5.6 MB (5628509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:871442536071afd80e752a805060e5ccea410cdb1bbb66cb1d9be9e8f09ae6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.2 KB (631161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77249c5c3c03727928bdf6b1e7e3ab91108a94df8f0c40acdb9e55273d9ee13e`

```dockerfile
```

-	Layers:
	-	`sha256:616c07363c26fda3f01b7c9ee9fbdb485f8e122dee2adece82ebfad30f7eb8f3`  
		Last Modified: Fri, 13 Jun 2025 02:18:06 GMT  
		Size: 621.8 KB (621823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ab2349d4454544f45190773ed419ed69c9a5044d8de964e13188d9a9bf01804`  
		Last Modified: Fri, 13 Jun 2025 02:18:07 GMT  
		Size: 9.3 KB (9338 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.21` - linux; s390x

```console
$ docker pull hylang@sha256:1644c9987e37ab86f3f25c80239d2deddb879f8a8bf84a4cff82dcf6752fd066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22553740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbcf6d0ee45cacd036bedb53c6ed59308b8ed1265cc1413a7fea2f9219f05e87`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_VERSION=3.13.5
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_SHA256=93e583f243454e6e9e4588ca2c2662206ad961659863277afcdb96801647d640
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289404968088d58c6b3a0ffe1ae7bd8f5cb001bacec9049fb0682278d2ce9ee6`  
		Last Modified: Fri, 13 Jun 2025 01:11:11 GMT  
		Size: 461.2 KB (461156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b0525eab77cd21a9ffad40e38ec9b67bf110e1f72995d18139c51f74bbeede`  
		Last Modified: Fri, 13 Jun 2025 03:16:25 GMT  
		Size: 13.0 MB (12997138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0059d0cbff3da80d8d40acf86f0f2bea223ed86e5bf9701fa822bc43a971d209`  
		Last Modified: Fri, 13 Jun 2025 01:11:18 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d806bc56187a4bbe2a6bb5cd0b1980ad6e2454cdeb4a5f77086135da469add`  
		Last Modified: Fri, 13 Jun 2025 02:33:29 GMT  
		Size: 5.6 MB (5627631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:01763a4588cf3abce27d024f521d5442050c31a6a7da223c11a72363f32b846d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.0 KB (631039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab828af97c9c0126af44cc8245dee1c03dd1696df3a8938d873cfd76f2ca7f12`

```dockerfile
```

-	Layers:
	-	`sha256:6a136b1fab47f478e1a1d4a4d8102df4e524a7f5e8d9cf8708ee9610690437d3`  
		Last Modified: Fri, 13 Jun 2025 05:17:58 GMT  
		Size: 621.8 KB (621769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dab790d1ff5943bb33ae2fabd5ef41747ca38417a2fdef1f5f8657c64eb9a857`  
		Last Modified: Fri, 13 Jun 2025 05:17:59 GMT  
		Size: 9.3 KB (9270 bytes)  
		MIME: application/vnd.in-toto+json
