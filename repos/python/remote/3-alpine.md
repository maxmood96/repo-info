## `python:3-alpine`

```console
$ docker pull python@sha256:c97d6e916998ebe4e08c44ca85a15abe70d084e6be803f19ffd59116725953ef
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

### `python:3-alpine` - linux; amd64

```console
$ docker pull python@sha256:f3abe4e694b3884b33812733a5818abdfb644e5abaaf9928f08df78aaf3c50a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17685530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cab61ae31c14734513856577747b8d5f9eb5c8f5ea1668dac51c92d194c7eef`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:32:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:32:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 03:32:59 GMT
ENV PYTHON_VERSION=3.14.2
# Wed, 28 Jan 2026 03:32:59 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Wed, 28 Jan 2026 03:35:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 03:35:46 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 03:35:46 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6e0b1647863beafdee1aebbdaeaeb2fda3507fe7e1339bbdd208cc1e50a840`  
		Last Modified: Wed, 28 Jan 2026 03:35:54 GMT  
		Size: 460.9 KB (460934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff83b2b57ff13d7d3ad1ccc77ff3a507c3ec3e1e2114fe6a549e922337320e8e`  
		Last Modified: Wed, 28 Jan 2026 03:35:54 GMT  
		Size: 13.4 MB (13362526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd701e501660028c5c9421ae4ad32b775dd4677863eebf922cab66ae731ee6f7`  
		Last Modified: Wed, 28 Jan 2026 03:35:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine` - unknown; unknown

```console
$ docker pull python@sha256:2b124badc2362e952a8f298430c1336047e9a936f834edf30eb452cc78ffa65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.6 KB (640627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b362c1eb5eaae095dbcdd0cceaae1b1d966b4fc6775d29081f87e6a2795137`

```dockerfile
```

-	Layers:
	-	`sha256:82934f90545ccfb81c781162f0482fa505229996a7bf80db901eaac70729afe6`  
		Last Modified: Wed, 28 Jan 2026 03:35:54 GMT  
		Size: 618.0 KB (617962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff17d2c58e7b4cae2c3b5712001d7e23b8bc48ebfa8b2b1dfe105f9d6737292`  
		Last Modified: Wed, 28 Jan 2026 03:35:54 GMT  
		Size: 22.7 KB (22665 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine` - linux; arm variant v6

```console
$ docker pull python@sha256:d9c51e8a1a2df8a08768f368dce8514d90f91d360d7ec7d3072f5c26c67c8255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17016833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695a08545a9ec591719daf867654d96bdde38cdecfc2a078c59e232b94deb334`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:03:32 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:03:32 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 03:03:32 GMT
ENV PYTHON_VERSION=3.14.2
# Wed, 28 Jan 2026 03:03:32 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Wed, 28 Jan 2026 03:06:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 03:06:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 03:06:20 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773b608ff05726281d3136f81e60ce6c20dc1d0693df62f1d6a69dd6bf20c406`  
		Last Modified: Wed, 28 Jan 2026 03:06:26 GMT  
		Size: 461.4 KB (461445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5706452906aecb55749ef0fb0e3fe3dc1847c941a20529c155508719d94319`  
		Last Modified: Wed, 28 Jan 2026 03:06:26 GMT  
		Size: 13.0 MB (12985317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdacc8220994199542da09cd03016899f0d7f0450c5b5fd865de45db9ae623d2`  
		Last Modified: Wed, 28 Jan 2026 03:06:25 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine` - unknown; unknown

```console
$ docker pull python@sha256:b6bb617adfa16b2951fd1565765966d1c53eb8be3b43ecec4ed6e2c52bf1a3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 KB (22588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b4c45dd717dc5d3c911b0368058d5cf5659475c3a15d7e6b7c36b0513b7e8e`

```dockerfile
```

-	Layers:
	-	`sha256:82b42821ab1d608b850d8f0d4388dbe240063c93c3a6da3b5bd9a1c11cea33d4`  
		Last Modified: Wed, 28 Jan 2026 03:06:26 GMT  
		Size: 22.6 KB (22588 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine` - linux; arm variant v7

```console
$ docker pull python@sha256:849e6461ff2555a50d9f5d837b030ebc56932b59fcb114173181a60c0cc79ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbdfbeab67f53398f52d8f8a1a63c5b55f05475d5022baa919644b926abad52`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:10:35 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:10:35 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 03:10:35 GMT
ENV PYTHON_VERSION=3.14.2
# Wed, 28 Jan 2026 03:10:35 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Wed, 28 Jan 2026 03:13:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 03:13:21 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 03:13:21 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db21d1bf3c84a4b75f11c997de066df8f8560f625bbcd5c4e56028ab14790a9`  
		Last Modified: Wed, 28 Jan 2026 03:13:28 GMT  
		Size: 460.7 KB (460721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92b4173f2ccc3d7763f645ed714ae475c75546c8e32d42809393c6735bfb76e`  
		Last Modified: Wed, 28 Jan 2026 03:13:28 GMT  
		Size: 12.6 MB (12588345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155d8d5184393d8afdf1537f0246407a5580073b18591a7159d7ad18c86277a5`  
		Last Modified: Wed, 28 Jan 2026 03:13:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine` - unknown; unknown

```console
$ docker pull python@sha256:02445f57b7392d31498013eac7f4d57aa70dffdc1626979c7fbaf918e6330228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.2 KB (643173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9693c61c9ce0442e8482dd1962945840cc14653c76b2fb14bb7c83205b06aa92`

```dockerfile
```

-	Layers:
	-	`sha256:fa3e007cf9914f412052716fd663091e66788719c8a51f613b8651910e3c7b69`  
		Last Modified: Wed, 28 Jan 2026 03:13:28 GMT  
		Size: 620.4 KB (620370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bf96d5cff0db3f1eb9549e71061a63b34c64120796f31d9c6239f1b69c8b3af`  
		Last Modified: Wed, 28 Jan 2026 03:13:28 GMT  
		Size: 22.8 KB (22803 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine` - linux; arm64 variant v8

```console
$ docker pull python@sha256:ead7f48f0c260d00a1b2c6d0f0dac37b424b670624e7ccbbe1cdca85cd5651e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18112102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d7243c04506d2ca65c54109a84148ce833fa8941d30a107b6438817f048e08`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:20:15 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:20:15 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 03:20:15 GMT
ENV PYTHON_VERSION=3.14.2
# Wed, 28 Jan 2026 03:20:15 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Wed, 28 Jan 2026 03:26:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 03:26:12 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 03:26:12 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217eb6daea6a539678017b05f049f5b9a73edce1373737c5b5f471ff3a13f3cb`  
		Last Modified: Wed, 28 Jan 2026 03:22:58 GMT  
		Size: 463.0 KB (462982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff4bb98855c76b5fb4face7f2ec94fb6ffc5dbc996eb0f5ca50b4823b0e1ee7`  
		Last Modified: Wed, 28 Jan 2026 03:26:19 GMT  
		Size: 13.5 MB (13451780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd27da92a3729fe1d7a383531f4c67ad67db46e9d2f1bfdf8ec04d2ef5658f6b`  
		Last Modified: Wed, 28 Jan 2026 03:26:19 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine` - unknown; unknown

```console
$ docker pull python@sha256:c3672763b200a91183a1db0e6ecbf3f05febcc48f9955afd1c538c2c61cbd7ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.3 KB (640263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7adea4e08ef88438a30543d06bbe386ffe2c4971c4913cbb6dd932ca1eca3c4e`

```dockerfile
```

-	Layers:
	-	`sha256:b30dc9554457aaf9d64d4e5fa8b1e361c5a8eae83b19f1bd1ef8081864a91c9c`  
		Last Modified: Wed, 28 Jan 2026 03:26:19 GMT  
		Size: 617.4 KB (617416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6af6b9598d60fa7681345f417c1235a0d5fac11ef361ce3bf496433084911a2`  
		Last Modified: Wed, 28 Jan 2026 03:26:18 GMT  
		Size: 22.8 KB (22847 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine` - linux; 386

```console
$ docker pull python@sha256:5c6040027c52e3a7fa208ada7c8128c66deaea0848e7b1817c5e422b96907bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17764072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9d1f2afde30117623f9015edde3f29d689f0fe80f3c666137c77cb9dc4ccc1`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:36:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:36:41 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 02:36:41 GMT
ENV PYTHON_VERSION=3.14.2
# Wed, 28 Jan 2026 02:36:41 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Wed, 28 Jan 2026 02:39:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 02:39:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 02:39:11 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387408edad8de8b3c6e410c6529e62fd1b23b834fcab71c87c358ff9eb5c2c1`  
		Last Modified: Wed, 28 Jan 2026 02:39:18 GMT  
		Size: 461.2 KB (461233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a715f4e19a277b4ae6f16cae496bfeb4af5e8b57e8e8b486a9afafcf36311fdf`  
		Last Modified: Wed, 28 Jan 2026 02:39:18 GMT  
		Size: 13.6 MB (13615594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac2822ba5d347180ff6d16ecc6b5310f6a69b37620648d27f95b7f63a9dd09f`  
		Last Modified: Wed, 28 Jan 2026 02:39:18 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine` - unknown; unknown

```console
$ docker pull python@sha256:2de34ea4898f1bf506b56baf6e974774484b18f7240182b317624263ac8ae1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.5 KB (640525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e432421697ac8a8a77a346879ad2e1396c590f21c6eb46497d42e68003ee6f3`

```dockerfile
```

-	Layers:
	-	`sha256:c944f48a85c526e1b46f19d9afbb960d923221b2b76153a622e0e9fa98163993`  
		Last Modified: Wed, 28 Jan 2026 02:39:18 GMT  
		Size: 617.9 KB (617917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf216f5595a0f40988590ee56a03116118c60d7b26cce2288d74522bfe3100f2`  
		Last Modified: Wed, 28 Jan 2026 02:39:17 GMT  
		Size: 22.6 KB (22608 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine` - linux; ppc64le

```console
$ docker pull python@sha256:a2bc3467b870bcccda5f82c254ff3a2a17c078641aa06640afac5e378c762e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18533715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af4f4335253e1ac4f5fb53b9d45d7c82570104a512bd21020ae6940aaac6f22`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:44:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 04:44:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 04:44:00 GMT
ENV PYTHON_VERSION=3.14.2
# Wed, 28 Jan 2026 04:44:00 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Wed, 28 Jan 2026 04:48:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 04:48:36 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 04:48:36 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143f2a7bbfcb07998418b0982b0f9e5f599c0db8360efdf65fc48a08ce71b452`  
		Last Modified: Wed, 28 Jan 2026 04:48:50 GMT  
		Size: 463.5 KB (463503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c64234b66d4d0bcc06391db5a81167c00e1e098dc6dc2530112366dedefb2d`  
		Last Modified: Wed, 28 Jan 2026 04:48:51 GMT  
		Size: 14.2 MB (14240321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43de9a1e3d6aa1af1b2affe24e74b44394f5f819a2526fe06e0b5aac0c4cf4d`  
		Last Modified: Wed, 28 Jan 2026 04:48:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine` - unknown; unknown

```console
$ docker pull python@sha256:5516f1149d6fc4cec0e899cf605c60c6262813e046e030f1934c7149e3611bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.1 KB (640105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd96181d23b8faa43fd3dc9fbe1cbb67bd916e4e8540ee21dac2a0be40217d0`

```dockerfile
```

-	Layers:
	-	`sha256:b0d33903213cbf9169ebb5f8449346d34e722d24416d69eb37c75cd3ed07680b`  
		Last Modified: Wed, 28 Jan 2026 04:48:51 GMT  
		Size: 617.4 KB (617369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d6572bc385f43666eceb66abcd7872a0113a56cb41a3dc4df36b0cf117abf1f`  
		Last Modified: Wed, 28 Jan 2026 04:48:50 GMT  
		Size: 22.7 KB (22736 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine` - linux; riscv64

```console
$ docker pull python@sha256:403046ef91f7cc62a19595e47edce80de469dd2a4c7c81d656de57acb7d43111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17528974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6e23ceb02fbdc3f29a3aa3b5c637674687f0a1413e802566ee5d130d68fb09`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:56:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Dec 2025 05:56:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 19 Dec 2025 05:56:43 GMT
ENV PYTHON_VERSION=3.14.2
# Fri, 19 Dec 2025 05:56:43 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Fri, 19 Dec 2025 07:19:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 19 Dec 2025 07:19:58 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 19 Dec 2025 07:19:58 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c1297d0b47f8cc996fa306111fc37eee4492b207584fc90d6151f5b00513f5`  
		Last Modified: Fri, 19 Dec 2025 06:38:01 GMT  
		Size: 461.2 KB (461189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac744c1eb54ba37619f7bf7648e886af8c31a724a7422d7c56c63dd25c48da59`  
		Last Modified: Fri, 19 Dec 2025 07:20:45 GMT  
		Size: 13.5 MB (13483595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cb6cdfe6728bc08af8b708a5e430c8483cc08e4b7c47f4e5e41c8e8664caa5`  
		Last Modified: Fri, 19 Dec 2025 07:20:42 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine` - unknown; unknown

```console
$ docker pull python@sha256:3647126b771967498a49facbd6b7e0e6d26f7ee4fde4e145f7800b579023da6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.1 KB (640102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39cb51d118e44721509aba7898c8e5bc507939e98872ffaeaca454533fc03950`

```dockerfile
```

-	Layers:
	-	`sha256:62523b6850e0402bd6823463ef403a97a5fe353f892d8dd3ed6f97f16d43cffc`  
		Last Modified: Fri, 19 Dec 2025 07:20:43 GMT  
		Size: 617.4 KB (617365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2ff63d23e31b115aa04922010c47050f7f89aa4202c398208f754f35756bb84`  
		Last Modified: Fri, 19 Dec 2025 07:20:42 GMT  
		Size: 22.7 KB (22737 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine` - linux; s390x

```console
$ docker pull python@sha256:1793e10627303794a46534ab2c2dc72e7de9465538dd7926cee3c0dc81c83bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18034527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a70c52b6ea7828d3ce3d96559aa96f115a7c0f1caa61336927cd9cde61203f`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 02:45:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 02:45:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 18 Dec 2025 02:45:06 GMT
ENV PYTHON_VERSION=3.14.2
# Thu, 18 Dec 2025 02:45:06 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Thu, 18 Dec 2025 03:04:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 18 Dec 2025 03:04:03 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 18 Dec 2025 03:04:03 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:04 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4b1699aa656b23eebe8081f75dec9a272ed29e847d1ea394e07fd40420d6c4`  
		Last Modified: Thu, 18 Dec 2025 02:54:46 GMT  
		Size: 461.7 KB (461734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9accacf7a821986d4fda2a0fea3ae7ebe664f2fc9b277edbe9a0888e6082e8`  
		Last Modified: Thu, 18 Dec 2025 03:04:34 GMT  
		Size: 13.8 MB (13848232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31477603734b9badbcbde1fcc36e9d08bee6a50006d2ac7d1933f95addcb1bf2`  
		Last Modified: Thu, 18 Dec 2025 03:04:28 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine` - unknown; unknown

```console
$ docker pull python@sha256:210b7507727d1bb39c8d10a95c3b5759b922902a761ea61bc34262edd9562bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 KB (639976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308ab683c5b1a3ed37bb3f39c00d4ad864dfb53266462489069682ed287f28ec`

```dockerfile
```

-	Layers:
	-	`sha256:9c4ae6fa11d5dd0fb9477f074d60a54b341d6015e93ef7ee752ae9296d3f229e`  
		Last Modified: Thu, 18 Dec 2025 03:04:29 GMT  
		Size: 617.3 KB (617311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a30a8dee995141441b785c482d595aa5502cfe90fc87a67fd9fb3ee9982921b`  
		Last Modified: Thu, 18 Dec 2025 03:04:29 GMT  
		Size: 22.7 KB (22665 bytes)  
		MIME: application/vnd.in-toto+json
