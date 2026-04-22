## `hylang:1-python3.14-bookworm`

```console
$ docker pull hylang@sha256:19c310e81d74b07cf223abc569d0cb18d85f9659c195c19922ba490f6edf63cc
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
$ docker pull hylang@sha256:712841fa06667d3ad100ef69eb7cde6b62ce8b1dd8e0da903af4a33eecf2b695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50269862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5eca7fc0ab602ce356bbab4484e0821ce82bb53248305a1fb78f045f8973a9d`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:59:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:59:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:59:59 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 22 Apr 2026 01:59:59 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 22 Apr 2026 02:10:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 02:10:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 02:10:11 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 04:59:54 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 04:59:54 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 04:59:54 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 04:59:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14c00e86a4e211714ff7697df241ae8ab1fa0cf6e940b95f4e743ee8c92e3d4`  
		Last Modified: Wed, 22 Apr 2026 02:10:19 GMT  
		Size: 3.5 MB (3517898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075160da95acd271bde59ba39de1e4b424dde1a5e825ca921e739c318ca89519`  
		Last Modified: Wed, 22 Apr 2026 02:10:20 GMT  
		Size: 12.9 MB (12949830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061e7c3a5a2744785321cc3c15a0807fadb22831c1ffd02802b1d26988ed2c0a`  
		Last Modified: Wed, 22 Apr 2026 02:10:19 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33431fdf8cbd8dbcaea5c906827a705ed3c086e3358e472f286f595799d5976b`  
		Last Modified: Wed, 22 Apr 2026 05:00:01 GMT  
		Size: 5.6 MB (5565632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:87bc60f1e350875cf0acebb1878a439b64c653988e0f4d1015cc153da88952f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2541267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd0df2b2b518c3f4fd23a67b08efba41ca6275e8c26af90dccdaef53b9fed16`

```dockerfile
```

-	Layers:
	-	`sha256:71f34e4d6feb8258116c9f91c754aa3fc0be5ac8f0577bba8466f1259f1bdfd8`  
		Last Modified: Wed, 22 Apr 2026 05:00:01 GMT  
		Size: 2.5 MB (2532008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57df256280d840ad04ad8ddab68760e79888bfe86b76733f6e190a43e1bfc392`  
		Last Modified: Wed, 22 Apr 2026 05:00:01 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:d834ba48a22475c084962359cce5f7d65c86bb890a3caba1e65abb9956c91102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46895346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e58dcace7d5e6342436f0ad0c9c639177592b910ac86b2450960ce8467eacbe`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:32:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:30 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 22 Apr 2026 02:32:30 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 22 Apr 2026 02:52:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 02:52:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 02:52:52 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 04:08:41 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 04:08:41 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 04:08:41 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 04:08:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:10e5e7c244713d6618375e8360e3d0989303f5cbb40b7ea158ce628f92e32f96`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 25.8 MB (25765657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f623673f8d8ace66c5438c33d63b06c60504914003f747ec80994fbc58a70fa1`  
		Last Modified: Wed, 22 Apr 2026 02:53:00 GMT  
		Size: 3.1 MB (3092396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c3326e5d5a3b01c3a853aa2689e30be5a66189ea4aec62a36a25225d440425`  
		Last Modified: Wed, 22 Apr 2026 02:53:01 GMT  
		Size: 12.5 MB (12471257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7548b8f7808f0363a7e066f72f94229d7341c946a8eb9eab4d26b810988dde05`  
		Last Modified: Wed, 22 Apr 2026 02:53:00 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa55f72187a097ca27cd5cd168a5ce289e2f261f1239f895502bd41e6277c763`  
		Last Modified: Wed, 22 Apr 2026 04:08:49 GMT  
		Size: 5.6 MB (5565787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:1cf693b508605ceba493d615cd72bc8936dd8463a489a71ab4f266307df9b85b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc07a455beeb9ab2c201e7c3fabac56de46c0f2c5756c42564ac50500b52a6cb`

```dockerfile
```

-	Layers:
	-	`sha256:f337adaa3d355a18356b35ad86f3c570e62cc72789ec448873e610b3b0b59cfa`  
		Last Modified: Wed, 22 Apr 2026 04:08:49 GMT  
		Size: 2.5 MB (2535852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d80bcf237340512a47f030bc151f4fe1766818a0969bfdb5985a52f70f0ab82f`  
		Last Modified: Wed, 22 Apr 2026 04:08:49 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:cab7370c4040895f73802fee0930871e6484ea6172311f0badb2e51f63e8a53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44513209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7ab7262d55e7f194ce7f7e59124ac4a06d1efb43313c51bea351ce74475f37`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 03:08:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 03:08:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:08:05 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 22 Apr 2026 03:08:05 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 22 Apr 2026 03:30:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 03:30:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 03:30:41 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 04:17:27 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 04:17:27 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 04:17:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 04:17:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d3311d55816cf34cc663f098f8e93bb8dca4772ce9f25ac1e909fa7b0628d17b`  
		Last Modified: Wed, 22 Apr 2026 00:16:41 GMT  
		Size: 23.9 MB (23941424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052f61d3e205f0dddd10154790934166327508622e3bb40928643f2000867f72`  
		Last Modified: Wed, 22 Apr 2026 03:30:49 GMT  
		Size: 2.9 MB (2927258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5091a437e08a39d42fc3bd6bc668acd381cbed19d552e051081ec9f9044085e`  
		Last Modified: Wed, 22 Apr 2026 03:30:49 GMT  
		Size: 12.1 MB (12078648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8b1d937aa0111a3f956c9dca8758e41cc5037dc0989867d8d8812045e10642`  
		Last Modified: Wed, 22 Apr 2026 03:30:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bd4979e471b6ad75ce1f114a8bb76c5fa10de71c9c6e743dfcff7637ff2114`  
		Last Modified: Wed, 22 Apr 2026 04:17:34 GMT  
		Size: 5.6 MB (5565629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:bc5d90dfc573cda82c38999e40feabca2bf738143d1d3a2c5d2705ca1dd95a49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2543656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0728a540cb284346d787f6ae0fd65802d4736edb964e6c340c952fbcf10ff772`

```dockerfile
```

-	Layers:
	-	`sha256:6bba2cec1d7d2cd8e7d333e0c800b5c21c711cccd4cacc752d799be712b8dd45`  
		Last Modified: Wed, 22 Apr 2026 04:17:33 GMT  
		Size: 2.5 MB (2534285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f14a4e8314fa2a64a3ab86fa9ab21ed76e0e1932edff338edf20aadea2e1f29`  
		Last Modified: Wed, 22 Apr 2026 04:17:33 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:c5d4f4a078251b6daa62e97a9e34561ef880ae90b18b0409b0c51ecd6d8d75a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49866713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5ed446f96f605614109d29d0be2daf7421a61554c161ccc7ad70590c67d18c`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:00:48 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:00:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:00:48 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 22 Apr 2026 02:00:48 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 22 Apr 2026 02:15:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 02:15:19 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 02:15:19 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 03:23:24 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 03:23:24 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 03:23:24 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 03:23:24 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5600657b3bc30def3671cd6722abb63b0bcc6e3288143761ebe72737869609a`  
		Last Modified: Wed, 22 Apr 2026 02:15:28 GMT  
		Size: 3.4 MB (3350683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6877fa75b4d9ba184c0e5fbb3fde385b477d2a95cbd2489a245bc49179a6087f`  
		Last Modified: Wed, 22 Apr 2026 02:15:29 GMT  
		Size: 12.8 MB (12834194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6d886aa4d9c7e16c621bb67cec4a80ebf5b449016c5ed60ed8ec8a7351cd33`  
		Last Modified: Wed, 22 Apr 2026 02:15:28 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cc569167ea8b2aa906012a2499d3ea668ebf8775da6c1811e5b2833d2dba1d`  
		Last Modified: Wed, 22 Apr 2026 03:23:31 GMT  
		Size: 5.6 MB (5565473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:b579f8907b9bcc8cba0b0774f14358a2f7a4032b0563b7567ade7bc5a5416a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2541732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d469cdda416bba29ceece44e3b5db0753728d1946b03cd24de9a141f7845fc0`

```dockerfile
```

-	Layers:
	-	`sha256:d32ac415baf7c2cf5971f8e1c7998fc925ae4078396d73afaf4d914c9c9f889f`  
		Last Modified: Wed, 22 Apr 2026 03:23:31 GMT  
		Size: 2.5 MB (2532321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1eebb826b7e7a851af10ea8905422312ad1f24713c1b84d24adc23c0f2e2d86`  
		Last Modified: Wed, 22 Apr 2026 03:23:31 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:94c4906c75c02024f51189f639d459d4bcff38771b98f35719bc7f43e7b3d564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51446824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ff595de3b9e5dcaae774528429ed0af8d3d6bf293ee7e3bfbdc790fec2d679`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:57:18 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:57:18 GMT
ENV PYTHON_VERSION=3.14.3
# Tue, 07 Apr 2026 01:57:18 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Tue, 07 Apr 2026 02:08:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 07 Apr 2026 02:08:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 07 Apr 2026 02:08:59 GMT
CMD ["python3"]
# Tue, 07 Apr 2026 02:56:36 GMT
ENV HY_VERSION=1.2.0
# Tue, 07 Apr 2026 02:56:36 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 07 Apr 2026 02:56:36 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 07 Apr 2026 02:56:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2686573d3309fb5ec86398e0f20a729a351a259d4d793edf6cb41a0ef910fccb`  
		Last Modified: Tue, 07 Apr 2026 00:10:58 GMT  
		Size: 29.2 MB (29221768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95820d563ccbfc24bf3362a1129c2de1f611226b3d7f23fd19b1922f2ffc63e`  
		Last Modified: Tue, 07 Apr 2026 02:09:06 GMT  
		Size: 3.5 MB (3518017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f48292519a90ab299f7bb5fcbb6909709fabfc13c3d29884ae98def45643d8`  
		Last Modified: Tue, 07 Apr 2026 02:09:07 GMT  
		Size: 13.2 MB (13187465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af94925ee7551c2792ae0326fe88ff47428bfc1af35a9113044c8142eda4fd`  
		Last Modified: Tue, 07 Apr 2026 02:09:06 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569b3b50e98ed00912f04b75e69ed29594e6c4ccb170bf580d0687673558440e`  
		Last Modified: Tue, 07 Apr 2026 02:56:42 GMT  
		Size: 5.5 MB (5519324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:23002526439543b50e34f3bf9b1d8af486cd37548ba2b2c62c83d69dcfde7ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c23e9e6e3f7d018a38fa3c8fa4237b2854ce13fa9737daf36ed4e23b9dc5674`

```dockerfile
```

-	Layers:
	-	`sha256:7a9334cadd4073dae987374e7e3f2c482e342f7431a0cf21c5b4e555ecfc8b09`  
		Last Modified: Tue, 07 Apr 2026 02:56:42 GMT  
		Size: 2.5 MB (2529147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d81d31422662b70abbb07c17b99725a0e3789ea595062b1238574d138040e0`  
		Last Modified: Tue, 07 Apr 2026 02:56:42 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:e3a197bfc07da611eada6ee7f4e66c6d49d24dbf9bbb3b6df05a4486cf6026a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54863635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633a130f9a9ba9fe345af41edd8cc7972d5df6eb057a0e14642b96753d1636a6`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Wed, 08 Apr 2026 18:16:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 18:16:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Apr 2026 18:16:40 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 08 Apr 2026 18:16:40 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 08 Apr 2026 20:05:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Apr 2026 20:05:48 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Apr 2026 20:05:48 GMT
CMD ["python3"]
# Wed, 08 Apr 2026 21:41:59 GMT
ENV HY_VERSION=1.2.0
# Wed, 08 Apr 2026 21:41:59 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 08 Apr 2026 21:41:59 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Apr 2026 21:41:59 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33043e3548e2df86b00079fd7aaa171a58383cbfea06b509475a1f239b7fcb4`  
		Last Modified: Wed, 08 Apr 2026 18:59:29 GMT  
		Size: 3.7 MB (3722944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b628e87ca071c88e123a2c7610d87639ee61c17d49c19ac3165a143446d716f3`  
		Last Modified: Wed, 08 Apr 2026 20:06:06 GMT  
		Size: 13.5 MB (13516236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494ddcca1e3e31510fb4e38e5cd8f79aa9a86c79fcd139e527cde5cdf0c27a3e`  
		Last Modified: Wed, 08 Apr 2026 20:06:05 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3b004e2727b2dee82722797b3eabdf4cf704754808cdc2553c71727d3737f7`  
		Last Modified: Wed, 08 Apr 2026 21:42:12 GMT  
		Size: 5.5 MB (5545741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:4402f53db9510ecc88fbda22229cbb0cc9532fa926e3f514c875e4b9aaf51d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41816f5e1c6c39ccd12950da2a1a32c986d2ce4ea5d7ac62af2879b6b069b425`

```dockerfile
```

-	Layers:
	-	`sha256:6a68a055ee71cd498000be53314b31ccb9418a2ba87ba27eefa6c7b57a987467`  
		Last Modified: Wed, 08 Apr 2026 21:42:12 GMT  
		Size: 2.5 MB (2536470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6e7c0f459066b4fc258b8bea159da4be07b0c89c31c087814975c990ef09c3e`  
		Last Modified: Wed, 08 Apr 2026 21:42:12 GMT  
		Size: 9.3 KB (9327 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:2e446651aca88d3ad2a979bd3375190500670a5cb86eb1a3473aa3c5132ce229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48417803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104f5253db61789b4f134adedf4ccb443e436eaa9107b97baacce0ecffd0274b`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 03:11:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 03:11:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:11:59 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 22 Apr 2026 03:11:59 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 22 Apr 2026 03:31:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 03:31:31 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 03:31:31 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 04:59:43 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 04:59:43 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 04:59:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 04:59:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0b5b44c1974a3951c34aeaa28a07ac6a442c4d55e166cbcb2c91def4ba2dda`  
		Last Modified: Wed, 22 Apr 2026 03:26:49 GMT  
		Size: 3.2 MB (3183127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e0688c39cc1ea8a60ebeb8b5644877a26aebfd7df069edae19f594c4f2b148`  
		Last Modified: Wed, 22 Apr 2026 03:31:44 GMT  
		Size: 12.8 MB (12777143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c294eb44647b85a287890b7626e69e48165625fac07e10f303bed2ebba951`  
		Last Modified: Wed, 22 Apr 2026 03:31:43 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eaf1058a8192d2d032fb825e014a9c85b12c01edc4f9d3d7d3fb9af26055847`  
		Last Modified: Wed, 22 Apr 2026 04:59:57 GMT  
		Size: 5.6 MB (5565721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:5ed561c7d55e85bc6f7cbf2f0b6c010679259d35003478e591c8219af6d409ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecbfea8425b2354ca18c1dc815d35bbf8047c0b5fc5e9cb5ddacee573e22806a`

```dockerfile
```

-	Layers:
	-	`sha256:c5032112d36a4708532bb371c9eeabd066577218579c9b4c69af8da11d438f1d`  
		Last Modified: Wed, 22 Apr 2026 04:59:57 GMT  
		Size: 2.5 MB (2528832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfbd63f8f05f2fadb1c4806f5db7225e2664db8ed1574580aa2e848dc4eba3b`  
		Last Modified: Wed, 22 Apr 2026 04:59:57 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.in-toto+json
