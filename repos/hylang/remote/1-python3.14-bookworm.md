## `hylang:1-python3.14-bookworm`

```console
$ docker pull hylang@sha256:1bef7e71e10b591a9624eeee051177d911ce009b59434cb6d9b20f63d916017d
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

### `hylang:1-python3.14-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:848e211f640a1440e932d53fb78f4aa10a61bb102f9cd4f93292fa4e946bae98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50479948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18213830eb577e7ee6310b87c85b60e9d0ba23ea45dad0ee64f4f9cf4dcd29b9`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Wed, 10 Jun 2026 20:38:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:38:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jun 2026 20:38:30 GMT
ENV PYTHON_VERSION=3.14.6
# Wed, 10 Jun 2026 20:38:30 GMT
ENV PYTHON_SHA256=143b1dddefaec3bd2e21e3b839b34a2b7fb9842272883c576420d605e9f30c63
# Wed, 10 Jun 2026 20:50:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 10 Jun 2026 20:50:22 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jun 2026 20:50:22 GMT
CMD ["python3"]
# Wed, 10 Jun 2026 20:59:40 GMT
ENV HY_VERSION=1.3.0
# Wed, 10 Jun 2026 20:59:40 GMT
ENV HYRULE_VERSION=1.1.0
# Wed, 10 Jun 2026 20:59:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jun 2026 20:59:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cbff6fca83b12b03239f0c730e3054aca1a6ef9437b79cf40b231bf55ab618`  
		Last Modified: Wed, 10 Jun 2026 20:50:29 GMT  
		Size: 3.5 MB (3520813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a273314af5600728967b8b75efc5f29ff9b240461f49c5f96add7fdad1fed7`  
		Last Modified: Wed, 10 Jun 2026 20:50:30 GMT  
		Size: 13.0 MB (13011727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b338ee559a0952dacaf35fdc70fde2dbacb89148baac8271bdc4e406d3599e0`  
		Last Modified: Wed, 10 Jun 2026 20:50:29 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071d31be464da7fc30c28333a2d494d07d72312dcbed86e49aa5b6f97d93e96f`  
		Last Modified: Wed, 10 Jun 2026 20:59:47 GMT  
		Size: 5.7 MB (5713615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:36f4b8a4ff214b5638feae8f3e7bc3196bc7bccc41e5b06b998cab2451177322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2541285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365993439283d195bda3512dbff1548310cb3125d1b21b4cdeab08b483522167`

```dockerfile
```

-	Layers:
	-	`sha256:64c5ab3d2654f76d40dbe53eadd3c264fa19f9f59780a0d8dd3681d4b68c90ba`  
		Last Modified: Wed, 10 Jun 2026 20:59:47 GMT  
		Size: 2.5 MB (2532026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4feab84e52a43864fd02606c59048ccae3bdc6f8d792a3793f44e08c7ab5d1b4`  
		Last Modified: Wed, 10 Jun 2026 20:59:47 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:1a88fa5ad190366ca1d63fc1f8f090e26ccd3a60a046f63c9b007443ae72f47a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47103476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19221f09299044dfbd5332753521b908fffd13960ce18466a89249aef9d3d445`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:13:28 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:13:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:13:28 GMT
ENV PYTHON_VERSION=3.14.5
# Wed, 20 May 2026 00:13:28 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Wed, 20 May 2026 00:34:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 20 May 2026 00:34:36 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 00:34:36 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:46:34 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:46:34 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:46:34 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:46:34 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3e5afa2eeb01167c187727ebcf5bb90554d4e6dd21fe61f1f694b128ceb15ac1`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 25.8 MB (25768291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1316c1ecb64eaf27ac63541ee3544fc9ea27f1b2f58f327364c14cbccb4e908d`  
		Last Modified: Wed, 20 May 2026 00:34:44 GMT  
		Size: 3.1 MB (3093114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015540b7e7378be9111f1707cbd224d29109f5650c47aa8649c787e509483519`  
		Last Modified: Wed, 20 May 2026 00:34:44 GMT  
		Size: 12.5 MB (12529896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b500f0600b155b5d6ddd5340f24e64479d62aa0404ad25902d1209c669a33c76`  
		Last Modified: Wed, 20 May 2026 00:34:44 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b0101596cc96fa0b3079c738c796f1f68435e6eea28b0726c3bf800e95f051`  
		Last Modified: Mon, 08 Jun 2026 22:46:41 GMT  
		Size: 5.7 MB (5711926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:b23236c0736c04b5b6c2abcba8b60d69d51181144ddd73900d3e9d4459938195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e737f2d16be246153c6e5f07e664badec9862b105af99c27c8e06804623218c6`

```dockerfile
```

-	Layers:
	-	`sha256:343ce8945bacc4e5a87cabff65fea341fcf00f03fe22d5edb3d2dd59880d2ea5`  
		Last Modified: Mon, 08 Jun 2026 22:46:41 GMT  
		Size: 2.5 MB (2535870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e0587196ac4e379e66b3ac16eaf564fd357ad329b152ed35f296e77936c663`  
		Last Modified: Mon, 08 Jun 2026 22:46:41 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:cf20ae876285fb9d4f983fb9be99d66fd8ac50cdd1f46f07d0563b2de665d759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44717595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9e2873a17c527cd1872d9456fd68169d7dbe9c1294f2db115b6f87937a878b`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:48:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:48:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:48:57 GMT
ENV PYTHON_VERSION=3.14.5
# Wed, 20 May 2026 00:48:57 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Wed, 20 May 2026 01:11:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 20 May 2026 01:11:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 01:11:52 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:45:56 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:45:56 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:45:56 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:45:56 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:af86988b12731b7fa2ac73fa1c3f6ab4510a6641d04afb18df09600383bc399d`  
		Last Modified: Tue, 19 May 2026 22:36:05 GMT  
		Size: 23.9 MB (23941643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a290093f9239696ef58353efac3526e6f631227c8f7b97791e55bced2ab0478`  
		Last Modified: Wed, 20 May 2026 01:11:59 GMT  
		Size: 2.9 MB (2928597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e687e92f9cd7007f53196d8f65a4430e486d66d4a01db41513ea89ee1da0fd`  
		Last Modified: Wed, 20 May 2026 01:12:00 GMT  
		Size: 12.1 MB (12135339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974f44912b315307360c73e15a67841f3d325dec246858941a32aab927036018`  
		Last Modified: Wed, 20 May 2026 01:11:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1af72260faea608836ffa1c22aca57a06067eafc46c62fe4b836a7e0d2d531`  
		Last Modified: Mon, 08 Jun 2026 22:46:04 GMT  
		Size: 5.7 MB (5711766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:4319edc497cc46de041e335f767c89645cb8c8389b14903de7459c973c7e5deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2543674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09bb29088a84cee0ccfc5d43034608075579f0c3208542c59661a69527088a34`

```dockerfile
```

-	Layers:
	-	`sha256:d8d92ef650e828057d3be4cec616d51f35c9f67d56fe190345129c2a7194bba4`  
		Last Modified: Mon, 08 Jun 2026 22:46:04 GMT  
		Size: 2.5 MB (2534303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c1eec87e1c34bd7fdde6bc5a4573a6ac34d96b671d8eccc19b65f4b354fe6e5`  
		Last Modified: Mon, 08 Jun 2026 22:46:03 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:cb3a971bf66a60bb54f0007a917460bdebbc13aaf6c0fa8bb3d499062a4b8896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50067329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e196d6d7c1de29eda9a444d5b682a921996786cdea966c3bf31ea770b6b94152`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:44:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:44:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:44:11 GMT
ENV PYTHON_VERSION=3.14.5
# Tue, 19 May 2026 23:44:11 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Tue, 19 May 2026 23:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 19 May 2026 23:58:56 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 May 2026 23:58:56 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:44:47 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:44:47 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:44:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:44:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1a4708554fd71acc44f0d889b4db5c923b417c540bfc7d05775e34756372e9`  
		Last Modified: Tue, 19 May 2026 23:59:05 GMT  
		Size: 3.4 MB (3351854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219c9e25b953f3c2de078796ac641826348ce318e595de4a22d2debb11a8fa39`  
		Last Modified: Tue, 19 May 2026 23:59:05 GMT  
		Size: 12.9 MB (12888303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5721e72fc5cb5eeb28eb2caa7d9df7e5817e11a115647789025f5f042c151a76`  
		Last Modified: Tue, 19 May 2026 23:59:05 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a5d16a0485574ddab19862e75c59984152bf25e8dfc4c3f5fa454f08b5169d`  
		Last Modified: Mon, 08 Jun 2026 22:44:54 GMT  
		Size: 5.7 MB (5711879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:a4bcf4db32f9d928e89d782ccc8c169dde376d53af7cd14b3295ca6d90704c62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2541750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66daf802398ad2d091257e845a4404b4580f64c5eab218ad9ab90fa433906bfb`

```dockerfile
```

-	Layers:
	-	`sha256:88f0c9265d4931a15e97b8ab3f86bcf673bdaee751dda7b4331d71fa6297a9ec`  
		Last Modified: Mon, 08 Jun 2026 22:44:55 GMT  
		Size: 2.5 MB (2532339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39d13b72cd016f6b0c33e489ab5ca39eedefab84974e80a8028865cc45b93100`  
		Last Modified: Mon, 08 Jun 2026 22:44:54 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:7f32c2be25b698a8c22f9ab6cf639b72820b308addce88723cea981c68d10d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51735477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087121dfd6fc798dc9f01a689b92c017b3dd9ccf21f74f85453c12427a392a30`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:37:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:37:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:37:53 GMT
ENV PYTHON_VERSION=3.14.5
# Tue, 19 May 2026 23:37:53 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Tue, 19 May 2026 23:50:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 19 May 2026 23:50:33 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 May 2026 23:50:33 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:45:58 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:45:58 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:45:58 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:45:58 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:408fe432485bb366e9a4871b553de2e6347ca580fe8a5d45c84c87fa58d5e5c7`  
		Last Modified: Tue, 19 May 2026 22:37:12 GMT  
		Size: 29.2 MB (29218601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3274c33d4eb883df7a933384ff5acb16852e752a435e1a27074357f69a6de39`  
		Last Modified: Tue, 19 May 2026 23:50:40 GMT  
		Size: 3.5 MB (3520890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2cd69c5ff237d41e555ba2ba6476e03fa1b9d999a85cd038b9ccc9d1e31243c`  
		Last Modified: Tue, 19 May 2026 23:50:40 GMT  
		Size: 13.3 MB (13283881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0e82ec9a80eddcff69a177a1480182d01475d090cce2d60d178233c14ff2f6`  
		Last Modified: Tue, 19 May 2026 23:50:40 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcca1730fbbd0d007bbf6af7183d220e014fac5d1f40aad161bf3c19a76658ea`  
		Last Modified: Mon, 08 Jun 2026 22:46:05 GMT  
		Size: 5.7 MB (5711855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:df9e60cdd1abbc8c1a51afd09c8df6552fa7688faf96863937270aa67d72b6d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d802929902e3c5b6042c2847a61278ba28f54fa4247e4597f8b46e3fecc85034`

```dockerfile
```

-	Layers:
	-	`sha256:4f752ec1511af9071a070efa8930719ce28d6774c6e31c8c734a25c1a0b5a6b9`  
		Last Modified: Mon, 08 Jun 2026 22:46:05 GMT  
		Size: 2.5 MB (2529173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0ec60c753700f0f7dca7299c68116a28cac04a7c152a6b5caa8fcced51bd109`  
		Last Modified: Mon, 08 Jun 2026 22:46:04 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:eab96c3585b360a6d301b99dd086c76d75350215eb51855a3ab1e7069fc9b1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55081589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd92923e78a0933ba6f3eeb0dc8ecbaa341e04c62651c0379b8b138c9289dd0f`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 02:54:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 02:54:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:54:07 GMT
ENV PYTHON_VERSION=3.14.5
# Wed, 20 May 2026 02:54:07 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Wed, 20 May 2026 04:13:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 20 May 2026 04:13:49 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 04:13:49 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 23:15:00 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 23:15:00 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 23:15:00 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 23:15:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656be72c102b00f533067cbc2d9437f945c4e7bfd322feb0c3a1cccb673dd5ba`  
		Last Modified: Wed, 20 May 2026 03:33:50 GMT  
		Size: 3.7 MB (3725042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e765c3f1f64ad7834a7a65367b0c52f3011efa1056575a50b98eb230cc10594a`  
		Last Modified: Wed, 20 May 2026 04:14:04 GMT  
		Size: 13.6 MB (13568587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51923ffe131ad88d08eff57042008ab4a3ccdd70fdd333987622c0f41d53a1a`  
		Last Modified: Wed, 20 May 2026 04:14:03 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4c513cb29e04ca19a6532179a12455310d8dc3ab85a7130afc7754f7e2079a`  
		Last Modified: Mon, 08 Jun 2026 23:15:17 GMT  
		Size: 5.7 MB (5711968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:c6153fd0fbc83158224eb017cea895cfabf09fc767eff73736e0e9214e19125c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fee5bbb9c436f1fc3c1cc1477fae0f287259437cdd7a4bc40b1cee51c418ed9`

```dockerfile
```

-	Layers:
	-	`sha256:4f1cd287dec52f92313f8100f73a8201cfde065804c8bedff7b0961b76dc07db`  
		Last Modified: Mon, 08 Jun 2026 23:15:16 GMT  
		Size: 2.5 MB (2536488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b92ea72b272b64589bb72e17aa97e47c98a3ac459733dee9ddfb86c6acfe972`  
		Last Modified: Mon, 08 Jun 2026 23:15:16 GMT  
		Size: 9.3 KB (9327 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:c774312fc5456343a5a022002123a9ca47ad71b4924df533f24df81bb1c6dd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48613425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e35cc463f19406f5722c3f55aebcff1e059ecb74defc20fca689c94f5cca8f9`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:59:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:59:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:59:38 GMT
ENV PYTHON_VERSION=3.14.5
# Wed, 20 May 2026 00:59:38 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Wed, 20 May 2026 01:14:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 20 May 2026 01:14:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 01:14:55 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:54:28 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:54:28 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:54:28 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:54:28 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc3b40ae0abc7d79db803a5d5f6b8363ddd984965d9be43d17b3b4e4d351706`  
		Last Modified: Wed, 20 May 2026 01:15:07 GMT  
		Size: 3.2 MB (3184026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d623b10a73907a1642f52fc7d5d7b3de8923d3748c7d6d974a06b1eadb768b`  
		Last Modified: Wed, 20 May 2026 01:15:08 GMT  
		Size: 12.8 MB (12828594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd6e2db2d5d8d32dacf2097157d795f305f6b48b7eeecd21f62b60269d03e82`  
		Last Modified: Wed, 20 May 2026 01:15:07 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5f263a98c1a9a5fb9aaab6184bfcd3aed47cf8252c4d9ce83d2dedec6bdfa9`  
		Last Modified: Mon, 08 Jun 2026 22:54:41 GMT  
		Size: 5.7 MB (5711957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:ba5fe37ac4a740998678a38d34fed95be0845d9a212edee130087945ecb1202f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b920f73fd0ba0d58a044f76c62ff3331aae8a82b88038663a3fa20f2fee14d5`

```dockerfile
```

-	Layers:
	-	`sha256:1a9dd090e4b290ed8e14aa5905d47dde5523e23392513a8b8f739e14e5b7e9c1`  
		Last Modified: Mon, 08 Jun 2026 22:54:41 GMT  
		Size: 2.5 MB (2528850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78e830b56dd804f8b9bb0f5bd22a7573c3883b5556bba635729507926f3d129c`  
		Last Modified: Mon, 08 Jun 2026 22:54:41 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.in-toto+json
