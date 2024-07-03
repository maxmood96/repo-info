## `python:3-bullseye`

```console
$ docker pull python@sha256:926092157cf70729a9b8f349134cae918a096886a698138c7de3eb45f5b5c28e
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
$ docker pull python@sha256:a74ecd3a22fd2acad3697943564d36e04777ae219e8b7ac3562a1c3e3ea6ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354453443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4dfe1a05512dfc75882121067f70ff841b00969af24518a2ce8b49cf0bb0de5`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 26 Jun 2024 21:58:20 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a305f523084f0a28b5daf532a5216d9be05d863c6bd3f5bd2969965eb7e9a27`  
		Last Modified: Tue, 02 Jul 2024 02:01:21 GMT  
		Size: 15.8 MB (15764174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da238dd9d1f579bf4f3cd6589e3ab75747f8ea35be2bf50403f8f3fafa942eea`  
		Last Modified: Tue, 02 Jul 2024 02:01:35 GMT  
		Size: 54.6 MB (54588637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414da18c1936c380bc310a14aa9627a150fd6e6393e752068962869f27d2907c`  
		Last Modified: Tue, 02 Jul 2024 02:02:06 GMT  
		Size: 197.0 MB (197018307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80df4e8bf17f81db8104f5b92a047eec5c61ddcffcce74eddd30012620a05e1d`  
		Last Modified: Wed, 03 Jul 2024 00:14:15 GMT  
		Size: 6.1 MB (6051049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47425031050be9bede3a729b8a9c46605f9a947d2107e4493247a2017515af0`  
		Last Modified: Wed, 03 Jul 2024 00:14:15 GMT  
		Size: 23.2 MB (23152926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7556b93cf6d679c9213319cc16e30f4590c0eb804541a2556e5f12ff776a8d`  
		Last Modified: Wed, 03 Jul 2024 00:14:15 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481c0778c04d96d6317c2689116171fd893e5c6fb241aa1733b31e0dde420c4b`  
		Last Modified: Wed, 03 Jul 2024 00:14:15 GMT  
		Size: 2.8 MB (2796752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:8ab57e2a548cc46248140e6d73b3deea4730b7cfe07aefc5be4557f343af08ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15486617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69801c76d94c9a45447a742d3d5209d3daef1eaabfca60e5199259bd2f8fd45e`

```dockerfile
```

-	Layers:
	-	`sha256:25be06101368e6d2cf78212f7c691345bf1aa7a3cab1df8c796baa195f4514c9`  
		Last Modified: Wed, 03 Jul 2024 00:14:15 GMT  
		Size: 15.5 MB (15462547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:478bb26c9daeb824467f6816bb98e4400fe9bc945338ee021d94fe580f368b56`  
		Last Modified: Wed, 03 Jul 2024 00:14:14 GMT  
		Size: 24.1 KB (24070 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; arm variant v5

```console
$ docker pull python@sha256:b61bafbf986ec614ce19fef18bd085ad5575461d9af0a040358c6c468ebc4b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326715096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b326ea0f55d762dd4209ee25224d98bd4bc7d5e28f747db85e62f7d5980655`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 26 Jun 2024 21:58:20 GMT
ADD file:cb32078a57dd8b6e640717e8afff9bcae9ea1cf42a7bd24509f83795da6d69ed in / 
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:cbbd165d7f0cb06245f1b11503844a1b512035157df3061a56ffc65bcd1fb0fa`  
		Last Modified: Tue, 02 Jul 2024 00:51:50 GMT  
		Size: 52.6 MB (52585748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55ce9f73827a53b1d65974ad06aecf88b83eb2b3dbde871489157a0a524be50`  
		Last Modified: Tue, 02 Jul 2024 01:23:51 GMT  
		Size: 15.4 MB (15375188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9122a9bdc64b2bf9d3d2754acd565e00d5cb246e7be6b39e5e2ab6d02e2b3a62`  
		Last Modified: Tue, 02 Jul 2024 01:24:09 GMT  
		Size: 52.3 MB (52328998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92d3c23f02c6a0096772f07544d2468710736f78f1ee80afd8fdef211fd9092`  
		Last Modified: Tue, 02 Jul 2024 01:24:42 GMT  
		Size: 175.2 MB (175212924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548cc47c117a3002ad34a1317f845a1930a3108605b474965db362cb39ccecb0`  
		Last Modified: Tue, 02 Jul 2024 20:35:43 GMT  
		Size: 5.8 MB (5777067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ab59d46ae80fbeb68fe5094e6d556d1b8dd30531de7eb9cdeed976460970f4`  
		Last Modified: Tue, 02 Jul 2024 20:35:49 GMT  
		Size: 22.6 MB (22638191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5929cd6f4ba6269c6ac5e612dff9e00026d835332e34c91ee22801dd95d419ed`  
		Last Modified: Tue, 02 Jul 2024 20:35:43 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cb4a1f4fbecfec39cb79da0342e3d166a39f06006b1caab6f5ca3643d717cc`  
		Last Modified: Wed, 03 Jul 2024 02:30:50 GMT  
		Size: 2.8 MB (2796748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:3de997147f9c6484c6338ab3a85a7193342abf7f4f6f9f9bce2317be17758fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15283260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d321ad39c456fa2a95b6f3672cb46e5b9edbc94e1d2161fb1dd474c4f13e1138`

```dockerfile
```

-	Layers:
	-	`sha256:da1754148e2a024380c7eee9fbd9673067dc98aecf4496f44378be81cf7eb46c`  
		Last Modified: Wed, 03 Jul 2024 02:30:50 GMT  
		Size: 15.3 MB (15259081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7149cbe5662fac588a6c865b107706b90d52915c889f5debeb325174661cb09f`  
		Last Modified: Wed, 03 Jul 2024 02:30:49 GMT  
		Size: 24.2 KB (24179 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; arm variant v7

```console
$ docker pull python@sha256:344b8f98fdb76d5fa71f1f441b41e91b4344084fe6998263f8a253dd20fa690b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 MB (313645565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a54a92467818a2197dd32634f48cc77956824245e15284edcc453aeee89c63`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 26 Jun 2024 21:58:20 GMT
ADD file:6e828fd5dbd54f949f96129ea922c27ff88709484119faef51401e338e900e6e in / 
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a0610bbe9cb80952dba5ef5efb55f03668fd4f8ab63ade3ba30e22a4c03c42da`  
		Last Modified: Tue, 02 Jul 2024 01:03:38 GMT  
		Size: 50.2 MB (50238998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c595e4d8c2d2c7ad66ab723b54c73c6a0aa876b01511358ec8af1aed8c8b94`  
		Last Modified: Tue, 02 Jul 2024 01:40:13 GMT  
		Size: 14.9 MB (14879331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577c5fe1f5243a6910c54b7b4a338cc9cbae0cfeba74a350b011d2a467e49daf`  
		Last Modified: Tue, 02 Jul 2024 01:40:31 GMT  
		Size: 50.4 MB (50358262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53a04feb4a55b8a4920c0ad42332dddf76ad9bb3bd19eac2f580036953cf88`  
		Last Modified: Tue, 02 Jul 2024 01:41:09 GMT  
		Size: 167.5 MB (167478798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8e9597253552182f5592005a3b1af72adce6eda6cef40ee9581d57343c67b9`  
		Last Modified: Tue, 02 Jul 2024 21:59:58 GMT  
		Size: 5.5 MB (5460202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac5819d8d1ac63a9bdaad5296f7ddbfccdf639c0a35769de8b70e19c1aee76d`  
		Last Modified: Tue, 02 Jul 2024 21:59:58 GMT  
		Size: 22.4 MB (22432978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b79c8219d8071d7231f457d2ab875f042584548b808196f85dbafd5120b3129`  
		Last Modified: Tue, 02 Jul 2024 21:59:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfa52a750c1fdbc041905ee97a67cf67d7f789ad129e3441d0d2e006a277b29`  
		Last Modified: Wed, 03 Jul 2024 06:48:02 GMT  
		Size: 2.8 MB (2796766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:c4027edb8f02681d9286b0b7a1c29f03545a5500f233b8ca037dc2e1601c84f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15288680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044e06b460a520b3a33745f84210e450c05ceb1804eb314785b789b12b7e6380`

```dockerfile
```

-	Layers:
	-	`sha256:8112f9d57019d37e1227d737b6cffeb01f9f669ead5a1b1866fc030263ec79dc`  
		Last Modified: Wed, 03 Jul 2024 06:48:02 GMT  
		Size: 15.3 MB (15264501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fffcfa153bb88c63a165716ad7b740138e86455bb7f4d9bd1f42f4e591b1a54c`  
		Last Modified: Wed, 03 Jul 2024 06:48:01 GMT  
		Size: 24.2 KB (24179 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; arm64 variant v8

```console
$ docker pull python@sha256:7dc644244b907f35d3501bd3cd548c117a51de032f9a922c48168ccaf154c875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.0 MB (345977393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f249fae48b1f0af0bec49a736782aeacdce8110e4ac8eb2cb96f0bb99f79363e`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 26 Jun 2024 21:58:20 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d9ac7785741df545f96a8744d3a9a5c29f75a171fb8de0a0bae196294ad50`  
		Last Modified: Tue, 02 Jul 2024 04:02:37 GMT  
		Size: 15.7 MB (15749565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eeecfcb7b2ee9a8806953208440dbffd4b9110e5d2950924c7395e7ea3c070`  
		Last Modified: Tue, 02 Jul 2024 04:02:51 GMT  
		Size: 54.7 MB (54695057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c75f0ece8974d005f2532701f9fffb099d09a9bd1a53465b796982e4c2f594c`  
		Last Modified: Tue, 02 Jul 2024 04:03:16 GMT  
		Size: 189.9 MB (189935947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b835256a972db611db1dc22447abc4e61151696587fa8f12c3e8425854519ab5`  
		Last Modified: Tue, 02 Jul 2024 21:10:26 GMT  
		Size: 6.2 MB (6163663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65d3b86b487297cef6764548695672b2f7810e2699590dd63ef462817080bc1`  
		Last Modified: Tue, 02 Jul 2024 21:10:26 GMT  
		Size: 22.9 MB (22914552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987170d32e9712f4b8ac42b346609abcaa11245b9d7d399120e6855fed519e4f`  
		Last Modified: Wed, 03 Jul 2024 05:22:43 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b109361570afa94b44e88329af6626be95c5c2f3c20e08653427f5be3ab6af2`  
		Last Modified: Wed, 03 Jul 2024 05:22:44 GMT  
		Size: 2.8 MB (2796727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:2b6ab6e0ffb08a25a4e809b62691c575be5f96f32224ba2b6eb6e2dcaa5969aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15489461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e3bbcf33b368df16a98228e65abf8c5f5ef6110ab014b6bfc3b1dc88a5a779`

```dockerfile
```

-	Layers:
	-	`sha256:7afbbb7eb4c46dd95295e058af2350fa2c4656e6930465f8740b4a5a3eb6d520`  
		Last Modified: Wed, 03 Jul 2024 05:22:44 GMT  
		Size: 15.5 MB (15465079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6488941070e2ce2e48b193635da7cba2d5f9d8ecd409e0406ac01337ada0aae6`  
		Last Modified: Wed, 03 Jul 2024 05:22:43 GMT  
		Size: 24.4 KB (24382 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; 386

```console
$ docker pull python@sha256:346cac3bf2d30c14dd663fe7a0012b145ae4d772b5aca12151e0877de221f59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359788036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4b56639344f5bfff3d8d03fc70d4c30201caf6288d20ae7402414a86b1cde3`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 26 Jun 2024 21:58:20 GMT
ADD file:e6fa59569d6234c463e39f7c2465f2984240a5e8cd613c1ffdc14ab3abb4a7ad in / 
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:72a2b38d7f88bb9b0be6097180e8f8261c31815017cb512a158422c2bfba6973`  
		Last Modified: Tue, 02 Jul 2024 00:43:02 GMT  
		Size: 56.1 MB (56064975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003014d72f23a9e0b16eb59708032ad565fe8e24244a34ae5b65e72f56314d8d`  
		Last Modified: Tue, 02 Jul 2024 01:15:23 GMT  
		Size: 16.3 MB (16267863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8e3ef3e76ff601cae23732babfc202314066da48aedac550440cd3cdf72f2c`  
		Last Modified: Tue, 02 Jul 2024 01:15:41 GMT  
		Size: 55.9 MB (55927528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c8df015cc32aa6b21dc9222a2e2b72a8c4c3819fa83b8c9ed309891e602d8f`  
		Last Modified: Tue, 02 Jul 2024 01:16:22 GMT  
		Size: 199.9 MB (199917917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848c1181f014dcd48645c646b76e422fca43606fc962c617b11a3d96c73dfbd4`  
		Last Modified: Wed, 03 Jul 2024 00:20:57 GMT  
		Size: 6.4 MB (6441115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7475dd595614e1f73c75b2ee16de3ac3ac37a8b08abf279b041969ad1adc3e12`  
		Last Modified: Wed, 03 Jul 2024 00:20:58 GMT  
		Size: 22.4 MB (22371668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdebc907d96de8c9895355b93052492f41f2d8ec198889c318853fcb6ddbbaa`  
		Last Modified: Wed, 03 Jul 2024 00:20:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22b737f9900ee13580299913cd244f4a2ed93e1565c3b0f95cf6876126c25c3`  
		Last Modified: Wed, 03 Jul 2024 00:20:57 GMT  
		Size: 2.8 MB (2796740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:05f97a9b8943027bd2aa331607b567b7253a8fff3bc14430d7314cd55694d88d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15475353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c0cc5f659257b86cb15b18e2ab5acd98e316dfe8d228f3d127ef11dae3886f`

```dockerfile
```

-	Layers:
	-	`sha256:b7e6876ddccc8c75097faa3c258d26214d4e77763ddb34eabe187dd7a729306e`  
		Last Modified: Wed, 03 Jul 2024 00:20:57 GMT  
		Size: 15.5 MB (15451318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b939af0973a10f3baecc2559d256fd4e04c7e85b4cc8d676231fe70d8e0a8b27`  
		Last Modified: Wed, 03 Jul 2024 00:20:57 GMT  
		Size: 24.0 KB (24035 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; ppc64le

```console
$ docker pull python@sha256:e738f1cd9aa98decf84b4d73f83f536a001645e88cf888106d45eda7953fe705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.6 MB (363612801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e19bb5a1f698c0f24c0750393740c9397246ab8b445ae3b96cd5092ef54b5b`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 26 Jun 2024 21:58:20 GMT
ADD file:288859e020cf9178f55732ac2eaa62400e2c2d66b3ca500ac7df69c8025abba9 in / 
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:202e493da11eac96a36d754afa396feec67f46e0492e70c0cc4d61dfb06d6a75`  
		Last Modified: Tue, 02 Jul 2024 01:22:20 GMT  
		Size: 59.0 MB (58950397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661ff02529d6818e558d6049a746391403c023c68ac6d75816221bd99e3244c`  
		Last Modified: Tue, 02 Jul 2024 02:05:47 GMT  
		Size: 16.8 MB (16765868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93f0edb37745f21593aefba0898d81dbc780a39dfe73cf03491e10c88480878`  
		Last Modified: Tue, 02 Jul 2024 02:06:04 GMT  
		Size: 58.9 MB (58872635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ef5fcf94d321c187fa4f90d7b4b53743171e2926b6152cebcc4b0206128a8f`  
		Last Modified: Tue, 02 Jul 2024 02:06:39 GMT  
		Size: 196.4 MB (196369493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf23a8ed97bf7ecff781fd733ed049652e3a9e396555e0317231bb8e516aa4f`  
		Last Modified: Wed, 03 Jul 2024 12:40:28 GMT  
		Size: 6.8 MB (6801777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285a5df8b1928b6b7c7ecf81c497e44432ee70c22b81e1d05f39b9d294b69fad`  
		Last Modified: Wed, 03 Jul 2024 12:40:29 GMT  
		Size: 23.1 MB (23055612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcf359f0b628a1c038a719f1c8108654dbd16c599619f090c1e4b4638fffed8`  
		Last Modified: Wed, 03 Jul 2024 12:40:28 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664956539374032e8ce6df0106f456e8588c29141fdc38360dfeee655f0d5964`  
		Last Modified: Wed, 03 Jul 2024 12:40:28 GMT  
		Size: 2.8 MB (2796787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:d3fb4a4ae1b45a03a82abd1f263ff000c33a139aa89f40dd0e3036b62e958db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15456103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26fb606b49f57917047825f3a6a1968ec199b325de93c270e2e951a816038da`

```dockerfile
```

-	Layers:
	-	`sha256:9d0bd0af235651ebb6d642154ce5239f4ed0b8cab1b201904bbaf4d4b2ae8b06`  
		Last Modified: Wed, 03 Jul 2024 12:40:28 GMT  
		Size: 15.4 MB (15431989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6537ddd7a9ff29029e1d86fda0e2df7d89dbfc300b7dd97cfcdd799e214e391`  
		Last Modified: Wed, 03 Jul 2024 12:40:28 GMT  
		Size: 24.1 KB (24114 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; s390x

```console
$ docker pull python@sha256:58d3c0a8470c4f865f0fca826861ce3c65315af228b762920045cec542e2d6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.0 MB (328012854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2a175120e7d357e2b03ecb25ab34024cc5c970469aabb168ab15cf704a906e`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 26 Jun 2024 21:58:20 GMT
ADD file:5752d26037cbb262eeafd1819ecd77ecf8a8cd0019683c05fb92c50c6a458861 in / 
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:aa9549a3d8effd17bc1f93fd40d83261d2505d37791c5aa837c9f7c0fff5c9e3`  
		Last Modified: Tue, 02 Jul 2024 00:48:47 GMT  
		Size: 53.3 MB (53319825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7860b53e214213e98b388ade5c0d289331e291bb4e43197e4a14a4e8a111583e`  
		Last Modified: Tue, 02 Jul 2024 03:45:25 GMT  
		Size: 15.6 MB (15641817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b8db73130bc88255a98f66627e7258a074a0223eef8b550e6c1084068d24d0`  
		Last Modified: Tue, 02 Jul 2024 03:45:38 GMT  
		Size: 54.1 MB (54075315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afac5d5564136a413fbebb4f4ab7b85f2fa277f71f996d27bc1d7e24b307c5d4`  
		Last Modified: Tue, 02 Jul 2024 03:46:03 GMT  
		Size: 173.0 MB (173024898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0ddab36b63cc03e67fbce409ba02357b99a5a93b0f5591a8b1a2452a3f42ff`  
		Last Modified: Tue, 02 Jul 2024 19:13:10 GMT  
		Size: 6.0 MB (6001030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffd7eecfa14e4b681d4ac7da916330b711e13af9c8b151c479d00bc09948d30`  
		Last Modified: Tue, 02 Jul 2024 19:13:11 GMT  
		Size: 23.2 MB (23152917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da9334ee2c0645fed446445b29a1347ff1fddceba70aeb0e01b3941a9961f75`  
		Last Modified: Wed, 03 Jul 2024 04:55:02 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8933a21d99f61db9fa65c91bba0953ad335b472817501381130554862665d88`  
		Last Modified: Wed, 03 Jul 2024 04:55:02 GMT  
		Size: 2.8 MB (2796821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:5a431ced8675c69122888a2df21dd7cdf035e4a9b30bb2229f8ea99b2c54a8ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15308266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff53d84c72f9a600aab2088ac28fc44f689900434708e9c132b9408cfd04307`

```dockerfile
```

-	Layers:
	-	`sha256:20640f9e23fc6fc4d76b2e8fa7c3716c02242ab22cb9f9d655f768dc376d8306`  
		Last Modified: Wed, 03 Jul 2024 04:55:02 GMT  
		Size: 15.3 MB (15284196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:191bc0b6ac2e806a3a0725868774837031a0a42accb684eb57f1b433f2a320b6`  
		Last Modified: Wed, 03 Jul 2024 04:55:02 GMT  
		Size: 24.1 KB (24070 bytes)  
		MIME: application/vnd.in-toto+json
