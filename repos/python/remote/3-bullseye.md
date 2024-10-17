## `python:3-bullseye`

```console
$ docker pull python@sha256:86f90d7b66bd0a92a69d6c79fd011b37efa22f492f0ba285b100b6a696bd7e52
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

### `python:3-bullseye` - linux; amd64

```console
$ docker pull python@sha256:45a0698849395e9b6ed1648f04bff93aeb260e075e4abe4d9e6137258322e23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.8 MB (354827601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a23a0e8def20018bc24c5c424ff9b2475e51f834c8b22192ed91471986de303`
-	Default Command: `["python3"]`

```dockerfile
# Mon, 07 Oct 2024 18:55:41 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Mon, 07 Oct 2024 18:55:41 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 18:55:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 18:55:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 18:55:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 18:55:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 18:55:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 18:55:41 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 07 Oct 2024 18:55:41 GMT
ENV PYTHON_VERSION=3.13.0
# Mon, 07 Oct 2024 18:55:41 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 07 Oct 2024 18:55:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 07 Oct 2024 18:55:41 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06817e07ed0f03c17ad0a7aa8ef22b2a6fcf2b939d6212ab0861571ef18a45b`  
		Last Modified: Thu, 17 Oct 2024 01:10:51 GMT  
		Size: 15.8 MB (15764889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2173ffc78585eeabe33105e00a7be99b0cad17d5e6edebf7f760d7824fa76969`  
		Last Modified: Thu, 17 Oct 2024 01:11:06 GMT  
		Size: 54.7 MB (54723650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe335f0e34a87e4cbd05c121253490f0c293f8ff29540aa8cd3fc22d4519931`  
		Last Modified: Thu, 17 Oct 2024 01:11:36 GMT  
		Size: 197.1 MB (197085334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18244fcc9f079b5680c0128874e5306943611d9730d2c023105ca6bc76d9c35`  
		Last Modified: Thu, 17 Oct 2024 03:04:30 GMT  
		Size: 6.1 MB (6051872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6f92f260a92d31dc16fd5b43d9ebae3b2fef1ad5f5e0df6d3a99eae497f954`  
		Last Modified: Thu, 17 Oct 2024 03:04:31 GMT  
		Size: 26.1 MB (26120997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfc438d1e7e71dfa4ab5653bc87c099eea736d4f9c448c72b79777652a38e3d`  
		Last Modified: Thu, 17 Oct 2024 03:04:30 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:3e3db979e49b774f411ab34f0610fa29b53f5f9e1ead588a6db3c1eb644c3d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15559876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7debadec39e451c437c620bc6ea9a8a921bd0554e89ae299a5d1df1fb41c228`

```dockerfile
```

-	Layers:
	-	`sha256:0f62c14d9d48eb47500ba5109573033fc7384aa10d9814a16e1af497c57abe44`  
		Last Modified: Thu, 17 Oct 2024 03:04:31 GMT  
		Size: 15.5 MB (15539889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e45e80324da123f16f4d5ee5c407413bb3f248822dcbdcee21b886de4a0782b`  
		Last Modified: Thu, 17 Oct 2024 03:04:30 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; arm variant v7

```console
$ docker pull python@sha256:0a8e38f4ea583b4e4eca76bc27f2ae7493990af187a1329b98c70a5ffceb6ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313964492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8722a6fecde64d6ee18a13547c247dfcde153d2c58c3bb41a67b00bc6ddf6b4b`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:55 GMT
ADD file:9ce266c398209e90f7206a05ac5b3ad0e1b36639b555d8c794491312b40e94cc in / 
# Fri, 27 Sep 2024 05:13:56 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:31:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:33:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 18:55:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 18:55:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 18:55:41 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 07 Oct 2024 18:55:41 GMT
ENV PYTHON_VERSION=3.13.0
# Mon, 07 Oct 2024 18:55:41 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 07 Oct 2024 18:55:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 07 Oct 2024 18:55:41 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:5b73fe599d8a11adf217817ed59555cdbc95d93efb1d72ea85683e0e5ea179d6`  
		Last Modified: Fri, 27 Sep 2024 05:17:30 GMT  
		Size: 50.2 MB (50240380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec523352a6e63a855ebebdbc8288b9cccf719fe4121211d5e0cae3f11e4f6b2`  
		Last Modified: Fri, 27 Sep 2024 07:39:46 GMT  
		Size: 14.9 MB (14879678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bfb8add2d4bda22b21df2a3eff38a6f4f66c2ef9fe110e7714a93f720a4f47`  
		Last Modified: Fri, 27 Sep 2024 07:40:06 GMT  
		Size: 50.6 MB (50618560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f69bcefdc97cf5fabaf3b01d416ce54278fa217058c4433beb68d39a6e1bc1`  
		Last Modified: Fri, 27 Sep 2024 07:40:47 GMT  
		Size: 167.5 MB (167508654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0499dfe0aa29f4f2aa11a27cc1fb5d1804209d57d0ddc8bc9dc81310ccc5fddd`  
		Last Modified: Sat, 28 Sep 2024 02:07:25 GMT  
		Size: 5.5 MB (5460971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e544450152b9ea5f3e6268104bf4ebb6d826880bb0eecdbd59378e752dddb31`  
		Last Modified: Tue, 08 Oct 2024 00:50:32 GMT  
		Size: 25.3 MB (25255999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46c91b1604ddb1f60c72e0c1f64fd33193d180cdbb950ca9fbed57917ac8102`  
		Last Modified: Tue, 08 Oct 2024 00:50:31 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:6f50263f17ca46bd03791fded4e6865d09bf05dc98d1a5f64ffdf8b10898ab95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15360872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9048d3c77764897f02dd2f96fb95da883b7477fc5e98b886608b4dd96cad9187`

```dockerfile
```

-	Layers:
	-	`sha256:dc5c39939a3afacfc0d6522cde42dad2a0890f22f42e11599eb8a565d125a5f2`  
		Last Modified: Tue, 08 Oct 2024 00:50:31 GMT  
		Size: 15.3 MB (15340823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb12039e1a3350a068fdb29673dbec6f63f31c948d71fcfbe3d0418a9f8620ac`  
		Last Modified: Tue, 08 Oct 2024 00:50:30 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; arm64 variant v8

```console
$ docker pull python@sha256:47f4f2987543a4ce316ad422adf58158bfd2f915d09e33b04dbb2e55db581fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.3 MB (346263770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e3f54b6285f36fa62b3d6473df8e1ed6f6eaa9058a7ba2623404f8b8da3022`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:20:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:20:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 18:55:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 18:55:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 18:55:41 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 07 Oct 2024 18:55:41 GMT
ENV PYTHON_VERSION=3.13.0
# Mon, 07 Oct 2024 18:55:41 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 07 Oct 2024 18:55:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 07 Oct 2024 18:55:41 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4bba36b8add5e5ec5da6aa2c18637b64bce2d5f3f7d83723817e2139a11bcc`  
		Last Modified: Fri, 27 Sep 2024 05:25:50 GMT  
		Size: 15.7 MB (15749698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f212bcfdd3a473cde2991df3e1cf5373d8f097a630557a35fa77d891acce93d6`  
		Last Modified: Fri, 27 Sep 2024 05:26:04 GMT  
		Size: 54.8 MB (54834694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe09310330a122777457e6d6b3094e1d1391aa246ba1b028adeb03cd353d0d29`  
		Last Modified: Fri, 27 Sep 2024 05:26:28 GMT  
		Size: 190.0 MB (189964252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b795c60f1d295f4ee1917aba25e42e874f2185fda42adeddbf3ba58536a0133`  
		Last Modified: Tue, 01 Oct 2024 23:02:55 GMT  
		Size: 6.2 MB (6164670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a98175c9394c919092a0858d1b11eaeacebaaa9a84c8b0d4cd0eef2655077f`  
		Last Modified: Tue, 08 Oct 2024 00:31:00 GMT  
		Size: 25.8 MB (25816341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31a3e1c1a387ab62752653c6951356c5ac3712962626a097c95465c91ccc53f`  
		Last Modified: Tue, 08 Oct 2024 00:30:59 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:8cfd17c89187578724e15e41c102a4a035489debe18620417db00036a6f62dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15562198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd3740380ccd1471bcd7382c7af79b7797bfc8c1d64d20119b65129f56f0984`

```dockerfile
```

-	Layers:
	-	`sha256:feb644ddee8df44d3b8549fe53d514ef399a8d4ad03ca104bd3ac0ff6306f728`  
		Last Modified: Tue, 08 Oct 2024 00:31:00 GMT  
		Size: 15.5 MB (15542116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e058dcbf8ba5cc3ebdb5e49b3551671065cc961208e8012c3ad7c5c96277938b`  
		Last Modified: Tue, 08 Oct 2024 00:30:59 GMT  
		Size: 20.1 KB (20082 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; 386

```console
$ docker pull python@sha256:fa17e85e2a2529f0e3263eb99bd75ab289ced5bcc13e915c21daa4595df8243a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.1 MB (360087291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4644d9ba61aca4bb4e3f91f4b2186659903854347365bd16966c4a1b47947312`
-	Default Command: `["python3"]`

```dockerfile
# Mon, 07 Oct 2024 18:55:41 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Mon, 07 Oct 2024 18:55:41 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 18:55:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 18:55:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 18:55:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 07 Oct 2024 18:55:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 18:55:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 18:55:41 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 07 Oct 2024 18:55:41 GMT
ENV PYTHON_VERSION=3.13.0
# Mon, 07 Oct 2024 18:55:41 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 07 Oct 2024 18:55:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 07 Oct 2024 18:55:41 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000ce4e381f50a8f76ae5a1d4bcd9702f5146bac4fb30afc4e12c284ee68ca9`  
		Last Modified: Thu, 17 Oct 2024 01:10:55 GMT  
		Size: 16.3 MB (16268542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d0b1f51e6e34773cde9f3b41201942ff88384d907912b25ff3349f296f69b8`  
		Last Modified: Thu, 17 Oct 2024 01:11:14 GMT  
		Size: 56.0 MB (56032019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b257135cb04b7c9d5ceaf0572a0941a80b7eb3f7dd31444289a12b792e314e8`  
		Last Modified: Thu, 17 Oct 2024 01:12:01 GMT  
		Size: 200.0 MB (199982090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a402f1eac91da497f9b9c694233e3020847bbbf78c4ee62a05c656885004fa2`  
		Last Modified: Thu, 17 Oct 2024 03:10:01 GMT  
		Size: 6.4 MB (6441612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ad1aa118dc193858fefcb52cd9f47e6b018b7e11b51f780c721d3cfa0e8063`  
		Last Modified: Thu, 17 Oct 2024 03:10:01 GMT  
		Size: 25.3 MB (25284955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c333f78be07faaf2cf8253ab0d848c8fa2a965c22599f105de395c40d8491998`  
		Last Modified: Thu, 17 Oct 2024 03:10:00 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:6eff6374b0f0bb9b079660b6807d5a7fbc6f18cc11ac9ebe76b40b36b0b5fea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15548328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19044099cb8ae11cad24b1bddfe68eab15a3c53c1323c9886630b2e39fb661f3`

```dockerfile
```

-	Layers:
	-	`sha256:47da8491a8fab6656419c2a83ddd74053dc5725e90461b3ff9b7b0716659b283`  
		Last Modified: Thu, 17 Oct 2024 03:10:01 GMT  
		Size: 15.5 MB (15528374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4494b199f97e98c56fa80c5103f94795e9321cbd9ce057bb6f8cdcfc397a1821`  
		Last Modified: Thu, 17 Oct 2024 03:10:00 GMT  
		Size: 20.0 KB (19954 bytes)  
		MIME: application/vnd.in-toto+json
