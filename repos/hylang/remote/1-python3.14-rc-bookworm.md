## `hylang:1-python3.14-rc-bookworm`

```console
$ docker pull hylang@sha256:ccdb62ebb6928cfc01619a3a4723854533aa61694567df69f66f64ea9fd66499
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

### `hylang:1-python3.14-rc-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:4de88d832468009edac80fd922c26cff7a7caf9177cbf0f6613da1d2f0ceecb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50320861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0afc5488dc80d4d6cfb5cd7f910d93b7a9e6cd10c616aaf2669558501703108`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.14.0rc3
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=646dc945e49c73a141896deda12d43f3f293fd69426774c16fc43496180e8fcd
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3275165109006b48c0e5800a4a60018d6040138c99b8b439567741d7a2107856`  
		Last Modified: Tue, 30 Sep 2025 00:43:08 GMT  
		Size: 3.5 MB (3515822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eb54103ea48036002243a1abc3948987f0150886f1b949d1df6a7504f3e1b7`  
		Last Modified: Tue, 30 Sep 2025 00:43:09 GMT  
		Size: 12.8 MB (12822742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a201d2aab0f1fea805faea22fcbeaf8775bbe334a090948176529a8843af854d`  
		Last Modified: Tue, 30 Sep 2025 00:43:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5044546021b81180f6d04e0a5b502c64fa48be82b627f9fcf5376d0d2dd950`  
		Last Modified: Tue, 30 Sep 2025 03:37:04 GMT  
		Size: 5.8 MB (5753713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:fdefccb4b04b8ef81ab91b32976585c451cdcc8fd186ae883c63c7d379279159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9f665089967c3621b0c6913ec00ab49a6d07dfba3e2500369c42fab304be92`

```dockerfile
```

-	Layers:
	-	`sha256:63b198623394234233f9e4236838be614eac27ca9c9b839a48f699d11f710af7`  
		Last Modified: Wed, 01 Oct 2025 14:18:48 GMT  
		Size: 2.5 MB (2532801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c33d71a6474f20fbcd1ab36d435743500a785015c1a161eb458673dbca365854`  
		Last Modified: Wed, 01 Oct 2025 14:18:49 GMT  
		Size: 9.3 KB (9273 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:c766864c3abd784ea3e0719a41b1c298333d1f834a3ed94f854878e147ffd53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46962696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e362711d1112dd9a95ba64689d3a908bdb4d4d855e40ad176f761c52d7f813`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1759104000'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.14.0rc3
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=646dc945e49c73a141896deda12d43f3f293fd69426774c16fc43496180e8fcd
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
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
	-	`sha256:e1e8cf6a98b379fbf689c13a9736cd1289212f7d1817f7bef04f737d92c4359f`  
		Last Modified: Mon, 29 Sep 2025 23:34:08 GMT  
		Size: 25.8 MB (25757437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87383b2345e33a40a1fcda802a4be042e0a499641dc384b21ec6a7871ae9f720`  
		Last Modified: Tue, 30 Sep 2025 01:37:06 GMT  
		Size: 3.1 MB (3090730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43809bb6000e662f6cfea82d7c1f244cfd023a1604b8ae31e190be95f0b1b921`  
		Last Modified: Tue, 30 Sep 2025 01:37:06 GMT  
		Size: 12.4 MB (12360579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19f884c6184fbf64d48055cec2c2905014656311a21f2ed4be9ec3d9e3c8f1`  
		Last Modified: Tue, 30 Sep 2025 01:37:05 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1177aec2fd59efc163f28dadb64690de120418da5c4c5cd2bf6ee62261ea7d2f`  
		Last Modified: Tue, 30 Sep 2025 03:04:28 GMT  
		Size: 5.8 MB (5753702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:0d83cd7ae510f3071fbef891b2bdbac218f0bae13b1c37370634ca43211bf1c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2546031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aae8052f7c01ec41ef90551545b0ab74a89ae76fb27f6592c84858909176dbf`

```dockerfile
```

-	Layers:
	-	`sha256:52020b7a5dfabdebccc08246d3d923a986fe541fa417793b05d49686ff0293f9`  
		Last Modified: Tue, 30 Sep 2025 08:18:59 GMT  
		Size: 2.5 MB (2536645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1f8cd3db1f0902d507d207d81c308836b822debffccddd951234a01ab00559e`  
		Last Modified: Tue, 30 Sep 2025 08:19:00 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:1f3eb4a1260433dda4c985c6e185d37778f3ce5b5247c9f323d35aab39142dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44580692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ecabac6b549aa9f53f5f0c06f58c20f6bad362ee108ef5e3a33708268701f6a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1759104000'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.14.0rc3
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=646dc945e49c73a141896deda12d43f3f293fd69426774c16fc43496180e8fcd
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
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
	-	`sha256:4c0d784fb90dddd991d201014e92ef1ebfe9a20d0f2ea56e2701fb9e8219be91`  
		Last Modified: Mon, 29 Sep 2025 23:34:19 GMT  
		Size: 23.9 MB (23933930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258e762b560bc07874c8518a62469ead6da73d28f1f9c1f0138ceca967cbf6ec`  
		Last Modified: Tue, 30 Sep 2025 02:13:02 GMT  
		Size: 2.9 MB (2925429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ddf4d7e000f15d82ded2b8e3586a19786d2ca3759afe74fba31b68a952a283`  
		Last Modified: Tue, 30 Sep 2025 02:13:02 GMT  
		Size: 12.0 MB (11967356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3d211b21860b35dc537e32283c67c7a4be812aace13081a9df42dced9e19e3`  
		Last Modified: Tue, 30 Sep 2025 02:13:01 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f18b2527c0b8a184970f2bea798a240b8c22e8ae308b40f4b6a09df9e12e871`  
		Last Modified: Tue, 30 Sep 2025 03:25:05 GMT  
		Size: 5.8 MB (5753727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:cde535033239126fd39cf98ed8d1cdf02ee2ab4e07ade08b1953d56b25dd7166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2544464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cf22197f5f965779362a6b586bf61b57199debf35e6764a311374ded890ae4`

```dockerfile
```

-	Layers:
	-	`sha256:d36f5749026fea51029dd9690c776dc446c36329ad4e1c42e9ff42cb8d9bbde5`  
		Last Modified: Wed, 01 Oct 2025 20:19:57 GMT  
		Size: 2.5 MB (2535078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f65de7cab518002c42aa9ddd538aad12828ca3ae5990de542c6e48e76bb3b29d`  
		Last Modified: Wed, 01 Oct 2025 20:19:58 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:9347801731540b8f14e73017642f366a944debe28488aa1a4106904c71f62823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49925462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e2d47deaeb10fa827c272878fda0da3f6cf1d9a88199dd9025a1a8590c0d13`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.14.0rc3
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=646dc945e49c73a141896deda12d43f3f293fd69426774c16fc43496180e8fcd
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f10b6f24d26e92ee85106c0e4b6d007c50134c7270c58adf7ed0813e0f51e1f`  
		Last Modified: Tue, 30 Sep 2025 01:24:40 GMT  
		Size: 3.3 MB (3349141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca43a5ac9f0d212a782ea2b7395fb0bf98d9a038006455ef86e48c38d70616c`  
		Last Modified: Tue, 30 Sep 2025 01:24:41 GMT  
		Size: 12.7 MB (12720254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bee4cd0e190e143259599bfc77f35f444d4b8efbbde45f86a2a19c55bb12db3`  
		Last Modified: Tue, 30 Sep 2025 01:24:40 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120b2685a31d604edd1fc0c43964ca85817be7688a15450363deea3d6c4508e0`  
		Last Modified: Tue, 30 Sep 2025 01:25:11 GMT  
		Size: 5.8 MB (5753674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:591997a65a43754d5ff1a91fe38ac455847285ae3cbed7c36aa855b24e0ed29e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3192b884e0bec5209e35df6fd912ea15e3aa81dfea0bb7d439aade24d401deba`

```dockerfile
```

-	Layers:
	-	`sha256:7639da381680cca5dffa64f2d16b5b10cf827e89e0148e440c2fcf7943915b8e`  
		Last Modified: Wed, 01 Oct 2025 11:35:46 GMT  
		Size: 2.5 MB (2533114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e01591e194cb1f35d64113dfe192644df9319e1bc2fa6f01a809afefc7b007b`  
		Last Modified: Wed, 01 Oct 2025 11:35:47 GMT  
		Size: 9.4 KB (9426 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:15810b6679e577506aaaa05468f4324f335cf3659c736b93125a3d916642173b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51583716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dc66ef6087c0cf503ae5936fa493ece9ea41debaa705bba9e99ab3ef9e4b1b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.14.0rc3
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=646dc945e49c73a141896deda12d43f3f293fd69426774c16fc43496180e8fcd
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
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
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242099538ad92960c35f02b759f532a6e7f2e96d8c562612f3e07974c7d2bea5`  
		Last Modified: Tue, 30 Sep 2025 00:43:09 GMT  
		Size: 3.5 MB (3516449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f664046900473e0facadeb16faab1981f6ab6c83c93ff68ba125588d5f4cdb`  
		Last Modified: Tue, 30 Sep 2025 00:43:10 GMT  
		Size: 13.1 MB (13103695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7746c5c78e141ab137feead52560456be50ea2effec0e57ca8e2bcd5612f8bd`  
		Last Modified: Tue, 30 Sep 2025 00:43:09 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13889af669030737edf862648d23109365c5ba6a5993aed77e2ea2a40f0d520`  
		Last Modified: Tue, 30 Sep 2025 01:24:16 GMT  
		Size: 5.8 MB (5753693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:1845319d30ac77b202963a012a9e764fb2455abe1b26f475f94608c2eae6844c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2539170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09bfe844c7fdf91f71aaec5f104da0542337e1fe5339535393b939a01116f5de`

```dockerfile
```

-	Layers:
	-	`sha256:e598459b124e7a64b4e257da0d21cf549844eb723475b2f152c6f23b66ed25e7`  
		Last Modified: Tue, 30 Sep 2025 17:22:32 GMT  
		Size: 2.5 MB (2529948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:999e76b627b7d38550c4d81d13f74a49925aad2defa9b90fb7468f19209ce365`  
		Last Modified: Tue, 30 Sep 2025 17:22:33 GMT  
		Size: 9.2 KB (9222 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:ffb622e478238eaff8a9c4ccfc3a1a24c22b303e1c243925feda7f068a34f86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54933822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb144ab144781e98de8357023e1a20419db0df155d72bb5ff1adf735a980ed03`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.14.0rc3
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=646dc945e49c73a141896deda12d43f3f293fd69426774c16fc43496180e8fcd
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
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
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98051b86cb01ab84c2bcd5593eee62dfe7ba883a17c247dcee3e63d9077b3db5`  
		Last Modified: Tue, 30 Sep 2025 04:16:08 GMT  
		Size: 3.7 MB (3721192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3b5ad45c20aedceb2410e46b4a6294da2b2d2e1beb2af4e916e706761140ed`  
		Last Modified: Tue, 30 Sep 2025 04:16:09 GMT  
		Size: 13.4 MB (13389763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52d1ae87b0ac49f3a95518224e715d71b6f019c43f72e4531aa3eaa29cd653b`  
		Last Modified: Tue, 30 Sep 2025 04:16:07 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6b84d297dd0671f75d4016a4aaba3bad58304c551a541b623ca0763e0ba8a1`  
		Last Modified: Tue, 30 Sep 2025 17:59:35 GMT  
		Size: 5.8 MB (5753922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:84bb8f5fd059857635670e116f0d0cd809c49aed07c84f10113e590d43b9fe76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2546605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c20baf3617099ecc26316135d65fef61213b3b5a2988ff65f3ef42352f148a`

```dockerfile
```

-	Layers:
	-	`sha256:60124b9272b932083b7ec91433c73fc96f6d1d30912db4411fa2d5e0b2e2b439`  
		Last Modified: Wed, 01 Oct 2025 20:20:08 GMT  
		Size: 2.5 MB (2537263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bd83403f289cd4784d2c93b177de9f0777abf2610097876e8ffbf7dd9a579bb`  
		Last Modified: Wed, 01 Oct 2025 20:20:09 GMT  
		Size: 9.3 KB (9342 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:7140b96943dea080e60d9007bcb30f58dc5d2a852fdca49ade64a6086be5cac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48480208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa7af22142e93089055541eb5d582a998d6c5d2cc2122757b1259eff51216a8`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.14.0rc3
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=646dc945e49c73a141896deda12d43f3f293fd69426774c16fc43496180e8fcd
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
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
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e431848a5c5e5b5f0214221268a9899677e80eaa32509991e1e5e6be59ed6dad`  
		Last Modified: Tue, 30 Sep 2025 04:36:08 GMT  
		Size: 3.2 MB (3181729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a1ab6beb7e07476e6621a7742445a1c4a95a85ca4ddae53b2ef1203b8e43fe`  
		Last Modified: Tue, 30 Sep 2025 04:36:10 GMT  
		Size: 12.7 MB (12660146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e49434eff5cc97919004ebff93a8c4e9d643d804035ac6120e892144c639e6`  
		Last Modified: Tue, 30 Sep 2025 04:36:09 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e65738cd740dea0803f13ec050058a2dab6cd46fd794537aa14924605d9d4c`  
		Last Modified: Tue, 30 Sep 2025 14:41:31 GMT  
		Size: 5.8 MB (5753764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:a95d1ca3cb5c52363464ae65d085fc7f73d78a7a1fb549a763885775a0bd70b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a7ecf12eac0df339f94d69ef5e793cd4e1c658bb889f17ae8449104de83b0d`

```dockerfile
```

-	Layers:
	-	`sha256:b4a5630db0b215f02359ddcf082cb155c163c4011dc69c8d08705820941a111b`  
		Last Modified: Wed, 01 Oct 2025 20:20:13 GMT  
		Size: 2.5 MB (2529625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:403cb238f00f0170785cd1a6ee82d33b19278b9b081e1ec099425019dc736876`  
		Last Modified: Wed, 01 Oct 2025 20:20:14 GMT  
		Size: 9.3 KB (9274 bytes)  
		MIME: application/vnd.in-toto+json
