## `hylang:0-bookworm`

```console
$ docker pull hylang@sha256:76551a4f0f778db1bcb72a9be80a88705e0261554414332a3a5826b20f502bdc
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

### `hylang:0-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:efc6feb2779ded4473175675d7b5cb9094fab8294170bcfe968ad7e6b94feaa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53339784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3303423ecbe5a292740a54aab77b015b858c7809ff22119afcad0c0b92cebe2`
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
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.12.5
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=24.2
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:3436ea9cd94528baf127b0fbf2da7be83a2d4ca52896281201483e7a1726b1a1`  
		Last Modified: Tue, 13 Aug 2024 01:33:34 GMT  
		Size: 3.5 MB (3509899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699e948b876a73dfab247efda41e01ed99235158d14d6a359f7cd4d45d11fe09`  
		Last Modified: Tue, 13 Aug 2024 01:33:35 GMT  
		Size: 11.7 MB (11725699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5fc93dff1232040d5e73bcd35fe92a68b5b35674ffd57eb91bc678a29b1b34`  
		Last Modified: Tue, 13 Aug 2024 01:33:34 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6b38c76ff31be6c1586a1f50ffbbcf5bcaf948828817c066f3d7c1f6525d67`  
		Last Modified: Tue, 13 Aug 2024 01:33:34 GMT  
		Size: 4.0 MB (3981617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613ee0986669f2e9e1c801e653adb13d984c5a597064459a59a9698126b77dea`  
		Last Modified: Tue, 13 Aug 2024 02:16:54 GMT  
		Size: 5.0 MB (4996105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:33ee1ff591fc912d52c63cb49406c36016bbe44bc56fd51f1228c654fbbb411a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2512290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8900b899e71ecf4ea43d25c6aafe95f86f5291eef279711969dfabeb99f9e2be`

```dockerfile
```

-	Layers:
	-	`sha256:77cedead09de7fcbbb50d8ef1b6d41dc6d2d985b5dca1cf5f67ca7d5fdd8b8ca`  
		Last Modified: Tue, 13 Aug 2024 02:16:54 GMT  
		Size: 2.5 MB (2500159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e90501dd8487bcd15a261fc958b569043c3662543082bbb84c0b912f8e91eef5`  
		Last Modified: Tue, 13 Aug 2024 02:16:54 GMT  
		Size: 12.1 KB (12131 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:0847b692e281eabaae1831c108be2cdf51507fbec0a0de17f48584ad59466a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50147018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d9222259b07c924f03cc8c097402c91a47c73ec4c669f18ed58149bb6fb6b4`
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
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.12.5
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=24.2
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:b8274d5fa77230b6831a2f091eedea6b84452923257054c6bffbfa3fdfbb074c`  
		Last Modified: Tue, 13 Aug 2024 19:41:32 GMT  
		Size: 11.2 MB (11204051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1141f6bb53f4328eb25bb51c615a8c0befebc0fe45a9a0a4c21f48a37e0ed9`  
		Last Modified: Tue, 13 Aug 2024 19:41:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c27a281d48ed69ef2c39a6190df9af32cb24da00737ffa3fadae871ae4820b`  
		Last Modified: Tue, 13 Aug 2024 19:41:32 GMT  
		Size: 4.0 MB (3980331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bde3b97de26e4896197a5cc5eea24467768001f8da1dd799b452f4a716e7d1`  
		Last Modified: Wed, 14 Aug 2024 00:33:16 GMT  
		Size: 5.0 MB (4994540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:aa19c5ad092f6189a7197b091974204baa8bc00653d2a5b7df688e384e3a50ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2515977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9d1075e5051a65d636cf41a709c298706e86e22c0dd3defad90572e47470b8`

```dockerfile
```

-	Layers:
	-	`sha256:fdde19e02d2afe1cce99195b86712f0ee8085aa80606d6198cf0294313fe0a5c`  
		Last Modified: Wed, 14 Aug 2024 00:33:15 GMT  
		Size: 2.5 MB (2503662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e260773458ce6af88b3a13d534a9af3c6d04b0d03d70a1b3aa18d6a46ee90ca1`  
		Last Modified: Wed, 14 Aug 2024 00:33:15 GMT  
		Size: 12.3 KB (12315 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:83794fead1de99c448fdc760a54f9ae281585d408e087cad91f32c23a288e050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47397260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda2d84cdc1e0547832ecfcf3f1ab947244c7c242406037a796c81926980aff4`
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
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.12.5
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=24.2
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:5b239eedd77815595c68fdf4b1c1d2f91236916c4e6be9d684115bfd7053f622`  
		Last Modified: Wed, 07 Aug 2024 21:11:41 GMT  
		Size: 10.8 MB (10789507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b775408cec72c6fa891dd943635c7d4d184a162ab5ea409fab172ab48ebae4`  
		Last Modified: Wed, 07 Aug 2024 21:11:41 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc80f2ad81d308a8fd202c9c98b1c3606568d5c45a748ca832676be8fc5535e`  
		Last Modified: Wed, 07 Aug 2024 21:11:41 GMT  
		Size: 4.0 MB (3981062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891b25fe076c8a6092b9665926fd7f4a9835f5ca1b69a81e01e253c8ee5391d4`  
		Last Modified: Wed, 07 Aug 2024 22:28:46 GMT  
		Size: 5.0 MB (4996095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:e79d44e266a1398d74b69a1087714c4078ea2002db90d3d0e4cf86bb044f85a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2514844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08143cf2954331caddaa0aa3d730c38d61ac8c9c4fbeb571e81c62373190e49`

```dockerfile
```

-	Layers:
	-	`sha256:30768930539e7f52a83455d2581cfac8ffc5c4c1ae1fa647a7db6867207ed866`  
		Last Modified: Wed, 07 Aug 2024 22:28:45 GMT  
		Size: 2.5 MB (2502529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f117f64a731f4b5441e31684d4a6f05659e86a438ed4e11ddbbbaeace4cfb8de`  
		Last Modified: Wed, 07 Aug 2024 22:28:45 GMT  
		Size: 12.3 KB (12315 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:29a89c32364af0af25f7362790bc5c80474b4ba963800e8a11f5dee938705ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53162025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d4828f31c86b14c18e781017d7a1832dc56c84218f95d38840bba37c60e6f5`
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
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.12.5
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=24.2
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:a2dfbe5c205a3147d63c40ce67edc381ee0707bd4a9e94e68f3eefa5b659a5d8`  
		Last Modified: Tue, 13 Aug 2024 10:22:47 GMT  
		Size: 11.7 MB (11697493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcc995a3982991aad07913fbce2bacafc9a6c22d387bfd509fa3cfc2915fe95`  
		Last Modified: Tue, 13 Aug 2024 10:22:46 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e57af2d6d064ff3032a685b90a98e07c677fee424c85dc3a04c06e0c2fe448f`  
		Last Modified: Tue, 13 Aug 2024 10:22:47 GMT  
		Size: 4.0 MB (3981752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7f2769802885fb35720f094cb9548e5c2f2cb1321d1737c54e8f5ea639c81a`  
		Last Modified: Tue, 13 Aug 2024 20:19:20 GMT  
		Size: 5.0 MB (4996131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:3a5d40dfac8a153236d559493b204157a5d1c733a221c035497b1c6034d3759a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7791b564f137f7b926e77b0afe7340aa77b927c266d1a6f7c4cc23903ecf6716`

```dockerfile
```

-	Layers:
	-	`sha256:9773b5259907379b53bd22513e662354b943cdffc5ecd93955174b120b97db99`  
		Last Modified: Tue, 13 Aug 2024 20:19:19 GMT  
		Size: 2.5 MB (2500577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de40f8685fe20ebb71fbe4eb88f53a7347913da0a7c99d7268d9fdc1abd5035`  
		Last Modified: Tue, 13 Aug 2024 20:19:19 GMT  
		Size: 12.7 KB (12672 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:e6b32b8f6757b516a93ae791868720b8af26ca79324648d2caf2fa75eb90a11e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54602671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b2fe06b5533714727bb8ce466676ed357224a75f34fc372b0d9ac1e0c9e4d3`
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
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.12.5
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=24.2
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:c2a4753faa129ca00840745b3a9b8c5bf92a8946427c54b1b91a1bf5c3c50864`  
		Last Modified: Tue, 13 Aug 2024 01:25:20 GMT  
		Size: 3.5 MB (3507298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5be89c89972a85424fbd1312dbedfcf049c6a5987092f39f3fc0e39e462a3c`  
		Last Modified: Tue, 13 Aug 2024 01:25:21 GMT  
		Size: 12.0 MB (11973543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa26952404a49f2c94c8c6bcfdc68b2f0cdc0419ad11d364f4f5b5ca0ec95f63`  
		Last Modified: Tue, 13 Aug 2024 01:25:20 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e87a7607b0e1bfedfa8e43ad64fa6d0c2cc26d40d9ec5fee5da6e0dfcb70cfd`  
		Last Modified: Tue, 13 Aug 2024 01:25:21 GMT  
		Size: 4.0 MB (3981224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c4ab8d245b210718439fd89286f27f84909664e3ced01ebe5a0ec5624a2090`  
		Last Modified: Tue, 13 Aug 2024 02:17:44 GMT  
		Size: 5.0 MB (4996093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:d13bad64ec01b55e394b6d2a18391f66dd2ec8273b5fff9e8432fbae8baefeab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2509232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e567bf763ee78fdbc23ec7b3785c748f19e55216a459fd49abab2b15995cb648`

```dockerfile
```

-	Layers:
	-	`sha256:10f73d4f5da430b8e5db2ec7a9bca973eaacfded3d1277bda832b65ba08bd592`  
		Last Modified: Tue, 13 Aug 2024 02:17:44 GMT  
		Size: 2.5 MB (2497193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca676cc936883a8e5c9a96dac771ea514a7413d2c44b152e6b965fb9a8521b2b`  
		Last Modified: Tue, 13 Aug 2024 02:17:44 GMT  
		Size: 12.0 KB (12039 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:6abecaeb8bff73b27e9b472adf5186ff25ebdd9d5731f7285b74f8577b88868b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58147563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0fe0c32bc1b2d19324ccd60a7534579733b30356b70f5f8274228cd4907ce5a`
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
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.12.5
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=24.2
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:17af5fbe6a16a246ff8b2499e74207d675d9c4aeab29190ae6ce0d539299a4a7`  
		Last Modified: Tue, 13 Aug 2024 10:38:51 GMT  
		Size: 12.3 MB (12338483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac29d3b36da268ad487f5894b8f136fa2f2eb229af15208ac698f65b226b014e`  
		Last Modified: Tue, 13 Aug 2024 10:38:50 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5dfac214eaaac4d963e5e5626fb471cefe4bf04ce2865f9610663a40580a64`  
		Last Modified: Tue, 13 Aug 2024 10:38:50 GMT  
		Size: 4.0 MB (3982152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7c33ecfc568923913e24ff494dbcb90739ab5d106fdd543919b2dbee201af9`  
		Last Modified: Tue, 13 Aug 2024 22:40:30 GMT  
		Size: 5.0 MB (4996208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:7548d05213283988ca159041c20e2aea62d081784ec746eca5591c975b4cea87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2516892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ebff6e7b3f8d92435009446a8b04a6e48161924133848649ad7b76e855b397`

```dockerfile
```

-	Layers:
	-	`sha256:25dd46411dfe890858452dec21049152748c771b610315bfbd82ef71dd6790c3`  
		Last Modified: Tue, 13 Aug 2024 22:40:30 GMT  
		Size: 2.5 MB (2504634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54655305c6dd3f68bb091d767cc72dfd871edd25bc96847481bed375eb72a0e5`  
		Last Modified: Tue, 13 Aug 2024 22:40:29 GMT  
		Size: 12.3 KB (12258 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:6e65fdf606f99c424b84f9e96f7ca23e9b7e5750897228894d46e6420c318151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51292690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58938cb3b11bcd134518666daae91dc34d73c485689c29b3fe4919282574d9db`
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
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.12.5
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=24.2
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:0873d42898de2e59a995d85e58ecfc5a6ee091e34f9d014064e3dab8db5ec214`  
		Last Modified: Tue, 13 Aug 2024 08:27:16 GMT  
		Size: 11.7 MB (11654608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84267a6f74021735af1c559d0dcc549f392a4a0ab1de08d43e9da485ff5a6ae2`  
		Last Modified: Tue, 13 Aug 2024 08:27:16 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff51913afcf947c9693351a1a8dbfa56ea377aefd7e61e893ce3ef81742671b8`  
		Last Modified: Tue, 13 Aug 2024 08:27:16 GMT  
		Size: 4.0 MB (3981306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a769e662ae2c37f0ca12a8ad7830c3b7dd2de588ef06e8739ed13dab71aa32`  
		Last Modified: Tue, 13 Aug 2024 21:47:10 GMT  
		Size: 5.0 MB (4996037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:420f840ecb802ed8253a65b3f94d6a130a0f0b3a74092a387b0b9777078c4c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2512113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a164780a56ce9bdcbfb35387a3bc26b517d368c7e4b805c84148cc6cb4d38659`

```dockerfile
```

-	Layers:
	-	`sha256:b8476e88962153ff3814059ca430e674d2dd76b95db1ad5da4085562d7e66d88`  
		Last Modified: Tue, 13 Aug 2024 21:47:10 GMT  
		Size: 2.5 MB (2499972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84a31879e3229ae0156da4db82707a346df51e40b80c13034721f5dedc8a0230`  
		Last Modified: Tue, 13 Aug 2024 21:47:10 GMT  
		Size: 12.1 KB (12141 bytes)  
		MIME: application/vnd.in-toto+json
