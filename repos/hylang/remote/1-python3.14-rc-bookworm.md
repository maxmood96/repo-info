## `hylang:1-python3.14-rc-bookworm`

```console
$ docker pull hylang@sha256:a647e6ce820a31b3b9bb720093eec670b3846c0f1af73f4f0066af349d3eff59
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
$ docker pull hylang@sha256:cd5e259e758840e65cfcdcdb4088beae09e7083a81973116a7cf1760d05bd437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50322032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819471d9382e2748be483a57abdd21eac009f1755a1e2c8346a381a636b59b4a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cd6339033426e47bc6332a54a0d309b63da52dec313ee0c74edaba0a256ab1`  
		Last Modified: Thu, 18 Sep 2025 20:25:23 GMT  
		Size: 3.5 MB (3515831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5136a46e30721dca5fb5cd72701d475fcba19fbb2ceb20f12bdaa09e12a73747`  
		Last Modified: Thu, 18 Sep 2025 20:25:27 GMT  
		Size: 12.8 MB (12823795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d202594199c4baa9e7a1e70222cc55a7d1dca1195ec2e56befd21bf6cab4783`  
		Last Modified: Thu, 18 Sep 2025 20:25:23 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ae4b3ad37ced4228b9ce2dbc133a897123cc869eca617bd84199dbb9d39c39`  
		Last Modified: Thu, 18 Sep 2025 21:11:58 GMT  
		Size: 5.8 MB (5753811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:8c1ee615f29eaf7ad0670b9dd1ab5ef1b3cb5f2069f92def7d52b25ccb5a30d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85de910dcf5faa6170a2793046c3afb5176937ef00350cb2f4808d3ddf3db389`

```dockerfile
```

-	Layers:
	-	`sha256:8ba2a9545d9c866e3bc3bf6b6089c90efe5dbefbe66f40eb248a4c2e67865de7`  
		Last Modified: Thu, 18 Sep 2025 23:18:25 GMT  
		Size: 2.5 MB (2532801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68a2e9569b2ece4986be635ab9674bc3e67b2e96a57d57362287092ad6171e40`  
		Last Modified: Thu, 18 Sep 2025 23:18:26 GMT  
		Size: 9.3 KB (9274 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:0ad05648aec53e64861c3f2d00393cc1be6576c0c6834aa9d0a6238d4f2516e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46963198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a48c0a68610ec9d91801d5b4530eaffcb7390035d3620f6329ecb092e8e146`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1757289600'
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
	-	`sha256:952ba1cf349522edb7270da2ee606695f7a7b47b332674ee825bd31cd9ffac57`  
		Last Modified: Mon, 08 Sep 2025 21:17:19 GMT  
		Size: 25.8 MB (25757446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bf51d497b533ca42ddc44b3afd0622a78eddb96c197a9d2f52184b5536e059`  
		Last Modified: Thu, 18 Sep 2025 20:33:16 GMT  
		Size: 3.1 MB (3090734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a60d27213dea7fda0c622d9055cb3d806ff5012cda52a55d452bbd7dcd5657`  
		Last Modified: Thu, 18 Sep 2025 20:33:27 GMT  
		Size: 12.4 MB (12360967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c260efe1cd2f6403e8d327a78088cfb13f3304e3ba51d3e87db7c31188526b`  
		Last Modified: Thu, 18 Sep 2025 20:33:16 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708cb6c905792d0aa6a1684724cbc4842594aac2916d29b6a42d26a7f5697281`  
		Last Modified: Thu, 18 Sep 2025 21:12:19 GMT  
		Size: 5.8 MB (5753800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:86f645e8bbd2ebdbb10829d8d23e033a50d578796c4a0b164f2f6d6b54da3e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2546030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15ca663dfd24a4441857c713c644ea146a41559e08e8d8ddbe23cd2a92322b9`

```dockerfile
```

-	Layers:
	-	`sha256:a935932ff13771d060aa9ecd592cc8c05041f26007aefd60fd30e7591e1c4739`  
		Last Modified: Thu, 18 Sep 2025 23:18:30 GMT  
		Size: 2.5 MB (2536645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67fcb0a98c7d233e79c72c62e07215871c8061d776cd38d5b20c8e2f343474fb`  
		Last Modified: Thu, 18 Sep 2025 23:18:31 GMT  
		Size: 9.4 KB (9385 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:31dcdc6bb73a2f34bad985b58514ce78aa52e5cdb1df05eca14c2bc743e77e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44582461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01491e3c24a37089a7a0007709ba79ecda207298cf25aac6a8ccc4a960c5c64`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
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
	-	`sha256:e747f8ef7f1d9a41c99bfb53889f7b8de3504300740a326627fc7522904708cc`  
		Last Modified: Mon, 08 Sep 2025 21:14:21 GMT  
		Size: 23.9 MB (23933904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73ec82e523485a51ff73db97ad1228dc0d7dace01c77703d521fdb05ed212d8`  
		Last Modified: Thu, 18 Sep 2025 20:33:59 GMT  
		Size: 2.9 MB (2925482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd73ff7e408ae82129b0e996f8471ca868eb82ce4c8e5dd3c723f59e858a52f1`  
		Last Modified: Thu, 18 Sep 2025 20:34:00 GMT  
		Size: 12.0 MB (11969028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa6de07273852bf24667da83e818179b03311c21c2e7fd5bb912f88b12aac99`  
		Last Modified: Thu, 18 Sep 2025 20:33:59 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3ea1f504a72ab791b850a946f60cf76af693004e02846e85fb0bc89c80f5e8`  
		Last Modified: Thu, 18 Sep 2025 21:10:20 GMT  
		Size: 5.8 MB (5753796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:81cda8f2fec7a231b4704485ddf0982e8a57cb362219d1c16aad1a68982fa2bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2544463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9342b14aa4dba1683c4c533f2646be6a252e5ba060b43c6f5741a87fc6fb76f4`

```dockerfile
```

-	Layers:
	-	`sha256:ae80c22b47c6072a420d204154bfc0bb5b1c3e3bf126771981d0712c8fa45066`  
		Last Modified: Thu, 18 Sep 2025 23:18:35 GMT  
		Size: 2.5 MB (2535078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8d128c6b1a43f0dbdfcee3168262a8dbd1084fb488992292a548148abc31362`  
		Last Modified: Thu, 18 Sep 2025 23:18:36 GMT  
		Size: 9.4 KB (9385 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:82efa2f5a1f006c6041aa113a736b03e5df2f67c6f456da3c30d2218a24e8eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49925044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ae85c91e36ae4680cdc9438af1f8014696a8482d6afd9d85ec8c3fa0422418`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64804ad73b0ed1209b15a6dd41986bc1e619efb6e8697191ddc7b1b69359d75e`  
		Last Modified: Thu, 18 Sep 2025 20:28:04 GMT  
		Size: 3.3 MB (3349128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f305c9d0455d113e33a847d3f0c9563d6e9f09c63f827e1e5e14cdff321b039b`  
		Last Modified: Thu, 18 Sep 2025 20:28:04 GMT  
		Size: 12.7 MB (12719738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a541592fd14d4cb0e6efc0a057285ad5014c8a8ba60d75117f670533e66170`  
		Last Modified: Thu, 18 Sep 2025 20:28:03 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a2a7e8a61ba583ae2598a3548ff04dbb98b9e6c53b78d9e43498fb278670e9`  
		Last Modified: Thu, 18 Sep 2025 21:12:14 GMT  
		Size: 5.8 MB (5753828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:7c80630071b5959ffaec17f83a2bbd22c5e424abb379000091d606d203f7b12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fa96a5d07932d61afb57e0b0a82a50964b519f6d1454d30b49e72a07744006`

```dockerfile
```

-	Layers:
	-	`sha256:1ee6b44a8a0462804a14ff0443822b5f88da264f644030fa67ddf3688e00b8c1`  
		Last Modified: Thu, 18 Sep 2025 23:18:39 GMT  
		Size: 2.5 MB (2533114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:297681884efb471130a20a3614ad414209b36722037379e4764bf730445a37b3`  
		Last Modified: Thu, 18 Sep 2025 23:18:40 GMT  
		Size: 9.4 KB (9426 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:62d51fe8a4c5d4e814bac039cd9cfa54455b211dc2a658fd672859348704bc1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51582721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d019f4e11b5c3e39fa7d1620797e00f9101e3193d012e8cffe2a2ecbde87b8`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
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
	-	`sha256:dc2a09b0db8b98044474925cacc9c009aa76e5883edf644cc36c3f6a2e3917ac`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 29.2 MB (29209634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8453bdc594c54e79553e39891f74d7618c04edfcbce848b73420e148579027e9`  
		Last Modified: Thu, 18 Sep 2025 20:26:05 GMT  
		Size: 3.5 MB (3516457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bacf4a67c49ea9342ece32038089571165b8a04faf103c3d17dc13b57c1ec7`  
		Last Modified: Thu, 18 Sep 2025 20:26:07 GMT  
		Size: 13.1 MB (13102534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8465d96bcff6ebc24e42da38196f73aed29f9915aefaf831e2dc8cc3d0b010dd`  
		Last Modified: Thu, 18 Sep 2025 20:26:04 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85f48ccf01bc1e04449e0f1892477790fa7c8ad61f041efa3a00885381d00c7`  
		Last Modified: Thu, 18 Sep 2025 21:11:50 GMT  
		Size: 5.8 MB (5753846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:25ea7234a282d94a6615be64adebd1d677dfe8cb36139d3e742790dd8be51366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2539169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509d946f4d9b6830b1f68e1aafb9eff1d53624fb95b370ad0b8a86095207ebd3`

```dockerfile
```

-	Layers:
	-	`sha256:8c5ae76fdfae4bb405ce485831ba27accf7976b1ce980e09e6ad1f8f6525ae5a`  
		Last Modified: Thu, 18 Sep 2025 23:18:44 GMT  
		Size: 2.5 MB (2529948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43bf6dccc632410517164d69f34cf5c030d3724cb54c93f8db02f872387a83b`  
		Last Modified: Thu, 18 Sep 2025 23:18:45 GMT  
		Size: 9.2 KB (9221 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:89e36f847aa16f179a9fb4f7bdd2dcc4c287817701918d396067346c15485c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54933879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8cd82e95b3c4fc6ce146157c8210e8af52a1bbdbef5ca38a48445edaebbbf7`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
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
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d29088e853ec3d1c942dbdb9e42b1d5593af4d4da19eba6fd3619483d01935e`  
		Last Modified: Thu, 18 Sep 2025 21:12:50 GMT  
		Size: 3.7 MB (3721165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02367e13cc65e31fc53c15cd7b1f387ff01d937953f6d4ec882bd16c4d2e59c4`  
		Last Modified: Thu, 18 Sep 2025 21:12:50 GMT  
		Size: 13.4 MB (13389980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766326e4c2f604e23ce9db51f4a591f1abe09f7f06c290b51d375450cc18015c`  
		Last Modified: Thu, 18 Sep 2025 21:12:49 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6104c9a8a0dd1daf9ee9bf6dff4cbc27063bb8b27b22dcd8624d132fb176fb5`  
		Last Modified: Thu, 18 Sep 2025 21:41:47 GMT  
		Size: 5.8 MB (5753721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:8b27b672fade5b70d02529ece9642710e0a54d3be9503bded6d7beba818e42fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2546605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ba2153e8d23e3239a2df1296f93399d89d844b65d91ad816c93d616cc632bb`

```dockerfile
```

-	Layers:
	-	`sha256:28261f8c05057a00550f26fa74e264dde2770a8e56d390f99ebbac58439fe046`  
		Last Modified: Thu, 18 Sep 2025 23:18:48 GMT  
		Size: 2.5 MB (2537263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4d98ca5c40784b2f0838b3feb4b7a5d384a2c051d090abef2289e6c5d458f71`  
		Last Modified: Thu, 18 Sep 2025 23:18:49 GMT  
		Size: 9.3 KB (9342 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:6f9af7c3e081c5c7ce3468eccf76659ddbef92eeb454d4ae21afb406b9843668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48481501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ead9e5a47f456046fe7ee28f63f1d35b3c482779b0c90f2bf86d498fc110fd1`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
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
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6962f6d3b0b48ce311ef72a5e556c28de61211d0d260a4f9a2db78211551c29`  
		Last Modified: Thu, 18 Sep 2025 21:17:03 GMT  
		Size: 3.2 MB (3181865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44916d7011985d8137f5cd8bb10a2564ce1b6c70d3d5c54a507f94b597820ad`  
		Last Modified: Thu, 18 Sep 2025 22:09:33 GMT  
		Size: 12.7 MB (12661301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc000920f57802d20ec3fd30688c0653e36144b444d1f339ed90a2b537679dc`  
		Last Modified: Thu, 18 Sep 2025 21:17:14 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bf5c79e0cd6d7dae68d06797eaf91b445b046781281fff3792cd42c8ba9ee0`  
		Last Modified: Thu, 18 Sep 2025 22:09:34 GMT  
		Size: 5.8 MB (5753787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:007cb31f0c0b14d1eb2447bd2a68cd7eaea54d70afb3a55386611c5b7bca3f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def552c458384f1432b0ee0654c9414ad6c57c5121a7afa076a3af0ba6366adc`

```dockerfile
```

-	Layers:
	-	`sha256:a70a3f33083ff585db1b85a27197f1bc46008cea2dda6b040cfce0fac36caff4`  
		Last Modified: Thu, 18 Sep 2025 23:18:53 GMT  
		Size: 2.5 MB (2529625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75934d5a3cd358020bfd9439773006654d3c2170d0b7d8c891f40bd2793d33c1`  
		Last Modified: Thu, 18 Sep 2025 23:18:54 GMT  
		Size: 9.3 KB (9274 bytes)  
		MIME: application/vnd.in-toto+json
