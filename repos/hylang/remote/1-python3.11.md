## `hylang:1-python3.11`

```console
$ docker pull hylang@sha256:f107d9a37bcb97775e8f21f496ecd631aaa4e54f85a577c10cad857fb515b5cd
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

### `hylang:1-python3.11` - linux; amd64

```console
$ docker pull hylang@sha256:ab7d8dba9a059647a55631a395ddb6fa5068505987820792527eabaeec18f3e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52391510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc026f9697118c187d09cf28bb897d880ad269ecd232e214425630651e3c61a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:03:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:03:07 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:03:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 01:03:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 11 Jun 2026 01:03:07 GMT
ENV PYTHON_VERSION=3.11.15
# Thu, 11 Jun 2026 01:03:07 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Thu, 11 Jun 2026 01:11:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 01:11:19 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 01:11:19 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 02:40:49 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 02:40:49 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 02:40:49 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 02:40:49 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c471a93fc525f2012a1d483a12540ba9df9189f0bfe12238f74273aa72590a7`  
		Last Modified: Thu, 11 Jun 2026 01:11:26 GMT  
		Size: 1.3 MB (1293278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd2cf7d3f6acc894d6ab00affeb6abf779933fa982aec49b9a4ebea322b7fbb`  
		Last Modified: Thu, 11 Jun 2026 01:11:26 GMT  
		Size: 14.4 MB (14360841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3250ea7ceadc1e9a40a2d832082ee8fe68631ef9c9bf7bd5447fbcff9f527439`  
		Last Modified: Thu, 11 Jun 2026 01:11:26 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef18a8d7f04704b7a1732468a042cc176535f8f2d1c4425aca7c89b02273cb1a`  
		Last Modified: Thu, 11 Jun 2026 02:40:56 GMT  
		Size: 7.0 MB (6951726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:0ec14ae3cad321c76c8e3c8988fc5e20e50ce0ea339aa1b6aa3582a41190fd99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9190b74eed9fb1cc40f5603cc2d7ff146eea6d5df3c466f78ec37be3f8782761`

```dockerfile
```

-	Layers:
	-	`sha256:d3e20b18a50326ed65642035b49421a7c475287cc9cf77ae942893f381db9f2f`  
		Last Modified: Thu, 11 Jun 2026 02:40:56 GMT  
		Size: 2.2 MB (2200049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d832d3099312f9590905c2df44bdff56a1814852855838d031ee97441124472`  
		Last Modified: Thu, 11 Jun 2026 02:40:56 GMT  
		Size: 9.3 KB (9320 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11` - linux; arm variant v5

```console
$ docker pull hylang@sha256:6166b448495847396e2e7675326f9a758e4e908ce7e0413ecb375f28a1b8d7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50185465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322dde0b6ec127f6d15295f586ec55cc5a755879cf20d0b3a4e7f2037c20d614`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:49:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:49:26 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:49:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 01:49:26 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 11 Jun 2026 01:49:26 GMT
ENV PYTHON_VERSION=3.11.15
# Thu, 11 Jun 2026 01:49:26 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Thu, 11 Jun 2026 02:07:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 02:07:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 02:07:37 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 03:06:03 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 03:06:03 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 03:06:03 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 03:06:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6acc83410246dbdc9fb02e6c3c8a0ff8892ca4aa8a91a6da4c810e3e1d81224`  
		Last Modified: Thu, 11 Jun 2026 02:07:45 GMT  
		Size: 1.3 MB (1276355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0668751d2aa6aa9af8375e5db341759ea477afe48ee085451d7e01890460172`  
		Last Modified: Thu, 11 Jun 2026 02:07:45 GMT  
		Size: 14.0 MB (13997795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539bae1f291b41b7ec92fa23774f3d14bbffbd50e3d9d8a8bd5f296ff2aae39a`  
		Last Modified: Thu, 11 Jun 2026 02:07:45 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0789765021ea6ebab88e3ae30ef7cfecd5cc36ffea7500a3506d9519212e609`  
		Last Modified: Thu, 11 Jun 2026 03:06:11 GMT  
		Size: 7.0 MB (6951866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:70a2739e3ca84f0bbaabfb459a4204019d2fc0865b1f068aeb800ebae6535cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ee5e432572c4e30bba49527a673bf74db9a96388dc776d7ed928715953dab5`

```dockerfile
```

-	Layers:
	-	`sha256:7d4d55000b9664198e03d781f82acd12fa09484acbb1354679ae1a4b9754d024`  
		Last Modified: Thu, 11 Jun 2026 03:06:11 GMT  
		Size: 2.2 MB (2203050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31b4ffd41d558dc48a5d2cf5155b3dc6c906fcee3c08f6bbb28502e50d88e6f5`  
		Last Modified: Thu, 11 Jun 2026 03:06:10 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11` - linux; arm variant v7

```console
$ docker pull hylang@sha256:f75d4cac95781d41495745334d60c871a1455991bcea8f2628e89dac07530889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48144514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df931d50dd5b9d1046784ace57895feb560b921121ce43eca2da94aa90f8189`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:18:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 02:18:20 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:18:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:18:20 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 11 Jun 2026 02:18:20 GMT
ENV PYTHON_VERSION=3.11.15
# Thu, 11 Jun 2026 02:18:20 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Thu, 11 Jun 2026 02:35:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 02:35:28 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 02:35:28 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 03:25:02 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 03:25:02 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 03:25:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 03:25:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f517fbab82334e16eb8c08cd3254e543644de5f5b8ba527224fcfacd2952512`  
		Last Modified: Thu, 11 Jun 2026 02:35:35 GMT  
		Size: 1.2 MB (1249141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181cce788eb66311196b1e2d032df626527ab4d79b9f9b3740db4bcc17204457`  
		Last Modified: Thu, 11 Jun 2026 02:35:36 GMT  
		Size: 13.7 MB (13732244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88a3273d7925cb5f1cae64544b02971e807c055e08687aa4293e97bfd97d8d5`  
		Last Modified: Thu, 11 Jun 2026 02:35:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1e859c4779e09ca8200e145facaa49f4e04d77658b54158adaa10d317785e0`  
		Last Modified: Thu, 11 Jun 2026 03:25:10 GMT  
		Size: 7.0 MB (6951876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:9596dcf4c246677d41ba746bf582e6b07630c87afa8f89dbeedcc7e86e249fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbfa3cbaba5ff15c38255187ab7f256c4880925aec9f747182360f038d4cd7b`

```dockerfile
```

-	Layers:
	-	`sha256:4f8c2ac41ab2c1270fd779c41dc0b91bafeff7c5c2f3cb8a459461bdb504cd64`  
		Last Modified: Thu, 11 Jun 2026 03:25:09 GMT  
		Size: 2.2 MB (2201503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5106180f5c0469c213d97070621c7f4a5dfacbb601f7834190e9a423cd3268f`  
		Last Modified: Thu, 11 Jun 2026 03:25:09 GMT  
		Size: 9.4 KB (9431 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:561216b2a48fb32150716f774f8314b68f4504ef930c72b74bf854b2cd10261d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52690063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc464f15bac476c55e373b33b5066fc4f2152e2dd5edd29c6711291e2ebe51e4`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:05:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:05:09 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:05:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 01:05:09 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 11 Jun 2026 01:05:09 GMT
ENV PYTHON_VERSION=3.11.15
# Thu, 11 Jun 2026 01:05:09 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Thu, 11 Jun 2026 01:16:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 01:16:04 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 01:16:04 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 02:41:07 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 02:41:07 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 02:41:07 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 02:41:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6eaa7747ea36ce09c07e556b94db03b4221eaa799d4d0ca387fb13a46d89f1`  
		Last Modified: Thu, 11 Jun 2026 01:16:13 GMT  
		Size: 1.3 MB (1274124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473b26fe033cfb7157bf8eccaaec7fb4c2973e971213128c1a817a6aa0132976`  
		Last Modified: Thu, 11 Jun 2026 01:16:13 GMT  
		Size: 14.3 MB (14315424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7603e6ebb8a9b94a429dcdb69477fc29b25e033752a99d537ba0d87a455212`  
		Last Modified: Thu, 11 Jun 2026 01:16:13 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714e752d0694c18fbcc8290cd5ec8bae44d2af2f2edc03bfbb4e9c6ff326843c`  
		Last Modified: Thu, 11 Jun 2026 02:41:15 GMT  
		Size: 7.0 MB (6951735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:345ff0ef8a80ceaec8265ae8a0808cfdc932691c772f770c05a560e7d13d05a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d45ded4ea340e0dbee19ca80a085c9691ee463bfbbe9dbf8bea1029d0a0d141`

```dockerfile
```

-	Layers:
	-	`sha256:5c0cae40caf908d2c382663918e8efc6a08a413c62f4b6cb2c0e53e3f07203e9`  
		Last Modified: Thu, 11 Jun 2026 02:41:14 GMT  
		Size: 2.2 MB (2200355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c200701a1d9eabbd880707666c90b3373e59c3e393488cf784e7f0c054560f9b`  
		Last Modified: Thu, 11 Jun 2026 02:41:14 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11` - linux; 386

```console
$ docker pull hylang@sha256:05e685244125c6cea164472b60255b90795b748c7bb33fc71fceb39191228d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53955389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea5e50d8f3e0d54c61839a8f8fcc1f49df03e6a7e6b4e3b8fc6cf6c8403fcebc`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:59:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:59:00 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:59:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:59:00 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 11 Jun 2026 00:59:00 GMT
ENV PYTHON_VERSION=3.11.15
# Thu, 11 Jun 2026 00:59:00 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Thu, 11 Jun 2026 01:19:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 01:19:14 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 01:19:14 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 02:39:50 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 02:39:50 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 02:39:50 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 02:39:50 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7189f5855a0389067ac9c768291ec385ae73b1df3e37ef35e421d3e90b75b683`  
		Last Modified: Thu, 11 Jun 2026 01:19:21 GMT  
		Size: 1.3 MB (1297790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00208508e10554868f9c709ebb207b01a6887e0f940b9cd5231d9e4d3b68298`  
		Last Modified: Thu, 11 Jun 2026 01:19:22 GMT  
		Size: 14.4 MB (14404502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c6c78a58cb4694f8d79bead898c8e939f253a42cefe2477c9abd14393ca`  
		Last Modified: Thu, 11 Jun 2026 01:19:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e0a6b6757da3ba24ee349ea9a495c68b25467f6ba4bced9f337ac4b371c0e4`  
		Last Modified: Thu, 11 Jun 2026 02:39:57 GMT  
		Size: 7.0 MB (6951654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:2f1ba74ba16dcb90a2fc6530449d34d172b1f451f1a67bb0f381d1deb1289d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787d9083d277abae25df848e596c007f23ef1cbb618a464bcbf9f7eb39c8cf8a`

```dockerfile
```

-	Layers:
	-	`sha256:5baa028c3c1c19207b5ed7802256c8b400fb1da3815b5639a8d91e59e52287a0`  
		Last Modified: Thu, 11 Jun 2026 02:39:57 GMT  
		Size: 2.2 MB (2197210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad3f7fcb7c872810fde7933fcb43aca92138d87f5c6d2b21c323e15321e13a88`  
		Last Modified: Thu, 11 Jun 2026 02:39:57 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11` - linux; ppc64le

```console
$ docker pull hylang@sha256:4d964012a01514b5b2592f3fb7a6123acfcca8adc642516d8c412ee4276ccfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56578661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9308c4e4f14734e7a7007716fe15d2cddd323cde8242bae850632e3e6bbeba`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 07:45:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 07:45:04 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 07:45:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 07:45:04 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 11 Jun 2026 07:45:04 GMT
ENV PYTHON_VERSION=3.11.15
# Thu, 11 Jun 2026 07:45:04 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Thu, 11 Jun 2026 08:38:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 08:38:16 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 08:38:16 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 12:35:03 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 12:35:03 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 12:35:03 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 12:35:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57fbe4f0b9ceabf43c157fcab90b068b7953cc59c03767db856195a2a61e8a9`  
		Last Modified: Thu, 11 Jun 2026 08:04:12 GMT  
		Size: 1.3 MB (1321251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea154f270773af66bca0f8cdf114ebbae5ea4b3716c16d806e905e1779288b2`  
		Last Modified: Thu, 11 Jun 2026 08:38:31 GMT  
		Size: 14.7 MB (14698722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d5f437552045f95e9641c9df940cd4b418131284f894e2a5fc15929b01797d`  
		Last Modified: Thu, 11 Jun 2026 08:38:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e124a89ad9d3a72c178daa08bed5cb7dac1d2d803930a2f8671419a318b4c1af`  
		Last Modified: Thu, 11 Jun 2026 12:35:25 GMT  
		Size: 7.0 MB (6952099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:20d3683d1e03ba3c6b26a396296df4e93b8e787e15bf0d92d26167fcef6022bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2213028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6b2f8d90da58b81e9f335b96dc3a7a6313f507f8fdfff34a91cb9dce6c9dc9`

```dockerfile
```

-	Layers:
	-	`sha256:00ae8909b660b1f1b2091db0b96722c9f714cd55f6c677d1e574a56a90ef5f65`  
		Last Modified: Thu, 11 Jun 2026 12:35:25 GMT  
		Size: 2.2 MB (2203640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7b6736c24a4a54f2e3d462737602fa1d2324b973ed84b9529dabe066a216697`  
		Last Modified: Thu, 11 Jun 2026 12:35:25 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11` - linux; riscv64

```console
$ docker pull hylang@sha256:8a07eb20366f6bb0e5d14e780e86ffd8d11599024c54431624049fe68622d59e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50686412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ba574bcfc597ddfb25684c9543e934bfb5dbce24812fdac2549b5c2530f799`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Fri, 22 May 2026 03:40:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 May 2026 03:40:21 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 03:40:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 22 May 2026 03:40:21 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 22 May 2026 03:40:21 GMT
ENV PYTHON_VERSION=3.11.15
# Fri, 22 May 2026 03:40:21 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Fri, 22 May 2026 06:48:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 22 May 2026 06:48:03 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 22 May 2026 06:48:03 GMT
CMD ["python3"]
# Tue, 09 Jun 2026 09:16:24 GMT
ENV HY_VERSION=1.3.0
# Tue, 09 Jun 2026 09:16:24 GMT
ENV HYRULE_VERSION=1.1.0
# Tue, 09 Jun 2026 09:16:24 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Jun 2026 09:16:24 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64887635710bb3720fe7560b7a4d5dad0dfb67a1d1866a9325f82ee51653a45b`  
		Last Modified: Fri, 22 May 2026 05:23:49 GMT  
		Size: 1.3 MB (1261219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b89d383be95aac86892142ff52cade70754fd5d0efdb194362b627e5438a47`  
		Last Modified: Fri, 22 May 2026 06:49:14 GMT  
		Size: 14.2 MB (14194434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef36bbc165033af559f396e5e64a77198d280142ef829256befad56ce35bb78`  
		Last Modified: Fri, 22 May 2026 06:49:12 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b53a9fcaf9bbaf1a775fdd141c813c2e2a13b5368627b3831bd2d81bdfb15a2`  
		Last Modified: Tue, 09 Jun 2026 09:17:28 GMT  
		Size: 7.0 MB (6952910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:ff1d0a874e3d78f67f8a619327ea94d4afd35cfdfc8630f690de75a98c59665c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3ffa465cfcc0e83fdd821e7700ac5daf39a4165ab87fd2a0348ba40782e64e`

```dockerfile
```

-	Layers:
	-	`sha256:2fe29edcebeaacdb938d5d8b3bff6e45c8a2920e03bd8404f64875a420312042`  
		Last Modified: Tue, 09 Jun 2026 09:17:28 GMT  
		Size: 2.2 MB (2194011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42474efa7d73ee92bb69e8eef0be13df573b94698ba046d293cf6b2d65fdfb3e`  
		Last Modified: Tue, 09 Jun 2026 09:17:28 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11` - linux; s390x

```console
$ docker pull hylang@sha256:4f9cbfe0586815fc784152ffc1a9bee0db1712006ba3fd11edbbe250bada4f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52485240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4f8dea61ecd1d679ff41b6f64f4d3e710b98010fe56ab259520cc1b7eb3f56`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:35:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 02:35:51 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:35:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:35:51 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 11 Jun 2026 02:35:51 GMT
ENV PYTHON_VERSION=3.11.15
# Thu, 11 Jun 2026 02:35:51 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Thu, 11 Jun 2026 02:55:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 02:55:02 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 02:55:02 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 04:03:59 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 04:03:59 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 04:03:59 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 04:03:59 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e6ebe81c809d11446cb9d8ee1dc54cfcefcebce9a4bfd457553a7118acf502`  
		Last Modified: Thu, 11 Jun 2026 02:51:02 GMT  
		Size: 1.3 MB (1305780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346af09b0c099c5ebf2aed3a6c6a33aa256ec6c29dafe8366209cee58f3daf9e`  
		Last Modified: Thu, 11 Jun 2026 02:55:15 GMT  
		Size: 14.4 MB (14375920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009a6a72895a1b27ca980fa736a157dbf9fab90b168fedc2840150f198f7963f`  
		Last Modified: Thu, 11 Jun 2026 02:55:15 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d997218b723a6213947b5936a76b1ef7a54f60b861d97b5ce3bd396a14dd7f`  
		Last Modified: Thu, 11 Jun 2026 04:04:12 GMT  
		Size: 7.0 MB (6951937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:8460c50b7dcc6457542a5a216411973c569b2d11d2577747745809a8351d2bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf67cd42dee3ab58b209a95f6437cb9df5a56ad1fe7acfc61c82c64d19ee4cf7`

```dockerfile
```

-	Layers:
	-	`sha256:3f06b13ee6f0b3a0c84dc11458cd2a91c281e93a6ec8cc2ef2a9d4f4c1dc489a`  
		Last Modified: Thu, 11 Jun 2026 04:04:11 GMT  
		Size: 2.2 MB (2201488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e7ec5afb4d55ee6f87365fa09a23d8a7e91d64fff02809dcdc27107223e007`  
		Last Modified: Thu, 11 Jun 2026 04:04:11 GMT  
		Size: 9.3 KB (9320 bytes)  
		MIME: application/vnd.in-toto+json
