## `hylang:1-python3.14-alpine3.22`

```console
$ docker pull hylang@sha256:a5c6cba25e9861bba64cda9cfbcd8cbaa61bdccd5c4cf2f3b852c3299ea0f331
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

### `hylang:1-python3.14-alpine3.22` - linux; amd64

```console
$ docker pull hylang@sha256:fe3f7186e5340b5b513df1cac5fc8d0d4ce42c8d3d2d2569f0fa615f9f874b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23177798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc6858f32212aa35d921d75f86bf5cc14220cefc89ba797461ee15345e4336e`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:30:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:30:51 GMT
ENV PYTHON_VERSION=3.14.4
# Fri, 17 Apr 2026 00:30:51 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Fri, 17 Apr 2026 00:33:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:33:09 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:33:09 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:16:04 GMT
ENV HY_VERSION=1.2.0
# Fri, 17 Apr 2026 01:16:04 GMT
ENV HYRULE_VERSION=1.0.1
# Fri, 17 Apr 2026 01:16:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 17 Apr 2026 01:16:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079f87febaa1fa4d72af1d7de69b362fb932eb9823b749baa9a68746c1624115`  
		Last Modified: Fri, 17 Apr 2026 00:33:15 GMT  
		Size: 455.0 KB (454973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d9f130c3a5e49e10c45441b7785bf41700f5abb6c9269f64e7fbfb4bb21244`  
		Last Modified: Fri, 17 Apr 2026 00:33:16 GMT  
		Size: 13.3 MB (13333825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d522021ae4e5098651090d8c581132d35dd25d523437e10e99e46205f13a9403`  
		Last Modified: Fri, 17 Apr 2026 00:33:15 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b225919b78d4e6d3b0eefab573c5ee5185fc64ae79696b8f833f2d43aea65`  
		Last Modified: Fri, 17 Apr 2026 01:16:10 GMT  
		Size: 5.6 MB (5580564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:a8adb1aa10cb544903636472ee6cc3a7d0755159098157576e7f2c1e0d237e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.2 KB (634236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0cdd16086e73758eff2de8a15cceb25da36be3a66565dec3c819097011a700`

```dockerfile
```

-	Layers:
	-	`sha256:d8c1ccbbd85e04dcf5c5abda9f6243c708939884f1c73e825e728bf3b084904b`  
		Last Modified: Fri, 17 Apr 2026 01:16:10 GMT  
		Size: 625.0 KB (624953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e2842d7b4724fbea67b32d312e01c372f58dcdef72890ecbd9422626e999e3b`  
		Last Modified: Fri, 17 Apr 2026 01:16:10 GMT  
		Size: 9.3 KB (9283 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine3.22` - linux; arm variant v6

```console
$ docker pull hylang@sha256:b62536501f7d3ec0299e6301a144d7ec4c269cd6b89b6107be6f41059bbb6a49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22465516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2683646e6b7b0bbe75b874550818ed3f573a18bb6921e6ad562a7bc8d8cc40`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:29:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:29:22 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:29:22 GMT
ENV PYTHON_VERSION=3.14.4
# Fri, 17 Apr 2026 00:29:22 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Fri, 17 Apr 2026 00:32:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:32:02 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:32:02 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:14:34 GMT
ENV HY_VERSION=1.2.0
# Fri, 17 Apr 2026 01:14:34 GMT
ENV HYRULE_VERSION=1.0.1
# Fri, 17 Apr 2026 01:14:34 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 17 Apr 2026 01:14:34 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168aea808760ffba94f72ba5968ba0d7e405c00b61c332fdf7fd4d4fd093e003`  
		Last Modified: Fri, 17 Apr 2026 00:32:07 GMT  
		Size: 455.9 KB (455915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d941bcd837c94c2c48d5880a1b76b8ae6572571fe157a5d1beae8e70fdf46c7`  
		Last Modified: Fri, 17 Apr 2026 00:32:07 GMT  
		Size: 12.9 MB (12921366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff78ce0e8f88556091662872d8631fa7bf275ad5a68d2ffa0a416c690bd6899`  
		Last Modified: Fri, 17 Apr 2026 00:32:07 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bed53ecd602116203ae473fffebccbb02517bc58246ec1cfc073ceb5d426308`  
		Last Modified: Fri, 17 Apr 2026 01:14:38 GMT  
		Size: 5.6 MB (5580601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:f0c537e1211a8d66c8acad5fd485c95cd2bbd4a960bb9e17456994600bb44ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b567880f52a0f5c7dea51d4b0f8d9c9a8083f0ac4762b9bcaf5801e3e4a6e203`

```dockerfile
```

-	Layers:
	-	`sha256:e7ac53125c54a699a411b15d0650026b6d21ebbe8eaf227d1e99700ed5b8bad4`  
		Last Modified: Fri, 17 Apr 2026 01:14:38 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine3.22` - linux; arm variant v7

```console
$ docker pull hylang@sha256:19d928580ab5913837e3f9f6cc16d8370cd936ae18e56c5ba8a37e61b9682854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21802558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8db17c925ba3ece42bd9b627240587b336621f6984c289229b358066735d200`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:32:41 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:32:41 GMT
ENV PYTHON_VERSION=3.14.4
# Fri, 17 Apr 2026 00:32:41 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Fri, 17 Apr 2026 00:35:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:35:22 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:35:22 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:18:14 GMT
ENV HY_VERSION=1.2.0
# Fri, 17 Apr 2026 01:18:14 GMT
ENV HYRULE_VERSION=1.0.1
# Fri, 17 Apr 2026 01:18:14 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 17 Apr 2026 01:18:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4eda64f2d0b6cf10c8f27dacf468d95322fa52f24b9e18e254c37c6d28692c3`  
		Last Modified: Fri, 17 Apr 2026 00:35:28 GMT  
		Size: 455.0 KB (455009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0a6841fb0b16398b615cbb7e6c49e2386e6a1f6874f0d5d34ef35f9b8ac8f9`  
		Last Modified: Fri, 17 Apr 2026 00:35:29 GMT  
		Size: 12.5 MB (12541022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ad76b87c23458221f76d8a84a2ef2623d856ebcad7a0f041eec1977e294759`  
		Last Modified: Fri, 17 Apr 2026 00:35:28 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9683d11601e4595ce954acc759ff5469389bffa5b19273c89531f209ee9f7235`  
		Last Modified: Fri, 17 Apr 2026 01:18:20 GMT  
		Size: 5.6 MB (5580449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:503242d28674033201df1e7654b6f3b6656d9e149f082f779236e953c6100ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.4 KB (637407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454390f18a171720a8867cb6cb1c33a54cd8ca5aa134ff8b01a32290c51a9b4e`

```dockerfile
```

-	Layers:
	-	`sha256:b32380c99384b103dcbbb99dc2f7e9583b3cf4ce2cea0f5aa053c95a89235033`  
		Last Modified: Fri, 17 Apr 2026 01:18:19 GMT  
		Size: 628.0 KB (628011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64d2b69861a4f79365982a7712415b3b2e2769895649617c8656b303ee15f8c5`  
		Last Modified: Fri, 17 Apr 2026 01:18:19 GMT  
		Size: 9.4 KB (9396 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:61410db5f01797ae891723cf0cc2a8051804a8ae1c83d76d18398318d886f1bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23491023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffd871e5585d7e7c41dc14b3e1ef0695244bbee98f0058e7ddd264f7473d00b`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:32:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:32:27 GMT
ENV PYTHON_VERSION=3.14.4
# Fri, 17 Apr 2026 00:32:27 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Fri, 17 Apr 2026 00:34:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:34:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:34:55 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:40:17 GMT
ENV HY_VERSION=1.2.0
# Fri, 17 Apr 2026 01:40:17 GMT
ENV HYRULE_VERSION=1.0.1
# Fri, 17 Apr 2026 01:40:17 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 17 Apr 2026 01:40:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5119ad6047b1f82c60ac9fd1042c184429bbf4d41408d253e76fe3ee5f85e10f`  
		Last Modified: Fri, 17 Apr 2026 00:35:02 GMT  
		Size: 457.3 KB (457320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab81cdd7e1a0d33be681ddd8583c497b3c41970f8e6d0de6c4cc66ca5ac1960f`  
		Last Modified: Fri, 17 Apr 2026 00:35:02 GMT  
		Size: 13.3 MB (13311056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9612b45ba11df423953a6986eb4b81b7ec436c348f366b21d5a80117c2b984e2`  
		Last Modified: Fri, 17 Apr 2026 00:35:02 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47408cf9eada78476376bdd484eebaf62c88f9009cb0dea4ade44607cde60d6d`  
		Last Modified: Fri, 17 Apr 2026 01:40:23 GMT  
		Size: 5.6 MB (5580507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:fe8aa0de3ecf947cb36194d3586cd561a3f539d97bf0aa41533aa727f4be54a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.5 KB (634493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8fe30e47b5cfd7c5d7ec03fa2a189af9ae38cc884fa87ece9af3b1bcdeea36`

```dockerfile
```

-	Layers:
	-	`sha256:0a4f94675164d9d27bf96769807c3b7c12065297ff1fd23f7ec7a4bd25302385`  
		Last Modified: Fri, 17 Apr 2026 01:40:23 GMT  
		Size: 625.1 KB (625057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7714475a13bf26bb5b9f4d958c6cd007e99b92f0a0298e1234eddea86ba871ec`  
		Last Modified: Fri, 17 Apr 2026 01:40:23 GMT  
		Size: 9.4 KB (9436 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine3.22` - linux; 386

```console
$ docker pull hylang@sha256:5896b29c7e5c9245252f1aaa163e84f7362974270edc2b1d7b1fb156df2748e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23274326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32b7f67bc7e7e6fbe22ceb74aa42aee2bb78ed7a12f67a6fecac04fb98f946e`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 05:55:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 05:55:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 05:55:45 GMT
ENV PYTHON_VERSION=3.14.4
# Fri, 17 Apr 2026 05:55:45 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Fri, 17 Apr 2026 05:58:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 05:58:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 05:58:23 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 09:06:08 GMT
ENV HY_VERSION=1.2.0
# Fri, 17 Apr 2026 09:06:08 GMT
ENV HYRULE_VERSION=1.0.1
# Fri, 17 Apr 2026 09:06:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 17 Apr 2026 09:06:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498b52605bf0eb0f5045eb5c2507009c524913c7eb12661ecb3f384802b774fc`  
		Last Modified: Fri, 17 Apr 2026 05:58:30 GMT  
		Size: 455.5 KB (455454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea76d455077ca9e8633ad5f9942b69f4755696e4430f0a6015f137ffcbec719`  
		Last Modified: Fri, 17 Apr 2026 05:58:30 GMT  
		Size: 13.6 MB (13613320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00909570fa9621a594d7b084a66df49a3d57bfa9e416e71c52d79a34509bef57`  
		Last Modified: Fri, 17 Apr 2026 05:58:29 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683146e8c3ee2bac89012efa6fda241c90f9492caef5a4cfbd1401b0c0f4a23f`  
		Last Modified: Fri, 17 Apr 2026 09:06:14 GMT  
		Size: 5.6 MB (5580582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:dd55bf0af2216c58323af03c165e94055fc9602717724c6ad317d9d36879f786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.1 KB (634140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08f6b8333f05d2e8b7fd54b84c97e53f2ed049fac748e63a671af510b23dc27`

```dockerfile
```

-	Layers:
	-	`sha256:4bc60877853db0fab7db135dc1352a7920312499a5b3d00cec47f770898e841d`  
		Last Modified: Fri, 17 Apr 2026 09:06:14 GMT  
		Size: 624.9 KB (624908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f180ea57cf14326456d521992c221e0dca616abab0efe0043a68b4cdfa83b48`  
		Last Modified: Fri, 17 Apr 2026 09:06:14 GMT  
		Size: 9.2 KB (9232 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine3.22` - linux; ppc64le

```console
$ docker pull hylang@sha256:37b1a1a9cd3242eff72d590d73994b9b65dbf70d3e26f296c9c427ec6bbc3f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23891524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39734859e7142eed002d5a90cf47ffa332f705498caadb27d12bfc1348d291a0`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:21:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 01:21:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 01:21:29 GMT
ENV PYTHON_VERSION=3.14.4
# Fri, 17 Apr 2026 01:21:29 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Fri, 17 Apr 2026 01:32:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 01:32:16 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 01:32:16 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 02:28:02 GMT
ENV HY_VERSION=1.2.0
# Fri, 17 Apr 2026 02:28:02 GMT
ENV HYRULE_VERSION=1.0.1
# Fri, 17 Apr 2026 02:28:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 17 Apr 2026 02:28:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971a7213f053e153251c4a5c2247a66c2cad85bc92c3e381645ea08c29b00b21`  
		Last Modified: Fri, 17 Apr 2026 01:26:59 GMT  
		Size: 457.7 KB (457749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56aede7b3eb468cd145d4f4844b94eed5f0d46aabb61b51890e67a8e7fbdafd8`  
		Last Modified: Fri, 17 Apr 2026 01:32:32 GMT  
		Size: 14.1 MB (14116075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a64753b6f0ffdc57d05d09e35b4586720bf994de01dc16251582c288dea31e`  
		Last Modified: Fri, 17 Apr 2026 01:32:32 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7dad74745cc2fb637a2217128d08b0944253d9508b6f079c6259232ebd8e55`  
		Last Modified: Fri, 17 Apr 2026 02:28:12 GMT  
		Size: 5.6 MB (5580796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:3aa27751f36a2313dc3fc9a25e4fb0c6ddcf73431bc11a766e78328c7d1c7916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.4 KB (632412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9dfd82124b79dbf8bf858bfd70c9c8fd334a3ae4142d5cd89dbe2fbeca1bdf`

```dockerfile
```

-	Layers:
	-	`sha256:cdaf0139dacb06f052c34d6e3179d7c7db6d70d78952f6d14812305771c56899`  
		Last Modified: Fri, 17 Apr 2026 02:28:12 GMT  
		Size: 623.1 KB (623060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e5faf23e3ea5daa33a3084efc3c7904d78e24f1897d92f5d1c54adddd482416`  
		Last Modified: Fri, 17 Apr 2026 02:28:12 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine3.22` - linux; riscv64

```console
$ docker pull hylang@sha256:a12b3de9224f0c52a14c4d1734d509b0d44099260052b3b116b996f6ecc25e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23036248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56b891bf7533fdb6e67ebbcea4039312289937e00c08c6ec602e9b14aa09e6c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Sat, 11 Apr 2026 13:28:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 13:28:14 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 11 Apr 2026 13:28:14 GMT
ENV PYTHON_VERSION=3.14.4
# Sat, 11 Apr 2026 13:28:14 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Sat, 11 Apr 2026 17:03:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Sat, 11 Apr 2026 17:03:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 11 Apr 2026 17:03:40 GMT
CMD ["python3"]
# Sun, 12 Apr 2026 19:33:48 GMT
ENV HY_VERSION=1.2.0
# Sun, 12 Apr 2026 19:33:48 GMT
ENV HYRULE_VERSION=1.0.1
# Sun, 12 Apr 2026 19:33:48 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 12 Apr 2026 19:33:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afe2869910de51d81c3f52246ebe5dc82f67c7310f75a06088aff45c17398e2`  
		Last Modified: Sat, 11 Apr 2026 14:07:07 GMT  
		Size: 457.4 KB (457411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eceaf30bd37b4dd45434c816207e6ff889965ebf029c5bf080a66ea53d6f3142`  
		Last Modified: Sat, 11 Apr 2026 17:04:27 GMT  
		Size: 13.5 MB (13498895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016c700f5b59f1d339205d21af7c237676241e2ff017cd289a909cc9eab9f428`  
		Last Modified: Sat, 11 Apr 2026 17:04:25 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf0bb3376e3d2bd175cc3f12f65921502fd475834ea63f8afac5afc27a5a512`  
		Last Modified: Sun, 12 Apr 2026 19:34:27 GMT  
		Size: 5.6 MB (5562270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:3db11a6a32c5d5a47bf8e70fa0996faca67e6306ace776f1122953e364365d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.1 KB (633095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d9e00d2a8a851369d6b3fb50630aaef2b2f65cb2af6b542047b180ea2fec72`

```dockerfile
```

-	Layers:
	-	`sha256:a65957d1f2572fb2d278461f4d95df5642c977b570de9a0f9753ff8aa3c2eb38`  
		Last Modified: Sun, 12 Apr 2026 19:34:26 GMT  
		Size: 623.7 KB (623743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9041d470a45041703edfaa75f5cdc588dbff4bf8abbfae41caf443b5ea1c1ec3`  
		Last Modified: Sun, 12 Apr 2026 19:34:26 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-alpine3.22` - linux; s390x

```console
$ docker pull hylang@sha256:1e18b3318f18e4a7e6ae4b826a343c37dace6a6b471609563fec98dc6c7624c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23526100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e3324caef00c906b640d0a1c08b54709d57fc31cd3d9a96594ec08898a158a`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:54:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 01:54:20 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 01:54:20 GMT
ENV PYTHON_VERSION=3.14.4
# Fri, 17 Apr 2026 01:54:20 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Fri, 17 Apr 2026 02:06:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 		zstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 02:06:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 02:06:34 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 03:07:16 GMT
ENV HY_VERSION=1.2.0
# Fri, 17 Apr 2026 03:07:16 GMT
ENV HYRULE_VERSION=1.0.1
# Fri, 17 Apr 2026 03:07:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 17 Apr 2026 03:07:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126d2341a9fe42be2ba1cb944d53be27f089405112724d2eeb7a16d2952ed81f`  
		Last Modified: Fri, 17 Apr 2026 02:00:28 GMT  
		Size: 456.0 KB (456010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bf62c9bb2bf2cd6c5d04060549dedd2512e06290d243a2860cdf1341ae530a`  
		Last Modified: Fri, 17 Apr 2026 02:06:46 GMT  
		Size: 13.8 MB (13835447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8a17308fd352e1808a270ab6aa3b56245acf9fc21ca5d63bbf2c2851f6bddc`  
		Last Modified: Fri, 17 Apr 2026 02:06:46 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d792c70025254be0f83ef4d85810dc75c1dcc61bcff19ec2fe5273b64fc2335`  
		Last Modified: Fri, 17 Apr 2026 03:07:27 GMT  
		Size: 5.6 MB (5580522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:c2b9f82b6541389e4bf6f8c7ad1ac8d5797495498d99205d8620b3e0abcabcbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.3 KB (632286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cccc4ef45a439dec5b239acd2246a0035f163ed38dd6baa277bbf1c4965fdf5`

```dockerfile
```

-	Layers:
	-	`sha256:4d49a5189374cfbd3d182832b4910e6410fa6d4466a08396ef1939757d930d6b`  
		Last Modified: Fri, 17 Apr 2026 03:07:27 GMT  
		Size: 623.0 KB (623002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86dcdd73c762ad10a565e6984c2daaaefae697dd4c48253918edd65142cf2dc1`  
		Last Modified: Fri, 17 Apr 2026 03:07:27 GMT  
		Size: 9.3 KB (9284 bytes)  
		MIME: application/vnd.in-toto+json
