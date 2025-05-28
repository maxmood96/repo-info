## `hylang:python3.14-rc`

```console
$ docker pull hylang@sha256:6618059d614ae58b67e0bc4f20a010b5643a472211b1f94cf105ccbfad2d37c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 17
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
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64
	-	windows version 10.0.17763.7314; amd64

### `hylang:python3.14-rc` - linux; amd64

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

### `hylang:python3.14-rc` - unknown; unknown

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

### `hylang:python3.14-rc` - linux; arm variant v5

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

### `hylang:python3.14-rc` - unknown; unknown

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

### `hylang:python3.14-rc` - linux; arm variant v7

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

### `hylang:python3.14-rc` - unknown; unknown

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

### `hylang:python3.14-rc` - linux; arm64 variant v8

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

### `hylang:python3.14-rc` - unknown; unknown

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

### `hylang:python3.14-rc` - linux; 386

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

### `hylang:python3.14-rc` - unknown; unknown

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

### `hylang:python3.14-rc` - linux; ppc64le

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

### `hylang:python3.14-rc` - unknown; unknown

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

### `hylang:python3.14-rc` - linux; s390x

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

### `hylang:python3.14-rc` - unknown; unknown

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

### `hylang:python3.14-rc` - windows version 10.0.26100.4061; amd64

```console
$ docker pull hylang@sha256:6bf06fb4a371a66923bd753864b523b23b5791ca9f4a8555fee9e024c49152e5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3500537300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4445586db3d3a08b995a812a07fd54f8ae01de9c8b6c22c73d19d7121eee84`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Tue, 27 May 2025 19:08:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 19:08:02 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 27 May 2025 19:08:05 GMT
ENV PYTHON_VERSION=3.14.0b2
# Tue, 27 May 2025 19:08:08 GMT
ENV PYTHON_SHA256=279b1d0e2b1b6cece6f03e49218aacccfd10367e07b785edeb1d4135507434c1
# Tue, 27 May 2025 19:08:49 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 27 May 2025 19:08:50 GMT
CMD ["python"]
# Tue, 27 May 2025 20:15:04 GMT
ENV HY_VERSION=1.1.0
# Tue, 27 May 2025 20:15:05 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 27 May 2025 20:15:40 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 27 May 2025 20:15:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Tue, 13 May 2025 21:56:34 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2eaa54494d5af27696a142815c48433664878387c27512aa22a5f5bae41225`  
		Last Modified: Tue, 27 May 2025 19:08:53 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ce19014fa410f682b36e6c1c3c1804466ba0fa303c9a484b6635f992771e9e`  
		Last Modified: Tue, 27 May 2025 19:08:52 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9e22507b0baff33137a06738f1c7bbb09b045287e7db623d4657cb8b9f9cb1`  
		Last Modified: Tue, 27 May 2025 19:08:52 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5266167b69f48a40f038142528167aea3a9ebb92cd0ea5d5dd7d598fddba4871`  
		Last Modified: Tue, 27 May 2025 19:08:52 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e8f764a1d0e6db4652e12ea237080f07a6557594321fe50b7717dcef975961`  
		Last Modified: Tue, 27 May 2025 19:08:58 GMT  
		Size: 61.1 MB (61136052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7437defd922a03b279c0e42940c94e0d019f4786d2221650300c05e088ebf3`  
		Last Modified: Tue, 27 May 2025 19:08:52 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a960057f3bbebfc8132dfb4017a67699dcdc8c4c6636be050e03f1bae0cfda84`  
		Last Modified: Tue, 27 May 2025 20:15:46 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca55282cdce779434b4aca0fa27d182952dee90da95aa6d6622f8409af6512a`  
		Last Modified: Tue, 27 May 2025 20:15:46 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2b49c7a54a44c55fdba3953afa602aad22fe7a41e0f27a26e4378782b61fe1`  
		Last Modified: Tue, 27 May 2025 20:15:47 GMT  
		Size: 8.6 MB (8624943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523c1eef34014d0979b12c3a853b1e8e7f08e51796160553e3e514dfbe0b764d`  
		Last Modified: Tue, 27 May 2025 20:15:46 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.14-rc` - windows version 10.0.20348.3692; amd64

```console
$ docker pull hylang@sha256:30ebcb9760fd8a132bbe34514f52747d70135913579d5befc259a1252fcd3884
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2343136213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d22e1bac7bf2f2f6ccdb5121078fb06d0483e9c10bfcadac3d8b828b9255a71`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 27 May 2025 19:14:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 19:14:30 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 27 May 2025 19:14:31 GMT
ENV PYTHON_VERSION=3.14.0b2
# Tue, 27 May 2025 19:14:32 GMT
ENV PYTHON_SHA256=279b1d0e2b1b6cece6f03e49218aacccfd10367e07b785edeb1d4135507434c1
# Tue, 27 May 2025 19:15:32 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 27 May 2025 19:15:33 GMT
CMD ["python"]
# Tue, 27 May 2025 20:21:21 GMT
ENV HY_VERSION=1.1.0
# Tue, 27 May 2025 20:21:22 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 27 May 2025 20:21:55 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 27 May 2025 20:21:56 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bae92a971aef15b45a0fe18763259990b4ea36ffe686528e6fd4923a8010e90`  
		Last Modified: Tue, 27 May 2025 19:15:37 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8352cb1e0e88c3078a0a72be592c7edc94e3f3253ff6ec46bcafb4ef9038ed`  
		Last Modified: Tue, 27 May 2025 19:15:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3b2ccd9d0ac90fadc17a7086116791be7b8335eb2cfad4da0e070208dd08c9`  
		Last Modified: Tue, 27 May 2025 19:15:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3feaec92c690bce384e65977ad738d1ae9b2a73577c5300a64accaf927073b24`  
		Last Modified: Tue, 27 May 2025 19:15:36 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee323e7444772ea2d2e2e1b51a5f2ccf0fca60470a8d413b72350e5f794de22`  
		Last Modified: Tue, 27 May 2025 19:15:41 GMT  
		Size: 61.0 MB (61003907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3762902937236a108e91436aeee2b73051dbe1c073e0de1f10fafcfe775221`  
		Last Modified: Tue, 27 May 2025 19:15:36 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5696d71d0e5105b494178f5947b2df0afb128d18b0507c0fad782b786ba63fdf`  
		Last Modified: Tue, 27 May 2025 20:21:59 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6285a0c454cf4a502e814793be07c869e4f358f4f0c9b0010c07265fde585789`  
		Last Modified: Tue, 27 May 2025 20:21:59 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e74ff00a98affd1ca4bacbb6530194c49914cb04be028a0ec16c97900d3c3e`  
		Last Modified: Tue, 27 May 2025 20:22:00 GMT  
		Size: 8.5 MB (8493780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759750ec5e764c7fff83668c1fce903db967cbd7e918d4c70775fe0461321cbf`  
		Last Modified: Tue, 27 May 2025 20:21:59 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.14-rc` - windows version 10.0.17763.7314; amd64

```console
$ docker pull hylang@sha256:6d13ea8eeeede5c41dbc617acb75008205cd07552f1550e7b564e1a134f049f4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2250560920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af56ae0dd5830fd047ea44f7f0f0273d47cb133f9df1e4ad9a62947226cae18`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Tue, 27 May 2025 19:09:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 19:09:44 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 27 May 2025 19:09:45 GMT
ENV PYTHON_VERSION=3.14.0b2
# Tue, 27 May 2025 19:09:46 GMT
ENV PYTHON_SHA256=279b1d0e2b1b6cece6f03e49218aacccfd10367e07b785edeb1d4135507434c1
# Tue, 27 May 2025 19:11:17 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 27 May 2025 19:11:18 GMT
CMD ["python"]
# Tue, 27 May 2025 20:12:01 GMT
ENV HY_VERSION=1.1.0
# Tue, 27 May 2025 20:12:02 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 27 May 2025 20:12:43 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 27 May 2025 20:12:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123717025a2861f93b2fdc09a61aadc82f45cec753e437286c98254cd170d3e6`  
		Last Modified: Tue, 27 May 2025 19:11:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ac9608920ce6c7af0025a05dba2264e8557e3a6769d92a6f3e15549915c2b9`  
		Last Modified: Tue, 27 May 2025 19:11:21 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2854583134be0e01193a61e90d869dde85a307ab4a16c165e783bbfe93fea517`  
		Last Modified: Tue, 27 May 2025 19:11:21 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc35f0372b67835b7f2c53c997dd1028770163f0cb152c67965301ee27a1ce4`  
		Last Modified: Tue, 27 May 2025 19:11:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d75229b4aa79bd66d604eae02f42d6da4de2395ee6b3cff7f600b08fb600815`  
		Last Modified: Tue, 27 May 2025 19:11:26 GMT  
		Size: 59.7 MB (59675215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1da02780c4ebaf9ff290be77db7d9a262ea604d2c082b27d7c830a5967e034`  
		Last Modified: Tue, 27 May 2025 19:11:21 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9625c8cee3fcf67e2e5e4f247fb08c00ace5be18d227930fb795990e4c1f76f5`  
		Last Modified: Tue, 27 May 2025 20:12:48 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76898a7eeea8e6df9bc96acc3c53c4016dae4840e3fd2fdf3452b79c1292c3f3`  
		Last Modified: Tue, 27 May 2025 20:12:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b779ce52c2d96cb61dd2089be52552b0d8c5fc06234cad5ebd962a88ac347cd`  
		Last Modified: Tue, 27 May 2025 20:12:49 GMT  
		Size: 7.2 MB (7157866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2cc55fc35ed9ddf7352f87b9a8a37b39a48f8f09d8b5a189d5c0dca1051a3d`  
		Last Modified: Tue, 27 May 2025 20:12:48 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
