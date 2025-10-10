## `hylang:python3.12-alpine3.22`

```console
$ docker pull hylang@sha256:0ffa2c82e5594e7b0db694bea3addda0cab38f15145b6ca434bbf8c6a967812a
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

### `hylang:python3.12-alpine3.22` - linux; amd64

```console
$ docker pull hylang@sha256:332ddb199bc92817e0b12dc7d5590fd23eaa251461882a9b503d266c6fa21ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23541289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f90f6f761713c52fe3cee42d233ba8fab9643ddf8e3d918e7cd1b5b423e190`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.12.11
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=c30bb24b7f1e9a19b11b55a546434f74e739bb4c271a3e3a80ff4380d49f7adb
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7981d7adf08345e86a8f1e865e135d48976f253bc88f2078b9cc19c604508e`  
		Last Modified: Wed, 08 Oct 2025 23:16:25 GMT  
		Size: 456.9 KB (456912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceab0f9a612ffe233cde5cace4f51d7931a192422d41afbdd8525ba04ac5eb81`  
		Last Modified: Wed, 08 Oct 2025 23:16:27 GMT  
		Size: 13.7 MB (13682851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5479191cfc91bdd920031939a8f444635d4d690f1a3384e8600e2fbd81f2e32`  
		Last Modified: Wed, 08 Oct 2025 23:16:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd0f7df8ec51418a99701a3244ddcc4c351916c8674476058b1756fae8535fc`  
		Last Modified: Wed, 08 Oct 2025 23:50:10 GMT  
		Size: 5.6 MB (5598827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:137e800390f8330e1fbead1bcf77aaf7b1053eeac1fab3bfd0a6752ced035dac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.3 KB (664269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30a991f3c9715727714117757f624121ef5b07abcf56b3ffb7cc21a19f63e6c`

```dockerfile
```

-	Layers:
	-	`sha256:919d19a97f487a600ef217e0c771c736009dc1790413de934266b82a5cd4e93e`  
		Last Modified: Thu, 09 Oct 2025 02:20:04 GMT  
		Size: 654.9 KB (654928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2bf86f497263e865a8b63057332f76df943bfa9042b80fc75c4c3d0b2db4696`  
		Last Modified: Thu, 09 Oct 2025 02:20:05 GMT  
		Size: 9.3 KB (9341 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.22` - linux; arm variant v6

```console
$ docker pull hylang@sha256:a84b86c9626214541c729eae9fb32939653393bf9d911e6025096bdc48ab9579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22775801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9d273031b7cba61fce4c2a202f55c6515de23a2c77391fefd3b618c6cbd835`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.12.12
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=fb85a13414b028c49ba18bbd523c2d055a30b56b18b92ce454ea2c51edc656c4
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7745ee696ce94c130002e019e3035b95a5011a6a206a04676dd1bb41b82e08`  
		Last Modified: Thu, 09 Oct 2025 22:41:07 GMT  
		Size: 457.8 KB (457751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bf52a25e023fd9b6419adc1b1aa4c45491d50ed7708205db64c1f22407f276`  
		Last Modified: Thu, 09 Oct 2025 22:41:08 GMT  
		Size: 13.2 MB (13212846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85e7d1a3710c50452d53ff58a3ada75a49cc6fc0adefd35cb5aaf557bfbc6c1`  
		Last Modified: Thu, 09 Oct 2025 22:41:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd631a0103fb303cb6b5809716d76283e3fa8a9885d3801f1a39d49ff9a8741`  
		Last Modified: Thu, 09 Oct 2025 23:24:06 GMT  
		Size: 5.6 MB (5600875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:c97c2de5e1098f9416f781a1f43bcb95bdae3a3e14cea8c1684fd122b0d720fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06319d55f39c1e463b5f3f2502295722cb7b657064f4c77bba4e0c063749eaf3`

```dockerfile
```

-	Layers:
	-	`sha256:78ff6c65fece3c73b9693e152fea81f4e0e74d96994a8f58e5bec57054abe741`  
		Last Modified: Fri, 10 Oct 2025 02:18:13 GMT  
		Size: 9.2 KB (9239 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.22` - linux; arm variant v7

```console
$ docker pull hylang@sha256:741ea98cb0feb243316f3a62e3e349cce776cf12f645d64039fb0bb57d7d5ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22110844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b6857b6c63a38f54a3866f505537807880623b2f8d2b0e495203cafd03b0b1`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.12.11
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=c30bb24b7f1e9a19b11b55a546434f74e739bb4c271a3e3a80ff4380d49f7adb
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a3ba62552a765fc0b7750c8451d66e4eac0d5ad041854e1dd850029181cf2d`  
		Last Modified: Wed, 08 Oct 2025 23:33:24 GMT  
		Size: 456.9 KB (456942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b8f8d5f71a8df1c667e9abeeb0848b6e5094f01c08ea2142da9b0daa9cd6dd`  
		Last Modified: Wed, 08 Oct 2025 23:33:25 GMT  
		Size: 12.8 MB (12833140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d84e0368d0abe7127b7795a56b4d53f6df7523de5e99f822e6d3e5a9512dd7`  
		Last Modified: Wed, 08 Oct 2025 23:33:24 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0bcedb0a9f5a67463f53e2b93b338eda7ba24d642b6601f86ecadf92b8821f`  
		Last Modified: Thu, 09 Oct 2025 00:16:15 GMT  
		Size: 5.6 MB (5598960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:88e5d716d582d0d6fbb69735551dea32fddf3e472aeefa9be69f604475c4dba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.4 KB (667440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34c26f1ef308567bea4b05d08dbaf0223e72d8325d692225a6abc1150a7f617`

```dockerfile
```

-	Layers:
	-	`sha256:fc070d4640cb60db2cc3402aa40ecb2504e4ee2a440e43d968f864d577271e76`  
		Last Modified: Thu, 09 Oct 2025 02:20:12 GMT  
		Size: 658.0 KB (657986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7398982c98abc761f9162ecb5695f8b9547340e95ea06da538cf64059fca412`  
		Last Modified: Thu, 09 Oct 2025 02:20:12 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:9bc88cdb105b57a87efb70fd70a77e6fd4d5257d8a58deac9342fc754c15d21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23923152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a1ab72465e25795b7aafbb31d5245997e3b4be161ee27fc4c1314df52fd666`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.12.11
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=c30bb24b7f1e9a19b11b55a546434f74e739bb4c271a3e3a80ff4380d49f7adb
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de168e5052cead172e8c06aed26fa4715425d004f5c3774f3692310e31b28f9c`  
		Last Modified: Wed, 08 Oct 2025 23:14:06 GMT  
		Size: 459.0 KB (459006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8797b1a2d5cb1eef16b356599e5014f94810e6834dbe2b21a3e469034258fb`  
		Last Modified: Wed, 08 Oct 2025 23:14:06 GMT  
		Size: 13.7 MB (13726960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a4792b2841a37feb577ab154c946af2256f6b7080f9a4891543fb98f56a96a`  
		Last Modified: Wed, 08 Oct 2025 23:14:05 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ef12b026031c7704176e76e0a74d21c367b2ace3cdf937d2761ddab929551d`  
		Last Modified: Wed, 08 Oct 2025 23:33:26 GMT  
		Size: 5.6 MB (5598870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:7b5f9296f1189a0a8b81f2d7d63afc2035e059b90b9668e1894fa931ec89444a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.5 KB (664526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5996cc1faabdf15751b2a9ada0e5963107a32b8455f79149207071152489763`

```dockerfile
```

-	Layers:
	-	`sha256:edf9b17b11c32d6cc42637be2a458bb1e402c60bbaf62edc8fc0e75971acbee4`  
		Last Modified: Thu, 09 Oct 2025 02:20:16 GMT  
		Size: 655.0 KB (655032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d76733f06d7cfdcc606d8cdddcfe8a9e1ba01da75041bb4fa15493b907aba2e4`  
		Last Modified: Thu, 09 Oct 2025 02:20:17 GMT  
		Size: 9.5 KB (9494 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.22` - linux; 386

```console
$ docker pull hylang@sha256:add1718af77ffae10bea745958235761c4c77ad73a9fed9d1d404f7175a9bebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23582408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781ee5d8d3d0419fb4d05e630d98f4964843126a2cab48d14d45420ef37e2164`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.12.11
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=c30bb24b7f1e9a19b11b55a546434f74e739bb4c271a3e3a80ff4380d49f7adb
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37cbe74655706d99207c3b80a548d50396eefc8b2bec61e104cf77d27becea3`  
		Last Modified: Wed, 08 Oct 2025 22:28:02 GMT  
		Size: 457.4 KB (457369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64411e7dce3941fd184d2ded50145df2bdf2c3aa5df18e0c5a1a942225143ca5`  
		Last Modified: Wed, 08 Oct 2025 22:28:02 GMT  
		Size: 13.9 MB (13906881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03ab6df45d23ad195b8466d1334d55b6f15e681ce7c83176a16806a21fa510a`  
		Last Modified: Wed, 08 Oct 2025 22:28:01 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5a029b63b35b530be5bbba4d3340d34ec48140f4557f30e9761809f08a8f4d`  
		Last Modified: Wed, 08 Oct 2025 22:28:30 GMT  
		Size: 5.6 MB (5598979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:ef66364c70a0c3234e7b8dfc23147b9e8991226f5ee3c66bbbe5909fee650136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.2 KB (664173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c93a85913d5380de2bde79c0194a315dc0f7beba2bc1dc63627e1a00f06a1c6`

```dockerfile
```

-	Layers:
	-	`sha256:c4e9a7d8375fb4263f4cf5ddf53d4ab3b8b50cbd80eef56dafb99c20033b6375`  
		Last Modified: Wed, 08 Oct 2025 23:24:15 GMT  
		Size: 654.9 KB (654883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:459457c832c3e4c426d4b4d9cc1d677cb130d39223f29b81771a784ed71920b6`  
		Last Modified: Wed, 08 Oct 2025 23:24:16 GMT  
		Size: 9.3 KB (9290 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.22` - linux; ppc64le

```console
$ docker pull hylang@sha256:3ee4016d1edc730feafb677a0195ac5127cdbcc214670225117fa56a81c32131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24245132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc395a2c25474d6473e761971239bc67351a742d337a377adcdfb6a7a806814`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.12.11
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=c30bb24b7f1e9a19b11b55a546434f74e739bb4c271a3e3a80ff4380d49f7adb
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d59558aec49aa561bba128776098134d977c895162d47f6feb60e130039a68`  
		Last Modified: Thu, 09 Oct 2025 08:28:28 GMT  
		Size: 459.4 KB (459435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f1cbce5b524686185664c60121ebb497611a8a27b7dcc551c675efb98c1779`  
		Last Modified: Thu, 09 Oct 2025 08:28:28 GMT  
		Size: 14.5 MB (14454318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57c9d4c1d2037ecb59422de274e3de21a6c576a8a9ff7a1babc29c6f3bca6ae`  
		Last Modified: Thu, 09 Oct 2025 08:28:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f0a6fc90a67f066d8b424e2282b23ec244d83941e5e47ce40033d4079aba2d`  
		Last Modified: Thu, 09 Oct 2025 11:17:28 GMT  
		Size: 5.6 MB (5598891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:876465239f6c91fc6db3d2acd2fb2b6f75c56360f41839a460677519bcd4ca53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.4 KB (662445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4002e89ad1ea1cf35820b80a0e36057e554af6c237dc3693f00d1adb3751e7f9`

```dockerfile
```

-	Layers:
	-	`sha256:060da73efa85f2deae3eb28f2eda3eab37f417e871a31ab9d40086d128a7264c`  
		Last Modified: Thu, 09 Oct 2025 14:18:48 GMT  
		Size: 653.0 KB (653035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90781b230efe35abc6d62be35cedcd1a5b07bc04b57ceb167dc097679a899f62`  
		Last Modified: Thu, 09 Oct 2025 14:18:49 GMT  
		Size: 9.4 KB (9410 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.22` - linux; riscv64

```console
$ docker pull hylang@sha256:df746a831f399b0727d6a6c024b2c0dab44d3d2159a555ec4f111cd93286f60a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23284894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b1d66e8a14e233eed48fdf0492cccb7fb5f773bd4ae866d9280423a8790d7f`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 18:20:34 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_VERSION=3.12.11
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_SHA256=c30bb24b7f1e9a19b11b55a546434f74e739bb4c271a3e3a80ff4380d49f7adb
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
CMD ["python3"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HY_VERSION=1.1.0
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 13 Aug 2025 21:03:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c605b78e30747b6919ee8087099ad76ec1f7fbb8cb796b19e9ed3387a270e5`  
		Last Modified: Thu, 17 Jul 2025 19:27:37 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109ad96c6ff7d0d45405b47c0b9aebba3f2458006ac862595334c12dde254ffb`  
		Last Modified: Wed, 13 Aug 2025 04:50:58 GMT  
		Size: 13.7 MB (13723765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b67532fd627bacd6a07782c057019b9b5abb74c88b4256a7aa3a9235b65084c`  
		Last Modified: Wed, 13 Aug 2025 04:50:54 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb07fbba545ee5618eef9b9c637787941c7caf81525cf528b5fa6d50141cc48d`  
		Last Modified: Sun, 17 Aug 2025 12:42:07 GMT  
		Size: 5.6 MB (5600022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:37ebfce565b0d5445062018ed9ca89b55915a3149055caaf1faff31b4055e559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.8 KB (659828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a216c0f4680b4750beea6735b202251e9bb7d554d00c128a33d4a20c891f3e`

```dockerfile
```

-	Layers:
	-	`sha256:8414d4881c3b204f1da58dee41bb5729d98a01b98699bf94983e3e170298c0f8`  
		Last Modified: Sun, 17 Aug 2025 14:18:26 GMT  
		Size: 650.4 KB (650418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d4c4ca6c0f23954842ec4d51873768075c8265c1c3b162c724705174133d3b9`  
		Last Modified: Sun, 17 Aug 2025 14:18:27 GMT  
		Size: 9.4 KB (9410 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine3.22` - linux; s390x

```console
$ docker pull hylang@sha256:f08d42b05ec81776b7ab71deb7a4a10cff7ee844027141f7491265cc8a170f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23913501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479a46784fd2e02d4fcb5b21ca66a625abea91656f86af76835eae9bbc21bd90`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.12.11
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=c30bb24b7f1e9a19b11b55a546434f74e739bb4c271a3e3a80ff4380d49f7adb
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4929a7616ec9e65e89e8fc96cf51868212bfa5dfaa51e5a68686d2f0903e035`  
		Last Modified: Thu, 09 Oct 2025 13:00:09 GMT  
		Size: 457.9 KB (457909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f695fc07223b1b1aa9e2f21f679cd79d837dc790ce1fcf04ff82a776940b5bf`  
		Last Modified: Thu, 09 Oct 2025 13:00:11 GMT  
		Size: 14.2 MB (14207327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058f937bbc8057a7148a0cd7a7128da2aadc199739dab88bc6bd4c2f23a72f78`  
		Last Modified: Thu, 09 Oct 2025 13:00:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f21076d3d64e4ceaebe5fd57ddb0f4387c8d62d269fd13668e1c05d2559eaa`  
		Last Modified: Thu, 09 Oct 2025 15:46:38 GMT  
		Size: 5.6 MB (5598772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:6dc2b4001398370b88adb66215695279e24f8da5812dc528a4012bb7130b10af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.3 KB (662319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74454fcf58a875c55b2f2addb6c74a064fef711c7bc01f13335f6470e8403169`

```dockerfile
```

-	Layers:
	-	`sha256:5e2910fc2b1b7ed050ae5fed132f6ba74e539fa72cc5356268117a1906df5b3b`  
		Last Modified: Thu, 09 Oct 2025 17:18:41 GMT  
		Size: 653.0 KB (652977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58511d5eeecbeb670c227171741918c508f07a52eed5333a095bcf2934f84d37`  
		Last Modified: Thu, 09 Oct 2025 17:18:42 GMT  
		Size: 9.3 KB (9342 bytes)  
		MIME: application/vnd.in-toto+json
