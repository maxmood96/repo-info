## `hylang:python3.8`

```console
$ docker pull hylang@sha256:9ad9710269e98a8356b8c55533739ef825af8bc2345299b71f62ee2a2f775ffd
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
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `hylang:python3.8` - linux; amd64

```console
$ docker pull hylang@sha256:e8f15a395891cbd3bb068c8e902bf1c11a2d90dbee6f11024ebaa733207cc315
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46249221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea8dbe611c9e07c18f283b2b7aa67eea0841139bcb18f38ffdd34410832bca4`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 15:15:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 15:15:47 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 15:48:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 15:48:31 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 10 Apr 2021 15:48:31 GMT
ENV PYTHON_VERSION=3.8.9
# Sat, 10 Apr 2021 15:56:01 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Sat, 10 Apr 2021 15:56:02 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 27 Apr 2021 22:52:37 GMT
ENV PYTHON_PIP_VERSION=21.1
# Tue, 27 Apr 2021 22:52:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ab9dde151f662745c13461f00c453dcf32a51ea9/public/get-pip.py
# Tue, 27 Apr 2021 22:52:37 GMT
ENV PYTHON_GET_PIP_SHA256=0ed17e859b835ad5bf00851f4dc8bbc3520c13dfff6c131d410cdb3a92ff0af9
# Tue, 27 Apr 2021 22:52:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 27 Apr 2021 22:52:49 GMT
CMD ["python3"]
# Tue, 27 Apr 2021 23:21:55 GMT
ENV HY_VERSION=1.0a1
# Tue, 27 Apr 2021 23:21:59 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Tue, 27 Apr 2021 23:21:59 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f318b7b4c32e5bbdcf826cefc687951e49af93c21b726f1ac537d6a74f86aa5`  
		Last Modified: Sat, 10 Apr 2021 16:56:06 GMT  
		Size: 2.8 MB (2769589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be07e2a755b449f878b2df8f385d1f2df981db4443de655ed5eb4936f47d0c`  
		Last Modified: Sat, 10 Apr 2021 16:56:07 GMT  
		Size: 10.7 MB (10690574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843bb564d1d08cefc14ec28a27e4cdd6b02c3f9d3f5cab64cf3b32d3cbf8062`  
		Last Modified: Sat, 10 Apr 2021 16:56:05 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e842f4dd41ec38705cc409a22f168b996966ee738c3dbc5b32f53fff87bb8f91`  
		Last Modified: Tue, 27 Apr 2021 23:00:11 GMT  
		Size: 2.6 MB (2599596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64174db3c245c22eeda11772688b128c44f9b8d02e615400aeb2fec5b83cc38`  
		Last Modified: Tue, 27 Apr 2021 23:26:17 GMT  
		Size: 3.0 MB (3049856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8` - linux; arm variant v5

```console
$ docker pull hylang@sha256:cc8f1e08b4cb46d696345595a0a9b8f0e476a3dde068f0edc8b83fd223f95da0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43335143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28250ce002122c48f0817d4b44ff0a6d159bcd7559fe1eca9fb21c5ea52d1225`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 10 Apr 2021 00:51:31 GMT
ADD file:926533a23a69aa2481a9122b667bb6300a347154eea366c9e679a230aa7f373a in / 
# Sat, 10 Apr 2021 00:51:34 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 08:27:46 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 08:27:47 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 09:22:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 09:22:19 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 10 Apr 2021 09:22:19 GMT
ENV PYTHON_VERSION=3.8.9
# Sat, 10 Apr 2021 09:34:57 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Sat, 10 Apr 2021 09:34:59 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 27 Apr 2021 23:36:36 GMT
ENV PYTHON_PIP_VERSION=21.1
# Tue, 27 Apr 2021 23:36:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ab9dde151f662745c13461f00c453dcf32a51ea9/public/get-pip.py
# Tue, 27 Apr 2021 23:36:38 GMT
ENV PYTHON_GET_PIP_SHA256=0ed17e859b835ad5bf00851f4dc8bbc3520c13dfff6c131d410cdb3a92ff0af9
# Tue, 27 Apr 2021 23:37:13 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 27 Apr 2021 23:37:14 GMT
CMD ["python3"]
# Wed, 28 Apr 2021 00:34:13 GMT
ENV HY_VERSION=1.0a1
# Wed, 28 Apr 2021 00:34:25 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 28 Apr 2021 00:34:26 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:33d77752597b664d047cc829e58a223d6fb077b61f69ca0462fcfb9b78d5f69b`  
		Last Modified: Sat, 10 Apr 2021 00:59:22 GMT  
		Size: 24.9 MB (24873199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1c506219953715a8e935e6f6e8569d33b4837fedb6bcdc29ecb972b5e9b172`  
		Last Modified: Sat, 10 Apr 2021 11:03:20 GMT  
		Size: 2.5 MB (2460001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ad7ede0590b6b46b7a7021bddfe2b5bba0980e6d51576e1edea972b838b9df`  
		Last Modified: Sat, 10 Apr 2021 11:03:22 GMT  
		Size: 10.4 MB (10352185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a19d6c30e54565b2e5aabeb65280697748eba19fabb1970a87c25db1fc41aa`  
		Last Modified: Sat, 10 Apr 2021 11:03:19 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9846624278bd311e5944248f582ceb6e7cd3d568b11feee0acdce2bd8b71824`  
		Last Modified: Tue, 27 Apr 2021 23:45:17 GMT  
		Size: 2.6 MB (2599384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31f3970af6531e66ac87506bd26798a5ac83845cb5f77521483c8c7952390dd`  
		Last Modified: Wed, 28 Apr 2021 00:37:18 GMT  
		Size: 3.1 MB (3050141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8` - linux; arm variant v7

```console
$ docker pull hylang@sha256:63b8971dd8de99b501f6459df751506ff1a2797ae48be7c830a57d9f55d079f5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40643542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6407086f8c803b99808a6fb6aa69dbb1a335bce05f6cc044f758d28e03eaa2d1`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 10 Apr 2021 00:59:45 GMT
ADD file:3fbd246a2de82566bcaaf62e3e0bf57175a7ad46b4156366a110661b31eab240 in / 
# Sat, 10 Apr 2021 00:59:47 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 04:20:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 04:20:41 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 04:51:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 04:51:19 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 10 Apr 2021 04:51:20 GMT
ENV PYTHON_VERSION=3.8.9
# Sat, 10 Apr 2021 05:04:13 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Sat, 10 Apr 2021 05:04:17 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 27 Apr 2021 23:15:44 GMT
ENV PYTHON_PIP_VERSION=21.1
# Tue, 27 Apr 2021 23:15:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ab9dde151f662745c13461f00c453dcf32a51ea9/public/get-pip.py
# Tue, 27 Apr 2021 23:15:46 GMT
ENV PYTHON_GET_PIP_SHA256=0ed17e859b835ad5bf00851f4dc8bbc3520c13dfff6c131d410cdb3a92ff0af9
# Tue, 27 Apr 2021 23:16:14 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 27 Apr 2021 23:16:16 GMT
CMD ["python3"]
# Wed, 28 Apr 2021 00:36:06 GMT
ENV HY_VERSION=1.0a1
# Wed, 28 Apr 2021 00:36:20 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 28 Apr 2021 00:36:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8c6bea184b33030fb923c3c09d634b73235dec3fe2d411db9fd22bda669f2c37`  
		Last Modified: Sat, 10 Apr 2021 01:07:51 GMT  
		Size: 22.7 MB (22739801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8643010f86fdab40a765293a0fecad0799df55d0fae94c8e802b365529acfadb`  
		Last Modified: Sat, 10 Apr 2021 05:59:25 GMT  
		Size: 2.4 MB (2358477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcde71c807d675c9238d92204d3d5a253994b561f713de94f94b1c1233914dd`  
		Last Modified: Sat, 10 Apr 2021 05:59:25 GMT  
		Size: 9.9 MB (9895520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91d47f8bb9090718ee9fe7b042b605cc97f881844be11b0692e06098447b639`  
		Last Modified: Sat, 10 Apr 2021 05:59:25 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48f9c80ef44da1794c2ea3b9f1cc8f08784924cb8510016fec7899071a615e5`  
		Last Modified: Tue, 27 Apr 2021 23:28:16 GMT  
		Size: 2.6 MB (2599416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3647dd448fbb7714eac2c7ce735e7a4f7294ccc7cb717a36ac66c52363a71279`  
		Last Modified: Wed, 28 Apr 2021 00:43:24 GMT  
		Size: 3.1 MB (3050096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:52655a394b1e4e419b68d788204014073490e7884450ecf1544a43053631c661
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44888497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba037af2b87f7ffa14611b89e849e4d74e8bd067fc5c90466b315fb6d3f9fc9`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 10 Apr 2021 00:41:25 GMT
ADD file:b24da7eb23eeae04e00d0e45da29a89fe8f992e8dcf4ba482afb907b8015b7bf in / 
# Sat, 10 Apr 2021 00:41:28 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:43:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 12:43:25 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 13:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 13:26:30 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 10 Apr 2021 13:26:31 GMT
ENV PYTHON_VERSION=3.8.9
# Sat, 10 Apr 2021 13:35:57 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Sat, 10 Apr 2021 13:36:01 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 27 Apr 2021 23:24:49 GMT
ENV PYTHON_PIP_VERSION=21.1
# Tue, 27 Apr 2021 23:24:50 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ab9dde151f662745c13461f00c453dcf32a51ea9/public/get-pip.py
# Tue, 27 Apr 2021 23:24:51 GMT
ENV PYTHON_GET_PIP_SHA256=0ed17e859b835ad5bf00851f4dc8bbc3520c13dfff6c131d410cdb3a92ff0af9
# Tue, 27 Apr 2021 23:25:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 27 Apr 2021 23:25:20 GMT
CMD ["python3"]
# Wed, 28 Apr 2021 00:06:57 GMT
ENV HY_VERSION=1.0a1
# Wed, 28 Apr 2021 00:07:11 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 28 Apr 2021 00:07:13 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:15cb40b9c4df1a06940dc2a154c3be46844241235c1a091afa70da0ee2dc811a`  
		Last Modified: Sat, 10 Apr 2021 00:47:53 GMT  
		Size: 25.9 MB (25904582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46fe17cb17c755ffac31e35a20eed681d6eee2901bcd029d1afb8d84229b4ebf`  
		Last Modified: Sat, 10 Apr 2021 15:10:00 GMT  
		Size: 2.6 MB (2635830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9cc796a80e7fa792ae212385163b0e3c922a1f3a68ddc1031084778d962802`  
		Last Modified: Sat, 10 Apr 2021 15:10:02 GMT  
		Size: 10.7 MB (10698048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667acad7082a3f1f6093cd7bf1f99de88305fd29d844ccd86609b12bb4dabe5b`  
		Last Modified: Sat, 10 Apr 2021 15:09:59 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916119f4302dfeebfbeb17984bd7f30820fe603ad346b8a2d607c0394c73c817`  
		Last Modified: Tue, 27 Apr 2021 23:38:14 GMT  
		Size: 2.6 MB (2599777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd94972f8ca5b149e5a232f4873dccb3491a93d9387593abb6255b8221eff34a`  
		Last Modified: Wed, 28 Apr 2021 00:14:27 GMT  
		Size: 3.1 MB (3050029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8` - linux; 386

```console
$ docker pull hylang@sha256:f54ed38fda22b082a1360547a34783a6b85183fab5ff3bb70fdfab9f7a6cc732
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47018483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94aedcd771135f45c76a480b3123e5df7bb6c8c73bae97aff7e0074c4a254fc9`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 10 Apr 2021 00:39:42 GMT
ADD file:8885d4d13678543780bb04ba14b621179665f7951d5b261036a7092df9b376e7 in / 
# Sat, 10 Apr 2021 00:39:43 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:14:28 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 01:14:28 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 01:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:37:12 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 10 Apr 2021 01:37:12 GMT
ENV PYTHON_VERSION=3.8.9
# Sat, 10 Apr 2021 01:46:46 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Sat, 10 Apr 2021 01:46:47 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 27 Apr 2021 22:45:50 GMT
ENV PYTHON_PIP_VERSION=21.1
# Tue, 27 Apr 2021 22:45:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ab9dde151f662745c13461f00c453dcf32a51ea9/public/get-pip.py
# Tue, 27 Apr 2021 22:45:51 GMT
ENV PYTHON_GET_PIP_SHA256=0ed17e859b835ad5bf00851f4dc8bbc3520c13dfff6c131d410cdb3a92ff0af9
# Tue, 27 Apr 2021 22:46:04 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 27 Apr 2021 22:46:05 GMT
CMD ["python3"]
# Tue, 27 Apr 2021 23:23:16 GMT
ENV HY_VERSION=1.0a1
# Tue, 27 Apr 2021 23:23:21 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Tue, 27 Apr 2021 23:23:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7cc57a8772e5e479618650dfa70f315b474d3f205d04bde7f602f469c1928d84`  
		Last Modified: Sat, 10 Apr 2021 00:46:07 GMT  
		Size: 27.8 MB (27788987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aceca6ccb88045694c2d380c9aed499d0b64604e99ccb7b28267aaeaae87779`  
		Last Modified: Sat, 10 Apr 2021 02:35:09 GMT  
		Size: 2.8 MB (2780825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3005c3bf706495a40881038cbd2e183504f5e8db60e635a3d46a06345e4455fb`  
		Last Modified: Sat, 10 Apr 2021 02:35:12 GMT  
		Size: 10.8 MB (10799264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768e5dab9937ffecc71e49555844804a9005a361509683c278675a668cf65901`  
		Last Modified: Sat, 10 Apr 2021 02:35:07 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad67b56ae41f59f41a23f33ad9528b2468fc17dba023bd26b9434b8b103479f3`  
		Last Modified: Tue, 27 Apr 2021 22:56:55 GMT  
		Size: 2.6 MB (2599323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4310329a179be6ef3018a1e6f35bdce491bf1cfabb43a99d900a6e785f5434`  
		Last Modified: Tue, 27 Apr 2021 23:29:45 GMT  
		Size: 3.0 MB (3049851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8` - linux; mips64le

```console
$ docker pull hylang@sha256:50fdde164f301e00f48b1e4379ba90e732e28a11f641adc4e1b430be3031d8c7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44065912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007e1803a65821fde8f816500ff8c09223b705c5719e6ed50f2f553b994b00c8`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 10 Apr 2021 01:09:40 GMT
ADD file:0c93801c4a3719dfd4c047d7f2f4d52bf463eba2ab875da1dc54dcc832aae20b in / 
# Sat, 10 Apr 2021 01:09:41 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 06:44:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 06:44:39 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 09:33:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 09:33:42 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 10 Apr 2021 09:33:43 GMT
ENV PYTHON_VERSION=3.8.9
# Sat, 10 Apr 2021 10:13:49 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Sat, 10 Apr 2021 10:13:50 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 10 Apr 2021 10:13:50 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Sat, 10 Apr 2021 10:13:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/29f37dbe6b3842ccd52d61816a3044173962ebeb/public/get-pip.py
# Sat, 10 Apr 2021 10:13:51 GMT
ENV PYTHON_GET_PIP_SHA256=e03eb8a33d3b441ff484c56a436ff10680479d4bd14e59268e67977ed40904de
# Sat, 10 Apr 2021 10:14:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 10 Apr 2021 10:14:30 GMT
CMD ["python3"]
# Tue, 20 Apr 2021 01:07:52 GMT
ENV HY_VERSION=1.0a1
# Tue, 20 Apr 2021 01:08:07 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Tue, 20 Apr 2021 01:08:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:09ea659ba566d9c3c62493e5ae0b964f1eee4fcf35aabc91c5c34ca1ad686541`  
		Last Modified: Sat, 10 Apr 2021 01:16:07 GMT  
		Size: 25.8 MB (25806410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58d1409df56f046dd83c9b1d8b65ad14f8c8fdfa2978d085734fc6fe4ad68a3`  
		Last Modified: Sat, 10 Apr 2021 12:38:01 GMT  
		Size: 2.3 MB (2321189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e935d83e0305d26afd08a8728a63104a9d2894b1ae10d620295a8ae7b1a3bf1c`  
		Last Modified: Sat, 10 Apr 2021 12:38:06 GMT  
		Size: 10.6 MB (10579379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4046c2eec0d0711de1335fedb1eddd9cf849e3e913216a0da7ff32a0b9c6264d`  
		Last Modified: Sat, 10 Apr 2021 12:37:59 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf399b34b15bfd77797a96f61322f359ff4fdbd50237c79cb0e6e45b813f1e9`  
		Last Modified: Sat, 10 Apr 2021 12:38:01 GMT  
		Size: 2.5 MB (2452595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef33021cc2f3e0a073b7993a6b051724fed64b24923dfda10b127c76b794abc`  
		Last Modified: Tue, 20 Apr 2021 01:09:50 GMT  
		Size: 2.9 MB (2906105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8` - linux; ppc64le

```console
$ docker pull hylang@sha256:bf03f729aa1a7aa7a42e3377228197e1579c4f062700891f3f6b6662f85cb50e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50560843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94fc9075ce598aa0f7168d5a221bea89d6596070575dce3c8f62d87287158370`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 10 Apr 2021 01:26:49 GMT
ADD file:ab87d4854aa8628ce8f4e603c0496499f6f28c3d2525ace782c7369691dafc8c in / 
# Sat, 10 Apr 2021 01:26:56 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 10:13:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 10:13:57 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 11:09:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 11:09:59 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 10 Apr 2021 11:10:05 GMT
ENV PYTHON_VERSION=3.8.9
# Sat, 10 Apr 2021 11:25:14 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Sat, 10 Apr 2021 11:25:27 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 28 Apr 2021 01:12:07 GMT
ENV PYTHON_PIP_VERSION=21.1
# Wed, 28 Apr 2021 01:12:17 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ab9dde151f662745c13461f00c453dcf32a51ea9/public/get-pip.py
# Wed, 28 Apr 2021 01:12:26 GMT
ENV PYTHON_GET_PIP_SHA256=0ed17e859b835ad5bf00851f4dc8bbc3520c13dfff6c131d410cdb3a92ff0af9
# Wed, 28 Apr 2021 01:13:41 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 28 Apr 2021 01:13:49 GMT
CMD ["python3"]
# Wed, 28 Apr 2021 02:29:37 GMT
ENV HY_VERSION=1.0a1
# Wed, 28 Apr 2021 02:30:07 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 28 Apr 2021 02:30:11 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3e1e599482ca47095f85e429b346b76375aa85015ddcca050e85c2a8b1fdda9c`  
		Last Modified: Sat, 10 Apr 2021 01:33:57 GMT  
		Size: 30.5 MB (30545933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b164c7f78fd59bf9c44751553c193fb3dc328725c71c8622ac771b36f6728be`  
		Last Modified: Sat, 10 Apr 2021 12:49:17 GMT  
		Size: 2.9 MB (2886962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfce385af4d24543914f2f38b686a5334166544b7b1f2e516edaaa009e2ce46d`  
		Last Modified: Sat, 10 Apr 2021 12:49:18 GMT  
		Size: 11.5 MB (11476028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4a9730b3c4801934b9b268a9a5ced5c68738d7bd433ebc9e37d27a54fd93bf`  
		Last Modified: Sat, 10 Apr 2021 12:49:18 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80a8e80e91afcad1951e9ed19cc39e419cb23fd4a1943c51167241f7d8895c1`  
		Last Modified: Wed, 28 Apr 2021 01:33:45 GMT  
		Size: 2.6 MB (2601207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fdaecbcfe42f1f8a0219939ade75167ec5adf40708aa327bb6b35be1a19e6e7`  
		Last Modified: Wed, 28 Apr 2021 02:43:15 GMT  
		Size: 3.1 MB (3050479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8` - linux; s390x

```console
$ docker pull hylang@sha256:0f932489c9fee6d986c8ab7b9d2b10402d5dfa9f82a84cc90700e8cc43f6232c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44394509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a128581e7ff33772d19a670b1d352524181c6be2878c3fa5539f038ff976f39a`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 10 Apr 2021 00:42:23 GMT
ADD file:dbe2182f8699f2a6011413ea01862e6c0e85853d922dffd72a28d994d23c79bc in / 
# Sat, 10 Apr 2021 00:42:25 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 05:01:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 05:01:21 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 05:25:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 05:25:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 10 Apr 2021 05:25:06 GMT
ENV PYTHON_VERSION=3.8.9
# Sat, 10 Apr 2021 05:30:13 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Sat, 10 Apr 2021 05:30:15 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 27 Apr 2021 23:18:03 GMT
ENV PYTHON_PIP_VERSION=21.1
# Tue, 27 Apr 2021 23:18:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ab9dde151f662745c13461f00c453dcf32a51ea9/public/get-pip.py
# Tue, 27 Apr 2021 23:18:04 GMT
ENV PYTHON_GET_PIP_SHA256=0ed17e859b835ad5bf00851f4dc8bbc3520c13dfff6c131d410cdb3a92ff0af9
# Tue, 27 Apr 2021 23:18:20 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 27 Apr 2021 23:18:21 GMT
CMD ["python3"]
# Tue, 27 Apr 2021 23:49:52 GMT
ENV HY_VERSION=1.0a1
# Tue, 27 Apr 2021 23:49:57 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Tue, 27 Apr 2021 23:49:58 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:65291f8717b3afd99b63cee867dd3e06b956a8ee6aa8580cc31d913b25de209d`  
		Last Modified: Sat, 10 Apr 2021 00:45:48 GMT  
		Size: 25.8 MB (25753787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd52de107b9bb95e9d6cf86a39e463aa4547fb101d940011fcddcfa1c061ddab`  
		Last Modified: Sat, 10 Apr 2021 05:53:22 GMT  
		Size: 2.5 MB (2459023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf700e483f26c4a148cc4dc48b0bb0b54e71a95a15d068a9d47d3d7e76dddc3`  
		Last Modified: Sat, 10 Apr 2021 05:53:23 GMT  
		Size: 10.5 MB (10532553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cff1f8128d590d756cae539e6d936ff405a292dd3d2cbd1e0ad232567debbc6`  
		Last Modified: Sat, 10 Apr 2021 05:53:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a318f7a363265d8e363092f41656988a34340d55b29647fb8c80d55d4131b3`  
		Last Modified: Tue, 27 Apr 2021 23:25:04 GMT  
		Size: 2.6 MB (2599129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa38795e4a86a804d9d5d8ca232b20a0a5fa13d4eefd0f8c18c2d486b129426`  
		Last Modified: Tue, 27 Apr 2021 23:53:55 GMT  
		Size: 3.0 MB (3049784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8` - windows version 10.0.17763.1879; amd64

```console
$ docker pull hylang@sha256:2adb99b54c702c34144c7742468ff841fa5d225b63fad45905168ea6d7f6c912
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2530786655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2fdc2c5640980628c5668a087ad48d7bc6a09c775bae300a47f2a2bde33574`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:14:23 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 14 Apr 2021 16:29:02 GMT
ENV PYTHON_VERSION=3.8.9
# Wed, 14 Apr 2021 16:29:04 GMT
ENV PYTHON_RELEASE=3.8.9
# Wed, 14 Apr 2021 16:30:59 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Tue, 27 Apr 2021 22:20:37 GMT
ENV PYTHON_PIP_VERSION=21.1
# Tue, 27 Apr 2021 22:20:38 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ab9dde151f662745c13461f00c453dcf32a51ea9/public/get-pip.py
# Tue, 27 Apr 2021 22:20:39 GMT
ENV PYTHON_GET_PIP_SHA256=0ed17e859b835ad5bf00851f4dc8bbc3520c13dfff6c131d410cdb3a92ff0af9
# Tue, 27 Apr 2021 22:21:24 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 27 Apr 2021 22:21:25 GMT
CMD ["python"]
# Tue, 27 Apr 2021 22:46:33 GMT
ENV HY_VERSION=1.0a1
# Tue, 27 Apr 2021 22:47:12 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Tue, 27 Apr 2021 22:47:13 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc61c4265bfe314fb772d57da4c3023d46cacdbdab9bb6fd5c475f11696dbab`  
		Last Modified: Wed, 14 Apr 2021 16:38:19 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6baabbe0a83d9983f3d3ef4c7a4052a8fd2bb38455f79e5367b7cdbd00c48a7c`  
		Last Modified: Wed, 14 Apr 2021 16:42:06 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669587e3d363485920eae92832523f99fb5ea29c99b8741ff96a6e8ab1d0c944`  
		Last Modified: Wed, 14 Apr 2021 16:42:06 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9c258f44937650d65ac4d44fb937e4bdd806421c907526ec22be710e6afc1c`  
		Last Modified: Wed, 14 Apr 2021 16:42:20 GMT  
		Size: 53.6 MB (53610284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:face02a0bd2affe599eeb5f34d5bad7c37b922fd33b6289ff474c1aceee05b26`  
		Last Modified: Tue, 27 Apr 2021 22:26:09 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe19fdc98b54b66fd8c591617e023e5c63e0ebc044bdc573376cc7654c247aa`  
		Last Modified: Tue, 27 Apr 2021 22:26:09 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecc2145f2557f1b4051ba762d0263b29058442f53409f1b641d77a10dc8702c`  
		Last Modified: Tue, 27 Apr 2021 22:26:09 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b5f8792f8f754d0fc38781d09f1cba88d7c55b099de5f9132f41b81c369df2`  
		Last Modified: Tue, 27 Apr 2021 22:26:16 GMT  
		Size: 6.2 MB (6191388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57291eeae00a5b1d69a012a03ba9c9df1cfcb378b7d1a53f77716234a587b9e8`  
		Last Modified: Tue, 27 Apr 2021 22:26:09 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dbc4114aaa0983dada0bc1bfac01b44c0a7c54addb34f314a3c55657d76085`  
		Last Modified: Wed, 28 Apr 2021 12:05:12 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0c998f48a6a8ac1428944dc0641f547ff95602b007a8d788a6d92cd5a08da9`  
		Last Modified: Wed, 28 Apr 2021 12:05:14 GMT  
		Size: 1.2 MB (1217116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4342a19e5611db55b13924dfc55606ee8f552793611ee8b4999241bd0c5677e`  
		Last Modified: Wed, 28 Apr 2021 12:05:11 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.8` - windows version 10.0.14393.4350; amd64

```console
$ docker pull hylang@sha256:97430e2098f1be76d8dfeb6186a9a1aaa3b8a425a0988bf6e744d4fe44d19d7c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5871427942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f97ab9f89bbfa4181b0cb9fb60852ea0eafe5be0703d04db56909d2c68629e4`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 16:15:18 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 14 Apr 2021 16:32:16 GMT
ENV PYTHON_VERSION=3.8.9
# Wed, 14 Apr 2021 16:32:17 GMT
ENV PYTHON_RELEASE=3.8.9
# Wed, 14 Apr 2021 16:34:56 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Tue, 27 Apr 2021 22:21:38 GMT
ENV PYTHON_PIP_VERSION=21.1
# Tue, 27 Apr 2021 22:21:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ab9dde151f662745c13461f00c453dcf32a51ea9/public/get-pip.py
# Tue, 27 Apr 2021 22:21:40 GMT
ENV PYTHON_GET_PIP_SHA256=0ed17e859b835ad5bf00851f4dc8bbc3520c13dfff6c131d410cdb3a92ff0af9
# Tue, 27 Apr 2021 22:23:20 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 27 Apr 2021 22:23:21 GMT
CMD ["python"]
# Tue, 27 Apr 2021 22:47:24 GMT
ENV HY_VERSION=1.0a1
# Tue, 27 Apr 2021 22:48:52 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Tue, 27 Apr 2021 22:48:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b4598ab88dab64b25b4257872564af9825cc6cd41fc8cc1ad11c32958d0da9`  
		Last Modified: Wed, 14 Apr 2021 16:39:38 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2ba2f82f3eddbacdc29cc778a55d06ae05a67ecde117b71217e52591dab5f2`  
		Last Modified: Wed, 14 Apr 2021 16:42:34 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9327741bb35a9e94c5d9774ebf204c6256a8f84fa6fa63112bcb14e5fb3580`  
		Last Modified: Wed, 14 Apr 2021 16:42:34 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b761757c76a5489a33afa548887814f66f6d6414128957a48a9511cb178d1109`  
		Last Modified: Wed, 14 Apr 2021 16:42:44 GMT  
		Size: 58.6 MB (58623548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b65c55d02062d357f28569cf5629dc0dc21f57144719f552ee0c495c01e0dc`  
		Last Modified: Tue, 27 Apr 2021 22:26:27 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54bfc76d4fd036324e594d632e1129a1e2eb9abb6b6e0d66ea2a794a8a96475`  
		Last Modified: Tue, 27 Apr 2021 22:26:27 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41bf02051d3de003fc00925b0e00b1e063aa8ad962077586a0e3d32e8c6d88db`  
		Last Modified: Tue, 27 Apr 2021 22:26:27 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee2dc08fed8d8ff7aac37dac864bac499652e077ccc35bfde61f8080b70b60f`  
		Last Modified: Tue, 27 Apr 2021 22:26:39 GMT  
		Size: 11.4 MB (11444503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c7f43dcebe057b7926da56cc84714ee215d2b24bd7311024e347ed2a061863`  
		Last Modified: Tue, 27 Apr 2021 22:26:27 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b432211768c8e871feb1191b01481e2fbe9007f92319d268083f96f275f205`  
		Last Modified: Wed, 28 Apr 2021 12:05:27 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09350e48ee2b491dde3ea6c3d409c677d53264f5d9b08c4256a17a8bab48bbac`  
		Last Modified: Wed, 28 Apr 2021 12:05:29 GMT  
		Size: 6.5 MB (6462037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f918c00f939f4249e2dcab7bb0ab9a404ecb8a3f4118150df0029dc1d10b0291`  
		Last Modified: Wed, 28 Apr 2021 12:05:28 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
