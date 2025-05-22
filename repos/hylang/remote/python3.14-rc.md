## `hylang:python3.14-rc`

```console
$ docker pull hylang@sha256:aba037b281b6ce6604c8728e0b3b62cf3c64cf43f827f00d7a8b23b35f945f09
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

### `hylang:python3.14-rc` - unknown; unknown

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

### `hylang:python3.14-rc` - linux; arm variant v5

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

### `hylang:python3.14-rc` - unknown; unknown

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

### `hylang:python3.14-rc` - linux; arm variant v7

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

### `hylang:python3.14-rc` - unknown; unknown

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

### `hylang:python3.14-rc` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:8cb7ba3e4d0987f1ef19753892b396626b7e568c15246f64e7c690da4b4ae88d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50056794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527323fad56962c5486a8d92e7bec5bb315b632ef626555f666fea663942e641`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 08 May 2025 22:27:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83bc4269c1ba113b740fa2e7f32e6b2e27c453db47ae90210db43a384501c8d`  
		Last Modified: Thu, 22 May 2025 05:16:34 GMT  
		Size: 3.3 MB (3333494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc248d81fa45ca5522883e02a0cf7feae006029e7d58e944685f0a7d4075c1b`  
		Last Modified: Thu, 22 May 2025 05:16:34 GMT  
		Size: 12.8 MB (12819845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036bc044491cdf63b77e51742aa5aff7e2a6dfbc621301525894252c1ee92b62`  
		Last Modified: Thu, 22 May 2025 05:16:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781f0f1cf14c047aa59df05cc29a3d81d8500cccf736a39a6a53ec04a55750f9`  
		Last Modified: Thu, 22 May 2025 12:15:38 GMT  
		Size: 5.8 MB (5837926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc` - unknown; unknown

```console
$ docker pull hylang@sha256:bf019a0e41b853ab7520efc8fcc33305f1ecfe71ce95bba570d9b9034a28a7ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2446115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e1b7c9dc63cd9f27132b49f8aba7fb03aecb6ac822e1a6021833d52085cf00`

```dockerfile
```

-	Layers:
	-	`sha256:420ec27b62703d7b23e0e82529e89dcf2c5882c2e22c9dadee11eac006864ff0`  
		Last Modified: Thu, 22 May 2025 12:15:38 GMT  
		Size: 2.4 MB (2436690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7230690846fb27c023e010214ca3baca0536a08803659075eda8be7e9223a125`  
		Last Modified: Thu, 22 May 2025 12:15:37 GMT  
		Size: 9.4 KB (9425 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc` - linux; 386

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

### `hylang:python3.14-rc` - unknown; unknown

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

### `hylang:python3.14-rc` - linux; ppc64le

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

### `hylang:python3.14-rc` - unknown; unknown

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

### `hylang:python3.14-rc` - linux; s390x

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

### `hylang:python3.14-rc` - unknown; unknown

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

### `hylang:python3.14-rc` - windows version 10.0.26100.4061; amd64

```console
$ docker pull hylang@sha256:c53f02cbbb9e5721aff8f2777c3851068b1b47a15757fcda30f1c7bd86df4f43
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3503268865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bbcf259c08c9fa6f34e5c2444b74c5960c7153a4ef8a52def66c8853d31ebe`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Wed, 14 May 2025 21:06:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:06:31 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 14 May 2025 21:06:33 GMT
ENV PYTHON_VERSION=3.14.0b1
# Wed, 14 May 2025 21:06:35 GMT
ENV PYTHON_SHA256=a878026c12b1a606d02f5bbf3ed65aa780ee8272964b8f95d8348ffa2d6ca096
# Wed, 14 May 2025 21:07:21 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Reinstalling pip to workaround a bug ...'; 	Remove-Item -Recurse C:\Python\Lib\site-packages\pip*; 	python -m ensurepip --default-pip -vvv; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 14 May 2025 21:07:24 GMT
CMD ["python"]
# Wed, 14 May 2025 22:13:03 GMT
ENV HY_VERSION=1.1.0
# Wed, 14 May 2025 22:13:04 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 14 May 2025 22:13:36 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 14 May 2025 22:13:36 GMT
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
	-	`sha256:4326fbfdaedf2ee482b8bd16fcfb5ee9ad4457108f68165a4a38b5942ab39639`  
		Last Modified: Wed, 14 May 2025 21:07:28 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3485313d0c62aaf09d3f0536e468e75096199f8de4958b59f699528016b598`  
		Last Modified: Wed, 14 May 2025 21:07:27 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c31c2a9d94028719a7b2a0d4db2d5ee38f2a6057541e80efd560a977eafe786`  
		Last Modified: Wed, 14 May 2025 21:07:27 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6861250362a010c9bcba849490ade14b2f966842fb6cd4eda81d673fd2ad1d2`  
		Last Modified: Wed, 14 May 2025 21:07:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb7508c86e97bd836dd030ab63993a79552c94f3bbfc72bf0724b1c0d5d49ab`  
		Last Modified: Wed, 14 May 2025 21:07:34 GMT  
		Size: 63.9 MB (63891967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26358008559c88011d35d23e1d9029eb3a5900e8501f79bbfeedf37847a0e881`  
		Last Modified: Wed, 14 May 2025 21:07:27 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba9355c60cf421ba27c478def5b6428a0ab4ea1a0438179add4e57959bc8f68`  
		Last Modified: Wed, 14 May 2025 22:13:41 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbafd659f3710bb7bd3fc1eb43457b4cc8264dae1dda590a17a71b630025e381`  
		Last Modified: Wed, 14 May 2025 22:13:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b64fcadf725ecabd2920e2ff404421d47421579a57773299093798ba4a98bb1`  
		Last Modified: Wed, 14 May 2025 22:13:42 GMT  
		Size: 8.6 MB (8600686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0ad2626977968832e70fd78c96e0980762415e1d04861cb8580f02cbeccacc`  
		Last Modified: Wed, 14 May 2025 22:13:41 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.14-rc` - windows version 10.0.20348.3692; amd64

```console
$ docker pull hylang@sha256:75d667ab5626d2236df4d4abe408f3485a4680ad38a6ae33fffd704f412c0616
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345887479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0fbf9fbad2da6cca1af11da11eac40c92cc009c176e0163c5c9fcf9958e8ab`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 21:11:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:11:16 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 14 May 2025 21:11:17 GMT
ENV PYTHON_VERSION=3.14.0b1
# Wed, 14 May 2025 21:11:18 GMT
ENV PYTHON_SHA256=a878026c12b1a606d02f5bbf3ed65aa780ee8272964b8f95d8348ffa2d6ca096
# Wed, 14 May 2025 21:12:05 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Reinstalling pip to workaround a bug ...'; 	Remove-Item -Recurse C:\Python\Lib\site-packages\pip*; 	python -m ensurepip --default-pip -vvv; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 14 May 2025 21:12:06 GMT
CMD ["python"]
# Wed, 14 May 2025 22:12:09 GMT
ENV HY_VERSION=1.1.0
# Wed, 14 May 2025 22:12:10 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 14 May 2025 22:12:39 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 14 May 2025 22:12:40 GMT
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
	-	`sha256:59e891cea8c7ad55e922eb2c207b3a3d400d78a85efc926b2830c5d35575ac4f`  
		Last Modified: Wed, 14 May 2025 21:12:10 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc7db674b2e4552863a4e045255b17b0715967dc4074e8176e1cb64195e37c4`  
		Last Modified: Wed, 14 May 2025 21:12:09 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d126c5fb01c9a051e7b3db6563e52fc045326c819da5eeff3e6f1d2bda6bd8d9`  
		Last Modified: Wed, 14 May 2025 21:12:09 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1d1a243b1cd00c3cb78bd8c75c7894f37edc8ea05be8c4ccea995a71621c30`  
		Last Modified: Wed, 14 May 2025 21:12:09 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7582934996ed603566d9f2f1a6a9f313c27a7434a0c1f2f3337355ab959d06`  
		Last Modified: Wed, 14 May 2025 21:12:14 GMT  
		Size: 63.8 MB (63773018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a68d826ef9b870e321dd52459c4788d0406e23803e29dbdff91b60dad54aa4`  
		Last Modified: Wed, 14 May 2025 21:12:09 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c89c1f80cd9538bb2129d87c265a25d81ae11476ddb69b41743c5d9e0daae97`  
		Last Modified: Wed, 14 May 2025 22:12:44 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12976e43a87e34edc9d0907edde25b0fddcc7de1cd914ad43684daff6f9b1ec8`  
		Last Modified: Wed, 14 May 2025 22:12:44 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c598a3033e8623bd0e23a1462fa87b3520e01c7189c8b9dbc2cffe320f54fd`  
		Last Modified: Wed, 14 May 2025 22:12:45 GMT  
		Size: 8.5 MB (8476029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd668abfb8ebea2f53c878a33ae32782dc1d9447318161377f5dec5db5293d2`  
		Last Modified: Wed, 14 May 2025 22:12:44 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.14-rc` - windows version 10.0.17763.7314; amd64

```console
$ docker pull hylang@sha256:0c99bd5d8a19a94cbeb4fbb4c7dbd9ce170c123ea0b54d58541d44ade67ea301
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2253359200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14202bb9a33ff0e6fe8a58878328fafa1f3f3d83aea586b6ad332d2051d3db22`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 20:58:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 20:58:31 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 14 May 2025 20:58:32 GMT
ENV PYTHON_VERSION=3.14.0b1
# Wed, 14 May 2025 20:58:32 GMT
ENV PYTHON_SHA256=a878026c12b1a606d02f5bbf3ed65aa780ee8272964b8f95d8348ffa2d6ca096
# Wed, 14 May 2025 20:59:23 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Reinstalling pip to workaround a bug ...'; 	Remove-Item -Recurse C:\Python\Lib\site-packages\pip*; 	python -m ensurepip --default-pip -vvv; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 14 May 2025 20:59:24 GMT
CMD ["python"]
# Wed, 14 May 2025 21:11:59 GMT
ENV HY_VERSION=1.1.0
# Wed, 14 May 2025 21:12:00 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 14 May 2025 21:12:41 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 14 May 2025 21:12:42 GMT
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
	-	`sha256:5758a99a633a6b453f305a28f132803fc1cd1a1b9b99d173d8d4469095a7a9ab`  
		Last Modified: Wed, 14 May 2025 20:59:30 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0556f1cde44ffeebea76d6442f398cf9ac7eedbff5b140ece7fb322866ec6c`  
		Last Modified: Wed, 14 May 2025 20:59:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c3d71da20dd32128de60dfaa197ff51cfbd03651a239185e45231f7004a461`  
		Last Modified: Wed, 14 May 2025 20:59:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b115367bbee830079c40a199ea35925180d63f20fde6b3895c0a635a353612`  
		Last Modified: Wed, 14 May 2025 20:59:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89eab9cd76de133416e8a94273afd5a890e77757f370ae78cc5a6363434292b`  
		Last Modified: Wed, 14 May 2025 20:59:34 GMT  
		Size: 62.5 MB (62464897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939f2ee22806dd9e626035f1ff9f62df4868b1fdfdecce6c8924afc7bdccfbed`  
		Last Modified: Wed, 14 May 2025 20:59:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7858a2c09212cc159a9d2ec8f7f5c5cf170522154f094467be99f126ae9db3bb`  
		Last Modified: Wed, 14 May 2025 21:12:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f0fef59a33ab4fc8c9d4cfd43afc9074636549db0973980e7f76dd9b08a1c3`  
		Last Modified: Wed, 14 May 2025 21:12:46 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218f98372964bc2c85ed671a2e67991619c3515f273cf2d67b95f4b897acf9c0`  
		Last Modified: Wed, 14 May 2025 21:12:47 GMT  
		Size: 7.2 MB (7166490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98140b83fbf006e91b70eb35e13c178baff1af047ca14a2a3208510343e8536b`  
		Last Modified: Wed, 14 May 2025 21:12:46 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
