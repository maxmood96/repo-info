## `hylang:1-python3.14-trixie`

```console
$ docker pull hylang@sha256:ecd2137e150c6f32b6dc7f57c2551d74d177c089ebced6ae68650ee04e28b77f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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

### `hylang:1-python3.14-trixie` - linux; amd64

```console
$ docker pull hylang@sha256:ff3dcf84c4318e176aa4502b9fbefa381523934507802716ec663df1aa877776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49002668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54a85f7831adad358d823a59b96db16691bbf50847ae0d3b93e5940e97701ac`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 18:52:37 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.14.0
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031242994df8c1b030b9b37cc31bed0908557209d882bc6e60afca2e0c06f617`  
		Last Modified: Tue, 21 Oct 2025 02:19:52 GMT  
		Size: 1.3 MB (1292656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c996efa345956dc673b33e4f944aa9ebecc835b085f4c7429399f2839c783be3`  
		Last Modified: Tue, 21 Oct 2025 03:39:55 GMT  
		Size: 12.2 MB (12172806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897f73a69795bec26775b3709f253a8f9cb8cba8bcf0ff7ec94fcdb5353df4d8`  
		Last Modified: Tue, 21 Oct 2025 02:20:02 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b269630efad96cceac52fb12b274a8296bfdae319b268747c970ba232476fe30`  
		Last Modified: Tue, 21 Oct 2025 05:02:40 GMT  
		Size: 5.8 MB (5759033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:5e3d6feb7fb752b638576de2bedd3e19c7321ced06f93a592990fd221fc2482b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c39c74b12e6dc9579992a993f230a50d46b8a423bfc36ff97f8df012b91d260`

```dockerfile
```

-	Layers:
	-	`sha256:a4c490713a4b276e44508d2f6a4b33a3ea16d92a3d319c298aaaac7c20c2d580`  
		Last Modified: Tue, 21 Oct 2025 11:17:24 GMT  
		Size: 2.2 MB (2157290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36bb34be113a843b8934310ccbf45ba0539f5217d4f41a4a69ffc228efb5db5c`  
		Last Modified: Tue, 21 Oct 2025 11:17:25 GMT  
		Size: 11.6 KB (11573 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-trixie` - linux; arm variant v5

```console
$ docker pull hylang@sha256:2557b42899d127c1c8eadec1c55cbedb52c4c4b5ea557d2a17c0a94ae53daf17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46833402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eaab749dd9a117a4fca9c1eb9b66e3ffeb111b072230fc791bc6bfc9cb51b23`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 18:52:37 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.14.0
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:389bac9f76fa529ccf801fd7c9cb260ecee27d208221c25004185ab22936c4d4`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 27.9 MB (27946283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6729506a6e4bceff92ab5e679e1ae287b9de0840bc02bf4552858d69fc8b5c`  
		Last Modified: Tue, 21 Oct 2025 03:01:36 GMT  
		Size: 1.3 MB (1275562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88675138991bed954d958815f141e6127f91e3ecfd612d6cebe3961bb6a9b6e2`  
		Last Modified: Tue, 21 Oct 2025 03:01:37 GMT  
		Size: 11.9 MB (11852125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630f3fd7674c9999f04002ea7aeed29b8035718d10229b03464decf7bb8afd88`  
		Last Modified: Tue, 21 Oct 2025 03:01:36 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4229a021c46401ef8ba1e4adaea93b2682e2c203d57233d908ecaf16b86f54ec`  
		Last Modified: Tue, 21 Oct 2025 04:06:16 GMT  
		Size: 5.8 MB (5759182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:4239eaa3c0f91ee32482157a0376fe88614d9362edd4d1cb4b9bb51c741b130b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e095eea90507253422dc1512970bde1670301b575886a6b636262c0cdba84ca`

```dockerfile
```

-	Layers:
	-	`sha256:c1f602272ebe1f7b57cbe2a42726816bcc181e9a7f278996a8dd31e135ac4933`  
		Last Modified: Tue, 21 Oct 2025 08:17:25 GMT  
		Size: 2.2 MB (2160355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:594853140e867ee7db2a1b46de25190d95c1612ee2a0f13cf4780553e916fed0`  
		Last Modified: Tue, 21 Oct 2025 08:17:26 GMT  
		Size: 11.8 KB (11750 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-trixie` - linux; arm variant v7

```console
$ docker pull hylang@sha256:203bb8b85ac9766215e8967993658a1f331b8b47ffd08c56bed4a58ca3bc2ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44767473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5352476798a2e6b44b0cbc03c035ffaf33052f1e2528aace4f80b7a9821f46`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 18:52:37 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.14.0
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33ab501f31070e58d316fa8c210315ff8d0bead7b959faac80c54c4cae8bf65`  
		Last Modified: Tue, 21 Oct 2025 03:38:17 GMT  
		Size: 1.2 MB (1248102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4f42d4e059599dccbbf1d214473433f4b967e5b3ab1a541276145d3c1c1623`  
		Last Modified: Tue, 21 Oct 2025 03:38:18 GMT  
		Size: 11.5 MB (11546942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de73277463deb4c08121ea9efcc4500e832d851ec813605c1d0d0eb02b43994d`  
		Last Modified: Tue, 21 Oct 2025 03:38:17 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eee03cdd792d6aafd2eefa6652e4a5bda03bb12922dd1c431391ab45fbfae9d`  
		Last Modified: Tue, 21 Oct 2025 04:35:59 GMT  
		Size: 5.8 MB (5759285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:a7084751d7afccc4e67772493dd5f1342f1793c159d8e1c09cd9ba4b478d3d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2170558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446414429d210c67d8b439a890e00055136c6b5488c4f92352991ea00ea5a08d`

```dockerfile
```

-	Layers:
	-	`sha256:12237275fd9317c0662dffc6ee4de118b547791d615101af5484577b01364e65`  
		Last Modified: Tue, 21 Oct 2025 08:17:29 GMT  
		Size: 2.2 MB (2158808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98e761cf0f68ae5f7b1ab1c01dc71b852c8cd56175a021d89c25decc229104ac`  
		Last Modified: Tue, 21 Oct 2025 08:17:30 GMT  
		Size: 11.8 KB (11750 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-trixie` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:4e23766211dcdc080765f555f72245d507d12f712e6aa58d160e9b6e754e78d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49257668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:334aa11bca5eb4ffe58fc5bc3495f5f9c9d4c103f3e4c0d3b4905a2ad5bb06fe`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 18:52:37 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.14.0
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260a013278b2d6be23f4b26dbf315eaca9ad7fd8f44ed32a0702ff789cbaf18d`  
		Last Modified: Tue, 21 Oct 2025 02:10:52 GMT  
		Size: 1.3 MB (1273085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96dc5f552c03ea58a56f42d03399a9cebc63e4a11e104816197023e8767d84b`  
		Last Modified: Tue, 21 Oct 2025 02:10:53 GMT  
		Size: 12.1 MB (12083168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e6fa5571e35404261a680a7c5f8d9c64475a979b2368855aff00b45c16f315`  
		Last Modified: Tue, 21 Oct 2025 02:10:52 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c9b5e5115f2b82eebbed8e57725e0cb8c07a8523caaa57d82b023660736750`  
		Last Modified: Tue, 21 Oct 2025 02:52:16 GMT  
		Size: 5.8 MB (5759038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:699bd6a3a3d37b904a6583d49c01d541499ea4c37893ebadf94b5691871bfda9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93438ce09686374ba88d5c15be532b8211dd1a998aae046d24fe2a966438978d`

```dockerfile
```

-	Layers:
	-	`sha256:6b83d96fbf142414883a393fd1edc50e06be698539655f123d85ff51b885eccc`  
		Last Modified: Tue, 21 Oct 2025 08:20:40 GMT  
		Size: 2.2 MB (2157700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32d82bf0bc5cf3b57a2b0b68565356eb8e1ca2828b97cbbbbc2dfac524613a0f`  
		Last Modified: Tue, 21 Oct 2025 08:20:41 GMT  
		Size: 11.8 KB (11822 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-trixie` - linux; 386

```console
$ docker pull hylang@sha256:84611895d64e883696523d87fb4cf63119439d9588c1b010a6b3cdeb684cc533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50646904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c836f343e25cb9c55bc2baab1e5b4e6acdc1ce2e50d9d462632f60914b60a15c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 18:52:37 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.14.0
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b715216cd419c547c3541ea533c3762f9c072bb2005647fa9e3cb316c52030`  
		Last Modified: Tue, 21 Oct 2025 02:11:34 GMT  
		Size: 1.3 MB (1296604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bbff1b8d1ac5af83acad992920c6a371d85b3b619820b1a2922ad78a9f64cf`  
		Last Modified: Tue, 21 Oct 2025 02:11:36 GMT  
		Size: 12.3 MB (12296217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2836b0e80218ac93a3fc0e44236f4e96233a5982a4b6a015331cf76d93479b`  
		Last Modified: Tue, 21 Oct 2025 02:11:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c3c58e2c13e80411da56d3c1efd42c939b9744ed6175284556006f86f4b147`  
		Last Modified: Tue, 21 Oct 2025 02:50:29 GMT  
		Size: 5.8 MB (5759206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:6b108fed449f0230bbede02090c55f3bc57abc0315ca50600c81d9b69451d6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143cb9262f74389f9968e787e4ec64e31e9450bdb2c21b5e6364563c2e424ee1`

```dockerfile
```

-	Layers:
	-	`sha256:6a27747c91a11877f786382ddd01072880cb0a14f15170370684ff42d5adb73a`  
		Last Modified: Tue, 21 Oct 2025 11:17:35 GMT  
		Size: 2.2 MB (2154411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8360848665fa0866a68c9fc898620aabbcbd6f7df0fc78fd7c113701044d38a2`  
		Last Modified: Tue, 21 Oct 2025 11:17:36 GMT  
		Size: 11.5 KB (11481 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-trixie` - linux; ppc64le

```console
$ docker pull hylang@sha256:7d25b8cb8388b1b87cdb8fe9b0342b6a2efe45f6c9cd59d9279d3f9e116e7c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53262376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4f5cbb1a66a8c0f52abc1e416d38753a46ad73b9b97f3d8ce8d3bad19e536c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 18:52:37 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.14.0
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5df13864257eb996eb7ecd5d52042f9612beb78124fdb6753821092c940448c`  
		Last Modified: Tue, 21 Oct 2025 10:49:16 GMT  
		Size: 1.3 MB (1320921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33976e5831e8a29ec73a170a0dcfd48f62c0d29f5ac913e088767eb729f3fc4f`  
		Last Modified: Tue, 21 Oct 2025 11:21:35 GMT  
		Size: 12.6 MB (12583413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a4e23deb3dd51e99ac0a4fd28fa41e7b83788a4f9c293fa30be48a1f2005a2`  
		Last Modified: Tue, 21 Oct 2025 11:21:33 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650ce51bf575c0dccb3e90df9e4410f635642c234203613d0385dbd8c9cba5bc`  
		Last Modified: Tue, 21 Oct 2025 21:56:53 GMT  
		Size: 5.8 MB (5759276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:5f91366f0232f23888c976438f38bebd9d5b57479e4b16fd5b2faf2aefe8c9e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f124ce4435012cf9852c89b5d866c3613adb6865864cad78663c06bab36869`

```dockerfile
```

-	Layers:
	-	`sha256:084ae8e578907dc6dcafef5ee76cacc7edd31c351ff085538234571af7f4b8f2`  
		Last Modified: Tue, 21 Oct 2025 23:17:33 GMT  
		Size: 2.2 MB (2160929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbd70deaa828acc2f8aa6dda164c5930cabcfdc6e01e408961274b11fda8a245`  
		Last Modified: Tue, 21 Oct 2025 23:17:33 GMT  
		Size: 11.7 KB (11690 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-trixie` - linux; riscv64

```console
$ docker pull hylang@sha256:bf5568a34927364302ab939b4d58b25b1c1da05ce6d3a6e4eeccc0d04ca93fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50100901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:970941906744eb71b9cc4b102f3202f991d5f11e94a0b7b2e712194894bd1ad9`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.14.0
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07881641e691ca6202df8ecc95ec2695a82945f59f23848306c6f524e1ecc797`  
		Last Modified: Wed, 08 Oct 2025 01:45:04 GMT  
		Size: 3.9 MB (3871072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9913085af2da8bd723f71a34498aca19a2f587f058b044ced4dd589cdbaf3d6`  
		Last Modified: Sat, 11 Oct 2025 00:59:02 GMT  
		Size: 12.2 MB (12194047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bad074313ed58460109420a8a2d08b15419e3621544ad9e6b7de8ea973cd87`  
		Last Modified: Sat, 11 Oct 2025 00:59:01 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3615c0661017f6c2791030dc6a426038265bded18a793ddb410137e95e8c5a0d`  
		Last Modified: Tue, 14 Oct 2025 13:25:10 GMT  
		Size: 5.8 MB (5760030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:61011b66040da84febce57addfa43eeeadfa39b8229703d191d53153d41b3470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2162990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9d5fe3f9ca1cfc2ff431b6ade69cc866b5c074775203bf5a50247427d32830`

```dockerfile
```

-	Layers:
	-	`sha256:e00c75aeb069d5f6f07f4ed3a402d2a550f52922ee9da3b99a6aa70b2cb89191`  
		Last Modified: Tue, 14 Oct 2025 14:17:42 GMT  
		Size: 2.2 MB (2151300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a39fe2cec502b9f4a3c8908b08991eedef9d98348ec1cf09c1a69bb47a39e3d`  
		Last Modified: Tue, 14 Oct 2025 14:17:43 GMT  
		Size: 11.7 KB (11690 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-trixie` - linux; s390x

```console
$ docker pull hylang@sha256:672b32cbfb0cf7c0096b0b7c380fccfdb7653018606e0af7fe4719aab4a0c953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51742831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3bcfe46e6ae882f74df7dae43d88bcfb6b666b28db510c831b475804dc03585`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.14.0
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=2299dae542d395ce3883aca00d3c910307cd68e0b2f7336098c8e7b7eee9f3e9
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7b17702cfe3c7d1897051161ba3ef82e1ffa2added4e44d0b8840676d17148`  
		Last Modified: Tue, 07 Oct 2025 20:56:23 GMT  
		Size: 3.9 MB (3906902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524ffda44eaab31211f604a51d5e5b9a87d28b8e174193a4d57d2ab1a6763762`  
		Last Modified: Thu, 09 Oct 2025 12:09:16 GMT  
		Size: 12.2 MB (12239448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e4784ff44d374d0f2556a821395f87b76f6575f5301d728b28145b9c18e7fe`  
		Last Modified: Thu, 09 Oct 2025 12:09:13 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16621680aada516856960306f2a4bd54e81d42065e26d81c2831080acbefe325`  
		Last Modified: Thu, 09 Oct 2025 18:03:10 GMT  
		Size: 5.8 MB (5759000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:a9de54211c159c45c044c86fa313df5f2d565f3f367626c0d71bbe9c1d7d570b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2170303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:327623d443b0860e7161e7b3d85d37c5669cbc5388893647939928214abceb54`

```dockerfile
```

-	Layers:
	-	`sha256:e58ea734d511c49cfc0d9fa8cd07c0d101ab5219d72b6a1f6dc04864c28a6896`  
		Last Modified: Thu, 09 Oct 2025 17:17:37 GMT  
		Size: 2.2 MB (2158729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95a2ff5deb0ff60473023ac9657742a0976466300e61541e8b429829b34ba6c3`  
		Last Modified: Thu, 09 Oct 2025 17:17:38 GMT  
		Size: 11.6 KB (11574 bytes)  
		MIME: application/vnd.in-toto+json
