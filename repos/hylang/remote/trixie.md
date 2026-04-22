## `hylang:trixie`

```console
$ docker pull hylang@sha256:4449b7e170e9470a2d1be6aec7824becdfe693d1d6606437f3ee4a1947953962
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

### `hylang:trixie` - linux; amd64

```console
$ docker pull hylang@sha256:4cb61115640448441b4c1810782abda60dd3b5d0a19486c85be64a00a0e0bb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48910909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f517dc6bae27b966ffdc78dba96008e3805dfd922d1e115b097349f4c49c143`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:57:46 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:57:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:57:46 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 22 Apr 2026 01:57:46 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 22 Apr 2026 02:05:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 02:05:10 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 02:05:10 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 04:59:52 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 04:59:52 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 04:59:52 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 04:59:52 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17e4149a30c055b15a2eaa23e071079f2904cdf53ec31b9c4c2370bcdbf2a43`  
		Last Modified: Wed, 22 Apr 2026 02:05:19 GMT  
		Size: 1.3 MB (1293085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a0871a37cca1c3f458c902b0efad4f5d07ccb0ee5475e1ac446e84ecdc3e0a`  
		Last Modified: Wed, 22 Apr 2026 02:05:19 GMT  
		Size: 12.3 MB (12271728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c11793f1d65b6b29f72bea1e01fe601c36b2d234ffefffd6a66f922860d5dce`  
		Last Modified: Wed, 22 Apr 2026 02:05:19 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f8e65d2372eb87635d68d22e04e6e8aeca2f3a4c6c496e18430896caae7902`  
		Last Modified: Wed, 22 Apr 2026 04:59:58 GMT  
		Size: 5.6 MB (5565673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:b06cf4e124810b8ea02a0131af810b7abc1f972522d9c60ad210c9fbf5f22fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fcfcd3bef5657051e43cdf6fffaf6d9a92da20f7925fc73bad63eb2d75c886`

```dockerfile
```

-	Layers:
	-	`sha256:b45fe96775ca960801f8eaab9a3a370e2e93a7bbe19a5d1f351c3694fc2a4c4e`  
		Last Modified: Wed, 22 Apr 2026 04:59:58 GMT  
		Size: 2.2 MB (2156649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cad7d4cf46b127763fec9f6bef0fea072ab25d2a7582c26989011df18fd7bc46`  
		Last Modified: Wed, 22 Apr 2026 04:59:58 GMT  
		Size: 11.6 KB (11643 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:trixie` - linux; arm variant v5

```console
$ docker pull hylang@sha256:44ce02a9f0883ac1189170bb5f102db762a921b7bf1eff1b108a546da5b51432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46740443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ca2096c2ecdd3018975b2b595b0b52645627980785c2876e4a9e53a10450b5`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:32:15 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:32:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:32:15 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 22 Apr 2026 02:32:15 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 22 Apr 2026 02:42:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 02:42:38 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 02:42:38 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 04:08:36 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 04:08:36 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 04:08:36 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 04:08:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074ae5f3629a41bc6b47874d3e8592dbadf27a8ee0b66988df7ac7626ef35366`  
		Last Modified: Wed, 22 Apr 2026 02:42:46 GMT  
		Size: 1.3 MB (1276187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9648e206876af12f27fbcc3b61acf018323df2ae437e8f489208398fdc7a0504`  
		Last Modified: Wed, 22 Apr 2026 02:42:46 GMT  
		Size: 12.0 MB (11950074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be24d1aaa714b9e00e8d1ca3e6ad770342095040eefa80bad56d17f4116c817e`  
		Last Modified: Wed, 22 Apr 2026 02:42:46 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30382cb8a31717af583323390456e2efb414a023ae98c696379038ace495e036`  
		Last Modified: Wed, 22 Apr 2026 04:08:43 GMT  
		Size: 5.6 MB (5565752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:db3e66149e1ca574e83a3a70cef94597bf61a4766e66cb4f0b79e0673c2219ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2171533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6462188a379181b0a769ef3eae8726af925ebbadfed802406467d0076f69d400`

```dockerfile
```

-	Layers:
	-	`sha256:0a3db04efe774595f0c7a0c44215e160088034ce21f5188a50ea4ee34624f1b1`  
		Last Modified: Wed, 22 Apr 2026 04:08:43 GMT  
		Size: 2.2 MB (2159714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3966fbd76d4ecaf966dacc4c378779837eec6c3fa675ba2a9e91d2d75e6f6bf5`  
		Last Modified: Wed, 22 Apr 2026 04:08:43 GMT  
		Size: 11.8 KB (11819 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:trixie` - linux; arm variant v7

```console
$ docker pull hylang@sha256:36ae337108f520d564b9c6e3ba48ea9525ab4e366ae537d25af9e219848f8a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44664842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552cce3632236c566a12a2763fcfe1e84139443ff5444f3c92670c274f2303ba`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:07:18 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 03:07:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:07:18 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 22 Apr 2026 03:07:18 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 22 Apr 2026 03:18:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 03:18:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 03:18:29 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 04:16:59 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 04:16:59 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 04:16:59 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 04:16:59 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640984de0453e95f5609f023cf84287239869e6e1516c902ca0743377cd98bec`  
		Last Modified: Wed, 22 Apr 2026 03:18:36 GMT  
		Size: 1.2 MB (1249074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb21094e3e90b0461eca4b14177107a3d01eddf0c67bc12338ad7640ac33eb99`  
		Last Modified: Wed, 22 Apr 2026 03:18:36 GMT  
		Size: 11.6 MB (11634902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f06b86068eb25335052ae13b5fc105e4451d39756fea0ca557940239509b5b0`  
		Last Modified: Wed, 22 Apr 2026 03:18:36 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2670c2c6b7fb49c43906456d93e663f8a94504e0e28f4d114667729a8be7ed7`  
		Last Modified: Wed, 22 Apr 2026 04:17:06 GMT  
		Size: 5.6 MB (5565780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:2005ed70bb3cf7e8eb05b8c7689121622dfa16d631d6e1af50d226ca73869b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c7f110c3bc4f356b0be457dcd02ecbb99ed6e49218db8ca50c56c5c83088e3`

```dockerfile
```

-	Layers:
	-	`sha256:cc144ded40ad2b3cf4f2f1feb3bb1b7bf540a4935f61961a08d3b4999fbdc2ac`  
		Last Modified: Wed, 22 Apr 2026 04:17:06 GMT  
		Size: 2.2 MB (2158167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afd9909b4918b661d2f35f85851cb4832c17190ad4182cae889ea5bdf4dde9d4`  
		Last Modified: Wed, 22 Apr 2026 04:17:06 GMT  
		Size: 11.8 KB (11819 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:trixie` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:c7755dab5680475466d161c469bc287b4b08165c68b0f6a759b0310fcdc2eae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49167033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c9a06e1bd0e94cbf11a955b905c1bb2822f393ffbd45fd27b508306d4b023c`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:00:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:00:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:00:09 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 22 Apr 2026 02:00:09 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 22 Apr 2026 02:07:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 02:07:44 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 02:07:44 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 02:47:57 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 02:47:57 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 02:47:57 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 02:47:57 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30430ade496b9c0573f53017e4f2c94d902451d9e06c7f712412d5636f93633b`  
		Last Modified: Wed, 22 Apr 2026 02:07:51 GMT  
		Size: 1.3 MB (1273870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6231176d9e49373836bc61512e4592cdb01182329540647435a969f9a8a8726b`  
		Last Modified: Wed, 22 Apr 2026 02:07:52 GMT  
		Size: 12.2 MB (12183715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e2c28dc105e1d0105bb477289d6f5a96ff4183c2007f95b132e690f335be4e`  
		Last Modified: Wed, 22 Apr 2026 02:07:51 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfa4c258ac00fee142bb3ba8f58b1ec2293fa1c7af1a137a75d18e8e8840084`  
		Last Modified: Wed, 22 Apr 2026 02:48:04 GMT  
		Size: 5.6 MB (5565594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:52b5c7bc93c03acf3bd299d0ddfc47423417669dc027e345e5abd3489e51a085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c215c032451bc973792c22ddbe251d2771bbd17765d040cc04ae8eb7255dff8`

```dockerfile
```

-	Layers:
	-	`sha256:b7e866d7a593d06788bf402b63ae667364fd07c560b0c454fd33811181265fb1`  
		Last Modified: Wed, 22 Apr 2026 02:48:04 GMT  
		Size: 2.2 MB (2157059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23857096f69057514918c79a561a65edb71411c2c8526e8bea14b930571ee8d9`  
		Last Modified: Wed, 22 Apr 2026 02:48:04 GMT  
		Size: 11.9 KB (11891 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:trixie` - linux; 386

```console
$ docker pull hylang@sha256:702d2ca900fdb9e0026d31d9b4b854902a76d9ea2a03c41ce81ee0a799781868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50486476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab00cda76b5a313ccdd049a5a96d23921affb54fe80e89d27c942ef714c9811`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:57:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:57:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 01:57:14 GMT
ENV PYTHON_VERSION=3.14.3
# Tue, 07 Apr 2026 01:57:14 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Tue, 07 Apr 2026 02:14:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 07 Apr 2026 02:14:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 07 Apr 2026 02:14:40 GMT
CMD ["python3"]
# Tue, 07 Apr 2026 02:56:41 GMT
ENV HY_VERSION=1.2.0
# Tue, 07 Apr 2026 02:56:41 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 07 Apr 2026 02:56:41 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 07 Apr 2026 02:56:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3ad58e7663dac2e874d85633f012dff41d0fc985f7d40eeef495d01a4201e3`  
		Last Modified: Tue, 07 Apr 2026 02:14:47 GMT  
		Size: 1.3 MB (1297206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0272dd4cb7195931b2beb5f7d5e2da6e442a6959e5120a272961a4ab57a2a012`  
		Last Modified: Tue, 07 Apr 2026 02:14:48 GMT  
		Size: 12.4 MB (12378090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96903a511312da826b57d25e208b7d468f2e0e463902203e0ad7b039a3a56cc`  
		Last Modified: Tue, 07 Apr 2026 02:14:47 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b21a66bb9c3a8c0461220a9eaefc6db5bf6d07a0338fa77d47558747edd035`  
		Last Modified: Tue, 07 Apr 2026 02:56:48 GMT  
		Size: 5.5 MB (5519679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:37eb874ea5b3019eac780a2e82c78289777c58cca909ab26f309f7705bbd49ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099aba0371647108d7591c594585b4bfd272da8c109080b7be661440a9d85d5e`

```dockerfile
```

-	Layers:
	-	`sha256:6d1061a4f6b9862e6f8ac06da30c0340b30cd9582bad91ccfb2f1f93af8c4ca6`  
		Last Modified: Tue, 07 Apr 2026 02:56:48 GMT  
		Size: 2.2 MB (2153762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb268c2b7e1850611e07742276dc8eebce1479c69e6cb3807fa69c70eb470eec`  
		Last Modified: Tue, 07 Apr 2026 02:56:48 GMT  
		Size: 11.6 KB (11551 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:trixie` - linux; ppc64le

```console
$ docker pull hylang@sha256:62f16729938720349cd644b9feb2cbd020b331aa97aa180b1b105866c7c98dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53163949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b87ea5eea1d68e8917fc2af5538d1412acf96e07902bf66244c4bda060ff42d`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 05:15:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 05:15:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:15:24 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 22 Apr 2026 05:15:24 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 22 Apr 2026 06:01:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 06:01:54 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 06:01:54 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 11:54:15 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 11:54:15 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 11:54:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 11:54:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f111c0180379849c2242c25410e5cfba1da759760c6fd915b382423a79dfeb09`  
		Last Modified: Wed, 22 Apr 2026 05:38:44 GMT  
		Size: 1.3 MB (1320835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c290091f0c19fe00c1215f778cb3a65746a096671294db07b1c01f69d45cb1ba`  
		Last Modified: Wed, 22 Apr 2026 06:02:21 GMT  
		Size: 12.7 MB (12679120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0a482d9841e740618dd9de888a37790e6517a17a81a92bf01a02c87a8e6e97`  
		Last Modified: Wed, 22 Apr 2026 06:02:20 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ad60bf50e6a2f2215d25fac6fc8110246a4d68079fe8ea8fcc284a2db32562`  
		Last Modified: Wed, 22 Apr 2026 11:54:36 GMT  
		Size: 5.6 MB (5565713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:6ec1831144d22a45aa68743c005c2ec81ac31f3b9631fdc4553c235bc2837571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf37dd11c02dc8dafc3b0970eb4b1e07fd3f158034cfad0ab14b639b54894ae`

```dockerfile
```

-	Layers:
	-	`sha256:d9e65f04fc280359a5625dd1a39aaa33399973287b641549db67fc90206a138f`  
		Last Modified: Wed, 22 Apr 2026 11:54:36 GMT  
		Size: 2.2 MB (2160288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75c067925e690744b55a603953fba24030b7dda96f913b2d76edc02283f47fd0`  
		Last Modified: Wed, 22 Apr 2026 11:54:36 GMT  
		Size: 11.8 KB (11758 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:trixie` - linux; riscv64

```console
$ docker pull hylang@sha256:c08087edfa93d5586246d6fdd233738ed6c1ed7e6bf9b5ddf85b28f0e7035a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49983428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b4cdc0e30b8bd85e1b5205260d3f35fe7782c533c38c7869cb25a0eaa9aa70`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 11:06:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 11:06:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Sat, 11 Apr 2026 11:06:39 GMT
ENV PYTHON_VERSION=3.14.4
# Sat, 11 Apr 2026 11:06:39 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Sat, 11 Apr 2026 15:42:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Sat, 11 Apr 2026 15:42:16 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 11 Apr 2026 15:42:16 GMT
CMD ["python3"]
# Sun, 12 Apr 2026 19:25:48 GMT
ENV HY_VERSION=1.2.0
# Sun, 12 Apr 2026 19:25:48 GMT
ENV HYRULE_VERSION=1.0.1
# Sun, 12 Apr 2026 19:25:48 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 12 Apr 2026 19:25:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14380c29384b5ed760b6898c4ce267c4a4b26800f0f895ed3c6f7c1456191663`  
		Last Modified: Sat, 11 Apr 2026 12:44:35 GMT  
		Size: 3.9 MB (3873978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab86fcd37fc7b53388c4f61cd8e2c5296241a76af81a47c5b98ead3a59b1fa20`  
		Last Modified: Sat, 11 Apr 2026 15:43:24 GMT  
		Size: 12.3 MB (12287099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5efda4d64fd216bd9edbeeb4574548976089f27dae179ba84a8a3a1e35c9cd`  
		Last Modified: Sat, 11 Apr 2026 15:43:22 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7087e3f8062dbc354b2acb03623e9107fc1d541324d9ac8c8804612e89bdafa6`  
		Last Modified: Sun, 12 Apr 2026 19:26:48 GMT  
		Size: 5.5 MB (5546323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:5b65395e2deb5991e886c263aea135c06420bffe71ccbf3b56153ab1110c0f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2162417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28b7316f3c15150911b89b6d29d2c36dbc27e9e2ade086eb33f876860e74928`

```dockerfile
```

-	Layers:
	-	`sha256:11e2930fba20fde01461b788a6441ba4946ddabd43bc614c223675b809c6ec98`  
		Last Modified: Sun, 12 Apr 2026 19:26:47 GMT  
		Size: 2.2 MB (2150659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f41af991b44688bb78da9fad6946d0956f8efcb820fe2e1edd3aad7774eef020`  
		Last Modified: Sun, 12 Apr 2026 19:26:46 GMT  
		Size: 11.8 KB (11758 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:trixie` - linux; s390x

```console
$ docker pull hylang@sha256:6e1ab28200b24edf0174d6d97c49a78fc15d1f6ef05ebeacd270e25e040dc618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49029681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061c430558cb8526335f4a6fa7f3dd95e49bb82d928996e062f331474573a774`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:15:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 03:15:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:15:05 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 22 Apr 2026 03:15:05 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 22 Apr 2026 03:23:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 03:23:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 03:23:43 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 04:59:44 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 04:59:44 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 04:59:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 04:59:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6bc7e62628f7335a45c95f070ee5a190c7df1b596fb688f203a3b7338b5ef1`  
		Last Modified: Wed, 22 Apr 2026 03:23:55 GMT  
		Size: 1.3 MB (1305522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f00b726247b9a6ee09fd6c62d03e238ddcf93883da7f86ee44d6e714f6ef80`  
		Last Modified: Wed, 22 Apr 2026 03:23:55 GMT  
		Size: 12.3 MB (12318009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab809bdeda9cec490e2c34e4693fb6709b6de589734d878fb96e634b3b930e92`  
		Last Modified: Wed, 22 Apr 2026 03:23:55 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5dcd8f648be0661a48a8129e51ceff0eec302661a914b2c269b7acfe57690c`  
		Last Modified: Wed, 22 Apr 2026 04:59:57 GMT  
		Size: 5.6 MB (5565599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:f991ab9a7e93adf1e27d3c97070b54b7f4bb81c79c04e7e4a5d1210c517ad511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5168bf0e0ac0a66ccb05202c276210ee75de617b2a671b5c712f3edb02e22a`

```dockerfile
```

-	Layers:
	-	`sha256:2ccc4c05ce73880cb92ba06a819a75afa6aace6753e4906ef39eaee4e4591ea0`  
		Last Modified: Wed, 22 Apr 2026 04:59:57 GMT  
		Size: 2.2 MB (2158088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bb1b31d051463ab894b9819ba3171a1a40197f41aabefea33355845f588cc2f`  
		Last Modified: Wed, 22 Apr 2026 04:59:57 GMT  
		Size: 11.6 KB (11643 bytes)  
		MIME: application/vnd.in-toto+json
