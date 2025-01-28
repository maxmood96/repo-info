## `hylang:1-python3.13-bullseye`

```console
$ docker pull hylang@sha256:845d8e4dd7de946b0b387208b67f13c075e3cc204fb0c00bb96ebb94001b94e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:1-python3.13-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:9e7778ceaf3f14b996f7299536809852bec2a2b3e803914e54759472b6297836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49547571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f773c84101463ab3041c8b7bab05b1c64ddb3a6747071f8a407844844d439a`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PYTHON_VERSION=3.13.1
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	test "$gnuArch" != 'i686-linux-gnu' && EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f166dd5356b4575633cb31a28767e5e1513ce4a1be9088eec3182650de99bd`  
		Last Modified: Fri, 24 Jan 2025 19:39:10 GMT  
		Size: 871.2 KB (871216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e190cf68396399bac2bbd854c7ab01e4517e063d69736fcb201b2b93ee25457d`  
		Last Modified: Fri, 24 Jan 2025 19:39:11 GMT  
		Size: 12.7 MB (12743705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c22742305ff0fb4bd13b96c923fd8e8ed98a62512795e088df54a14c42cb40`  
		Last Modified: Fri, 24 Jan 2025 19:39:10 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a082b852f77c288fc0378d7e5bd9ba687a9f83795ae36c85925c3c572527eb80`  
		Last Modified: Fri, 24 Jan 2025 20:08:13 GMT  
		Size: 5.7 MB (5679735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:6c5d9ebac11c23732db39529c7e509e5a2bf76c2aed75a0c0ad51c2e7a270553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18cfaa9afddf0d1b8536448ef1a69703e6e04f581efd1c540afa0f01e9753db`

```dockerfile
```

-	Layers:
	-	`sha256:6771d87b82511e896825b2476838676e4dbf120edee8d76ae9a14992dc868877`  
		Last Modified: Fri, 24 Jan 2025 20:08:12 GMT  
		Size: 2.7 MB (2711616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fb944884c9526eefc747c10b64594fd5590e697d2214010b39d9fa7bd474c2d`  
		Last Modified: Fri, 24 Jan 2025 20:08:12 GMT  
		Size: 9.2 KB (9243 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:e8ab01ff35857d502e1a4b90f531461330702e7cbdf1f93ae52b16d6a9d558c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43946319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71a3ed91fc64d6bd310aae9a7e22b2d222823e266808b5695b4659b5f5bd765`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 02:30:19 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_VERSION=3.13.1
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da349cc9b59389845d7f146a6f3def31d2aa46a1032494954cdf3278f7077d37`  
		Last Modified: Tue, 14 Jan 2025 11:52:27 GMT  
		Size: 837.0 KB (836996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f05a7d962f873eaca2f8c6276fa31a5979d69c510142f965aee8730c8b112c9`  
		Last Modified: Tue, 14 Jan 2025 12:39:40 GMT  
		Size: 11.9 MB (11895254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b4165c1ad2e74ce8d91a8b86f44fc771d638f4c8473048e7f36635b62ab5b8`  
		Last Modified: Tue, 14 Jan 2025 12:39:39 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d2420e5b954338b80dff978a79a74d0040be9d8cbcf8ccdd119e8c94d23bce`  
		Last Modified: Tue, 14 Jan 2025 21:39:49 GMT  
		Size: 5.7 MB (5679859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:cb6d734aaaac9d3973b2ab2fda471f7dc0ae6110b3f0363a65c1c543e2039658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2723244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6825d5d3cb9a045d59d0c826696486735236b7b945c22f79fb8d2113cee3ee5c`

```dockerfile
```

-	Layers:
	-	`sha256:1c2542a1ec6ed6a63ea3d42d37d61bad3580cc21fcfd293c99a24484c8403a75`  
		Last Modified: Thu, 23 Jan 2025 05:09:26 GMT  
		Size: 2.7 MB (2713893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d16f5d7b918d0f2469366195da6951de4b766e53f7e41af6d361de176d70aaf`  
		Last Modified: Thu, 23 Jan 2025 05:09:26 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:e6fa95efa1e7c6579cf21325904f1471b9fabffc72073473965de4817fcfb1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48056103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a869c1692c73dfe528d4444222d6a453ef0567492407de7409e89fa1eff8ccf`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PYTHON_VERSION=3.13.1
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	test "$gnuArch" != 'i686-linux-gnu' && EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056ac591a050d805155fc120660521a3df4ac1d80fd654e4093acf209e4f024c`  
		Last Modified: Tue, 14 Jan 2025 09:41:03 GMT  
		Size: 859.2 KB (859157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249bbb7f956a08535c709ec1eb4ba9357c0574302adfa9da42f5d8c652de348d`  
		Last Modified: Fri, 24 Jan 2025 21:32:13 GMT  
		Size: 12.8 MB (12772177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a61435f030ad1b9d97f154f54681d9d3114be71c3eeab4a8cfd871a566e3d5`  
		Last Modified: Fri, 24 Jan 2025 21:32:12 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dd5e45dcf1344636020132a53957db022fa93af996f421538b4f893d1242db`  
		Last Modified: Fri, 24 Jan 2025 23:10:20 GMT  
		Size: 5.7 MB (5679607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:c4d0228fbad9de9f0e2843cae1ea53c4958bfc3c9eb807138cc4408f3c0ac887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2721318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f56c67b6d99e75fd872273cab54b2d70433f65b70a9bbb4143fc129cfab566a`

```dockerfile
```

-	Layers:
	-	`sha256:887c74a1099a299f54ec638e55c323377e2e6ba5bd102495482937d922227972`  
		Last Modified: Fri, 24 Jan 2025 23:10:20 GMT  
		Size: 2.7 MB (2711923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:929bbe07cbd639c7e3ceec460d7a1b1406c5630587fff6a2c3100c11c7496b79`  
		Last Modified: Fri, 24 Jan 2025 23:10:19 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:d1ab008f0e686ce624c9d06e300634a2ff94e7c0f7bfa6acfec476f40dd57acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50637050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929651656d63fd1b3c2be54ebe7316e73606d5b3698f8086f24486d015692880`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PYTHON_VERSION=3.13.1
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	test "$gnuArch" != 'i686-linux-gnu' && EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a125d4f3404f0ae309a257ad706fcefd5bef176020e3b257d791466aafc01c`  
		Last Modified: Fri, 24 Jan 2025 19:46:39 GMT  
		Size: 884.1 KB (884084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456efe768a70cd8c60ca14f326d95e7f36ab823257ede02579cdaa5545c22368`  
		Last Modified: Fri, 24 Jan 2025 19:46:40 GMT  
		Size: 12.9 MB (12893979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fec335deb60e55bff5c300a325d87aa29f71e5aef0bf410296b872a28050ea`  
		Last Modified: Fri, 24 Jan 2025 19:46:39 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50545b52b1126af37a0d56be87192793b50a38523c7a985c5abe2e227bd1d455`  
		Last Modified: Fri, 24 Jan 2025 20:08:03 GMT  
		Size: 5.7 MB (5679709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:a73bc6df6f697c89f5a17080f1ee9406d022993dc891ec84dbae264283c4fa74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c2e21244d7398a050544b10bde9c5ee70052bd3002d064df147aa1f52898bc`

```dockerfile
```

-	Layers:
	-	`sha256:fededaad4ba3df260356adf3a743ec802c4a6162fd9c88b6d454a73fea863072`  
		Last Modified: Fri, 24 Jan 2025 20:08:03 GMT  
		Size: 2.7 MB (2708708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4445819b41c320981b9cbe019e26de45ca1ba1f7d01feba9e317e29ed93165bb`  
		Last Modified: Fri, 24 Jan 2025 20:08:03 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.in-toto+json
