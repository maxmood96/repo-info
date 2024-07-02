## `python:latest`

```console
$ docker pull python@sha256:27d499edab2db8f3e28c2506c053075922fab1ae6cdd38a10f04fa2c9f8c5b41
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
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `python:latest` - linux; amd64

```console
$ docker pull python@sha256:fab2ed34b862ca283769e0b9f0312a2c64c18a14c6b318ecf46d96ea6cb888e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.7 MB (380651914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089e68aeaa6ed7ee97a6c1bd2c6c26b45c59a129fa5a370ba05d8a536f915e2e`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 07 Jun 2024 03:53:24 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["bash"]
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jun 2024 03:53:24 GMT
ENV LANG=C.UTF-8
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_VERSION=3.12.4
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbed71fc5444cf6889a21b002de3e7805e810aa88f91a9ca941b4e3880246d1`  
		Last Modified: Tue, 02 Jul 2024 02:00:35 GMT  
		Size: 64.1 MB (64142928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae70830af8b64968596022cd9041ce522f0c77eab5419b19e169b53582c69e3f`  
		Last Modified: Tue, 02 Jul 2024 02:01:09 GMT  
		Size: 211.2 MB (211225279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f07d3ee7cefe34357699490d74b30e7002aab91b4084e28cd62c0855d534e02`  
		Last Modified: Tue, 02 Jul 2024 03:15:54 GMT  
		Size: 6.2 MB (6161721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22139052d279c68e6e4d33f516366bf197342482dc9fb02627f9efe8ac8d89f`  
		Last Modified: Tue, 02 Jul 2024 03:15:54 GMT  
		Size: 22.7 MB (22721136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce8f53bf8e434212c3151d3f9761213f22c034ad18b9a450196230a90acafeb`  
		Last Modified: Tue, 02 Jul 2024 03:15:54 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d171edeed7f6dd31eeb5ecc0531e7609f4bbc9728b362c8dcc4d8f0ae16dbd`  
		Last Modified: Tue, 02 Jul 2024 03:15:54 GMT  
		Size: 2.8 MB (2796760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:latest` - unknown; unknown

```console
$ docker pull python@sha256:c086168d9e090ab7a22ad5eb5f476610028b03717355f08c4d0af4b78c9cb160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15883245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68eb50b1586897f0aaf07499d15c4a8d06698fb47b3e53b89bb9cba79576bfb5`

```dockerfile
```

-	Layers:
	-	`sha256:587b446126221d4568344b58877e04b40e3e307e8825b772eb3f1439ba231650`  
		Last Modified: Tue, 02 Jul 2024 03:15:54 GMT  
		Size: 15.9 MB (15857997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e05ef252eb941cf63f30854f54462151e9cb7e1fb571bb56fde20fc550379fbc`  
		Last Modified: Tue, 02 Jul 2024 03:15:54 GMT  
		Size: 25.2 KB (25248 bytes)  
		MIME: application/vnd.in-toto+json

### `python:latest` - linux; arm variant v5

```console
$ docker pull python@sha256:d1e306c3bfcb36ee3aff601282cb2ef6448407a6c23a0162df7b67201dfdad94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.7 MB (346719667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c5d9b896f0a9847a6cf818f90fbbe317eaa9a477addca1ac7c9ab7574e3d7c`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 07 Jun 2024 03:53:24 GMT
ADD file:ce7f1a42beaf6b57d9cd3b9b043cd6434d5b8da1315fee8cac2cd6fc2e7cc981 in / 
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["bash"]
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jun 2024 03:53:24 GMT
ENV LANG=C.UTF-8
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_VERSION=3.12.4
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:ba68704cd532bca61f763f11a4142906ee2aa565b2583052f6ddfff3fdf96b74`  
		Last Modified: Thu, 13 Jun 2024 00:51:14 GMT  
		Size: 47.3 MB (47338510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb056c8f4290f2ae7f12204b417f783b3346fe7fee14a5916fed571483b57f89`  
		Last Modified: Thu, 13 Jun 2024 01:24:01 GMT  
		Size: 22.7 MB (22728300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f981a74b01c05f914b1f13564a2cf75fc9471592be602f7b699412e5a62b8d`  
		Last Modified: Thu, 13 Jun 2024 01:24:23 GMT  
		Size: 61.5 MB (61517456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0475d9394b70464b90e234102b87625699171564d5f8cad8ec2f1d4de8fae2`  
		Last Modified: Thu, 13 Jun 2024 01:25:04 GMT  
		Size: 184.5 MB (184522344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e598764bc4241ee0e10c297138a1c0831e9c0a006cc8d5894fdb9cb4f0dbf53a`  
		Last Modified: Thu, 27 Jun 2024 01:29:15 GMT  
		Size: 5.9 MB (5871746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a033eb22d9b763463905e1fcff3ccbeabe7428c224d4473959ce371ad896b42`  
		Last Modified: Thu, 27 Jun 2024 01:29:16 GMT  
		Size: 22.0 MB (21985089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a8edc1d2c9af6d09b57f6eaa4230ecbd9171449ca0d3afc48093f3a3805049`  
		Last Modified: Thu, 27 Jun 2024 01:29:15 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c43724e866109095637b372d2fa639ded205bd3cc4539778abba8e7da59ae35`  
		Last Modified: Thu, 27 Jun 2024 01:29:15 GMT  
		Size: 2.8 MB (2755992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:latest` - unknown; unknown

```console
$ docker pull python@sha256:8a73a04f0974b4a20b65b75d54a537c6cbd55fd80dbf21a8644d66de81b75893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15687573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be2a3977bd2d5643a9cae5844fb83f69fe641e9dc4e98db486f3ce42bf821f74`

```dockerfile
```

-	Layers:
	-	`sha256:6ac5c428d5f83c51107cb0acbea04b267c21af6ecd22f4538a2233966db4d2b4`  
		Last Modified: Thu, 27 Jun 2024 01:29:16 GMT  
		Size: 15.7 MB (15662184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d47efc8783856393d8ae90d65be2ccc9b7ad579b143f3605d4b53e79436a883`  
		Last Modified: Thu, 27 Jun 2024 01:29:15 GMT  
		Size: 25.4 KB (25389 bytes)  
		MIME: application/vnd.in-toto+json

### `python:latest` - linux; arm variant v7

```console
$ docker pull python@sha256:a2930751bed39db0c0b9922e7a0c026fd88d181ff7625d7e235a41ba7ec55cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.7 MB (331683363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d47649ba99a91e17300f778e095ae870f1879e3805a729bf09358789da2234c`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 07 Jun 2024 03:53:24 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["bash"]
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jun 2024 03:53:24 GMT
ENV LANG=C.UTF-8
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_VERSION=3.12.4
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f43007e7b264595fb644d227437b5b5a40a08cf506f8905f388bee805d2e9ba`  
		Last Modified: Thu, 13 Jun 2024 01:33:04 GMT  
		Size: 22.0 MB (21953778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba09d7f8a9b10217e3ad0b9a640e8644b91701e59675c4e2443e6e4f8eb69c72`  
		Last Modified: Thu, 13 Jun 2024 01:33:24 GMT  
		Size: 59.2 MB (59217226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21d8970e0ba89fca18dc8a8432adc4570843d9db8e5e79d0ffb8099ce62748f`  
		Last Modified: Thu, 13 Jun 2024 01:34:03 GMT  
		Size: 175.2 MB (175175030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb2c17ce4618a9d8d65c7ae54c7cccbb06f0f1868221a162c694c2c6efc6551`  
		Last Modified: Thu, 27 Jun 2024 02:12:40 GMT  
		Size: 5.5 MB (5543528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a883bc820ad4f2a9c7b0718d70605f4d9fab07a04b4580d7be9603ae81fa98`  
		Last Modified: Thu, 27 Jun 2024 02:12:41 GMT  
		Size: 21.9 MB (21862532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb08662be5f404a18deb37aca9c2dc4883b5c4d61bdd6ff574d1646917ec855`  
		Last Modified: Thu, 27 Jun 2024 02:12:40 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2fbb021474a39631e85f64bb4ac8acb6d12ea5e4592f3b160e0beadb45ecdc`  
		Last Modified: Thu, 27 Jun 2024 02:12:40 GMT  
		Size: 2.8 MB (2755996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:latest` - unknown; unknown

```console
$ docker pull python@sha256:b39750d29d6d2aa7e4350aa26746f0903025868cafef2d70a96c157cfbed28ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15693092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c0cd13b4cd0515fe39b56b34d1bbdba92156d55b23bf1f3b798ecd17cc74a5`

```dockerfile
```

-	Layers:
	-	`sha256:65c0faf6b61d9ca8a13a5f7a0fd0178ee12f9421bdc88913f3480a47cb5e7a03`  
		Last Modified: Thu, 27 Jun 2024 02:12:40 GMT  
		Size: 15.7 MB (15667704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ae9f7036e9b47a0abe50cbaac2595b6a64f4c64390f8443a60b0ccb016ca193`  
		Last Modified: Thu, 27 Jun 2024 02:12:40 GMT  
		Size: 25.4 KB (25388 bytes)  
		MIME: application/vnd.in-toto+json

### `python:latest` - linux; arm64 variant v8

```console
$ docker pull python@sha256:cded368ed27193920bcfa5b1f9f72deef59967e7c82c74d2803441ac02e6c7bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.0 MB (371010593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f2b951bc7b564af8f443deffd30b80297ed362840bc57a1917a21a826aa300`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 07 Jun 2024 03:53:24 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["bash"]
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jun 2024 03:53:24 GMT
ENV LANG=C.UTF-8
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_VERSION=3.12.4
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cd5f8f608f832afd85dc82fbac4aea05183fd7fccf555dd4a53a4bbe06b013`  
		Last Modified: Thu, 13 Jun 2024 01:30:33 GMT  
		Size: 64.0 MB (63994737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222cb3bce424c387cc9f91f975242473b8be06d3426252fad4895105c051ad28`  
		Last Modified: Thu, 13 Jun 2024 01:31:02 GMT  
		Size: 202.6 MB (202593329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458d31dbab238688a82e20fc7bf24ba7f7153af48e51e4d6d34cddc8b2b753a6`  
		Last Modified: Thu, 27 Jun 2024 01:31:25 GMT  
		Size: 6.2 MB (6239044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc816a00c84f0562e8b15e8de59d9deff7391be54e19f23205a43f509c238e69`  
		Last Modified: Thu, 27 Jun 2024 01:31:25 GMT  
		Size: 22.2 MB (22227321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30925498a597bd44ffd2e5cf104fa3e4d62284f466e5294dc2aa199c1e6b7fae`  
		Last Modified: Thu, 27 Jun 2024 01:31:24 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d931bb0790b1e550a2f265a7a7e7720fbbfed665fdb662f91c1909e034e1b0`  
		Last Modified: Thu, 27 Jun 2024 01:31:25 GMT  
		Size: 2.8 MB (2755957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:latest` - unknown; unknown

```console
$ docker pull python@sha256:7e03ff335a7e2968abd5b071cbfdfd044cddc3068fdc2d3af6e208cdddac8b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15916002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538969e78c64e57c6ff14e0cedc73469102111b073c978678b5973782bd7d442`

```dockerfile
```

-	Layers:
	-	`sha256:1ab14e379e610f80ba41939d8e42fd019c45a1ffadb6a08ce37e83082cc9da4d`  
		Last Modified: Thu, 27 Jun 2024 01:31:25 GMT  
		Size: 15.9 MB (15890394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc2cb5e782a370b4ff2275a6b87dcff0784436c6c5b27e21d46c606b0365ebf9`  
		Last Modified: Thu, 27 Jun 2024 01:31:24 GMT  
		Size: 25.6 KB (25608 bytes)  
		MIME: application/vnd.in-toto+json

### `python:latest` - linux; 386

```console
$ docker pull python@sha256:1eef662d2849cd88d1b4049b36608546091c7cf369f596ed300f938c28b4fb55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.9 MB (382919678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5bdf96b79b207f111d6b51681f7cf6186f2136a69e6372053ab00c7e03def5`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 07 Jun 2024 03:53:24 GMT
ADD file:262529672396993121e97bbbdda3d91ce43c7548adf11a263b7ec53bb7cda4d2 in / 
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["bash"]
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jun 2024 03:53:24 GMT
ENV LANG=C.UTF-8
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_VERSION=3.12.4
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:04a42c358dbd9e835f8ae412589572f1bb5a19d9428a4854e4e845c88e34cb31`  
		Last Modified: Tue, 02 Jul 2024 00:42:16 GMT  
		Size: 50.6 MB (50579307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fc07fa7086d431c647128f1beada8efce9ea5808c01b2bf497e7e85b1fda1b`  
		Last Modified: Tue, 02 Jul 2024 01:14:02 GMT  
		Size: 24.9 MB (24890132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bff6c9a28c036769727a4cf9dbe067b96273c0352a50922f6e950491245fc03`  
		Last Modified: Tue, 02 Jul 2024 01:14:24 GMT  
		Size: 66.0 MB (65988734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517d78d8993f755e32d16bdd9d852de52b88366b9799e3015e185a4a9b88f991`  
		Last Modified: Tue, 02 Jul 2024 01:15:11 GMT  
		Size: 210.1 MB (210139446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654a8c3ede3187a6493545f102098aa9c2208b0ab2eeb1783f765ada3ad10072`  
		Last Modified: Tue, 02 Jul 2024 03:17:35 GMT  
		Size: 6.5 MB (6538528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178bf1f15a19586b70a28472922f014ff38ddc146ec026a34a381c2d657a07eb`  
		Last Modified: Tue, 02 Jul 2024 03:17:35 GMT  
		Size: 22.0 MB (21986535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803385bbd911913f51b705fae7740187e52b52b364264174b9296d9b7b6c637e`  
		Last Modified: Tue, 02 Jul 2024 03:17:35 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0f73f4a8d1b94cab47d44bbe2486bedf247c4bb76dbdf33c6ef337c69a381d`  
		Last Modified: Tue, 02 Jul 2024 03:17:35 GMT  
		Size: 2.8 MB (2796764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:latest` - unknown; unknown

```console
$ docker pull python@sha256:7ee309ee43f19c4b38f5ffcb9495138ced654cb8586e5de712568a0d8fb037fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15862184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1102bad13a2ea6490c3f41ad17644245df81dfb6f0fb2d32a7dcf69d0c03f3ca`

```dockerfile
```

-	Layers:
	-	`sha256:e869aa2f2188b6fdec15c1bb6f2230b17ce9bc535831f451a616d3116482b3bf`  
		Last Modified: Tue, 02 Jul 2024 03:17:35 GMT  
		Size: 15.8 MB (15836991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9327a325c863d4c516044dcde66c80273130eae9ded3d0f6873be07d49aba2a0`  
		Last Modified: Tue, 02 Jul 2024 03:17:35 GMT  
		Size: 25.2 KB (25193 bytes)  
		MIME: application/vnd.in-toto+json

### `python:latest` - linux; ppc64le

```console
$ docker pull python@sha256:8623134f43591620ce5ee33bdc31f9e58c2cb99c934e39f187f60d322253b771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.6 MB (395567728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec1a24733183dee8218247631eff1bd83a9ada16e0335c26ae2833fb75c26b2`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 07 Jun 2024 03:53:24 GMT
ADD file:a02c311ba745dd8d5b3cc5585e2fe57a4aa9807b1ca2005815257da116010b54 in / 
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["bash"]
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jun 2024 03:53:24 GMT
ENV LANG=C.UTF-8
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_VERSION=3.12.4
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:2ebe64104880a6a83eee169b12fbd82da8a0ddeac711670e50f30e975bcb92bc`  
		Last Modified: Tue, 02 Jul 2024 01:21:30 GMT  
		Size: 53.6 MB (53557015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf317c43d118e9cf38efabf9b1e93b406add8c26e307fde367e39a47a1c5821`  
		Last Modified: Tue, 02 Jul 2024 02:04:25 GMT  
		Size: 25.7 MB (25695092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91f1c93d43f65ddb5b49fa7540ab263862ed9868139cb0bfc51bd8dffe47f60`  
		Last Modified: Tue, 02 Jul 2024 02:04:48 GMT  
		Size: 69.6 MB (69582302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3851398057330b42908d94c58bef25257d4970fa040c693d176d2cf32992a715`  
		Last Modified: Tue, 02 Jul 2024 02:05:34 GMT  
		Size: 214.3 MB (214252411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4fa06027e8cfb8f92b0c5af152a092b42ac5a41579dbeaf01df5b8ae5ada9b`  
		Last Modified: Tue, 02 Jul 2024 16:55:16 GMT  
		Size: 6.9 MB (6899613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f2fccdd7e2cebae84ac7f80afde0726b7313f6d428ba2119768e5c7c582e45`  
		Last Modified: Tue, 02 Jul 2024 16:55:17 GMT  
		Size: 22.8 MB (22784336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545f748ee1542678dc1b3ce1f1bc8101f59d4cd6e4a1fbb9b2a929413f9d69e9`  
		Last Modified: Tue, 02 Jul 2024 16:55:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9391e2a37521ce753bcd5786273637d5aeedd1e9eb026064e32a22ea95dd55`  
		Last Modified: Tue, 02 Jul 2024 16:55:16 GMT  
		Size: 2.8 MB (2796729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:latest` - unknown; unknown

```console
$ docker pull python@sha256:0beeae48c0ddc813ebe213ae089d52383d11551572e4921cfe1e1bd52321191d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15860140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41f648638b2bc03385e11bbce1e0bb5c7a6a4a6d946f727a9a6c9d397e1a258`

```dockerfile
```

-	Layers:
	-	`sha256:d42c84f40c49bbce596ca1b1f6de6eee8f4e5dfcebb775a6ac624ecfb071c49b`  
		Last Modified: Tue, 02 Jul 2024 16:55:17 GMT  
		Size: 15.8 MB (15834824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f64b2ad50e61c7540596eaf757b8f04974395040fc46b2b735adb8d6eb76a45`  
		Last Modified: Tue, 02 Jul 2024 16:55:16 GMT  
		Size: 25.3 KB (25316 bytes)  
		MIME: application/vnd.in-toto+json

### `python:latest` - linux; s390x

```console
$ docker pull python@sha256:4d8767100e7c816e7dc510ae469e02e6aebc61d22d08b39fc093dc48943ec410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.7 MB (349693825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9387677f691a44b493927de0bab277f7d5c979687a571192b7bb8a4b960cfe9b`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 07 Jun 2024 03:53:24 GMT
ADD file:397aa43721bc5ca67ab359263843a05c62e131f07114e92f39927f59790c9a5b in / 
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["bash"]
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jun 2024 03:53:24 GMT
ENV LANG=C.UTF-8
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_VERSION=3.12.4
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:1b8bfe08588d8939b4d39134c5c614351649e3890ceb7c234b7542f58d7bcc28`  
		Last Modified: Tue, 02 Jul 2024 00:48:16 GMT  
		Size: 47.9 MB (47931511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37bf3d98ae5de59851adab45daeaaca9d29f76110a2923bd8937c4ad2e8cd52`  
		Last Modified: Tue, 02 Jul 2024 03:44:34 GMT  
		Size: 24.0 MB (24048872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6cb3bef78d7b20f095bd16b5a39e3ffec90c96f6d1307f8672edb9deef1c5f`  
		Last Modified: Tue, 02 Jul 2024 03:44:49 GMT  
		Size: 63.1 MB (63125178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e457fb781c30f5a251f0251b0cafc815abfed65652bdecac052b60618b497a23`  
		Last Modified: Tue, 02 Jul 2024 03:45:17 GMT  
		Size: 183.3 MB (183253702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d6acf8583d9bb7ba8851552d910c3f34989a7030e7fa0eaafcd88b2d88d4e4`  
		Last Modified: Tue, 02 Jul 2024 19:04:05 GMT  
		Size: 6.1 MB (6070556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd177138f109485517b2b2db7f71675726cec957e5faf0889e4643d27cb73f`  
		Last Modified: Tue, 02 Jul 2024 19:04:04 GMT  
		Size: 22.5 MB (22467047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f49ef3340f640413ae9fab00058a02e1bc299342850d3bfb89af2c1e84b5b1f`  
		Last Modified: Tue, 02 Jul 2024 19:04:04 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b061c62c1f7f8d687f10b765de8da64573a4f0038ebf4c065e225b53cc76a65`  
		Last Modified: Tue, 02 Jul 2024 19:04:05 GMT  
		Size: 2.8 MB (2796728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:latest` - unknown; unknown

```console
$ docker pull python@sha256:54deaf73fe0e99051af5cb50ce11bd532748cd663b6c93848e9ea0fa9ceb9a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15697904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed274b36911bc0ea883d3b829377348862e8fec456369c20deeea9e3f90be88`

```dockerfile
```

-	Layers:
	-	`sha256:009975a4f9467c7cf4d2c99b77ee91889fe865a00c0cac9aaa322764a16974b0`  
		Last Modified: Tue, 02 Jul 2024 19:04:04 GMT  
		Size: 15.7 MB (15672656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d24b56f57403046ee301376233838fd1834838cee4627e3d9aa9fbde037b0d09`  
		Last Modified: Tue, 02 Jul 2024 19:04:04 GMT  
		Size: 25.2 KB (25248 bytes)  
		MIME: application/vnd.in-toto+json

### `python:latest` - windows version 10.0.20348.2529; amd64

```console
$ docker pull python@sha256:dfe37173bc536df83a7234d04b758341956b185c3f756e82cb7a3b44aa64e5e1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2178273324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965906f5363c728a77a5183577e9513d84eaf96542797e8dabefcd8a80caea9e`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Thu, 27 Jun 2024 00:11:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Jun 2024 00:11:11 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 27 Jun 2024 00:11:11 GMT
ENV PYTHON_VERSION=3.12.4
# Thu, 27 Jun 2024 00:11:47 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Thu, 27 Jun 2024 00:11:48 GMT
ENV PYTHON_PIP_VERSION=24.0
# Thu, 27 Jun 2024 00:11:48 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 27 Jun 2024 00:11:49 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 27 Jun 2024 00:12:05 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 27 Jun 2024 00:12:05 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344694d52138a4fe45ba14b1c42eec63de90655517a2d4264f79a24c2f7c319d`  
		Last Modified: Thu, 27 Jun 2024 00:12:09 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e6b38fc7502259bc41ce7828500cb8ea9190bbb5cbdd2630c2fa744bf12f20`  
		Last Modified: Thu, 27 Jun 2024 00:12:09 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18483a19e4063625db50066b4e3ad55cf49afc65535bb7e4952a316cc788860b`  
		Last Modified: Thu, 27 Jun 2024 00:12:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20557e6a8361cf9568bc9e14cb6a3eef59762629b4061a765a6cea6f845d9e8`  
		Last Modified: Thu, 27 Jun 2024 00:12:12 GMT  
		Size: 48.6 MB (48579306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc0d0246c3697e6c0ff808b194bb6b2760401e5ed6baa9f6e91b8682224268a`  
		Last Modified: Thu, 27 Jun 2024 00:12:08 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a7622a69242ee332e3af88bdc571712d1360b051d01e56d09a22f3cffd45c5`  
		Last Modified: Thu, 27 Jun 2024 00:12:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd81cc02daec9707cbbac49a409bc0ed24c3e1f66bf6f12aea81f3bc30b5c13`  
		Last Modified: Thu, 27 Jun 2024 00:12:08 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb9c96ab9671761fb7147a896c45a633858d196dd26a62a5bbfbb8d4669b1f`  
		Last Modified: Thu, 27 Jun 2024 00:12:09 GMT  
		Size: 11.5 MB (11494719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bebb676d364b5f75bb602f057c79a244680080946c6b18451148c4c27a0103`  
		Last Modified: Thu, 27 Jun 2024 00:12:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:latest` - windows version 10.0.17763.5936; amd64

```console
$ docker pull python@sha256:423898430ce7bf86784ddbc25a4d03647aa99acb0c6155d2bbdf9ab8c7b5bf1a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279244704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e98311f75f9d7bbf49b7a43292b0a304cffb5180e85ffb397ee5e34618124d`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Thu, 27 Jun 2024 00:15:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Jun 2024 00:15:19 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 27 Jun 2024 00:15:20 GMT
ENV PYTHON_VERSION=3.12.4
# Thu, 27 Jun 2024 00:16:39 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Thu, 27 Jun 2024 00:16:40 GMT
ENV PYTHON_PIP_VERSION=24.0
# Thu, 27 Jun 2024 00:16:40 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 27 Jun 2024 00:16:41 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 27 Jun 2024 00:17:11 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 27 Jun 2024 00:17:12 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f09dbfbfa48ab8858dfb005f1c950e47542c182b18ad0f48162e89174bf349`  
		Last Modified: Thu, 27 Jun 2024 00:17:16 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12f45c45d966dd198bf129f110e1965a9a500a0d5754cf9a9f47ad86a2a0e9`  
		Last Modified: Thu, 27 Jun 2024 00:17:16 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b85732f503830ed08960bbac305c9895f7a7d4b0c0c42e445761bfee74ab3e3`  
		Last Modified: Thu, 27 Jun 2024 00:17:15 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f1d14ebd9a61e18f1dbb7228b7d70f4008a63a99622b7b39b105d19b206fc2`  
		Last Modified: Thu, 27 Jun 2024 00:17:19 GMT  
		Size: 48.8 MB (48756905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50511c590320bad059a5165443b8d6a435a5bfec87cd74560b6718de9bead147`  
		Last Modified: Thu, 27 Jun 2024 00:17:14 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf454cf975a7d3ea012a344d14a25ed866739a843b6502eacc57c1955364dfa`  
		Last Modified: Thu, 27 Jun 2024 00:17:14 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e8ea0d97e4e4bbbf614abb78994bfa7db6b9318aa5577f7d1730a809c9c167`  
		Last Modified: Thu, 27 Jun 2024 00:17:14 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a52ab9f50465303fc94e4276d9e5cd77002964b30fc71928ca07c87c2859351`  
		Last Modified: Thu, 27 Jun 2024 00:17:15 GMT  
		Size: 9.8 MB (9797562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3727e244b839ad849feffed4cdf1e6148e8d297ccb3a03bb08f2d80595b3a895`  
		Last Modified: Thu, 27 Jun 2024 00:17:14 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
