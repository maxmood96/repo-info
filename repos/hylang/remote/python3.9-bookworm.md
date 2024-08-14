## `hylang:python3.9-bookworm`

```console
$ docker pull hylang@sha256:eb377b0c2a56c8fabaf2ae9197a1046f5e3f2b258816b607fa278851d98ee1ce
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

### `hylang:python3.9-bookworm` - linux; amd64

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

### `hylang:python3.9-bookworm` - unknown; unknown

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

### `hylang:python3.9-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:1bacaca1c8a5aa4d3afcd572bbbd02857de6334666cba73cc98f79b9fb0243ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47821248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b4af8032f7a79f5afe9b24ca0b47edc7389eb1b4edcd3017e0bac32205a33a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:0a38a76ef88f0bc858f9663f2ec636121970b50fcd7a62192be7a7eba71bd6b4 in / 
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
	-	`sha256:1bc90b37f777aded897944b0ce596c103432c1b84f7b626b9fd4a53356f006da`  
		Last Modified: Tue, 13 Aug 2024 00:58:27 GMT  
		Size: 26.9 MB (26887303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf2571c7cc2e20cf84295a40f908bfe49458a3a670305f6fb4562a4fff4521c`  
		Last Modified: Tue, 13 Aug 2024 19:41:32 GMT  
		Size: 3.1 MB (3080563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d9ad14eb44d081f8459fa8b5e16b4db1e20e3a4c390468766b91dfb1b623fe`  
		Last Modified: Tue, 13 Aug 2024 21:54:04 GMT  
		Size: 11.4 MB (11431516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ac7d44c8b23671236560e8947db41c340929fd7f691153b9ee6984a8ffffb3`  
		Last Modified: Tue, 13 Aug 2024 21:54:03 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d15a0a578a3251072feb3a1eb0d51a6755a88f6e86da717bdafdc68f7cb022`  
		Last Modified: Tue, 13 Aug 2024 21:54:03 GMT  
		Size: 2.8 MB (2773662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1205960d6eee785dd7b65b7c8a5d0e75127dd52e0be550b200008ef26178c5b2`  
		Last Modified: Wed, 14 Aug 2024 00:37:23 GMT  
		Size: 3.6 MB (3647972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:5ce176dfed4866c926067c0ea13f06267a3aa2626e630951267f18c8363a0214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3851ccd1360318d949762ff70d5edfd76a17fbaf8eed9e89eaa708784d6094`

```dockerfile
```

-	Layers:
	-	`sha256:9c405c7b6b210ae0b034814d59907ef77b84465e83a3bb9e0de3d8d50ef5098a`  
		Last Modified: Wed, 14 Aug 2024 00:37:23 GMT  
		Size: 2.5 MB (2461256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8129efbabd335cd77787bb96f746c05b04abc38684bfee6830db2c9c4ebb392`  
		Last Modified: Wed, 14 Aug 2024 00:37:23 GMT  
		Size: 9.9 KB (9855 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-bookworm` - linux; arm variant v7

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

### `hylang:python3.9-bookworm` - unknown; unknown

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

### `hylang:python3.9-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:0bbaaeb56172b0e56d35afa26e6674cf1f1c4535568147dd51c554e9a5136d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50769759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8160cc8f5f44a91a898f864421b461321f6f9690860ffe8cb320af4dd3285eb4`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
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
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c8ca4554382886f5d683b411ea62b09aaa2c3915a506b4aca130d262e81ebd`  
		Last Modified: Tue, 13 Aug 2024 10:22:47 GMT  
		Size: 3.3 MB (3329890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0163ba53f5501df0b9705b562df60e5610e4b11df8bc087e23a3d22dba7c5b0a`  
		Last Modified: Tue, 13 Aug 2024 11:08:37 GMT  
		Size: 11.9 MB (11861367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb8574ef7df5e0c48bb1fab011dc7c2fc21db911d1c880bc9d4b05e64917680`  
		Last Modified: Tue, 13 Aug 2024 11:08:36 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3baf8ab11d00a0a1eeb68851a6d39a76138078d7ea7b63e059e3688e8d281a89`  
		Last Modified: Tue, 13 Aug 2024 11:08:36 GMT  
		Size: 2.8 MB (2773951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f805530b7e496b0f9027d1697c0554bb86963c6ceae3cab42a16225924b3ca62`  
		Last Modified: Tue, 13 Aug 2024 20:22:49 GMT  
		Size: 3.6 MB (3647792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:02c1aecfb15fac74cf4d079aa2bc3c77592d8f72b7ef7f65a97c53d58ab2d6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe1e0318585917f2318c2d5ea7836a2182f7c971d76b75cb1f395817fa8317a2`

```dockerfile
```

-	Layers:
	-	`sha256:895809296c6184c7d11c021d9d23eadea7d07baac9f2eefb5fe57f9ce9497324`  
		Last Modified: Tue, 13 Aug 2024 20:22:49 GMT  
		Size: 2.5 MB (2458139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0efacaa2e97813a19ffbcb1754754a45d440d30826c1d78b27ce49a9c4f09aef`  
		Last Modified: Tue, 13 Aug 2024 20:22:49 GMT  
		Size: 10.2 KB (10180 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-bookworm` - linux; 386

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

### `hylang:python3.9-bookworm` - unknown; unknown

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

### `hylang:python3.9-bookworm` - linux; mips64le

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

### `hylang:python3.9-bookworm` - unknown; unknown

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

### `hylang:python3.9-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:3d26d5cc2799d830c12abc024fef2d8ad964bf1f664a795841c30e1278710b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55726639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cdbf7d4e99d8fed2df39d9c69f609de2e3dd39d10f5a85b360762d5dd2637e2`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:2fb9d7e332d1c4cadd8151a8485091fce600b230987f3b306d19efc82ed0ac9c in / 
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
	-	`sha256:36f5dfff311b1880d6202ab548fb824c9591bd1c9a04f7ab677235edddf9ab23`  
		Last Modified: Tue, 13 Aug 2024 00:26:22 GMT  
		Size: 33.1 MB (33122300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fd4f3453f7aaf24515b73d164091c7aa580a42ae767d3ef5c14c65e9c7da8a`  
		Last Modified: Tue, 13 Aug 2024 10:38:50 GMT  
		Size: 3.7 MB (3708189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fefa55b462f99f61913a2c877f2f9195003b8f4008075a2bf5fc22df8ad1f0`  
		Last Modified: Tue, 13 Aug 2024 11:50:21 GMT  
		Size: 12.5 MB (12473702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513080e8458cef43ca56b7c65f7b78c8426b8fbfc0f5c307485698e04463949c`  
		Last Modified: Tue, 13 Aug 2024 11:50:20 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31595bbdd2f9acd19ac66b51160aa9b2b9bb07e66eb758cd37a626e13f43ccd`  
		Last Modified: Tue, 13 Aug 2024 11:50:21 GMT  
		Size: 2.8 MB (2774297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82e9ebf163f48a337548492a5a39c089bf273d0897d87808820fce1844eb838`  
		Last Modified: Tue, 13 Aug 2024 22:45:33 GMT  
		Size: 3.6 MB (3647919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:27344ebfb0ee487a6501b74e1ddf16ca408912c243bdd2eb90086fbbc23687e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d35bfec5f0a10e151c69ae2d2e0629372e0ae23e7e91e224e0c5fd45e7c8996`

```dockerfile
```

-	Layers:
	-	`sha256:970409734f48f2fe0a59b7cf511e2bfd8e6761dfed42f8b540f82d371a15f64a`  
		Last Modified: Tue, 13 Aug 2024 22:45:33 GMT  
		Size: 2.5 MB (2462244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7650c8ef402be7b516f1aa29d31d105c1d6fee079c6d85d0824372ba4426a971`  
		Last Modified: Tue, 13 Aug 2024 22:45:32 GMT  
		Size: 9.8 KB (9815 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:7e33a0b46ad5b29ac60d6192be7e669e1c7d7d4b4d6b7d5bc38d1d0e7f387268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48861989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7fc3af07ae00b1b5f2b47f7a31b4c162f2fdf41246d784d59d3bc3ec44cc2a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:2e68e80c30908adf6b4b6a8ea2cb0711c5b296a8ba63e2cff3b70422a4daaf97 in / 
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
	-	`sha256:218a263fc97fdfaefe7df9b0e23e00c5a0b71a094fd212f91621d5683c6e3514`  
		Last Modified: Tue, 13 Aug 2024 00:47:29 GMT  
		Size: 27.5 MB (27490097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b461ff07044838bd88b7de32a95b4eef04d4cda65fd41506dd33c5dac7812683`  
		Last Modified: Tue, 13 Aug 2024 08:27:16 GMT  
		Size: 3.2 MB (3170410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7976f89a5202862259b70e8174e452d9d24cbd92c3634c621b285cbfb1218e3`  
		Last Modified: Tue, 13 Aug 2024 09:17:39 GMT  
		Size: 11.8 MB (11779792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974ea421900553cf251f1f826b1f587ef5621af58d69216834b0b762f343c0e0`  
		Last Modified: Tue, 13 Aug 2024 09:17:39 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7411f7ea6a69f52bc69bde07481621d0256693c0254f1c1e1bf6ddd4514a17`  
		Last Modified: Tue, 13 Aug 2024 09:17:40 GMT  
		Size: 2.8 MB (2773542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f74fe2f58e733abb2b696c86a661ad31c14a5fc009203957eb3092ea096bd0e`  
		Last Modified: Tue, 13 Aug 2024 21:50:56 GMT  
		Size: 3.6 MB (3647916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:3d255f90f24668f4dae03d336dbacbef9c8007e68594b301f1b6d0a3fc82865a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80b3b16750962511e9cea355b1a5815e447a86de9292677b144271f4d3ee287`

```dockerfile
```

-	Layers:
	-	`sha256:549b919efc745266089b75635be69533860a3ba930a101508923bed80494677d`  
		Last Modified: Tue, 13 Aug 2024 21:50:56 GMT  
		Size: 2.5 MB (2457630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ba5d1ffa5369912545fe1415cf9415230cd457242da266fe672bf6c8d391af0`  
		Last Modified: Tue, 13 Aug 2024 21:50:55 GMT  
		Size: 9.7 KB (9747 bytes)  
		MIME: application/vnd.in-toto+json
