## `hylang:python3.13-alpine3.22`

```console
$ docker pull hylang@sha256:0b92897842bb9c5def841a6292605ac92261438949c47b84dc7eed5c945e2261
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

### `hylang:python3.13-alpine3.22` - linux; amd64

```console
$ docker pull hylang@sha256:9517775ecfc5ddb82d6c7f7c2c895ee41da42724fba0534317e1f43c2af448a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22136275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5d23f99ae4dc1665e206355b8348cc97e1929089d527cb9baf62fa67a3991b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:30:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:30:58 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:36:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:36:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:36:20 GMT
CMD ["python3"]
# Wed, 14 Jan 2026 21:58:44 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 21:58:44 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 21:58:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 14 Jan 2026 21:58:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26daf640290a5c96818eeceda9d0ca2e9fc41fc3a6b57a9042ed93a479c15161`  
		Last Modified: Mon, 08 Dec 2025 20:36:26 GMT  
		Size: 456.9 KB (456928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b1972ad510f9ac01c1a925be2d191877631aa1ac5fb973b6e7bd8bcb4133e2`  
		Last Modified: Mon, 08 Dec 2025 20:36:33 GMT  
		Size: 12.4 MB (12438092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25dc0fb9705edc6661711090bbb88c90560b516b861680a35178aaf986296a8`  
		Last Modified: Mon, 08 Dec 2025 20:36:26 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a34ce703a985aea6553db324f2b0b0f4f0e549cd56fb7071118f7e6b6cf75d`  
		Last Modified: Wed, 14 Jan 2026 21:58:59 GMT  
		Size: 5.4 MB (5438552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:74186ff71ae5729641984b308d90b4cb50a8485593f0cfd2ae259eb78c561da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.4 KB (629420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a4c7b5715f870bffbcbb0e41ef9523e7a6ea18bd0ddf8cab3707a8a6778e8d`

```dockerfile
```

-	Layers:
	-	`sha256:a4fbde9018dcb109941abc1f1e97e95b889c85a88727b03b057dfd126125541d`  
		Last Modified: Wed, 14 Jan 2026 21:58:50 GMT  
		Size: 621.3 KB (621333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb4993db2c7dc4dde53b6704d61b7bc26445dde5dcbcd2e8eac06f863d41e7b6`  
		Last Modified: Wed, 14 Jan 2026 21:58:50 GMT  
		Size: 8.1 KB (8087 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; arm variant v6

```console
$ docker pull hylang@sha256:ae41b5429e74fb581ff8b40dcba874b9ad7775ff0005bc73a0c885ebc37844af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 MB (21459048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b80ae7f6d5cd20efe76240f70d50cff222d0a5755569943bdee199c1d0ae78`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:37:17 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:37:17 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:37:17 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:37:17 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:37:17 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:44:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:44:31 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:44:31 GMT
CMD ["python3"]
# Wed, 14 Jan 2026 21:59:51 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 21:59:51 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 21:59:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 14 Jan 2026 21:59:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4ef9953e8f76830690723b424052e9d0aaa92ddf1db0ea2151888d611a1410`  
		Last Modified: Mon, 08 Dec 2025 20:44:36 GMT  
		Size: 457.7 KB (457746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960947f74747eb5d3fa23020c8433c87df91a346c87d7ffca2325e6c6ec37f26`  
		Last Modified: Mon, 08 Dec 2025 20:44:44 GMT  
		Size: 12.1 MB (12058386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948232beba1fcd2e2960ee4be1f127fab143e669419e510951ce890f59d91446`  
		Last Modified: Mon, 08 Dec 2025 20:44:42 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7157e08adf9debe68333370c17a9a2d93280e07f4788191325c7be3b1082b8b`  
		Last Modified: Wed, 14 Jan 2026 21:59:56 GMT  
		Size: 5.4 MB (5438588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:b3c3c725410d2465646005f81cb0c0149f2d205160f15cfcc354d02bd158e77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 KB (7953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe19ae4d31dfe8af11aaf2099c19983f1b87abeba871357f4da9c383bf889bf0`

```dockerfile
```

-	Layers:
	-	`sha256:4cb075cc3b65260bc1099f0708ea708933964a7256455917a7cdaafcfe529303`  
		Last Modified: Wed, 14 Jan 2026 21:59:56 GMT  
		Size: 8.0 KB (7953 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; arm variant v7

```console
$ docker pull hylang@sha256:fcf5874ddc7a68945690fd2e73c086ea992fac4f10ae38d96f9295b875c7edaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20850021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f426f316a40dfad2f4d40c2628c2a0cf6fe0e23021f60d109fb6ce4fc8337c2c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:26:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:26:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:26:33 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:26:33 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:26:33 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:36:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:36:49 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:36:49 GMT
CMD ["python3"]
# Wed, 14 Jan 2026 22:00:26 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 22:00:26 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 22:00:26 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 14 Jan 2026 22:00:26 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:18 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2474599e695d7437ca707c1ff8a909d36e24da5d83b0796f3c299f61617550`  
		Last Modified: Mon, 08 Dec 2025 20:29:28 GMT  
		Size: 456.9 KB (456934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9d1e8408e3c7369d6c88672e34d23d0dd9b36dee622956047d4aec2ebf8364`  
		Last Modified: Mon, 08 Dec 2025 20:36:55 GMT  
		Size: 11.7 MB (11732736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba5d4e32ca6499e7d2e59fbba3ddaca83b1d21d05f59a301de1cf1620210bc4`  
		Last Modified: Mon, 08 Dec 2025 20:36:55 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1d31642aa25776d337eb5bcdfc75d7b38b7181843783c7405e9c281dd6dc72`  
		Last Modified: Wed, 14 Jan 2026 22:00:40 GMT  
		Size: 5.4 MB (5438549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:ae6a97441c8a7e26f908e40596f5d98b86618ed58b4c765de3f33b592e8b0076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.5 KB (632526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3660dafa1da4dfaefc80ca5e64197e384c5b0b0fd7b99634098d3e07b2d940`

```dockerfile
```

-	Layers:
	-	`sha256:41c319c6fd7f2539bf9005e2860dfa056fabb9abad41dfe78b0000ea9453e884`  
		Last Modified: Thu, 15 Jan 2026 00:25:47 GMT  
		Size: 624.4 KB (624359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89682a25acc526bc539377357225b1737c1e737afbce7af19173f1fef77a9e92`  
		Last Modified: Wed, 14 Jan 2026 22:00:33 GMT  
		Size: 8.2 KB (8167 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:a26fbfaa9ac7fcb6fd00644e336a169771f7ac2b15b66b2c405eeaed7aa1c2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22489359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a912302935ed130d68ff1051fe75966ec228ec77dae9c0d5ae6c19354804b7`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:13:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:13:36 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:20:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:20:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:20:06 GMT
CMD ["python3"]
# Wed, 14 Jan 2026 21:59:32 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 21:59:32 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 21:59:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 14 Jan 2026 21:59:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04eda5d87448437994b338947f03a72065bf589d08071ba33ba5dc3ea1ddcf9`  
		Last Modified: Mon, 08 Dec 2025 20:20:23 GMT  
		Size: 459.0 KB (459020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19756ed87e004e14deeb5d042df980b7204f44649d4cce479201223a8589ab`  
		Last Modified: Mon, 08 Dec 2025 20:20:23 GMT  
		Size: 12.5 MB (12453549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be90ee3c5e8855f927e9dabc42fd16e3baec85cb245b81e43412665495c6b4a`  
		Last Modified: Mon, 08 Dec 2025 20:20:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa941e20e5f9d9adbb3d390785800ac9944eb5cc6a10dc1bcd96e1258b69c67b`  
		Last Modified: Wed, 14 Jan 2026 21:59:39 GMT  
		Size: 5.4 MB (5438474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:75058fd3a5feee9d79d56b62b7af80f9044eea3b31940d257d2b2b8fa17e523c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.6 KB (629581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882fa8886a108c8ad4b52be3cff748b3c3e6f22619507b798cafc2b64eac8acd`

```dockerfile
```

-	Layers:
	-	`sha256:2516ae800e2485651d5317fc75a3f1770252049500d4086537039d54b7a602c5`  
		Last Modified: Wed, 14 Jan 2026 21:59:38 GMT  
		Size: 621.4 KB (621389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f84b152f86d8e9bcf06241eaed1eb7cee17ece1667a2b795456bc9684fd4eec0`  
		Last Modified: Wed, 14 Jan 2026 21:59:38 GMT  
		Size: 8.2 KB (8192 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; 386

```console
$ docker pull hylang@sha256:cbb22a1eb0c295b0018e6f31450058aff7a62766d1e2920231182b623f7da49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.2 MB (22211720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664882ae763f2c81a364da97c6f3ca48ad765e0f12802f8605a66b16419e3b8b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:19:03 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:19:03 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:19:03 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:19:03 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:19:03 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:25:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:25:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:25:13 GMT
CMD ["python3"]
# Wed, 14 Jan 2026 22:00:39 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 22:00:39 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 22:00:39 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 14 Jan 2026 22:00:39 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Sun, 07 Dec 2025 14:06:47 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21799b38655028ac8c9328b18eeb2e493498195aea46a07a8f147ca24d20ce0`  
		Last Modified: Mon, 08 Dec 2025 20:25:26 GMT  
		Size: 457.4 KB (457378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cc7951148b66fc858ade47919aa366b45aa6f7a95d0cdc60adab160a8fc30d`  
		Last Modified: Mon, 08 Dec 2025 20:25:27 GMT  
		Size: 12.7 MB (12696615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dbd0c0ca02a7152c118024e1971194aab390d9f7306380eb80ecbd854408d7`  
		Last Modified: Mon, 08 Dec 2025 20:25:20 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5385dec301402df6c9c070eaca4db1834f379961b4bb7e1165b3971c21410b0e`  
		Last Modified: Wed, 14 Jan 2026 22:00:54 GMT  
		Size: 5.4 MB (5438547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:57eac770cd86cf44c6f17310a5b44b1f20265d4d3dfecb6d8e9541aaff7d9aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.4 KB (629363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16e5f21f0fe7fc3afce7f15c87486864f73ea5e5b7d5adbc750b8c1f1b34ff4`

```dockerfile
```

-	Layers:
	-	`sha256:4f532bb49ea2c250cb3c2f8e4dc2719ec26caa56740079ddf023e73b227408ca`  
		Last Modified: Thu, 15 Jan 2026 00:25:58 GMT  
		Size: 621.3 KB (621308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63eced23f8a772b3a197f5231bc038bb6105728b3b47cb9d683758ce4159dc29`  
		Last Modified: Wed, 14 Jan 2026 22:00:46 GMT  
		Size: 8.1 KB (8055 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; ppc64le

```console
$ docker pull hylang@sha256:a9a07bdf6e4028ac4bb5ecf42c8554f2dafda550cc017ddd06c9f8ce66000f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22792386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0168b2f7d743e981eb892b254e0c1ba672d129b6305a5614f624dcf9c59d09d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 21:04:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 21:04:57 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 21:04:57 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 21:04:57 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 21:04:57 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 21:57:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 21:57:32 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 21:57:32 GMT
CMD ["python3"]
# Wed, 14 Jan 2026 21:59:48 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 21:59:48 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 21:59:48 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 14 Jan 2026 21:59:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:06 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5562f27fade7a45fdd6b307b93ea9aea9528474a73ae82b42116409f5faa697e`  
		Last Modified: Mon, 08 Dec 2025 21:08:18 GMT  
		Size: 459.4 KB (459424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390c473f185f700ddaae1fbe70990b90c9d80e2edcead928cd318ac254e4be93`  
		Last Modified: Mon, 08 Dec 2025 21:57:45 GMT  
		Size: 13.2 MB (13161915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b81681e57b20a98c57d069c568708a1af970225c7ad7c39eb1ae93c63cf5ec`  
		Last Modified: Mon, 08 Dec 2025 21:57:44 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49399f3b1ecbaf457b288a4c35ac37d726d68a351d6a6f6a8f84ad04ad4d8390`  
		Last Modified: Wed, 14 Jan 2026 22:00:23 GMT  
		Size: 5.4 MB (5438557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:c282f5e57e83d6437c05b6524e564d413f9c96a52b74317cee9574ed6226e227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.5 KB (627548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b7c5fdd4f1f7414daaadd94fd56acffb8535ef894e3024f8fbb3f485f47e0e`

```dockerfile
```

-	Layers:
	-	`sha256:253c51237783daab52f8bbc88f0301cc4af5256fb80a5f111a9a2c41696a5ab7`  
		Last Modified: Wed, 14 Jan 2026 22:00:13 GMT  
		Size: 619.4 KB (619416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:504d5ca6393771e6b849a5f85e642d29ad5dcbad20cf22f6232048a15d1d9f4c`  
		Last Modified: Wed, 14 Jan 2026 22:00:14 GMT  
		Size: 8.1 KB (8132 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; riscv64

```console
$ docker pull hylang@sha256:51f388352764e5c0fdaaac3c59b5590517bbcdf99078a3579049eedf31aeb93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21917253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da66b888f797c3a711ffa9261cb175d8beb4e74dded4459e199cb6bc6a08b4f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 21 Nov 2025 02:32:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Nov 2025 02:32:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 21 Nov 2025 02:32:45 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 21 Nov 2025 02:32:45 GMT
ENV PYTHON_VERSION=3.13.11
# Fri, 21 Nov 2025 02:32:45 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Tue, 09 Dec 2025 01:39:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 09 Dec 2025 01:39:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 09 Dec 2025 01:39:37 GMT
CMD ["python3"]
# Mon, 19 Jan 2026 09:33:38 GMT
ENV HY_VERSION=1.2.0
# Mon, 19 Jan 2026 09:33:38 GMT
ENV HYRULE_VERSION=1.0.1
# Mon, 19 Jan 2026 09:33:38 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 19 Jan 2026 09:33:38 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:17:39 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2877bb53774363add4a89387f6600996a5058bff9f65b88b5e8eee6ca3040264`  
		Last Modified: Tue, 20 Jan 2026 10:08:19 GMT  
		Size: 457.3 KB (457273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbda78d52bc0c783de1c78acab3c57cde99e9d79d1324b71d7e4bf91a1fd2f4`  
		Last Modified: Tue, 09 Dec 2025 01:40:31 GMT  
		Size: 12.5 MB (12505146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9979dd7f5d471fd0f57e0348b603b63333e3d8ca9d4882d9766cd85b2269580`  
		Last Modified: Tue, 09 Dec 2025 01:40:30 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf50a1c82a2297c347d7cc0f38368c65cce666448ded6153ff01f3cbd95032b`  
		Last Modified: Mon, 19 Jan 2026 09:34:21 GMT  
		Size: 5.4 MB (5439344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:5679743ea2c39a7ec7b635214cf4ceac024571066348d2460b5e937b88bfd434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.5 KB (627544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb52f5244d37bfcbebf02118a2773227117ef7955bc1011e6dd7cc65d2e6fb5`

```dockerfile
```

-	Layers:
	-	`sha256:c4127de94daedc5c627e0a026ff9ad8ec3cde5a09850939aa83fcb93781d5b98`  
		Last Modified: Mon, 19 Jan 2026 09:34:15 GMT  
		Size: 619.4 KB (619412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98d29c91452fef43d3bda4e924db71aedf70dac3b150a242e573e3b6f22aafc1`  
		Last Modified: Mon, 19 Jan 2026 09:34:15 GMT  
		Size: 8.1 KB (8132 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; s390x

```console
$ docker pull hylang@sha256:05c14f28f82d8aea08253e7509725ea14f41e3c19e2832b4e41eefbd2281db99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.4 MB (22445696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e290cfae21870847e6454a594f22fde9a8030e942154d6931bff16e6b54e7f40`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:21:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:21:13 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:21:13 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:21:13 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:21:13 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:46:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:46:38 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:46:38 GMT
CMD ["python3"]
# Wed, 14 Jan 2026 23:02:09 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 23:02:09 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 23:02:09 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 14 Jan 2026 23:02:09 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81cf0a73ea61915b865d24fdaefdc809c8f550c8e9651c5b6ccca95977058d8`  
		Last Modified: Mon, 08 Dec 2025 20:32:28 GMT  
		Size: 457.9 KB (457916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0930b4e226aa4b7a0be68020a5d4a7f5fc129a2e062e286a470e42cf45bd1b`  
		Last Modified: Mon, 08 Dec 2025 20:46:48 GMT  
		Size: 12.9 MB (12899941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebda395a7e947f463eb52b64b17b91fa32309e2a2e16849f8be5b4c18a84c21`  
		Last Modified: Mon, 08 Dec 2025 20:46:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e839cd0fbdd40ee585fe314ab0abffc99d4d057533f0bb95cea5c117478fc6d`  
		Last Modified: Wed, 14 Jan 2026 23:02:26 GMT  
		Size: 5.4 MB (5438347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:6af10dacbba75707b74935a17de08b3ef7c5f46dec9e4e708d260ff5ef61e0cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.5 KB (627470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bdd2e786d06dd97bbad8c5b35fc3d7fee18b6e82be9885681b55132e038e72`

```dockerfile
```

-	Layers:
	-	`sha256:68527b6a4abc8e074a41c9358768f9469f7bd912be3fb483fda11cc7fd26a8f8`  
		Last Modified: Wed, 14 Jan 2026 23:02:18 GMT  
		Size: 619.4 KB (619382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aedddb6f4d191b6e56f31ddd8c5e20d851fe2fa6d80ca433047039424dd87132`  
		Last Modified: Wed, 14 Jan 2026 23:02:18 GMT  
		Size: 8.1 KB (8088 bytes)  
		MIME: application/vnd.in-toto+json
