## `python:3-bookworm`

```console
$ docker pull python@sha256:70b2e244053eca39a645f0479619cbfb706ed5b4812bb4e94f9e94d9e0daff88
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

### `python:3-bookworm` - linux; amd64

```console
$ docker pull python@sha256:e1fb1423ec9c0c6d2d781d8f6db0b7eef08fa193c8c4534f483dbd3bf13c2d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.7 MB (380652748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899a7886bebcfbd0b38a8ad6ac24cb8e241ab4212ba3ff008ec592d4fb20867f`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 26 Jun 2024 21:58:20 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 21:58:20 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_VERSION=3.12.4
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
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
	-	`sha256:e9dab428da9ae6b5406df45ee25492eb81e2a2b94726ea98b509381223ed663e`  
		Last Modified: Wed, 03 Jul 2024 00:16:35 GMT  
		Size: 6.2 MB (6161718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11192e3f2ef193d4c53a811a2a004e5372d660899646bb5c4c446931708bc222`  
		Last Modified: Wed, 03 Jul 2024 00:16:35 GMT  
		Size: 22.7 MB (22722006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93673920160f6eccf56b228586d9def71676dc637367e596c88aeb444f27645f`  
		Last Modified: Wed, 03 Jul 2024 00:16:34 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473095d974483518af3302fa35215759d891946cd590dd7591d500bdcdaa1fa3`  
		Last Modified: Wed, 03 Jul 2024 00:16:35 GMT  
		Size: 2.8 MB (2796728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bookworm` - unknown; unknown

```console
$ docker pull python@sha256:1df25b201708ffd3dca1b1061293d51d8a16ff077a83cca15970aab0202b11db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15883244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf599e4b9b7f4155e9496b6b7a0c60d5ac07a24d4a50bcd35867957b4855e4b`

```dockerfile
```

-	Layers:
	-	`sha256:8ef12ba1cb6188de4fc125ce1acb6d98578702f99f9f366c9c0ee6c7139a0387`  
		Last Modified: Wed, 03 Jul 2024 00:16:35 GMT  
		Size: 15.9 MB (15857997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd62c4f67cc7e076777a21d3a1a524afad697fc5c37be4af47b82b170bbb58d5`  
		Last Modified: Wed, 03 Jul 2024 00:16:34 GMT  
		Size: 25.2 KB (25247 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bookworm` - linux; arm variant v5

```console
$ docker pull python@sha256:8c6d2ff225a608714811d140bb1c7f7504261f9f4ea46132294f11ca30667e14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.7 MB (346733705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe39e5f07e5ba548dbeea43965713409148da73dbb02f9a37efc53c58192e992`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 26 Jun 2024 21:58:20 GMT
ADD file:e0c33927a1af62d353710ab02fe9345a8805475ab99685993742946d38302465 in / 
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 21:58:20 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_VERSION=3.12.4
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:f1ff7b6851f56d19040d12cd1d8757075037a3e51cd0d20ddfedfe600e399be6`  
		Last Modified: Tue, 02 Jul 2024 00:51:07 GMT  
		Size: 47.3 MB (47320358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ec281dca54581a50ec4a927c64bebe7b6ef47dad0b260009c44ae5a8feddc`  
		Last Modified: Tue, 02 Jul 2024 01:22:39 GMT  
		Size: 22.7 MB (22727504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c366b742114f1b314834ae656bee5e41f5e30629107aed4bd693207e1ed0df`  
		Last Modified: Tue, 02 Jul 2024 01:23:00 GMT  
		Size: 61.5 MB (61520104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec006b2fd0fa59480156cd480431866e4136d69ec003c1c9a01cc6cf74b4a11`  
		Last Modified: Tue, 02 Jul 2024 01:23:39 GMT  
		Size: 184.5 MB (184511793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab2e7e431b98d6d436c9dbefed996821f20b1ac66db377b321ab36a7b28c023`  
		Last Modified: Tue, 02 Jul 2024 21:13:12 GMT  
		Size: 5.9 MB (5871988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a7fdbbf1f02c01f51a71dfbae7ecb1710db973618fbc87f956ff19b85f6998`  
		Last Modified: Wed, 03 Jul 2024 02:28:31 GMT  
		Size: 22.0 MB (21984906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66279d72472a646486bd3faaee5bb9229b048fea00c07bd0f1904e4692d0f84a`  
		Last Modified: Wed, 03 Jul 2024 02:28:30 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61e26e5a332d977ecd045030a6f33b8e3af95170799949272c77ee803af2ed5`  
		Last Modified: Wed, 03 Jul 2024 02:28:30 GMT  
		Size: 2.8 MB (2796822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bookworm` - unknown; unknown

```console
$ docker pull python@sha256:cd8d67878276ba143428e560ef0186f9c679de3ad534282d7aaad3202d3de935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15683802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c345f78210b4ac1ef63b70ad21dc6f36c63015803461ce00509448db6c5e540`

```dockerfile
```

-	Layers:
	-	`sha256:41e86e82b6e9865ea7a7786f5ca0e26cdbed9e67cb0cf86fb91cf136264e54bc`  
		Last Modified: Wed, 03 Jul 2024 02:28:30 GMT  
		Size: 15.7 MB (15658414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0b647dd1cee4230a1a01bba60385183a2dc87d00cfb0d45d11123202ee148a4`  
		Last Modified: Wed, 03 Jul 2024 02:28:30 GMT  
		Size: 25.4 KB (25388 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bookworm` - linux; arm variant v7

```console
$ docker pull python@sha256:b196ea99548682957e353fdf83365c83fd0347008f70b7f8d6b19da10509dab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.7 MB (331686789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8bc862fb44c6789aed0e50b52aa839cb384261d35fe2f3c0eea23d7880a2c54`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 26 Jun 2024 21:58:20 GMT
ADD file:526dbb34ac449ae8f3c9025d71b3ffeb0e24fa5dc1a01da707f0a8b834eb4e33 in / 
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 21:58:20 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_VERSION=3.12.4
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:335f2c484898b910fac13d5650ed3c78e5e673fe8dab1b06a071c71478a153d0`  
		Last Modified: Tue, 02 Jul 2024 01:02:57 GMT  
		Size: 45.1 MB (45148097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa30b2bcbde45c2fc67abf425197af3af3e67d55296f168143343ef1b0e2d3e`  
		Last Modified: Tue, 02 Jul 2024 01:39:04 GMT  
		Size: 22.0 MB (21954038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4650a14deed524a46f7f7b410ff5d81e5ff66e51c7345e2b05887b6e3f4030`  
		Last Modified: Tue, 02 Jul 2024 01:39:24 GMT  
		Size: 59.2 MB (59222408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ceb3cc12c0338c85a0602b703f838a13aa2e232ffde0c008b8db42bec79a26`  
		Last Modified: Tue, 02 Jul 2024 01:40:01 GMT  
		Size: 175.2 MB (175164748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61307447c76502ab2acb040e5ac2e89dbb560f0c8914dbd19b0c78cf28514c59`  
		Last Modified: Tue, 02 Jul 2024 21:19:46 GMT  
		Size: 5.5 MB (5543705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82ae5c52c03222416a147c50a295730fc3da558ffca0b475c80bf47f798c530`  
		Last Modified: Tue, 02 Jul 2024 21:19:46 GMT  
		Size: 21.9 MB (21856803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16eca3b23ddb2f386b3ab2baf13aeeb1f8210fba94019e528768489253ced88`  
		Last Modified: Tue, 02 Jul 2024 21:19:45 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f28cadc93a35962e026256fc47faf02a58d5e0d3fbe66cef115e9c1df0270b`  
		Last Modified: Wed, 03 Jul 2024 06:46:20 GMT  
		Size: 2.8 MB (2796759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bookworm` - unknown; unknown

```console
$ docker pull python@sha256:0d3299827198fbe369180b7734826bdde1be0fe96c4baffe0f7dd5b06db50a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15689323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d869b036d48ec08b005c865d653e6be31d9fab90a003e4342f0b94303c1a33e2`

```dockerfile
```

-	Layers:
	-	`sha256:1f364ad58e0ad1a42823da8c005823d516c2ec94bfcb2c38d032ad07bcdc337f`  
		Last Modified: Wed, 03 Jul 2024 06:46:20 GMT  
		Size: 15.7 MB (15663934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff7f961bbfd463d500b257c28c3f3e43973ad40a9a7e7cbe519a17ab497af327`  
		Last Modified: Wed, 03 Jul 2024 06:46:19 GMT  
		Size: 25.4 KB (25389 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bookworm` - linux; arm64 variant v8

```console
$ docker pull python@sha256:26b991d580591db070b7982639bd707de1ffec721b190b059bc6e2fe340a648a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.1 MB (371054998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2a2a87a538eb7b0de676874cb458763f11a7d1ddf7d4478fe1ded3f34a6d9e`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 26 Jun 2024 21:58:20 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 21:58:20 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_VERSION=3.12.4
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a6ab51b82df5ee608db374a16686eefb99bc53834af17064184653121729b3`  
		Last Modified: Tue, 02 Jul 2024 04:01:58 GMT  
		Size: 64.0 MB (63994637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f8241ab9fefcedcf3f5b57b6b8b870d07c8ac5d8e37b6c24189ae5b084f48`  
		Last Modified: Tue, 02 Jul 2024 04:02:26 GMT  
		Size: 202.6 MB (202610801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2d0a549cea7390c013b4e89302752b775d5f701c8f881cb5372aad0cc8e558`  
		Last Modified: Tue, 02 Jul 2024 20:49:54 GMT  
		Size: 6.2 MB (6239063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57792a6dc65d0f90b034cd836ecba1767cc3ed4ea32d58d5d2859b683e5dcb1e`  
		Last Modified: Tue, 02 Jul 2024 20:49:54 GMT  
		Size: 22.2 MB (22233902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37533368cc931539f624105561e929e193974f7fac06d6047927bd41e51aa019`  
		Last Modified: Wed, 03 Jul 2024 05:21:34 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1303ffd61bf4b00b8b87b2dc028ed46da653cc281383a13fe5d46587b4123d06`  
		Last Modified: Wed, 03 Jul 2024 05:21:34 GMT  
		Size: 2.8 MB (2796769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bookworm` - unknown; unknown

```console
$ docker pull python@sha256:00bdfc85fd2774f030c0b099aea94d814188e0705078bc81413b371066e35dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15912232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7543fee520107f16833e9cbd101e8efad0b8ca56a9cb40eab60b1ece0134c6c9`

```dockerfile
```

-	Layers:
	-	`sha256:8cca3217fc143f5efa0775da04898ba0f33cc51872953b9923dcec9684839e80`  
		Last Modified: Wed, 03 Jul 2024 05:21:34 GMT  
		Size: 15.9 MB (15886624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cb5238cd8107f3ab7d690bad43b9ce26731bc176bb2b8cbce56fd3190fbc36b`  
		Last Modified: Wed, 03 Jul 2024 05:21:33 GMT  
		Size: 25.6 KB (25608 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bookworm` - linux; 386

```console
$ docker pull python@sha256:add497ce4bdc25076c0554d4f17f66166b24f83ae7b2d62f98fbf3b08facdaae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.9 MB (382921050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12af98ebf675d016e7f65677b23ee5fbc609687a4d76b3b656ef95537c677f8`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 26 Jun 2024 21:58:20 GMT
ADD file:262529672396993121e97bbbdda3d91ce43c7548adf11a263b7ec53bb7cda4d2 in / 
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 21:58:20 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_VERSION=3.12.4
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
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
	-	`sha256:a2f6d105df66819de574b11515f546b93f62e53e533eaaa01918b446be25170c`  
		Last Modified: Wed, 03 Jul 2024 00:18:27 GMT  
		Size: 6.5 MB (6538494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e3cbcc7fdaefc9bab8a682bae56c9806fbd05363ec53c30e3392031beb65ce`  
		Last Modified: Wed, 03 Jul 2024 00:18:27 GMT  
		Size: 22.0 MB (21987995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fee09e8b39edcd863b3ac4fe35bfa2ed25117ef99e6e1fc0d46c19cb4b28e15`  
		Last Modified: Wed, 03 Jul 2024 00:18:27 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc9b5c697deb543b4bf8b4d147d13b57f81f3f56103814fc562b5b3382fa97d`  
		Last Modified: Wed, 03 Jul 2024 00:18:27 GMT  
		Size: 2.8 MB (2796711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bookworm` - unknown; unknown

```console
$ docker pull python@sha256:63a543de54cfd2c3803896d3388b95543ea7911774d7be5d7508b990b1d149a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15862183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e22cb48c39b7a2713b8b6edf5c5ecc7f98e0d10bd47139a11dbe9e77a5dc275`

```dockerfile
```

-	Layers:
	-	`sha256:1d96237dcebc39c55be78b0086ac0601a62032f2d72fa09839ac73eaa3542309`  
		Last Modified: Wed, 03 Jul 2024 00:18:27 GMT  
		Size: 15.8 MB (15836991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a6edd842d336de67b160e3b2664abec5e739ee5e9b8b53740d29ee22653e08`  
		Last Modified: Wed, 03 Jul 2024 00:18:26 GMT  
		Size: 25.2 KB (25192 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bookworm` - linux; ppc64le

```console
$ docker pull python@sha256:e8ff006a649c9891dac5a4afb99be8592b8527dc7f256755bcfb3d0449480af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.6 MB (395569470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac8813f463501341bca0e5ace6a3097629d1006bb325b31921d06adfca23f8c`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 26 Jun 2024 21:58:20 GMT
ADD file:a02c311ba745dd8d5b3cc5585e2fe57a4aa9807b1ca2005815257da116010b54 in / 
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 21:58:20 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_VERSION=3.12.4
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
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
	-	`sha256:363a81c416c83e946ff14010a7ad9745dd2bf0b99e57b0a7f44f8a140f67a0b2`  
		Last Modified: Wed, 03 Jul 2024 12:08:23 GMT  
		Size: 6.9 MB (6899610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be05aa7baa4d1a8d609f21b9e8aa2e8137ced67227a71a7e2c304763893f70a`  
		Last Modified: Wed, 03 Jul 2024 12:08:23 GMT  
		Size: 22.8 MB (22786065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246dcb1c1b184acb4bbe94fbb6ebeec469f278ef28aa69303157576ee7f7c71`  
		Last Modified: Wed, 03 Jul 2024 12:08:22 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5c8924112a3c59a125a2bff962faac630ef8af364e22011e78ebac2772982b`  
		Last Modified: Wed, 03 Jul 2024 12:08:22 GMT  
		Size: 2.8 MB (2796744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bookworm` - unknown; unknown

```console
$ docker pull python@sha256:0397210c3622fb98cf4a1f452aff812d04634d24c0dfb0d473890571b8a349e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15860140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b09dfb19d5ac4c0ac45e5b8127f72c8b967c32b196d8af23245216725d9e2bc`

```dockerfile
```

-	Layers:
	-	`sha256:5708a91cac8eb8c987676c9f54578f1b5656a0a03e5835d5c27481ae64b79251`  
		Last Modified: Wed, 03 Jul 2024 12:08:23 GMT  
		Size: 15.8 MB (15834824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:112b1dcd8f6f64a7797aba2e6fc7a1c5d67fcafd2799b10e722694e26af183f3`  
		Last Modified: Wed, 03 Jul 2024 12:08:22 GMT  
		Size: 25.3 KB (25316 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bookworm` - linux; s390x

```console
$ docker pull python@sha256:eec2b40812d58db2e3750765d6794b5cf6c851152b13fcb29a5886f47354a095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.7 MB (349693851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00cc82b4d5a17f96c8a34ddf16946c394e7c61bdbacb61cbad13566179fbacf1`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 26 Jun 2024 21:58:20 GMT
ADD file:397aa43721bc5ca67ab359263843a05c62e131f07114e92f39927f59790c9a5b in / 
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 21:58:20 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_VERSION=3.12.4
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
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
	-	`sha256:f05ca37c212e6bac1dbc6bad3537f8f5d0bcf10b0fe13882ba37f71c2fa3f096`  
		Last Modified: Wed, 03 Jul 2024 04:53:22 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb08b902ec590a650ad9a0f53de09b5d4e096973e5a49392282ee05543583ad`  
		Last Modified: Wed, 03 Jul 2024 04:53:23 GMT  
		Size: 2.8 MB (2796753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bookworm` - unknown; unknown

```console
$ docker pull python@sha256:134c573f36de4060028dea915b2bcd4f59df799465f242e3490d71ade10f054e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15697904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2713fd0d3656a924176376f5c0c7958efaa760983fcfff1e3077f32357484d14`

```dockerfile
```

-	Layers:
	-	`sha256:e865562f35e555324fd807d9c516d55f8cec8781fd8911e8d014d97b101e056a`  
		Last Modified: Wed, 03 Jul 2024 04:53:23 GMT  
		Size: 15.7 MB (15672656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54768765c84d42ff90fbd43077f95c4b0b794e6fd04f0f113bb5f58ded410318`  
		Last Modified: Wed, 03 Jul 2024 04:53:22 GMT  
		Size: 25.2 KB (25248 bytes)  
		MIME: application/vnd.in-toto+json
