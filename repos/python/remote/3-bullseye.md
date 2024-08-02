## `python:3-bullseye`

```console
$ docker pull python@sha256:38b14b0e259671934423af45eabb7a2197c7d45796ccbe983a89f73de883d69a
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

### `python:3-bullseye` - linux; amd64

```console
$ docker pull python@sha256:20127f68429dffbfb497ca52d44902e8fff5f148381df3e03eab4b133af0f922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.8 MB (355837017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f479b96519dfd5d31114ef7b5e66494564fc2e25f9b1acdae2c99c81b1e39062`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:25 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Tue, 23 Jul 2024 05:24:25 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:08:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:09:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 06:49:02 GMT
ENV LANG=C.UTF-8
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_VERSION=3.12.4
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_PIP_VERSION=24.0
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8ed7043ae24342affc9e27ba2f362a3d02c164d6f2cc7b837f33b475f4ef54`  
		Last Modified: Tue, 23 Jul 2024 06:14:32 GMT  
		Size: 54.6 MB (54588538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c6efb0908b76d25c6355b6afc739337771c5a9f3a556c262cb1d0c767b6604`  
		Last Modified: Tue, 23 Jul 2024 06:15:02 GMT  
		Size: 197.0 MB (197039174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f4aba5a2f8b26442f3bc770fe7954357617381af452c4addce40e223990a8e`  
		Last Modified: Fri, 02 Aug 2024 14:43:31 GMT  
		Size: 6.1 MB (6051157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575bae77b1b8b42254668cf12f107c1c564eeeadc3a53482d0a2049f2056a704`  
		Last Modified: Fri, 02 Aug 2024 14:43:32 GMT  
		Size: 23.2 MB (23152057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05e808465c4938707ede6dc35afb28e3da58a2ef41ded6b157c97b21a165869`  
		Last Modified: Fri, 02 Aug 2024 14:43:31 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a7eb7916a2221c07608853608e0e1f46b74d1ab334576ae14422bfecfabdb9`  
		Last Modified: Fri, 02 Aug 2024 14:43:31 GMT  
		Size: 4.2 MB (4156994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:032656de0669d3fbbf8ced67baaae3f6c655374357e14c58d3fcc0131efaff6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15607482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49b7d525cf5f7e1df636c32397027d5a4c48e3ea6fe3a7d4eaafaaf992a3d3e`

```dockerfile
```

-	Layers:
	-	`sha256:d8d925c4c2d55d56ab8f48c0f5375ece0e22ab60db8c342a6107f6e15f1c7c49`  
		Last Modified: Fri, 02 Aug 2024 14:43:32 GMT  
		Size: 15.6 MB (15583412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1251524ce1235a0ddda656eb91f7a4a670e15ed1093d4e5cd7397516658b667d`  
		Last Modified: Fri, 02 Aug 2024 14:43:31 GMT  
		Size: 24.1 KB (24070 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; arm variant v5

```console
$ docker pull python@sha256:380cee690f55e014c3fa917ec833f58d2ea0d8d87380a4cbd0905e44e996a052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.1 MB (328114911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125196e87ce38fe11251697745f629082a93212949e2f9c319305279f4cfc2ad`
-	Default Command: `["python3"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:12 GMT
ADD file:05c877f820dfe73bd5cecf959b857152065c40802cad0d9a46229bc0d5708339 in / 
# Mon, 22 Jul 2024 23:57:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:40:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:41:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:43:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 06:49:02 GMT
ENV LANG=C.UTF-8
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_VERSION=3.12.4
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_PIP_VERSION=24.0
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:6faa199d3f09eecc4762c527abd2e9a5bc86f34a15c78145707b6b0b0ee526d5`  
		Last Modified: Tue, 23 Jul 2024 00:01:42 GMT  
		Size: 52.6 MB (52588961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd35925e7431e8e36d2900def8d6954e5c811ce7a1c205db5d4cc183c4696b67`  
		Last Modified: Tue, 23 Jul 2024 03:53:27 GMT  
		Size: 15.4 MB (15375348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b062df9eea8fb3b005e76c03f7ef72ba9331888f68b2b9dd6b1f7afaddd042cc`  
		Last Modified: Tue, 23 Jul 2024 03:53:50 GMT  
		Size: 52.3 MB (52329700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5972ef34abc8f8302675fa051e04d2b0db7995a024a1f4298f5a462fcabd0d`  
		Last Modified: Tue, 23 Jul 2024 03:54:35 GMT  
		Size: 175.2 MB (175246775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799611c469e808399221460a75983b772213036a50e5241c8d057950f8bea559`  
		Last Modified: Wed, 24 Jul 2024 01:08:39 GMT  
		Size: 5.8 MB (5777183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549ce101c8ad1ea87d0bac3e531f72c218d977e409151cfe7d3587202af562e6`  
		Last Modified: Wed, 24 Jul 2024 01:08:39 GMT  
		Size: 22.6 MB (22639678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54084aba0c7375e6d216fadf5e14c0d3c4c5a4a3e6fbc56c3e143f1e44e83e10`  
		Last Modified: Wed, 24 Jul 2024 01:08:38 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c95a30bbf8a09355c85027558c4dbcf5cfad0cb6af7c4aba218672fb352597d`  
		Last Modified: Thu, 01 Aug 2024 20:17:38 GMT  
		Size: 4.2 MB (4157034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:60597308aadce180da512f9277ff28aec82919e9ba3e3e8ceaf5617af232ea03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15403267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3960863cdfcc3bf359fee5f58616e4cfcaf726243ef781f2ec9491e696e8462`

```dockerfile
```

-	Layers:
	-	`sha256:f76001b9eb91ac19ec9ac592918cf599fc8eb2dbcb3de6670c212a8248841e48`  
		Last Modified: Thu, 01 Aug 2024 20:17:38 GMT  
		Size: 15.4 MB (15379088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7559d905e0aefd3824249472e2cdcf7560cdd3e50691085e1551ce0bb861398`  
		Last Modified: Thu, 01 Aug 2024 20:17:37 GMT  
		Size: 24.2 KB (24179 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; arm variant v7

```console
$ docker pull python@sha256:7f20cf4a846861314f977fc7b52b36be3295f8059e9f819d8d77dc5e76a5229d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.0 MB (315033793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884729d4c900dc84bd795c60e1eb9b78c40e32ee6c9bef0e391d55db3be63e09`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:18 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Tue, 23 Jul 2024 03:03:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:37:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:39:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 06:49:02 GMT
ENV LANG=C.UTF-8
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_VERSION=3.12.4
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_PIP_VERSION=24.0
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a61d577d5393ca0b5e52e6cbd75569b7d9e9b50cb27f783d5482f5f97240ba0`  
		Last Modified: Tue, 23 Jul 2024 03:48:23 GMT  
		Size: 14.9 MB (14879665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6354534da26fdc193140968c5b8a059bd98e1fc05e33deacad3b97f257fd35f`  
		Last Modified: Tue, 23 Jul 2024 03:48:44 GMT  
		Size: 50.4 MB (50357798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82623cfc0dda8411ed87ecde5f4fe0993f1ef9fe052103e7d162351520e9b5a`  
		Last Modified: Tue, 23 Jul 2024 03:49:26 GMT  
		Size: 167.5 MB (167501970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72690803adc47c224e0c05bd4a1b44fd21541469344f2b80589f3f55ff7ea277`  
		Last Modified: Wed, 24 Jul 2024 09:09:17 GMT  
		Size: 5.5 MB (5460240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768423156486a5e209a22ac6f8c4b3b8702d1de532b780d8994ba66432c1aef2`  
		Last Modified: Wed, 24 Jul 2024 09:09:17 GMT  
		Size: 22.4 MB (22434501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722226df822b42e9807908da59f861cabf9f0257d1b457f44e744a5a83c01741`  
		Last Modified: Wed, 24 Jul 2024 09:09:16 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8917c9352c6a443d5f1e13b45aae0b7264bbd71e4ff654194585dd5df10b9bff`  
		Last Modified: Thu, 01 Aug 2024 21:32:17 GMT  
		Size: 4.2 MB (4157030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:faba36a4bd8c7889c3210660ee04dcf5eaec3c71c9e560f89c439dcb8132c041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15408687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba564a1aa0be27783e0df149f2855d3732e4bc6ff67f8efdda3165d91006858`

```dockerfile
```

-	Layers:
	-	`sha256:0e86436c7d346e137ba2ed012f258a6197f467fb085e73c31cc3718e6bf56720`  
		Last Modified: Thu, 01 Aug 2024 21:32:17 GMT  
		Size: 15.4 MB (15384508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e25ccd5e77f33eb1826d65ed7d62add045d16e21a7034f6b9efd182e51c8323`  
		Last Modified: Thu, 01 Aug 2024 21:32:16 GMT  
		Size: 24.2 KB (24179 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; arm64 variant v8

```console
$ docker pull python@sha256:b23dadd803ce876595cc835bafdd4fc145e544cd204e14ce4798bab5ca5f083e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.4 MB (347376249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d692689e7d31945f1a30683da51a28b24be18cced9b00375162448a60fe14cf`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:58 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Tue, 23 Jul 2024 04:17:59 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:04:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:05:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:05:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 06:49:02 GMT
ENV LANG=C.UTF-8
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_VERSION=3.12.4
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_PIP_VERSION=24.0
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c27a83c76abd51a72277b6a74eb7f88e560054e0d04383f64e2886877a20dd5`  
		Last Modified: Tue, 23 Jul 2024 08:11:04 GMT  
		Size: 15.7 MB (15749501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac540a55631c4cba93c7e4e4bf634300076d45e71db5f34f3c0d770eb826303`  
		Last Modified: Tue, 23 Jul 2024 08:11:17 GMT  
		Size: 54.7 MB (54694822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df233b2a5328fe9ae508771678b5a4faaefca18e64196b4ac65584baa5c8aa9f`  
		Last Modified: Tue, 23 Jul 2024 08:11:41 GMT  
		Size: 190.0 MB (189965935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f59bf0e2668cead0c915d436faf92f2012da6eb87a2d93e1b225a8493f86e0`  
		Last Modified: Thu, 01 Aug 2024 21:25:32 GMT  
		Size: 6.2 MB (6163716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f133a4c11c844a5baa1ce17a3afc0fb071e738e5e5d50e4d7ed22c9ef2f520`  
		Last Modified: Thu, 01 Aug 2024 21:25:33 GMT  
		Size: 22.9 MB (22915019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b877b33ce356339b2ce5d808e69ccec61438faf2ed685edb3e8482beb1ea05d`  
		Last Modified: Thu, 01 Aug 2024 21:25:32 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f37475623e61d6548aa015fdffe41629627cff4f31ab935b8b7f7e55f25d16`  
		Last Modified: Thu, 01 Aug 2024 21:25:32 GMT  
		Size: 4.2 MB (4157038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:dbfd34f1d39c9e621d9b4bdfe075641d99dd44fabf1da0e3bbdab347503d990b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15610183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a2ac35dbdc380c20919cdb2b08dfbf117df67051b729bd1d94057d28a596ab`

```dockerfile
```

-	Layers:
	-	`sha256:f838499f88c61486ce4ff7cfb7f12c6ab2d17bf12c725b68e473b0b6197c9f9b`  
		Last Modified: Thu, 01 Aug 2024 21:25:32 GMT  
		Size: 15.6 MB (15585801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:729d7ec6c9f410be0f3fa1d9d6630f811c2335c13e98280f42dd437611497643`  
		Last Modified: Thu, 01 Aug 2024 21:25:32 GMT  
		Size: 24.4 KB (24382 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; 386

```console
$ docker pull python@sha256:106c7801dd6bfcabbd20cd3ff01b85b5e49c199a74e2f116c1f458c219e9137e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361184481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea07eb80e39051336b96f9819467cef087b2f57e7ac288682c0b9b4084dc2f94`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:24 GMT
ADD file:d1f79afb47e16fbf87d0a90342c567c752e14b1bf325fa45d6de69ea871b26df in / 
# Tue, 23 Jul 2024 03:54:24 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:42:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:42:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:43:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 06:49:02 GMT
ENV LANG=C.UTF-8
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_VERSION=3.12.4
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_PIP_VERSION=24.0
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:35a8dcedb97fd8133fbcd18694f30c60eebc7e4f268630ab7b35eefe40254457`  
		Last Modified: Tue, 23 Jul 2024 03:58:11 GMT  
		Size: 56.1 MB (56074170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4dc1000d9e0251c16eaa821d62c15a6b192ccf2a5a7ca1f418356c9510042e`  
		Last Modified: Tue, 23 Jul 2024 04:50:03 GMT  
		Size: 16.3 MB (16267809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb2358914d635fc6784c6b2db8c1b20149653f26b9311bf6d676476a452297f`  
		Last Modified: Tue, 23 Jul 2024 04:50:23 GMT  
		Size: 55.9 MB (55927780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30928a030df8a953adc83c67e2ab17a4c5048cc04287762bc9e03e269fe7c3dc`  
		Last Modified: Tue, 23 Jul 2024 04:51:04 GMT  
		Size: 199.9 MB (199944219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a8a261b0a6f377258834e6eb32c20cfe26bb1fe90eae1368463767f40bea94`  
		Last Modified: Fri, 02 Aug 2024 14:50:11 GMT  
		Size: 6.4 MB (6441005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66a5fcd38a08bfaad16ea79bbea4a1ed3cb613177dbde2943b3045467098b09`  
		Last Modified: Fri, 02 Aug 2024 14:50:11 GMT  
		Size: 22.4 MB (22372289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294f28d8551c0b717a27232e0f6dd46fc0ef3a4e405d4fd84411319bc4f758a0`  
		Last Modified: Fri, 02 Aug 2024 14:50:10 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bdb9ce010a47faaabd2e79419f1bbbbd3099f01825debfa7959f99769b4999`  
		Last Modified: Fri, 02 Aug 2024 14:50:11 GMT  
		Size: 4.2 MB (4156977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:8ac0a730ee7e552b23d36c2fb58e4db3852bdf3e8d0d07893b2dce45fc5c5c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15595932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247173ba12e2c6d16182fc1b1abe2dd40af230cb97fa1a1c354488866a17b86b`

```dockerfile
```

-	Layers:
	-	`sha256:e016272f0efe1bb59d95b1cc7c1f1e17fc8421fbb56464e40682e5aee0801048`  
		Last Modified: Fri, 02 Aug 2024 14:50:11 GMT  
		Size: 15.6 MB (15571897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d03ce994738ed51dea1e7579eb9dac7b977bc45f378cdfbc756c50176a78247d`  
		Last Modified: Fri, 02 Aug 2024 14:50:10 GMT  
		Size: 24.0 KB (24035 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; ppc64le

```console
$ docker pull python@sha256:8ff161f56549e486a8c7573630cb37421c23be90b69f73ecb3445b0348f1759c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.0 MB (365004913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a442170f7920add809e9d9eb48deb2d3d0e6d79ee0d4b6bdfc63ce1ac767307`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:09 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Tue, 23 Jul 2024 01:27:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:34:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 06:49:02 GMT
ENV LANG=C.UTF-8
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_VERSION=3.12.4
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_PIP_VERSION=24.0
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Mon, 29 Jul 2024 06:49:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Mon, 29 Jul 2024 06:49:02 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 29 Jul 2024 06:49:02 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89f3ec0749e802be2768d4d8d990f300a55cd418831db42ee374e4bb81ab0a3`  
		Last Modified: Tue, 23 Jul 2024 02:43:09 GMT  
		Size: 16.8 MB (16765814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3543cad9c41f9c9127d1adde535bc13ac5b446330727c5083aafa4b8d005c62`  
		Last Modified: Tue, 23 Jul 2024 02:43:26 GMT  
		Size: 58.9 MB (58872667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8d0e14af4e3c68b0eae63b664f02cecf25bea995af2d28db767811530400f5`  
		Last Modified: Tue, 23 Jul 2024 02:44:02 GMT  
		Size: 196.4 MB (196396379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083b820e20811dd23731c7826536c5bd92bb0f3cb68a5ee3adcd43df1c783ff`  
		Last Modified: Thu, 01 Aug 2024 21:28:39 GMT  
		Size: 6.8 MB (6801705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b66a4c01600329414b3f72c1c4dbbdb2bb83016587999da4d132b4fe711308`  
		Last Modified: Fri, 02 Aug 2024 03:00:04 GMT  
		Size: 23.1 MB (23056411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53a70745b6ebfa849507ef110aff4e36dc745ff8f1c892c797a054ad8cd4779`  
		Last Modified: Fri, 02 Aug 2024 03:00:03 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c57d503e91cfc28ccff4819d92371c23f95647c33921746862fc51f6fea575a`  
		Last Modified: Fri, 02 Aug 2024 03:00:04 GMT  
		Size: 4.2 MB (4157017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:a7c210eb1720b6a765f05a90fab798b0816d14be78527004aba611a36da50712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15576968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba9a1b0fd0af0d9c08ad1546f7da4cfb8d3b2d1777f5bd8fe0130211b39ff88`

```dockerfile
```

-	Layers:
	-	`sha256:7c17da49ee7ac35ca3098614d80734b5c0c08b81b9f72822750f6357ab4bcc6e`  
		Last Modified: Fri, 02 Aug 2024 03:00:04 GMT  
		Size: 15.6 MB (15552854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a49fd4dc67df7fb9b648503efddc55be89e115bed174de978ba430995c0ff4f`  
		Last Modified: Fri, 02 Aug 2024 03:00:03 GMT  
		Size: 24.1 KB (24114 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; s390x

```console
$ docker pull python@sha256:1af5626578d0e17409836a134abfd69ebf15e60816d555d45b958c70117f95a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.4 MB (329412948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c430ad659126c0261fa0e2a5667c8ea2f36cc7f716c57467f49319622503456`
-	Default Command: `["python3"]`

```dockerfile
# Sun, 07 Jul 2024 23:32:36 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Sun, 07 Jul 2024 23:32:36 GMT
CMD ["bash"]
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 23:32:36 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_VERSION=3.12.4
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 23:32:36 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 23:32:36 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 23:32:36 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e924418f310f18ad368886d6df84cac76659f51225b0784a1e53ff07318533`  
		Last Modified: Tue, 23 Jul 2024 03:15:16 GMT  
		Size: 15.6 MB (15641720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af67dae0133d3a5f116411c20eed624558ce4a187db4fd8eb9a8d622a827e5f`  
		Last Modified: Tue, 23 Jul 2024 03:15:29 GMT  
		Size: 54.1 MB (54075295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d2fba31676a932e41fb57a433c1ba42080bc1e363d7a190b9c73795d53b569`  
		Last Modified: Tue, 23 Jul 2024 03:15:55 GMT  
		Size: 173.1 MB (173058357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b0fb7dfd33db6dea581b4b4564ec7775a01f7bbd9c804a6b0e6927df7172ae`  
		Last Modified: Wed, 24 Jul 2024 05:11:26 GMT  
		Size: 6.0 MB (6001112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7b005cea4239292bf9c85089ea3f858e5336b3e80e78970f9003c980b2d8c7`  
		Last Modified: Wed, 24 Jul 2024 05:11:26 GMT  
		Size: 23.2 MB (23152072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032badb87903235091a1ca5c763867aaf77fd6d470546a5ceaf3d102a4b17823`  
		Last Modified: Wed, 24 Jul 2024 05:11:26 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5786abda8789a2b739ae2a3e1ce2ff8fe2e84e7e0ee06539c11839c8306268`  
		Last Modified: Wed, 24 Jul 2024 05:11:26 GMT  
		Size: 4.2 MB (4160069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:200996c7277236bf269d6931dad23564c8425b02dbd3620ba83c5d9ccdcd72ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15428416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf81f4840d7da4e089616e6e5f7829fb9800caeb0233ac333914425658b2e1b`

```dockerfile
```

-	Layers:
	-	`sha256:0383e01cef9ba9d0927ccfdae884772e22ad443568b9c7eec0b2ed275a10182c`  
		Last Modified: Wed, 24 Jul 2024 05:11:26 GMT  
		Size: 15.4 MB (15404346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68a44c53113492b656b74ffd739f8afd97c9f1b8561791128d7861b85f19e501`  
		Last Modified: Wed, 24 Jul 2024 05:11:26 GMT  
		Size: 24.1 KB (24070 bytes)  
		MIME: application/vnd.in-toto+json
