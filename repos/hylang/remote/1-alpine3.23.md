## `hylang:1-alpine3.23`

```console
$ docker pull hylang@sha256:2b119d9f05d23289b30ef1499307feac0c8e88f03f601be7431c0f6a099bce4a
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

### `hylang:1-alpine3.23` - linux; amd64

```console
$ docker pull hylang@sha256:c9f26dd2d50541155d43cd91262422a990565e7273f58f27354ddce297100a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23422895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d027954a73bd8d07a4d25f45fbc5b814a1d629682b6e99c6ef970d9142748ce9`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:02:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 20:02:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 22 Jun 2026 20:02:19 GMT
ENV PYTHON_VERSION=3.14.6
# Mon, 22 Jun 2026 20:02:19 GMT
ENV PYTHON_SHA256=143b1dddefaec3bd2e21e3b839b34a2b7fb9842272883c576420d605e9f30c63
# Mon, 22 Jun 2026 20:04:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 22 Jun 2026 20:04:46 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 22 Jun 2026 20:04:46 GMT
CMD ["python3"]
# Mon, 22 Jun 2026 20:26:49 GMT
ENV HY_VERSION=1.3.0
# Mon, 22 Jun 2026 20:26:49 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 22 Jun 2026 20:26:49 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 22 Jun 2026 20:26:49 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74e2545a14c0e6f7995007062051d8e3db701c3b361c6063599b2c2ba2714fc`  
		Last Modified: Mon, 22 Jun 2026 20:04:52 GMT  
		Size: 408.7 KB (408749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7d208ac0265559f045a7dd3750b810d4e4f6a8e5bf5a958184ad342db80076`  
		Last Modified: Mon, 22 Jun 2026 20:04:53 GMT  
		Size: 13.5 MB (13455987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b284fb5df1b95b8705cc2b711e60227195896112d993804bbfaa5968756343d1`  
		Last Modified: Mon, 22 Jun 2026 20:04:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bae1bafb8b49b8f96380c1094bbca51cd15caf6e168e1f130eca7e8254b8364`  
		Last Modified: Mon, 22 Jun 2026 20:26:55 GMT  
		Size: 5.7 MB (5713490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:3f740f2e95ac585120e5dcca1becfcc1fc5948cc42ff3c6c6e739f5e8d9aaef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.1 KB (616069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e7d3898550588002baf51f3215f7cd05c09e4b35ece76284b6b7322c4a6b3b`

```dockerfile
```

-	Layers:
	-	`sha256:0d3afa0c16a08e3a715bac4a111b0b3eccc297179bbcea06477567975d9d95f1`  
		Last Modified: Mon, 22 Jun 2026 20:26:54 GMT  
		Size: 606.8 KB (606788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c07f3c1cbaac993740651def7494f3d99bb1e9419e10219da00a3419d340621e`  
		Last Modified: Mon, 22 Jun 2026 20:26:54 GMT  
		Size: 9.3 KB (9281 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull hylang@sha256:ea0569d7230a7ef42a2936d2c1dab42f6ec9eef7b68f705fd7de27c5673c52c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22756964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4180e7f504ab542bff2332cec1b09a868ba6367ef877bf3ba53bb70ef30d3655`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:55:21 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 22 Jun 2026 19:55:21 GMT
ENV PYTHON_VERSION=3.14.6
# Mon, 22 Jun 2026 19:55:21 GMT
ENV PYTHON_SHA256=143b1dddefaec3bd2e21e3b839b34a2b7fb9842272883c576420d605e9f30c63
# Mon, 22 Jun 2026 19:58:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 22 Jun 2026 19:58:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 22 Jun 2026 19:58:01 GMT
CMD ["python3"]
# Mon, 22 Jun 2026 20:36:38 GMT
ENV HY_VERSION=1.3.0
# Mon, 22 Jun 2026 20:36:38 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 22 Jun 2026 20:36:38 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 22 Jun 2026 20:36:38 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823da189bfadbe6c40aa844e7680172e67829fba115e00bbd398f7808f554fca`  
		Last Modified: Mon, 22 Jun 2026 19:58:06 GMT  
		Size: 410.6 KB (410587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455318ee357208875b5699f8bda5a240f374e38ae4df165f554a011e28876bcd`  
		Last Modified: Mon, 22 Jun 2026 19:58:06 GMT  
		Size: 13.1 MB (13079986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd0cf868e19304e4147e2f94be21ec2cf69b8911a5ee7b0bab462e909f29b0c`  
		Last Modified: Mon, 22 Jun 2026 19:58:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d59f27f0cb5aab2f33d8184abcb0ac8f1433a7516d9c256b6507ebde8e3a76b`  
		Last Modified: Mon, 22 Jun 2026 20:36:43 GMT  
		Size: 5.7 MB (5713549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:10e860e8a748f1679fe0a5a74b393e8e4eb566de5be1438dbcffc9c51b032f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd81fae765b69f51245b136025708e13f43e4331fca0e806f45537f2e0862ec`

```dockerfile
```

-	Layers:
	-	`sha256:763a2292e00bd2970d9e1da1896383f4e3b969f8402523e1504a4a395887a27d`  
		Last Modified: Mon, 22 Jun 2026 20:36:42 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull hylang@sha256:710fc9dbde0738abced2d7d8fcce7ac70c7e228c14bf787d89b89e47f9da4950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22064680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63fa6e18c4165ee59d4e3a7414067d684c5971c903b5016fcb4e92d745ada8f4`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:18 GMT
ADD alpine-minirootfs-3.23.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:09:25 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 20:09:25 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 22 Jun 2026 20:09:25 GMT
ENV PYTHON_VERSION=3.14.6
# Mon, 22 Jun 2026 20:09:25 GMT
ENV PYTHON_SHA256=143b1dddefaec3bd2e21e3b839b34a2b7fb9842272883c576420d605e9f30c63
# Mon, 22 Jun 2026 20:12:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 22 Jun 2026 20:12:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 22 Jun 2026 20:12:11 GMT
CMD ["python3"]
# Mon, 22 Jun 2026 21:54:59 GMT
ENV HY_VERSION=1.3.0
# Mon, 22 Jun 2026 21:54:59 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 22 Jun 2026 21:54:59 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 22 Jun 2026 21:54:59 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:177f8e1e6f831989320cf2b59b7eabd21cbf36804c79506912f3a81caff426f2`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddf015b0a49985001b5e70ba681fcf50dbe4f62825f81d6f0cda6771045590c`  
		Last Modified: Mon, 22 Jun 2026 20:12:18 GMT  
		Size: 409.3 KB (409279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5302d2e82eb8b3bbf8b92b37b378c4187782398a68607778d798fdb7ce996fee`  
		Last Modified: Mon, 22 Jun 2026 20:12:18 GMT  
		Size: 12.7 MB (12679773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862bf8383d4edfb2fc1abf4ebf62091f41d1beb10c3fc0f8dafe70ea2b2d72b0`  
		Last Modified: Mon, 22 Jun 2026 20:12:18 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ac10424e3bd0c60cbc1cf1eceb54bd4e17b7efff8be7420385297071ab66c5`  
		Last Modified: Mon, 22 Jun 2026 21:55:05 GMT  
		Size: 5.7 MB (5713525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:42f11e312e541d35c532f390c14b3508fc2cd9df9b777c62efd64f7d2b7831bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.6 KB (618592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2d8f218f9f5de3fa49ed24c7cd9cb228b953a49a5996f96031ddbde7c71789`

```dockerfile
```

-	Layers:
	-	`sha256:0574840c81a14941e802ed5162c45c036c988262efc6bf2162917b6498e2663f`  
		Last Modified: Mon, 22 Jun 2026 21:55:05 GMT  
		Size: 609.2 KB (609196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2910b94723017bf94cb3631981ea9be8524489219eb2865c7ef5d87b514ded26`  
		Last Modified: Mon, 22 Jun 2026 21:55:05 GMT  
		Size: 9.4 KB (9396 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:37a8b1810fa69ddcab63e691f9395319cef3abadfb2270da990cb7f5a7e79480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23850880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3c376cdb665aafbe1f8e0faf9baa4295fbd61ced6151feedbe40c145d35363`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:03:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 20:03:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 22 Jun 2026 20:03:00 GMT
ENV PYTHON_VERSION=3.14.6
# Mon, 22 Jun 2026 20:03:00 GMT
ENV PYTHON_SHA256=143b1dddefaec3bd2e21e3b839b34a2b7fb9842272883c576420d605e9f30c63
# Mon, 22 Jun 2026 20:05:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 22 Jun 2026 20:05:36 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 22 Jun 2026 20:05:36 GMT
CMD ["python3"]
# Mon, 22 Jun 2026 21:01:22 GMT
ENV HY_VERSION=1.3.0
# Mon, 22 Jun 2026 21:01:22 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 22 Jun 2026 21:01:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 22 Jun 2026 21:01:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be7425ceb5f1c6384b6883790c6ef4c8f2dee9cde812ddd70a09ec6b43226d5`  
		Last Modified: Mon, 22 Jun 2026 20:05:42 GMT  
		Size: 412.5 KB (412454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235affca4fcc26e56a621c4db6e2604c11a8ac639f9fcaa08b42b53276a2a933`  
		Last Modified: Mon, 22 Jun 2026 20:05:43 GMT  
		Size: 13.5 MB (13542739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfd90ef17371869764ab912b4ec789eb5830144a82b64dcae46e8fc9c71b52e`  
		Last Modified: Mon, 22 Jun 2026 20:05:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107fc4551f578c7b9aaaa31f4634f4530c3e86e41a8f1d3ed0401b54ecc69ffc`  
		Last Modified: Mon, 22 Jun 2026 21:01:28 GMT  
		Size: 5.7 MB (5713579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:30f36e25d049948def197f0eae2274e9c3cffe839bdee8cef70ac8e7d716942c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.7 KB (615678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4daef652b13a810f3a23afaa5169f1b830ccc68a26d0a67434aa4ac17ea2932c`

```dockerfile
```

-	Layers:
	-	`sha256:d6f3a817ce22a9f6461202699998a3fd0522981ce1a5bf4f3779992a3dfb758a`  
		Last Modified: Mon, 22 Jun 2026 21:01:28 GMT  
		Size: 606.2 KB (606242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9d0a9820ced356ea888ff30b1fee2d53878503df0d91f98fe9e959cc4354c1c`  
		Last Modified: Mon, 22 Jun 2026 21:01:28 GMT  
		Size: 9.4 KB (9436 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.23` - linux; 386

```console
$ docker pull hylang@sha256:3b84ae593b6eceabdf7ebabd97535b9aa668694fcd1386eb2e524fd2b8c0403a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23505905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b0bba535308da2df70ca2508c4efed2339029200f1f0dc09b9cd2cdabf3eff`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:54:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 22 Jun 2026 19:54:27 GMT
ENV PYTHON_VERSION=3.14.6
# Mon, 22 Jun 2026 19:54:27 GMT
ENV PYTHON_SHA256=143b1dddefaec3bd2e21e3b839b34a2b7fb9842272883c576420d605e9f30c63
# Mon, 22 Jun 2026 19:57:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 22 Jun 2026 19:57:26 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 22 Jun 2026 19:57:26 GMT
CMD ["python3"]
# Mon, 22 Jun 2026 20:20:59 GMT
ENV HY_VERSION=1.3.0
# Mon, 22 Jun 2026 20:20:59 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 22 Jun 2026 20:20:59 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 22 Jun 2026 20:20:59 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450993fc4068c70a123393cf4e7a9f1c820debda3b1328dd5bba84f62b8b0f84`  
		Last Modified: Mon, 22 Jun 2026 19:57:33 GMT  
		Size: 409.6 KB (409645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad6a24896ef81621ae012ab7d2cfa8dee0614d40db326709060137aaf7f30a6`  
		Last Modified: Mon, 22 Jun 2026 19:57:33 GMT  
		Size: 13.7 MB (13714533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704fffd63be4edc471cced4aaf1d626b91fdd0145b3824cede7030145e7b04df`  
		Last Modified: Mon, 22 Jun 2026 19:57:33 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62738c8f73a6bd37df13a9dabc74f124f4fd2928055159bbafbc770219f0bab9`  
		Last Modified: Mon, 22 Jun 2026 20:21:05 GMT  
		Size: 5.7 MB (5713489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:26696232e66658bd505d2a28f97c4f14c0d74ba75d9f750ac3a51180af647a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 KB (615975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79efebac6f8586541da6be4742c3998e15d5321f476cea2f93eff518b5426074`

```dockerfile
```

-	Layers:
	-	`sha256:aa7c111c9cadbe91eb169c614a5b817c43a170f0912e1707e045d8643b5b5550`  
		Last Modified: Mon, 22 Jun 2026 20:21:05 GMT  
		Size: 606.7 KB (606743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5085333aa36843b15ea0e0da530871b5db3273bf1f59a242c6142ea6ef653a03`  
		Last Modified: Mon, 22 Jun 2026 20:21:05 GMT  
		Size: 9.2 KB (9232 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.23` - linux; ppc64le

```console
$ docker pull hylang@sha256:aad812f5fbda0a90b89411b5cf03e98ed0d1bc6312fa2c8a4416b7cebbe8fb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 MB (24267898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc3ff885372df96b5944016fd1816ec6dd57b56e6e2f5c44d7616757579bc83`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:59:48 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 20:59:48 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 22 Jun 2026 20:59:48 GMT
ENV PYTHON_VERSION=3.14.6
# Mon, 22 Jun 2026 20:59:48 GMT
ENV PYTHON_SHA256=143b1dddefaec3bd2e21e3b839b34a2b7fb9842272883c576420d605e9f30c63
# Mon, 22 Jun 2026 21:02:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 22 Jun 2026 21:02:49 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 22 Jun 2026 21:02:49 GMT
CMD ["python3"]
# Mon, 22 Jun 2026 22:22:42 GMT
ENV HY_VERSION=1.3.0
# Mon, 22 Jun 2026 22:22:42 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 22 Jun 2026 22:22:42 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 22 Jun 2026 22:22:42 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e85c91277939a95804180f970e5faf12a64decf3e878de721a31d5d9645f9c`  
		Last Modified: Mon, 22 Jun 2026 21:03:01 GMT  
		Size: 412.9 KB (412925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233f72c2ad9955dbccf286e96b2e78358e6aec8fc7c2da3a9fd913a8f55eb981`  
		Last Modified: Mon, 22 Jun 2026 21:03:01 GMT  
		Size: 14.3 MB (14328785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ea8ffce7a3df07feaa626584f780cfa958b94abc40ae5ae6db432ce105eaae`  
		Last Modified: Mon, 22 Jun 2026 21:03:01 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5f113ae6f295adf401725257c874d9fae6fb44a0f8294ef974e54ef03a0290`  
		Last Modified: Mon, 22 Jun 2026 22:22:53 GMT  
		Size: 5.7 MB (5713642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:2c72294c46c35c9d5aceac4ad782cf196b1ce7110ce85549be12e8f4b3f54252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.5 KB (615547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a1a6ca5505dc0122575c86ba6fd4dcf87be96024464bbc63a73329af0900ba`

```dockerfile
```

-	Layers:
	-	`sha256:1ca48ea74668368778e0dd99b390e72000cfb4a5a1c1eea26d0a47b52f2e3fa1`  
		Last Modified: Mon, 22 Jun 2026 22:22:52 GMT  
		Size: 606.2 KB (606195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7a550a611d6e7ff0da6655e872490a2516ff47ecea42ecd115d03d5434f114a`  
		Last Modified: Mon, 22 Jun 2026 22:22:52 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.23` - linux; riscv64

```console
$ docker pull hylang@sha256:8be81669035235e19f928228ad39957ee241bb386a36320bb7465da2247a0afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25610062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c435e1da3de7e69d18935a286a3cbf2cfcb8163477bbd17106fe9e6df2438a`
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
ENV PYTHON_VERSION=3.14.6
# Thu, 04 Jun 2026 01:58:15 GMT
ENV PYTHON_SHA256=143b1dddefaec3bd2e21e3b839b34a2b7fb9842272883c576420d605e9f30c63
# Thu, 11 Jun 2026 16:01:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 16:01:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 16:01:55 GMT
CMD ["python3"]
# Sun, 14 Jun 2026 08:52:15 GMT
ENV HY_VERSION=1.3.0
# Sun, 14 Jun 2026 08:52:15 GMT
ENV HYRULE_VERSION=1.1.0
# Sun, 14 Jun 2026 08:52:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 14 Jun 2026 08:52:15 GMT
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
	-	`sha256:67d8ee023c8429ac04faf3b8d50f83e709d11ec8b63c6871a67e6289c14b8efe`  
		Last Modified: Thu, 11 Jun 2026 16:02:45 GMT  
		Size: 15.9 MB (15852060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad42cb99cc4aef69c0005632f72efbf376c68723f960ecdb35d8a4ec050aa5d`  
		Last Modified: Thu, 11 Jun 2026 16:02:42 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29995b8df84a9f74963c690369bca2a2a3eec979b9770a7624454e4b7e138d92`  
		Last Modified: Sun, 14 Jun 2026 08:52:54 GMT  
		Size: 5.7 MB (5714259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:2135996ebea0f9ba564ddc9ccba45f260d61062de76d86d5b1ef74afc864d2c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.4 KB (632435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954711140e62fdc00608c796ca6e769c5b932859bcbabb9d865f7d83cf5242c8`

```dockerfile
```

-	Layers:
	-	`sha256:8e65d2cda3c008a48789bf9b69b40d2a9fccee6dcf8f298f8c99fe2955f436cd`  
		Last Modified: Sun, 14 Jun 2026 08:52:53 GMT  
		Size: 623.1 KB (623083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:978a52cf423bac4491f90114a8102a07803bb07284640ba66660e583bc670bad`  
		Last Modified: Sun, 14 Jun 2026 08:52:53 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.23` - linux; s390x

```console
$ docker pull hylang@sha256:8c6409868d759622a8fe898718b656d5d5a61469c5a8819aa68e4615d6362b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23770935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4050c97bbaea48cf768ea1dd8bdb697ce839b35d6017534fdc94066c10067324`
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
ENV PYTHON_VERSION=3.14.6
# Mon, 22 Jun 2026 20:18:59 GMT
ENV PYTHON_SHA256=143b1dddefaec3bd2e21e3b839b34a2b7fb9842272883c576420d605e9f30c63
# Mon, 22 Jun 2026 20:24:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 22 Jun 2026 20:24:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 22 Jun 2026 20:24:11 GMT
CMD ["python3"]
# Mon, 22 Jun 2026 21:58:01 GMT
ENV HY_VERSION=1.3.0
# Mon, 22 Jun 2026 21:58:01 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 22 Jun 2026 21:58:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 22 Jun 2026 21:58:01 GMT
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
	-	`sha256:0843161bc587f900f3ae8b99dca9275996ce3c8302d821445e28a7c7455d8102`  
		Last Modified: Mon, 22 Jun 2026 20:24:22 GMT  
		Size: 13.9 MB (13939593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861d1f6933bde2bc8db107097e02d5e951f25b2cc4e7156338a5ed2b25ee17f7`  
		Last Modified: Mon, 22 Jun 2026 20:24:22 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd535cfbfc1764ac0b9512eb969127c396540113e5c5565c57aa65735e12d18`  
		Last Modified: Mon, 22 Jun 2026 21:58:10 GMT  
		Size: 5.7 MB (5713558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:2861216b9209597ed0f05340dfc4c9fab1d8893b5eb6926f6005b327a7df0dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.4 KB (615421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79628636ae52dae43cd6234393446d666c0416dbb51363698c78ee1cbd6e1d4b`

```dockerfile
```

-	Layers:
	-	`sha256:a13e4b8081720dcdb857419184a6755c230a55eb91367cf23b5daadebea1d01c`  
		Last Modified: Mon, 22 Jun 2026 21:58:10 GMT  
		Size: 606.1 KB (606137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaa15b700e35432f2b9bcf65723b42555856a38ea1dc62a6a17140490d756ccc`  
		Last Modified: Mon, 22 Jun 2026 21:58:10 GMT  
		Size: 9.3 KB (9284 bytes)  
		MIME: application/vnd.in-toto+json
