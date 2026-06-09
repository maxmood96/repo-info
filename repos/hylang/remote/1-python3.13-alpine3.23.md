## `hylang:1-python3.13-alpine3.23`

```console
$ docker pull hylang@sha256:3caef70df12473b1f8df9f737022353a42556ca5373f5426eb29bad5a80a9776
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

### `hylang:1-python3.13-alpine3.23` - linux; amd64

```console
$ docker pull hylang@sha256:a98821bf688d45fd1832124fc67cd4a932bf2accce19f4f6896061985138b455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.2 MB (22230341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3381f7068329549c128b0b46d04f8801fa0daf1138686539a5365ddb8a4384f7`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:46:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:46:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 20:46:59 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 15 Apr 2026 20:46:59 GMT
ENV PYTHON_VERSION=3.13.13
# Wed, 15 Apr 2026 20:46:59 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Wed, 15 Apr 2026 20:52:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 20:52:50 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 20:52:50 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:45:04 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:45:04 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:45:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:45:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a9d634f9dc83ef653914ab9c5e2e1e87e8389bf2d8a77b767c6bd0d3d5ad75`  
		Last Modified: Wed, 15 Apr 2026 20:52:56 GMT  
		Size: 455.7 KB (455665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d49f4bef16a382a5f10aa3c249fb29f6ff69ca0f4f8238b9a5fdbed0d16cef`  
		Last Modified: Wed, 15 Apr 2026 20:52:57 GMT  
		Size: 12.5 MB (12533688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574f89312598a601a7cd72935b57ca1b10777d0d9486a797d034b4db08cb0ce4`  
		Last Modified: Wed, 15 Apr 2026 20:52:56 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56789c7d3d21cb882796bc4dc1520203716fc7a78d8ce0a9ba4184d6c1e2b943`  
		Last Modified: Mon, 08 Jun 2026 22:45:10 GMT  
		Size: 5.4 MB (5376548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:e82fc6edb25cd38a13ebedf6ee687468fbbec7938a969b9e19059d495c1dc42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.1 KB (630077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a2c43864518d4c76be3e9382e3cce410e5534d188fe7cf5e9b93a5240f0554`

```dockerfile
```

-	Layers:
	-	`sha256:37a7ea4e4c6322d9438e279fc7919577ccd255a8dc8a9cab749269e53d47923e`  
		Last Modified: Mon, 08 Jun 2026 22:45:09 GMT  
		Size: 620.7 KB (620685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c04601e06f77f4dc09bdf3aec76e80b9c5276c15069b56a4d990f8a9d495471f`  
		Last Modified: Mon, 08 Jun 2026 22:45:09 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-alpine3.23` - linux; arm variant v6

```console
$ docker pull hylang@sha256:7b115db83ca131cc39004d30f59d09c022d1cb2176932558b49eed8ae8a58ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21578940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00aa345558bc222d5af486a35a645867b6c46198ab9841fddfddbc730845030e`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:32:48 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:32:48 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 20:32:48 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 15 Apr 2026 20:32:48 GMT
ENV PYTHON_VERSION=3.13.13
# Wed, 15 Apr 2026 20:32:48 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Wed, 15 Apr 2026 20:40:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 20:40:33 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 20:40:33 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:44:13 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:44:13 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:44:13 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:44:13 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f7776ddf1c68505df5dac9b6cd8d24c5c64af92b0c14be500a80aea2e29378`  
		Last Modified: Wed, 15 Apr 2026 20:40:38 GMT  
		Size: 456.5 KB (456512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac44588bb59c7933ee08bb25a1c0732beb89577b5af92def87c87de058e5ba6c`  
		Last Modified: Wed, 15 Apr 2026 20:40:39 GMT  
		Size: 12.2 MB (12173673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd33c3e046705d0a34e2b4aafcd2e36532dcf583edb3ab3917cf4ab89492185e`  
		Last Modified: Wed, 15 Apr 2026 20:40:38 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3e2e0b1086234c9bdcd6ca4e63695c391e0fdc0ce6a7b8bc10d134fdddd672`  
		Last Modified: Mon, 08 Jun 2026 22:44:18 GMT  
		Size: 5.4 MB (5376643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:0e8637d6cd5f25d7216e50ab0aeca14b6abe7c9699473619f6d7968648bad4eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a03a8a5f27bcebfbf7bdeb8d99f28448cf11bd81d91985f5432fd18dc64d4eb`

```dockerfile
```

-	Layers:
	-	`sha256:252bff6d35c997d5ae046a77389fac93fe34d96cd66f096932fef06d9949466d`  
		Last Modified: Mon, 08 Jun 2026 22:44:17 GMT  
		Size: 9.3 KB (9289 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-alpine3.23` - linux; arm variant v7

```console
$ docker pull hylang@sha256:17571dcb30e31866917943e6a993d63e5ddbdf95f0451039a2706675f53ef2c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20947548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3a2630705270dd1f183c7e6a89644927316aae9de487ca8f5be44f183265d7`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:41:48 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:41:48 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 20:41:48 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 15 Apr 2026 20:41:48 GMT
ENV PYTHON_VERSION=3.13.13
# Wed, 15 Apr 2026 20:41:48 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Wed, 15 Apr 2026 20:50:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 20:50:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 20:50:47 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:47:04 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:47:04 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:47:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:47:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c308f75576a36648b24364593b337dd6287fe15f339efe36b70fa850805fdc1`  
		Last Modified: Wed, 15 Apr 2026 20:50:54 GMT  
		Size: 455.6 KB (455629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0462cb2943ab71a254515f943f962fc191121f8e72847b49c1252632e813602b`  
		Last Modified: Wed, 15 Apr 2026 20:50:54 GMT  
		Size: 11.8 MB (11832106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da779aab26c9e5f105c45619ebf1e7ce22d1865f1f63fe56f138e0afee0a776c`  
		Last Modified: Wed, 15 Apr 2026 20:50:53 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e465ff3b6acf9a22ae4ce399d426dee20fb3ad06beecfbdc023afb817a25d198`  
		Last Modified: Mon, 08 Jun 2026 22:47:10 GMT  
		Size: 5.4 MB (5376442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:117a8fc43d3e56fbecb8a7d764aad07a4e45e4a3e3112696fab710caed980552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.6 KB (632597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aca8d0003f20e323be194065ee47a32c4e3f463cc0703cbee42cc2ca53d378b`

```dockerfile
```

-	Layers:
	-	`sha256:f384da7c7e9011a29f9e820b74ba41b8a70d6dd417082adeab930b023d5a7799`  
		Last Modified: Mon, 08 Jun 2026 22:47:10 GMT  
		Size: 623.1 KB (623093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b4e09ad91fb734084bcfbd84f9c3972f5577ae865bd4191f3f574062ca6e9a`  
		Last Modified: Mon, 08 Jun 2026 22:47:09 GMT  
		Size: 9.5 KB (9504 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:cd41c859092155a67028458524d1abc29f26fa1721dd411ba1549dad6b7d7c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22675706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4406614736ad004ed8148d76e2544808f791751bdf60af1335ecc29e998f1e4a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:47:03 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:47:03 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 20:47:03 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 15 Apr 2026 20:47:03 GMT
ENV PYTHON_VERSION=3.13.13
# Wed, 15 Apr 2026 20:47:03 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Wed, 15 Apr 2026 20:57:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 20:57:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 20:57:41 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:45:15 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:45:15 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:45:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:45:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3070388042c6d2de93821dba1cb8d03af7dec9dd34bffe43470c5a3206ecb932`  
		Last Modified: Wed, 15 Apr 2026 20:49:54 GMT  
		Size: 457.9 KB (457916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aec0c7a51b0e84041e46a198a2cabe5b884121ffd1ea800aa4cf4eb7f9ccf7c`  
		Last Modified: Wed, 15 Apr 2026 20:57:47 GMT  
		Size: 12.6 MB (12641104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c84d37ae3543eef382dc00181213db003ba2a7b8591347a96de50a35ee7a99a`  
		Last Modified: Wed, 15 Apr 2026 20:57:47 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeb4f190cdb09ab1f095e8ed4225a892e3b23878746fe37b0bca002ee88190f`  
		Last Modified: Mon, 08 Jun 2026 22:45:21 GMT  
		Size: 5.4 MB (5376565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:fb8ca2ad9f3e5d77e597c1781cdd70f931fb20a79b4688819533a5d5ca70ee82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.7 KB (629683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af21e3c47440f62668227b8f2937d231720e2062181fa27c777999c1d3a996f`

```dockerfile
```

-	Layers:
	-	`sha256:b557cc8edfabd9253b2114ee1981f560870fd015c4b0ec46ae0ad855abead67a`  
		Last Modified: Mon, 08 Jun 2026 22:45:21 GMT  
		Size: 620.1 KB (620139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df4c2b9e4103f3d3397e3124c7ecf10099599fa710b8dd5c1222ebf49c0c6d31`  
		Last Modified: Mon, 08 Jun 2026 22:45:20 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-alpine3.23` - linux; 386

```console
$ docker pull hylang@sha256:001d674e7c5c716172fc3649670b74877ddd756b59c7591e2343b96b472e0dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22295378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f38273d03e45204a452d0aa4e8bca6d908e8c42a8ee7e12202adc0938e45ed0`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:27:50 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:27:50 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 22:27:50 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 15 Apr 2026 22:27:50 GMT
ENV PYTHON_VERSION=3.13.13
# Wed, 15 Apr 2026 22:27:50 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Wed, 15 Apr 2026 22:33:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 22:33:08 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 22:33:08 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:46:54 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:46:54 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:46:54 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:46:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20d641aa9f028c34170d723d3b8f7c91b762399461a7d7493bf7a49b9cc80e2`  
		Last Modified: Wed, 15 Apr 2026 22:33:14 GMT  
		Size: 456.1 KB (456126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad0798b806e236f9393dc36e89ce46a039dfedddead476dcfaea6e716c023a1`  
		Last Modified: Wed, 15 Apr 2026 22:33:14 GMT  
		Size: 12.8 MB (12772123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403868cfde3df139eca4f9ad2a9573ad0f6fb6a28d260c43d95973e1e110c988`  
		Last Modified: Wed, 15 Apr 2026 22:33:14 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c3e0343c575af84f02d6c59c9473ad002d03a77302400dc53e05f649ea0831`  
		Last Modified: Mon, 08 Jun 2026 22:47:00 GMT  
		Size: 5.4 MB (5376437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:1fb9e9a5a587ecbb3dd1e184fdc9b9de255fe3947ea39c8138c9b68c5e728275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.0 KB (629980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df1c7c4af748a2197b39e87fb60166b7eca214aa821a1875eb1b52127d59d9a2`

```dockerfile
```

-	Layers:
	-	`sha256:432804e08adb708f60d16704e8f429bbcad51c5786a71b451f41a30391eb4df0`  
		Last Modified: Mon, 08 Jun 2026 22:47:00 GMT  
		Size: 620.6 KB (620640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d4e9a5e7691820a858acfeb34c0023757f5286e6d1cd2f73ff701747701eac9`  
		Last Modified: Mon, 08 Jun 2026 22:46:59 GMT  
		Size: 9.3 KB (9340 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-alpine3.23` - linux; ppc64le

```console
$ docker pull hylang@sha256:e65c1812e42a01bcf69345d87c7aa1c8adc9d94833147ed7fefb8b52957d5582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23005063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae92c7a2afbe635ccf78cb717ec261ce5811119b48936d9ecd55a9d46cc21e7`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:24:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:24:53 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 22:24:53 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 15 Apr 2026 22:24:53 GMT
ENV PYTHON_VERSION=3.13.13
# Wed, 15 Apr 2026 22:24:53 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Wed, 15 Apr 2026 22:38:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 22:38:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 22:38:06 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 23:17:01 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 23:17:01 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 23:17:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 23:17:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733c1cad5f8e0c40c970a427f687a14dcfa498e80380cc189bb3aaa48c76c673`  
		Last Modified: Wed, 15 Apr 2026 22:29:06 GMT  
		Size: 458.3 KB (458317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5644f4970cbc9c91f44939051b999ca55b983f272d601cc49e128e7ba8b3e6d`  
		Last Modified: Wed, 15 Apr 2026 22:38:19 GMT  
		Size: 13.3 MB (13338980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24631d31a2b2b7f1aa59d0c0b2671627ca26268024e6db35c4750605dfdac8b7`  
		Last Modified: Wed, 15 Apr 2026 22:38:18 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ef0f11258df5a655eb95863312e3f8c473308321f0613de375a30006f3f9aa`  
		Last Modified: Mon, 08 Jun 2026 23:17:12 GMT  
		Size: 5.4 MB (5376589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:30ecd4b13253bb5658caf8af7532db152876c66ca62f9eea8e108b293cca4216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.6 KB (629552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ece6c1ea4637d0f6397e9efe9165cd55d8ba88d56a0f35acd32796c467e644`

```dockerfile
```

-	Layers:
	-	`sha256:10cdbc11ad522f307d8391b57d6e4b4d054e038fc1696486955eeda2d3575666`  
		Last Modified: Mon, 08 Jun 2026 23:17:12 GMT  
		Size: 620.1 KB (620092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49d25e4b8afe20f4648e5f0dbedf78a5898ae7d222e22706a793386540891395`  
		Last Modified: Mon, 08 Jun 2026 23:17:12 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-alpine3.23` - linux; riscv64

```console
$ docker pull hylang@sha256:fa75687783a0680bd71cdafa79db5c481238c3df08ca1b08427ad79e41e64fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (21988447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfce6cde604c86fdc4e5ffe4eb9b60dcc841eebddcc999997953a613f0178ee9`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 17:40:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 17:40:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 16 Apr 2026 17:40:08 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 16 Apr 2026 17:40:08 GMT
ENV PYTHON_VERSION=3.13.13
# Thu, 16 Apr 2026 17:40:08 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Thu, 16 Apr 2026 19:56:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 16 Apr 2026 19:56:25 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 16 Apr 2026 19:56:25 GMT
CMD ["python3"]
# Thu, 28 May 2026 20:38:45 GMT
ENV HY_VERSION=1.3.0
# Thu, 28 May 2026 20:38:45 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 28 May 2026 20:38:45 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 28 May 2026 20:38:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61e59a057c814c53a5464ba84ff684eba3f6ab2211a1502be9ca09e40486184`  
		Last Modified: Thu, 16 Apr 2026 18:22:41 GMT  
		Size: 456.0 KB (456003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012dbc93cf003ebb157060c8e11109f2994085a3c1b79c904d7fb233e5731491`  
		Last Modified: Thu, 16 Apr 2026 19:57:10 GMT  
		Size: 12.6 MB (12570067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b225295d88993642ccd50302c0791e055098b41530200f883690dff076db09d3`  
		Last Modified: Thu, 16 Apr 2026 19:57:08 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a059e4642c526bfd908c75932a234a746f59e9e030576507c16fbeb39a2f490d`  
		Last Modified: Thu, 28 May 2026 20:39:24 GMT  
		Size: 5.4 MB (5374463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:00182d115c089e4960b9718bf7ab727021cd46c716401bfb5460a795c70d7a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.5 KB (629548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb536d736c58bec95c83f046ad521a0c99222ed24f8ae220fad0d8cf40e1aeb1`

```dockerfile
```

-	Layers:
	-	`sha256:2ae138ef5084ba3cbe88fc3993eea20333dce2b98dd0bd7fce78d98c5df2f084`  
		Last Modified: Thu, 28 May 2026 20:39:23 GMT  
		Size: 620.1 KB (620088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:720eec39cfd75172b0a3d1a34dac3b55fd822e2cb1d754136220bf6a363fedec`  
		Last Modified: Thu, 28 May 2026 20:39:23 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-alpine3.23` - linux; s390x

```console
$ docker pull hylang@sha256:cd8dd31a7b0b01698c036a167e5c8e274b6d952ed50ddf699960213d1f16686f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22548146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b4ed21186305c4f13b8b3a1403308fe0ca96a93781c8b5e92d936ee3508baf`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:17:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:17:53 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 22:17:53 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 15 Apr 2026 22:17:53 GMT
ENV PYTHON_VERSION=3.13.13
# Wed, 15 Apr 2026 22:17:53 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Wed, 15 Apr 2026 22:51:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 22:51:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 22:51:23 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:55:28 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:55:28 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:55:28 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:55:28 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6d783dc3f612930ddb20e808297a0ce017500fb3f8134bae566eb50ec93746`  
		Last Modified: Wed, 15 Apr 2026 22:27:13 GMT  
		Size: 456.7 KB (456670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a62eab1a86ac6ff6ecba1ac9878d7d1c9173f32af3071e2ba03320ef382d954`  
		Last Modified: Wed, 15 Apr 2026 22:51:59 GMT  
		Size: 13.0 MB (12988243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bbb00a59719e4a0020895ed9d29c58ca9566e2780d027f48730d15438901d3`  
		Last Modified: Wed, 15 Apr 2026 22:51:54 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979019c7fd28dc598159b573b2e273b0733a7d9d637209d5a199531314668db4`  
		Last Modified: Mon, 08 Jun 2026 22:55:39 GMT  
		Size: 5.4 MB (5376455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:d421a4c153d174e0a3683b67513d3fbe935c299c4c4d54e0e0eff8787a0bfbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.4 KB (629425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d356695e7bdb398badfeca973a29416b5e9bfc412df84005117faaa07fd12f1`

```dockerfile
```

-	Layers:
	-	`sha256:be48ccc2df1d58475916bc4c4bdc71a131118795db62984f8618cf6e17ae7ba3`  
		Last Modified: Mon, 08 Jun 2026 22:55:38 GMT  
		Size: 620.0 KB (620034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b45d68e2da94527054baf01cb9d8a5f9b4f0249af281bcbea56a53436276f05d`  
		Last Modified: Mon, 08 Jun 2026 22:55:38 GMT  
		Size: 9.4 KB (9391 bytes)  
		MIME: application/vnd.in-toto+json
