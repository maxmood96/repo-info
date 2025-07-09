## `hylang:1-python3.14-rc-bullseye`

```console
$ docker pull hylang@sha256:f737e649ca863480c0d131580eae0968f5da5bf511e6402d84ca02d6a46164fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:1-python3.14-rc-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:f5afa5140d6302b23e984ecff66b70b73f23ed453d874c85facb87500f8a4f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50414641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3efa70f14d7cdde53c45a860890c1be4c1a3d91701b35b95309dd4764a941fd1`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Tue, 08 Jul 2025 15:49:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Jul 2025 15:49:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 15:49:29 GMT
ENV PYTHON_VERSION=3.14.0b4
# Tue, 08 Jul 2025 15:49:29 GMT
ENV PYTHON_SHA256=15e123e056abebba6de5e73cfa304459a8c82cafa85d4fc7fc6de80e6a3e1b39
# Tue, 08 Jul 2025 15:49:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Jul 2025 15:49:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Jul 2025 15:49:29 GMT
CMD ["python3"]
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 16:37:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Jul 2025 16:37:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89816c90aafd39769ba92b46d25c6591319eea2ff685ca81fc929b3b09da8b5c`  
		Last Modified: Tue, 08 Jul 2025 21:07:36 GMT  
		Size: 1.1 MB (1077884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0ac226ccbad3042010225ba0b41ed34503793c0a59f52d5239c93a8e820a2b`  
		Last Modified: Tue, 08 Jul 2025 21:07:37 GMT  
		Size: 13.2 MB (13238801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d89d88dfb92c47d30cfed92cb4ef51ee822bbb29c1e9537f7a6ec4ed37a486`  
		Last Modified: Tue, 08 Jul 2025 21:07:37 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8245d41029c5476037f1819a0c122d81ae976cae155012147e285b792f9b728e`  
		Last Modified: Wed, 09 Jul 2025 15:00:05 GMT  
		Size: 5.8 MB (5841659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:52506e10435c80254c0414ca0f2614f62d7a73262c8a092aed027201eaebffc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2828502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2880065bda15c109e47827e9e3a1a00fee59cbe68e2bc8aca146708e5b7fec89`

```dockerfile
```

-	Layers:
	-	`sha256:29fe9a9ee9d2369bc1c4ffeab797a4d1f5ff72a6ad1302b8156c17a049ffeca4`  
		Last Modified: Tue, 08 Jul 2025 23:19:44 GMT  
		Size: 2.8 MB (2820501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea75fb3d35dab8f9173d8b429280b97c1052e93fd991a5bd60bf1729bac4cf70`  
		Last Modified: Tue, 08 Jul 2025 23:19:44 GMT  
		Size: 8.0 KB (8001 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:e08c8b959a5b8057962eafe22080ca852bb3cf07429b6726bda3a169a6185474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44815670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0e4f3a6c3536cccf84c625cfef119cf526d5ba3536282df9049f9d07d5dfb2`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1751241600'
# Tue, 08 Jul 2025 15:49:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Jul 2025 15:49:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 15:49:29 GMT
ENV PYTHON_VERSION=3.14.0b4
# Tue, 08 Jul 2025 15:49:29 GMT
ENV PYTHON_SHA256=15e123e056abebba6de5e73cfa304459a8c82cafa85d4fc7fc6de80e6a3e1b39
# Tue, 08 Jul 2025 15:49:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Jul 2025 15:49:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Jul 2025 15:49:29 GMT
CMD ["python3"]
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 16:37:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Jul 2025 16:37:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:96b51e81cdb8508366118f41a9ec499f52f0d0211b084d5d516e1be131b35266`  
		Last Modified: Tue, 01 Jul 2025 01:15:21 GMT  
		Size: 25.5 MB (25544163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaceb2398d483b38c56e706771d4b949b87b6cc3198fb4676caadcefa977ad43`  
		Last Modified: Tue, 01 Jul 2025 11:52:32 GMT  
		Size: 1.0 MB (1042888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af210564775b4e2d185c7e3b8050b98ffb470ce0d452d9e2437d1583b4c2fc4`  
		Last Modified: Tue, 08 Jul 2025 23:20:19 GMT  
		Size: 12.4 MB (12386679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925378ae181f7b9d0a79ec11200e6148ec1ed9bba7852a0f086dbf8fc8cb181d`  
		Last Modified: Tue, 08 Jul 2025 23:20:18 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3167b74e508951f41ceb932317f73c3aa0c95eea4e676fb779f03e622f226180`  
		Last Modified: Tue, 08 Jul 2025 22:07:56 GMT  
		Size: 5.8 MB (5841691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:448f3897dc33f21202b567aee49699aaf3bf4bc3c98156d2116e41a3052c4725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2830823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17a45f9fd0f1a0a7df01336763ea3ca1eabeb5065de48f4bfda8dd932c6565a4`

```dockerfile
```

-	Layers:
	-	`sha256:8d27317cbf6f35e7c3c5542a68ea5a2e219416dbd52832844f80614e11c2d963`  
		Last Modified: Tue, 08 Jul 2025 23:19:49 GMT  
		Size: 2.8 MB (2822746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7787f2b541d2be605a54b9f3ab17a5e31332f8f173f262465e20da485a03e9a`  
		Last Modified: Tue, 08 Jul 2025 23:19:50 GMT  
		Size: 8.1 KB (8077 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:ca0711d267a70efca728ddb8a5f72d643f89803ff6b7cc7179d781e1c8eddf5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48926598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c816af3bafc1f0589da305bac9d382a3ce789b8f14ea158374ac1555bb3989`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Tue, 08 Jul 2025 15:49:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Jul 2025 15:49:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 15:49:29 GMT
ENV PYTHON_VERSION=3.14.0b4
# Tue, 08 Jul 2025 15:49:29 GMT
ENV PYTHON_SHA256=15e123e056abebba6de5e73cfa304459a8c82cafa85d4fc7fc6de80e6a3e1b39
# Tue, 08 Jul 2025 15:49:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Jul 2025 15:49:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Jul 2025 15:49:29 GMT
CMD ["python3"]
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 16:37:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Jul 2025 16:37:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c0e25075b051decf050e3330687e2dd6ade3d7e05a0143b22d2e6f6237ed59`  
		Last Modified: Wed, 09 Jul 2025 01:31:43 GMT  
		Size: 1.1 MB (1065704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837ba87fa317b75c57f3908e14caf7ca519145611b46f0bae1ca22719a61d7d7`  
		Last Modified: Wed, 09 Jul 2025 01:31:45 GMT  
		Size: 13.3 MB (13274755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7994977bc1e6e55b5f5ad452c19ead1c3e30a99eba7a7695b71130b6d5ce6c22`  
		Last Modified: Wed, 09 Jul 2025 01:31:47 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e54ca92b2a97b4e0eab28ab933c3efc23e11a805eb2429cfcae6617ef6f9e31`  
		Last Modified: Wed, 09 Jul 2025 19:57:49 GMT  
		Size: 5.8 MB (5841749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:f4c356f9fa1eefb23a15f7d41484b3dfc827822dead11063abd08b5c20b145b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2828864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abc3f220df71041db6b4ae053c81fef6bf44f40be6abdcbfa7d3cbbbd5c0cc3`

```dockerfile
```

-	Layers:
	-	`sha256:c1e8b6dd5efc8b2aed9af8588d0f6c61143cc5001cc8c911c47fb2dd3d3f3cb4`  
		Last Modified: Tue, 08 Jul 2025 23:19:54 GMT  
		Size: 2.8 MB (2820760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3bac30f038af032450837acc385b5915a1ca32ec4442c0686b6b996f8d51086`  
		Last Modified: Tue, 08 Jul 2025 23:19:54 GMT  
		Size: 8.1 KB (8104 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:73ee8232871775a10d6986f28b01a22f34b8c9dfe1c284ce723d9c33525a4b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51529511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492dffd69ccb6880c2d2c5d54691d65de0f928d65107a4e27efdc9dfafebd8f6`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Tue, 08 Jul 2025 15:49:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Jul 2025 15:49:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 15:49:29 GMT
ENV PYTHON_VERSION=3.14.0b4
# Tue, 08 Jul 2025 15:49:29 GMT
ENV PYTHON_SHA256=15e123e056abebba6de5e73cfa304459a8c82cafa85d4fc7fc6de80e6a3e1b39
# Tue, 08 Jul 2025 15:49:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Jul 2025 15:49:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Jul 2025 15:49:29 GMT
CMD ["python3"]
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 16:37:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Jul 2025 16:37:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:40be1da6146972d9df50a98eef7b5c0f729cd95a3a38782418f354f3b9355a9a`  
		Last Modified: Tue, 01 Jul 2025 01:14:57 GMT  
		Size: 31.2 MB (31189680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b985a1d742f64d59279ebf4bda7c581e465ed5a6eddc53e67fae0e0eb963f793`  
		Last Modified: Tue, 08 Jul 2025 21:07:50 GMT  
		Size: 1.1 MB (1090530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebccd72dcd12ee9791044c9f712463b819133039d184b7d1516761d6a4433502`  
		Last Modified: Tue, 08 Jul 2025 21:07:50 GMT  
		Size: 13.4 MB (13407344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ab58f2f909ac083f939559bc06b36037578367eadf5776eed56e1b92580b0a`  
		Last Modified: Tue, 08 Jul 2025 21:07:50 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4789a44110a2c0d51fb3057e7a6a99ca984a7126d6bd6452d2ca5971e49d115`  
		Last Modified: Tue, 08 Jul 2025 21:08:12 GMT  
		Size: 5.8 MB (5841707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:cf40082b6070407b85f00b7d903dd5041255a3d633196d8dfc4735c188061db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2825633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4fc955d975b71fc3457690eca487fc84946304fede6ebac667dc17d90a083f`

```dockerfile
```

-	Layers:
	-	`sha256:c2166e02b408cff81dd138d5226e4a68ee7d6c20cc446d347ee060789323df95`  
		Last Modified: Tue, 08 Jul 2025 23:19:58 GMT  
		Size: 2.8 MB (2817664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfc8bc567e1a9770d3c832b439c2bdab49711745a19bc6784047dde65c292106`  
		Last Modified: Tue, 08 Jul 2025 23:19:59 GMT  
		Size: 8.0 KB (7969 bytes)  
		MIME: application/vnd.in-toto+json
