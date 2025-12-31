## `hylang:latest`

```console
$ docker pull hylang@sha256:451c42e5407562fc7fe1317725fc6032b180f8173ea9e3ab898a5305fa95244f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `hylang:latest` - linux; amd64

```console
$ docker pull hylang@sha256:f7efbf4d70cfd0ebc6ce928903a799aa9f9ce7518e666e9c546a6d44d46ffc00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49008211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53e440a17c0a6bbdb882101e749d2e94477ab07c2fc710a23bae06f5198281b`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:33:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:33:54 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 30 Dec 2025 00:33:54 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Tue, 30 Dec 2025 00:39:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 30 Dec 2025 00:39:35 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 30 Dec 2025 00:39:35 GMT
CMD ["python3"]
# Tue, 30 Dec 2025 01:49:31 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 01:49:31 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 01:49:31 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 01:49:31 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ece212626a44451fd18280956791ed8d3fed8fd252717a970c2b79411c4903`  
		Last Modified: Tue, 30 Dec 2025 00:39:50 GMT  
		Size: 1.3 MB (1292736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4025aea9e4c1e743787a4c2298d6f6d593a0200c17f93f55a7b730ffe271398`  
		Last Modified: Tue, 30 Dec 2025 00:39:50 GMT  
		Size: 12.2 MB (12236221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbf6e277eea76010be1dccc57e6edac2bd3ad9e2fde8db2270a64508b233780`  
		Last Modified: Tue, 30 Dec 2025 00:39:53 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c1cbb3a59c7796923ceb55d54f03cd346731f746074882ee37c11f3f5f1820`  
		Last Modified: Tue, 30 Dec 2025 01:49:42 GMT  
		Size: 5.7 MB (5702473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:latest` - unknown; unknown

```console
$ docker pull hylang@sha256:7918c12a3262314c4b490045954cdf975b295825e84a29d23489ad07da9cfdfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dd26b4a7a966971fb8fb9e17d18307ab4df759a7ff4da7a13deec3ef3de6e4`

```dockerfile
```

-	Layers:
	-	`sha256:0f0f3089a3bd82914908014e2206411060b41a3ec13c6dd9ef2ce93e2dd9a4cd`  
		Last Modified: Tue, 30 Dec 2025 03:25:48 GMT  
		Size: 2.2 MB (2156543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de21569c5a7b00917af478d5349919da69ce958ec5ea80ab5cc73a066f87038e`  
		Last Modified: Tue, 30 Dec 2025 03:25:49 GMT  
		Size: 11.6 KB (11643 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:latest` - linux; arm variant v5

```console
$ docker pull hylang@sha256:d11f698c17e7c28d2b5c7b6a7d625f06296396f39d691c3ca546c96a0e481719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46834394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f146db83e2a15b14209b63e6abeb14c97302b78a7c0871cd0e3ea76ce9c9af31`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:44:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:44:26 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 30 Dec 2025 00:44:26 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Tue, 30 Dec 2025 00:54:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 30 Dec 2025 00:54:48 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 30 Dec 2025 00:54:48 GMT
CMD ["python3"]
# Tue, 30 Dec 2025 01:59:57 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 01:59:57 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 01:59:57 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 01:59:57 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0431c846b026335d267d6349a999990f56440f916951a2877858371cf13000f5`  
		Last Modified: Tue, 30 Dec 2025 00:55:02 GMT  
		Size: 1.3 MB (1275902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777eabd2672b084ee61ce408a7ce481553ea504efd3f3f6f140a50210f291784`  
		Last Modified: Tue, 30 Dec 2025 00:55:02 GMT  
		Size: 11.9 MB (11911548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a793b97baaa4b97622d4d7ca5044c5a6c23bf93ecd21929ea456ef367b5ab23c`  
		Last Modified: Tue, 30 Dec 2025 00:55:01 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea68794c3e4e01a48443e476bf86fa21483599b536e42f3c0cf153d9712298be`  
		Last Modified: Tue, 30 Dec 2025 02:00:13 GMT  
		Size: 5.7 MB (5702550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:latest` - unknown; unknown

```console
$ docker pull hylang@sha256:cea5ae722cf03202a6c2a9fc29383180eef8e39a3f9222e687597c35b5ea57fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2171427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39aa71392fbd7485e6e80447ac969b2aab07b4e313937f1024623120c0fe854`

```dockerfile
```

-	Layers:
	-	`sha256:9a1032db25fbcb972e714bff568a95d3ddd80e7fb37760286ab9642ec83aa07d`  
		Last Modified: Tue, 30 Dec 2025 03:18:17 GMT  
		Size: 2.2 MB (2159608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b000f7765372ddfbcb43b08b9c9b0e683de2c0b09a9aea751f56276b80af1c`  
		Last Modified: Tue, 30 Dec 2025 03:18:17 GMT  
		Size: 11.8 KB (11819 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:latest` - linux; arm variant v7

```console
$ docker pull hylang@sha256:c20a28a6ffba55bb00091fbdbb99c191f306d14d29c48a4ba1dfcf6ba690f42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44757701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2e7ff4451e87ae96a03ad5c21c8bb31c6505f8af9947778637c25bf8fbb05b`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:23:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:23:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:23:01 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 30 Dec 2025 01:23:01 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Tue, 30 Dec 2025 01:32:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 30 Dec 2025 01:32:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 30 Dec 2025 01:32:06 GMT
CMD ["python3"]
# Tue, 30 Dec 2025 02:43:36 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 02:43:36 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 02:43:36 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 02:43:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fdc61a254d303b8d8d4459871bb7f69e39a09e8ed341ab5e653c9fdb37f7db`  
		Last Modified: Tue, 30 Dec 2025 01:32:20 GMT  
		Size: 1.2 MB (1248509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4a684368c669e5438ef9027ef20a09e71af79ea7700eae5d41edbf6f88b557`  
		Last Modified: Tue, 30 Dec 2025 01:32:22 GMT  
		Size: 11.6 MB (11596305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548663d3fb546e0febcf79206b378c15e39cb3c8a4ee4a208638b1d28f142c25`  
		Last Modified: Tue, 30 Dec 2025 01:32:20 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a19a0a0e40a34585f9c999af04ad30025dbeabd9df7ab712cda3a97b66e4758`  
		Last Modified: Tue, 30 Dec 2025 02:43:50 GMT  
		Size: 5.7 MB (5702638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:latest` - unknown; unknown

```console
$ docker pull hylang@sha256:b3ae1ac3fea89b53a3e84359a5c87e607369c2e44623085ed51a8c23baf68213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a501aef469ededba584af6a7cca42242337df322a942068ee2fe4c7f7c1cb34d`

```dockerfile
```

-	Layers:
	-	`sha256:ac6676e26d9e0ab64c32e72f0d2aedeec6716f2cd370e62ec972f5ffdc71546f`  
		Last Modified: Tue, 30 Dec 2025 03:23:29 GMT  
		Size: 2.2 MB (2158061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b05071eef701c73ca8093cb3f9c0e0948727e0d0193fbae8977cca6781b3e436`  
		Last Modified: Tue, 30 Dec 2025 03:23:30 GMT  
		Size: 11.8 KB (11819 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:latest` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:4388b7480bcb7f93c6d429132407792f11f1a00e8e6860cd79722adb229d58bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49259696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ae8465478ec96593ba043431b6b33d00b1913c9fb77e9eddb2246ab92ff9ff`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:35:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:35:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:35:47 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 30 Dec 2025 00:35:47 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Tue, 30 Dec 2025 00:41:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 30 Dec 2025 00:41:38 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 30 Dec 2025 00:41:38 GMT
CMD ["python3"]
# Tue, 30 Dec 2025 01:49:23 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 01:49:23 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 01:49:23 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 01:49:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14998a248d350de213db31091e5cc619079a6b2e1daf613610a375a804d0258`  
		Last Modified: Tue, 30 Dec 2025 00:41:53 GMT  
		Size: 1.3 MB (1273783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64455e1677ed4186fc05a3dbe8b04f8fcc4ecc6ecaff5f3772d268658d168020`  
		Last Modified: Tue, 30 Dec 2025 00:41:54 GMT  
		Size: 12.1 MB (12144629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b098086d0477bc9adf737e8771d2352d768cc038b9dc0bd0db1ec46b17b66e40`  
		Last Modified: Tue, 30 Dec 2025 00:41:52 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5618ace3b588b371637d46151f18ac85f0cba4c80efb9940fda5b8b0481b38ce`  
		Last Modified: Tue, 30 Dec 2025 01:49:35 GMT  
		Size: 5.7 MB (5702399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:latest` - unknown; unknown

```console
$ docker pull hylang@sha256:f90914eca12d14737372fd52ce267e1fdca57bee9f4cb42bf9775770a6d5a6dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1db48a31c53f3ebbeba0220bd776bc6eff888a917b13ea3f009f8029332ef9`

```dockerfile
```

-	Layers:
	-	`sha256:d047699e2eca01e36f1eee95245681ea0f56ba29e92df1d828acb1da2939887c`  
		Last Modified: Tue, 30 Dec 2025 06:17:35 GMT  
		Size: 2.2 MB (2156953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:735dcf6b79a7fa3cd33c209b72cff79be41a4339bb178b0182121dcff6a1381d`  
		Last Modified: Tue, 30 Dec 2025 06:17:36 GMT  
		Size: 11.9 KB (11891 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:latest` - linux; 386

```console
$ docker pull hylang@sha256:10693a80a9788643ced129728955a07d485860e5f8733c75d7b8eb27c179fb6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50657509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714bddeb322d714f003cf48acee50b6dba600296feda8865d0315b94d0b4f581`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:59:17 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:59:17 GMT
ENV PYTHON_VERSION=3.14.2
# Mon, 29 Dec 2025 23:59:17 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Tue, 30 Dec 2025 00:05:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 30 Dec 2025 00:05:50 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 30 Dec 2025 00:05:50 GMT
CMD ["python3"]
# Tue, 30 Dec 2025 01:06:20 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 01:06:20 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 01:06:20 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 01:06:20 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7420cca60f59fc7e6698d074c6c533a206babff599e59f3c89159ba3bc6942`  
		Last Modified: Tue, 30 Dec 2025 00:06:03 GMT  
		Size: 1.3 MB (1296811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb1a8be0f6da8f51f3f22b81a3e4d1579ad81bb08ae97a8763b36d48faa27c7`  
		Last Modified: Tue, 30 Dec 2025 00:06:04 GMT  
		Size: 12.4 MB (12364914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7caa4be062f5a6bd386856bf3048c469e168a0f3696bc527a06c9312892a5be7`  
		Last Modified: Tue, 30 Dec 2025 00:06:02 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9f3ac2a32f5773728b872f87f996c1264de0734e5562ce39fc1315cbd42510`  
		Last Modified: Tue, 30 Dec 2025 01:06:32 GMT  
		Size: 5.7 MB (5702435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:latest` - unknown; unknown

```console
$ docker pull hylang@sha256:c42fdb50eed65f5a5d2ac12bca799f44255fab30d411cabcec71b064fcc6f730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bebc902ae9ef1a68fbb6aacffebe379d1997bc9c0875eaca1312377d4ca854c2`

```dockerfile
```

-	Layers:
	-	`sha256:3d8e06b14a3ba189ea6aaa48d3c4df453f649ff7eaa44e9dedafb5b6d717792d`  
		Last Modified: Tue, 30 Dec 2025 03:18:27 GMT  
		Size: 2.2 MB (2153664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ab5dc5e62fbb319170a8cced0f4636ab846f6adf3eda7db5fa09d1e2fc12701`  
		Last Modified: Tue, 30 Dec 2025 03:18:27 GMT  
		Size: 11.6 KB (11551 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:latest` - linux; ppc64le

```console
$ docker pull hylang@sha256:064d9bdeee565715a9f5b27dd83c55fa6178e24078df7989db7cbdd24b8a77e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53259670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4611c9b57631991162337545241e7aa2b7b7a9a48a655ac1acf9b1824d2c2274`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 18:07:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 18:07:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 18:07:06 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 30 Dec 2025 18:07:06 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Tue, 30 Dec 2025 18:22:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 30 Dec 2025 18:22:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 30 Dec 2025 18:22:43 GMT
CMD ["python3"]
# Tue, 30 Dec 2025 21:18:20 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 21:18:20 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 21:18:20 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 21:18:20 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4bd4729a286b142b5a98c2563d17744b9f63bb8beb815a0079615bfb48d0f8`  
		Last Modified: Tue, 30 Dec 2025 18:15:45 GMT  
		Size: 1.3 MB (1320613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204545554418f2301e925f0f26e2bf520a20c824ca5b955207b1a1019dec1def`  
		Last Modified: Tue, 30 Dec 2025 18:23:17 GMT  
		Size: 12.6 MB (12639280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0151d570a21198ea3e2b6a3fb7cd4f95b26c69a651546add3b418d01096faaf`  
		Last Modified: Tue, 30 Dec 2025 18:23:15 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6e4fd44f8ca2f31c1c4118eae98b1248b294496d54c37dc0e7b2d51b9b07ec`  
		Last Modified: Tue, 30 Dec 2025 21:18:50 GMT  
		Size: 5.7 MB (5702637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:latest` - unknown; unknown

```console
$ docker pull hylang@sha256:c8aa40401317d7b174776081d481a4cdc2454fa9040af6ac19e4346a58a39818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2171941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f613981d6d589db42c162349168537f2c189c9e1b807c8a6eea3595e6eb1b1`

```dockerfile
```

-	Layers:
	-	`sha256:cf9a1de7d0e5e023ab0111ed225d3ab1bd70b23b315b15bbc13911106e71430b`  
		Last Modified: Wed, 31 Dec 2025 00:17:35 GMT  
		Size: 2.2 MB (2160182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:570f3bf5e0fe7924955d9079c5ec6a0b414ec68bb3e6dbed55827aaddf4896e2`  
		Last Modified: Wed, 31 Dec 2025 00:17:36 GMT  
		Size: 11.8 KB (11759 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:latest` - linux; riscv64

```console
$ docker pull hylang@sha256:68b4d80a3e3c688b5931e3764f1f5e9cc00d79c20b498c8d392e68e4a0b3e504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47488816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40ba8477b8f9ac7993aa6756e73257a9a9fdd9dbb897e7dab1ff8bfbfc03a7e`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Fri, 12 Dec 2025 11:42:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Dec 2025 11:42:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 12 Dec 2025 11:42:49 GMT
ENV PYTHON_VERSION=3.14.2
# Fri, 12 Dec 2025 11:42:49 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Fri, 12 Dec 2025 15:26:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 12 Dec 2025 15:26:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 12 Dec 2025 15:26:20 GMT
CMD ["python3"]
# Sun, 14 Dec 2025 16:56:52 GMT
ENV HY_VERSION=1.1.0
# Sun, 14 Dec 2025 16:56:52 GMT
ENV HYRULE_VERSION=1.0.1
# Sun, 14 Dec 2025 16:56:52 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 14 Dec 2025 16:56:52 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7a18dd7255d28116e5034ded923398dc215d1d14b5b19d6e2de6447e5e3d7b`  
		Last Modified: Fri, 12 Dec 2025 13:34:12 GMT  
		Size: 1.3 MB (1259919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb99f6a8a0de78cdf49a04b5351a082c40b1155b3c7da410a2832151c483c7c`  
		Last Modified: Fri, 12 Dec 2025 15:27:40 GMT  
		Size: 12.3 MB (12251714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212635fcb97e68995984e7625b524bf304167e25a01f991e952b9e5ea7b3ca30`  
		Last Modified: Fri, 12 Dec 2025 15:27:39 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9769d73c2b514d45ae98d5fefd68e396783eac20e6a755ae1b62018f10ea91af`  
		Last Modified: Sun, 14 Dec 2025 16:58:00 GMT  
		Size: 5.7 MB (5703777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:latest` - unknown; unknown

```console
$ docker pull hylang@sha256:6d358dc47eba73ab95ce82fa1186c2243bdc89ef9084c831d4a601ceb076a1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2162312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a437cfca83711a3b0bd25455d2d7b34182215c67f17857fbda035497ffe84c97`

```dockerfile
```

-	Layers:
	-	`sha256:b6cc166838e246fd705ab99c5087b3a8caac504a13765bd9d906906ae3b1a887`  
		Last Modified: Sun, 14 Dec 2025 18:17:42 GMT  
		Size: 2.2 MB (2150553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bd97f42a812c0f8edc2c1957d3ffc5622be4e65488caafc2898bc0b10b30439`  
		Last Modified: Sun, 14 Dec 2025 18:17:43 GMT  
		Size: 11.8 KB (11759 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:latest` - linux; s390x

```console
$ docker pull hylang@sha256:916bf3ed8639370e81a4cea104e705a6603b610f5ce8ba8ac837b43ddd74349f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49124192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daeee652800c7fed729f35e9e74cf7d5b29dede5805c66592fdb0d338a3d0ed2`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:17:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:17:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:17:21 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 30 Dec 2025 01:17:21 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Tue, 30 Dec 2025 01:25:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 30 Dec 2025 01:25:31 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 30 Dec 2025 01:25:31 GMT
CMD ["python3"]
# Tue, 30 Dec 2025 03:03:08 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 03:03:08 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 03:03:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 03:03:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5c95ab9515f2ae19805c793521a57ba8b31b74e28a3d77cdc74e8d30ee5182`  
		Last Modified: Tue, 30 Dec 2025 01:25:49 GMT  
		Size: 1.3 MB (1305200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93876a31a7311a7d4a4c7c1c4ad111b393c54f247016a641465432d99dadb969`  
		Last Modified: Tue, 30 Dec 2025 01:25:50 GMT  
		Size: 12.3 MB (12282285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18bbc6ea2b5240febd37658007d9e5008080ea56a76aae201e0a2d807e3e0a4`  
		Last Modified: Tue, 30 Dec 2025 01:25:50 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a01ee15c758685077aa146a84a70f874ec5fc0ad7ec8a3e1a97f6a58ef49d23`  
		Last Modified: Tue, 30 Dec 2025 03:03:25 GMT  
		Size: 5.7 MB (5702039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:latest` - unknown; unknown

```console
$ docker pull hylang@sha256:1b1163e47c69212b85e829c5f734db7e78f0eea3d2eba6c74f49648043a0c21f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7784af751e027099643881b056ea658512e9c534862a34556207b9430679ffc3`

```dockerfile
```

-	Layers:
	-	`sha256:dc478e50967776ba9b5796eb3d3a8fa23bde5a9d7fc0b6438dbf3b87958baa85`  
		Last Modified: Tue, 30 Dec 2025 03:23:22 GMT  
		Size: 2.2 MB (2157982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e03d1b538f6581cdd48336d0a41c7b3ee04ad6403eb207418e3e220c6c711752`  
		Last Modified: Tue, 30 Dec 2025 03:23:23 GMT  
		Size: 11.6 KB (11643 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:latest` - windows version 10.0.26100.7462; amd64

```console
$ docker pull hylang@sha256:a5471035e2fc9d5495e1b4cacd8f5c3319ec1d287617811ee7f182b4abb9641b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3322794273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e37d11bac81c940106aaebfb635f85f4b2f08d87bf7cb5089ca0e434c6f92989`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:36:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:48:39 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 09 Dec 2025 20:48:39 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 09 Dec 2025 20:48:40 GMT
ENV PYTHON_SHA256=9db919cefe30a0051658c600a9912acb0cd2b872aaf35842c9ec2bf401efa848
# Tue, 09 Dec 2025 20:49:20 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:49:21 GMT
CMD ["python"]
# Tue, 09 Dec 2025 21:19:45 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 21:19:45 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 21:20:17 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 09 Dec 2025 21:20:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a705a6e8ee03f99b80a0bf2257b33ccbf03d0695038a45544f551b47f1bad3`  
		Last Modified: Tue, 09 Dec 2025 20:46:08 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf2ec845e36092f35025b446f4a84789d0001875a44461df70da99007d8c432`  
		Last Modified: Tue, 09 Dec 2025 20:49:36 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea37b5eb971dd19514c3870274b3fd9711466e67cccb7a7f24a91c38b0362fa`  
		Last Modified: Tue, 09 Dec 2025 20:49:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d417a9df3ccce81c9113e8703f978f15412ac84a925185238929e01cb6766e38`  
		Last Modified: Tue, 09 Dec 2025 20:49:36 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c61149ef6a0674515ed5e1b6e541ff115a9eb10b693013a24c76c520c72142`  
		Last Modified: Tue, 09 Dec 2025 20:49:40 GMT  
		Size: 61.0 MB (60991350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572b5e0dfab25e9a33e424ed104eaf77ebbbb399d910a48202a88479848d285b`  
		Last Modified: Tue, 09 Dec 2025 20:49:36 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9772c8c66e0357966cf423f2876cd6852a0866d50f1dcd0d0dc73b92611ba556`  
		Last Modified: Tue, 09 Dec 2025 21:20:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5eedfc4b9c1ff3d56ffb488e88b218a64ea42891d75b8d8e14897910a29d079`  
		Last Modified: Tue, 09 Dec 2025 21:20:31 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4e63ae16a595240a6642a2c658581dc1a9eba03313ca02417c7e308134cb0b`  
		Last Modified: Tue, 09 Dec 2025 21:20:32 GMT  
		Size: 8.7 MB (8671998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8aff4cfa4c88ec8903d511519914d8020c142d82432226272620d94f28498a`  
		Last Modified: Tue, 09 Dec 2025 21:20:31 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:latest` - windows version 10.0.20348.4529; amd64

```console
$ docker pull hylang@sha256:85c4c33c61f82db63e78abda88b57e1891ddc3afda49bc0bcb46e4a29746b836
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1849278774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612f3f589b4ad22120d6bebc31c84d9ff03b0d7f5e9d4737b382d42d2c614882`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:32:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:46:49 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 09 Dec 2025 20:46:50 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 09 Dec 2025 20:46:51 GMT
ENV PYTHON_SHA256=9db919cefe30a0051658c600a9912acb0cd2b872aaf35842c9ec2bf401efa848
# Tue, 09 Dec 2025 20:47:32 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:47:33 GMT
CMD ["python"]
# Tue, 09 Dec 2025 21:18:07 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 21:18:07 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 21:18:37 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 09 Dec 2025 21:18:37 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768ea431b13531bd18fa519503dcde235d1371c06640fff6c434a8dc2f78f370`  
		Last Modified: Tue, 09 Dec 2025 20:40:48 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34587e3124c2354fd0c0ebc422da5a49bd90585ddb565123a6a607568a27d77f`  
		Last Modified: Tue, 09 Dec 2025 20:47:53 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73959298aa0c72f2ef4c2adaca9c6319ad8f57fb3ad3139a3ffb6f2bcc4a5b3`  
		Last Modified: Tue, 09 Dec 2025 20:47:53 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6b048b9df31de6a2a4089f32d19b21bd49c1d7b7f74b76ccb3aa9c0bc59fa8`  
		Last Modified: Tue, 09 Dec 2025 20:47:53 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee5ca9163acd37c8180f34b414cf06699edfa777c693d18342d5ef32acf65d1`  
		Last Modified: Tue, 09 Dec 2025 20:47:56 GMT  
		Size: 60.9 MB (60925935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00182617a1921b03d51762122e1f5fba52b8fc8b81bb5dce8c52a89e1006f37f`  
		Last Modified: Tue, 09 Dec 2025 20:47:53 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a90193fde56b94387115cb7a9bb70247f3edc2ad56c4ff21a7f579334ba0f0`  
		Last Modified: Tue, 09 Dec 2025 21:18:50 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00d4a78ee2079fb5985f93c52b3f084eccb212b54c40ba741e5420246382084`  
		Last Modified: Tue, 09 Dec 2025 21:18:49 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee27e8ac372fc8a0aae394d73c7808d9d8e95cb91b4399b0636a296d5b5d5f7`  
		Last Modified: Tue, 09 Dec 2025 21:18:50 GMT  
		Size: 8.5 MB (8463038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5d0fa7ccdddd9c04be3e2eee5ef7917d4dcd00aad2f373a94f8adbb7168fb8`  
		Last Modified: Tue, 09 Dec 2025 21:18:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
