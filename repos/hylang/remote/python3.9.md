## `hylang:python3.9`

```console
$ docker pull hylang@sha256:c76fd3acaee224a8dced1969aba146cf2cc652526165154d29946e4669ebb17c
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `hylang:python3.9` - linux; amd64

```console
$ docker pull hylang@sha256:aa27017eb337b09c0d191d06ce730eb7124bf9ff17b520528e0a3c07d460629d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50342719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003ae4493e7ee6ee3f032a95b93eec489ffcb9037f8b78d185b5185de114b172`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 17:12:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 17:12:13 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_VERSION=3.9.22
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_SHA256=8c136d199d3637a1fce98a16adc809c1d83c922d02d41f3614b34f8b6e7d38ec
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2481a58f9b3dcc989088df77c786078a59d807e6409a9d165ed4587814cdfbe0`  
		Last Modified: Wed, 21 May 2025 23:31:29 GMT  
		Size: 3.5 MB (3511840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692d37168f614092ffd355652aa0a07223ed129e6417aa144564fbd3d773884`  
		Last Modified: Wed, 21 May 2025 23:31:30 GMT  
		Size: 14.9 MB (14934784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0684e18c375e78b2595b04f87cae91cff938ec9996b274e397c73f96605c69d`  
		Last Modified: Wed, 21 May 2025 23:31:29 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed3141fa3e6867601b56c691d2a99af9fa02877cedd8b6f341d399996da4325`  
		Last Modified: Thu, 22 May 2025 00:13:16 GMT  
		Size: 3.7 MB (3670517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:0da04c4a1065af86e0ca51865e65e9651210a476889624e13b9d7b7aa318595a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2495864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da61e2edd1a051645700245577df7d2bcf80b13a179ef8fc35aa820f889e4e60`

```dockerfile
```

-	Layers:
	-	`sha256:466d4835392a9c01a51bfb417e1b4e3b7c71fad8560e76c6c7cce43c7438f896`  
		Last Modified: Thu, 22 May 2025 00:13:16 GMT  
		Size: 2.5 MB (2486607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c612e27bd61c29faed77393e08451008150ed9df56777399beae02cb2ae0546`  
		Last Modified: Thu, 22 May 2025 00:13:15 GMT  
		Size: 9.3 KB (9257 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9` - linux; arm variant v5

```console
$ docker pull hylang@sha256:78584cae999f3ee9fd79eba8bb394b7e0b15a81b440c8f5424fa65c4dac14462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46877845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55733ba13624af02e01c1e9b300b3658ef4ba72957e1d332105944c167765d8`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 17:12:13 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 17:12:13 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_VERSION=3.9.22
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_SHA256=8c136d199d3637a1fce98a16adc809c1d83c922d02d41f3614b34f8b6e7d38ec
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dbb1b0ed7af2455215de8a12234a760614bfce24304f66df8e2699b6b0bc7b`  
		Last Modified: Thu, 22 May 2025 03:17:52 GMT  
		Size: 3.1 MB (3085107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1e766c917ef9f79ace99fa245263c96b37c511502e3f2181330b2bbbdc330f`  
		Last Modified: Thu, 22 May 2025 03:36:11 GMT  
		Size: 14.4 MB (14364887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930c75023f272588e12d516b1a92c8674f8586b5211bc36741f047ec9c12232e`  
		Last Modified: Thu, 22 May 2025 03:36:10 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231b6fe8e20c784ee8b739ffee209e8eaaf9ba7b4356ec16a3001dd33f01da83`  
		Last Modified: Thu, 22 May 2025 06:26:49 GMT  
		Size: 3.7 MB (3670704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:408768ebeacd22693a3f70d2c10330ba0f24b962784742a16ba676d3262eb402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2499824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fdfd4c34ffb961a4aff69d3a7d65df3badbe2b5eb231d46ce7e383bfefe69f`

```dockerfile
```

-	Layers:
	-	`sha256:f46978e547518e8b3b7fa31fad0204ba7c14f75e399d6df649fa6b1f372b32b3`  
		Last Modified: Thu, 22 May 2025 06:26:48 GMT  
		Size: 2.5 MB (2490459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7314dcb664cd990e652df99597bd633a81d2b9e7b20003b839da86a31bae0b0b`  
		Last Modified: Thu, 22 May 2025 06:26:48 GMT  
		Size: 9.4 KB (9365 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9` - linux; arm variant v7

```console
$ docker pull hylang@sha256:7a8cb815ca3bd6366bdfaa39eae02cae3fe503f2620c28bea6f0536df54084b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44479502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0edb23c85b5db78bf29c85cb84784f2781faad5492a0f94d11e327ce7c0b03`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 17:12:13 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 17:12:13 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_VERSION=3.9.22
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_SHA256=8c136d199d3637a1fce98a16adc809c1d83c922d02d41f3614b34f8b6e7d38ec
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852143121088e2c1467edf9863ea215b241b9651107e4b15c277b8b08b00309b`  
		Last Modified: Tue, 29 Apr 2025 07:37:06 GMT  
		Size: 2.9 MB (2914879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcdf3fae289bac16c7df4f513d6809c4df3725ac039f98a0f34c0ff7f524446`  
		Last Modified: Tue, 29 Apr 2025 09:16:16 GMT  
		Size: 14.0 MB (13955414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967dd63284ed070dab2974aa884abfeb69f788e5d9c55a46513c7d68f377e5d9`  
		Last Modified: Tue, 29 Apr 2025 09:16:15 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952bd1a151095a1347a6396517c97e97392193d3ca4152c0e85711c83da60ae1`  
		Last Modified: Fri, 09 May 2025 18:47:02 GMT  
		Size: 3.7 MB (3670886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:981fce9b42b4f53c42c55751159e3f932236839e35ea06c0f605dcf91c22f089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2477568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4eabd1afd9882cdfd7d4ff8ba498aca67b2b681fad7bf849577e7808307e2f`

```dockerfile
```

-	Layers:
	-	`sha256:0b61b30dab0d4258cea713c415ab2958d2b1e783a79043234142ba8a46d59f06`  
		Last Modified: Fri, 09 May 2025 18:47:02 GMT  
		Size: 2.5 MB (2468203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93313e0a2fc730bd054031339dac27d20cfcd37c5c75329b0fbfdc5fb993b1db`  
		Last Modified: Fri, 09 May 2025 18:47:02 GMT  
		Size: 9.4 KB (9365 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:ef1317c4757d1ecae75d02f68a0506d2d1895978ce58ec6817198562809b1ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49904218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba2beda7a2f0e289d3640c7ef7f4361fd7bb8aa88aaf8e11222cd1b92890890`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 17:12:13 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 17:12:13 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_VERSION=3.9.22
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_SHA256=8c136d199d3637a1fce98a16adc809c1d83c922d02d41f3614b34f8b6e7d38ec
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df007eea74a31e334ec983fe01bc025b73676e29573b2429960f3b0a9869c81f`  
		Last Modified: Tue, 29 Apr 2025 23:04:15 GMT  
		Size: 3.3 MB (3332107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6905635aaf90f90b1045703b47911a29f7b49f19503ab4c09e4d6e9ad8c8f3`  
		Last Modified: Wed, 30 Apr 2025 00:02:04 GMT  
		Size: 14.8 MB (14834558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad8221d8d1ebf1607bdfaa97e0d91f11d3d57cef8df662ffd94288f9fd705f4`  
		Last Modified: Wed, 30 Apr 2025 00:02:03 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e4a3e5d3f238f587f51f2309112c54667d89c267448073a1f24f8ee102635f`  
		Last Modified: Fri, 09 May 2025 18:58:29 GMT  
		Size: 3.7 MB (3670681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:a84c80bc21c2e5b8b3449eb836dd3783a0c84f064549defb91f6587a2e20c47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2475632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435935206065bc690b50ff486b4aeb95ecfaab5ed34dd729d5408c37ec9e8abc`

```dockerfile
```

-	Layers:
	-	`sha256:4041db27029c84f2c9beaa2ca1920bc9f35913387531238e8666b5f012d5353a`  
		Last Modified: Fri, 09 May 2025 18:58:28 GMT  
		Size: 2.5 MB (2466223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64d52d7d1a0f10a18e7d5fbafbf96a5cd3500a18fe4d49ac40142a3dd2b3c3b1`  
		Last Modified: Fri, 09 May 2025 18:58:28 GMT  
		Size: 9.4 KB (9409 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9` - linux; 386

```console
$ docker pull hylang@sha256:a8d94abc13c7382e8c19494ed6fd97e157658092619c1848dfe25883c391a54a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51571620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0747958227011e8e84eaea97b15539f7b54b0fec8199af5609ae214c175d808c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 17:12:13 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 17:12:13 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_VERSION=3.9.22
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_SHA256=8c136d199d3637a1fce98a16adc809c1d83c922d02d41f3614b34f8b6e7d38ec
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f514bf603f6c63bf034a525ab5914a27522fcd67c17eb62ce6d0bc75b0ba3470`  
		Last Modified: Wed, 21 May 2025 23:29:12 GMT  
		Size: 3.5 MB (3511105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6922c30e9b64220da47ef3034258e333f97272d6ea4745256b4d906be84a6064`  
		Last Modified: Wed, 21 May 2025 23:29:12 GMT  
		Size: 15.2 MB (15182146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90669e65f9f206a21aa33eee8bf10d634d882cc5549a149f1ea7b9a5617bade4`  
		Last Modified: Wed, 21 May 2025 23:29:12 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce8ec9ac097d1601fa9c2a72b82ba0702f80aaeb9435020fe80a91e192073e0`  
		Last Modified: Wed, 21 May 2025 23:44:12 GMT  
		Size: 3.7 MB (3670632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:e037943778e1830ea115a8d4b2c54703875cb0b87be77c325fd5a01741a5344f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2492943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5547ac00d56750c3a39284d3a968fcaf81fe64d1e1b645d4fc29f2784114e313`

```dockerfile
```

-	Layers:
	-	`sha256:3f49c5d4f12d985ab84ff327c5939931a80bd2c265b4579f7d009b60885e6dd0`  
		Last Modified: Wed, 21 May 2025 23:44:12 GMT  
		Size: 2.5 MB (2483738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:625daadf35c8b9bd95cf26a7710d90e74d3cc5005e02040cd1f96e8141575aa6`  
		Last Modified: Wed, 21 May 2025 23:44:12 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9` - linux; mips64le

```console
$ docker pull hylang@sha256:4865b75b1adca3ea738891c769071da9ed7d50785184b724bcdf3f06b3d1f9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49710196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b27f0848764d984a0d27bb0bce805e5035299bbf2f00b74c550e1ec0885f67`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 17:12:13 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1745798400'
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 17:12:13 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_VERSION=3.9.22
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_SHA256=8c136d199d3637a1fce98a16adc809c1d83c922d02d41f3614b34f8b6e7d38ec
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:901060d913f9d0bbb82847b3b60c3a263ed0dac4f75aa29161be6ed89b57082a`  
		Last Modified: Mon, 28 Apr 2025 21:11:19 GMT  
		Size: 28.5 MB (28514138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcdb53dce0796afc0fe942ceea6871583e05d0f52eacee78be8e3e338b38dcb1`  
		Last Modified: Tue, 29 Apr 2025 17:43:02 GMT  
		Size: 2.9 MB (2907098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20de79e7d7da51db3d67b12ba1cadfb2d5a05d7b9b9c6940c5f045468ad2fbe4`  
		Last Modified: Tue, 29 Apr 2025 17:43:04 GMT  
		Size: 14.6 MB (14617329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fca948d1d5f9fd3945561fc91f5827e874d6120560f1bc27d9f6e08aa687543`  
		Last Modified: Tue, 29 Apr 2025 17:43:02 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b5c538582a5274fc5798bb0b71b2d0b70eaa947089ea7114012a6c6c94176d`  
		Last Modified: Fri, 09 May 2025 20:05:09 GMT  
		Size: 3.7 MB (3671376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:2ce9fc09f6d18823550b59f7989a2c939c983dcd0a1e3dfbba1595fced3bd4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f694dc44475406b14c405d03858779cddfe3d09de807439f8e6cf76e587bcf0`

```dockerfile
```

-	Layers:
	-	`sha256:180af86a14e4671147e841e85db3f3e9b3b1b8de933f42da4c1ee9cb4f47f6f0`  
		Last Modified: Fri, 09 May 2025 20:05:08 GMT  
		Size: 9.1 KB (9144 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9` - linux; ppc64le

```console
$ docker pull hylang@sha256:5ea56989855a1c1ccb5b6e97ade1c5b353bea7e0e6871aa2e4bff2172d9c0ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (54992085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bde4de79443b1209c10d9b9423691a1e88968e3cad1f0801dc09eeec2e43b0b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 17:12:13 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 17:12:13 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_VERSION=3.9.22
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_SHA256=8c136d199d3637a1fce98a16adc809c1d83c922d02d41f3614b34f8b6e7d38ec
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14081b1afe897cce9676c9df550a4ef4deae350ae7ce3f01cbaf00ca3d0fc44`  
		Last Modified: Tue, 29 Apr 2025 02:44:59 GMT  
		Size: 3.7 MB (3713706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8fc7d10d63a1e4e234b94efc2d065bb7a65998b15784a605627909dc9ecc91`  
		Last Modified: Tue, 29 Apr 2025 03:18:58 GMT  
		Size: 15.5 MB (15538917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9666187326fa45f8ea1d07124d2b51b9d221f766eef7d9605d126f1b863f2c4c`  
		Last Modified: Tue, 29 Apr 2025 03:18:57 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3578c9320740d5dc1c78120d416c7b35976836dc9fe3d38ef9af0dd562e37e`  
		Last Modified: Fri, 09 May 2025 22:48:43 GMT  
		Size: 3.7 MB (3670770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:66776b48657738b868b2872a93c249d58f3dbc70f47e268f9a810d5d944abd24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2479643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de36bb4acb609f8f3a48ff7cb93cd19e6d932aa36077e150cc3595283b6e59c`

```dockerfile
```

-	Layers:
	-	`sha256:72f2023096fe31ba928392ca639a4654c0968360a2c09dea5c8376ab8ca20b69`  
		Last Modified: Fri, 09 May 2025 22:48:43 GMT  
		Size: 2.5 MB (2470318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:296ed07d96a8d6224518843fea764052c6bcda2bc9465f16cacb1fbd8f59da4e`  
		Last Modified: Fri, 09 May 2025 22:48:43 GMT  
		Size: 9.3 KB (9325 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9` - linux; s390x

```console
$ docker pull hylang@sha256:9da61306f0639253e822536fa2bf8fb0cc75d07d0e0e72d3854384e7cbeaecf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48449946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9add53d60907c20f922fb1f9c16efb697eb6964aee455252471f89ab9ca8f26b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 17:12:13 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 17:12:13 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_VERSION=3.9.22
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_SHA256=8c136d199d3637a1fce98a16adc809c1d83c922d02d41f3614b34f8b6e7d38ec
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d718881e7dc24c84b353b68bbc5ea4d8da2442eab69433253c52d5adf961304f`  
		Last Modified: Thu, 22 May 2025 02:58:20 GMT  
		Size: 3.2 MB (3175300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f37d005028df240b819a5c70abb684e39f646d871d5889dbc8b5fe287eef71`  
		Last Modified: Thu, 22 May 2025 03:22:18 GMT  
		Size: 14.7 MB (14721025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989a47dfe9a73fda4f090ed809fee50c126d14314fea03f969886b86222d45ab`  
		Last Modified: Thu, 22 May 2025 03:22:18 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96160e754295742a45fbc03e43b53bb03f3160e135bb6dfcd07effa6a73939c0`  
		Last Modified: Thu, 22 May 2025 06:26:09 GMT  
		Size: 3.7 MB (3670566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:31c1bd64f7f49a8779cbe266d7f6586a6ecb4269967ef3dfc2fc3dddecb49af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2495570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23d798fa26b3e8078b8e2784cf2629968e384d1b74900013b60fab3bf18edad`

```dockerfile
```

-	Layers:
	-	`sha256:193b46136251230a01297eb52ff2853ae131257f8652cdf27f675829f1212cf4`  
		Last Modified: Thu, 22 May 2025 06:26:09 GMT  
		Size: 2.5 MB (2486315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f05915e71418be2a615aa4f8b9aea2792b27664750460b01993aa1ba5a0924`  
		Last Modified: Thu, 22 May 2025 06:26:09 GMT  
		Size: 9.3 KB (9255 bytes)  
		MIME: application/vnd.in-toto+json
