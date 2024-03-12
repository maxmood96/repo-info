## `python:slim-bullseye`

```console
$ docker pull python@sha256:0c93bc21260500c52ab687466ae22a20ea4b34fc77ec9ac6bf031f5272a057bc
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
$ docker pull python@sha256:94807e1ea3cf5bc799fcc2e7f754ae7b67879903b44ff9590ad4120b5f4003d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46698910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad59f1de882e4123dc46d331b34665ce6cd5dcd5333862869f4377900a05e65`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0ce72dbd5289c0e02b1d98f7747653636ee970942af7482d50315cca6df0de`  
		Last Modified: Tue, 13 Feb 2024 11:13:19 GMT  
		Size: 1.1 MB (1076589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9d44fb7926c1f5960d3547f1db56c51fdb2824919cb181fee3902c8658b7f1`  
		Last Modified: Tue, 13 Feb 2024 11:14:22 GMT  
		Size: 11.2 MB (11210366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801b91790fe70a4e405b8495c52649c70557c164d2e0c45f222ed7a3447e5926`  
		Last Modified: Tue, 13 Feb 2024 11:14:20 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7453ed7e92bd22eb26a75288cedec46c576ddbe3f1e0ce55d044020233cc36c9`  
		Last Modified: Tue, 13 Feb 2024 11:14:21 GMT  
		Size: 3.0 MB (2989287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:slim-bullseye` - linux; arm variant v5

```console
$ docker pull python@sha256:d992b7b22963064571fdd740e3811585514da967642713a0ff3c2525adb5e137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43878980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee2502dceae8ba9ec763438934b5b22195600660020eaed33e2531884f439ed`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:47 GMT
ADD file:90e7b77db704f73ce102dcbc0f6cbe5d778409a08ca0d29224ab736a76537669 in / 
# Tue, 12 Mar 2024 00:48:47 GMT
CMD ["bash"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:5f50de7913c8d45142222ead3575799095853dd5af08b7c42fe0f070c5947afc`  
		Last Modified: Tue, 12 Mar 2024 00:52:28 GMT  
		Size: 28.9 MB (28924563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9079355558ace9e1791c1fa4b575fb402fddbc59ac1d87d7c802c81e960bd17a`  
		Last Modified: Tue, 12 Mar 2024 07:54:54 GMT  
		Size: 1.1 MB (1059921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9019ae4e816aef9d262e893f0a3b71313c68c6f86e68d53b367a5df07a03781`  
		Last Modified: Tue, 12 Mar 2024 07:55:59 GMT  
		Size: 10.9 MB (10905357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3debdcf6f032a19df47293f04f8e8a2f102a2ccdf9fa63bbfb1834c6532a2370`  
		Last Modified: Tue, 12 Mar 2024 07:55:56 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c6e82356bd1e466b14de4db6a316d9f44e1cf45344ac09ef6a00e8295e566b`  
		Last Modified: Tue, 12 Mar 2024 07:55:58 GMT  
		Size: 3.0 MB (2988897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:slim-bullseye` - linux; arm variant v7

```console
$ docker pull python@sha256:47db36cfdefff6e5215c51ebc9ed3bc9f46153d8c3ccf4d0a5093b22fd025653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41078721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab47c37633867c088c68c767003e00b521fae3d609565bd0774c818d44276dd4`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:38 GMT
ADD file:f0436b046c7a5f796efae4d2d2be5a99ad212807e4aa49fc8cc372a4c4c8c4b0 in / 
# Tue, 12 Mar 2024 00:59:38 GMT
CMD ["bash"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:5b16029f28c496dabb357a7310d24f957046a925411ccd44eca962c03f85e38e`  
		Last Modified: Tue, 12 Mar 2024 01:04:23 GMT  
		Size: 26.6 MB (26582714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b356a650895887f2dff41fd74528a07c2c12caf7a8a33e48c08a3440e538e5b4`  
		Last Modified: Tue, 12 Mar 2024 06:46:06 GMT  
		Size: 1.0 MB (1042014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f9e996d79ca3c81f6865e1f3f238adca81244f294329efc10e5f3218f415f5`  
		Last Modified: Tue, 12 Mar 2024 06:47:09 GMT  
		Size: 10.5 MB (10464542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8deb6a799bb4b67ba64c4beee6012434316c8213ec9741bbf7ea4bdada469c`  
		Last Modified: Tue, 12 Mar 2024 06:47:07 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e686ad22bce52ce010cb259c2c354ec08fd4fe712716e61e35a556fb1dae033`  
		Last Modified: Tue, 12 Mar 2024 06:47:09 GMT  
		Size: 3.0 MB (2989207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull python@sha256:c95c54a29eda104e441a6e6c74adc3f9249e6bdb9825c77e6092b387aa5c0a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45404890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958164645e2893fa343c9539dd925f69f289dbd4b04519375c0d19f8e058e5e1`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532fd75d6f3a4d86fea3efa8f4b8375dda1eb2ed1a0271860026d72f44ac98f1`  
		Last Modified: Tue, 12 Mar 2024 09:46:57 GMT  
		Size: 1.1 MB (1064441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a10f039496a69d06c62f387eeb28a8bfdfd3387e29fe4b9492cc180d3aca13`  
		Last Modified: Tue, 12 Mar 2024 09:47:57 GMT  
		Size: 11.3 MB (11279602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc107d23b67540803de57cb7415e617835bca54128ecdaffefbc0fb0e458ee`  
		Last Modified: Tue, 12 Mar 2024 09:47:55 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a06dad87cc451c21a35cf1e9a1da9f4fa7847b17de8ddd19d0ba5f9c878e277`  
		Last Modified: Tue, 12 Mar 2024 09:47:56 GMT  
		Size: 3.0 MB (2989486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:slim-bullseye` - linux; 386

```console
$ docker pull python@sha256:fbfd90dae29f6b781f68d5b41cd8896a6c3fbee0675d06d6293ff24017b982cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47794919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7573936d0b8b3cfae9bef47490749b946f3314d7c8777f98a89501cf57093340`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:18 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Tue, 13 Feb 2024 00:39:19 GMT
CMD ["bash"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81aa71ae6d26b7ff4709cef02593dbfaa1d00387d6a94a19984a51edb7f04602`  
		Last Modified: Tue, 13 Feb 2024 14:51:49 GMT  
		Size: 1.1 MB (1089158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f590bbcffcab3f84f74614e3a8977ac61cb899ade43ea6ce67943ab7803b80`  
		Last Modified: Tue, 13 Feb 2024 14:53:04 GMT  
		Size: 11.3 MB (11309075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8404ce3f5abe31a057439030d839ec02afae6460b4f539443063830eb0e465b`  
		Last Modified: Tue, 13 Feb 2024 14:53:01 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5fdd1fe937f098832c845a564603f205b1db1c9a86b654f0b84c901e54962f4`  
		Last Modified: Tue, 13 Feb 2024 14:53:03 GMT  
		Size: 3.0 MB (2989001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:slim-bullseye` - linux; ppc64le

```console
$ docker pull python@sha256:c08d92f265f3a34f5ed8a723ebe60f53ca86c0951242e55c253e53d7a2f9ee10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50905602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f16a73af3fa987d77bbf200145adff951ab89da0a76f146609ae8910ec274cc`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:33 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Tue, 13 Feb 2024 00:39:36 GMT
CMD ["bash"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7c5d48c6f116f8816d1870166cb1bea3c20c501f4c0d2440ffd475824cd8de`  
		Last Modified: Tue, 13 Feb 2024 03:40:53 GMT  
		Size: 1.1 MB (1095207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9e5862a1f08112c75fbead6eb9ebbca68929785f919ddb39666e5d8654645e`  
		Last Modified: Tue, 13 Feb 2024 03:41:34 GMT  
		Size: 11.5 MB (11522460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d90bd86cda3e08e5a45ed9d20417841bd9ee24821e847f30032ccf2a8120e6`  
		Last Modified: Tue, 13 Feb 2024 03:41:31 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920340b60644851f61ced0a0513b9922da9e3861a95e55f839c47b26cd7080d7`  
		Last Modified: Tue, 13 Feb 2024 03:41:32 GMT  
		Size: 3.0 MB (2989893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:slim-bullseye` - linux; s390x

```console
$ docker pull python@sha256:dc3e79b4b2f8addc8015981322d0024143e71629264cd0ee88a696e6bb27becb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44883163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6945916687f4078342a806cd4f8917e3d4a665cdf70f9490c2e16529b27e827`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:49 GMT
ADD file:e121f5164f2335792d17befe564e4a4caf1dec33d5039c8245ce418144782215 in / 
# Tue, 12 Mar 2024 00:57:50 GMT
CMD ["bash"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:840335d52e6c781c13aaaed8df36659831a5cb0747048da9bf578dd19a02b30e`  
		Last Modified: Tue, 12 Mar 2024 01:21:45 GMT  
		Size: 29.7 MB (29660245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f3413722f739c4b7935b6e1a07231dd5ab107b48e54cf5c49c765475af556a`  
		Last Modified: Tue, 12 Mar 2024 07:57:44 GMT  
		Size: 1.1 MB (1076135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48383d937504dba4857aa593c4038c47b26750862aa1aaa0c750bf334b711dd`  
		Last Modified: Tue, 12 Mar 2024 07:58:28 GMT  
		Size: 11.2 MB (11157233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9ecbcc5fe27bba7d357df90eeb02a3a5819e9a58253db3e52a812bc1ead8aa`  
		Last Modified: Tue, 12 Mar 2024 07:58:27 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bfe55502ce9aefacbfc4a4941c299f850b76e9d2135a2ff68183115d76c0ca`  
		Last Modified: Tue, 12 Mar 2024 07:58:27 GMT  
		Size: 3.0 MB (2989306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
