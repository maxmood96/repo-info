## `hylang:python3.10-buster`

```console
$ docker pull hylang@sha256:ce4cb470c0e054c8ac1f3bee980e6fbc40ff02a80465a187d8ea7c520a66e97d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:python3.10-buster` - linux; amd64

```console
$ docker pull hylang@sha256:a4adc363e8da324a380ab0fa432b70cdf73d5bd80d1edead54162240470f9c9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49424276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a411674cac81f206be649752c5792e430e0d3500ec45df52dc31b56deba9b25`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:52 GMT
ADD file:660e0093a3da49e4ca41260d09d585754ccb1eff8974c4b0dd4456b76ddbbc9a in / 
# Wed, 21 Dec 2022 01:20:52 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 07:59:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 07:59:14 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 07:59:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 08:28:38 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 21 Dec 2022 08:54:17 GMT
ENV PYTHON_VERSION=3.10.9
# Wed, 21 Dec 2022 09:05:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 21 Dec 2022 09:05:19 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 21 Dec 2022 09:05:19 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Wed, 21 Dec 2022 09:05:19 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 21 Dec 2022 09:05:19 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 21 Dec 2022 09:05:20 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 21 Dec 2022 09:05:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 21 Dec 2022 09:05:32 GMT
CMD ["python3"]
# Wed, 21 Dec 2022 15:36:06 GMT
ENV HY_VERSION=0.25.0
# Wed, 21 Dec 2022 15:36:06 GMT
ENV HYRULE_VERSION=0.2.1
# Wed, 21 Dec 2022 15:36:19 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 21 Dec 2022 15:36:19 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b52ebda398ed2c4602ea06056f78d45a59474ee4e2a020967251ba082424e7e2`  
		Last Modified: Wed, 21 Dec 2022 01:25:17 GMT  
		Size: 27.1 MB (27140331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea3b77facf9f24e5cda370be6af00cfc85988f3140bee862e2529dd50e6eec1`  
		Last Modified: Wed, 21 Dec 2022 09:51:53 GMT  
		Size: 2.8 MB (2781011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e1052e40c0d142dda938e55b91fdacfe5256ebf04c987961b9b97ddddf1074`  
		Last Modified: Wed, 21 Dec 2022 09:53:05 GMT  
		Size: 12.0 MB (12023602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc86fab7159e2a79953db5aa4cb98d170a4aaa0cbfa2eb8642ec92187d9c18e`  
		Last Modified: Wed, 21 Dec 2022 09:53:03 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7da034f8a9bb947ae915fd033cea3ccc2b61b586f175ec98a1ffeb7a9c77d7`  
		Last Modified: Wed, 21 Dec 2022 09:53:03 GMT  
		Size: 3.3 MB (3345360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2880995e7af7e47e885d2798338a2e56acbb71e695206c9f39d1868bd44a1884`  
		Last Modified: Wed, 21 Dec 2022 15:44:29 GMT  
		Size: 4.1 MB (4133738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-buster` - linux; arm variant v7

```console
$ docker pull hylang@sha256:b572e739326fa07d3658d4cf71cd87adcfff7d729eadc69317dfb73ff9c69f89
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43802671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7152f1c3cc29e9aee631d9d547f60894014cee34d5eea10e598004851a953f`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 06 Dec 2022 00:59:27 GMT
ADD file:be297820b3c24f32c3d19e62f8aad3c9d2b37db08077869258a7d3aba92f555f in / 
# Tue, 06 Dec 2022 00:59:27 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 06:41:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 06:41:01 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 06:41:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 07:26:44 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 08 Dec 2022 03:13:08 GMT
ENV PYTHON_VERSION=3.10.9
# Thu, 08 Dec 2022 03:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Thu, 08 Dec 2022 03:26:47 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 08 Dec 2022 03:26:47 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Thu, 08 Dec 2022 03:26:47 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Thu, 08 Dec 2022 03:26:47 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Thu, 08 Dec 2022 03:26:47 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Thu, 08 Dec 2022 03:27:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 08 Dec 2022 03:27:06 GMT
CMD ["python3"]
# Thu, 08 Dec 2022 08:28:06 GMT
ENV HY_VERSION=0.25.0
# Thu, 08 Dec 2022 08:28:06 GMT
ENV HYRULE_VERSION=0.2.1
# Thu, 08 Dec 2022 08:28:18 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 08 Dec 2022 08:28:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f2a5c00904a21a940a9e4ec3efaca80bebbbf2775e4c9bbe0ce9c05e967335f0`  
		Last Modified: Tue, 06 Dec 2022 01:06:56 GMT  
		Size: 22.7 MB (22748937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d58a3430d527ad0efdbb3ea5ee1feaad67d5b4f09beb6ef1687341db104db`  
		Last Modified: Tue, 06 Dec 2022 09:18:22 GMT  
		Size: 2.4 MB (2368371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a3118a7f49f48f532b03689679d6aa910923b6787e6ab07c8dc460172e0f57`  
		Last Modified: Thu, 08 Dec 2022 06:25:43 GMT  
		Size: 11.2 MB (11209321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f754e88c3b6d4f50b4e705a070a79f3dfdf79b27c8144d853647e1d81ff6b6f6`  
		Last Modified: Thu, 08 Dec 2022 06:25:41 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b552227431dd9801025d0029460a79a03517d5a00ce493beaa898bee35f0791`  
		Last Modified: Thu, 08 Dec 2022 06:25:42 GMT  
		Size: 3.3 MB (3344462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5847d92ed8f74fccc5cf3da7816e4235a7fec43990efe2fbedf1546136130db`  
		Last Modified: Thu, 08 Dec 2022 08:42:46 GMT  
		Size: 4.1 MB (4131347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-buster` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:9763760b34fb61fa9ffae7e31aec481556ba74caf4fbee218e94e79e6dbe8f72
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48060688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55581a3649b2695bfff46509dbabe1f48e4459177491934cc6a471e968182f28`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:34 GMT
ADD file:764288ad3920160093c500e1a7277f174a656030bbe3a0511e7925e84495b6ee in / 
# Tue, 06 Dec 2022 01:40:34 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 07:39:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 07:39:16 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 07:39:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 08:33:37 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 08 Dec 2022 01:09:37 GMT
ENV PYTHON_VERSION=3.10.9
# Thu, 08 Dec 2022 01:18:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Thu, 08 Dec 2022 01:18:25 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 08 Dec 2022 01:18:25 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Thu, 08 Dec 2022 01:18:25 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Thu, 08 Dec 2022 01:18:25 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Thu, 08 Dec 2022 01:18:25 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Thu, 08 Dec 2022 01:18:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 08 Dec 2022 01:18:40 GMT
CMD ["python3"]
# Thu, 08 Dec 2022 04:24:19 GMT
ENV HY_VERSION=0.25.0
# Thu, 08 Dec 2022 04:24:19 GMT
ENV HYRULE_VERSION=0.2.1
# Thu, 08 Dec 2022 04:24:29 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 08 Dec 2022 04:24:29 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b473b36a3d93c888196b326b1aad1f802bb6a9fa6fcbc5d2614d99a67899d587`  
		Last Modified: Tue, 06 Dec 2022 01:44:33 GMT  
		Size: 25.9 MB (25914951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4cbb358ee013a18adfaebc6ed0ff314c26ee71c2b5bd357fe6e0dcf852a8ea`  
		Last Modified: Tue, 06 Dec 2022 10:29:12 GMT  
		Size: 2.6 MB (2646691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eea36b69cbcfeee2ffa42fc78826bbcdb771de42ce44bcfc3bfc642569b222b`  
		Last Modified: Thu, 08 Dec 2022 03:14:15 GMT  
		Size: 12.0 MB (12020269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f65306a8fef4b6d76b75b7e5fcd144992f1751eb20e2b764838405773daa05`  
		Last Modified: Thu, 08 Dec 2022 03:14:13 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f9f30d16a1d846f491305ba678703a6afbe497d6f34a9ed98f04366714d359`  
		Last Modified: Thu, 08 Dec 2022 03:14:14 GMT  
		Size: 3.3 MB (3344929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484459a4ec59d941603e58f0fabf88de37493cb2720751b7d914f8a6c3dd3367`  
		Last Modified: Thu, 08 Dec 2022 04:33:31 GMT  
		Size: 4.1 MB (4133616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-buster` - linux; 386

```console
$ docker pull hylang@sha256:48ee9994deb5830c6d5bf032051b2da7abfa3cf08efa54ea6559f78259a2c85f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50006432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d55e18908cde5ca739e07e81030d8e97b5486d1885bd084afcb018d47c0276`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:21 GMT
ADD file:d1161a047b155d436f12a377ddf5a4a85ad0d20ac1f3f5d4444259a8773d6ef5 in / 
# Tue, 06 Dec 2022 01:40:22 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 08:22:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 08:22:44 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 08:22:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 09:41:06 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 08 Dec 2022 02:06:21 GMT
ENV PYTHON_VERSION=3.10.9
# Thu, 08 Dec 2022 02:19:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Thu, 08 Dec 2022 02:19:28 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 08 Dec 2022 02:19:29 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Thu, 08 Dec 2022 02:19:30 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Thu, 08 Dec 2022 02:19:31 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Thu, 08 Dec 2022 02:19:32 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Thu, 08 Dec 2022 02:19:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 08 Dec 2022 02:19:46 GMT
CMD ["python3"]
# Thu, 08 Dec 2022 05:56:25 GMT
ENV HY_VERSION=0.25.0
# Thu, 08 Dec 2022 05:56:26 GMT
ENV HYRULE_VERSION=0.2.1
# Thu, 08 Dec 2022 05:56:41 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 08 Dec 2022 05:56:42 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:da96e1773ee343324a0519eb38b71097e939e2d40d51ae4f19dcd9932b7cf638`  
		Last Modified: Tue, 06 Dec 2022 01:46:27 GMT  
		Size: 27.8 MB (27798436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace7dfc78a228f19b9cf7862afcd36de7b147e5b088efb45a5c8eebb0f796801`  
		Last Modified: Tue, 06 Dec 2022 12:26:49 GMT  
		Size: 2.8 MB (2788446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb45b24e02f7ab9c21252d591f177a8acce8ab7953e809a6b153fd06f2e9196`  
		Last Modified: Thu, 08 Dec 2022 04:51:10 GMT  
		Size: 12.2 MB (12156046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf55f80522c1f1c4b62fa256c35b7a0c551483e4483b65e157939cd44a41df4`  
		Last Modified: Thu, 08 Dec 2022 04:51:08 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44859177eca242edc8ca865e5f26a785ac17ac48837204c41ccb98f6688e40f`  
		Last Modified: Thu, 08 Dec 2022 04:51:09 GMT  
		Size: 3.1 MB (3131966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34cea7d5ac0465da0a3baeaeb808ea02396765014c01144944a5624e4db89b8`  
		Last Modified: Thu, 08 Dec 2022 06:12:24 GMT  
		Size: 4.1 MB (4131304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
