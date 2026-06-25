## `hylang:python3.15-rc-alpine3.24`

```console
$ docker pull hylang@sha256:f29adf4703547d8c9e207cc21ff10e7cf977ff714c8a267b225c9958dfc28eee
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

### `hylang:python3.15-rc-alpine3.24` - linux; amd64

```console
$ docker pull hylang@sha256:8a1b928cd9bdc721dfc42bc1a9ea66ccdd43afef80ce2e584ad0054d8e3a70d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24173422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9aba8c70168ea0dc607926155d20aad4a8747ef5dc419c915860a05a93acc8`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2026 01:25:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 01:25:57 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 25 Jun 2026 01:25:57 GMT
ENV PYTHON_VERSION=3.15.0b3
# Thu, 25 Jun 2026 01:25:57 GMT
ENV PYTHON_SHA256=6a935ae234a67e6549894373b0cfeb8361182d03b21442328ae9598ab7422127
# Thu, 25 Jun 2026 01:28:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 25 Jun 2026 01:28:35 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 25 Jun 2026 01:28:35 GMT
CMD ["python3"]
# Thu, 25 Jun 2026 02:14:28 GMT
ENV HY_VERSION=1.3.0
# Thu, 25 Jun 2026 02:14:28 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 25 Jun 2026 02:14:28 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 25 Jun 2026 02:14:28 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ac0bd2803b7984ac74555cc60b0df09969982d295dbec2e993388c15f61297`  
		Last Modified: Thu, 25 Jun 2026 01:28:42 GMT  
		Size: 408.8 KB (408750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25b4cedf1a7f363b420e89e53e7772c5966364bea00f6bc8553e0ee0508cad9`  
		Last Modified: Thu, 25 Jun 2026 01:28:42 GMT  
		Size: 14.1 MB (14072433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46642124c087b4a5ac65869ea3dd56f6e679a8416cad58aabaff2780f38641e7`  
		Last Modified: Thu, 25 Jun 2026 01:28:42 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a790a9b9263cd2672f294486693db702a9bceba4a1cd1eef8d7c3cb286a3d52`  
		Last Modified: Thu, 25 Jun 2026 02:14:34 GMT  
		Size: 5.8 MB (5845599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-alpine3.24` - unknown; unknown

```console
$ docker pull hylang@sha256:a60219402e129817b76355b057227a83b5235eff7a4d640a6260b50d3c43f547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.3 KB (616261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea579d960c8036eb3c6d77cd49fd61fea31b3f2dab985296432046dc06b9728`

```dockerfile
```

-	Layers:
	-	`sha256:976d2684ece45788f7f7cb047ac60eabcd7501154d142df81ae7a6c8ce4a2ea5`  
		Last Modified: Thu, 25 Jun 2026 02:14:34 GMT  
		Size: 606.9 KB (606858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45524db2ca511bc1e89aba7b62937335e97c6adb5ce9f6989f98504cd2a37de2`  
		Last Modified: Thu, 25 Jun 2026 02:14:34 GMT  
		Size: 9.4 KB (9403 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:136b39398857f470c198428ec8c510fd51aeca1ba39f7f7ad4ba990e42896ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24584456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0f7692e8413406ab71223293c6a3cda1454f84a2aeeb578d1eff76a13e714f`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2026 01:27:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 01:27:02 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 25 Jun 2026 01:27:02 GMT
ENV PYTHON_VERSION=3.15.0b3
# Thu, 25 Jun 2026 01:27:02 GMT
ENV PYTHON_SHA256=6a935ae234a67e6549894373b0cfeb8361182d03b21442328ae9598ab7422127
# Thu, 25 Jun 2026 01:29:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 25 Jun 2026 01:29:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 25 Jun 2026 01:29:47 GMT
CMD ["python3"]
# Thu, 25 Jun 2026 02:14:09 GMT
ENV HY_VERSION=1.3.0
# Thu, 25 Jun 2026 02:14:09 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 25 Jun 2026 02:14:09 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 25 Jun 2026 02:14:09 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e28a72124ab45d5425e3efd5021e6b2dc08df3d4c7ca82e8dd84aab0e38ed1e`  
		Last Modified: Thu, 25 Jun 2026 01:29:53 GMT  
		Size: 412.5 KB (412453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18623808a712d3ba39b10d9a3b4963b94d70bdb3618757611881ad2ef61a41a`  
		Last Modified: Thu, 25 Jun 2026 01:29:54 GMT  
		Size: 14.1 MB (14143095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff57eb41bb34ea233fdfa5114240cb21c97d14e94e679253ba7efb8a159529d9`  
		Last Modified: Thu, 25 Jun 2026 01:29:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1af65d4735e06adc5c542713da6334a27f760253d45bef2d660d9bed1ee812`  
		Last Modified: Thu, 25 Jun 2026 02:14:16 GMT  
		Size: 5.8 MB (5845624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-alpine3.24` - unknown; unknown

```console
$ docker pull hylang@sha256:39c8846bdc4010e20ea9d3c94ced55c0353a3ff94554fc8067442c7fbaac047e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.9 KB (615867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872cb86dc9e64ac5aaf58e6ec6801bb0a092d7e748d273b939943583c514160a`

```dockerfile
```

-	Layers:
	-	`sha256:76ad04ab09da2b9cb13bb1d21de7dca57841110c57a330f0866dd32034a28142`  
		Last Modified: Thu, 25 Jun 2026 02:14:16 GMT  
		Size: 606.3 KB (606312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7df928b9060416b12d063eb4b31834247489e42287797be3840537fbcbf61447`  
		Last Modified: Thu, 25 Jun 2026 02:14:15 GMT  
		Size: 9.6 KB (9555 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-alpine3.24` - linux; riscv64

```console
$ docker pull hylang@sha256:23e79ff0100ec33a7d7eaa3502b6db1681740cb5a9f093fca9c3256e6a03fc80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (24002378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57e7d2075750ce7ba19be49d79222cab51af423d41a3cfc10227eb227f15ce3`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Thu, 18 Jun 2026 07:41:18 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jun 2026 07:41:18 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 18 Jun 2026 07:41:18 GMT
ENV PYTHON_VERSION=3.15.0b2
# Thu, 18 Jun 2026 07:41:18 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Thu, 18 Jun 2026 08:25:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 18 Jun 2026 08:25:32 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 18 Jun 2026 08:25:32 GMT
CMD ["python3"]
# Fri, 19 Jun 2026 06:39:07 GMT
ENV HY_VERSION=1.3.0
# Fri, 19 Jun 2026 06:39:07 GMT
ENV HYRULE_VERSION=1.1.0
# Fri, 19 Jun 2026 06:39:07 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 19 Jun 2026 06:39:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719f07c5695780a29e6e3100cb79cefaf3d7c807b13c5be3e805b5e8709f33a8`  
		Last Modified: Thu, 18 Jun 2026 08:26:19 GMT  
		Size: 409.4 KB (409412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6562e4a5134227fd6b0cb7baa6a14bba1418f8d4d14953f5884abe2d2ca5c1b9`  
		Last Modified: Thu, 18 Jun 2026 08:26:21 GMT  
		Size: 14.2 MB (14173451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068324945e22c5297b77396c8b843b8d219140e5db6ff7989bfa99e328c7d1c6`  
		Last Modified: Thu, 18 Jun 2026 08:26:19 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886ac1f9284e15dbf64770016398036ab9c327c56d8301af16a26c800d7e097e`  
		Last Modified: Fri, 19 Jun 2026 06:39:47 GMT  
		Size: 5.8 MB (5844906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-alpine3.24` - unknown; unknown

```console
$ docker pull hylang@sha256:ab2fa688d0372e8e73a8c0d65be8ad811c95c707aa181227913966eeb7466b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.7 KB (615724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6d342461d5149db5227a49c184e512a7247099fbbf3b0b29bf3fc3a928e90a`

```dockerfile
```

-	Layers:
	-	`sha256:295d7dae047be134c89b2119cbb9feb9ca889cd6e85fc2362ed0ad6b8d614631`  
		Last Modified: Fri, 19 Jun 2026 06:39:46 GMT  
		Size: 606.3 KB (606253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74f1957c950e37610e3adea9b7476bbb154ce72600e90f183f8cdb08f95eb923`  
		Last Modified: Fri, 19 Jun 2026 06:39:46 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-alpine3.24` - linux; s390x

```console
$ docker pull hylang@sha256:5f5c4a88918d00e98a87717a6ea74610652c40bed1d4c16353e2684b8ac0dd3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24517925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d3ff52ba3dc0ede34ca283f5d8c0fb939f29feff837463ec97b85aadde4c60`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2026 01:56:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 01:56:39 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 25 Jun 2026 01:56:39 GMT
ENV PYTHON_VERSION=3.15.0b3
# Thu, 25 Jun 2026 01:56:39 GMT
ENV PYTHON_SHA256=6a935ae234a67e6549894373b0cfeb8361182d03b21442328ae9598ab7422127
# Thu, 25 Jun 2026 02:02:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 25 Jun 2026 02:02:10 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 25 Jun 2026 02:02:10 GMT
CMD ["python3"]
# Thu, 25 Jun 2026 02:21:10 GMT
ENV HY_VERSION=1.3.0
# Thu, 25 Jun 2026 02:21:10 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 25 Jun 2026 02:21:10 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 25 Jun 2026 02:21:10 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a233cecb851878333aad200cd950b02fac0bf8d4ecdc222ba5f6ddc1acf0ae05`  
		Last Modified: Thu, 25 Jun 2026 02:02:21 GMT  
		Size: 410.3 KB (410276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620d7427731c94ba5104051596cf9f43969cd3dc404503aaf5028534edce5407`  
		Last Modified: Thu, 25 Jun 2026 02:02:21 GMT  
		Size: 14.6 MB (14552439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb3362cc1aa4233785f510696f1bd23a556b0555f7fb5f015b8c16b8bb8c643`  
		Last Modified: Thu, 25 Jun 2026 02:02:21 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9fbf687da75b98f9abd3372eef5a2c9a32c92a70bc08fb9e0e156948e74b65`  
		Last Modified: Thu, 25 Jun 2026 02:21:20 GMT  
		Size: 5.8 MB (5845642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-alpine3.24` - unknown; unknown

```console
$ docker pull hylang@sha256:d45af6ca1d4423ab7f511684d9eb12f149c1405b46b42d3703db5a4c1db14fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.6 KB (615609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c061d08a35e7dd6dafbe017c0f46d3d15fa1367233fc9c16ae5836cb952fafdd`

```dockerfile
```

-	Layers:
	-	`sha256:c4f3646469eea9c56ffe1c5984357ecf2d8741e0af67b98da0dea21b24035d21`  
		Last Modified: Thu, 25 Jun 2026 02:21:20 GMT  
		Size: 606.2 KB (606207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1c97fa51e810140788b7e50e6135846f9b67ae2d3316aedf56d9d48e0f28280`  
		Last Modified: Thu, 25 Jun 2026 02:21:20 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json
