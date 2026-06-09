## `hylang:1-python3.15-rc-alpine3.23`

```console
$ docker pull hylang@sha256:f16cdde277ce3b5372f1721d37b7d68c5949ce85dd1eb8e6391be17da40259c5
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
$ docker pull hylang@sha256:445d53213fb96c035e5ee0c3fccbc0da89da38a1845eaea8ea10442892640b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24207767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21827537eec5717b5424393497605b117da2ceb338e824172ee53eceb322658e`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 03 Jun 2026 18:17:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jun 2026 18:17:34 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 03 Jun 2026 18:17:34 GMT
ENV PYTHON_VERSION=3.15.0b2
# Wed, 03 Jun 2026 18:17:34 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Wed, 03 Jun 2026 18:19:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Jun 2026 18:19:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Jun 2026 18:19:55 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:44:15 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:44:15 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:44:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:44:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df99b4f9098547e96cd76e4921730c00eea6a92215ab083d9086fc3b2d01410`  
		Last Modified: Wed, 03 Jun 2026 18:20:02 GMT  
		Size: 455.5 KB (455490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557badf6ab900b04526f7d8af842ca25afd0f7bf395f32945133ccf419ca6c6f`  
		Last Modified: Wed, 03 Jun 2026 18:20:02 GMT  
		Size: 14.0 MB (14043497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0676fd7772072a1fea38511966e48a3ac760f46755fc90e44155baf6bee6ce6d`  
		Last Modified: Wed, 03 Jun 2026 18:20:02 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99de53818c51f32efadca677eda84d69e2b8899d4b550656c45e4df5c3c110a5`  
		Last Modified: Mon, 08 Jun 2026 22:44:21 GMT  
		Size: 5.8 MB (5844342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.15-rc-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:4bdc8661adcc47b5b7a9e4f526fe85287230f8f8da167f261de23a739c8272bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.2 KB (633191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904801b3a099b1cb3ac2c7fcd5c4a854f13beca89ee7746e6de36d8547af9828`

```dockerfile
```

-	Layers:
	-	`sha256:1c82cd83d81182fe2b496b72fe7e16b266ff87e8540c596ae7012207fd21366b`  
		Last Modified: Mon, 08 Jun 2026 22:44:21 GMT  
		Size: 623.8 KB (623788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a852416db060e5309befd29bd600ea73aec80e2b69c23705f4a89d3bebf89be`  
		Last Modified: Mon, 08 Jun 2026 22:44:20 GMT  
		Size: 9.4 KB (9403 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.15-rc-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:acd749d21f55fd7312c6f202a1670ae680cd703b9ed5d6a7240a0261425e3348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24618619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff04b4fb4052ea1edf8abcb67d15cd592ac929384d7f29cb90511e1d96c1f1a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 03 Jun 2026 18:17:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jun 2026 18:17:22 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 03 Jun 2026 18:17:22 GMT
ENV PYTHON_VERSION=3.15.0b2
# Wed, 03 Jun 2026 18:17:22 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Wed, 03 Jun 2026 18:20:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Jun 2026 18:20:04 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Jun 2026 18:20:04 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:44:25 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:44:25 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:44:25 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:44:25 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85054daebbc71b0f44e6b5d64d3811bafa23f5f4f6c2456c17127574bf18ab4c`  
		Last Modified: Wed, 03 Jun 2026 18:20:11 GMT  
		Size: 457.8 KB (457761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfb951e23e4a07d05f11cee0c3f17479f1293b945fffd238ab70a70a887ab57`  
		Last Modified: Wed, 03 Jun 2026 18:20:11 GMT  
		Size: 14.1 MB (14116487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3eb6cec7bfed22746f3ba7553543a47c53e999babc5fe555c920231c0ee3cf`  
		Last Modified: Wed, 03 Jun 2026 18:20:11 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dd97641785d55ac98a11817f031ea8de3057af23c1cfecb1bcd159d5d175f1`  
		Last Modified: Mon, 08 Jun 2026 22:44:31 GMT  
		Size: 5.8 MB (5844253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.15-rc-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:17399a3c12e12b8246dac38aa7af312b69a6fecfd1aa9caeab2f1af5a1c96383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.8 KB (632797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ea91f5cf1480551bf0e7f231703d58a3c5d41c20cf35e4cba099fbda6accb3`

```dockerfile
```

-	Layers:
	-	`sha256:d8268cb16c3f64c2ec7087249f8518055671b17691616e1820689c081c7b5dd9`  
		Last Modified: Mon, 08 Jun 2026 22:44:31 GMT  
		Size: 623.2 KB (623242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52e4ffcaa78da77fadb2cc4ff7c4b3491a7710ae4c4c190d5be45f3853fd09bf`  
		Last Modified: Mon, 08 Jun 2026 22:44:30 GMT  
		Size: 9.6 KB (9555 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.15-rc-alpine3.23` - linux; riscv64

```console
$ docker pull hylang@sha256:1438409ce64c84528c76cc209ff84bc4e8c30afd87a4c7ececbee6a61190d5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (24037099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc49b996df249b7d536f11d0df351c5c7602b36208fc4ca8faaabf312e2cf557`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 01:58:15 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 01:58:15 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 04 Jun 2026 01:58:15 GMT
ENV PYTHON_VERSION=3.15.0b2
# Thu, 04 Jun 2026 01:58:15 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Thu, 04 Jun 2026 02:41:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 04 Jun 2026 02:41:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 04 Jun 2026 02:41:13 GMT
CMD ["python3"]
# Thu, 04 Jun 2026 03:45:58 GMT
ENV HY_VERSION=1.3.0
# Thu, 04 Jun 2026 03:45:58 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 04 Jun 2026 03:45:58 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 04 Jun 2026 03:45:58 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765866854439454599b98b3453482041066c253a5bb4172d859d005f14f950ff`  
		Last Modified: Thu, 04 Jun 2026 02:41:58 GMT  
		Size: 455.8 KB (455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade6d6a20fcb68992a4db3b3eaff05ebd630ca6df0b614a6920cd066741543ff`  
		Last Modified: Thu, 04 Jun 2026 02:42:01 GMT  
		Size: 14.2 MB (14151047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d571a66a89d3d5a8e1d5bdc7754da6cb0644ae7a963180b1224d5d48506890b7`  
		Last Modified: Thu, 04 Jun 2026 02:41:59 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b242c2eff04f3bbe08e4a6f21c96b73f62d5cd574deaa52c5f27ebfb27a080ea`  
		Last Modified: Thu, 04 Jun 2026 03:46:38 GMT  
		Size: 5.8 MB (5842310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.15-rc-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:5ab14193aee9ad2fd9d6339b46ae2d45e461e2b0371ac44969ed5082f775101f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.7 KB (632662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16c8501a29fa0ba79565698f1a8ec25f53088d3a1cbf352f54803b32f428c08`

```dockerfile
```

-	Layers:
	-	`sha256:031bee18720d74665672d81955835ae4cbddf8e2131db008bcd005d448fcc6c8`  
		Last Modified: Thu, 04 Jun 2026 03:46:37 GMT  
		Size: 623.2 KB (623191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:915098206badd6a48c696a44a82ea9d90e673f64ba264cd5fb9ee19e4786ac6e`  
		Last Modified: Thu, 04 Jun 2026 03:46:37 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.15-rc-alpine3.23` - linux; s390x

```console
$ docker pull hylang@sha256:c6f613885b2f7a25f26a7b0d3017ed87e21a565dc6ed819de85df793dbd1eb8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24553426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6d17afb4d9c1eb1cd33856c166ce8d5a074f879ac62aa9acc792eecd58e378`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 03 Jun 2026 18:23:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jun 2026 18:23:41 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 03 Jun 2026 18:23:41 GMT
ENV PYTHON_VERSION=3.15.0b2
# Wed, 03 Jun 2026 18:23:41 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Wed, 03 Jun 2026 18:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Jun 2026 18:28:14 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Jun 2026 18:28:14 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:53:49 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:53:49 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:53:49 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:53:49 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeefb3b1180cfa1729e6278a2f495eb387fb9dc2f8d42a2b3b65911ff5b9749a`  
		Last Modified: Wed, 03 Jun 2026 18:28:25 GMT  
		Size: 456.5 KB (456473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c9f35fc121c0dfbc605a3c83365cba577649c7ea02fa127e5bb12e36e1c4d7`  
		Last Modified: Wed, 03 Jun 2026 18:28:25 GMT  
		Size: 14.5 MB (14525939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f824da1ef9cf04db00052849feb880fe814ae5eca88e4fc619f5a123efb8265c`  
		Last Modified: Wed, 03 Jun 2026 18:28:25 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e262a7558a0ef4561f17268cbf98806d4a50875913bba5c41727af4e4abce412`  
		Last Modified: Mon, 08 Jun 2026 22:53:59 GMT  
		Size: 5.8 MB (5844233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.15-rc-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:5cad563d2402bb479823d062f0949406218e17f02585d266c33543af8a2afc36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.5 KB (632539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b813e9079c7f362a7c299b905d8f5c83aed24a3aeb4de0516f6f9ac34fef6ae`

```dockerfile
```

-	Layers:
	-	`sha256:b50bb3226bcddfc8873dd0e9c37138f15c6e5d6c7873bc4c8b1c2d25e25682d6`  
		Last Modified: Mon, 08 Jun 2026 22:53:58 GMT  
		Size: 623.1 KB (623137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f3a4fe33a15ccca6d1ac3f35b2c30c4b73877de11d05bbb5b57e0247dcdfad2`  
		Last Modified: Mon, 08 Jun 2026 22:53:58 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json
