## `hylang:python3.14-alpine3.22`

```console
$ docker pull hylang@sha256:958f1bace9716664ab8330a33971157407b8e941395614d4dba299cb5a817145
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

### `hylang:python3.14-alpine3.22` - linux; amd64

```console
$ docker pull hylang@sha256:7dbd137854c5f3169a6159db2ad62be65d4104f56917105ff1969969d65cb5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23225328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f23319f8393f1d629d3d78688252748e25e9b10ade50d52382a44c2f4a6c3b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:30:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:30:57 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:30:57 GMT
ENV PYTHON_VERSION=3.14.2
# Mon, 08 Dec 2025 20:30:57 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Mon, 08 Dec 2025 20:33:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:33:33 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:33:33 GMT
CMD ["python3"]
# Wed, 14 Jan 2026 21:59:21 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 21:59:21 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 21:59:21 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 14 Jan 2026 21:59:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d886d4dec287c8ee5e1675000393880605d2bc469f506c3a33d86e6205edb2`  
		Last Modified: Mon, 08 Dec 2025 20:33:41 GMT  
		Size: 456.9 KB (456925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ec91ddee74965879f5f56c96e53be6112e127a963606744878c41904983177`  
		Last Modified: Mon, 08 Dec 2025 20:33:41 GMT  
		Size: 13.3 MB (13301552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2e4e18032acab8a1e953b35cae787b0d28a9d984b3ebd3d946fa5588933e02`  
		Last Modified: Mon, 08 Dec 2025 20:33:40 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b9860a5b388ff0cad9be4ec1f6fea858c00dbfbece9e9d29f2470abec3d9b8`  
		Last Modified: Wed, 14 Jan 2026 21:59:27 GMT  
		Size: 5.7 MB (5664152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:fb90f4be7e721b2cdf6686c6256ca33de4f3bc585cfa9a632cbf8fbfe7063720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.9 KB (634916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0716c76af4de497762719e5023c1ebe6e96c5269848abe985bca1b7c7fb7bea2`

```dockerfile
```

-	Layers:
	-	`sha256:c43ec21dddd39b75cac6076252552ea291eddf2600e1b6a528c171a38d102be8`  
		Last Modified: Thu, 15 Jan 2026 00:18:38 GMT  
		Size: 625.6 KB (625632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb02efb5485a9d9765807f5720046a71acfe7ba0fab213c875eaf70fd0db1372`  
		Last Modified: Thu, 15 Jan 2026 00:18:39 GMT  
		Size: 9.3 KB (9284 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.22` - linux; arm variant v6

```console
$ docker pull hylang@sha256:a29150b76df8f8d0e43118cc73b097c7c7cc7c9e9658862df0326861f1a2bbf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22515228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80a194e501c633bd2e58519ec0497d3d710d09851f92527c9d48ce6e502a5ea`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:37:28 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:37:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:37:28 GMT
ENV PYTHON_VERSION=3.14.2
# Mon, 08 Dec 2025 20:37:28 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Mon, 08 Dec 2025 20:40:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:40:09 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:40:09 GMT
CMD ["python3"]
# Wed, 14 Jan 2026 21:59:46 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 21:59:46 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 21:59:46 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 14 Jan 2026 21:59:46 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e037e5611005d82eeea55d2477da9bcc581c6c5ea780ebf1ea2f4080e284574d`  
		Last Modified: Mon, 08 Dec 2025 20:40:14 GMT  
		Size: 457.7 KB (457737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50a1afe201fd2bf27c454834ce1b82d5d87a1225e68b90126922a12372031cd`  
		Last Modified: Mon, 08 Dec 2025 20:40:21 GMT  
		Size: 12.9 MB (12889069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b675ecf9cc5caec68a31816eea3df4df321b903f008d291cf7bfdadeaa6cd630`  
		Last Modified: Mon, 08 Dec 2025 20:40:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befc0c7e08302c90c8a94ac41fd3d98eb1de55b3895ab5def46641d2bdf6f32f`  
		Last Modified: Wed, 14 Jan 2026 21:59:55 GMT  
		Size: 5.7 MB (5664095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:21e6d87814a31105d74ab4bca5b7771bd0003c87d8ae8bbb194951b6871bb060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72d0451973350c9906901a4d320b50258f0bfd209e52197f20cab2394e03932`

```dockerfile
```

-	Layers:
	-	`sha256:ce81a49dda32261eed6522ce06c831e3a977efe869c78e929fa7860bc43de7be`  
		Last Modified: Thu, 15 Jan 2026 00:18:42 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.22` - linux; arm variant v7

```console
$ docker pull hylang@sha256:500f0a1012027404de098b7f6aa9ac5d16a5d10142bc94b1d4857f13cbe887b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21849533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269a1b99861cfc22629f8caf510c0bd68be08b55354df63c2e53d3fcb7862222`
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
ENV PYTHON_VERSION=3.14.2
# Mon, 08 Dec 2025 20:26:33 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Mon, 08 Dec 2025 20:29:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:29:21 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:29:21 GMT
CMD ["python3"]
# Wed, 14 Jan 2026 21:58:57 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 21:58:57 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 21:58:57 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 14 Jan 2026 21:58:57 GMT
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
	-	`sha256:3e93650cdcdc97d7cfaa56dc124cbc4fe237ce893159367e9679f779f8f0a5ab`  
		Last Modified: Mon, 08 Dec 2025 20:29:34 GMT  
		Size: 12.5 MB (12506742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6db2b4f3cd94b1801ccf1db066ad55b1431cc9e0d7c07258e7d990e6c0af27`  
		Last Modified: Mon, 08 Dec 2025 20:29:33 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245d14c96cd43ba80abe83c839110a938d681467f67f33cec0e3b84df56714d2`  
		Last Modified: Wed, 14 Jan 2026 21:59:09 GMT  
		Size: 5.7 MB (5664055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:6ac3cc3132a8bd903925166c453e0162553183a25845a08bfb9854160c27c327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.1 KB (638085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2debe76c964c1b515b6f609ccfc350481119e1c4592a157ab091db92187af1e`

```dockerfile
```

-	Layers:
	-	`sha256:ca325c3e50617aa2eaacb1371b6c771d7b21419493b3c3a93acb3425295ba48a`  
		Last Modified: Thu, 15 Jan 2026 00:18:46 GMT  
		Size: 628.7 KB (628690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e97e08526da72336b86b21604777803af3fa88c58429f13d87e8c91e4d2d7090`  
		Last Modified: Wed, 14 Jan 2026 21:59:03 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:0d453739a78fb876f50e7393ea72c1eeb1e042c4961962183143b537f7108103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23541763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0d5b4a5e98dd3605cd0bb32a779d56b742c88f2770b069375f62b97f6ed530`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:09:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:09:34 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:09:34 GMT
ENV PYTHON_VERSION=3.14.2
# Mon, 08 Dec 2025 20:09:34 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Mon, 08 Dec 2025 20:11:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:11:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:11:59 GMT
CMD ["python3"]
# Wed, 14 Jan 2026 21:58:54 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 21:58:54 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 21:58:54 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 14 Jan 2026 21:58:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045c6b1868f769e10fee9ae87f0d077088865aa45101ec1bcfe7a1b6cda54424`  
		Last Modified: Mon, 08 Dec 2025 20:55:26 GMT  
		Size: 459.0 KB (459027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6a171ca6202d287867ec84ab3f7a9ec217613ea6fc6c829efecad88a644b4b`  
		Last Modified: Mon, 08 Dec 2025 20:12:07 GMT  
		Size: 13.3 MB (13280414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1241d7c5aa9287178de98cf0b02be4d0c58b903358e8a63b44243a64e22a457a`  
		Last Modified: Mon, 08 Dec 2025 20:55:24 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ba740964af5252137edeee9b623710b211fd84899fd750e3dab3f1595f6f7c`  
		Last Modified: Wed, 14 Jan 2026 21:59:07 GMT  
		Size: 5.7 MB (5664006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:14fd6cab0bc7403e40f0ff787ad8c055ce0f7981f7144388bca12189c6f838b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.2 KB (635172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f466b7d68749f23b194b07eb258282ae99c0b903a0249e5d70cb34b03ecd55`

```dockerfile
```

-	Layers:
	-	`sha256:8b4a4ebca2ee2703a2a592baa8a65a2c23b72593d7ccd575aabff9c72b913585`  
		Last Modified: Wed, 14 Jan 2026 21:59:00 GMT  
		Size: 625.7 KB (625736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bebbdb4542cf24067b07af28304f84deb74a98b7f15359692610944a0a8e8a05`  
		Last Modified: Thu, 15 Jan 2026 00:18:51 GMT  
		Size: 9.4 KB (9436 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.22` - linux; 386

```console
$ docker pull hylang@sha256:7c849e021fd1c056800f1164613e6da96b57e18d748fb5fca17910857c575eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23319370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60dbbf40cb52c529f6265fc11ccc603124a2ff18cf42bea03c3a91b8894861c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:17:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:17:34 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:17:34 GMT
ENV PYTHON_VERSION=3.14.2
# Mon, 08 Dec 2025 20:17:34 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Mon, 08 Dec 2025 20:20:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:20:12 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:20:12 GMT
CMD ["python3"]
# Wed, 14 Jan 2026 22:00:05 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 22:00:05 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 22:00:05 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 14 Jan 2026 22:00:05 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Sun, 07 Dec 2025 14:06:47 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21dfdfcdacb7ae5627d2f81dc35ab13a5cbf2557c02da53b9d5f274814d8e6af`  
		Last Modified: Mon, 08 Dec 2025 20:20:25 GMT  
		Size: 457.4 KB (457375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f2f98be4addc2e7c02c2c930662325e3eb6b48613066cfe9f93cba1fb12b69`  
		Last Modified: Mon, 08 Dec 2025 20:20:26 GMT  
		Size: 13.6 MB (13578694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f68324fd33d2fa3f7dac5b8f6e3f7cd18224ed2b5fbffeaf2c2d56ee148e09`  
		Last Modified: Mon, 08 Dec 2025 20:20:24 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7f69141ac34d8845ab3ce8c96e86841c37bac7b985c4929e645086291a33cb`  
		Last Modified: Wed, 14 Jan 2026 22:00:12 GMT  
		Size: 5.7 MB (5664121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:78ab890848c60a7fc895042bd06c0b2be9666dec17bd9fab5715b2ca5b5157ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.8 KB (634819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0f09a43ba394b5f49aee066e0cf84d69ae09278939f70781325155e5387442`

```dockerfile
```

-	Layers:
	-	`sha256:b418ea2caff9fb87635dad8bd068f47aaaf985605f76f084cd52fc92b66baf32`  
		Last Modified: Wed, 14 Jan 2026 22:00:12 GMT  
		Size: 625.6 KB (625587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3505015a5bc582594dc37196bc6bcdb02a1b7b561dbd25e547ab5734a2c2bc`  
		Last Modified: Thu, 15 Jan 2026 00:18:55 GMT  
		Size: 9.2 KB (9232 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.22` - linux; ppc64le

```console
$ docker pull hylang@sha256:39c6c2e3fd971151036805810a96351c0c376d77f34d645799b125c0104343ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23936055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e30e17257a6556ad38372b136140e843bde5d2149a2b5123cadca33132874dd`
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
ENV PYTHON_VERSION=3.14.2
# Mon, 08 Dec 2025 21:04:57 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Mon, 08 Dec 2025 21:08:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 21:08:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 21:08:05 GMT
CMD ["python3"]
# Wed, 14 Jan 2026 21:57:25 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 21:57:25 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 21:57:25 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 14 Jan 2026 21:57:25 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5562f27fade7a45fdd6b307b93ea9aea9528474a73ae82b42116409f5faa697e`  
		Last Modified: Mon, 08 Dec 2025 21:08:18 GMT  
		Size: 459.4 KB (459424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267c51e8096c6e2805a913447574a18e4b77d5bc6ef75f72c6141eea9976bfd3`  
		Last Modified: Mon, 08 Dec 2025 21:08:27 GMT  
		Size: 14.1 MB (14079935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe554d6cc15455443ae678809a3c99506fb1aa01f78bf5cfbefc4cf6323b2c7d`  
		Last Modified: Mon, 08 Dec 2025 21:08:18 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a37b0110521c13ffe3fd4685c753b700e6067ebef6e764baa53d5dc98f8b79`  
		Last Modified: Wed, 14 Jan 2026 21:57:46 GMT  
		Size: 5.7 MB (5664206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:bf062b75b4a4d3bb79244d6c0ee56f6960a716a0137ebcd70f9a952c1f35d67a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.1 KB (633091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4825378067e0227b69a4d7adc251e45b64e2112f1b0594db6a554e4b08ab9e3`

```dockerfile
```

-	Layers:
	-	`sha256:6a2858816ef3410b82a61645805e1255c38230a9da76558dff38046d9ee82d77`  
		Last Modified: Thu, 15 Jan 2026 00:18:58 GMT  
		Size: 623.7 KB (623739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c810a4721ce70e3838be7fc10c6351fe1673b04046fbf80525f2e4ba2cbeff9e`  
		Last Modified: Thu, 15 Jan 2026 00:18:59 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.22` - linux; riscv64

```console
$ docker pull hylang@sha256:547eab3a72b01910c985e9b056b6543b73edc37ee7380f0b9c89d5cb97998427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23095281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8512c49b0571d0d674add57b536703ebeae536ff5093618be6e82e59f2e0eb`
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
ENV PYTHON_VERSION=3.14.2
# Fri, 21 Nov 2025 02:32:45 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Tue, 09 Dec 2025 00:23:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 09 Dec 2025 00:23:24 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 09 Dec 2025 00:23:24 GMT
CMD ["python3"]
# Mon, 19 Jan 2026 09:22:02 GMT
ENV HY_VERSION=1.2.0
# Mon, 19 Jan 2026 09:22:02 GMT
ENV HYRULE_VERSION=1.0.1
# Mon, 19 Jan 2026 09:22:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 19 Jan 2026 09:22:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Sun, 07 Dec 2025 22:49:04 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2877bb53774363add4a89387f6600996a5058bff9f65b88b5e8eee6ca3040264`  
		Last Modified: Tue, 20 Jan 2026 10:08:19 GMT  
		Size: 457.3 KB (457273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f2322d67e1cb2b8f747c8c61b52c8566af936e8efc292af2d981442cd673f`  
		Last Modified: Tue, 09 Dec 2025 00:24:19 GMT  
		Size: 13.5 MB (13457482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a113a5d21f58b29543201e900d4daed9b69978aff012bcef64c9e95aaf0f15a`  
		Last Modified: Tue, 09 Dec 2025 00:24:19 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80ba6fbac34f044f5f73c4c5926f2dc7599ba45be3dae8ab449fb6a07ea44a8`  
		Last Modified: Mon, 19 Jan 2026 09:22:48 GMT  
		Size: 5.7 MB (5665035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:77aab6e5961708c6c70abc0ea5d3355d5abc401cc17af967dfa8ad6a8c88d030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.1 KB (633087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c7a878a8d044609b7698a44c93a95f326f4178aebaa9877482853f7eb09fc5`

```dockerfile
```

-	Layers:
	-	`sha256:cada199c281a60058cdea729f1c203f5383a337811518b3b59c3d7a751a64c21`  
		Last Modified: Mon, 19 Jan 2026 12:17:50 GMT  
		Size: 623.7 KB (623735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207b6def19d6f3ed4f8b9c3b6025e68b066dc29352c616fbb235ab6efc34f9f1`  
		Last Modified: Mon, 19 Jan 2026 09:22:41 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-alpine3.22` - linux; s390x

```console
$ docker pull hylang@sha256:fc8277841e1ff0164812e22e513063955d0aa12c759bd9cbd19d562e57ec3e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23573047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe15afafd5b0ce19f762f825fd30535f6f07cb8574f3ab639062428823ca6f6c`
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
ENV PYTHON_VERSION=3.14.2
# Mon, 08 Dec 2025 20:21:13 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Mon, 08 Dec 2025 20:26:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:26:02 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:26:02 GMT
CMD ["python3"]
# Wed, 14 Jan 2026 23:01:13 GMT
ENV HY_VERSION=1.2.0
# Wed, 14 Jan 2026 23:01:13 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 14 Jan 2026 23:01:13 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 14 Jan 2026 23:01:13 GMT
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
	-	`sha256:e46766f6f7223f4db0eb8fe05514f9751b63de4a3756f8b6c4187bb65acda6f2`  
		Last Modified: Mon, 08 Dec 2025 20:26:12 GMT  
		Size: 13.8 MB (13801561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ced4b3527cbd48e469c1245fa240da9b6595cc033888ebb3023b374f4a15ac`  
		Last Modified: Mon, 08 Dec 2025 20:32:55 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a836314a800e9afb50078ee123acd96b8b42ad9ee260ba7cb289c386fe24b91`  
		Last Modified: Wed, 14 Jan 2026 23:01:24 GMT  
		Size: 5.7 MB (5664077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:a1f956475fa4cb1547cd50ada5f1e2e2ed07880cfd45d565634420baa45d9184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.0 KB (632965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec986081dbf7f470fc63c23660ad41f65a13819b7e391356d60c6a06e3ea0241`

```dockerfile
```

-	Layers:
	-	`sha256:28e77e805e194239b16bf54da56c8778b57d861f5d8011c5b7bfad5f7a2fbbe1`  
		Last Modified: Thu, 15 Jan 2026 00:19:06 GMT  
		Size: 623.7 KB (623681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e787606a259df7bb7346d8d752c0d9c1661193de7f1fc62ad57ed0a71afe1761`  
		Last Modified: Thu, 15 Jan 2026 00:19:07 GMT  
		Size: 9.3 KB (9284 bytes)  
		MIME: application/vnd.in-toto+json
