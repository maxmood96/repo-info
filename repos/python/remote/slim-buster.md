## `python:slim-buster`

```console
$ docker pull python@sha256:f92aa905e0871638217c29a66012bcbbe6b199e70f092f3f589e7f828d06cf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `python:slim-buster` - linux; amd64

```console
$ docker pull python@sha256:8448620dbeed1bb5ad13ddfae5e3b092362624ffcb639f60941c9313e73fcff2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43674126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d44b3a8f0e20bf82bda8ab741906dad1a4fc25d3b8198411737b62bd2dda6e3`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 02:56:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Mar 2022 02:56:27 GMT
ENV LANG=C.UTF-8
# Wed, 02 Mar 2022 02:56:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 02:56:34 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 02 Mar 2022 04:01:51 GMT
ENV PYTHON_VERSION=3.10.2
# Wed, 02 Mar 2022 04:15:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 02 Mar 2022 04:15:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Wed, 02 Mar 2022 04:15:51 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Wed, 02 Mar 2022 04:15:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 02 Mar 2022 04:15:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/2caf84b14febcda8077e59e9b8a6ef9a680aa392/public/get-pip.py
# Wed, 02 Mar 2022 04:15:51 GMT
ENV PYTHON_GET_PIP_SHA256=7c5239cea323cadae36083079a5ee6b2b3d56f25762a0c060d2867b89e5e06c5
# Wed, 02 Mar 2022 04:16:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 02 Mar 2022 04:16:05 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d445d10bda3af2679c0ec1ae7bf1cde7ff0737468e7b73e539a265caf24299a`  
		Last Modified: Wed, 02 Mar 2022 05:59:38 GMT  
		Size: 2.8 MB (2770146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7ba5177a876f583991486a2a0cb008da75ec2ef110ec55e2e107be1140599c`  
		Last Modified: Wed, 02 Mar 2022 06:01:08 GMT  
		Size: 11.1 MB (11116335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4759db5e555e0f12e42d09ac56e2e27b602a9b725441c9f7a6ecd5bba670f95`  
		Last Modified: Wed, 02 Mar 2022 06:01:06 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e804f45f3414d957f5f722c02d8cd026651dda92ca206ba906884c99e69c88`  
		Last Modified: Wed, 02 Mar 2022 06:01:07 GMT  
		Size: 2.6 MB (2633673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:slim-buster` - linux; arm variant v5

```console
$ docker pull python@sha256:0078bf642427ab25d1189748fea5c178a3f855076bda615b93f1c2153fc4a68c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40787110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbcddb1dcec66156005ba447773485897f1dafc966064f3d97120051ef499ec4`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 01 Mar 2022 02:03:56 GMT
ADD file:f5674cd595d2eb9d698a67c0669348b7dca3158b3c949498321a875d56d1db0e in / 
# Tue, 01 Mar 2022 02:03:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 18:13:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 18:13:37 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 18:13:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 18:13:58 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 01 Mar 2022 20:22:10 GMT
ENV PYTHON_VERSION=3.10.2
# Tue, 01 Mar 2022 20:51:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 01 Mar 2022 20:51:09 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Tue, 01 Mar 2022 20:51:10 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Tue, 01 Mar 2022 20:51:10 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 01 Mar 2022 20:51:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/2caf84b14febcda8077e59e9b8a6ef9a680aa392/public/get-pip.py
# Tue, 01 Mar 2022 20:51:11 GMT
ENV PYTHON_GET_PIP_SHA256=7c5239cea323cadae36083079a5ee6b2b3d56f25762a0c060d2867b89e5e06c5
# Tue, 01 Mar 2022 20:51:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 01 Mar 2022 20:51:45 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:d93143e6711bdadb9413c811c28fed68303bd0eafd6640f6552d2147730818af`  
		Last Modified: Tue, 01 Mar 2022 02:20:01 GMT  
		Size: 24.9 MB (24886227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1812dca044a6fc378d00f59bd6b41dde5387808cc2f1dc9155398ed2678760`  
		Last Modified: Wed, 02 Mar 2022 00:13:08 GMT  
		Size: 2.5 MB (2460696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc953bc09c4fa9c1d3fdce7649a0caf34705996013a23eaaff8e17abf3600f0`  
		Last Modified: Wed, 02 Mar 2022 00:15:38 GMT  
		Size: 10.8 MB (10806743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11612e36a33f3d2e10661da1ccec1af3aff3dcc1ee88941eade4d270c48697fb`  
		Last Modified: Wed, 02 Mar 2022 00:15:30 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2179acc6e4f58a6c25e290756d0e733d57c6bf1652769db9a04c0a3ab5568fc`  
		Last Modified: Wed, 02 Mar 2022 00:15:33 GMT  
		Size: 2.6 MB (2633208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:slim-buster` - linux; arm variant v7

```console
$ docker pull python@sha256:5e96624f689f022346292f1d0540d0a5aebff724f45ba19043a84dd412380af6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (38047023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b18f915c7cb11debf055bbb1dd88d52d6206d49cbe2a653596e46b50914c24b`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 01 Mar 2022 02:04:06 GMT
ADD file:d73a3eaf767825b31d0c0189624b35193e5ad7c5907f839edf6f7917036c2d0b in / 
# Tue, 01 Mar 2022 02:04:07 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 05:32:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Mar 2022 05:32:16 GMT
ENV LANG=C.UTF-8
# Wed, 02 Mar 2022 05:32:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 05:32:40 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 02 Mar 2022 07:59:29 GMT
ENV PYTHON_VERSION=3.10.2
# Wed, 02 Mar 2022 08:31:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 02 Mar 2022 08:31:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Wed, 02 Mar 2022 08:31:21 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Wed, 02 Mar 2022 08:31:21 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 02 Mar 2022 08:31:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/2caf84b14febcda8077e59e9b8a6ef9a680aa392/public/get-pip.py
# Wed, 02 Mar 2022 08:31:22 GMT
ENV PYTHON_GET_PIP_SHA256=7c5239cea323cadae36083079a5ee6b2b3d56f25762a0c060d2867b89e5e06c5
# Wed, 02 Mar 2022 08:31:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 02 Mar 2022 08:31:51 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:1acfd43b1a25aefe6117ba65bf2b46a19e3cf8e72b76f522a9fe299412e1c5f2`  
		Last Modified: Tue, 01 Mar 2022 02:20:32 GMT  
		Size: 22.8 MB (22754370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf78e200ead32b580cda8e03c12b1c531861f0ded1b1127a5b140b8c2c0707b`  
		Last Modified: Wed, 02 Mar 2022 12:57:04 GMT  
		Size: 2.4 MB (2358997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc566689d67b75d1ab1f6ecc07121802dd5ac016decc88f1dbda0baa06ff5bdf`  
		Last Modified: Wed, 02 Mar 2022 12:59:28 GMT  
		Size: 10.3 MB (10300190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d228d4688940dc2b013c37c5882ddbf7e586a3b5a3c37296f6fc99dd1c5c099`  
		Last Modified: Wed, 02 Mar 2022 12:59:21 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a60141bae2ea46e32fbad75d78665ec2e70c6da3df635aa62ba8eb9710f6ac`  
		Last Modified: Wed, 02 Mar 2022 12:59:23 GMT  
		Size: 2.6 MB (2633232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:slim-buster` - linux; arm64 variant v8

```console
$ docker pull python@sha256:36cf3cfb47ce302bf373971b3f4d1c556f9b3499de4dc0190eba1bf721c38e7c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42093227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abd61716882553dd7918600ff8d4b7b15345f03e8513e1227690dfaca167854`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:57 GMT
ADD file:7d35162eea06441e7115c6fd9508802eafee00f64b11a7529a8f125bc67fa95e in / 
# Tue, 01 Mar 2022 02:11:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 19:47:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 19:47:24 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 19:47:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 19:47:31 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 01 Mar 2022 20:32:21 GMT
ENV PYTHON_VERSION=3.10.2
# Tue, 01 Mar 2022 20:42:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 01 Mar 2022 20:42:06 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Tue, 01 Mar 2022 20:42:07 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Tue, 01 Mar 2022 20:42:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 08 Mar 2022 03:03:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/38e54e5de07c66e875c11a1ebbdb938854625dd8/public/get-pip.py
# Tue, 08 Mar 2022 03:03:34 GMT
ENV PYTHON_GET_PIP_SHA256=e235c437e5c7d7524fbce3880ca39b917a73dc565e0c813465b7a7a329bb279a
# Tue, 08 Mar 2022 03:03:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 08 Mar 2022 03:03:52 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:69bf0018a85cc0775a59a4dbda1b2f2e71086a2d817473f72336bf4d0a83b9d0`  
		Last Modified: Tue, 01 Mar 2022 02:19:15 GMT  
		Size: 25.9 MB (25923140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99d2ad45cad19756f963eafcc80d7f87fbe4ac96f5fce0a6afe21e83af6fb45`  
		Last Modified: Tue, 01 Mar 2022 21:57:33 GMT  
		Size: 2.6 MB (2636110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67ece4d2166e3cf89d2cb67b4f10359ba73d8dc63cfd15e552b70dd984319ee`  
		Last Modified: Tue, 01 Mar 2022 21:59:04 GMT  
		Size: 11.1 MB (11111363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce2ecd8efcd2cef766b6b5f3490309a4a731d3865684f890ef156cbf407a625`  
		Last Modified: Tue, 01 Mar 2022 21:59:02 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16caa00e19f6e48cf537c154b63426e723027bd3a27da4b68acb7156ab358d52`  
		Last Modified: Tue, 08 Mar 2022 03:14:47 GMT  
		Size: 2.4 MB (2422379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:slim-buster` - linux; 386

```console
$ docker pull python@sha256:d2dec10214e45c0b6708b82c12e469ccf74da357838da63ddd8dbff56905ac51
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44468090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f71f8cc8dfd9ff3b51322816062c6cd2b922ce2737c5c17fa51c11b4a7bf6b`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 01 Mar 2022 02:08:04 GMT
ADD file:d9d384f0402bc696e46e7529f52d64859a66aa7a60bca9c7beee7433a5f7af6e in / 
# Tue, 01 Mar 2022 02:08:04 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 23:00:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 23:00:37 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 23:00:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 23:00:43 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 02 Mar 2022 00:13:55 GMT
ENV PYTHON_VERSION=3.10.2
# Wed, 02 Mar 2022 00:31:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 02 Mar 2022 00:31:22 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Wed, 02 Mar 2022 00:31:22 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Wed, 02 Mar 2022 00:31:22 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 08 Mar 2022 03:38:06 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/38e54e5de07c66e875c11a1ebbdb938854625dd8/public/get-pip.py
# Tue, 08 Mar 2022 03:38:06 GMT
ENV PYTHON_GET_PIP_SHA256=e235c437e5c7d7524fbce3880ca39b917a73dc565e0c813465b7a7a329bb279a
# Tue, 08 Mar 2022 03:38:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 08 Mar 2022 03:38:19 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:c761ce6f2bf0aed07e1198c6f827444969d6e76dda0e55dbb45900920e551d27`  
		Last Modified: Tue, 01 Mar 2022 02:16:51 GMT  
		Size: 27.8 MB (27804590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3732310af3a21f79d28ad07be855cf934da0caadc03263a18b52b7b0a94c0d6`  
		Last Modified: Wed, 02 Mar 2022 02:39:02 GMT  
		Size: 2.8 MB (2781563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2ac748805b6bca9ec1c9a10b9a27640aae7ec57a93dd6dabcc9f422821c2a7`  
		Last Modified: Wed, 02 Mar 2022 02:41:00 GMT  
		Size: 11.2 MB (11248324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e6d9878a1a67c6dfca0c16e00257cc38a88037c474f7bde5ecc7830d5dd48e`  
		Last Modified: Wed, 02 Mar 2022 02:40:57 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f24aa69275a5a259e93e32062431aadec0a2d716b1700f84c30b5db386939ce`  
		Last Modified: Tue, 08 Mar 2022 03:49:34 GMT  
		Size: 2.6 MB (2633378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:slim-buster` - linux; ppc64le

```console
$ docker pull python@sha256:df5d53161ebe19e38dcfcef71b9b11ae56fb25afa02f6c10f2b76b195c751850
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48009497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ff7f22f9ceaceae4670288310d613a663859d4e8a229448374f27da6a59227`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 01 Mar 2022 02:06:09 GMT
ADD file:005ec6e437fc9cf8458edb6369462ce53feb585501ea6b5e5f4a6264557b3a01 in / 
# Tue, 01 Mar 2022 02:06:14 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 19:08:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 19:08:21 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 19:08:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 19:09:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 01 Mar 2022 20:46:22 GMT
ENV PYTHON_VERSION=3.10.2
# Tue, 01 Mar 2022 21:07:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 01 Mar 2022 21:07:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Tue, 01 Mar 2022 21:07:57 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Tue, 01 Mar 2022 21:08:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 01 Mar 2022 21:08:03 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/2caf84b14febcda8077e59e9b8a6ef9a680aa392/public/get-pip.py
# Tue, 01 Mar 2022 21:08:07 GMT
ENV PYTHON_GET_PIP_SHA256=7c5239cea323cadae36083079a5ee6b2b3d56f25762a0c060d2867b89e5e06c5
# Tue, 01 Mar 2022 21:08:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 01 Mar 2022 21:08:50 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:3cee81bb9485c9d0b620c87842e566d7a1f93086ef88c00a4d7175fc776b7f3f`  
		Last Modified: Tue, 01 Mar 2022 02:16:22 GMT  
		Size: 30.6 MB (30562288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2ceee1a1325a3d6743de7471b6bed2f51edc3acb819f882064c9932632261b`  
		Last Modified: Tue, 01 Mar 2022 23:57:12 GMT  
		Size: 2.9 MB (2887538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d26fb4d6f7e4e0d14b67afc0c8003c2c565178e612302a065f780da158a427b`  
		Last Modified: Tue, 01 Mar 2022 23:59:31 GMT  
		Size: 11.9 MB (11924817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b2de1abecbf69709a927ce52095d96c60e2180d9b5e16c4040d0ff8cbc88ca`  
		Last Modified: Tue, 01 Mar 2022 23:59:29 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a423bae0806bd52166058a7de37113888aa116409d5506f4b5bd9933b0229a79`  
		Last Modified: Tue, 01 Mar 2022 23:59:29 GMT  
		Size: 2.6 MB (2634619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:slim-buster` - linux; s390x

```console
$ docker pull python@sha256:5fb8a86a275133e86add4da4c3e437232ac10e67d4bc61801a561d1d36ed1e70
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41780628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de55fc44fe181ddae261fefd9157e799c62f8bc66149423628b4093e97018d2`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:27 GMT
ADD file:908bd36a2b17b792aa02339ed6a72d1051267279d72330b1c5cd8617ca5d819e in / 
# Tue, 01 Mar 2022 02:02:28 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:53:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:53:55 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 10:53:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:53:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 01 Mar 2022 11:31:48 GMT
ENV PYTHON_VERSION=3.10.2
# Tue, 01 Mar 2022 11:40:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 01 Mar 2022 11:40:15 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Tue, 01 Mar 2022 11:40:15 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Tue, 01 Mar 2022 11:40:15 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 01 Mar 2022 11:40:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/2caf84b14febcda8077e59e9b8a6ef9a680aa392/public/get-pip.py
# Tue, 01 Mar 2022 11:40:15 GMT
ENV PYTHON_GET_PIP_SHA256=7c5239cea323cadae36083079a5ee6b2b3d56f25762a0c060d2867b89e5e06c5
# Tue, 01 Mar 2022 11:40:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 01 Mar 2022 11:40:25 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:cb73b674076b2da947cefa0692c1d193bda8bfd443c178f9bb39bbae7656ead8`  
		Last Modified: Tue, 01 Mar 2022 02:08:05 GMT  
		Size: 25.8 MB (25769053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfef4d19cc7d3537586233da8e2d4f810a292090eaedd6b56849d4e798b431b`  
		Last Modified: Tue, 01 Mar 2022 12:41:17 GMT  
		Size: 2.5 MB (2459523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f24c2d6ee04882a38d464275e7a1dcde2e32dc5465878ec4acd984c181ce675`  
		Last Modified: Tue, 01 Mar 2022 12:42:15 GMT  
		Size: 10.9 MB (10918750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417120747848c45f3c2d488a517a048ff8175bf4acd93b25a058970f8287eba2`  
		Last Modified: Tue, 01 Mar 2022 12:42:13 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad787f5258f6a36f01a6026282d2caa8dbfe69ecc93b48ffb757c4fdcf08649`  
		Last Modified: Tue, 01 Mar 2022 12:42:14 GMT  
		Size: 2.6 MB (2633066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
