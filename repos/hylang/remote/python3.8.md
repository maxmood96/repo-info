## `hylang:python3.8`

```console
$ docker pull hylang@sha256:0115e11fb637457b7b678288678005e6b26ee331a1c5e0f3d09ef999b56e96af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `hylang:python3.8` - linux; amd64

```console
$ docker pull hylang@sha256:6020ce25f538c42fb2a1c97a6cf2f78eb690be30a112827260cfd2e249877ac6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48973124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d029baa25244fba052aecc61e20be9ee3405ca14e4e08974c39d5e42e2efb239`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 23:54:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 23:54:30 GMT
ENV LANG=C.UTF-8
# Fri, 03 Dec 2021 01:53:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 01:53:59 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 03 Dec 2021 01:54:00 GMT
ENV PYTHON_VERSION=3.8.12
# Fri, 03 Dec 2021 02:03:57 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Fri, 03 Dec 2021 02:04:00 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 03 Dec 2021 02:04:00 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Fri, 03 Dec 2021 02:04:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Fri, 03 Dec 2021 02:04:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Fri, 03 Dec 2021 02:04:01 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Fri, 03 Dec 2021 02:04:23 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 03 Dec 2021 02:04:23 GMT
CMD ["python3"]
# Fri, 03 Dec 2021 19:56:03 GMT
ENV HY_VERSION=1.0a3
# Fri, 03 Dec 2021 19:56:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 03 Dec 2021 19:56:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5007e9ae005c1e8657c373ad27d7a6054d2b8cfc037ac22a0c959241bff9b364`  
		Last Modified: Fri, 03 Dec 2021 03:34:54 GMT  
		Size: 1.1 MB (1075899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c5660d119c1dc80800a9611aa5d90221883bd93494c9cafbdf50d5978687c`  
		Last Modified: Fri, 03 Dec 2021 03:34:56 GMT  
		Size: 10.8 MB (10767904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4490731c277a3a6235130fe0f103bdfa2863d7a2c044e078ca923c0952f8f73`  
		Last Modified: Fri, 03 Dec 2021 03:34:53 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f951ddd7713a4ddee0e0e88855cc445610b85e5c5fe9eccaaf9df2516635bf`  
		Last Modified: Fri, 03 Dec 2021 03:34:54 GMT  
		Size: 2.6 MB (2640522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ac2228cf9da7144cb6458b2b1849fbad9058cbe9b64fefdd5687b3d748ca50`  
		Last Modified: Fri, 03 Dec 2021 20:00:18 GMT  
		Size: 3.1 MB (3118346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8` - linux; arm variant v5

```console
$ docker pull hylang@sha256:0018d3902357d3d2592c54ffe80f69828ede7b2f741ce5501c9925235431a084
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46057695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d00209869e4763eb3fe77e7e5f7c13c2c92e683606b9025f61aced6a14b10e0`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 02 Dec 2021 02:50:37 GMT
ADD file:7debbdb237139cb08189976f79cfa64cfd71f5cc98dfb2f560b558acb5f7cec9 in / 
# Thu, 02 Dec 2021 02:50:38 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:04:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:04:22 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 14:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 14:59:15 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 02 Dec 2021 14:59:15 GMT
ENV PYTHON_VERSION=3.8.12
# Thu, 02 Dec 2021 15:13:26 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Thu, 02 Dec 2021 15:13:28 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 02 Dec 2021 15:13:28 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Thu, 02 Dec 2021 15:13:29 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 02 Dec 2021 15:13:29 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Thu, 02 Dec 2021 15:13:30 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Thu, 02 Dec 2021 15:14:02 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 02 Dec 2021 15:14:03 GMT
CMD ["python3"]
# Fri, 03 Dec 2021 10:26:07 GMT
ENV HY_VERSION=1.0a3
# Fri, 03 Dec 2021 10:26:18 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 03 Dec 2021 10:26:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c5e429166894878430c39748965935f89ffa957667340c3c8bd872418dbce663`  
		Last Modified: Thu, 02 Dec 2021 03:09:28 GMT  
		Size: 28.9 MB (28910824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e8d7688b551e0a08d00174e6f36009241e200969badfa700941ad5afb34424`  
		Last Modified: Thu, 02 Dec 2021 17:58:16 GMT  
		Size: 1.1 MB (1059097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1025efa528a49d753c93868938f9332d8b9075d980a2f486de2c7564e3baecc3`  
		Last Modified: Thu, 02 Dec 2021 17:58:22 GMT  
		Size: 10.3 MB (10328615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8365b563b27077149c5b5ad77490298d58a6c46cebea40f87432fb84e2f3dd16`  
		Last Modified: Thu, 02 Dec 2021 17:58:15 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ede392e60c5734b2ab465b28394e3105f991a6f909bc44e1afd7ea78b49ec28`  
		Last Modified: Thu, 02 Dec 2021 17:58:17 GMT  
		Size: 2.6 MB (2640172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a40c552e84aa0dd9bfdc8ae552960ad6c1018a1b99bd257899c516d5b19d53`  
		Last Modified: Fri, 03 Dec 2021 10:32:09 GMT  
		Size: 3.1 MB (3118754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8` - linux; arm variant v7

```console
$ docker pull hylang@sha256:904ed870369a4ae51b5f906737ff100c6338b0d6c6d877b3c8d19275cd8becd1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43271305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1944db69c425276e27f996386ed570b5b60eaecd2de4c32afa7ac72869326c5`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 02 Dec 2021 09:05:17 GMT
ADD file:97ce5af9ff4fb4002733d5c402ddc01a13e765d31b85bb6525a7fa797b698e10 in / 
# Thu, 02 Dec 2021 09:05:17 GMT
CMD ["bash"]
# Fri, 03 Dec 2021 08:30:35 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 08:30:36 GMT
ENV LANG=C.UTF-8
# Fri, 03 Dec 2021 13:16:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 13:16:00 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 03 Dec 2021 13:16:01 GMT
ENV PYTHON_VERSION=3.8.12
# Fri, 03 Dec 2021 13:36:29 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Fri, 03 Dec 2021 13:36:31 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 03 Dec 2021 13:36:31 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Fri, 03 Dec 2021 13:36:32 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Fri, 03 Dec 2021 13:36:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Fri, 03 Dec 2021 13:36:33 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Fri, 03 Dec 2021 13:37:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 03 Dec 2021 13:37:01 GMT
CMD ["python3"]
# Sat, 04 Dec 2021 12:13:18 GMT
ENV HY_VERSION=1.0a3
# Sat, 04 Dec 2021 12:13:28 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 04 Dec 2021 12:13:28 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ba82a1312e1efdcd1cc6eb31cd40358dcec180da31779dac399cba31bf3dc206`  
		Last Modified: Thu, 02 Dec 2021 09:21:03 GMT  
		Size: 26.6 MB (26573192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dcc84035ff9344ba0005be7fa561bbe2e89c3deecc16233a0c515922659aff`  
		Last Modified: Fri, 03 Dec 2021 17:03:17 GMT  
		Size: 1.0 MB (1041358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b56fb80872ea0b1275851a7e259d54534be9f40077f04c68c6dbb2367664aa`  
		Last Modified: Fri, 03 Dec 2021 17:03:23 GMT  
		Size: 9.9 MB (9897533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564446b6ad0aafa4ad6842c04eff407e25053df6b7a96fe787df24ae37a73df9`  
		Last Modified: Fri, 03 Dec 2021 17:03:16 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec44f44412a93d7c8561dd4e71f81343cad2edaa18672e0e20dd0ae2ac3c16c3`  
		Last Modified: Fri, 03 Dec 2021 17:03:19 GMT  
		Size: 2.6 MB (2640264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7386a32f492c1bc9733416f8008559605ff406d49987d27566a2a024045a60c3`  
		Last Modified: Sat, 04 Dec 2021 12:24:42 GMT  
		Size: 3.1 MB (3118725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:a3b7c81f0f156b8bf26a4a81a06337dfead3351f0bc750bd7a1aa9c4cd7d04ea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47234066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7470668db96c04b77b3ab62986cc8f0f65d942d3f8e1583bf3f6262e01db57bd`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:09 GMT
ADD file:002f2f7c6dc806b24b6c365882acd59d2b3d3fcec46d8fd99130b07a4575c88c in / 
# Thu, 02 Dec 2021 08:08:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 18:37:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 18:38:00 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 20:00:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 20:00:44 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 02 Dec 2021 20:00:45 GMT
ENV PYTHON_VERSION=3.8.12
# Thu, 02 Dec 2021 20:05:23 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Thu, 02 Dec 2021 20:05:24 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 02 Dec 2021 20:05:25 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Thu, 02 Dec 2021 20:05:26 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 02 Dec 2021 20:05:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Thu, 02 Dec 2021 20:05:28 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Thu, 02 Dec 2021 20:05:41 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 02 Dec 2021 20:05:42 GMT
CMD ["python3"]
# Fri, 03 Dec 2021 16:20:13 GMT
ENV HY_VERSION=1.0a3
# Fri, 03 Dec 2021 16:20:17 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 03 Dec 2021 16:20:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:968621624b326084ed82349252b333e649eaab39f71866edb2b9a4f847283680`  
		Last Modified: Thu, 02 Dec 2021 08:40:45 GMT  
		Size: 30.1 MB (30056536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbc34a04f24b25819582f3c9f5781daa3200d3d90035f2f930b18fac5bb5b23`  
		Last Modified: Thu, 02 Dec 2021 21:13:46 GMT  
		Size: 859.1 KB (859100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e76cdadf897f9982009c198a08b77a4bfedd5a53cebc0b32dd12f51663a517`  
		Last Modified: Thu, 02 Dec 2021 21:13:48 GMT  
		Size: 10.8 MB (10773088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e904bb1736824b731a5df04f9dcdc2f0f95387796f6d34db964c4acd70ad7e`  
		Last Modified: Thu, 02 Dec 2021 21:13:46 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87a520a6b16294ac277531a9597eedd3add38827c6de5ec18c5403a35581b30`  
		Last Modified: Thu, 02 Dec 2021 21:13:47 GMT  
		Size: 2.4 MB (2427150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed2b081a702ef57f6c0755484f9e840c378b871707368cb4a924365dd8dff80`  
		Last Modified: Fri, 03 Dec 2021 16:26:50 GMT  
		Size: 3.1 MB (3117958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8` - linux; 386

```console
$ docker pull hylang@sha256:8235e92accf90b1fe7435082da00339c82b86199957b20c209be96adafc49f90
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50098027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc5c159849060b6e0b786948c976d2b7d3a538918edc78f61e5f11c8bfc3251`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 02 Dec 2021 02:39:54 GMT
ADD file:0284c10b06ba22560408e1e14c1147887f4302c79dba143277ece2e333d6dcbc in / 
# Thu, 02 Dec 2021 02:39:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 19:52:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 19:52:47 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 23:15:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 23:15:17 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 02 Dec 2021 23:15:18 GMT
ENV PYTHON_VERSION=3.8.12
# Thu, 02 Dec 2021 23:25:57 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Thu, 02 Dec 2021 23:25:58 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 02 Dec 2021 23:25:59 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Thu, 02 Dec 2021 23:25:59 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 02 Dec 2021 23:25:59 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Thu, 02 Dec 2021 23:25:59 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Thu, 02 Dec 2021 23:26:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 02 Dec 2021 23:26:16 GMT
CMD ["python3"]
# Fri, 03 Dec 2021 06:28:29 GMT
ENV HY_VERSION=1.0a3
# Fri, 03 Dec 2021 06:28:39 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 03 Dec 2021 06:28:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2df7932f17d752876c686aa22054692a38e88e182dd7b6a5cca7ffce4ffe6f84`  
		Last Modified: Thu, 02 Dec 2021 02:47:59 GMT  
		Size: 32.4 MB (32380814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b9913594558fe663b59612e6a1c1a21988cbd99f3ae6297d61307862b0905f`  
		Last Modified: Fri, 03 Dec 2021 01:29:50 GMT  
		Size: 1.1 MB (1088340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c536cd1a5c9beec416d4e5a7df4bc1efa80b954695bbcbc826013d0e6c5b85`  
		Last Modified: Fri, 03 Dec 2021 01:29:53 GMT  
		Size: 10.9 MB (10869777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8552121cd2d4c66d45f5a86310c6c5f306f0dc7a9c8d8bfe96aa9460cd044414`  
		Last Modified: Fri, 03 Dec 2021 01:29:49 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29ee5af4d23c4ac9da526dc0e6958dd0b3cdd9efe480e9098c54103084b2596`  
		Last Modified: Fri, 03 Dec 2021 01:29:50 GMT  
		Size: 2.6 MB (2640036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ed84b522f28b7689596e8e9bc042ad6a55bba423f47c6eca9feab48cd2e785`  
		Last Modified: Fri, 03 Dec 2021 06:38:24 GMT  
		Size: 3.1 MB (3118827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8` - linux; mips64le

```console
$ docker pull hylang@sha256:4d274bdc2d0aef53213c2ffabe9c3bc6cbec683bee5d13a044df6f9926b873cb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47077446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d24eb8ba548cd177cbb75fdd38ad7f0ea9f3e60e6aa46339c09ffedb69d1ed`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 02 Dec 2021 03:09:10 GMT
ADD file:419aff162077eb16923c3ede6455ca86756a929a5a837bc6ac6b8dc67913503a in / 
# Thu, 02 Dec 2021 03:09:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 07:46:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 07:46:02 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 17:31:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 17:31:04 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 02 Dec 2021 17:31:04 GMT
ENV PYTHON_VERSION=3.8.12
# Thu, 02 Dec 2021 18:15:17 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Thu, 02 Dec 2021 18:15:19 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 02 Dec 2021 18:15:19 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Thu, 02 Dec 2021 18:15:20 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 02 Dec 2021 18:15:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Thu, 02 Dec 2021 18:15:20 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Thu, 02 Dec 2021 18:16:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 02 Dec 2021 18:16:11 GMT
CMD ["python3"]
# Sat, 04 Dec 2021 02:24:58 GMT
ENV HY_VERSION=1.0a3
# Sat, 04 Dec 2021 02:25:14 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 04 Dec 2021 02:25:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:df61fb15db6391af55d70bc3c0db3e9014438c81bf802619fb527221adf5e8a8`  
		Last Modified: Thu, 02 Dec 2021 03:17:58 GMT  
		Size: 29.6 MB (29630496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03920be873b336fcc82e9ce2457278948b2be761b0c6376d7bbeb0ce84e2aa83`  
		Last Modified: Fri, 03 Dec 2021 00:57:21 GMT  
		Size: 1.0 MB (1049296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0352fe87b39904d8d86e56711d8980e51af8e4ab8f886e2223254155c3697090`  
		Last Modified: Fri, 03 Dec 2021 00:57:28 GMT  
		Size: 10.6 MB (10638784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c447cd7c1e4d3db68d8c2268decb093ac08c707b3aa635568e250340246de01`  
		Last Modified: Fri, 03 Dec 2021 00:57:20 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ae72f99a4c629a57afeb60f60ca5816e08170de450613e233185748dde0cfa`  
		Last Modified: Fri, 03 Dec 2021 00:57:23 GMT  
		Size: 2.6 MB (2640093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d25ec190865ababc6731d2ad92af4a3892418b1227f7deed4de93fad81d63ba`  
		Last Modified: Sat, 04 Dec 2021 02:31:45 GMT  
		Size: 3.1 MB (3118544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8` - linux; ppc64le

```console
$ docker pull hylang@sha256:b75d6b2649fbc09a022cc9dae8e17c17eb749328a78fcd8588cf56020a290e30
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53252444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560dff3ba02a96f639fb4e901f2746840b822416331511837fecf761e296e7c0`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 02 Dec 2021 07:21:21 GMT
ADD file:81a93de7f5dcdbb9397c05b9b6bb7dc5a4742119d46faf929b4c6277b02be7a5 in / 
# Thu, 02 Dec 2021 07:21:25 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 14:34:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 14:34:52 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 17:41:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 17:41:21 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 02 Dec 2021 17:41:22 GMT
ENV PYTHON_VERSION=3.8.12
# Thu, 02 Dec 2021 17:56:25 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Thu, 02 Dec 2021 17:56:34 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 02 Dec 2021 17:56:38 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Thu, 02 Dec 2021 17:56:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 02 Dec 2021 17:56:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Thu, 02 Dec 2021 17:56:45 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Thu, 02 Dec 2021 17:57:23 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 02 Dec 2021 17:57:26 GMT
CMD ["python3"]
# Fri, 03 Dec 2021 21:02:47 GMT
ENV HY_VERSION=1.0a3
# Fri, 03 Dec 2021 21:03:11 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 03 Dec 2021 21:03:19 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8d46978b233ccedeaa1cbef7248b214991469fa922cc4fbf9916f9d0711d2d2e`  
		Last Modified: Thu, 02 Dec 2021 07:31:43 GMT  
		Size: 35.3 MB (35271379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad766671d163f618045bb75289f5be688901743b6313769331ba7a13b966abd7`  
		Last Modified: Thu, 02 Dec 2021 20:36:04 GMT  
		Size: 1.1 MB (1094364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94758a1311080642d8347d03e9ea2c2e767c434e5c09c961f0a4530ce6db58f`  
		Last Modified: Thu, 02 Dec 2021 20:36:05 GMT  
		Size: 11.1 MB (11125821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed50903e1f698c6d1f9ae8b20dafc7b6ab3561ceb4d3dae1815bba3568efad0`  
		Last Modified: Thu, 02 Dec 2021 20:36:03 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a27702a7e8eacf59d7f4c1b0867d9e3f11ba089eebb4b0abf94a04755ef2427`  
		Last Modified: Thu, 02 Dec 2021 20:36:04 GMT  
		Size: 2.6 MB (2641585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1917e0ab1ed1c962fa9c5b8eb9a8e07556db85da12353959f87f547699aa2221`  
		Last Modified: Fri, 03 Dec 2021 21:12:57 GMT  
		Size: 3.1 MB (3119063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8` - linux; s390x

```console
$ docker pull hylang@sha256:902cea043ead24db4e287dd714b818b79bec15dd35f0726ae8b105fe84261420
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47061825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45a19c7a1d65f3f8ed475d1a214714b3114961b7c815bee6fcf51b68901370e`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:27 GMT
ADD file:c8a482d41bf09dfb6484bf2a6e38535bf0594d26dd6eedd5abde4e3cc811fa6c in / 
# Tue, 21 Dec 2021 01:42:29 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 08:28:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 08:28:54 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 09:39:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 09:39:45 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 21 Dec 2021 09:39:45 GMT
ENV PYTHON_VERSION=3.8.12
# Tue, 21 Dec 2021 09:44:06 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Tue, 21 Dec 2021 09:44:07 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 21 Dec 2021 09:44:07 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Tue, 21 Dec 2021 09:44:07 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 21 Dec 2021 09:44:07 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Tue, 21 Dec 2021 09:44:07 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Tue, 21 Dec 2021 09:44:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 21 Dec 2021 09:44:17 GMT
CMD ["python3"]
# Tue, 21 Dec 2021 18:36:35 GMT
ENV HY_VERSION=1.0a3
# Tue, 21 Dec 2021 18:36:39 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Tue, 21 Dec 2021 18:36:39 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:12562551722a758d23ceea9abcdc2bee737e38c8f62a0f3d3afb2cc2626c28b1`  
		Last Modified: Tue, 21 Dec 2021 01:48:15 GMT  
		Size: 29.6 MB (29641636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5554a866a6ce1b589e2e3f7232a8a2f5c6783b9ba827783f09b22e10bf9b95f9`  
		Last Modified: Tue, 21 Dec 2021 10:39:05 GMT  
		Size: 1.1 MB (1075371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb0f3c8828ed112f01657c91c6553b08919b0f25549eaf932ea2f23d02272bc`  
		Last Modified: Tue, 21 Dec 2021 10:39:06 GMT  
		Size: 10.6 MB (10586380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e46d7314520c1979efe35aca39cbcb5bbfd1fabcbec583fe2537b02a38f5868`  
		Last Modified: Tue, 21 Dec 2021 10:39:04 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0140333c385b496da1c4cf2357800bb2829c0cf01a380a4b68fe313d18c6005a`  
		Last Modified: Tue, 21 Dec 2021 10:39:05 GMT  
		Size: 2.6 MB (2639997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc545e39e75654c127a1ffa494824acf0ed0baac72c2ff92aadbf2f3d728f98`  
		Last Modified: Tue, 21 Dec 2021 18:42:46 GMT  
		Size: 3.1 MB (3118207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
