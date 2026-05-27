## `hylang:1-python3.13-alpine3.22`

```console
$ docker pull hylang@sha256:a28f4e903d3f93607b48058e1de6393f56d52eba31b14dd9be65787d380602bd
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

### `hylang:1-python3.13-alpine3.22` - linux; amd64

```console
$ docker pull hylang@sha256:73e951d9f1a137dd2a129a76a4c7af42cb6360c306e7d615267621c785a6a590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22109480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb415661e169e283a0b74f96c519c9a78fa66b3d6d3c650392057905aea7af3`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:30:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:30:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 00:36:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:36:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:36:29 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:10:08 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:10:08 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:10:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:10:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df730813d20b0cb8062fb76ce24dc8fc02961ddd625cd6be3c86a0bc4dde8e56`  
		Last Modified: Fri, 17 Apr 2026 00:36:36 GMT  
		Size: 455.0 KB (454972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe818d7ffa27044c9667e73b415f9ae4c37a5d5d78c0cc4462423ded6b373a5`  
		Last Modified: Fri, 17 Apr 2026 00:36:36 GMT  
		Size: 12.5 MB (12472237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf71161b7b0782d25e76411844b95d7c41c91a90891d50df620e89e99fe18b8`  
		Last Modified: Fri, 17 Apr 2026 00:36:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d5d75edc94534334e7f80061956c46c790d0b3c567c441e07cf1257194b9f3`  
		Last Modified: Wed, 27 May 2026 00:10:14 GMT  
		Size: 5.4 MB (5373836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:e199fc51db9cf802c4d531818c9a909715a0c4673ea6cc28e0c6d9059b0243f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.7 KB (628742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f26cd5595927eb0328cca5c19c44017ddcb2b88a122f33eb6d4f57cee016ac`

```dockerfile
```

-	Layers:
	-	`sha256:25478640c65bcc97b6e6b0e43bf0627472e3fec21c64a6bf97a05fbbd4423ffa`  
		Last Modified: Wed, 27 May 2026 00:10:13 GMT  
		Size: 620.7 KB (620654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:416e9fe5edf7ae7129bb4c02c8b9f031405e1c6dd6a3f5a51f0442483fdd5ae1`  
		Last Modified: Wed, 27 May 2026 00:10:13 GMT  
		Size: 8.1 KB (8088 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-alpine3.22` - linux; arm variant v6

```console
$ docker pull hylang@sha256:709f27931b6acf465491e043cd4dd13cafaf9009e5b0ed8e5188060ffdcfaba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21422155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402ca8f1d53f142853701bba093ffb09d0d8e15de74d5b6d4d1ec3a6457f2c06`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:30:24 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:30:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 00:30:24 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 00:30:24 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 00:37:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:37:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:37:27 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:10:55 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:10:55 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:10:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:10:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565eadce8655ef2937ac93d46da0132342f65ba1e40a6a394505ebd7000c89e7`  
		Last Modified: Fri, 17 Apr 2026 00:37:31 GMT  
		Size: 455.9 KB (455916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c66201b04110a960498d96bdb5baf22ec06dd963e4b9a99d67cfea98be0c40b`  
		Last Modified: Fri, 17 Apr 2026 00:37:32 GMT  
		Size: 12.1 MB (12084757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58225ea593fb95c5ec04a163db802f55333c7a7f537a8329659e3bc91cf6774e`  
		Last Modified: Fri, 17 Apr 2026 00:37:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852acbcdc4d626845652d4a79de78119f1b5f08d8dd00113eaabd00954a80cf7`  
		Last Modified: Wed, 27 May 2026 00:11:00 GMT  
		Size: 5.4 MB (5373853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:cd7733c1a6e553cb3773ffaf659ac7afa427aeb420dad8adf1be2b17fe51584d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 KB (7953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70aa5e4b3954c52446a7dae3072eebcc14575420c22710036fe850353ffc30ba`

```dockerfile
```

-	Layers:
	-	`sha256:5b0ef29fe8dd07c38bbdcbba0a0fb51f0c8403a79c989a535d197632f59cac9c`  
		Last Modified: Wed, 27 May 2026 00:10:59 GMT  
		Size: 8.0 KB (7953 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-alpine3.22` - linux; arm variant v7

```console
$ docker pull hylang@sha256:a95d8acac937640ad399af67b5881e2cfcb814bf0895843d705db3d06e6ede09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20818489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343c5c9bfd81b8a3299a56ca4e649b560e995ca5b68633f423c67d7959174816`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:32:14 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:32:14 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 00:32:14 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 00:32:14 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 00:42:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:42:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:42:37 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:11:27 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:11:27 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:11:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:11:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f2d7ea620d691384017ca8ec53d50e6da646aa10189b3e1c54099acc64801b`  
		Last Modified: Fri, 17 Apr 2026 00:35:12 GMT  
		Size: 455.0 KB (455004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7729b8ca694c8639dc29a3c3fec5de2471191c83de0ca01a93bba2ee986efed`  
		Last Modified: Fri, 17 Apr 2026 00:42:44 GMT  
		Size: 11.8 MB (11763561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e6e11ab6e5ce32a46e18d36c4ddedbf13391fa34154e9ed8e2ba2cf83ba477`  
		Last Modified: Fri, 17 Apr 2026 00:42:43 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e54d4159aef4192de2a18f7c93f764f85371f6e227c7a19d314008af6c1f173`  
		Last Modified: Wed, 27 May 2026 00:11:33 GMT  
		Size: 5.4 MB (5373845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:8384313ae169eafb29e3f58867b54cd32e225e48a89a5d288058261fdc5219cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.8 KB (631848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60463e53d637ebd77dfd5987e70596be819db942e127856a605b68c6061c32d2`

```dockerfile
```

-	Layers:
	-	`sha256:c0e304ddb9456781709101323f3dccd77a93df96745dd64f226842b1703ebf46`  
		Last Modified: Wed, 27 May 2026 00:11:32 GMT  
		Size: 623.7 KB (623680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f5f28ea9d7dce7ee36855cc6594d43b4c696198a3c01f4809931a0ee0a26335`  
		Last Modified: Wed, 27 May 2026 00:11:32 GMT  
		Size: 8.2 KB (8168 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:d070f89836762bd59fb572d3398ddb7b8fecd750d4f0a8c1b358623b128d8414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22459816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743b06b87fc6aa69ed39eb80685b62562818cdc52c222706a43da7bd9275bd0a`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:32:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:32:45 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 00:39:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:39:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:39:34 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:11:33 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:11:33 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:11:33 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:11:33 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaff11adfb133e9e9320abbc299cc834c1403c253c3f7ea4ccaab6d6932fa60`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 457.3 KB (457313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53736ed35b86baa4c031683ba780c3f739bb4f9961f7885b78af60392fbe5836`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 12.5 MB (12486525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2c305c7606c8ddaf30bedaeaa4c18783036b29fbe2d07fc7eda11e7d1ddc34`  
		Last Modified: Fri, 17 Apr 2026 00:39:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc878fe8f6c858c0152d91cbf0ea6de47d07a588babcad757be0de4fb85887aa`  
		Last Modified: Wed, 27 May 2026 00:11:39 GMT  
		Size: 5.4 MB (5373835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:1c2deee591f72abad881fe42f931ba50c3ce3053346363c8805b7aa99da6e1cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.9 KB (628902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df31c06451d96cf4a42021bd823e0cb295c85238db168d81c70ca809b9bbb9df`

```dockerfile
```

-	Layers:
	-	`sha256:371eee819342f984e16c2b6df84e0265809d1b9f0c4e54f598973dab2f700de5`  
		Last Modified: Wed, 27 May 2026 00:11:38 GMT  
		Size: 620.7 KB (620710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b28b01a0ed3657ae00bfe001e059e5fe649f8200a3ec07e2b659874a445f534f`  
		Last Modified: Wed, 27 May 2026 00:11:38 GMT  
		Size: 8.2 KB (8192 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-alpine3.22` - linux; 386

```console
$ docker pull hylang@sha256:8c5bba07d11b99e703eb4a35b739957b95d99a2e0bf9eda6d49c4865d271b8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.2 MB (22183030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66bd0d1748778c25d3b7c0c040038509808965ef260cb69bb4ce0c93be6fa01e`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 05:55:46 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 05:55:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 05:55:46 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 05:55:46 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 05:55:46 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 06:01:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 06:01:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 06:01:20 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:10:37 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:10:37 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:10:37 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:10:37 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70d5b3e8b17e3d565bbe0eae9398152c2790e995f902d33155bae605eb3e35e`  
		Last Modified: Fri, 17 Apr 2026 06:01:27 GMT  
		Size: 455.4 KB (455447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7470ff3efda86ad429adec44c2ecb51c5432745525fb9a619d49f4fbfc9eb5`  
		Last Modified: Fri, 17 Apr 2026 06:01:27 GMT  
		Size: 12.7 MB (12728699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e10dc29680f9ca7658f306f98024c22198169c39fea2c5c459fd97469aba1e`  
		Last Modified: Fri, 17 Apr 2026 06:01:27 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb40d8542df91eee1863159a40cb01abb9f72741d21eae58949f85afd1afb41`  
		Last Modified: Wed, 27 May 2026 00:10:43 GMT  
		Size: 5.4 MB (5373915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:77508611fd8b03d9fccd308653ea36db00f9e35a23a3e637264a60496ad77852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.7 KB (628685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc897dac797f18606844d7a77227eddf7fcb3db2773cf30b5b47ed8a677b1f73`

```dockerfile
```

-	Layers:
	-	`sha256:7795a05306527980ac2a5cac68f0a13e901d12f9e18f95cc911c8acf58a53ca2`  
		Last Modified: Wed, 27 May 2026 00:10:43 GMT  
		Size: 620.6 KB (620629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade8a7caff2413d25c2afd9a2fff8be64aa291f71aed8453194f1a34d78a32a4`  
		Last Modified: Wed, 27 May 2026 00:10:43 GMT  
		Size: 8.1 KB (8056 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-alpine3.22` - linux; ppc64le

```console
$ docker pull hylang@sha256:37bcc656afcaec106ab8672ff0ae4ba47eab5ec37a2ce5884162c6a61edd129a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22759369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f144c13172570539aecc739f6cd79fc9a190a5e205157e3e88cc3040998d00c0`
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
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 01:21:29 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 01:21:29 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 01:44:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 01:44:45 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 01:44:45 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:21:55 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:21:55 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:21:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:21:55 GMT
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
	-	`sha256:d95fa66c720946d5a8fb393c6c080965d6b26fd7156222b2d09cb08eb82df795`  
		Last Modified: Fri, 17 Apr 2026 01:44:58 GMT  
		Size: 13.2 MB (13190803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1380cdc0758705833eed064555e891706c064be64e535e502120927d0dcf7d7b`  
		Last Modified: Fri, 17 Apr 2026 01:44:57 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9e2535357d7dd03f441f4ec4b96005883094eb187cf7ddd7263998ee8f3a3b`  
		Last Modified: Wed, 27 May 2026 00:22:05 GMT  
		Size: 5.4 MB (5373912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:1c9e426ae6d5365865b47396e41fefd0958efcd2d5b3ec32fa0d3e4da1321bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.9 KB (626869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3d702cabcc1d0e0bc993c5391c607b85d698d37423de489e5bab7d15b2507c`

```dockerfile
```

-	Layers:
	-	`sha256:3afbd27b4b9e0cc8edff2553d627b4a04cf6ec0b7ede5fa5e3c3446bf4c60b49`  
		Last Modified: Wed, 27 May 2026 00:22:05 GMT  
		Size: 618.7 KB (618737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f08fc37c01802f9799248d60416dc2b11fe914bf9118a03cef1b08764192d150`  
		Last Modified: Wed, 27 May 2026 00:22:05 GMT  
		Size: 8.1 KB (8132 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-alpine3.22` - linux; riscv64

```console
$ docker pull hylang@sha256:63cd80e4b39f807e8a300ffcee15d39b8c8afe6d14047658a66260f357b64ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21870153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7db314aa5af9496f821a04c8d2beb9154d693a58df48b9e4c7edcc7324b163`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sun, 19 Apr 2026 07:12:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 19 Apr 2026 07:12:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 19 Apr 2026 07:12:06 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Sun, 19 Apr 2026 07:12:06 GMT
ENV PYTHON_VERSION=3.13.13
# Sun, 19 Apr 2026 07:12:06 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Sun, 19 Apr 2026 09:04:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Sun, 19 Apr 2026 09:04:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 19 Apr 2026 09:04:29 GMT
CMD ["python3"]
# Sun, 19 Apr 2026 19:25:01 GMT
ENV HY_VERSION=1.2.0
# Sun, 19 Apr 2026 19:25:01 GMT
ENV HYRULE_VERSION=1.0.1
# Sun, 19 Apr 2026 19:25:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 19 Apr 2026 19:25:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77435711a7c7fa61413c4f682cc122e32bc104574fedb02c49b2d94017543d1c`  
		Last Modified: Sun, 19 Apr 2026 07:50:55 GMT  
		Size: 455.3 KB (455334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5822d3b1ab6ce57e11b30800e95aadc03be863f705232c78cb62ba7141e46d25`  
		Last Modified: Sun, 19 Apr 2026 09:05:15 GMT  
		Size: 12.5 MB (12538232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a02b79c3f2a8fb80401cf091a833e58a4e3a2cf1cde34e5f480c45ae9ffd2f3`  
		Last Modified: Sun, 19 Apr 2026 09:05:13 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e8bbf02f18f8179f6df947b605830fb0da62dc4c3c2ef187b0d782ffbb0e0f`  
		Last Modified: Sun, 19 Apr 2026 19:25:38 GMT  
		Size: 5.4 MB (5355458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:e0febad00e7e1a1cfe657fd5975ec61daf98dd38982028a78e1d625e951c2827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.9 KB (626865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48aa864e5e5be74bcddb5c6ddcc91b2b911fbbad8fa8f69ca967456c17552f02`

```dockerfile
```

-	Layers:
	-	`sha256:87116031360c28e36dd20af93f3bfc568dd3966fc83c04141072df9c4dfaa093`  
		Last Modified: Sun, 19 Apr 2026 19:25:37 GMT  
		Size: 618.7 KB (618733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3074ff25c3631259a3cfed477279e2b1ca9cc765a2b27ac6ff08e956a86966c8`  
		Last Modified: Sun, 19 Apr 2026 19:25:37 GMT  
		Size: 8.1 KB (8132 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-alpine3.22` - linux; s390x

```console
$ docker pull hylang@sha256:e8c257387c5d11ed3d3b82cd07a633f8368292c0e0a26e5408ed479db2f2b50a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.4 MB (22414055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb28f6394bb76a3b0a7a1a8adc6e3074ab0cdbd84f154c6818f260e4556f3cb1`
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
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 01:54:20 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 01:54:20 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 02:16:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 02:16:00 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 02:16:00 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:16:54 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:16:54 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:16:54 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:16:54 GMT
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
	-	`sha256:0dd80b0fabfbc310dbd47303215b6c3f9ac715a01f2d6b15a9e7b74c5435a907`  
		Last Modified: Fri, 17 Apr 2026 02:16:11 GMT  
		Size: 12.9 MB (12930014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8ffbc1151f3980466369850c5906f90dbf648f521e1b0f90d087b53216a9d7`  
		Last Modified: Fri, 17 Apr 2026 02:16:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296406abf14122696203982d1fd0771eca98844fdbac27037c94b4f3364b9641`  
		Last Modified: Wed, 27 May 2026 00:17:08 GMT  
		Size: 5.4 MB (5373911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:1d79cfc80b1a288e66aba3c5fc12b80eeb162a6c4fdad35f58c424896be634e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.8 KB (626791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dbec7c5215c2a532d13d27575c144e61767da6c0635bd49ed897346b6b35d11`

```dockerfile
```

-	Layers:
	-	`sha256:2ecd2b83efaf4c63c1ff2aa8443dddf86662c0928188ab00c48d4da323749973`  
		Last Modified: Wed, 27 May 2026 00:17:07 GMT  
		Size: 618.7 KB (618703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:653601f32dd9831f68ced771630be4b940ff06d17b13376ffab2e1508a332858`  
		Last Modified: Wed, 27 May 2026 00:17:07 GMT  
		Size: 8.1 KB (8088 bytes)  
		MIME: application/vnd.in-toto+json
