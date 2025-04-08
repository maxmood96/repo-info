## `hylang:python3.13`

```console
$ docker pull hylang@sha256:29172bf45f19e597245186bbc3a71197fac6d9f0e944f43cf3abd3f0f43a6aee
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
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `hylang:python3.13` - linux; amd64

```console
$ docker pull hylang@sha256:b4a8b724f6f39c9683b941ffd4bc519f777b94ba8033b321728fb0e432a9e32b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50031740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca378ad6c80051c1f150714c214ddda30c926fb785539008f523d44f79982571`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 23:51:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_VERSION=3.13.2
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c672e0471fb7888ec4a8553101b8d9f2af1a01f7cf174c09e22e1a9b3e2db70`  
		Last Modified: Tue, 08 Apr 2025 01:44:51 GMT  
		Size: 3.5 MB (3511473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1860f6e4e054049511f7661734ef07393e3dcc9c60b148aa1a060c6eff99718`  
		Last Modified: Tue, 08 Apr 2025 01:44:51 GMT  
		Size: 12.6 MB (12583449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b226e61ce4a02d9f6209995017c25196fff5f803f32d6d8c12ac8a7212a46b5`  
		Last Modified: Tue, 08 Apr 2025 01:44:50 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165ca6af08def0d433fd4bb98842d615c0706a3ba7da1ff7ff9e6dd41e048d87`  
		Last Modified: Tue, 08 Apr 2025 02:22:14 GMT  
		Size: 5.7 MB (5709309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:e7ad5bb4944167699b60492e30f3d69a00583f6031302467c5604e6e3cf8ef80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2431900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58456c9d660680125b21eaefe4eb4befbd9fcffdc4df43ffa7b5d54b849c409`

```dockerfile
```

-	Layers:
	-	`sha256:6b3a282a48fa2d38535f8252f006e6ee81e636b9bca09b871593e0b5aeb28ed9`  
		Last Modified: Tue, 08 Apr 2025 02:22:14 GMT  
		Size: 2.4 MB (2420233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e6c12749b41f3c13f0e61f26f4480a6fca57beb0830f4a385d8e0bfb699c678`  
		Last Modified: Tue, 08 Apr 2025 02:22:13 GMT  
		Size: 11.7 KB (11667 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; arm variant v5

```console
$ docker pull hylang@sha256:8b962330c338200670b4af28f2aa5395965b053215d7cc87c216ddd1b6b2b1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46647810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a77a6a127098e6c35a47c812ee39edf2fee61b641af4b5c56cf8f2c3341f98`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 23:51:20 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_VERSION=3.13.2
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:87c352465466fcf04c9686fee29c2541af5fc39172801545bb24d9faa8cdeabb`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 25.7 MB (25735853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4776ee79e4c5b67eff9510b879c6b04f59a0dc171d3e9d3d46c8499a8ec1587`  
		Last Modified: Tue, 18 Mar 2025 02:45:54 GMT  
		Size: 3.1 MB (3082374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea143dc01b5cf19274f7c0ec6da2665030fd210321ea21de0f2864d89b186fab`  
		Last Modified: Tue, 18 Mar 2025 02:45:55 GMT  
		Size: 12.1 MB (12121822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48c6440a71f68151cf74d6dc1eda50dd139d61437694cd641160f2e698a4234`  
		Last Modified: Tue, 18 Mar 2025 02:45:54 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5499ee344f581d81eba3a7918abc97f46bce63d9a0bc36004fa652d7e18d4c27`  
		Last Modified: Wed, 19 Mar 2025 23:05:42 GMT  
		Size: 5.7 MB (5707511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:54a784ff7f3b5c28b2dfbedd57b53de34d617f89bf2ab409a95ae12ca9956cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2434334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a831b54c904f94ed2bb05138daa0666425542a540b53144a847734fd058f6e0`

```dockerfile
```

-	Layers:
	-	`sha256:2cf61e21decc1e6e6d4c3085c8f5ac6a1095cddc9fc50b31491fce818fc86054`  
		Last Modified: Wed, 19 Mar 2025 23:05:41 GMT  
		Size: 2.4 MB (2422497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:563bfccaa5e2c8e4f0325b1c99c3c5fa6ae16de90dac55ed3ff5a6204f2d306f`  
		Last Modified: Wed, 19 Mar 2025 23:05:41 GMT  
		Size: 11.8 KB (11837 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; arm variant v7

```console
$ docker pull hylang@sha256:735ed9ffdece08b451ef8e5c3940569697e4e7ed3eb0d0b25bb40e1296b1aba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44289734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16afaad0125c318a2573214c3ec98f978d66eee086e438d06eb598539003013d`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 23:51:20 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_VERSION=3.13.2
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feeb271cab05b82bd07a633e707a26fff380aee02822791ebf2041b13a2db673`  
		Last Modified: Tue, 18 Mar 2025 01:13:20 GMT  
		Size: 2.9 MB (2914835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc451f36793e24754a65ee49b000c5aa1a95ba26148e8ca8637050a76f99d99d`  
		Last Modified: Tue, 18 Mar 2025 04:07:02 GMT  
		Size: 11.8 MB (11752079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e63c55c4aa74bef44074aba10eb99424069cd0bd0d5f5efe1dc662aefdd4fc`  
		Last Modified: Tue, 18 Mar 2025 04:07:02 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cbc2bd3a92c5f7e07e080bd7d3e397537b1eefe5721aa5216d6df16c415f88`  
		Last Modified: Wed, 19 Mar 2025 23:27:20 GMT  
		Size: 5.7 MB (5707483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:fe8a3f820e31c493827f2aa84d11d7e89a452830c8e37a7524b77d69663fd54d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2433076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a98110894628bccf59619910d213748f67496b7e6a490431870d3d476ed7ae`

```dockerfile
```

-	Layers:
	-	`sha256:414bbaf364756b33e2587b857242eaba8e7b100cdbbde6a3389abfd2428eed12`  
		Last Modified: Wed, 19 Mar 2025 23:27:20 GMT  
		Size: 2.4 MB (2421238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd0bbf891deab84f89e286df5381cc8404c3f76ace735aabd3d660bafa412363`  
		Last Modified: Wed, 19 Mar 2025 23:27:19 GMT  
		Size: 11.8 KB (11838 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:e05fd0fccd7b66730361c089ff9265c08b53db0b0b8da08aa187d67044ce3b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49559427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf64a6765e797cceec795ac7573eb1a7d259380823e74cb8a77432a81efed37`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 23:51:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_VERSION=3.13.2
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06dd23feb933b4a7c0748580688f06eeef7dbb9a738bd9f6c4616d26c19100b5`  
		Last Modified: Tue, 18 Mar 2025 01:53:35 GMT  
		Size: 3.3 MB (3332058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e9c4181a6224544c3fc6280fae7938a556c21f77b0a242dfe7a2f5b2bad323`  
		Last Modified: Tue, 18 Mar 2025 01:53:35 GMT  
		Size: 12.5 MB (12475664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d92553a84fd4f4cf9c188e393425c6653cfe5c00f593bc6ebbcca9bf1dc7f30`  
		Last Modified: Tue, 18 Mar 2025 01:53:34 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba00492517ab2fe5f6dbc7bb61e95b3c013d3be79abf6c07b13844fc509ee77`  
		Last Modified: Wed, 19 Mar 2025 23:15:03 GMT  
		Size: 5.7 MB (5707419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:40b0939a76a90e9d89dbce771785b8c606dfbc1a74895c3273e518ed250c37ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2431221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:158be1b2d55a2a3dffe1383685f3877a2a9e2431e7e5f239652b1acbb832922b`

```dockerfile
```

-	Layers:
	-	`sha256:54d0ad1866487f53474149dda0b999adde0cf9a441640d78aceaec0c8b1512fe`  
		Last Modified: Wed, 19 Mar 2025 23:15:03 GMT  
		Size: 2.4 MB (2419306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:841fd762bfb385751cc159bcc7134674c2ffa85fd1e79d4b94523f3048608583`  
		Last Modified: Wed, 19 Mar 2025 23:15:02 GMT  
		Size: 11.9 KB (11915 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; 386

```console
$ docker pull hylang@sha256:87ebda21287676b425299dd7d5bcdcdcef83548462a004fa5dec3b658b590c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51232925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11b79f276dca4310fa6a1c3b457dc1d533650e6ad95241613528f8687b1e87c`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 23:51:20 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_VERSION=3.13.2
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7718fd1c9dbad1b48011b6db22ecc5811efe5f8ef624b2fd706fbefac83bc8a2`  
		Last Modified: Mon, 17 Mar 2025 23:44:34 GMT  
		Size: 3.5 MB (3509835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca9c5583b3c0c4824971828592506cc9dda60e49e3b79081d2917b0fc1e8c0b`  
		Last Modified: Mon, 17 Mar 2025 23:44:34 GMT  
		Size: 12.8 MB (12825951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b110c0ea63f0bfb1fd162c4bb7673c34cec69aa99c356a4af14de9517d95d812`  
		Last Modified: Mon, 17 Mar 2025 23:44:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc9476aee0b8734fa1abd9e0abd163b7035a12ef5b1ed8549119735b420acea`  
		Last Modified: Wed, 19 Mar 2025 22:58:43 GMT  
		Size: 5.7 MB (5707362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:8eda5fe32b31c4506710264229562dbca0296b419eec747f08cddc356f429bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2427535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a72dec31282110abcd8e400d488b4fbccb81d47769bc38685bc46b4aa7b35d`

```dockerfile
```

-	Layers:
	-	`sha256:278d89ac345510c8c9040e683fdad11b506245a67b97cff3b622dac20277f2f1`  
		Last Modified: Wed, 19 Mar 2025 22:58:43 GMT  
		Size: 2.4 MB (2415960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cecd33304fe975a9c94942f684e92352b38cc727c9f2cf4c604cdada14d14cb3`  
		Last Modified: Wed, 19 Mar 2025 22:58:43 GMT  
		Size: 11.6 KB (11575 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; ppc64le

```console
$ docker pull hylang@sha256:6bfbeb5b0e64f71b8be17f00af79bccc374208381d41fe1cd1547398fc32f491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54598265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad016209e94ac7fc5f0349755115b854bf1052fe9d974b69ac0bba1f6d02040`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 23:51:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_VERSION=3.13.2
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0212cead740079c3cc006fe80cf0918161060c9edbd6c71c175589fa385ad255`  
		Last Modified: Tue, 18 Mar 2025 01:53:51 GMT  
		Size: 3.7 MB (3713731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc54d7d62bbf2d491ea8a3e202c164a4de85c869aa378e5eb70d461356d379b`  
		Last Modified: Tue, 18 Mar 2025 01:53:51 GMT  
		Size: 13.1 MB (13128997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a171ad67212c49b0a24b73e0fc8593c7fcbeb8cf8694881d036c42e85c9eabd9`  
		Last Modified: Tue, 18 Mar 2025 01:53:50 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f86a1b923ebd989fa627729f87905858e6330929b5212626f84dd4b46eec22`  
		Last Modified: Wed, 19 Mar 2025 23:21:05 GMT  
		Size: 5.7 MB (5707473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:0a3654143dcf4cc573a1cb18e8b5e4ad9cbaca2542a7bb8cbd5b2683c122f188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2435090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66c3db0d057ad0bcb287b87b63089b2d77b6f5ec85df41c0f8e0fad59d63414`

```dockerfile
```

-	Layers:
	-	`sha256:418db1d3d16ad72f1794768bef0ade5f306b2212bef85140ccc9ae0895e559d3`  
		Last Modified: Wed, 19 Mar 2025 23:21:05 GMT  
		Size: 2.4 MB (2423307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:052d2e23ddb5dcdb6f2112f77d7998d77339536ce806355884bb33c2237b14a5`  
		Last Modified: Wed, 19 Mar 2025 23:21:05 GMT  
		Size: 11.8 KB (11783 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; s390x

```console
$ docker pull hylang@sha256:7d3f52ecbebe127bf47f78120967192559d3069bb65cad388d98ea6fd3612c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48169557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1088186d3e6ff7f312f2d961bd9ff3163f844e5f89cc5bcaa88b148823897e`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 23:51:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_VERSION=3.13.2
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a43eca806cf2681241a791cd5946764133eeefada81d25a41e5a3a530455eec`  
		Last Modified: Tue, 18 Mar 2025 01:00:14 GMT  
		Size: 3.2 MB (3173186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2a69037752363453b3de1a06aef7a4b009679f39b05ff410b1857a7c9e09be`  
		Last Modified: Tue, 18 Mar 2025 01:00:15 GMT  
		Size: 12.4 MB (12427513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1afc9cc199ac2fdb6945594f951dd8cd1784c3d688136709f6003d034451262`  
		Last Modified: Tue, 18 Mar 2025 01:00:14 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1849c5787e97b8b4b46419fcc83b6454897f04523eccd432a0c0b33ada2d1b37`  
		Last Modified: Wed, 19 Mar 2025 23:43:52 GMT  
		Size: 5.7 MB (5707550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:70317bc6319ac0ba4c503888fa2fcdb7143528eff1bf6dfbb4b7d442180ffc38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2430280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33cf91a37c2fdf4a2e97b07ba375b2a689652318757bb1ccf0fcdd19286b49ca`

```dockerfile
```

-	Layers:
	-	`sha256:671b28cbd8bb50ce56d4361b5bb7016b886c4594b976e32d72ec91cf45c423ff`  
		Last Modified: Wed, 19 Mar 2025 23:43:52 GMT  
		Size: 2.4 MB (2418613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a902dd90ac511290ab64195d4c516bf620b71cc556d896a6e5c762e5e8701194`  
		Last Modified: Wed, 19 Mar 2025 23:43:52 GMT  
		Size: 11.7 KB (11667 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - windows version 10.0.26100.3476; amd64

```console
$ docker pull hylang@sha256:a83d8e93c8dad822102bb37f52d670ae0ba6540b08315f465ec23a05074ef6f1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2976540505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5015d99bcd13304f9fa6ee6bc5a195305f61d7ebaa6660a708bab1c9c7ada982`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:48:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:48:07 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 12 Mar 2025 18:48:07 GMT
ENV PYTHON_VERSION=3.13.2
# Wed, 12 Mar 2025 18:48:08 GMT
ENV PYTHON_SHA256=9aaa1075d0bd3e8abd0623d2d05de692ff00780579e1b232f259028bac19bb51
# Wed, 12 Mar 2025 18:48:45 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:48:46 GMT
CMD ["python"]
# Wed, 19 Mar 2025 23:03:26 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 23:03:27 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 23:04:03 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 19 Mar 2025 23:04:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db05ebafac5b0fb7dfa4ed97cc8b2683be4b287bba5e884a0a5e1e13057cfe7`  
		Last Modified: Wed, 12 Mar 2025 18:48:49 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cd8e49651a452d31e3a3a7a7f4def3fdcb2c7e50b25a4b73fff3fc5cbfeac0`  
		Last Modified: Wed, 12 Mar 2025 18:48:48 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb0a44871b4a0b85a7d8842de002af943c755e89a56a55e938cb82f1bb27b3a`  
		Last Modified: Wed, 12 Mar 2025 18:48:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debf2ff1ef0c7393113b5fc5d7c95015e4488ea283411bb029236334bbceacc2`  
		Last Modified: Wed, 12 Mar 2025 18:48:48 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097f71ff76ec962ef08c9a66553840cf263f1263f2764877bfa28038280c63c2`  
		Last Modified: Wed, 12 Mar 2025 18:48:53 GMT  
		Size: 59.2 MB (59215131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc46af2be7643fc9d0674f87668a6ac672b920e08ec9e61ef2066c25469151f`  
		Last Modified: Wed, 12 Mar 2025 18:48:48 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415a8bd81c939f915a9a65e6db198701cdd850ebb92e221087ab29d2694c146d`  
		Last Modified: Wed, 19 Mar 2025 23:04:07 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3696a62814ee854c257fb2a8e03a7d0aba1877847234e135f445fd029388822a`  
		Last Modified: Wed, 19 Mar 2025 23:04:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602037106b78aaa16512367aa9e782d1d9d3fc859b140a36744724f4af687d82`  
		Last Modified: Wed, 19 Mar 2025 23:04:08 GMT  
		Size: 8.7 MB (8667231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20e012a60b82c021a0517ea3e61a5f04dde98c5bf06cdfe918b388ca3d16dc4`  
		Last Modified: Wed, 19 Mar 2025 23:04:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.13` - windows version 10.0.20348.3328; amd64

```console
$ docker pull hylang@sha256:cdc24631e1cf34a9c272b8415255e832d967c1b013e9f882982965ff52313071
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2337547811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4fbd21f1e7fbe6a9738947312b00136380c0b526ffd261eb611d74bb1e4e76`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 19:05:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 19:05:36 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 12 Mar 2025 19:05:37 GMT
ENV PYTHON_VERSION=3.13.2
# Wed, 12 Mar 2025 19:05:38 GMT
ENV PYTHON_SHA256=9aaa1075d0bd3e8abd0623d2d05de692ff00780579e1b232f259028bac19bb51
# Wed, 12 Mar 2025 19:06:29 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:06:30 GMT
CMD ["python"]
# Wed, 19 Mar 2025 23:12:08 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 23:12:09 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 23:12:48 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 19 Mar 2025 23:12:49 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d117d2b306c4a9efdb192b47ef35e094ff26524560ebe6f1c4667dc24b6b278`  
		Last Modified: Wed, 12 Mar 2025 19:06:33 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408c0dbfe38dcc275928577ba52d0522b23c588a52f2ae02bfe2914f3737f39d`  
		Last Modified: Wed, 12 Mar 2025 19:06:32 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c105133d2d861d6b62ea70a342d2eca0334a3ce26112ba2429da2c4eb9444e9`  
		Last Modified: Wed, 12 Mar 2025 19:06:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9b6bdc718a5d7c67dc2bb33d7f33f0362571e96b00e5cd2ca7f193e55a3662`  
		Last Modified: Wed, 12 Mar 2025 19:06:32 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc95cf06368369047c38e863ce6592935e4414f77332c3afdb3eb5b804dd2b7`  
		Last Modified: Wed, 12 Mar 2025 19:06:37 GMT  
		Size: 59.1 MB (59082607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eda5f8cbc2aaa97fada4d17ebba41695d121212cc7ab220cceabc5fcb9cc9a8`  
		Last Modified: Wed, 12 Mar 2025 19:06:32 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a60379f2ea62870363b56a3ff176311ed71e96748dbc2b4ed6e208add8e960`  
		Last Modified: Wed, 19 Mar 2025 23:12:52 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673a8f6fd664cff3c18c11d3c1fda08dbdee1ad66e3574d39cc8184ee0f95e74`  
		Last Modified: Wed, 19 Mar 2025 23:12:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c0dd5fe81f1dfacefd59bdf659a1a857dec0e08a96a4e1814e68b0706d7fec`  
		Last Modified: Wed, 19 Mar 2025 23:12:53 GMT  
		Size: 8.5 MB (8513670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f72c3884d603a8a01c9a3483d0acc8788d4a771f36b086838d45c407016e05`  
		Last Modified: Wed, 19 Mar 2025 23:12:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.13` - windows version 10.0.17763.7009; amd64

```console
$ docker pull hylang@sha256:293fc36d70665504e319e0dac3103ccc42422e4ecc21f3d7cab064a7c50ccd31
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216555898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b8b32dc6bc74bf7533ed9285b15554c82b9c32b3a1cb7c90b57eca0ea7b530`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:55:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:55:45 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 12 Mar 2025 18:55:46 GMT
ENV PYTHON_VERSION=3.13.2
# Wed, 12 Mar 2025 18:55:46 GMT
ENV PYTHON_SHA256=9aaa1075d0bd3e8abd0623d2d05de692ff00780579e1b232f259028bac19bb51
# Wed, 12 Mar 2025 18:57:25 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:57:26 GMT
CMD ["python"]
# Wed, 19 Mar 2025 23:12:08 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 23:12:11 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 23:13:29 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 19 Mar 2025 23:13:30 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a22a4c42a919099f93eb0448bbf22221e5f1ad7f8e0cb797dd2c576c582d8e`  
		Last Modified: Wed, 12 Mar 2025 18:57:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f930bb580d3662cfda06ce17cf4317350a4e86cf9d9fc4e65e2b92fe383ba8a6`  
		Last Modified: Wed, 12 Mar 2025 18:57:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69339a3e609449ec77a0db937e8a3c351c2733f98b759f939f6f0902c6d49a50`  
		Last Modified: Wed, 12 Mar 2025 18:57:28 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6d13cd637afb7ffa35035e4e52059652b8cc5d29c88fd6fd174ca75f32d8dc`  
		Last Modified: Wed, 12 Mar 2025 18:57:28 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161a85e590b107d865f863fc00bfa1985305617d4e88642df9ed4a0d945217e4`  
		Last Modified: Wed, 12 Mar 2025 18:57:33 GMT  
		Size: 57.8 MB (57751070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c49f0a8a406b17ca17c02c84a230128dff721fa57def525e725c2fcdf47a4b`  
		Last Modified: Wed, 12 Mar 2025 18:57:28 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba7719d23823c6f77fca8f5138243fab31996b717ff10d6750365469418983d`  
		Last Modified: Wed, 19 Mar 2025 23:13:33 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4dbdf7eb693d67b200f49d06b642c706a32274dba96c6f209b67315fdea0c0`  
		Last Modified: Wed, 19 Mar 2025 23:13:32 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5d812de04b3e7fae5f2db8ef7000c4d19185a06fd394217d1f57fb65887b39`  
		Last Modified: Wed, 19 Mar 2025 23:13:33 GMT  
		Size: 7.2 MB (7159709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5e6b5919fad3785b76d6a459352ffc6f2b9eeb0dc7d44e36c864c5786e4ac9`  
		Last Modified: Wed, 19 Mar 2025 23:13:32 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
