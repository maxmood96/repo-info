## `hylang:latest`

```console
$ docker pull hylang@sha256:2845158113802488c6b296afa3d53d4c00466088e821329be30ab133c3ba92a6
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

### `hylang:latest` - linux; amd64

```console
$ docker pull hylang@sha256:4122240aa9261215d8ed652698e15651e5a4878879de71e77e06141ac30b0a12
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50518351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4c165f134bafb197c1ec3814c264ab0004ceca0e6194bb087a0b9c2cd9f016`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 11 May 2022 01:20:16 GMT
ADD file:4a0bb88956083aa56032fdd9601d9b66c39b18c896ba35ea33594cd75621640a in / 
# Wed, 11 May 2022 01:20:16 GMT
CMD ["bash"]
# Wed, 11 May 2022 06:25:15 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 06:25:15 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 06:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 06:25:20 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 11 May 2022 07:18:06 GMT
ENV PYTHON_VERSION=3.10.4
# Wed, 11 May 2022 07:28:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 11 May 2022 07:28:29 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 11 May 2022 07:28:29 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Wed, 11 May 2022 07:28:29 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 25 May 2022 21:16:53 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a312303dbd516f6a692f2fee59852701bd828dd8/public/get-pip.py
# Wed, 25 May 2022 21:16:53 GMT
ENV PYTHON_GET_PIP_SHA256=8dd03e99645c19f49bbb629ce65c46b665ee92a1d94d246418bad6afade89f8d
# Wed, 25 May 2022 21:17:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 25 May 2022 21:17:05 GMT
CMD ["python3"]
# Thu, 26 May 2022 00:47:16 GMT
ENV HY_VERSION=1.0a4
# Thu, 26 May 2022 00:47:16 GMT
ENV HYRULE_VERSION=0.1
# Thu, 26 May 2022 00:47:19 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 26 May 2022 00:47:19 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:214ca5fb90323fe769c63a12af092f2572bf1c6b300263e09883909fc865d260`  
		Last Modified: Wed, 11 May 2022 01:25:13 GMT  
		Size: 31.4 MB (31379476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7d81b69b9af8e7d8748b3d3ccc7a4dd28dd7752c0e118ad1f3238d3b5f1ee6`  
		Last Modified: Wed, 11 May 2022 09:14:18 GMT  
		Size: 1.1 MB (1076137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd428def9648cf2ad4b6e1ff0ca5b09204cac37b389c4eacee99cafd753d27d`  
		Last Modified: Wed, 11 May 2022 09:15:21 GMT  
		Size: 11.8 MB (11777073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9d27b71a51878857690766e437f6c2ad8cc6679d7e10811124edef6f1ae82f`  
		Last Modified: Wed, 11 May 2022 09:15:20 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1383d29945270428881e4c762cdb0c3980a1bc48ab1ce72dd7e5b33e4feba9fd`  
		Last Modified: Wed, 25 May 2022 21:52:32 GMT  
		Size: 3.2 MB (3166926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afe225f6fbadbefbba55c6e69e38d161c69e75836107eb428a812bdc95ebb7b`  
		Last Modified: Thu, 26 May 2022 00:50:05 GMT  
		Size: 3.1 MB (3118506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:latest` - linux; arm variant v5

```console
$ docker pull hylang@sha256:94d032e14bab3ad5232359c82d8a1f4453782176275c5526d48229da89c24971
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49022470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035d2de9915156c4858a4a22c158b295206b2dc30a7e87138b3191deba140699`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 11 May 2022 00:50:34 GMT
ADD file:72357b75d7e4546f06abf4648ab600980e742a3017f36da3c7a6c086f2f5fb56 in / 
# Wed, 11 May 2022 00:50:35 GMT
CMD ["bash"]
# Wed, 11 May 2022 14:09:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 14:09:36 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 14:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 14:09:56 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 11 May 2022 16:08:03 GMT
ENV PYTHON_VERSION=3.10.4
# Wed, 18 May 2022 05:29:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 18 May 2022 05:29:34 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 18 May 2022 05:29:34 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Wed, 18 May 2022 05:29:35 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 25 May 2022 18:52:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a312303dbd516f6a692f2fee59852701bd828dd8/public/get-pip.py
# Wed, 25 May 2022 18:52:13 GMT
ENV PYTHON_GET_PIP_SHA256=8dd03e99645c19f49bbb629ce65c46b665ee92a1d94d246418bad6afade89f8d
# Wed, 25 May 2022 18:52:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 25 May 2022 18:52:47 GMT
CMD ["python3"]
# Wed, 25 May 2022 19:35:59 GMT
ENV HY_VERSION=1.0a4
# Wed, 25 May 2022 19:36:00 GMT
ENV HYRULE_VERSION=0.1
# Wed, 25 May 2022 19:36:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 25 May 2022 19:36:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f7b69be15db1cb94a249f74b27edd4f5e5923a8701b026179a593f6888e897aa`  
		Last Modified: Wed, 11 May 2022 01:05:51 GMT  
		Size: 28.9 MB (28921122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637f39db37a79ee09ab6121c88f50fcfde02bad8a712854fa636f78fc72a8d33`  
		Last Modified: Thu, 12 May 2022 13:08:46 GMT  
		Size: 1.1 MB (1059465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e4ef87599a4c88e42a0f14bb89cfb56f26d10c48a0cc95f89ac12d61667928`  
		Last Modified: Wed, 18 May 2022 07:00:41 GMT  
		Size: 12.8 MB (12756386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0e6884c2b87d1219bc823a940fa2ba7b6a0dbc6be06b5ad2ba32246e66f05e`  
		Last Modified: Wed, 18 May 2022 07:00:33 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c962b7794e8ded8345e502f97e2a855c0a3b324593462c7ee63097e7f7b426`  
		Last Modified: Wed, 25 May 2022 19:08:06 GMT  
		Size: 3.2 MB (3166697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71781a078594abd7a4ac8f0ceb1ed19eccfebcaeae07a903c2794cd403d68afa`  
		Last Modified: Wed, 25 May 2022 19:40:56 GMT  
		Size: 3.1 MB (3118566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:latest` - linux; arm variant v7

```console
$ docker pull hylang@sha256:899d40389ece3b19907e84348fb47845416e8dddd196c78fc681500bfbad7480
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44777782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a1381478874bc72a00f633e057ace08e4bfbe4467f966063ce36237a17e1b6`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 11 May 2022 01:49:07 GMT
ADD file:7c0451fffe8a520c2ab23048948d76bfe0dc0d90298c3d859279ccd8815b84f6 in / 
# Wed, 11 May 2022 01:49:08 GMT
CMD ["bash"]
# Wed, 11 May 2022 22:35:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 22:35:41 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 22:35:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 22:35:58 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 12 May 2022 01:51:42 GMT
ENV PYTHON_VERSION=3.10.4
# Thu, 12 May 2022 02:26:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Thu, 12 May 2022 02:26:59 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 12 May 2022 02:26:59 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Thu, 12 May 2022 02:26:59 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 25 May 2022 22:03:31 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a312303dbd516f6a692f2fee59852701bd828dd8/public/get-pip.py
# Wed, 25 May 2022 22:03:31 GMT
ENV PYTHON_GET_PIP_SHA256=8dd03e99645c19f49bbb629ce65c46b665ee92a1d94d246418bad6afade89f8d
# Wed, 25 May 2022 22:04:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 25 May 2022 22:04:01 GMT
CMD ["python3"]
# Thu, 26 May 2022 05:20:57 GMT
ENV HY_VERSION=1.0a4
# Thu, 26 May 2022 05:20:58 GMT
ENV HYRULE_VERSION=0.1
# Thu, 26 May 2022 05:21:05 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 26 May 2022 05:21:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1a9427b75b1c1db800cae7a9199bb4e508702e6761b17cc904d21441df43016c`  
		Last Modified: Wed, 11 May 2022 02:04:35 GMT  
		Size: 26.6 MB (26575672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526ff35074445b92acef69cb3d3e497aad5d1e536b01e937c800b0c7cc33714c`  
		Last Modified: Thu, 12 May 2022 07:41:57 GMT  
		Size: 1.0 MB (1041444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fd29855f2b44b862dfa95d16e9569562f95ef1d81e57d0bad3459e86c0ec0f`  
		Last Modified: Thu, 12 May 2022 07:43:40 GMT  
		Size: 10.9 MB (10875241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff025e24c7cd35445f29b19e44400802dfeb964873aa5e7448332b1b96f38c4b`  
		Last Modified: Thu, 12 May 2022 07:43:36 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5968d2e05877070589311d335298a0369417615f4cfb072f9eabbc377af08389`  
		Last Modified: Wed, 25 May 2022 23:41:00 GMT  
		Size: 3.2 MB (3166529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa23840de0b0bb9b7f373bbed0a589a2adb956c9c3f990898165e7a576e758e2`  
		Last Modified: Thu, 26 May 2022 05:30:07 GMT  
		Size: 3.1 MB (3118663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:latest` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:8b21eeebac61ffc859932d87e709d238ac82febeb8c843ef13c4abe8b78cfd20
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48809246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f3924b22acb6fa9cd85a9c23f2a3e21e049ce646eef17942ce18d5b14fe7d1`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 11 May 2022 00:46:59 GMT
ADD file:158a0e401328bd7c0d49b9e8539186098967218f1b1a8c811f4398d29b74397f in / 
# Wed, 11 May 2022 00:47:00 GMT
CMD ["bash"]
# Wed, 11 May 2022 09:04:46 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 09:04:47 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 09:04:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 09:04:53 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 11 May 2022 10:03:19 GMT
ENV PYTHON_VERSION=3.10.4
# Wed, 11 May 2022 10:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 11 May 2022 10:13:31 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 11 May 2022 10:13:32 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Wed, 11 May 2022 10:13:33 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 25 May 2022 22:35:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a312303dbd516f6a692f2fee59852701bd828dd8/public/get-pip.py
# Wed, 25 May 2022 22:35:44 GMT
ENV PYTHON_GET_PIP_SHA256=8dd03e99645c19f49bbb629ce65c46b665ee92a1d94d246418bad6afade89f8d
# Wed, 25 May 2022 22:35:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 25 May 2022 22:35:57 GMT
CMD ["python3"]
# Thu, 26 May 2022 02:15:37 GMT
ENV HY_VERSION=1.0a4
# Thu, 26 May 2022 02:15:38 GMT
ENV HYRULE_VERSION=0.1
# Thu, 26 May 2022 02:15:42 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 26 May 2022 02:15:42 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:dfdd5ffb257742b891ccad9400a77dad2a6260b2451e0f5e48a9ade1d17a87ec`  
		Last Modified: Wed, 11 May 2022 00:53:46 GMT  
		Size: 30.1 MB (30065693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d252b4015fa93dc9f330d813bf7ba931736380ec2d1388cfd347ebeac41de7`  
		Last Modified: Wed, 11 May 2022 11:49:01 GMT  
		Size: 858.7 KB (858739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b59bfc67f1ca7ca2ca49725003bd4b24f85a15eccd70d4df5dbd61ea3871248`  
		Last Modified: Wed, 11 May 2022 11:50:12 GMT  
		Size: 11.8 MB (11820102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5753104512bd9af8aa5d0f94da4f9f19620d3ea47890ef0d74c0e37d3ef771b8`  
		Last Modified: Wed, 11 May 2022 11:50:10 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7df0e3e521fe5307472798c41cdce2a82237c9b21958f9fadde839e536bdef`  
		Last Modified: Wed, 25 May 2022 23:24:54 GMT  
		Size: 2.9 MB (2947723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2e2f16890be6ea8d92d280b2c847497f0018f9d09d8943a8693a4dca90dc92`  
		Last Modified: Thu, 26 May 2022 02:21:20 GMT  
		Size: 3.1 MB (3116756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:latest` - linux; 386

```console
$ docker pull hylang@sha256:c5f1de364b2ba32ee71c1f0c082fb30c2966c8983a6cd20028ae70ed24f94467
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51230275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837bb968e2eeb1e3be22610452dae0b1ced4da90d7ac9a6fa548bcc15c024387`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 28 May 2022 00:39:33 GMT
ADD file:8320d7b95b9f68313e086faff974bb38977e0c9da4984afb6382eb0405742bde in / 
# Sat, 28 May 2022 00:39:33 GMT
CMD ["bash"]
# Sat, 28 May 2022 08:30:25 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 08:30:25 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 08:30:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 08:30:31 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 28 May 2022 09:43:18 GMT
ENV PYTHON_VERSION=3.10.4
# Sat, 28 May 2022 09:55:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Sat, 28 May 2022 09:55:18 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 28 May 2022 09:55:19 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Sat, 28 May 2022 09:55:20 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Sat, 28 May 2022 09:55:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a312303dbd516f6a692f2fee59852701bd828dd8/public/get-pip.py
# Sat, 28 May 2022 09:55:22 GMT
ENV PYTHON_GET_PIP_SHA256=8dd03e99645c19f49bbb629ce65c46b665ee92a1d94d246418bad6afade89f8d
# Sat, 28 May 2022 09:55:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Sat, 28 May 2022 09:55:36 GMT
CMD ["python3"]
# Sat, 28 May 2022 15:49:11 GMT
ENV HY_VERSION=1.0a4
# Sat, 28 May 2022 15:49:11 GMT
ENV HYRULE_VERSION=0.1
# Sat, 28 May 2022 15:49:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Sat, 28 May 2022 15:49:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5e7494d2ee6c81c73ce32f8bde3ea8658c6224c2cc22d7bb01df4bc3d42949aa`  
		Last Modified: Sat, 28 May 2022 00:46:43 GMT  
		Size: 32.4 MB (32390321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aee27a6f82fff07c9af81db999fc2b2d65f9ecb3b14fbecccd268f45121f7b6`  
		Last Modified: Sat, 28 May 2022 11:38:03 GMT  
		Size: 883.6 KB (883566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f541c5e2ba1790c818fd67304868f3abefbc96f71b8ced7fdb55d8fda9b0ba9`  
		Last Modified: Sat, 28 May 2022 11:39:16 GMT  
		Size: 11.9 MB (11891968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ef9d2f42ee40c18e4262cadbde753327f782d3113a466ad657b85225ce2219`  
		Last Modified: Sat, 28 May 2022 11:39:14 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa2288ba4888a010f2940f79fcbc1e0651f77b9fc80e28f296646e925dd72ec`  
		Last Modified: Sat, 28 May 2022 11:39:15 GMT  
		Size: 2.9 MB (2947573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926e18695984aa99f4e3cc04faa458327221253afc0ad4f8841725c75556b1b5`  
		Last Modified: Sat, 28 May 2022 15:55:11 GMT  
		Size: 3.1 MB (3116615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:latest` - linux; ppc64le

```console
$ docker pull hylang@sha256:9cca4da66cad31d91e37c9b388ff1d142db73e351244feb77ea2b258a2ad1d14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54809667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a96d449a0455e15efedc12a1b741ec234f4805daf57bfa9fcb73ae297b7ca2d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 11 May 2022 01:32:29 GMT
ADD file:1e94716789ec21981460f74be38a668bc212bd804c1d41cecf90036a5bccac5a in / 
# Wed, 11 May 2022 01:32:34 GMT
CMD ["bash"]
# Wed, 11 May 2022 21:00:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 21:00:05 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 21:00:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 21:00:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 11 May 2022 23:11:42 GMT
ENV PYTHON_VERSION=3.10.4
# Wed, 11 May 2022 23:39:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 11 May 2022 23:39:23 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 11 May 2022 23:39:30 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Wed, 11 May 2022 23:39:35 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 25 May 2022 22:34:05 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a312303dbd516f6a692f2fee59852701bd828dd8/public/get-pip.py
# Wed, 25 May 2022 22:34:08 GMT
ENV PYTHON_GET_PIP_SHA256=8dd03e99645c19f49bbb629ce65c46b665ee92a1d94d246418bad6afade89f8d
# Wed, 25 May 2022 22:34:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 25 May 2022 22:34:57 GMT
CMD ["python3"]
# Thu, 26 May 2022 04:55:07 GMT
ENV HY_VERSION=1.0a4
# Thu, 26 May 2022 04:55:13 GMT
ENV HYRULE_VERSION=0.1
# Thu, 26 May 2022 04:56:11 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 26 May 2022 04:56:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2533109ed11eefd6415e0370d6d7a3ea879b582b1887c98b819a598ad18fca24`  
		Last Modified: Wed, 11 May 2022 01:43:03 GMT  
		Size: 35.3 MB (35286467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980057956258174120e46894eca1d570f19e6c2ab3421c954c166aa8b1e40ce0`  
		Last Modified: Thu, 12 May 2022 04:10:34 GMT  
		Size: 1.1 MB (1094573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1047af94401654023015562f9b709828c6694104b81453fc97097a8be964ff`  
		Last Modified: Thu, 12 May 2022 04:12:10 GMT  
		Size: 12.1 MB (12140787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411b93b01052104f2ab33503ff058652ca96f2e7bc6f7fd47345a7b50d6d2052`  
		Last Modified: Thu, 12 May 2022 04:12:07 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ca830226b696034541d17ec4feabd4abe9b30c16270cad24c3cb6676efe193`  
		Last Modified: Wed, 25 May 2022 23:53:55 GMT  
		Size: 3.2 MB (3168325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc649a0976feb714bb806abdf433ac8409e9c5918c9f3adcd4675bb210c1016`  
		Last Modified: Thu, 26 May 2022 05:24:41 GMT  
		Size: 3.1 MB (3119282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:latest` - linux; s390x

```console
$ docker pull hylang@sha256:7409e77ffd0340a8b5dd00d3f8cf3d1f1918b554d0a74ea19fd43f1c5d8efe8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48591064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c86f7c985c393d310df9dbacc321c86406747e84347a1dbb3927bc3bdae688`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 11 May 2022 00:44:17 GMT
ADD file:d93a1cf64a813d01774cd628dfd683c006e20159e2ab3464c2159c8d9897c725 in / 
# Wed, 11 May 2022 00:44:19 GMT
CMD ["bash"]
# Wed, 11 May 2022 06:39:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 06:39:54 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 06:39:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 06:39:58 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 11 May 2022 07:23:24 GMT
ENV PYTHON_VERSION=3.10.4
# Wed, 11 May 2022 07:32:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 11 May 2022 07:32:21 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 11 May 2022 07:32:21 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Wed, 11 May 2022 07:32:21 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 25 May 2022 22:17:56 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a312303dbd516f6a692f2fee59852701bd828dd8/public/get-pip.py
# Wed, 25 May 2022 22:17:56 GMT
ENV PYTHON_GET_PIP_SHA256=8dd03e99645c19f49bbb629ce65c46b665ee92a1d94d246418bad6afade89f8d
# Wed, 25 May 2022 22:18:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 25 May 2022 22:18:14 GMT
CMD ["python3"]
# Thu, 26 May 2022 01:52:53 GMT
ENV HY_VERSION=1.0a4
# Thu, 26 May 2022 01:52:54 GMT
ENV HYRULE_VERSION=0.1
# Thu, 26 May 2022 01:53:00 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 26 May 2022 01:53:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9f3750f6094217808e26d471752341db88153c8d5b5f9bb11577b74671303bbc`  
		Last Modified: Wed, 11 May 2022 00:50:03 GMT  
		Size: 29.7 MB (29654739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b56df21812720343417b7387b2763aaa28b9a23746a67bc00c31a2fdd6f6c0`  
		Last Modified: Wed, 11 May 2022 08:55:52 GMT  
		Size: 1.1 MB (1075546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ef772c550c69f3c783079410c28b8083b8159aae91b9b6a989ce13aafc1fb9`  
		Last Modified: Wed, 11 May 2022 08:56:40 GMT  
		Size: 11.6 MB (11575495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d9d476f22c8381dc241a7aacc30b75bd8b967825efeee527c232e49dd56ec1`  
		Last Modified: Wed, 11 May 2022 08:56:39 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a2f65769ff7b1b0f1b0ff0098c341e1da0af13d96cbe5b4d93685bfb93cfba`  
		Last Modified: Wed, 25 May 2022 23:09:29 GMT  
		Size: 3.2 MB (3166378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40af53247399108e5d172f7ee93d734e93b65386445ad067f6c7ee76f2fddcfc`  
		Last Modified: Thu, 26 May 2022 01:59:50 GMT  
		Size: 3.1 MB (3118673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
