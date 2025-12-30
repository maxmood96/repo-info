## `hylang:python3.14-bookworm`

```console
$ docker pull hylang@sha256:92c7f0f8d41e6d1705b710096e9ba4cf3dc6859feb062208b1c1564f0f18b5bb
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

### `hylang:python3.14-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:2f394a9715cec606024fcb566454ab031cd3f1d7b53e0517f5e578bfffd5965c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50355574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feff1e4eab104370e97bc977de727de0d51b8347bafc5e44cbc9572d211648da`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:35:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:35:05 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 30 Dec 2025 00:35:05 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Tue, 30 Dec 2025 00:45:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 30 Dec 2025 00:45:46 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 30 Dec 2025 00:45:46 GMT
CMD ["python3"]
# Tue, 30 Dec 2025 01:49:29 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 01:49:29 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 01:49:29 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 01:49:29 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6389cf4e2b13074b5a8dbebcb820766ec9f591080586fd82f430265d9fef6f5a`  
		Last Modified: Tue, 30 Dec 2025 00:46:01 GMT  
		Size: 3.5 MB (3515868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d776ce772ec902e408f4bef903f004f64eb1abd3b819346d16717fcaca8525`  
		Last Modified: Tue, 30 Dec 2025 00:46:02 GMT  
		Size: 12.9 MB (12908434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22640d12b0c43502224235d7e4b0591fde126bda4d4e446f1e6cbf44291292cf`  
		Last Modified: Tue, 30 Dec 2025 00:46:00 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e36d0c6f6f795d4fb24b7a269344eb1e1a19f89e3ec49858a18e2526cb0ee30`  
		Last Modified: Tue, 30 Dec 2025 01:49:43 GMT  
		Size: 5.7 MB (5702600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:67ff2156017e75e79e5280d9d87f46c60f177775f152a578c37aa51362005767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2541249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc3330349ff5fc0f58e98e3128e906137dbd7da50608dea013c96214591c0d2`

```dockerfile
```

-	Layers:
	-	`sha256:b539e8f0f06093823cd571d480631a0fe18b55c70f7118d8223646a5d4666696`  
		Last Modified: Tue, 30 Dec 2025 03:25:42 GMT  
		Size: 2.5 MB (2531990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:feeccc88f8fa6d17f9bbfc2786c8ed5423d93bd07e6b7ba6145d721327e558df`  
		Last Modified: Tue, 30 Dec 2025 03:25:44 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:76e53ddf64ff3fd3ddc7aea2ba46df32d43cff0761d3a6ec2d70e87de878420a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46987416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc1f9a9e5778e010075358efbff3da26cf36fe378cc5cc84a7c70fc5ce27f7f`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:45:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:45:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:45:49 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 30 Dec 2025 00:45:49 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Tue, 30 Dec 2025 01:06:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 30 Dec 2025 01:06:16 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 30 Dec 2025 01:06:16 GMT
CMD ["python3"]
# Tue, 30 Dec 2025 02:00:08 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 02:00:08 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 02:00:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 02:00:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:cdd01b66e4b6599d6f59fe75d883783e8ddfc67db8fda967c6ce250da575cc0b`  
		Last Modified: Mon, 29 Dec 2025 22:25:33 GMT  
		Size: 25.8 MB (25757576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adaad57750f854d1b54e59660abfd7476c3b4dbda515c63393813c20b3e4d4a8`  
		Last Modified: Tue, 30 Dec 2025 01:06:29 GMT  
		Size: 3.1 MB (3090736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815395b7987cbfff9020ac89412ebe4566ab8a5c18fb28370ff024e7531c8f4f`  
		Last Modified: Tue, 30 Dec 2025 01:06:30 GMT  
		Size: 12.4 MB (12436107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e64254dc2d6b0e08dc7804737a20af494f165c97e4f779a92e9ca1982079240`  
		Last Modified: Tue, 30 Dec 2025 01:06:29 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ed91337782cb4da154a52d82dad9aad8b5afef532c4a17fe40af60b7497b54`  
		Last Modified: Tue, 30 Dec 2025 02:00:22 GMT  
		Size: 5.7 MB (5702748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:4e872c9389dc363ea159207ec36866f824f19edb4816a841db2509be0cc12d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6672f5cbc8f75f1c484bf00a1045cc03c3e282f33e7d98dc49ed5746013ca4`

```dockerfile
```

-	Layers:
	-	`sha256:5a75d17b89734e76bc0c531b1d953e9172dcfebf20ac065b3d5ac091b9ac00cd`  
		Last Modified: Tue, 30 Dec 2025 03:18:30 GMT  
		Size: 2.5 MB (2535834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ea4300e47195137704cb6bee8e25b2c238317f9c78e9fc65dbf5e2ae3a61f2`  
		Last Modified: Tue, 30 Dec 2025 03:18:31 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:73f6076c15a692b07c0c654691aa72778050f0f90f370e70f2ea767889e6f26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44600611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa610bc53d3cd4093cc3450f68c78502ca31d4105270aa7d5efb45dd69ccecc`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:23:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:23:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:23:26 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 30 Dec 2025 01:23:26 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Tue, 30 Dec 2025 01:43:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 30 Dec 2025 01:43:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 30 Dec 2025 01:43:23 GMT
CMD ["python3"]
# Tue, 30 Dec 2025 02:43:37 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 02:43:37 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 02:43:37 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 02:43:37 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16048c195a059d6dd298f984dde341773cd8ba7dee9549be607542fdce32c64`  
		Last Modified: Tue, 30 Dec 2025 01:43:36 GMT  
		Size: 2.9 MB (2925452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663252da00508d3c372891943c2bad624d6f831747aed468c1254003f3b125b7`  
		Last Modified: Tue, 30 Dec 2025 01:43:36 GMT  
		Size: 12.0 MB (12038381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899a80118b40608a084b1bc701fd70578684d274f2ebf4502445eee8de3b1070`  
		Last Modified: Tue, 30 Dec 2025 01:43:35 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ba281e09cac22fd4b58fdc1060b0503a79548813b5630aa179abf4c181b0cb`  
		Last Modified: Tue, 30 Dec 2025 02:43:50 GMT  
		Size: 5.7 MB (5702475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:55c15b697c462f0d15bb7758bc79b1e39ed9b766ba75004c964308ff70ac6e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2543638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84275e7a205cb8965b813ef0271ce083cffe1593a0def676d5ae02950e277d9`

```dockerfile
```

-	Layers:
	-	`sha256:be9433799850227e95898cef6e07f1deacd504935c008a45a43d5f023087a1da`  
		Last Modified: Tue, 30 Dec 2025 03:23:25 GMT  
		Size: 2.5 MB (2534267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e8595bac82c70363523f40d372d71ef25059a4f97d0f7fb6e76157728bfb5d8`  
		Last Modified: Tue, 30 Dec 2025 03:23:25 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:ccadb7003b030c556ebd21916abad418a5294328f6499422c64b03b649d4a426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49951315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b82ceb7fbb55494626a90967e12f6e199bfb777db87613faec0242667bf0da`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:37:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:37:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:37:07 GMT
ENV PYTHON_VERSION=3.14.2
# Mon, 08 Dec 2025 23:37:07 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Mon, 08 Dec 2025 23:50:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 23:50:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 23:50:47 GMT
CMD ["python3"]
# Tue, 09 Dec 2025 00:56:07 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 00:56:07 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 00:56:07 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Dec 2025 00:56:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab3e36ae108c9011b071d086181e64a00ea765b99aa1543205a989723b413f5`  
		Last Modified: Mon, 08 Dec 2025 23:51:00 GMT  
		Size: 3.3 MB (3349148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511187c9a052e1924af43624150c8055a4ee2946debb8d89eddf3c5db8188b93`  
		Last Modified: Mon, 08 Dec 2025 23:51:02 GMT  
		Size: 12.8 MB (12797115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c982ded6e9b81190665adeba3a25c57ac065f695ec3c8f606673b361200ca50`  
		Last Modified: Mon, 08 Dec 2025 23:51:00 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841c2da6aecb21b024191ceaa147e248198799c105d7aa47b7b009b584da3248`  
		Last Modified: Tue, 09 Dec 2025 00:56:18 GMT  
		Size: 5.7 MB (5702568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:2f3db04c7c5bf92600d29dcdd0ef76caa158ccf035d075407fa11b673fcc9ffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2541712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e02b2742bb1330f17bfa07e1f2b80a2ac18f006fc1addd63b0cfe42695d0500`

```dockerfile
```

-	Layers:
	-	`sha256:901d28f606eff8c8c2db2e78dec873c4c05e27b16c0cf17a21df843297508ecb`  
		Last Modified: Tue, 09 Dec 2025 03:19:33 GMT  
		Size: 2.5 MB (2532303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1860fed34178cf04ec257b8f066ed41ec1bef223b483e4b21818c89558fc368`  
		Last Modified: Tue, 09 Dec 2025 03:19:33 GMT  
		Size: 9.4 KB (9409 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:88b99b56539c577dfd5c6a2ce4bd59fee5df2c1fb3a6493ac153196ba8940f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51608232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afae974aa179d25e512b54101847621a0f278c138d7585e6efe02ad7359b29b7`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:59:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:59:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:59:33 GMT
ENV PYTHON_VERSION=3.14.2
# Mon, 29 Dec 2025 23:59:33 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Tue, 30 Dec 2025 00:11:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 30 Dec 2025 00:11:38 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 30 Dec 2025 00:11:38 GMT
CMD ["python3"]
# Tue, 30 Dec 2025 01:06:30 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 01:06:30 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 01:06:30 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 01:06:30 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8088bca50f9b26a02f41f2bd4e6b472988face7fad2a2b3eee7b94f77eb1461f`  
		Last Modified: Tue, 30 Dec 2025 00:11:51 GMT  
		Size: 3.5 MB (3516541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aedfa913633f74755f6af33562175e16a342ef1fcbc8ccafd848aa57026406d`  
		Last Modified: Tue, 30 Dec 2025 00:11:52 GMT  
		Size: 13.2 MB (13179249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d1753a0b4e81b68db9c0856ab1a9b7236440c36a0348aff1630b86b436e5a0`  
		Last Modified: Tue, 30 Dec 2025 00:11:51 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7983eaf543c5a72adb6596a276752462195006c1a221bcb81097b1d53c454e76`  
		Last Modified: Tue, 30 Dec 2025 01:06:43 GMT  
		Size: 5.7 MB (5702420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:56edd0b5a713d4e0857699e2a533e6e74dd9adb48301c5adefd113fc15066829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb6c72a462fb072227e2428b7b1dfde153549cba573b266099944c2d68be425`

```dockerfile
```

-	Layers:
	-	`sha256:ca16e4761086cd3236c461678bfc9e80731034643f66e1d12b85509368089983`  
		Last Modified: Tue, 30 Dec 2025 03:18:45 GMT  
		Size: 2.5 MB (2529137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bb402fc81d063f143a7d4f7fc542df8193e683da662a920b219d0e52f5f499e`  
		Last Modified: Tue, 30 Dec 2025 03:18:46 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:261286efd2e0ffd265f773d2f85bba0ab8c65bcb592d2d383415fe1472137b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (54961586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7775229ab32752fc61145a1928117ee9954d97d630479039dd8a9b52162901eb`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 14:59:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 14:59:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 14:59:47 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 09 Dec 2025 14:59:47 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Tue, 09 Dec 2025 15:22:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 09 Dec 2025 15:22:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 09 Dec 2025 15:22:53 GMT
CMD ["python3"]
# Tue, 09 Dec 2025 17:06:46 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 17:06:46 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 17:06:46 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Dec 2025 17:06:46 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01aa8ea3b9e18c2505b5d96e87828ce96346dc10021eeba1c1791ffc0ac2002`  
		Last Modified: Tue, 09 Dec 2025 15:23:16 GMT  
		Size: 3.7 MB (3721200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c197284ea6f73e860fbb7b5e3e4fa452838baaa489cacbdf55d141cf9053cf12`  
		Last Modified: Tue, 09 Dec 2025 15:23:16 GMT  
		Size: 13.5 MB (13468463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5311febf5241e2ef5638d20d19c7f07a746fe7274fdbc652e5775c8aef8c41f0`  
		Last Modified: Tue, 09 Dec 2025 15:23:15 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e54c89be1e1600b80e161d5f68675bc15da7f77df007e149a84cb5f107e7c0b`  
		Last Modified: Tue, 09 Dec 2025 17:07:22 GMT  
		Size: 5.7 MB (5702828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:a5e3d3ac8262e5b709d531b9a1250f13bf04afbbd99ce99f63f0a6ba03005b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0bb0808a67a8a9dbb133debc510b6f293732b10d626d9b2c231b41a1bef3e1e`

```dockerfile
```

-	Layers:
	-	`sha256:ee85390571990ce1017dc53a8355428404fb7ea6f9054dfd5269c7e00f55a834`  
		Last Modified: Tue, 09 Dec 2025 18:17:44 GMT  
		Size: 2.5 MB (2536452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:924db494305ffa775609682d7c5f42da896f14f5c6a5f0720f76fcb3ec491052`  
		Last Modified: Tue, 09 Dec 2025 18:17:45 GMT  
		Size: 9.3 KB (9327 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:bd537cea9d693ede9ffa5a61a5e1e6434a683a1dfcff4d11be85bedc5e1619f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48507481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174c638d080ca55fb19c2c68bc401c8ae05b8798cab17ae57a328158308a32e6`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:18:10 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:18:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:18:10 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 30 Dec 2025 01:18:10 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Tue, 30 Dec 2025 01:31:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 30 Dec 2025 01:31:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 30 Dec 2025 01:31:34 GMT
CMD ["python3"]
# Tue, 30 Dec 2025 03:03:11 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 03:03:11 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 03:03:11 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 03:03:11 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865980def2e56282fb4b70aea55c2650827b05ae0031b83884bbc3fd76dacb05`  
		Last Modified: Tue, 30 Dec 2025 01:31:51 GMT  
		Size: 3.2 MB (3181818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3a6adc1f4c8c3e5a59ff20feee0f51b326ef9dfb4e2fef9c3087baebdef35f`  
		Last Modified: Tue, 30 Dec 2025 01:31:52 GMT  
		Size: 12.7 MB (12739119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923c916e245a84ee2e363537e1f91787e045c2a52160239d1a842357072612a5`  
		Last Modified: Tue, 30 Dec 2025 01:31:51 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346229816058d36fd61e3397a9d47d3e1d9ee7ba324cfa4649c05da953db901f`  
		Last Modified: Tue, 30 Dec 2025 03:03:25 GMT  
		Size: 5.7 MB (5701897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:c5f15262f0f8df9e71aaaa58da989b917f55d99cbd0554f27773bb47b8ac5119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0479cacdcc2d85aa7f5581b574c0ab04e4b3abdc6cff071697ff23f0b1b73f27`

```dockerfile
```

-	Layers:
	-	`sha256:d9495dd517b35fe5ceca424babdcc547fda7ed23792484cf8e8b78aad0a9806e`  
		Last Modified: Tue, 30 Dec 2025 03:23:37 GMT  
		Size: 2.5 MB (2528814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efb0fc9dfea5271e6548a9defaa5fc44769bad58af1aad765ae5415e50a359e9`  
		Last Modified: Tue, 30 Dec 2025 03:23:38 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.in-toto+json
