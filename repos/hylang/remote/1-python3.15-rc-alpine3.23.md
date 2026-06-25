## `hylang:1-python3.15-rc-alpine3.23`

```console
$ docker pull hylang@sha256:019b82f371a1e0e6df41f30c871ad7aae5ea20667ee96c26c76e7137017c72a5
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

### `hylang:1-python3.15-rc-alpine3.23` - linux; amd64

```console
$ docker pull hylang@sha256:17e3a7537a595ca2c797c4d8921a7aff691dc2c6cdc7fabb4831b15bda8ab4cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24152039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf41127f896df0b1785104b759f32b7a7a8e9b703c984580d34dd320bf3cec2`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2026 01:26:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 01:26:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 25 Jun 2026 01:26:19 GMT
ENV PYTHON_VERSION=3.15.0b3
# Thu, 25 Jun 2026 01:26:19 GMT
ENV PYTHON_SHA256=6a935ae234a67e6549894373b0cfeb8361182d03b21442328ae9598ab7422127
# Thu, 25 Jun 2026 01:29:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 25 Jun 2026 01:29:00 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 25 Jun 2026 01:29:00 GMT
CMD ["python3"]
# Thu, 25 Jun 2026 02:14:32 GMT
ENV HY_VERSION=1.3.0
# Thu, 25 Jun 2026 02:14:32 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 25 Jun 2026 02:14:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 25 Jun 2026 02:14:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cae8bde6538b444eeb1d4835b7749ffd5f960f31e6d3115328a0ccff616ba1`  
		Last Modified: Thu, 25 Jun 2026 01:29:06 GMT  
		Size: 408.7 KB (408737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df20713b60cc91755801b5f27258d255069c882be765554080f3262580361b38`  
		Last Modified: Thu, 25 Jun 2026 01:29:07 GMT  
		Size: 14.1 MB (14053044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d78e33c1d8f94b81169c6330340ac46f025783165e85a9c80a4f54af31b81c`  
		Last Modified: Thu, 25 Jun 2026 01:29:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b3e384079847ebcd681c9d7212e862a845b8f29e34b915f79da434887f36d4`  
		Last Modified: Thu, 25 Jun 2026 02:14:38 GMT  
		Size: 5.8 MB (5845588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.15-rc-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:55afc65d70bfce996b80ad091f26fa41c5fd36fde44fd5faed5aa883b59ae71f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.6 KB (613643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e6b1e7961e85b7a9e2f95bba15f8cceec52de190e6ef2ff4e95f659de533ac`

```dockerfile
```

-	Layers:
	-	`sha256:bafd08319ef5ab6002135b3059136e77974f2ae00194a0e48e0e7d29ed33fbe3`  
		Last Modified: Thu, 25 Jun 2026 02:14:37 GMT  
		Size: 605.6 KB (605568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de4a49f9418e243888212b970d316a46d642ffbd068964a286930484c4a8f2f`  
		Last Modified: Thu, 25 Jun 2026 02:14:37 GMT  
		Size: 8.1 KB (8075 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.15-rc-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:4db1e224451674a9efd0c589e9a5b79915699bf57bd7e8adba4526a1670c60ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24564515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf430abf61814510736e7131d6538b8ee521d054923854c4f898ef9e53c43d42`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2026 01:27:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 01:27:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 25 Jun 2026 01:27:08 GMT
ENV PYTHON_VERSION=3.15.0b3
# Thu, 25 Jun 2026 01:27:08 GMT
ENV PYTHON_SHA256=6a935ae234a67e6549894373b0cfeb8361182d03b21442328ae9598ab7422127
# Thu, 25 Jun 2026 01:29:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 25 Jun 2026 01:29:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 25 Jun 2026 01:29:52 GMT
CMD ["python3"]
# Thu, 25 Jun 2026 02:14:11 GMT
ENV HY_VERSION=1.3.0
# Thu, 25 Jun 2026 02:14:11 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 25 Jun 2026 02:14:11 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 25 Jun 2026 02:14:11 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab461ec337d6a5a44ed2b15bbb55b66d4ac4ddeaf7cf5231251c8352dced63a7`  
		Last Modified: Thu, 25 Jun 2026 01:29:59 GMT  
		Size: 412.5 KB (412461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961a7114759021d8d8ca98b9ce33095f86bb1205616dd40f80f71bdaff2d05c0`  
		Last Modified: Thu, 25 Jun 2026 01:29:59 GMT  
		Size: 14.1 MB (14124325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04490f9ad5bc910fa3b943b0a2245a3c36dc8dda63e4712824f7b5bdfc9a194c`  
		Last Modified: Thu, 25 Jun 2026 01:29:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccdf06d73fddd80c11ec2d72eb67c177197a0857d86537139c5e2b1f74f0f4a`  
		Last Modified: Thu, 25 Jun 2026 02:14:17 GMT  
		Size: 5.8 MB (5845622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.15-rc-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:4845eb57f79bb022f7be91bc41d574ba14bd2aa637ed6b5faaef78cc14eac9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.2 KB (613153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1d7fd9a26f35e299fa684baf5f698075ab9c2b9c1c85dbbe474d8b362c09fe`

```dockerfile
```

-	Layers:
	-	`sha256:5a3db28ef2847d70fbef59855ffdf87270ca9624a7bfd6137997c91737ada170`  
		Last Modified: Thu, 25 Jun 2026 02:14:17 GMT  
		Size: 605.0 KB (604974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1df5164affa68732ac792d9fa95ff191268419e911c4aa746bc50ec1e40435a6`  
		Last Modified: Thu, 25 Jun 2026 02:14:17 GMT  
		Size: 8.2 KB (8179 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.15-rc-alpine3.23` - linux; riscv64

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

### `hylang:1-python3.15-rc-alpine3.23` - unknown; unknown

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

### `hylang:1-python3.15-rc-alpine3.23` - linux; s390x

```console
$ docker pull hylang@sha256:7f29e1485da5a110cd0ddd2430668408fcae29e6d8480dd66b0f6d6373b9c564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24499100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a2b960655dacb5a516313b1c032757d15111a153bdcd61c77d323443c6a53a`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:18:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 20:18:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 22 Jun 2026 20:18:59 GMT
ENV PYTHON_VERSION=3.15.0b3
# Mon, 22 Jun 2026 20:18:59 GMT
ENV PYTHON_SHA256=6a935ae234a67e6549894373b0cfeb8361182d03b21442328ae9598ab7422127
# Thu, 25 Jun 2026 02:16:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 25 Jun 2026 02:16:21 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 25 Jun 2026 02:16:21 GMT
CMD ["python3"]
# Thu, 25 Jun 2026 04:12:53 GMT
ENV HY_VERSION=1.3.0
# Thu, 25 Jun 2026 04:12:53 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 25 Jun 2026 04:12:53 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 25 Jun 2026 04:12:53 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a029c4feade980ba0ffd4101c9dabc4675f9c0d8e0ea2329350f7f3103cd63`  
		Last Modified: Mon, 22 Jun 2026 20:24:22 GMT  
		Size: 410.3 KB (410286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8dd8bd4eabc5480635e62e9f7d93022ee668238e08d98ae52a7000e8c2b8f0`  
		Last Modified: Thu, 25 Jun 2026 02:16:32 GMT  
		Size: 14.5 MB (14535745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7090d4d35fbecb5df4f35f2604deb0c5a0d03533b59a17c95238746502df0135`  
		Last Modified: Thu, 25 Jun 2026 02:16:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebcd810a962622f2fa8a8514241ce5cb47672af32b830a40db4251aed2df34b`  
		Last Modified: Thu, 25 Jun 2026 04:13:03 GMT  
		Size: 5.8 MB (5845571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.15-rc-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:58d2ab2fa8b25412edd26b5aec6a397a06f2ada72c31114120a47644b637891e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.0 KB (612992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53077542a57c9142a0a3cf21228bb84a4f2bfcb24a8be9d1b9eb0dbe529943b3`

```dockerfile
```

-	Layers:
	-	`sha256:33de71596eef61e6f006afae38635621300af6a0e8230b8369dfda8d97833ec0`  
		Last Modified: Thu, 25 Jun 2026 04:13:03 GMT  
		Size: 604.9 KB (604917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c050a9d5f605d955ca68ec0c2f90561e66f45e6661597204a1daa6d800fbc66d`  
		Last Modified: Thu, 25 Jun 2026 04:13:03 GMT  
		Size: 8.1 KB (8075 bytes)  
		MIME: application/vnd.in-toto+json
