## `hylang:python3.9-buster`

```console
$ docker pull hylang@sha256:a7b8dbc764cd3a69be43a398953b253a322986e4b54c619184689f80dc680fa8
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

### `hylang:python3.9-buster` - linux; amd64

```console
$ docker pull hylang@sha256:f19bf4044b05e9762434029598f80a90ef191d97f7c2958bf0e125c66ca0e726
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46593495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47b3124bac16280d3174931a974cdc096af1172f6485d855105d519a4a9a4b6`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:58:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 14:58:42 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 14:59:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 15:17:29 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 22 Jul 2021 15:17:29 GMT
ENV PYTHON_VERSION=3.9.6
# Thu, 22 Jul 2021 15:25:19 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Thu, 22 Jul 2021 15:25:20 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 02 Aug 2021 19:36:26 GMT
ENV PYTHON_PIP_VERSION=21.2.2
# Mon, 02 Aug 2021 19:36:26 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a1675ab6c2bd898ed82b1f58c486097f763c74a9/public/get-pip.py
# Mon, 02 Aug 2021 19:36:27 GMT
ENV PYTHON_GET_PIP_SHA256=6665659241292b2147b58922b9ffe11dda66b39d52d8a6f3aa310bc1d60ea6f7
# Mon, 02 Aug 2021 19:36:38 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 02 Aug 2021 19:36:38 GMT
CMD ["python3"]
# Mon, 02 Aug 2021 20:37:27 GMT
ENV HY_VERSION=1.0a3
# Mon, 02 Aug 2021 20:37:31 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Mon, 02 Aug 2021 20:37:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b693dfa28d38fd92288f84a9e7ffeba93eba5caff2c1b7d9fe3385b6dd972b5d`  
		Last Modified: Thu, 22 Jul 2021 16:42:29 GMT  
		Size: 2.8 MB (2769689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8f1a8cefd144b4ee4871a7d0d9e34f67c8c266f516c221e6d20bca001ce2a5`  
		Last Modified: Thu, 22 Jul 2021 16:43:16 GMT  
		Size: 10.9 MB (10939022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248d7d56b4a792ca7bdfe866fde773a9cf2028f973216160323684ceabb36451`  
		Last Modified: Thu, 22 Jul 2021 16:43:14 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae7b795eae044caca4942f6cadb2f57d65de60c7e9c91cec744c4bc09b3a02d`  
		Last Modified: Mon, 02 Aug 2021 19:44:06 GMT  
		Size: 2.6 MB (2644505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0141c04b6ca1b8ebf72ec8c3a0cd67a4a739c082c1489e75c2d9cb649fbe7dc8`  
		Last Modified: Mon, 02 Aug 2021 20:41:12 GMT  
		Size: 3.1 MB (3094251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-buster` - linux; arm variant v5

```console
$ docker pull hylang@sha256:08e1375b5cdff239246b07d74388ded62e8162b24437e51ca850a913740dcd55
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43691985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad6838f5b640ca5ee77ed565d28b14063ab4b3b9554a4ec07ce0a65662d3965`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 22 Jul 2021 00:50:06 GMT
ADD file:885454a996e63d5eb93f1f365a3be77a441f368d7f5a77a7fd1636edf5d0b8cd in / 
# Thu, 22 Jul 2021 00:50:07 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 02:46:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 02:46:32 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 02:46:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 03:18:27 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 22 Jul 2021 03:18:27 GMT
ENV PYTHON_VERSION=3.9.6
# Thu, 22 Jul 2021 03:34:13 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Thu, 22 Jul 2021 03:34:16 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 06 Aug 2021 19:41:54 GMT
ENV PYTHON_PIP_VERSION=21.2.3
# Fri, 06 Aug 2021 19:41:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c20b0cfd643cd4a19246ccf204e2997af70f6b21/public/get-pip.py
# Fri, 06 Aug 2021 19:41:55 GMT
ENV PYTHON_GET_PIP_SHA256=fa6f3fb93cce234cd4e8dd2beb54a51ab9c247653b52855a48dd44e6b21ff28b
# Fri, 06 Aug 2021 19:42:29 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 06 Aug 2021 19:42:29 GMT
CMD ["python3"]
# Fri, 06 Aug 2021 20:56:54 GMT
ENV HY_VERSION=1.0a3
# Fri, 06 Aug 2021 20:57:05 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 06 Aug 2021 20:57:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2b96a0a1ddfe4fab89025b13e583392414251af73361434f28af076c3db77100`  
		Last Modified: Thu, 22 Jul 2021 01:02:11 GMT  
		Size: 24.9 MB (24879093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2bd7a406444a1ab8415b34650bdea7389dfc5c163c21388aeaf09598c0aea7`  
		Last Modified: Thu, 22 Jul 2021 05:53:54 GMT  
		Size: 2.5 MB (2460051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc76618a98af4f06cbf24fc7667720155e9c590ffff68a44567c861ffd2a36a`  
		Last Modified: Thu, 22 Jul 2021 05:55:05 GMT  
		Size: 10.6 MB (10614413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2f3871e82968075132318d9fa3f4f032e74a3bb873047c8e4753dea35b65fb`  
		Last Modified: Thu, 22 Jul 2021 05:54:59 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56a1991a03251c29db063a3dff54c379dff991781573c9ed2b8ec3a7d6eb0d1`  
		Last Modified: Fri, 06 Aug 2021 19:55:31 GMT  
		Size: 2.6 MB (2642984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea8a1a99e47c874e70f2839f4499d76a2d937d171df573bc7dbf34e710aaf86`  
		Last Modified: Fri, 06 Aug 2021 21:01:48 GMT  
		Size: 3.1 MB (3095212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-buster` - linux; arm variant v7

```console
$ docker pull hylang@sha256:66128281f502f82dff16fe397767c6ea0f0aca6daa3bce2d5cb03a2d29b9e2f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40988065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1354e9c1caf566aeb858f3b127922d4e218cbc5e32c8a5e8ba4de668c6ddc90`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 22 Jul 2021 02:03:46 GMT
ADD file:8f466611d9ba85407e1768128a6a2a51886b78675a4775badb9d42e57c4a182e in / 
# Thu, 22 Jul 2021 02:03:47 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 21:35:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 21:35:27 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 21:35:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 22:17:07 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 22 Jul 2021 22:17:07 GMT
ENV PYTHON_VERSION=3.9.6
# Thu, 22 Jul 2021 22:37:16 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Thu, 22 Jul 2021 22:37:18 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 02 Aug 2021 19:12:00 GMT
ENV PYTHON_PIP_VERSION=21.2.2
# Mon, 02 Aug 2021 19:12:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a1675ab6c2bd898ed82b1f58c486097f763c74a9/public/get-pip.py
# Mon, 02 Aug 2021 19:12:00 GMT
ENV PYTHON_GET_PIP_SHA256=6665659241292b2147b58922b9ffe11dda66b39d52d8a6f3aa310bc1d60ea6f7
# Mon, 02 Aug 2021 19:12:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 02 Aug 2021 19:12:30 GMT
CMD ["python3"]
# Mon, 02 Aug 2021 20:23:38 GMT
ENV HY_VERSION=1.0a3
# Mon, 02 Aug 2021 20:23:49 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Mon, 02 Aug 2021 20:23:50 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:607f77084e8a15bf45d56215b058a593cdcf4e0039e5326157954b12663c0d31`  
		Last Modified: Thu, 22 Jul 2021 02:16:17 GMT  
		Size: 22.7 MB (22745974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1a8191a10072c4e750ee9dc8ef81c1ab84e1fa1637d46ed0328eead2788749`  
		Last Modified: Fri, 23 Jul 2021 01:33:43 GMT  
		Size: 2.4 MB (2358464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41b1ed47412d9acd7b9e4b8593b77af20c12c410ed56b0cd2c0cb470b703e95`  
		Last Modified: Fri, 23 Jul 2021 01:35:03 GMT  
		Size: 10.1 MB (10144760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51f7a0be6a3dfc83c6092b90f79b371ac5faa2eaabd1ba9aec46294444e0f6a`  
		Last Modified: Fri, 23 Jul 2021 01:34:56 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc2fb20ca26b2e15a062804e5ced1bdbdba53f7259e4fe0984a37a580414338`  
		Last Modified: Mon, 02 Aug 2021 19:31:09 GMT  
		Size: 2.6 MB (2644239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6951277ccbd2c72b96a8f37f094110d05631d3aae5c2b28dfa8298da580964bc`  
		Last Modified: Mon, 02 Aug 2021 20:34:47 GMT  
		Size: 3.1 MB (3094395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-buster` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:d59594d99645b23feef4b1b07dab26d3a32e9ee1bf45b0b8d2bbb9734451b878
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45234894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9e59f20a22db59546c6d38b7008fe80302664ef96eb08e9a31563a00497eaf`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 22 Jul 2021 00:40:14 GMT
ADD file:074ffc2065bab83c9a5c596576656b04d271dd78406aadad160b68e38f38269f in / 
# Thu, 22 Jul 2021 00:40:14 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 10:36:58 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 10:36:58 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 10:37:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 10:51:22 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 22 Jul 2021 10:51:22 GMT
ENV PYTHON_VERSION=3.9.6
# Thu, 22 Jul 2021 10:57:52 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Thu, 22 Jul 2021 10:57:52 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 02 Aug 2021 19:48:08 GMT
ENV PYTHON_PIP_VERSION=21.2.2
# Mon, 02 Aug 2021 19:48:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a1675ab6c2bd898ed82b1f58c486097f763c74a9/public/get-pip.py
# Mon, 02 Aug 2021 19:48:08 GMT
ENV PYTHON_GET_PIP_SHA256=6665659241292b2147b58922b9ffe11dda66b39d52d8a6f3aa310bc1d60ea6f7
# Mon, 02 Aug 2021 19:48:21 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 02 Aug 2021 19:48:21 GMT
CMD ["python3"]
# Mon, 02 Aug 2021 20:18:54 GMT
ENV HY_VERSION=1.0a3
# Mon, 02 Aug 2021 20:18:58 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Mon, 02 Aug 2021 20:18:58 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:513c6babab2b9079da61a69300c0e26d1037ca98910376098e9ae87baeb112c0`  
		Last Modified: Thu, 22 Jul 2021 00:45:53 GMT  
		Size: 25.9 MB (25914794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb026ab86bfde63d2e93f1781974de6d6e29967ae8f8452c37895255d415228`  
		Last Modified: Thu, 22 Jul 2021 12:08:24 GMT  
		Size: 2.6 MB (2635781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2221f4b81546ae8552ef943e76f3d7c85a76a49cfef2cb08fada630df2fefbfa`  
		Last Modified: Thu, 22 Jul 2021 12:09:21 GMT  
		Size: 10.9 MB (10945902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebda1cac0449441af4ba0a1f2bf4ec564e3706c0f40e0dda56812619e97629d`  
		Last Modified: Thu, 22 Jul 2021 12:09:19 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746b3740f61fc7433ea72c20f89af6e2bee9e43cd8a9caab3597779b16ca5cdd`  
		Last Modified: Mon, 02 Aug 2021 19:58:00 GMT  
		Size: 2.6 MB (2644205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f909947611a76b04f6201257d5ec48b09f8807b4e6bb0742d88eb49cde4dbc7`  
		Last Modified: Mon, 02 Aug 2021 20:24:29 GMT  
		Size: 3.1 MB (3093979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-buster` - linux; 386

```console
$ docker pull hylang@sha256:3bc4a653106dcfc21c7da58fa042c4d4421df5ed49079df89f91017fba6f9e00
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47393904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8daeb2003cba2b887033f506142c10eb6219fca56ed2bc8a4bd547a8f280cd74`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:50 GMT
ADD file:cb657a3d01f25bf815677ce223e8802d054f11aeb95f85b160982277916637bd in / 
# Thu, 22 Jul 2021 00:39:51 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 13:00:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 13:00:21 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 13:00:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 13:28:32 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 22 Jul 2021 13:28:32 GMT
ENV PYTHON_VERSION=3.9.6
# Thu, 22 Jul 2021 13:39:32 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Thu, 22 Jul 2021 13:39:34 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 02 Aug 2021 19:46:23 GMT
ENV PYTHON_PIP_VERSION=21.2.2
# Mon, 02 Aug 2021 19:46:23 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a1675ab6c2bd898ed82b1f58c486097f763c74a9/public/get-pip.py
# Mon, 02 Aug 2021 19:46:23 GMT
ENV PYTHON_GET_PIP_SHA256=6665659241292b2147b58922b9ffe11dda66b39d52d8a6f3aa310bc1d60ea6f7
# Mon, 02 Aug 2021 19:46:37 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 02 Aug 2021 19:46:37 GMT
CMD ["python3"]
# Mon, 02 Aug 2021 20:18:16 GMT
ENV HY_VERSION=1.0a3
# Mon, 02 Aug 2021 20:18:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Mon, 02 Aug 2021 20:18:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:fa9d06db5f4195bd51665a89e08e2e7db25636ac28ab162fe876ae0a53093fe5`  
		Last Modified: Thu, 22 Jul 2021 00:46:36 GMT  
		Size: 27.8 MB (27797459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fc0ce2f007e7c0470501e9ca112bb34d54938816bbf73cfb9cda09a164d548`  
		Last Modified: Thu, 22 Jul 2021 15:17:35 GMT  
		Size: 2.8 MB (2780804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503c15da1c23c081e737e4fd77ba5ad66ebcd7f47c7077b27c63eae6c1575370`  
		Last Modified: Thu, 22 Jul 2021 15:18:45 GMT  
		Size: 11.1 MB (11077093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f7976373f9cc37535f2f9ffb3e88b695be7b9045dde5f772b9457efece1ddb`  
		Last Modified: Thu, 22 Jul 2021 15:18:43 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf3d8ceea1f59af513be2230101390fbfd0f556c1fbbffbacc922e7f62e384e`  
		Last Modified: Mon, 02 Aug 2021 19:57:10 GMT  
		Size: 2.6 MB (2644174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04099fe85a605cfcba70c5f91fbb579408397d1d936c71c73b081ae80459e0a`  
		Last Modified: Mon, 02 Aug 2021 20:24:16 GMT  
		Size: 3.1 MB (3094142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-buster` - linux; mips64le

```console
$ docker pull hylang@sha256:33146ae4380656955431873a975612d06c9fcbea5d0dba8120995d5285dbb65c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44702357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4baa360990d8214f1cf874d197fc3a30b93175cb2109e337c5aa6d3128b2f71`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 22 Jul 2021 00:09:45 GMT
ADD file:1f77b9001c4977ba733be674fc5eb4b85130f1dea8a7b39d545b70f9c107695f in / 
# Thu, 22 Jul 2021 00:09:46 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 10:49:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 10:49:39 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 10:49:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 12:16:02 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 22 Jul 2021 12:16:02 GMT
ENV PYTHON_VERSION=3.9.6
# Thu, 22 Jul 2021 12:58:17 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Thu, 22 Jul 2021 12:58:18 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 06 Aug 2021 19:11:02 GMT
ENV PYTHON_PIP_VERSION=21.2.3
# Fri, 06 Aug 2021 19:11:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c20b0cfd643cd4a19246ccf204e2997af70f6b21/public/get-pip.py
# Fri, 06 Aug 2021 19:11:02 GMT
ENV PYTHON_GET_PIP_SHA256=fa6f3fb93cce234cd4e8dd2beb54a51ab9c247653b52855a48dd44e6b21ff28b
# Fri, 06 Aug 2021 19:11:46 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 06 Aug 2021 19:11:47 GMT
CMD ["python3"]
# Fri, 06 Aug 2021 19:34:58 GMT
ENV HY_VERSION=1.0a3
# Fri, 06 Aug 2021 19:35:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 06 Aug 2021 19:35:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:99ee621d0b0485e9de65aa19604aa2453d19ea7fc86b22c5b77c1bab74e3cb42`  
		Last Modified: Thu, 22 Jul 2021 00:16:11 GMT  
		Size: 25.8 MB (25812771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc33a9b4255d04a4bdb2ff9117ff657e1446dbbf7e1bf065fc0961fa1892b793`  
		Last Modified: Thu, 22 Jul 2021 16:41:49 GMT  
		Size: 2.3 MB (2321157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f702a3d7a4de7502384d7c2b9182d085fad364861cd10a7ba2f6c581a73feccc`  
		Last Modified: Thu, 22 Jul 2021 16:42:54 GMT  
		Size: 10.8 MB (10830282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add03a3a923d39cdf73b46a671bcd7ac3a1367ca9773e7c5f5946f9c93c990d2`  
		Last Modified: Thu, 22 Jul 2021 16:42:46 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c211bbe72c67ac41095b8499e841c882df5f0a6c558f995b24724e77b1c56c`  
		Last Modified: Fri, 06 Aug 2021 19:17:16 GMT  
		Size: 2.6 MB (2642803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b07e40d2d2c4058feff973e2d2ca3ae8bb39ec6b7c11b657a84bcd786666394`  
		Last Modified: Fri, 06 Aug 2021 19:37:10 GMT  
		Size: 3.1 MB (3095110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-buster` - linux; ppc64le

```console
$ docker pull hylang@sha256:75b0f91cd62598d1f15bc8fc1c2d1ef5a5f4423c0f6f91571ad6f5787da5d7a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50942286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121ebfa77e6bcc09b23a603616d7446010c24d1f91ce6150f3422119a4829040`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 22 Jul 2021 00:19:04 GMT
ADD file:3a6bd6ce3eff98b88a13de5d0f26cff0b026f876674204dbad6f84fafcf145b1 in / 
# Thu, 22 Jul 2021 00:19:13 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 17:59:32 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 17:59:41 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 18:01:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 18:42:00 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 22 Jul 2021 18:42:02 GMT
ENV PYTHON_VERSION=3.9.6
# Thu, 22 Jul 2021 18:58:55 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Thu, 22 Jul 2021 18:59:06 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 02 Aug 2021 19:34:53 GMT
ENV PYTHON_PIP_VERSION=21.2.2
# Mon, 02 Aug 2021 19:34:56 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a1675ab6c2bd898ed82b1f58c486097f763c74a9/public/get-pip.py
# Mon, 02 Aug 2021 19:35:00 GMT
ENV PYTHON_GET_PIP_SHA256=6665659241292b2147b58922b9ffe11dda66b39d52d8a6f3aa310bc1d60ea6f7
# Mon, 02 Aug 2021 19:36:02 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 02 Aug 2021 19:36:13 GMT
CMD ["python3"]
# Mon, 02 Aug 2021 20:16:57 GMT
ENV HY_VERSION=1.0a3
# Mon, 02 Aug 2021 20:17:29 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Mon, 02 Aug 2021 20:17:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1130517d52da84a09f9465006bddab5e49afd398860890eab6274fd0bff32371`  
		Last Modified: Thu, 22 Jul 2021 00:27:49 GMT  
		Size: 30.6 MB (30553709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b045079c902caed53719113abce25d038439c592302f28f5d77fc93a85b2579`  
		Last Modified: Thu, 22 Jul 2021 21:38:26 GMT  
		Size: 2.9 MB (2887078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623c76baa89af8d81e05511127b28a335856914de2a34cb67121b868b7b06fd3`  
		Last Modified: Thu, 22 Jul 2021 21:39:45 GMT  
		Size: 11.8 MB (11761064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c85568e9a9cf77c557244f94ca56e95cfe66dc874c9c45f10464e80f904e052`  
		Last Modified: Thu, 22 Jul 2021 21:39:43 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e648a9664e080f1ce3181db70aaa3e4d3883b28a3e4221d4a2a2ed9bfbe051`  
		Last Modified: Mon, 02 Aug 2021 19:56:45 GMT  
		Size: 2.6 MB (2645861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc1d3c3b7dd9d7daf2b79defeb27269c1c228c576cf38267f547c322f25b354`  
		Last Modified: Mon, 02 Aug 2021 20:29:24 GMT  
		Size: 3.1 MB (3094342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-buster` - linux; s390x

```console
$ docker pull hylang@sha256:bf40ff602a39e425c65704ee1ecc9f0bd47cccf128622ea1b530b1e5a0495aa7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44752687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e55b25c4a745826c2c9102ae0b109638c1e2930f36e893e8df66090f655a09`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 22 Jul 2021 00:42:45 GMT
ADD file:1ab999eb6f80d8ce91ce3a173e23fd2710f2779117bba29037eaa82aadcbf6ed in / 
# Thu, 22 Jul 2021 00:42:48 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 12:00:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 12:00:34 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 12:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 12:33:16 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 22 Jul 2021 12:33:17 GMT
ENV PYTHON_VERSION=3.9.6
# Thu, 22 Jul 2021 12:45:02 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Thu, 22 Jul 2021 12:45:06 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 02 Aug 2021 19:52:41 GMT
ENV PYTHON_PIP_VERSION=21.2.2
# Mon, 02 Aug 2021 19:52:41 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a1675ab6c2bd898ed82b1f58c486097f763c74a9/public/get-pip.py
# Mon, 02 Aug 2021 19:52:41 GMT
ENV PYTHON_GET_PIP_SHA256=6665659241292b2147b58922b9ffe11dda66b39d52d8a6f3aa310bc1d60ea6f7
# Mon, 02 Aug 2021 19:52:58 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 02 Aug 2021 19:52:59 GMT
CMD ["python3"]
# Mon, 02 Aug 2021 20:31:18 GMT
ENV HY_VERSION=1.0a3
# Mon, 02 Aug 2021 20:31:24 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Mon, 02 Aug 2021 20:31:25 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7a50fdd85ff244c1465e71c51354d055e3df0b90ff5faad28cc22d9ecde9daf3`  
		Last Modified: Thu, 22 Jul 2021 00:48:13 GMT  
		Size: 25.8 MB (25760761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7190142e37353d1d80058553543df522b7d70624d58b147c8472aa6d2ef4077e`  
		Last Modified: Thu, 22 Jul 2021 13:55:33 GMT  
		Size: 2.5 MB (2458990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff247dec74f70ae19da010df0193356f91c62ed0e3c50c81601c5fe9b82d3b8`  
		Last Modified: Thu, 22 Jul 2021 13:56:13 GMT  
		Size: 10.8 MB (10794209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e827b07d89da5d68c75fd0293a9ba01a81aac1ea5f6c550b56c7e87d5a7ff2`  
		Last Modified: Thu, 22 Jul 2021 13:56:11 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749cd7b84a895ca251a5f4a2e2aa7b328bf7c3dc3c8aef73c0f0d711ca53a7e6`  
		Last Modified: Mon, 02 Aug 2021 20:13:03 GMT  
		Size: 2.6 MB (2644391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50689885e153eadb0c23973d47e0ad4d9b378f18156d19ab17dcd3d4e060360b`  
		Last Modified: Mon, 02 Aug 2021 20:35:31 GMT  
		Size: 3.1 MB (3094098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
