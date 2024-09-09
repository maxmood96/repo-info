## `python:3-bullseye`

```console
$ docker pull python@sha256:02ca52f5ed91e3dc7100bc108d6559865f4503902413cf28aaa6204fbb31c6f7
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
$ docker pull python@sha256:857f26712845994fad2dee8bf2697f73109a81bce3472e0917e68a421b3626e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.3 MB (353275336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d64d4840747e886ca43d5989f0e1a5e1903f6411b80264462eb327ac133216d`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:56 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Wed, 04 Sep 2024 22:30:57 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:56:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:57:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 16:46:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:46:54 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 16:46:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:46:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 09 Sep 2024 16:46:54 GMT
ENV PYTHON_VERSION=3.12.6
# Mon, 09 Sep 2024 16:46:54 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Mon, 09 Sep 2024 16:46:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 16:46:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Mon, 09 Sep 2024 16:46:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Mon, 09 Sep 2024 16:46:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Mon, 09 Sep 2024 16:46:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 09 Sep 2024 16:46:54 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d691dff6d17d00b0cbbc4772eb805d97e02504d89ea3e5857cb97c943b74462`  
		Last Modified: Wed, 04 Sep 2024 23:02:33 GMT  
		Size: 54.7 MB (54726023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cfd30604666dfdd92bea930c06ee58dc927e0da651b862491af1648a4aca73`  
		Last Modified: Wed, 04 Sep 2024 23:03:03 GMT  
		Size: 197.1 MB (197067753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0617c566fa49ba91511f26295ffe31d7276bd5237c369f3b2014f4689add9e`  
		Last Modified: Mon, 09 Sep 2024 18:06:57 GMT  
		Size: 6.1 MB (6051803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f98cdf65e490dc360cae257ec36e2bd06f45581c4c591697524257bb70107a`  
		Last Modified: Mon, 09 Sep 2024 18:06:57 GMT  
		Size: 22.9 MB (22909958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805d33221dcefc9d463add0ba46ba0ec3f0412a23cd64399b7c8492b30d15100`  
		Last Modified: Mon, 09 Sep 2024 18:06:57 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e66a1f9fe00967311c4119de7d6eb58a4e297048942d00d192be94db4107e7`  
		Last Modified: Mon, 09 Sep 2024 18:06:57 GMT  
		Size: 1.7 MB (1673839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:6d3082416e0343acb8946767fb63f9aacffd94c993f7cadbfc6032b141a848b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15563947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20632ba1fed566e4d70f379feedd0f55b0a99d70ccba7ea97847b9432749a10`

```dockerfile
```

-	Layers:
	-	`sha256:db9db11013cb901a007d366751559ef7de96654db6c6bdb334d684ce221a8254`  
		Last Modified: Mon, 09 Sep 2024 18:06:57 GMT  
		Size: 15.5 MB (15539714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b048b4ce082d05b5264c955b48bd0ceb08d9e477eb60b8c4b0ef0598934eb880`  
		Last Modified: Mon, 09 Sep 2024 18:06:57 GMT  
		Size: 24.2 KB (24233 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; arm variant v5

```console
$ docker pull python@sha256:961e7cc40bd74833268f6ba491780e0675b10bbd08393b4e120aff9f51c68554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325359369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdf23a944bae5420c65e2e6431a0f106d076790ca03c2c9038fa4ddab033877`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:39 GMT
ADD file:f6ccc0737bdcac3d7694a1fd4ab0609c22377d55dbc283a021ed8df0d5ee807d in / 
# Wed, 04 Sep 2024 21:48:40 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:17:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 00:17:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 00:18:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 16:46:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:46:54 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 16:46:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:46:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 09 Sep 2024 16:46:54 GMT
ENV PYTHON_VERSION=3.12.6
# Mon, 09 Sep 2024 16:46:54 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Mon, 09 Sep 2024 16:46:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 16:46:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Mon, 09 Sep 2024 16:46:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Mon, 09 Sep 2024 16:46:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Mon, 09 Sep 2024 16:46:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 09 Sep 2024 16:46:54 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:9fc6954b7a342e92200747f4676bd2b9223d22aee96dec921c2d55657e0bdaeb`  
		Last Modified: Wed, 04 Sep 2024 21:51:52 GMT  
		Size: 52.6 MB (52582753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af64ccde22e77ee4dbfcddc6165730a7acf92e30572bc7ca38ce8823aab8bea`  
		Last Modified: Thu, 05 Sep 2024 00:25:07 GMT  
		Size: 15.4 MB (15375718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7a961b5130e4ecfa7355c211a605995662ab52f22cdedca888a80a28b50499`  
		Last Modified: Thu, 05 Sep 2024 00:25:23 GMT  
		Size: 52.3 MB (52329511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722539d9a39ccb4043e4974ec89b17b8abff2a5cab04be7be1490350d3f7a9a7`  
		Last Modified: Thu, 05 Sep 2024 00:25:54 GMT  
		Size: 175.2 MB (175237132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81a2528b9f1d90c85beeb225a0b58b8a9202b238e2683bb7e980e538a1dd9af`  
		Last Modified: Fri, 06 Sep 2024 01:54:01 GMT  
		Size: 5.8 MB (5777059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb83738a88276e49d6b304e0c50572564a03ede9e302d2ebdb53f583b2bc59b0`  
		Last Modified: Mon, 09 Sep 2024 19:54:07 GMT  
		Size: 22.4 MB (22383109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a942b7e40a6da27156df856b9662e0341291033ae2531efffac7a66f19ca01`  
		Last Modified: Mon, 09 Sep 2024 19:54:06 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbe81daaa81d282a7e4179374384d1f55d5d722d942d47ceeae84674ea451a7`  
		Last Modified: Mon, 09 Sep 2024 19:54:06 GMT  
		Size: 1.7 MB (1673854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:e551fd72e6719d8913185431c624b8ee53367115023b513117ef7c7565959030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15359732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb8a39ecbce9e4852f4faddaadcbcfc4398107e8d3f0162589bb587ddbab903`

```dockerfile
```

-	Layers:
	-	`sha256:ddf6b70491dd6aa3ed8dcc9d8979e28b7527bce312af4e8ed5cb20c89ec16bb4`  
		Last Modified: Mon, 09 Sep 2024 19:54:07 GMT  
		Size: 15.3 MB (15335390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c66c4d935c278947ffc380c8ef7b9d1a4d2592da7278d82fad0b02e345daab6`  
		Last Modified: Mon, 09 Sep 2024 19:54:06 GMT  
		Size: 24.3 KB (24342 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; arm variant v7

```console
$ docker pull python@sha256:57ef9e98f9c345521f150a7c4eda6928b21f722116912b1f6d087c936faca2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.5 MB (312538444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812c3bc250081a73d888ea7be1d7ac5da38500b2fb77655b3e1ce127054a594a`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 29 Aug 2024 23:26:33 GMT
ADD file:e3043c245364d9fe593e24bbcac51334dca659e8ec7cd42b6368ba7ea83ea087 in / 
# Thu, 29 Aug 2024 23:26:33 GMT
CMD ["bash"]
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 23:26:33 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_VERSION=3.12.5
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_PIP_VERSION=24.2
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:3e424c6173543918aac0bf0552ca8359d23f7b7baa2d77fc8e2c9deb6756f39d`  
		Last Modified: Wed, 04 Sep 2024 22:02:04 GMT  
		Size: 50.2 MB (50240273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0451e8e66d2aa4834e6580560eb32abf8bbac64409d70c85811226b651f2aba`  
		Last Modified: Wed, 04 Sep 2024 22:37:06 GMT  
		Size: 14.9 MB (14879935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a810222c5e9f2cbfb1260daae6fe81f9c63f9fa8cad05812e717e0135194dd`  
		Last Modified: Wed, 04 Sep 2024 22:37:24 GMT  
		Size: 50.6 MB (50616939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae26722d7d3c0994148ae4ede7eb08ae409fa7ac05c21ff66d41b5f7966fcad`  
		Last Modified: Wed, 04 Sep 2024 22:37:57 GMT  
		Size: 167.5 MB (167509349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3756c7f6b50019520fa504ba05924179789ace9ed185a1cff02f5bd958d2f061`  
		Last Modified: Fri, 06 Sep 2024 02:47:11 GMT  
		Size: 5.5 MB (5460217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067df0d1552d21680a4cefe0997d2b9b7e74e491537337bbbf14df583684530c`  
		Last Modified: Fri, 06 Sep 2024 02:47:12 GMT  
		Size: 22.2 MB (22157664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1422e8a1f91ad6d2f6a8159a65eaa8f76905be19665e1b1a06bcef5dbef8adc1`  
		Last Modified: Fri, 06 Sep 2024 02:47:11 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9d7ccd13ce38fdc8c1aa71c6ce0ab2ee25c7d50d26edce2c3a8bb2b3ade015`  
		Last Modified: Fri, 06 Sep 2024 02:47:11 GMT  
		Size: 1.7 MB (1673835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:a8501d9e80d5aa9f34d84fdb237f723faf6c21c00596879338a8ce8826d3600d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15365152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d139ddfdb6a5e52c7b67e00c69a61ad822b3ac7183160d51d2195d7d921afed`

```dockerfile
```

-	Layers:
	-	`sha256:8f5cb685aed81173a980f0f45dcf213acd31fcb9cb8a3337705f11a77ecd549e`  
		Last Modified: Fri, 06 Sep 2024 02:47:11 GMT  
		Size: 15.3 MB (15340810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a334c9f95711cbedc3940565ce1893a05f6c1776348fb46cb261ed07a7be635d`  
		Last Modified: Fri, 06 Sep 2024 02:47:11 GMT  
		Size: 24.3 KB (24342 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; arm64 variant v8

```console
$ docker pull python@sha256:c8bb6ff43cc9e51dc28cb566090d2ee71efbf5871e5233aea204763a36d83d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.8 MB (344772177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbac6a827a1b6c5ef69e67e03ee369f5fab73f9e498f1de74b8d4a3decf0139d`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:59 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Wed, 04 Sep 2024 21:40:00 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:03:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:04:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 16:46:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:46:54 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 16:46:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:46:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 09 Sep 2024 16:46:54 GMT
ENV PYTHON_VERSION=3.12.6
# Mon, 09 Sep 2024 16:46:54 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Mon, 09 Sep 2024 16:46:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 16:46:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Mon, 09 Sep 2024 16:46:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Mon, 09 Sep 2024 16:46:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Mon, 09 Sep 2024 16:46:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 09 Sep 2024 16:46:54 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf248fd698830ce7c74f07fb7ca6adac7bea55a16521e9e1f2afe06219e00f6`  
		Last Modified: Wed, 04 Sep 2024 22:08:56 GMT  
		Size: 15.7 MB (15749712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b216df41d3eb392b55b4bb8c654fe024d7c3d00404a7e105f494ef43990fad`  
		Last Modified: Wed, 04 Sep 2024 22:09:10 GMT  
		Size: 54.8 MB (54833449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2c74c1774e448d6bb324968dd639df704566af4ae9461a86ec79cc6e8de709`  
		Last Modified: Wed, 04 Sep 2024 22:09:38 GMT  
		Size: 190.0 MB (189961799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18108ef85c47a3dd40a04d776309dbae88db956d6f82780d996ca999bd193007`  
		Last Modified: Mon, 09 Sep 2024 19:49:30 GMT  
		Size: 6.2 MB (6164679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf35baa3706a3fb2b18976abc493c71ecbda13a08e5a74359292070d5cbea3d3`  
		Last Modified: Mon, 09 Sep 2024 19:49:30 GMT  
		Size: 22.7 MB (22656857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccad44d06f1e47207375439e6436a6cbc9544775bd960ed6a45a443f583a0b0d`  
		Last Modified: Mon, 09 Sep 2024 19:49:29 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c349eb8e9ca142005f974b02c875a7ed37bc1e8ed360eecc79fa68e8354fc09`  
		Last Modified: Mon, 09 Sep 2024 19:49:29 GMT  
		Size: 1.7 MB (1673830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:c06da11099448c31691c861b6ef1add8c20b17a319417655e737710dab64b85b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15566648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7ddfaa6872461f6857632661355138d6468be3d5021bc0199e5b3531981c6a`

```dockerfile
```

-	Layers:
	-	`sha256:7b48796dc7f425c9665e06ec01ff723a093beb64dafb86f3f54785158d8df520`  
		Last Modified: Mon, 09 Sep 2024 19:49:30 GMT  
		Size: 15.5 MB (15542103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d75113f2f75c26eb9d7decb3b1fd118a19a729c12a1370f9a67f9a2817cd140`  
		Last Modified: Mon, 09 Sep 2024 19:49:29 GMT  
		Size: 24.5 KB (24545 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; 386

```console
$ docker pull python@sha256:0b215eaeafbee3060db041be53f3fb286d19934573c9b6953cf51abe33fe65a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.6 MB (358572109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59acba3ce85b2d7f20f985855fdbbd08f89badbed0e465254255ef8e20ed9225`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:44 GMT
ADD file:1d8ae4e7067486ce0279b3d90aaecbc5973872ad64266d252bfa3fd5e4fc2e5f in / 
# Wed, 04 Sep 2024 22:44:45 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:14:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:14:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:15:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 16:46:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:46:54 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 16:46:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:46:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 09 Sep 2024 16:46:54 GMT
ENV PYTHON_VERSION=3.12.6
# Mon, 09 Sep 2024 16:46:54 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Mon, 09 Sep 2024 16:46:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 16:46:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Mon, 09 Sep 2024 16:46:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Mon, 09 Sep 2024 16:46:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Mon, 09 Sep 2024 16:46:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 09 Sep 2024 16:46:54 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:c6549675a9e3cbb8e77f08089828d3b4f24a06d332dc86c4d140aa273748ba57`  
		Last Modified: Wed, 04 Sep 2024 22:48:29 GMT  
		Size: 56.1 MB (56076167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4533261556c046eefdf517bc6e06bc455b876caf2226aa504a13b5d66d250281`  
		Last Modified: Wed, 04 Sep 2024 23:21:18 GMT  
		Size: 16.3 MB (16268301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341d50e4bbed9704aae2147f28b4a07fc71b73539d282c37f60e183d38865daf`  
		Last Modified: Wed, 04 Sep 2024 23:21:37 GMT  
		Size: 56.0 MB (56030074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d04d357b859cf9b5eb038042f7df289289aee35371021b6ba1005ff2818f428`  
		Last Modified: Wed, 04 Sep 2024 23:22:18 GMT  
		Size: 200.0 MB (199965007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee3246bb9aa2607b5117d32799a260098220dce6a35d39c003c98e053e44b4d`  
		Last Modified: Mon, 09 Sep 2024 18:13:07 GMT  
		Size: 6.4 MB (6441576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6098556e2d5c20bf7ca86363ab21ec9cc793f0a917a5689d2a95ab31e07d18ba`  
		Last Modified: Mon, 09 Sep 2024 18:13:08 GMT  
		Size: 22.1 MB (22116926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37959711fdfbcd1478fddd4913dac298ed7c3fe86aa66daaac0bafff4f7e13e7`  
		Last Modified: Mon, 09 Sep 2024 18:13:07 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a82d98000181c0642ff05d8bf3b1558f06fb7dde27b383c5351e0484947bf00`  
		Last Modified: Mon, 09 Sep 2024 18:13:07 GMT  
		Size: 1.7 MB (1673827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:3d426de145cc12962c812b32daf31b305be7de170af45cbdfbe43bea5026122a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15552397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbbb596c4d4c7d729403377d8dbdd69f4e50d130aa751ba4e6d8ccd260b52f8`

```dockerfile
```

-	Layers:
	-	`sha256:7a4ae44ee5eecc830d5ff3223cd0acda3e2465a532319a004d941eac18476a37`  
		Last Modified: Mon, 09 Sep 2024 18:13:07 GMT  
		Size: 15.5 MB (15528199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f98cbc5d7ad046462d3d6f6f30013a285bfdd7492601e43c29dbb8d5065109`  
		Last Modified: Mon, 09 Sep 2024 18:13:07 GMT  
		Size: 24.2 KB (24198 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; ppc64le

```console
$ docker pull python@sha256:868a60c28140471537835ff89df94fabf8dc895cd61877a7e9afc3481a530bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.3 MB (362258562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ecaa19c4896020299c27c2a7f52685d5c8bbceead3383e8be3481d122df898b`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 29 Aug 2024 23:26:33 GMT
ADD file:af2c25052aab46bab5ee70bf1b7f7c8d0339d147a2bd4daeb04ec25bd34e4799 in / 
# Thu, 29 Aug 2024 23:26:33 GMT
CMD ["bash"]
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 23:26:33 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_VERSION=3.12.5
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_PIP_VERSION=24.2
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:a8e5e0425eb7845f41056f6e5fe36c228a23a602de31f39d88868def2b2bf980`  
		Last Modified: Wed, 04 Sep 2024 22:30:31 GMT  
		Size: 59.0 MB (58950090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e76b45808a7b15592738cc59f261bb4109d1d280c5fa410f157dd270ddbf8c9`  
		Last Modified: Wed, 04 Sep 2024 23:14:50 GMT  
		Size: 16.8 MB (16766250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb7a5e65d3cbab78e31accfce79b09855b78c5b547ef6a738d98e4678a2af87`  
		Last Modified: Wed, 04 Sep 2024 23:15:06 GMT  
		Size: 58.9 MB (58872541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49975637c562cd117e86d9b35bd61ab045430938723115feadf0b276d917f54`  
		Last Modified: Wed, 04 Sep 2024 23:15:41 GMT  
		Size: 196.4 MB (196413350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a30629a93af93ef18b702085c0074cef35c1a71a05ab283295740ea042e53ed`  
		Last Modified: Thu, 05 Sep 2024 20:47:19 GMT  
		Size: 6.8 MB (6801849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcab017bf7eb6bff7752012a3c6322430f3bc3145e794c12914f1697e0ad4047`  
		Last Modified: Thu, 05 Sep 2024 20:47:19 GMT  
		Size: 22.8 MB (22780418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d735a85a8a71b36c49cfe68183a465f9b058709cad566a6ea3733d92ca441dbb`  
		Last Modified: Thu, 05 Sep 2024 20:47:18 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9e173bd5c48f1fbb42189724e5b9a9e927c271bbebb6d006364b0bd73ea5c9`  
		Last Modified: Thu, 05 Sep 2024 20:47:18 GMT  
		Size: 1.7 MB (1673832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:56f37dad3e8d7a7db4954bd30e5c5fde1c2ead08fac37012b3e3f15c53102e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15533433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3eaa6c8e1a36f2ee9d4191f7c2858a81a861b7f1ae62233e1b8e781258254fd`

```dockerfile
```

-	Layers:
	-	`sha256:a49ad732cbe95ac132cfdfe8f6ad0521118d97301f52c2a8782932bf4fafab55`  
		Last Modified: Thu, 05 Sep 2024 20:47:19 GMT  
		Size: 15.5 MB (15509156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f649c721adcac2825361a7a983f782a3c00935a285e745de01de31dbb216f112`  
		Last Modified: Thu, 05 Sep 2024 20:47:18 GMT  
		Size: 24.3 KB (24277 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; s390x

```console
$ docker pull python@sha256:07c0a5f2d836c46f6f7ffcead1ab38c35dd856b2c4d6c287f3aa475f831240a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.6 MB (326634311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6771ab073b037497e8a1673e26ae028dae917ef0806f944af904c316673e59a1`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 29 Aug 2024 23:26:33 GMT
ADD file:855e3f68f57762c16941f4426d4c9911e4dcaf77abfb6d1993bd8c8f0d7e83b5 in / 
# Thu, 29 Aug 2024 23:26:33 GMT
CMD ["bash"]
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 23:26:33 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_VERSION=3.12.5
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_PIP_VERSION=24.2
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 23:26:33 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 23:26:33 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 23:26:33 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:52560ec7a98b7f8127e927ecee98fe2d97be23a6a2ec8ffbbb0b71455e06dc54`  
		Last Modified: Wed, 04 Sep 2024 21:47:54 GMT  
		Size: 53.3 MB (53317200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deb07fb0f47d9daa6d0bf809dee66d9c90207821b4a8f6c849f8287efdda0fd`  
		Last Modified: Thu, 05 Sep 2024 00:00:53 GMT  
		Size: 15.6 MB (15642390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed93d5f01b376419cd54d2ce3b7abf1bb4ab16f8c188ed6e0bca4959d860c9e`  
		Last Modified: Thu, 05 Sep 2024 00:01:05 GMT  
		Size: 54.1 MB (54075084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819f8402428b6e76aa2474a2ad7b60bda05d2333b58c0ce2e044e6474eb477b3`  
		Last Modified: Thu, 05 Sep 2024 00:01:31 GMT  
		Size: 173.0 MB (173047915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae490e2a50dcccda1e25f6496ae2b81aa97ed40dd6ec7b010295fe311a44f89`  
		Last Modified: Fri, 06 Sep 2024 01:26:10 GMT  
		Size: 6.0 MB (6001151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb101a7a30851df5f280220d5eecf9e91cf8b91fea3037c54ae953a484fa08c`  
		Last Modified: Fri, 06 Sep 2024 01:26:10 GMT  
		Size: 22.9 MB (22876515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae6d5141000eccef3d37df5d58f8e4993aee8bc667f9d335a4b2198ce910b86`  
		Last Modified: Fri, 06 Sep 2024 01:26:10 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2f93baa04c79cad06fc91af256f0fd8a050223e12689def8e24ed2d9b0b7c3`  
		Last Modified: Fri, 06 Sep 2024 01:26:10 GMT  
		Size: 1.7 MB (1673824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:36c082da9d0f2021b86f61a3f77b7ce267ee802e3b54c74c82da286ea72935fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15384881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357f93ad20d74897d7920211265dd20e859715d61a17370ca95b7fcd2f949ce7`

```dockerfile
```

-	Layers:
	-	`sha256:46f14dbca67e6a07694cb6d20d28b90801e756269b9fd588021cdd9229f55ec3`  
		Last Modified: Fri, 06 Sep 2024 01:26:10 GMT  
		Size: 15.4 MB (15360648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b2c73c03bc28f91cd42014ded828e421be3aecfbb321ef50852faf5d069e5a8`  
		Last Modified: Fri, 06 Sep 2024 01:26:10 GMT  
		Size: 24.2 KB (24233 bytes)  
		MIME: application/vnd.in-toto+json
