## `hylang:1-alpine3.22`

```console
$ docker pull hylang@sha256:636b3bd2adbbc0618691129662fea6bfb0cd69e4a6bdf22fa07d67890c30a746
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

### `hylang:1-alpine3.22` - linux; amd64

```console
$ docker pull hylang@sha256:4472466c650690106cc10e73945d0a936fe78c2814bab87ff385f4aa6ab446fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23160976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b695bb860384f2ce8f417b7ee785de8d4fda3a69cfcb33a92fbd6154477c63b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:04:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:04:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:04:01 GMT
ENV PYTHON_VERSION=3.14.3
# Wed, 04 Feb 2026 20:04:01 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Wed, 04 Feb 2026 20:09:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:09:31 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:09:31 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:12:10 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:12:10 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:12:10 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:12:10 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721411f3124f66c19438187aebf5e433f3863d4f479d6ddde0dde13b5855b487`  
		Last Modified: Wed, 04 Feb 2026 20:06:45 GMT  
		Size: 457.0 KB (457048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1fae1463515589ad88c0082498abcdbdb8fd47d59681f42557be54c64fd34b`  
		Last Modified: Wed, 04 Feb 2026 20:09:37 GMT  
		Size: 13.3 MB (13310552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb035045ac3e7de6827ce89c22e2d5487baa10dd88042b36c05a56de1633a5a8`  
		Last Modified: Wed, 04 Feb 2026 20:09:37 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721c8ec1b9bda9f7408830750d1e51812d0cf63c55fb267fa67f2067ba46ef17`  
		Last Modified: Wed, 04 Feb 2026 21:12:16 GMT  
		Size: 5.6 MB (5588251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:63b44d146dd2436992561bf5f07f12c309059f76a5246a09f5016525138f4198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.9 KB (634916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893aa5bb5d6a61552123a6644727c667cdf39b1f98c34cb3f9d664a2ec555721`

```dockerfile
```

-	Layers:
	-	`sha256:66370a21958d19b96496a0c03b2c09aa059e902425b25d7114bf312086db0e90`  
		Last Modified: Wed, 04 Feb 2026 21:12:16 GMT  
		Size: 625.6 KB (625632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:904c2e3c23fa341f07c840be1048d0b3df3ceb390eff30a2ffdbf9d899b8085c`  
		Last Modified: Wed, 04 Feb 2026 21:12:16 GMT  
		Size: 9.3 KB (9284 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.22` - linux; arm variant v6

```console
$ docker pull hylang@sha256:a36bd0c1d9277813274671269dfc4b7d0209e7b4762574a7e0674f2e1c4d1037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.4 MB (22447975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b838d72d57bcb5e4a77e7f5bdfe7fe811d1dc3daadb0053f6325eae5ceddac63`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:04:10 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:04:10 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:04:10 GMT
ENV PYTHON_VERSION=3.14.3
# Wed, 04 Feb 2026 20:04:10 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Wed, 04 Feb 2026 20:06:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:06:48 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:06:48 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:30:20 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:30:20 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:30:20 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:30:20 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f78bfc4a1614cf70b6cfc2bc7601efb54f3932c97203186a93a378bd9a5096f`  
		Last Modified: Wed, 04 Feb 2026 20:06:53 GMT  
		Size: 457.9 KB (457871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7656c0046db4eec187618ac0eec4ddf9195e2ab89d28d6c2a32f8e027b8ba6`  
		Last Modified: Wed, 04 Feb 2026 20:06:54 GMT  
		Size: 12.9 MB (12896436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68043514b46443fc64e91b423b324f0b07d53b2e791d80af82f84ed189ea377`  
		Last Modified: Wed, 04 Feb 2026 20:06:54 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fc005a3bf7eaf2009198deb186c172cb4576b96c1ad7312df58472d32abd53`  
		Last Modified: Wed, 04 Feb 2026 21:30:24 GMT  
		Size: 5.6 MB (5588375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:e7647e546d026cf5004f924abc3a5ca57cbcd45929a2e46eda996dafe96b2bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfddae5480b95c1b45eba93183ff8cec20a6b2d135f4173a94dd846577af6a4`

```dockerfile
```

-	Layers:
	-	`sha256:c178f380fe6b2c670ce16b5d6fc611d26fb1f4e39ca29de4879e466d185c1ce8`  
		Last Modified: Wed, 04 Feb 2026 21:30:23 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.22` - linux; arm variant v7

```console
$ docker pull hylang@sha256:fc32faf1e3dd9d7cc77eb6395b508a12e0dd9f461dd9ea809051acc3f34e9860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21786776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc55edf0d32342d211bb000611d53535256e0868b3cca46a57fc4d7a39aee5a2`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:14:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:14:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:14:36 GMT
ENV PYTHON_VERSION=3.14.3
# Wed, 04 Feb 2026 20:14:36 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Wed, 04 Feb 2026 20:17:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:17:17 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:17:17 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:31:58 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:31:58 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:31:58 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:31:58 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a11c4ee6a0eeb47ddd111e41db1b3a70cd99b0e2f908683381b3b7ee8bd1bd`  
		Last Modified: Wed, 04 Feb 2026 20:17:24 GMT  
		Size: 457.1 KB (457072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1faddf0e6c45d97f11723364278ac135d0ce523ee3df1a2415017ceea86bef11`  
		Last Modified: Wed, 04 Feb 2026 20:17:24 GMT  
		Size: 12.5 MB (12517553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ad91636b32da31d9235879a2a4ac6487d0d5b7805059524033f211829ecca6`  
		Last Modified: Wed, 04 Feb 2026 20:17:24 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2154beea3d76ccfc0190ca7f5bc0c803a81fe567bcff538a136141a1b5ee29ad`  
		Last Modified: Wed, 04 Feb 2026 21:32:04 GMT  
		Size: 5.6 MB (5588272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:43ec1def8ec9876030b698280997ff201898fe59042c29d8d9c93f3bcb4930e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.1 KB (638085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512569b06c28c74af0d816fec7944a3044fb2a48e301545cd02cf04ba6db50a5`

```dockerfile
```

-	Layers:
	-	`sha256:9bb7499e5c636700ffa6d1e06413fd0ae9adb1375a761cf55c6609ca2a98758d`  
		Last Modified: Wed, 04 Feb 2026 21:32:04 GMT  
		Size: 628.7 KB (628690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d62a6d33c2b830add4335789577f91983c07b0b8b0d2e165e1a210356c394dca`  
		Last Modified: Wed, 04 Feb 2026 21:32:04 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:91abbaefa57e4a77f0f2b70266b06433708bb4d31b685819b2ea70c69293ec5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23479776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c84e289a5b4dfdd4bf4d50abcd1a20f3ae6b66358ca21470d4a072ecdd91f2`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:04:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:04:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:04:08 GMT
ENV PYTHON_VERSION=3.14.3
# Wed, 04 Feb 2026 20:04:08 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Wed, 04 Feb 2026 20:09:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:09:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:09:29 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:10:07 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:10:07 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:10:07 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:10:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1a6b74439e8677c9460b5bc6d4c97d29ea7073cb8f640a83602710d484a3db`  
		Last Modified: Wed, 04 Feb 2026 20:06:48 GMT  
		Size: 459.2 KB (459152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ad5cce29c608b70ea8591757c55b123ac98625282a6997b030a699d016a2cd`  
		Last Modified: Wed, 04 Feb 2026 20:09:36 GMT  
		Size: 13.3 MB (13292565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c663bc312c61e55d4cb3ddffe172f4844a63850a3e32e4f3e5301baef853ab`  
		Last Modified: Wed, 04 Feb 2026 20:09:36 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27904bba2c7f6093799936f6d9d0e0806dc45e20e4380b508cd1a7e44795bde8`  
		Last Modified: Wed, 04 Feb 2026 21:10:13 GMT  
		Size: 5.6 MB (5588291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:7826f4fe9e7552ebc839baee6af9a85b30ab04b6003d7a3e2ac194cb5aefa840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.2 KB (635170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8e428f4782ea924d497e557a3bee36877659c313f6ef652b92a845db860ff4`

```dockerfile
```

-	Layers:
	-	`sha256:127468b7313aa1249a5e8afa0e452844ef52d488bb502ddf08e7daae4b257a2d`  
		Last Modified: Wed, 04 Feb 2026 21:10:13 GMT  
		Size: 625.7 KB (625736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9565c0dfeb6866f0f494e8d59bbe8c2c8d9778137df7203de950d4eac2edbea`  
		Last Modified: Wed, 04 Feb 2026 21:10:13 GMT  
		Size: 9.4 KB (9434 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.22` - linux; 386

```console
$ docker pull hylang@sha256:2a6031680ecc5e8720b43549b60b9c7ffcef6615b2598032acc8bc292fe8ba29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23255913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077c006eeb658bfa25191c026b36086a8a83ce5c2727ae84ef23dd3df50b1f98`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:07:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:07:09 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:07:09 GMT
ENV PYTHON_VERSION=3.14.3
# Wed, 04 Feb 2026 20:07:09 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Wed, 04 Feb 2026 20:09:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:09:33 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:09:33 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:06:40 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:06:40 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:06:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:06:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8dc36f4e023c67e4ac5ff400f4b7cd6f9e16799be1d85818ef71053e761266`  
		Last Modified: Wed, 04 Feb 2026 20:09:39 GMT  
		Size: 457.5 KB (457509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2d380c6f5618e3fd1fc650b3d6aa679e3459a4495417cff8d617bf093e8d38`  
		Last Modified: Wed, 04 Feb 2026 20:09:39 GMT  
		Size: 13.6 MB (13589139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e181a523de1cee6ea6f28f7076a60a376948871e68fb3105230de0ae847184`  
		Last Modified: Wed, 04 Feb 2026 20:09:39 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fef8fddbddbc74bbd717ab33803149ff8113b41f200da44114cbe86d73f41c`  
		Last Modified: Wed, 04 Feb 2026 21:06:46 GMT  
		Size: 5.6 MB (5588284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:14e9a9881d8c30b50dc508b20515e3033ff0a9c8bcaa29a4968aff045ac866df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.8 KB (634819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66f4bb923029fad624fbca8a8fe2b580742c2a27aa50cbd6ecb8d566b366705`

```dockerfile
```

-	Layers:
	-	`sha256:f459d479161dc8a1fd6ac620277f048313632d08f0dc08d0cf029bb2d2b3818b`  
		Last Modified: Wed, 04 Feb 2026 21:06:46 GMT  
		Size: 625.6 KB (625587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aee4991451d8d808d3c92a9954ea32931f00af63414d93c4687a35c8bc7122d8`  
		Last Modified: Wed, 04 Feb 2026 21:06:46 GMT  
		Size: 9.2 KB (9232 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.22` - linux; ppc64le

```console
$ docker pull hylang@sha256:c207ae1cfd26b9019da6a2e9ad72027a6725807d1b956cb07bbce4059502cc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23873764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4cb7aed65d022d3a3b53a823c0226d1b8235320ea64241915bce17244357ff`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:42:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:42:04 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:42:04 GMT
ENV PYTHON_VERSION=3.14.3
# Wed, 04 Feb 2026 20:42:04 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Wed, 04 Feb 2026 21:29:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 21:29:31 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 21:29:31 GMT
CMD ["python3"]
# Thu, 05 Feb 2026 01:35:37 GMT
ENV HY_VERSION=1.2.0
# Thu, 05 Feb 2026 01:35:37 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 05 Feb 2026 01:35:37 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 05 Feb 2026 01:35:37 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe4825cc83b433a0dc6254fcfa84fd1a2be06c6d2420aebf146e6e850a62030`  
		Last Modified: Wed, 04 Feb 2026 20:46:42 GMT  
		Size: 459.6 KB (459577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ad3d38cd9d61c041d1d805eed57e62f372ae64a9c0ba2f509aed949fdb07a8`  
		Last Modified: Wed, 04 Feb 2026 21:29:45 GMT  
		Size: 14.1 MB (14091275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64bcc352f77caf11d3ba9409cd1ab9ab7e67b1481e7d8c2b138e3538ad45bff7`  
		Last Modified: Wed, 04 Feb 2026 21:29:44 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330fd805eb78023da7a2602c9c03eea1e7aee69a5a4fb673d631073736da78b8`  
		Last Modified: Thu, 05 Feb 2026 01:35:51 GMT  
		Size: 5.6 MB (5588366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:423ec4e46d4bf0d18bdfef6d6c7f4f9d353450423bb4658290d8cd2798f44b71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.1 KB (633091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d502057c537813629b3fa1b242a61692c53d529aebe9763abc1b769b36073c`

```dockerfile
```

-	Layers:
	-	`sha256:e034ed411b45533ec00710d19c27ec049968cf03fcfc0776a19fa05bde72b482`  
		Last Modified: Thu, 05 Feb 2026 01:35:51 GMT  
		Size: 623.7 KB (623739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c88bb6e933c8632e63428eafdd4732a262befc1d1e1bee31e1c58113ee134c70`  
		Last Modified: Thu, 05 Feb 2026 01:35:50 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.22` - linux; riscv64

```console
$ docker pull hylang@sha256:0745520200f0d489b2815fd2857254d7f2c8a291cb1e6ec595920909af95c19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23020090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9211cef45bc8335ee7daca38363e3d60e7c9d17a1b20e31aff787156b4fbbb`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 20:12:03 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 20:12:03 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Jan 2026 20:12:03 GMT
ENV PYTHON_VERSION=3.14.2
# Thu, 29 Jan 2026 20:12:03 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Thu, 29 Jan 2026 22:10:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 29 Jan 2026 22:10:33 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Jan 2026 22:10:33 GMT
CMD ["python3"]
# Sun, 01 Feb 2026 05:57:11 GMT
ENV HY_VERSION=1.2.0
# Sun, 01 Feb 2026 05:57:11 GMT
ENV HYRULE_VERSION=1.0.1
# Sun, 01 Feb 2026 05:57:11 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 01 Feb 2026 05:57:11 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f09c06bcb0cd7a2f20a63c8a8409f2c94c296872976bd8ac6cc3232892a618e`  
		Last Modified: Thu, 29 Jan 2026 20:49:52 GMT  
		Size: 457.4 KB (457400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6ec509f0e99d1489b0a03ae91d2d5485099c5badf646de1bea9df8bd4eea4a`  
		Last Modified: Thu, 29 Jan 2026 22:11:20 GMT  
		Size: 13.5 MB (13457582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615e9412ef6f8b08fae02173dca9ddfdad0b33b427b860c371e0d45f0443d664`  
		Last Modified: Thu, 29 Jan 2026 22:11:17 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcb0c94593c9d8e3a8112c1652266d1810bfdcbfdf1a0f350dd95aa051b4b71`  
		Last Modified: Sun, 01 Feb 2026 05:57:51 GMT  
		Size: 5.6 MB (5587436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:abb098067a4047f1dd84b0a80d494714d8c859379d00f58a9058f5f2a9e64a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.1 KB (633086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b776abe457a1c05a8c9391669ddfcb7752bf3785b8c109b33cc2b5615338b6e2`

```dockerfile
```

-	Layers:
	-	`sha256:9ee22e6979bbec14c27fca3a72ae85033b741b42497310bb729b6e2a60aa7c82`  
		Last Modified: Sun, 01 Feb 2026 05:57:51 GMT  
		Size: 623.7 KB (623735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cb19d833723caed36576c983c57d29ad9dcbded99a929e652e8284fa31a0850`  
		Last Modified: Sun, 01 Feb 2026 05:57:51 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine3.22` - linux; s390x

```console
$ docker pull hylang@sha256:1ef94da82b380a2312b062d9314b70ba1bdc1ae3f253932044baf465a93e87b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23508546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc6cc360adf9fae52734a5986b95c4e0810c7deb2fda3e8b5a17f24a763f122`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:25:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:25:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:25:19 GMT
ENV PYTHON_VERSION=3.14.3
# Wed, 04 Feb 2026 20:25:19 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Wed, 04 Feb 2026 20:28:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:28:32 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:28:32 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:37:06 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:37:06 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:37:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:37:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541a0e405e1817999737b4d25b91276ba7e9aff94d31b0fbf798b79e9f8b8bc2`  
		Last Modified: Wed, 04 Feb 2026 20:28:42 GMT  
		Size: 458.0 KB (458035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ce91076a711c4b432588d74997082ef57f4996332c7754d0be0def115a0f3d`  
		Last Modified: Wed, 04 Feb 2026 20:28:42 GMT  
		Size: 13.8 MB (13811374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e904c17abcb92084294e073cb2ff06eea8edb930dad0489315b22a01d7c50ff`  
		Last Modified: Wed, 04 Feb 2026 20:28:42 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f80ec4d1f5008cbb44860d6ad567082bc47fc988797e8db2c97415a55fa11e0`  
		Last Modified: Wed, 04 Feb 2026 21:37:20 GMT  
		Size: 5.6 MB (5588455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:a3690f7d438ce89ba28f7b5addb47b989df29ff6f9b0e8060f8e85ba4e251741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.0 KB (632965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d54ae72cf437b37e592803640f6625babed7f860e38dfefd7604b1faedeb0061`

```dockerfile
```

-	Layers:
	-	`sha256:1f86c6254f47348c43e46c7d8cca497e300c88f12c0696708784fcab5752f4b1`  
		Last Modified: Wed, 04 Feb 2026 21:37:20 GMT  
		Size: 623.7 KB (623681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46f239f981b4bb9d9c3c8d43646ece8a13147ce116e12a17cde82a5f30b0fcc2`  
		Last Modified: Wed, 04 Feb 2026 21:37:20 GMT  
		Size: 9.3 KB (9284 bytes)  
		MIME: application/vnd.in-toto+json
