## `hylang:python3.15-rc-bookworm`

```console
$ docker pull hylang@sha256:d8d45ebe6cd94f4c9e3793e2851b0a1c0e6f7c94c13634a6df09e589b8ab08e7
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

### `hylang:python3.15-rc-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:abd09b2375a06f1f281dec8e775a3f208ccb1f5c52d8742f76a3c0479a9ed536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51168255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b3cca5c233b184377022b6bfebc96a6ec9cd08c4db8d723135a50f775284f4f`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Wed, 03 Jun 2026 18:17:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jun 2026 18:17:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jun 2026 18:17:34 GMT
ENV PYTHON_VERSION=3.15.0b2
# Wed, 03 Jun 2026 18:17:34 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Wed, 03 Jun 2026 18:29:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Jun 2026 18:29:54 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Jun 2026 18:29:54 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:44:16 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:44:16 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:44:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:44:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4979aa5258e9f5166ae072cdff0b41f3320aeff0a7be980c8cef66df000c4d49`  
		Last Modified: Wed, 03 Jun 2026 18:30:02 GMT  
		Size: 3.5 MB (3519905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f2c08352ea9c4e7aa5ce97bef3f4cea3ede745149bab864baa44db8c64e50c`  
		Last Modified: Wed, 03 Jun 2026 18:30:02 GMT  
		Size: 13.6 MB (13570089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba06653ab655fa3222eae71ac608523182f90c2f41b6786ad0504b7ae11220e`  
		Last Modified: Wed, 03 Jun 2026 18:30:02 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4dd6be19083a8b26331eeddfa2656330d0ed550982fc7fd5903c9838442a197`  
		Last Modified: Mon, 08 Jun 2026 22:44:23 GMT  
		Size: 5.8 MB (5844469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:2411041bf3c25a2906d529e5e0e83af065bf8ba17995a984449750d62f7c2804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c4913e3e7954e1d0265e53b96304afc41926fd5af60db55496d5d858929c32`

```dockerfile
```

-	Layers:
	-	`sha256:606e02dd88abb9a09ca582eca10cc1462790e1498da64779f8528504923a4a04`  
		Last Modified: Mon, 08 Jun 2026 22:44:23 GMT  
		Size: 2.5 MB (2530822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aada91e3dba25f44e0129158911d444565ff47b197e942ee6e761ac186804d7`  
		Last Modified: Mon, 08 Jun 2026 22:44:23 GMT  
		Size: 8.1 KB (8066 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:e1126b55e4c0d0e777ac8e982dc6efd26c608a53eabcaece72055d6438e7ce10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47827693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a94a2bbbf47a919656f21a2c95617b03f12188fc9d7ec5e0a0f792545ebf4d2`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1779062400'
# Wed, 03 Jun 2026 18:19:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jun 2026 18:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jun 2026 18:19:08 GMT
ENV PYTHON_VERSION=3.15.0b2
# Wed, 03 Jun 2026 18:19:08 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Wed, 03 Jun 2026 18:40:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Jun 2026 18:40:21 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Jun 2026 18:40:21 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:46:00 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:46:00 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:46:00 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:46:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3e5afa2eeb01167c187727ebcf5bb90554d4e6dd21fe61f1f694b128ceb15ac1`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 25.8 MB (25768291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f782093446a02fa0dd2bc50025491af4f79102e41d4dd80773f239583e60d89e`  
		Last Modified: Wed, 03 Jun 2026 18:40:29 GMT  
		Size: 3.1 MB (3093157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa0f658d7ca34fe5e9555e694da60eef33c029d827b284cd71e95878fcaead7`  
		Last Modified: Wed, 03 Jun 2026 18:40:29 GMT  
		Size: 13.1 MB (13121506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4323a966c38f90189e4aee4be0a60317685fa063053316455d7537edab963b`  
		Last Modified: Wed, 03 Jun 2026 18:40:29 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741297e076702eeeb7c04ef7e9f2d86eaffb87b16e0a44cece7f85dcd9af1191`  
		Last Modified: Mon, 08 Jun 2026 22:46:08 GMT  
		Size: 5.8 MB (5844489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:8907d8d6ea0ac49eafdfdccf212da5ab81d9af3ee29313bea7e52ff0ccd636a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf63bfefe7a3c005444144503581d8426e7607144025e46066bbe5ca6024e0d`

```dockerfile
```

-	Layers:
	-	`sha256:81be2044d925fc4cd01ca6c96de835092153615f04733aa23eeaac836d1feb05`  
		Last Modified: Mon, 08 Jun 2026 22:46:07 GMT  
		Size: 2.5 MB (2534634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4015f4b78761deb37522276f0cb18db5026948aa8da18b3980c95edce5672512`  
		Last Modified: Mon, 08 Jun 2026 22:46:07 GMT  
		Size: 8.1 KB (8146 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:a667d07d6b4e91d8682c5810acd9467798bae38565a4bb9f61bd00ee984ee7bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45672861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975a2479f8ad4922857e2225c131dd8744c78073ea13d3373de99322b0a9dde6`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 03 Jun 2026 18:17:50 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jun 2026 18:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jun 2026 18:17:50 GMT
ENV PYTHON_VERSION=3.15.0b2
# Wed, 03 Jun 2026 18:17:50 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Wed, 03 Jun 2026 18:41:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Jun 2026 18:41:36 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Jun 2026 18:41:36 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:45:24 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:45:24 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:45:24 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:45:24 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:af86988b12731b7fa2ac73fa1c3f6ab4510a6641d04afb18df09600383bc399d`  
		Last Modified: Tue, 19 May 2026 22:36:05 GMT  
		Size: 23.9 MB (23941643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d651d85028456ce517fb991d77e9777e60648cb7b85494a07baaca3026b79e`  
		Last Modified: Wed, 03 Jun 2026 18:41:44 GMT  
		Size: 2.9 MB (2928551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff73552cdfc04b69da7a58271f18b516e3088a9421b49633138bf59e91f48d81`  
		Last Modified: Wed, 03 Jun 2026 18:41:45 GMT  
		Size: 13.0 MB (12957918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ef5f969362d191a0a6ab8380dc9b3700a8c1de0fc8eaa333cc381dcf0f1234`  
		Last Modified: Wed, 03 Jun 2026 18:41:44 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ae18cbc0ae877c2a65167b47abc1cd52d8d57f8906fcd708b641729f3764bc`  
		Last Modified: Mon, 08 Jun 2026 22:45:32 GMT  
		Size: 5.8 MB (5844499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:7aa1f7045e6dc9b35284f834dc86ab165e3c44e59f4d1aa30dd13a24a332e178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2541212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8a836e5ee2e3626ff59e3a646f7d910fa595684223380f18e0b4ff00cf0c8b`

```dockerfile
```

-	Layers:
	-	`sha256:385898da1d25bfb308282ad941b51f9e28a4101ec59010ab7561bc6e2c6b5f5e`  
		Last Modified: Mon, 08 Jun 2026 22:45:31 GMT  
		Size: 2.5 MB (2533067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5b39ff57972ab1e3c84343e93d6f714a629093e5568cbcdeceb39ddf66c0bb6`  
		Last Modified: Mon, 08 Jun 2026 22:45:31 GMT  
		Size: 8.1 KB (8145 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:4e6e55091c4206274a63ffb8753dffd57a6d335549532823c03d329e13239b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50770394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3302c12805fc4850e265332c296c9d394cc70bd84bed26f0351a226da794f1`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 03 Jun 2026 18:17:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jun 2026 18:17:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jun 2026 18:17:41 GMT
ENV PYTHON_VERSION=3.15.0b2
# Wed, 03 Jun 2026 18:17:41 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Wed, 03 Jun 2026 18:32:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Jun 2026 18:32:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Jun 2026 18:32:47 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:44:22 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:44:22 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:44:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:44:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd498dec2cd85524e642fab86f90026725c0ac6b2092f3f64d3219d0ad4f87a`  
		Last Modified: Wed, 03 Jun 2026 18:32:56 GMT  
		Size: 3.4 MB (3351875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23caca7eeb8bc4639584497a94670f32d207027bdca42f49ab857ed9a7464271`  
		Last Modified: Wed, 03 Jun 2026 18:32:56 GMT  
		Size: 13.5 MB (13458752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c790a7d0380ba6e1f25f9862e3d1d81e36db5a5b357cea4ae5ebabf0f64eb8e`  
		Last Modified: Wed, 03 Jun 2026 18:32:56 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658d9ddaf84e81078f49c8893140df03308e9dea922ec4a70746f31150f3ec9b`  
		Last Modified: Mon, 08 Jun 2026 22:44:29 GMT  
		Size: 5.8 MB (5844473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:f5f6d0518caf42e66884384a373b1ff087966f071e6c249cc4a8ed73dfd2c75b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2539257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49bb62b93cf222045a4489c597c91ee1d7951dee8162061e4da3ba7346714a1`

```dockerfile
```

-	Layers:
	-	`sha256:b95f259eeb9207e27c710034d85f13648849b043fbebd4bb4de89bd9eb1d005e`  
		Last Modified: Mon, 08 Jun 2026 22:44:29 GMT  
		Size: 2.5 MB (2531087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b192bb96b1e901ef24f8c8371e107f319b522b9e158e75499567ea3deadac9a3`  
		Last Modified: Mon, 08 Jun 2026 22:44:29 GMT  
		Size: 8.2 KB (8170 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:8a53f341295cc5809dc7634e33ec384e4024790bb84eb2fd441311e00de50d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52203853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e8ef1f753d7156480a7d7c7e6daa6095b7ee6bff3efc17d9918c8837867cd4`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Wed, 03 Jun 2026 18:18:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jun 2026 18:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jun 2026 18:18:09 GMT
ENV PYTHON_VERSION=3.15.0b2
# Wed, 03 Jun 2026 18:18:09 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Wed, 03 Jun 2026 18:32:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Jun 2026 18:32:03 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Jun 2026 18:32:03 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:45:06 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:45:06 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:45:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:45:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:408fe432485bb366e9a4871b553de2e6347ca580fe8a5d45c84c87fa58d5e5c7`  
		Last Modified: Tue, 19 May 2026 22:37:12 GMT  
		Size: 29.2 MB (29218601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47259d1b1730e7c58c41d6e54e9ee5f658f11d7ac10d60272e37e614a986645`  
		Last Modified: Wed, 03 Jun 2026 18:32:12 GMT  
		Size: 3.5 MB (3520868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e97976452d718ecb433fb899599a21b36e3ddf152e42e7b0e320da91c7fd6f9`  
		Last Modified: Wed, 03 Jun 2026 18:32:12 GMT  
		Size: 13.6 MB (13619627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123062a9011989eb9687991d4731109853da9588b849d50e6f07195ba0db4004`  
		Last Modified: Wed, 03 Jun 2026 18:32:11 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffbb18b8ba4657590319330fed96ded5d859b172aca62a93133e1e1aa9a879c`  
		Last Modified: Mon, 08 Jun 2026 22:45:13 GMT  
		Size: 5.8 MB (5844507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:652d29a7a52e61e417db895efc441aff50c4a2daf4c76d48354ed0d6022e6318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2536023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3baebaf71cc56c6521b1d3413bdb21877084de796b63520a5497633181395de5`

```dockerfile
```

-	Layers:
	-	`sha256:b699f7ab69ee809ad3be285171e41ed838a03c3d62b55c5435a2f4795fc17bfa`  
		Last Modified: Mon, 08 Jun 2026 22:45:12 GMT  
		Size: 2.5 MB (2527989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82ca40a2f0483756834e4e17ba9cb6d0d1cb389b8e6277e004f09f6710cee8bf`  
		Last Modified: Mon, 08 Jun 2026 22:45:12 GMT  
		Size: 8.0 KB (8034 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:bc71e53a962c597d23c6aabec4e33f08756ad536a8d7d10d4afc04f4df3a129b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55777143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6aad24a76da29f7063cf7e09832edc6128f39e894028e12b3a093ac07d946d`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 03 Jun 2026 18:38:58 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jun 2026 18:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jun 2026 18:38:58 GMT
ENV PYTHON_VERSION=3.15.0b2
# Wed, 03 Jun 2026 18:38:58 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Wed, 03 Jun 2026 19:23:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Jun 2026 19:23:35 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Jun 2026 19:23:35 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 23:12:43 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 23:12:43 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 23:12:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 23:12:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1dd21d9872001ffd295d89cef45026c050b438b8e750d23a2734675d981540`  
		Last Modified: Wed, 03 Jun 2026 19:23:56 GMT  
		Size: 3.7 MB (3725062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37217f6f3f45b06ec7e149b86de2e37335b4901c69e6d89251d112b110ad2c58`  
		Last Modified: Wed, 03 Jun 2026 19:23:56 GMT  
		Size: 14.1 MB (14131381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbdfd18468fe7c814226ed6f6cc47884f523960a36b8aa2b841e9f650f11984`  
		Last Modified: Wed, 03 Jun 2026 19:23:56 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d5697b4b1783b069f354d8daebebd772795555344891782515ee9f5c8f4f6c`  
		Last Modified: Mon, 08 Jun 2026 23:12:59 GMT  
		Size: 5.8 MB (5844708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:0ed2b06da48ba41b591e2569231eceebe60e59f4a7907c3f9126b8dd5a05d49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2543370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d94fab1e955ebe55815b02bdf4218007b7b67f4f3aa632267cbc27e9458a2e0`

```dockerfile
```

-	Layers:
	-	`sha256:d5c7a11f7dd98c3c0003e54193fc4003087428541c42bc870f512f092990f458`  
		Last Modified: Mon, 08 Jun 2026 23:12:59 GMT  
		Size: 2.5 MB (2535260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ddc0962b68e34c5b5ced49cce9e0df728106f13650582180e08ea6b831708e1`  
		Last Modified: Mon, 08 Jun 2026 23:12:58 GMT  
		Size: 8.1 KB (8110 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:9c9c751b91ce9793f1e507a31eed190f71b9c812300f0b5ac44153d7e7a87509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49341195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb39139c8dbea1a32148e7e3dcedd05702a3236b27f2eff964dc226fca35c759`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 03 Jun 2026 18:13:42 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jun 2026 18:13:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jun 2026 18:13:42 GMT
ENV PYTHON_VERSION=3.15.0b2
# Wed, 03 Jun 2026 18:13:42 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Wed, 03 Jun 2026 18:30:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Jun 2026 18:30:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Jun 2026 18:30:43 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:53:36 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:53:36 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:53:36 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:53:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1ec5aa309d8fd4d7322e605de2644ebe3c01efde3b8ebd24ec74122366ec63`  
		Last Modified: Wed, 03 Jun 2026 18:30:56 GMT  
		Size: 3.2 MB (3184020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6a5ec0c7e7aa8b66ee8cff8cd721882d7e585d1142a7ba49df8a9dd929a0de`  
		Last Modified: Wed, 03 Jun 2026 18:30:56 GMT  
		Size: 13.4 MB (13423911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b05ff1c5d95e972c891fd93ec585b05b5c5e6475966996e4e095a0971698fe3`  
		Last Modified: Wed, 03 Jun 2026 18:30:56 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e70500b66cdc6c5cd56c9ee5196501a263bc5bfa03ed68867b01d5448a1b974`  
		Last Modified: Mon, 08 Jun 2026 22:53:49 GMT  
		Size: 5.8 MB (5844417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:8105917a056929342c598cfa568535c84f27081f0feb3e6c3eee806724ca6102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2535712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d1808827a833c4637f4178c341426a70152598f4a557bbafb4605b3b5809f50`

```dockerfile
```

-	Layers:
	-	`sha256:3e3bf7486243d9afd6630b142bc059d47a35f45f468d1ac9d78a50e4d014d02d`  
		Last Modified: Mon, 08 Jun 2026 22:53:49 GMT  
		Size: 2.5 MB (2527646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb2ad699809ce2c148bd7b49277a9926bee8430d9016b1aa27a907d96cec5ba7`  
		Last Modified: Mon, 08 Jun 2026 22:53:49 GMT  
		Size: 8.1 KB (8066 bytes)  
		MIME: application/vnd.in-toto+json
