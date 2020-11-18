## `python:rc`

```console
$ docker pull python@sha256:38df3a97f6e6660204e4be77d0a70a14eecf0d5a1f3da56fd1571f463071ce32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.14393.4046; amd64
	-	windows version 10.0.17763.1577; amd64

### `python:rc` - linux; amd64

```console
$ docker pull python@sha256:61b228842cd4e72013b380264043a91bbe299d7b145b4cf3aa1e74bde5e319dd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.0 MB (339988557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce51c22136fcb3048eacaafd7296786cded1678df30becedd6f8be97cd0a9ee`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 13 Oct 2020 01:38:30 GMT
ADD file:6627ad39ea0cb9fcb212342326d14efaff51aece1fd0dc16d5bbcaa25d858622 in / 
# Tue, 13 Oct 2020 01:38:30 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:14:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:14:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:15:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:16:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 19:41:46 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Oct 2020 19:41:46 GMT
ENV LANG=C.UTF-8
# Tue, 13 Oct 2020 19:41:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 19:41:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Nov 2020 01:20:54 GMT
ENV PYTHON_VERSION=3.10.0a2
# Wed, 04 Nov 2020 01:28:58 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& python3 --version
# Wed, 04 Nov 2020 01:28:59 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 04 Nov 2020 01:28:59 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Wed, 04 Nov 2020 01:28:59 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/fa7dc83944936bf09a0e4cb5d5ec852c0d256599/get-pip.py
# Wed, 04 Nov 2020 01:29:00 GMT
ENV PYTHON_GET_PIP_SHA256=6e0bb0a2c2533361d7f297ed547237caf1b7507f197835974c0dd7eba998c53c
# Wed, 04 Nov 2020 01:29:05 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 04 Nov 2020 01:29:06 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:e4c3d3e4f7b024979a1c12daa4073f6353b2ba92d96418bc90451994927c9bff`  
		Last Modified: Tue, 13 Oct 2020 01:48:02 GMT  
		Size: 50.4 MB (50395978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101c41d0463bc77661fb3343235b16d536a92d2efb687046164d413e51bd4fc4`  
		Last Modified: Tue, 13 Oct 2020 02:28:35 GMT  
		Size: 7.8 MB (7811737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8275efcd805f9905d7def23603618236284b0be6b9e47455c638fbfb03fa9208`  
		Last Modified: Tue, 13 Oct 2020 02:28:35 GMT  
		Size: 10.0 MB (9996326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751620502a7a2905067c2f32d4982fb9b310b9808670ce82c0e2b40f5307a3ee`  
		Last Modified: Tue, 13 Oct 2020 02:28:53 GMT  
		Size: 51.8 MB (51829492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5e725150a20c71bdc806daa04c9c9438aed5f5a4dd376f3be66fae213b1d43`  
		Last Modified: Tue, 13 Oct 2020 02:29:32 GMT  
		Size: 192.3 MB (192263478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397dba5694dbe6da34f1abfc75362ca3f23a0421505dd3502885e9bc9a167f42`  
		Last Modified: Tue, 13 Oct 2020 22:01:36 GMT  
		Size: 6.1 MB (6145350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fda60e85f24a5354c0711a60956a2bd72681654c22b1d71054b11ce1c664739`  
		Last Modified: Wed, 04 Nov 2020 01:49:27 GMT  
		Size: 19.4 MB (19425128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55f376a74c2c22a2b4e46329974549e4b74e275eb7e1685e38e72dda317d9a5`  
		Last Modified: Wed, 04 Nov 2020 01:49:22 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72eaa0556565c2183a15ef5b3c6e586c1654e485f65405b2f777e267f5dda3f4`  
		Last Modified: Wed, 04 Nov 2020 01:49:22 GMT  
		Size: 2.1 MB (2120834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:rc` - linux; arm variant v5

```console
$ docker pull python@sha256:cc09c2730f88b74488e0c2b1e6367d047aadba0561f1bc93e148247b3f51efa6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.4 MB (312420820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1915460d9b8ae5fbd28d8933a7d8869d8befefefdbc34776ebfff2f407133f28`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:11 GMT
ADD file:bb3447356f67bcc742643d914d0254a63f6ae355a30f0ac2471abe10df2ef70d in / 
# Tue, 17 Nov 2020 20:20:12 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:41:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:42:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Nov 2020 21:43:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:46:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:22:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Nov 2020 22:22:32 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 22:22:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:23:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 17 Nov 2020 22:23:02 GMT
ENV PYTHON_VERSION=3.10.0a2
# Tue, 17 Nov 2020 22:34:44 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& python3 --version
# Tue, 17 Nov 2020 22:34:47 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 17 Nov 2020 22:34:48 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Tue, 17 Nov 2020 22:34:49 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/fa7dc83944936bf09a0e4cb5d5ec852c0d256599/get-pip.py
# Tue, 17 Nov 2020 22:34:50 GMT
ENV PYTHON_GET_PIP_SHA256=6e0bb0a2c2533361d7f297ed547237caf1b7507f197835974c0dd7eba998c53c
# Tue, 17 Nov 2020 22:35:03 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 17 Nov 2020 22:35:03 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:5ab3aa180a853babda6a9051719fe6ec0d84c2b928c417dcb59a1728ad58b664`  
		Last Modified: Tue, 17 Nov 2020 20:30:07 GMT  
		Size: 48.1 MB (48111175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521d5b6df6edc5ecad2cf2b768fbd613543aa0e4cf088cf833831721dfbe9ed3`  
		Last Modified: Tue, 17 Nov 2020 22:08:19 GMT  
		Size: 7.4 MB (7361320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2374b91c31c8256125e91fff26b9eb051ec11e6d4bcd609fb19d7416c500c0`  
		Last Modified: Tue, 17 Nov 2020 22:08:20 GMT  
		Size: 9.7 MB (9687117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4b93b1a93df4915c39e81ab18cea9e915b703dac510437aaa30c87712011ce`  
		Last Modified: Tue, 17 Nov 2020 22:08:49 GMT  
		Size: 49.6 MB (49572331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5b2c6f6356612a563f026d6b0f44d0400943c9355ffbcc9611d33323e19e10`  
		Last Modified: Tue, 17 Nov 2020 22:09:48 GMT  
		Size: 171.2 MB (171239057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1511931f7cff4461e4da6c1c7c09217ccfe7fffa5fa78a1d074663abbc1d5ae8`  
		Last Modified: Wed, 18 Nov 2020 01:13:50 GMT  
		Size: 5.8 MB (5840411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31731c6f9c99e8a8c4c7c11c930b58466720dd21a19f63ccadb36a2f856c8988`  
		Last Modified: Wed, 18 Nov 2020 01:13:54 GMT  
		Size: 18.5 MB (18488021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e1dea329ed42d151e4923905662a54941788e9d1fe5d2717a0aecbdaed1b40`  
		Last Modified: Wed, 18 Nov 2020 01:13:48 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca2721b0003e47d5878ac964b9e015874eb1ac471d4ebc4e373f3e42f134b9a`  
		Last Modified: Wed, 18 Nov 2020 01:13:49 GMT  
		Size: 2.1 MB (2121155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:rc` - linux; arm variant v7

```console
$ docker pull python@sha256:dd342fc556619cf1fd417a6574b2d573d94c21274c3464ba84be44b6676ab598
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (304047607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b52aff332cc33d6e6b2032cfb5affd9f83aaa3f9a3e9b5bf335a39aea81809`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:30 GMT
ADD file:81141d8fa450e1e5af67bb3757057f3fc34d3ed35cfd0caedb0aab64c5da9aaf in / 
# Tue, 17 Nov 2020 20:20:33 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:41:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:41:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Nov 2020 21:42:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:45:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 03:57:03 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Nov 2020 03:57:07 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 03:57:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 03:57:27 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 18 Nov 2020 03:57:27 GMT
ENV PYTHON_VERSION=3.10.0a2
# Wed, 18 Nov 2020 04:09:41 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& python3 --version
# Wed, 18 Nov 2020 04:09:45 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 18 Nov 2020 04:09:46 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Wed, 18 Nov 2020 04:09:47 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/fa7dc83944936bf09a0e4cb5d5ec852c0d256599/get-pip.py
# Wed, 18 Nov 2020 04:09:49 GMT
ENV PYTHON_GET_PIP_SHA256=6e0bb0a2c2533361d7f297ed547237caf1b7507f197835974c0dd7eba998c53c
# Wed, 18 Nov 2020 04:10:03 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 18 Nov 2020 04:10:06 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:ebde10b2510128140d24e66909ceb0c80e00656af313829f82d31ae8cf08bcf8`  
		Last Modified: Tue, 17 Nov 2020 20:31:13 GMT  
		Size: 45.9 MB (45868212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05478d2a9ec4daaef33a6c87d057451c262677d02e4d9c61125bbb68bc56a601`  
		Last Modified: Tue, 17 Nov 2020 22:07:16 GMT  
		Size: 7.1 MB (7098267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c5f002cc82f5d62a78100714f451edb33a717fbf6795e309e0b1768712c093`  
		Last Modified: Tue, 17 Nov 2020 22:07:17 GMT  
		Size: 9.3 MB (9343289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d327c3810299006837433575844fea13af679784a13df32d477f1207e94ea8c`  
		Last Modified: Tue, 17 Nov 2020 22:07:42 GMT  
		Size: 47.4 MB (47356208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb9b79ac75491ca0d6be5abb23a07ad8026b4aae731e13376684bff9969e8a8`  
		Last Modified: Tue, 17 Nov 2020 22:08:38 GMT  
		Size: 168.5 MB (168486176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13634106be2c0d30c1d01e60f95d9c748701f3e0b903bf23dbeae2eb7b7880f6`  
		Last Modified: Wed, 18 Nov 2020 07:02:54 GMT  
		Size: 5.5 MB (5536455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47763b94ba93caa2e46952e7b53a734f1df2ba3e0e1cedb2123c8365cb7334c4`  
		Last Modified: Wed, 18 Nov 2020 07:02:58 GMT  
		Size: 18.2 MB (18237628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f478dc9a041c71d78f157bf67cc3ab6dae1c9caed81c673764c071858910ea73`  
		Last Modified: Wed, 18 Nov 2020 07:02:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e266c1171f2ac29e38f17eac95aa3c32dc78e31fb79d48ecf039b62095d73c`  
		Last Modified: Wed, 18 Nov 2020 07:02:53 GMT  
		Size: 2.1 MB (2121140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:rc` - linux; arm64 variant v8

```console
$ docker pull python@sha256:39915a836b11e57fa5cbbf5f7e94f2977419e2cd77a80669d84987f9f1c41205
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.1 MB (330085713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45483e0d306242c0ee3d606ea445a73c074ff83e3c5caaa90d8860e220ad0f0`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 13 Oct 2020 01:40:40 GMT
ADD file:7a9016f6c75910c392bbea2cb9e146d1eba3942cdfd666a44004c79951c5d46f in / 
# Tue, 13 Oct 2020 01:40:45 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:32:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:33:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:33:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:35:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 05:43:32 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Oct 2020 05:43:33 GMT
ENV LANG=C.UTF-8
# Tue, 13 Oct 2020 05:43:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 05:43:48 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Nov 2020 02:03:46 GMT
ENV PYTHON_VERSION=3.10.0a2
# Wed, 04 Nov 2020 02:13:03 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& python3 --version
# Wed, 04 Nov 2020 02:13:08 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 04 Nov 2020 02:13:10 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Wed, 04 Nov 2020 02:13:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/fa7dc83944936bf09a0e4cb5d5ec852c0d256599/get-pip.py
# Wed, 04 Nov 2020 02:13:12 GMT
ENV PYTHON_GET_PIP_SHA256=6e0bb0a2c2533361d7f297ed547237caf1b7507f197835974c0dd7eba998c53c
# Wed, 04 Nov 2020 02:13:23 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 04 Nov 2020 02:13:24 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:04aacb10cb67f5fa248646a0ac9f40af5a6d3b0dbef65505bb7766bed6bf4885`  
		Last Modified: Tue, 13 Oct 2020 01:47:53 GMT  
		Size: 49.2 MB (49175405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136d6e4f4b17bdbefbe60820da5f5711a26d31c075dc69bcaf9b077d7d29262d`  
		Last Modified: Tue, 13 Oct 2020 02:47:32 GMT  
		Size: 7.7 MB (7681432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28db65b8364fc73072a0d5b51199cc9c6b108b4229d92e784b92ae67898dd0bd`  
		Last Modified: Tue, 13 Oct 2020 02:47:32 GMT  
		Size: 10.0 MB (9983936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff74fb95e95674d2f0c26f446a2cb7c0ee055d78182a9d61e1578c64c171f2b4`  
		Last Modified: Tue, 13 Oct 2020 02:48:00 GMT  
		Size: 52.2 MB (52163324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0afbf256edbdd3581a644041583033e21d35818e6f262f8f91f419bb29a253`  
		Last Modified: Tue, 13 Oct 2020 02:48:59 GMT  
		Size: 183.8 MB (183802302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae6747d28132b8303a22b1333299dc11bb746895bc8c6a0855c1a2da152d411`  
		Last Modified: Tue, 13 Oct 2020 08:15:12 GMT  
		Size: 6.3 MB (6259641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562dc5a55fb3cfaf323f459832d2d3e5c917157f18f843ee7791a9b1b3209a23`  
		Last Modified: Wed, 04 Nov 2020 02:35:08 GMT  
		Size: 18.9 MB (18898417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1beb9fcee9cdc30b09d646ba43b4c33b614ab2512658c53ca783ef38308a1083`  
		Last Modified: Wed, 04 Nov 2020 02:35:02 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce3d6aec6d90088d0fe798478845b0a0ccc051a702d7c6b9d8c7be82bb7c5b7`  
		Last Modified: Wed, 04 Nov 2020 02:35:03 GMT  
		Size: 2.1 MB (2121022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:rc` - linux; 386

```console
$ docker pull python@sha256:640389e2743a38724c118ed9af4e1d98bbf24e59143b5022961915fcec1894f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.1 MB (349050090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0535f1ce3431002047722331393d1cbf2a70722fb402a13106203d478ce899a0`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 13 Oct 2020 01:40:35 GMT
ADD file:67b2b1e6cbc655edc4f78c724cd2048f8b0b336c3b56cca448b65ee9bb594ede in / 
# Tue, 13 Oct 2020 01:40:36 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:19:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:19:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:20:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:21:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 17:02:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Oct 2020 17:02:53 GMT
ENV LANG=C.UTF-8
# Tue, 13 Oct 2020 17:03:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 17:03:03 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Nov 2020 01:45:26 GMT
ENV PYTHON_VERSION=3.10.0a2
# Wed, 04 Nov 2020 01:57:30 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& python3 --version
# Wed, 04 Nov 2020 01:57:31 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 04 Nov 2020 01:57:31 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Wed, 04 Nov 2020 01:57:31 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/fa7dc83944936bf09a0e4cb5d5ec852c0d256599/get-pip.py
# Wed, 04 Nov 2020 01:57:32 GMT
ENV PYTHON_GET_PIP_SHA256=6e0bb0a2c2533361d7f297ed547237caf1b7507f197835974c0dd7eba998c53c
# Wed, 04 Nov 2020 01:57:38 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 04 Nov 2020 01:57:39 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:c303ed7c76e74ddfd5fc798c4922c89902a340db03b34bdaeb1974366f3c46a1`  
		Last Modified: Tue, 13 Oct 2020 01:48:38 GMT  
		Size: 51.2 MB (51158779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63785be044bb8d2e10e90138f54d46ca10cdf3c488a506f016e20e3616b3ed47`  
		Last Modified: Tue, 13 Oct 2020 02:38:23 GMT  
		Size: 8.0 MB (7981175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7a218c61768debfbd306af73aba7ce33e177373f9074a3655c5289d599706b`  
		Last Modified: Tue, 13 Oct 2020 02:38:23 GMT  
		Size: 10.3 MB (10338487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70642f7883120399f94e6ebeaf462f650791e043356533691f94187b38407d54`  
		Last Modified: Tue, 13 Oct 2020 02:38:49 GMT  
		Size: 53.4 MB (53432730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98b00b6d1a9933686acaae03ae77ab7f0e02e9aa81d8f50fef3419171602dd5`  
		Last Modified: Tue, 13 Oct 2020 02:40:05 GMT  
		Size: 198.8 MB (198825829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ec63ff9fd1fc5d3695d39b4fec77e9bc9acc0f6b9122f240e017da1c96191f`  
		Last Modified: Tue, 13 Oct 2020 20:11:59 GMT  
		Size: 6.5 MB (6489207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275cacbce0d5c62ad165a9ff139615dbd2a7a20100dbd39b0f824bbf1c047092`  
		Last Modified: Wed, 04 Nov 2020 02:20:44 GMT  
		Size: 18.7 MB (18702905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b5aeb7a2ea444496ee59bc71ea7efaa8a467f0205883a92a33e833da676c91`  
		Last Modified: Wed, 04 Nov 2020 02:20:38 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45303b29a9b05ea1a900e32371dc9756b93e3716a65cfb20acc14b7ee15e8d8`  
		Last Modified: Wed, 04 Nov 2020 02:20:38 GMT  
		Size: 2.1 MB (2120745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:rc` - linux; mips64le

```console
$ docker pull python@sha256:4483b9384f10570a5afade89a14faec649d0f01af4123bf6496d93a41d41ca7e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.6 MB (324562693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b8158950ac2802c25ea65629c1c22342e7be56b6ab1b56e9bbc49f52e7357f`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 17 Nov 2020 20:18:57 GMT
ADD file:a535d2f623f959d14749f458ffedfb6a0ec8dc8081509e3d4961929b20654a10 in / 
# Tue, 17 Nov 2020 20:18:58 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 22:39:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:39:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Nov 2020 22:40:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:43:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:40:50 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Nov 2020 00:40:50 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 00:41:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:41:11 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 18 Nov 2020 00:41:11 GMT
ENV PYTHON_VERSION=3.10.0a2
# Wed, 18 Nov 2020 01:21:14 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& python3 --version
# Wed, 18 Nov 2020 01:21:16 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 18 Nov 2020 01:21:16 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Wed, 18 Nov 2020 01:21:17 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/fa7dc83944936bf09a0e4cb5d5ec852c0d256599/get-pip.py
# Wed, 18 Nov 2020 01:21:17 GMT
ENV PYTHON_GET_PIP_SHA256=6e0bb0a2c2533361d7f297ed547237caf1b7507f197835974c0dd7eba998c53c
# Wed, 18 Nov 2020 01:21:38 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 18 Nov 2020 01:21:39 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:dfb90274558af841c9796a5beea46490849a7c976f581a0c8b88abf06db56f1e`  
		Last Modified: Tue, 17 Nov 2020 20:25:47 GMT  
		Size: 49.0 MB (49020349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9818d418c7b576c15024336a4aea56a58529ecd9b3079f0655966933948695`  
		Last Modified: Tue, 17 Nov 2020 22:52:01 GMT  
		Size: 7.2 MB (7231919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788e51b5e72a4c84a4871396b113a204ef677df1acb708cb1632fdb0a1a1c14d`  
		Last Modified: Tue, 17 Nov 2020 22:52:02 GMT  
		Size: 10.0 MB (10015783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa993f09cad1532e4160e328520aeb5341e617ebacc30ba42c7845bfe78f938d`  
		Last Modified: Tue, 17 Nov 2020 22:52:56 GMT  
		Size: 50.8 MB (50842729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2207c46abff3ac9a752e7cf978c9550e007843969d5d69eb6f122ac4204adee2`  
		Last Modified: Tue, 17 Nov 2020 22:55:09 GMT  
		Size: 179.8 MB (179815372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9312bdbc815e166144603ea797ae53230c0681b1461d0c9ee1144d3f322ac8`  
		Last Modified: Wed, 18 Nov 2020 07:09:38 GMT  
		Size: 6.5 MB (6455136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8704e5965ff193eedbd32fff75ba3bdc6af1600babb6cf5dbdd7de4259aa15d`  
		Last Modified: Wed, 18 Nov 2020 07:09:48 GMT  
		Size: 19.1 MB (19060264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce2dc9c61cbf4c926159564a1bd7087bedc9bb4a1219c33da04a49371a84b37`  
		Last Modified: Wed, 18 Nov 2020 07:09:33 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264a93856b6e76adc2810d3d5444fa2548540b0717fd1e7614deaebd142e7cbc`  
		Last Modified: Wed, 18 Nov 2020 07:09:35 GMT  
		Size: 2.1 MB (2120908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:rc` - linux; ppc64le

```console
$ docker pull python@sha256:768440e88d8aabf3690601702291741928a9284efbaf25e140168520d04ec2e6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362632066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29080bd0b6587306cee1d5b4cbe1e3d908e58529f4163fdba0a747201327a58e`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 13 Oct 2020 01:37:39 GMT
ADD file:339c3116c875720e7ba27e67ec6c60bc913e8108f7cccce90537c0915c5130a5 in / 
# Tue, 13 Oct 2020 01:37:48 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 08:58:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 08:58:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 09:01:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 09:09:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 12:43:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Oct 2020 12:44:03 GMT
ENV LANG=C.UTF-8
# Tue, 13 Oct 2020 12:45:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 12:45:10 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Nov 2020 03:20:43 GMT
ENV PYTHON_VERSION=3.10.0a2
# Wed, 04 Nov 2020 03:31:58 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& python3 --version
# Wed, 04 Nov 2020 03:32:15 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 04 Nov 2020 03:32:23 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Wed, 04 Nov 2020 03:32:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/fa7dc83944936bf09a0e4cb5d5ec852c0d256599/get-pip.py
# Wed, 04 Nov 2020 03:32:37 GMT
ENV PYTHON_GET_PIP_SHA256=6e0bb0a2c2533361d7f297ed547237caf1b7507f197835974c0dd7eba998c53c
# Wed, 04 Nov 2020 03:33:08 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 04 Nov 2020 03:33:20 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:b5d2617265f370f18bc3d48beee684b1ba0eb6a2b02f813353f4bbd7084830ff`  
		Last Modified: Tue, 13 Oct 2020 01:49:15 GMT  
		Size: 54.1 MB (54142565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a3ae049e8243812509a783d05c2170162d6fb319e07323793cc134f45c8c1c`  
		Last Modified: Tue, 13 Oct 2020 09:34:09 GMT  
		Size: 8.3 MB (8254882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458ef48afca43b31f71a9dd56c10f499a3833b0904195936caa007028295fb36`  
		Last Modified: Tue, 13 Oct 2020 09:34:12 GMT  
		Size: 10.7 MB (10727221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e90a018c82f576b578427df3b9f10a7edce9b4092e97eeaba3877383220d62`  
		Last Modified: Tue, 13 Oct 2020 09:35:20 GMT  
		Size: 57.5 MB (57455375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e336ecebf001fc4a867089fbedc70b9be5e3cc1d088cf2d2527836ff2df487`  
		Last Modified: Tue, 13 Oct 2020 09:38:09 GMT  
		Size: 203.1 MB (203084484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e89f14c8bf9a2651c5fba79cf864925a52097c4e6bb01870602bb85a851638`  
		Last Modified: Tue, 13 Oct 2020 15:11:13 GMT  
		Size: 6.9 MB (6892270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbeee03621b2f58029e8779e2cd85d4f4ed32368446b21e9fde7c107a89776c`  
		Last Modified: Wed, 04 Nov 2020 04:06:28 GMT  
		Size: 20.0 MB (19953877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d09f151d0c97fd31f43e3ce687c387d28e13352e1637db6ffe1caceb0717cca`  
		Last Modified: Wed, 04 Nov 2020 04:06:23 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22b78ed12ea0be4f50c6da82711797a4362469d93bdeddb548171429fef1763`  
		Last Modified: Wed, 04 Nov 2020 04:06:24 GMT  
		Size: 2.1 MB (2121158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:rc` - linux; s390x

```console
$ docker pull python@sha256:ee79fc9d0291136d52129ddd34fc26336d9b3c077bcbe4b391b9296813b72077
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.7 MB (321724880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94bde4e285c3bf435daae224b4d2ed9c277a51ec74d318e1f85ab96f0d2ec1e`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 17 Nov 2020 20:17:56 GMT
ADD file:dfb1d2f775a9c4493397d0ca05aa6486393c6dad4f0fb5f48ffd209397301bdb in / 
# Tue, 17 Nov 2020 20:18:05 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:32:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:32:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Nov 2020 21:32:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:35:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 02:23:50 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Nov 2020 02:23:51 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 02:24:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 02:24:05 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 18 Nov 2020 02:24:06 GMT
ENV PYTHON_VERSION=3.10.0a2
# Wed, 18 Nov 2020 02:31:29 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& python3 --version
# Wed, 18 Nov 2020 02:31:33 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 18 Nov 2020 02:31:33 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Wed, 18 Nov 2020 02:31:34 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/fa7dc83944936bf09a0e4cb5d5ec852c0d256599/get-pip.py
# Wed, 18 Nov 2020 02:31:35 GMT
ENV PYTHON_GET_PIP_SHA256=6e0bb0a2c2533361d7f297ed547237caf1b7507f197835974c0dd7eba998c53c
# Wed, 18 Nov 2020 02:31:43 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 18 Nov 2020 02:31:44 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:6e95a7d20e6bbf957d2bb5912f19784daba6953d8afac5562453108dd45940e1`  
		Last Modified: Tue, 17 Nov 2020 20:23:18 GMT  
		Size: 49.0 MB (48968246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab56d289be912cd903623a00b35bdc52f4f1b54a6778c1ba4c076e5cfe339aa5`  
		Last Modified: Tue, 17 Nov 2020 21:48:36 GMT  
		Size: 7.4 MB (7385996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29ee109f7efbe0700da6e225717912b22d8e015d8d9a9968e564419b1ba97a3`  
		Last Modified: Tue, 17 Nov 2020 21:48:36 GMT  
		Size: 9.9 MB (9882242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e45adeb409573e310b14d50aaf13f2a71a45e62f9f872239e36eb86f927b54`  
		Last Modified: Tue, 17 Nov 2020 21:50:38 GMT  
		Size: 51.4 MB (51380183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29eec538f7c27dd46ca5cff5bd6e29299adea0933747804e60e0dc381865c13d`  
		Last Modified: Tue, 17 Nov 2020 21:53:15 GMT  
		Size: 176.8 MB (176833166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df669021968714da2a1de33d1edeab6ad4cf34452706be135410fe592a08ef2`  
		Last Modified: Wed, 18 Nov 2020 04:16:06 GMT  
		Size: 6.1 MB (6058779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab2b6faffbf15dde21b35b6be691b907a26e4ab0ea1a90e691d9bde33ff3f1d`  
		Last Modified: Wed, 18 Nov 2020 04:16:09 GMT  
		Size: 19.1 MB (19095031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9259170dd06e49b5c7f98c148bf6c0a1069ae2dd7ebc111759bfc832259a41`  
		Last Modified: Wed, 18 Nov 2020 04:16:05 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4119b9e6d2f8aa18313ae1a0ca3481d7834e091562df2c743c56e40ebc60e367`  
		Last Modified: Wed, 18 Nov 2020 04:16:05 GMT  
		Size: 2.1 MB (2121004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:rc` - windows version 10.0.14393.4046; amd64

```console
$ docker pull python@sha256:f7ce984e2e1d81b8c30f6a7eb7cd4c9c0e24433144fdb94969674ef590081c84
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5845411576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3363b83a08286aae2dd960af9420ee0ab6da74181ed8ec98c000b2f306d89151`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 13:23:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 17:09:28 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 11 Nov 2020 17:09:28 GMT
ENV PYTHON_VERSION=3.10.0a2
# Wed, 11 Nov 2020 17:09:29 GMT
ENV PYTHON_RELEASE=3.10.0
# Wed, 11 Nov 2020 17:11:43 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Wed, 11 Nov 2020 17:11:44 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Wed, 11 Nov 2020 17:11:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/fa7dc83944936bf09a0e4cb5d5ec852c0d256599/get-pip.py
# Wed, 11 Nov 2020 17:11:46 GMT
ENV PYTHON_GET_PIP_SHA256=6e0bb0a2c2533361d7f297ed547237caf1b7507f197835974c0dd7eba998c53c
# Wed, 11 Nov 2020 17:13:26 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 11 Nov 2020 17:13:27 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:126d9a92c0cb7b68c56dec2dd5ba118de9dde3ec6368db734c5135fdf1528a33`  
		Last Modified: Wed, 11 Nov 2020 13:34:53 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32d36bd6ec3b70ad877771d7f97cafedd40418fb1bba46babfeda374e5ada5b`  
		Last Modified: Wed, 11 Nov 2020 17:37:45 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3043aa20fb451b77ae59c9efb9c6dc59b512b9e8845e5d93a13c234475a663a`  
		Last Modified: Wed, 11 Nov 2020 17:37:44 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133d105f80267981732d55d045c9d792b94ffd3d53d7346efbdf4988ac056c89`  
		Last Modified: Wed, 11 Nov 2020 17:37:44 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a4d424d4d03012877812df8eef23dfb1358d5eb5c4518871aba2324348a9e4`  
		Last Modified: Wed, 11 Nov 2020 17:37:54 GMT  
		Size: 59.2 MB (59179983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63263730a00b94d1b927f6972174cbe4ddb12e53b6b100290704a3668ce434c0`  
		Last Modified: Wed, 11 Nov 2020 17:37:42 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5549c36240b2f8ef8546ea53b43384db0eb596b0c29f761062928dd6d97a67`  
		Last Modified: Wed, 11 Nov 2020 17:37:41 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b831984dc3e0b7e1f78e637b7f1612ed3f9e09e8f817acd3622c4d9f2a5ed480`  
		Last Modified: Wed, 11 Nov 2020 17:37:41 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97f546ffdf92e2021889498f7b4a68a68fc4be7bccad16ca50995414cc4077f`  
		Last Modified: Wed, 11 Nov 2020 17:37:45 GMT  
		Size: 15.7 MB (15663683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fd1bb174b66d7c5b7d87735d3f2c173be2ac2eed957211f66c2c4bcc48868d`  
		Last Modified: Wed, 11 Nov 2020 17:37:41 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:rc` - windows version 10.0.17763.1577; amd64

```console
$ docker pull python@sha256:93880e3723e02918723166a80d3b0846ab7d87de294b7837ac6141d02f81d600
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2456745666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc83cbba7ae692ed1db50d93026ea324b92f03ace3c76cbe499c9c922fcc8f1`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 13:26:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 17:13:40 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 11 Nov 2020 17:13:40 GMT
ENV PYTHON_VERSION=3.10.0a2
# Wed, 11 Nov 2020 17:13:41 GMT
ENV PYTHON_RELEASE=3.10.0
# Wed, 11 Nov 2020 17:15:20 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Wed, 11 Nov 2020 17:15:22 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Wed, 11 Nov 2020 17:15:23 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/fa7dc83944936bf09a0e4cb5d5ec852c0d256599/get-pip.py
# Wed, 11 Nov 2020 17:15:23 GMT
ENV PYTHON_GET_PIP_SHA256=6e0bb0a2c2533361d7f297ed547237caf1b7507f197835974c0dd7eba998c53c
# Wed, 11 Nov 2020 17:16:08 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 11 Nov 2020 17:16:09 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da5a67a9f3a363cb69c8104913a5a58c1c47e8f648a07d057fc28a5f98790e60`  
		Last Modified: Wed, 11 Nov 2020 13:37:50 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba27fafdef0dd2d90225160fe1fa0393acbcfbe112b6442bf74fa7f41916bcfb`  
		Last Modified: Wed, 11 Nov 2020 17:38:15 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d151bd581671d37a546f79c9c5afda96cd407e11d445b3e1b7a4cbcc25146c`  
		Last Modified: Wed, 11 Nov 2020 17:38:14 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18844c027dd533aa266555588e3065a0ac21230d148ad96e069d44e59d75b77a`  
		Last Modified: Wed, 11 Nov 2020 17:38:14 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e474d026f79d1340dd26f1d903adcbb315af64d8c8571289e5c49884ca916ee1`  
		Last Modified: Wed, 11 Nov 2020 17:38:22 GMT  
		Size: 58.4 MB (58383816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8d587dd9eb7d7bbf1c3e81648491968b453e16745de4bcc1e3a8b366298149`  
		Last Modified: Wed, 11 Nov 2020 17:38:11 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751897ce7a79b868435119e47d6d0c52efdd51502a1bf4c25932eb6505ce9061`  
		Last Modified: Wed, 11 Nov 2020 17:38:10 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e544ea8bbad3119f56d154e3032bba5ad928e5aeb12521fdd788b0d9c0fa1a8c`  
		Last Modified: Wed, 11 Nov 2020 17:38:11 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe074aca215c9edf63df08406b54ca86c74df80404dfb1f0343c0dd736f08825`  
		Last Modified: Wed, 11 Nov 2020 17:38:14 GMT  
		Size: 10.3 MB (10323433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe57335c99740ebc6fb18b58d4bc5f6a7831738aab324acbdb3ce701adaac87`  
		Last Modified: Wed, 11 Nov 2020 17:38:11 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
