## `hylang:1-python3.13-alpine`

```console
$ docker pull hylang@sha256:3ffc01c8eafb677b14dcac09f28639a84af142dee01fd1795869de8d9ecd3d5c
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

### `hylang:1-python3.13-alpine` - linux; amd64

```console
$ docker pull hylang@sha256:d2ca50c10e6bd19392675ad21818c47de1f0a0b657f051894ab25c32a03cf9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.2 MB (22195440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5023d1bac1d4d2e0a5515f4d4b43f7ea669e827965c980b290155e4d8ab84f2a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:09:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:09:44 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:09:44 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Feb 2026 20:09:44 GMT
ENV PYTHON_VERSION=3.13.12
# Wed, 04 Feb 2026 20:09:44 GMT
ENV PYTHON_SHA256=2a84cd31dd8d8ea8aaff75de66fc1b4b0127dd5799aa50a64ae9a313885b4593
# Wed, 04 Feb 2026 20:15:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:15:33 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:15:33 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:12:20 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:12:20 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:12:20 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:12:20 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98914020a3beeda22b5feedb62785c0369da8445f1e38817540570e4351534a2`  
		Last Modified: Wed, 04 Feb 2026 20:15:40 GMT  
		Size: 460.9 KB (460943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2fee0bf4ecbf895cbe636c5c9a13b8b63ac8dc00db76105cfa5e2a4bcaf527`  
		Last Modified: Wed, 04 Feb 2026 20:15:40 GMT  
		Size: 12.5 MB (12507948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a000d511eb3d8ba3007557b8d855c0e649b79a652c3f64b20045b5d595498f`  
		Last Modified: Wed, 04 Feb 2026 20:15:39 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab464f5669a6e6ced68bc156a704b8c013df6a423e04235242aabf69054d1633`  
		Last Modified: Wed, 04 Feb 2026 21:12:26 GMT  
		Size: 5.4 MB (5364480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:064cd4ae5dc1094686cd6958f3d75b955c8512a4769e4ef35f9d9f9f9812e3b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.0 KB (632023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c4e325367a58cf56987defc817c035c9012e23a249d0e8941bfa89184e96a1`

```dockerfile
```

-	Layers:
	-	`sha256:ea09e05274083d105f4c70c4bd6215190459dc265915496ad684f1a11e55477a`  
		Last Modified: Wed, 04 Feb 2026 21:12:26 GMT  
		Size: 622.6 KB (622632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1255719bf634b9282046b43443a1ed71cb2e94d2c2f4ac905d68df5933f8135d`  
		Last Modified: Wed, 04 Feb 2026 21:12:26 GMT  
		Size: 9.4 KB (9391 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-alpine` - linux; arm variant v6

```console
$ docker pull hylang@sha256:ddc02bce5ac5f35be8791f4609c0f15e48aafe909d33dd1506001c3aa802701a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21551212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef17e3f0b63237fc0abb55279048d4ad5fbe91040cb5e8d847e831eefd4770a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:03:25 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:03:25 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:03:25 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Feb 2026 20:03:25 GMT
ENV PYTHON_VERSION=3.13.12
# Wed, 04 Feb 2026 20:03:25 GMT
ENV PYTHON_SHA256=2a84cd31dd8d8ea8aaff75de66fc1b4b0127dd5799aa50a64ae9a313885b4593
# Wed, 04 Feb 2026 20:11:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:11:35 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:11:35 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:30:40 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:30:40 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:30:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:30:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848fa3a8e263b8476868647e8854141a251fa101282a234385e17c934817e20e`  
		Last Modified: Wed, 04 Feb 2026 20:11:40 GMT  
		Size: 461.4 KB (461438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b082a78975f6f16fae0498da7c726e91c01c5830eeb5c2ccee46b2a1dca7bad`  
		Last Modified: Wed, 04 Feb 2026 20:11:41 GMT  
		Size: 12.2 MB (12155107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc333407e6559005ad10628c1e1f34ab76b6e147953810f755ca2203f15ee478`  
		Last Modified: Wed, 04 Feb 2026 20:11:40 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253951e4b3e86d461c7df1e321aeff20c95be2983646a591cf4c78b93572e1dd`  
		Last Modified: Wed, 04 Feb 2026 21:30:44 GMT  
		Size: 5.4 MB (5364599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:a823646e4f00c7d992fadf9b0a08b77f15988af550dc0e2c41dbf0fef3b63111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf44db6d93a672167e9f49f49532ca970684b00383d7b7fb662223171dc4210`

```dockerfile
```

-	Layers:
	-	`sha256:91195e132a49a78a97ee64e88ae761b4760da195699796ac0ad7ccf5e5a40ed0`  
		Last Modified: Wed, 04 Feb 2026 21:30:44 GMT  
		Size: 9.3 KB (9289 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-alpine` - linux; arm variant v7

```console
$ docker pull hylang@sha256:24ba065662002874cbd685c367bfe501b5a5a323cbd8931ed15d3050fe03cba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20922790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f047893b3a8163136282c5e4feffec78f0b14c25d0819db0d85378debe36263`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:24:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:24:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:24:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Feb 2026 20:24:05 GMT
ENV PYTHON_VERSION=3.13.12
# Wed, 04 Feb 2026 20:24:05 GMT
ENV PYTHON_SHA256=2a84cd31dd8d8ea8aaff75de66fc1b4b0127dd5799aa50a64ae9a313885b4593
# Wed, 04 Feb 2026 20:32:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:32:14 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:32:14 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:32:07 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:32:07 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:32:07 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:32:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6255788e41fd0ae348926a9de7eec554d40dc85f0cbf19f0cfb9fe027d81d96`  
		Last Modified: Wed, 04 Feb 2026 20:32:20 GMT  
		Size: 460.7 KB (460741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8d16316445fa31aaa0a4be5aac837dc22fe743276b937bd44af36905c8d323`  
		Last Modified: Wed, 04 Feb 2026 20:32:21 GMT  
		Size: 11.8 MB (11815553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8608cb62444f6f007ddfc267f35d34a95f18086dff1f877060d74018da18ed6c`  
		Last Modified: Wed, 04 Feb 2026 20:32:20 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abab13c3074f9841720a3658b6ed71f7f1c5ea225d9a65c874793b1596a44b18`  
		Last Modified: Wed, 04 Feb 2026 21:32:13 GMT  
		Size: 5.4 MB (5364524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:98ef894e22790745083dc66c691428fe3030a198e7e8219e84f6aac87ef6b213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.5 KB (634544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0291d08fdf995c2faab245b98e81b16e16e097804dc89cf072faf9acb034b145`

```dockerfile
```

-	Layers:
	-	`sha256:363a1e32a78134b0529f6a12ac4dae8c00cb42a9da8ad7d24b3c58894c8dcc4c`  
		Last Modified: Wed, 04 Feb 2026 21:32:12 GMT  
		Size: 625.0 KB (625040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:828b4e97691324824f2a7182964e9b5dd493882127796625715389bc861bf5e7`  
		Last Modified: Wed, 04 Feb 2026 21:32:12 GMT  
		Size: 9.5 KB (9504 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-alpine` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:bcf98149be6ed74de5916c6fbc7c7e925f9604f8c8d46462ff893ce5dabd0e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22645406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20986fde645ccde0c955218a29f4bd5aeda8e84cc810ebe9590baad17ae61de6`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:10:28 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:10:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:10:28 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Feb 2026 20:10:28 GMT
ENV PYTHON_VERSION=3.13.12
# Wed, 04 Feb 2026 20:10:28 GMT
ENV PYTHON_SHA256=2a84cd31dd8d8ea8aaff75de66fc1b4b0127dd5799aa50a64ae9a313885b4593
# Wed, 04 Feb 2026 20:17:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:17:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:17:47 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:10:23 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:10:23 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:10:23 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:10:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a1da23b32fb1a9c7768eda7e12307dc200b2198056f06b357c2e3c287cabd9`  
		Last Modified: Wed, 04 Feb 2026 20:17:54 GMT  
		Size: 463.0 KB (463005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0f29d884b0cea26be46e229cd42db2470a78b15327709fa254b12a431f2fca`  
		Last Modified: Wed, 04 Feb 2026 20:17:54 GMT  
		Size: 12.6 MB (12620576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5d4204b445b13499868d7075309b0825e1589c866002acc2d9d451124146a6`  
		Last Modified: Wed, 04 Feb 2026 20:17:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfa31a241412340277c4c30b82053dde86983c09bb11e6b3b9df53e443a649c`  
		Last Modified: Wed, 04 Feb 2026 21:10:28 GMT  
		Size: 5.4 MB (5364485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:b69a97e16c1e77220d19952364d404974461dcf1907e2a307493e19922f5aaa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.6 KB (631630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df361985ab27f4ebe156a6a4b0887544bd3e39cb4a8cd8f2fda1aa7f5706c4d6`

```dockerfile
```

-	Layers:
	-	`sha256:bae1b9421e31d0488de89d3bb7dd5c66e55f6339d5718f26e69126dcec0e2a44`  
		Last Modified: Wed, 04 Feb 2026 21:10:28 GMT  
		Size: 622.1 KB (622086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73084f9990625a24467d9d4e2553b81620957d31aa843d55c5d9cbee0c89203b`  
		Last Modified: Wed, 04 Feb 2026 21:10:28 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-alpine` - linux; 386

```console
$ docker pull hylang@sha256:c1b11f240d605eef24b1814ffe847f102745556ddf2c38b7d6c408245cc62004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22258194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df07dbd492716343d0845cca8dfd341f10a0d21a7a8af13c7c70241688076c6`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:11:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:11:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:11:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Feb 2026 20:11:43 GMT
ENV PYTHON_VERSION=3.13.12
# Wed, 04 Feb 2026 20:11:43 GMT
ENV PYTHON_SHA256=2a84cd31dd8d8ea8aaff75de66fc1b4b0127dd5799aa50a64ae9a313885b4593
# Wed, 04 Feb 2026 20:18:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:18:32 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:18:32 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:06:54 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:06:54 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:06:54 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:06:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cac25cced6875574ac300e3e79fb033ac66adc0e948973a218118e35a3a20e1`  
		Last Modified: Wed, 04 Feb 2026 20:18:38 GMT  
		Size: 461.2 KB (461235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6604ace7d888b962d3830e6366be98e0af48239c33d05f9251846cf21fd178`  
		Last Modified: Wed, 04 Feb 2026 20:18:39 GMT  
		Size: 12.7 MB (12745185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d3c6ea2817f8c38b6eb045aaabcd019132819ae42f637abd99173ed95d7f4e`  
		Last Modified: Wed, 04 Feb 2026 20:18:38 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78852d4c7294dc7f48c61a533826379d6b8bafa6c511feaa22b570e8b06886c`  
		Last Modified: Wed, 04 Feb 2026 21:07:00 GMT  
		Size: 5.4 MB (5364528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:3147b5e5f37e4a6d3a0914584ea3c516b98f572f17ea8437d68cd8a0e5e8d57b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.9 KB (631927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67faed225fc5246a441d9c892c0ee1419c9fc486d9dff625e2b38f7a91e4d66`

```dockerfile
```

-	Layers:
	-	`sha256:8e8ac74c75bc5e90f9b7881c191615da8c2a879e9cdfcd5b084c98ab6ecbfb35`  
		Last Modified: Wed, 04 Feb 2026 21:07:00 GMT  
		Size: 622.6 KB (622587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9259de7ca9948e918f022ba16c65fe5dce7d68d4a5e531ca64c5e2b9bcb4ba3`  
		Last Modified: Wed, 04 Feb 2026 21:07:00 GMT  
		Size: 9.3 KB (9340 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-alpine` - linux; ppc64le

```console
$ docker pull hylang@sha256:6fbbaff39853771e3a927ff9183d02d3d783f89967a30f449654b16ebcda0c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (22972214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562ff4280bb1e5a49c0ca3f4dfb3a51f721cb72efe7a09c44cc570e07a35b06d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:40:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:40:44 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:40:44 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Feb 2026 20:40:44 GMT
ENV PYTHON_VERSION=3.13.12
# Wed, 04 Feb 2026 20:40:44 GMT
ENV PYTHON_SHA256=2a84cd31dd8d8ea8aaff75de66fc1b4b0127dd5799aa50a64ae9a313885b4593
# Wed, 04 Feb 2026 22:28:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 22:28:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 22:28:55 GMT
CMD ["python3"]
# Thu, 05 Feb 2026 01:37:17 GMT
ENV HY_VERSION=1.2.0
# Thu, 05 Feb 2026 01:37:17 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 05 Feb 2026 01:37:17 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 05 Feb 2026 01:37:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2192b557a530eeb9753a79cc2bf687d27f9d6c5d97252deb6915a15f66fda1b5`  
		Last Modified: Wed, 04 Feb 2026 21:25:05 GMT  
		Size: 463.7 KB (463656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec49c20bffbc88812b7b8dc02b99bb97a6e7068504ce5682ee73a697de84218`  
		Last Modified: Wed, 04 Feb 2026 22:29:07 GMT  
		Size: 13.3 MB (13314094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33dd4f73a37fa7632ed79372497606680410e97281658b05d7d5dc7ec3729002`  
		Last Modified: Wed, 04 Feb 2026 22:29:07 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa8492f6dc998a672d3380be035cf1af08ea4b6af0a1ecb5404f18504a5d63b`  
		Last Modified: Thu, 05 Feb 2026 01:37:31 GMT  
		Size: 5.4 MB (5364573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:ba6804ef3ca4870d584419cb6d9be848806747bbe350a2af27ab7b72cd87a010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.5 KB (631499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98cfc68cb8937972ccbf94b364db518de5d13bdb8382c39f1004874832257756`

```dockerfile
```

-	Layers:
	-	`sha256:3f2ce670561b1ebe576d9a6997cd72e996c4a008f9a53961c4c90cb9f15c1af6`  
		Last Modified: Thu, 05 Feb 2026 01:37:31 GMT  
		Size: 622.0 KB (622039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0728ecbd03cb6e62db847e29898b384465d4968b399d21862f796366483745f6`  
		Last Modified: Thu, 05 Feb 2026 01:37:31 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-alpine` - linux; riscv64

```console
$ docker pull hylang@sha256:8b5188a36948bc6a6b421279c07d0ddca1d3de416a5bd437000cd6741f3998f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (21952909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16b02cb900b6a8134737a7c26a3435f354601a758d5b67d53ca02f6eaa8d036`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Fri, 06 Feb 2026 21:02:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 21:02:57 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 06 Feb 2026 21:02:57 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 06 Feb 2026 21:02:57 GMT
ENV PYTHON_VERSION=3.13.12
# Fri, 06 Feb 2026 21:02:57 GMT
ENV PYTHON_SHA256=2a84cd31dd8d8ea8aaff75de66fc1b4b0127dd5799aa50a64ae9a313885b4593
# Sat, 07 Feb 2026 03:52:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Sat, 07 Feb 2026 03:52:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 07 Feb 2026 03:52:47 GMT
CMD ["python3"]
# Sun, 08 Feb 2026 02:56:55 GMT
ENV HY_VERSION=1.2.0
# Sun, 08 Feb 2026 02:56:55 GMT
ENV HYRULE_VERSION=1.0.1
# Sun, 08 Feb 2026 02:56:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 08 Feb 2026 02:56:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42271b075187de2a0c6c8a6e3df157acabf5ab65011704f66714db26ad53aa1`  
		Last Modified: Fri, 06 Feb 2026 21:44:15 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e096f7ae9dfddb540c97a59ceb4013b14bf7d8f96afea1edb81c4c8c0ea37c`  
		Last Modified: Sat, 07 Feb 2026 03:53:32 GMT  
		Size: 12.5 MB (12541890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acda4a4431e99d40931515b53f7e9311f0daec88c618f32a4cdf31a646bb8c0f`  
		Last Modified: Sat, 07 Feb 2026 03:53:30 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6797fde59d33f061dcb378fcdda2e46b1626db337c24c4fb585cb437c1007660`  
		Last Modified: Sun, 08 Feb 2026 02:57:33 GMT  
		Size: 5.4 MB (5364283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:82efae8e2e215a32bde2bd916417c6a425709eead36a632f14113f57b0d87236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.5 KB (631494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46411a0e93ddd8968b9e6e5cfb700a1fd7f84a02973debdcf69552787cf4b7f0`

```dockerfile
```

-	Layers:
	-	`sha256:e54b9b5041fe61c6ceb1a3d56e26dbb71b7ebc84e898ebe408468daa07cd7dd6`  
		Last Modified: Sun, 08 Feb 2026 02:57:32 GMT  
		Size: 622.0 KB (622035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2daa4a9d948a7883393e5438ca4ee0ba910321900aaecb24e18c3084aef2fff2`  
		Last Modified: Sun, 08 Feb 2026 02:57:32 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-alpine` - linux; s390x

```console
$ docker pull hylang@sha256:2673a5d967eb0f2767af0ef377840222e3770193bed89f7d300a8cc0f81e34ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22511520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449dc34b342e7e085b6c04449c21d338076c867b90c103c9335c8b3a33916bf3`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:12:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:12:24 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:12:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Feb 2026 20:12:24 GMT
ENV PYTHON_VERSION=3.13.12
# Wed, 04 Feb 2026 20:12:24 GMT
ENV PYTHON_SHA256=2a84cd31dd8d8ea8aaff75de66fc1b4b0127dd5799aa50a64ae9a313885b4593
# Wed, 04 Feb 2026 20:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:49:32 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:49:32 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:38:05 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:38:05 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:38:05 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:38:05 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e602ccca2f0f4b2b4eca286804ababcfed26effae18fd8c57044b782c28051bc`  
		Last Modified: Wed, 04 Feb 2026 20:16:43 GMT  
		Size: 461.7 KB (461746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e4216bc17cfb0f5ef58fcfa5046c78692500a115acfe5b2deaf4aebf9fc351`  
		Last Modified: Wed, 04 Feb 2026 20:49:43 GMT  
		Size: 13.0 MB (12959632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949c8b51007feb2dd755a3d0c2c691592648bbd353ceefa379e6e9b3d6bd7242`  
		Last Modified: Wed, 04 Feb 2026 20:49:42 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7249b734666416b62251cf6574b93ef8b98eadc2ca4e34a9ba0d998d41190a5f`  
		Last Modified: Wed, 04 Feb 2026 21:38:18 GMT  
		Size: 5.4 MB (5364561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:0d1906b0f5c2493dbae787c15fc13d0497603f056f866ff468ee270a8dead45d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.4 KB (631373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b401eb7fb8de9c8d8b5270e78047fb1be668c2f44097356d7b14817a6e695308`

```dockerfile
```

-	Layers:
	-	`sha256:8ee74ffa50793736139850cb677ea1fb219fa918eef595c956635391cdc37493`  
		Last Modified: Wed, 04 Feb 2026 21:38:18 GMT  
		Size: 622.0 KB (621981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b728cce5e0e1f0d430134bdc46c3a1414d09a72c69febd07a9259780e7891616`  
		Last Modified: Wed, 04 Feb 2026 21:38:18 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.in-toto+json
