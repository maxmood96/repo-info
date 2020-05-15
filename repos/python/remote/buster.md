## `python:buster`

```console
$ docker pull python@sha256:6e40dd37dc3b45648ed8cb2a80ae0636385e2cf5ce883b65d01e886558286756
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

### `python:buster` - linux; amd64

```console
$ docker pull python@sha256:87c9159bf6c3168f5ce7070c978201220fc61a77d603496cf3daa3c19a36f4fe
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.0 MB (349964626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8bf31794b92e39814690136062acfff1be1de7164a6d0ec3e4dada8c92b309e`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 13 May 2020 21:20:19 GMT
ADD file:a50affde4f5ccdfd6450a642199121ffc180bb8cace944a55fab7a78ea851199 in / 
# Wed, 13 May 2020 21:20:19 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:27:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:27:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:28:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:29:44 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 03:45:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2020 03:45:31 GMT
ENV LANG=C.UTF-8
# Thu, 14 May 2020 22:21:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 22:21:29 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 14 May 2020 22:33:06 GMT
ENV PYTHON_VERSION=3.8.3
# Thu, 14 May 2020 22:44:07 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 14 May 2020 22:44:08 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 14 May 2020 22:44:08 GMT
ENV PYTHON_PIP_VERSION=20.1
# Thu, 14 May 2020 22:44:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Thu, 14 May 2020 22:44:08 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Thu, 14 May 2020 22:44:17 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 14 May 2020 22:44:18 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:be2ea06d55bb33c31098151d199a24029c4e0dd6bc5b3da9f617bb04e37d79d9`  
		Last Modified: Wed, 13 May 2020 21:26:07 GMT  
		Size: 50.4 MB (50387525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b353a80f0a7f8fad0ab9c83c30a335d821e084c20b62cf5ea881c00f5ee6aff6`  
		Last Modified: Wed, 13 May 2020 22:45:09 GMT  
		Size: 7.8 MB (7812385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f42905b195f8e4cad9788956a131dedb26c1be58f7e369ae2501e029fa863cb`  
		Last Modified: Wed, 13 May 2020 22:45:09 GMT  
		Size: 10.0 MB (9996250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c983e7b0e4d15e55eca9b2619b632703323413da9e3a2f4115776ddd2a5eb18a`  
		Last Modified: Wed, 13 May 2020 22:45:30 GMT  
		Size: 51.8 MB (51827301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393dca3cd7d4378d10f8f71dbff31fd73e185f2c66c8ec98136d4c12482901f4`  
		Last Modified: Wed, 13 May 2020 22:46:19 GMT  
		Size: 192.2 MB (192211292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb525d4b0a6e6b013aa266ded0239e565f17b07f5547944e1eb584649560eb18`  
		Last Modified: Fri, 15 May 2020 00:57:22 GMT  
		Size: 6.1 MB (6145236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9503d3b9be534ca449d8877ee522d126b2229280808e89c3ba7ea933ec7a10`  
		Last Modified: Fri, 15 May 2020 00:57:39 GMT  
		Size: 29.7 MB (29653245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90018d2cca6e1d34cfb946fcaf84e66f42d062d297ba8d4de132debe65b36c7`  
		Last Modified: Fri, 15 May 2020 00:57:33 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c85bb9fbeb47b2a7b1bd9c53845fc4ec0ff3752cb48241904ad8ac1e0b511a`  
		Last Modified: Fri, 15 May 2020 00:57:33 GMT  
		Size: 1.9 MB (1931159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:buster` - linux; arm variant v5

```console
$ docker pull python@sha256:487c2baa49620f2506ade20aacce8995c52fed81edd17ab59ce16368a37e7ae9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.8 MB (320829637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bb59e93cbd990a3a88d9ccc685e951b8d48d558dda5076683c61f5b641ccb0`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 13 May 2020 21:49:42 GMT
ADD file:0d750ede80457d700cc7920bf7758097730f05dd745594645d18f752b03ee4ac in / 
# Wed, 13 May 2020 21:49:44 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:31:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:32:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:32:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:36:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 00:57:46 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2020 00:57:47 GMT
ENV LANG=C.UTF-8
# Thu, 14 May 2020 00:58:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 00:58:23 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 14 May 2020 19:51:30 GMT
ENV PYTHON_VERSION=3.8.3
# Thu, 14 May 2020 20:03:29 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 14 May 2020 20:03:36 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 14 May 2020 20:03:42 GMT
ENV PYTHON_PIP_VERSION=20.1
# Thu, 14 May 2020 20:03:44 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Thu, 14 May 2020 20:03:45 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Thu, 14 May 2020 20:04:06 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 14 May 2020 20:04:09 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:daa20d7c2fc68b19ac519617f67e18594a86dae573165b8260331168fd68440d`  
		Last Modified: Wed, 13 May 2020 21:59:00 GMT  
		Size: 48.1 MB (48105223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1ed27e51f518bb7f9d3d8f217e841fa0e04cec84e4be751525518dcc9a05bf`  
		Last Modified: Wed, 13 May 2020 22:55:11 GMT  
		Size: 7.4 MB (7359297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb6799de4bbd5a170a48ae198dc7bf17edd128910c4afe2e792507f17519938`  
		Last Modified: Wed, 13 May 2020 22:55:12 GMT  
		Size: 9.7 MB (9687057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a20c21d3f5a3259a90a0f246387bf2d405adcdbc3d6d94b2d18c8a7cbaa1a21`  
		Last Modified: Wed, 13 May 2020 22:55:40 GMT  
		Size: 49.6 MB (49573343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ef486adcb1a643113e21719dfd2c7c18ad2be283553d146726cb7948530080`  
		Last Modified: Wed, 13 May 2020 22:56:41 GMT  
		Size: 171.2 MB (171166703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638fc2b9fc194c8c22ed2835990f340ffb8c402ef38456bf41602361ebfc5da9`  
		Last Modified: Thu, 14 May 2020 03:47:49 GMT  
		Size: 5.8 MB (5840096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa4a9b8c046b8d33a6e26365ae2a88b7b482d00917902874c1ef00914656d9a`  
		Last Modified: Thu, 14 May 2020 20:25:30 GMT  
		Size: 27.2 MB (27166318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a96e71ad82c45240f7f72c8cc83eaa619440b1714f8d61f96a547c5cecc0207`  
		Last Modified: Thu, 14 May 2020 20:25:20 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61acdb3054092e496bcd619fd528c2f710ebcda92334e73403fa43a9f38defb2`  
		Last Modified: Thu, 14 May 2020 20:25:21 GMT  
		Size: 1.9 MB (1931367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:buster` - linux; arm variant v7

```console
$ docker pull python@sha256:df893af652c0d2879b4d4b678a7a994fc719daf18febdcc929c0a3e5aea815af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.4 MB (312351151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4815ce5c2259a9b96f13b8b2792edb58eebfa9c490cbdf8af3e74edb1c67af92`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 13 May 2020 21:13:33 GMT
ADD file:8a00a4e8b308e132c6e665ca4e517d4f8b3ba171a2f539903029bc01271087d7 in / 
# Wed, 13 May 2020 21:13:36 GMT
CMD ["bash"]
# Wed, 13 May 2020 23:56:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:56:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 23:57:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:59:33 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 00:52:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2020 00:52:35 GMT
ENV LANG=C.UTF-8
# Thu, 14 May 2020 00:52:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 00:52:55 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 14 May 2020 21:23:59 GMT
ENV PYTHON_VERSION=3.8.3
# Thu, 14 May 2020 21:36:11 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 14 May 2020 21:36:13 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 14 May 2020 21:36:14 GMT
ENV PYTHON_PIP_VERSION=20.1
# Thu, 14 May 2020 21:36:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Thu, 14 May 2020 21:36:15 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Thu, 14 May 2020 21:36:28 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 14 May 2020 21:36:28 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:152c1d0ea8a0c219e7a54e8b39fa0bc45d7a9e072c2388cb928448e26aed5418`  
		Last Modified: Wed, 13 May 2020 21:23:12 GMT  
		Size: 45.9 MB (45871321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bff79e1c1f74ad9a60f91709c157c26840bb33b1c4e92d724bad04374160f1`  
		Last Modified: Thu, 14 May 2020 00:20:12 GMT  
		Size: 7.1 MB (7096779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a316208b08652f2aea0cc849622bf6cb91a53f9b10a9d0892580ae96ebb9e90`  
		Last Modified: Thu, 14 May 2020 00:20:13 GMT  
		Size: 9.3 MB (9343194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab435daaee3f8db4fd8c2b79f87c3ae0f33afb42c951ab15d24d8946cf31ec`  
		Last Modified: Thu, 14 May 2020 00:20:36 GMT  
		Size: 47.4 MB (47355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15a0da8a934107507930d13a6a6f22a664fdb89d80cee88a99dec9a59f63504`  
		Last Modified: Thu, 14 May 2020 00:21:30 GMT  
		Size: 168.4 MB (168419252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6d524414ffe442558f35ad613b0841d57821ed29a6f69403c90236d1fd986f`  
		Last Modified: Thu, 14 May 2020 03:56:13 GMT  
		Size: 5.5 MB (5535959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a466cf3211efb867fb11b85f57c50c7374afb9cbd8b5edc8d801ebe100487f35`  
		Last Modified: Thu, 14 May 2020 22:07:57 GMT  
		Size: 26.8 MB (26797655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db40fcfa939080c927c1cd9e0017b20b8bbb590bb35393045b26e04339745d0d`  
		Last Modified: Thu, 14 May 2020 22:07:49 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918745699419db0893a48bd38a4beda64fc2c9b02394f836d32acac2c269dd76`  
		Last Modified: Thu, 14 May 2020 22:07:51 GMT  
		Size: 1.9 MB (1931360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:buster` - linux; arm64 variant v8

```console
$ docker pull python@sha256:66869166c6a0dc8131e4ebf1c50d01dd4e012aa49eb63829ea096789d18c12e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339593525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72662c109229c88fc7883bc505e2751c123fdbdba5fef5f522b96f80ece19f1`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 13 May 2020 21:43:08 GMT
ADD file:685903e2621502d2f743969aaf293a5feab58680a95cd93a5ebf2b07f3b5d358 in / 
# Wed, 13 May 2020 21:43:10 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:24:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:24:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:24:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:27:21 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 20:29:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2020 20:29:36 GMT
ENV LANG=C.UTF-8
# Thu, 14 May 2020 20:30:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 20:30:03 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 14 May 2020 20:41:10 GMT
ENV PYTHON_VERSION=3.8.3
# Thu, 14 May 2020 20:50:07 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 14 May 2020 20:50:13 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 14 May 2020 20:50:14 GMT
ENV PYTHON_PIP_VERSION=20.1
# Thu, 14 May 2020 20:50:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Thu, 14 May 2020 20:50:16 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Thu, 14 May 2020 20:50:30 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 14 May 2020 20:50:31 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:0be831822ade5f87765ba6ff26243b12a3ecd4c379df96483549a7992c1fd35b`  
		Last Modified: Wed, 13 May 2020 21:52:50 GMT  
		Size: 49.2 MB (49168115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2879905fcfbdfe9945e6eb39396c6b52b929faf145449ab656f7b35bb6387a`  
		Last Modified: Wed, 13 May 2020 22:39:40 GMT  
		Size: 7.7 MB (7681618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2769f7d2af01c05219ba1529b243249dcedccd56fabeee3d41d792b819f494`  
		Last Modified: Wed, 13 May 2020 22:39:39 GMT  
		Size: 10.0 MB (9983943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e8c22f4290c6000d75544c42d271474d93302f7cd74ef79832ba3c93c962a`  
		Last Modified: Wed, 13 May 2020 22:40:02 GMT  
		Size: 52.2 MB (52155958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9b85452f917a631debce0633df2f9e9a5ee7f79a4d2553949182ffd209a6f5`  
		Last Modified: Wed, 13 May 2020 22:40:54 GMT  
		Size: 183.7 MB (183741566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3ec242a525b26acd13ada6ee2de1be6a48222caaf10992e98ea182de4f2094`  
		Last Modified: Thu, 14 May 2020 23:31:43 GMT  
		Size: 6.3 MB (6259391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43fe65a73401fd13101622ac621dbc32cf882dc0617569e3124e10cb1635ec8f`  
		Last Modified: Thu, 14 May 2020 23:32:11 GMT  
		Size: 28.7 MB (28671343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0834cec50abbf4ab7a9b8e6eb183676576b50d24cca387798e15a7ada2561ee`  
		Last Modified: Thu, 14 May 2020 23:31:59 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b973b292abb5025e136f02ed5cf5349f31110e85e4af126676cd6ee4530ae57`  
		Last Modified: Thu, 14 May 2020 23:32:00 GMT  
		Size: 1.9 MB (1931357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:buster` - linux; 386

```console
$ docker pull python@sha256:db8b273eba9b5d1736a58a841690aedc79a31225ee753fb2c8a82c4192a1b862
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.7 MB (357745252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ab8cb02afa2116dc93e7afe4f6e88ee8537ffbed884ebcf3dbc6c82caeb841c`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 13 May 2020 21:39:08 GMT
ADD file:6aac8e08fe944df3eddb4f6d5754281e407717bf6c2ec1ed9b6ab6af21dd6ee8 in / 
# Wed, 13 May 2020 21:39:09 GMT
CMD ["bash"]
# Wed, 13 May 2020 23:41:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:41:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 23:42:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:43:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 21:44:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2020 21:44:57 GMT
ENV LANG=C.UTF-8
# Thu, 14 May 2020 21:45:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 21:45:11 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 14 May 2020 22:04:07 GMT
ENV PYTHON_VERSION=3.8.3
# Thu, 14 May 2020 22:19:35 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 14 May 2020 22:19:36 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 14 May 2020 22:19:36 GMT
ENV PYTHON_PIP_VERSION=20.1
# Thu, 14 May 2020 22:19:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Thu, 14 May 2020 22:19:37 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Thu, 14 May 2020 22:19:45 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 14 May 2020 22:19:46 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:adf8f9afd28c61bb1494b99fd6560afa547f46892f87c9847b019ac6d551809e`  
		Last Modified: Wed, 13 May 2020 21:46:14 GMT  
		Size: 51.2 MB (51153891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da0d50611a9ebbc8b9bf756eedd764a8de229bfc658664649463c92bfc78831`  
		Last Modified: Thu, 14 May 2020 00:01:55 GMT  
		Size: 8.0 MB (7981818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32f66937263dbe4d20950081f58d45120003be827ee862cad76fc2f62a25e9e`  
		Last Modified: Thu, 14 May 2020 00:01:56 GMT  
		Size: 10.3 MB (10338527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4a10f86926521fbad92e4a027acc69061b22316507703b81ea029bea5e1557`  
		Last Modified: Thu, 14 May 2020 00:02:19 GMT  
		Size: 53.4 MB (53428843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46a0f3146e68fda6cd33a9c41f18fbe7066058d8583dbd7434a69c7026de50c`  
		Last Modified: Thu, 14 May 2020 00:03:19 GMT  
		Size: 198.8 MB (198754945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba17ef6b31a5c5254ebdec8f32489c5ccd869b03c0fe7f85696bd022f2e36e4d`  
		Last Modified: Fri, 15 May 2020 01:12:39 GMT  
		Size: 6.5 MB (6489129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcb471045f9f8a1c52412b672311154998b517531c6bc3f37adab5187c2c8ed`  
		Last Modified: Fri, 15 May 2020 01:13:02 GMT  
		Size: 27.7 MB (27666776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8900028743f045fda60795206c1fa08a67d1fefc7be6ec792592b231a3ec787`  
		Last Modified: Fri, 15 May 2020 01:12:52 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbddb5aa966258e4c58dfcad8d25f43b6aecb3e0db0d493ef0b8ea4a9fb7122`  
		Last Modified: Fri, 15 May 2020 01:12:54 GMT  
		Size: 1.9 MB (1931090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:buster` - linux; mips64le

```console
$ docker pull python@sha256:5fbb43e93b84826e99ad97e31dcc21341093602b73a6c7f00ca7e4ec87d4a7fb
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.4 MB (334421215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b51e564e8b9b06e55d50f455071bba632c40ea3b69b141e8455273d156dd7d15`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 13 May 2020 22:48:28 GMT
ADD file:97e851af4cc7dad736e0b6bdf3cb1b91e138aa9258cde6c860281333581b653a in / 
# Wed, 13 May 2020 22:48:29 GMT
CMD ["bash"]
# Wed, 13 May 2020 23:57:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:57:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 23:58:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 00:01:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 02:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2020 02:58:40 GMT
ENV LANG=C.UTF-8
# Thu, 14 May 2020 02:59:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 02:59:07 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 14 May 2020 18:07:36 GMT
ENV PYTHON_VERSION=3.8.3
# Thu, 14 May 2020 18:49:31 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 14 May 2020 18:49:33 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 14 May 2020 18:49:34 GMT
ENV PYTHON_PIP_VERSION=20.1
# Thu, 14 May 2020 18:49:34 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Thu, 14 May 2020 18:49:34 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Thu, 14 May 2020 18:49:54 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 14 May 2020 18:49:54 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:73ad38a668fc7790605704e34ddd5538366afd1604b76791e166187e503daf85`  
		Last Modified: Wed, 13 May 2020 22:57:04 GMT  
		Size: 49.0 MB (49021790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298d60c32e1de1409e5c95129f71a0e8a0806469bf44e7bd3c1ab4cba940ed67`  
		Last Modified: Thu, 14 May 2020 00:16:02 GMT  
		Size: 7.2 MB (7229789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f486b519d052c2fa785f0c37d788177cec9f73ef162f88cd44e383c2503b553b`  
		Last Modified: Thu, 14 May 2020 00:16:02 GMT  
		Size: 10.0 MB (10015786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0e37a3285c74bfb82aa286c4a7e7bd3a5094a91d7bf4ebb27e5f3d6fc2361d`  
		Last Modified: Thu, 14 May 2020 00:16:58 GMT  
		Size: 50.8 MB (50838680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6940b2964aa6c178b2ea24c65b8c648cf884a05581be3ff84ccfdf32bfae0ae9`  
		Last Modified: Thu, 14 May 2020 00:19:25 GMT  
		Size: 179.7 MB (179749657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11084821a034cabe46f139edde7d58282f98770f1c40bee592e09c83a10d031b`  
		Last Modified: Fri, 15 May 2020 01:16:28 GMT  
		Size: 6.5 MB (6454840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cad4508adc9fd54d793806ad84bef77324c4a399bf0520cef4d9cb5e3c2cb01`  
		Last Modified: Fri, 15 May 2020 01:17:33 GMT  
		Size: 29.2 MB (29179234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889247e2808e3ead41aff3215e678e726f63f6ace9a67037d2dbeb7dfe2271d0`  
		Last Modified: Fri, 15 May 2020 01:17:05 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b701c11418beb1521569bfe3e8c94f33fdb0fa66fc09b0832f0357718d86fb`  
		Last Modified: Fri, 15 May 2020 01:17:07 GMT  
		Size: 1.9 MB (1931206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:buster` - linux; ppc64le

```console
$ docker pull python@sha256:03e93883c7f96603464a0e669e697a28dc312a5f63916b06547ca96bf4537b3b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.9 MB (372864487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c397856b350f531691c191355942dea2b69414f1323a9a36d834a61633ca8216`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 13 May 2020 22:20:32 GMT
ADD file:ed5dc7bd2c0c0dafef9ca4829cd89719c538cd23991fb941589e7fd3bf96b407 in / 
# Wed, 13 May 2020 22:20:38 GMT
CMD ["bash"]
# Wed, 13 May 2020 23:43:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:44:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 23:45:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:54:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:01:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2020 17:01:46 GMT
ENV LANG=C.UTF-8
# Thu, 14 May 2020 20:13:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 20:13:23 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 14 May 2020 20:26:17 GMT
ENV PYTHON_VERSION=3.8.3
# Thu, 14 May 2020 20:35:11 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 14 May 2020 20:35:24 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 14 May 2020 20:35:27 GMT
ENV PYTHON_PIP_VERSION=20.1
# Thu, 14 May 2020 20:35:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Thu, 14 May 2020 20:35:41 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Thu, 14 May 2020 20:36:33 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 14 May 2020 20:36:44 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:19aca0f2a5b89bbc37caa77bbd1612566fadbbce5c3381246fe356d7e5d14774`  
		Last Modified: Wed, 13 May 2020 22:57:18 GMT  
		Size: 54.1 MB (54142914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556cd6fadc0f341d090a18ecfc4b6aedccd3d99f6eb6a336e3bee33f096c095f`  
		Last Modified: Thu, 14 May 2020 00:28:57 GMT  
		Size: 8.3 MB (8252823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633177125031b056c9e79b442829845cc6886ad14d5de3cc2459317eaa054d94`  
		Last Modified: Thu, 14 May 2020 00:28:59 GMT  
		Size: 10.7 MB (10727164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e762e21652d78f0bcf2f8011e2751e5d6be323a639e89c083f93a086fe1b6005`  
		Last Modified: Thu, 14 May 2020 00:30:19 GMT  
		Size: 57.5 MB (57459915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25daff9ab67476e2376e496ffe3b8ee9e8b1ce159afabc20b9925d9ffc106448`  
		Last Modified: Thu, 14 May 2020 00:33:04 GMT  
		Size: 203.0 MB (203016026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3574b232379c43a88ad5b06eab7012c39dc2730116496fb7539ea7393ddb854`  
		Last Modified: Fri, 15 May 2020 00:16:57 GMT  
		Size: 6.9 MB (6892251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ac62001b506d976168504aad861acd13d2c1c59d13975edb6dfe742ee4b6f1`  
		Last Modified: Fri, 15 May 2020 00:17:54 GMT  
		Size: 30.4 MB (30441736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55871abffa06dfec2984f9bcb801be4471aa8c68fea3937dae7d7bf1c45bf7ff`  
		Last Modified: Fri, 15 May 2020 00:17:26 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1106557e6b4230baaea29ed8f501cfc275bb838d4b8c7fcf7de9e32dc0c4202`  
		Last Modified: Fri, 15 May 2020 00:17:30 GMT  
		Size: 1.9 MB (1931425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:buster` - linux; s390x

```console
$ docker pull python@sha256:67488084ab548ea959e43f0374ff430ffab349fdada08d1ac83ab14fa3ad464a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.7 MB (331689308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c43017468e29006f0858c00d8de7f339331f989018db450bf54f49776171c4`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 13 May 2020 21:42:20 GMT
ADD file:8f8ce7623c9f93bb85bf3b2bb1f2515de7b053e11c2efc56feb959322aefc0a0 in / 
# Wed, 13 May 2020 21:42:22 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:39:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:39:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:40:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:41:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 02:34:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2020 02:34:36 GMT
ENV LANG=C.UTF-8
# Thu, 14 May 2020 02:37:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 02:37:50 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 14 May 2020 20:40:23 GMT
ENV PYTHON_VERSION=3.8.3
# Thu, 14 May 2020 20:44:50 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 14 May 2020 20:44:52 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 14 May 2020 20:44:52 GMT
ENV PYTHON_PIP_VERSION=20.1
# Thu, 14 May 2020 20:44:53 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Thu, 14 May 2020 20:44:53 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Thu, 14 May 2020 20:44:59 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 14 May 2020 20:44:59 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:6542b1e7bcc740fe79dab47cd5bcdb30fe618acd5d0d0e2583571b2ed256809c`  
		Last Modified: Wed, 13 May 2020 21:46:45 GMT  
		Size: 49.0 MB (48965117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfdd777c0ca04e5c74f52bdae1cc0e2a1ba232e895f109269bf84d8bb598a7a`  
		Last Modified: Wed, 13 May 2020 22:48:24 GMT  
		Size: 7.4 MB (7382349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be4faee9a8c310dbd16b8d77a0a4eee7f207a8cd04340c0852eb46655b9e7e`  
		Last Modified: Wed, 13 May 2020 22:48:29 GMT  
		Size: 9.9 MB (9882141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e46e850fe7f7138b3f6c7d0aa73ac1e5c4d1c8ee2d6272e32c6727088efcd9`  
		Last Modified: Wed, 13 May 2020 22:48:43 GMT  
		Size: 51.4 MB (51369321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f78e7e65e237be1d924b8cc10d6a39902a63883ea34c4836d92c32c45007c62`  
		Last Modified: Wed, 13 May 2020 22:49:11 GMT  
		Size: 176.8 MB (176762581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9620a37f100ae522c09866811a9cd1b31a683feb5641f45fc1eb76a1d952d17`  
		Last Modified: Thu, 14 May 2020 03:51:16 GMT  
		Size: 6.1 MB (6057906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4c9ba758ec769ea6e46246c9734ff7ff450f02803e82bc4aadaa19c4043e9b`  
		Last Modified: Thu, 14 May 2020 21:01:32 GMT  
		Size: 29.3 MB (29338483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066227c13a47953578760b1fcb62dd1368de0f1c23e846a4b6b975d39be77931`  
		Last Modified: Thu, 14 May 2020 21:01:40 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055738d04a8233877faf5bd986f447c8f7fa448e8757fd01101765bfba75a34c`  
		Last Modified: Thu, 14 May 2020 21:01:41 GMT  
		Size: 1.9 MB (1931177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
