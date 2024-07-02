## `python:slim-bullseye`

```console
$ docker pull python@sha256:d2d0fbc8ef267a825ec9052ab70b8e29d5002be6bf339fde07da7a3d1e702ddb
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

### `python:slim-bullseye` - linux; amd64

```console
$ docker pull python@sha256:7ad75a39d176fe14c8d75068153a79a450b9b7fbe541b9f7b694b91860d40499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46601540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d302cac7422b9caaf3679d1560ccbcbf508fd52c9dfc64cb0d7ce74b5cfc3ff0`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 07 Jun 2024 03:53:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["bash"]
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jun 2024 03:53:24 GMT
ENV LANG=C.UTF-8
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_VERSION=3.12.4
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bc145b26d5e6de6199a858268bb14cd4d291aa32b5de07b03dc3958ee5adc4`  
		Last Modified: Tue, 02 Jul 2024 03:15:48 GMT  
		Size: 1.1 MB (1076284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a316f9597ba9d82ee2673d255e82673977947b6be01adefa56b2711eca15ef42`  
		Last Modified: Tue, 02 Jul 2024 03:15:48 GMT  
		Size: 11.2 MB (11228670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a8853486c64fe69c56b49df91bec5caa7fac5cc321c92a03b40af0e0fe5260`  
		Last Modified: Tue, 02 Jul 2024 03:15:47 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235554504dcb2fc49c0c378bf65b7bf612b9154fe9da40889cdac230991682c1`  
		Last Modified: Tue, 02 Jul 2024 03:15:48 GMT  
		Size: 2.9 MB (2874072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:354b986cd2793786ad8834d529e0977a9e5838aaf29f5656f2d8744f908cb143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2705666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8682cb8517346c5073d4c1b7e812dba3188c3283d2510cf0ea0b49c96a354c`

```dockerfile
```

-	Layers:
	-	`sha256:7dce4f1712c0c4f554af2164890db8e4a2f3f7cb258c3eeb901dc19a51feb6de`  
		Last Modified: Tue, 02 Jul 2024 03:15:48 GMT  
		Size: 2.7 MB (2679740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dec24c5a21f17445ef0f317bfe16d0746a7db1782de0096e5cfa48ca284c140b`  
		Last Modified: Tue, 02 Jul 2024 03:15:47 GMT  
		Size: 25.9 KB (25926 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-bullseye` - linux; arm variant v5

```console
$ docker pull python@sha256:7cfaccf868d0aa1bc5e6aa6bdfe4456ae219f7a462b2bcc22f3ba261731515d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43546082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b31b06d57cc0b0032759104620a85ea7161039fcaa3370d88435a5160cc026`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 07 Jun 2024 03:53:24 GMT
ADD file:78cff0ed53bbaaa1d7680e733d50b8fc9042e257b78718ad822f9ac57a5d1dbb in / 
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["bash"]
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jun 2024 03:53:24 GMT
ENV LANG=C.UTF-8
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_VERSION=3.12.4
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:f8a34d14f57d3fcf2d97b9fc0fb4439a2d00afe9411fdc788629eb4074186288`  
		Last Modified: Thu, 13 Jun 2024 00:52:21 GMT  
		Size: 28.9 MB (28936731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e505440c19d32bf663204471b090b7e317b8d940c84da46a0f0faf45a19a7330`  
		Last Modified: Thu, 27 Jun 2024 02:17:37 GMT  
		Size: 856.1 KB (856101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be90c1892ca0e5855a30dd4a8011c24a7701ab7a2fa2fe497295a98e8e271110`  
		Last Modified: Thu, 27 Jun 2024 02:17:37 GMT  
		Size: 10.9 MB (10919820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad9bb2aedcebc5d00b185e4c512990a40f3ff6e0636c2c35cc9a311e478cd55`  
		Last Modified: Thu, 27 Jun 2024 02:17:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b1b97bdd07a08f9ce444b27bb3842c245ab6b01fb1da78113a2445283ff32b`  
		Last Modified: Thu, 27 Jun 2024 02:17:37 GMT  
		Size: 2.8 MB (2833197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:69956dc252d8fd65000872a7f09e1f5d53b0b1ec636db0a19a69c5b46224efba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2706011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeaa3f1b6d55b11488584d8680ab2c05b691c6fd82a597b21c39a478671a508e`

```dockerfile
```

-	Layers:
	-	`sha256:3d1177fc3d56737a81bbf40c288fcf62be28b1a520229e19baf4c23592824e2d`  
		Last Modified: Thu, 27 Jun 2024 02:17:37 GMT  
		Size: 2.7 MB (2679980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11e2e5d4a07c21d288a88b7449f9f2e8fc03221897355ae9588493518423d650`  
		Last Modified: Thu, 27 Jun 2024 02:17:37 GMT  
		Size: 26.0 KB (26031 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-bullseye` - linux; arm variant v7

```console
$ docker pull python@sha256:c04f2eabc53ed3a25c900b63b644ae9987aa475f7844b54c9f24bcf83020a8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40744391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb09535f28fdc19568ecb26bf14ffc685dc85f362566a10791f4ca62700fdbc`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 07 Jun 2024 03:53:24 GMT
ADD file:b23992f77c1f22e7bf9048641d6da1d6ef922d78b4118f6d513e183ae6de7e34 in / 
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["bash"]
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jun 2024 03:53:24 GMT
ENV LANG=C.UTF-8
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_VERSION=3.12.4
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:4873d96591a32d2d686ff6c86338fc9a63b9d60639482601b5402eb76e56a566`  
		Last Modified: Thu, 13 Jun 2024 01:02:22 GMT  
		Size: 26.6 MB (26594507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46b4de15aaddca66b3a24bc742dfa9cdb649ed0113659185052bfefc9fc109c`  
		Last Modified: Thu, 27 Jun 2024 03:03:21 GMT  
		Size: 837.4 KB (837396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4874680a89cd27c93ced451ab943409005e5b660d4a0024a1fab8a823c023fa7`  
		Last Modified: Thu, 27 Jun 2024 03:03:21 GMT  
		Size: 10.5 MB (10479068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02c3354959658bc0564afe28bc0e108052c180015601486436c8bb50f3c6509`  
		Last Modified: Thu, 27 Jun 2024 03:03:20 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8bd93ce358ad27bf0f5218adfc5aa42ccb25a5d3d73eff64bfe2ccf22bcc8c`  
		Last Modified: Thu, 27 Jun 2024 03:03:21 GMT  
		Size: 2.8 MB (2833189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:593230014c29f986f0a1afabd3dc3e5d15c91681ec6fd9fc9d047a391f24eaca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2708019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb167c8c7cba31b19d17460553d6626a63ad12ddb692dd34d08dad50a02ce21`

```dockerfile
```

-	Layers:
	-	`sha256:7bb491bce7fba41cefe008a7a2afaa289189336415b645c61f92c7788336bdaa`  
		Last Modified: Thu, 27 Jun 2024 03:03:21 GMT  
		Size: 2.7 MB (2681988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6ec4b7c7f990e038f55da4386b73c8d68f668050b2c360767b5b25aacbd6587`  
		Last Modified: Thu, 27 Jun 2024 03:03:20 GMT  
		Size: 26.0 KB (26031 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull python@sha256:fde59aced53cd60ba933012a395c6a8efa95c622b047682138232c9250e7a390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45076024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8979f91c948f33954dd60097d3f7ebe20975cb0d8c5ce1d5b496c0eee0991f0`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 07 Jun 2024 03:53:24 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["bash"]
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jun 2024 03:53:24 GMT
ENV LANG=C.UTF-8
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_VERSION=3.12.4
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aee3611c294e8e92568be7d452b276ef9e65edbf2b4094aff64b5230e5263f5`  
		Last Modified: Thu, 27 Jun 2024 02:03:16 GMT  
		Size: 859.9 KB (859926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5711e9bc4d0b26444b0c03c10dea12d9016dc2a253e8cc96d8baa8a1977c9f0d`  
		Last Modified: Thu, 27 Jun 2024 02:03:17 GMT  
		Size: 11.3 MB (11295394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d8026d2630cf0aa51b1c290785619b2fea3835938f62f10d9dac7208ba2b38`  
		Last Modified: Thu, 27 Jun 2024 02:03:16 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8fb69f6c876986944023b9f15d8dc45a9ed892bb5dc2cf015881216a5fd781`  
		Last Modified: Thu, 27 Jun 2024 02:03:17 GMT  
		Size: 2.8 MB (2833498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:85a497b8772d290430f737cce1860da61dcca27bfe3ccd0420c96c5cc1795931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2706229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a5231716b717328d95b541c501fb504484d5e106a280ab77357ddd57329faf`

```dockerfile
```

-	Layers:
	-	`sha256:9d3f6df18cdf5bc7348f8fd2814a4663cd9227314592a8109b979c5eb86e15ae`  
		Last Modified: Thu, 27 Jun 2024 02:03:16 GMT  
		Size: 2.7 MB (2679998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b664faf6726df1156fa2204184dab15da43e577b5054ac53b21398f75a32751`  
		Last Modified: Thu, 27 Jun 2024 02:03:16 GMT  
		Size: 26.2 KB (26231 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-bullseye` - linux; 386

```console
$ docker pull python@sha256:661da043dc2f576df8ced9f9c29f2582e669b7ed44055cff7c6dcbe25479791c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47698331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe657473a8ba52dc76cb4822b585ce6cd9f3876a6babb93fd7c7026d3686176`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 07 Jun 2024 03:53:24 GMT
ADD file:82c5579b81dad9a5dff7724fd8e74d225f919e378995a95c9a0a9c17ca55a77a in / 
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["bash"]
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jun 2024 03:53:24 GMT
ENV LANG=C.UTF-8
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_VERSION=3.12.4
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:1084208571fd0651d255a493f4e05ba8b2b837b52064c5f2f317a2d979e679bc`  
		Last Modified: Tue, 02 Jul 2024 00:43:26 GMT  
		Size: 32.4 MB (32408452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e5b30078f0c8ea31cb2ff489fad41c96f383e1d15e2534836cf7ca661f67c3`  
		Last Modified: Tue, 02 Jul 2024 03:22:20 GMT  
		Size: 1.1 MB (1088864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6593ceac3822222490d15af10f9614a764e537164c974d9199ae93bb5bf04707`  
		Last Modified: Tue, 02 Jul 2024 03:22:20 GMT  
		Size: 11.3 MB (11327112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12271913872c623e2a14f687a7a7f25d637158f5400daa38c3d3ca846d78496c`  
		Last Modified: Tue, 02 Jul 2024 03:22:20 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2a673101d0de534a6cd002b44b7a43052132e62adf8c0a6144810e25d48623`  
		Last Modified: Tue, 02 Jul 2024 03:22:20 GMT  
		Size: 2.9 MB (2873671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:b1084a58ad4b9fe92d61a65b19c05890dabecf40e7cda392e0b92724f567f0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2702736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f931adaa5148ee050edc04779c0ca5911ebdc1d14d4396d73e0a0f66f1df8e1e`

```dockerfile
```

-	Layers:
	-	`sha256:c7d883904b25cbef10a0985af6a016a7f0aab33b944813b14a0a75b7caa333f0`  
		Last Modified: Tue, 02 Jul 2024 03:22:20 GMT  
		Size: 2.7 MB (2676846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff51fa8065a8b75dc068027ae69a983be0af8e1ee79447324b24be7789aa82d2`  
		Last Modified: Tue, 02 Jul 2024 03:22:20 GMT  
		Size: 25.9 KB (25890 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-bullseye` - linux; ppc64le

```console
$ docker pull python@sha256:35d8ad141724c87c5bef813f0b6c7dba810fa03129b3c5bea9b575c7d09ea7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50806562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d99025db73950bd62aa7fabb7c9140d430d9210d68f9744fd265971708b682`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 07 Jun 2024 03:53:24 GMT
ADD file:8fcbfde241e9377ada40ad73089516c86d20e018c99a8192ba63a50f0168b8b9 in / 
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["bash"]
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jun 2024 03:53:24 GMT
ENV LANG=C.UTF-8
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_VERSION=3.12.4
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:687d52b24394339ceb9470debd0e5f0d6b612ceb063cc228cbef23d23fb7f6a2`  
		Last Modified: Tue, 02 Jul 2024 01:22:46 GMT  
		Size: 35.3 MB (35299189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37468e61e8f33dac3a009e153236ed6daa269e219ae7c51205077b3662b2cf85`  
		Last Modified: Tue, 02 Jul 2024 17:44:58 GMT  
		Size: 1.1 MB (1094932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c850140bcc9c37c49f8c7659790a697d14519d42d71f0f03542eeec872713a5`  
		Last Modified: Tue, 02 Jul 2024 17:44:58 GMT  
		Size: 11.5 MB (11537749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b41fb9d1dcc281ac80a1890764cee9b1424da97082134e1005ab82d49300d5`  
		Last Modified: Tue, 02 Jul 2024 17:44:57 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a4b20af8074b518d5c8fd28ce61f82586f92f2547d6a7ac1abb127fbaf92d0`  
		Last Modified: Tue, 02 Jul 2024 17:44:58 GMT  
		Size: 2.9 MB (2874460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:708f9a549e00c32ffe377aa763ce3ef63e84e24536d77ce9b746e1d1fbdf3a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2710087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c4be507394c3be6602c6c33667d679317bdbda8ba74d0842f7ecfb71827a11`

```dockerfile
```

-	Layers:
	-	`sha256:967f867b2a029f56e2060708d17f17a5ff673d0f8b94952596dc59594c459c80`  
		Last Modified: Tue, 02 Jul 2024 17:44:58 GMT  
		Size: 2.7 MB (2684117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bbc34a2e97dfe36652a698b72b2128428ca220d5871101e890165c8041c12bf`  
		Last Modified: Tue, 02 Jul 2024 17:44:57 GMT  
		Size: 26.0 KB (25970 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-bullseye` - linux; s390x

```console
$ docker pull python@sha256:f1bf4780136461a4ff73a07cd93b74b35dedd6c9eaaa04b5104899352e6d3a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44786832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093f84f2bc684daed47d8bd767f86523e1930344bc1ca46c86031928dea85cb8`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 07 Jun 2024 03:53:24 GMT
ADD file:31ece4c92b8738b187a4c8ac4ec5558c9127823e7a57214b84a551afab6e97a0 in / 
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["bash"]
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jun 2024 03:53:24 GMT
ENV LANG=C.UTF-8
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_VERSION=3.12.4
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 07 Jun 2024 03:53:24 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 07 Jun 2024 03:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 07 Jun 2024 03:53:24 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:a3136cefab0552c07b47b507af992477c2b33aff541d74a1bdb0f0c475f008fe`  
		Last Modified: Tue, 02 Jul 2024 00:49:04 GMT  
		Size: 29.7 MB (29662353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14220572a7603ca678630a49daa33ea1fc9e1570b0be8aa0f934f8d0d7c8553`  
		Last Modified: Tue, 02 Jul 2024 09:22:07 GMT  
		Size: 1.1 MB (1075919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22461a621e39cfec29db38130aca775a4e452467aca25591a1dae7b408074b4`  
		Last Modified: Tue, 02 Jul 2024 09:22:07 GMT  
		Size: 11.2 MB (11174497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66852eaf5d1efe7da9af8743fa809ead52deae55a646eb8f1491ac65ebba767f`  
		Last Modified: Tue, 02 Jul 2024 09:22:07 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eba856f43353f98876df61060e3543e1df172a72baf79be72836de2f4007d9`  
		Last Modified: Tue, 02 Jul 2024 09:22:07 GMT  
		Size: 2.9 MB (2873832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:7a22640ac0fc6a8c931433392325a5e74546618d2fa46378ae4b17f7dfda9678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2705860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f459f83226b8b84f16bf6df41b5e5df1a3b50a86c4940ac0152c45960515e5a`

```dockerfile
```

-	Layers:
	-	`sha256:f8b7948b509de7164694c045b57b9d278811616a31fbbf34e186d530614a9572`  
		Last Modified: Tue, 02 Jul 2024 09:22:07 GMT  
		Size: 2.7 MB (2679936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85a391ba35ce6a7a85ae4beeafef13d3aef8a0d93e97ec95887ecbcdd2dab8c6`  
		Last Modified: Tue, 02 Jul 2024 09:22:07 GMT  
		Size: 25.9 KB (25924 bytes)  
		MIME: application/vnd.in-toto+json
