## `hylang:python3.10-alpine3.22`

```console
$ docker pull hylang@sha256:a9dbd381b2c30866f57898116de0683f4757f87bc5dd791df77307fc2d79656c
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

### `hylang:python3.10-alpine3.22` - linux; amd64

```console
$ docker pull hylang@sha256:4fbd5f0d865be58d4e33e013f076e3de7f82213f600e28bc33434e8bf1148c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24823914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf62861dd5cc4d02a6a27ed21571513b465670a20148efaae6c8da2af770361`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:15:46 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:15:46 GMT
ENV LANG=C.UTF-8
# Wed, 04 Feb 2026 20:15:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:15:46 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Feb 2026 20:15:46 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 04 Feb 2026 20:15:46 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 04 Feb 2026 20:29:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:29:10 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:29:10 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:12:49 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:12:49 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:12:49 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:12:49 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1018f8bea1bb9998f3aa7379c7ff0a3e8530f3c71064a445f2d0cb382ea159c`  
		Last Modified: Wed, 04 Feb 2026 20:20:57 GMT  
		Size: 457.1 KB (457062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a35c85c45b075b48d7893591409e7dee30343cd5ba8eed4a9bba4a75af6080`  
		Last Modified: Wed, 04 Feb 2026 20:29:17 GMT  
		Size: 15.4 MB (15387039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0c447ec76b67a0cbbfe72735421cc97a0e99bfed8910864e242a416c549a6e`  
		Last Modified: Wed, 04 Feb 2026 20:29:17 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3614b557e333c845426c7e46133a499ce406ee1355266e7f352c81e19bcc2919`  
		Last Modified: Wed, 04 Feb 2026 21:12:56 GMT  
		Size: 5.2 MB (5174690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:be71e55df129a2cad9d55b6f47f9aefba9d498a35c24ee56551e1d6c6cddd60e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.8 KB (706770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2e237de7aed702572d79a740fde06ecba82fb65049c55d1c68afbb120d7b17`

```dockerfile
```

-	Layers:
	-	`sha256:56394028d0c00c9273ba5a6237e3c732be93f287a6c62cef5171bf6bdc047287`  
		Last Modified: Wed, 04 Feb 2026 21:12:55 GMT  
		Size: 698.7 KB (698667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f34cad9317b8dfd87eeb970a858e076ded1773acb91ce473dcb6e97cd80060`  
		Last Modified: Wed, 04 Feb 2026 21:12:55 GMT  
		Size: 8.1 KB (8103 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine3.22` - linux; arm variant v6

```console
$ docker pull hylang@sha256:7f2231a42c7800ce5c0e43fc7b661478ad3edbf16f07d8f3d2e036f440ce0d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24104273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d133d3db6b2b37d47ef335153cde94f568d8fa15471d020699a459c646eadf`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:35:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:35:06 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 03:35:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 03:35:06 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 28 Jan 2026 03:35:06 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 28 Jan 2026 03:35:06 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 28 Jan 2026 03:38:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 03:38:56 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 03:38:56 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 04:47:03 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 04:47:03 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 04:47:03 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 04:47:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fe9d47b9f7882221fa593eb039a7ca4cfc5a4f9bb3083a5cd64de43deb870f`  
		Last Modified: Wed, 28 Jan 2026 03:39:01 GMT  
		Size: 457.9 KB (457886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fbb6fd61aa1b988b6ec6396828c10041ca4e533bb07f0600408d6cbf73e621`  
		Last Modified: Wed, 28 Jan 2026 03:39:02 GMT  
		Size: 15.0 MB (14966520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88db186576e837d4534800ee423d4f9d2d334dd78b82ab0a35794ee4818cbd7f`  
		Last Modified: Wed, 28 Jan 2026 03:39:01 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bb0badf18c27d40414f90ff47dcfe972605641cceaddac16c1249f0f8cf773`  
		Last Modified: Wed, 28 Jan 2026 04:47:08 GMT  
		Size: 5.2 MB (5174573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:ff5ef323dfe2b54ad361b85d5551b575ba4fcb4cd8a7cdf8f5e0a7a84e126eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 KB (7968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49e900eb0fcdde9bdefdf5417eb6e8a4bc100b24644dad75af25a78183e3127`

```dockerfile
```

-	Layers:
	-	`sha256:03a7833b87cb1e5b198abf4cb3faf343ed222e86ffe694abd167018b2825e8d8`  
		Last Modified: Wed, 28 Jan 2026 04:47:08 GMT  
		Size: 8.0 KB (7968 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine3.22` - linux; arm variant v7

```console
$ docker pull hylang@sha256:00f0e5961adb75e11fad437da0901e213b7952a1b8ee552e79b637b131afbe42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23420744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929f694b81c878e3f6bfade0e2ae6d89fcf87a8fe155f1d8cfef0cbf1189be2b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:36:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:36:19 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 03:36:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 03:36:19 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 28 Jan 2026 03:36:19 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 28 Jan 2026 03:36:19 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 28 Jan 2026 03:40:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 03:40:17 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 03:40:17 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 04:31:16 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 04:31:16 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 04:31:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 04:31:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c3c8f4d62a688051f65611d09270ef6aa28918e7ff681b1de4023794ac8b58`  
		Last Modified: Wed, 28 Jan 2026 03:40:24 GMT  
		Size: 457.1 KB (457071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40ecb3f8a6d9cfdc5b901df304bf855f159cc471e97d9c4f79b3df20d668ffa`  
		Last Modified: Wed, 28 Jan 2026 03:40:24 GMT  
		Size: 14.6 MB (14565185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef3754a6acaa4397cac3f76de90d09ff62cf047749b390601b64c00eab2ec24`  
		Last Modified: Wed, 28 Jan 2026 03:40:24 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89996b9e6b0e75a8bcd6e575ce22d68db27fe196bbccf31501dd8c08558bcb5d`  
		Last Modified: Wed, 28 Jan 2026 04:31:23 GMT  
		Size: 5.2 MB (5174610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:43bfd3cdb1a8aff4ebffc4f7023d9f8dd4aeb875c218e8aaa731f29efebe6ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.9 KB (709875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ef75f5e5e4504ebc32a4e0ee41faaf1d58b2700dfcc658d8b2f3beda871f6b`

```dockerfile
```

-	Layers:
	-	`sha256:37cf6177b9ad2e13cf3a90a042f2d31fb590f30e5a26ab9626276d1ecdea5884`  
		Last Modified: Wed, 28 Jan 2026 04:31:22 GMT  
		Size: 701.7 KB (701693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e87d40d16f150059cbfa353282a0694f0b65e297b5cf958ad6ee770c0d56611c`  
		Last Modified: Wed, 28 Jan 2026 04:31:22 GMT  
		Size: 8.2 KB (8182 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:a0ed7b6696dc34825446c7bcea79f13ce82a73d76a0185bab56b7015c2c1a895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25217525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30608107acf1a3f2ca0d834811e0c4803e288d828dd61a03cb22b36e150d5a58`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:19:15 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:19:15 GMT
ENV LANG=C.UTF-8
# Wed, 04 Feb 2026 20:19:15 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:19:15 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Feb 2026 20:19:15 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 04 Feb 2026 20:19:15 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 04 Feb 2026 20:36:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:36:35 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:36:35 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:11:08 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:11:08 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:11:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:11:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ac648a6de96948970e283b39f46d0b21290c6c503caffc62a0c953617a50de`  
		Last Modified: Wed, 04 Feb 2026 20:25:31 GMT  
		Size: 459.2 KB (459160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421b12fc6746d9b1297b4fe9cffa9b845c201a0ecaa3a777f927fc2665617948`  
		Last Modified: Wed, 04 Feb 2026 20:36:42 GMT  
		Size: 15.4 MB (15443555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bf829e0983414cd6eae0be19e17220fe7d83df14800c1ef348f50d95c064d8`  
		Last Modified: Wed, 04 Feb 2026 20:36:42 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558b1e7c455c52f19c5313f8882a9ec49441c3237525a40d4999f32f29e07bb5`  
		Last Modified: Wed, 04 Feb 2026 21:11:14 GMT  
		Size: 5.2 MB (5175042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:766221938c4d43d99f95370e44284cc653ce2f42ebe8241f23244fe19d8b966b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.9 KB (706930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84aaf9223b0539dd1b87282a22eb41106e2aedc1cfe81eb49bb908bb408ea9bb`

```dockerfile
```

-	Layers:
	-	`sha256:3bf86e6e78f79982f8f9cb6a257b0368c2127aa1ffcec1cf5bb391d260d8f59e`  
		Last Modified: Wed, 04 Feb 2026 21:11:14 GMT  
		Size: 698.7 KB (698723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2179f1a14d3286a5d088e1722d5cb43457b266bbd9700ee5fa65e5e47418122a`  
		Last Modified: Wed, 04 Feb 2026 21:11:14 GMT  
		Size: 8.2 KB (8207 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine3.22` - linux; 386

```console
$ docker pull hylang@sha256:723d9878943bcff907220a2b5c1c42a2b450c3ef6df30022db8a8fc63b976bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24879239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f6097f6c32911421142302d8bd2ef65252a9407b01e1a1473909e650f7d7d5`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:29:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:29:16 GMT
ENV LANG=C.UTF-8
# Wed, 04 Feb 2026 20:29:16 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:29:16 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Feb 2026 20:29:16 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 04 Feb 2026 20:29:16 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 04 Feb 2026 20:32:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:32:16 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:32:16 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:07:15 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:07:15 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:07:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:07:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1c7ce8ca77611e854f9035fcd02d77482960be696152a162fa4f8627a42f65`  
		Last Modified: Wed, 04 Feb 2026 20:32:22 GMT  
		Size: 457.5 KB (457501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9421aa5499c6c414ba1bcd2709b1df77176994b04a0c8d6ce3a85c6822427704`  
		Last Modified: Wed, 04 Feb 2026 20:32:23 GMT  
		Size: 15.6 MB (15625904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681c5bd85ae8f9cbf92755efc0bf4119f09f32338783be546ac41c6b5730253b`  
		Last Modified: Wed, 04 Feb 2026 20:32:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83088c67e3da2e3a97ac284f0e524a2e1bc41faaaebfc62d91d7f6e60abd429c`  
		Last Modified: Wed, 04 Feb 2026 21:07:21 GMT  
		Size: 5.2 MB (5174855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:d65396386505c6e440b8ab8826da22dc5552f492e1b66428752c6c42448be5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.7 KB (706712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08691acfe4dd5194ae9d0345171ae0b91bd2614b1c5f61742ba34359458f155d`

```dockerfile
```

-	Layers:
	-	`sha256:6568c6e371b80c264acd1c18a6dc32719ae38ca2d37c4a3d599bddca54a7fb6a`  
		Last Modified: Wed, 04 Feb 2026 21:07:21 GMT  
		Size: 698.6 KB (698642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db1ee485dec0a3a66951e2a919e3c352a7ebd1242930b3f14c53c4c25c4c5f41`  
		Last Modified: Wed, 04 Feb 2026 21:07:20 GMT  
		Size: 8.1 KB (8070 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine3.22` - linux; ppc64le

```console
$ docker pull hylang@sha256:a67bcae2c93982b6508f71a8553dfb45b2e0f013047b3944dbd404f4b64d7f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25453200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d6aa9debc1346a9231340bf2126e5f665d1502bc11963ee42cdad5382c6659`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 05:01:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 05:01:19 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 05:01:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 05:01:19 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 28 Jan 2026 05:01:19 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 28 Jan 2026 05:01:19 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 28 Jan 2026 05:24:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 05:24:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 05:24:20 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 07:10:31 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 07:10:31 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 07:10:31 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 07:10:31 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a1124713274b84816a9b9a21d6590700313917e03834ff9f07f7a03392d032`  
		Last Modified: Wed, 28 Jan 2026 05:09:44 GMT  
		Size: 459.6 KB (459583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9b50986b98c23dc9989f0e2c485364aa72392ea78091fa03ba53a82699f1b0`  
		Last Modified: Wed, 28 Jan 2026 05:24:36 GMT  
		Size: 16.1 MB (16084461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a69e8f12337d5813764152be808962bf59c6bf4506ddd35adce7c2fabc0d28`  
		Last Modified: Wed, 28 Jan 2026 05:24:36 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81de07a7fb9ac3f94989331c81b692f0e053f8553fe4466b1ca2b0a6b4aa404`  
		Last Modified: Wed, 28 Jan 2026 07:10:56 GMT  
		Size: 5.2 MB (5174611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:21696f2fe6184918ee271fb62927922a8f70bc2dc07b2d0a04a2d3ae1a27c867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.9 KB (704897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aeebc74070e1c4e2737410ca52c5fd23dfde402d521ad381493bacdd6439fb9`

```dockerfile
```

-	Layers:
	-	`sha256:297b17a558885045a6a29e617f0edb6ee1a2f509e4c1349b845eb6eee80b919b`  
		Last Modified: Wed, 28 Jan 2026 07:10:56 GMT  
		Size: 696.8 KB (696750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6b07c3a67eac37812ab36815db9c81af547b693f4f4095a046aa7e2ac9f0b37`  
		Last Modified: Wed, 28 Jan 2026 07:10:55 GMT  
		Size: 8.1 KB (8147 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine3.22` - linux; riscv64

```console
$ docker pull hylang@sha256:29acfebc1c81090a844e9d8073faa5bc4281c87e32b7f62d381877a419505a3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24548599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d210b1b7e567b2704b1e09c6c90807c946a8b470477be35b8bcba63396fd76`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Fri, 30 Jan 2026 00:03:32 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 00:03:32 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 00:03:32 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 30 Jan 2026 00:03:32 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 30 Jan 2026 00:03:32 GMT
ENV PYTHON_VERSION=3.10.19
# Fri, 30 Jan 2026 00:03:32 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Fri, 30 Jan 2026 02:33:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 30 Jan 2026 02:33:46 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 30 Jan 2026 02:33:46 GMT
CMD ["python3"]
# Sun, 01 Feb 2026 06:28:26 GMT
ENV HY_VERSION=1.2.0
# Sun, 01 Feb 2026 06:28:26 GMT
ENV HYRULE_VERSION=1.0.1
# Sun, 01 Feb 2026 06:28:26 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 01 Feb 2026 06:28:26 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1156d8af98cc33f4884dab56eabe3cb3caa5a48e17b9027d8523aa48a49480b2`  
		Last Modified: Fri, 30 Jan 2026 00:36:06 GMT  
		Size: 457.4 KB (457409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822a202e685e4587eac854010e6fd036ae7040fd9eebb7e8ae92bfe41964b0f6`  
		Last Modified: Fri, 30 Jan 2026 02:34:37 GMT  
		Size: 15.4 MB (15397363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3588f602eb5aba53686685b7f3546279753fadba16699e74f588b9cef4d56f`  
		Last Modified: Fri, 30 Jan 2026 02:34:35 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c87576238170dcdedf5294960c95c1613a3ce5c977cf886f69cb9fae5e38b03`  
		Last Modified: Sun, 01 Feb 2026 06:29:08 GMT  
		Size: 5.2 MB (5176155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:d61d9fd1041266afa8eeaa74825003918d3ee2efbba394ce20636301066c3577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.9 KB (704893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d8a905dcc1566a68ce1ecaceb538d640886b17c2e991af05fbdaa85ccd5e35`

```dockerfile
```

-	Layers:
	-	`sha256:d6bf0361938236af79a07c7fb2d35b4602877ba86671078d3cc56b0e93ff152f`  
		Last Modified: Sun, 01 Feb 2026 06:29:07 GMT  
		Size: 696.7 KB (696746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df173ef30308099b887dd3799434864e130d76a6cd1e314f90b9d8c4f925036b`  
		Last Modified: Sun, 01 Feb 2026 06:29:07 GMT  
		Size: 8.1 KB (8147 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine3.22` - linux; s390x

```console
$ docker pull hylang@sha256:2b16c7303faf162c55049e99fb5c93b6580a14c76c5608e7442c7b4b039b1527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25081321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a060a61617fa5846a73dde9af3c0fb9f9c694d1d40cdb96ae12c9f2632c3e57d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:43:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 06:43:43 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 06:43:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 06:43:43 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 28 Jan 2026 06:43:43 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 28 Jan 2026 06:43:43 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 28 Jan 2026 06:47:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 06:47:19 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 06:47:19 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 07:29:15 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 07:29:15 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 07:29:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 07:29:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce6f78c7148df03b26cbeffe5c6e54aa640b27e5d2aab0cb3588feb7071a6a7`  
		Last Modified: Wed, 28 Jan 2026 06:47:30 GMT  
		Size: 458.0 KB (458025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c0071ea5c269432b726076086a9cf5004b766a5079a0356be7e495f399a75`  
		Last Modified: Wed, 28 Jan 2026 06:47:30 GMT  
		Size: 15.8 MB (15798099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98be9b687d42e5f5fc04fd95a94e024d22b65157529c5d02d5d6e504b753ea03`  
		Last Modified: Wed, 28 Jan 2026 06:47:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b248dfcecb096623e313263a657c4dd97b07c28347445813bca075f3490e42c1`  
		Last Modified: Wed, 28 Jan 2026 07:29:25 GMT  
		Size: 5.2 MB (5174514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:99bb543de18a2aec11086f4a7bb536c0d0879dda2e1833dce9c672c757745823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.8 KB (704818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980dbce606342cb6efc364a2679825223d54096bad5689fba0096b99be335385`

```dockerfile
```

-	Layers:
	-	`sha256:d6fe3f2a42782e0158b5381fb49d06f0eeaa1aae48a3aaf40760fc4e1dded747`  
		Last Modified: Wed, 28 Jan 2026 07:29:25 GMT  
		Size: 696.7 KB (696716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:944f79404f0e792bb0180887d967c46ac1c456573dcae91ec49933196720d8e1`  
		Last Modified: Wed, 28 Jan 2026 07:29:25 GMT  
		Size: 8.1 KB (8102 bytes)  
		MIME: application/vnd.in-toto+json
