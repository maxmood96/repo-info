## `hylang:python3.11-bookworm`

```console
$ docker pull hylang@sha256:f4a50490282f16419d0ab4c542e2224f9ee08f778ef49a6801e09881cd736e7f
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

### `hylang:python3.11-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:584a070714dac467195af1e9efedce1aed91ea94c9b5f9e8ab8f0adecc40815e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54640932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b67387000bd31c698d808df02a8b566a02c7ffe8a4d2fc0f7daf7dc71fc7c9b`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:43:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:43:59 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:43:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:43:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 19 May 2026 23:43:59 GMT
ENV PYTHON_VERSION=3.11.15
# Tue, 19 May 2026 23:43:59 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Tue, 19 May 2026 23:52:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 19 May 2026 23:52:32 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 May 2026 23:52:32 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:45:45 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:45:45 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:45:45 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:45:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c23e389790426bfcee3a40b799e08430a86e79a77cc590c1f3adbcf473efebe`  
		Last Modified: Tue, 19 May 2026 23:52:41 GMT  
		Size: 3.5 MB (3519913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bf18422c9cf5f29d07b8af72df31bd0edb6b31ec4bd57b4777a00eee4a8b28`  
		Last Modified: Tue, 19 May 2026 23:52:41 GMT  
		Size: 15.9 MB (15935228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b323b53a19e2208b498bd0f55473a1dc9498460583e3c9fbd268f1dddffddd6a`  
		Last Modified: Tue, 19 May 2026 23:52:41 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0705b7e74f7bf975dd0d07555f253a8b15b176393d5fc80f044b46233dd7b4`  
		Last Modified: Mon, 08 Jun 2026 22:45:52 GMT  
		Size: 7.0 MB (6951999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:d72956b721ff9cb10a2e5dba48b8704a55d1a841187b6cc099f2f0dc2f6a1583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2631105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fed2af8b2b264c2c5750d4f7e19b485fd191ffab33e9bac7548af4714c305bf`

```dockerfile
```

-	Layers:
	-	`sha256:47746454638d92503cbf792f2996a529863d675d980635b4daec5a9824e9e314`  
		Last Modified: Mon, 08 Jun 2026 22:45:52 GMT  
		Size: 2.6 MB (2623012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39d0d6b24edc39c77e59cb82b8caffe157bcd4ab175e5e2b50cd92f007f732cd`  
		Last Modified: Mon, 08 Jun 2026 22:45:51 GMT  
		Size: 8.1 KB (8093 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:919e059991d43cbe13c2854d64095a157e40f7ccf79838b626d52acc5c29eb7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51157628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7f123ce0ecc5993f4098d6d7687c1eb7752e23a2d0ffcff4ee49aa1aeb004c`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:23:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:23:41 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:23:41 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 20 May 2026 00:23:41 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 20 May 2026 00:23:41 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 20 May 2026 00:39:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 20 May 2026 00:39:46 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 00:39:46 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:47:52 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:47:52 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:47:52 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:47:52 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3e5afa2eeb01167c187727ebcf5bb90554d4e6dd21fe61f1f694b128ceb15ac1`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 25.8 MB (25768291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f82083b7e5267968edbf269a14113361cf185ff2ee69ef46e9caafefeef4018`  
		Last Modified: Wed, 20 May 2026 00:39:54 GMT  
		Size: 3.1 MB (3093161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04719ea44d80e826ab7e805fa1d142271a4822d1eccd469de7cce215ea0a5fcf`  
		Last Modified: Wed, 20 May 2026 00:39:54 GMT  
		Size: 15.3 MB (15343795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7cd69e339e9912f1ad434ff6dd657ceec8df93256f29ec577c67e4267f316b`  
		Last Modified: Wed, 20 May 2026 00:39:54 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcd51b6365d7d87c8f95e99e111a1e68d54e2411a19446219b79753b593beb5`  
		Last Modified: Mon, 08 Jun 2026 22:48:00 GMT  
		Size: 7.0 MB (6952131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:a95ea8ee3d35d44654076a0bb00e4f40a16fde39b39f984194e12c8b80b5f922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0d9416edc35b0e2c3486a58d1a80d32a70ae9ea4830eda6268245dd826860d`

```dockerfile
```

-	Layers:
	-	`sha256:1b87888be9648bd78cd0519bc41311a0cb13675a93a19081a84dd51de2b82bd3`  
		Last Modified: Mon, 08 Jun 2026 22:47:59 GMT  
		Size: 2.6 MB (2626832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceb4b89dbf938e5ffcaefc72c7644a241b4a4e1cbb59314efec5cd7234d7272b`  
		Last Modified: Mon, 08 Jun 2026 22:47:59 GMT  
		Size: 8.2 KB (8174 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:01f5871008428e3664d06a45422780899f6ac502d28b1c711adb44eee607d4b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48745640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19c00cfc9183467aca3522529d89b10b1fa8b0ad9d8664671e8a594808308bd`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:52:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:52:39 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:52:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:52:39 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 20 May 2026 00:52:39 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 20 May 2026 00:52:39 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 20 May 2026 01:09:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 20 May 2026 01:09:28 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 01:09:28 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:48:15 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:48:15 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:48:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:48:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:af86988b12731b7fa2ac73fa1c3f6ab4510a6641d04afb18df09600383bc399d`  
		Last Modified: Tue, 19 May 2026 22:36:05 GMT  
		Size: 23.9 MB (23941643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5f459c3a550381d99bbd5251a52fdcaf276c4cb5d264d926e99beace42539b`  
		Last Modified: Wed, 20 May 2026 01:09:36 GMT  
		Size: 2.9 MB (2928535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4cdcb3750e17a8544dfde9c6f053e3a1aea21590972e667cbc07dffefb6cad`  
		Last Modified: Wed, 20 May 2026 01:09:37 GMT  
		Size: 14.9 MB (14923173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0e9aa0d419b1471d08c46598c6d14e7e1be7c4d4b23ea51248df675c4fefe8`  
		Last Modified: Wed, 20 May 2026 01:09:36 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4713645c28ebdf01f0cc5fdf5fe581ce0d3098a9a2e12edbf94ed0d1e3bd0ad0`  
		Last Modified: Mon, 08 Jun 2026 22:48:23 GMT  
		Size: 7.0 MB (6952040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:afe994f4804a493ff4d4e128add77ccd8d50ce9c3ca76bf76349740c39f15c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2633455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620cc1960b0486f6b64f584371c5ca6834d068d657592b4816398a413fb076d2`

```dockerfile
```

-	Layers:
	-	`sha256:a0d8bc17ca273035557f75a4953c846ce400fd7fa68f8706d0da0478b1a5cffd`  
		Last Modified: Mon, 08 Jun 2026 22:48:23 GMT  
		Size: 2.6 MB (2625281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af7835f1c8c656d1037c2a5c764f92012a9e13b1f67c4ed577eebf2e747b25d6`  
		Last Modified: Mon, 08 Jun 2026 22:48:22 GMT  
		Size: 8.2 KB (8174 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:1bcb02388b1cd59d01fa7d0c8425c2ba311afb1977961e6d26a2a40f66569afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54293051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b977b38c3c3ed59b783e190072e09d2dfac4a3ae36ff0665e7077eb5f762fef`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:48:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:48:02 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:48:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:48:02 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 19 May 2026 23:48:02 GMT
ENV PYTHON_VERSION=3.11.15
# Tue, 19 May 2026 23:48:02 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Tue, 19 May 2026 23:59:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 19 May 2026 23:59:12 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 May 2026 23:59:12 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:46:03 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:46:03 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:46:03 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:46:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae85f80de19a95447035673506a86aca8b0415f269b43a8535236c3320d04375`  
		Last Modified: Tue, 19 May 2026 23:59:20 GMT  
		Size: 3.4 MB (3351810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775f62d3f67010227ca1f1db54a6016a9e19b7c80ed81697a9706bcab714431a`  
		Last Modified: Tue, 19 May 2026 23:59:21 GMT  
		Size: 15.9 MB (15873917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af711a5378390f945cb7d896ce79546204ad77a5fe3f4baaba96b50089ec3d20`  
		Last Modified: Tue, 19 May 2026 23:59:20 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93a98d261d5adf9d211c40d1d286abef492214f007f8b9d4344c0529f48b826`  
		Last Modified: Mon, 08 Jun 2026 22:46:11 GMT  
		Size: 7.0 MB (6952031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:4409004f6270b978fa52f002f2971efd4b4a29c36e02e6cd17438e283b6e665d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2631483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dbc0f3c3a45fc8306ec2579b68879ee8199299ff97f3ca5ba250275cb3a821d`

```dockerfile
```

-	Layers:
	-	`sha256:c417e86f73d25c1ac078e844992ac025af94ba0fbbc836b012c1f050e84862ab`  
		Last Modified: Mon, 08 Jun 2026 22:46:10 GMT  
		Size: 2.6 MB (2623285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52d7e3148807d3c57ab96f27a8dba2cb4eaa7a39af2a10b94e84f80136ba2a4f`  
		Last Modified: Mon, 08 Jun 2026 22:46:10 GMT  
		Size: 8.2 KB (8198 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:5d1e4c74c01de1cddc1334dc0c89779ce3b7197bbe37f1941d9e29b3ad07c2c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55861386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2adbc52faf755e7fd2952ee26c42556d1ab4f49f0384c8232aa89dfc503a8f`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:39:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:39:02 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:39:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:39:02 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 19 May 2026 23:39:02 GMT
ENV PYTHON_VERSION=3.11.15
# Tue, 19 May 2026 23:39:02 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Tue, 19 May 2026 23:49:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 19 May 2026 23:49:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 May 2026 23:49:23 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:48:00 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:48:00 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:48:00 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:48:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:408fe432485bb366e9a4871b553de2e6347ca580fe8a5d45c84c87fa58d5e5c7`  
		Last Modified: Tue, 19 May 2026 22:37:12 GMT  
		Size: 29.2 MB (29218601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce3ed21c0e2007f6fd8ec8f21505670c8613b414204f8ff206fecf8dc323214`  
		Last Modified: Tue, 19 May 2026 23:49:32 GMT  
		Size: 3.5 MB (3520839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b490b6b9dd028312c4f6cc89b47c339eb58aa5e6f66fe99293b692428bf038b2`  
		Last Modified: Tue, 19 May 2026 23:49:32 GMT  
		Size: 16.2 MB (16169620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07125ec8734a1b65ce30bcc62b6f94a8d800754815e21ec899775302c7e56a7`  
		Last Modified: Tue, 19 May 2026 23:49:31 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a60ba7dfe2d311f7a4bc4d7179a84341001ac01a1e220ada7eba5851a74b8a`  
		Last Modified: Mon, 08 Jun 2026 22:48:07 GMT  
		Size: 7.0 MB (6952076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:cc818634a96fa3a58493c1c59e6baca561f45de343c535ee4034e64311de053e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b452e73a04e6566cd2f42adeb164c0148b755e71c581baaf689bc0ca269044ea`

```dockerfile
```

-	Layers:
	-	`sha256:f1b3f35d31b53381b7574b110fba5762731f3e838c05a758e9e27cf090452c5e`  
		Last Modified: Mon, 08 Jun 2026 22:48:07 GMT  
		Size: 2.6 MB (2620163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad25ff1a034f7f086e95e783cf344ed8c4bff50310c1df838a171928eea712e1`  
		Last Modified: Mon, 08 Jun 2026 22:48:06 GMT  
		Size: 8.1 KB (8061 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:5712ebfb62b1fa0b3279874f059ff2000451038d1986ac4309aebeb6b480b69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59319851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511a2fed4842cc6a5e2642311136d281c57d7c9a3fc4c657622ab0a398236c4b`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 04:33:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 04:33:44 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 04:33:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 04:33:44 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 20 May 2026 04:33:44 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 20 May 2026 04:33:44 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 20 May 2026 05:12:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 20 May 2026 05:12:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 05:12:23 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 23:20:45 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 23:20:45 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 23:20:45 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 23:20:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9992109105b99d139cd44d383159fc226ead8096c0467c99111f3a441a0537e2`  
		Last Modified: Wed, 20 May 2026 04:53:37 GMT  
		Size: 3.7 MB (3725057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4efffb71cfd392d3e6e0b98da2d6fcf52f07b0c08c02a03c55fca07185732a`  
		Last Modified: Wed, 20 May 2026 05:12:38 GMT  
		Size: 16.6 MB (16566564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e61ebc18093b74f5e76657ce35a359d4367c02b98679056b4b8759779e62154`  
		Last Modified: Wed, 20 May 2026 05:12:37 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421f0656a4bc2cce5364025b0d7543af68f30cec5d88e09bdeacef2ff7eb8d39`  
		Last Modified: Mon, 08 Jun 2026 23:20:59 GMT  
		Size: 7.0 MB (6952238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:0d7073052ee61c27e95f908d5f72c7b43bd33b79bfb496b13e18a7e6a94c0c89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55a7c96e395bcfbaf50671ff7cce63c556d00e07916e7099532433c92df60b1`

```dockerfile
```

-	Layers:
	-	`sha256:f8f3406b5053d666553e1b3e1ed913238f9b142d9b5a5217c37bdd479079255d`  
		Last Modified: Mon, 08 Jun 2026 23:20:59 GMT  
		Size: 2.6 MB (2627518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6478fa87afb8c53641b4affe71ef00ad0fa73f7bf50a8628544e174b7cf724`  
		Last Modified: Mon, 08 Jun 2026 23:20:59 GMT  
		Size: 8.1 KB (8138 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:a727ac50c044baee12b56fffc508db3e3fa482c568f25b8f0a4ecfa12d41e012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52789118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a667de9ae0a7f32ffddc01ad4d2d6d8a958e7d59b5279e0c861408d6ad9a53b9`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:15:32 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:15:32 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 01:15:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:15:32 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 20 May 2026 01:15:32 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 20 May 2026 01:15:32 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 20 May 2026 01:32:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 20 May 2026 01:33:00 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 01:33:00 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:56:54 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:56:54 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:56:54 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:56:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908d95ecc58e29f001750d357eea736423e2548d14ad0d284c6c148dd3071050`  
		Last Modified: Wed, 20 May 2026 01:29:03 GMT  
		Size: 3.2 MB (3184031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd170bea9e1d5083e75fe2d26b369ea35b44ddd22bede72144b94d190df336ff`  
		Last Modified: Wed, 20 May 2026 01:33:13 GMT  
		Size: 15.8 MB (15764211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e43b0e70835ba698f66f41fce45cd0ebd26d3e9305dd0c0c623b965257b5226`  
		Last Modified: Wed, 20 May 2026 01:33:12 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f343dc7d4d9622d90c98e26e66b695298b9c7807114d6b1c6f99b029a6c9d204`  
		Last Modified: Mon, 08 Jun 2026 22:57:08 GMT  
		Size: 7.0 MB (6952028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:aee1b2e2b75350eb65f981b957c0ce6ca16f86a8ebda537eadef8f56554e08dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d86d4e896ae18b2cc8c123aa71d62a51054306fa8c01e9c7c0f33c9ba5607d8`

```dockerfile
```

-	Layers:
	-	`sha256:e851341d3aa078fe7ac1da2b9cb3eae61a50a97dbbfe7dd4c1feab83e514aea9`  
		Last Modified: Mon, 08 Jun 2026 22:57:08 GMT  
		Size: 2.6 MB (2619828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3b8e2154dd0d6a69da46c1cac279a149094d1680121f0b73ba398a288c7e1ff`  
		Last Modified: Mon, 08 Jun 2026 22:57:08 GMT  
		Size: 8.1 KB (8093 bytes)  
		MIME: application/vnd.in-toto+json
