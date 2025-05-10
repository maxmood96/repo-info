## `hylang:1-python3.14-rc`

```console
$ docker pull hylang@sha256:ddb92188fc4b67bc844decd151691585fb56ad59b48527d35f7242d04072dfc0
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
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `hylang:1-python3.14-rc` - linux; amd64

```console
$ docker pull hylang@sha256:7478b515375046c81e3d1bb842ca5d1deae4bf75812df052604869c36ce7f4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50504905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c547810a6b82119d1afa153de429a509c9a729cc109958d9022a4a65fccbb205`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef12a421c2d6dd1355f766ffdd1b39b597a1548edbb91064692a23e3f072c7d4`  
		Last Modified: Fri, 09 May 2025 23:52:40 GMT  
		Size: 3.5 MB (3511543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eaa4e10b15f185cd5051fa3b195764ae61489e190bbeee30dec23f6134ea384`  
		Last Modified: Fri, 09 May 2025 23:52:40 GMT  
		Size: 12.9 MB (12928920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a521f6bf43dd89adf9e831a017dd174bc08a1c2bfa8462eec26a0a8cc5742713`  
		Last Modified: Fri, 09 May 2025 23:52:40 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbcd8d5c3aa802e5996a81664d86642e298bf2a196ebdbc5d19c47bb0242e4b`  
		Last Modified: Sat, 10 May 2025 00:08:23 GMT  
		Size: 5.8 MB (5836550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc` - unknown; unknown

```console
$ docker pull hylang@sha256:ef4a47f7073a0c8bbf8064b7b109e74da8f7d019537ca3b29e64256797e748bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2427152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e13996c03a3c50704da91278d1204c53b116f56ea971efdc8792ed7d8576a2`

```dockerfile
```

-	Layers:
	-	`sha256:0c4c0bcba8ddec966e347a8266a67c02299b67e35b34d83889576d996308c4af`  
		Last Modified: Sat, 10 May 2025 00:08:23 GMT  
		Size: 2.4 MB (2417879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94dc292931f90e67aaee434a0f0d605d9aacfa6ea7c92b06d0478694c846dc69`  
		Last Modified: Sat, 10 May 2025 00:08:23 GMT  
		Size: 9.3 KB (9273 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc` - linux; arm variant v5

```console
$ docker pull hylang@sha256:680ac08a6df27018802f3480bbc06fd307a0a4a48f527fe243a0b16192794e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47143528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee917f0461f0a93d209515e86485677d36abaae880bfe488337beff11969e9bb`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1745798400'
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
	-	`sha256:3bc532ff9d2a2a12c6cfc746359843257a240960865aea7ecb10c71e0b93ec78`  
		Last Modified: Mon, 28 Apr 2025 21:07:56 GMT  
		Size: 25.8 MB (25757836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b8d512a04fed6149402cb65a83d9920655b3fcbdaf346d2eca33197082bfab`  
		Last Modified: Tue, 29 Apr 2025 01:56:41 GMT  
		Size: 3.1 MB (3082287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724cce1bd12d2c2fe9a1a7ac21054f3ce3e4a66840d4a0f156216d0e088ac670`  
		Last Modified: Sat, 10 May 2025 00:29:39 GMT  
		Size: 12.5 MB (12466278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbc892516cd8dc28c3dfd6d3e5114e34df0ec0758177251adfebefb1ef23725`  
		Last Modified: Sat, 10 May 2025 00:29:39 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30c5e649a8fe8640a75b45733bb93e521fd291f2aba4de6f0285bdbdda21d50`  
		Last Modified: Sat, 10 May 2025 05:46:33 GMT  
		Size: 5.8 MB (5836877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc` - unknown; unknown

```console
$ docker pull hylang@sha256:0bcab333a316ed98b7db4774355f7d190dc555477d442e59852cf994a20cf2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2430796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0393f4ada17c184ac4b1d494b7daa5172611d3e43272d8be0194b780687d44b`

```dockerfile
```

-	Layers:
	-	`sha256:5d5a737003dced75bf748e9d97dbfc6b2ce1f83bc6baf18dfb7ab8b37d130544`  
		Last Modified: Sat, 10 May 2025 05:46:33 GMT  
		Size: 2.4 MB (2421415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70bfcadaf89b7a591364c51fd6edb78cb95be564eaea62af9cbe744ae8045a67`  
		Last Modified: Sat, 10 May 2025 05:46:33 GMT  
		Size: 9.4 KB (9381 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc` - linux; arm variant v7

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

### `hylang:1-python3.14-rc` - unknown; unknown

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

### `hylang:1-python3.14-rc` - linux; arm64 variant v8

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

### `hylang:1-python3.14-rc` - unknown; unknown

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

### `hylang:1-python3.14-rc` - linux; 386

```console
$ docker pull hylang@sha256:b9102934855f1535c2f2f61e0714f271d982be415dbf084fe67bd95dba1ec049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51756599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b21b46e0a70052073decb5536a34d4b93bec98da0ddee62d182e0a0188009f`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f7997e8017b3af87403d22f64fad1d610aaef069008f2d81a3450f7586aae7`  
		Last Modified: Fri, 09 May 2025 23:56:18 GMT  
		Size: 3.5 MB (3509842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ff3eaf8eaf21a9aba9cbe4b1934d9cea6b4da95cab11ad48d5ca4b0ebd6def`  
		Last Modified: Fri, 09 May 2025 23:56:18 GMT  
		Size: 13.2 MB (13198968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a782399c5bbacb7908c9aa71cf4c730596b1232aab8ef0829fac2ddaae7d238`  
		Last Modified: Fri, 09 May 2025 23:56:18 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28d35af1616d540a8a91fcebedaf9e6d5f6d201cdf909b89f3d16009c26f120`  
		Last Modified: Sat, 10 May 2025 00:08:24 GMT  
		Size: 5.8 MB (5836673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc` - unknown; unknown

```console
$ docker pull hylang@sha256:bc0a1480feeb7fa00aace53be8c56e9c0b67e9f3e04a2c0e441c475b5748787b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2424203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26479d9b788b14b2dfe23c39cb54c285aa242eca7feee4dcde26865eff6910aa`

```dockerfile
```

-	Layers:
	-	`sha256:f64d593ff0c669b5dfc16f9d2d178f3234a7825e535c12eac77fbe58eee5968f`  
		Last Modified: Sat, 10 May 2025 00:08:24 GMT  
		Size: 2.4 MB (2414982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f04d6b3f9aa738b6cb85b35b5b56e17f9105a1033ae134c6fdfd1842cdd53de`  
		Last Modified: Sat, 10 May 2025 00:08:24 GMT  
		Size: 9.2 KB (9221 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc` - linux; ppc64le

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

### `hylang:1-python3.14-rc` - unknown; unknown

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

### `hylang:1-python3.14-rc` - linux; s390x

```console
$ docker pull hylang@sha256:7101a9f7a2202a3614950e2ea5c97442974a892b8c4d092df9b51f786a17cba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48658404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57305a4e5bdf248ae4e02563db61e11ce6ec8e4bbe63ed665954d390adcce8c9`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecb4989536cb9f05eecafcab5ea2269701d85b5ab709d3356c89dff9c4af0bd`  
		Last Modified: Thu, 08 May 2025 21:44:02 GMT  
		Size: 3.2 MB (3173164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1072a99de4540bf92d7ce6c8f6c5df157a2b77f759a59b356ba2364059bbf9`  
		Last Modified: Sat, 10 May 2025 00:06:04 GMT  
		Size: 12.8 MB (12763503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a2bdb659ed79e9590c0bcaa9bdd75b4a588154293e96d0cee2249ecc5bb295`  
		Last Modified: Sat, 10 May 2025 00:06:04 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f5276a455fdb189ccb23df04373e729c01a144500f96b1720d6e63c03b2da3`  
		Last Modified: Sat, 10 May 2025 02:43:55 GMT  
		Size: 5.8 MB (5836620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc` - unknown; unknown

```console
$ docker pull hylang@sha256:36154be59117f36daa837403d35014916294c74c5162bc29130a8480b0eea359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2426868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655ddedefb0813c6fb5e9f62cea62b7fa81e0b9c8d0f3cec888178138b04399b`

```dockerfile
```

-	Layers:
	-	`sha256:08b3ff8fb23034116980515180b94d79489a9e58a567ddb3af5a57e7a558cf53`  
		Last Modified: Sat, 10 May 2025 02:43:55 GMT  
		Size: 2.4 MB (2417595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e1b3a381836e1e736ff35c44e8620da665bd6c0f0f148cf3cd4170a8e1d5b31`  
		Last Modified: Sat, 10 May 2025 02:43:54 GMT  
		Size: 9.3 KB (9273 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc` - windows version 10.0.26100.3781; amd64

```console
$ docker pull hylang@sha256:51c90b46a1d2ec847addb2c72a33269430b47219b7c00b840f53b42589d1f398
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3467863316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c52c8bc2764a35a4831c7aa0e0030b890c2e70dca90f4964674cb2ea06e4aa`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Thu, 08 May 2025 21:07:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 08 May 2025 21:07:30 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 08 May 2025 21:07:32 GMT
ENV PYTHON_VERSION=3.14.0b1
# Thu, 08 May 2025 21:07:34 GMT
ENV PYTHON_SHA256=a878026c12b1a606d02f5bbf3ed65aa780ee8272964b8f95d8348ffa2d6ca096
# Thu, 08 May 2025 21:08:21 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Reinstalling pip to workaround a bug ...'; 	Remove-Item -Recurse C:\Python\Lib\site-packages\pip*; 	python -m ensurepip --default-pip -vvv; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 08 May 2025 21:08:24 GMT
CMD ["python"]
# Fri, 09 May 2025 17:36:29 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 17:36:29 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 17:37:02 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 09 May 2025 17:37:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e566d8b06fba270b2f042931911ff37db43220097b48a11faf9b0cf7773fd752`  
		Last Modified: Thu, 08 May 2025 21:08:31 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c3fa78ea6d722c36a4e2b5935d54060c60038a248d22b1f52b0cd07b31b473`  
		Last Modified: Thu, 08 May 2025 21:08:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d5913ea8d7f396026fcbcc442e045fa4fd5e2ca298fca4539e00338432b275`  
		Last Modified: Thu, 08 May 2025 21:08:29 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4cda6e19e3e33bb8e5baa4a336333f2d75b48ca5281f45d5c774941ccc649ee`  
		Last Modified: Thu, 08 May 2025 21:08:29 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cc5727a3596993ee02afce413fd8f55b6d22c33b0239c09141b02a7660e4be`  
		Last Modified: Thu, 08 May 2025 21:08:35 GMT  
		Size: 64.0 MB (63993881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2303d8c688e1602f30854ef73997e17c02a3c9ce46b56b01792ca4b96d34d5c1`  
		Last Modified: Thu, 08 May 2025 21:08:29 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19f88a81731fae32a6e170e54805cb2d33faea32e4ed692ed25687c7b244870`  
		Last Modified: Fri, 09 May 2025 17:37:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c830b1c192f748bddff1307f8d0f9433687fab0beb8da9202e9528225de73ab8`  
		Last Modified: Fri, 09 May 2025 17:37:05 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500094bd11160239c18cac5b075ae042685cb072e62d7730bab8989327f6198d`  
		Last Modified: Fri, 09 May 2025 17:37:06 GMT  
		Size: 8.7 MB (8697592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d163b60293e1efc7d571589ef4707c98466747047138fe894a04b56bb178488`  
		Last Modified: Fri, 09 May 2025 17:37:06 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-python3.14-rc` - windows version 10.0.20348.3566; amd64

```console
$ docker pull hylang@sha256:b216552a5c6520426e3a883b372e7e3f5c8bb68d8373adb9abc2c5d8145366be
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345942996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943a41a1b0399afd6f63c9868a98b1c5b0dfc95004c2abaf3bb566d528b9ef65`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Thu, 08 May 2025 21:01:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 08 May 2025 21:01:49 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 08 May 2025 21:01:50 GMT
ENV PYTHON_VERSION=3.14.0b1
# Thu, 08 May 2025 21:01:50 GMT
ENV PYTHON_SHA256=a878026c12b1a606d02f5bbf3ed65aa780ee8272964b8f95d8348ffa2d6ca096
# Thu, 08 May 2025 21:04:24 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Reinstalling pip to workaround a bug ...'; 	Remove-Item -Recurse C:\Python\Lib\site-packages\pip*; 	python -m ensurepip --default-pip -vvv; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 08 May 2025 21:04:25 GMT
CMD ["python"]
# Fri, 09 May 2025 17:30:52 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 17:30:52 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 17:31:55 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 09 May 2025 17:31:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77ac229fd430772d28ff8bd422201baf2162fa3bd6d5a753b0bf14b3819ff75`  
		Last Modified: Thu, 08 May 2025 21:04:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f62bd2f04e256071c04669da32543921691cc128bd5396fb6bfa31eb0a15759`  
		Last Modified: Thu, 08 May 2025 21:04:27 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33c3a5c7a3bfb6a62ae1c787525d99969ddb03e01b8e384c4ff236b7605e5dc`  
		Last Modified: Thu, 08 May 2025 21:04:27 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f187d6387794e3a368eac5c5531b616310b56495a8c378a929bd56816c50deb`  
		Last Modified: Thu, 08 May 2025 21:04:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65ad62684f17a178594e1d092fb46615753253ae4cc7be0d644ed1123cd0a41`  
		Last Modified: Thu, 08 May 2025 21:04:32 GMT  
		Size: 63.8 MB (63832221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a6652b296e686e517dd0b32bd29ac0eb1a1d030095f7cfca4c9c0d8eceb881`  
		Last Modified: Thu, 08 May 2025 21:04:27 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83927c534a25d76f93f73cd13a5ae221ac5d22864de564cda6671a169fb9ea74`  
		Last Modified: Fri, 09 May 2025 17:31:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a65882d9924950cc5bd5e93e22d812e0dd544fbf6216eae9bf93ffa5567993`  
		Last Modified: Fri, 09 May 2025 17:31:59 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade6d07000471c491dad045a779d63a6c34394f9fa49bb5ebd2bff940f135884`  
		Last Modified: Fri, 09 May 2025 17:32:01 GMT  
		Size: 8.5 MB (8517962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321c8d7b4cfcf564bd81f2fbf76bd8f4d87b6c1428aafaf7accdc77c35741c9`  
		Last Modified: Fri, 09 May 2025 17:31:59 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-python3.14-rc` - windows version 10.0.17763.7249; amd64

```console
$ docker pull hylang@sha256:0b044e403b4b68ca51979f4da007420ede929ddce206d72f3450cbef306778cd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2235232339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7c8f0cf03b67e2ab277e9ca02ce89d2922f30d649481a9ce1ff8241a5ac5c5`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Thu, 08 May 2025 21:01:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 08 May 2025 21:01:51 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 08 May 2025 21:01:52 GMT
ENV PYTHON_VERSION=3.14.0b1
# Thu, 08 May 2025 21:01:53 GMT
ENV PYTHON_SHA256=a878026c12b1a606d02f5bbf3ed65aa780ee8272964b8f95d8348ffa2d6ca096
# Thu, 08 May 2025 21:04:15 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Reinstalling pip to workaround a bug ...'; 	Remove-Item -Recurse C:\Python\Lib\site-packages\pip*; 	python -m ensurepip --default-pip -vvv; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 08 May 2025 21:04:16 GMT
CMD ["python"]
# Fri, 09 May 2025 17:31:02 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 17:31:04 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 17:32:25 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 09 May 2025 17:32:26 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1674151a2d1b57666fcff6b438873f56e36b92efa4f09b3509ea6addeece66`  
		Last Modified: Thu, 08 May 2025 21:04:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a63f24da543e1237bb8e0b121c9dd19962a80ff42cf8cab1ea9e470d92e113`  
		Last Modified: Thu, 08 May 2025 21:04:21 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a50b1404ee5a6d956410e4529e308eae0b3d5fbb6226df8d9f7cacaa719c89`  
		Last Modified: Thu, 08 May 2025 21:04:21 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70772678ff5e1030977e8f1455967923e436a36f2d3b868592ecbfc32721e503`  
		Last Modified: Thu, 08 May 2025 21:04:21 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af1fd92df97140b7b08bd0fb56c0de8a4e433a402e0e7156f516291dcdc70c8`  
		Last Modified: Thu, 08 May 2025 21:04:26 GMT  
		Size: 62.5 MB (62523985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047ae51ab74cba2a32c17ce18bdfcc8ef9e33156680932be42566225314b78c0`  
		Last Modified: Thu, 08 May 2025 21:04:20 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814946dc155e44e6c7734d892d572d64a16609b15b50ac48d8367a51682415ed`  
		Last Modified: Fri, 09 May 2025 17:32:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55296eb4f22fbd87e133066316bef7bccdfee3c7b29266406fb907acb5ceabc1`  
		Last Modified: Fri, 09 May 2025 17:32:31 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8847574b0d301e41efd2313c2616d8bb69290b2f9adc6e0f6a0fd11e7daaf240`  
		Last Modified: Fri, 09 May 2025 17:32:32 GMT  
		Size: 7.2 MB (7172138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a941ff55302d9de24a1bea12410b8ad789d6eb880461ef5866e85ef1ecbab`  
		Last Modified: Fri, 09 May 2025 17:32:31 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
