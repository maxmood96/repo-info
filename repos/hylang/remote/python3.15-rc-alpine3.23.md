## `hylang:python3.15-rc-alpine3.23`

```console
$ docker pull hylang@sha256:a231a2729c0b583ea6aa1c2a29b26780a4db5f9d4ca6a9308611d8fb749ebd96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `hylang:python3.15-rc-alpine3.23` - linux; amd64

```console
$ docker pull hylang@sha256:ac4775318ef4e92a5b9002e3c1c37b72a128ebe6ce2304ae171fd20fc4240e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24139683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3066045542717052e6200f8a85c1e1bf750817930db31069502c898bbdeed11`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:02:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 20:02:11 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 22 Jun 2026 20:02:11 GMT
ENV PYTHON_VERSION=3.15.0b2
# Mon, 22 Jun 2026 20:02:11 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Mon, 22 Jun 2026 20:04:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 22 Jun 2026 20:04:38 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 22 Jun 2026 20:04:38 GMT
CMD ["python3"]
# Mon, 22 Jun 2026 20:26:38 GMT
ENV HY_VERSION=1.3.0
# Mon, 22 Jun 2026 20:26:38 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 22 Jun 2026 20:26:38 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 22 Jun 2026 20:26:38 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2810b9d3d15fa4718fe673829fdbe03099c9440442a9b2e7c34ccbb726b97b2`  
		Last Modified: Mon, 22 Jun 2026 20:04:45 GMT  
		Size: 408.7 KB (408746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5528a2abd3649a02ddf053bfa37c39250389a4d9be0d34e8f95e8e700ed89c`  
		Last Modified: Mon, 22 Jun 2026 20:04:45 GMT  
		Size: 14.0 MB (14042122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02a7c7a96ba059d46efeba28cab77406e10a7565edba02374fd9e58d88d9eb2`  
		Last Modified: Mon, 22 Jun 2026 20:04:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6256c3ac8ab718d6bffc7f4aefe2da83dbae6354108f43c84ba24a9739855c1a`  
		Last Modified: Mon, 22 Jun 2026 20:26:44 GMT  
		Size: 5.8 MB (5844147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:cedf8a8bdd61b39de4cf73c682444c16394fcdf858aefdec573eff374befde05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.6 KB (613643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4e38a04ccd189bae099ca1d2510bda627a67e781e2f2dcf30c59130b1b6f42`

```dockerfile
```

-	Layers:
	-	`sha256:1f96d0063fa7f2d0fa9c7cea34e42422edbd74910597175318b87625069bad36`  
		Last Modified: Mon, 22 Jun 2026 20:26:44 GMT  
		Size: 605.6 KB (605568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38ced22e1e65a1c63bfed2a3bcfb680758c0bc2bf97a48563b5eb7b4a1d188d2`  
		Last Modified: Mon, 22 Jun 2026 20:26:43 GMT  
		Size: 8.1 KB (8075 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:f489b5a6a06593936562709b7feac3702cdc8b66e3979b564b3169e35761990b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24556049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afffeefa78ed7b988ea33b296e8c5022f1684f84fdd26bda63f1c5c9aa85b7f9`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:02:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 20:02:41 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 22 Jun 2026 20:02:41 GMT
ENV PYTHON_VERSION=3.15.0b2
# Mon, 22 Jun 2026 20:02:41 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Mon, 22 Jun 2026 20:05:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 22 Jun 2026 20:05:28 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 22 Jun 2026 20:05:28 GMT
CMD ["python3"]
# Mon, 22 Jun 2026 21:01:23 GMT
ENV HY_VERSION=1.3.0
# Mon, 22 Jun 2026 21:01:23 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 22 Jun 2026 21:01:23 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 22 Jun 2026 21:01:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c121f1486a4c6111b37678676fe058c83a1a573ef8d4a171be1a25edef88098`  
		Last Modified: Mon, 22 Jun 2026 20:05:35 GMT  
		Size: 412.5 KB (412454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367435d7c03278e4e460e89d5f98098e9442aeebffcf62d959fa880f5424d9de`  
		Last Modified: Mon, 22 Jun 2026 20:05:35 GMT  
		Size: 14.1 MB (14117259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01286b33141fdcca6099472864a1ded0f0877e708209d64739d7dacc4063d6c`  
		Last Modified: Mon, 22 Jun 2026 20:05:34 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac223604dd60cc0e91ecbbd6f8431297b3cab1085a9f241cfb5f46e89c5bfe70`  
		Last Modified: Mon, 22 Jun 2026 21:01:30 GMT  
		Size: 5.8 MB (5844229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:10f7c230ab291bf2b0af5d9073be2f4ab75f6d9f9203921340ab0d5bf0284bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.2 KB (613152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0751196feb2c7bcb181d52bf534815bb61388f38aaf5773c16a94aa68db2585`

```dockerfile
```

-	Layers:
	-	`sha256:9d0e9c5eeee611c088027e6a2fac168daf7854f8a46ef53d0dc81dabe2742ee5`  
		Last Modified: Mon, 22 Jun 2026 21:01:29 GMT  
		Size: 605.0 KB (604974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a77aa14a7832dffcf4d81531c085d80000353dbf5023b4ee9b63a1b379eb70df`  
		Last Modified: Mon, 22 Jun 2026 21:01:29 GMT  
		Size: 8.2 KB (8178 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-alpine3.23` - linux; riscv64

```console
$ docker pull hylang@sha256:7ca0caf13d201f2d4cb68a5834286065259d140eb2d5eaa9b8e11e8e20fc5720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23979108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e973cdd7f733481876c4b5e292dcd0cba44767df2c099b8fe74ae7ac3daf88`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 22 Jun 2026 19:30:17 GMT
ADD alpine-minirootfs-3.23.5-riscv64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:30:17 GMT
CMD ["/bin/sh"]
# Tue, 23 Jun 2026 14:35:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jun 2026 14:35:39 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 23 Jun 2026 14:35:39 GMT
ENV PYTHON_VERSION=3.15.0b2
# Tue, 23 Jun 2026 14:35:39 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Tue, 23 Jun 2026 15:18:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 23 Jun 2026 15:18:39 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 23 Jun 2026 15:18:39 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 11:26:48 GMT
ENV HY_VERSION=1.3.0
# Wed, 24 Jun 2026 11:26:48 GMT
ENV HYRULE_VERSION=1.1.0
# Wed, 24 Jun 2026 11:26:48 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 24 Jun 2026 11:26:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8a1e5860a6401101356d3688f519ef896539fceeb0e505b24a7224fe7e76fdb1`  
		Last Modified: Mon, 22 Jun 2026 19:30:41 GMT  
		Size: 3.6 MB (3573240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e081e16f7eeed526345a2430e871a74e8d0212efda89a5ac0b222ff6b58309e0`  
		Last Modified: Tue, 23 Jun 2026 15:19:25 GMT  
		Size: 409.4 KB (409391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab7ff07d33d18cb03ea3884f0b7013359e0ef6dea52f93781bd33c6a79d968d`  
		Last Modified: Tue, 23 Jun 2026 15:19:27 GMT  
		Size: 14.2 MB (14151380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d812b7688bce3a99bd9a3c397bf7ae4e0078602aca9b8fde497451ea0eafc942`  
		Last Modified: Tue, 23 Jun 2026 15:19:25 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de82e9dfd373ee2fb6020e0e06791e1e366b98dfec4fbd9c02006459cb28e64`  
		Last Modified: Wed, 24 Jun 2026 11:27:27 GMT  
		Size: 5.8 MB (5844847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:b9e7380b9be24af910a95784d4fa87b0e679b82e72746e2742574a5fd77d7fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.1 KB (613065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149777fd0f66ea20cf4266a91b31e3cdf2122973cee3bf14b80cefd68fedd0a3`

```dockerfile
```

-	Layers:
	-	`sha256:ed45fe37e446fbc6578847fb57b389ee80c295480d9179739bf707fe4fb80ba1`  
		Last Modified: Wed, 24 Jun 2026 11:27:26 GMT  
		Size: 604.9 KB (604947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ff1f010a98da65f03d49dde50a706239adadcd73d65cf926675f8ec3249ca40`  
		Last Modified: Wed, 24 Jun 2026 11:27:25 GMT  
		Size: 8.1 KB (8118 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-alpine3.23` - linux; s390x

```console
$ docker pull hylang@sha256:bbd223ed0656feb7001f001108bba367d3b6223a80e28519b199a6f09c099b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24488145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f075c27f4fdf256b17029a04aca72ca5e2fd40c57806a008fc73f35017a2cd2e`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:16:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 20:16:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 22 Jun 2026 20:16:40 GMT
ENV PYTHON_VERSION=3.15.0b2
# Mon, 22 Jun 2026 20:16:40 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Mon, 22 Jun 2026 20:22:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 22 Jun 2026 20:22:02 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 22 Jun 2026 20:22:02 GMT
CMD ["python3"]
# Mon, 22 Jun 2026 21:57:56 GMT
ENV HY_VERSION=1.3.0
# Mon, 22 Jun 2026 21:57:56 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 22 Jun 2026 21:57:56 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 22 Jun 2026 21:57:56 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daa2e913c517118ce70937eada8ed50954e974f01824ccd943f3c7002098786`  
		Last Modified: Mon, 22 Jun 2026 20:22:13 GMT  
		Size: 410.3 KB (410318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978476651e3cc0f2945c674578024138332a83989832ebf5ec911cc24c627161`  
		Last Modified: Mon, 22 Jun 2026 20:22:13 GMT  
		Size: 14.5 MB (14526115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be08f8e0dc5bce04d60c61d7377ab27f383cab87c035b2086925da7c1025529`  
		Last Modified: Mon, 22 Jun 2026 20:22:13 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d8f87f1cb50d1f8a07c942efb1744de98d328537b5d8fccb1fca1f9902f2be`  
		Last Modified: Mon, 22 Jun 2026 21:58:05 GMT  
		Size: 5.8 MB (5844215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:75236219adcf95dddd328c0690d68a7ad7025525f26cb4cae1d5d7397f28db37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.0 KB (612992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee929ef700bae3bf842a5660f680e322fb603eb4d1972e584cd0219c765e824`

```dockerfile
```

-	Layers:
	-	`sha256:9faf041831a30ef98d373cb966043b18a8b8fe29497ce6e466716fd1bc6c96ae`  
		Last Modified: Mon, 22 Jun 2026 21:58:05 GMT  
		Size: 604.9 KB (604917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:145acfef79db991a684f8b88ebc9d66ad85887b2c1a3f1e20b7b6cfa34a1c6f4`  
		Last Modified: Mon, 22 Jun 2026 21:58:05 GMT  
		Size: 8.1 KB (8075 bytes)  
		MIME: application/vnd.in-toto+json
