## `python:latest`

```console
$ docker pull python@sha256:6f36deb58b90ad780f66dab8267ba4c47a9d6e83cadadcf23d761e4325df48ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 10
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.768; amd64
	-	windows version 10.0.17763.3046; amd64

### `python:latest` - linux; amd64

```console
$ docker pull python@sha256:607635763e54907fd75397fedfeb83890e62a0f9b54a1d99d27d748c5d269be4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351249570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930516bcf91017085701aa206ed5b6f05b880c1c43d4be61627c59ac1fb08f9d`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 12 Jul 2022 01:19:57 GMT
ADD file:3451708ab45bc1bcfc1ebb2075d3af16767477cbeb79334959e0d1ff02b0864b in / 
# Tue, 12 Jul 2022 01:19:58 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:48:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jul 2022 02:48:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:49:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 10:23:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 10:23:44 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 10:23:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 10:23:50 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 12 Jul 2022 11:23:52 GMT
ENV PYTHON_VERSION=3.10.5
# Tue, 12 Jul 2022 11:34:18 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version
# Tue, 12 Jul 2022 11:34:19 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 12 Jul 2022 11:34:19 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Tue, 12 Jul 2022 11:34:19 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 12 Jul 2022 11:34:19 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/6ce3639da143c5d79b44f94b04080abf2531fd6e/public/get-pip.py
# Tue, 12 Jul 2022 11:34:19 GMT
ENV PYTHON_GET_PIP_SHA256=ba3ab8267d91fd41c58dbce08f76db99f747f716d85ce1865813842bb035524d
# Tue, 12 Jul 2022 11:34:25 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 12 Jul 2022 11:34:26 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:d836772a1c1f9c4b1f280fb2a98ace30a4c4c87370f89aa092b35dfd9556278a`  
		Last Modified: Tue, 12 Jul 2022 01:24:06 GMT  
		Size: 55.0 MB (54999406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9e63c657ad881997f5165c0826be395bfc064415876b9fbaae74bcb5dc721`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 5.2 MB (5156110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1989b6e74cfdda1591b9dd23be47c5caeb002b7a151379361ec0c3f0e6d0e52`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 10.9 MB (10876416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28818711e1ed38df107014a20127b41491b224d7aed8aa7066b55552d9600d2`  
		Last Modified: Tue, 12 Jul 2022 02:55:23 GMT  
		Size: 54.6 MB (54579006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5084fa7ebd744165b15df008a9c14db7fc3d6af34cce64ba85bbaa348af594a3`  
		Last Modified: Tue, 12 Jul 2022 02:56:00 GMT  
		Size: 196.8 MB (196774352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f162c881e4f4673d8c7093e578c2dff9d249bc73fe24db52f9eb05c0575fa38`  
		Last Modified: Tue, 12 Jul 2022 13:17:59 GMT  
		Size: 6.3 MB (6290793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f48ccb2876ae27ffef0b6d25a19592e3753e336df89239f8ea90c2c12ffa98`  
		Last Modified: Tue, 12 Jul 2022 13:18:57 GMT  
		Size: 19.7 MB (19701232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315a1520c10e286803d5dabe4df67d96aedd2a9fda4c8e6f1bb2655ee3eee5e7`  
		Last Modified: Tue, 12 Jul 2022 13:18:53 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba0bda87095a22a072d4502de5a4f767edfea7f191d4f868f41b527fef413a1`  
		Last Modified: Tue, 12 Jul 2022 13:18:54 GMT  
		Size: 2.9 MB (2872022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:latest` - linux; arm variant v5

```console
$ docker pull python@sha256:01177de106d0a25cb654a1eecf02b32a35572ee78f6ccef3b6ff55e6a7a62d45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323155306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80d5c450fe0a2b4a9b3ac6bd68e2a01c4820fc51bbf641f91ada44de298da1e`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 23 Jun 2022 00:50:04 GMT
ADD file:a9a29412ef2a46df9ac08c0263e1fd3872777bcafdf6f172dae904af96ff7585 in / 
# Thu, 23 Jun 2022 00:50:04 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:37:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:37:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:38:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:40:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 13:11:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 13:11:55 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 13:12:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 13:12:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 23 Jun 2022 16:14:44 GMT
ENV PYTHON_VERSION=3.10.5
# Thu, 23 Jun 2022 16:42:49 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version
# Thu, 23 Jun 2022 16:42:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 23 Jun 2022 16:42:51 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Thu, 23 Jun 2022 16:42:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Thu, 23 Jun 2022 16:42:52 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/6ce3639da143c5d79b44f94b04080abf2531fd6e/public/get-pip.py
# Thu, 23 Jun 2022 16:42:52 GMT
ENV PYTHON_GET_PIP_SHA256=ba3ab8267d91fd41c58dbce08f76db99f747f716d85ce1865813842bb035524d
# Thu, 23 Jun 2022 16:43:07 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 23 Jun 2022 16:43:07 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:6e4031f48ff7c3b7223afff91721ded4a4de5f7c666f84c58a5d8298dd0fe028`  
		Last Modified: Thu, 23 Jun 2022 01:04:50 GMT  
		Size: 52.5 MB (52541138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81d328795b20b164711abd9d265ebf98fa864c36cc2ac7b79fcde10ea683a47`  
		Last Modified: Thu, 23 Jun 2022 02:01:21 GMT  
		Size: 5.1 MB (5065402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6df15bbc2ab79e81b31649e3d85b8e92141abf53487afd2e2dac38a9889b4d3`  
		Last Modified: Thu, 23 Jun 2022 02:01:23 GMT  
		Size: 10.6 MB (10573065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6277f05327b720d120a7609bad575356aea3c0f1ce8901aa52717c2f196ffb56`  
		Last Modified: Thu, 23 Jun 2022 02:02:17 GMT  
		Size: 52.3 MB (52315681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bcb5356225f839cd3d29f5be0f1b7818d19c263fbbb1187e7b9237f0f1c526`  
		Last Modified: Thu, 23 Jun 2022 02:04:18 GMT  
		Size: 175.0 MB (174954643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d927cbcc088810cb3634928bbd676ab3fa044840473aeb2bc622eac0a3737065`  
		Last Modified: Thu, 23 Jun 2022 21:35:54 GMT  
		Size: 6.0 MB (6018379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd26f29749e0139c41cb36404e72635915347d39d2701cfb2b150db97e1f5726`  
		Last Modified: Thu, 23 Jun 2022 21:37:40 GMT  
		Size: 18.8 MB (18814431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe14e138b197d642f337455a67fb87b2320efc38b551a550cf39bb312c822d4`  
		Last Modified: Thu, 23 Jun 2022 21:37:27 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7393fb2a6339fd7ff95316888c42b7af4158a27bfec5cedd27f0b393ac9ed876`  
		Last Modified: Thu, 23 Jun 2022 21:37:30 GMT  
		Size: 2.9 MB (2872333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:latest` - linux; arm variant v7

```console
$ docker pull python@sha256:d9cb50bbdb81bbd838e25ff1dc7e3b33207bddc56c49aa9ebd1e0d7dd3c00784
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.0 MB (310027936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce159d2b6f2a0df35f4d0749094c93adb99d8ec189d679535d67d2c596be1a1`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 23 Jun 2022 00:59:08 GMT
ADD file:59a6186285c4849971ea2d4801e6ebc1e4310f5e3dc0f87389f39d1fa8a63c58 in / 
# Thu, 23 Jun 2022 00:59:10 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:46:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:46:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:47:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:49:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 01:16:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jun 2022 01:16:03 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jun 2022 01:16:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 01:16:17 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 24 Jun 2022 04:56:32 GMT
ENV PYTHON_VERSION=3.10.5
# Fri, 24 Jun 2022 05:30:41 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version
# Fri, 24 Jun 2022 05:30:45 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Fri, 24 Jun 2022 05:30:48 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Fri, 24 Jun 2022 05:30:49 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Fri, 24 Jun 2022 05:30:50 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/6ce3639da143c5d79b44f94b04080abf2531fd6e/public/get-pip.py
# Fri, 24 Jun 2022 05:30:50 GMT
ENV PYTHON_GET_PIP_SHA256=ba3ab8267d91fd41c58dbce08f76db99f747f716d85ce1865813842bb035524d
# Fri, 24 Jun 2022 05:31:08 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Fri, 24 Jun 2022 05:31:09 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:2147df557f50051066d8920b460727b890c1da5cb2c15b055c99ed8216b5528f`  
		Last Modified: Thu, 23 Jun 2022 01:14:34 GMT  
		Size: 50.2 MB (50199604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b28303e18c4d3b1788071e1a67ed51ad28c9574bf30371176fc152638acdbe`  
		Last Modified: Thu, 23 Jun 2022 02:13:15 GMT  
		Size: 4.9 MB (4924846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536c76bf1b84e75e4834c8b50a6f3697460303c4b2021434891103b94ca78fac`  
		Last Modified: Thu, 23 Jun 2022 02:13:17 GMT  
		Size: 10.2 MB (10217964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72032391c22caab41b7e492fc3cac93cd17f7c920e05ff5c34031a544a4a833e`  
		Last Modified: Thu, 23 Jun 2022 02:14:07 GMT  
		Size: 50.3 MB (50329194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce902e7596eca4913ba3977a3f359a5df0ee13c148538d24d880f6687ee8ff1`  
		Last Modified: Thu, 23 Jun 2022 02:15:51 GMT  
		Size: 167.2 MB (167235667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c8ea064fe9f960b908b83b93bfea7fd952279f4291970bf72b3b8302143d45`  
		Last Modified: Fri, 24 Jun 2022 11:44:13 GMT  
		Size: 5.7 MB (5702509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2aaa6516cf6f120518d66c94f027959f9aa66caaf605282321b1f08fdaf56a`  
		Last Modified: Fri, 24 Jun 2022 11:46:05 GMT  
		Size: 18.5 MB (18545576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3e949dc61fa58d875b9c0c866a47eb368925f29a0a40a89a6383f968ad76cf`  
		Last Modified: Fri, 24 Jun 2022 11:45:53 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa15c435bff5ecafcb271021da48f8149ed1258e850a848b74810f9492d9fb3`  
		Last Modified: Fri, 24 Jun 2022 11:45:56 GMT  
		Size: 2.9 MB (2872343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:latest` - linux; arm64 variant v8

```console
$ docker pull python@sha256:dd7e34e45ab5f11c48fff92fde477650de79e6403ad6107e2ead853119af1c46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.2 MB (342168346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e005b03234cd99b3f50ee2143d45304b98bf33c7250b73007a9b07e19724e2d`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:18 GMT
ADD file:2dcc013bca5a420cad3b6a1ac61f52ea58a29ae05fe282078a744979c0e1a89e in / 
# Tue, 12 Jul 2022 00:40:19 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:33:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:33:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jul 2022 02:33:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:34:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 09:50:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 09:50:41 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 09:50:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 09:50:48 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 12 Jul 2022 10:54:57 GMT
ENV PYTHON_VERSION=3.10.5
# Tue, 12 Jul 2022 11:04:35 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version
# Tue, 12 Jul 2022 11:04:37 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 12 Jul 2022 11:04:38 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Tue, 12 Jul 2022 11:04:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 12 Jul 2022 11:04:40 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/6ce3639da143c5d79b44f94b04080abf2531fd6e/public/get-pip.py
# Tue, 12 Jul 2022 11:04:41 GMT
ENV PYTHON_GET_PIP_SHA256=ba3ab8267d91fd41c58dbce08f76db99f747f716d85ce1865813842bb035524d
# Tue, 12 Jul 2022 11:04:47 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 12 Jul 2022 11:04:48 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:cfc947b533a3ed8b8ce79820c7fe5e7634bf9c08479ed0aee1e74ee7b4f2b068`  
		Last Modified: Tue, 12 Jul 2022 00:45:41 GMT  
		Size: 53.7 MB (53683129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca36aa4204d2a708dcd1d41d1d4a128b095f8d88a2f9544f89799c36914e356`  
		Last Modified: Tue, 12 Jul 2022 02:42:29 GMT  
		Size: 5.1 MB (5142960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdcd2014de70fbce8c43a70cd1f42bceab4f1e35953db987fc318dbc0fb0d26`  
		Last Modified: Tue, 12 Jul 2022 02:42:30 GMT  
		Size: 10.7 MB (10657500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e288b20a616767a00416e22f7d8ee6390ba5b48061d92577f55bdb11121e6946`  
		Last Modified: Tue, 12 Jul 2022 02:42:53 GMT  
		Size: 54.7 MB (54673820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c814ed089439a4f3618519b0ae7ef02da9c1c3fc1535824d633ca1f76e78dbf`  
		Last Modified: Tue, 12 Jul 2022 02:43:32 GMT  
		Size: 189.7 MB (189680887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6c125e963db6d4d0713e74efe1da90b4ac60eb9a3b6a6f6508f529e9dbbdf2`  
		Last Modified: Tue, 12 Jul 2022 12:49:53 GMT  
		Size: 6.2 MB (6162711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cea02ceb178a99310639cef2d4960d630eddebfe5ec1e04321c1da40b755cce`  
		Last Modified: Tue, 12 Jul 2022 12:51:03 GMT  
		Size: 19.3 MB (19295283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e02b5c8de75246abbeb1dc9b19ea15d1f3104674352eb6ebc4639c02f994b5`  
		Last Modified: Tue, 12 Jul 2022 12:51:00 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3370a7d977b8481541233af9f179153bab41e4951440b65787d2030b9d87d9e`  
		Last Modified: Tue, 12 Jul 2022 12:51:01 GMT  
		Size: 2.9 MB (2871823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:latest` - linux; 386

```console
$ docker pull python@sha256:f48b3076c14a31529f310b3ea706e20e10faac36e184af763e151911f59beb82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.0 MB (356011364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1459a077c84783756820097637331bd3db46269e9e03d46edae1d9a51954b24a`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:17 GMT
ADD file:38ad8e7562f238cf436c2a32b21b397a0ad3dd5c8f68f29bc724458cad18a47e in / 
# Thu, 23 Jun 2022 00:39:18 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:11:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:11:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:12:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:12:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 06:23:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 06:23:49 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 06:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 06:24:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 23 Jun 2022 07:43:10 GMT
ENV PYTHON_VERSION=3.10.5
# Thu, 23 Jun 2022 07:54:38 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version
# Thu, 23 Jun 2022 07:54:39 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 23 Jun 2022 07:54:40 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Thu, 23 Jun 2022 07:54:41 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Thu, 23 Jun 2022 07:54:42 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/6ce3639da143c5d79b44f94b04080abf2531fd6e/public/get-pip.py
# Thu, 23 Jun 2022 07:54:43 GMT
ENV PYTHON_GET_PIP_SHA256=ba3ab8267d91fd41c58dbce08f76db99f747f716d85ce1865813842bb035524d
# Thu, 23 Jun 2022 07:54:51 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 23 Jun 2022 07:54:52 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:8bfd9a7ec075cef3ff84a270710c704347f9a866aeb50e5a286491696168d5f5`  
		Last Modified: Thu, 23 Jun 2022 00:46:04 GMT  
		Size: 56.0 MB (56007522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45f3c7c07e8e6bb9d2c30f8b932d9db0300b97850bfbf921a5b56ebefa99769`  
		Last Modified: Thu, 23 Jun 2022 01:22:14 GMT  
		Size: 5.1 MB (5080447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f01d925e37f51b5dbeac306dc641b52957d383e5fd3d61dc8822590b97d171`  
		Last Modified: Thu, 23 Jun 2022 01:22:15 GMT  
		Size: 11.0 MB (11033739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb4b9d72cb12455c850c1823ae918d6d05a7a2052a285314d41c63c81bbc32a`  
		Last Modified: Thu, 23 Jun 2022 01:22:37 GMT  
		Size: 55.9 MB (55914398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a325e396a9724c0a906a2b3b6f2f74d2ccc7c720ef1b464f807fcfa71aa5451`  
		Last Modified: Thu, 23 Jun 2022 01:23:14 GMT  
		Size: 199.7 MB (199687174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b946c44a41b956757c022574032d24877fd7821da06e4d02b6463b7bd7409a`  
		Last Modified: Thu, 23 Jun 2022 09:57:16 GMT  
		Size: 6.4 MB (6440298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc04ffe0daabe88ac0bb78e7401e009d11a5131a60a6e2b230704bcbe6bf96d9`  
		Last Modified: Thu, 23 Jun 2022 09:58:29 GMT  
		Size: 19.0 MB (18975754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fbe31965835c4c965baab941f310100bf968dbfc6a6d51dff1f46d91e769e5`  
		Last Modified: Thu, 23 Jun 2022 09:58:25 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc3b2cce548ba087be9f93a8e3ebb2a49e13174ef483932571e1b8c1e8af9b4`  
		Last Modified: Thu, 23 Jun 2022 09:58:26 GMT  
		Size: 2.9 MB (2871798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:latest` - linux; mips64le

```console
$ docker pull python@sha256:61fc47c0e55afa337509e21be868dd72e1fceb88b1f44002e0778caf9b9ad061
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329934363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f558608d4ef304ce98e71e6b5f0cfc0dbf06ed6975aa250a3bc28d8cd4f35bcd`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 23 Jun 2022 01:09:48 GMT
ADD file:b4c1f4f21cc3a6a3ebc27c9c15cfab9e67c385c2df87110392754663c02722f8 in / 
# Thu, 23 Jun 2022 01:09:53 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:52:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:53:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:54:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:59:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 13:04:58 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 13:05:04 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 13:05:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 13:05:50 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 23 Jun 2022 13:05:56 GMT
ENV PYTHON_VERSION=3.10.5
# Thu, 23 Jun 2022 14:19:26 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version
# Thu, 23 Jun 2022 14:19:35 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 23 Jun 2022 14:19:41 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Thu, 23 Jun 2022 14:19:47 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Thu, 23 Jun 2022 14:19:53 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/6ce3639da143c5d79b44f94b04080abf2531fd6e/public/get-pip.py
# Thu, 23 Jun 2022 14:19:59 GMT
ENV PYTHON_GET_PIP_SHA256=ba3ab8267d91fd41c58dbce08f76db99f747f716d85ce1865813842bb035524d
# Thu, 23 Jun 2022 14:20:31 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 23 Jun 2022 14:20:38 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:5a63618d87cd80f12f8640fecf6d13ece7ce3ac6260be88adcebe60f4da899b8`  
		Last Modified: Thu, 23 Jun 2022 01:19:34 GMT  
		Size: 53.3 MB (53273237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ac43be31041e2631cd8bdabfb3934fb423e7237e142c5b86e532e192e4fe36`  
		Last Modified: Thu, 23 Jun 2022 02:19:58 GMT  
		Size: 4.9 MB (4912505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dfda9893d218bf2decc23f236eb8276f1b5512b4d2647fbab36c43e9bbf96d3`  
		Last Modified: Thu, 23 Jun 2022 02:20:00 GMT  
		Size: 10.7 MB (10660150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5205b64237f8e05552a56eb9f5faffb06894bd3f477e61b3e1b2716380279e6f`  
		Last Modified: Thu, 23 Jun 2022 02:20:57 GMT  
		Size: 53.3 MB (53298997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b0c2f1d405a64bf4c2a9741495fbebc93a40357f5b2a4cb973d9a490fb51b7`  
		Last Modified: Thu, 23 Jun 2022 02:23:03 GMT  
		Size: 178.9 MB (178899942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e621176ca04a7c27a3f7702eaf380b68deedb5251873971a264a8b03fc351c0`  
		Last Modified: Fri, 24 Jun 2022 03:40:35 GMT  
		Size: 6.4 MB (6381672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ff4b33d864bb55b2aea9f625607d1debcc219469916a6054b4f30501619457`  
		Last Modified: Fri, 24 Jun 2022 03:40:43 GMT  
		Size: 19.6 MB (19635809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ec94a42708fc24a0cc2ddca4a72ce79936d847bd38d0798631c8d77b92747b`  
		Last Modified: Fri, 24 Jun 2022 03:40:30 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcfa693929f7164589ee6ff0a959097fe317393453406e8b5909fba330dd93b`  
		Last Modified: Fri, 24 Jun 2022 03:40:33 GMT  
		Size: 2.9 MB (2871818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:latest` - linux; ppc64le

```console
$ docker pull python@sha256:cd806bd82dd9e534fb0f449ed9044f8fa4d77a4aa5903b0d9a438acf5e57c59f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.6 MB (360561249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e04296c37e28c11b7f53cedb01617a1f13df6dbadbb4bf42affb8ffe6d83046`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 23 Jun 2022 02:01:53 GMT
ADD file:8e4c382536553538abd5a62333996023e484596173131dab18020775b0731238 in / 
# Thu, 23 Jun 2022 02:01:58 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:53:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 03:53:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 03:54:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:00:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 18:19:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 18:20:03 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 18:21:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 18:21:26 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 23 Jun 2022 20:35:20 GMT
ENV PYTHON_VERSION=3.10.5
# Thu, 23 Jun 2022 20:54:53 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version
# Thu, 23 Jun 2022 20:55:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 23 Jun 2022 20:55:03 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Thu, 23 Jun 2022 20:55:06 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Thu, 23 Jun 2022 20:55:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/6ce3639da143c5d79b44f94b04080abf2531fd6e/public/get-pip.py
# Thu, 23 Jun 2022 20:55:10 GMT
ENV PYTHON_GET_PIP_SHA256=ba3ab8267d91fd41c58dbce08f76db99f747f716d85ce1865813842bb035524d
# Thu, 23 Jun 2022 20:55:34 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 23 Jun 2022 20:55:38 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:03691a2d4065f9ca4fafadaa8229407224c6aac10796fc0884981e6c81a43b8d`  
		Last Modified: Thu, 23 Jun 2022 02:14:21 GMT  
		Size: 58.9 MB (58903151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a26b659a43f0973605ce681b0a27a9563e32a560c64518a32cbf9284ffbe8bf`  
		Last Modified: Thu, 23 Jun 2022 04:56:06 GMT  
		Size: 5.4 MB (5405243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d46f40a862767538cfa58e9d25dca4b07caa0e31992187e566a6c24b0e11f0`  
		Last Modified: Thu, 23 Jun 2022 04:56:07 GMT  
		Size: 11.6 MB (11627442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03898d1bb379aab2aa192ab335931abcab4a1a3cb67af8d83900ba9d2045af0`  
		Last Modified: Thu, 23 Jun 2022 04:56:34 GMT  
		Size: 58.9 MB (58855018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65476b8f919067f953bff76371cbc72b97c37a96fa033b668fe7cd72731a87d`  
		Last Modified: Thu, 23 Jun 2022 04:57:23 GMT  
		Size: 196.1 MB (196132098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6de5318da2bbef2d256fea9e904ec51c073c92604647afcb8978349f2f2ebb`  
		Last Modified: Fri, 24 Jun 2022 00:45:20 GMT  
		Size: 7.0 MB (7041924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861633baa9d3701b6394799ea81bcc1ef094f12802b19c645558e66e54326671`  
		Last Modified: Fri, 24 Jun 2022 00:46:37 GMT  
		Size: 19.7 MB (19723760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9130f81d0d1182693e6729f78f6de66c606a664b565751b3310a1379cac0dec`  
		Last Modified: Fri, 24 Jun 2022 00:46:33 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177551b00c77407d6564b6e054d335369fb002f217a1ac434e177eac0330c7d7`  
		Last Modified: Fri, 24 Jun 2022 00:46:34 GMT  
		Size: 2.9 MB (2872379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:latest` - linux; s390x

```console
$ docker pull python@sha256:84b88acd96d219964b11d6cb00d49e6080cd68390f0995ee8eacb3e2df630d54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.5 MB (324523929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff609b965e4a9885a4fccfd7ee675095d64ee474ffeb2cc9f96f2c1f58038a50`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:40 GMT
ADD file:80a08f446549ae1b71aaab0aada00625b804fd959e2a21a9c0747fb3cdb0afc0 in / 
# Thu, 23 Jun 2022 00:42:48 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:16:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:16:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:17:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:19:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 09:33:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 09:33:13 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 09:33:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 09:33:24 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 23 Jun 2022 10:49:57 GMT
ENV PYTHON_VERSION=3.10.5
# Thu, 23 Jun 2022 11:02:40 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		python3 --version
# Thu, 23 Jun 2022 11:02:45 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 23 Jun 2022 11:02:45 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Thu, 23 Jun 2022 11:02:46 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Thu, 23 Jun 2022 11:02:46 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/6ce3639da143c5d79b44f94b04080abf2531fd6e/public/get-pip.py
# Thu, 23 Jun 2022 11:02:47 GMT
ENV PYTHON_GET_PIP_SHA256=ba3ab8267d91fd41c58dbce08f76db99f747f716d85ce1865813842bb035524d
# Thu, 23 Jun 2022 11:02:56 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 23 Jun 2022 11:02:58 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:e92226c94dce8ebeb505bbbebdc70207295a4a602fc736044e4e69866dc05e58`  
		Last Modified: Thu, 23 Jun 2022 00:51:36 GMT  
		Size: 53.3 MB (53276772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d640cc8936c5cb6e3d305ec831be1b35a79839e07490358519cd2f48759274a`  
		Last Modified: Thu, 23 Jun 2022 01:35:00 GMT  
		Size: 5.1 MB (5140923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356e72745d061d1b1515a417d346c741fdcf0e3c58b6aa88cc86eee96ec3daac`  
		Last Modified: Thu, 23 Jun 2022 01:35:01 GMT  
		Size: 10.8 MB (10765497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f2f2ecbda16c1aa0309b44daf39322108f0e9dd6dfeaee815a8dd53cfee576`  
		Last Modified: Thu, 23 Jun 2022 01:35:19 GMT  
		Size: 54.0 MB (54045148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a279dbec4bccf345aae5f41c1b982cb7f5d871e7aebea1449dac9aa692f8bbb`  
		Last Modified: Thu, 23 Jun 2022 01:35:48 GMT  
		Size: 172.8 MB (172766694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf89a666945b7ebc60cc84dea311a20e0adf48da2770ace030678a8919c35660`  
		Last Modified: Thu, 23 Jun 2022 12:49:03 GMT  
		Size: 6.2 MB (6241966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbc6abc4ae9e80fd675801def4d6cd5b26208427c156c3b55528ac55f8877b1`  
		Last Modified: Thu, 23 Jun 2022 12:49:54 GMT  
		Size: 19.4 MB (19414380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925d63f4df4faba0f28a8cb77f78a9bed211a174dcf9649ef215c0cb86ea4e9d`  
		Last Modified: Thu, 23 Jun 2022 12:49:51 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94876683504fba053899f63db010e2029a217500756c1766c2cea313309904e7`  
		Last Modified: Thu, 23 Jun 2022 12:49:51 GMT  
		Size: 2.9 MB (2872316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:latest` - windows version 10.0.20348.768; amd64

```console
$ docker pull python@sha256:849b6013699452b5048fb9eebfcb5da1f252d2be08e4e79db5cb98048460458c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330905523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6960d0d954062da5ce0a61f7f742b093a16f4ab50d7b730360e768917ebe129`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 09 Jun 2022 04:32:50 GMT
RUN Install update 10.0.20348.768
# Wed, 15 Jun 2022 12:13:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jun 2022 12:38:33 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 15 Jun 2022 17:06:45 GMT
ENV PYTHON_VERSION=3.10.5
# Wed, 15 Jun 2022 17:08:09 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 15 Jun 2022 17:08:13 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Wed, 15 Jun 2022 17:08:15 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 15 Jun 2022 17:08:16 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/6ce3639da143c5d79b44f94b04080abf2531fd6e/public/get-pip.py
# Wed, 15 Jun 2022 17:08:17 GMT
ENV PYTHON_GET_PIP_SHA256=ba3ab8267d91fd41c58dbce08f76db99f747f716d85ce1865813842bb035524d
# Wed, 15 Jun 2022 17:09:07 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 15 Jun 2022 17:09:08 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6c71967ff41928927e4c407171e4ffbac3c9ab4221eb64f5ca5a34ff4c230567`  
		Size: 841.6 MB (841600427 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dec0338feaf01f35eb916b7fd9ecc08b719354163254885d5215e513c1a3eb2e`  
		Last Modified: Wed, 15 Jun 2022 12:49:26 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49758f20adbc06f35c19ffe31b46483c54cf98777d19e71c5858f41dbebd666`  
		Last Modified: Wed, 15 Jun 2022 12:54:00 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9150e1ceaf354a37638621abf0c974c8bab9e1c97493377128a19672394593`  
		Last Modified: Wed, 15 Jun 2022 17:22:52 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5d88098d2ab5acf529340f4789673eeaac64ce08ce8acd9c82ea127ee4479d`  
		Last Modified: Wed, 15 Jun 2022 17:23:01 GMT  
		Size: 48.7 MB (48681231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb2a14d2e34f13259f9ca5c9daa714d5bb901937fe9b6a7d140694b1534734d`  
		Last Modified: Wed, 15 Jun 2022 17:22:53 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9df643894a75bab8959755db1932b3d21132ae4889296816290b7292ff5559`  
		Last Modified: Wed, 15 Jun 2022 17:22:50 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f1ba76d952847fd758e8331ee4c593a13bedd9b16b5339b1e3549d86af3766`  
		Last Modified: Wed, 15 Jun 2022 17:22:50 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6cb44c5212eb2fd4427a68f369397fb91d2614b4c149cb4c1b59ccaba2bfd8`  
		Last Modified: Wed, 15 Jun 2022 17:22:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cf57f9aefd0b8261a26f940a6bf4bdfa82122f7d47a10396f1ecb7faae9a2f`  
		Last Modified: Wed, 15 Jun 2022 17:22:52 GMT  
		Size: 3.7 MB (3748859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00914738df4648031a2d1b14f8ebaf8969420f79b3ff8d5acb768fb22b1ea0da`  
		Last Modified: Wed, 15 Jun 2022 17:22:50 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:latest` - windows version 10.0.17763.3046; amd64

```console
$ docker pull python@sha256:438a38b4cd12c56aa1b2b8b5fb2d6cef602e3e39fcf29313c3d1a59ab73e2f92
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2715201688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb294ac021a097644b12cf02e719d617b576d26ade68993fab372c74604bf70`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 09 Jun 2022 19:41:03 GMT
RUN Install update 10.0.17763.3046
# Wed, 15 Jun 2022 12:18:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jun 2022 12:41:47 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 15 Jun 2022 17:09:32 GMT
ENV PYTHON_VERSION=3.10.5
# Wed, 15 Jun 2022 17:11:39 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 15 Jun 2022 17:11:40 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Wed, 15 Jun 2022 17:11:41 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 15 Jun 2022 17:11:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/6ce3639da143c5d79b44f94b04080abf2531fd6e/public/get-pip.py
# Wed, 15 Jun 2022 17:11:44 GMT
ENV PYTHON_GET_PIP_SHA256=ba3ab8267d91fd41c58dbce08f76db99f747f716d85ce1865813842bb035524d
# Wed, 15 Jun 2022 17:13:27 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 15 Jun 2022 17:13:28 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc6ae6c5aa2b4920ae68469c5e7e7c3a3c85e5eaafc24660e7b3adb21d6fce77`  
		Size: 786.1 MB (786113785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4ed911f97ae3a2a6279c70738e5692b14369ac11871a2bbd2f6ad301419527ad`  
		Last Modified: Wed, 15 Jun 2022 12:50:13 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a06c506fd1c86229974813982c21c141062b8d6df41c48831faa8ad1fd29cff`  
		Last Modified: Wed, 15 Jun 2022 12:54:55 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b9977c29d8fea1352edd7b1a632c25ad4276a49b984fe10962fb1bcadfbbe1`  
		Last Modified: Wed, 15 Jun 2022 17:23:20 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e0ae3f58f17b3a1807f290d0d5e516bd0cedcb0300812efc8af8f87ffdd34`  
		Last Modified: Wed, 15 Jun 2022 17:23:29 GMT  
		Size: 48.4 MB (48426391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e06ca1437326cf682f8e226eac5d936899227803676e2dfdfbef0c750c8d9b`  
		Last Modified: Wed, 15 Jun 2022 17:23:20 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3731a93550792e1e0b409a089264e2f2ccb97c84ea9d1a0b4215114304b8aa56`  
		Last Modified: Wed, 15 Jun 2022 17:23:18 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d843176538ba9f392a64070b48a6577c5d8dee79421a3da35f7cbc9fb3484f0`  
		Last Modified: Wed, 15 Jun 2022 17:23:18 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec2681144fe76dcbb52d6aea13a7b4265966c7b032c4913f313f22bd017f265`  
		Last Modified: Wed, 15 Jun 2022 17:23:18 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29aed4a29744f717fcf3762581312b8d9c9745d3079d369ed90d1bad93d6d4b`  
		Last Modified: Wed, 15 Jun 2022 17:23:22 GMT  
		Size: 3.5 MB (3484232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066e5880784a1644c0490dc0c9649f6b937e9a71f6be8c0a6d3e74da1810f04e`  
		Last Modified: Wed, 15 Jun 2022 17:23:18 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
