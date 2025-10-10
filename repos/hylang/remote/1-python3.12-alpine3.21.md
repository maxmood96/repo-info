## `hylang:1-python3.12-alpine3.21`

```console
$ docker pull hylang@sha256:b7673b99cec5a242bcd36ac464adcb75f357aef5d544f802b86642709e822b78
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

### `hylang:1-python3.12-alpine3.21` - linux; amd64

```console
$ docker pull hylang@sha256:3b7316ce15ae5e8d6287d7814966d63b6b017c3a83757eee60667e9de45ac508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23367396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4353303400f3e7c8e9478b225df661e2574bb23f229ed685954c3e544228093c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.12.11
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=c30bb24b7f1e9a19b11b55a546434f74e739bb4c271a3e3a80ff4380d49f7adb
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbd27cc9a04a689b047fbb5f9452a891e05ed418e4f9b6fb592a2172107769f`  
		Last Modified: Wed, 08 Oct 2025 23:48:12 GMT  
		Size: 456.9 KB (456868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c953728a0dfa5b66faa8d5b0b1de9137c49378dacc6cb98c0f6339bab3e7f7d`  
		Last Modified: Wed, 08 Oct 2025 23:49:46 GMT  
		Size: 13.7 MB (13668757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7b373dd78e2f81ad0365aaea4f43054082377d7f9c3dc5045fcd51b89d3dcf`  
		Last Modified: Wed, 08 Oct 2025 23:48:19 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c8758f97c1d40b7ba3afbd10203081ec8b1d6be7d809707bf33f8b113ce6e2`  
		Last Modified: Wed, 08 Oct 2025 23:50:15 GMT  
		Size: 5.6 MB (5598956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:011579ff3e764a2a8cb6a04ebd4dc00cde7bceba06c3f46293f85462dd02473f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.1 KB (660135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e348b77ee67d5fa084be5ba76cc9d7fb3ad2125f60dc9d14be93e3a38c7b40d`

```dockerfile
```

-	Layers:
	-	`sha256:e7bca8b1568ffd8991b7b701699b1c1d9c60fce2c1478edb9de46e1204da3c10`  
		Last Modified: Thu, 09 Oct 2025 02:20:00 GMT  
		Size: 652.1 KB (652097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b0bd2b751e438a53fba9ad26ea4bd5efccca7094f43d253737bf4cd6419bab`  
		Last Modified: Thu, 09 Oct 2025 02:20:00 GMT  
		Size: 8.0 KB (8038 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine3.21` - linux; arm variant v6

```console
$ docker pull hylang@sha256:283b282e5dac2d3d906c51f41f74edf09fcd8cb75dc21d480ba23d41f816fd88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22631799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1faccf0991872f56754cb8a3acb23a415e013e6368daccbe28141a85b82f1d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.12.12
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=fb85a13414b028c49ba18bbd523c2d055a30b56b18b92ce454ea2c51edc656c4
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a354d4eda470b43231cbf360a76cdb7d0ba148fa93e4cf4d4b530e71891d9c`  
		Last Modified: Thu, 09 Oct 2025 22:41:22 GMT  
		Size: 457.7 KB (457683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aafde30fd95c5f5a24d4d2a4976baa5332a6fe888844f1cc21359268e26c2e7`  
		Last Modified: Thu, 09 Oct 2025 23:23:42 GMT  
		Size: 13.2 MB (13207501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7c273b841bdc089db03ef4ab8f899f5e24645af2c2d1a209bd45338cb691f3`  
		Last Modified: Thu, 09 Oct 2025 22:41:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f838a922b1a259d79ea0aa10e9290ffa4f1c707f0cd85711ab10a0827902a14a`  
		Last Modified: Thu, 09 Oct 2025 23:24:23 GMT  
		Size: 5.6 MB (5600901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:f874ada11a772cae383196f7656f3f09942e56a227de637521503a86e0bdd207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1c80ae7cf6eaaabb885e037d424701be891689a1fc08ae70288c71071a0a7b`

```dockerfile
```

-	Layers:
	-	`sha256:5034a96bc2c9732c72340f3f9d2a63945c1f6a45c475947ff5cb4c0911531566`  
		Last Modified: Fri, 10 Oct 2025 02:18:20 GMT  
		Size: 7.9 KB (7903 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine3.21` - linux; arm variant v7

```console
$ docker pull hylang@sha256:403b40fb7f4372fb5b1f314067bc343b280997142773551048b534d37221ebd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (21969622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31fe2b75eee5431a968b8af6e3b98d8d3bcc31c097752192203de7bff45b961`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.12.11
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=c30bb24b7f1e9a19b11b55a546434f74e739bb4c271a3e3a80ff4380d49f7adb
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b31bd6442fb0eca8e4d4dd63ff92ffa87121cac0c1a3896be9c2c0fc012a71`  
		Last Modified: Wed, 08 Oct 2025 23:33:29 GMT  
		Size: 456.9 KB (456876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef04b47768918699ef2ef1b57a00cc3f60c9ca70e88cfcf45074eebe9c3c3d2`  
		Last Modified: Wed, 08 Oct 2025 23:33:30 GMT  
		Size: 12.8 MB (12814947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7201aa4425f14be62a19c7fdb55d4c477e2397005014d14a676ff4bc138a41f2`  
		Last Modified: Wed, 08 Oct 2025 23:33:29 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599798dbc80e1a65a7886e869956d95301367062117881abc1cb1314a0b63ca7`  
		Last Modified: Thu, 09 Oct 2025 00:18:06 GMT  
		Size: 5.6 MB (5598940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:33ceff2bf1cbd688bd447bbf3609c622fbe50a64a971458cec169ab80099e486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.2 KB (663241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06760a18f89e1ae58fe9aa315e45e1a8f50d3402c6cea299da3720d015562e29`

```dockerfile
```

-	Layers:
	-	`sha256:f61e3cec0d1686384f7f2464a5aabfa5818552307ab952786a432d95dda29acb`  
		Last Modified: Thu, 09 Oct 2025 02:20:07 GMT  
		Size: 655.1 KB (655123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15856e3f584036d4b0d2ecdbdcbe300544c2d1a2977462e53698435c34cfa4b8`  
		Last Modified: Thu, 09 Oct 2025 02:20:08 GMT  
		Size: 8.1 KB (8118 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:1c0281b9483d5479300625e0929f9d910c34941a352fad9ba2d359acb0bc0989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23766994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e693f1cb13f875fe2c30724680d696e8ff38c21ee04a60f01c9280ace61c15`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.12.11
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=c30bb24b7f1e9a19b11b55a546434f74e739bb4c271a3e3a80ff4380d49f7adb
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a15deca6ac987f9edd3c9deb517293f116e026dc6274bba74a530a207062d9f`  
		Last Modified: Wed, 08 Oct 2025 23:14:05 GMT  
		Size: 459.0 KB (458985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a770cd182584554ebbf72971434a80e3f11e85b8e2e0d6f339bc04f7c70d3`  
		Last Modified: Wed, 08 Oct 2025 23:14:06 GMT  
		Size: 13.7 MB (13716509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e593bfd5e4de05faf014c2d781da01566b93648e18d3b7296e09f1fba5229a3`  
		Last Modified: Wed, 08 Oct 2025 23:14:05 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2354d235067cacba2cf3f0fb1e894ab7e4bdf1f2127d4cb2340eb01f3d98d7d7`  
		Last Modified: Wed, 08 Oct 2025 23:33:33 GMT  
		Size: 5.6 MB (5598900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:123a9b3cafbf83bbc8aae13c9c2ea07be36852bc46c11fb6819dbcec25cbab58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.3 KB (660294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae55fa8c4f4296516b7abdffd8a29a790749dfd1595c8f9aa32137863bc246af`

```dockerfile
```

-	Layers:
	-	`sha256:4621dd0bf64c1dc2a8144194a11e993df8a6956fff54a2ba660c7aecaf7a692d`  
		Last Modified: Thu, 09 Oct 2025 02:20:11 GMT  
		Size: 652.2 KB (652153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dfee6cb61684e83846d5fb5c0f35c3202bbbc7443cdf341031fa219d7134581`  
		Last Modified: Thu, 09 Oct 2025 02:20:12 GMT  
		Size: 8.1 KB (8141 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine3.21` - linux; 386

```console
$ docker pull hylang@sha256:d28d25436809e14ff9c4aad4229b96b2ec37e9be2154ae705057cf6ef2b88a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23410134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8fa94643b4af1a9f3e264c4ad025b8a09e5db080b4f68cbd7c1bba359e3059`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.12.11
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=c30bb24b7f1e9a19b11b55a546434f74e739bb4c271a3e3a80ff4380d49f7adb
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1140196fa2abf7b47f134bc52ccd4605d0e871ef8ccaed1587a188b7e2eea8`  
		Last Modified: Wed, 08 Oct 2025 21:55:03 GMT  
		Size: 457.3 KB (457346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a919fcf5d9a9c7b617730ab364b637a994e6fc3f2b301cb05c323903b72e49f`  
		Last Modified: Wed, 08 Oct 2025 21:55:05 GMT  
		Size: 13.9 MB (13888799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93a6932919ab8c2db39ce45024f4838d1a6976bbf6510be9a335cf017d126ae`  
		Last Modified: Wed, 08 Oct 2025 21:55:03 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bec5562a1817603214621c0c66621b62ed444f8e31f3cf72820b08e7fd990d`  
		Last Modified: Wed, 08 Oct 2025 22:28:30 GMT  
		Size: 5.6 MB (5599036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:c7452768f4dfb58218597e31751e4d0ab3e7830a6d2cc694db41c8229f7e7448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.1 KB (660078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe75a27abe5a6d62bcec914372a344c26a16a14e47a5d36396a164a5b1cdc7f`

```dockerfile
```

-	Layers:
	-	`sha256:c61bfaa82d1fa3203328646656540daee04c6142526f8f317ea2fa3d0f0ff6d8`  
		Last Modified: Wed, 08 Oct 2025 23:24:15 GMT  
		Size: 652.1 KB (652072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19cbf9046e741086eb038a808e36c9027f667666a1a8eba38b80c50249c740c3`  
		Last Modified: Wed, 08 Oct 2025 23:24:15 GMT  
		Size: 8.0 KB (8006 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine3.21` - linux; ppc64le

```console
$ docker pull hylang@sha256:cb5dafac73a7e7af7d79afb76e3d4dc8fdbaefcc755b489608295ba05d6e848d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24066759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80836c4632d702126be235680a8ee705d0145ce57a00e0265cee592b1f69ba06`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.12.11
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=c30bb24b7f1e9a19b11b55a546434f74e739bb4c271a3e3a80ff4380d49f7adb
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0026c7dc43c0a7255a1ad9f4da34ccbef2597f65b422a86bda4c70ee1f6cbd4`  
		Last Modified: Thu, 09 Oct 2025 08:37:20 GMT  
		Size: 459.4 KB (459409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adce90de504f9dd95964bef46a9ccd1249d14761e6ab96417ea8516cde47856`  
		Last Modified: Thu, 09 Oct 2025 08:37:24 GMT  
		Size: 14.4 MB (14434072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9d838316872129259a9c45dc4e31795e8a93bd844e5102a1bd6c5cbb577394`  
		Last Modified: Thu, 09 Oct 2025 08:37:20 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c223fa38ebba1ea25d283a45362b28e3837205c55cc1e912e69c1f113c36d2eb`  
		Last Modified: Thu, 09 Oct 2025 11:18:26 GMT  
		Size: 5.6 MB (5598954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:a7f7f98a7d3a19110406859fb8e496b73ccaab220410b57afae0969861287a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.3 KB (658262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8efa305e252bb989bb272d01b64e9f7b16fe065b5e16aa4b3bbe627348f7c6`

```dockerfile
```

-	Layers:
	-	`sha256:6a932382bfe5fad0ca18e816bd5ee6b4fd90d77bdb9659b63b9fc8784430f46a`  
		Last Modified: Thu, 09 Oct 2025 14:18:54 GMT  
		Size: 650.2 KB (650180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:538f59dedc0a895b4f7314bb185f4b6b0f9dfb8f813136427725cac43b6ba24b`  
		Last Modified: Thu, 09 Oct 2025 14:18:55 GMT  
		Size: 8.1 KB (8082 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine3.21` - linux; riscv64

```console
$ docker pull hylang@sha256:299db121cb5ba392899e4aeaaeff19281bcbce02eab84aafaa99bd5feda337f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23113156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c4d7507981377ceb831b10043f34e401ac26c5ae0cbad2eec9d76c225f3144`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 18:20:34 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_VERSION=3.12.11
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_SHA256=c30bb24b7f1e9a19b11b55a546434f74e739bb4c271a3e3a80ff4380d49f7adb
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
CMD ["python3"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HY_VERSION=1.1.0
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 13 Aug 2025 21:03:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab0152f745fe105bd917dd035bf213e5a0afdd2b6b1e0eb9374377da919271d`  
		Last Modified: Thu, 17 Jul 2025 19:53:24 GMT  
		Size: 448.0 KB (448014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62088cc96bab99ba05d98868d136635efacdb22c04aab5a4fd98e0549b91103`  
		Last Modified: Wed, 13 Aug 2025 07:10:05 GMT  
		Size: 13.7 MB (13715716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2eea3bb96d4e029105a3eec6cd8a2031a812ecb2f010dc7e696a40a68132f0`  
		Last Modified: Wed, 13 Aug 2025 05:37:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f6e445de210310adaa87e53071204911c595d9b7550fcdef98c54cb3ca7c32`  
		Last Modified: Sun, 17 Aug 2025 12:47:37 GMT  
		Size: 5.6 MB (5600087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:4db766f23b50dabe5d93937239f45222f9dc8a74f526799083825fa3e565921e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.6 KB (655645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab8b19d6d6f41742904c264136313d07189107aa91f60edbb78749c8c5334df`

```dockerfile
```

-	Layers:
	-	`sha256:87da98fdb9db158dd7fbb92040df1bfd5248bd29719e3d31c6aa3b781924e51f`  
		Last Modified: Sun, 17 Aug 2025 14:18:32 GMT  
		Size: 647.6 KB (647563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d13d8df6939e067fad35cb8de4f70d96c56855b1fecb85e5f5a64ce6f499029d`  
		Last Modified: Sun, 17 Aug 2025 14:18:33 GMT  
		Size: 8.1 KB (8082 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine3.21` - linux; s390x

```console
$ docker pull hylang@sha256:25bca09efebb31f4b933f9f747322ddd36ae490bd7a39f0161d46867b575565b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23721660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf3a9e97b9cb6910b6457146ad74edac061621f06e5ff6481187e69cded45d9`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.12.11
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=c30bb24b7f1e9a19b11b55a546434f74e739bb4c271a3e3a80ff4380d49f7adb
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Wed, 08 Oct 2025 16:25:19 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d403476d77f3c6d174042f0a35c75c77af9283be8ed3f5fdc93ad0cd153034`  
		Last Modified: Thu, 09 Oct 2025 13:06:21 GMT  
		Size: 457.9 KB (457870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6092d968d3728650b0954afdc84c10f1371071183733fce783686ecaefc6253a`  
		Last Modified: Thu, 09 Oct 2025 13:06:22 GMT  
		Size: 14.2 MB (14198360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8039dfde25e07b7f103f0fcfa31027e1711b531a4e0cea894e5f0d3a36c13f`  
		Last Modified: Thu, 09 Oct 2025 13:06:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797700de88c2c456fa2b691aec1bd7b3817eea3fcdd46562cec92a70e9d5c7eb`  
		Last Modified: Thu, 09 Oct 2025 15:47:22 GMT  
		Size: 5.6 MB (5598747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:2e7d4afcb764d9dc5941ed250b05fd7f6c4a346cb2c3dc5f0cf52602558442d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.2 KB (658183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26dfccd9e21d373226833d2f04a6079a3fe21e5acc1662f226b14e34bd91887a`

```dockerfile
```

-	Layers:
	-	`sha256:0100f39815da782c35a281e9b8704acbc2f862702298de30de67555f82dc013c`  
		Last Modified: Thu, 09 Oct 2025 17:18:46 GMT  
		Size: 650.1 KB (650146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a1011c0a1c000e4cf30b5d958ba60a5dabf689be5c7fa7ddb7f2940ab1dcdf0`  
		Last Modified: Thu, 09 Oct 2025 17:18:46 GMT  
		Size: 8.0 KB (8037 bytes)  
		MIME: application/vnd.in-toto+json
