<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `satosa`

-	[`satosa:8`](#satosa8)
-	[`satosa:8-alpine`](#satosa8-alpine)
-	[`satosa:8-alpine3.16`](#satosa8-alpine316)
-	[`satosa:8-bullseye`](#satosa8-bullseye)
-	[`satosa:8.1`](#satosa81)
-	[`satosa:8.1-alpine`](#satosa81-alpine)
-	[`satosa:8.1-alpine3.16`](#satosa81-alpine316)
-	[`satosa:8.1-bullseye`](#satosa81-bullseye)
-	[`satosa:8.1.1`](#satosa811)
-	[`satosa:8.1.1-alpine`](#satosa811-alpine)
-	[`satosa:8.1.1-alpine3.16`](#satosa811-alpine316)
-	[`satosa:8.1.1-bullseye`](#satosa811-bullseye)
-	[`satosa:alpine`](#satosaalpine)
-	[`satosa:alpine3.16`](#satosaalpine316)
-	[`satosa:bullseye`](#satosabullseye)
-	[`satosa:latest`](#satosalatest)

## `satosa:8`

```console
$ docker pull satosa@sha256:b952f0d280486a79665537c956718dec4fff75e9e6a343a79e1048bc3bf3c861
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

### `satosa:8` - linux; amd64

```console
$ docker pull satosa@sha256:3d92574bf94e0395a41762efa378d221f605ea12bea73ae604c71310fe6036fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82653895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d245b28169a1e1f7dd888fa2381fc3aa02a91b2210f7b6b481c4016173ac8d0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 09:39:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 09:39:09 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 09:39:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 09:39:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 10:15:41 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 10:26:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 10:26:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 10:26:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 10:26:31 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 11:46:24 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 11:46:24 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 11:47:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 11:47:19 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 11:47:19 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 11:47:19 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 11:47:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 11:47:20 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 11:47:20 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 11:47:20 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126aaa6587b8608b62fa39019a891e98460e23bad2d04fb235c4dc8fae2adf3c`  
		Last Modified: Tue, 02 Aug 2022 12:33:29 GMT  
		Size: 1.1 MB (1076278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd06b55ca686f29b26c8a7e051ce98ad571fd6cf22bba07f5cd17e98fd31e13`  
		Last Modified: Wed, 03 Aug 2022 11:18:36 GMT  
		Size: 12.1 MB (12106838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3950cece0b727ab257c49317871d00f22d2abcb77bcce19ddf86aab5c4d88e21`  
		Last Modified: Wed, 03 Aug 2022 11:18:34 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e27c1167cc2a09e30e53c0fd2933e189e20b4785284e84a919fe5fd3013388b`  
		Last Modified: Wed, 03 Aug 2022 11:18:35 GMT  
		Size: 3.3 MB (3336043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb69b4e4539d59ea0fbed39563b5042d023cd4713d9a38bde6b930fb548e8b9a`  
		Last Modified: Wed, 03 Aug 2022 11:48:44 GMT  
		Size: 19.6 MB (19587061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620aa9bb44333fe5af9257a47e9e0de0e7a0596721959465531442e2b753aa5a`  
		Last Modified: Wed, 03 Aug 2022 11:48:44 GMT  
		Size: 15.2 MB (15169129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffc5c41689ca0d4f9b9e1beea0953f2bec48e3ab6becfee1b8c8862100aadbe`  
		Last Modified: Wed, 03 Aug 2022 11:48:41 GMT  
		Size: 9.4 KB (9443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebafed1e50948cce1a8ec458a2dbc933ec93924419791a83613e224356054ee`  
		Last Modified: Wed, 03 Aug 2022 11:48:41 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8` - linux; arm variant v5

```console
$ docker pull satosa@sha256:e4ee7d4d43b26f8dc6b5a7d8358af5463aa5ebf830249e6272afbe2a819e9732
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.7 MB (203698783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160cc52ce9b78d794b4acbd3286cc62c771bad645eb50e8c9af6722d743f166c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:10 GMT
ADD file:4cd2f95737fd3007912428eeac56036c9e67e989e66cec08a8be99da47f88494 in / 
# Tue, 02 Aug 2022 00:49:10 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:38:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 20:38:12 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 20:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:38:23 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 22:45:24 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 23:08:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 23:08:11 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 23:08:11 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 23:08:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 23:08:30 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 19:10:52 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 19:10:52 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 19:17:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 19:17:42 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 19:17:42 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 19:17:43 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 19:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 19:17:43 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 19:17:43 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 19:17:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5890b0ca6af5e8467a488e68716691950496a8f247d0495c2d595ddcb1893aff`  
		Last Modified: Tue, 02 Aug 2022 00:56:06 GMT  
		Size: 28.9 MB (28905515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eafe902d3c868e979e01e5c5aca6567b8be8b60814b9e1ce93c2b749451b410`  
		Last Modified: Wed, 03 Aug 2022 02:16:47 GMT  
		Size: 1.1 MB (1059641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e073b0922c53e3aee167b94b195f01b7740c95a691b391e30bbc1dd36133f578`  
		Last Modified: Wed, 03 Aug 2022 02:18:15 GMT  
		Size: 11.7 MB (11687058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1563deb88ac81fbc07f66164de09058989bc2f52e4b201209996fc610e7424`  
		Last Modified: Wed, 03 Aug 2022 02:18:11 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9586a9ae76d2fcf29975a3cbac30868417a5e7209b4d681ab4d8cdc9417e1127`  
		Last Modified: Wed, 03 Aug 2022 02:18:13 GMT  
		Size: 3.3 MB (3335517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2138d4d7c7c422781a7da5bbba917dfee3de2e44c0b89e2c05cd5fb54d6aec`  
		Last Modified: Wed, 03 Aug 2022 19:18:28 GMT  
		Size: 21.2 MB (21220513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ec77684813e78ff3c43e62e86fde2b1964089fb2e02c36be1b197e18d76199`  
		Last Modified: Wed, 03 Aug 2022 19:18:38 GMT  
		Size: 137.5 MB (137478750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecfeff163b4d6f23860d774bf123b6ad13105fce4fa35bddd9e46a56b0c09af`  
		Last Modified: Wed, 03 Aug 2022 19:18:21 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb3f6f2ab2014dd8287001b208c1dc97200c2c3e16a2cb980fd938dfd82858b`  
		Last Modified: Wed, 03 Aug 2022 19:18:22 GMT  
		Size: 2.1 KB (2111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8` - linux; arm variant v7

```console
$ docker pull satosa@sha256:1eb7ef57547ada8079868ad16a792df4e4cbc8571c4b2beb50d5682d1bc6250f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202351243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194a9b56fc0cc44a0542e47df53c65db1e4f7a579b5a8624e2b202e21462c73d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:58:59 GMT
ADD file:1575b776a15adacebc0875642e97a80807d42dcfc8917e1406d47af7ac244c97 in / 
# Tue, 02 Aug 2022 00:58:59 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:34:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 04:34:22 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 04:34:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 04:34:30 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 06:30:14 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 06:52:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 06:52:09 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 06:52:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 06:52:24 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 13:20:49 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 13:20:50 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 13:26:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 13:26:45 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 13:26:45 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 13:26:45 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 13:26:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 13:26:45 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 13:26:45 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 13:26:45 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1dd75a3a9c893a7dc313f683dd62464b7eab6c6d522ee62c8a17022631830f32`  
		Last Modified: Tue, 02 Aug 2022 01:06:45 GMT  
		Size: 26.6 MB (26560586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4206fea8c3d0ae09213fad25e06bb550a03c76c2b15e7a3c134ee5e2d217cd`  
		Last Modified: Wed, 03 Aug 2022 11:19:22 GMT  
		Size: 1.0 MB (1041632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed9dda465ec974f3e81b6b5f48dee0c43b63aeae625042e1e5f8ca482d43f1f`  
		Last Modified: Wed, 03 Aug 2022 11:21:19 GMT  
		Size: 11.2 MB (11205345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c669588520ce26d52819574b6ac8f40bc121ec539aae49c4cdc6aa899fcea`  
		Last Modified: Wed, 03 Aug 2022 11:21:15 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75c71e6575f11c76771634448c2e1c7e6988853591c1422d979aaf3dfa73569`  
		Last Modified: Wed, 03 Aug 2022 11:21:17 GMT  
		Size: 3.3 MB (3335656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d5ac04f9c39c2ba1d884f419e586ede32f2779ea0bbb6a7033e0f70c79d670`  
		Last Modified: Thu, 04 Aug 2022 13:31:15 GMT  
		Size: 20.9 MB (20949533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65844885dbff2fac2bccf9e5a7b69d9c423352d19d5ffb5eeca720f5e2a10886`  
		Last Modified: Thu, 04 Aug 2022 13:31:26 GMT  
		Size: 139.2 MB (139246702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53ebddc2eb90a987a1bae1b3a245f2d88ae7ea81a35f85f6bfdf10891217d58`  
		Last Modified: Thu, 04 Aug 2022 13:31:10 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa39e50e9a3812f026202131476b98a06e4a65a16a21fee180aeb54d979e2cb8`  
		Last Modified: Thu, 04 Aug 2022 13:31:10 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:8a7bc186f7c0a8725b284d01a4dceac8636d5f7f96b11f0d4031fd66f199e2b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79849083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56454aaf2924873a1f55890e93e1c83261d4047ce84a080d73750691435b3d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:03:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 12:03:30 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 12:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:03:36 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 09:19:10 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 09:29:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 09:29:22 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 09:29:22 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 09:29:23 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 09:29:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 09:29:25 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 09:29:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 09:29:37 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 10:39:28 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 10:39:28 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 10:40:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 10:40:15 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 10:40:16 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 10:40:18 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 10:40:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 10:40:19 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 10:40:20 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 10:40:21 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f101f90cc8f7640b7db5f7094941a1fe4ff28e11a968d3a36f146a89a480ecbb`  
		Last Modified: Tue, 02 Aug 2022 14:47:06 GMT  
		Size: 1.1 MB (1063812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a5d6cf27653f158e4f7552f31dc146332b6d820679ee42ebff5b4e47f4dac`  
		Last Modified: Wed, 03 Aug 2022 10:31:15 GMT  
		Size: 12.2 MB (12153733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd415bdc2c72c852623e384c90826d41aa2739adbc3158bd814bc3e562ab16ea`  
		Last Modified: Wed, 03 Aug 2022 10:31:13 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90ceb316b2d011719d35fb58a5d69ec1b84ebc6a9ab5568354ca370aad48524`  
		Last Modified: Wed, 03 Aug 2022 10:31:14 GMT  
		Size: 3.1 MB (3119919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7a23c6e6d4ea56699e3033f9fd616c6fa79290a257066f21578bf773f283cb`  
		Last Modified: Wed, 03 Aug 2022 10:42:23 GMT  
		Size: 19.3 MB (19324710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f64adba6c540f9f4fde33df9a99fa32be543c937e20b203b409ba3340f7b62`  
		Last Modified: Wed, 03 Aug 2022 10:42:23 GMT  
		Size: 14.1 MB (14120866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9df97e7203d91c6109257b6e98c0bb926732214ee96a7110c86550f8c271b74`  
		Last Modified: Wed, 03 Aug 2022 10:42:20 GMT  
		Size: 9.4 KB (9394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d56269ee4307b5c76ba7efef9346008e1440979b95ee777b9d5e8e3e4ead5b1`  
		Last Modified: Wed, 03 Aug 2022 10:42:20 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8` - linux; 386

```console
$ docker pull satosa@sha256:ff2180ab006e1d173a6d157a2ef8b05c4abae7d45d5693889e12f05e6861a42d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207396057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b9632c4df58a4c5e3e68e82bf8bab7462b2530f9ecfb108feb8726a85ab4d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:39:20 GMT
ADD file:f771e2286465694126158821089d801c7296376be2a56189e6041a15d2fe79f5 in / 
# Tue, 02 Aug 2022 00:39:21 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 11:22:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 11:22:53 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 11:22:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 11:22:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 20:51:53 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 21:03:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 21:03:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 21:03:55 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 21:03:56 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 21:03:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 21:03:58 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 21:04:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 21:04:12 GMT
CMD ["python3"]
# Tue, 02 Aug 2022 22:21:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 02 Aug 2022 22:21:44 GMT
ENV SATOSA_VERSION=8.1.1
# Tue, 02 Aug 2022 23:39:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 02 Aug 2022 23:39:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 02 Aug 2022 23:39:26 GMT
WORKDIR /etc/satosa
# Tue, 02 Aug 2022 23:39:28 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Tue, 02 Aug 2022 23:39:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 23:39:29 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 23:39:30 GMT
USER satosa:satosa
# Tue, 02 Aug 2022 23:39:31 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:90eb7f0ce9f33cf5dcd67d54c2fa606186dbaa5f95b6046f36145097267f9e53`  
		Last Modified: Tue, 02 Aug 2022 00:45:14 GMT  
		Size: 32.4 MB (32374054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd27ead98f25cd891e8dfae23b5500c856f3a9db336a545eed8b5f180a6df0b4`  
		Last Modified: Tue, 02 Aug 2022 14:37:54 GMT  
		Size: 1.1 MB (1088442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7362ecffe5fefdfcff89188358cb648fae40c1fed6254cd3325ef1c340a0ca9b`  
		Last Modified: Tue, 02 Aug 2022 22:15:01 GMT  
		Size: 12.2 MB (12224818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fb82e70fda9a811619f0b6cfd165d59473bcc467e702a70231630e64335b18`  
		Last Modified: Tue, 02 Aug 2022 22:14:59 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab067ab28a29ee91955ebd00b4849cd1d1993a430051ce801b5eaffeeb59b976`  
		Last Modified: Tue, 02 Aug 2022 22:15:00 GMT  
		Size: 3.1 MB (3119814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c68c7fda4b282e37efe94863aed2872d62133ead0fed4a4b4174eab16a125f`  
		Last Modified: Tue, 02 Aug 2022 23:40:27 GMT  
		Size: 22.6 MB (22586591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4630af60cc9f0637de40da0789c8be2b49091d860ae7f21753e736c5a24b0fac`  
		Last Modified: Tue, 02 Aug 2022 23:40:44 GMT  
		Size: 136.0 MB (135990599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ba92ddedaf8e60d74aac7773867aec0a84b2812ba92a5742090bee107e7736`  
		Last Modified: Tue, 02 Aug 2022 23:40:24 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e28ea4f42ac6baac91e14de0ee8d101956ac6d64c7d4078bb57ebfddde33184`  
		Last Modified: Tue, 02 Aug 2022 23:40:24 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8` - linux; mips64le

```console
$ docker pull satosa@sha256:b9bdbc69a8a0be593fe150cbd4334f006447c17a9538b850002e7fa96445593b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.8 MB (205844024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7d3830a289e7a92a0277b60e6cce741d4887ea889e4e236cdd2d878fb1f64b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:10:34 GMT
ADD file:6dc22a1e5b5fcf23f2549406ddcc45c4e244f46e21eafa881de81fa87438e5d8 in / 
# Tue, 02 Aug 2022 01:10:38 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 10:25:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 10:25:08 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 10:25:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:25:36 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 04 Aug 2022 04:16:09 GMT
ENV PYTHON_VERSION=3.10.6
# Thu, 04 Aug 2022 05:33:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Thu, 04 Aug 2022 05:33:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 04 Aug 2022 05:33:27 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Thu, 04 Aug 2022 05:33:30 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Thu, 04 Aug 2022 05:33:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Thu, 04 Aug 2022 05:33:35 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Thu, 04 Aug 2022 05:34:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 04 Aug 2022 05:34:30 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 08:35:12 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 08:35:15 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 08:52:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 08:52:17 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 08:52:21 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 08:52:25 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 08:52:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 08:52:34 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 08:52:39 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 08:52:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:88350749a27614c791450c256b051f023d81cdd256211274b1efac493779d2be`  
		Last Modified: Tue, 02 Aug 2022 01:21:02 GMT  
		Size: 29.6 MB (29628964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61130d003a0ea87819935a3a252db1861d9b87e1313fa7988d5f0642637f3e`  
		Last Modified: Tue, 02 Aug 2022 23:46:40 GMT  
		Size: 1.0 MB (1049605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e786491697e5d2bd3dee622f7eae98810c04c895d5024e910e2394f92b37ad8`  
		Last Modified: Thu, 04 Aug 2022 08:14:51 GMT  
		Size: 12.1 MB (12124464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fb1366c066d6bf94df2bf081524439083c14a1f292da85f218000ac515a2f5`  
		Last Modified: Thu, 04 Aug 2022 08:14:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe7637d1173b353af8622199dfbc92d0f74f8cff129fe540541b9c069a058d3`  
		Last Modified: Thu, 04 Aug 2022 08:14:46 GMT  
		Size: 3.1 MB (3120804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4655831cce551d936028a78d3d4a295cd96e3ca02ea0f5f726d0b963350a0e`  
		Last Modified: Thu, 04 Aug 2022 08:53:18 GMT  
		Size: 21.3 MB (21288233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54965dd4effca16f75a92cdac5dd71e708a50d218ca30b0806964a58d8b726ee`  
		Last Modified: Thu, 04 Aug 2022 08:53:58 GMT  
		Size: 138.6 MB (138620211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a449c61594c6b3d2e0fa03d876ebe6fc8561eaa1d46ebf088772a42dea52b596`  
		Last Modified: Thu, 04 Aug 2022 08:53:06 GMT  
		Size: 9.4 KB (9396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54e620f3a05fe34c293ac1de03899ec567f49faa21a8db43216f796387f8f65`  
		Last Modified: Thu, 04 Aug 2022 08:53:06 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8` - linux; ppc64le

```console
$ docker pull satosa@sha256:b84ad93ccca31f2ba03b7c0586ad9f3a2d71764d4338922af798ae737ec87f23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212244381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f29a99f45c08fb90c8ad9dec84fd55c14d0ca8ecbc00c2160fc3464a14feca9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:17:30 GMT
ADD file:3a95a896d463569ce82199957052b3467123a4bd3385a0a4e397cf08402a99c3 in / 
# Tue, 02 Aug 2022 01:17:32 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:03:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 16:03:13 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 16:03:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 16:03:24 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 18:10:29 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 18:43:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 18:43:03 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 18:43:03 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 18:43:03 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 18:43:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 18:43:04 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 18:43:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 18:43:25 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 21:09:20 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 21:09:21 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 21:14:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 21:14:39 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 21:14:39 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 21:14:40 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 21:14:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 21:14:41 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 21:14:41 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 21:14:42 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5241cd116d6e6e2d62f3d8c2245b74daca9f6cc154eaccd738feb41984c74714`  
		Last Modified: Tue, 02 Aug 2022 01:24:39 GMT  
		Size: 35.3 MB (35272771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf6dcfcb4fa2f4e24ce6bed8b3eda6b0d49d92062cb34d95830e4e9f512270`  
		Last Modified: Wed, 03 Aug 2022 00:14:29 GMT  
		Size: 1.1 MB (1094658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdc50327f93cca5ad2c5f8500471040045b715045a9a4852ece90b3155d5aea`  
		Last Modified: Wed, 03 Aug 2022 20:42:55 GMT  
		Size: 12.5 MB (12473465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49f3fdf44cc1cf9b0e2d32c8ea2b62a0d3eb7eac481b56c9d11e44c66b764fe`  
		Last Modified: Wed, 03 Aug 2022 20:42:52 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd9d6c8cb5530b56f02a736bb1cc24d2d0ffc11d6fb55dc6befb0e114a1ff74`  
		Last Modified: Wed, 03 Aug 2022 20:42:53 GMT  
		Size: 3.3 MB (3336216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209342dd334b280e74196c0e693487033f7f2d08880ab61f5f9113dbbd5d0461`  
		Last Modified: Wed, 03 Aug 2022 21:22:32 GMT  
		Size: 22.2 MB (22158681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11809242e6bd5adbd0096d37646b954f666a1e2a107dd5442773977caa919360`  
		Last Modified: Wed, 03 Aug 2022 21:22:45 GMT  
		Size: 137.9 MB (137896801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa36501b6a1d8ec2e51a6a162f1f43d70ea4b035335513b65b800346790717`  
		Last Modified: Wed, 03 Aug 2022 21:22:27 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fe38c0944e97231334e780f32f3cd041644756c5b195812b19edd697268021`  
		Last Modified: Wed, 03 Aug 2022 21:22:27 GMT  
		Size: 2.1 KB (2113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8` - linux; s390x

```console
$ docker pull satosa@sha256:f52b8375aeb8b39ad8ae5b9f05f4f94a47f4776b3f500aeeadee19c4ed572f5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202163420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f253b8b35e8bbaf69f23beb8a8584dc48a0c682127faa17ed9d639b33dfdf3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 08:30:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 08:30:40 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 08:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 08:30:44 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 22:09:42 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 22:18:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 22:18:03 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 22:18:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 22:18:13 GMT
CMD ["python3"]
# Tue, 02 Aug 2022 23:28:28 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 02 Aug 2022 23:28:31 GMT
ENV SATOSA_VERSION=8.1.1
# Tue, 02 Aug 2022 23:32:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 02 Aug 2022 23:33:02 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 02 Aug 2022 23:33:02 GMT
WORKDIR /etc/satosa
# Tue, 02 Aug 2022 23:33:02 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Tue, 02 Aug 2022 23:33:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 23:33:02 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 23:33:03 GMT
USER satosa:satosa
# Tue, 02 Aug 2022 23:33:03 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c36d12a9d2aa3bd2ed5880b10e768bae6cab779992e198cf595d3b8d6924d5`  
		Last Modified: Tue, 02 Aug 2022 10:43:27 GMT  
		Size: 1.1 MB (1075771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a2fa2a5f3f4be291fac87451996292e32ad4b6b7e7ae168c720b6501ba676f`  
		Last Modified: Tue, 02 Aug 2022 23:23:49 GMT  
		Size: 11.9 MB (11900903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1958402e81da32fc50ee2b3d3d48a5714015a6589a9b0882e2e0862173874f52`  
		Last Modified: Tue, 02 Aug 2022 23:23:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adc16df778c23094a004c62669c6de553142901db4933d76959d223598473b`  
		Last Modified: Tue, 02 Aug 2022 23:23:49 GMT  
		Size: 3.3 MB (3335624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5f479e9444a18e7100a74300ba30ab5818c9023c386c0a537811de457f1e99`  
		Last Modified: Tue, 02 Aug 2022 23:33:39 GMT  
		Size: 19.6 MB (19580744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573792100821147cd9e469e566ed70175d1fe8ec2b68e371484abc92f0aeaf74`  
		Last Modified: Tue, 02 Aug 2022 23:33:45 GMT  
		Size: 136.6 MB (136618328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cb6a07895307e25b49bb3cdebc3f6e29fef231b0390c00ddacc6b74ee5f9fd`  
		Last Modified: Tue, 02 Aug 2022 23:33:36 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0ce3aebbe275e54928297909f6f1ed7c7beee5c901706ccef91eec96eb8bc5`  
		Last Modified: Tue, 02 Aug 2022 23:33:36 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8-alpine`

```console
$ docker pull satosa@sha256:fa00b0ab420886685085b244405746ecce141ff81c408876a6d8c17f5e0960ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `satosa:8-alpine` - linux; amd64

```console
$ docker pull satosa@sha256:889e8b702bc04ca43d059bdf24c8db677954c87e5318ba8a93d795e450d485dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42508179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa3cc16430e95981e37a39687b5b6a8e23b8adf5eb81881cab4136b31de9b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:14:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 02:01:52 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 02:01:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 19 Jul 2022 02:01:54 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 10:48:21 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 11:00:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 11:00:14 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 11:00:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 11:00:21 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 11:47:34 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 11:47:34 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 11:48:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 11:48:18 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 11:48:19 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 11:48:19 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 11:48:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 11:48:19 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 11:48:19 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 11:48:19 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c14b1a767335de44f2bc926cb52487979a0fe602ac5429643dbb238f297fb`  
		Last Modified: Tue, 19 Jul 2022 02:56:13 GMT  
		Size: 666.8 KB (666769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571274b8543b548747b5e9bef700a89692fe9403cc364be8d6e8a0792ccfe2b4`  
		Last Modified: Wed, 03 Aug 2022 11:19:35 GMT  
		Size: 12.5 MB (12508608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f79a08255af5d614c7b4b81e358b5bb607bdcb14a6475c836d3d4f92f094846`  
		Last Modified: Wed, 03 Aug 2022 11:19:34 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6b20e3f6abd46292c29437a6917dc82b769ebb239e2d971aedb6695e057715`  
		Last Modified: Wed, 03 Aug 2022 11:19:34 GMT  
		Size: 3.0 MB (3043671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c974d4972d870a99bf0fba525cab86b298dd6e9405d3329a3495a164ae5c7`  
		Last Modified: Wed, 03 Aug 2022 11:49:00 GMT  
		Size: 9.4 MB (9398243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c482d554455c83821852ea2cd26eaf97f49bb1c7983342cec7242b8ea5432234`  
		Last Modified: Wed, 03 Aug 2022 11:49:01 GMT  
		Size: 14.1 MB (14080297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b861965b84abb04a92b63eb19a620daf7360785f485bc2d526885601454b19ca`  
		Last Modified: Wed, 03 Aug 2022 11:48:58 GMT  
		Size: 9.4 KB (9439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16e011f2d9efad78d03ac0d4c7abe2f694dfc5f6c158ef9fa350a3f21d22a8e`  
		Last Modified: Wed, 03 Aug 2022 11:48:58 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine` - linux; arm variant v6

```console
$ docker pull satosa@sha256:1ed78492e93849ebbee5cd80dd5e4a91eb2a41676fbc3d21584a17d402028ca7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160179359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e822b6bb9258ee22b55f2f03c3d389710a39d0a3fa1d10f1250cb00db2f3e268`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 19:49:37 GMT
ADD file:7a20333469e71664904a0cb8f61613250f2bd092b4a27bfa7bbae1dc7e21b7ed in / 
# Mon, 18 Jul 2022 19:49:37 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 00:30:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 00:30:05 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 00:30:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 00:30:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 19:50:04 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 20:30:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 02 Aug 2022 20:30:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 20:30:20 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 20:30:20 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 03:20:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 03:20:45 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 03:27:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 03:27:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 03:27:54 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 03:27:54 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 03:27:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 03:27:55 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 03:27:55 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 03:27:55 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b7885075fcd06a866d12dfd56eb704045eaadbd22dc03a224cd98715be566677`  
		Last Modified: Mon, 18 Jul 2022 19:08:42 GMT  
		Size: 2.6 MB (2606431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ebe8e3a2f83d0ddc301c9b9d6405376eecb906b92082e05d5e257eff5f6293`  
		Last Modified: Wed, 27 Jul 2022 11:08:23 GMT  
		Size: 672.3 KB (672287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b647934af90a736595f675559fd3aebbcdbcfc67277de68401980916f3c217d7`  
		Last Modified: Wed, 03 Aug 2022 00:13:17 GMT  
		Size: 12.1 MB (12085055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaef313095ff837d4848dec2c5e458a33e59ee4e1ab7a9d4e3d244d20b92fbf`  
		Last Modified: Wed, 03 Aug 2022 00:13:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba453d098c35b58faf7cc2ac6a90a0e9a8941dc90611ee397d12af0a546bbe87`  
		Last Modified: Wed, 03 Aug 2022 00:13:15 GMT  
		Size: 3.0 MB (3043708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0a90158473abc47e6b9744b5cc61265a9552ba9217486241f5b7b4a5d12eec`  
		Last Modified: Wed, 03 Aug 2022 03:28:44 GMT  
		Size: 8.3 MB (8280231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a82dd9e01f89340501ac0415caccc1ad608cc08d55219cb26db2226dc64b83`  
		Last Modified: Wed, 03 Aug 2022 03:29:07 GMT  
		Size: 133.5 MB (133479861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ee2ba314aef7361329abd7eaa7a8860079655317f4d5fc9d37f73f8b34de4`  
		Last Modified: Wed, 03 Aug 2022 03:28:39 GMT  
		Size: 9.4 KB (9438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24649d01bd9f34f035857fcb9324aef45128d255b0e7d7c9be9d0d9d58a928f3`  
		Last Modified: Wed, 03 Aug 2022 03:28:39 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine` - linux; arm variant v7

```console
$ docker pull satosa@sha256:9c12b392cb5946a433fe0c98001d362d79a953040068a9d0843c3a9a9c12fb8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163401667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55a50fb783bb28da31c92c6cff33c408ef6ea7e1c6da179086af8ce588f092d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:24:47 GMT
ADD file:68590e866bc6db27ad54d23de7dd275d0389cb86e4e6291a1243fcc234f2f7a1 in / 
# Mon, 18 Jul 2022 21:24:47 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 03:57:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 03:57:44 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 03:57:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 03:57:46 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 07:37:59 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 08:07:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 08:07:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 08:07:50 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 08:07:51 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 13:27:03 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 13:27:03 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 13:30:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 13:30:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 13:30:25 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 13:30:25 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 13:30:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 13:30:25 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 13:30:25 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 13:30:25 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a6b45ace95f42a930d15c33679ab9c85d46019b7e73954cadc73bb9ba176509b`  
		Last Modified: Mon, 18 Jul 2022 19:08:56 GMT  
		Size: 2.4 MB (2412307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d826ef3e3e077607452c51ac5332613cc0a20903abe17b56af4b973f31f0e9b7`  
		Last Modified: Wed, 27 Jul 2022 10:54:47 GMT  
		Size: 664.1 KB (664079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116f12212b7e97cde5b72713f0f3a3025a9ef6dffccdc353cd4d15407d343a72`  
		Last Modified: Wed, 03 Aug 2022 11:22:41 GMT  
		Size: 11.6 MB (11558755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef2affe775c9998dea9fd354aa8d4b6e97117d2092c84f1401265b9f9528bf7`  
		Last Modified: Wed, 03 Aug 2022 11:22:38 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032af4833525c8884057f85c0da98a7f2dedc337784e4ce3645fad79e6633b26`  
		Last Modified: Wed, 03 Aug 2022 11:22:39 GMT  
		Size: 3.0 MB (3043658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65c3d7d841a308ff58960bdd0832a9c2fc9d01d091b4478549cf91ad4551edc`  
		Last Modified: Thu, 04 Aug 2022 13:31:47 GMT  
		Size: 8.0 MB (8026973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553863577a06e5d191ae29abc79bb81603188e34e406ebce36a4e4da49320df8`  
		Last Modified: Thu, 04 Aug 2022 13:31:59 GMT  
		Size: 137.7 MB (137684108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d66d75890a5436b91b581c5023634cbedf248e1dbb622b1241f80c5a4ed29`  
		Last Modified: Thu, 04 Aug 2022 13:31:45 GMT  
		Size: 9.4 KB (9439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cab52b5f6577ce2ac31dd72be231ca9d43531003be80eacfe2f20bbfa5c5d5`  
		Last Modified: Thu, 04 Aug 2022 13:31:46 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:cccb94f4511ba8a1fd8ab69a69f483edef010e4fab16eeccfb637ae5395cdc67
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40930309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83c2e990bd9017e2a1f46423fc6e313b33122d383dda9f8f9c00e8006d36921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:10:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 01:53:04 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 01:53:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 19 Jul 2022 01:53:06 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 09:50:39 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 10:05:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 10:05:10 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 10:05:11 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 10:05:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 10:05:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 10:05:14 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 10:05:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 10:05:22 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 10:40:42 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 10:40:43 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 10:41:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 10:41:33 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 10:41:34 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 10:41:36 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 10:41:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 10:41:37 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 10:41:38 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 10:41:39 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c36086fc9356a3d9879c8427af90dd86ad6fd35b3929bab2af384e98d0571c`  
		Last Modified: Tue, 19 Jul 2022 02:56:56 GMT  
		Size: 668.0 KB (668022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255e9c7248a65c9bb1f14e3ffaf6aad2e14b965bfd9196b30e8c1efc8ddd1747`  
		Last Modified: Wed, 03 Aug 2022 10:34:00 GMT  
		Size: 12.6 MB (12579036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d32815e9cd0f789447579f484cec5ed6ff5b006c50c121a5e314519ffad01d5`  
		Last Modified: Wed, 03 Aug 2022 10:33:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c6e4018f23818adb74c050daeddb28d2efddbabe1135f85ed3ef29b17ec7b`  
		Last Modified: Wed, 03 Aug 2022 10:32:56 GMT  
		Size: 3.0 MB (3045000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2feaf81b71b2f7b13ac6cefc0f434f31221423c1c94002a89138b4c60741ced`  
		Last Modified: Wed, 03 Aug 2022 10:42:41 GMT  
		Size: 8.2 MB (8224897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c9e9ae46115c582ac3a68bb4b583d2ed73875acfb5ff520c5877d481be9cdc`  
		Last Modified: Wed, 03 Aug 2022 10:42:42 GMT  
		Size: 13.7 MB (13706894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e959a5cfce7f6c07db205394594178b791ab1fd7b3425ded77627110666277`  
		Last Modified: Wed, 03 Aug 2022 10:42:40 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143d97f09a0b08aff0f4993e07d50c6a62b1d1c84b442a35f1c8b7f9535005f4`  
		Last Modified: Wed, 03 Aug 2022 10:42:40 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine` - linux; 386

```console
$ docker pull satosa@sha256:3b7052fea622f5d95da31220bc234a9258ae473482fb55269dea295fd83b4e05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (173023892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712f8d15ddeef960a7327c512f8d03f337021df170d7531f5aa93eafbe51d2c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 21:22:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 21:22:15 GMT
ENV LANG=C.UTF-8
# Tue, 09 Aug 2022 21:22:17 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 09 Aug 2022 21:22:18 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 09 Aug 2022 22:02:59 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 09 Aug 2022 22:16:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 09 Aug 2022 22:16:19 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 09 Aug 2022 22:16:20 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 09 Aug 2022 22:16:21 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 09 Aug 2022 22:16:22 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 09 Aug 2022 22:16:23 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 09 Aug 2022 22:16:31 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 09 Aug 2022 22:16:31 GMT
CMD ["python3"]
# Wed, 10 Aug 2022 03:30:07 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 10 Aug 2022 03:30:08 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 10 Aug 2022 03:33:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 10 Aug 2022 03:33:03 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 10 Aug 2022 03:33:04 GMT
WORKDIR /etc/satosa
# Wed, 10 Aug 2022 03:33:06 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 10 Aug 2022 03:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 03:33:07 GMT
EXPOSE 8080
# Wed, 10 Aug 2022 03:33:08 GMT
USER satosa:satosa
# Wed, 10 Aug 2022 03:33:09 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6e4c463b4b085b81ccd90e5d99d5d5b64a56c2f756e7ff5575080b0efc2e9f`  
		Last Modified: Tue, 09 Aug 2022 23:12:22 GMT  
		Size: 689.1 KB (689070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30e501e19288fafd4b62af6aaf0b588b8da1b9f7bf0ed0bd8c7cf5550131f4b`  
		Last Modified: Tue, 09 Aug 2022 23:13:12 GMT  
		Size: 12.7 MB (12700838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5383c9c382f8845fcf42a8ea747ddb3a99c87e277380a509277f27c6bf8d85`  
		Last Modified: Tue, 09 Aug 2022 23:13:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2450ac53e437f841f48f00e832466a3d7ce73190f3f5255c89dfb89edcd9193`  
		Last Modified: Tue, 09 Aug 2022 23:13:11 GMT  
		Size: 3.0 MB (3045003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3183acab5e336c62f2d06a000d65364d4484e755eb4c01749dd6e443ee703e32`  
		Last Modified: Wed, 10 Aug 2022 03:34:01 GMT  
		Size: 8.5 MB (8512861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350ea1863d968db10b0fe1fd8772d772c84631136d5fb13934b7c5a360cf66fc`  
		Last Modified: Wed, 10 Aug 2022 03:34:28 GMT  
		Size: 145.3 MB (145257262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92895882e21832e6f4d040fa6f60752d36b168dbc7f3893d1fc81a19da18cfc3`  
		Last Modified: Wed, 10 Aug 2022 03:33:59 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85df40b1b491557b15d24c816c82279561fd23244d53603eeea4f9976ce8766`  
		Last Modified: Wed, 10 Aug 2022 03:33:59 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine` - linux; ppc64le

```console
$ docker pull satosa@sha256:f70b3121c8db732d980c4272ea937145d0745875aba33578b5667bbaf28fb1ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164310759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef00aeaa317867dd9dca82b0661794be10c5d0a082d11a8f76b597b76e88cb55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:29:30 GMT
ADD file:69e4080f15f54e2d8f8aa25fdcba9c01dde149d43592edd5023106675e54a769 in / 
# Mon, 18 Jul 2022 21:29:31 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 04:30:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 04:30:31 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 04:30:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 04:30:33 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 19:40:20 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 20:04:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 20:05:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 20:05:00 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 20:05:00 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 20:05:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 20:05:01 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 20:05:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 20:05:13 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 21:15:12 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 21:15:12 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 21:21:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 21:21:41 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 21:21:41 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 21:21:42 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 21:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 21:21:42 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 21:21:43 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 21:21:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:602896d442490cd3fbb6599f0f862d3673b7cd58eca3ac842b8e09bf8d012443`  
		Last Modified: Mon, 18 Jul 2022 19:09:09 GMT  
		Size: 2.8 MB (2789923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6556a4bf6509d5fd24900f56a6175bd811b9dd8c6f4f51e2732b6888a2b8933`  
		Last Modified: Wed, 27 Jul 2022 13:49:16 GMT  
		Size: 677.0 KB (676971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c735731e55a5ddb324dd5eb175e1f3d88895a77ea93b8fb08428ee522445708b`  
		Last Modified: Wed, 03 Aug 2022 20:44:16 GMT  
		Size: 12.8 MB (12819587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e525d9b2b00fc7130f21f05f981c44d849b279417c15b38703c3f11d3c9bd667`  
		Last Modified: Wed, 03 Aug 2022 20:44:13 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9bc880d40f528e2c6046dd7bad61fc78f27a3fbebe3f45d1348a72ace67d9b`  
		Last Modified: Wed, 03 Aug 2022 20:44:15 GMT  
		Size: 3.0 MB (3043656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b74e25b6a705707a07e0411366545458ad05f07844bde5b7bebddd988e69068`  
		Last Modified: Wed, 03 Aug 2022 21:23:08 GMT  
		Size: 8.5 MB (8476895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141bd7d880682fd816129f41549c798cabb9e94494f7ee7714d6e83e63606b82`  
		Last Modified: Wed, 03 Aug 2022 21:23:23 GMT  
		Size: 136.5 MB (136491944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b412f1d24946cb1e7f3d66a4ae5595d3b71ae6040af529dc49507cb1dd4e06c`  
		Last Modified: Wed, 03 Aug 2022 21:23:06 GMT  
		Size: 9.4 KB (9434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8aa237953d155695df1943bb27b03cf1cc3f1716ea63b1cf5a8b12d97cd6cea`  
		Last Modified: Wed, 03 Aug 2022 21:23:06 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8-alpine3.16`

```console
$ docker pull satosa@sha256:fa00b0ab420886685085b244405746ecce141ff81c408876a6d8c17f5e0960ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `satosa:8-alpine3.16` - linux; amd64

```console
$ docker pull satosa@sha256:889e8b702bc04ca43d059bdf24c8db677954c87e5318ba8a93d795e450d485dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42508179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa3cc16430e95981e37a39687b5b6a8e23b8adf5eb81881cab4136b31de9b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:14:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 02:01:52 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 02:01:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 19 Jul 2022 02:01:54 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 10:48:21 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 11:00:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 11:00:14 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 11:00:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 11:00:21 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 11:47:34 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 11:47:34 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 11:48:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 11:48:18 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 11:48:19 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 11:48:19 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 11:48:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 11:48:19 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 11:48:19 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 11:48:19 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c14b1a767335de44f2bc926cb52487979a0fe602ac5429643dbb238f297fb`  
		Last Modified: Tue, 19 Jul 2022 02:56:13 GMT  
		Size: 666.8 KB (666769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571274b8543b548747b5e9bef700a89692fe9403cc364be8d6e8a0792ccfe2b4`  
		Last Modified: Wed, 03 Aug 2022 11:19:35 GMT  
		Size: 12.5 MB (12508608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f79a08255af5d614c7b4b81e358b5bb607bdcb14a6475c836d3d4f92f094846`  
		Last Modified: Wed, 03 Aug 2022 11:19:34 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6b20e3f6abd46292c29437a6917dc82b769ebb239e2d971aedb6695e057715`  
		Last Modified: Wed, 03 Aug 2022 11:19:34 GMT  
		Size: 3.0 MB (3043671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c974d4972d870a99bf0fba525cab86b298dd6e9405d3329a3495a164ae5c7`  
		Last Modified: Wed, 03 Aug 2022 11:49:00 GMT  
		Size: 9.4 MB (9398243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c482d554455c83821852ea2cd26eaf97f49bb1c7983342cec7242b8ea5432234`  
		Last Modified: Wed, 03 Aug 2022 11:49:01 GMT  
		Size: 14.1 MB (14080297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b861965b84abb04a92b63eb19a620daf7360785f485bc2d526885601454b19ca`  
		Last Modified: Wed, 03 Aug 2022 11:48:58 GMT  
		Size: 9.4 KB (9439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16e011f2d9efad78d03ac0d4c7abe2f694dfc5f6c158ef9fa350a3f21d22a8e`  
		Last Modified: Wed, 03 Aug 2022 11:48:58 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine3.16` - linux; arm variant v6

```console
$ docker pull satosa@sha256:1ed78492e93849ebbee5cd80dd5e4a91eb2a41676fbc3d21584a17d402028ca7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160179359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e822b6bb9258ee22b55f2f03c3d389710a39d0a3fa1d10f1250cb00db2f3e268`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 19:49:37 GMT
ADD file:7a20333469e71664904a0cb8f61613250f2bd092b4a27bfa7bbae1dc7e21b7ed in / 
# Mon, 18 Jul 2022 19:49:37 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 00:30:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 00:30:05 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 00:30:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 00:30:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 19:50:04 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 20:30:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 02 Aug 2022 20:30:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 20:30:20 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 20:30:20 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 03:20:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 03:20:45 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 03:27:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 03:27:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 03:27:54 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 03:27:54 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 03:27:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 03:27:55 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 03:27:55 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 03:27:55 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b7885075fcd06a866d12dfd56eb704045eaadbd22dc03a224cd98715be566677`  
		Last Modified: Mon, 18 Jul 2022 19:08:42 GMT  
		Size: 2.6 MB (2606431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ebe8e3a2f83d0ddc301c9b9d6405376eecb906b92082e05d5e257eff5f6293`  
		Last Modified: Wed, 27 Jul 2022 11:08:23 GMT  
		Size: 672.3 KB (672287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b647934af90a736595f675559fd3aebbcdbcfc67277de68401980916f3c217d7`  
		Last Modified: Wed, 03 Aug 2022 00:13:17 GMT  
		Size: 12.1 MB (12085055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaef313095ff837d4848dec2c5e458a33e59ee4e1ab7a9d4e3d244d20b92fbf`  
		Last Modified: Wed, 03 Aug 2022 00:13:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba453d098c35b58faf7cc2ac6a90a0e9a8941dc90611ee397d12af0a546bbe87`  
		Last Modified: Wed, 03 Aug 2022 00:13:15 GMT  
		Size: 3.0 MB (3043708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0a90158473abc47e6b9744b5cc61265a9552ba9217486241f5b7b4a5d12eec`  
		Last Modified: Wed, 03 Aug 2022 03:28:44 GMT  
		Size: 8.3 MB (8280231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a82dd9e01f89340501ac0415caccc1ad608cc08d55219cb26db2226dc64b83`  
		Last Modified: Wed, 03 Aug 2022 03:29:07 GMT  
		Size: 133.5 MB (133479861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ee2ba314aef7361329abd7eaa7a8860079655317f4d5fc9d37f73f8b34de4`  
		Last Modified: Wed, 03 Aug 2022 03:28:39 GMT  
		Size: 9.4 KB (9438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24649d01bd9f34f035857fcb9324aef45128d255b0e7d7c9be9d0d9d58a928f3`  
		Last Modified: Wed, 03 Aug 2022 03:28:39 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine3.16` - linux; arm variant v7

```console
$ docker pull satosa@sha256:9c12b392cb5946a433fe0c98001d362d79a953040068a9d0843c3a9a9c12fb8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163401667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55a50fb783bb28da31c92c6cff33c408ef6ea7e1c6da179086af8ce588f092d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:24:47 GMT
ADD file:68590e866bc6db27ad54d23de7dd275d0389cb86e4e6291a1243fcc234f2f7a1 in / 
# Mon, 18 Jul 2022 21:24:47 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 03:57:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 03:57:44 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 03:57:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 03:57:46 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 07:37:59 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 08:07:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 08:07:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 08:07:50 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 08:07:51 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 13:27:03 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 13:27:03 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 13:30:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 13:30:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 13:30:25 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 13:30:25 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 13:30:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 13:30:25 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 13:30:25 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 13:30:25 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a6b45ace95f42a930d15c33679ab9c85d46019b7e73954cadc73bb9ba176509b`  
		Last Modified: Mon, 18 Jul 2022 19:08:56 GMT  
		Size: 2.4 MB (2412307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d826ef3e3e077607452c51ac5332613cc0a20903abe17b56af4b973f31f0e9b7`  
		Last Modified: Wed, 27 Jul 2022 10:54:47 GMT  
		Size: 664.1 KB (664079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116f12212b7e97cde5b72713f0f3a3025a9ef6dffccdc353cd4d15407d343a72`  
		Last Modified: Wed, 03 Aug 2022 11:22:41 GMT  
		Size: 11.6 MB (11558755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef2affe775c9998dea9fd354aa8d4b6e97117d2092c84f1401265b9f9528bf7`  
		Last Modified: Wed, 03 Aug 2022 11:22:38 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032af4833525c8884057f85c0da98a7f2dedc337784e4ce3645fad79e6633b26`  
		Last Modified: Wed, 03 Aug 2022 11:22:39 GMT  
		Size: 3.0 MB (3043658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65c3d7d841a308ff58960bdd0832a9c2fc9d01d091b4478549cf91ad4551edc`  
		Last Modified: Thu, 04 Aug 2022 13:31:47 GMT  
		Size: 8.0 MB (8026973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553863577a06e5d191ae29abc79bb81603188e34e406ebce36a4e4da49320df8`  
		Last Modified: Thu, 04 Aug 2022 13:31:59 GMT  
		Size: 137.7 MB (137684108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d66d75890a5436b91b581c5023634cbedf248e1dbb622b1241f80c5a4ed29`  
		Last Modified: Thu, 04 Aug 2022 13:31:45 GMT  
		Size: 9.4 KB (9439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cab52b5f6577ce2ac31dd72be231ca9d43531003be80eacfe2f20bbfa5c5d5`  
		Last Modified: Thu, 04 Aug 2022 13:31:46 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:cccb94f4511ba8a1fd8ab69a69f483edef010e4fab16eeccfb637ae5395cdc67
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40930309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83c2e990bd9017e2a1f46423fc6e313b33122d383dda9f8f9c00e8006d36921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:10:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 01:53:04 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 01:53:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 19 Jul 2022 01:53:06 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 09:50:39 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 10:05:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 10:05:10 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 10:05:11 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 10:05:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 10:05:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 10:05:14 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 10:05:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 10:05:22 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 10:40:42 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 10:40:43 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 10:41:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 10:41:33 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 10:41:34 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 10:41:36 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 10:41:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 10:41:37 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 10:41:38 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 10:41:39 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c36086fc9356a3d9879c8427af90dd86ad6fd35b3929bab2af384e98d0571c`  
		Last Modified: Tue, 19 Jul 2022 02:56:56 GMT  
		Size: 668.0 KB (668022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255e9c7248a65c9bb1f14e3ffaf6aad2e14b965bfd9196b30e8c1efc8ddd1747`  
		Last Modified: Wed, 03 Aug 2022 10:34:00 GMT  
		Size: 12.6 MB (12579036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d32815e9cd0f789447579f484cec5ed6ff5b006c50c121a5e314519ffad01d5`  
		Last Modified: Wed, 03 Aug 2022 10:33:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c6e4018f23818adb74c050daeddb28d2efddbabe1135f85ed3ef29b17ec7b`  
		Last Modified: Wed, 03 Aug 2022 10:32:56 GMT  
		Size: 3.0 MB (3045000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2feaf81b71b2f7b13ac6cefc0f434f31221423c1c94002a89138b4c60741ced`  
		Last Modified: Wed, 03 Aug 2022 10:42:41 GMT  
		Size: 8.2 MB (8224897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c9e9ae46115c582ac3a68bb4b583d2ed73875acfb5ff520c5877d481be9cdc`  
		Last Modified: Wed, 03 Aug 2022 10:42:42 GMT  
		Size: 13.7 MB (13706894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e959a5cfce7f6c07db205394594178b791ab1fd7b3425ded77627110666277`  
		Last Modified: Wed, 03 Aug 2022 10:42:40 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143d97f09a0b08aff0f4993e07d50c6a62b1d1c84b442a35f1c8b7f9535005f4`  
		Last Modified: Wed, 03 Aug 2022 10:42:40 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine3.16` - linux; 386

```console
$ docker pull satosa@sha256:3b7052fea622f5d95da31220bc234a9258ae473482fb55269dea295fd83b4e05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (173023892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712f8d15ddeef960a7327c512f8d03f337021df170d7531f5aa93eafbe51d2c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 21:22:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 21:22:15 GMT
ENV LANG=C.UTF-8
# Tue, 09 Aug 2022 21:22:17 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 09 Aug 2022 21:22:18 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 09 Aug 2022 22:02:59 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 09 Aug 2022 22:16:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 09 Aug 2022 22:16:19 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 09 Aug 2022 22:16:20 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 09 Aug 2022 22:16:21 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 09 Aug 2022 22:16:22 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 09 Aug 2022 22:16:23 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 09 Aug 2022 22:16:31 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 09 Aug 2022 22:16:31 GMT
CMD ["python3"]
# Wed, 10 Aug 2022 03:30:07 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 10 Aug 2022 03:30:08 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 10 Aug 2022 03:33:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 10 Aug 2022 03:33:03 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 10 Aug 2022 03:33:04 GMT
WORKDIR /etc/satosa
# Wed, 10 Aug 2022 03:33:06 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 10 Aug 2022 03:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 03:33:07 GMT
EXPOSE 8080
# Wed, 10 Aug 2022 03:33:08 GMT
USER satosa:satosa
# Wed, 10 Aug 2022 03:33:09 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6e4c463b4b085b81ccd90e5d99d5d5b64a56c2f756e7ff5575080b0efc2e9f`  
		Last Modified: Tue, 09 Aug 2022 23:12:22 GMT  
		Size: 689.1 KB (689070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30e501e19288fafd4b62af6aaf0b588b8da1b9f7bf0ed0bd8c7cf5550131f4b`  
		Last Modified: Tue, 09 Aug 2022 23:13:12 GMT  
		Size: 12.7 MB (12700838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5383c9c382f8845fcf42a8ea747ddb3a99c87e277380a509277f27c6bf8d85`  
		Last Modified: Tue, 09 Aug 2022 23:13:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2450ac53e437f841f48f00e832466a3d7ce73190f3f5255c89dfb89edcd9193`  
		Last Modified: Tue, 09 Aug 2022 23:13:11 GMT  
		Size: 3.0 MB (3045003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3183acab5e336c62f2d06a000d65364d4484e755eb4c01749dd6e443ee703e32`  
		Last Modified: Wed, 10 Aug 2022 03:34:01 GMT  
		Size: 8.5 MB (8512861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350ea1863d968db10b0fe1fd8772d772c84631136d5fb13934b7c5a360cf66fc`  
		Last Modified: Wed, 10 Aug 2022 03:34:28 GMT  
		Size: 145.3 MB (145257262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92895882e21832e6f4d040fa6f60752d36b168dbc7f3893d1fc81a19da18cfc3`  
		Last Modified: Wed, 10 Aug 2022 03:33:59 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85df40b1b491557b15d24c816c82279561fd23244d53603eeea4f9976ce8766`  
		Last Modified: Wed, 10 Aug 2022 03:33:59 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine3.16` - linux; ppc64le

```console
$ docker pull satosa@sha256:f70b3121c8db732d980c4272ea937145d0745875aba33578b5667bbaf28fb1ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164310759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef00aeaa317867dd9dca82b0661794be10c5d0a082d11a8f76b597b76e88cb55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:29:30 GMT
ADD file:69e4080f15f54e2d8f8aa25fdcba9c01dde149d43592edd5023106675e54a769 in / 
# Mon, 18 Jul 2022 21:29:31 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 04:30:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 04:30:31 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 04:30:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 04:30:33 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 19:40:20 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 20:04:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 20:05:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 20:05:00 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 20:05:00 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 20:05:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 20:05:01 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 20:05:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 20:05:13 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 21:15:12 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 21:15:12 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 21:21:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 21:21:41 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 21:21:41 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 21:21:42 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 21:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 21:21:42 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 21:21:43 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 21:21:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:602896d442490cd3fbb6599f0f862d3673b7cd58eca3ac842b8e09bf8d012443`  
		Last Modified: Mon, 18 Jul 2022 19:09:09 GMT  
		Size: 2.8 MB (2789923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6556a4bf6509d5fd24900f56a6175bd811b9dd8c6f4f51e2732b6888a2b8933`  
		Last Modified: Wed, 27 Jul 2022 13:49:16 GMT  
		Size: 677.0 KB (676971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c735731e55a5ddb324dd5eb175e1f3d88895a77ea93b8fb08428ee522445708b`  
		Last Modified: Wed, 03 Aug 2022 20:44:16 GMT  
		Size: 12.8 MB (12819587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e525d9b2b00fc7130f21f05f981c44d849b279417c15b38703c3f11d3c9bd667`  
		Last Modified: Wed, 03 Aug 2022 20:44:13 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9bc880d40f528e2c6046dd7bad61fc78f27a3fbebe3f45d1348a72ace67d9b`  
		Last Modified: Wed, 03 Aug 2022 20:44:15 GMT  
		Size: 3.0 MB (3043656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b74e25b6a705707a07e0411366545458ad05f07844bde5b7bebddd988e69068`  
		Last Modified: Wed, 03 Aug 2022 21:23:08 GMT  
		Size: 8.5 MB (8476895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141bd7d880682fd816129f41549c798cabb9e94494f7ee7714d6e83e63606b82`  
		Last Modified: Wed, 03 Aug 2022 21:23:23 GMT  
		Size: 136.5 MB (136491944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b412f1d24946cb1e7f3d66a4ae5595d3b71ae6040af529dc49507cb1dd4e06c`  
		Last Modified: Wed, 03 Aug 2022 21:23:06 GMT  
		Size: 9.4 KB (9434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8aa237953d155695df1943bb27b03cf1cc3f1716ea63b1cf5a8b12d97cd6cea`  
		Last Modified: Wed, 03 Aug 2022 21:23:06 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8-bullseye`

```console
$ docker pull satosa@sha256:b952f0d280486a79665537c956718dec4fff75e9e6a343a79e1048bc3bf3c861
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

### `satosa:8-bullseye` - linux; amd64

```console
$ docker pull satosa@sha256:3d92574bf94e0395a41762efa378d221f605ea12bea73ae604c71310fe6036fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82653895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d245b28169a1e1f7dd888fa2381fc3aa02a91b2210f7b6b481c4016173ac8d0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 09:39:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 09:39:09 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 09:39:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 09:39:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 10:15:41 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 10:26:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 10:26:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 10:26:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 10:26:31 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 11:46:24 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 11:46:24 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 11:47:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 11:47:19 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 11:47:19 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 11:47:19 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 11:47:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 11:47:20 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 11:47:20 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 11:47:20 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126aaa6587b8608b62fa39019a891e98460e23bad2d04fb235c4dc8fae2adf3c`  
		Last Modified: Tue, 02 Aug 2022 12:33:29 GMT  
		Size: 1.1 MB (1076278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd06b55ca686f29b26c8a7e051ce98ad571fd6cf22bba07f5cd17e98fd31e13`  
		Last Modified: Wed, 03 Aug 2022 11:18:36 GMT  
		Size: 12.1 MB (12106838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3950cece0b727ab257c49317871d00f22d2abcb77bcce19ddf86aab5c4d88e21`  
		Last Modified: Wed, 03 Aug 2022 11:18:34 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e27c1167cc2a09e30e53c0fd2933e189e20b4785284e84a919fe5fd3013388b`  
		Last Modified: Wed, 03 Aug 2022 11:18:35 GMT  
		Size: 3.3 MB (3336043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb69b4e4539d59ea0fbed39563b5042d023cd4713d9a38bde6b930fb548e8b9a`  
		Last Modified: Wed, 03 Aug 2022 11:48:44 GMT  
		Size: 19.6 MB (19587061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620aa9bb44333fe5af9257a47e9e0de0e7a0596721959465531442e2b753aa5a`  
		Last Modified: Wed, 03 Aug 2022 11:48:44 GMT  
		Size: 15.2 MB (15169129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffc5c41689ca0d4f9b9e1beea0953f2bec48e3ab6becfee1b8c8862100aadbe`  
		Last Modified: Wed, 03 Aug 2022 11:48:41 GMT  
		Size: 9.4 KB (9443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebafed1e50948cce1a8ec458a2dbc933ec93924419791a83613e224356054ee`  
		Last Modified: Wed, 03 Aug 2022 11:48:41 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-bullseye` - linux; arm variant v5

```console
$ docker pull satosa@sha256:e4ee7d4d43b26f8dc6b5a7d8358af5463aa5ebf830249e6272afbe2a819e9732
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.7 MB (203698783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160cc52ce9b78d794b4acbd3286cc62c771bad645eb50e8c9af6722d743f166c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:10 GMT
ADD file:4cd2f95737fd3007912428eeac56036c9e67e989e66cec08a8be99da47f88494 in / 
# Tue, 02 Aug 2022 00:49:10 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:38:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 20:38:12 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 20:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:38:23 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 22:45:24 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 23:08:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 23:08:11 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 23:08:11 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 23:08:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 23:08:30 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 19:10:52 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 19:10:52 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 19:17:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 19:17:42 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 19:17:42 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 19:17:43 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 19:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 19:17:43 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 19:17:43 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 19:17:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5890b0ca6af5e8467a488e68716691950496a8f247d0495c2d595ddcb1893aff`  
		Last Modified: Tue, 02 Aug 2022 00:56:06 GMT  
		Size: 28.9 MB (28905515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eafe902d3c868e979e01e5c5aca6567b8be8b60814b9e1ce93c2b749451b410`  
		Last Modified: Wed, 03 Aug 2022 02:16:47 GMT  
		Size: 1.1 MB (1059641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e073b0922c53e3aee167b94b195f01b7740c95a691b391e30bbc1dd36133f578`  
		Last Modified: Wed, 03 Aug 2022 02:18:15 GMT  
		Size: 11.7 MB (11687058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1563deb88ac81fbc07f66164de09058989bc2f52e4b201209996fc610e7424`  
		Last Modified: Wed, 03 Aug 2022 02:18:11 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9586a9ae76d2fcf29975a3cbac30868417a5e7209b4d681ab4d8cdc9417e1127`  
		Last Modified: Wed, 03 Aug 2022 02:18:13 GMT  
		Size: 3.3 MB (3335517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2138d4d7c7c422781a7da5bbba917dfee3de2e44c0b89e2c05cd5fb54d6aec`  
		Last Modified: Wed, 03 Aug 2022 19:18:28 GMT  
		Size: 21.2 MB (21220513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ec77684813e78ff3c43e62e86fde2b1964089fb2e02c36be1b197e18d76199`  
		Last Modified: Wed, 03 Aug 2022 19:18:38 GMT  
		Size: 137.5 MB (137478750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecfeff163b4d6f23860d774bf123b6ad13105fce4fa35bddd9e46a56b0c09af`  
		Last Modified: Wed, 03 Aug 2022 19:18:21 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb3f6f2ab2014dd8287001b208c1dc97200c2c3e16a2cb980fd938dfd82858b`  
		Last Modified: Wed, 03 Aug 2022 19:18:22 GMT  
		Size: 2.1 KB (2111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-bullseye` - linux; arm variant v7

```console
$ docker pull satosa@sha256:1eb7ef57547ada8079868ad16a792df4e4cbc8571c4b2beb50d5682d1bc6250f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202351243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194a9b56fc0cc44a0542e47df53c65db1e4f7a579b5a8624e2b202e21462c73d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:58:59 GMT
ADD file:1575b776a15adacebc0875642e97a80807d42dcfc8917e1406d47af7ac244c97 in / 
# Tue, 02 Aug 2022 00:58:59 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:34:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 04:34:22 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 04:34:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 04:34:30 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 06:30:14 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 06:52:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 06:52:09 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 06:52:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 06:52:24 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 13:20:49 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 13:20:50 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 13:26:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 13:26:45 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 13:26:45 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 13:26:45 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 13:26:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 13:26:45 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 13:26:45 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 13:26:45 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1dd75a3a9c893a7dc313f683dd62464b7eab6c6d522ee62c8a17022631830f32`  
		Last Modified: Tue, 02 Aug 2022 01:06:45 GMT  
		Size: 26.6 MB (26560586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4206fea8c3d0ae09213fad25e06bb550a03c76c2b15e7a3c134ee5e2d217cd`  
		Last Modified: Wed, 03 Aug 2022 11:19:22 GMT  
		Size: 1.0 MB (1041632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed9dda465ec974f3e81b6b5f48dee0c43b63aeae625042e1e5f8ca482d43f1f`  
		Last Modified: Wed, 03 Aug 2022 11:21:19 GMT  
		Size: 11.2 MB (11205345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c669588520ce26d52819574b6ac8f40bc121ec539aae49c4cdc6aa899fcea`  
		Last Modified: Wed, 03 Aug 2022 11:21:15 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75c71e6575f11c76771634448c2e1c7e6988853591c1422d979aaf3dfa73569`  
		Last Modified: Wed, 03 Aug 2022 11:21:17 GMT  
		Size: 3.3 MB (3335656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d5ac04f9c39c2ba1d884f419e586ede32f2779ea0bbb6a7033e0f70c79d670`  
		Last Modified: Thu, 04 Aug 2022 13:31:15 GMT  
		Size: 20.9 MB (20949533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65844885dbff2fac2bccf9e5a7b69d9c423352d19d5ffb5eeca720f5e2a10886`  
		Last Modified: Thu, 04 Aug 2022 13:31:26 GMT  
		Size: 139.2 MB (139246702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53ebddc2eb90a987a1bae1b3a245f2d88ae7ea81a35f85f6bfdf10891217d58`  
		Last Modified: Thu, 04 Aug 2022 13:31:10 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa39e50e9a3812f026202131476b98a06e4a65a16a21fee180aeb54d979e2cb8`  
		Last Modified: Thu, 04 Aug 2022 13:31:10 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-bullseye` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:8a7bc186f7c0a8725b284d01a4dceac8636d5f7f96b11f0d4031fd66f199e2b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79849083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56454aaf2924873a1f55890e93e1c83261d4047ce84a080d73750691435b3d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:03:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 12:03:30 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 12:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:03:36 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 09:19:10 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 09:29:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 09:29:22 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 09:29:22 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 09:29:23 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 09:29:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 09:29:25 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 09:29:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 09:29:37 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 10:39:28 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 10:39:28 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 10:40:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 10:40:15 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 10:40:16 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 10:40:18 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 10:40:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 10:40:19 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 10:40:20 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 10:40:21 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f101f90cc8f7640b7db5f7094941a1fe4ff28e11a968d3a36f146a89a480ecbb`  
		Last Modified: Tue, 02 Aug 2022 14:47:06 GMT  
		Size: 1.1 MB (1063812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a5d6cf27653f158e4f7552f31dc146332b6d820679ee42ebff5b4e47f4dac`  
		Last Modified: Wed, 03 Aug 2022 10:31:15 GMT  
		Size: 12.2 MB (12153733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd415bdc2c72c852623e384c90826d41aa2739adbc3158bd814bc3e562ab16ea`  
		Last Modified: Wed, 03 Aug 2022 10:31:13 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90ceb316b2d011719d35fb58a5d69ec1b84ebc6a9ab5568354ca370aad48524`  
		Last Modified: Wed, 03 Aug 2022 10:31:14 GMT  
		Size: 3.1 MB (3119919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7a23c6e6d4ea56699e3033f9fd616c6fa79290a257066f21578bf773f283cb`  
		Last Modified: Wed, 03 Aug 2022 10:42:23 GMT  
		Size: 19.3 MB (19324710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f64adba6c540f9f4fde33df9a99fa32be543c937e20b203b409ba3340f7b62`  
		Last Modified: Wed, 03 Aug 2022 10:42:23 GMT  
		Size: 14.1 MB (14120866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9df97e7203d91c6109257b6e98c0bb926732214ee96a7110c86550f8c271b74`  
		Last Modified: Wed, 03 Aug 2022 10:42:20 GMT  
		Size: 9.4 KB (9394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d56269ee4307b5c76ba7efef9346008e1440979b95ee777b9d5e8e3e4ead5b1`  
		Last Modified: Wed, 03 Aug 2022 10:42:20 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-bullseye` - linux; 386

```console
$ docker pull satosa@sha256:ff2180ab006e1d173a6d157a2ef8b05c4abae7d45d5693889e12f05e6861a42d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207396057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b9632c4df58a4c5e3e68e82bf8bab7462b2530f9ecfb108feb8726a85ab4d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:39:20 GMT
ADD file:f771e2286465694126158821089d801c7296376be2a56189e6041a15d2fe79f5 in / 
# Tue, 02 Aug 2022 00:39:21 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 11:22:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 11:22:53 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 11:22:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 11:22:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 20:51:53 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 21:03:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 21:03:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 21:03:55 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 21:03:56 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 21:03:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 21:03:58 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 21:04:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 21:04:12 GMT
CMD ["python3"]
# Tue, 02 Aug 2022 22:21:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 02 Aug 2022 22:21:44 GMT
ENV SATOSA_VERSION=8.1.1
# Tue, 02 Aug 2022 23:39:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 02 Aug 2022 23:39:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 02 Aug 2022 23:39:26 GMT
WORKDIR /etc/satosa
# Tue, 02 Aug 2022 23:39:28 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Tue, 02 Aug 2022 23:39:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 23:39:29 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 23:39:30 GMT
USER satosa:satosa
# Tue, 02 Aug 2022 23:39:31 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:90eb7f0ce9f33cf5dcd67d54c2fa606186dbaa5f95b6046f36145097267f9e53`  
		Last Modified: Tue, 02 Aug 2022 00:45:14 GMT  
		Size: 32.4 MB (32374054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd27ead98f25cd891e8dfae23b5500c856f3a9db336a545eed8b5f180a6df0b4`  
		Last Modified: Tue, 02 Aug 2022 14:37:54 GMT  
		Size: 1.1 MB (1088442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7362ecffe5fefdfcff89188358cb648fae40c1fed6254cd3325ef1c340a0ca9b`  
		Last Modified: Tue, 02 Aug 2022 22:15:01 GMT  
		Size: 12.2 MB (12224818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fb82e70fda9a811619f0b6cfd165d59473bcc467e702a70231630e64335b18`  
		Last Modified: Tue, 02 Aug 2022 22:14:59 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab067ab28a29ee91955ebd00b4849cd1d1993a430051ce801b5eaffeeb59b976`  
		Last Modified: Tue, 02 Aug 2022 22:15:00 GMT  
		Size: 3.1 MB (3119814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c68c7fda4b282e37efe94863aed2872d62133ead0fed4a4b4174eab16a125f`  
		Last Modified: Tue, 02 Aug 2022 23:40:27 GMT  
		Size: 22.6 MB (22586591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4630af60cc9f0637de40da0789c8be2b49091d860ae7f21753e736c5a24b0fac`  
		Last Modified: Tue, 02 Aug 2022 23:40:44 GMT  
		Size: 136.0 MB (135990599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ba92ddedaf8e60d74aac7773867aec0a84b2812ba92a5742090bee107e7736`  
		Last Modified: Tue, 02 Aug 2022 23:40:24 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e28ea4f42ac6baac91e14de0ee8d101956ac6d64c7d4078bb57ebfddde33184`  
		Last Modified: Tue, 02 Aug 2022 23:40:24 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-bullseye` - linux; mips64le

```console
$ docker pull satosa@sha256:b9bdbc69a8a0be593fe150cbd4334f006447c17a9538b850002e7fa96445593b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.8 MB (205844024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7d3830a289e7a92a0277b60e6cce741d4887ea889e4e236cdd2d878fb1f64b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:10:34 GMT
ADD file:6dc22a1e5b5fcf23f2549406ddcc45c4e244f46e21eafa881de81fa87438e5d8 in / 
# Tue, 02 Aug 2022 01:10:38 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 10:25:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 10:25:08 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 10:25:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:25:36 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 04 Aug 2022 04:16:09 GMT
ENV PYTHON_VERSION=3.10.6
# Thu, 04 Aug 2022 05:33:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Thu, 04 Aug 2022 05:33:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 04 Aug 2022 05:33:27 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Thu, 04 Aug 2022 05:33:30 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Thu, 04 Aug 2022 05:33:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Thu, 04 Aug 2022 05:33:35 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Thu, 04 Aug 2022 05:34:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 04 Aug 2022 05:34:30 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 08:35:12 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 08:35:15 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 08:52:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 08:52:17 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 08:52:21 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 08:52:25 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 08:52:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 08:52:34 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 08:52:39 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 08:52:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:88350749a27614c791450c256b051f023d81cdd256211274b1efac493779d2be`  
		Last Modified: Tue, 02 Aug 2022 01:21:02 GMT  
		Size: 29.6 MB (29628964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61130d003a0ea87819935a3a252db1861d9b87e1313fa7988d5f0642637f3e`  
		Last Modified: Tue, 02 Aug 2022 23:46:40 GMT  
		Size: 1.0 MB (1049605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e786491697e5d2bd3dee622f7eae98810c04c895d5024e910e2394f92b37ad8`  
		Last Modified: Thu, 04 Aug 2022 08:14:51 GMT  
		Size: 12.1 MB (12124464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fb1366c066d6bf94df2bf081524439083c14a1f292da85f218000ac515a2f5`  
		Last Modified: Thu, 04 Aug 2022 08:14:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe7637d1173b353af8622199dfbc92d0f74f8cff129fe540541b9c069a058d3`  
		Last Modified: Thu, 04 Aug 2022 08:14:46 GMT  
		Size: 3.1 MB (3120804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4655831cce551d936028a78d3d4a295cd96e3ca02ea0f5f726d0b963350a0e`  
		Last Modified: Thu, 04 Aug 2022 08:53:18 GMT  
		Size: 21.3 MB (21288233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54965dd4effca16f75a92cdac5dd71e708a50d218ca30b0806964a58d8b726ee`  
		Last Modified: Thu, 04 Aug 2022 08:53:58 GMT  
		Size: 138.6 MB (138620211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a449c61594c6b3d2e0fa03d876ebe6fc8561eaa1d46ebf088772a42dea52b596`  
		Last Modified: Thu, 04 Aug 2022 08:53:06 GMT  
		Size: 9.4 KB (9396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54e620f3a05fe34c293ac1de03899ec567f49faa21a8db43216f796387f8f65`  
		Last Modified: Thu, 04 Aug 2022 08:53:06 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-bullseye` - linux; ppc64le

```console
$ docker pull satosa@sha256:b84ad93ccca31f2ba03b7c0586ad9f3a2d71764d4338922af798ae737ec87f23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212244381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f29a99f45c08fb90c8ad9dec84fd55c14d0ca8ecbc00c2160fc3464a14feca9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:17:30 GMT
ADD file:3a95a896d463569ce82199957052b3467123a4bd3385a0a4e397cf08402a99c3 in / 
# Tue, 02 Aug 2022 01:17:32 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:03:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 16:03:13 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 16:03:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 16:03:24 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 18:10:29 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 18:43:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 18:43:03 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 18:43:03 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 18:43:03 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 18:43:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 18:43:04 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 18:43:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 18:43:25 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 21:09:20 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 21:09:21 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 21:14:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 21:14:39 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 21:14:39 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 21:14:40 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 21:14:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 21:14:41 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 21:14:41 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 21:14:42 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5241cd116d6e6e2d62f3d8c2245b74daca9f6cc154eaccd738feb41984c74714`  
		Last Modified: Tue, 02 Aug 2022 01:24:39 GMT  
		Size: 35.3 MB (35272771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf6dcfcb4fa2f4e24ce6bed8b3eda6b0d49d92062cb34d95830e4e9f512270`  
		Last Modified: Wed, 03 Aug 2022 00:14:29 GMT  
		Size: 1.1 MB (1094658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdc50327f93cca5ad2c5f8500471040045b715045a9a4852ece90b3155d5aea`  
		Last Modified: Wed, 03 Aug 2022 20:42:55 GMT  
		Size: 12.5 MB (12473465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49f3fdf44cc1cf9b0e2d32c8ea2b62a0d3eb7eac481b56c9d11e44c66b764fe`  
		Last Modified: Wed, 03 Aug 2022 20:42:52 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd9d6c8cb5530b56f02a736bb1cc24d2d0ffc11d6fb55dc6befb0e114a1ff74`  
		Last Modified: Wed, 03 Aug 2022 20:42:53 GMT  
		Size: 3.3 MB (3336216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209342dd334b280e74196c0e693487033f7f2d08880ab61f5f9113dbbd5d0461`  
		Last Modified: Wed, 03 Aug 2022 21:22:32 GMT  
		Size: 22.2 MB (22158681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11809242e6bd5adbd0096d37646b954f666a1e2a107dd5442773977caa919360`  
		Last Modified: Wed, 03 Aug 2022 21:22:45 GMT  
		Size: 137.9 MB (137896801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa36501b6a1d8ec2e51a6a162f1f43d70ea4b035335513b65b800346790717`  
		Last Modified: Wed, 03 Aug 2022 21:22:27 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fe38c0944e97231334e780f32f3cd041644756c5b195812b19edd697268021`  
		Last Modified: Wed, 03 Aug 2022 21:22:27 GMT  
		Size: 2.1 KB (2113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-bullseye` - linux; s390x

```console
$ docker pull satosa@sha256:f52b8375aeb8b39ad8ae5b9f05f4f94a47f4776b3f500aeeadee19c4ed572f5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202163420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f253b8b35e8bbaf69f23beb8a8584dc48a0c682127faa17ed9d639b33dfdf3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 08:30:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 08:30:40 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 08:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 08:30:44 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 22:09:42 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 22:18:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 22:18:03 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 22:18:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 22:18:13 GMT
CMD ["python3"]
# Tue, 02 Aug 2022 23:28:28 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 02 Aug 2022 23:28:31 GMT
ENV SATOSA_VERSION=8.1.1
# Tue, 02 Aug 2022 23:32:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 02 Aug 2022 23:33:02 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 02 Aug 2022 23:33:02 GMT
WORKDIR /etc/satosa
# Tue, 02 Aug 2022 23:33:02 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Tue, 02 Aug 2022 23:33:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 23:33:02 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 23:33:03 GMT
USER satosa:satosa
# Tue, 02 Aug 2022 23:33:03 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c36d12a9d2aa3bd2ed5880b10e768bae6cab779992e198cf595d3b8d6924d5`  
		Last Modified: Tue, 02 Aug 2022 10:43:27 GMT  
		Size: 1.1 MB (1075771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a2fa2a5f3f4be291fac87451996292e32ad4b6b7e7ae168c720b6501ba676f`  
		Last Modified: Tue, 02 Aug 2022 23:23:49 GMT  
		Size: 11.9 MB (11900903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1958402e81da32fc50ee2b3d3d48a5714015a6589a9b0882e2e0862173874f52`  
		Last Modified: Tue, 02 Aug 2022 23:23:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adc16df778c23094a004c62669c6de553142901db4933d76959d223598473b`  
		Last Modified: Tue, 02 Aug 2022 23:23:49 GMT  
		Size: 3.3 MB (3335624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5f479e9444a18e7100a74300ba30ab5818c9023c386c0a537811de457f1e99`  
		Last Modified: Tue, 02 Aug 2022 23:33:39 GMT  
		Size: 19.6 MB (19580744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573792100821147cd9e469e566ed70175d1fe8ec2b68e371484abc92f0aeaf74`  
		Last Modified: Tue, 02 Aug 2022 23:33:45 GMT  
		Size: 136.6 MB (136618328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cb6a07895307e25b49bb3cdebc3f6e29fef231b0390c00ddacc6b74ee5f9fd`  
		Last Modified: Tue, 02 Aug 2022 23:33:36 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0ce3aebbe275e54928297909f6f1ed7c7beee5c901706ccef91eec96eb8bc5`  
		Last Modified: Tue, 02 Aug 2022 23:33:36 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.1`

```console
$ docker pull satosa@sha256:b952f0d280486a79665537c956718dec4fff75e9e6a343a79e1048bc3bf3c861
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

### `satosa:8.1` - linux; amd64

```console
$ docker pull satosa@sha256:3d92574bf94e0395a41762efa378d221f605ea12bea73ae604c71310fe6036fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82653895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d245b28169a1e1f7dd888fa2381fc3aa02a91b2210f7b6b481c4016173ac8d0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 09:39:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 09:39:09 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 09:39:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 09:39:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 10:15:41 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 10:26:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 10:26:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 10:26:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 10:26:31 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 11:46:24 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 11:46:24 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 11:47:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 11:47:19 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 11:47:19 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 11:47:19 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 11:47:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 11:47:20 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 11:47:20 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 11:47:20 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126aaa6587b8608b62fa39019a891e98460e23bad2d04fb235c4dc8fae2adf3c`  
		Last Modified: Tue, 02 Aug 2022 12:33:29 GMT  
		Size: 1.1 MB (1076278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd06b55ca686f29b26c8a7e051ce98ad571fd6cf22bba07f5cd17e98fd31e13`  
		Last Modified: Wed, 03 Aug 2022 11:18:36 GMT  
		Size: 12.1 MB (12106838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3950cece0b727ab257c49317871d00f22d2abcb77bcce19ddf86aab5c4d88e21`  
		Last Modified: Wed, 03 Aug 2022 11:18:34 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e27c1167cc2a09e30e53c0fd2933e189e20b4785284e84a919fe5fd3013388b`  
		Last Modified: Wed, 03 Aug 2022 11:18:35 GMT  
		Size: 3.3 MB (3336043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb69b4e4539d59ea0fbed39563b5042d023cd4713d9a38bde6b930fb548e8b9a`  
		Last Modified: Wed, 03 Aug 2022 11:48:44 GMT  
		Size: 19.6 MB (19587061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620aa9bb44333fe5af9257a47e9e0de0e7a0596721959465531442e2b753aa5a`  
		Last Modified: Wed, 03 Aug 2022 11:48:44 GMT  
		Size: 15.2 MB (15169129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffc5c41689ca0d4f9b9e1beea0953f2bec48e3ab6becfee1b8c8862100aadbe`  
		Last Modified: Wed, 03 Aug 2022 11:48:41 GMT  
		Size: 9.4 KB (9443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebafed1e50948cce1a8ec458a2dbc933ec93924419791a83613e224356054ee`  
		Last Modified: Wed, 03 Aug 2022 11:48:41 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1` - linux; arm variant v5

```console
$ docker pull satosa@sha256:e4ee7d4d43b26f8dc6b5a7d8358af5463aa5ebf830249e6272afbe2a819e9732
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.7 MB (203698783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160cc52ce9b78d794b4acbd3286cc62c771bad645eb50e8c9af6722d743f166c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:10 GMT
ADD file:4cd2f95737fd3007912428eeac56036c9e67e989e66cec08a8be99da47f88494 in / 
# Tue, 02 Aug 2022 00:49:10 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:38:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 20:38:12 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 20:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:38:23 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 22:45:24 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 23:08:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 23:08:11 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 23:08:11 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 23:08:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 23:08:30 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 19:10:52 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 19:10:52 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 19:17:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 19:17:42 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 19:17:42 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 19:17:43 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 19:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 19:17:43 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 19:17:43 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 19:17:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5890b0ca6af5e8467a488e68716691950496a8f247d0495c2d595ddcb1893aff`  
		Last Modified: Tue, 02 Aug 2022 00:56:06 GMT  
		Size: 28.9 MB (28905515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eafe902d3c868e979e01e5c5aca6567b8be8b60814b9e1ce93c2b749451b410`  
		Last Modified: Wed, 03 Aug 2022 02:16:47 GMT  
		Size: 1.1 MB (1059641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e073b0922c53e3aee167b94b195f01b7740c95a691b391e30bbc1dd36133f578`  
		Last Modified: Wed, 03 Aug 2022 02:18:15 GMT  
		Size: 11.7 MB (11687058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1563deb88ac81fbc07f66164de09058989bc2f52e4b201209996fc610e7424`  
		Last Modified: Wed, 03 Aug 2022 02:18:11 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9586a9ae76d2fcf29975a3cbac30868417a5e7209b4d681ab4d8cdc9417e1127`  
		Last Modified: Wed, 03 Aug 2022 02:18:13 GMT  
		Size: 3.3 MB (3335517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2138d4d7c7c422781a7da5bbba917dfee3de2e44c0b89e2c05cd5fb54d6aec`  
		Last Modified: Wed, 03 Aug 2022 19:18:28 GMT  
		Size: 21.2 MB (21220513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ec77684813e78ff3c43e62e86fde2b1964089fb2e02c36be1b197e18d76199`  
		Last Modified: Wed, 03 Aug 2022 19:18:38 GMT  
		Size: 137.5 MB (137478750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecfeff163b4d6f23860d774bf123b6ad13105fce4fa35bddd9e46a56b0c09af`  
		Last Modified: Wed, 03 Aug 2022 19:18:21 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb3f6f2ab2014dd8287001b208c1dc97200c2c3e16a2cb980fd938dfd82858b`  
		Last Modified: Wed, 03 Aug 2022 19:18:22 GMT  
		Size: 2.1 KB (2111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1` - linux; arm variant v7

```console
$ docker pull satosa@sha256:1eb7ef57547ada8079868ad16a792df4e4cbc8571c4b2beb50d5682d1bc6250f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202351243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194a9b56fc0cc44a0542e47df53c65db1e4f7a579b5a8624e2b202e21462c73d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:58:59 GMT
ADD file:1575b776a15adacebc0875642e97a80807d42dcfc8917e1406d47af7ac244c97 in / 
# Tue, 02 Aug 2022 00:58:59 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:34:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 04:34:22 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 04:34:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 04:34:30 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 06:30:14 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 06:52:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 06:52:09 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 06:52:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 06:52:24 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 13:20:49 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 13:20:50 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 13:26:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 13:26:45 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 13:26:45 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 13:26:45 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 13:26:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 13:26:45 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 13:26:45 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 13:26:45 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1dd75a3a9c893a7dc313f683dd62464b7eab6c6d522ee62c8a17022631830f32`  
		Last Modified: Tue, 02 Aug 2022 01:06:45 GMT  
		Size: 26.6 MB (26560586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4206fea8c3d0ae09213fad25e06bb550a03c76c2b15e7a3c134ee5e2d217cd`  
		Last Modified: Wed, 03 Aug 2022 11:19:22 GMT  
		Size: 1.0 MB (1041632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed9dda465ec974f3e81b6b5f48dee0c43b63aeae625042e1e5f8ca482d43f1f`  
		Last Modified: Wed, 03 Aug 2022 11:21:19 GMT  
		Size: 11.2 MB (11205345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c669588520ce26d52819574b6ac8f40bc121ec539aae49c4cdc6aa899fcea`  
		Last Modified: Wed, 03 Aug 2022 11:21:15 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75c71e6575f11c76771634448c2e1c7e6988853591c1422d979aaf3dfa73569`  
		Last Modified: Wed, 03 Aug 2022 11:21:17 GMT  
		Size: 3.3 MB (3335656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d5ac04f9c39c2ba1d884f419e586ede32f2779ea0bbb6a7033e0f70c79d670`  
		Last Modified: Thu, 04 Aug 2022 13:31:15 GMT  
		Size: 20.9 MB (20949533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65844885dbff2fac2bccf9e5a7b69d9c423352d19d5ffb5eeca720f5e2a10886`  
		Last Modified: Thu, 04 Aug 2022 13:31:26 GMT  
		Size: 139.2 MB (139246702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53ebddc2eb90a987a1bae1b3a245f2d88ae7ea81a35f85f6bfdf10891217d58`  
		Last Modified: Thu, 04 Aug 2022 13:31:10 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa39e50e9a3812f026202131476b98a06e4a65a16a21fee180aeb54d979e2cb8`  
		Last Modified: Thu, 04 Aug 2022 13:31:10 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:8a7bc186f7c0a8725b284d01a4dceac8636d5f7f96b11f0d4031fd66f199e2b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79849083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56454aaf2924873a1f55890e93e1c83261d4047ce84a080d73750691435b3d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:03:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 12:03:30 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 12:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:03:36 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 09:19:10 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 09:29:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 09:29:22 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 09:29:22 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 09:29:23 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 09:29:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 09:29:25 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 09:29:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 09:29:37 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 10:39:28 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 10:39:28 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 10:40:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 10:40:15 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 10:40:16 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 10:40:18 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 10:40:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 10:40:19 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 10:40:20 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 10:40:21 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f101f90cc8f7640b7db5f7094941a1fe4ff28e11a968d3a36f146a89a480ecbb`  
		Last Modified: Tue, 02 Aug 2022 14:47:06 GMT  
		Size: 1.1 MB (1063812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a5d6cf27653f158e4f7552f31dc146332b6d820679ee42ebff5b4e47f4dac`  
		Last Modified: Wed, 03 Aug 2022 10:31:15 GMT  
		Size: 12.2 MB (12153733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd415bdc2c72c852623e384c90826d41aa2739adbc3158bd814bc3e562ab16ea`  
		Last Modified: Wed, 03 Aug 2022 10:31:13 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90ceb316b2d011719d35fb58a5d69ec1b84ebc6a9ab5568354ca370aad48524`  
		Last Modified: Wed, 03 Aug 2022 10:31:14 GMT  
		Size: 3.1 MB (3119919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7a23c6e6d4ea56699e3033f9fd616c6fa79290a257066f21578bf773f283cb`  
		Last Modified: Wed, 03 Aug 2022 10:42:23 GMT  
		Size: 19.3 MB (19324710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f64adba6c540f9f4fde33df9a99fa32be543c937e20b203b409ba3340f7b62`  
		Last Modified: Wed, 03 Aug 2022 10:42:23 GMT  
		Size: 14.1 MB (14120866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9df97e7203d91c6109257b6e98c0bb926732214ee96a7110c86550f8c271b74`  
		Last Modified: Wed, 03 Aug 2022 10:42:20 GMT  
		Size: 9.4 KB (9394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d56269ee4307b5c76ba7efef9346008e1440979b95ee777b9d5e8e3e4ead5b1`  
		Last Modified: Wed, 03 Aug 2022 10:42:20 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1` - linux; 386

```console
$ docker pull satosa@sha256:ff2180ab006e1d173a6d157a2ef8b05c4abae7d45d5693889e12f05e6861a42d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207396057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b9632c4df58a4c5e3e68e82bf8bab7462b2530f9ecfb108feb8726a85ab4d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:39:20 GMT
ADD file:f771e2286465694126158821089d801c7296376be2a56189e6041a15d2fe79f5 in / 
# Tue, 02 Aug 2022 00:39:21 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 11:22:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 11:22:53 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 11:22:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 11:22:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 20:51:53 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 21:03:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 21:03:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 21:03:55 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 21:03:56 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 21:03:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 21:03:58 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 21:04:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 21:04:12 GMT
CMD ["python3"]
# Tue, 02 Aug 2022 22:21:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 02 Aug 2022 22:21:44 GMT
ENV SATOSA_VERSION=8.1.1
# Tue, 02 Aug 2022 23:39:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 02 Aug 2022 23:39:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 02 Aug 2022 23:39:26 GMT
WORKDIR /etc/satosa
# Tue, 02 Aug 2022 23:39:28 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Tue, 02 Aug 2022 23:39:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 23:39:29 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 23:39:30 GMT
USER satosa:satosa
# Tue, 02 Aug 2022 23:39:31 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:90eb7f0ce9f33cf5dcd67d54c2fa606186dbaa5f95b6046f36145097267f9e53`  
		Last Modified: Tue, 02 Aug 2022 00:45:14 GMT  
		Size: 32.4 MB (32374054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd27ead98f25cd891e8dfae23b5500c856f3a9db336a545eed8b5f180a6df0b4`  
		Last Modified: Tue, 02 Aug 2022 14:37:54 GMT  
		Size: 1.1 MB (1088442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7362ecffe5fefdfcff89188358cb648fae40c1fed6254cd3325ef1c340a0ca9b`  
		Last Modified: Tue, 02 Aug 2022 22:15:01 GMT  
		Size: 12.2 MB (12224818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fb82e70fda9a811619f0b6cfd165d59473bcc467e702a70231630e64335b18`  
		Last Modified: Tue, 02 Aug 2022 22:14:59 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab067ab28a29ee91955ebd00b4849cd1d1993a430051ce801b5eaffeeb59b976`  
		Last Modified: Tue, 02 Aug 2022 22:15:00 GMT  
		Size: 3.1 MB (3119814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c68c7fda4b282e37efe94863aed2872d62133ead0fed4a4b4174eab16a125f`  
		Last Modified: Tue, 02 Aug 2022 23:40:27 GMT  
		Size: 22.6 MB (22586591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4630af60cc9f0637de40da0789c8be2b49091d860ae7f21753e736c5a24b0fac`  
		Last Modified: Tue, 02 Aug 2022 23:40:44 GMT  
		Size: 136.0 MB (135990599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ba92ddedaf8e60d74aac7773867aec0a84b2812ba92a5742090bee107e7736`  
		Last Modified: Tue, 02 Aug 2022 23:40:24 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e28ea4f42ac6baac91e14de0ee8d101956ac6d64c7d4078bb57ebfddde33184`  
		Last Modified: Tue, 02 Aug 2022 23:40:24 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1` - linux; mips64le

```console
$ docker pull satosa@sha256:b9bdbc69a8a0be593fe150cbd4334f006447c17a9538b850002e7fa96445593b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.8 MB (205844024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7d3830a289e7a92a0277b60e6cce741d4887ea889e4e236cdd2d878fb1f64b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:10:34 GMT
ADD file:6dc22a1e5b5fcf23f2549406ddcc45c4e244f46e21eafa881de81fa87438e5d8 in / 
# Tue, 02 Aug 2022 01:10:38 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 10:25:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 10:25:08 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 10:25:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:25:36 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 04 Aug 2022 04:16:09 GMT
ENV PYTHON_VERSION=3.10.6
# Thu, 04 Aug 2022 05:33:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Thu, 04 Aug 2022 05:33:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 04 Aug 2022 05:33:27 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Thu, 04 Aug 2022 05:33:30 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Thu, 04 Aug 2022 05:33:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Thu, 04 Aug 2022 05:33:35 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Thu, 04 Aug 2022 05:34:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 04 Aug 2022 05:34:30 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 08:35:12 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 08:35:15 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 08:52:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 08:52:17 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 08:52:21 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 08:52:25 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 08:52:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 08:52:34 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 08:52:39 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 08:52:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:88350749a27614c791450c256b051f023d81cdd256211274b1efac493779d2be`  
		Last Modified: Tue, 02 Aug 2022 01:21:02 GMT  
		Size: 29.6 MB (29628964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61130d003a0ea87819935a3a252db1861d9b87e1313fa7988d5f0642637f3e`  
		Last Modified: Tue, 02 Aug 2022 23:46:40 GMT  
		Size: 1.0 MB (1049605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e786491697e5d2bd3dee622f7eae98810c04c895d5024e910e2394f92b37ad8`  
		Last Modified: Thu, 04 Aug 2022 08:14:51 GMT  
		Size: 12.1 MB (12124464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fb1366c066d6bf94df2bf081524439083c14a1f292da85f218000ac515a2f5`  
		Last Modified: Thu, 04 Aug 2022 08:14:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe7637d1173b353af8622199dfbc92d0f74f8cff129fe540541b9c069a058d3`  
		Last Modified: Thu, 04 Aug 2022 08:14:46 GMT  
		Size: 3.1 MB (3120804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4655831cce551d936028a78d3d4a295cd96e3ca02ea0f5f726d0b963350a0e`  
		Last Modified: Thu, 04 Aug 2022 08:53:18 GMT  
		Size: 21.3 MB (21288233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54965dd4effca16f75a92cdac5dd71e708a50d218ca30b0806964a58d8b726ee`  
		Last Modified: Thu, 04 Aug 2022 08:53:58 GMT  
		Size: 138.6 MB (138620211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a449c61594c6b3d2e0fa03d876ebe6fc8561eaa1d46ebf088772a42dea52b596`  
		Last Modified: Thu, 04 Aug 2022 08:53:06 GMT  
		Size: 9.4 KB (9396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54e620f3a05fe34c293ac1de03899ec567f49faa21a8db43216f796387f8f65`  
		Last Modified: Thu, 04 Aug 2022 08:53:06 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1` - linux; ppc64le

```console
$ docker pull satosa@sha256:b84ad93ccca31f2ba03b7c0586ad9f3a2d71764d4338922af798ae737ec87f23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212244381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f29a99f45c08fb90c8ad9dec84fd55c14d0ca8ecbc00c2160fc3464a14feca9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:17:30 GMT
ADD file:3a95a896d463569ce82199957052b3467123a4bd3385a0a4e397cf08402a99c3 in / 
# Tue, 02 Aug 2022 01:17:32 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:03:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 16:03:13 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 16:03:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 16:03:24 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 18:10:29 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 18:43:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 18:43:03 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 18:43:03 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 18:43:03 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 18:43:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 18:43:04 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 18:43:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 18:43:25 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 21:09:20 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 21:09:21 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 21:14:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 21:14:39 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 21:14:39 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 21:14:40 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 21:14:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 21:14:41 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 21:14:41 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 21:14:42 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5241cd116d6e6e2d62f3d8c2245b74daca9f6cc154eaccd738feb41984c74714`  
		Last Modified: Tue, 02 Aug 2022 01:24:39 GMT  
		Size: 35.3 MB (35272771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf6dcfcb4fa2f4e24ce6bed8b3eda6b0d49d92062cb34d95830e4e9f512270`  
		Last Modified: Wed, 03 Aug 2022 00:14:29 GMT  
		Size: 1.1 MB (1094658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdc50327f93cca5ad2c5f8500471040045b715045a9a4852ece90b3155d5aea`  
		Last Modified: Wed, 03 Aug 2022 20:42:55 GMT  
		Size: 12.5 MB (12473465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49f3fdf44cc1cf9b0e2d32c8ea2b62a0d3eb7eac481b56c9d11e44c66b764fe`  
		Last Modified: Wed, 03 Aug 2022 20:42:52 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd9d6c8cb5530b56f02a736bb1cc24d2d0ffc11d6fb55dc6befb0e114a1ff74`  
		Last Modified: Wed, 03 Aug 2022 20:42:53 GMT  
		Size: 3.3 MB (3336216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209342dd334b280e74196c0e693487033f7f2d08880ab61f5f9113dbbd5d0461`  
		Last Modified: Wed, 03 Aug 2022 21:22:32 GMT  
		Size: 22.2 MB (22158681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11809242e6bd5adbd0096d37646b954f666a1e2a107dd5442773977caa919360`  
		Last Modified: Wed, 03 Aug 2022 21:22:45 GMT  
		Size: 137.9 MB (137896801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa36501b6a1d8ec2e51a6a162f1f43d70ea4b035335513b65b800346790717`  
		Last Modified: Wed, 03 Aug 2022 21:22:27 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fe38c0944e97231334e780f32f3cd041644756c5b195812b19edd697268021`  
		Last Modified: Wed, 03 Aug 2022 21:22:27 GMT  
		Size: 2.1 KB (2113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1` - linux; s390x

```console
$ docker pull satosa@sha256:f52b8375aeb8b39ad8ae5b9f05f4f94a47f4776b3f500aeeadee19c4ed572f5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202163420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f253b8b35e8bbaf69f23beb8a8584dc48a0c682127faa17ed9d639b33dfdf3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 08:30:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 08:30:40 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 08:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 08:30:44 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 22:09:42 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 22:18:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 22:18:03 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 22:18:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 22:18:13 GMT
CMD ["python3"]
# Tue, 02 Aug 2022 23:28:28 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 02 Aug 2022 23:28:31 GMT
ENV SATOSA_VERSION=8.1.1
# Tue, 02 Aug 2022 23:32:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 02 Aug 2022 23:33:02 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 02 Aug 2022 23:33:02 GMT
WORKDIR /etc/satosa
# Tue, 02 Aug 2022 23:33:02 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Tue, 02 Aug 2022 23:33:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 23:33:02 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 23:33:03 GMT
USER satosa:satosa
# Tue, 02 Aug 2022 23:33:03 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c36d12a9d2aa3bd2ed5880b10e768bae6cab779992e198cf595d3b8d6924d5`  
		Last Modified: Tue, 02 Aug 2022 10:43:27 GMT  
		Size: 1.1 MB (1075771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a2fa2a5f3f4be291fac87451996292e32ad4b6b7e7ae168c720b6501ba676f`  
		Last Modified: Tue, 02 Aug 2022 23:23:49 GMT  
		Size: 11.9 MB (11900903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1958402e81da32fc50ee2b3d3d48a5714015a6589a9b0882e2e0862173874f52`  
		Last Modified: Tue, 02 Aug 2022 23:23:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adc16df778c23094a004c62669c6de553142901db4933d76959d223598473b`  
		Last Modified: Tue, 02 Aug 2022 23:23:49 GMT  
		Size: 3.3 MB (3335624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5f479e9444a18e7100a74300ba30ab5818c9023c386c0a537811de457f1e99`  
		Last Modified: Tue, 02 Aug 2022 23:33:39 GMT  
		Size: 19.6 MB (19580744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573792100821147cd9e469e566ed70175d1fe8ec2b68e371484abc92f0aeaf74`  
		Last Modified: Tue, 02 Aug 2022 23:33:45 GMT  
		Size: 136.6 MB (136618328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cb6a07895307e25b49bb3cdebc3f6e29fef231b0390c00ddacc6b74ee5f9fd`  
		Last Modified: Tue, 02 Aug 2022 23:33:36 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0ce3aebbe275e54928297909f6f1ed7c7beee5c901706ccef91eec96eb8bc5`  
		Last Modified: Tue, 02 Aug 2022 23:33:36 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.1-alpine`

```console
$ docker pull satosa@sha256:fa00b0ab420886685085b244405746ecce141ff81c408876a6d8c17f5e0960ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `satosa:8.1-alpine` - linux; amd64

```console
$ docker pull satosa@sha256:889e8b702bc04ca43d059bdf24c8db677954c87e5318ba8a93d795e450d485dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42508179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa3cc16430e95981e37a39687b5b6a8e23b8adf5eb81881cab4136b31de9b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:14:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 02:01:52 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 02:01:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 19 Jul 2022 02:01:54 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 10:48:21 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 11:00:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 11:00:14 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 11:00:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 11:00:21 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 11:47:34 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 11:47:34 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 11:48:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 11:48:18 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 11:48:19 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 11:48:19 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 11:48:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 11:48:19 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 11:48:19 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 11:48:19 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c14b1a767335de44f2bc926cb52487979a0fe602ac5429643dbb238f297fb`  
		Last Modified: Tue, 19 Jul 2022 02:56:13 GMT  
		Size: 666.8 KB (666769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571274b8543b548747b5e9bef700a89692fe9403cc364be8d6e8a0792ccfe2b4`  
		Last Modified: Wed, 03 Aug 2022 11:19:35 GMT  
		Size: 12.5 MB (12508608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f79a08255af5d614c7b4b81e358b5bb607bdcb14a6475c836d3d4f92f094846`  
		Last Modified: Wed, 03 Aug 2022 11:19:34 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6b20e3f6abd46292c29437a6917dc82b769ebb239e2d971aedb6695e057715`  
		Last Modified: Wed, 03 Aug 2022 11:19:34 GMT  
		Size: 3.0 MB (3043671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c974d4972d870a99bf0fba525cab86b298dd6e9405d3329a3495a164ae5c7`  
		Last Modified: Wed, 03 Aug 2022 11:49:00 GMT  
		Size: 9.4 MB (9398243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c482d554455c83821852ea2cd26eaf97f49bb1c7983342cec7242b8ea5432234`  
		Last Modified: Wed, 03 Aug 2022 11:49:01 GMT  
		Size: 14.1 MB (14080297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b861965b84abb04a92b63eb19a620daf7360785f485bc2d526885601454b19ca`  
		Last Modified: Wed, 03 Aug 2022 11:48:58 GMT  
		Size: 9.4 KB (9439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16e011f2d9efad78d03ac0d4c7abe2f694dfc5f6c158ef9fa350a3f21d22a8e`  
		Last Modified: Wed, 03 Aug 2022 11:48:58 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1-alpine` - linux; arm variant v6

```console
$ docker pull satosa@sha256:1ed78492e93849ebbee5cd80dd5e4a91eb2a41676fbc3d21584a17d402028ca7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160179359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e822b6bb9258ee22b55f2f03c3d389710a39d0a3fa1d10f1250cb00db2f3e268`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 19:49:37 GMT
ADD file:7a20333469e71664904a0cb8f61613250f2bd092b4a27bfa7bbae1dc7e21b7ed in / 
# Mon, 18 Jul 2022 19:49:37 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 00:30:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 00:30:05 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 00:30:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 00:30:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 19:50:04 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 20:30:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 02 Aug 2022 20:30:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 20:30:20 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 20:30:20 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 03:20:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 03:20:45 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 03:27:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 03:27:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 03:27:54 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 03:27:54 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 03:27:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 03:27:55 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 03:27:55 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 03:27:55 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b7885075fcd06a866d12dfd56eb704045eaadbd22dc03a224cd98715be566677`  
		Last Modified: Mon, 18 Jul 2022 19:08:42 GMT  
		Size: 2.6 MB (2606431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ebe8e3a2f83d0ddc301c9b9d6405376eecb906b92082e05d5e257eff5f6293`  
		Last Modified: Wed, 27 Jul 2022 11:08:23 GMT  
		Size: 672.3 KB (672287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b647934af90a736595f675559fd3aebbcdbcfc67277de68401980916f3c217d7`  
		Last Modified: Wed, 03 Aug 2022 00:13:17 GMT  
		Size: 12.1 MB (12085055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaef313095ff837d4848dec2c5e458a33e59ee4e1ab7a9d4e3d244d20b92fbf`  
		Last Modified: Wed, 03 Aug 2022 00:13:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba453d098c35b58faf7cc2ac6a90a0e9a8941dc90611ee397d12af0a546bbe87`  
		Last Modified: Wed, 03 Aug 2022 00:13:15 GMT  
		Size: 3.0 MB (3043708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0a90158473abc47e6b9744b5cc61265a9552ba9217486241f5b7b4a5d12eec`  
		Last Modified: Wed, 03 Aug 2022 03:28:44 GMT  
		Size: 8.3 MB (8280231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a82dd9e01f89340501ac0415caccc1ad608cc08d55219cb26db2226dc64b83`  
		Last Modified: Wed, 03 Aug 2022 03:29:07 GMT  
		Size: 133.5 MB (133479861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ee2ba314aef7361329abd7eaa7a8860079655317f4d5fc9d37f73f8b34de4`  
		Last Modified: Wed, 03 Aug 2022 03:28:39 GMT  
		Size: 9.4 KB (9438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24649d01bd9f34f035857fcb9324aef45128d255b0e7d7c9be9d0d9d58a928f3`  
		Last Modified: Wed, 03 Aug 2022 03:28:39 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1-alpine` - linux; arm variant v7

```console
$ docker pull satosa@sha256:9c12b392cb5946a433fe0c98001d362d79a953040068a9d0843c3a9a9c12fb8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163401667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55a50fb783bb28da31c92c6cff33c408ef6ea7e1c6da179086af8ce588f092d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:24:47 GMT
ADD file:68590e866bc6db27ad54d23de7dd275d0389cb86e4e6291a1243fcc234f2f7a1 in / 
# Mon, 18 Jul 2022 21:24:47 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 03:57:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 03:57:44 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 03:57:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 03:57:46 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 07:37:59 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 08:07:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 08:07:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 08:07:50 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 08:07:51 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 13:27:03 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 13:27:03 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 13:30:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 13:30:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 13:30:25 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 13:30:25 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 13:30:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 13:30:25 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 13:30:25 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 13:30:25 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a6b45ace95f42a930d15c33679ab9c85d46019b7e73954cadc73bb9ba176509b`  
		Last Modified: Mon, 18 Jul 2022 19:08:56 GMT  
		Size: 2.4 MB (2412307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d826ef3e3e077607452c51ac5332613cc0a20903abe17b56af4b973f31f0e9b7`  
		Last Modified: Wed, 27 Jul 2022 10:54:47 GMT  
		Size: 664.1 KB (664079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116f12212b7e97cde5b72713f0f3a3025a9ef6dffccdc353cd4d15407d343a72`  
		Last Modified: Wed, 03 Aug 2022 11:22:41 GMT  
		Size: 11.6 MB (11558755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef2affe775c9998dea9fd354aa8d4b6e97117d2092c84f1401265b9f9528bf7`  
		Last Modified: Wed, 03 Aug 2022 11:22:38 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032af4833525c8884057f85c0da98a7f2dedc337784e4ce3645fad79e6633b26`  
		Last Modified: Wed, 03 Aug 2022 11:22:39 GMT  
		Size: 3.0 MB (3043658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65c3d7d841a308ff58960bdd0832a9c2fc9d01d091b4478549cf91ad4551edc`  
		Last Modified: Thu, 04 Aug 2022 13:31:47 GMT  
		Size: 8.0 MB (8026973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553863577a06e5d191ae29abc79bb81603188e34e406ebce36a4e4da49320df8`  
		Last Modified: Thu, 04 Aug 2022 13:31:59 GMT  
		Size: 137.7 MB (137684108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d66d75890a5436b91b581c5023634cbedf248e1dbb622b1241f80c5a4ed29`  
		Last Modified: Thu, 04 Aug 2022 13:31:45 GMT  
		Size: 9.4 KB (9439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cab52b5f6577ce2ac31dd72be231ca9d43531003be80eacfe2f20bbfa5c5d5`  
		Last Modified: Thu, 04 Aug 2022 13:31:46 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1-alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:cccb94f4511ba8a1fd8ab69a69f483edef010e4fab16eeccfb637ae5395cdc67
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40930309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83c2e990bd9017e2a1f46423fc6e313b33122d383dda9f8f9c00e8006d36921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:10:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 01:53:04 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 01:53:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 19 Jul 2022 01:53:06 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 09:50:39 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 10:05:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 10:05:10 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 10:05:11 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 10:05:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 10:05:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 10:05:14 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 10:05:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 10:05:22 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 10:40:42 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 10:40:43 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 10:41:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 10:41:33 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 10:41:34 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 10:41:36 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 10:41:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 10:41:37 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 10:41:38 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 10:41:39 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c36086fc9356a3d9879c8427af90dd86ad6fd35b3929bab2af384e98d0571c`  
		Last Modified: Tue, 19 Jul 2022 02:56:56 GMT  
		Size: 668.0 KB (668022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255e9c7248a65c9bb1f14e3ffaf6aad2e14b965bfd9196b30e8c1efc8ddd1747`  
		Last Modified: Wed, 03 Aug 2022 10:34:00 GMT  
		Size: 12.6 MB (12579036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d32815e9cd0f789447579f484cec5ed6ff5b006c50c121a5e314519ffad01d5`  
		Last Modified: Wed, 03 Aug 2022 10:33:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c6e4018f23818adb74c050daeddb28d2efddbabe1135f85ed3ef29b17ec7b`  
		Last Modified: Wed, 03 Aug 2022 10:32:56 GMT  
		Size: 3.0 MB (3045000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2feaf81b71b2f7b13ac6cefc0f434f31221423c1c94002a89138b4c60741ced`  
		Last Modified: Wed, 03 Aug 2022 10:42:41 GMT  
		Size: 8.2 MB (8224897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c9e9ae46115c582ac3a68bb4b583d2ed73875acfb5ff520c5877d481be9cdc`  
		Last Modified: Wed, 03 Aug 2022 10:42:42 GMT  
		Size: 13.7 MB (13706894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e959a5cfce7f6c07db205394594178b791ab1fd7b3425ded77627110666277`  
		Last Modified: Wed, 03 Aug 2022 10:42:40 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143d97f09a0b08aff0f4993e07d50c6a62b1d1c84b442a35f1c8b7f9535005f4`  
		Last Modified: Wed, 03 Aug 2022 10:42:40 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1-alpine` - linux; 386

```console
$ docker pull satosa@sha256:3b7052fea622f5d95da31220bc234a9258ae473482fb55269dea295fd83b4e05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (173023892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712f8d15ddeef960a7327c512f8d03f337021df170d7531f5aa93eafbe51d2c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 21:22:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 21:22:15 GMT
ENV LANG=C.UTF-8
# Tue, 09 Aug 2022 21:22:17 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 09 Aug 2022 21:22:18 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 09 Aug 2022 22:02:59 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 09 Aug 2022 22:16:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 09 Aug 2022 22:16:19 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 09 Aug 2022 22:16:20 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 09 Aug 2022 22:16:21 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 09 Aug 2022 22:16:22 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 09 Aug 2022 22:16:23 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 09 Aug 2022 22:16:31 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 09 Aug 2022 22:16:31 GMT
CMD ["python3"]
# Wed, 10 Aug 2022 03:30:07 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 10 Aug 2022 03:30:08 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 10 Aug 2022 03:33:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 10 Aug 2022 03:33:03 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 10 Aug 2022 03:33:04 GMT
WORKDIR /etc/satosa
# Wed, 10 Aug 2022 03:33:06 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 10 Aug 2022 03:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 03:33:07 GMT
EXPOSE 8080
# Wed, 10 Aug 2022 03:33:08 GMT
USER satosa:satosa
# Wed, 10 Aug 2022 03:33:09 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6e4c463b4b085b81ccd90e5d99d5d5b64a56c2f756e7ff5575080b0efc2e9f`  
		Last Modified: Tue, 09 Aug 2022 23:12:22 GMT  
		Size: 689.1 KB (689070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30e501e19288fafd4b62af6aaf0b588b8da1b9f7bf0ed0bd8c7cf5550131f4b`  
		Last Modified: Tue, 09 Aug 2022 23:13:12 GMT  
		Size: 12.7 MB (12700838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5383c9c382f8845fcf42a8ea747ddb3a99c87e277380a509277f27c6bf8d85`  
		Last Modified: Tue, 09 Aug 2022 23:13:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2450ac53e437f841f48f00e832466a3d7ce73190f3f5255c89dfb89edcd9193`  
		Last Modified: Tue, 09 Aug 2022 23:13:11 GMT  
		Size: 3.0 MB (3045003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3183acab5e336c62f2d06a000d65364d4484e755eb4c01749dd6e443ee703e32`  
		Last Modified: Wed, 10 Aug 2022 03:34:01 GMT  
		Size: 8.5 MB (8512861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350ea1863d968db10b0fe1fd8772d772c84631136d5fb13934b7c5a360cf66fc`  
		Last Modified: Wed, 10 Aug 2022 03:34:28 GMT  
		Size: 145.3 MB (145257262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92895882e21832e6f4d040fa6f60752d36b168dbc7f3893d1fc81a19da18cfc3`  
		Last Modified: Wed, 10 Aug 2022 03:33:59 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85df40b1b491557b15d24c816c82279561fd23244d53603eeea4f9976ce8766`  
		Last Modified: Wed, 10 Aug 2022 03:33:59 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1-alpine` - linux; ppc64le

```console
$ docker pull satosa@sha256:f70b3121c8db732d980c4272ea937145d0745875aba33578b5667bbaf28fb1ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164310759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef00aeaa317867dd9dca82b0661794be10c5d0a082d11a8f76b597b76e88cb55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:29:30 GMT
ADD file:69e4080f15f54e2d8f8aa25fdcba9c01dde149d43592edd5023106675e54a769 in / 
# Mon, 18 Jul 2022 21:29:31 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 04:30:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 04:30:31 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 04:30:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 04:30:33 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 19:40:20 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 20:04:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 20:05:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 20:05:00 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 20:05:00 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 20:05:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 20:05:01 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 20:05:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 20:05:13 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 21:15:12 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 21:15:12 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 21:21:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 21:21:41 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 21:21:41 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 21:21:42 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 21:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 21:21:42 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 21:21:43 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 21:21:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:602896d442490cd3fbb6599f0f862d3673b7cd58eca3ac842b8e09bf8d012443`  
		Last Modified: Mon, 18 Jul 2022 19:09:09 GMT  
		Size: 2.8 MB (2789923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6556a4bf6509d5fd24900f56a6175bd811b9dd8c6f4f51e2732b6888a2b8933`  
		Last Modified: Wed, 27 Jul 2022 13:49:16 GMT  
		Size: 677.0 KB (676971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c735731e55a5ddb324dd5eb175e1f3d88895a77ea93b8fb08428ee522445708b`  
		Last Modified: Wed, 03 Aug 2022 20:44:16 GMT  
		Size: 12.8 MB (12819587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e525d9b2b00fc7130f21f05f981c44d849b279417c15b38703c3f11d3c9bd667`  
		Last Modified: Wed, 03 Aug 2022 20:44:13 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9bc880d40f528e2c6046dd7bad61fc78f27a3fbebe3f45d1348a72ace67d9b`  
		Last Modified: Wed, 03 Aug 2022 20:44:15 GMT  
		Size: 3.0 MB (3043656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b74e25b6a705707a07e0411366545458ad05f07844bde5b7bebddd988e69068`  
		Last Modified: Wed, 03 Aug 2022 21:23:08 GMT  
		Size: 8.5 MB (8476895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141bd7d880682fd816129f41549c798cabb9e94494f7ee7714d6e83e63606b82`  
		Last Modified: Wed, 03 Aug 2022 21:23:23 GMT  
		Size: 136.5 MB (136491944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b412f1d24946cb1e7f3d66a4ae5595d3b71ae6040af529dc49507cb1dd4e06c`  
		Last Modified: Wed, 03 Aug 2022 21:23:06 GMT  
		Size: 9.4 KB (9434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8aa237953d155695df1943bb27b03cf1cc3f1716ea63b1cf5a8b12d97cd6cea`  
		Last Modified: Wed, 03 Aug 2022 21:23:06 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.1-alpine3.16`

```console
$ docker pull satosa@sha256:fa00b0ab420886685085b244405746ecce141ff81c408876a6d8c17f5e0960ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `satosa:8.1-alpine3.16` - linux; amd64

```console
$ docker pull satosa@sha256:889e8b702bc04ca43d059bdf24c8db677954c87e5318ba8a93d795e450d485dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42508179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa3cc16430e95981e37a39687b5b6a8e23b8adf5eb81881cab4136b31de9b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:14:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 02:01:52 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 02:01:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 19 Jul 2022 02:01:54 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 10:48:21 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 11:00:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 11:00:14 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 11:00:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 11:00:21 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 11:47:34 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 11:47:34 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 11:48:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 11:48:18 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 11:48:19 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 11:48:19 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 11:48:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 11:48:19 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 11:48:19 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 11:48:19 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c14b1a767335de44f2bc926cb52487979a0fe602ac5429643dbb238f297fb`  
		Last Modified: Tue, 19 Jul 2022 02:56:13 GMT  
		Size: 666.8 KB (666769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571274b8543b548747b5e9bef700a89692fe9403cc364be8d6e8a0792ccfe2b4`  
		Last Modified: Wed, 03 Aug 2022 11:19:35 GMT  
		Size: 12.5 MB (12508608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f79a08255af5d614c7b4b81e358b5bb607bdcb14a6475c836d3d4f92f094846`  
		Last Modified: Wed, 03 Aug 2022 11:19:34 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6b20e3f6abd46292c29437a6917dc82b769ebb239e2d971aedb6695e057715`  
		Last Modified: Wed, 03 Aug 2022 11:19:34 GMT  
		Size: 3.0 MB (3043671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c974d4972d870a99bf0fba525cab86b298dd6e9405d3329a3495a164ae5c7`  
		Last Modified: Wed, 03 Aug 2022 11:49:00 GMT  
		Size: 9.4 MB (9398243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c482d554455c83821852ea2cd26eaf97f49bb1c7983342cec7242b8ea5432234`  
		Last Modified: Wed, 03 Aug 2022 11:49:01 GMT  
		Size: 14.1 MB (14080297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b861965b84abb04a92b63eb19a620daf7360785f485bc2d526885601454b19ca`  
		Last Modified: Wed, 03 Aug 2022 11:48:58 GMT  
		Size: 9.4 KB (9439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16e011f2d9efad78d03ac0d4c7abe2f694dfc5f6c158ef9fa350a3f21d22a8e`  
		Last Modified: Wed, 03 Aug 2022 11:48:58 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1-alpine3.16` - linux; arm variant v6

```console
$ docker pull satosa@sha256:1ed78492e93849ebbee5cd80dd5e4a91eb2a41676fbc3d21584a17d402028ca7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160179359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e822b6bb9258ee22b55f2f03c3d389710a39d0a3fa1d10f1250cb00db2f3e268`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 19:49:37 GMT
ADD file:7a20333469e71664904a0cb8f61613250f2bd092b4a27bfa7bbae1dc7e21b7ed in / 
# Mon, 18 Jul 2022 19:49:37 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 00:30:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 00:30:05 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 00:30:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 00:30:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 19:50:04 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 20:30:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 02 Aug 2022 20:30:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 20:30:20 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 20:30:20 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 03:20:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 03:20:45 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 03:27:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 03:27:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 03:27:54 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 03:27:54 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 03:27:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 03:27:55 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 03:27:55 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 03:27:55 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b7885075fcd06a866d12dfd56eb704045eaadbd22dc03a224cd98715be566677`  
		Last Modified: Mon, 18 Jul 2022 19:08:42 GMT  
		Size: 2.6 MB (2606431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ebe8e3a2f83d0ddc301c9b9d6405376eecb906b92082e05d5e257eff5f6293`  
		Last Modified: Wed, 27 Jul 2022 11:08:23 GMT  
		Size: 672.3 KB (672287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b647934af90a736595f675559fd3aebbcdbcfc67277de68401980916f3c217d7`  
		Last Modified: Wed, 03 Aug 2022 00:13:17 GMT  
		Size: 12.1 MB (12085055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaef313095ff837d4848dec2c5e458a33e59ee4e1ab7a9d4e3d244d20b92fbf`  
		Last Modified: Wed, 03 Aug 2022 00:13:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba453d098c35b58faf7cc2ac6a90a0e9a8941dc90611ee397d12af0a546bbe87`  
		Last Modified: Wed, 03 Aug 2022 00:13:15 GMT  
		Size: 3.0 MB (3043708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0a90158473abc47e6b9744b5cc61265a9552ba9217486241f5b7b4a5d12eec`  
		Last Modified: Wed, 03 Aug 2022 03:28:44 GMT  
		Size: 8.3 MB (8280231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a82dd9e01f89340501ac0415caccc1ad608cc08d55219cb26db2226dc64b83`  
		Last Modified: Wed, 03 Aug 2022 03:29:07 GMT  
		Size: 133.5 MB (133479861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ee2ba314aef7361329abd7eaa7a8860079655317f4d5fc9d37f73f8b34de4`  
		Last Modified: Wed, 03 Aug 2022 03:28:39 GMT  
		Size: 9.4 KB (9438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24649d01bd9f34f035857fcb9324aef45128d255b0e7d7c9be9d0d9d58a928f3`  
		Last Modified: Wed, 03 Aug 2022 03:28:39 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1-alpine3.16` - linux; arm variant v7

```console
$ docker pull satosa@sha256:9c12b392cb5946a433fe0c98001d362d79a953040068a9d0843c3a9a9c12fb8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163401667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55a50fb783bb28da31c92c6cff33c408ef6ea7e1c6da179086af8ce588f092d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:24:47 GMT
ADD file:68590e866bc6db27ad54d23de7dd275d0389cb86e4e6291a1243fcc234f2f7a1 in / 
# Mon, 18 Jul 2022 21:24:47 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 03:57:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 03:57:44 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 03:57:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 03:57:46 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 07:37:59 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 08:07:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 08:07:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 08:07:50 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 08:07:51 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 13:27:03 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 13:27:03 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 13:30:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 13:30:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 13:30:25 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 13:30:25 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 13:30:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 13:30:25 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 13:30:25 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 13:30:25 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a6b45ace95f42a930d15c33679ab9c85d46019b7e73954cadc73bb9ba176509b`  
		Last Modified: Mon, 18 Jul 2022 19:08:56 GMT  
		Size: 2.4 MB (2412307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d826ef3e3e077607452c51ac5332613cc0a20903abe17b56af4b973f31f0e9b7`  
		Last Modified: Wed, 27 Jul 2022 10:54:47 GMT  
		Size: 664.1 KB (664079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116f12212b7e97cde5b72713f0f3a3025a9ef6dffccdc353cd4d15407d343a72`  
		Last Modified: Wed, 03 Aug 2022 11:22:41 GMT  
		Size: 11.6 MB (11558755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef2affe775c9998dea9fd354aa8d4b6e97117d2092c84f1401265b9f9528bf7`  
		Last Modified: Wed, 03 Aug 2022 11:22:38 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032af4833525c8884057f85c0da98a7f2dedc337784e4ce3645fad79e6633b26`  
		Last Modified: Wed, 03 Aug 2022 11:22:39 GMT  
		Size: 3.0 MB (3043658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65c3d7d841a308ff58960bdd0832a9c2fc9d01d091b4478549cf91ad4551edc`  
		Last Modified: Thu, 04 Aug 2022 13:31:47 GMT  
		Size: 8.0 MB (8026973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553863577a06e5d191ae29abc79bb81603188e34e406ebce36a4e4da49320df8`  
		Last Modified: Thu, 04 Aug 2022 13:31:59 GMT  
		Size: 137.7 MB (137684108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d66d75890a5436b91b581c5023634cbedf248e1dbb622b1241f80c5a4ed29`  
		Last Modified: Thu, 04 Aug 2022 13:31:45 GMT  
		Size: 9.4 KB (9439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cab52b5f6577ce2ac31dd72be231ca9d43531003be80eacfe2f20bbfa5c5d5`  
		Last Modified: Thu, 04 Aug 2022 13:31:46 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:cccb94f4511ba8a1fd8ab69a69f483edef010e4fab16eeccfb637ae5395cdc67
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40930309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83c2e990bd9017e2a1f46423fc6e313b33122d383dda9f8f9c00e8006d36921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:10:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 01:53:04 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 01:53:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 19 Jul 2022 01:53:06 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 09:50:39 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 10:05:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 10:05:10 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 10:05:11 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 10:05:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 10:05:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 10:05:14 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 10:05:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 10:05:22 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 10:40:42 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 10:40:43 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 10:41:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 10:41:33 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 10:41:34 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 10:41:36 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 10:41:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 10:41:37 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 10:41:38 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 10:41:39 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c36086fc9356a3d9879c8427af90dd86ad6fd35b3929bab2af384e98d0571c`  
		Last Modified: Tue, 19 Jul 2022 02:56:56 GMT  
		Size: 668.0 KB (668022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255e9c7248a65c9bb1f14e3ffaf6aad2e14b965bfd9196b30e8c1efc8ddd1747`  
		Last Modified: Wed, 03 Aug 2022 10:34:00 GMT  
		Size: 12.6 MB (12579036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d32815e9cd0f789447579f484cec5ed6ff5b006c50c121a5e314519ffad01d5`  
		Last Modified: Wed, 03 Aug 2022 10:33:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c6e4018f23818adb74c050daeddb28d2efddbabe1135f85ed3ef29b17ec7b`  
		Last Modified: Wed, 03 Aug 2022 10:32:56 GMT  
		Size: 3.0 MB (3045000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2feaf81b71b2f7b13ac6cefc0f434f31221423c1c94002a89138b4c60741ced`  
		Last Modified: Wed, 03 Aug 2022 10:42:41 GMT  
		Size: 8.2 MB (8224897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c9e9ae46115c582ac3a68bb4b583d2ed73875acfb5ff520c5877d481be9cdc`  
		Last Modified: Wed, 03 Aug 2022 10:42:42 GMT  
		Size: 13.7 MB (13706894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e959a5cfce7f6c07db205394594178b791ab1fd7b3425ded77627110666277`  
		Last Modified: Wed, 03 Aug 2022 10:42:40 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143d97f09a0b08aff0f4993e07d50c6a62b1d1c84b442a35f1c8b7f9535005f4`  
		Last Modified: Wed, 03 Aug 2022 10:42:40 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1-alpine3.16` - linux; 386

```console
$ docker pull satosa@sha256:3b7052fea622f5d95da31220bc234a9258ae473482fb55269dea295fd83b4e05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (173023892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712f8d15ddeef960a7327c512f8d03f337021df170d7531f5aa93eafbe51d2c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 21:22:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 21:22:15 GMT
ENV LANG=C.UTF-8
# Tue, 09 Aug 2022 21:22:17 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 09 Aug 2022 21:22:18 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 09 Aug 2022 22:02:59 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 09 Aug 2022 22:16:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 09 Aug 2022 22:16:19 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 09 Aug 2022 22:16:20 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 09 Aug 2022 22:16:21 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 09 Aug 2022 22:16:22 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 09 Aug 2022 22:16:23 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 09 Aug 2022 22:16:31 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 09 Aug 2022 22:16:31 GMT
CMD ["python3"]
# Wed, 10 Aug 2022 03:30:07 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 10 Aug 2022 03:30:08 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 10 Aug 2022 03:33:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 10 Aug 2022 03:33:03 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 10 Aug 2022 03:33:04 GMT
WORKDIR /etc/satosa
# Wed, 10 Aug 2022 03:33:06 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 10 Aug 2022 03:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 03:33:07 GMT
EXPOSE 8080
# Wed, 10 Aug 2022 03:33:08 GMT
USER satosa:satosa
# Wed, 10 Aug 2022 03:33:09 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6e4c463b4b085b81ccd90e5d99d5d5b64a56c2f756e7ff5575080b0efc2e9f`  
		Last Modified: Tue, 09 Aug 2022 23:12:22 GMT  
		Size: 689.1 KB (689070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30e501e19288fafd4b62af6aaf0b588b8da1b9f7bf0ed0bd8c7cf5550131f4b`  
		Last Modified: Tue, 09 Aug 2022 23:13:12 GMT  
		Size: 12.7 MB (12700838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5383c9c382f8845fcf42a8ea747ddb3a99c87e277380a509277f27c6bf8d85`  
		Last Modified: Tue, 09 Aug 2022 23:13:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2450ac53e437f841f48f00e832466a3d7ce73190f3f5255c89dfb89edcd9193`  
		Last Modified: Tue, 09 Aug 2022 23:13:11 GMT  
		Size: 3.0 MB (3045003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3183acab5e336c62f2d06a000d65364d4484e755eb4c01749dd6e443ee703e32`  
		Last Modified: Wed, 10 Aug 2022 03:34:01 GMT  
		Size: 8.5 MB (8512861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350ea1863d968db10b0fe1fd8772d772c84631136d5fb13934b7c5a360cf66fc`  
		Last Modified: Wed, 10 Aug 2022 03:34:28 GMT  
		Size: 145.3 MB (145257262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92895882e21832e6f4d040fa6f60752d36b168dbc7f3893d1fc81a19da18cfc3`  
		Last Modified: Wed, 10 Aug 2022 03:33:59 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85df40b1b491557b15d24c816c82279561fd23244d53603eeea4f9976ce8766`  
		Last Modified: Wed, 10 Aug 2022 03:33:59 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1-alpine3.16` - linux; ppc64le

```console
$ docker pull satosa@sha256:f70b3121c8db732d980c4272ea937145d0745875aba33578b5667bbaf28fb1ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164310759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef00aeaa317867dd9dca82b0661794be10c5d0a082d11a8f76b597b76e88cb55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:29:30 GMT
ADD file:69e4080f15f54e2d8f8aa25fdcba9c01dde149d43592edd5023106675e54a769 in / 
# Mon, 18 Jul 2022 21:29:31 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 04:30:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 04:30:31 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 04:30:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 04:30:33 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 19:40:20 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 20:04:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 20:05:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 20:05:00 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 20:05:00 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 20:05:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 20:05:01 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 20:05:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 20:05:13 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 21:15:12 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 21:15:12 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 21:21:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 21:21:41 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 21:21:41 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 21:21:42 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 21:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 21:21:42 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 21:21:43 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 21:21:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:602896d442490cd3fbb6599f0f862d3673b7cd58eca3ac842b8e09bf8d012443`  
		Last Modified: Mon, 18 Jul 2022 19:09:09 GMT  
		Size: 2.8 MB (2789923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6556a4bf6509d5fd24900f56a6175bd811b9dd8c6f4f51e2732b6888a2b8933`  
		Last Modified: Wed, 27 Jul 2022 13:49:16 GMT  
		Size: 677.0 KB (676971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c735731e55a5ddb324dd5eb175e1f3d88895a77ea93b8fb08428ee522445708b`  
		Last Modified: Wed, 03 Aug 2022 20:44:16 GMT  
		Size: 12.8 MB (12819587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e525d9b2b00fc7130f21f05f981c44d849b279417c15b38703c3f11d3c9bd667`  
		Last Modified: Wed, 03 Aug 2022 20:44:13 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9bc880d40f528e2c6046dd7bad61fc78f27a3fbebe3f45d1348a72ace67d9b`  
		Last Modified: Wed, 03 Aug 2022 20:44:15 GMT  
		Size: 3.0 MB (3043656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b74e25b6a705707a07e0411366545458ad05f07844bde5b7bebddd988e69068`  
		Last Modified: Wed, 03 Aug 2022 21:23:08 GMT  
		Size: 8.5 MB (8476895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141bd7d880682fd816129f41549c798cabb9e94494f7ee7714d6e83e63606b82`  
		Last Modified: Wed, 03 Aug 2022 21:23:23 GMT  
		Size: 136.5 MB (136491944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b412f1d24946cb1e7f3d66a4ae5595d3b71ae6040af529dc49507cb1dd4e06c`  
		Last Modified: Wed, 03 Aug 2022 21:23:06 GMT  
		Size: 9.4 KB (9434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8aa237953d155695df1943bb27b03cf1cc3f1716ea63b1cf5a8b12d97cd6cea`  
		Last Modified: Wed, 03 Aug 2022 21:23:06 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.1-bullseye`

```console
$ docker pull satosa@sha256:b952f0d280486a79665537c956718dec4fff75e9e6a343a79e1048bc3bf3c861
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

### `satosa:8.1-bullseye` - linux; amd64

```console
$ docker pull satosa@sha256:3d92574bf94e0395a41762efa378d221f605ea12bea73ae604c71310fe6036fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82653895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d245b28169a1e1f7dd888fa2381fc3aa02a91b2210f7b6b481c4016173ac8d0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 09:39:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 09:39:09 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 09:39:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 09:39:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 10:15:41 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 10:26:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 10:26:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 10:26:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 10:26:31 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 11:46:24 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 11:46:24 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 11:47:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 11:47:19 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 11:47:19 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 11:47:19 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 11:47:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 11:47:20 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 11:47:20 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 11:47:20 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126aaa6587b8608b62fa39019a891e98460e23bad2d04fb235c4dc8fae2adf3c`  
		Last Modified: Tue, 02 Aug 2022 12:33:29 GMT  
		Size: 1.1 MB (1076278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd06b55ca686f29b26c8a7e051ce98ad571fd6cf22bba07f5cd17e98fd31e13`  
		Last Modified: Wed, 03 Aug 2022 11:18:36 GMT  
		Size: 12.1 MB (12106838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3950cece0b727ab257c49317871d00f22d2abcb77bcce19ddf86aab5c4d88e21`  
		Last Modified: Wed, 03 Aug 2022 11:18:34 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e27c1167cc2a09e30e53c0fd2933e189e20b4785284e84a919fe5fd3013388b`  
		Last Modified: Wed, 03 Aug 2022 11:18:35 GMT  
		Size: 3.3 MB (3336043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb69b4e4539d59ea0fbed39563b5042d023cd4713d9a38bde6b930fb548e8b9a`  
		Last Modified: Wed, 03 Aug 2022 11:48:44 GMT  
		Size: 19.6 MB (19587061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620aa9bb44333fe5af9257a47e9e0de0e7a0596721959465531442e2b753aa5a`  
		Last Modified: Wed, 03 Aug 2022 11:48:44 GMT  
		Size: 15.2 MB (15169129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffc5c41689ca0d4f9b9e1beea0953f2bec48e3ab6becfee1b8c8862100aadbe`  
		Last Modified: Wed, 03 Aug 2022 11:48:41 GMT  
		Size: 9.4 KB (9443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebafed1e50948cce1a8ec458a2dbc933ec93924419791a83613e224356054ee`  
		Last Modified: Wed, 03 Aug 2022 11:48:41 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1-bullseye` - linux; arm variant v5

```console
$ docker pull satosa@sha256:e4ee7d4d43b26f8dc6b5a7d8358af5463aa5ebf830249e6272afbe2a819e9732
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.7 MB (203698783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160cc52ce9b78d794b4acbd3286cc62c771bad645eb50e8c9af6722d743f166c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:10 GMT
ADD file:4cd2f95737fd3007912428eeac56036c9e67e989e66cec08a8be99da47f88494 in / 
# Tue, 02 Aug 2022 00:49:10 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:38:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 20:38:12 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 20:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:38:23 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 22:45:24 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 23:08:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 23:08:11 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 23:08:11 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 23:08:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 23:08:30 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 19:10:52 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 19:10:52 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 19:17:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 19:17:42 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 19:17:42 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 19:17:43 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 19:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 19:17:43 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 19:17:43 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 19:17:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5890b0ca6af5e8467a488e68716691950496a8f247d0495c2d595ddcb1893aff`  
		Last Modified: Tue, 02 Aug 2022 00:56:06 GMT  
		Size: 28.9 MB (28905515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eafe902d3c868e979e01e5c5aca6567b8be8b60814b9e1ce93c2b749451b410`  
		Last Modified: Wed, 03 Aug 2022 02:16:47 GMT  
		Size: 1.1 MB (1059641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e073b0922c53e3aee167b94b195f01b7740c95a691b391e30bbc1dd36133f578`  
		Last Modified: Wed, 03 Aug 2022 02:18:15 GMT  
		Size: 11.7 MB (11687058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1563deb88ac81fbc07f66164de09058989bc2f52e4b201209996fc610e7424`  
		Last Modified: Wed, 03 Aug 2022 02:18:11 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9586a9ae76d2fcf29975a3cbac30868417a5e7209b4d681ab4d8cdc9417e1127`  
		Last Modified: Wed, 03 Aug 2022 02:18:13 GMT  
		Size: 3.3 MB (3335517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2138d4d7c7c422781a7da5bbba917dfee3de2e44c0b89e2c05cd5fb54d6aec`  
		Last Modified: Wed, 03 Aug 2022 19:18:28 GMT  
		Size: 21.2 MB (21220513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ec77684813e78ff3c43e62e86fde2b1964089fb2e02c36be1b197e18d76199`  
		Last Modified: Wed, 03 Aug 2022 19:18:38 GMT  
		Size: 137.5 MB (137478750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecfeff163b4d6f23860d774bf123b6ad13105fce4fa35bddd9e46a56b0c09af`  
		Last Modified: Wed, 03 Aug 2022 19:18:21 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb3f6f2ab2014dd8287001b208c1dc97200c2c3e16a2cb980fd938dfd82858b`  
		Last Modified: Wed, 03 Aug 2022 19:18:22 GMT  
		Size: 2.1 KB (2111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1-bullseye` - linux; arm variant v7

```console
$ docker pull satosa@sha256:1eb7ef57547ada8079868ad16a792df4e4cbc8571c4b2beb50d5682d1bc6250f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202351243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194a9b56fc0cc44a0542e47df53c65db1e4f7a579b5a8624e2b202e21462c73d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:58:59 GMT
ADD file:1575b776a15adacebc0875642e97a80807d42dcfc8917e1406d47af7ac244c97 in / 
# Tue, 02 Aug 2022 00:58:59 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:34:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 04:34:22 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 04:34:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 04:34:30 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 06:30:14 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 06:52:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 06:52:09 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 06:52:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 06:52:24 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 13:20:49 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 13:20:50 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 13:26:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 13:26:45 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 13:26:45 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 13:26:45 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 13:26:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 13:26:45 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 13:26:45 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 13:26:45 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1dd75a3a9c893a7dc313f683dd62464b7eab6c6d522ee62c8a17022631830f32`  
		Last Modified: Tue, 02 Aug 2022 01:06:45 GMT  
		Size: 26.6 MB (26560586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4206fea8c3d0ae09213fad25e06bb550a03c76c2b15e7a3c134ee5e2d217cd`  
		Last Modified: Wed, 03 Aug 2022 11:19:22 GMT  
		Size: 1.0 MB (1041632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed9dda465ec974f3e81b6b5f48dee0c43b63aeae625042e1e5f8ca482d43f1f`  
		Last Modified: Wed, 03 Aug 2022 11:21:19 GMT  
		Size: 11.2 MB (11205345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c669588520ce26d52819574b6ac8f40bc121ec539aae49c4cdc6aa899fcea`  
		Last Modified: Wed, 03 Aug 2022 11:21:15 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75c71e6575f11c76771634448c2e1c7e6988853591c1422d979aaf3dfa73569`  
		Last Modified: Wed, 03 Aug 2022 11:21:17 GMT  
		Size: 3.3 MB (3335656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d5ac04f9c39c2ba1d884f419e586ede32f2779ea0bbb6a7033e0f70c79d670`  
		Last Modified: Thu, 04 Aug 2022 13:31:15 GMT  
		Size: 20.9 MB (20949533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65844885dbff2fac2bccf9e5a7b69d9c423352d19d5ffb5eeca720f5e2a10886`  
		Last Modified: Thu, 04 Aug 2022 13:31:26 GMT  
		Size: 139.2 MB (139246702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53ebddc2eb90a987a1bae1b3a245f2d88ae7ea81a35f85f6bfdf10891217d58`  
		Last Modified: Thu, 04 Aug 2022 13:31:10 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa39e50e9a3812f026202131476b98a06e4a65a16a21fee180aeb54d979e2cb8`  
		Last Modified: Thu, 04 Aug 2022 13:31:10 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1-bullseye` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:8a7bc186f7c0a8725b284d01a4dceac8636d5f7f96b11f0d4031fd66f199e2b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79849083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56454aaf2924873a1f55890e93e1c83261d4047ce84a080d73750691435b3d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:03:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 12:03:30 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 12:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:03:36 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 09:19:10 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 09:29:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 09:29:22 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 09:29:22 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 09:29:23 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 09:29:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 09:29:25 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 09:29:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 09:29:37 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 10:39:28 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 10:39:28 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 10:40:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 10:40:15 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 10:40:16 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 10:40:18 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 10:40:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 10:40:19 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 10:40:20 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 10:40:21 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f101f90cc8f7640b7db5f7094941a1fe4ff28e11a968d3a36f146a89a480ecbb`  
		Last Modified: Tue, 02 Aug 2022 14:47:06 GMT  
		Size: 1.1 MB (1063812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a5d6cf27653f158e4f7552f31dc146332b6d820679ee42ebff5b4e47f4dac`  
		Last Modified: Wed, 03 Aug 2022 10:31:15 GMT  
		Size: 12.2 MB (12153733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd415bdc2c72c852623e384c90826d41aa2739adbc3158bd814bc3e562ab16ea`  
		Last Modified: Wed, 03 Aug 2022 10:31:13 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90ceb316b2d011719d35fb58a5d69ec1b84ebc6a9ab5568354ca370aad48524`  
		Last Modified: Wed, 03 Aug 2022 10:31:14 GMT  
		Size: 3.1 MB (3119919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7a23c6e6d4ea56699e3033f9fd616c6fa79290a257066f21578bf773f283cb`  
		Last Modified: Wed, 03 Aug 2022 10:42:23 GMT  
		Size: 19.3 MB (19324710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f64adba6c540f9f4fde33df9a99fa32be543c937e20b203b409ba3340f7b62`  
		Last Modified: Wed, 03 Aug 2022 10:42:23 GMT  
		Size: 14.1 MB (14120866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9df97e7203d91c6109257b6e98c0bb926732214ee96a7110c86550f8c271b74`  
		Last Modified: Wed, 03 Aug 2022 10:42:20 GMT  
		Size: 9.4 KB (9394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d56269ee4307b5c76ba7efef9346008e1440979b95ee777b9d5e8e3e4ead5b1`  
		Last Modified: Wed, 03 Aug 2022 10:42:20 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1-bullseye` - linux; 386

```console
$ docker pull satosa@sha256:ff2180ab006e1d173a6d157a2ef8b05c4abae7d45d5693889e12f05e6861a42d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207396057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b9632c4df58a4c5e3e68e82bf8bab7462b2530f9ecfb108feb8726a85ab4d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:39:20 GMT
ADD file:f771e2286465694126158821089d801c7296376be2a56189e6041a15d2fe79f5 in / 
# Tue, 02 Aug 2022 00:39:21 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 11:22:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 11:22:53 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 11:22:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 11:22:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 20:51:53 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 21:03:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 21:03:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 21:03:55 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 21:03:56 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 21:03:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 21:03:58 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 21:04:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 21:04:12 GMT
CMD ["python3"]
# Tue, 02 Aug 2022 22:21:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 02 Aug 2022 22:21:44 GMT
ENV SATOSA_VERSION=8.1.1
# Tue, 02 Aug 2022 23:39:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 02 Aug 2022 23:39:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 02 Aug 2022 23:39:26 GMT
WORKDIR /etc/satosa
# Tue, 02 Aug 2022 23:39:28 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Tue, 02 Aug 2022 23:39:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 23:39:29 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 23:39:30 GMT
USER satosa:satosa
# Tue, 02 Aug 2022 23:39:31 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:90eb7f0ce9f33cf5dcd67d54c2fa606186dbaa5f95b6046f36145097267f9e53`  
		Last Modified: Tue, 02 Aug 2022 00:45:14 GMT  
		Size: 32.4 MB (32374054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd27ead98f25cd891e8dfae23b5500c856f3a9db336a545eed8b5f180a6df0b4`  
		Last Modified: Tue, 02 Aug 2022 14:37:54 GMT  
		Size: 1.1 MB (1088442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7362ecffe5fefdfcff89188358cb648fae40c1fed6254cd3325ef1c340a0ca9b`  
		Last Modified: Tue, 02 Aug 2022 22:15:01 GMT  
		Size: 12.2 MB (12224818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fb82e70fda9a811619f0b6cfd165d59473bcc467e702a70231630e64335b18`  
		Last Modified: Tue, 02 Aug 2022 22:14:59 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab067ab28a29ee91955ebd00b4849cd1d1993a430051ce801b5eaffeeb59b976`  
		Last Modified: Tue, 02 Aug 2022 22:15:00 GMT  
		Size: 3.1 MB (3119814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c68c7fda4b282e37efe94863aed2872d62133ead0fed4a4b4174eab16a125f`  
		Last Modified: Tue, 02 Aug 2022 23:40:27 GMT  
		Size: 22.6 MB (22586591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4630af60cc9f0637de40da0789c8be2b49091d860ae7f21753e736c5a24b0fac`  
		Last Modified: Tue, 02 Aug 2022 23:40:44 GMT  
		Size: 136.0 MB (135990599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ba92ddedaf8e60d74aac7773867aec0a84b2812ba92a5742090bee107e7736`  
		Last Modified: Tue, 02 Aug 2022 23:40:24 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e28ea4f42ac6baac91e14de0ee8d101956ac6d64c7d4078bb57ebfddde33184`  
		Last Modified: Tue, 02 Aug 2022 23:40:24 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1-bullseye` - linux; mips64le

```console
$ docker pull satosa@sha256:b9bdbc69a8a0be593fe150cbd4334f006447c17a9538b850002e7fa96445593b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.8 MB (205844024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7d3830a289e7a92a0277b60e6cce741d4887ea889e4e236cdd2d878fb1f64b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:10:34 GMT
ADD file:6dc22a1e5b5fcf23f2549406ddcc45c4e244f46e21eafa881de81fa87438e5d8 in / 
# Tue, 02 Aug 2022 01:10:38 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 10:25:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 10:25:08 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 10:25:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:25:36 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 04 Aug 2022 04:16:09 GMT
ENV PYTHON_VERSION=3.10.6
# Thu, 04 Aug 2022 05:33:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Thu, 04 Aug 2022 05:33:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 04 Aug 2022 05:33:27 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Thu, 04 Aug 2022 05:33:30 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Thu, 04 Aug 2022 05:33:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Thu, 04 Aug 2022 05:33:35 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Thu, 04 Aug 2022 05:34:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 04 Aug 2022 05:34:30 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 08:35:12 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 08:35:15 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 08:52:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 08:52:17 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 08:52:21 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 08:52:25 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 08:52:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 08:52:34 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 08:52:39 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 08:52:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:88350749a27614c791450c256b051f023d81cdd256211274b1efac493779d2be`  
		Last Modified: Tue, 02 Aug 2022 01:21:02 GMT  
		Size: 29.6 MB (29628964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61130d003a0ea87819935a3a252db1861d9b87e1313fa7988d5f0642637f3e`  
		Last Modified: Tue, 02 Aug 2022 23:46:40 GMT  
		Size: 1.0 MB (1049605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e786491697e5d2bd3dee622f7eae98810c04c895d5024e910e2394f92b37ad8`  
		Last Modified: Thu, 04 Aug 2022 08:14:51 GMT  
		Size: 12.1 MB (12124464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fb1366c066d6bf94df2bf081524439083c14a1f292da85f218000ac515a2f5`  
		Last Modified: Thu, 04 Aug 2022 08:14:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe7637d1173b353af8622199dfbc92d0f74f8cff129fe540541b9c069a058d3`  
		Last Modified: Thu, 04 Aug 2022 08:14:46 GMT  
		Size: 3.1 MB (3120804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4655831cce551d936028a78d3d4a295cd96e3ca02ea0f5f726d0b963350a0e`  
		Last Modified: Thu, 04 Aug 2022 08:53:18 GMT  
		Size: 21.3 MB (21288233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54965dd4effca16f75a92cdac5dd71e708a50d218ca30b0806964a58d8b726ee`  
		Last Modified: Thu, 04 Aug 2022 08:53:58 GMT  
		Size: 138.6 MB (138620211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a449c61594c6b3d2e0fa03d876ebe6fc8561eaa1d46ebf088772a42dea52b596`  
		Last Modified: Thu, 04 Aug 2022 08:53:06 GMT  
		Size: 9.4 KB (9396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54e620f3a05fe34c293ac1de03899ec567f49faa21a8db43216f796387f8f65`  
		Last Modified: Thu, 04 Aug 2022 08:53:06 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1-bullseye` - linux; ppc64le

```console
$ docker pull satosa@sha256:b84ad93ccca31f2ba03b7c0586ad9f3a2d71764d4338922af798ae737ec87f23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212244381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f29a99f45c08fb90c8ad9dec84fd55c14d0ca8ecbc00c2160fc3464a14feca9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:17:30 GMT
ADD file:3a95a896d463569ce82199957052b3467123a4bd3385a0a4e397cf08402a99c3 in / 
# Tue, 02 Aug 2022 01:17:32 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:03:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 16:03:13 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 16:03:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 16:03:24 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 18:10:29 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 18:43:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 18:43:03 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 18:43:03 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 18:43:03 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 18:43:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 18:43:04 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 18:43:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 18:43:25 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 21:09:20 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 21:09:21 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 21:14:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 21:14:39 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 21:14:39 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 21:14:40 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 21:14:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 21:14:41 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 21:14:41 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 21:14:42 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5241cd116d6e6e2d62f3d8c2245b74daca9f6cc154eaccd738feb41984c74714`  
		Last Modified: Tue, 02 Aug 2022 01:24:39 GMT  
		Size: 35.3 MB (35272771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf6dcfcb4fa2f4e24ce6bed8b3eda6b0d49d92062cb34d95830e4e9f512270`  
		Last Modified: Wed, 03 Aug 2022 00:14:29 GMT  
		Size: 1.1 MB (1094658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdc50327f93cca5ad2c5f8500471040045b715045a9a4852ece90b3155d5aea`  
		Last Modified: Wed, 03 Aug 2022 20:42:55 GMT  
		Size: 12.5 MB (12473465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49f3fdf44cc1cf9b0e2d32c8ea2b62a0d3eb7eac481b56c9d11e44c66b764fe`  
		Last Modified: Wed, 03 Aug 2022 20:42:52 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd9d6c8cb5530b56f02a736bb1cc24d2d0ffc11d6fb55dc6befb0e114a1ff74`  
		Last Modified: Wed, 03 Aug 2022 20:42:53 GMT  
		Size: 3.3 MB (3336216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209342dd334b280e74196c0e693487033f7f2d08880ab61f5f9113dbbd5d0461`  
		Last Modified: Wed, 03 Aug 2022 21:22:32 GMT  
		Size: 22.2 MB (22158681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11809242e6bd5adbd0096d37646b954f666a1e2a107dd5442773977caa919360`  
		Last Modified: Wed, 03 Aug 2022 21:22:45 GMT  
		Size: 137.9 MB (137896801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa36501b6a1d8ec2e51a6a162f1f43d70ea4b035335513b65b800346790717`  
		Last Modified: Wed, 03 Aug 2022 21:22:27 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fe38c0944e97231334e780f32f3cd041644756c5b195812b19edd697268021`  
		Last Modified: Wed, 03 Aug 2022 21:22:27 GMT  
		Size: 2.1 KB (2113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1-bullseye` - linux; s390x

```console
$ docker pull satosa@sha256:f52b8375aeb8b39ad8ae5b9f05f4f94a47f4776b3f500aeeadee19c4ed572f5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202163420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f253b8b35e8bbaf69f23beb8a8584dc48a0c682127faa17ed9d639b33dfdf3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 08:30:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 08:30:40 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 08:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 08:30:44 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 22:09:42 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 22:18:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 22:18:03 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 22:18:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 22:18:13 GMT
CMD ["python3"]
# Tue, 02 Aug 2022 23:28:28 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 02 Aug 2022 23:28:31 GMT
ENV SATOSA_VERSION=8.1.1
# Tue, 02 Aug 2022 23:32:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 02 Aug 2022 23:33:02 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 02 Aug 2022 23:33:02 GMT
WORKDIR /etc/satosa
# Tue, 02 Aug 2022 23:33:02 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Tue, 02 Aug 2022 23:33:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 23:33:02 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 23:33:03 GMT
USER satosa:satosa
# Tue, 02 Aug 2022 23:33:03 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c36d12a9d2aa3bd2ed5880b10e768bae6cab779992e198cf595d3b8d6924d5`  
		Last Modified: Tue, 02 Aug 2022 10:43:27 GMT  
		Size: 1.1 MB (1075771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a2fa2a5f3f4be291fac87451996292e32ad4b6b7e7ae168c720b6501ba676f`  
		Last Modified: Tue, 02 Aug 2022 23:23:49 GMT  
		Size: 11.9 MB (11900903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1958402e81da32fc50ee2b3d3d48a5714015a6589a9b0882e2e0862173874f52`  
		Last Modified: Tue, 02 Aug 2022 23:23:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adc16df778c23094a004c62669c6de553142901db4933d76959d223598473b`  
		Last Modified: Tue, 02 Aug 2022 23:23:49 GMT  
		Size: 3.3 MB (3335624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5f479e9444a18e7100a74300ba30ab5818c9023c386c0a537811de457f1e99`  
		Last Modified: Tue, 02 Aug 2022 23:33:39 GMT  
		Size: 19.6 MB (19580744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573792100821147cd9e469e566ed70175d1fe8ec2b68e371484abc92f0aeaf74`  
		Last Modified: Tue, 02 Aug 2022 23:33:45 GMT  
		Size: 136.6 MB (136618328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cb6a07895307e25b49bb3cdebc3f6e29fef231b0390c00ddacc6b74ee5f9fd`  
		Last Modified: Tue, 02 Aug 2022 23:33:36 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0ce3aebbe275e54928297909f6f1ed7c7beee5c901706ccef91eec96eb8bc5`  
		Last Modified: Tue, 02 Aug 2022 23:33:36 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.1.1`

```console
$ docker pull satosa@sha256:b952f0d280486a79665537c956718dec4fff75e9e6a343a79e1048bc3bf3c861
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

### `satosa:8.1.1` - linux; amd64

```console
$ docker pull satosa@sha256:3d92574bf94e0395a41762efa378d221f605ea12bea73ae604c71310fe6036fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82653895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d245b28169a1e1f7dd888fa2381fc3aa02a91b2210f7b6b481c4016173ac8d0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 09:39:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 09:39:09 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 09:39:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 09:39:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 10:15:41 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 10:26:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 10:26:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 10:26:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 10:26:31 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 11:46:24 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 11:46:24 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 11:47:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 11:47:19 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 11:47:19 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 11:47:19 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 11:47:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 11:47:20 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 11:47:20 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 11:47:20 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126aaa6587b8608b62fa39019a891e98460e23bad2d04fb235c4dc8fae2adf3c`  
		Last Modified: Tue, 02 Aug 2022 12:33:29 GMT  
		Size: 1.1 MB (1076278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd06b55ca686f29b26c8a7e051ce98ad571fd6cf22bba07f5cd17e98fd31e13`  
		Last Modified: Wed, 03 Aug 2022 11:18:36 GMT  
		Size: 12.1 MB (12106838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3950cece0b727ab257c49317871d00f22d2abcb77bcce19ddf86aab5c4d88e21`  
		Last Modified: Wed, 03 Aug 2022 11:18:34 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e27c1167cc2a09e30e53c0fd2933e189e20b4785284e84a919fe5fd3013388b`  
		Last Modified: Wed, 03 Aug 2022 11:18:35 GMT  
		Size: 3.3 MB (3336043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb69b4e4539d59ea0fbed39563b5042d023cd4713d9a38bde6b930fb548e8b9a`  
		Last Modified: Wed, 03 Aug 2022 11:48:44 GMT  
		Size: 19.6 MB (19587061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620aa9bb44333fe5af9257a47e9e0de0e7a0596721959465531442e2b753aa5a`  
		Last Modified: Wed, 03 Aug 2022 11:48:44 GMT  
		Size: 15.2 MB (15169129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffc5c41689ca0d4f9b9e1beea0953f2bec48e3ab6becfee1b8c8862100aadbe`  
		Last Modified: Wed, 03 Aug 2022 11:48:41 GMT  
		Size: 9.4 KB (9443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebafed1e50948cce1a8ec458a2dbc933ec93924419791a83613e224356054ee`  
		Last Modified: Wed, 03 Aug 2022 11:48:41 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1` - linux; arm variant v5

```console
$ docker pull satosa@sha256:e4ee7d4d43b26f8dc6b5a7d8358af5463aa5ebf830249e6272afbe2a819e9732
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.7 MB (203698783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160cc52ce9b78d794b4acbd3286cc62c771bad645eb50e8c9af6722d743f166c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:10 GMT
ADD file:4cd2f95737fd3007912428eeac56036c9e67e989e66cec08a8be99da47f88494 in / 
# Tue, 02 Aug 2022 00:49:10 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:38:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 20:38:12 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 20:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:38:23 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 22:45:24 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 23:08:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 23:08:11 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 23:08:11 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 23:08:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 23:08:30 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 19:10:52 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 19:10:52 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 19:17:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 19:17:42 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 19:17:42 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 19:17:43 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 19:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 19:17:43 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 19:17:43 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 19:17:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5890b0ca6af5e8467a488e68716691950496a8f247d0495c2d595ddcb1893aff`  
		Last Modified: Tue, 02 Aug 2022 00:56:06 GMT  
		Size: 28.9 MB (28905515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eafe902d3c868e979e01e5c5aca6567b8be8b60814b9e1ce93c2b749451b410`  
		Last Modified: Wed, 03 Aug 2022 02:16:47 GMT  
		Size: 1.1 MB (1059641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e073b0922c53e3aee167b94b195f01b7740c95a691b391e30bbc1dd36133f578`  
		Last Modified: Wed, 03 Aug 2022 02:18:15 GMT  
		Size: 11.7 MB (11687058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1563deb88ac81fbc07f66164de09058989bc2f52e4b201209996fc610e7424`  
		Last Modified: Wed, 03 Aug 2022 02:18:11 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9586a9ae76d2fcf29975a3cbac30868417a5e7209b4d681ab4d8cdc9417e1127`  
		Last Modified: Wed, 03 Aug 2022 02:18:13 GMT  
		Size: 3.3 MB (3335517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2138d4d7c7c422781a7da5bbba917dfee3de2e44c0b89e2c05cd5fb54d6aec`  
		Last Modified: Wed, 03 Aug 2022 19:18:28 GMT  
		Size: 21.2 MB (21220513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ec77684813e78ff3c43e62e86fde2b1964089fb2e02c36be1b197e18d76199`  
		Last Modified: Wed, 03 Aug 2022 19:18:38 GMT  
		Size: 137.5 MB (137478750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecfeff163b4d6f23860d774bf123b6ad13105fce4fa35bddd9e46a56b0c09af`  
		Last Modified: Wed, 03 Aug 2022 19:18:21 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb3f6f2ab2014dd8287001b208c1dc97200c2c3e16a2cb980fd938dfd82858b`  
		Last Modified: Wed, 03 Aug 2022 19:18:22 GMT  
		Size: 2.1 KB (2111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1` - linux; arm variant v7

```console
$ docker pull satosa@sha256:1eb7ef57547ada8079868ad16a792df4e4cbc8571c4b2beb50d5682d1bc6250f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202351243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194a9b56fc0cc44a0542e47df53c65db1e4f7a579b5a8624e2b202e21462c73d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:58:59 GMT
ADD file:1575b776a15adacebc0875642e97a80807d42dcfc8917e1406d47af7ac244c97 in / 
# Tue, 02 Aug 2022 00:58:59 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:34:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 04:34:22 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 04:34:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 04:34:30 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 06:30:14 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 06:52:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 06:52:09 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 06:52:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 06:52:24 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 13:20:49 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 13:20:50 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 13:26:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 13:26:45 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 13:26:45 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 13:26:45 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 13:26:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 13:26:45 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 13:26:45 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 13:26:45 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1dd75a3a9c893a7dc313f683dd62464b7eab6c6d522ee62c8a17022631830f32`  
		Last Modified: Tue, 02 Aug 2022 01:06:45 GMT  
		Size: 26.6 MB (26560586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4206fea8c3d0ae09213fad25e06bb550a03c76c2b15e7a3c134ee5e2d217cd`  
		Last Modified: Wed, 03 Aug 2022 11:19:22 GMT  
		Size: 1.0 MB (1041632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed9dda465ec974f3e81b6b5f48dee0c43b63aeae625042e1e5f8ca482d43f1f`  
		Last Modified: Wed, 03 Aug 2022 11:21:19 GMT  
		Size: 11.2 MB (11205345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c669588520ce26d52819574b6ac8f40bc121ec539aae49c4cdc6aa899fcea`  
		Last Modified: Wed, 03 Aug 2022 11:21:15 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75c71e6575f11c76771634448c2e1c7e6988853591c1422d979aaf3dfa73569`  
		Last Modified: Wed, 03 Aug 2022 11:21:17 GMT  
		Size: 3.3 MB (3335656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d5ac04f9c39c2ba1d884f419e586ede32f2779ea0bbb6a7033e0f70c79d670`  
		Last Modified: Thu, 04 Aug 2022 13:31:15 GMT  
		Size: 20.9 MB (20949533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65844885dbff2fac2bccf9e5a7b69d9c423352d19d5ffb5eeca720f5e2a10886`  
		Last Modified: Thu, 04 Aug 2022 13:31:26 GMT  
		Size: 139.2 MB (139246702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53ebddc2eb90a987a1bae1b3a245f2d88ae7ea81a35f85f6bfdf10891217d58`  
		Last Modified: Thu, 04 Aug 2022 13:31:10 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa39e50e9a3812f026202131476b98a06e4a65a16a21fee180aeb54d979e2cb8`  
		Last Modified: Thu, 04 Aug 2022 13:31:10 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:8a7bc186f7c0a8725b284d01a4dceac8636d5f7f96b11f0d4031fd66f199e2b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79849083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56454aaf2924873a1f55890e93e1c83261d4047ce84a080d73750691435b3d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:03:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 12:03:30 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 12:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:03:36 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 09:19:10 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 09:29:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 09:29:22 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 09:29:22 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 09:29:23 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 09:29:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 09:29:25 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 09:29:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 09:29:37 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 10:39:28 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 10:39:28 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 10:40:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 10:40:15 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 10:40:16 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 10:40:18 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 10:40:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 10:40:19 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 10:40:20 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 10:40:21 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f101f90cc8f7640b7db5f7094941a1fe4ff28e11a968d3a36f146a89a480ecbb`  
		Last Modified: Tue, 02 Aug 2022 14:47:06 GMT  
		Size: 1.1 MB (1063812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a5d6cf27653f158e4f7552f31dc146332b6d820679ee42ebff5b4e47f4dac`  
		Last Modified: Wed, 03 Aug 2022 10:31:15 GMT  
		Size: 12.2 MB (12153733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd415bdc2c72c852623e384c90826d41aa2739adbc3158bd814bc3e562ab16ea`  
		Last Modified: Wed, 03 Aug 2022 10:31:13 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90ceb316b2d011719d35fb58a5d69ec1b84ebc6a9ab5568354ca370aad48524`  
		Last Modified: Wed, 03 Aug 2022 10:31:14 GMT  
		Size: 3.1 MB (3119919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7a23c6e6d4ea56699e3033f9fd616c6fa79290a257066f21578bf773f283cb`  
		Last Modified: Wed, 03 Aug 2022 10:42:23 GMT  
		Size: 19.3 MB (19324710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f64adba6c540f9f4fde33df9a99fa32be543c937e20b203b409ba3340f7b62`  
		Last Modified: Wed, 03 Aug 2022 10:42:23 GMT  
		Size: 14.1 MB (14120866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9df97e7203d91c6109257b6e98c0bb926732214ee96a7110c86550f8c271b74`  
		Last Modified: Wed, 03 Aug 2022 10:42:20 GMT  
		Size: 9.4 KB (9394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d56269ee4307b5c76ba7efef9346008e1440979b95ee777b9d5e8e3e4ead5b1`  
		Last Modified: Wed, 03 Aug 2022 10:42:20 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1` - linux; 386

```console
$ docker pull satosa@sha256:ff2180ab006e1d173a6d157a2ef8b05c4abae7d45d5693889e12f05e6861a42d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207396057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b9632c4df58a4c5e3e68e82bf8bab7462b2530f9ecfb108feb8726a85ab4d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:39:20 GMT
ADD file:f771e2286465694126158821089d801c7296376be2a56189e6041a15d2fe79f5 in / 
# Tue, 02 Aug 2022 00:39:21 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 11:22:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 11:22:53 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 11:22:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 11:22:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 20:51:53 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 21:03:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 21:03:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 21:03:55 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 21:03:56 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 21:03:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 21:03:58 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 21:04:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 21:04:12 GMT
CMD ["python3"]
# Tue, 02 Aug 2022 22:21:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 02 Aug 2022 22:21:44 GMT
ENV SATOSA_VERSION=8.1.1
# Tue, 02 Aug 2022 23:39:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 02 Aug 2022 23:39:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 02 Aug 2022 23:39:26 GMT
WORKDIR /etc/satosa
# Tue, 02 Aug 2022 23:39:28 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Tue, 02 Aug 2022 23:39:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 23:39:29 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 23:39:30 GMT
USER satosa:satosa
# Tue, 02 Aug 2022 23:39:31 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:90eb7f0ce9f33cf5dcd67d54c2fa606186dbaa5f95b6046f36145097267f9e53`  
		Last Modified: Tue, 02 Aug 2022 00:45:14 GMT  
		Size: 32.4 MB (32374054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd27ead98f25cd891e8dfae23b5500c856f3a9db336a545eed8b5f180a6df0b4`  
		Last Modified: Tue, 02 Aug 2022 14:37:54 GMT  
		Size: 1.1 MB (1088442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7362ecffe5fefdfcff89188358cb648fae40c1fed6254cd3325ef1c340a0ca9b`  
		Last Modified: Tue, 02 Aug 2022 22:15:01 GMT  
		Size: 12.2 MB (12224818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fb82e70fda9a811619f0b6cfd165d59473bcc467e702a70231630e64335b18`  
		Last Modified: Tue, 02 Aug 2022 22:14:59 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab067ab28a29ee91955ebd00b4849cd1d1993a430051ce801b5eaffeeb59b976`  
		Last Modified: Tue, 02 Aug 2022 22:15:00 GMT  
		Size: 3.1 MB (3119814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c68c7fda4b282e37efe94863aed2872d62133ead0fed4a4b4174eab16a125f`  
		Last Modified: Tue, 02 Aug 2022 23:40:27 GMT  
		Size: 22.6 MB (22586591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4630af60cc9f0637de40da0789c8be2b49091d860ae7f21753e736c5a24b0fac`  
		Last Modified: Tue, 02 Aug 2022 23:40:44 GMT  
		Size: 136.0 MB (135990599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ba92ddedaf8e60d74aac7773867aec0a84b2812ba92a5742090bee107e7736`  
		Last Modified: Tue, 02 Aug 2022 23:40:24 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e28ea4f42ac6baac91e14de0ee8d101956ac6d64c7d4078bb57ebfddde33184`  
		Last Modified: Tue, 02 Aug 2022 23:40:24 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1` - linux; mips64le

```console
$ docker pull satosa@sha256:b9bdbc69a8a0be593fe150cbd4334f006447c17a9538b850002e7fa96445593b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.8 MB (205844024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7d3830a289e7a92a0277b60e6cce741d4887ea889e4e236cdd2d878fb1f64b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:10:34 GMT
ADD file:6dc22a1e5b5fcf23f2549406ddcc45c4e244f46e21eafa881de81fa87438e5d8 in / 
# Tue, 02 Aug 2022 01:10:38 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 10:25:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 10:25:08 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 10:25:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:25:36 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 04 Aug 2022 04:16:09 GMT
ENV PYTHON_VERSION=3.10.6
# Thu, 04 Aug 2022 05:33:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Thu, 04 Aug 2022 05:33:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 04 Aug 2022 05:33:27 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Thu, 04 Aug 2022 05:33:30 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Thu, 04 Aug 2022 05:33:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Thu, 04 Aug 2022 05:33:35 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Thu, 04 Aug 2022 05:34:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 04 Aug 2022 05:34:30 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 08:35:12 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 08:35:15 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 08:52:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 08:52:17 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 08:52:21 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 08:52:25 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 08:52:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 08:52:34 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 08:52:39 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 08:52:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:88350749a27614c791450c256b051f023d81cdd256211274b1efac493779d2be`  
		Last Modified: Tue, 02 Aug 2022 01:21:02 GMT  
		Size: 29.6 MB (29628964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61130d003a0ea87819935a3a252db1861d9b87e1313fa7988d5f0642637f3e`  
		Last Modified: Tue, 02 Aug 2022 23:46:40 GMT  
		Size: 1.0 MB (1049605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e786491697e5d2bd3dee622f7eae98810c04c895d5024e910e2394f92b37ad8`  
		Last Modified: Thu, 04 Aug 2022 08:14:51 GMT  
		Size: 12.1 MB (12124464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fb1366c066d6bf94df2bf081524439083c14a1f292da85f218000ac515a2f5`  
		Last Modified: Thu, 04 Aug 2022 08:14:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe7637d1173b353af8622199dfbc92d0f74f8cff129fe540541b9c069a058d3`  
		Last Modified: Thu, 04 Aug 2022 08:14:46 GMT  
		Size: 3.1 MB (3120804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4655831cce551d936028a78d3d4a295cd96e3ca02ea0f5f726d0b963350a0e`  
		Last Modified: Thu, 04 Aug 2022 08:53:18 GMT  
		Size: 21.3 MB (21288233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54965dd4effca16f75a92cdac5dd71e708a50d218ca30b0806964a58d8b726ee`  
		Last Modified: Thu, 04 Aug 2022 08:53:58 GMT  
		Size: 138.6 MB (138620211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a449c61594c6b3d2e0fa03d876ebe6fc8561eaa1d46ebf088772a42dea52b596`  
		Last Modified: Thu, 04 Aug 2022 08:53:06 GMT  
		Size: 9.4 KB (9396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54e620f3a05fe34c293ac1de03899ec567f49faa21a8db43216f796387f8f65`  
		Last Modified: Thu, 04 Aug 2022 08:53:06 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1` - linux; ppc64le

```console
$ docker pull satosa@sha256:b84ad93ccca31f2ba03b7c0586ad9f3a2d71764d4338922af798ae737ec87f23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212244381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f29a99f45c08fb90c8ad9dec84fd55c14d0ca8ecbc00c2160fc3464a14feca9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:17:30 GMT
ADD file:3a95a896d463569ce82199957052b3467123a4bd3385a0a4e397cf08402a99c3 in / 
# Tue, 02 Aug 2022 01:17:32 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:03:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 16:03:13 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 16:03:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 16:03:24 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 18:10:29 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 18:43:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 18:43:03 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 18:43:03 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 18:43:03 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 18:43:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 18:43:04 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 18:43:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 18:43:25 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 21:09:20 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 21:09:21 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 21:14:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 21:14:39 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 21:14:39 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 21:14:40 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 21:14:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 21:14:41 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 21:14:41 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 21:14:42 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5241cd116d6e6e2d62f3d8c2245b74daca9f6cc154eaccd738feb41984c74714`  
		Last Modified: Tue, 02 Aug 2022 01:24:39 GMT  
		Size: 35.3 MB (35272771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf6dcfcb4fa2f4e24ce6bed8b3eda6b0d49d92062cb34d95830e4e9f512270`  
		Last Modified: Wed, 03 Aug 2022 00:14:29 GMT  
		Size: 1.1 MB (1094658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdc50327f93cca5ad2c5f8500471040045b715045a9a4852ece90b3155d5aea`  
		Last Modified: Wed, 03 Aug 2022 20:42:55 GMT  
		Size: 12.5 MB (12473465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49f3fdf44cc1cf9b0e2d32c8ea2b62a0d3eb7eac481b56c9d11e44c66b764fe`  
		Last Modified: Wed, 03 Aug 2022 20:42:52 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd9d6c8cb5530b56f02a736bb1cc24d2d0ffc11d6fb55dc6befb0e114a1ff74`  
		Last Modified: Wed, 03 Aug 2022 20:42:53 GMT  
		Size: 3.3 MB (3336216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209342dd334b280e74196c0e693487033f7f2d08880ab61f5f9113dbbd5d0461`  
		Last Modified: Wed, 03 Aug 2022 21:22:32 GMT  
		Size: 22.2 MB (22158681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11809242e6bd5adbd0096d37646b954f666a1e2a107dd5442773977caa919360`  
		Last Modified: Wed, 03 Aug 2022 21:22:45 GMT  
		Size: 137.9 MB (137896801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa36501b6a1d8ec2e51a6a162f1f43d70ea4b035335513b65b800346790717`  
		Last Modified: Wed, 03 Aug 2022 21:22:27 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fe38c0944e97231334e780f32f3cd041644756c5b195812b19edd697268021`  
		Last Modified: Wed, 03 Aug 2022 21:22:27 GMT  
		Size: 2.1 KB (2113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1` - linux; s390x

```console
$ docker pull satosa@sha256:f52b8375aeb8b39ad8ae5b9f05f4f94a47f4776b3f500aeeadee19c4ed572f5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202163420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f253b8b35e8bbaf69f23beb8a8584dc48a0c682127faa17ed9d639b33dfdf3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 08:30:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 08:30:40 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 08:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 08:30:44 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 22:09:42 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 22:18:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 22:18:03 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 22:18:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 22:18:13 GMT
CMD ["python3"]
# Tue, 02 Aug 2022 23:28:28 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 02 Aug 2022 23:28:31 GMT
ENV SATOSA_VERSION=8.1.1
# Tue, 02 Aug 2022 23:32:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 02 Aug 2022 23:33:02 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 02 Aug 2022 23:33:02 GMT
WORKDIR /etc/satosa
# Tue, 02 Aug 2022 23:33:02 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Tue, 02 Aug 2022 23:33:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 23:33:02 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 23:33:03 GMT
USER satosa:satosa
# Tue, 02 Aug 2022 23:33:03 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c36d12a9d2aa3bd2ed5880b10e768bae6cab779992e198cf595d3b8d6924d5`  
		Last Modified: Tue, 02 Aug 2022 10:43:27 GMT  
		Size: 1.1 MB (1075771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a2fa2a5f3f4be291fac87451996292e32ad4b6b7e7ae168c720b6501ba676f`  
		Last Modified: Tue, 02 Aug 2022 23:23:49 GMT  
		Size: 11.9 MB (11900903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1958402e81da32fc50ee2b3d3d48a5714015a6589a9b0882e2e0862173874f52`  
		Last Modified: Tue, 02 Aug 2022 23:23:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adc16df778c23094a004c62669c6de553142901db4933d76959d223598473b`  
		Last Modified: Tue, 02 Aug 2022 23:23:49 GMT  
		Size: 3.3 MB (3335624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5f479e9444a18e7100a74300ba30ab5818c9023c386c0a537811de457f1e99`  
		Last Modified: Tue, 02 Aug 2022 23:33:39 GMT  
		Size: 19.6 MB (19580744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573792100821147cd9e469e566ed70175d1fe8ec2b68e371484abc92f0aeaf74`  
		Last Modified: Tue, 02 Aug 2022 23:33:45 GMT  
		Size: 136.6 MB (136618328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cb6a07895307e25b49bb3cdebc3f6e29fef231b0390c00ddacc6b74ee5f9fd`  
		Last Modified: Tue, 02 Aug 2022 23:33:36 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0ce3aebbe275e54928297909f6f1ed7c7beee5c901706ccef91eec96eb8bc5`  
		Last Modified: Tue, 02 Aug 2022 23:33:36 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.1.1-alpine`

```console
$ docker pull satosa@sha256:fa00b0ab420886685085b244405746ecce141ff81c408876a6d8c17f5e0960ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `satosa:8.1.1-alpine` - linux; amd64

```console
$ docker pull satosa@sha256:889e8b702bc04ca43d059bdf24c8db677954c87e5318ba8a93d795e450d485dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42508179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa3cc16430e95981e37a39687b5b6a8e23b8adf5eb81881cab4136b31de9b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:14:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 02:01:52 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 02:01:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 19 Jul 2022 02:01:54 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 10:48:21 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 11:00:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 11:00:14 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 11:00:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 11:00:21 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 11:47:34 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 11:47:34 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 11:48:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 11:48:18 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 11:48:19 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 11:48:19 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 11:48:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 11:48:19 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 11:48:19 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 11:48:19 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c14b1a767335de44f2bc926cb52487979a0fe602ac5429643dbb238f297fb`  
		Last Modified: Tue, 19 Jul 2022 02:56:13 GMT  
		Size: 666.8 KB (666769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571274b8543b548747b5e9bef700a89692fe9403cc364be8d6e8a0792ccfe2b4`  
		Last Modified: Wed, 03 Aug 2022 11:19:35 GMT  
		Size: 12.5 MB (12508608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f79a08255af5d614c7b4b81e358b5bb607bdcb14a6475c836d3d4f92f094846`  
		Last Modified: Wed, 03 Aug 2022 11:19:34 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6b20e3f6abd46292c29437a6917dc82b769ebb239e2d971aedb6695e057715`  
		Last Modified: Wed, 03 Aug 2022 11:19:34 GMT  
		Size: 3.0 MB (3043671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c974d4972d870a99bf0fba525cab86b298dd6e9405d3329a3495a164ae5c7`  
		Last Modified: Wed, 03 Aug 2022 11:49:00 GMT  
		Size: 9.4 MB (9398243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c482d554455c83821852ea2cd26eaf97f49bb1c7983342cec7242b8ea5432234`  
		Last Modified: Wed, 03 Aug 2022 11:49:01 GMT  
		Size: 14.1 MB (14080297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b861965b84abb04a92b63eb19a620daf7360785f485bc2d526885601454b19ca`  
		Last Modified: Wed, 03 Aug 2022 11:48:58 GMT  
		Size: 9.4 KB (9439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16e011f2d9efad78d03ac0d4c7abe2f694dfc5f6c158ef9fa350a3f21d22a8e`  
		Last Modified: Wed, 03 Aug 2022 11:48:58 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1-alpine` - linux; arm variant v6

```console
$ docker pull satosa@sha256:1ed78492e93849ebbee5cd80dd5e4a91eb2a41676fbc3d21584a17d402028ca7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160179359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e822b6bb9258ee22b55f2f03c3d389710a39d0a3fa1d10f1250cb00db2f3e268`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 19:49:37 GMT
ADD file:7a20333469e71664904a0cb8f61613250f2bd092b4a27bfa7bbae1dc7e21b7ed in / 
# Mon, 18 Jul 2022 19:49:37 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 00:30:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 00:30:05 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 00:30:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 00:30:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 19:50:04 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 20:30:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 02 Aug 2022 20:30:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 20:30:20 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 20:30:20 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 03:20:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 03:20:45 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 03:27:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 03:27:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 03:27:54 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 03:27:54 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 03:27:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 03:27:55 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 03:27:55 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 03:27:55 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b7885075fcd06a866d12dfd56eb704045eaadbd22dc03a224cd98715be566677`  
		Last Modified: Mon, 18 Jul 2022 19:08:42 GMT  
		Size: 2.6 MB (2606431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ebe8e3a2f83d0ddc301c9b9d6405376eecb906b92082e05d5e257eff5f6293`  
		Last Modified: Wed, 27 Jul 2022 11:08:23 GMT  
		Size: 672.3 KB (672287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b647934af90a736595f675559fd3aebbcdbcfc67277de68401980916f3c217d7`  
		Last Modified: Wed, 03 Aug 2022 00:13:17 GMT  
		Size: 12.1 MB (12085055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaef313095ff837d4848dec2c5e458a33e59ee4e1ab7a9d4e3d244d20b92fbf`  
		Last Modified: Wed, 03 Aug 2022 00:13:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba453d098c35b58faf7cc2ac6a90a0e9a8941dc90611ee397d12af0a546bbe87`  
		Last Modified: Wed, 03 Aug 2022 00:13:15 GMT  
		Size: 3.0 MB (3043708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0a90158473abc47e6b9744b5cc61265a9552ba9217486241f5b7b4a5d12eec`  
		Last Modified: Wed, 03 Aug 2022 03:28:44 GMT  
		Size: 8.3 MB (8280231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a82dd9e01f89340501ac0415caccc1ad608cc08d55219cb26db2226dc64b83`  
		Last Modified: Wed, 03 Aug 2022 03:29:07 GMT  
		Size: 133.5 MB (133479861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ee2ba314aef7361329abd7eaa7a8860079655317f4d5fc9d37f73f8b34de4`  
		Last Modified: Wed, 03 Aug 2022 03:28:39 GMT  
		Size: 9.4 KB (9438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24649d01bd9f34f035857fcb9324aef45128d255b0e7d7c9be9d0d9d58a928f3`  
		Last Modified: Wed, 03 Aug 2022 03:28:39 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1-alpine` - linux; arm variant v7

```console
$ docker pull satosa@sha256:9c12b392cb5946a433fe0c98001d362d79a953040068a9d0843c3a9a9c12fb8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163401667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55a50fb783bb28da31c92c6cff33c408ef6ea7e1c6da179086af8ce588f092d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:24:47 GMT
ADD file:68590e866bc6db27ad54d23de7dd275d0389cb86e4e6291a1243fcc234f2f7a1 in / 
# Mon, 18 Jul 2022 21:24:47 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 03:57:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 03:57:44 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 03:57:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 03:57:46 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 07:37:59 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 08:07:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 08:07:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 08:07:50 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 08:07:51 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 13:27:03 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 13:27:03 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 13:30:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 13:30:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 13:30:25 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 13:30:25 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 13:30:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 13:30:25 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 13:30:25 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 13:30:25 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a6b45ace95f42a930d15c33679ab9c85d46019b7e73954cadc73bb9ba176509b`  
		Last Modified: Mon, 18 Jul 2022 19:08:56 GMT  
		Size: 2.4 MB (2412307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d826ef3e3e077607452c51ac5332613cc0a20903abe17b56af4b973f31f0e9b7`  
		Last Modified: Wed, 27 Jul 2022 10:54:47 GMT  
		Size: 664.1 KB (664079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116f12212b7e97cde5b72713f0f3a3025a9ef6dffccdc353cd4d15407d343a72`  
		Last Modified: Wed, 03 Aug 2022 11:22:41 GMT  
		Size: 11.6 MB (11558755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef2affe775c9998dea9fd354aa8d4b6e97117d2092c84f1401265b9f9528bf7`  
		Last Modified: Wed, 03 Aug 2022 11:22:38 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032af4833525c8884057f85c0da98a7f2dedc337784e4ce3645fad79e6633b26`  
		Last Modified: Wed, 03 Aug 2022 11:22:39 GMT  
		Size: 3.0 MB (3043658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65c3d7d841a308ff58960bdd0832a9c2fc9d01d091b4478549cf91ad4551edc`  
		Last Modified: Thu, 04 Aug 2022 13:31:47 GMT  
		Size: 8.0 MB (8026973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553863577a06e5d191ae29abc79bb81603188e34e406ebce36a4e4da49320df8`  
		Last Modified: Thu, 04 Aug 2022 13:31:59 GMT  
		Size: 137.7 MB (137684108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d66d75890a5436b91b581c5023634cbedf248e1dbb622b1241f80c5a4ed29`  
		Last Modified: Thu, 04 Aug 2022 13:31:45 GMT  
		Size: 9.4 KB (9439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cab52b5f6577ce2ac31dd72be231ca9d43531003be80eacfe2f20bbfa5c5d5`  
		Last Modified: Thu, 04 Aug 2022 13:31:46 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1-alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:cccb94f4511ba8a1fd8ab69a69f483edef010e4fab16eeccfb637ae5395cdc67
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40930309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83c2e990bd9017e2a1f46423fc6e313b33122d383dda9f8f9c00e8006d36921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:10:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 01:53:04 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 01:53:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 19 Jul 2022 01:53:06 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 09:50:39 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 10:05:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 10:05:10 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 10:05:11 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 10:05:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 10:05:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 10:05:14 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 10:05:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 10:05:22 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 10:40:42 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 10:40:43 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 10:41:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 10:41:33 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 10:41:34 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 10:41:36 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 10:41:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 10:41:37 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 10:41:38 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 10:41:39 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c36086fc9356a3d9879c8427af90dd86ad6fd35b3929bab2af384e98d0571c`  
		Last Modified: Tue, 19 Jul 2022 02:56:56 GMT  
		Size: 668.0 KB (668022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255e9c7248a65c9bb1f14e3ffaf6aad2e14b965bfd9196b30e8c1efc8ddd1747`  
		Last Modified: Wed, 03 Aug 2022 10:34:00 GMT  
		Size: 12.6 MB (12579036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d32815e9cd0f789447579f484cec5ed6ff5b006c50c121a5e314519ffad01d5`  
		Last Modified: Wed, 03 Aug 2022 10:33:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c6e4018f23818adb74c050daeddb28d2efddbabe1135f85ed3ef29b17ec7b`  
		Last Modified: Wed, 03 Aug 2022 10:32:56 GMT  
		Size: 3.0 MB (3045000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2feaf81b71b2f7b13ac6cefc0f434f31221423c1c94002a89138b4c60741ced`  
		Last Modified: Wed, 03 Aug 2022 10:42:41 GMT  
		Size: 8.2 MB (8224897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c9e9ae46115c582ac3a68bb4b583d2ed73875acfb5ff520c5877d481be9cdc`  
		Last Modified: Wed, 03 Aug 2022 10:42:42 GMT  
		Size: 13.7 MB (13706894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e959a5cfce7f6c07db205394594178b791ab1fd7b3425ded77627110666277`  
		Last Modified: Wed, 03 Aug 2022 10:42:40 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143d97f09a0b08aff0f4993e07d50c6a62b1d1c84b442a35f1c8b7f9535005f4`  
		Last Modified: Wed, 03 Aug 2022 10:42:40 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1-alpine` - linux; 386

```console
$ docker pull satosa@sha256:3b7052fea622f5d95da31220bc234a9258ae473482fb55269dea295fd83b4e05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (173023892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712f8d15ddeef960a7327c512f8d03f337021df170d7531f5aa93eafbe51d2c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 21:22:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 21:22:15 GMT
ENV LANG=C.UTF-8
# Tue, 09 Aug 2022 21:22:17 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 09 Aug 2022 21:22:18 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 09 Aug 2022 22:02:59 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 09 Aug 2022 22:16:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 09 Aug 2022 22:16:19 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 09 Aug 2022 22:16:20 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 09 Aug 2022 22:16:21 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 09 Aug 2022 22:16:22 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 09 Aug 2022 22:16:23 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 09 Aug 2022 22:16:31 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 09 Aug 2022 22:16:31 GMT
CMD ["python3"]
# Wed, 10 Aug 2022 03:30:07 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 10 Aug 2022 03:30:08 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 10 Aug 2022 03:33:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 10 Aug 2022 03:33:03 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 10 Aug 2022 03:33:04 GMT
WORKDIR /etc/satosa
# Wed, 10 Aug 2022 03:33:06 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 10 Aug 2022 03:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 03:33:07 GMT
EXPOSE 8080
# Wed, 10 Aug 2022 03:33:08 GMT
USER satosa:satosa
# Wed, 10 Aug 2022 03:33:09 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6e4c463b4b085b81ccd90e5d99d5d5b64a56c2f756e7ff5575080b0efc2e9f`  
		Last Modified: Tue, 09 Aug 2022 23:12:22 GMT  
		Size: 689.1 KB (689070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30e501e19288fafd4b62af6aaf0b588b8da1b9f7bf0ed0bd8c7cf5550131f4b`  
		Last Modified: Tue, 09 Aug 2022 23:13:12 GMT  
		Size: 12.7 MB (12700838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5383c9c382f8845fcf42a8ea747ddb3a99c87e277380a509277f27c6bf8d85`  
		Last Modified: Tue, 09 Aug 2022 23:13:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2450ac53e437f841f48f00e832466a3d7ce73190f3f5255c89dfb89edcd9193`  
		Last Modified: Tue, 09 Aug 2022 23:13:11 GMT  
		Size: 3.0 MB (3045003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3183acab5e336c62f2d06a000d65364d4484e755eb4c01749dd6e443ee703e32`  
		Last Modified: Wed, 10 Aug 2022 03:34:01 GMT  
		Size: 8.5 MB (8512861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350ea1863d968db10b0fe1fd8772d772c84631136d5fb13934b7c5a360cf66fc`  
		Last Modified: Wed, 10 Aug 2022 03:34:28 GMT  
		Size: 145.3 MB (145257262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92895882e21832e6f4d040fa6f60752d36b168dbc7f3893d1fc81a19da18cfc3`  
		Last Modified: Wed, 10 Aug 2022 03:33:59 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85df40b1b491557b15d24c816c82279561fd23244d53603eeea4f9976ce8766`  
		Last Modified: Wed, 10 Aug 2022 03:33:59 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1-alpine` - linux; ppc64le

```console
$ docker pull satosa@sha256:f70b3121c8db732d980c4272ea937145d0745875aba33578b5667bbaf28fb1ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164310759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef00aeaa317867dd9dca82b0661794be10c5d0a082d11a8f76b597b76e88cb55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:29:30 GMT
ADD file:69e4080f15f54e2d8f8aa25fdcba9c01dde149d43592edd5023106675e54a769 in / 
# Mon, 18 Jul 2022 21:29:31 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 04:30:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 04:30:31 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 04:30:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 04:30:33 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 19:40:20 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 20:04:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 20:05:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 20:05:00 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 20:05:00 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 20:05:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 20:05:01 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 20:05:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 20:05:13 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 21:15:12 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 21:15:12 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 21:21:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 21:21:41 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 21:21:41 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 21:21:42 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 21:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 21:21:42 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 21:21:43 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 21:21:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:602896d442490cd3fbb6599f0f862d3673b7cd58eca3ac842b8e09bf8d012443`  
		Last Modified: Mon, 18 Jul 2022 19:09:09 GMT  
		Size: 2.8 MB (2789923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6556a4bf6509d5fd24900f56a6175bd811b9dd8c6f4f51e2732b6888a2b8933`  
		Last Modified: Wed, 27 Jul 2022 13:49:16 GMT  
		Size: 677.0 KB (676971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c735731e55a5ddb324dd5eb175e1f3d88895a77ea93b8fb08428ee522445708b`  
		Last Modified: Wed, 03 Aug 2022 20:44:16 GMT  
		Size: 12.8 MB (12819587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e525d9b2b00fc7130f21f05f981c44d849b279417c15b38703c3f11d3c9bd667`  
		Last Modified: Wed, 03 Aug 2022 20:44:13 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9bc880d40f528e2c6046dd7bad61fc78f27a3fbebe3f45d1348a72ace67d9b`  
		Last Modified: Wed, 03 Aug 2022 20:44:15 GMT  
		Size: 3.0 MB (3043656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b74e25b6a705707a07e0411366545458ad05f07844bde5b7bebddd988e69068`  
		Last Modified: Wed, 03 Aug 2022 21:23:08 GMT  
		Size: 8.5 MB (8476895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141bd7d880682fd816129f41549c798cabb9e94494f7ee7714d6e83e63606b82`  
		Last Modified: Wed, 03 Aug 2022 21:23:23 GMT  
		Size: 136.5 MB (136491944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b412f1d24946cb1e7f3d66a4ae5595d3b71ae6040af529dc49507cb1dd4e06c`  
		Last Modified: Wed, 03 Aug 2022 21:23:06 GMT  
		Size: 9.4 KB (9434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8aa237953d155695df1943bb27b03cf1cc3f1716ea63b1cf5a8b12d97cd6cea`  
		Last Modified: Wed, 03 Aug 2022 21:23:06 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.1.1-alpine3.16`

```console
$ docker pull satosa@sha256:fa00b0ab420886685085b244405746ecce141ff81c408876a6d8c17f5e0960ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `satosa:8.1.1-alpine3.16` - linux; amd64

```console
$ docker pull satosa@sha256:889e8b702bc04ca43d059bdf24c8db677954c87e5318ba8a93d795e450d485dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42508179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa3cc16430e95981e37a39687b5b6a8e23b8adf5eb81881cab4136b31de9b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:14:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 02:01:52 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 02:01:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 19 Jul 2022 02:01:54 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 10:48:21 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 11:00:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 11:00:14 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 11:00:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 11:00:21 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 11:47:34 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 11:47:34 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 11:48:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 11:48:18 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 11:48:19 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 11:48:19 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 11:48:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 11:48:19 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 11:48:19 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 11:48:19 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c14b1a767335de44f2bc926cb52487979a0fe602ac5429643dbb238f297fb`  
		Last Modified: Tue, 19 Jul 2022 02:56:13 GMT  
		Size: 666.8 KB (666769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571274b8543b548747b5e9bef700a89692fe9403cc364be8d6e8a0792ccfe2b4`  
		Last Modified: Wed, 03 Aug 2022 11:19:35 GMT  
		Size: 12.5 MB (12508608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f79a08255af5d614c7b4b81e358b5bb607bdcb14a6475c836d3d4f92f094846`  
		Last Modified: Wed, 03 Aug 2022 11:19:34 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6b20e3f6abd46292c29437a6917dc82b769ebb239e2d971aedb6695e057715`  
		Last Modified: Wed, 03 Aug 2022 11:19:34 GMT  
		Size: 3.0 MB (3043671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c974d4972d870a99bf0fba525cab86b298dd6e9405d3329a3495a164ae5c7`  
		Last Modified: Wed, 03 Aug 2022 11:49:00 GMT  
		Size: 9.4 MB (9398243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c482d554455c83821852ea2cd26eaf97f49bb1c7983342cec7242b8ea5432234`  
		Last Modified: Wed, 03 Aug 2022 11:49:01 GMT  
		Size: 14.1 MB (14080297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b861965b84abb04a92b63eb19a620daf7360785f485bc2d526885601454b19ca`  
		Last Modified: Wed, 03 Aug 2022 11:48:58 GMT  
		Size: 9.4 KB (9439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16e011f2d9efad78d03ac0d4c7abe2f694dfc5f6c158ef9fa350a3f21d22a8e`  
		Last Modified: Wed, 03 Aug 2022 11:48:58 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1-alpine3.16` - linux; arm variant v6

```console
$ docker pull satosa@sha256:1ed78492e93849ebbee5cd80dd5e4a91eb2a41676fbc3d21584a17d402028ca7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160179359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e822b6bb9258ee22b55f2f03c3d389710a39d0a3fa1d10f1250cb00db2f3e268`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 19:49:37 GMT
ADD file:7a20333469e71664904a0cb8f61613250f2bd092b4a27bfa7bbae1dc7e21b7ed in / 
# Mon, 18 Jul 2022 19:49:37 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 00:30:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 00:30:05 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 00:30:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 00:30:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 19:50:04 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 20:30:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 02 Aug 2022 20:30:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 20:30:20 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 20:30:20 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 03:20:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 03:20:45 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 03:27:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 03:27:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 03:27:54 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 03:27:54 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 03:27:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 03:27:55 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 03:27:55 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 03:27:55 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b7885075fcd06a866d12dfd56eb704045eaadbd22dc03a224cd98715be566677`  
		Last Modified: Mon, 18 Jul 2022 19:08:42 GMT  
		Size: 2.6 MB (2606431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ebe8e3a2f83d0ddc301c9b9d6405376eecb906b92082e05d5e257eff5f6293`  
		Last Modified: Wed, 27 Jul 2022 11:08:23 GMT  
		Size: 672.3 KB (672287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b647934af90a736595f675559fd3aebbcdbcfc67277de68401980916f3c217d7`  
		Last Modified: Wed, 03 Aug 2022 00:13:17 GMT  
		Size: 12.1 MB (12085055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaef313095ff837d4848dec2c5e458a33e59ee4e1ab7a9d4e3d244d20b92fbf`  
		Last Modified: Wed, 03 Aug 2022 00:13:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba453d098c35b58faf7cc2ac6a90a0e9a8941dc90611ee397d12af0a546bbe87`  
		Last Modified: Wed, 03 Aug 2022 00:13:15 GMT  
		Size: 3.0 MB (3043708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0a90158473abc47e6b9744b5cc61265a9552ba9217486241f5b7b4a5d12eec`  
		Last Modified: Wed, 03 Aug 2022 03:28:44 GMT  
		Size: 8.3 MB (8280231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a82dd9e01f89340501ac0415caccc1ad608cc08d55219cb26db2226dc64b83`  
		Last Modified: Wed, 03 Aug 2022 03:29:07 GMT  
		Size: 133.5 MB (133479861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ee2ba314aef7361329abd7eaa7a8860079655317f4d5fc9d37f73f8b34de4`  
		Last Modified: Wed, 03 Aug 2022 03:28:39 GMT  
		Size: 9.4 KB (9438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24649d01bd9f34f035857fcb9324aef45128d255b0e7d7c9be9d0d9d58a928f3`  
		Last Modified: Wed, 03 Aug 2022 03:28:39 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1-alpine3.16` - linux; arm variant v7

```console
$ docker pull satosa@sha256:9c12b392cb5946a433fe0c98001d362d79a953040068a9d0843c3a9a9c12fb8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163401667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55a50fb783bb28da31c92c6cff33c408ef6ea7e1c6da179086af8ce588f092d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:24:47 GMT
ADD file:68590e866bc6db27ad54d23de7dd275d0389cb86e4e6291a1243fcc234f2f7a1 in / 
# Mon, 18 Jul 2022 21:24:47 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 03:57:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 03:57:44 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 03:57:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 03:57:46 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 07:37:59 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 08:07:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 08:07:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 08:07:50 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 08:07:51 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 13:27:03 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 13:27:03 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 13:30:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 13:30:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 13:30:25 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 13:30:25 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 13:30:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 13:30:25 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 13:30:25 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 13:30:25 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a6b45ace95f42a930d15c33679ab9c85d46019b7e73954cadc73bb9ba176509b`  
		Last Modified: Mon, 18 Jul 2022 19:08:56 GMT  
		Size: 2.4 MB (2412307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d826ef3e3e077607452c51ac5332613cc0a20903abe17b56af4b973f31f0e9b7`  
		Last Modified: Wed, 27 Jul 2022 10:54:47 GMT  
		Size: 664.1 KB (664079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116f12212b7e97cde5b72713f0f3a3025a9ef6dffccdc353cd4d15407d343a72`  
		Last Modified: Wed, 03 Aug 2022 11:22:41 GMT  
		Size: 11.6 MB (11558755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef2affe775c9998dea9fd354aa8d4b6e97117d2092c84f1401265b9f9528bf7`  
		Last Modified: Wed, 03 Aug 2022 11:22:38 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032af4833525c8884057f85c0da98a7f2dedc337784e4ce3645fad79e6633b26`  
		Last Modified: Wed, 03 Aug 2022 11:22:39 GMT  
		Size: 3.0 MB (3043658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65c3d7d841a308ff58960bdd0832a9c2fc9d01d091b4478549cf91ad4551edc`  
		Last Modified: Thu, 04 Aug 2022 13:31:47 GMT  
		Size: 8.0 MB (8026973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553863577a06e5d191ae29abc79bb81603188e34e406ebce36a4e4da49320df8`  
		Last Modified: Thu, 04 Aug 2022 13:31:59 GMT  
		Size: 137.7 MB (137684108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d66d75890a5436b91b581c5023634cbedf248e1dbb622b1241f80c5a4ed29`  
		Last Modified: Thu, 04 Aug 2022 13:31:45 GMT  
		Size: 9.4 KB (9439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cab52b5f6577ce2ac31dd72be231ca9d43531003be80eacfe2f20bbfa5c5d5`  
		Last Modified: Thu, 04 Aug 2022 13:31:46 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:cccb94f4511ba8a1fd8ab69a69f483edef010e4fab16eeccfb637ae5395cdc67
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40930309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83c2e990bd9017e2a1f46423fc6e313b33122d383dda9f8f9c00e8006d36921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:10:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 01:53:04 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 01:53:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 19 Jul 2022 01:53:06 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 09:50:39 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 10:05:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 10:05:10 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 10:05:11 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 10:05:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 10:05:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 10:05:14 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 10:05:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 10:05:22 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 10:40:42 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 10:40:43 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 10:41:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 10:41:33 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 10:41:34 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 10:41:36 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 10:41:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 10:41:37 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 10:41:38 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 10:41:39 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c36086fc9356a3d9879c8427af90dd86ad6fd35b3929bab2af384e98d0571c`  
		Last Modified: Tue, 19 Jul 2022 02:56:56 GMT  
		Size: 668.0 KB (668022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255e9c7248a65c9bb1f14e3ffaf6aad2e14b965bfd9196b30e8c1efc8ddd1747`  
		Last Modified: Wed, 03 Aug 2022 10:34:00 GMT  
		Size: 12.6 MB (12579036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d32815e9cd0f789447579f484cec5ed6ff5b006c50c121a5e314519ffad01d5`  
		Last Modified: Wed, 03 Aug 2022 10:33:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c6e4018f23818adb74c050daeddb28d2efddbabe1135f85ed3ef29b17ec7b`  
		Last Modified: Wed, 03 Aug 2022 10:32:56 GMT  
		Size: 3.0 MB (3045000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2feaf81b71b2f7b13ac6cefc0f434f31221423c1c94002a89138b4c60741ced`  
		Last Modified: Wed, 03 Aug 2022 10:42:41 GMT  
		Size: 8.2 MB (8224897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c9e9ae46115c582ac3a68bb4b583d2ed73875acfb5ff520c5877d481be9cdc`  
		Last Modified: Wed, 03 Aug 2022 10:42:42 GMT  
		Size: 13.7 MB (13706894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e959a5cfce7f6c07db205394594178b791ab1fd7b3425ded77627110666277`  
		Last Modified: Wed, 03 Aug 2022 10:42:40 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143d97f09a0b08aff0f4993e07d50c6a62b1d1c84b442a35f1c8b7f9535005f4`  
		Last Modified: Wed, 03 Aug 2022 10:42:40 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1-alpine3.16` - linux; 386

```console
$ docker pull satosa@sha256:3b7052fea622f5d95da31220bc234a9258ae473482fb55269dea295fd83b4e05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (173023892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712f8d15ddeef960a7327c512f8d03f337021df170d7531f5aa93eafbe51d2c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 21:22:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 21:22:15 GMT
ENV LANG=C.UTF-8
# Tue, 09 Aug 2022 21:22:17 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 09 Aug 2022 21:22:18 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 09 Aug 2022 22:02:59 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 09 Aug 2022 22:16:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 09 Aug 2022 22:16:19 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 09 Aug 2022 22:16:20 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 09 Aug 2022 22:16:21 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 09 Aug 2022 22:16:22 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 09 Aug 2022 22:16:23 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 09 Aug 2022 22:16:31 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 09 Aug 2022 22:16:31 GMT
CMD ["python3"]
# Wed, 10 Aug 2022 03:30:07 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 10 Aug 2022 03:30:08 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 10 Aug 2022 03:33:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 10 Aug 2022 03:33:03 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 10 Aug 2022 03:33:04 GMT
WORKDIR /etc/satosa
# Wed, 10 Aug 2022 03:33:06 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 10 Aug 2022 03:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 03:33:07 GMT
EXPOSE 8080
# Wed, 10 Aug 2022 03:33:08 GMT
USER satosa:satosa
# Wed, 10 Aug 2022 03:33:09 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6e4c463b4b085b81ccd90e5d99d5d5b64a56c2f756e7ff5575080b0efc2e9f`  
		Last Modified: Tue, 09 Aug 2022 23:12:22 GMT  
		Size: 689.1 KB (689070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30e501e19288fafd4b62af6aaf0b588b8da1b9f7bf0ed0bd8c7cf5550131f4b`  
		Last Modified: Tue, 09 Aug 2022 23:13:12 GMT  
		Size: 12.7 MB (12700838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5383c9c382f8845fcf42a8ea747ddb3a99c87e277380a509277f27c6bf8d85`  
		Last Modified: Tue, 09 Aug 2022 23:13:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2450ac53e437f841f48f00e832466a3d7ce73190f3f5255c89dfb89edcd9193`  
		Last Modified: Tue, 09 Aug 2022 23:13:11 GMT  
		Size: 3.0 MB (3045003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3183acab5e336c62f2d06a000d65364d4484e755eb4c01749dd6e443ee703e32`  
		Last Modified: Wed, 10 Aug 2022 03:34:01 GMT  
		Size: 8.5 MB (8512861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350ea1863d968db10b0fe1fd8772d772c84631136d5fb13934b7c5a360cf66fc`  
		Last Modified: Wed, 10 Aug 2022 03:34:28 GMT  
		Size: 145.3 MB (145257262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92895882e21832e6f4d040fa6f60752d36b168dbc7f3893d1fc81a19da18cfc3`  
		Last Modified: Wed, 10 Aug 2022 03:33:59 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85df40b1b491557b15d24c816c82279561fd23244d53603eeea4f9976ce8766`  
		Last Modified: Wed, 10 Aug 2022 03:33:59 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1-alpine3.16` - linux; ppc64le

```console
$ docker pull satosa@sha256:f70b3121c8db732d980c4272ea937145d0745875aba33578b5667bbaf28fb1ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164310759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef00aeaa317867dd9dca82b0661794be10c5d0a082d11a8f76b597b76e88cb55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:29:30 GMT
ADD file:69e4080f15f54e2d8f8aa25fdcba9c01dde149d43592edd5023106675e54a769 in / 
# Mon, 18 Jul 2022 21:29:31 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 04:30:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 04:30:31 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 04:30:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 04:30:33 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 19:40:20 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 20:04:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 20:05:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 20:05:00 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 20:05:00 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 20:05:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 20:05:01 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 20:05:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 20:05:13 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 21:15:12 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 21:15:12 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 21:21:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 21:21:41 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 21:21:41 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 21:21:42 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 21:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 21:21:42 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 21:21:43 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 21:21:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:602896d442490cd3fbb6599f0f862d3673b7cd58eca3ac842b8e09bf8d012443`  
		Last Modified: Mon, 18 Jul 2022 19:09:09 GMT  
		Size: 2.8 MB (2789923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6556a4bf6509d5fd24900f56a6175bd811b9dd8c6f4f51e2732b6888a2b8933`  
		Last Modified: Wed, 27 Jul 2022 13:49:16 GMT  
		Size: 677.0 KB (676971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c735731e55a5ddb324dd5eb175e1f3d88895a77ea93b8fb08428ee522445708b`  
		Last Modified: Wed, 03 Aug 2022 20:44:16 GMT  
		Size: 12.8 MB (12819587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e525d9b2b00fc7130f21f05f981c44d849b279417c15b38703c3f11d3c9bd667`  
		Last Modified: Wed, 03 Aug 2022 20:44:13 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9bc880d40f528e2c6046dd7bad61fc78f27a3fbebe3f45d1348a72ace67d9b`  
		Last Modified: Wed, 03 Aug 2022 20:44:15 GMT  
		Size: 3.0 MB (3043656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b74e25b6a705707a07e0411366545458ad05f07844bde5b7bebddd988e69068`  
		Last Modified: Wed, 03 Aug 2022 21:23:08 GMT  
		Size: 8.5 MB (8476895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141bd7d880682fd816129f41549c798cabb9e94494f7ee7714d6e83e63606b82`  
		Last Modified: Wed, 03 Aug 2022 21:23:23 GMT  
		Size: 136.5 MB (136491944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b412f1d24946cb1e7f3d66a4ae5595d3b71ae6040af529dc49507cb1dd4e06c`  
		Last Modified: Wed, 03 Aug 2022 21:23:06 GMT  
		Size: 9.4 KB (9434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8aa237953d155695df1943bb27b03cf1cc3f1716ea63b1cf5a8b12d97cd6cea`  
		Last Modified: Wed, 03 Aug 2022 21:23:06 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.1.1-bullseye`

```console
$ docker pull satosa@sha256:b952f0d280486a79665537c956718dec4fff75e9e6a343a79e1048bc3bf3c861
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

### `satosa:8.1.1-bullseye` - linux; amd64

```console
$ docker pull satosa@sha256:3d92574bf94e0395a41762efa378d221f605ea12bea73ae604c71310fe6036fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82653895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d245b28169a1e1f7dd888fa2381fc3aa02a91b2210f7b6b481c4016173ac8d0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 09:39:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 09:39:09 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 09:39:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 09:39:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 10:15:41 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 10:26:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 10:26:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 10:26:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 10:26:31 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 11:46:24 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 11:46:24 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 11:47:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 11:47:19 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 11:47:19 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 11:47:19 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 11:47:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 11:47:20 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 11:47:20 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 11:47:20 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126aaa6587b8608b62fa39019a891e98460e23bad2d04fb235c4dc8fae2adf3c`  
		Last Modified: Tue, 02 Aug 2022 12:33:29 GMT  
		Size: 1.1 MB (1076278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd06b55ca686f29b26c8a7e051ce98ad571fd6cf22bba07f5cd17e98fd31e13`  
		Last Modified: Wed, 03 Aug 2022 11:18:36 GMT  
		Size: 12.1 MB (12106838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3950cece0b727ab257c49317871d00f22d2abcb77bcce19ddf86aab5c4d88e21`  
		Last Modified: Wed, 03 Aug 2022 11:18:34 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e27c1167cc2a09e30e53c0fd2933e189e20b4785284e84a919fe5fd3013388b`  
		Last Modified: Wed, 03 Aug 2022 11:18:35 GMT  
		Size: 3.3 MB (3336043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb69b4e4539d59ea0fbed39563b5042d023cd4713d9a38bde6b930fb548e8b9a`  
		Last Modified: Wed, 03 Aug 2022 11:48:44 GMT  
		Size: 19.6 MB (19587061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620aa9bb44333fe5af9257a47e9e0de0e7a0596721959465531442e2b753aa5a`  
		Last Modified: Wed, 03 Aug 2022 11:48:44 GMT  
		Size: 15.2 MB (15169129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffc5c41689ca0d4f9b9e1beea0953f2bec48e3ab6becfee1b8c8862100aadbe`  
		Last Modified: Wed, 03 Aug 2022 11:48:41 GMT  
		Size: 9.4 KB (9443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebafed1e50948cce1a8ec458a2dbc933ec93924419791a83613e224356054ee`  
		Last Modified: Wed, 03 Aug 2022 11:48:41 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1-bullseye` - linux; arm variant v5

```console
$ docker pull satosa@sha256:e4ee7d4d43b26f8dc6b5a7d8358af5463aa5ebf830249e6272afbe2a819e9732
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.7 MB (203698783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160cc52ce9b78d794b4acbd3286cc62c771bad645eb50e8c9af6722d743f166c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:10 GMT
ADD file:4cd2f95737fd3007912428eeac56036c9e67e989e66cec08a8be99da47f88494 in / 
# Tue, 02 Aug 2022 00:49:10 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:38:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 20:38:12 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 20:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:38:23 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 22:45:24 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 23:08:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 23:08:11 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 23:08:11 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 23:08:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 23:08:30 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 19:10:52 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 19:10:52 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 19:17:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 19:17:42 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 19:17:42 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 19:17:43 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 19:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 19:17:43 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 19:17:43 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 19:17:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5890b0ca6af5e8467a488e68716691950496a8f247d0495c2d595ddcb1893aff`  
		Last Modified: Tue, 02 Aug 2022 00:56:06 GMT  
		Size: 28.9 MB (28905515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eafe902d3c868e979e01e5c5aca6567b8be8b60814b9e1ce93c2b749451b410`  
		Last Modified: Wed, 03 Aug 2022 02:16:47 GMT  
		Size: 1.1 MB (1059641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e073b0922c53e3aee167b94b195f01b7740c95a691b391e30bbc1dd36133f578`  
		Last Modified: Wed, 03 Aug 2022 02:18:15 GMT  
		Size: 11.7 MB (11687058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1563deb88ac81fbc07f66164de09058989bc2f52e4b201209996fc610e7424`  
		Last Modified: Wed, 03 Aug 2022 02:18:11 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9586a9ae76d2fcf29975a3cbac30868417a5e7209b4d681ab4d8cdc9417e1127`  
		Last Modified: Wed, 03 Aug 2022 02:18:13 GMT  
		Size: 3.3 MB (3335517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2138d4d7c7c422781a7da5bbba917dfee3de2e44c0b89e2c05cd5fb54d6aec`  
		Last Modified: Wed, 03 Aug 2022 19:18:28 GMT  
		Size: 21.2 MB (21220513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ec77684813e78ff3c43e62e86fde2b1964089fb2e02c36be1b197e18d76199`  
		Last Modified: Wed, 03 Aug 2022 19:18:38 GMT  
		Size: 137.5 MB (137478750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecfeff163b4d6f23860d774bf123b6ad13105fce4fa35bddd9e46a56b0c09af`  
		Last Modified: Wed, 03 Aug 2022 19:18:21 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb3f6f2ab2014dd8287001b208c1dc97200c2c3e16a2cb980fd938dfd82858b`  
		Last Modified: Wed, 03 Aug 2022 19:18:22 GMT  
		Size: 2.1 KB (2111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1-bullseye` - linux; arm variant v7

```console
$ docker pull satosa@sha256:1eb7ef57547ada8079868ad16a792df4e4cbc8571c4b2beb50d5682d1bc6250f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202351243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194a9b56fc0cc44a0542e47df53c65db1e4f7a579b5a8624e2b202e21462c73d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:58:59 GMT
ADD file:1575b776a15adacebc0875642e97a80807d42dcfc8917e1406d47af7ac244c97 in / 
# Tue, 02 Aug 2022 00:58:59 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:34:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 04:34:22 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 04:34:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 04:34:30 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 06:30:14 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 06:52:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 06:52:09 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 06:52:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 06:52:24 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 13:20:49 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 13:20:50 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 13:26:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 13:26:45 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 13:26:45 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 13:26:45 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 13:26:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 13:26:45 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 13:26:45 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 13:26:45 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1dd75a3a9c893a7dc313f683dd62464b7eab6c6d522ee62c8a17022631830f32`  
		Last Modified: Tue, 02 Aug 2022 01:06:45 GMT  
		Size: 26.6 MB (26560586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4206fea8c3d0ae09213fad25e06bb550a03c76c2b15e7a3c134ee5e2d217cd`  
		Last Modified: Wed, 03 Aug 2022 11:19:22 GMT  
		Size: 1.0 MB (1041632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed9dda465ec974f3e81b6b5f48dee0c43b63aeae625042e1e5f8ca482d43f1f`  
		Last Modified: Wed, 03 Aug 2022 11:21:19 GMT  
		Size: 11.2 MB (11205345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c669588520ce26d52819574b6ac8f40bc121ec539aae49c4cdc6aa899fcea`  
		Last Modified: Wed, 03 Aug 2022 11:21:15 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75c71e6575f11c76771634448c2e1c7e6988853591c1422d979aaf3dfa73569`  
		Last Modified: Wed, 03 Aug 2022 11:21:17 GMT  
		Size: 3.3 MB (3335656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d5ac04f9c39c2ba1d884f419e586ede32f2779ea0bbb6a7033e0f70c79d670`  
		Last Modified: Thu, 04 Aug 2022 13:31:15 GMT  
		Size: 20.9 MB (20949533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65844885dbff2fac2bccf9e5a7b69d9c423352d19d5ffb5eeca720f5e2a10886`  
		Last Modified: Thu, 04 Aug 2022 13:31:26 GMT  
		Size: 139.2 MB (139246702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53ebddc2eb90a987a1bae1b3a245f2d88ae7ea81a35f85f6bfdf10891217d58`  
		Last Modified: Thu, 04 Aug 2022 13:31:10 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa39e50e9a3812f026202131476b98a06e4a65a16a21fee180aeb54d979e2cb8`  
		Last Modified: Thu, 04 Aug 2022 13:31:10 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1-bullseye` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:8a7bc186f7c0a8725b284d01a4dceac8636d5f7f96b11f0d4031fd66f199e2b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79849083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56454aaf2924873a1f55890e93e1c83261d4047ce84a080d73750691435b3d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:03:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 12:03:30 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 12:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:03:36 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 09:19:10 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 09:29:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 09:29:22 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 09:29:22 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 09:29:23 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 09:29:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 09:29:25 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 09:29:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 09:29:37 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 10:39:28 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 10:39:28 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 10:40:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 10:40:15 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 10:40:16 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 10:40:18 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 10:40:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 10:40:19 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 10:40:20 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 10:40:21 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f101f90cc8f7640b7db5f7094941a1fe4ff28e11a968d3a36f146a89a480ecbb`  
		Last Modified: Tue, 02 Aug 2022 14:47:06 GMT  
		Size: 1.1 MB (1063812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a5d6cf27653f158e4f7552f31dc146332b6d820679ee42ebff5b4e47f4dac`  
		Last Modified: Wed, 03 Aug 2022 10:31:15 GMT  
		Size: 12.2 MB (12153733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd415bdc2c72c852623e384c90826d41aa2739adbc3158bd814bc3e562ab16ea`  
		Last Modified: Wed, 03 Aug 2022 10:31:13 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90ceb316b2d011719d35fb58a5d69ec1b84ebc6a9ab5568354ca370aad48524`  
		Last Modified: Wed, 03 Aug 2022 10:31:14 GMT  
		Size: 3.1 MB (3119919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7a23c6e6d4ea56699e3033f9fd616c6fa79290a257066f21578bf773f283cb`  
		Last Modified: Wed, 03 Aug 2022 10:42:23 GMT  
		Size: 19.3 MB (19324710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f64adba6c540f9f4fde33df9a99fa32be543c937e20b203b409ba3340f7b62`  
		Last Modified: Wed, 03 Aug 2022 10:42:23 GMT  
		Size: 14.1 MB (14120866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9df97e7203d91c6109257b6e98c0bb926732214ee96a7110c86550f8c271b74`  
		Last Modified: Wed, 03 Aug 2022 10:42:20 GMT  
		Size: 9.4 KB (9394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d56269ee4307b5c76ba7efef9346008e1440979b95ee777b9d5e8e3e4ead5b1`  
		Last Modified: Wed, 03 Aug 2022 10:42:20 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1-bullseye` - linux; 386

```console
$ docker pull satosa@sha256:ff2180ab006e1d173a6d157a2ef8b05c4abae7d45d5693889e12f05e6861a42d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207396057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b9632c4df58a4c5e3e68e82bf8bab7462b2530f9ecfb108feb8726a85ab4d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:39:20 GMT
ADD file:f771e2286465694126158821089d801c7296376be2a56189e6041a15d2fe79f5 in / 
# Tue, 02 Aug 2022 00:39:21 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 11:22:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 11:22:53 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 11:22:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 11:22:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 20:51:53 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 21:03:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 21:03:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 21:03:55 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 21:03:56 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 21:03:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 21:03:58 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 21:04:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 21:04:12 GMT
CMD ["python3"]
# Tue, 02 Aug 2022 22:21:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 02 Aug 2022 22:21:44 GMT
ENV SATOSA_VERSION=8.1.1
# Tue, 02 Aug 2022 23:39:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 02 Aug 2022 23:39:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 02 Aug 2022 23:39:26 GMT
WORKDIR /etc/satosa
# Tue, 02 Aug 2022 23:39:28 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Tue, 02 Aug 2022 23:39:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 23:39:29 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 23:39:30 GMT
USER satosa:satosa
# Tue, 02 Aug 2022 23:39:31 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:90eb7f0ce9f33cf5dcd67d54c2fa606186dbaa5f95b6046f36145097267f9e53`  
		Last Modified: Tue, 02 Aug 2022 00:45:14 GMT  
		Size: 32.4 MB (32374054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd27ead98f25cd891e8dfae23b5500c856f3a9db336a545eed8b5f180a6df0b4`  
		Last Modified: Tue, 02 Aug 2022 14:37:54 GMT  
		Size: 1.1 MB (1088442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7362ecffe5fefdfcff89188358cb648fae40c1fed6254cd3325ef1c340a0ca9b`  
		Last Modified: Tue, 02 Aug 2022 22:15:01 GMT  
		Size: 12.2 MB (12224818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fb82e70fda9a811619f0b6cfd165d59473bcc467e702a70231630e64335b18`  
		Last Modified: Tue, 02 Aug 2022 22:14:59 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab067ab28a29ee91955ebd00b4849cd1d1993a430051ce801b5eaffeeb59b976`  
		Last Modified: Tue, 02 Aug 2022 22:15:00 GMT  
		Size: 3.1 MB (3119814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c68c7fda4b282e37efe94863aed2872d62133ead0fed4a4b4174eab16a125f`  
		Last Modified: Tue, 02 Aug 2022 23:40:27 GMT  
		Size: 22.6 MB (22586591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4630af60cc9f0637de40da0789c8be2b49091d860ae7f21753e736c5a24b0fac`  
		Last Modified: Tue, 02 Aug 2022 23:40:44 GMT  
		Size: 136.0 MB (135990599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ba92ddedaf8e60d74aac7773867aec0a84b2812ba92a5742090bee107e7736`  
		Last Modified: Tue, 02 Aug 2022 23:40:24 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e28ea4f42ac6baac91e14de0ee8d101956ac6d64c7d4078bb57ebfddde33184`  
		Last Modified: Tue, 02 Aug 2022 23:40:24 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1-bullseye` - linux; mips64le

```console
$ docker pull satosa@sha256:b9bdbc69a8a0be593fe150cbd4334f006447c17a9538b850002e7fa96445593b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.8 MB (205844024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7d3830a289e7a92a0277b60e6cce741d4887ea889e4e236cdd2d878fb1f64b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:10:34 GMT
ADD file:6dc22a1e5b5fcf23f2549406ddcc45c4e244f46e21eafa881de81fa87438e5d8 in / 
# Tue, 02 Aug 2022 01:10:38 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 10:25:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 10:25:08 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 10:25:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:25:36 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 04 Aug 2022 04:16:09 GMT
ENV PYTHON_VERSION=3.10.6
# Thu, 04 Aug 2022 05:33:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Thu, 04 Aug 2022 05:33:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 04 Aug 2022 05:33:27 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Thu, 04 Aug 2022 05:33:30 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Thu, 04 Aug 2022 05:33:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Thu, 04 Aug 2022 05:33:35 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Thu, 04 Aug 2022 05:34:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 04 Aug 2022 05:34:30 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 08:35:12 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 08:35:15 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 08:52:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 08:52:17 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 08:52:21 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 08:52:25 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 08:52:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 08:52:34 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 08:52:39 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 08:52:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:88350749a27614c791450c256b051f023d81cdd256211274b1efac493779d2be`  
		Last Modified: Tue, 02 Aug 2022 01:21:02 GMT  
		Size: 29.6 MB (29628964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61130d003a0ea87819935a3a252db1861d9b87e1313fa7988d5f0642637f3e`  
		Last Modified: Tue, 02 Aug 2022 23:46:40 GMT  
		Size: 1.0 MB (1049605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e786491697e5d2bd3dee622f7eae98810c04c895d5024e910e2394f92b37ad8`  
		Last Modified: Thu, 04 Aug 2022 08:14:51 GMT  
		Size: 12.1 MB (12124464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fb1366c066d6bf94df2bf081524439083c14a1f292da85f218000ac515a2f5`  
		Last Modified: Thu, 04 Aug 2022 08:14:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe7637d1173b353af8622199dfbc92d0f74f8cff129fe540541b9c069a058d3`  
		Last Modified: Thu, 04 Aug 2022 08:14:46 GMT  
		Size: 3.1 MB (3120804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4655831cce551d936028a78d3d4a295cd96e3ca02ea0f5f726d0b963350a0e`  
		Last Modified: Thu, 04 Aug 2022 08:53:18 GMT  
		Size: 21.3 MB (21288233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54965dd4effca16f75a92cdac5dd71e708a50d218ca30b0806964a58d8b726ee`  
		Last Modified: Thu, 04 Aug 2022 08:53:58 GMT  
		Size: 138.6 MB (138620211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a449c61594c6b3d2e0fa03d876ebe6fc8561eaa1d46ebf088772a42dea52b596`  
		Last Modified: Thu, 04 Aug 2022 08:53:06 GMT  
		Size: 9.4 KB (9396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54e620f3a05fe34c293ac1de03899ec567f49faa21a8db43216f796387f8f65`  
		Last Modified: Thu, 04 Aug 2022 08:53:06 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1-bullseye` - linux; ppc64le

```console
$ docker pull satosa@sha256:b84ad93ccca31f2ba03b7c0586ad9f3a2d71764d4338922af798ae737ec87f23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212244381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f29a99f45c08fb90c8ad9dec84fd55c14d0ca8ecbc00c2160fc3464a14feca9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:17:30 GMT
ADD file:3a95a896d463569ce82199957052b3467123a4bd3385a0a4e397cf08402a99c3 in / 
# Tue, 02 Aug 2022 01:17:32 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:03:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 16:03:13 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 16:03:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 16:03:24 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 18:10:29 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 18:43:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 18:43:03 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 18:43:03 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 18:43:03 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 18:43:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 18:43:04 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 18:43:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 18:43:25 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 21:09:20 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 21:09:21 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 21:14:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 21:14:39 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 21:14:39 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 21:14:40 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 21:14:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 21:14:41 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 21:14:41 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 21:14:42 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5241cd116d6e6e2d62f3d8c2245b74daca9f6cc154eaccd738feb41984c74714`  
		Last Modified: Tue, 02 Aug 2022 01:24:39 GMT  
		Size: 35.3 MB (35272771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf6dcfcb4fa2f4e24ce6bed8b3eda6b0d49d92062cb34d95830e4e9f512270`  
		Last Modified: Wed, 03 Aug 2022 00:14:29 GMT  
		Size: 1.1 MB (1094658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdc50327f93cca5ad2c5f8500471040045b715045a9a4852ece90b3155d5aea`  
		Last Modified: Wed, 03 Aug 2022 20:42:55 GMT  
		Size: 12.5 MB (12473465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49f3fdf44cc1cf9b0e2d32c8ea2b62a0d3eb7eac481b56c9d11e44c66b764fe`  
		Last Modified: Wed, 03 Aug 2022 20:42:52 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd9d6c8cb5530b56f02a736bb1cc24d2d0ffc11d6fb55dc6befb0e114a1ff74`  
		Last Modified: Wed, 03 Aug 2022 20:42:53 GMT  
		Size: 3.3 MB (3336216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209342dd334b280e74196c0e693487033f7f2d08880ab61f5f9113dbbd5d0461`  
		Last Modified: Wed, 03 Aug 2022 21:22:32 GMT  
		Size: 22.2 MB (22158681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11809242e6bd5adbd0096d37646b954f666a1e2a107dd5442773977caa919360`  
		Last Modified: Wed, 03 Aug 2022 21:22:45 GMT  
		Size: 137.9 MB (137896801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa36501b6a1d8ec2e51a6a162f1f43d70ea4b035335513b65b800346790717`  
		Last Modified: Wed, 03 Aug 2022 21:22:27 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fe38c0944e97231334e780f32f3cd041644756c5b195812b19edd697268021`  
		Last Modified: Wed, 03 Aug 2022 21:22:27 GMT  
		Size: 2.1 KB (2113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.1.1-bullseye` - linux; s390x

```console
$ docker pull satosa@sha256:f52b8375aeb8b39ad8ae5b9f05f4f94a47f4776b3f500aeeadee19c4ed572f5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202163420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f253b8b35e8bbaf69f23beb8a8584dc48a0c682127faa17ed9d639b33dfdf3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 08:30:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 08:30:40 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 08:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 08:30:44 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 22:09:42 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 22:18:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 22:18:03 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 22:18:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 22:18:13 GMT
CMD ["python3"]
# Tue, 02 Aug 2022 23:28:28 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 02 Aug 2022 23:28:31 GMT
ENV SATOSA_VERSION=8.1.1
# Tue, 02 Aug 2022 23:32:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 02 Aug 2022 23:33:02 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 02 Aug 2022 23:33:02 GMT
WORKDIR /etc/satosa
# Tue, 02 Aug 2022 23:33:02 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Tue, 02 Aug 2022 23:33:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 23:33:02 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 23:33:03 GMT
USER satosa:satosa
# Tue, 02 Aug 2022 23:33:03 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c36d12a9d2aa3bd2ed5880b10e768bae6cab779992e198cf595d3b8d6924d5`  
		Last Modified: Tue, 02 Aug 2022 10:43:27 GMT  
		Size: 1.1 MB (1075771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a2fa2a5f3f4be291fac87451996292e32ad4b6b7e7ae168c720b6501ba676f`  
		Last Modified: Tue, 02 Aug 2022 23:23:49 GMT  
		Size: 11.9 MB (11900903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1958402e81da32fc50ee2b3d3d48a5714015a6589a9b0882e2e0862173874f52`  
		Last Modified: Tue, 02 Aug 2022 23:23:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adc16df778c23094a004c62669c6de553142901db4933d76959d223598473b`  
		Last Modified: Tue, 02 Aug 2022 23:23:49 GMT  
		Size: 3.3 MB (3335624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5f479e9444a18e7100a74300ba30ab5818c9023c386c0a537811de457f1e99`  
		Last Modified: Tue, 02 Aug 2022 23:33:39 GMT  
		Size: 19.6 MB (19580744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573792100821147cd9e469e566ed70175d1fe8ec2b68e371484abc92f0aeaf74`  
		Last Modified: Tue, 02 Aug 2022 23:33:45 GMT  
		Size: 136.6 MB (136618328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cb6a07895307e25b49bb3cdebc3f6e29fef231b0390c00ddacc6b74ee5f9fd`  
		Last Modified: Tue, 02 Aug 2022 23:33:36 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0ce3aebbe275e54928297909f6f1ed7c7beee5c901706ccef91eec96eb8bc5`  
		Last Modified: Tue, 02 Aug 2022 23:33:36 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:alpine`

```console
$ docker pull satosa@sha256:fa00b0ab420886685085b244405746ecce141ff81c408876a6d8c17f5e0960ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `satosa:alpine` - linux; amd64

```console
$ docker pull satosa@sha256:889e8b702bc04ca43d059bdf24c8db677954c87e5318ba8a93d795e450d485dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42508179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa3cc16430e95981e37a39687b5b6a8e23b8adf5eb81881cab4136b31de9b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:14:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 02:01:52 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 02:01:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 19 Jul 2022 02:01:54 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 10:48:21 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 11:00:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 11:00:14 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 11:00:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 11:00:21 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 11:47:34 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 11:47:34 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 11:48:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 11:48:18 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 11:48:19 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 11:48:19 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 11:48:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 11:48:19 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 11:48:19 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 11:48:19 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c14b1a767335de44f2bc926cb52487979a0fe602ac5429643dbb238f297fb`  
		Last Modified: Tue, 19 Jul 2022 02:56:13 GMT  
		Size: 666.8 KB (666769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571274b8543b548747b5e9bef700a89692fe9403cc364be8d6e8a0792ccfe2b4`  
		Last Modified: Wed, 03 Aug 2022 11:19:35 GMT  
		Size: 12.5 MB (12508608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f79a08255af5d614c7b4b81e358b5bb607bdcb14a6475c836d3d4f92f094846`  
		Last Modified: Wed, 03 Aug 2022 11:19:34 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6b20e3f6abd46292c29437a6917dc82b769ebb239e2d971aedb6695e057715`  
		Last Modified: Wed, 03 Aug 2022 11:19:34 GMT  
		Size: 3.0 MB (3043671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c974d4972d870a99bf0fba525cab86b298dd6e9405d3329a3495a164ae5c7`  
		Last Modified: Wed, 03 Aug 2022 11:49:00 GMT  
		Size: 9.4 MB (9398243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c482d554455c83821852ea2cd26eaf97f49bb1c7983342cec7242b8ea5432234`  
		Last Modified: Wed, 03 Aug 2022 11:49:01 GMT  
		Size: 14.1 MB (14080297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b861965b84abb04a92b63eb19a620daf7360785f485bc2d526885601454b19ca`  
		Last Modified: Wed, 03 Aug 2022 11:48:58 GMT  
		Size: 9.4 KB (9439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16e011f2d9efad78d03ac0d4c7abe2f694dfc5f6c158ef9fa350a3f21d22a8e`  
		Last Modified: Wed, 03 Aug 2022 11:48:58 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine` - linux; arm variant v6

```console
$ docker pull satosa@sha256:1ed78492e93849ebbee5cd80dd5e4a91eb2a41676fbc3d21584a17d402028ca7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160179359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e822b6bb9258ee22b55f2f03c3d389710a39d0a3fa1d10f1250cb00db2f3e268`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 19:49:37 GMT
ADD file:7a20333469e71664904a0cb8f61613250f2bd092b4a27bfa7bbae1dc7e21b7ed in / 
# Mon, 18 Jul 2022 19:49:37 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 00:30:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 00:30:05 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 00:30:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 00:30:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 19:50:04 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 20:30:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 02 Aug 2022 20:30:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 20:30:20 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 20:30:20 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 03:20:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 03:20:45 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 03:27:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 03:27:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 03:27:54 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 03:27:54 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 03:27:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 03:27:55 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 03:27:55 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 03:27:55 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b7885075fcd06a866d12dfd56eb704045eaadbd22dc03a224cd98715be566677`  
		Last Modified: Mon, 18 Jul 2022 19:08:42 GMT  
		Size: 2.6 MB (2606431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ebe8e3a2f83d0ddc301c9b9d6405376eecb906b92082e05d5e257eff5f6293`  
		Last Modified: Wed, 27 Jul 2022 11:08:23 GMT  
		Size: 672.3 KB (672287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b647934af90a736595f675559fd3aebbcdbcfc67277de68401980916f3c217d7`  
		Last Modified: Wed, 03 Aug 2022 00:13:17 GMT  
		Size: 12.1 MB (12085055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaef313095ff837d4848dec2c5e458a33e59ee4e1ab7a9d4e3d244d20b92fbf`  
		Last Modified: Wed, 03 Aug 2022 00:13:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba453d098c35b58faf7cc2ac6a90a0e9a8941dc90611ee397d12af0a546bbe87`  
		Last Modified: Wed, 03 Aug 2022 00:13:15 GMT  
		Size: 3.0 MB (3043708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0a90158473abc47e6b9744b5cc61265a9552ba9217486241f5b7b4a5d12eec`  
		Last Modified: Wed, 03 Aug 2022 03:28:44 GMT  
		Size: 8.3 MB (8280231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a82dd9e01f89340501ac0415caccc1ad608cc08d55219cb26db2226dc64b83`  
		Last Modified: Wed, 03 Aug 2022 03:29:07 GMT  
		Size: 133.5 MB (133479861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ee2ba314aef7361329abd7eaa7a8860079655317f4d5fc9d37f73f8b34de4`  
		Last Modified: Wed, 03 Aug 2022 03:28:39 GMT  
		Size: 9.4 KB (9438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24649d01bd9f34f035857fcb9324aef45128d255b0e7d7c9be9d0d9d58a928f3`  
		Last Modified: Wed, 03 Aug 2022 03:28:39 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine` - linux; arm variant v7

```console
$ docker pull satosa@sha256:9c12b392cb5946a433fe0c98001d362d79a953040068a9d0843c3a9a9c12fb8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163401667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55a50fb783bb28da31c92c6cff33c408ef6ea7e1c6da179086af8ce588f092d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:24:47 GMT
ADD file:68590e866bc6db27ad54d23de7dd275d0389cb86e4e6291a1243fcc234f2f7a1 in / 
# Mon, 18 Jul 2022 21:24:47 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 03:57:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 03:57:44 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 03:57:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 03:57:46 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 07:37:59 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 08:07:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 08:07:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 08:07:50 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 08:07:51 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 13:27:03 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 13:27:03 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 13:30:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 13:30:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 13:30:25 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 13:30:25 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 13:30:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 13:30:25 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 13:30:25 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 13:30:25 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a6b45ace95f42a930d15c33679ab9c85d46019b7e73954cadc73bb9ba176509b`  
		Last Modified: Mon, 18 Jul 2022 19:08:56 GMT  
		Size: 2.4 MB (2412307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d826ef3e3e077607452c51ac5332613cc0a20903abe17b56af4b973f31f0e9b7`  
		Last Modified: Wed, 27 Jul 2022 10:54:47 GMT  
		Size: 664.1 KB (664079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116f12212b7e97cde5b72713f0f3a3025a9ef6dffccdc353cd4d15407d343a72`  
		Last Modified: Wed, 03 Aug 2022 11:22:41 GMT  
		Size: 11.6 MB (11558755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef2affe775c9998dea9fd354aa8d4b6e97117d2092c84f1401265b9f9528bf7`  
		Last Modified: Wed, 03 Aug 2022 11:22:38 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032af4833525c8884057f85c0da98a7f2dedc337784e4ce3645fad79e6633b26`  
		Last Modified: Wed, 03 Aug 2022 11:22:39 GMT  
		Size: 3.0 MB (3043658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65c3d7d841a308ff58960bdd0832a9c2fc9d01d091b4478549cf91ad4551edc`  
		Last Modified: Thu, 04 Aug 2022 13:31:47 GMT  
		Size: 8.0 MB (8026973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553863577a06e5d191ae29abc79bb81603188e34e406ebce36a4e4da49320df8`  
		Last Modified: Thu, 04 Aug 2022 13:31:59 GMT  
		Size: 137.7 MB (137684108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d66d75890a5436b91b581c5023634cbedf248e1dbb622b1241f80c5a4ed29`  
		Last Modified: Thu, 04 Aug 2022 13:31:45 GMT  
		Size: 9.4 KB (9439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cab52b5f6577ce2ac31dd72be231ca9d43531003be80eacfe2f20bbfa5c5d5`  
		Last Modified: Thu, 04 Aug 2022 13:31:46 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:cccb94f4511ba8a1fd8ab69a69f483edef010e4fab16eeccfb637ae5395cdc67
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40930309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83c2e990bd9017e2a1f46423fc6e313b33122d383dda9f8f9c00e8006d36921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:10:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 01:53:04 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 01:53:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 19 Jul 2022 01:53:06 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 09:50:39 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 10:05:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 10:05:10 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 10:05:11 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 10:05:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 10:05:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 10:05:14 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 10:05:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 10:05:22 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 10:40:42 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 10:40:43 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 10:41:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 10:41:33 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 10:41:34 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 10:41:36 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 10:41:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 10:41:37 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 10:41:38 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 10:41:39 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c36086fc9356a3d9879c8427af90dd86ad6fd35b3929bab2af384e98d0571c`  
		Last Modified: Tue, 19 Jul 2022 02:56:56 GMT  
		Size: 668.0 KB (668022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255e9c7248a65c9bb1f14e3ffaf6aad2e14b965bfd9196b30e8c1efc8ddd1747`  
		Last Modified: Wed, 03 Aug 2022 10:34:00 GMT  
		Size: 12.6 MB (12579036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d32815e9cd0f789447579f484cec5ed6ff5b006c50c121a5e314519ffad01d5`  
		Last Modified: Wed, 03 Aug 2022 10:33:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c6e4018f23818adb74c050daeddb28d2efddbabe1135f85ed3ef29b17ec7b`  
		Last Modified: Wed, 03 Aug 2022 10:32:56 GMT  
		Size: 3.0 MB (3045000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2feaf81b71b2f7b13ac6cefc0f434f31221423c1c94002a89138b4c60741ced`  
		Last Modified: Wed, 03 Aug 2022 10:42:41 GMT  
		Size: 8.2 MB (8224897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c9e9ae46115c582ac3a68bb4b583d2ed73875acfb5ff520c5877d481be9cdc`  
		Last Modified: Wed, 03 Aug 2022 10:42:42 GMT  
		Size: 13.7 MB (13706894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e959a5cfce7f6c07db205394594178b791ab1fd7b3425ded77627110666277`  
		Last Modified: Wed, 03 Aug 2022 10:42:40 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143d97f09a0b08aff0f4993e07d50c6a62b1d1c84b442a35f1c8b7f9535005f4`  
		Last Modified: Wed, 03 Aug 2022 10:42:40 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine` - linux; 386

```console
$ docker pull satosa@sha256:3b7052fea622f5d95da31220bc234a9258ae473482fb55269dea295fd83b4e05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (173023892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712f8d15ddeef960a7327c512f8d03f337021df170d7531f5aa93eafbe51d2c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 21:22:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 21:22:15 GMT
ENV LANG=C.UTF-8
# Tue, 09 Aug 2022 21:22:17 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 09 Aug 2022 21:22:18 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 09 Aug 2022 22:02:59 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 09 Aug 2022 22:16:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 09 Aug 2022 22:16:19 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 09 Aug 2022 22:16:20 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 09 Aug 2022 22:16:21 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 09 Aug 2022 22:16:22 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 09 Aug 2022 22:16:23 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 09 Aug 2022 22:16:31 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 09 Aug 2022 22:16:31 GMT
CMD ["python3"]
# Wed, 10 Aug 2022 03:30:07 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 10 Aug 2022 03:30:08 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 10 Aug 2022 03:33:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 10 Aug 2022 03:33:03 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 10 Aug 2022 03:33:04 GMT
WORKDIR /etc/satosa
# Wed, 10 Aug 2022 03:33:06 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 10 Aug 2022 03:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 03:33:07 GMT
EXPOSE 8080
# Wed, 10 Aug 2022 03:33:08 GMT
USER satosa:satosa
# Wed, 10 Aug 2022 03:33:09 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6e4c463b4b085b81ccd90e5d99d5d5b64a56c2f756e7ff5575080b0efc2e9f`  
		Last Modified: Tue, 09 Aug 2022 23:12:22 GMT  
		Size: 689.1 KB (689070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30e501e19288fafd4b62af6aaf0b588b8da1b9f7bf0ed0bd8c7cf5550131f4b`  
		Last Modified: Tue, 09 Aug 2022 23:13:12 GMT  
		Size: 12.7 MB (12700838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5383c9c382f8845fcf42a8ea747ddb3a99c87e277380a509277f27c6bf8d85`  
		Last Modified: Tue, 09 Aug 2022 23:13:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2450ac53e437f841f48f00e832466a3d7ce73190f3f5255c89dfb89edcd9193`  
		Last Modified: Tue, 09 Aug 2022 23:13:11 GMT  
		Size: 3.0 MB (3045003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3183acab5e336c62f2d06a000d65364d4484e755eb4c01749dd6e443ee703e32`  
		Last Modified: Wed, 10 Aug 2022 03:34:01 GMT  
		Size: 8.5 MB (8512861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350ea1863d968db10b0fe1fd8772d772c84631136d5fb13934b7c5a360cf66fc`  
		Last Modified: Wed, 10 Aug 2022 03:34:28 GMT  
		Size: 145.3 MB (145257262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92895882e21832e6f4d040fa6f60752d36b168dbc7f3893d1fc81a19da18cfc3`  
		Last Modified: Wed, 10 Aug 2022 03:33:59 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85df40b1b491557b15d24c816c82279561fd23244d53603eeea4f9976ce8766`  
		Last Modified: Wed, 10 Aug 2022 03:33:59 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine` - linux; ppc64le

```console
$ docker pull satosa@sha256:f70b3121c8db732d980c4272ea937145d0745875aba33578b5667bbaf28fb1ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164310759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef00aeaa317867dd9dca82b0661794be10c5d0a082d11a8f76b597b76e88cb55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:29:30 GMT
ADD file:69e4080f15f54e2d8f8aa25fdcba9c01dde149d43592edd5023106675e54a769 in / 
# Mon, 18 Jul 2022 21:29:31 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 04:30:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 04:30:31 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 04:30:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 04:30:33 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 19:40:20 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 20:04:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 20:05:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 20:05:00 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 20:05:00 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 20:05:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 20:05:01 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 20:05:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 20:05:13 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 21:15:12 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 21:15:12 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 21:21:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 21:21:41 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 21:21:41 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 21:21:42 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 21:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 21:21:42 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 21:21:43 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 21:21:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:602896d442490cd3fbb6599f0f862d3673b7cd58eca3ac842b8e09bf8d012443`  
		Last Modified: Mon, 18 Jul 2022 19:09:09 GMT  
		Size: 2.8 MB (2789923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6556a4bf6509d5fd24900f56a6175bd811b9dd8c6f4f51e2732b6888a2b8933`  
		Last Modified: Wed, 27 Jul 2022 13:49:16 GMT  
		Size: 677.0 KB (676971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c735731e55a5ddb324dd5eb175e1f3d88895a77ea93b8fb08428ee522445708b`  
		Last Modified: Wed, 03 Aug 2022 20:44:16 GMT  
		Size: 12.8 MB (12819587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e525d9b2b00fc7130f21f05f981c44d849b279417c15b38703c3f11d3c9bd667`  
		Last Modified: Wed, 03 Aug 2022 20:44:13 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9bc880d40f528e2c6046dd7bad61fc78f27a3fbebe3f45d1348a72ace67d9b`  
		Last Modified: Wed, 03 Aug 2022 20:44:15 GMT  
		Size: 3.0 MB (3043656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b74e25b6a705707a07e0411366545458ad05f07844bde5b7bebddd988e69068`  
		Last Modified: Wed, 03 Aug 2022 21:23:08 GMT  
		Size: 8.5 MB (8476895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141bd7d880682fd816129f41549c798cabb9e94494f7ee7714d6e83e63606b82`  
		Last Modified: Wed, 03 Aug 2022 21:23:23 GMT  
		Size: 136.5 MB (136491944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b412f1d24946cb1e7f3d66a4ae5595d3b71ae6040af529dc49507cb1dd4e06c`  
		Last Modified: Wed, 03 Aug 2022 21:23:06 GMT  
		Size: 9.4 KB (9434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8aa237953d155695df1943bb27b03cf1cc3f1716ea63b1cf5a8b12d97cd6cea`  
		Last Modified: Wed, 03 Aug 2022 21:23:06 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:alpine3.16`

```console
$ docker pull satosa@sha256:fa00b0ab420886685085b244405746ecce141ff81c408876a6d8c17f5e0960ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `satosa:alpine3.16` - linux; amd64

```console
$ docker pull satosa@sha256:889e8b702bc04ca43d059bdf24c8db677954c87e5318ba8a93d795e450d485dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42508179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa3cc16430e95981e37a39687b5b6a8e23b8adf5eb81881cab4136b31de9b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:14:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 02:01:52 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 02:01:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 19 Jul 2022 02:01:54 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 10:48:21 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 11:00:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 11:00:14 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 11:00:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 11:00:21 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 11:47:34 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 11:47:34 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 11:48:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 11:48:18 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 11:48:19 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 11:48:19 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 11:48:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 11:48:19 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 11:48:19 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 11:48:19 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c14b1a767335de44f2bc926cb52487979a0fe602ac5429643dbb238f297fb`  
		Last Modified: Tue, 19 Jul 2022 02:56:13 GMT  
		Size: 666.8 KB (666769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571274b8543b548747b5e9bef700a89692fe9403cc364be8d6e8a0792ccfe2b4`  
		Last Modified: Wed, 03 Aug 2022 11:19:35 GMT  
		Size: 12.5 MB (12508608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f79a08255af5d614c7b4b81e358b5bb607bdcb14a6475c836d3d4f92f094846`  
		Last Modified: Wed, 03 Aug 2022 11:19:34 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6b20e3f6abd46292c29437a6917dc82b769ebb239e2d971aedb6695e057715`  
		Last Modified: Wed, 03 Aug 2022 11:19:34 GMT  
		Size: 3.0 MB (3043671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c974d4972d870a99bf0fba525cab86b298dd6e9405d3329a3495a164ae5c7`  
		Last Modified: Wed, 03 Aug 2022 11:49:00 GMT  
		Size: 9.4 MB (9398243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c482d554455c83821852ea2cd26eaf97f49bb1c7983342cec7242b8ea5432234`  
		Last Modified: Wed, 03 Aug 2022 11:49:01 GMT  
		Size: 14.1 MB (14080297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b861965b84abb04a92b63eb19a620daf7360785f485bc2d526885601454b19ca`  
		Last Modified: Wed, 03 Aug 2022 11:48:58 GMT  
		Size: 9.4 KB (9439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16e011f2d9efad78d03ac0d4c7abe2f694dfc5f6c158ef9fa350a3f21d22a8e`  
		Last Modified: Wed, 03 Aug 2022 11:48:58 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine3.16` - linux; arm variant v6

```console
$ docker pull satosa@sha256:1ed78492e93849ebbee5cd80dd5e4a91eb2a41676fbc3d21584a17d402028ca7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160179359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e822b6bb9258ee22b55f2f03c3d389710a39d0a3fa1d10f1250cb00db2f3e268`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 19:49:37 GMT
ADD file:7a20333469e71664904a0cb8f61613250f2bd092b4a27bfa7bbae1dc7e21b7ed in / 
# Mon, 18 Jul 2022 19:49:37 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 00:30:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 00:30:05 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 00:30:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 00:30:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 19:50:04 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 20:30:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 02 Aug 2022 20:30:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 20:30:20 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 20:30:20 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 03:20:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 03:20:45 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 03:27:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 03:27:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 03:27:54 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 03:27:54 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 03:27:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 03:27:55 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 03:27:55 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 03:27:55 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b7885075fcd06a866d12dfd56eb704045eaadbd22dc03a224cd98715be566677`  
		Last Modified: Mon, 18 Jul 2022 19:08:42 GMT  
		Size: 2.6 MB (2606431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ebe8e3a2f83d0ddc301c9b9d6405376eecb906b92082e05d5e257eff5f6293`  
		Last Modified: Wed, 27 Jul 2022 11:08:23 GMT  
		Size: 672.3 KB (672287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b647934af90a736595f675559fd3aebbcdbcfc67277de68401980916f3c217d7`  
		Last Modified: Wed, 03 Aug 2022 00:13:17 GMT  
		Size: 12.1 MB (12085055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaef313095ff837d4848dec2c5e458a33e59ee4e1ab7a9d4e3d244d20b92fbf`  
		Last Modified: Wed, 03 Aug 2022 00:13:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba453d098c35b58faf7cc2ac6a90a0e9a8941dc90611ee397d12af0a546bbe87`  
		Last Modified: Wed, 03 Aug 2022 00:13:15 GMT  
		Size: 3.0 MB (3043708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0a90158473abc47e6b9744b5cc61265a9552ba9217486241f5b7b4a5d12eec`  
		Last Modified: Wed, 03 Aug 2022 03:28:44 GMT  
		Size: 8.3 MB (8280231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a82dd9e01f89340501ac0415caccc1ad608cc08d55219cb26db2226dc64b83`  
		Last Modified: Wed, 03 Aug 2022 03:29:07 GMT  
		Size: 133.5 MB (133479861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ee2ba314aef7361329abd7eaa7a8860079655317f4d5fc9d37f73f8b34de4`  
		Last Modified: Wed, 03 Aug 2022 03:28:39 GMT  
		Size: 9.4 KB (9438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24649d01bd9f34f035857fcb9324aef45128d255b0e7d7c9be9d0d9d58a928f3`  
		Last Modified: Wed, 03 Aug 2022 03:28:39 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine3.16` - linux; arm variant v7

```console
$ docker pull satosa@sha256:9c12b392cb5946a433fe0c98001d362d79a953040068a9d0843c3a9a9c12fb8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163401667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55a50fb783bb28da31c92c6cff33c408ef6ea7e1c6da179086af8ce588f092d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:24:47 GMT
ADD file:68590e866bc6db27ad54d23de7dd275d0389cb86e4e6291a1243fcc234f2f7a1 in / 
# Mon, 18 Jul 2022 21:24:47 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 03:57:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 03:57:44 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 03:57:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 03:57:46 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 07:37:59 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 08:07:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 08:07:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 08:07:50 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 08:07:51 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 13:27:03 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 13:27:03 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 13:30:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 13:30:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 13:30:25 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 13:30:25 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 13:30:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 13:30:25 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 13:30:25 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 13:30:25 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a6b45ace95f42a930d15c33679ab9c85d46019b7e73954cadc73bb9ba176509b`  
		Last Modified: Mon, 18 Jul 2022 19:08:56 GMT  
		Size: 2.4 MB (2412307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d826ef3e3e077607452c51ac5332613cc0a20903abe17b56af4b973f31f0e9b7`  
		Last Modified: Wed, 27 Jul 2022 10:54:47 GMT  
		Size: 664.1 KB (664079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116f12212b7e97cde5b72713f0f3a3025a9ef6dffccdc353cd4d15407d343a72`  
		Last Modified: Wed, 03 Aug 2022 11:22:41 GMT  
		Size: 11.6 MB (11558755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef2affe775c9998dea9fd354aa8d4b6e97117d2092c84f1401265b9f9528bf7`  
		Last Modified: Wed, 03 Aug 2022 11:22:38 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032af4833525c8884057f85c0da98a7f2dedc337784e4ce3645fad79e6633b26`  
		Last Modified: Wed, 03 Aug 2022 11:22:39 GMT  
		Size: 3.0 MB (3043658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65c3d7d841a308ff58960bdd0832a9c2fc9d01d091b4478549cf91ad4551edc`  
		Last Modified: Thu, 04 Aug 2022 13:31:47 GMT  
		Size: 8.0 MB (8026973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553863577a06e5d191ae29abc79bb81603188e34e406ebce36a4e4da49320df8`  
		Last Modified: Thu, 04 Aug 2022 13:31:59 GMT  
		Size: 137.7 MB (137684108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d66d75890a5436b91b581c5023634cbedf248e1dbb622b1241f80c5a4ed29`  
		Last Modified: Thu, 04 Aug 2022 13:31:45 GMT  
		Size: 9.4 KB (9439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cab52b5f6577ce2ac31dd72be231ca9d43531003be80eacfe2f20bbfa5c5d5`  
		Last Modified: Thu, 04 Aug 2022 13:31:46 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine3.16` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:cccb94f4511ba8a1fd8ab69a69f483edef010e4fab16eeccfb637ae5395cdc67
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40930309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83c2e990bd9017e2a1f46423fc6e313b33122d383dda9f8f9c00e8006d36921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:10:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 01:53:04 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 01:53:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 19 Jul 2022 01:53:06 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 09:50:39 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 10:05:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 10:05:10 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 10:05:11 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 10:05:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 10:05:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 10:05:14 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 10:05:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 10:05:22 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 10:40:42 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 10:40:43 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 10:41:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 10:41:33 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 10:41:34 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 10:41:36 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 10:41:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 10:41:37 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 10:41:38 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 10:41:39 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c36086fc9356a3d9879c8427af90dd86ad6fd35b3929bab2af384e98d0571c`  
		Last Modified: Tue, 19 Jul 2022 02:56:56 GMT  
		Size: 668.0 KB (668022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255e9c7248a65c9bb1f14e3ffaf6aad2e14b965bfd9196b30e8c1efc8ddd1747`  
		Last Modified: Wed, 03 Aug 2022 10:34:00 GMT  
		Size: 12.6 MB (12579036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d32815e9cd0f789447579f484cec5ed6ff5b006c50c121a5e314519ffad01d5`  
		Last Modified: Wed, 03 Aug 2022 10:33:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c6e4018f23818adb74c050daeddb28d2efddbabe1135f85ed3ef29b17ec7b`  
		Last Modified: Wed, 03 Aug 2022 10:32:56 GMT  
		Size: 3.0 MB (3045000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2feaf81b71b2f7b13ac6cefc0f434f31221423c1c94002a89138b4c60741ced`  
		Last Modified: Wed, 03 Aug 2022 10:42:41 GMT  
		Size: 8.2 MB (8224897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c9e9ae46115c582ac3a68bb4b583d2ed73875acfb5ff520c5877d481be9cdc`  
		Last Modified: Wed, 03 Aug 2022 10:42:42 GMT  
		Size: 13.7 MB (13706894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e959a5cfce7f6c07db205394594178b791ab1fd7b3425ded77627110666277`  
		Last Modified: Wed, 03 Aug 2022 10:42:40 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143d97f09a0b08aff0f4993e07d50c6a62b1d1c84b442a35f1c8b7f9535005f4`  
		Last Modified: Wed, 03 Aug 2022 10:42:40 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine3.16` - linux; 386

```console
$ docker pull satosa@sha256:3b7052fea622f5d95da31220bc234a9258ae473482fb55269dea295fd83b4e05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (173023892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712f8d15ddeef960a7327c512f8d03f337021df170d7531f5aa93eafbe51d2c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 21:22:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 21:22:15 GMT
ENV LANG=C.UTF-8
# Tue, 09 Aug 2022 21:22:17 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 09 Aug 2022 21:22:18 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 09 Aug 2022 22:02:59 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 09 Aug 2022 22:16:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 09 Aug 2022 22:16:19 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 09 Aug 2022 22:16:20 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 09 Aug 2022 22:16:21 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 09 Aug 2022 22:16:22 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 09 Aug 2022 22:16:23 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 09 Aug 2022 22:16:31 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 09 Aug 2022 22:16:31 GMT
CMD ["python3"]
# Wed, 10 Aug 2022 03:30:07 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 10 Aug 2022 03:30:08 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 10 Aug 2022 03:33:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 10 Aug 2022 03:33:03 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 10 Aug 2022 03:33:04 GMT
WORKDIR /etc/satosa
# Wed, 10 Aug 2022 03:33:06 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 10 Aug 2022 03:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 03:33:07 GMT
EXPOSE 8080
# Wed, 10 Aug 2022 03:33:08 GMT
USER satosa:satosa
# Wed, 10 Aug 2022 03:33:09 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6e4c463b4b085b81ccd90e5d99d5d5b64a56c2f756e7ff5575080b0efc2e9f`  
		Last Modified: Tue, 09 Aug 2022 23:12:22 GMT  
		Size: 689.1 KB (689070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30e501e19288fafd4b62af6aaf0b588b8da1b9f7bf0ed0bd8c7cf5550131f4b`  
		Last Modified: Tue, 09 Aug 2022 23:13:12 GMT  
		Size: 12.7 MB (12700838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5383c9c382f8845fcf42a8ea747ddb3a99c87e277380a509277f27c6bf8d85`  
		Last Modified: Tue, 09 Aug 2022 23:13:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2450ac53e437f841f48f00e832466a3d7ce73190f3f5255c89dfb89edcd9193`  
		Last Modified: Tue, 09 Aug 2022 23:13:11 GMT  
		Size: 3.0 MB (3045003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3183acab5e336c62f2d06a000d65364d4484e755eb4c01749dd6e443ee703e32`  
		Last Modified: Wed, 10 Aug 2022 03:34:01 GMT  
		Size: 8.5 MB (8512861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350ea1863d968db10b0fe1fd8772d772c84631136d5fb13934b7c5a360cf66fc`  
		Last Modified: Wed, 10 Aug 2022 03:34:28 GMT  
		Size: 145.3 MB (145257262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92895882e21832e6f4d040fa6f60752d36b168dbc7f3893d1fc81a19da18cfc3`  
		Last Modified: Wed, 10 Aug 2022 03:33:59 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85df40b1b491557b15d24c816c82279561fd23244d53603eeea4f9976ce8766`  
		Last Modified: Wed, 10 Aug 2022 03:33:59 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine3.16` - linux; ppc64le

```console
$ docker pull satosa@sha256:f70b3121c8db732d980c4272ea937145d0745875aba33578b5667bbaf28fb1ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164310759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef00aeaa317867dd9dca82b0661794be10c5d0a082d11a8f76b597b76e88cb55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:29:30 GMT
ADD file:69e4080f15f54e2d8f8aa25fdcba9c01dde149d43592edd5023106675e54a769 in / 
# Mon, 18 Jul 2022 21:29:31 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 04:30:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 04:30:31 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 04:30:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 04:30:33 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 19:40:20 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 20:04:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 20:05:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 20:05:00 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 20:05:00 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 20:05:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 20:05:01 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 20:05:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 20:05:13 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 21:15:12 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 21:15:12 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 21:21:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 21:21:41 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 21:21:41 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 21:21:42 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 21:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 21:21:42 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 21:21:43 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 21:21:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:602896d442490cd3fbb6599f0f862d3673b7cd58eca3ac842b8e09bf8d012443`  
		Last Modified: Mon, 18 Jul 2022 19:09:09 GMT  
		Size: 2.8 MB (2789923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6556a4bf6509d5fd24900f56a6175bd811b9dd8c6f4f51e2732b6888a2b8933`  
		Last Modified: Wed, 27 Jul 2022 13:49:16 GMT  
		Size: 677.0 KB (676971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c735731e55a5ddb324dd5eb175e1f3d88895a77ea93b8fb08428ee522445708b`  
		Last Modified: Wed, 03 Aug 2022 20:44:16 GMT  
		Size: 12.8 MB (12819587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e525d9b2b00fc7130f21f05f981c44d849b279417c15b38703c3f11d3c9bd667`  
		Last Modified: Wed, 03 Aug 2022 20:44:13 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9bc880d40f528e2c6046dd7bad61fc78f27a3fbebe3f45d1348a72ace67d9b`  
		Last Modified: Wed, 03 Aug 2022 20:44:15 GMT  
		Size: 3.0 MB (3043656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b74e25b6a705707a07e0411366545458ad05f07844bde5b7bebddd988e69068`  
		Last Modified: Wed, 03 Aug 2022 21:23:08 GMT  
		Size: 8.5 MB (8476895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141bd7d880682fd816129f41549c798cabb9e94494f7ee7714d6e83e63606b82`  
		Last Modified: Wed, 03 Aug 2022 21:23:23 GMT  
		Size: 136.5 MB (136491944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b412f1d24946cb1e7f3d66a4ae5595d3b71ae6040af529dc49507cb1dd4e06c`  
		Last Modified: Wed, 03 Aug 2022 21:23:06 GMT  
		Size: 9.4 KB (9434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8aa237953d155695df1943bb27b03cf1cc3f1716ea63b1cf5a8b12d97cd6cea`  
		Last Modified: Wed, 03 Aug 2022 21:23:06 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:bullseye`

```console
$ docker pull satosa@sha256:b952f0d280486a79665537c956718dec4fff75e9e6a343a79e1048bc3bf3c861
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

### `satosa:bullseye` - linux; amd64

```console
$ docker pull satosa@sha256:3d92574bf94e0395a41762efa378d221f605ea12bea73ae604c71310fe6036fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82653895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d245b28169a1e1f7dd888fa2381fc3aa02a91b2210f7b6b481c4016173ac8d0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 09:39:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 09:39:09 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 09:39:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 09:39:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 10:15:41 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 10:26:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 10:26:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 10:26:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 10:26:31 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 11:46:24 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 11:46:24 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 11:47:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 11:47:19 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 11:47:19 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 11:47:19 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 11:47:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 11:47:20 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 11:47:20 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 11:47:20 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126aaa6587b8608b62fa39019a891e98460e23bad2d04fb235c4dc8fae2adf3c`  
		Last Modified: Tue, 02 Aug 2022 12:33:29 GMT  
		Size: 1.1 MB (1076278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd06b55ca686f29b26c8a7e051ce98ad571fd6cf22bba07f5cd17e98fd31e13`  
		Last Modified: Wed, 03 Aug 2022 11:18:36 GMT  
		Size: 12.1 MB (12106838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3950cece0b727ab257c49317871d00f22d2abcb77bcce19ddf86aab5c4d88e21`  
		Last Modified: Wed, 03 Aug 2022 11:18:34 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e27c1167cc2a09e30e53c0fd2933e189e20b4785284e84a919fe5fd3013388b`  
		Last Modified: Wed, 03 Aug 2022 11:18:35 GMT  
		Size: 3.3 MB (3336043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb69b4e4539d59ea0fbed39563b5042d023cd4713d9a38bde6b930fb548e8b9a`  
		Last Modified: Wed, 03 Aug 2022 11:48:44 GMT  
		Size: 19.6 MB (19587061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620aa9bb44333fe5af9257a47e9e0de0e7a0596721959465531442e2b753aa5a`  
		Last Modified: Wed, 03 Aug 2022 11:48:44 GMT  
		Size: 15.2 MB (15169129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffc5c41689ca0d4f9b9e1beea0953f2bec48e3ab6becfee1b8c8862100aadbe`  
		Last Modified: Wed, 03 Aug 2022 11:48:41 GMT  
		Size: 9.4 KB (9443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebafed1e50948cce1a8ec458a2dbc933ec93924419791a83613e224356054ee`  
		Last Modified: Wed, 03 Aug 2022 11:48:41 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:bullseye` - linux; arm variant v5

```console
$ docker pull satosa@sha256:e4ee7d4d43b26f8dc6b5a7d8358af5463aa5ebf830249e6272afbe2a819e9732
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.7 MB (203698783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160cc52ce9b78d794b4acbd3286cc62c771bad645eb50e8c9af6722d743f166c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:10 GMT
ADD file:4cd2f95737fd3007912428eeac56036c9e67e989e66cec08a8be99da47f88494 in / 
# Tue, 02 Aug 2022 00:49:10 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:38:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 20:38:12 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 20:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:38:23 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 22:45:24 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 23:08:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 23:08:11 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 23:08:11 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 23:08:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 23:08:30 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 19:10:52 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 19:10:52 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 19:17:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 19:17:42 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 19:17:42 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 19:17:43 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 19:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 19:17:43 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 19:17:43 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 19:17:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5890b0ca6af5e8467a488e68716691950496a8f247d0495c2d595ddcb1893aff`  
		Last Modified: Tue, 02 Aug 2022 00:56:06 GMT  
		Size: 28.9 MB (28905515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eafe902d3c868e979e01e5c5aca6567b8be8b60814b9e1ce93c2b749451b410`  
		Last Modified: Wed, 03 Aug 2022 02:16:47 GMT  
		Size: 1.1 MB (1059641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e073b0922c53e3aee167b94b195f01b7740c95a691b391e30bbc1dd36133f578`  
		Last Modified: Wed, 03 Aug 2022 02:18:15 GMT  
		Size: 11.7 MB (11687058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1563deb88ac81fbc07f66164de09058989bc2f52e4b201209996fc610e7424`  
		Last Modified: Wed, 03 Aug 2022 02:18:11 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9586a9ae76d2fcf29975a3cbac30868417a5e7209b4d681ab4d8cdc9417e1127`  
		Last Modified: Wed, 03 Aug 2022 02:18:13 GMT  
		Size: 3.3 MB (3335517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2138d4d7c7c422781a7da5bbba917dfee3de2e44c0b89e2c05cd5fb54d6aec`  
		Last Modified: Wed, 03 Aug 2022 19:18:28 GMT  
		Size: 21.2 MB (21220513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ec77684813e78ff3c43e62e86fde2b1964089fb2e02c36be1b197e18d76199`  
		Last Modified: Wed, 03 Aug 2022 19:18:38 GMT  
		Size: 137.5 MB (137478750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecfeff163b4d6f23860d774bf123b6ad13105fce4fa35bddd9e46a56b0c09af`  
		Last Modified: Wed, 03 Aug 2022 19:18:21 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb3f6f2ab2014dd8287001b208c1dc97200c2c3e16a2cb980fd938dfd82858b`  
		Last Modified: Wed, 03 Aug 2022 19:18:22 GMT  
		Size: 2.1 KB (2111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:bullseye` - linux; arm variant v7

```console
$ docker pull satosa@sha256:1eb7ef57547ada8079868ad16a792df4e4cbc8571c4b2beb50d5682d1bc6250f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202351243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194a9b56fc0cc44a0542e47df53c65db1e4f7a579b5a8624e2b202e21462c73d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:58:59 GMT
ADD file:1575b776a15adacebc0875642e97a80807d42dcfc8917e1406d47af7ac244c97 in / 
# Tue, 02 Aug 2022 00:58:59 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:34:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 04:34:22 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 04:34:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 04:34:30 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 06:30:14 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 06:52:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 06:52:09 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 06:52:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 06:52:24 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 13:20:49 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 13:20:50 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 13:26:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 13:26:45 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 13:26:45 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 13:26:45 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 13:26:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 13:26:45 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 13:26:45 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 13:26:45 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1dd75a3a9c893a7dc313f683dd62464b7eab6c6d522ee62c8a17022631830f32`  
		Last Modified: Tue, 02 Aug 2022 01:06:45 GMT  
		Size: 26.6 MB (26560586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4206fea8c3d0ae09213fad25e06bb550a03c76c2b15e7a3c134ee5e2d217cd`  
		Last Modified: Wed, 03 Aug 2022 11:19:22 GMT  
		Size: 1.0 MB (1041632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed9dda465ec974f3e81b6b5f48dee0c43b63aeae625042e1e5f8ca482d43f1f`  
		Last Modified: Wed, 03 Aug 2022 11:21:19 GMT  
		Size: 11.2 MB (11205345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c669588520ce26d52819574b6ac8f40bc121ec539aae49c4cdc6aa899fcea`  
		Last Modified: Wed, 03 Aug 2022 11:21:15 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75c71e6575f11c76771634448c2e1c7e6988853591c1422d979aaf3dfa73569`  
		Last Modified: Wed, 03 Aug 2022 11:21:17 GMT  
		Size: 3.3 MB (3335656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d5ac04f9c39c2ba1d884f419e586ede32f2779ea0bbb6a7033e0f70c79d670`  
		Last Modified: Thu, 04 Aug 2022 13:31:15 GMT  
		Size: 20.9 MB (20949533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65844885dbff2fac2bccf9e5a7b69d9c423352d19d5ffb5eeca720f5e2a10886`  
		Last Modified: Thu, 04 Aug 2022 13:31:26 GMT  
		Size: 139.2 MB (139246702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53ebddc2eb90a987a1bae1b3a245f2d88ae7ea81a35f85f6bfdf10891217d58`  
		Last Modified: Thu, 04 Aug 2022 13:31:10 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa39e50e9a3812f026202131476b98a06e4a65a16a21fee180aeb54d979e2cb8`  
		Last Modified: Thu, 04 Aug 2022 13:31:10 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:bullseye` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:8a7bc186f7c0a8725b284d01a4dceac8636d5f7f96b11f0d4031fd66f199e2b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79849083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56454aaf2924873a1f55890e93e1c83261d4047ce84a080d73750691435b3d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:03:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 12:03:30 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 12:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:03:36 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 09:19:10 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 09:29:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 09:29:22 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 09:29:22 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 09:29:23 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 09:29:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 09:29:25 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 09:29:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 09:29:37 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 10:39:28 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 10:39:28 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 10:40:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 10:40:15 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 10:40:16 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 10:40:18 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 10:40:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 10:40:19 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 10:40:20 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 10:40:21 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f101f90cc8f7640b7db5f7094941a1fe4ff28e11a968d3a36f146a89a480ecbb`  
		Last Modified: Tue, 02 Aug 2022 14:47:06 GMT  
		Size: 1.1 MB (1063812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a5d6cf27653f158e4f7552f31dc146332b6d820679ee42ebff5b4e47f4dac`  
		Last Modified: Wed, 03 Aug 2022 10:31:15 GMT  
		Size: 12.2 MB (12153733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd415bdc2c72c852623e384c90826d41aa2739adbc3158bd814bc3e562ab16ea`  
		Last Modified: Wed, 03 Aug 2022 10:31:13 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90ceb316b2d011719d35fb58a5d69ec1b84ebc6a9ab5568354ca370aad48524`  
		Last Modified: Wed, 03 Aug 2022 10:31:14 GMT  
		Size: 3.1 MB (3119919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7a23c6e6d4ea56699e3033f9fd616c6fa79290a257066f21578bf773f283cb`  
		Last Modified: Wed, 03 Aug 2022 10:42:23 GMT  
		Size: 19.3 MB (19324710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f64adba6c540f9f4fde33df9a99fa32be543c937e20b203b409ba3340f7b62`  
		Last Modified: Wed, 03 Aug 2022 10:42:23 GMT  
		Size: 14.1 MB (14120866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9df97e7203d91c6109257b6e98c0bb926732214ee96a7110c86550f8c271b74`  
		Last Modified: Wed, 03 Aug 2022 10:42:20 GMT  
		Size: 9.4 KB (9394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d56269ee4307b5c76ba7efef9346008e1440979b95ee777b9d5e8e3e4ead5b1`  
		Last Modified: Wed, 03 Aug 2022 10:42:20 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:bullseye` - linux; 386

```console
$ docker pull satosa@sha256:ff2180ab006e1d173a6d157a2ef8b05c4abae7d45d5693889e12f05e6861a42d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207396057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b9632c4df58a4c5e3e68e82bf8bab7462b2530f9ecfb108feb8726a85ab4d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:39:20 GMT
ADD file:f771e2286465694126158821089d801c7296376be2a56189e6041a15d2fe79f5 in / 
# Tue, 02 Aug 2022 00:39:21 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 11:22:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 11:22:53 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 11:22:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 11:22:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 20:51:53 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 21:03:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 21:03:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 21:03:55 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 21:03:56 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 21:03:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 21:03:58 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 21:04:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 21:04:12 GMT
CMD ["python3"]
# Tue, 02 Aug 2022 22:21:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 02 Aug 2022 22:21:44 GMT
ENV SATOSA_VERSION=8.1.1
# Tue, 02 Aug 2022 23:39:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 02 Aug 2022 23:39:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 02 Aug 2022 23:39:26 GMT
WORKDIR /etc/satosa
# Tue, 02 Aug 2022 23:39:28 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Tue, 02 Aug 2022 23:39:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 23:39:29 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 23:39:30 GMT
USER satosa:satosa
# Tue, 02 Aug 2022 23:39:31 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:90eb7f0ce9f33cf5dcd67d54c2fa606186dbaa5f95b6046f36145097267f9e53`  
		Last Modified: Tue, 02 Aug 2022 00:45:14 GMT  
		Size: 32.4 MB (32374054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd27ead98f25cd891e8dfae23b5500c856f3a9db336a545eed8b5f180a6df0b4`  
		Last Modified: Tue, 02 Aug 2022 14:37:54 GMT  
		Size: 1.1 MB (1088442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7362ecffe5fefdfcff89188358cb648fae40c1fed6254cd3325ef1c340a0ca9b`  
		Last Modified: Tue, 02 Aug 2022 22:15:01 GMT  
		Size: 12.2 MB (12224818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fb82e70fda9a811619f0b6cfd165d59473bcc467e702a70231630e64335b18`  
		Last Modified: Tue, 02 Aug 2022 22:14:59 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab067ab28a29ee91955ebd00b4849cd1d1993a430051ce801b5eaffeeb59b976`  
		Last Modified: Tue, 02 Aug 2022 22:15:00 GMT  
		Size: 3.1 MB (3119814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c68c7fda4b282e37efe94863aed2872d62133ead0fed4a4b4174eab16a125f`  
		Last Modified: Tue, 02 Aug 2022 23:40:27 GMT  
		Size: 22.6 MB (22586591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4630af60cc9f0637de40da0789c8be2b49091d860ae7f21753e736c5a24b0fac`  
		Last Modified: Tue, 02 Aug 2022 23:40:44 GMT  
		Size: 136.0 MB (135990599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ba92ddedaf8e60d74aac7773867aec0a84b2812ba92a5742090bee107e7736`  
		Last Modified: Tue, 02 Aug 2022 23:40:24 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e28ea4f42ac6baac91e14de0ee8d101956ac6d64c7d4078bb57ebfddde33184`  
		Last Modified: Tue, 02 Aug 2022 23:40:24 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:bullseye` - linux; mips64le

```console
$ docker pull satosa@sha256:b9bdbc69a8a0be593fe150cbd4334f006447c17a9538b850002e7fa96445593b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.8 MB (205844024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7d3830a289e7a92a0277b60e6cce741d4887ea889e4e236cdd2d878fb1f64b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:10:34 GMT
ADD file:6dc22a1e5b5fcf23f2549406ddcc45c4e244f46e21eafa881de81fa87438e5d8 in / 
# Tue, 02 Aug 2022 01:10:38 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 10:25:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 10:25:08 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 10:25:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:25:36 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 04 Aug 2022 04:16:09 GMT
ENV PYTHON_VERSION=3.10.6
# Thu, 04 Aug 2022 05:33:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Thu, 04 Aug 2022 05:33:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 04 Aug 2022 05:33:27 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Thu, 04 Aug 2022 05:33:30 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Thu, 04 Aug 2022 05:33:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Thu, 04 Aug 2022 05:33:35 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Thu, 04 Aug 2022 05:34:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 04 Aug 2022 05:34:30 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 08:35:12 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 08:35:15 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 08:52:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 08:52:17 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 08:52:21 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 08:52:25 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 08:52:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 08:52:34 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 08:52:39 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 08:52:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:88350749a27614c791450c256b051f023d81cdd256211274b1efac493779d2be`  
		Last Modified: Tue, 02 Aug 2022 01:21:02 GMT  
		Size: 29.6 MB (29628964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61130d003a0ea87819935a3a252db1861d9b87e1313fa7988d5f0642637f3e`  
		Last Modified: Tue, 02 Aug 2022 23:46:40 GMT  
		Size: 1.0 MB (1049605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e786491697e5d2bd3dee622f7eae98810c04c895d5024e910e2394f92b37ad8`  
		Last Modified: Thu, 04 Aug 2022 08:14:51 GMT  
		Size: 12.1 MB (12124464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fb1366c066d6bf94df2bf081524439083c14a1f292da85f218000ac515a2f5`  
		Last Modified: Thu, 04 Aug 2022 08:14:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe7637d1173b353af8622199dfbc92d0f74f8cff129fe540541b9c069a058d3`  
		Last Modified: Thu, 04 Aug 2022 08:14:46 GMT  
		Size: 3.1 MB (3120804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4655831cce551d936028a78d3d4a295cd96e3ca02ea0f5f726d0b963350a0e`  
		Last Modified: Thu, 04 Aug 2022 08:53:18 GMT  
		Size: 21.3 MB (21288233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54965dd4effca16f75a92cdac5dd71e708a50d218ca30b0806964a58d8b726ee`  
		Last Modified: Thu, 04 Aug 2022 08:53:58 GMT  
		Size: 138.6 MB (138620211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a449c61594c6b3d2e0fa03d876ebe6fc8561eaa1d46ebf088772a42dea52b596`  
		Last Modified: Thu, 04 Aug 2022 08:53:06 GMT  
		Size: 9.4 KB (9396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54e620f3a05fe34c293ac1de03899ec567f49faa21a8db43216f796387f8f65`  
		Last Modified: Thu, 04 Aug 2022 08:53:06 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:bullseye` - linux; ppc64le

```console
$ docker pull satosa@sha256:b84ad93ccca31f2ba03b7c0586ad9f3a2d71764d4338922af798ae737ec87f23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212244381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f29a99f45c08fb90c8ad9dec84fd55c14d0ca8ecbc00c2160fc3464a14feca9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:17:30 GMT
ADD file:3a95a896d463569ce82199957052b3467123a4bd3385a0a4e397cf08402a99c3 in / 
# Tue, 02 Aug 2022 01:17:32 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:03:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 16:03:13 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 16:03:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 16:03:24 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 18:10:29 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 18:43:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 18:43:03 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 18:43:03 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 18:43:03 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 18:43:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 18:43:04 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 18:43:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 18:43:25 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 21:09:20 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 21:09:21 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 21:14:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 21:14:39 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 21:14:39 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 21:14:40 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 21:14:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 21:14:41 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 21:14:41 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 21:14:42 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5241cd116d6e6e2d62f3d8c2245b74daca9f6cc154eaccd738feb41984c74714`  
		Last Modified: Tue, 02 Aug 2022 01:24:39 GMT  
		Size: 35.3 MB (35272771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf6dcfcb4fa2f4e24ce6bed8b3eda6b0d49d92062cb34d95830e4e9f512270`  
		Last Modified: Wed, 03 Aug 2022 00:14:29 GMT  
		Size: 1.1 MB (1094658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdc50327f93cca5ad2c5f8500471040045b715045a9a4852ece90b3155d5aea`  
		Last Modified: Wed, 03 Aug 2022 20:42:55 GMT  
		Size: 12.5 MB (12473465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49f3fdf44cc1cf9b0e2d32c8ea2b62a0d3eb7eac481b56c9d11e44c66b764fe`  
		Last Modified: Wed, 03 Aug 2022 20:42:52 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd9d6c8cb5530b56f02a736bb1cc24d2d0ffc11d6fb55dc6befb0e114a1ff74`  
		Last Modified: Wed, 03 Aug 2022 20:42:53 GMT  
		Size: 3.3 MB (3336216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209342dd334b280e74196c0e693487033f7f2d08880ab61f5f9113dbbd5d0461`  
		Last Modified: Wed, 03 Aug 2022 21:22:32 GMT  
		Size: 22.2 MB (22158681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11809242e6bd5adbd0096d37646b954f666a1e2a107dd5442773977caa919360`  
		Last Modified: Wed, 03 Aug 2022 21:22:45 GMT  
		Size: 137.9 MB (137896801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa36501b6a1d8ec2e51a6a162f1f43d70ea4b035335513b65b800346790717`  
		Last Modified: Wed, 03 Aug 2022 21:22:27 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fe38c0944e97231334e780f32f3cd041644756c5b195812b19edd697268021`  
		Last Modified: Wed, 03 Aug 2022 21:22:27 GMT  
		Size: 2.1 KB (2113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:bullseye` - linux; s390x

```console
$ docker pull satosa@sha256:f52b8375aeb8b39ad8ae5b9f05f4f94a47f4776b3f500aeeadee19c4ed572f5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202163420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f253b8b35e8bbaf69f23beb8a8584dc48a0c682127faa17ed9d639b33dfdf3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 08:30:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 08:30:40 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 08:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 08:30:44 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 22:09:42 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 22:18:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 22:18:03 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 22:18:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 22:18:13 GMT
CMD ["python3"]
# Tue, 02 Aug 2022 23:28:28 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 02 Aug 2022 23:28:31 GMT
ENV SATOSA_VERSION=8.1.1
# Tue, 02 Aug 2022 23:32:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 02 Aug 2022 23:33:02 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 02 Aug 2022 23:33:02 GMT
WORKDIR /etc/satosa
# Tue, 02 Aug 2022 23:33:02 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Tue, 02 Aug 2022 23:33:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 23:33:02 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 23:33:03 GMT
USER satosa:satosa
# Tue, 02 Aug 2022 23:33:03 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c36d12a9d2aa3bd2ed5880b10e768bae6cab779992e198cf595d3b8d6924d5`  
		Last Modified: Tue, 02 Aug 2022 10:43:27 GMT  
		Size: 1.1 MB (1075771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a2fa2a5f3f4be291fac87451996292e32ad4b6b7e7ae168c720b6501ba676f`  
		Last Modified: Tue, 02 Aug 2022 23:23:49 GMT  
		Size: 11.9 MB (11900903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1958402e81da32fc50ee2b3d3d48a5714015a6589a9b0882e2e0862173874f52`  
		Last Modified: Tue, 02 Aug 2022 23:23:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adc16df778c23094a004c62669c6de553142901db4933d76959d223598473b`  
		Last Modified: Tue, 02 Aug 2022 23:23:49 GMT  
		Size: 3.3 MB (3335624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5f479e9444a18e7100a74300ba30ab5818c9023c386c0a537811de457f1e99`  
		Last Modified: Tue, 02 Aug 2022 23:33:39 GMT  
		Size: 19.6 MB (19580744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573792100821147cd9e469e566ed70175d1fe8ec2b68e371484abc92f0aeaf74`  
		Last Modified: Tue, 02 Aug 2022 23:33:45 GMT  
		Size: 136.6 MB (136618328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cb6a07895307e25b49bb3cdebc3f6e29fef231b0390c00ddacc6b74ee5f9fd`  
		Last Modified: Tue, 02 Aug 2022 23:33:36 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0ce3aebbe275e54928297909f6f1ed7c7beee5c901706ccef91eec96eb8bc5`  
		Last Modified: Tue, 02 Aug 2022 23:33:36 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:latest`

```console
$ docker pull satosa@sha256:b952f0d280486a79665537c956718dec4fff75e9e6a343a79e1048bc3bf3c861
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

### `satosa:latest` - linux; amd64

```console
$ docker pull satosa@sha256:3d92574bf94e0395a41762efa378d221f605ea12bea73ae604c71310fe6036fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82653895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d245b28169a1e1f7dd888fa2381fc3aa02a91b2210f7b6b481c4016173ac8d0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 09:39:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 09:39:09 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 09:39:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 09:39:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 10:15:41 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 10:26:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 10:26:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 10:26:20 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 10:26:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 10:26:31 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 11:46:24 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 11:46:24 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 11:47:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 11:47:19 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 11:47:19 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 11:47:19 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 11:47:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 11:47:20 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 11:47:20 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 11:47:20 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126aaa6587b8608b62fa39019a891e98460e23bad2d04fb235c4dc8fae2adf3c`  
		Last Modified: Tue, 02 Aug 2022 12:33:29 GMT  
		Size: 1.1 MB (1076278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd06b55ca686f29b26c8a7e051ce98ad571fd6cf22bba07f5cd17e98fd31e13`  
		Last Modified: Wed, 03 Aug 2022 11:18:36 GMT  
		Size: 12.1 MB (12106838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3950cece0b727ab257c49317871d00f22d2abcb77bcce19ddf86aab5c4d88e21`  
		Last Modified: Wed, 03 Aug 2022 11:18:34 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e27c1167cc2a09e30e53c0fd2933e189e20b4785284e84a919fe5fd3013388b`  
		Last Modified: Wed, 03 Aug 2022 11:18:35 GMT  
		Size: 3.3 MB (3336043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb69b4e4539d59ea0fbed39563b5042d023cd4713d9a38bde6b930fb548e8b9a`  
		Last Modified: Wed, 03 Aug 2022 11:48:44 GMT  
		Size: 19.6 MB (19587061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620aa9bb44333fe5af9257a47e9e0de0e7a0596721959465531442e2b753aa5a`  
		Last Modified: Wed, 03 Aug 2022 11:48:44 GMT  
		Size: 15.2 MB (15169129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffc5c41689ca0d4f9b9e1beea0953f2bec48e3ab6becfee1b8c8862100aadbe`  
		Last Modified: Wed, 03 Aug 2022 11:48:41 GMT  
		Size: 9.4 KB (9443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebafed1e50948cce1a8ec458a2dbc933ec93924419791a83613e224356054ee`  
		Last Modified: Wed, 03 Aug 2022 11:48:41 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:latest` - linux; arm variant v5

```console
$ docker pull satosa@sha256:e4ee7d4d43b26f8dc6b5a7d8358af5463aa5ebf830249e6272afbe2a819e9732
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.7 MB (203698783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160cc52ce9b78d794b4acbd3286cc62c771bad645eb50e8c9af6722d743f166c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:10 GMT
ADD file:4cd2f95737fd3007912428eeac56036c9e67e989e66cec08a8be99da47f88494 in / 
# Tue, 02 Aug 2022 00:49:10 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:38:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 20:38:12 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 20:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:38:23 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 22:45:24 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 23:08:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 23:08:11 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 23:08:11 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 23:08:12 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 23:08:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 23:08:30 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 19:10:52 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 19:10:52 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 19:17:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 19:17:42 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 19:17:42 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 19:17:43 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 19:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 19:17:43 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 19:17:43 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 19:17:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5890b0ca6af5e8467a488e68716691950496a8f247d0495c2d595ddcb1893aff`  
		Last Modified: Tue, 02 Aug 2022 00:56:06 GMT  
		Size: 28.9 MB (28905515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eafe902d3c868e979e01e5c5aca6567b8be8b60814b9e1ce93c2b749451b410`  
		Last Modified: Wed, 03 Aug 2022 02:16:47 GMT  
		Size: 1.1 MB (1059641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e073b0922c53e3aee167b94b195f01b7740c95a691b391e30bbc1dd36133f578`  
		Last Modified: Wed, 03 Aug 2022 02:18:15 GMT  
		Size: 11.7 MB (11687058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1563deb88ac81fbc07f66164de09058989bc2f52e4b201209996fc610e7424`  
		Last Modified: Wed, 03 Aug 2022 02:18:11 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9586a9ae76d2fcf29975a3cbac30868417a5e7209b4d681ab4d8cdc9417e1127`  
		Last Modified: Wed, 03 Aug 2022 02:18:13 GMT  
		Size: 3.3 MB (3335517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2138d4d7c7c422781a7da5bbba917dfee3de2e44c0b89e2c05cd5fb54d6aec`  
		Last Modified: Wed, 03 Aug 2022 19:18:28 GMT  
		Size: 21.2 MB (21220513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ec77684813e78ff3c43e62e86fde2b1964089fb2e02c36be1b197e18d76199`  
		Last Modified: Wed, 03 Aug 2022 19:18:38 GMT  
		Size: 137.5 MB (137478750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecfeff163b4d6f23860d774bf123b6ad13105fce4fa35bddd9e46a56b0c09af`  
		Last Modified: Wed, 03 Aug 2022 19:18:21 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb3f6f2ab2014dd8287001b208c1dc97200c2c3e16a2cb980fd938dfd82858b`  
		Last Modified: Wed, 03 Aug 2022 19:18:22 GMT  
		Size: 2.1 KB (2111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:latest` - linux; arm variant v7

```console
$ docker pull satosa@sha256:1eb7ef57547ada8079868ad16a792df4e4cbc8571c4b2beb50d5682d1bc6250f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202351243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194a9b56fc0cc44a0542e47df53c65db1e4f7a579b5a8624e2b202e21462c73d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:58:59 GMT
ADD file:1575b776a15adacebc0875642e97a80807d42dcfc8917e1406d47af7ac244c97 in / 
# Tue, 02 Aug 2022 00:58:59 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 04:34:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 04:34:22 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 04:34:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 04:34:30 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 06:30:14 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 06:52:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 06:52:09 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 06:52:10 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 06:52:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 06:52:24 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 13:20:49 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 13:20:50 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 13:26:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 13:26:45 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 13:26:45 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 13:26:45 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 13:26:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 13:26:45 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 13:26:45 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 13:26:45 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1dd75a3a9c893a7dc313f683dd62464b7eab6c6d522ee62c8a17022631830f32`  
		Last Modified: Tue, 02 Aug 2022 01:06:45 GMT  
		Size: 26.6 MB (26560586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4206fea8c3d0ae09213fad25e06bb550a03c76c2b15e7a3c134ee5e2d217cd`  
		Last Modified: Wed, 03 Aug 2022 11:19:22 GMT  
		Size: 1.0 MB (1041632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed9dda465ec974f3e81b6b5f48dee0c43b63aeae625042e1e5f8ca482d43f1f`  
		Last Modified: Wed, 03 Aug 2022 11:21:19 GMT  
		Size: 11.2 MB (11205345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c669588520ce26d52819574b6ac8f40bc121ec539aae49c4cdc6aa899fcea`  
		Last Modified: Wed, 03 Aug 2022 11:21:15 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75c71e6575f11c76771634448c2e1c7e6988853591c1422d979aaf3dfa73569`  
		Last Modified: Wed, 03 Aug 2022 11:21:17 GMT  
		Size: 3.3 MB (3335656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d5ac04f9c39c2ba1d884f419e586ede32f2779ea0bbb6a7033e0f70c79d670`  
		Last Modified: Thu, 04 Aug 2022 13:31:15 GMT  
		Size: 20.9 MB (20949533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65844885dbff2fac2bccf9e5a7b69d9c423352d19d5ffb5eeca720f5e2a10886`  
		Last Modified: Thu, 04 Aug 2022 13:31:26 GMT  
		Size: 139.2 MB (139246702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53ebddc2eb90a987a1bae1b3a245f2d88ae7ea81a35f85f6bfdf10891217d58`  
		Last Modified: Thu, 04 Aug 2022 13:31:10 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa39e50e9a3812f026202131476b98a06e4a65a16a21fee180aeb54d979e2cb8`  
		Last Modified: Thu, 04 Aug 2022 13:31:10 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:latest` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:8a7bc186f7c0a8725b284d01a4dceac8636d5f7f96b11f0d4031fd66f199e2b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79849083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56454aaf2924873a1f55890e93e1c83261d4047ce84a080d73750691435b3d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:03:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 12:03:30 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 12:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:03:36 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 09:19:10 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 09:29:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 09:29:22 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 09:29:22 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 09:29:23 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 09:29:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 09:29:25 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 09:29:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 09:29:37 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 10:39:28 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 10:39:28 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 10:40:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 10:40:15 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 10:40:16 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 10:40:18 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 10:40:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 10:40:19 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 10:40:20 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 10:40:21 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f101f90cc8f7640b7db5f7094941a1fe4ff28e11a968d3a36f146a89a480ecbb`  
		Last Modified: Tue, 02 Aug 2022 14:47:06 GMT  
		Size: 1.1 MB (1063812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a5d6cf27653f158e4f7552f31dc146332b6d820679ee42ebff5b4e47f4dac`  
		Last Modified: Wed, 03 Aug 2022 10:31:15 GMT  
		Size: 12.2 MB (12153733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd415bdc2c72c852623e384c90826d41aa2739adbc3158bd814bc3e562ab16ea`  
		Last Modified: Wed, 03 Aug 2022 10:31:13 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90ceb316b2d011719d35fb58a5d69ec1b84ebc6a9ab5568354ca370aad48524`  
		Last Modified: Wed, 03 Aug 2022 10:31:14 GMT  
		Size: 3.1 MB (3119919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7a23c6e6d4ea56699e3033f9fd616c6fa79290a257066f21578bf773f283cb`  
		Last Modified: Wed, 03 Aug 2022 10:42:23 GMT  
		Size: 19.3 MB (19324710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f64adba6c540f9f4fde33df9a99fa32be543c937e20b203b409ba3340f7b62`  
		Last Modified: Wed, 03 Aug 2022 10:42:23 GMT  
		Size: 14.1 MB (14120866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9df97e7203d91c6109257b6e98c0bb926732214ee96a7110c86550f8c271b74`  
		Last Modified: Wed, 03 Aug 2022 10:42:20 GMT  
		Size: 9.4 KB (9394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d56269ee4307b5c76ba7efef9346008e1440979b95ee777b9d5e8e3e4ead5b1`  
		Last Modified: Wed, 03 Aug 2022 10:42:20 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:latest` - linux; 386

```console
$ docker pull satosa@sha256:ff2180ab006e1d173a6d157a2ef8b05c4abae7d45d5693889e12f05e6861a42d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207396057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b9632c4df58a4c5e3e68e82bf8bab7462b2530f9ecfb108feb8726a85ab4d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:39:20 GMT
ADD file:f771e2286465694126158821089d801c7296376be2a56189e6041a15d2fe79f5 in / 
# Tue, 02 Aug 2022 00:39:21 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 11:22:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 11:22:53 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 11:22:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 11:22:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 20:51:53 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 21:03:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 21:03:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 21:03:55 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 21:03:56 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 21:03:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 21:03:58 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 21:04:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 21:04:12 GMT
CMD ["python3"]
# Tue, 02 Aug 2022 22:21:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 02 Aug 2022 22:21:44 GMT
ENV SATOSA_VERSION=8.1.1
# Tue, 02 Aug 2022 23:39:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 02 Aug 2022 23:39:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 02 Aug 2022 23:39:26 GMT
WORKDIR /etc/satosa
# Tue, 02 Aug 2022 23:39:28 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Tue, 02 Aug 2022 23:39:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 23:39:29 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 23:39:30 GMT
USER satosa:satosa
# Tue, 02 Aug 2022 23:39:31 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:90eb7f0ce9f33cf5dcd67d54c2fa606186dbaa5f95b6046f36145097267f9e53`  
		Last Modified: Tue, 02 Aug 2022 00:45:14 GMT  
		Size: 32.4 MB (32374054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd27ead98f25cd891e8dfae23b5500c856f3a9db336a545eed8b5f180a6df0b4`  
		Last Modified: Tue, 02 Aug 2022 14:37:54 GMT  
		Size: 1.1 MB (1088442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7362ecffe5fefdfcff89188358cb648fae40c1fed6254cd3325ef1c340a0ca9b`  
		Last Modified: Tue, 02 Aug 2022 22:15:01 GMT  
		Size: 12.2 MB (12224818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fb82e70fda9a811619f0b6cfd165d59473bcc467e702a70231630e64335b18`  
		Last Modified: Tue, 02 Aug 2022 22:14:59 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab067ab28a29ee91955ebd00b4849cd1d1993a430051ce801b5eaffeeb59b976`  
		Last Modified: Tue, 02 Aug 2022 22:15:00 GMT  
		Size: 3.1 MB (3119814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c68c7fda4b282e37efe94863aed2872d62133ead0fed4a4b4174eab16a125f`  
		Last Modified: Tue, 02 Aug 2022 23:40:27 GMT  
		Size: 22.6 MB (22586591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4630af60cc9f0637de40da0789c8be2b49091d860ae7f21753e736c5a24b0fac`  
		Last Modified: Tue, 02 Aug 2022 23:40:44 GMT  
		Size: 136.0 MB (135990599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ba92ddedaf8e60d74aac7773867aec0a84b2812ba92a5742090bee107e7736`  
		Last Modified: Tue, 02 Aug 2022 23:40:24 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e28ea4f42ac6baac91e14de0ee8d101956ac6d64c7d4078bb57ebfddde33184`  
		Last Modified: Tue, 02 Aug 2022 23:40:24 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:latest` - linux; mips64le

```console
$ docker pull satosa@sha256:b9bdbc69a8a0be593fe150cbd4334f006447c17a9538b850002e7fa96445593b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.8 MB (205844024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7d3830a289e7a92a0277b60e6cce741d4887ea889e4e236cdd2d878fb1f64b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:10:34 GMT
ADD file:6dc22a1e5b5fcf23f2549406ddcc45c4e244f46e21eafa881de81fa87438e5d8 in / 
# Tue, 02 Aug 2022 01:10:38 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 10:25:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 10:25:08 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 10:25:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:25:36 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 04 Aug 2022 04:16:09 GMT
ENV PYTHON_VERSION=3.10.6
# Thu, 04 Aug 2022 05:33:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Thu, 04 Aug 2022 05:33:24 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 04 Aug 2022 05:33:27 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Thu, 04 Aug 2022 05:33:30 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Thu, 04 Aug 2022 05:33:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Thu, 04 Aug 2022 05:33:35 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Thu, 04 Aug 2022 05:34:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 04 Aug 2022 05:34:30 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 08:35:12 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 08:35:15 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 08:52:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 08:52:17 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 08:52:21 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 08:52:25 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 08:52:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 08:52:34 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 08:52:39 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 08:52:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:88350749a27614c791450c256b051f023d81cdd256211274b1efac493779d2be`  
		Last Modified: Tue, 02 Aug 2022 01:21:02 GMT  
		Size: 29.6 MB (29628964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61130d003a0ea87819935a3a252db1861d9b87e1313fa7988d5f0642637f3e`  
		Last Modified: Tue, 02 Aug 2022 23:46:40 GMT  
		Size: 1.0 MB (1049605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e786491697e5d2bd3dee622f7eae98810c04c895d5024e910e2394f92b37ad8`  
		Last Modified: Thu, 04 Aug 2022 08:14:51 GMT  
		Size: 12.1 MB (12124464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fb1366c066d6bf94df2bf081524439083c14a1f292da85f218000ac515a2f5`  
		Last Modified: Thu, 04 Aug 2022 08:14:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe7637d1173b353af8622199dfbc92d0f74f8cff129fe540541b9c069a058d3`  
		Last Modified: Thu, 04 Aug 2022 08:14:46 GMT  
		Size: 3.1 MB (3120804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4655831cce551d936028a78d3d4a295cd96e3ca02ea0f5f726d0b963350a0e`  
		Last Modified: Thu, 04 Aug 2022 08:53:18 GMT  
		Size: 21.3 MB (21288233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54965dd4effca16f75a92cdac5dd71e708a50d218ca30b0806964a58d8b726ee`  
		Last Modified: Thu, 04 Aug 2022 08:53:58 GMT  
		Size: 138.6 MB (138620211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a449c61594c6b3d2e0fa03d876ebe6fc8561eaa1d46ebf088772a42dea52b596`  
		Last Modified: Thu, 04 Aug 2022 08:53:06 GMT  
		Size: 9.4 KB (9396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54e620f3a05fe34c293ac1de03899ec567f49faa21a8db43216f796387f8f65`  
		Last Modified: Thu, 04 Aug 2022 08:53:06 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:latest` - linux; ppc64le

```console
$ docker pull satosa@sha256:b84ad93ccca31f2ba03b7c0586ad9f3a2d71764d4338922af798ae737ec87f23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212244381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f29a99f45c08fb90c8ad9dec84fd55c14d0ca8ecbc00c2160fc3464a14feca9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 01:17:30 GMT
ADD file:3a95a896d463569ce82199957052b3467123a4bd3385a0a4e397cf08402a99c3 in / 
# Tue, 02 Aug 2022 01:17:32 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:03:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 16:03:13 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 16:03:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 16:03:24 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 18:10:29 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 18:43:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 03 Aug 2022 18:43:03 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 18:43:03 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 18:43:03 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 18:43:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 18:43:04 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 18:43:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 18:43:25 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 21:09:20 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 21:09:21 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 21:14:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 21:14:39 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 21:14:39 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 21:14:40 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 21:14:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 21:14:41 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 21:14:41 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 21:14:42 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5241cd116d6e6e2d62f3d8c2245b74daca9f6cc154eaccd738feb41984c74714`  
		Last Modified: Tue, 02 Aug 2022 01:24:39 GMT  
		Size: 35.3 MB (35272771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf6dcfcb4fa2f4e24ce6bed8b3eda6b0d49d92062cb34d95830e4e9f512270`  
		Last Modified: Wed, 03 Aug 2022 00:14:29 GMT  
		Size: 1.1 MB (1094658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdc50327f93cca5ad2c5f8500471040045b715045a9a4852ece90b3155d5aea`  
		Last Modified: Wed, 03 Aug 2022 20:42:55 GMT  
		Size: 12.5 MB (12473465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49f3fdf44cc1cf9b0e2d32c8ea2b62a0d3eb7eac481b56c9d11e44c66b764fe`  
		Last Modified: Wed, 03 Aug 2022 20:42:52 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd9d6c8cb5530b56f02a736bb1cc24d2d0ffc11d6fb55dc6befb0e114a1ff74`  
		Last Modified: Wed, 03 Aug 2022 20:42:53 GMT  
		Size: 3.3 MB (3336216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209342dd334b280e74196c0e693487033f7f2d08880ab61f5f9113dbbd5d0461`  
		Last Modified: Wed, 03 Aug 2022 21:22:32 GMT  
		Size: 22.2 MB (22158681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11809242e6bd5adbd0096d37646b954f666a1e2a107dd5442773977caa919360`  
		Last Modified: Wed, 03 Aug 2022 21:22:45 GMT  
		Size: 137.9 MB (137896801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa36501b6a1d8ec2e51a6a162f1f43d70ea4b035335513b65b800346790717`  
		Last Modified: Wed, 03 Aug 2022 21:22:27 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fe38c0944e97231334e780f32f3cd041644756c5b195812b19edd697268021`  
		Last Modified: Wed, 03 Aug 2022 21:22:27 GMT  
		Size: 2.1 KB (2113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:latest` - linux; s390x

```console
$ docker pull satosa@sha256:f52b8375aeb8b39ad8ae5b9f05f4f94a47f4776b3f500aeeadee19c4ed572f5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202163420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f253b8b35e8bbaf69f23beb8a8584dc48a0c682127faa17ed9d639b33dfdf3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 08:30:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 08:30:40 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 08:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 08:30:44 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 22:09:42 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 22:18:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 02 Aug 2022 22:18:03 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 22:18:04 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 22:18:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 22:18:13 GMT
CMD ["python3"]
# Tue, 02 Aug 2022 23:28:28 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 02 Aug 2022 23:28:31 GMT
ENV SATOSA_VERSION=8.1.1
# Tue, 02 Aug 2022 23:32:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 02 Aug 2022 23:33:02 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 02 Aug 2022 23:33:02 GMT
WORKDIR /etc/satosa
# Tue, 02 Aug 2022 23:33:02 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Tue, 02 Aug 2022 23:33:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 23:33:02 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 23:33:03 GMT
USER satosa:satosa
# Tue, 02 Aug 2022 23:33:03 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c36d12a9d2aa3bd2ed5880b10e768bae6cab779992e198cf595d3b8d6924d5`  
		Last Modified: Tue, 02 Aug 2022 10:43:27 GMT  
		Size: 1.1 MB (1075771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a2fa2a5f3f4be291fac87451996292e32ad4b6b7e7ae168c720b6501ba676f`  
		Last Modified: Tue, 02 Aug 2022 23:23:49 GMT  
		Size: 11.9 MB (11900903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1958402e81da32fc50ee2b3d3d48a5714015a6589a9b0882e2e0862173874f52`  
		Last Modified: Tue, 02 Aug 2022 23:23:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adc16df778c23094a004c62669c6de553142901db4933d76959d223598473b`  
		Last Modified: Tue, 02 Aug 2022 23:23:49 GMT  
		Size: 3.3 MB (3335624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5f479e9444a18e7100a74300ba30ab5818c9023c386c0a537811de457f1e99`  
		Last Modified: Tue, 02 Aug 2022 23:33:39 GMT  
		Size: 19.6 MB (19580744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573792100821147cd9e469e566ed70175d1fe8ec2b68e371484abc92f0aeaf74`  
		Last Modified: Tue, 02 Aug 2022 23:33:45 GMT  
		Size: 136.6 MB (136618328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cb6a07895307e25b49bb3cdebc3f6e29fef231b0390c00ddacc6b74ee5f9fd`  
		Last Modified: Tue, 02 Aug 2022 23:33:36 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0ce3aebbe275e54928297909f6f1ed7c7beee5c901706ccef91eec96eb8bc5`  
		Last Modified: Tue, 02 Aug 2022 23:33:36 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
