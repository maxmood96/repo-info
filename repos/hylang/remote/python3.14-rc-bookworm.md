## `hylang:python3.14-rc-bookworm`

```console
$ docker pull hylang@sha256:453e8a0188375050797de5e8cfe72a945964c478fc4d8bcdf8a5bd1e516134ed
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

### `hylang:python3.14-rc-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:d579e4c5967e637d6d88c6e0931f6517368b1b7fa647a525b5c4cfdc46a5a1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50530145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd6f0cce9cd237054521cd7ba61dbc8f72556d709cd36637419fd31052c6235`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 09 May 2025 15:36:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Fri, 09 May 2025 15:36:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 May 2025 15:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 May 2025 15:36:44 GMT
ENV PYTHON_VERSION=3.14.0b2
# Fri, 09 May 2025 15:36:44 GMT
ENV PYTHON_SHA256=7ac9e84844bbc0a5a8f1f79a37a68b3b8caf2a58b4aa5999c49227cb36e70ea6
# Fri, 09 May 2025 15:36:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 09 May 2025 15:36:44 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b325d293a1359ee172e5fd4615925d0ae8e7f8d9bdbe8c8fbbc51df456096990`  
		Last Modified: Tue, 27 May 2025 19:16:25 GMT  
		Size: 3.5 MB (3511874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ed0ab6d9fdaf3b897d47dcf7e2f0a2c05054e5b36ac39206f10e463aca62ed`  
		Last Modified: Tue, 27 May 2025 19:16:26 GMT  
		Size: 13.0 MB (12953879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8415ef7ce9a2094f1e9cf6c2fbd2961dc98d4f60f36bb865a0337c64a35e94`  
		Last Modified: Tue, 27 May 2025 19:16:25 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133c56f686a752a0aa6a65e1a30c4f8220dd3468d2b51c297711beac22481ddf`  
		Last Modified: Tue, 27 May 2025 20:09:04 GMT  
		Size: 5.8 MB (5838812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:ac662fa32ddd574c5845c6bef9052faa1bb19d1d25b8abe7fd2d2ba3461978c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2445650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c87ccb50a72617ec3818fdeb47dc62b8aa2a61ef59ff2593e5c248be4bea6c`

```dockerfile
```

-	Layers:
	-	`sha256:ca0b2546b057ca36731c9af9c27cea333f04994b2571e67142f519ea4812a562`  
		Last Modified: Tue, 27 May 2025 20:09:04 GMT  
		Size: 2.4 MB (2436377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22a7a3e5ed1ddad548a9a0cdc88f20b75b84a2c0ae0653c726efc83236c8430f`  
		Last Modified: Tue, 27 May 2025 20:09:04 GMT  
		Size: 9.3 KB (9273 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:8cead8d755848aab5b72576862a336914dd0410cbeef01065c51f898cf99539d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47166442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925ebe821e81e3cf8f56e82cad52b8d44729c1aa1fe6ef2136e56064c0cbbc2e`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 09 May 2025 15:36:44 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Fri, 09 May 2025 15:36:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 May 2025 15:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 May 2025 15:36:44 GMT
ENV PYTHON_VERSION=3.14.0b2
# Fri, 09 May 2025 15:36:44 GMT
ENV PYTHON_SHA256=7ac9e84844bbc0a5a8f1f79a37a68b3b8caf2a58b4aa5999c49227cb36e70ea6
# Fri, 09 May 2025 15:36:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 09 May 2025 15:36:44 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d78d4f876460f6e79885e30d4a3563545b64c1ed8e7f4bbc7d54f9689a745d4`  
		Last Modified: Thu, 22 May 2025 02:40:13 GMT  
		Size: 3.1 MB (3085134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643936952d6fe932920ed25ed7c038671d0eeb8ba57b6a058bdbcdb11d31ba18`  
		Last Modified: Tue, 27 May 2025 19:47:48 GMT  
		Size: 12.5 MB (12485261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c71b3417a3cb1910717b5047c3e0bddd75700043cd70b661883a21f2a11f4a`  
		Last Modified: Tue, 27 May 2025 19:47:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f128ebcde917fe8e231efbf379a4ca9087d16e299b8477f23166305d2ef9170f`  
		Last Modified: Tue, 27 May 2025 20:08:38 GMT  
		Size: 5.8 MB (5838901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:ef5dba410a95758e7cce5ea8bfc9df08267b698bcf5052728042de10a962b608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2449602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d609b35b27fab65625e1e009336a5635e5384ed5f0c2f69242c9cb19c620d0b`

```dockerfile
```

-	Layers:
	-	`sha256:2edd729476bf3911a9e8d4af91267e683adc9490dd069979a962dffeb19ec21a`  
		Last Modified: Tue, 27 May 2025 20:08:38 GMT  
		Size: 2.4 MB (2440221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:332631f10b49f24e24083ad7d4b13cd307051f9ad2929104a2e84db68c9ec5f0`  
		Last Modified: Tue, 27 May 2025 20:08:37 GMT  
		Size: 9.4 KB (9381 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:c45d2723f326837ae4343d9d5042f856f8df0bde88ec975b0e93a498443265a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44787151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59231b81669eb36a29a00e081a138f81d4a2dab9b17503ad2b9e898f6ef4deb7`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 09 May 2025 15:36:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Fri, 09 May 2025 15:36:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 May 2025 15:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 May 2025 15:36:44 GMT
ENV PYTHON_VERSION=3.14.0b2
# Fri, 09 May 2025 15:36:44 GMT
ENV PYTHON_SHA256=7ac9e84844bbc0a5a8f1f79a37a68b3b8caf2a58b4aa5999c49227cb36e70ea6
# Fri, 09 May 2025 15:36:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 09 May 2025 15:36:44 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c62e8d6ce033c3cdd5f768c45f28d95065a01f7494bd5d0c240723c969de447`  
		Last Modified: Thu, 22 May 2025 05:15:31 GMT  
		Size: 2.9 MB (2919654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a22ab752b3f2b497ea1040eda113002235cda1a0bb08d42b416090ff058417`  
		Last Modified: Tue, 27 May 2025 20:05:35 GMT  
		Size: 12.1 MB (12095385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd4266303c62025ad9d2974a4b4ddd20622d357064ab285599a21b716d00473`  
		Last Modified: Tue, 27 May 2025 20:05:35 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05999ef2d9d61432c31c3d2b9ac19f2532e65cf398b8f451d72ea6b2e4318d91`  
		Last Modified: Tue, 27 May 2025 21:07:50 GMT  
		Size: 5.8 MB (5838942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:117e45838e3c859a5aacca186f7577bbd45584022afba61d5aed7e4c055f76cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2448035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eae8e112ee77088d2b5ea1644625a7d9139737b5649ccd8fb83aaf359befe49`

```dockerfile
```

-	Layers:
	-	`sha256:04cebf0c5913c2a44219a0fba00cf2863f02c058a03b8242839f99a30e249fb5`  
		Last Modified: Tue, 27 May 2025 21:07:50 GMT  
		Size: 2.4 MB (2438654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:987aef7a9aa9e464cfd9f442201bf089bf715297083607bd6cc8e83045e0c906`  
		Last Modified: Tue, 27 May 2025 21:07:49 GMT  
		Size: 9.4 KB (9381 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:bd4df01fb7bfe33e5c6d51105a48f6e030766e298956465b4d6019a92d118d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50072664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0880a3f056625d5dd681e944823eef6042f518f58e38d9af852f71ffd87dee16`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 09 May 2025 15:36:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Fri, 09 May 2025 15:36:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 May 2025 15:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 May 2025 15:36:44 GMT
ENV PYTHON_VERSION=3.14.0b2
# Fri, 09 May 2025 15:36:44 GMT
ENV PYTHON_SHA256=7ac9e84844bbc0a5a8f1f79a37a68b3b8caf2a58b4aa5999c49227cb36e70ea6
# Fri, 09 May 2025 15:36:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 09 May 2025 15:36:44 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ecf2f954c44733fc53cf15eaf87d82d7d93595479119ee9a78962db5701bf9`  
		Last Modified: Tue, 27 May 2025 20:36:08 GMT  
		Size: 3.3 MB (3333480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43aa235024731e8a181c7787f4a0d8faa4357ca2849ab0066e52ce5e9eeda3d`  
		Last Modified: Tue, 27 May 2025 20:36:08 GMT  
		Size: 12.8 MB (12834813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6269c4722de1f8b8a24735c2630841954dd644b1258c71a53e4845dc67525767`  
		Last Modified: Tue, 27 May 2025 20:36:08 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698b661deb5f00e9f71de5bd93adcbe058fea9b36918befdf0166263f4838c4e`  
		Last Modified: Tue, 27 May 2025 21:57:17 GMT  
		Size: 5.8 MB (5838842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:447af79099651244b586977d79dfb13c72db41c319a07fe31499038c23a0cb48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2446115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a39f7fd97a299cf7a37d0b9f67ed2b95f8504d2d043cb9eca3a9d558ea970da`

```dockerfile
```

-	Layers:
	-	`sha256:60b06ae16118560594b7d6dd85fb1ffb547b19cc094f32a7e30bf1f0b8fd7cf7`  
		Last Modified: Tue, 27 May 2025 21:57:17 GMT  
		Size: 2.4 MB (2436690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c3ef9587b98e619dc8fa7bdb746d0aec7527c5fef1f4aaa3d21e258c04c5088`  
		Last Modified: Tue, 27 May 2025 21:57:17 GMT  
		Size: 9.4 KB (9425 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:d345ea6d6244ee6059bb154383f95b0d7d0076bbf8641996d77bb78271e2a1f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51776841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bcc149627128e7b56f0645da9482a7e91f51ba8b3426781fae31963b4a61ba`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 09 May 2025 15:36:44 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Fri, 09 May 2025 15:36:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 May 2025 15:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 May 2025 15:36:44 GMT
ENV PYTHON_VERSION=3.14.0b2
# Fri, 09 May 2025 15:36:44 GMT
ENV PYTHON_SHA256=7ac9e84844bbc0a5a8f1f79a37a68b3b8caf2a58b4aa5999c49227cb36e70ea6
# Fri, 09 May 2025 15:36:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 09 May 2025 15:36:44 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748312ca7c296b46c5a4acedd288cb87b7a180044f9ba073b3442b2cd022d802`  
		Last Modified: Tue, 27 May 2025 19:18:56 GMT  
		Size: 3.5 MB (3511101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bd166a6b131b236ecc4b25229ef22803b677d815989982e47d44f905e8b707`  
		Last Modified: Tue, 27 May 2025 19:18:56 GMT  
		Size: 13.2 MB (13219097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0284dc03201bb74eb7df0e038c214d018688ef8e1254524a3050da41e8f1b8e`  
		Last Modified: Tue, 27 May 2025 19:18:55 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa139c3c2c396265f3b01319d4eb0d71c314953e58ce608251f0a71a34bbe120`  
		Last Modified: Tue, 27 May 2025 20:09:14 GMT  
		Size: 5.8 MB (5838908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:00177bf49c497b97e574f1e692e83faea78f59748911f744c6493cd2fce8237a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2442745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efda9d5248aefe1efa69fc00da303f8298050d9208b9fbbd633d34eb4611f376`

```dockerfile
```

-	Layers:
	-	`sha256:9b78b88cfa3a0c34260364fc23315ebad9656d474a9a18c85ef6f7a8f68f2b7b`  
		Last Modified: Tue, 27 May 2025 20:09:14 GMT  
		Size: 2.4 MB (2433524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5595c6ed299c282c250c061a55bc7ca0ea320a0d9d20ffb03828593a2201a8f7`  
		Last Modified: Tue, 27 May 2025 20:09:14 GMT  
		Size: 9.2 KB (9221 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:71008dd075cad90e4baa06752a771df7cfae459d9a88bd9543a58c2ce3048d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55138829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bdba399a99276189750ed24ede7528bb62ef5f6949376a1e22c6f9304ce0415`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 09 May 2025 15:36:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Fri, 09 May 2025 15:36:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 May 2025 15:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 May 2025 15:36:44 GMT
ENV PYTHON_VERSION=3.14.0b2
# Fri, 09 May 2025 15:36:44 GMT
ENV PYTHON_SHA256=7ac9e84844bbc0a5a8f1f79a37a68b3b8caf2a58b4aa5999c49227cb36e70ea6
# Fri, 09 May 2025 15:36:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 09 May 2025 15:36:44 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Wed, 21 May 2025 22:28:16 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efb614459ee156d8da1b529ee09d4d6823feb7dd9ae28ac3c6babac9930e1bb`  
		Last Modified: Thu, 22 May 2025 09:12:41 GMT  
		Size: 3.7 MB (3716190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc8a00ae4d82246a4d26162c63262ca83a329b544849f61ddb44c8943e87d1f`  
		Last Modified: Tue, 27 May 2025 20:21:26 GMT  
		Size: 13.5 MB (13516494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac1f01988b576909aea0132410c551b52dfd42d3d6946c8fd5f480ee58859b7`  
		Last Modified: Tue, 27 May 2025 20:21:25 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3417703ae007d703a55933de52c39704093526e068a96cb1513347ed1ae6083`  
		Last Modified: Tue, 27 May 2025 20:43:39 GMT  
		Size: 5.8 MB (5838983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:70613fe83b17f97781a2e34d231fb45732d8672b1612777f91a2c337e85ddda7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2450180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca6c7c2c8005a3a7205f622cb53bfb3fb77cd9289cd366932441d0dbc6dbb32`

```dockerfile
```

-	Layers:
	-	`sha256:93a2b48953cbb02f44de0a55d7d429cfeaa108ff8ebd5175f26065a678c14aa1`  
		Last Modified: Tue, 27 May 2025 20:43:38 GMT  
		Size: 2.4 MB (2440839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83c0a423fad4cacb8e481f4ab8b6b40fda153cf17540f3d37a3a53e730576219`  
		Last Modified: Tue, 27 May 2025 20:43:38 GMT  
		Size: 9.3 KB (9341 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:cef60333b02f9476e4e81469b83c03f99537afce4476c390444e32c56c7c7e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48682730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1dad37591e6a0523012e2c3a4aba45ee7ee07dc4ff13ba6768534d47085fb35`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 09 May 2025 15:36:44 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Fri, 09 May 2025 15:36:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 May 2025 15:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 May 2025 15:36:44 GMT
ENV PYTHON_VERSION=3.14.0b2
# Fri, 09 May 2025 15:36:44 GMT
ENV PYTHON_SHA256=7ac9e84844bbc0a5a8f1f79a37a68b3b8caf2a58b4aa5999c49227cb36e70ea6
# Fri, 09 May 2025 15:36:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 09 May 2025 15:36:44 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ca0a6f1cbf84e313657fc4da4e1da95221c6f19c2384181373cbc26f63585d`  
		Last Modified: Thu, 22 May 2025 02:33:09 GMT  
		Size: 3.2 MB (3175331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c046ed68b879a54e59aaeeb121f211b6897b61417b75e1dfd18172ba964d7507`  
		Last Modified: Tue, 27 May 2025 19:52:49 GMT  
		Size: 12.8 MB (12785542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4566710f9c59a95e78db2c4687be5b50814ba41f16dd631963f681405af1da1f`  
		Last Modified: Tue, 27 May 2025 19:52:49 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed66e927b63f2cbff49863fad8d01e0742e2f1ffa4fa15a6520b4af4035aa1e`  
		Last Modified: Tue, 27 May 2025 20:11:50 GMT  
		Size: 5.8 MB (5838800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:97700b43aadf2a4f3f94cf6608b03b8990bcf823332a5e1147295c18d9ac8253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2445366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861be834f92645d3a6792edae4c1179eac98c0cf3a387898379f8f744b367a24`

```dockerfile
```

-	Layers:
	-	`sha256:ae9d643f9baa2e1ca8ab4ae483f37bdaede2a5fedcbaae9f8f6ccb19c097daf3`  
		Last Modified: Tue, 27 May 2025 20:11:50 GMT  
		Size: 2.4 MB (2436093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4a8524a0aef11e6885b4d2ca94d5eda1212876db542ae2529f1be9311bc4d4a`  
		Last Modified: Tue, 27 May 2025 20:11:50 GMT  
		Size: 9.3 KB (9273 bytes)  
		MIME: application/vnd.in-toto+json
