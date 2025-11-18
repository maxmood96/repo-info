## `hylang:bookworm`

```console
$ docker pull hylang@sha256:ecec0958b67ce4fb876325b89cf8c42d77b080de7b3918afc8e46f3924d75ef6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `hylang:bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:44042f76d6e17d42b295989f89e6bf4fdee8b7095cafe689d49f1cbfa667ebb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50347875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf1003ca07b911ca3cd09ce75cc58217553e40ec5c9efa433b39e4e7baa5de0`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:49:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:49:12 GMT
ENV PYTHON_VERSION=3.14.0
# Tue, 18 Nov 2025 05:49:12 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Tue, 18 Nov 2025 05:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 18 Nov 2025 05:58:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 18 Nov 2025 05:58:59 GMT
CMD ["python3"]
# Tue, 18 Nov 2025 07:10:07 GMT
ENV HY_VERSION=1.1.0
# Tue, 18 Nov 2025 07:10:07 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 18 Nov 2025 07:10:07 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 18 Nov 2025 07:10:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c4978290e9e80620919d3d9f2092dc28f2c39e323168bae3e8f9792de41177`  
		Last Modified: Tue, 18 Nov 2025 05:59:12 GMT  
		Size: 3.5 MB (3515872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4286962e54ec357ab9c3660841e126a1744f0014b38ecafce0f4f3e523405c`  
		Last Modified: Tue, 18 Nov 2025 05:59:12 GMT  
		Size: 12.8 MB (12844252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac4fa5ee453a5333eba749adcd6026cdb202b1ca1b313fe33c6e6e440e44acf`  
		Last Modified: Tue, 18 Nov 2025 05:59:11 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458259935a45dc3615d14bf9df30817abe79eb18f84a91685debbe8e66d295d4`  
		Last Modified: Tue, 18 Nov 2025 07:10:20 GMT  
		Size: 5.8 MB (5759052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:4943eab258abcdb6fe52cc8142e59e25007d58dc8ec1030ea236ee1d1696aee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2541990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a148a29ffb8b98b967c5b2ce98edbd0aab83ecbcb68b3447b1ffe6adbfed3ed5`

```dockerfile
```

-	Layers:
	-	`sha256:076914b895c130a746b8eaec9251b57213d9797ab09c8580799cf6ba4864a1d2`  
		Last Modified: Tue, 18 Nov 2025 09:18:57 GMT  
		Size: 2.5 MB (2532731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf989e5579ae3586de744d1647641c6d027b85d6d66a33f772aab039d9d5748c`  
		Last Modified: Tue, 18 Nov 2025 09:18:58 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:14d6384ed8eeeab1cb48477b4d970a25fa4bf48c38e27f08ddaf352a7348c9a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46989748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:260fe1dc469e00ddf5bb22019b050d9d6a706b4e5896f42a1f46ea5e082c3dbc`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:58:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:58:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:58:05 GMT
ENV PYTHON_VERSION=3.14.0
# Tue, 18 Nov 2025 03:58:05 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Tue, 18 Nov 2025 04:18:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 18 Nov 2025 04:18:24 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 18 Nov 2025 04:18:24 GMT
CMD ["python3"]
# Tue, 18 Nov 2025 05:31:33 GMT
ENV HY_VERSION=1.1.0
# Tue, 18 Nov 2025 05:31:33 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 18 Nov 2025 05:31:33 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 18 Nov 2025 05:31:33 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c97fff5eb07550dcbd62ce4fa3fb5ea12d73e0d973b150828279c3d911c81f0f`  
		Last Modified: Tue, 18 Nov 2025 01:13:41 GMT  
		Size: 25.8 MB (25757530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb00d43a8cb2ece14b680b5c0009074f8ae060cdfd684c52fc7a84f338ff57ff`  
		Last Modified: Tue, 18 Nov 2025 04:18:36 GMT  
		Size: 3.1 MB (3090755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4d84d32ce5b46b033b564f6d6e1164656e31ea9a35716025bc14dc7615c41b`  
		Last Modified: Tue, 18 Nov 2025 04:18:36 GMT  
		Size: 12.4 MB (12382005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faad7042290b60cce422c6c0d0d93e923667be0f58cc88eaf9cb538b46aa0697`  
		Last Modified: Tue, 18 Nov 2025 04:18:36 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d448365f809d53bbcc87063152a008f579751caef0d01025b9e1025e7409309`  
		Last Modified: Tue, 18 Nov 2025 05:31:47 GMT  
		Size: 5.8 MB (5759209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:503ff3dcb5208abba48f556ace618713f3f8e86874fb6ff0111e15319e7d8dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c45aa8e45e4c29a80a12bf9823729b0b302a6c0dd6ce520c242b808f8066d4`

```dockerfile
```

-	Layers:
	-	`sha256:96fa5fcd53a8df14580d0986ccb99aba968e038684e570e2d36854840e8b45c8`  
		Last Modified: Tue, 18 Nov 2025 06:18:59 GMT  
		Size: 2.5 MB (2536575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e96aab20315158b2579fb8d43d2fb92f7dd4f28fb00790d8b813257c67f4a9`  
		Last Modified: Tue, 18 Nov 2025 06:19:01 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:667d9b62655b327d6b8108a39e8254b11e0a47a57ed82448bdb3ce7820a0df5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44605609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25cc8bb34e6cf270687f5b6147cf9de6f3fb2984c7cd619694decd29d4c971af`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:38:50 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:38:50 GMT
ENV PYTHON_VERSION=3.14.0
# Tue, 18 Nov 2025 04:38:50 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Tue, 18 Nov 2025 04:58:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 18 Nov 2025 04:58:36 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 18 Nov 2025 04:58:36 GMT
CMD ["python3"]
# Tue, 18 Nov 2025 07:27:22 GMT
ENV HY_VERSION=1.1.0
# Tue, 18 Nov 2025 07:27:22 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 18 Nov 2025 07:27:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 18 Nov 2025 07:27:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:56c31a75d861775217bba58452ad642136804e02ff927a701d20990b4efd6793`  
		Last Modified: Tue, 18 Nov 2025 01:13:27 GMT  
		Size: 23.9 MB (23934009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113a6f6d7cd3ba0ae2960d64daa68674bd637bd0183290bdaff83998e81fb9ec`  
		Last Modified: Tue, 18 Nov 2025 04:58:50 GMT  
		Size: 2.9 MB (2925446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39dcc5d7a47f9bf4663ea221375a0edcb5f507e2ed9b3229e14e0bedd67a13a`  
		Last Modified: Tue, 18 Nov 2025 04:58:50 GMT  
		Size: 12.0 MB (11986578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86b8ffe237f84636521e19a4159a65744636611b5fdca1a071258ed85f413f2`  
		Last Modified: Tue, 18 Nov 2025 04:58:49 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f11b110e38699262b3d795c11e530d19b9012e01dae60c264d06317f94c381`  
		Last Modified: Tue, 18 Nov 2025 07:27:35 GMT  
		Size: 5.8 MB (5759327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:aa0f9a187082ad9d828a728913b1aa5dd35f8e511d33431c668e917c14366384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2544379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627b461263c174dde2471ae0f6c0023e63a03c424903794bfc405e601bf55a44`

```dockerfile
```

-	Layers:
	-	`sha256:402a507043baf72ff40767a6b9ff1f9103b42fb5adc1d0f9317808af0a5263c0`  
		Last Modified: Tue, 18 Nov 2025 09:22:27 GMT  
		Size: 2.5 MB (2535008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:988db3b59f0fe1dbe666295b89e81e9a7fa231f46478f05ad8891897d13ef1af`  
		Last Modified: Tue, 18 Nov 2025 09:22:27 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:e29d4e48805888d4077bcc46c832bf92adacd42ea3cc5199a8c038df54e5672f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49948509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f5cf65dde65944f85f532f6082c9986c72ef1784ebb487bf557e593041129e`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:31:28 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:31:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:31:28 GMT
ENV PYTHON_VERSION=3.14.0
# Tue, 18 Nov 2025 04:31:28 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Tue, 18 Nov 2025 04:45:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 18 Nov 2025 04:45:30 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 18 Nov 2025 04:45:30 GMT
CMD ["python3"]
# Tue, 18 Nov 2025 06:16:55 GMT
ENV HY_VERSION=1.1.0
# Tue, 18 Nov 2025 06:16:55 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 18 Nov 2025 06:16:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 18 Nov 2025 06:16:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c5ebef4249710973f7885882fb37ada1ae9a1f1fc653fa4c937377426e3533`  
		Last Modified: Tue, 18 Nov 2025 04:45:44 GMT  
		Size: 3.3 MB (3349153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69870e2bc98fb44caf91980c837769b6541587a5e87f4ce6fb2574a8dae596b2`  
		Last Modified: Tue, 18 Nov 2025 04:45:44 GMT  
		Size: 12.7 MB (12737778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d26ed09fc5258b5b6695cfabf691efc3177e1d1fe751d19f5d4eb9d651c5d1`  
		Last Modified: Tue, 18 Nov 2025 04:45:43 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6165cc63ef911324fb977e245f35f09a172dbe9a0e1b3576ece631f8cd8abb7`  
		Last Modified: Tue, 18 Nov 2025 06:17:08 GMT  
		Size: 5.8 MB (5759121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:b5aa0e25af2b0e8fd01d2c60aa57d6fc69acbf9eabd67d234247a2cb6f57ae3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebc4a855c14721a7dbaff2ecc084597b912099423bda8bbdc949d71be59671b`

```dockerfile
```

-	Layers:
	-	`sha256:cc5a408b45e940659e7c545bd4a61e6e0efd8c5a90bb1442872abd99b8c7659a`  
		Last Modified: Tue, 18 Nov 2025 09:22:31 GMT  
		Size: 2.5 MB (2533044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:761ec738d8cdc3b4c0a89e02d40dd422a9d20b4485e3c58bb4b8f9bec847a95a`  
		Last Modified: Tue, 18 Nov 2025 09:22:32 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:bookworm` - linux; 386

```console
$ docker pull hylang@sha256:f548e6b2ce3ab9beb83fc4620ece5e7b3b72befa9a4e6f729321e48fcd090ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51609753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3f379e991374e848bb1861ebacc996432288ae1c82c8dedb43ea7f67583d5a`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:27:18 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:27:18 GMT
ENV PYTHON_VERSION=3.14.0
# Tue, 18 Nov 2025 03:27:18 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Tue, 18 Nov 2025 03:40:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 18 Nov 2025 03:40:00 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 18 Nov 2025 03:40:00 GMT
CMD ["python3"]
# Tue, 18 Nov 2025 05:20:32 GMT
ENV HY_VERSION=1.1.0
# Tue, 18 Nov 2025 05:20:32 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 18 Nov 2025 05:20:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 18 Nov 2025 05:20:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfcd399c0301f0dacbd8e173937bf7d5527aa84f7794d3393b64cf7f416ac33a`  
		Last Modified: Tue, 18 Nov 2025 03:40:15 GMT  
		Size: 3.5 MB (3516575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6007c9acf74b20952cf8b2663f40a03a7901daeb36243d9b263fcd33283fd96c`  
		Last Modified: Tue, 18 Nov 2025 03:40:15 GMT  
		Size: 13.1 MB (13123889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e62808724b75ae66bcc7f3ca7276770cb1857d27ef585737040139bcfd65988`  
		Last Modified: Tue, 18 Nov 2025 03:40:14 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3884a8a0834e71b9671919b6b9e2f283f470ac351ae995fb824ba2773fae5a4`  
		Last Modified: Tue, 18 Nov 2025 05:20:45 GMT  
		Size: 5.8 MB (5759337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:edddb92cb76eb8518bbe2c5395861f1b0cce5893af5609480c4c2e30a1bbcf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2539085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ee2755406ee8e037bf896fb39d18d1a616afe8448e2b33bc96774337a55381`

```dockerfile
```

-	Layers:
	-	`sha256:f991ac10075b34df0a448d689942e22a4114dd4b399c81388013be4b834b6860`  
		Last Modified: Tue, 18 Nov 2025 09:22:36 GMT  
		Size: 2.5 MB (2529878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb6ed8cc88cd84aab43a66ce39d6d26e4abf026436319c8409a8dda10beaab1e`  
		Last Modified: Tue, 18 Nov 2025 09:22:37 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:2dcdf78d0c0c026ebc3a94c76bb4e8ffc25d439a505d692814463cfeefe7ecb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (54959569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34dece8ebc72b14792e807de1ee6202f716dd256cf0db72c05e8ff143068bf6d`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:57:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:57:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:57:59 GMT
ENV PYTHON_VERSION=3.14.0
# Tue, 18 Nov 2025 04:57:59 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Tue, 18 Nov 2025 05:21:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 18 Nov 2025 05:21:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 18 Nov 2025 05:21:40 GMT
CMD ["python3"]
# Tue, 18 Nov 2025 07:48:50 GMT
ENV HY_VERSION=1.1.0
# Tue, 18 Nov 2025 07:48:50 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 18 Nov 2025 07:48:50 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 18 Nov 2025 07:48:50 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bcd4a9df630c3cd42b7dae4063de889393a96227a9209ca113e387786cb78c`  
		Last Modified: Tue, 18 Nov 2025 05:19:47 GMT  
		Size: 3.7 MB (3721123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359b07d3138de9ca08c3fb708e19e475c931978a364309ce54608f1239943e72`  
		Last Modified: Tue, 18 Nov 2025 05:22:15 GMT  
		Size: 13.4 MB (13410032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ea52eae41aba1f434841529dd038591e4254d769c1c4dd861dc4993d88d322`  
		Last Modified: Tue, 18 Nov 2025 05:22:13 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d056883b5fe60a4c2d6a933d2daae412b460a6b518e8d15b3aa0b7f9103e031e`  
		Last Modified: Tue, 18 Nov 2025 07:49:25 GMT  
		Size: 5.8 MB (5759339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:6920db88ac9eb62f60a668c1567e57bae5ab262d63319a70fdc846dd0aca8f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2546520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab63db2d49c73f3a43107ffb3fd1f64302ccd7bc7493a2d8b0f1eb4e9e2233d`

```dockerfile
```

-	Layers:
	-	`sha256:9a8ffa062fee9a3923c3edd96d145174b174cdcb7255cd6aa31b3ea440bfe69e`  
		Last Modified: Tue, 18 Nov 2025 09:22:41 GMT  
		Size: 2.5 MB (2537193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40f595461482b6e4479933cb31db1aad16a314c2caa43852adc2dfc0921efd92`  
		Last Modified: Tue, 18 Nov 2025 09:22:41 GMT  
		Size: 9.3 KB (9327 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:f39fb25b646539a5cf7b10fbe4e0694f660eb352b28b440dcff18aeae5c63789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48507626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17303390c1b6d65b972356d37d8f6b1176fa17ec30bacda4ecf9390d66e379a3`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:39:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:39:22 GMT
ENV PYTHON_VERSION=3.14.0
# Tue, 18 Nov 2025 04:39:22 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Tue, 18 Nov 2025 04:54:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 18 Nov 2025 04:54:35 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 18 Nov 2025 04:54:35 GMT
CMD ["python3"]
# Tue, 18 Nov 2025 06:58:58 GMT
ENV HY_VERSION=1.1.0
# Tue, 18 Nov 2025 06:58:58 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 18 Nov 2025 06:58:58 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 18 Nov 2025 06:58:58 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf5506214a483caae7c5be1ecb5fa163feb5040404a41e9876529630ca141e2`  
		Last Modified: Tue, 18 Nov 2025 04:52:31 GMT  
		Size: 3.2 MB (3181819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20715cbde24a49580a0bf7eb5ef79107640ade0f1427b9dbb048a81fddc4ad62`  
		Last Modified: Tue, 18 Nov 2025 04:54:51 GMT  
		Size: 12.7 MB (12681459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17db300e5ee8e10fd2c19e327806450cb199bf178a9f7b028c40f5f074c1a5b`  
		Last Modified: Tue, 18 Nov 2025 04:54:51 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68599e424fc76624f13bd24a7b5ceeafbe1575075e395399779163ce8ab7a38`  
		Last Modified: Tue, 18 Nov 2025 06:59:33 GMT  
		Size: 5.8 MB (5759706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:fc9740f312ac45b275b3f670a9da0d1e82090e104a5a31ee951f3329d49beee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180b06b8847d8acce2eb373f769b74303f521d966956f0cb21e6055dc8b1665d`

```dockerfile
```

-	Layers:
	-	`sha256:9b20c9a1b4f461f381c57c7f6bec5522fe64a8d0795cc801b7e7090f602bd91c`  
		Last Modified: Tue, 18 Nov 2025 09:22:46 GMT  
		Size: 2.5 MB (2529555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24deacb482d68dd1f99726521c1166a063bdcca2e4e226a92cded95cc36c25f2`  
		Last Modified: Tue, 18 Nov 2025 09:22:46 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.in-toto+json
