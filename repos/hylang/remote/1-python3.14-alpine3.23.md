## `hylang:1-python3.14-alpine3.23`

```console
$ docker pull hylang@sha256:ad4ffdd04dc0ba6f823dc2604b9d5da44cba4d3ea711b6a2a5b34bcdaff5d387
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

### `hylang:1-python3.14-alpine3.23` - linux; amd64

```console
$ docker pull hylang@sha256:ee08441a413dfb128fe2646d5b7232d5ccbf489e49497cd55a3790173a2981b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23477507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba695f66b0e7b05a74f8e3d32bbca399f582c48970e178276e92f9e72303693`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:06:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:06:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 11 May 2026 23:06:55 GMT
ENV PYTHON_VERSION=3.14.5
# Mon, 11 May 2026 23:06:55 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Mon, 11 May 2026 23:09:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 11 May 2026 23:09:35 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 11 May 2026 23:09:35 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:44:41 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:44:41 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:44:41 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:44:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafef4f1a46c8f17ca44cfb33ae79bb07d54ce7abeba8618466a8144cea386c3`  
		Last Modified: Mon, 11 May 2026 23:09:42 GMT  
		Size: 455.5 KB (455502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f1e103f334e724ec9e5cdfa0eb63e35df78ba9c7d642ea67d973671c010416`  
		Last Modified: Mon, 11 May 2026 23:09:42 GMT  
		Size: 13.4 MB (13445937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe5e153acbf7f2a9712301e26d1a8e48447530facbe8b525fe380cb3c948ec9`  
		Last Modified: Mon, 11 May 2026 23:09:42 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd50a971d10cfa137d3d97455069c3af279179ea3cb9174d3d81ff09e57b764`  
		Last Modified: Mon, 08 Jun 2026 22:44:47 GMT  
		Size: 5.7 MB (5711632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:5d0efa3e247b3a96f50e1aff40d0495750f8ca3fb87a5a47b9cef466197888aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.0 KB (638004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666c3122a1aa4b741353e47407f2677524fe73e1b4804abc303d2e58d9bd1a28`

```dockerfile
```

-	Layers:
	-	`sha256:61111d8e8ff3cdaf043d12801da1b86ed13e8ccd0877dbdcb2569e709bf61a52`  
		Last Modified: Mon, 08 Jun 2026 22:44:46 GMT  
		Size: 626.2 KB (626200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d7c1ef9896fdc5527c4866630e7a2d8bf47b0dd659cc39387a21fcc2069e33f`  
		Last Modified: Mon, 08 Jun 2026 22:44:46 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine3.23` - linux; arm variant v6

```console
$ docker pull hylang@sha256:2782d919e2bab501c16bd931438edb421142e93e49c58b853f29db23cd8d46dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22813378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b4474fa2792447d1aae28401e86c9fba68a35c19ba11527b7b3aff9deda75c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:06:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:06:21 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 11 May 2026 23:06:21 GMT
ENV PYTHON_VERSION=3.14.5
# Mon, 11 May 2026 23:06:21 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Mon, 11 May 2026 23:09:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 11 May 2026 23:09:14 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 11 May 2026 23:09:14 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:44:18 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:44:18 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:44:18 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:44:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b31c8219cc16e32a9a5affbec238b090bda18f4a89ff56805be9014b144fce3`  
		Last Modified: Mon, 11 May 2026 23:09:19 GMT  
		Size: 456.3 KB (456340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fbeb122a94ff325372c381bf50733523e8433e8df9b263cdb637339d4ca282`  
		Last Modified: Mon, 11 May 2026 23:09:20 GMT  
		Size: 13.1 MB (13073254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a9955d94a701166a473f83edf4c85a4e8596ca6f8fb82564d1c4088c7a96fb`  
		Last Modified: Mon, 11 May 2026 23:09:19 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8daf303f2c574c7addbb03b3120a36649add94bdbd073ef84e53c8882db6738`  
		Last Modified: Mon, 08 Jun 2026 22:44:22 GMT  
		Size: 5.7 MB (5711672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:f7ed13249cb1981764ba704d39405d149f7bb270e5a34ec42b1a9d201826c672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 KB (11765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c969c152d0768bcb9a949d954499e1f03c7a67d4aca76dbe42eae9aacdf17b79`

```dockerfile
```

-	Layers:
	-	`sha256:4fae07a5cc2c77e2ff032cb10e1cff87689081caac85ad1a6c9c399eb6c9e114`  
		Last Modified: Mon, 08 Jun 2026 22:44:22 GMT  
		Size: 11.8 KB (11765 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine3.23` - linux; arm variant v7

```console
$ docker pull hylang@sha256:370c8c82f62a94bd0555df7037f470444f87708c4136f5bcef9d18218d42bcfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22122383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da56394d58f50dcf45345eedb6725ad83f8b033a6051610d53e3ab0e469ff21`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:09:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:09:41 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 11 May 2026 23:09:41 GMT
ENV PYTHON_VERSION=3.14.5
# Mon, 11 May 2026 23:09:41 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Mon, 11 May 2026 23:12:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 11 May 2026 23:12:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 11 May 2026 23:12:34 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:46:00 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:46:00 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:46:00 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:46:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efff5da5f626860bef337fd8478b7dc3e151f438354b62f996626519bca7138d`  
		Last Modified: Mon, 11 May 2026 23:12:41 GMT  
		Size: 455.5 KB (455459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785d056630910e8ba5242607d8eaca5cab55ca4052ee5a78753df8dd24e48d72`  
		Last Modified: Mon, 11 May 2026 23:12:41 GMT  
		Size: 12.7 MB (12671909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f38fdc275528038680d979566604abbf9d3f78a8a9181e99b9b454022435cf`  
		Last Modified: Mon, 11 May 2026 23:12:41 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b093f5bb25213b1236ad5e249f8fe10be6956c547480d8d84cff5420eac79f`  
		Last Modified: Mon, 08 Jun 2026 22:46:06 GMT  
		Size: 5.7 MB (5711645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:424af294f0d0257003ba1b353f4c4d845d68333cee6c0f668714bf390818df12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.7 KB (640651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5380c8045ba66ac275efa39b38269be192b4902514d8cbd1a74b6f21605a67bd`

```dockerfile
```

-	Layers:
	-	`sha256:5c871bcbadf3740eb0132206a8ca5447e920822ea55e2783cd1984c872f2ed8d`  
		Last Modified: Mon, 08 Jun 2026 22:46:06 GMT  
		Size: 628.7 KB (628672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cabde9fb27be7730970b399b34ce5cd5a08183f9bd47116f8d5154d8d3096df2`  
		Last Modified: Mon, 08 Jun 2026 22:46:06 GMT  
		Size: 12.0 KB (11979 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:24b878a7fb5ed6596764b96a1c258e3b844ab94b009bed208096c6901266eb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23903249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f4f95e6fc4a243409685cbe92665430965f2e5151fb9231c79d1de93b89ba9`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:06:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:06:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 11 May 2026 23:06:45 GMT
ENV PYTHON_VERSION=3.14.5
# Mon, 11 May 2026 23:06:45 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Mon, 11 May 2026 23:09:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 11 May 2026 23:09:19 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 11 May 2026 23:09:19 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:44:50 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:44:50 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:44:50 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:44:50 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8d402a4e0f76b57ba75563229ba99e4445b6d4f37bdbff3121b4d5a5291805`  
		Last Modified: Mon, 11 May 2026 23:09:25 GMT  
		Size: 457.8 KB (457770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c752a20044121659cf133fc3e1b8d42aaf9725f0433f544402f93aca2793d581`  
		Last Modified: Mon, 11 May 2026 23:09:26 GMT  
		Size: 13.5 MB (13533663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46342b95b0c55bda2532a29c88677602e5bc7aba310e0d1467f82ac1ab54f02`  
		Last Modified: Mon, 11 May 2026 23:09:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef75a3c15651f5896fcaa902c86572b54418e16ca2a0585aae32b7dd229af93b`  
		Last Modified: Mon, 08 Jun 2026 22:44:56 GMT  
		Size: 5.7 MB (5711699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:2f3694deffcad1d46fb9ac9d17f18118b857a3257c18af22fe396b13a4987463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.8 KB (637802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ab05ec290de7063438b9dd88fae42a5c7a26585829de10aa875cb8f4d206b54`

```dockerfile
```

-	Layers:
	-	`sha256:6c2e976dec48119a663e4b780577ec6367768d2892cc753bb953c4f883cf7e46`  
		Last Modified: Mon, 08 Jun 2026 22:44:56 GMT  
		Size: 625.8 KB (625750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71831bdb9c9555ad1f4473e2a789ff25b7406be772c4780cf69503290221b2bf`  
		Last Modified: Mon, 08 Jun 2026 22:44:56 GMT  
		Size: 12.1 KB (12052 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine3.23` - linux; 386

```console
$ docker pull hylang@sha256:1b645e23b3bbb224411397138772d47dc328d78b655d9afbedbcdb15fdaf59d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23562542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d13b0b82dcd03c041e4169e82ebf7294ba789bb5d682abc2e3085d7b143e38c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:07:58 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:07:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 11 May 2026 23:07:58 GMT
ENV PYTHON_VERSION=3.14.5
# Mon, 11 May 2026 23:07:58 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Mon, 11 May 2026 23:10:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 11 May 2026 23:10:56 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 11 May 2026 23:10:56 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:46:24 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:46:24 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:46:24 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:46:24 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf643a1d7291abd5f3bd6ef5489e535ce61e63cad1dd08ff3625a7e5cfd1401`  
		Last Modified: Mon, 11 May 2026 23:11:03 GMT  
		Size: 455.9 KB (455928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e789ec44d2796f062b92e284c7c26f91c116941fee5f896d7ce4bb4db106c29`  
		Last Modified: Mon, 11 May 2026 23:11:03 GMT  
		Size: 13.7 MB (13704192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e7f5feec8ad3f07cb13e7c86813bc25d7a192941d732dd65286a69c7cbc650`  
		Last Modified: Mon, 11 May 2026 23:11:03 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4350c7a98245973d7d774c1b44b3a0db299af230b30eddd72b1139fca1f93e49`  
		Last Modified: Mon, 08 Jun 2026 22:46:30 GMT  
		Size: 5.7 MB (5711723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:db7c1814661c914a06a882d6a300f63b2e00a4c2978098f2730cfb3cd1dea30b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.8 KB (637827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3065caac813b9436fda5ecaf08d8f508c0e1693c2d708bd22aea867f42c8f1`

```dockerfile
```

-	Layers:
	-	`sha256:4231012acb9170782e71ad3fe3327d12ca3f911905b171e4f85ee7c963fe1880`  
		Last Modified: Mon, 08 Jun 2026 22:46:30 GMT  
		Size: 626.1 KB (626115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6bedb3ab7be220c319e6af76ac76374c0d695a3fa3f564abd72221e8dac0fd0`  
		Last Modified: Mon, 08 Jun 2026 22:46:29 GMT  
		Size: 11.7 KB (11712 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine3.23` - linux; ppc64le

```console
$ docker pull hylang@sha256:bab0951b2aa15b72e89b5dbda9b2771bddb937f37f34928c48727480fc24390d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 MB (24320494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a7aa5be1bab8f0cd496e4d5b75174380bd3a2bc9ae729fe4b6ede7cb6fd46d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 00:05:42 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:05:42 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 12 May 2026 00:05:42 GMT
ENV PYTHON_VERSION=3.14.5
# Tue, 12 May 2026 00:05:42 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Tue, 12 May 2026 00:09:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 12 May 2026 00:09:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 12 May 2026 00:09:06 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 23:15:05 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 23:15:05 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 23:15:05 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 23:15:05 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba42f71d28c12f39dbf72ef122e75b5d0610be96ee5da3a7c25675d82b55b01`  
		Last Modified: Tue, 12 May 2026 00:09:18 GMT  
		Size: 458.2 KB (458178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74eb4afee91d4e502bd1ed96af0274f0395981c5192729d54dbfa13acabee28`  
		Last Modified: Tue, 12 May 2026 00:09:18 GMT  
		Size: 14.3 MB (14319300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadb0916f0f0010426a80df0d5f0526fbf08a979576cb571c140d0bfedc6ef01`  
		Last Modified: Tue, 12 May 2026 00:09:18 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86d839771448f9c5abc37a23d09edbb22fd7564b237057d6f0bf196f276ffdb`  
		Last Modified: Mon, 08 Jun 2026 23:15:17 GMT  
		Size: 5.7 MB (5711839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:09eb00caa86dbefa5b0f08531de31b11ef9cd8b20b3fc10e6e6dd5b592460708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.6 KB (637575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9d82f50cdd0369b91e40545c8759620f496000c60c83a7133ed69f3071172f`

```dockerfile
```

-	Layers:
	-	`sha256:b3f98651547105a2759bbe299e45786cd9cf056b6d19e647adee982e7b5d1c5e`  
		Last Modified: Mon, 08 Jun 2026 23:15:17 GMT  
		Size: 625.7 KB (625655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f57c3cb18c2a9b83b1f7fa7a683914e65ffed48178bb1b282742a1a7314c6457`  
		Last Modified: Mon, 08 Jun 2026 23:15:17 GMT  
		Size: 11.9 KB (11920 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine3.23` - linux; riscv64

```console
$ docker pull hylang@sha256:d8f3940efeda9e982a9b05559ae09f89f8ce463d6324ce5af1afa170f643ab1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23328782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9c3f294561e546b53674164994cb69b7c08e65a1184a463737911df715f8ef`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 13 May 2026 19:23:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2026 19:23:31 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 13 May 2026 19:23:31 GMT
ENV PYTHON_VERSION=3.14.5
# Wed, 13 May 2026 19:23:31 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Fri, 15 May 2026 14:37:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 15 May 2026 14:37:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 15 May 2026 14:37:11 GMT
CMD ["python3"]
# Thu, 28 May 2026 12:02:36 GMT
ENV HY_VERSION=1.3.0
# Thu, 28 May 2026 12:02:36 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 28 May 2026 12:02:36 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 28 May 2026 12:02:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d4c57e2da2e794667e1c6895203762933331ab57e4f6193d2f47897fe36f7b`  
		Last Modified: Fri, 15 May 2026 14:37:56 GMT  
		Size: 455.8 KB (455836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d778d6d2ad9bf44e6bd225df32813030e4bf4caa84f0233fc093cccbb2b112`  
		Last Modified: Fri, 15 May 2026 14:37:57 GMT  
		Size: 13.6 MB (13576055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6967c4c5212bec044ac9582d45f586f623b0a4de178eb4b4a7b14b585f59f60`  
		Last Modified: Fri, 15 May 2026 14:37:55 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e06cce999519054b2084f7ea8cc58aed83a26a3a8aed49b682f530d321cf8`  
		Last Modified: Thu, 28 May 2026 12:03:15 GMT  
		Size: 5.7 MB (5708979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:f1e15e19d91b6151b1c6920218bd8b06fedbd01f4dc31852624e1b6197e64500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.6 KB (637571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ab071cd7f9f073b2f4b160cd4b497da92b55c04ca8d364d722b3c25e115b1d`

```dockerfile
```

-	Layers:
	-	`sha256:d45624197964805e2ad84d722fd511ff82a7f584e71ecbe410048cb491981294`  
		Last Modified: Thu, 28 May 2026 12:03:14 GMT  
		Size: 625.7 KB (625651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfea4a8cf273ee8ae71bdeb7cafbc26ee8dff814636fa34e01d09e2d0e82f331`  
		Last Modified: Thu, 28 May 2026 12:03:14 GMT  
		Size: 11.9 KB (11920 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine3.23` - linux; s390x

```console
$ docker pull hylang@sha256:d3a3cb2cc110dfe8dcaccd55d5f0f7f81c86582b1079c57b1565f103a20bd387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23822871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a8c3e77a7106b005be5a3137c306ee66918992f83216d4af5238fdff3fe1bb`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:13:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:13:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 11 May 2026 23:13:55 GMT
ENV PYTHON_VERSION=3.14.5
# Mon, 11 May 2026 23:13:55 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Mon, 11 May 2026 23:17:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 11 May 2026 23:17:57 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 11 May 2026 23:17:57 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:54:40 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:54:40 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:54:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:54:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c9e8098c99227eb052139a43abb91c848558b636dc8749cf6b4b37554b6a99`  
		Last Modified: Mon, 11 May 2026 23:18:08 GMT  
		Size: 456.5 KB (456477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5b4eb1f94cf9aa27b68a64ead7ef62f0fb13cfdc3764e38f7fa2f147b657f1`  
		Last Modified: Mon, 11 May 2026 23:18:08 GMT  
		Size: 13.9 MB (13927933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50199799189f74f646c61d1fab74af92599dce801e02f26dc5cefcebb7ded86`  
		Last Modified: Mon, 11 May 2026 23:18:08 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7991e949b91c48b5f89b1e2ef2234eca227034b94a8c2b8a7493982f32957dc`  
		Last Modified: Mon, 08 Jun 2026 22:54:52 GMT  
		Size: 5.7 MB (5711680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:fbccf0b4149d5924eeaa2018b2a95116cf2ee9d3159492f10d4e7b57378e5b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.4 KB (637353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e94412adcc90069c109035c48bec59afe4164dc7be534d98d601feed59c8d93`

```dockerfile
```

-	Layers:
	-	`sha256:a37017187d845db799a7ab025a60f7496c741bc37e9c02d6026f04f79e74c873`  
		Last Modified: Mon, 08 Jun 2026 22:54:52 GMT  
		Size: 625.5 KB (625549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1657964b7e116e8c5da7c7714ba7821d0b91b92d68253d627fbb1c20c347fd87`  
		Last Modified: Mon, 08 Jun 2026 22:54:52 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json
