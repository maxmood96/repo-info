## `hylang:bullseye`

```console
$ docker pull hylang@sha256:235578d6d85e8de1b49ca95ab509bc90d8f46bdc69890bd91013273ea7695844
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

### `hylang:bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:b2d07d9f0d0eba4f4acbfbc9ed4528ab8db686ef339d203c6449761f7ea33653
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54489047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3379f4159b72d10c0d6ad7dcdc3cb732c73c5ee4cf2bdb19fc11a5a2efc36f1a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 07:44:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 07:44:34 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 07:44:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 08:13:58 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 21 Dec 2022 08:13:58 GMT
ENV PYTHON_VERSION=3.11.1
# Wed, 21 Dec 2022 08:28:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 21 Dec 2022 08:28:14 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 21 Dec 2022 08:28:14 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Fri, 06 Jan 2023 18:41:43 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 06 Jan 2023 18:41:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Fri, 06 Jan 2023 18:41:43 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Fri, 06 Jan 2023 18:41:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Fri, 06 Jan 2023 18:41:54 GMT
CMD ["python3"]
# Fri, 06 Jan 2023 19:05:46 GMT
ENV HY_VERSION=0.25.0
# Fri, 06 Jan 2023 19:05:46 GMT
ENV HYRULE_VERSION=0.2.1
# Fri, 06 Jan 2023 19:05:58 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Fri, 06 Jan 2023 19:05:58 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f487a3359db51ac4dbd797f76b61641328818f50fafc53d2cf760bc63584293`  
		Last Modified: Wed, 21 Dec 2022 09:51:37 GMT  
		Size: 1.1 MB (1076322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a081ff2e6f9880e1a4f95feff6dd524a3f04cb1ae274c319ef11c14b74fa8b4`  
		Last Modified: Wed, 21 Dec 2022 09:52:08 GMT  
		Size: 12.6 MB (12589019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb74cc1c8e1b85e54b38e82e12d6a3a70073aa3ad6694f2d1064ad624d681adb`  
		Last Modified: Wed, 21 Dec 2022 09:52:06 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8311e684bf421255b3cd1bd6012299495c99dcdfd77f315d3e60be4bf51945`  
		Last Modified: Fri, 06 Jan 2023 18:47:18 GMT  
		Size: 3.3 MB (3348159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5904abd3599db63fa948d5bbd499d068d5d415775789321507e2e341dbc596`  
		Last Modified: Fri, 06 Jan 2023 19:10:45 GMT  
		Size: 6.1 MB (6078370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:bullseye` - linux; arm variant v5

```console
$ docker pull hylang@sha256:b21b4dbebdfafbb6c0953febd8a02d3d0d302735d3cc9c4dd62d8f7ad7c7f942
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51526510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c1a12a9ea49ed7a662dee4ebdd8b08f710161f393deb4f8c2afc907f8ddce2`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 11 Jan 2023 01:55:36 GMT
ADD file:f279d5ada9c5980d920c7b9ff126ce11ec9499a532ea3bfd8b717de3348c8439 in / 
# Wed, 11 Jan 2023 01:55:37 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 07:40:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 07:40:49 GMT
ENV LANG=C.UTF-8
# Wed, 11 Jan 2023 07:40:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 08:24:58 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 11 Jan 2023 08:24:59 GMT
ENV PYTHON_VERSION=3.11.1
# Wed, 11 Jan 2023 08:47:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 11 Jan 2023 08:47:33 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 11 Jan 2023 08:47:33 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Wed, 11 Jan 2023 08:47:33 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Wed, 11 Jan 2023 08:47:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 11 Jan 2023 08:47:33 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 11 Jan 2023 08:47:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 11 Jan 2023 08:47:51 GMT
CMD ["python3"]
# Wed, 11 Jan 2023 15:25:09 GMT
ENV HY_VERSION=0.25.0
# Wed, 11 Jan 2023 15:25:09 GMT
ENV HYRULE_VERSION=0.2.1
# Wed, 11 Jan 2023 15:25:21 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 11 Jan 2023 15:25:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:77f56a6f12b7a55a95e6f2c8beadc0eb0243b5881f73f45d09c343f2a8926d62`  
		Last Modified: Wed, 11 Jan 2023 02:00:42 GMT  
		Size: 28.9 MB (28898675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45935e69698e20598038886784c69933330f7adebef776084e760dcb0200680`  
		Last Modified: Wed, 11 Jan 2023 10:07:24 GMT  
		Size: 1.1 MB (1059616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aba8316e048aec5c155cb9548cdd64cdd016fbe96b3b1ff338556dbdac1374b`  
		Last Modified: Wed, 11 Jan 2023 10:08:06 GMT  
		Size: 12.1 MB (12145021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98365d1956e2a5b320349b7448ed8090d6be33707460697c97b60a4bc839a595`  
		Last Modified: Wed, 11 Jan 2023 10:08:04 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d41844aa12d2cc6cf4b3c9e05569e7ec2aa755185e81c34d62f42480a16cfec`  
		Last Modified: Wed, 11 Jan 2023 10:08:04 GMT  
		Size: 3.3 MB (3347391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e169705d5d01e44a2188da404b423c314a509baf94e00c05f0cf42c9eb038d`  
		Last Modified: Wed, 11 Jan 2023 15:28:43 GMT  
		Size: 6.1 MB (6075574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:d61145c533a2370d0877298ebd0a8a1b4682190e0a884dea11211e174b411e2f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48670909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:473668d3c30144701e86d99a8b1f97f053557ac9652c8d71294aebbd30e7b5b4`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 21 Dec 2022 01:58:25 GMT
ADD file:d62015d4eb206b606ae0bc76253de55403ede851d6fae0277e76bdaed196a848 in / 
# Wed, 21 Dec 2022 01:58:26 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 07:34:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 07:34:19 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 07:34:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 09:03:03 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 21 Dec 2022 09:03:03 GMT
ENV PYTHON_VERSION=3.11.1
# Wed, 21 Dec 2022 09:25:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 21 Dec 2022 09:25:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 21 Dec 2022 09:25:02 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Fri, 06 Jan 2023 23:34:04 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 06 Jan 2023 23:34:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Fri, 06 Jan 2023 23:34:04 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Fri, 06 Jan 2023 23:34:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Fri, 06 Jan 2023 23:34:17 GMT
CMD ["python3"]
# Sat, 07 Jan 2023 00:21:46 GMT
ENV HY_VERSION=0.25.0
# Sat, 07 Jan 2023 00:21:46 GMT
ENV HYRULE_VERSION=0.2.1
# Sat, 07 Jan 2023 00:21:58 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Sat, 07 Jan 2023 00:21:59 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f8686edc9eb6f431c8c17a5eddc7bd38917d3b2d7835970d4fdb2ad0db464766`  
		Last Modified: Wed, 21 Dec 2022 02:05:08 GMT  
		Size: 26.6 MB (26559455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438a6125113825e38ede085db815d8fec93954f18e387e25ff99c80c426b40e2`  
		Last Modified: Wed, 21 Dec 2022 15:46:02 GMT  
		Size: 1.0 MB (1041575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2985bfe829b2880369dde74a6aecf5be5df4c53417fbf386296194cab1e94fd4`  
		Last Modified: Wed, 21 Dec 2022 15:47:18 GMT  
		Size: 11.6 MB (11646537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d670af71a8170e19536de5914fff0cdce73cff1284a4531551084504dc4a78`  
		Last Modified: Wed, 21 Dec 2022 15:47:16 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0672c4cda79d9d649172ad532f750d7903572424c77cfaa6851123de211be10a`  
		Last Modified: Fri, 06 Jan 2023 23:44:50 GMT  
		Size: 3.3 MB (3347552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1fda9a3791b393aef49fa430c1c96e34c7c2fb20ff905abb0151d36903ef0c`  
		Last Modified: Sat, 07 Jan 2023 00:30:54 GMT  
		Size: 6.1 MB (6075556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:e3703d3b6d011846be43f65e185c28272b47a3214c0a36d7e9be3c066d49b1d6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53174621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b2447dc4ac117b20bfe6389c5cd7e9cd4717c0a19d883c54469e4aad689479`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 08:46:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 08:46:23 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 08:46:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 09:39:58 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 21 Dec 2022 09:39:58 GMT
ENV PYTHON_VERSION=3.11.1
# Wed, 21 Dec 2022 09:53:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 21 Dec 2022 09:53:45 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 21 Dec 2022 09:53:45 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Fri, 06 Jan 2023 20:53:16 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 06 Jan 2023 20:53:16 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Fri, 06 Jan 2023 20:53:16 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Fri, 06 Jan 2023 20:53:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Fri, 06 Jan 2023 20:53:26 GMT
CMD ["python3"]
# Fri, 06 Jan 2023 21:27:29 GMT
ENV HY_VERSION=0.25.0
# Fri, 06 Jan 2023 21:27:29 GMT
ENV HYRULE_VERSION=0.2.1
# Fri, 06 Jan 2023 21:27:39 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Fri, 06 Jan 2023 21:27:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce1f4048a78497d1b06b07487a1f0b24b5260d0b19065df630a81d22453a00a`  
		Last Modified: Wed, 21 Dec 2022 12:01:48 GMT  
		Size: 1.1 MB (1064161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e68599b131bb8af1667bb92fcebb428cd6743eccc15950e78f030ba2840cea0`  
		Last Modified: Wed, 21 Dec 2022 12:02:45 GMT  
		Size: 12.6 MB (12639397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b52f1d8532e4ebe805671ea2a990c1781601b8f8125ae1cc7206aa099c270e`  
		Last Modified: Wed, 21 Dec 2022 12:02:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0104d7bce7efe690637598bbf5297c3bf83a88794cb99a189d3a4aad04957cc4`  
		Last Modified: Fri, 06 Jan 2023 20:58:46 GMT  
		Size: 3.3 MB (3347834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2539d5847b86935519af75792c7ccbc5b71ed5422f41b5466bca17a687c9613`  
		Last Modified: Fri, 06 Jan 2023 21:32:24 GMT  
		Size: 6.1 MB (6078224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:bullseye` - linux; 386

```console
$ docker pull hylang@sha256:fee48f625c83fa5559cdb4ec40cd2735112d5a251456163b9eb65d0ef9ac26f1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.4 MB (55361729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061980564cba541e4ada26b4f5042d8f9ec123ea0f204b49fd5220a952f0c790`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:22 GMT
ADD file:5f553fdf893bb3198d173c48f4531e9bfdbab61798c1aa8217fd80e9d686d7ae in / 
# Wed, 21 Dec 2022 01:39:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 10:22:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 10:22:37 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 10:22:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:39:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 21 Dec 2022 11:40:00 GMT
ENV PYTHON_VERSION=3.11.1
# Wed, 21 Dec 2022 11:58:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 21 Dec 2022 11:58:50 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 21 Dec 2022 11:58:51 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Fri, 06 Jan 2023 18:42:56 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 06 Jan 2023 18:42:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Fri, 06 Jan 2023 18:42:58 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Fri, 06 Jan 2023 18:43:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Fri, 06 Jan 2023 18:43:11 GMT
CMD ["python3"]
# Fri, 06 Jan 2023 19:12:18 GMT
ENV HY_VERSION=0.25.0
# Fri, 06 Jan 2023 19:12:18 GMT
ENV HYRULE_VERSION=0.2.1
# Fri, 06 Jan 2023 19:12:33 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Fri, 06 Jan 2023 19:12:33 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3228cb514e81f042720b7fd118ace0f279d1a4bc422b7e24189514a574dfa546`  
		Last Modified: Wed, 21 Dec 2022 01:44:46 GMT  
		Size: 32.4 MB (32375745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abde5e2eabe9ac55bd32be43e299138701b9b17dcbf806da92c2ec9d95f886fe`  
		Last Modified: Wed, 21 Dec 2022 15:04:28 GMT  
		Size: 1.1 MB (1088469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818d4cbc0808a665f919966a94f5376beecbd502be2858a22dba80d499c0b2dc`  
		Last Modified: Wed, 21 Dec 2022 15:05:35 GMT  
		Size: 12.7 MB (12689201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb74b0c8ed5ee2a91c617607e87292d0d99ae1c1774299dbae1fc5377dd87f2b`  
		Last Modified: Wed, 21 Dec 2022 15:05:33 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad1622268bb0afc87dd8314ead33e25e6a608de5bfc7fc3ad6891ad1549368a`  
		Last Modified: Fri, 06 Jan 2023 18:52:55 GMT  
		Size: 3.1 MB (3132486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1d2e16a91743aeeb5ffdc4b6bd8302806f2dd6d11daefe7f33a68e8538fc73`  
		Last Modified: Fri, 06 Jan 2023 19:21:31 GMT  
		Size: 6.1 MB (6075594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:bullseye` - linux; ppc64le

```console
$ docker pull hylang@sha256:6f24aa96a43596cff7945aab75f5759bcc8fc69d9f77dfccd7b2df927c864026
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58745040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81121dcc0887e9b5e5a2627ac3030fca50619eba514bd6aec6b95313f7806834`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:41 GMT
ADD file:5ab731e5c1e145738476449b6b0748f44822bb2cd6c53ae5bbf6ae6bfec83383 in / 
# Wed, 21 Dec 2022 01:17:43 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 09:13:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 09:13:20 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 09:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 10:46:33 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 21 Dec 2022 10:46:33 GMT
ENV PYTHON_VERSION=3.11.1
# Wed, 21 Dec 2022 11:34:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 21 Dec 2022 11:34:18 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 21 Dec 2022 11:34:18 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Fri, 06 Jan 2023 20:50:23 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 06 Jan 2023 20:50:23 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Fri, 06 Jan 2023 20:50:24 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Fri, 06 Jan 2023 20:50:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Fri, 06 Jan 2023 20:50:46 GMT
CMD ["python3"]
# Fri, 06 Jan 2023 21:31:56 GMT
ENV HY_VERSION=0.25.0
# Fri, 06 Jan 2023 21:31:56 GMT
ENV HYRULE_VERSION=0.2.1
# Fri, 06 Jan 2023 21:32:21 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Fri, 06 Jan 2023 21:32:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ba010cdd67bb149ba042a834d84020887fc3f8ca9d8e51b31f3104286cafb9ba`  
		Last Modified: Wed, 21 Dec 2022 01:23:22 GMT  
		Size: 35.3 MB (35268748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93a8b8ac08b88c89904606a3d4c83a35d7d5413b497628a5c25ed66b3d82465`  
		Last Modified: Wed, 21 Dec 2022 14:09:10 GMT  
		Size: 1.1 MB (1094708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b528b67d5c0ea2108d826ab02274cfe879157aa3bebb8d32f38ced684109374`  
		Last Modified: Wed, 21 Dec 2022 14:10:03 GMT  
		Size: 13.0 MB (12954429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22c105b6cf566b9740705717b5822c06d182044291fef4fa6aa5d1d03afd0ad`  
		Last Modified: Wed, 21 Dec 2022 14:09:59 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95987e5e06eb22cbd15b78a823e28bd7083e4b2bea177a8c4ade936a0e77c259`  
		Last Modified: Fri, 06 Jan 2023 20:58:05 GMT  
		Size: 3.3 MB (3348326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6505f5e37c725c16fec6f23199e6a7f962f926d73d5b1003a77699b2806b0e8f`  
		Last Modified: Fri, 06 Jan 2023 21:39:44 GMT  
		Size: 6.1 MB (6078595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:bullseye` - linux; s390x

```console
$ docker pull hylang@sha256:1eb856ffdefc7fda4fcb5881ed5a1f7ae49803bd4142e18f76e21648b67b32d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52554567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38781faf70886d8c22c937467104d69ff0b3b0ee0e0be45704befe3b3abe6a25`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 11 Jan 2023 02:22:23 GMT
ADD file:14f332233d8fa1ca519992e52aaf550bcee52d346c375e94ee73d36864933f8e in / 
# Wed, 11 Jan 2023 02:22:25 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 07:14:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 07:14:46 GMT
ENV LANG=C.UTF-8
# Wed, 11 Jan 2023 07:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 07:39:42 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 11 Jan 2023 07:39:43 GMT
ENV PYTHON_VERSION=3.11.1
# Wed, 11 Jan 2023 07:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 11 Jan 2023 07:51:59 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 11 Jan 2023 07:51:59 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Wed, 11 Jan 2023 07:52:00 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Wed, 11 Jan 2023 07:52:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 11 Jan 2023 07:52:00 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 11 Jan 2023 07:52:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 11 Jan 2023 07:52:10 GMT
CMD ["python3"]
# Wed, 11 Jan 2023 15:16:46 GMT
ENV HY_VERSION=0.25.0
# Wed, 11 Jan 2023 15:16:46 GMT
ENV HYRULE_VERSION=0.2.1
# Wed, 11 Jan 2023 15:16:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 11 Jan 2023 15:16:56 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5895b3b9300287ac4aca79440c1c4979b6d4fad1ceb06fba32443d012c83cc37`  
		Last Modified: Wed, 11 Jan 2023 02:26:52 GMT  
		Size: 29.6 MB (29629731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b3a8ce85ae9cc67b14819342062a49b17a9d8f37c30baf9e402eb388373d44`  
		Last Modified: Wed, 11 Jan 2023 08:45:13 GMT  
		Size: 1.1 MB (1075803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c7f2bf950f3e397bae0f61f66c2292c9cfc4d95de68eeb6c7a11ed48ac3fd3`  
		Last Modified: Wed, 11 Jan 2023 08:45:43 GMT  
		Size: 12.4 MB (12422673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11832ecd254f96182fd69704278c48a6d37a49f1b3b08eff5729c3bc55c51821`  
		Last Modified: Wed, 11 Jan 2023 08:45:41 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7206eb2e955e038fa8c84fd33cff7e11d6ba934a037439eda20d8e645b96c3`  
		Last Modified: Wed, 11 Jan 2023 08:45:42 GMT  
		Size: 3.3 MB (3347718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e975a425a11a902ac627613765256b5a592b2165d5570b5ad0961b6bfed60073`  
		Last Modified: Wed, 11 Jan 2023 15:22:45 GMT  
		Size: 6.1 MB (6078409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
