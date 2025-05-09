## `hylang:1-python3.10-bookworm`

```console
$ docker pull hylang@sha256:b50400c96dfa268255b64297d3ef16e30862b459f28eba456c228768b8d27107
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

### `hylang:1-python3.10-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:8f8f122148ce1c3a4b554f6d7b7375af14f6c4c601a6d5fde2c51bb13cd05165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51573283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312180a4c4a8ad5273576c728469fdf4512dfe8250d69cfc43266f5c96a866c5`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 17:12:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 17:12:13 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_VERSION=3.10.17
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_SHA256=4c68050f049d1b4ac5aadd0df5f27941c0350d2a9e7ab0907ee5eb5225d9d6b0
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e5f9e5de64a1369423a10d83393bf1a3533dd76c039b32cb0251bffd7ae33d`  
		Last Modified: Mon, 28 Apr 2025 22:11:19 GMT  
		Size: 3.5 MB (3511514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765ef9c81879b3bfc7185726a38c8b3531b80fc48d6e54d8725a6cabf02c60e1`  
		Last Modified: Mon, 28 Apr 2025 22:11:20 GMT  
		Size: 15.6 MB (15649095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15668d6a1de27ac749c4d14e5aa7769b29e8853056f3f17e0678fa13aae1812`  
		Last Modified: Mon, 28 Apr 2025 22:11:19 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089adbdeaa5c5d29b92538b1466cdd2b44d58923308b32d39d6660aaee1b524b`  
		Last Modified: Fri, 09 May 2025 17:37:42 GMT  
		Size: 4.2 MB (4184784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:cff734e137620bc395c5d5f45da3c50ef4fb11b596372b5c0508bd9dfa66d1d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2475243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c33dc24639e3b3e7bf881637899cc3161a05553e4c11390cefb19e353adf16`

```dockerfile
```

-	Layers:
	-	`sha256:1e88548fd7f7d618103a9e9d9ac36fbbd6c0460a27d91d6dd8838e867ded6eb1`  
		Last Modified: Fri, 09 May 2025 17:37:41 GMT  
		Size: 2.5 MB (2465968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef42219a32b3f0904d8bc72776107c2e5ac1438b9b040e9d7eee52864d82d9ec`  
		Last Modified: Fri, 09 May 2025 17:37:41 GMT  
		Size: 9.3 KB (9275 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:b5188a46cfc6f8855fd0860d1a2230cef10c63b06a4bd67367f4fe4607b0c03e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48126235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aaddc668d91f305afcf527d46dea7a8c6a2e9e172c40537c80d2b4dade0a742`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 17:12:13 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1745798400'
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 17:12:13 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_VERSION=3.10.17
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_SHA256=4c68050f049d1b4ac5aadd0df5f27941c0350d2a9e7ab0907ee5eb5225d9d6b0
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
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
	-	`sha256:3bc532ff9d2a2a12c6cfc746359843257a240960865aea7ecb10c71e0b93ec78`  
		Last Modified: Mon, 28 Apr 2025 21:07:56 GMT  
		Size: 25.8 MB (25757836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd3f52acbe9abc4f7abed187506e721554093a556b5a4a20128eb901cf2806e`  
		Last Modified: Tue, 29 Apr 2025 02:34:30 GMT  
		Size: 3.1 MB (3082299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1bd83ff4894fe14aa0ede28424c88bb1dfc328e61b3a080d7316961d66b1e6f`  
		Last Modified: Tue, 29 Apr 2025 03:03:02 GMT  
		Size: 15.1 MB (15100674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ad0b5f9dbf6e18a941b26de28eddd3753c2fe9413abe42350fdb46a76e7cb0`  
		Last Modified: Tue, 29 Apr 2025 03:03:01 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d846ba4a2d394e564081199ba1a812b8af93afe52dbdd7e2ee60ad01eea3a17d`  
		Last Modified: Fri, 09 May 2025 17:53:07 GMT  
		Size: 4.2 MB (4185177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:ea13ca033174400d5e376f5005dd597688c1d3ad423e141253dcdd37360c4d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2478897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda68e52a93e90a76765f82b0fbff787ad24833eaa3cc194d3262aa01c993b5a`

```dockerfile
```

-	Layers:
	-	`sha256:343682015e78d24ba0346cbb8e0734742432e18e77de62d3d62180a9c790eaec`  
		Last Modified: Fri, 09 May 2025 17:53:06 GMT  
		Size: 2.5 MB (2469512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f1874408454e83cfb8d8cef8a0485f44509c202e73f184909db43dd0507b1e0`  
		Last Modified: Fri, 09 May 2025 17:53:06 GMT  
		Size: 9.4 KB (9385 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:6878e6dc49e4ba7acef9d2c1ed165d9fdb7ebb5e33f6246aae05fb04fc0ad2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45726238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55a8e6cc14491a9c366dc4a15e9717b4d16cf7c188d1719a080130fd35c5cd0`
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
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_VERSION=3.10.17
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_SHA256=4c68050f049d1b4ac5aadd0df5f27941c0350d2a9e7ab0907ee5eb5225d9d6b0
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
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
	-	`sha256:3150eb01d81e65cc6548f4bdd78acf9873928df6a91385dee5818b77ac61228d`  
		Last Modified: Tue, 29 Apr 2025 08:50:28 GMT  
		Size: 14.7 MB (14688042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab4199316906eba7326d0a17a03af3380c5fb50a7ab38367e719330a4d43995`  
		Last Modified: Tue, 29 Apr 2025 08:50:27 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127bd5cb6607f83ddddeb2c70c4211843c9005133c710fb01a4d3ce0fdbf35a5`  
		Last Modified: Fri, 09 May 2025 18:44:49 GMT  
		Size: 4.2 MB (4184993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:de2df488c64ce6b171038f3089aa012932006f73bf377d6826664ff3f5ed4f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2477654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4079376b42446b46046c698e5bf0614077f79d12f6787146ebc6524b3b10cda`

```dockerfile
```

-	Layers:
	-	`sha256:9961075348961b4c2b6f3378ed7b923359ed29b7d10b8dc54ea6313879f4838e`  
		Last Modified: Fri, 09 May 2025 18:44:48 GMT  
		Size: 2.5 MB (2468269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ba4f737cade9b3da331c8028d19ea43333f6258b1e69428fd92efcb22f24a46`  
		Last Modified: Fri, 09 May 2025 18:44:48 GMT  
		Size: 9.4 KB (9385 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:6bd9e66eb9fbb4d4deb30e60a2f7c2a64c2a5371e3ace8964e20547902c10e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51149010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29466973f81a48527184a9336de4146ec1a633886dda0ad7585c4c9aba9c9ac3`
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
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_VERSION=3.10.17
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_SHA256=4c68050f049d1b4ac5aadd0df5f27941c0350d2a9e7ab0907ee5eb5225d9d6b0
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
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
	-	`sha256:501be45329d77435987a90b22e080ea5b202618497f0318af849d9b0bdce44d3`  
		Last Modified: Tue, 29 Apr 2025 23:49:05 GMT  
		Size: 15.6 MB (15565048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8651daaa9ee30d413b7eacc7eea6a10afe597f1954aabef4a3581e421c50034`  
		Last Modified: Tue, 29 Apr 2025 23:49:03 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea347c1e706b2a3325658adf883d18476995774a61f993f82f2935c87988d8b`  
		Last Modified: Fri, 09 May 2025 18:56:27 GMT  
		Size: 4.2 MB (4184983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:013158cc53178c05181e5c873ac5489fdde903f45a6e5dccd4d1f12a8b1b6604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2475717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3407f71e8d1c0a8b5f65b2f4b62f793de184fd266a89c8fa0e6b636636244d5`

```dockerfile
```

-	Layers:
	-	`sha256:4780cdbb8302421e2a160f733ab5d0bdb6f5f032f6f03bdb523eaf446de850d5`  
		Last Modified: Fri, 09 May 2025 18:56:27 GMT  
		Size: 2.5 MB (2466289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9259d949ce69434a2b2ea2d3d37f3feba72dd43ee6a281a09c7d74c3a55a1c2`  
		Last Modified: Fri, 09 May 2025 18:56:26 GMT  
		Size: 9.4 KB (9428 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:dbaeeafb7deefb3552203723bfb55c9f43f9f0c748ce8fce975778a1f4e62632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52797531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cccb4aa380802e1a49bade586bf8f9d3602fa8bc6253ad1e2fc07a7c9f995837`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 17:12:13 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 17:12:13 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 17:12:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_VERSION=3.10.17
# Wed, 09 Apr 2025 17:12:13 GMT
ENV PYTHON_SHA256=4c68050f049d1b4ac5aadd0df5f27941c0350d2a9e7ab0907ee5eb5225d9d6b0
# Wed, 09 Apr 2025 17:12:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
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
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad86352255b2d2d1f2b7391aa6708c1a0f3f8bdb52c591b70d26aa206829531`  
		Last Modified: Mon, 28 Apr 2025 22:18:37 GMT  
		Size: 3.5 MB (3509857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b723dadf1ff43c904bb7e5586fcb3c20abeaeadc1708f68d59f03489a966353`  
		Last Modified: Mon, 28 Apr 2025 22:18:38 GMT  
		Size: 15.9 MB (15891599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05728c708481b02370e7934a6077411df7fd7603e48ecb35513b4f0b02b77e4c`  
		Last Modified: Mon, 28 Apr 2025 22:18:37 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47374cccd56c02a65b3972c12121506ea670dcf1899d2b19aa468971b987f79e`  
		Last Modified: Fri, 09 May 2025 17:36:45 GMT  
		Size: 4.2 MB (4184959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:02671842e83a0fcf2db3952ab3ccbf2c539cd96cbec3020782302018105dc5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f3380c7184e564865b3812342499cfb24bb78717de13756caa8825f3608cf9b`

```dockerfile
```

-	Layers:
	-	`sha256:c75e17160b927a268bdb5f5c22c75790806182a2a9e2fbfa5e757abb76a9fae8`  
		Last Modified: Fri, 09 May 2025 17:36:45 GMT  
		Size: 2.5 MB (2463048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56d6ab38bad38de9c4d522695bea530d27ab6c7d49497bde085ebd0d99aa520e`  
		Last Modified: Fri, 09 May 2025 17:36:45 GMT  
		Size: 9.2 KB (9225 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:c182208ea7a742e078aa575d8052fd1afa5010234da542ae45eba38b23526437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56233527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fbb4c77d2db29e60b7b03096ef0d61230c3ed2a43bb2ced6aa87c8efaafb413`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 17:54:43 GMT
ENV LANG=C.UTF-8
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_VERSION=3.10.17
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_SHA256=4c68050f049d1b4ac5aadd0df5f27941c0350d2a9e7ab0907ee5eb5225d9d6b0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
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
	-	`sha256:250acd947c00a8dba79c2128a1eff9c2c2931c347ee55c783cf5e958d587470f`  
		Last Modified: Tue, 29 Apr 2025 03:12:31 GMT  
		Size: 16.3 MB (16266696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903535a51f1bb9f10c2bcdbc7834298339186f4cb9906450a8d9f88c5ae3b8d1`  
		Last Modified: Tue, 29 Apr 2025 03:12:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4516f552e1c79820fd99134246f69a4bb0b7964bfcfedcc73881c678564e9b53`  
		Last Modified: Tue, 29 Apr 2025 08:15:14 GMT  
		Size: 4.2 MB (4184433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:f27f1053ec2d2bd05b79e7a30f55ab86b4a85e32ee28671ef8d77a4590ae029c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2479729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d4d30a45ed7be3e13ab3fd01527ec50ba7abf7a6976cb48507535f02d6594f`

```dockerfile
```

-	Layers:
	-	`sha256:98b93e651a9cc1d15f9351081ab0a4d4810a55ba2a9b288d0755ffc1f9fabcf5`  
		Last Modified: Tue, 29 Apr 2025 08:15:14 GMT  
		Size: 2.5 MB (2470384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e54274a5bc8341abc6330ed338f74d04f9b10b3517581829627dabf47178c7db`  
		Last Modified: Tue, 29 Apr 2025 08:15:13 GMT  
		Size: 9.3 KB (9345 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:106269238eaa86de132591bfcafdba97094f7cd2784b8fc63746add773cb6aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49682297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edcb26fc9a559ba2b22e3aafd0f181703426f362a8979c3819f557c75bd35d0d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 17:54:43 GMT
ENV LANG=C.UTF-8
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_VERSION=3.10.17
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_SHA256=4c68050f049d1b4ac5aadd0df5f27941c0350d2a9e7ab0907ee5eb5225d9d6b0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4bd54a9f3382d42e097f7db7e6c47d5b56175964eb40e170669bc0efc3af66`  
		Last Modified: Tue, 29 Apr 2025 02:08:39 GMT  
		Size: 3.2 MB (3173138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280ee85252ba87e5ad6ab3d385049c21f9ea006649a6196c0dbcd25cb8649410`  
		Last Modified: Tue, 29 Apr 2025 02:16:47 GMT  
		Size: 15.4 MB (15439835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c59f8e073f85ebf52d6a3d4599b2846c778d924a10da7bf2f2ac088e100a2da`  
		Last Modified: Tue, 29 Apr 2025 02:16:47 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3651dc31239526c184dd79fab1716dfdd090204054bb15b92fd0287a222a673`  
		Last Modified: Tue, 29 Apr 2025 05:58:06 GMT  
		Size: 4.2 MB (4184207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:d20dfe50d045b18f579d9d07cadbd6a91c12e67c5f6079eaa2441423a6cff0ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2474953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dca986f5d0ca28f754ab65ef8ce89e56c1e2d7f798f45949b39005839a13aee`

```dockerfile
```

-	Layers:
	-	`sha256:84f469de3fbb68c0c1b872351fdd7b53b9a9626cf56eaa6b263d230eeeba3f37`  
		Last Modified: Tue, 29 Apr 2025 05:58:06 GMT  
		Size: 2.5 MB (2465676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b615f170ab60794eec8473a6e08c9652d8ee5db676f17037e5ec246ec3132a03`  
		Last Modified: Tue, 29 Apr 2025 05:58:06 GMT  
		Size: 9.3 KB (9277 bytes)  
		MIME: application/vnd.in-toto+json
