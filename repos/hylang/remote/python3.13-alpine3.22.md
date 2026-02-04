## `hylang:python3.13-alpine3.22`

```console
$ docker pull hylang@sha256:fd2de2b68d47ca4dc17c1a8b4d7c645cef4afd9be2c1a3a7b4636974aa830dab
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
$ docker pull hylang@sha256:7627666d08b7f99b266cb04f5fe1c63180e73ea5f4de3a042edb062ab7d36ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22074008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e6b065f4843f13345cdc56b87751dbdcb94aee2031a5e22b0387df853da555`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:09:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:09:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:09:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Feb 2026 20:09:55 GMT
ENV PYTHON_VERSION=3.13.12
# Wed, 04 Feb 2026 20:09:55 GMT
ENV PYTHON_SHA256=2a84cd31dd8d8ea8aaff75de66fc1b4b0127dd5799aa50a64ae9a313885b4593
# Wed, 04 Feb 2026 20:15:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:15:09 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:15:09 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:12:21 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:12:21 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:12:21 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:12:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d6ed173981e0e874f9a790365a061ad35a738bc1219b7673d71050b3b1962b`  
		Last Modified: Wed, 04 Feb 2026 20:15:15 GMT  
		Size: 457.1 KB (457062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f390d439e4c8c70d0c46509acad835adc5e664445785906f74f10f59f820f0`  
		Last Modified: Wed, 04 Feb 2026 20:15:16 GMT  
		Size: 12.4 MB (12447311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a144893fbbbc5295d76f2a71b1395fed51e96c075b0f571058308d4aed74033f`  
		Last Modified: Wed, 04 Feb 2026 20:15:15 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a698abd3e017dcd8196b18b3708a3fe494d88b8fc5f15158630d359804c5ee1a`  
		Last Modified: Wed, 04 Feb 2026 21:12:27 GMT  
		Size: 5.4 MB (5364513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:5a4ba8f5471588119277c83dc24782f6270ec8251df741d9d4cfd1643dc96133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.4 KB (629420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10497dbce1199ddc6f62403a8cf19f76a830b4830cd3017cfac2b1ab57e45c21`

```dockerfile
```

-	Layers:
	-	`sha256:4e36c6653c83b433ea183eb6654ce5ed92050bd6e20250a369a631609cc9aed2`  
		Last Modified: Wed, 04 Feb 2026 21:12:26 GMT  
		Size: 621.3 KB (621333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:398bfe64e0deaadd8825025470a91c6fdce221c80e5fca3f41b5f25df65ce9ee`  
		Last Modified: Wed, 04 Feb 2026 21:12:26 GMT  
		Size: 8.1 KB (8087 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; arm variant v6

```console
$ docker pull hylang@sha256:dbcffbe956e113cae00f6f0a8928dbfe052f62593281774fd5b235b09b6bfae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21384405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b8b66bae3a4b40f77c0643c3ad8dc72d0a9ed15b5222a6a39695492a1fbfb3`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:03:28 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:03:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 03:03:28 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 28 Jan 2026 03:03:28 GMT
ENV PYTHON_VERSION=3.13.11
# Wed, 28 Jan 2026 03:03:28 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Wed, 28 Jan 2026 03:24:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 03:24:30 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 03:24:30 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 04:45:35 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 04:45:35 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 04:45:35 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 04:45:35 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41954f5615d4c13349de947b7db96b9914d13138a34d290849f34d5159c2ad1`  
		Last Modified: Wed, 28 Jan 2026 03:06:22 GMT  
		Size: 457.9 KB (457857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7b74ed75e1416245b2420a538bd2b384a57a5b9f024a4b8ce9a03c9f09ccde`  
		Last Modified: Wed, 28 Jan 2026 03:24:35 GMT  
		Size: 12.1 MB (12058109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810b59c953ecb2b42c47956fed04f29a8dc15ca9f4ea9f8efbdc048551f8280b`  
		Last Modified: Wed, 28 Jan 2026 03:24:35 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fa4e67dd64fa82e48ad58b0573e06a27d4e37908431b8226c0d2fc0a9b52d2`  
		Last Modified: Wed, 28 Jan 2026 04:45:40 GMT  
		Size: 5.4 MB (5363146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:e378cc37dc5f46d0014db212df030f7b9db8f38f76f04d35b048972f1f7be8ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 KB (7953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7919383e12874561f899bf21d650e9f12ec58fa9108d51de76128fb90ed105`

```dockerfile
```

-	Layers:
	-	`sha256:45ec62fc3ca3b41fe98b17e60655f52ee602d004a062bdc9768026250ff99c22`  
		Last Modified: Wed, 28 Jan 2026 04:45:40 GMT  
		Size: 8.0 KB (7953 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; arm variant v7

```console
$ docker pull hylang@sha256:dcd440be8a66cf28ce926c50e491b15c5c60a5ec1af21ee3096f6ebfcd304d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20776992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bcdf3e21276cdd430d87c73006f0165d1c4f7148bd1d53b54b4ececebbedb5`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:26:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:26:09 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 03:26:09 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 28 Jan 2026 03:26:09 GMT
ENV PYTHON_VERSION=3.13.11
# Wed, 28 Jan 2026 03:26:09 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Wed, 28 Jan 2026 03:33:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 03:33:28 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 03:33:28 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 04:30:00 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 04:30:00 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 04:30:00 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 04:30:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688155e444fc9e9f23fad9f9184a95cd40617f39f87b145693fb447fdf9b70a4`  
		Last Modified: Wed, 28 Jan 2026 03:33:34 GMT  
		Size: 457.1 KB (457054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fc497bb3fd7a119749aa66a78e4449a42694afaddb943a8eeabbf4b28f9ab4`  
		Last Modified: Wed, 28 Jan 2026 03:33:34 GMT  
		Size: 11.7 MB (11732819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61112e910391d73417d3b64fe98158815f58237a1b115e22aae315abb11dd4f9`  
		Last Modified: Wed, 28 Jan 2026 03:33:34 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78cf1dc59cd5bf34b1b41675b831cccf951bd488a880669727555f970ebe186`  
		Last Modified: Wed, 28 Jan 2026 04:30:06 GMT  
		Size: 5.4 MB (5363243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:3e41f5659611fd4113cdb34fc03ad79f2d975c797a4b48e6d56e875331b3e0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.5 KB (632526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd44bdf15c4e51a1cfb911adea9ca688c26a097c8ce900453c867b7709a03fbb`

```dockerfile
```

-	Layers:
	-	`sha256:225a6043a7e2510cb8a3f15726e09e18da03533f5eba3b4bf884aa46c6ee50b3`  
		Last Modified: Wed, 28 Jan 2026 04:30:06 GMT  
		Size: 624.4 KB (624359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8475ac6f0e15d5bdfe3aebd239691a0341511148e79b37478b27d4a5b8c0965f`  
		Last Modified: Wed, 28 Jan 2026 04:30:05 GMT  
		Size: 8.2 KB (8167 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:c5ff987b30ce5ccf4b9dfcffdeb04720204dbd93f378a158d92c62950d4f3af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.4 MB (22424580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da598ea61a9c6d32e66be0679fa3c2a91a73ac0b408a706698b639e1215b8fba`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:10:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:10:31 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:10:31 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Feb 2026 20:10:31 GMT
ENV PYTHON_VERSION=3.13.12
# Wed, 04 Feb 2026 20:10:31 GMT
ENV PYTHON_SHA256=2a84cd31dd8d8ea8aaff75de66fc1b4b0127dd5799aa50a64ae9a313885b4593
# Wed, 04 Feb 2026 20:16:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:16:57 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:16:57 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:10:26 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:10:26 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:10:26 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:10:26 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84173767172b4294095c6a04ba8e7c98ab10c5e3dc6d2c7429a3a8f74cae82ed`  
		Last Modified: Wed, 04 Feb 2026 20:17:04 GMT  
		Size: 459.1 KB (459150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60baf23321ead73361938a9ceb303c93e33e93a037060fd6ef08f73727a804b2`  
		Last Modified: Wed, 04 Feb 2026 20:17:04 GMT  
		Size: 12.5 MB (12461114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea9e44f8f37e9481ce0328d4051bcd7ec5ea584809393dcee50336f3dbc90bc`  
		Last Modified: Wed, 04 Feb 2026 20:17:03 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5985c8c2ea88f88d33b1e59f08ba751b51f10e330188504f368dac7e93910ae9`  
		Last Modified: Wed, 04 Feb 2026 21:10:32 GMT  
		Size: 5.4 MB (5364547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:7f78d79f2d2243c7856695252b2cd9c434dba49d4467c750fb69ce87aec239ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.6 KB (629581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1f72a75a4e3535aad7f9c78f457adc5eee4c6971e73fe3777d9035325e48c4`

```dockerfile
```

-	Layers:
	-	`sha256:56ad1b23347ec30d242c70bddc3b0d52612f90b3b2e2b9277834037462f5a16b`  
		Last Modified: Wed, 04 Feb 2026 21:10:31 GMT  
		Size: 621.4 KB (621389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5c319f4e051b32741354da391e4539eddaff7e727adfa4eb4f1ccaa5533eb7e`  
		Last Modified: Wed, 04 Feb 2026 21:10:31 GMT  
		Size: 8.2 KB (8192 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; 386

```console
$ docker pull hylang@sha256:cf576765cf830ed96b7422850ab8790489460d5382a75d7ff5e4e936a06dde4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22146316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59604de01f1bf916f016877849a27b821ae9a4bdb44c9d7f60de10c2e0451e9b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:11:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:11:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:11:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Feb 2026 20:11:55 GMT
ENV PYTHON_VERSION=3.13.12
# Wed, 04 Feb 2026 20:11:55 GMT
ENV PYTHON_SHA256=2a84cd31dd8d8ea8aaff75de66fc1b4b0127dd5799aa50a64ae9a313885b4593
# Wed, 04 Feb 2026 20:17:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:17:15 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:17:15 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:07:00 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:07:00 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:07:00 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:07:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0ee45bbecbfb00e68cb64771a283f4281a204b0ab7f5906080ffaa2191c6d8`  
		Last Modified: Wed, 04 Feb 2026 20:17:21 GMT  
		Size: 457.5 KB (457506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9840b4ba92ebe68e1d3f43d347812a20c73d8ca203d62d9532fb101e5a96262`  
		Last Modified: Wed, 04 Feb 2026 20:17:22 GMT  
		Size: 12.7 MB (12703327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab32a827a55e793c2833e83467a0cf4d36fd305bb4df5b292c81f9e16c94d79`  
		Last Modified: Wed, 04 Feb 2026 20:17:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf3e0a66f68854d1ef461b487715e1dde992474be00259a794ba70ca6696610`  
		Last Modified: Wed, 04 Feb 2026 21:07:07 GMT  
		Size: 5.4 MB (5364502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:748ec79c89f8d38abf1f6f60931a0a76aa555cd195c6f860ca8fa6e00a4402c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.4 KB (629364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500ba3bf31fce089cc829809220aa02d3fd2eef412320f9b467ae5223999d62f`

```dockerfile
```

-	Layers:
	-	`sha256:1f81729195386563046513f38e99d46a85dfd57f5ad26173296e323df7bccd4e`  
		Last Modified: Wed, 04 Feb 2026 21:07:06 GMT  
		Size: 621.3 KB (621308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:771b5243439a6f4b5883c9d457139f50dcd5239b4ad1955cbb5faff4ee01caa3`  
		Last Modified: Wed, 04 Feb 2026 21:07:06 GMT  
		Size: 8.1 KB (8056 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; ppc64le

```console
$ docker pull hylang@sha256:50fb759a2021cef88ff8e59c2acd84e7fcf8243021589bd94cc84928b5ef99b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22719056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55e5cdecbe55560a3e5ff46cd16b0807babd890dbb15a3c9b6111be4b1bd6d5`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:44:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 04:44:31 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 04:44:31 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 28 Jan 2026 04:44:31 GMT
ENV PYTHON_VERSION=3.13.11
# Wed, 28 Jan 2026 04:44:31 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Wed, 28 Jan 2026 05:00:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 05:00:31 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 05:00:31 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 07:00:07 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 07:00:07 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 07:00:07 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 07:00:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1c0afa633a3760fd9ab687459d95fd4798539d5a78dcc7093921a89ff5eff`  
		Last Modified: Wed, 28 Jan 2026 04:47:43 GMT  
		Size: 459.6 KB (459568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecd0ffb2bee318d8e00c9e6cd20ca338ab8309143abb7a41ce6cffbf02c59f5`  
		Last Modified: Wed, 28 Jan 2026 05:00:45 GMT  
		Size: 13.2 MB (13161767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2a192628f9cc7cb94fa2b77ce39f951502c05c44dc97235b0b879c845fa51f`  
		Last Modified: Wed, 28 Jan 2026 05:00:45 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84b409d24d39072d2fbbde3c08902c06d16685e9d36ff71895c14fbd3b0365b`  
		Last Modified: Wed, 28 Jan 2026 07:00:18 GMT  
		Size: 5.4 MB (5363176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:8d6246e8ecc8dfe870a2b3dc157ca2b32ea31eebd867dc6c409063c691c25f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.5 KB (627547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8f164fbb3dd66e6d31703ce73b2e71612104b33a7a60072bef68c0896ceb14`

```dockerfile
```

-	Layers:
	-	`sha256:38322456a8ac14db4c2ffdc0778c92b1b15ebddf10294ca738b4b127b21e6217`  
		Last Modified: Wed, 28 Jan 2026 07:00:19 GMT  
		Size: 619.4 KB (619416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647bc0473e09b68a14dd096645dfdf3ea29eb5a13918b64acd4802a67fbdda89`  
		Last Modified: Wed, 28 Jan 2026 07:00:20 GMT  
		Size: 8.1 KB (8131 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; riscv64

```console
$ docker pull hylang@sha256:7ad0780360430c06476b607b5083615a1ca603f48b8ac4e7b949ad9922b8a66f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21844316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8856750f81b27810afbf9cc7cb3bc4b031749cca561665c574c636e5b2393245`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 20:12:03 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 20:12:03 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Jan 2026 20:12:03 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 29 Jan 2026 20:12:03 GMT
ENV PYTHON_VERSION=3.13.11
# Thu, 29 Jan 2026 20:12:03 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Thu, 29 Jan 2026 23:26:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 29 Jan 2026 23:26:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Jan 2026 23:26:11 GMT
CMD ["python3"]
# Sun, 01 Feb 2026 06:04:51 GMT
ENV HY_VERSION=1.2.0
# Sun, 01 Feb 2026 06:04:51 GMT
ENV HYRULE_VERSION=1.0.1
# Sun, 01 Feb 2026 06:04:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 01 Feb 2026 06:04:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f09c06bcb0cd7a2f20a63c8a8409f2c94c296872976bd8ac6cc3232892a618e`  
		Last Modified: Thu, 29 Jan 2026 20:49:52 GMT  
		Size: 457.4 KB (457400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dfef49d187eeee5d542e9f18e822bdd94d39699fc67eab2f72675a5418443c`  
		Last Modified: Thu, 29 Jan 2026 23:26:56 GMT  
		Size: 12.5 MB (12505274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67705fe4b6ccfefead585f21aeab114b98911416f24b640ed21e94e96df4a5bb`  
		Last Modified: Thu, 29 Jan 2026 23:26:54 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192f08d451eb75505c6b0bd22916551ee06bb67d37f9cf93b27898d75976e61c`  
		Last Modified: Sun, 01 Feb 2026 06:05:30 GMT  
		Size: 5.4 MB (5363970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:94e9e5cc2253cd1fe1bf149cf3f6da0672dfe0fda3df483c027627c2a296eb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.5 KB (627544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ebcbc953f714b6d66a641a1ec62f7e30e6f2ad07f3722d859e00aec193b74a`

```dockerfile
```

-	Layers:
	-	`sha256:2a07d892fb4f5fc7e3e09a49924fbcb84b5c4c5d366cf5412133bbac96c83f8f`  
		Last Modified: Sun, 01 Feb 2026 06:05:29 GMT  
		Size: 619.4 KB (619412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc7f80cf2b2f63b7736227461891d2ac776ae2c13535ab7d3aab8e10305b4ad`  
		Last Modified: Sun, 01 Feb 2026 06:05:29 GMT  
		Size: 8.1 KB (8132 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine3.22` - linux; s390x

```console
$ docker pull hylang@sha256:466740271fc4567577ad3cc0b1ac3f8d5a9131c5340976b379d0c932a3fe563b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.4 MB (22371890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6205adad2be3f7a26261c9d7929aca900fcd5cb1b820c49ea2ae830942c1128`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:27:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 06:27:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 06:27:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 28 Jan 2026 06:27:54 GMT
ENV PYTHON_VERSION=3.13.11
# Wed, 28 Jan 2026 06:27:54 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Wed, 28 Jan 2026 06:42:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 06:42:00 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 06:42:00 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 07:28:13 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 07:28:13 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 07:28:13 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 07:28:13 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3774a20bd11bb03ab9932bdbf32f75779c80e3db7f10da48aeecbff4bb4662e9`  
		Last Modified: Wed, 28 Jan 2026 06:31:42 GMT  
		Size: 458.0 KB (458037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7b87c8062d5650a4d385d9a347254bbd609cc18fac94f779366d605eedbd6c`  
		Last Modified: Wed, 28 Jan 2026 06:42:10 GMT  
		Size: 12.9 MB (12900004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58858879cc088f5b6993ac9a5a8138311b105913d5760cd46e1d0ce38215e954`  
		Last Modified: Wed, 28 Jan 2026 06:42:10 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3332afb728cf1f4410cdd509882743c9d14c9e36d9bc7c2966e5388c56f318c3`  
		Last Modified: Wed, 28 Jan 2026 07:28:22 GMT  
		Size: 5.4 MB (5363167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:eae1b71859d91e39bb8480f6c79b5fe0b92c89cc5495371664d7d31bdb057d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.5 KB (627470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced7ba20fa1bb1340f4852830d25bb1644d3f64f21ba8c1c18d73f607e8634d0`

```dockerfile
```

-	Layers:
	-	`sha256:8e7eb76ad8e1fb925b50c135e121140bde37310857d3ca1f0a6b3991c9b0feff`  
		Last Modified: Wed, 28 Jan 2026 07:28:22 GMT  
		Size: 619.4 KB (619382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7ab987b650e77499decc241e7c5f318b82707828e065cfe38541f999a4f7b9e`  
		Last Modified: Wed, 28 Jan 2026 07:28:22 GMT  
		Size: 8.1 KB (8088 bytes)  
		MIME: application/vnd.in-toto+json
