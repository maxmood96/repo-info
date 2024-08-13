## `hylang:0-python3.9`

```console
$ docker pull hylang@sha256:96b1e9ebfcb18b73b1d692e11afa444c839e89e9d85a961a47c9ef042576f8d6
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

### `hylang:0-python3.9` - linux; amd64

```console
$ docker pull hylang@sha256:a0b0ad29cf164db3a5b3346f0e9f80254e6ad46dd2bbc4ba9a8e41ce393b6c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50948750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666511607dd32c2648149abef8508ff305b18951369eca2e2b0b6e8227696afe`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.9.19
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be20a4ff2774cd684d410f8ea49b03991524f012d2f5a93e1ef573451b2bd6e`  
		Last Modified: Tue, 13 Aug 2024 01:15:55 GMT  
		Size: 3.5 MB (3509927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48174a2f2dd9bbae1a67ceb64b7ab049fe8b392f1a6aae6937152c034ffcb138`  
		Last Modified: Tue, 13 Aug 2024 01:15:55 GMT  
		Size: 11.9 MB (11890571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb9f64d8db64a7b5c5f6aa8ee563fed15ae2df77f1659eb143d0d6f5ee43573`  
		Last Modified: Tue, 13 Aug 2024 01:15:55 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9140ff79093c868190cd8e242ae1738f9fe734fd53081717fd559b8268cf3d3`  
		Last Modified: Tue, 13 Aug 2024 01:15:55 GMT  
		Size: 2.8 MB (2773873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96c8789aa554d0c27fb662819052918b47a7a5d45f1f4cbe2c0bc9610f23a71`  
		Last Modified: Tue, 13 Aug 2024 02:17:29 GMT  
		Size: 3.6 MB (3647915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:ab98d0d21ccc99d10339634a145e32328b75abd908b8ccaa624173b8229f7129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8cbc661e8f6e364c68587f5acdbc4d7ce2d3491e273b677b7a1e832682c472`

```dockerfile
```

-	Layers:
	-	`sha256:c188e019f8205bee602d33e62e625c2f410ce373fa0378654d85244e548af73c`  
		Last Modified: Tue, 13 Aug 2024 02:17:29 GMT  
		Size: 2.5 MB (2457817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7ae645cd4579de145d24a7aabd00ad63b0a0b64798abba38dcafc381deb254b`  
		Last Modified: Tue, 13 Aug 2024 02:17:29 GMT  
		Size: 9.7 KB (9735 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.9` - linux; arm variant v5

```console
$ docker pull hylang@sha256:e5e2fdbabaf8ee9cbf3d53b19d7e3a3371403ea457ae57e82de4374bb528d4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47823646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2d6684a4975395e3f6c7187d55eeaebabfd40b50f3f235dcf8cc9e729a11da`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:752589c0ca446e2e74ef0b8c412eabb01e2a8035cfec47b1d9630b9f704fbda7 in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.9.19
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b695a3453560aacd42060f43ccf1cbd7d20412f50126ca6a469af38d3fe1e5b1`  
		Last Modified: Tue, 23 Jul 2024 00:01:19 GMT  
		Size: 26.9 MB (26887299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652c16af5bfa1219d86389da98bf2114b0fa0c2c34f86882d98783c006e6ce4a`  
		Last Modified: Tue, 23 Jul 2024 14:19:00 GMT  
		Size: 3.1 MB (3080511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598b854e4608d05b4b9bd302c2e18a9ed204cea99c7156175bd447465cfe9f30`  
		Last Modified: Tue, 23 Jul 2024 15:35:00 GMT  
		Size: 11.4 MB (11431667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eaf20de0f75beb389a776c6b3f77719e6e2190d705cc8f07245989a5ac87fda`  
		Last Modified: Tue, 23 Jul 2024 15:34:59 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e227ad674f796a03a98e6caa44a9b9665a71030bdeb9a735d3c931933fcabd85`  
		Last Modified: Thu, 01 Aug 2024 20:27:12 GMT  
		Size: 2.8 MB (2772812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e95b31e3b1eade765116138da422096cbf246e0887cadab574a8869c524f3a8`  
		Last Modified: Thu, 01 Aug 2024 22:34:00 GMT  
		Size: 3.7 MB (3651126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:ddd2feec167c86fccc1242f952fc094c28191dfc3c365889ff82f533e0d9bf0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3294537ee400fe1f7be7dcf5ced0604ac4219f6bc735fab0200089fc7cb89047`

```dockerfile
```

-	Layers:
	-	`sha256:f6361656f6268c955d077f04535542388e7460657818f4c98111a60dd5225480`  
		Last Modified: Thu, 01 Aug 2024 22:33:59 GMT  
		Size: 2.5 MB (2461256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e59e746bb74991b8d09b8c6f36c06a0b5d5a72ee17c8b113f34627bfd8b55665`  
		Last Modified: Thu, 01 Aug 2024 22:33:59 GMT  
		Size: 9.9 KB (9855 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.9` - linux; arm variant v7

```console
$ docker pull hylang@sha256:a6e28b9bc4510547bb7c6daabb89b6bc2f3b4a0452e8904faae8d9efae462b49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45086916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28226d8500ba512b50cd719a69a015e506b9241f71888d722794df4206fc2e31`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.9.19
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9e89a9a0ff00898681ed65fdf1b4314005b314abcdccf71af481df01c0b68`  
		Last Modified: Wed, 24 Jul 2024 08:52:42 GMT  
		Size: 2.9 MB (2912163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f06a41bd33215352aa6bf454537fd41786e14a5e892737475b631c68ed392b8`  
		Last Modified: Wed, 24 Jul 2024 12:38:25 GMT  
		Size: 11.0 MB (11032894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3167cb0da8b8572deb4da0783993f29e0a6d930e0f6e54a2d3817b3c585fa4c`  
		Last Modified: Wed, 24 Jul 2024 12:38:24 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd2e351ce5e22ebac6d656b271bf73d870ff4357f283c46f22048603e7730b1`  
		Last Modified: Thu, 01 Aug 2024 22:56:02 GMT  
		Size: 2.8 MB (2772389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337369a9c2a28051a97a9d79a0455915e4e9b6cf7ec872d303b61069b997e886`  
		Last Modified: Fri, 02 Aug 2024 02:28:05 GMT  
		Size: 3.7 MB (3651037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:013b625d651321d8d95c23de3af68c1c3f84d63ce918d7676281277e15cf7376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55cc16b10a147c0b219e44ac91f2a3942bf0f0a51197ad7060be85788786b25`

```dockerfile
```

-	Layers:
	-	`sha256:defbbf860afb359887d239f25abeb66198c455e5a7e6a35c68e7ce8fff6974cf`  
		Last Modified: Fri, 02 Aug 2024 02:28:05 GMT  
		Size: 2.5 MB (2460123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16a8d4b9614dc87fa353cdcb3e3fb04dc0f3616c4220c16b6660c96df45577e3`  
		Last Modified: Fri, 02 Aug 2024 02:28:05 GMT  
		Size: 9.9 KB (9855 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.9` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:8c5ff05109d07b344d25da2fd2c47b2e4deeb4cf71ca25eca364582bb5472556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50772415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebc490298166d6321fd9f85b14910a4736e4d862056e415641fe732b547f5a2`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.9.19
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba32bf0f91fccf36472f9ad3da47b1bd3638fa0c80d026ea6a6a5571ce334a12`  
		Last Modified: Thu, 01 Aug 2024 21:16:03 GMT  
		Size: 3.3 MB (3329912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e161aac9bcc413c9cb1cd0b1799bd1c8df60e08b94062f709b45b08709300103`  
		Last Modified: Fri, 02 Aug 2024 02:57:32 GMT  
		Size: 11.9 MB (11861636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cb38e67018cabd2ea2afeaf699ac22eacb99cc8fc12ec59a47526de3c6c486`  
		Last Modified: Fri, 02 Aug 2024 02:57:32 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656bfe61e2c88e890e8cb449548e5400c70a5e6e6085f85fc47cb4df00309f72`  
		Last Modified: Fri, 02 Aug 2024 02:57:32 GMT  
		Size: 2.8 MB (2772989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0906a27c03cc5f6683238b20e5340554265aa5af3c0ffea2f9797d364435498`  
		Last Modified: Fri, 02 Aug 2024 05:56:05 GMT  
		Size: 3.7 MB (3651074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:f5b40107f779d27d5099be297ba513d2ae386fbdc43c8d246286e6ca70626fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6b1bbc81c6a91cdf2c4cd7ac5966e59c226a1d81591c91f445f922554f041e`

```dockerfile
```

-	Layers:
	-	`sha256:51449061b3903422bb17dca9213f77d4c5791ec882c6b28de54586490d2811b0`  
		Last Modified: Fri, 02 Aug 2024 05:56:05 GMT  
		Size: 2.5 MB (2458139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4250a69c181af32787e889917e7dd059f80a2b461a613d3220dd9108b10305e0`  
		Last Modified: Fri, 02 Aug 2024 05:56:04 GMT  
		Size: 10.2 KB (10180 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.9` - linux; 386

```console
$ docker pull hylang@sha256:43c25f3619fdce9dc9cf752e4f08877d0a11d03af2629eae7cd5f614ed1217de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52225917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01eb3fb69916e4404994314c94116946eb462725d1aaa6fcd554d37fd7426fe`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:6c928b979f82a9dc0b3801b97a516aaa3d17fe57cb9eecc077d202afda56d2fb in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.9.19
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:82c8eed510ac33a6df3a546a738b1f3806df7958ea977484d0f77eabe177108d`  
		Last Modified: Tue, 13 Aug 2024 00:42:35 GMT  
		Size: 30.1 MB (30144281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d9c3c58c3dafebacbcc8f197dcc99d254ba182fab9e8f200d7d2f8a109ba1b`  
		Last Modified: Tue, 13 Aug 2024 01:16:36 GMT  
		Size: 3.5 MB (3507325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7322e48d327a7fc478edd40943c56bc513a6d888342881c941b67412618c767e`  
		Last Modified: Tue, 13 Aug 2024 01:16:36 GMT  
		Size: 12.2 MB (12152871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc4ff01b3b2ee3d49e117403fe4409a8ec142baa61df9ad707d7eb080c8159e`  
		Last Modified: Tue, 13 Aug 2024 01:16:35 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40861ccfc0b1c07f49fac8c6499b4783afcc1621b2e88c20fa4686832e88b4c8`  
		Last Modified: Tue, 13 Aug 2024 01:16:36 GMT  
		Size: 2.8 MB (2773363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932a0cd9c8896e51066b84df0a7366a3d59055ba981f370821e801b1345a1c4f`  
		Last Modified: Tue, 13 Aug 2024 02:17:21 GMT  
		Size: 3.6 MB (3647845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:fe331c6aa859ed273b03afd8fed64dd5378412e1beb4f03f4ca7d2e3d0a2be2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443008262c345498d24c33595709511d02eea92fed3ab3b5bff11607e168eaa8`

```dockerfile
```

-	Layers:
	-	`sha256:baa097524eeece1df25fff66052e37ada2e6d6b6dc731cb9f90ac4550965d021`  
		Last Modified: Tue, 13 Aug 2024 02:17:21 GMT  
		Size: 2.5 MB (2454891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a51fa29d0ecfda69bc67b1cc583bc9363eb00f8d132a22193b9b1368311b9b4`  
		Last Modified: Tue, 13 Aug 2024 02:17:21 GMT  
		Size: 9.7 KB (9683 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.9` - linux; mips64le

```console
$ docker pull hylang@sha256:87615235d83877bb20fcd8e53ba98ae6ed97fd6b7a5e5beb74a7a18d276cf4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50127101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e955215358251088f177d93c6773d2a52dbafc0391aac989d4db4e6f6a7de9e4`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:6b0de87e15c6880fed3a8430d23a511322519e32c50677c24f4597141e3a85ff in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.9.19
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f8de7af9de8596141237ef7c589f08f773ca8ce07671b2bd7e192055d5165f74`  
		Last Modified: Tue, 23 Jul 2024 00:49:06 GMT  
		Size: 29.1 MB (29124926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b568c54b892960e195cfc213cb142b5b987ae04aa6e353d0b08b6a31f0d2a570`  
		Last Modified: Thu, 25 Jul 2024 08:43:28 GMT  
		Size: 2.9 MB (2905088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22ea30d2c30ec621e9cdbee2e023043c7e00125636ce9c8ca5c6ddb14153823`  
		Last Modified: Thu, 25 Jul 2024 08:43:30 GMT  
		Size: 11.7 MB (11671916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59eeaa92843fa1e406e6a281a10a6cc2d5bd6b5744fe277e7ab0188b49948e31`  
		Last Modified: Thu, 25 Jul 2024 08:43:28 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb392a36860249686626ce0f3ce536b89635c49c3cf7142124a6717904db52d`  
		Last Modified: Thu, 01 Aug 2024 18:02:36 GMT  
		Size: 2.8 MB (2773306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2be9883cdb037d907888890c5e21dbf5dffff20c4d45d92805fe49e0c832413`  
		Last Modified: Thu, 01 Aug 2024 18:59:17 GMT  
		Size: 3.7 MB (3651635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:80c8dc9df8a1c1102fbcf494625ab5f976e59d0241387219440c7b7c1928a1d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8019a115ba39fe97d514e557e7cc4502495b56fea108d2f35276cc209e2372c`

```dockerfile
```

-	Layers:
	-	`sha256:18998dac78cf563ce790d10a2b24d1015478ac162c887ae4deb22c8711d58cb5`  
		Last Modified: Thu, 01 Aug 2024 18:59:16 GMT  
		Size: 9.6 KB (9630 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.9` - linux; ppc64le

```console
$ docker pull hylang@sha256:3d4dc345847193ce9e5a40a0a97878c56bbb6d901d7fe29d81e3d7f89bd3f2ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55728642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366660b482407e2a803a923d6a55e432045264a7254202c4c7d96dbeac2dab5b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.9.19
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00727597bf5fb6407a0ed311ead2327da6f7ba9c8bfbef711680ea567fa867a`  
		Last Modified: Wed, 24 Jul 2024 05:26:08 GMT  
		Size: 3.7 MB (3708173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac17c8096b54338dd58654f826e162490472815ca4fd72e3313252f8bcbb0101`  
		Last Modified: Wed, 24 Jul 2024 09:19:04 GMT  
		Size: 12.5 MB (12473433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892948d99c3e384c10b78a658d93c541531fbe66e22b627f30fe181521d22d0a`  
		Last Modified: Wed, 24 Jul 2024 09:19:03 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26735c19a56d0d1518762d6363789ee56c3a905793d7422e4b9a040deb584619`  
		Last Modified: Thu, 01 Aug 2024 23:40:22 GMT  
		Size: 2.8 MB (2773314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c1c39486fca6d79c28b3b6bcfce110e5555c24d177e56de56ba14c8474b05e`  
		Last Modified: Fri, 02 Aug 2024 02:06:58 GMT  
		Size: 3.7 MB (3651215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:98db444f57b5ba4bb6b040798fa2b1751ccb9bbd37b0df61fd63beb0be1b77d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d3bf544bacf6cf13fd8c522d63cb64c520015d0d6a468940ea235bf42be80d`

```dockerfile
```

-	Layers:
	-	`sha256:0c1940931ab933bcfe4a3983fb41b8446765e6459b8d45202fd669a115b660ec`  
		Last Modified: Fri, 02 Aug 2024 02:06:58 GMT  
		Size: 2.5 MB (2462244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c21c21b5413340e5ce12b22c0f88a2dbfc09930a03b0f170db4e4e1d89301f`  
		Last Modified: Fri, 02 Aug 2024 02:06:58 GMT  
		Size: 9.8 KB (9815 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.9` - linux; s390x

```console
$ docker pull hylang@sha256:3a435fdb15e507d0547ae58b3033f493763f23b83666caa48f375e967790570d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48862164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64e2ae2a500f67477f9b664964cc92480be4bd327e9cefd012b54446dde092f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:d8b037f30c0a2aeded43f72fe61531da3a0e449e034255bb0a7b2182e4e3ca8a in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.9.19
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:48319744c6dacda7d13413becf85a83639982e97ecf615295a1257ccc3082721`  
		Last Modified: Tue, 23 Jul 2024 02:32:44 GMT  
		Size: 27.5 MB (27490099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b51cfee76bcf61f72507ba36f6a5fe1af8c1828b22e9ca6a55b6d993f364cc`  
		Last Modified: Sun, 04 Aug 2024 13:12:39 GMT  
		Size: 3.2 MB (3170502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3081006a195ed39b906e668e9084f970c7ad65c95cf6c4826471a04bdb3e5cce`  
		Last Modified: Mon, 05 Aug 2024 19:05:08 GMT  
		Size: 11.8 MB (11779822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a1e79cf74b30447119290e17bf810e9770d3e5b8dffe3644045996dcd6e186`  
		Last Modified: Mon, 05 Aug 2024 19:05:08 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ee650c6733a634911f5d452200336a390130076d5428b17c77dfa6559b30ce`  
		Last Modified: Mon, 05 Aug 2024 19:05:08 GMT  
		Size: 2.8 MB (2773585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ae402c060713250dc47ae73add0603c14f32cfe25831b7f8c4cf57c0a6d870`  
		Last Modified: Wed, 07 Aug 2024 00:15:57 GMT  
		Size: 3.6 MB (3647923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:464a9185d408582c6a7b7619bf78e260307fd499141f01786160a7698842c58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da50ebf85132b68bc50b45e8c6091b1c6ca12e1b2f03a29185e87404c585da4`

```dockerfile
```

-	Layers:
	-	`sha256:abd34ffbbf74f081c01fd0d5870ffe32dc2fccca3fc540924240c69207a102e3`  
		Last Modified: Wed, 07 Aug 2024 00:15:56 GMT  
		Size: 2.5 MB (2457630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436b50df868b405181a6ef4bad9563e3f7ea71082b1c507d768277e41f668029`  
		Last Modified: Wed, 07 Aug 2024 00:15:56 GMT  
		Size: 9.7 KB (9747 bytes)  
		MIME: application/vnd.in-toto+json
