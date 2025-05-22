## `hylang:python3.14-rc-bookworm`

```console
$ docker pull hylang@sha256:46eb0d9d02809a07d0c64843cbdad08e36d13d677ffdc4e815f97ed2d6e90a63
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
$ docker pull hylang@sha256:4e1f362d3234297ef7c9bf8743cff309e8a0eb854c5cdfd3dad229b71f54c4d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50504874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82e0559551f327c3e0ae0d7885c04b48c22761e4ac2a8c29bbf53bb8c885427`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 08 May 2025 22:27:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.14.0b1
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=2ddd30a77c9f62e065ce648664a254b9b0c011bcdaa8c1c2787087e644cbeb39
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
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
	-	`sha256:635977a8a2bae7b5fc90b6a1ef0c95da83e61f9438bd2743d4a4aabf16a2c02e`  
		Last Modified: Wed, 21 May 2025 23:39:02 GMT  
		Size: 3.5 MB (3511815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306c47f5cf2e8c92cf1dea909a6862f0b4d48e619b34b17be4e76801d30e2f97`  
		Last Modified: Wed, 21 May 2025 23:39:02 GMT  
		Size: 12.9 MB (12929696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79b07fa8a740db09c874083f1ebed8cda0cff2d9a5a1e6c407c96154661a7e8`  
		Last Modified: Wed, 21 May 2025 23:39:01 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0aa832ab64a082e5f6bdd91c2aea427809adf7d2bd1036212ff9eae35ee356`  
		Last Modified: Thu, 22 May 2025 00:13:18 GMT  
		Size: 5.8 MB (5837783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:8a4c6b3473c7357608f46911856038e62fbf9b544fefeec24da48e1c0723bdc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2445650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404c8a5f1742bb25feeb0d8a7d40f021ac97e83c79d5f0ff8cdfd6802cf0b0c9`

```dockerfile
```

-	Layers:
	-	`sha256:b741113e98f56568ca2d07d545bcbdda6591e4c59a5078c9097d611619742f1e`  
		Last Modified: Thu, 22 May 2025 00:13:18 GMT  
		Size: 2.4 MB (2436377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11a93bbe1b2617a53bf2cbb859a466f07745fd3a0f73769719ac4c3c827f607e`  
		Last Modified: Thu, 22 May 2025 00:13:17 GMT  
		Size: 9.3 KB (9273 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:9b6e9053e58fc0aa4fae63c7e5fe7c9a17def2c917bcb591c593bf9833e9dfba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47147873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702f8c576f4dd4306457a637b80c5f4b082947534b1f162f8a94b0fadf7ea206`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 08 May 2025 22:27:23 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.14.0b1
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=2ddd30a77c9f62e065ce648664a254b9b0c011bcdaa8c1c2787087e644cbeb39
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
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
	-	`sha256:1a1bccaba7a687b9f21342343f4b7ea4a597f2a211ae6db7de772cf0df8f6127`  
		Last Modified: Thu, 22 May 2025 02:40:14 GMT  
		Size: 12.5 MB (12467653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1ff8950dcf593548ddb6d6c16b6f6f12663ea2974aff27e5f453a56604ca15`  
		Last Modified: Thu, 22 May 2025 02:40:13 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6a8a3fba459a8a2cbc9a6b07361bf330e4bacd2d6e8edf6f61b44acd24cd6c`  
		Last Modified: Thu, 22 May 2025 06:27:25 GMT  
		Size: 5.8 MB (5837940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:400bfcc24c1bebd7288b24600a85c4413789a99e3eff083e62a58eb1d9d925f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2449602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d00463d9f0c0cecd423ec06153b4766115a3ce48833ea9ad21dd24c5a43b7b`

```dockerfile
```

-	Layers:
	-	`sha256:5e3dbd87dd0eb1614d1700c8cd9b2df80a73967ed2469ec3deaf1f6f56a9e35d`  
		Last Modified: Thu, 22 May 2025 06:27:24 GMT  
		Size: 2.4 MB (2440221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae283aed4309ea04879b8e3c99e8d9575c02db937a61286cb82142b94f98ae78`  
		Last Modified: Thu, 22 May 2025 06:27:24 GMT  
		Size: 9.4 KB (9381 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:c3e5d93c1ed76d521f49404b8eb7940a51fc26da3d3c19b5c2708efe3b11ff89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44762794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1ee8fedd68fe21dd90fcd24783de211226911d4f6af185c038dbad8ad95a35`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.14.0b1
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=2ddd30a77c9f62e065ce648664a254b9b0c011bcdaa8c1c2787087e644cbeb39
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a168ab6ef055ca3f234935fd6c1b1e230b4a5c9af36834c70ba6ccb2e6aa9935`  
		Last Modified: Tue, 29 Apr 2025 06:15:55 GMT  
		Size: 2.9 MB (2914845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a690f08a4d4d6b4a416980e8882d6335f708782891c0b35c38e76ce2a98075`  
		Last Modified: Sat, 10 May 2025 00:53:07 GMT  
		Size: 12.1 MB (12072770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1aa7d5aec9933816b14ce0d6df6c6da2a6c6fa571a59edc2b748a35d7de3fe`  
		Last Modified: Sat, 10 May 2025 00:53:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256e8fd15adcee067d5c2a307ef46a5ccc2e5cd41ef74ef2f846971ea9eb13d3`  
		Last Modified: Sat, 10 May 2025 07:49:05 GMT  
		Size: 5.8 MB (5836856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:4e96d28035c237acdb7bf32965026495e143fc3048c7d2f0228f59a857070fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680a7a8b9da177f499620803cce855b0958f13501785f71a6a37127b98c94f38`

```dockerfile
```

-	Layers:
	-	`sha256:4bc03f240962c8b605eda16bc18060005e8c35d0d535355162f6e92a1c9ffa63`  
		Last Modified: Sat, 10 May 2025 07:49:05 GMT  
		Size: 2.4 MB (2420156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:580ca37e09743b4d89d381f6fde45993d2d7f42bbb2c43cbf44962613e1f4cb2`  
		Last Modified: Sat, 10 May 2025 07:49:05 GMT  
		Size: 9.4 KB (9381 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:548fefdd71d9f06b1ca606120b2d6124e0f02277a058f6f7fcc6aa5a0e2f6c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50037184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:464db90b4571c20a2b87e1f3ce111c8b03d5a97f1d20d0b38d01a7d5ecfefb13`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.14.0b1
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=2ddd30a77c9f62e065ce648664a254b9b0c011bcdaa8c1c2787087e644cbeb39
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cbf253efde557c5344b6b66ea9fcfb70a6f4bf8d619a1a73634aec15d97afc`  
		Last Modified: Tue, 29 Apr 2025 22:10:47 GMT  
		Size: 3.3 MB (3332086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fba775b6b3aa1b5200f17024c9af08dc67fd91f9239a9b63967d636274b7776`  
		Last Modified: Sat, 10 May 2025 00:07:03 GMT  
		Size: 12.8 MB (12801590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6714e8da574a3cff2c51009a79f24737a93604254ed7a4a602c5cf27f88aef`  
		Last Modified: Sat, 10 May 2025 00:07:02 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0474cdd1d40f41289ff5c1234b783c8252f946f710ec271e391deaf859ba2f2`  
		Last Modified: Sat, 10 May 2025 04:54:10 GMT  
		Size: 5.8 MB (5836636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:5626bdb35179cdf3cf386a3cfb7c8ea3e58da2e90c64b6a18abfc015c8575404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2427617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da07e1892934250293d500dc5d660744ec8d8ea9533fc8398a2a17b06e0738ac`

```dockerfile
```

-	Layers:
	-	`sha256:4fd7a6c6c6fb9313c707ea78ab3116a7e6d83d489dd4a314a1148d49f82f9e5b`  
		Last Modified: Sat, 10 May 2025 04:54:09 GMT  
		Size: 2.4 MB (2418192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91694c5a69bd33e806b5527f64076d0fccf83260dfeff6ef2ce54864e7eecc9c`  
		Last Modified: Sat, 10 May 2025 04:54:09 GMT  
		Size: 9.4 KB (9425 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:ad2ece14fc8d8c7b808d166381e8f5fb8b3b105766e0facdecde5efc894c7058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51756459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a28b7ef823a0a7f4c813a21773769e37adb35898dce8791938b76e34fb2b07`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 08 May 2025 22:27:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.14.0b1
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=2ddd30a77c9f62e065ce648664a254b9b0c011bcdaa8c1c2787087e644cbeb39
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
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
	-	`sha256:ccc34a38bd333d8ed470376b9c8750a4e363cf7a9675df1057ce3a13dfdb98dc`  
		Last Modified: Wed, 21 May 2025 23:39:55 GMT  
		Size: 3.5 MB (3511131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c403adbdd3d4da0e802b9c7d1982623e4b51c24ce752ee0fa783d850bb75709`  
		Last Modified: Wed, 21 May 2025 23:39:55 GMT  
		Size: 13.2 MB (13199786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f695af6e7aa67d5dcc0aa074a980d819d9a4d9d860a4d95df3fc424e8bb0b579`  
		Last Modified: Wed, 21 May 2025 23:39:55 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d6f054c4add49379776f50d44bea340c2138a257fe76b1e58ba22b1cea603b`  
		Last Modified: Thu, 22 May 2025 00:12:32 GMT  
		Size: 5.8 MB (5837806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:99506c25c35649e604a7fc11d7a4e96952289818a29c75f6e9b25e89eb5a93fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2442745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9ddcf6c6492670aea781675c767b15a1719dd8dd411482ed609a62d339cb2f`

```dockerfile
```

-	Layers:
	-	`sha256:93dd93f107dba14922c560c0aa8fe0b443d63a537b34f89974d8716dd9da4bb8`  
		Last Modified: Thu, 22 May 2025 00:12:32 GMT  
		Size: 2.4 MB (2433524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceecc2189f25bad61e5080860fe9fcc8a3a499e042deb1c460ef2cd50b89773b`  
		Last Modified: Thu, 22 May 2025 00:12:31 GMT  
		Size: 9.2 KB (9221 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:ee47943c65d47b9e25def28ee17c04ed2daf97a619306e8949d30b653a0822dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55108021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f44789e4d4942f5ec3aed1f39c0fc4b3b568ccc14a093e04c1b8773c199d14`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.14.0b1
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=2ddd30a77c9f62e065ce648664a254b9b0c011bcdaa8c1c2787087e644cbeb39
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
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
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2e8b43d1f65f6e9b34d109b97cf9b76288ecc9297cdfd5289eefc8e1d17c20`  
		Last Modified: Thu, 08 May 2025 21:39:34 GMT  
		Size: 3.7 MB (3713699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cadc06f1ec3c73c06928bd30fe022b6229510e4d5643f87a0cd36a8c8eb6969`  
		Last Modified: Sat, 10 May 2025 00:17:35 GMT  
		Size: 13.5 MB (13488847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1587eddbafa0ed6a0857c5838df5e42bbe1dfc31a936d354e084471f88af94bc`  
		Last Modified: Sat, 10 May 2025 00:17:34 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce546904b184b3d09d76d0194ddfa129abaf933667a5e73fedb5648568277883`  
		Last Modified: Sat, 10 May 2025 03:44:17 GMT  
		Size: 5.8 MB (5836783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:5588088cab665639b072e54c9623ba3593b77e07c331f49d8b5bf2b98a0dab59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2431582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a871f8d50ee99f232192d8828086c12ab34597e969067a1ecbac4e336cf118e3`

```dockerfile
```

-	Layers:
	-	`sha256:c64d98a8a9dd33eaead3e014470a7e139853e31436d6000e253a572c033081d6`  
		Last Modified: Sat, 10 May 2025 03:44:17 GMT  
		Size: 2.4 MB (2422241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b12863aaebeb3b0c562e2ec2b2f8f68dc3a2c83b50399c45da87fd4df23d8b`  
		Last Modified: Sat, 10 May 2025 03:44:16 GMT  
		Size: 9.3 KB (9341 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:db2e90fbccdaf42b555256f806a206471120f4c1f6a43d650de55fa333d67274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48659753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391bb0b9165f4a621dde49a3730ab393c19f184d0f23d58bb1242dc434abe0fe`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 08 May 2025 22:27:23 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.14.0b1
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=2ddd30a77c9f62e065ce648664a254b9b0c011bcdaa8c1c2787087e644cbeb39
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
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
	-	`sha256:2b66a14ae5b8ebe7b31c6e56648cbf0dbac714b31d0bbcb216672a02724f08c1`  
		Last Modified: Thu, 22 May 2025 02:33:10 GMT  
		Size: 12.8 MB (12763512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59b936a78999dd449a78d7f417950acaa2702c3660d9f7575ff0d62e2049503`  
		Last Modified: Thu, 22 May 2025 02:33:09 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e7f84ee4b7d4c2599159da7f6fed537296c63ab71265359a95e5206a2ea717`  
		Last Modified: Thu, 22 May 2025 06:26:48 GMT  
		Size: 5.8 MB (5837852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:64683c5976514d464197434401c4682149087712e0b8227209a0abcf5d1e66bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2445366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c6cdc5736301adb2336e1f1b0f7a98e5720d9e3d09fac19aaefc81d8b92f27`

```dockerfile
```

-	Layers:
	-	`sha256:f4dc12e3af11910271f85ee04df3b4302cb9e938456f01006b07eb4c1e71bbe1`  
		Last Modified: Thu, 22 May 2025 06:26:48 GMT  
		Size: 2.4 MB (2436093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a958c7e6b1d69840d8e10030660a4e1b1f6a3ac366180a57c89e7ee2b0edf393`  
		Last Modified: Thu, 22 May 2025 06:26:48 GMT  
		Size: 9.3 KB (9273 bytes)  
		MIME: application/vnd.in-toto+json
