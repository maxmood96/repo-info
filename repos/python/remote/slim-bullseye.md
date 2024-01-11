## `python:slim-bullseye`

```console
$ docker pull python@sha256:14cfaa6a5550e132b5a50652113c73425d0657f67e7892d9da716d599a76d1b7
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

### `python:slim-bullseye` - linux; amd64

```console
$ docker pull python@sha256:ad98ce2e3bfbac348e03e4481525dda1575ac8e2f55619d0112099fa2a3c13d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46650591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9472091857b9e324dfb3e259d8c4c9ad0edf6936ea69d3d178ca5a5981523fc7`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 04:49:21 GMT
ENV LANG=C.UTF-8
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_VERSION=3.12.1
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f85b902acc6cbfe88473f650e355e0d2496e8aac55421a013e61e77d08cd83`  
		Last Modified: Thu, 11 Jan 2024 11:48:02 GMT  
		Size: 1.1 MB (1078390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e0b75de46d6bd4db79886ce63a26aaffccce81fd69a1f42f8ced45ab9551b1`  
		Last Modified: Thu, 11 Jan 2024 11:49:18 GMT  
		Size: 11.2 MB (11183936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf3cae1449a01d9c6ff581cc633e1fb814aae122ead86d3a95f9854a66ec4c9`  
		Last Modified: Thu, 11 Jan 2024 11:49:16 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89af42e15358763da399cbe7163befce639eb7d16053c6a7a6f1e613914a314c`  
		Last Modified: Thu, 11 Jan 2024 11:49:17 GMT  
		Size: 3.0 MB (2970066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:slim-bullseye` - linux; arm variant v5

```console
$ docker pull python@sha256:7fd652e3cbd866a72eea2bdf252150a3b0db7207e72482c7d8a10b1a3fe4fa9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43825468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c124b2aae707257e32511b3e6e4b452e5042d0ea880a4df2a8b38847d75f0ec`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:38 GMT
ADD file:831966ecbc1ad85566dda1f3580cd9306cc099069cd418506e8befd03c296d1c in / 
# Tue, 19 Dec 2023 01:55:38 GMT
CMD ["bash"]
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 04:49:21 GMT
ENV LANG=C.UTF-8
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_VERSION=3.12.1
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:fdebea600ba5b47ddd94c41d9d687679a030fdad563a3490945a5433dae01d54`  
		Last Modified: Tue, 19 Dec 2023 01:59:22 GMT  
		Size: 28.9 MB (28921283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a46d6592e825de315762c0c2ee6dc9cd764ff2859b2b568f4640703f1f5edf`  
		Last Modified: Tue, 19 Dec 2023 12:34:34 GMT  
		Size: 1.1 MB (1061361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3c5f79d0e747c8bbda5f2b62e151322fe3908896e2f8c5b3c8e35d1e09c816`  
		Last Modified: Tue, 19 Dec 2023 12:35:42 GMT  
		Size: 10.9 MB (10873012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e5802fd0f67149bce0a4f712581a737ab077d86e5f6607da5a27e0d767b257`  
		Last Modified: Tue, 19 Dec 2023 12:35:40 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0db733b5be5e017402d54ca920cfc7d635a752f909d79ac483ac5e6abd7a354`  
		Last Modified: Tue, 19 Dec 2023 12:35:41 GMT  
		Size: 3.0 MB (2969567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:slim-bullseye` - linux; arm variant v7

```console
$ docker pull python@sha256:61583f05f216d76dccf2522de62e295830ed5a9eb9af4b5a259ab5d88062a984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41030968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ce58d5a7a6c75e1a8687b696698501028e05a4c55d3ab37030683250f2d7be`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:37 GMT
ADD file:1a36d919bfcbaa6b981b71ce99d777d303e69c2d6cb1924992e5a9cd811c11c5 in / 
# Thu, 11 Jan 2024 02:42:38 GMT
CMD ["bash"]
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 04:49:21 GMT
ENV LANG=C.UTF-8
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_VERSION=3.12.1
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:d976170654fe1bc717306b8bf14dc57d20e331b13e4797bc137e6911aa745a8a`  
		Last Modified: Thu, 11 Jan 2024 02:49:26 GMT  
		Size: 26.6 MB (26578974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75883f542e0ccc402d04e36ebb46d0024e058ff434b909b4ba77914d7c2b7b2`  
		Last Modified: Thu, 11 Jan 2024 19:08:40 GMT  
		Size: 1.0 MB (1043403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f39a8b53d3b8b2f7d5285fa7d2852d15ca55daab1795e2b395844327e7117cb`  
		Last Modified: Thu, 11 Jan 2024 19:10:00 GMT  
		Size: 10.4 MB (10438553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84f66709f362d762b0e19b753ff2595961c5c5111bbc4a033fa2ccf50852564`  
		Last Modified: Thu, 11 Jan 2024 19:09:57 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ad8a4df50aad6ab58a299715ad0e0c6bc7bf84205e5f1e0b2ee8c9301c8ca1`  
		Last Modified: Thu, 11 Jan 2024 19:09:59 GMT  
		Size: 3.0 MB (2969794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull python@sha256:1a869059370ac7a3f465c81a0a0882fe38fa561b8e6c04071d7460116d8e80a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45349898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246facc7e742794cd410a5cbc9e23457accd0d836875271b43f1544b1fbcd71c`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 04:49:21 GMT
ENV LANG=C.UTF-8
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_VERSION=3.12.1
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ecf4b5d865bda41981d4a96589698efad2b639e76cec775aee85efce3f5c9a7`  
		Last Modified: Thu, 11 Jan 2024 07:54:56 GMT  
		Size: 1.1 MB (1066233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe8ecb3bf1680c1ec7c64997f659cc87724f65328e7510a67d6c4b3768a240a`  
		Last Modified: Thu, 11 Jan 2024 07:55:30 GMT  
		Size: 11.2 MB (11249577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebda371f11c7f1daaa8fe080c8d763b4dd074cc1def6c802c0d4961bc7abb74e`  
		Last Modified: Thu, 11 Jan 2024 07:55:29 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988115fa28d14d5e3133d933db436cb1b0170d307a0a50043d96c17491c85655`  
		Last Modified: Thu, 11 Jan 2024 07:55:29 GMT  
		Size: 3.0 MB (2969835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:slim-bullseye` - linux; 386

```console
$ docker pull python@sha256:1788f794ae14c62f3ded57ba49ca0e223df93e64fbddd95745a293e10e08f5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47749689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d615a968e88fae0e45fd3ede621090b6258da6c68c97e6e753de06a3957c8c`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 11 Jan 2024 02:39:01 GMT
ADD file:ed1ce84cc05c621c3311366a5ef8f9ed36bdff95d75ee1564c10e7a20f993b61 in / 
# Thu, 11 Jan 2024 02:39:01 GMT
CMD ["bash"]
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 04:49:21 GMT
ENV LANG=C.UTF-8
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_VERSION=3.12.1
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:d19cbf7b148868960150824d1e6f8ebc5f6d7542a422061491e92178f7db879b`  
		Last Modified: Thu, 11 Jan 2024 02:44:06 GMT  
		Size: 32.4 MB (32402672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b854ec9560593c9d1c9349bdc7ada7cd444372300a9521f83fedc99f705f0f5b`  
		Last Modified: Thu, 11 Jan 2024 14:57:58 GMT  
		Size: 1.1 MB (1091143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b4fd497124dbd0b1c572cebbdcf8e643dea527f7455be64105c24d4cbc9eed`  
		Last Modified: Thu, 11 Jan 2024 14:59:15 GMT  
		Size: 11.3 MB (11285851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad17d557785314c7890cc44065d1b260c0d47e4df78f43a035d53239aec644b`  
		Last Modified: Thu, 11 Jan 2024 14:59:12 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3d38a33ae51d421f2408f99fe2d690355afac04af5c50f9c200fa539101376`  
		Last Modified: Thu, 11 Jan 2024 14:59:13 GMT  
		Size: 3.0 MB (2969780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:slim-bullseye` - linux; ppc64le

```console
$ docker pull python@sha256:81e99399b0b08a782e9f291649385b04585c7c19d28c83f7626e19e3b9905b71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50858816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9eaf23542942167677af929244553772232a94c464557489de4c7299e097f4f`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:59 GMT
ADD file:577ec786dad9a86344b678e69a7f514c3deede7cc45d9b3c9088449060272d55 in / 
# Thu, 11 Jan 2024 02:35:01 GMT
CMD ["bash"]
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 04:49:21 GMT
ENV LANG=C.UTF-8
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_VERSION=3.12.1
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:4c9dbec0f2ecfefcce502a32967ad48a18396e58a4950f972d672b4d95c84bcc`  
		Last Modified: Thu, 11 Jan 2024 02:40:16 GMT  
		Size: 35.3 MB (35293800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7ecc01f1c593116ad4f9475f2286b714f881eb7bb55f7ddfc414797dd4574d`  
		Last Modified: Thu, 11 Jan 2024 11:59:27 GMT  
		Size: 1.1 MB (1097024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2add04020a9df57bcfe5cc94fbd6e349154b9a502f09b62977739b14638ede2`  
		Last Modified: Thu, 11 Jan 2024 12:00:51 GMT  
		Size: 11.5 MB (11496517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6612a5788cf50debc256236a6ad5dec6494b4336b9a31ce9b64d29d441d6421`  
		Last Modified: Thu, 11 Jan 2024 12:00:48 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ba894a4d96a6f63a413309dc56414ebeaa565484e420bd092405217a7adf2e`  
		Last Modified: Thu, 11 Jan 2024 12:00:50 GMT  
		Size: 3.0 MB (2971230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:slim-bullseye` - linux; s390x

```console
$ docker pull python@sha256:0d7aaf3b5a033d58ee68def9b1cb0ca563a96b52c48d30a62150dd2906a742f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44837748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ad3ab7013ad792922f2474ab3c2d96f446866554d2b42a2f52e4173adfea7c`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 11 Jan 2024 01:45:46 GMT
ADD file:77a92d4e9397475a6c68f4341baba607a7c875bc6e252de3e096482dd074f8ca in / 
# Thu, 11 Jan 2024 01:45:49 GMT
CMD ["bash"]
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 04:49:21 GMT
ENV LANG=C.UTF-8
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_VERSION=3.12.1
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Fri, 08 Dec 2023 04:49:21 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Fri, 08 Dec 2023 04:49:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 08 Dec 2023 04:49:21 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:a8470cec8ee9510bf45556c756635d84eb3cbc0220b52812522196008c6b0d3e`  
		Last Modified: Thu, 11 Jan 2024 01:51:19 GMT  
		Size: 29.7 MB (29656884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1cf615fe494a2b2f61c711ea028c6a6dc336c43a53e105c47b1f2eb8f7902e`  
		Last Modified: Thu, 11 Jan 2024 05:07:21 GMT  
		Size: 1.1 MB (1077849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9765cad88aceb18975c049a027e33d75981b6ed642717c73420da1894891fb8b`  
		Last Modified: Thu, 11 Jan 2024 05:08:11 GMT  
		Size: 11.1 MB (11133005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670b647507ae33ff6372fd7075a432d7b63c66db328c24975d7e3d004d7a79ab`  
		Last Modified: Thu, 11 Jan 2024 05:08:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a73e765f453fc7ae5f6a37421daa11785016e9ad83f2fce04c92b960b40955f`  
		Last Modified: Thu, 11 Jan 2024 05:08:10 GMT  
		Size: 3.0 MB (2969765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
