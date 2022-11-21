<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `satosa`

-	[`satosa:8`](#satosa8)
-	[`satosa:8-alpine`](#satosa8-alpine)
-	[`satosa:8-alpine3.16`](#satosa8-alpine316)
-	[`satosa:8-bullseye`](#satosa8-bullseye)
-	[`satosa:8.2`](#satosa82)
-	[`satosa:8.2-alpine`](#satosa82-alpine)
-	[`satosa:8.2-alpine3.16`](#satosa82-alpine316)
-	[`satosa:8.2-bullseye`](#satosa82-bullseye)
-	[`satosa:8.2.0`](#satosa820)
-	[`satosa:8.2.0-alpine`](#satosa820-alpine)
-	[`satosa:8.2.0-alpine3.16`](#satosa820-alpine316)
-	[`satosa:8.2.0-bullseye`](#satosa820-bullseye)
-	[`satosa:alpine`](#satosaalpine)
-	[`satosa:alpine3.16`](#satosaalpine316)
-	[`satosa:bullseye`](#satosabullseye)
-	[`satosa:latest`](#satosalatest)

## `satosa:8`

```console
$ docker pull satosa@sha256:920b2db648258e4779443b954cbc17015f3e7feda80d41ee006fdf102363bce8
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

### `satosa:8` - linux; amd64

```console
$ docker pull satosa@sha256:2b75f1966b97e958ab7b3edb499a68b28221198f61990a4e20b66bf461a02dfb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87754433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da994718d5841d288b6e518373ab9111b96651fc972c162c8ec1e737bb52fd08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 18:54:42 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 18:54:42 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 18:54:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 20:02:05 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 20:02:05 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 20:16:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 20:16:53 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 20:16:53 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 20:16:53 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:55:31 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:55:32 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:55:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:55:42 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:27:35 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:27:35 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:28:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:28:36 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:28:36 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:28:36 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:28:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:28:36 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:28:36 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:28:36 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00aaacf759c581712fa578a6b4e8e0b9fc780919a5d835a168457b754755644`  
		Last Modified: Tue, 15 Nov 2022 22:58:09 GMT  
		Size: 1.1 MB (1077982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b9691827181afb85e2027be1b34b948a9de4110f0253de4e0c9dfcf1559f7b`  
		Last Modified: Tue, 15 Nov 2022 22:59:24 GMT  
		Size: 12.6 MB (12586017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf69ec4fb1d1d974ad18c827b094bb4a4242791b94344e6f059ed9d0b8eb62be`  
		Last Modified: Tue, 15 Nov 2022 22:59:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7bf64971b8ca870b8bc8476ffc783c777f6bb3bb53e50d8e719f1ea1bad697`  
		Last Modified: Wed, 16 Nov 2022 07:04:31 GMT  
		Size: 3.3 MB (3348953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c001071f815bdbd3fc5e231343c0b4b3337b9d339bd507162ce825aa8eff5643`  
		Last Modified: Mon, 21 Nov 2022 19:29:13 GMT  
		Size: 21.1 MB (21096341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c4d15fc7d1e06ddff844be580c929a202aeef96ed8cb426f2e1f60c6291d80`  
		Last Modified: Mon, 21 Nov 2022 19:29:14 GMT  
		Size: 18.2 MB (18220647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6220bf882cf516ac06374d47fe5f7eb9cb8ac7207c16648c87262453bcb5dd`  
		Last Modified: Mon, 21 Nov 2022 19:29:10 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9610156b7a28fe2c40ba7509e651e32b895a71e7c2999362f9d0dcdefefc7830`  
		Last Modified: Mon, 21 Nov 2022 19:29:10 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8` - linux; arm variant v5

```console
$ docker pull satosa@sha256:191432b034c13284a7a750492dc4bbbaab7cbdab72b127ccdc3276685c0a6277
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.3 MB (374337256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddea723e3d8081cb37968943d59ce80b13516d5314627468f2f689ac477edb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:49:18 GMT
ADD file:1949af7e583a1b54055a421129c32315fc101e53e2cda05da3171ed461bde0a6 in / 
# Tue, 15 Nov 2022 01:49:19 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:45:56 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 07:45:56 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 07:46:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 08:28:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 08:28:59 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 08:51:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 08:51:04 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 08:51:04 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 08:51:04 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:33:16 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:33:16 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:33:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:33:32 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:48:45 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:48:45 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:53:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:53:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:53:25 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:53:26 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:53:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:53:26 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:53:26 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:53:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b56836d864a6d857be3d12242b65962f2a2cf0d77c48cfb85bbbdf9d56a7e93d`  
		Last Modified: Tue, 15 Nov 2022 01:54:26 GMT  
		Size: 28.9 MB (28914126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a6e5b3ab314e2965853a4ddc03100cfb0fd0d2825cdc2fb4f1bc363cca39b9`  
		Last Modified: Tue, 15 Nov 2022 10:08:43 GMT  
		Size: 1.1 MB (1060732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db96a74ae1eb60de22f4973a045a1b638a39090565ee2fdf0d4a8c4319bf21c`  
		Last Modified: Tue, 15 Nov 2022 10:09:24 GMT  
		Size: 12.1 MB (12146339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb7e08f0a09cbc7e1269f3c705f9ff28966afe27388fc990a03c00f3200360a`  
		Last Modified: Tue, 15 Nov 2022 10:09:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdc4079d02fdf319fd5aa22d26a4a8b2ec80e3f8beb0ada18ed0aa2ace5e0d7`  
		Last Modified: Wed, 16 Nov 2022 00:39:40 GMT  
		Size: 3.3 MB (3348246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0106290c3f2418d61678711f86fda97637dff84ccfae811034f743dcae2eb8`  
		Last Modified: Mon, 21 Nov 2022 19:54:08 GMT  
		Size: 22.7 MB (22693132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745925b8b4315a2b9b975665bd6158b73df587417a7fade9559f85ddfc27139d`  
		Last Modified: Mon, 21 Nov 2022 19:54:31 GMT  
		Size: 306.2 MB (306162846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c0f3ca52005fb9ed30e05bac90f93fbd6237467e4145b4950ac388200c78fc`  
		Last Modified: Mon, 21 Nov 2022 19:54:04 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15ae5fb82b045c21046c703a63283b8053930321884f0aa7174a12966b6fb46`  
		Last Modified: Mon, 21 Nov 2022 19:54:04 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8` - linux; arm variant v7

```console
$ docker pull satosa@sha256:c31d3aa2b933736a4d50e795d7d017bdbe9163970108978759602cc4b09333de
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.1 MB (371088257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d8463fe00f06c45603677eff859db0d7b45fc077a01e06584c25b28d75a300`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 03:43:25 GMT
ADD file:1b5c939bd2a35667d7fc44c3009a56ed92a932f512a73df1617dec6ccbd6e6b1 in / 
# Tue, 15 Nov 2022 03:43:26 GMT
CMD ["bash"]
# Wed, 16 Nov 2022 02:10:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Nov 2022 02:10:52 GMT
ENV LANG=C.UTF-8
# Wed, 16 Nov 2022 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Nov 2022 04:26:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 16 Nov 2022 04:26:07 GMT
ENV PYTHON_VERSION=3.11.0
# Wed, 16 Nov 2022 04:47:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 16 Nov 2022 04:47:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_PIP_VERSION=22.3
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 04:47:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 04:47:40 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:58:12 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:58:13 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 20:02:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 20:02:37 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 20:02:37 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 20:02:38 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 20:02:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 20:02:38 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 20:02:38 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 20:02:38 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:fd18d0201d0ce0c5e103902d894f5d601fc5dde76688aa7dae786840141d23e4`  
		Last Modified: Tue, 15 Nov 2022 03:50:11 GMT  
		Size: 26.6 MB (26576195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f4e2c2480160d1670c2ebb7d1c8290f0a3956265f0069d1de3e5b60d587141`  
		Last Modified: Wed, 16 Nov 2022 08:13:53 GMT  
		Size: 1.0 MB (1042833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9254168af81f2bf98cb621d697e2b624446620a5acce3412a20ed6f6912fd248`  
		Last Modified: Wed, 16 Nov 2022 08:15:35 GMT  
		Size: 11.6 MB (11642276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a40d929533b6fb9173ac38ebf09de1f187f9aa8c6b49de778a38b52abbda11`  
		Last Modified: Wed, 16 Nov 2022 08:15:33 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b04522957691b19b0ac6940e157f56337b27084782602ad4d8a7229397944e1`  
		Last Modified: Wed, 16 Nov 2022 08:15:34 GMT  
		Size: 3.3 MB (3348201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978ebe46f9e524ab17da6008d165ad70ca5187930fb4cd7fc6cd17cccbe7002e`  
		Last Modified: Mon, 21 Nov 2022 20:03:41 GMT  
		Size: 22.4 MB (22430741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa27795d0d8f0524db63e5fbf00dcc9ac44cfeb68c3a66350870d3c3e903fe9`  
		Last Modified: Mon, 21 Nov 2022 20:04:05 GMT  
		Size: 306.0 MB (306036175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5483a349efd69231e68a3b2f9212afd52f92c5498da8c707b5a60f90db6399a`  
		Last Modified: Mon, 21 Nov 2022 20:03:37 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa6d2f8593d4d5bca10332fd90d782e457560c6a50b6fd53614a5eb88d04109`  
		Last Modified: Mon, 21 Nov 2022 20:03:37 GMT  
		Size: 2.1 KB (2144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:a654eeeefb6f573740cf6dc83bc68eb3ff1ad0e4ab660417964ee9664772c6a9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85480362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa7f1d11b3d6d0006e3d3dce2de48cfc52f63ddd139cfddfd1a79675972969b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:41:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 07:41:31 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 07:41:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 08:34:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 08:34:07 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 08:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 08:47:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 08:47:37 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 08:47:37 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:17:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:17:57 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:18:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:18:07 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:49:25 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:49:25 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:50:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:50:21 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:50:21 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:50:21 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:50:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:50:21 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:50:21 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:50:21 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbd8719487c40bfcc7d42d53f202d1dbbbb7ac0fb4e4919ed791664b7f4e47b`  
		Last Modified: Tue, 15 Nov 2022 10:55:04 GMT  
		Size: 1.1 MB (1065870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb07c67a71797e21118367f8ed3ec8f9561b4e4e3f662aed2467c97a93a6dc3f`  
		Last Modified: Tue, 15 Nov 2022 10:56:03 GMT  
		Size: 12.6 MB (12637055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130567c01926a008d097f8a10e6c4348f8cf6f6bae2df7860e1ebad57caf457d`  
		Last Modified: Tue, 15 Nov 2022 10:56:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad488014eea42b129f9a60d9258bfd09ddf59c75a5ccdc55e196cc0eef88cfe`  
		Last Modified: Wed, 16 Nov 2022 01:26:28 GMT  
		Size: 3.3 MB (3348606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cc72b0c430a3bd0d92649200cd8c6da867ea3a7f33b5066d9b8bae085c587c`  
		Last Modified: Mon, 21 Nov 2022 19:50:50 GMT  
		Size: 21.0 MB (20975486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c84b4c195beedd08e708b18de7f11a9e87d3ac3ef1bed9904140963320cb472`  
		Last Modified: Mon, 21 Nov 2022 19:50:50 GMT  
		Size: 17.4 MB (17380880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15489ffd1801184e8a797e1467fb0a83eec71433d9efe85b7fcc060f9c77547`  
		Last Modified: Mon, 21 Nov 2022 19:50:47 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6345651cb201b249a31896d42f4f630bd5f4ee5dc259842a415b1e1d21bc36ab`  
		Last Modified: Mon, 21 Nov 2022 19:50:47 GMT  
		Size: 2.1 KB (2141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8` - linux; 386

```console
$ docker pull satosa@sha256:34866c133ed80b3650fcac32e7f67597fa1598e16fc84e51e0e8ee340d0e6ca9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 MB (380177011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25aed64d35227d6dd9deb0905d3a0f76dc6e28a9ce7465ec44f6985baf78563`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:27 GMT
ADD file:608bec4ba3e2543714da4c5158f3c46a168f63ee69ac3f48bff54474ba9a6f27 in / 
# Tue, 15 Nov 2022 01:41:27 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 12:57:10 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 12:57:11 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 12:57:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:13:48 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 14:13:49 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 14:32:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 14:32:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 14:32:38 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 14:32:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:37:29 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:37:29 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:37:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:37:42 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:39:08 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:39:08 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:43:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:43:23 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:43:23 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:43:25 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:43:26 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:43:27 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:43:28 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f6a1e975b34444ecb7c6a2b537403fd6b94d2ff3225944ac2ac3b292466e4078`  
		Last Modified: Tue, 15 Nov 2022 01:47:05 GMT  
		Size: 32.4 MB (32392982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a4ead92cc7eae0396b0fbac1238e0bee3f677740a65a67474e08bcbaa003ba`  
		Last Modified: Tue, 15 Nov 2022 17:38:22 GMT  
		Size: 884.5 KB (884461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd0f4ed85c962a057d2c2667c8b4e1a210aea5e2c9e68520214eb87926f684e`  
		Last Modified: Tue, 15 Nov 2022 19:31:55 GMT  
		Size: 12.7 MB (12683309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72250ba4c687654d3be8943b7bf9591f4dc5de08989c26f5654409682ffbdbfd`  
		Last Modified: Tue, 15 Nov 2022 19:31:53 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ffce336712f2fe573ad63960925a12291df3e7598c36c326698f1308f9caae`  
		Last Modified: Wed, 16 Nov 2022 01:51:48 GMT  
		Size: 3.1 MB (3132128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab52fcbbc37aab1d08731873c11e68396df78043d92d74c7faa4c5b09467c928`  
		Last Modified: Mon, 21 Nov 2022 19:44:19 GMT  
		Size: 24.1 MB (24065495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc904879f9ede6886b46d646fa18a746d32afacfe68d200cbd6259eb315d64a5`  
		Last Modified: Mon, 21 Nov 2022 19:44:46 GMT  
		Size: 307.0 MB (307006821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debe7b65c57d841640da19f01ceedfd6f2d319eabb09c1027621317ab5e75159`  
		Last Modified: Mon, 21 Nov 2022 19:44:15 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ea23efc09b0e6df59a86e0ce421416ed60dbfd3ee8016fdf2d744574b117cd`  
		Last Modified: Mon, 21 Nov 2022 19:44:15 GMT  
		Size: 2.1 KB (2143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8` - linux; ppc64le

```console
$ docker pull satosa@sha256:aa91656e4b6a0f6b51aa29a1219617190b462ee7f8b0f25fddd786c831f542f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.5 MB (382489126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88774150f37054a63d09106df180126b080812678a23cfb365f6c4c5fcd1ec22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 05:18:45 GMT
ADD file:520926164fdc762143905745329e568c67289232bec450e48645d82a4613dccf in / 
# Tue, 15 Nov 2022 05:18:47 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:06:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 13:06:51 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 13:07:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:38:22 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 14:38:22 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 15:25:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 15:25:30 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 15:25:31 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 15:25:31 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:27:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:27:46 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:28:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:28:07 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:17:24 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:17:25 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:24:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:24:32 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:24:32 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:24:33 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:24:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:24:33 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:24:34 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:24:34 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:c57913b7d0318ef1a47f0348ce54d9865316776aa1ffb2c7871b1473b3d29407`  
		Last Modified: Tue, 15 Nov 2022 05:24:22 GMT  
		Size: 35.3 MB (35285140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa173aadf3e5fa326d1f1b9f9263051781dc9833e8b60e5bb5a9a994739e18ee`  
		Last Modified: Tue, 15 Nov 2022 17:58:02 GMT  
		Size: 1.1 MB (1096202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2c11a6d1874c9a04e310b3de6f884a5db20d8b2819f963dfbb87d255d4041d`  
		Last Modified: Tue, 15 Nov 2022 17:58:54 GMT  
		Size: 13.0 MB (12955764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53510645cb4e75dba43f2960e61295b7e4092e32b65c05d78e4a222a1035b0`  
		Last Modified: Tue, 15 Nov 2022 17:58:50 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76a75d59183d172f23c152a8f9b934d52c2bbe4e381b7d98e6254342b65c9ad`  
		Last Modified: Wed, 16 Nov 2022 07:01:30 GMT  
		Size: 3.3 MB (3349130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789086c936cb86df67a1bcdf02c069f46030c960a874385b1c09458ea09c9e28`  
		Last Modified: Mon, 21 Nov 2022 19:25:29 GMT  
		Size: 23.6 MB (23636418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf604bdc50ad0b740586882da17fa028eb433f3e9291ae1752d62a62443a5dbd`  
		Last Modified: Mon, 21 Nov 2022 19:25:54 GMT  
		Size: 306.2 MB (306154608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24af618620347663fdfc4357acbffd238b3cc0a2d84703ef629fe73ef009c9bf`  
		Last Modified: Mon, 21 Nov 2022 19:25:23 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b025a5ca25095fb82fa5f084b355cf1b4387400fe727ec454daad74044e9445`  
		Last Modified: Mon, 21 Nov 2022 19:25:23 GMT  
		Size: 2.1 KB (2143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8` - linux; s390x

```console
$ docker pull satosa@sha256:11d52a081306682d815a39f964424df846d178a0cd0e043c4c6392ff3f219e6a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.2 MB (375225534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec1f645b1f322cd61afb287021cc9f964eccaaecf3250c047df64b92f392d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 10:52:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 10:52:16 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 10:52:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 11:31:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 11:31:14 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 11:46:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 11:46:18 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 11:46:19 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 11:46:19 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:47:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:47:51 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:48:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:48:06 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:42:07 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:42:08 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:46:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:46:10 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:46:10 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:46:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:46:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:46:10 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:46:10 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:46:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1487a90d7d45334f92d990a52e5750391ed66b11532972979f0792745cedca`  
		Last Modified: Tue, 15 Nov 2022 13:07:54 GMT  
		Size: 1.1 MB (1077428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81becff7fb0cea099dc76445874abd672598812e9ae8fb990ce90a07971a00c2`  
		Last Modified: Tue, 15 Nov 2022 13:08:34 GMT  
		Size: 12.4 MB (12422163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e82170644b3fad2be2ca3ce0cd517e5487772520f4eccaf5e60ce99b9533cf`  
		Last Modified: Tue, 15 Nov 2022 13:08:32 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8aa6e35e336a7de98329dc7ecba62f34a24d5eacb447feafcaac381b01a578`  
		Last Modified: Wed, 16 Nov 2022 00:58:52 GMT  
		Size: 3.3 MB (3348811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55521d94cc6014114d16684de5cf415a987eb5306bb707b2c9c89612bae7434`  
		Last Modified: Mon, 21 Nov 2022 19:46:42 GMT  
		Size: 21.0 MB (21008499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453920ba520592eb4a4712ce352cacced35e45b4c29dc9ba96af152f4263f10a`  
		Last Modified: Mon, 21 Nov 2022 19:46:54 GMT  
		Size: 307.7 MB (307712990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b654413945b74c59b340cba2b01bbd308650ac51a2cefcaede178af5de4e030`  
		Last Modified: Mon, 21 Nov 2022 19:46:39 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a8d82d6fccb2478507a3f5986cf0cf8538a12e3f01d8780e85ed975218703`  
		Last Modified: Mon, 21 Nov 2022 19:46:40 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8-alpine`

```console
$ docker pull satosa@sha256:96837510b982a984c0f69c23c7424082c1030cd0ca1de70f3a1dda2d5e3a9688
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
$ docker pull satosa@sha256:6e3e4da73ae0c0d1ee3192a90d4e47dd1711df0f3e2d5cda5ec9b5d0146dc48b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c03699dd38f4ddbe3655ace3de96f6a1cef874a71cdabefd8c2f24970096df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:56:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 06:39:07 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 06:39:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 06:57:28 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 06:57:28 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 07:15:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 07:15:59 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 07:15:59 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 07:15:59 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:56:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:56:08 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:56:15 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:56:15 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:22:15 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:22:15 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:22:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:23:00 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:23:00 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:23:00 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:23:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:23:01 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:23:01 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:23:01 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e124a36b9ab9caae9b9b43bffcb6f6d9f126ab89cf2a8b20b9a6f912df03d36`  
		Last Modified: Sat, 12 Nov 2022 07:47:59 GMT  
		Size: 661.8 KB (661831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86456952aa287ca80ac7d7f349dc9edbabda9393ab022d20f2e4c2263cd7d2e7`  
		Last Modified: Sat, 12 Nov 2022 07:48:26 GMT  
		Size: 13.0 MB (12998794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ece9ef7a5797feb2ddaf23aee223848643c0baaedaaa203c721aecb6b272b25`  
		Last Modified: Sat, 12 Nov 2022 07:48:24 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef27b859822294ab1253f8e09a8712d63ea9939eadd1dc4b595d52726c0b020d`  
		Last Modified: Wed, 16 Nov 2022 07:05:43 GMT  
		Size: 3.1 MB (3056443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824935fc626e0971164be442423360798c85d529053e967a909cd1273bda190e`  
		Last Modified: Fri, 18 Nov 2022 18:23:39 GMT  
		Size: 10.9 MB (10872324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fed4aaf1a18111683af619a1e71edd5804307567ed23a83f6f40d15d2794af`  
		Last Modified: Fri, 18 Nov 2022 18:23:41 GMT  
		Size: 17.4 MB (17363712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e090e2c9c7e5d74822d9f71487ec5a71f3058a6f2d8bf756ddaaed8180da06e`  
		Last Modified: Fri, 18 Nov 2022 18:23:38 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41247ef96bde894139c620ba77d7e56bed539612bc8605d4495a7b78bd90ebfb`  
		Last Modified: Fri, 18 Nov 2022 18:23:38 GMT  
		Size: 2.1 KB (2146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine` - linux; arm variant v6

```console
$ docker pull satosa@sha256:a6fbc6091cf0e1a4e5f6e3d7f2cb1e798e64a2324ff1c80eb9d46b342c11fd39
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327070023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313e9fa4c6d8a5fe836e6b47a9dcef3b27b5b56032c637bb8c15c6c2ecaba99b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:28:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 06:28:49 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 06:28:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 06:55:00 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 06:55:00 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 07:21:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 07:21:39 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 07:21:39 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 07:21:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:41:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:41:32 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:41:39 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:41:39 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:49:39 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:49:39 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:54:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:54:44 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:54:44 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:54:44 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:54:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:54:44 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:54:44 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:54:44 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe974d15ab7b1ace1e4997a68bcfb22f2652af9f902f110d0a90fbdd2ef2053`  
		Last Modified: Sat, 12 Nov 2022 08:03:00 GMT  
		Size: 666.2 KB (666196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69683a8852c8900b94150a78af049bb63d4f73fbdd7239fba1302b9b211ec82`  
		Last Modified: Sat, 12 Nov 2022 08:03:24 GMT  
		Size: 12.5 MB (12545209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63725fb700eaa74dc7942aef8ee5d333eb6b74e224f29ff11f0a997c56208595`  
		Last Modified: Sat, 12 Nov 2022 08:03:22 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012ec3c62fe317e21430242a858a7e489044f55ef1b0398a0c40d9b08e49a357`  
		Last Modified: Wed, 16 Nov 2022 00:46:22 GMT  
		Size: 3.1 MB (3056167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f055f28d65cb7615e57588e003562504a3430b08b6f6e1b13afde191879907f`  
		Last Modified: Fri, 18 Nov 2022 18:55:21 GMT  
		Size: 9.7 MB (9749625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328dee8fb8e4a3a68d2eaea6c4b4eee56bed5bf0e214820a5f81312650be64cf`  
		Last Modified: Fri, 18 Nov 2022 18:55:46 GMT  
		Size: 298.4 MB (298425888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15eaa52f90ffd951ff72991440bbf786b70e29887c6aac6337a8a778504b135e`  
		Last Modified: Fri, 18 Nov 2022 18:55:19 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7997f2f2f20f25fc39c97114744f2d8d8bf61520dcf9641712b83c710b9c87f4`  
		Last Modified: Fri, 18 Nov 2022 18:55:19 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine` - linux; arm variant v7

```console
$ docker pull satosa@sha256:3bae4cd91de90ed4b33d66d1f77a22cd0b9fcd0ab1b4eaef2cff5417c9275733
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325957233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f631246a1547940b3f84d445fda67d7237809b05753009f90e9037abebd08a84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:12:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 08:12:04 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 08:12:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 08:38:23 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 08:38:23 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 09:08:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 09:08:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 09:08:09 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 09:08:09 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 05:31:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 05:31:37 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 05:31:43 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 05:31:44 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 19:02:52 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 19:02:52 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 19:07:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 19:07:42 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 19:07:42 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 19:07:43 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 19:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 19:07:43 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 19:07:43 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 19:07:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb04c1ebc7f7005f359b85d4698d031de9ca4a4e8bc776ac6faa3f052b3a3f1`  
		Last Modified: Sat, 12 Nov 2022 10:03:05 GMT  
		Size: 659.3 KB (659291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997ef90ff733ebe7a201a71b832a552bd33839b74047f89bc3f1f00139c6e629`  
		Last Modified: Sat, 12 Nov 2022 10:03:50 GMT  
		Size: 12.0 MB (11996460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2e907876797a7e7631369ff616b83ed0b57d0c152d486322351a767e140814`  
		Last Modified: Sat, 12 Nov 2022 10:03:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0291337573b1029d149b2fca6ebe6b0b3601a0d0f5eaecc06c1e75696f8c6731`  
		Last Modified: Wed, 16 Nov 2022 08:16:48 GMT  
		Size: 3.1 MB (3056225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8f69cf77b68a4b6e967edd1ed5cebd3eda7ce3b4c37d3cc3c6c80941a0509`  
		Last Modified: Fri, 18 Nov 2022 19:09:23 GMT  
		Size: 9.5 MB (9499491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63ac0856d1f8f6029e19cbd1091942b95aa2bf50d51d2e6be43d3fbe7f3bb7d`  
		Last Modified: Fri, 18 Nov 2022 19:09:51 GMT  
		Size: 298.3 MB (298315139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8470d03ed17d2c6c783bb46ad242efce0cc3f549f5b98e001e42fda3b56824b8`  
		Last Modified: Fri, 18 Nov 2022 19:09:21 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598946608775d3c0df6899c4da0bfec0d2ef162decc5c884d73764d4a72f6789`  
		Last Modified: Fri, 18 Nov 2022 19:09:21 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:2c93dd162547b7b44c8202cf0599e16fb7d2a686c396e6130f122c1b3f61dc4e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46167316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4ccc5a457a36ea94161437a8f9f5053f0e75d381326a3d6a0d8e1e91cc02a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:23:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 08:16:58 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 08:16:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 08:35:03 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 08:35:03 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 08:53:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 08:53:19 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 08:53:19 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 08:53:19 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:18:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:18:37 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:18:42 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:18:42 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:48:20 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:48:20 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:49:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:49:01 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:49:01 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:49:01 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:49:01 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:49:01 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:49:01 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e190eeb0612a6514b857c64886ec8f64d8e235210be5682cf6abbc5bd172b135`  
		Last Modified: Sat, 12 Nov 2022 09:21:43 GMT  
		Size: 663.1 KB (663101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4727b51eed627eface71c55490f3017153992b7d9ae395a99b1e11841128d06`  
		Last Modified: Sat, 12 Nov 2022 09:22:08 GMT  
		Size: 13.1 MB (13073328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce34a3004b391575b577e7922f6d501a0b8ba079dc0741b068b86558c26ee4a1`  
		Last Modified: Sat, 12 Nov 2022 09:22:06 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c270266b6f1942f4120af4ec7278184a61adb708209c33c2320154d82f8a31`  
		Last Modified: Wed, 16 Nov 2022 01:27:26 GMT  
		Size: 3.1 MB (3056436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286cee3bdb5335ff6bca12b16beabdce685e5fdb0a9d0561b1e6cb24ba774152`  
		Last Modified: Fri, 18 Nov 2022 18:49:43 GMT  
		Size: 9.7 MB (9699369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fc21cbba39c03767e72e06461ef113f17eae2671200bbff9598e569d7b5be7`  
		Last Modified: Fri, 18 Nov 2022 18:49:45 GMT  
		Size: 17.0 MB (16955466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5513e43b833e2f30026902bd7a4a1af1addd71ecb1736426f8252fc49d442006`  
		Last Modified: Fri, 18 Nov 2022 18:49:43 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed37a61b2c4a8b46b1ab69bf0c36dcccc4b0e44802a41f019fcb2efd750418a3`  
		Last Modified: Fri, 18 Nov 2022 18:49:42 GMT  
		Size: 2.1 KB (2145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine` - linux; 386

```console
$ docker pull satosa@sha256:2db0679167412bbbf2ab4702b8580f18935847abe845bb15e8472bda6204190d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328240269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9c562b6c31c0440d0e58b8f9b031c6bcbb90cb33beb9032c8b3544236d5c33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:29:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 05:29:12 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 05:29:14 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 05:50:43 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 05:50:44 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 06:11:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 06:11:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 06:11:39 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 06:11:40 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:38:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:38:28 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:38:35 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:38:36 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:43:42 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:43:43 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:47:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:47:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:47:55 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:47:57 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:47:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:47:58 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:47:59 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:48:00 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a152a67ad9fd5011f8da356e104e14cdbd9cd925941bb6c241b50471eef5a520`  
		Last Modified: Sat, 12 Nov 2022 06:51:44 GMT  
		Size: 669.6 KB (669609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81c595fa967dddaa2db39bd0328b1e7e07583641e9870975cc6d7f37a54f069`  
		Last Modified: Sat, 12 Nov 2022 06:52:19 GMT  
		Size: 13.2 MB (13163166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8750f6265e3be5e75d2d9bb8766f7ae3208bd6ec29a99ab721971a438e8692`  
		Last Modified: Sat, 12 Nov 2022 06:52:17 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c32efb655c88520610dfffc30bc04d2a99130cbac9bd50f8f43c0a37aef6d28`  
		Last Modified: Wed, 16 Nov 2022 01:52:46 GMT  
		Size: 3.1 MB (3054164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e426180bebf4c41e9095922812af13b228b8a1891f925b18c6418706d09d589c`  
		Last Modified: Fri, 18 Nov 2022 18:49:32 GMT  
		Size: 10.0 MB (9981921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35638e3376e5dee654e447a8aded8def08d009dc15a9a6492ea89f0f6cf991d`  
		Last Modified: Fri, 18 Nov 2022 18:49:48 GMT  
		Size: 298.6 MB (298551244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed3a4f7081736c94dcc732f68489dc73f4dbfb0033bb1565e56218bf56e0eba`  
		Last Modified: Fri, 18 Nov 2022 18:49:31 GMT  
		Size: 9.4 KB (9437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84eedc2257c4e9334b63cca383a14503a49dcd221ab8e62a83dd2811a1c87895`  
		Last Modified: Fri, 18 Nov 2022 18:49:31 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine` - linux; ppc64le

```console
$ docker pull satosa@sha256:78f6a669461f794f0b3dd8e4ed981afb6864275142dd4e3e84b2c9d9e502f748
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328360558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c362cb6cae301a29e6e4675274c3ec62a3fab9aa0ca147eb8167fb57c2d3c92e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 09:09:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 09:09:52 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 09:09:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 09:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 09:49:13 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 10:29:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 10:29:46 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 10:29:47 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 10:29:47 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:28:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:28:15 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:28:26 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:28:27 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:25:31 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:25:31 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:33:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:34:00 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:34:01 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:34:01 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:34:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:34:02 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:34:02 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:34:02 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0578c681eac19aa83cc60a5d383147a7c56a35a3ac13286945daa470f25157e`  
		Last Modified: Sat, 12 Nov 2022 11:31:49 GMT  
		Size: 670.3 KB (670297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bcec55fc14204d6d5b10511d2dcb4b565f19ea0c07a815947bf4616259786f`  
		Last Modified: Sat, 12 Nov 2022 11:32:23 GMT  
		Size: 13.3 MB (13307557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd9e47c00af72c31f09498bcdbb9f23c6b599d96b3262a847fd18af79d8ec83`  
		Last Modified: Sat, 12 Nov 2022 11:32:20 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbba60b66096fca5cbb93d7c032bf2aa7755ea3c73fcddca01bb6d3af1fb0f86`  
		Last Modified: Wed, 16 Nov 2022 07:01:58 GMT  
		Size: 3.1 MB (3056418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59aba7b954790c375454d90d43b7e21ef374bf3fc2cfbca50b660cb08066a22b`  
		Last Modified: Fri, 18 Nov 2022 18:35:37 GMT  
		Size: 10.0 MB (9950742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840cb6e59e4841e4831f3736de75cdf2d9a9d41a587a37d4f6eb185bc212f816`  
		Last Modified: Fri, 18 Nov 2022 18:36:05 GMT  
		Size: 298.6 MB (298562127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605fa8f9b6826c59c0ecc11cc54f8a7a6193c33cee3839935c7409ec2c4bd610`  
		Last Modified: Fri, 18 Nov 2022 18:35:34 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f7512564d5a154d9f72c5ff30f44cfb66410e160250b0ffba25e4abaaaacd1`  
		Last Modified: Fri, 18 Nov 2022 18:35:34 GMT  
		Size: 2.2 KB (2151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8-alpine3.16`

```console
$ docker pull satosa@sha256:96837510b982a984c0f69c23c7424082c1030cd0ca1de70f3a1dda2d5e3a9688
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
$ docker pull satosa@sha256:6e3e4da73ae0c0d1ee3192a90d4e47dd1711df0f3e2d5cda5ec9b5d0146dc48b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c03699dd38f4ddbe3655ace3de96f6a1cef874a71cdabefd8c2f24970096df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:56:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 06:39:07 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 06:39:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 06:57:28 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 06:57:28 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 07:15:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 07:15:59 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 07:15:59 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 07:15:59 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:56:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:56:08 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:56:15 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:56:15 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:22:15 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:22:15 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:22:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:23:00 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:23:00 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:23:00 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:23:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:23:01 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:23:01 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:23:01 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e124a36b9ab9caae9b9b43bffcb6f6d9f126ab89cf2a8b20b9a6f912df03d36`  
		Last Modified: Sat, 12 Nov 2022 07:47:59 GMT  
		Size: 661.8 KB (661831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86456952aa287ca80ac7d7f349dc9edbabda9393ab022d20f2e4c2263cd7d2e7`  
		Last Modified: Sat, 12 Nov 2022 07:48:26 GMT  
		Size: 13.0 MB (12998794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ece9ef7a5797feb2ddaf23aee223848643c0baaedaaa203c721aecb6b272b25`  
		Last Modified: Sat, 12 Nov 2022 07:48:24 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef27b859822294ab1253f8e09a8712d63ea9939eadd1dc4b595d52726c0b020d`  
		Last Modified: Wed, 16 Nov 2022 07:05:43 GMT  
		Size: 3.1 MB (3056443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824935fc626e0971164be442423360798c85d529053e967a909cd1273bda190e`  
		Last Modified: Fri, 18 Nov 2022 18:23:39 GMT  
		Size: 10.9 MB (10872324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fed4aaf1a18111683af619a1e71edd5804307567ed23a83f6f40d15d2794af`  
		Last Modified: Fri, 18 Nov 2022 18:23:41 GMT  
		Size: 17.4 MB (17363712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e090e2c9c7e5d74822d9f71487ec5a71f3058a6f2d8bf756ddaaed8180da06e`  
		Last Modified: Fri, 18 Nov 2022 18:23:38 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41247ef96bde894139c620ba77d7e56bed539612bc8605d4495a7b78bd90ebfb`  
		Last Modified: Fri, 18 Nov 2022 18:23:38 GMT  
		Size: 2.1 KB (2146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine3.16` - linux; arm variant v6

```console
$ docker pull satosa@sha256:a6fbc6091cf0e1a4e5f6e3d7f2cb1e798e64a2324ff1c80eb9d46b342c11fd39
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327070023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313e9fa4c6d8a5fe836e6b47a9dcef3b27b5b56032c637bb8c15c6c2ecaba99b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:28:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 06:28:49 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 06:28:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 06:55:00 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 06:55:00 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 07:21:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 07:21:39 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 07:21:39 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 07:21:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:41:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:41:32 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:41:39 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:41:39 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:49:39 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:49:39 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:54:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:54:44 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:54:44 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:54:44 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:54:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:54:44 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:54:44 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:54:44 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe974d15ab7b1ace1e4997a68bcfb22f2652af9f902f110d0a90fbdd2ef2053`  
		Last Modified: Sat, 12 Nov 2022 08:03:00 GMT  
		Size: 666.2 KB (666196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69683a8852c8900b94150a78af049bb63d4f73fbdd7239fba1302b9b211ec82`  
		Last Modified: Sat, 12 Nov 2022 08:03:24 GMT  
		Size: 12.5 MB (12545209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63725fb700eaa74dc7942aef8ee5d333eb6b74e224f29ff11f0a997c56208595`  
		Last Modified: Sat, 12 Nov 2022 08:03:22 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012ec3c62fe317e21430242a858a7e489044f55ef1b0398a0c40d9b08e49a357`  
		Last Modified: Wed, 16 Nov 2022 00:46:22 GMT  
		Size: 3.1 MB (3056167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f055f28d65cb7615e57588e003562504a3430b08b6f6e1b13afde191879907f`  
		Last Modified: Fri, 18 Nov 2022 18:55:21 GMT  
		Size: 9.7 MB (9749625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328dee8fb8e4a3a68d2eaea6c4b4eee56bed5bf0e214820a5f81312650be64cf`  
		Last Modified: Fri, 18 Nov 2022 18:55:46 GMT  
		Size: 298.4 MB (298425888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15eaa52f90ffd951ff72991440bbf786b70e29887c6aac6337a8a778504b135e`  
		Last Modified: Fri, 18 Nov 2022 18:55:19 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7997f2f2f20f25fc39c97114744f2d8d8bf61520dcf9641712b83c710b9c87f4`  
		Last Modified: Fri, 18 Nov 2022 18:55:19 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine3.16` - linux; arm variant v7

```console
$ docker pull satosa@sha256:3bae4cd91de90ed4b33d66d1f77a22cd0b9fcd0ab1b4eaef2cff5417c9275733
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325957233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f631246a1547940b3f84d445fda67d7237809b05753009f90e9037abebd08a84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:12:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 08:12:04 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 08:12:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 08:38:23 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 08:38:23 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 09:08:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 09:08:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 09:08:09 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 09:08:09 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 05:31:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 05:31:37 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 05:31:43 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 05:31:44 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 19:02:52 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 19:02:52 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 19:07:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 19:07:42 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 19:07:42 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 19:07:43 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 19:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 19:07:43 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 19:07:43 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 19:07:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb04c1ebc7f7005f359b85d4698d031de9ca4a4e8bc776ac6faa3f052b3a3f1`  
		Last Modified: Sat, 12 Nov 2022 10:03:05 GMT  
		Size: 659.3 KB (659291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997ef90ff733ebe7a201a71b832a552bd33839b74047f89bc3f1f00139c6e629`  
		Last Modified: Sat, 12 Nov 2022 10:03:50 GMT  
		Size: 12.0 MB (11996460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2e907876797a7e7631369ff616b83ed0b57d0c152d486322351a767e140814`  
		Last Modified: Sat, 12 Nov 2022 10:03:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0291337573b1029d149b2fca6ebe6b0b3601a0d0f5eaecc06c1e75696f8c6731`  
		Last Modified: Wed, 16 Nov 2022 08:16:48 GMT  
		Size: 3.1 MB (3056225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8f69cf77b68a4b6e967edd1ed5cebd3eda7ce3b4c37d3cc3c6c80941a0509`  
		Last Modified: Fri, 18 Nov 2022 19:09:23 GMT  
		Size: 9.5 MB (9499491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63ac0856d1f8f6029e19cbd1091942b95aa2bf50d51d2e6be43d3fbe7f3bb7d`  
		Last Modified: Fri, 18 Nov 2022 19:09:51 GMT  
		Size: 298.3 MB (298315139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8470d03ed17d2c6c783bb46ad242efce0cc3f549f5b98e001e42fda3b56824b8`  
		Last Modified: Fri, 18 Nov 2022 19:09:21 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598946608775d3c0df6899c4da0bfec0d2ef162decc5c884d73764d4a72f6789`  
		Last Modified: Fri, 18 Nov 2022 19:09:21 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:2c93dd162547b7b44c8202cf0599e16fb7d2a686c396e6130f122c1b3f61dc4e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46167316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4ccc5a457a36ea94161437a8f9f5053f0e75d381326a3d6a0d8e1e91cc02a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:23:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 08:16:58 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 08:16:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 08:35:03 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 08:35:03 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 08:53:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 08:53:19 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 08:53:19 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 08:53:19 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:18:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:18:37 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:18:42 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:18:42 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:48:20 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:48:20 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:49:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:49:01 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:49:01 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:49:01 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:49:01 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:49:01 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:49:01 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e190eeb0612a6514b857c64886ec8f64d8e235210be5682cf6abbc5bd172b135`  
		Last Modified: Sat, 12 Nov 2022 09:21:43 GMT  
		Size: 663.1 KB (663101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4727b51eed627eface71c55490f3017153992b7d9ae395a99b1e11841128d06`  
		Last Modified: Sat, 12 Nov 2022 09:22:08 GMT  
		Size: 13.1 MB (13073328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce34a3004b391575b577e7922f6d501a0b8ba079dc0741b068b86558c26ee4a1`  
		Last Modified: Sat, 12 Nov 2022 09:22:06 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c270266b6f1942f4120af4ec7278184a61adb708209c33c2320154d82f8a31`  
		Last Modified: Wed, 16 Nov 2022 01:27:26 GMT  
		Size: 3.1 MB (3056436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286cee3bdb5335ff6bca12b16beabdce685e5fdb0a9d0561b1e6cb24ba774152`  
		Last Modified: Fri, 18 Nov 2022 18:49:43 GMT  
		Size: 9.7 MB (9699369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fc21cbba39c03767e72e06461ef113f17eae2671200bbff9598e569d7b5be7`  
		Last Modified: Fri, 18 Nov 2022 18:49:45 GMT  
		Size: 17.0 MB (16955466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5513e43b833e2f30026902bd7a4a1af1addd71ecb1736426f8252fc49d442006`  
		Last Modified: Fri, 18 Nov 2022 18:49:43 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed37a61b2c4a8b46b1ab69bf0c36dcccc4b0e44802a41f019fcb2efd750418a3`  
		Last Modified: Fri, 18 Nov 2022 18:49:42 GMT  
		Size: 2.1 KB (2145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine3.16` - linux; 386

```console
$ docker pull satosa@sha256:2db0679167412bbbf2ab4702b8580f18935847abe845bb15e8472bda6204190d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328240269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9c562b6c31c0440d0e58b8f9b031c6bcbb90cb33beb9032c8b3544236d5c33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:29:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 05:29:12 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 05:29:14 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 05:50:43 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 05:50:44 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 06:11:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 06:11:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 06:11:39 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 06:11:40 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:38:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:38:28 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:38:35 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:38:36 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:43:42 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:43:43 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:47:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:47:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:47:55 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:47:57 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:47:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:47:58 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:47:59 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:48:00 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a152a67ad9fd5011f8da356e104e14cdbd9cd925941bb6c241b50471eef5a520`  
		Last Modified: Sat, 12 Nov 2022 06:51:44 GMT  
		Size: 669.6 KB (669609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81c595fa967dddaa2db39bd0328b1e7e07583641e9870975cc6d7f37a54f069`  
		Last Modified: Sat, 12 Nov 2022 06:52:19 GMT  
		Size: 13.2 MB (13163166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8750f6265e3be5e75d2d9bb8766f7ae3208bd6ec29a99ab721971a438e8692`  
		Last Modified: Sat, 12 Nov 2022 06:52:17 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c32efb655c88520610dfffc30bc04d2a99130cbac9bd50f8f43c0a37aef6d28`  
		Last Modified: Wed, 16 Nov 2022 01:52:46 GMT  
		Size: 3.1 MB (3054164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e426180bebf4c41e9095922812af13b228b8a1891f925b18c6418706d09d589c`  
		Last Modified: Fri, 18 Nov 2022 18:49:32 GMT  
		Size: 10.0 MB (9981921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35638e3376e5dee654e447a8aded8def08d009dc15a9a6492ea89f0f6cf991d`  
		Last Modified: Fri, 18 Nov 2022 18:49:48 GMT  
		Size: 298.6 MB (298551244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed3a4f7081736c94dcc732f68489dc73f4dbfb0033bb1565e56218bf56e0eba`  
		Last Modified: Fri, 18 Nov 2022 18:49:31 GMT  
		Size: 9.4 KB (9437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84eedc2257c4e9334b63cca383a14503a49dcd221ab8e62a83dd2811a1c87895`  
		Last Modified: Fri, 18 Nov 2022 18:49:31 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine3.16` - linux; ppc64le

```console
$ docker pull satosa@sha256:78f6a669461f794f0b3dd8e4ed981afb6864275142dd4e3e84b2c9d9e502f748
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328360558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c362cb6cae301a29e6e4675274c3ec62a3fab9aa0ca147eb8167fb57c2d3c92e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 09:09:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 09:09:52 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 09:09:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 09:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 09:49:13 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 10:29:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 10:29:46 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 10:29:47 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 10:29:47 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:28:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:28:15 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:28:26 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:28:27 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:25:31 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:25:31 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:33:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:34:00 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:34:01 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:34:01 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:34:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:34:02 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:34:02 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:34:02 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0578c681eac19aa83cc60a5d383147a7c56a35a3ac13286945daa470f25157e`  
		Last Modified: Sat, 12 Nov 2022 11:31:49 GMT  
		Size: 670.3 KB (670297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bcec55fc14204d6d5b10511d2dcb4b565f19ea0c07a815947bf4616259786f`  
		Last Modified: Sat, 12 Nov 2022 11:32:23 GMT  
		Size: 13.3 MB (13307557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd9e47c00af72c31f09498bcdbb9f23c6b599d96b3262a847fd18af79d8ec83`  
		Last Modified: Sat, 12 Nov 2022 11:32:20 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbba60b66096fca5cbb93d7c032bf2aa7755ea3c73fcddca01bb6d3af1fb0f86`  
		Last Modified: Wed, 16 Nov 2022 07:01:58 GMT  
		Size: 3.1 MB (3056418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59aba7b954790c375454d90d43b7e21ef374bf3fc2cfbca50b660cb08066a22b`  
		Last Modified: Fri, 18 Nov 2022 18:35:37 GMT  
		Size: 10.0 MB (9950742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840cb6e59e4841e4831f3736de75cdf2d9a9d41a587a37d4f6eb185bc212f816`  
		Last Modified: Fri, 18 Nov 2022 18:36:05 GMT  
		Size: 298.6 MB (298562127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605fa8f9b6826c59c0ecc11cc54f8a7a6193c33cee3839935c7409ec2c4bd610`  
		Last Modified: Fri, 18 Nov 2022 18:35:34 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f7512564d5a154d9f72c5ff30f44cfb66410e160250b0ffba25e4abaaaacd1`  
		Last Modified: Fri, 18 Nov 2022 18:35:34 GMT  
		Size: 2.2 KB (2151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8-bullseye`

```console
$ docker pull satosa@sha256:920b2db648258e4779443b954cbc17015f3e7feda80d41ee006fdf102363bce8
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

### `satosa:8-bullseye` - linux; amd64

```console
$ docker pull satosa@sha256:2b75f1966b97e958ab7b3edb499a68b28221198f61990a4e20b66bf461a02dfb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87754433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da994718d5841d288b6e518373ab9111b96651fc972c162c8ec1e737bb52fd08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 18:54:42 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 18:54:42 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 18:54:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 20:02:05 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 20:02:05 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 20:16:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 20:16:53 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 20:16:53 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 20:16:53 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:55:31 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:55:32 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:55:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:55:42 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:27:35 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:27:35 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:28:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:28:36 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:28:36 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:28:36 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:28:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:28:36 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:28:36 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:28:36 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00aaacf759c581712fa578a6b4e8e0b9fc780919a5d835a168457b754755644`  
		Last Modified: Tue, 15 Nov 2022 22:58:09 GMT  
		Size: 1.1 MB (1077982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b9691827181afb85e2027be1b34b948a9de4110f0253de4e0c9dfcf1559f7b`  
		Last Modified: Tue, 15 Nov 2022 22:59:24 GMT  
		Size: 12.6 MB (12586017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf69ec4fb1d1d974ad18c827b094bb4a4242791b94344e6f059ed9d0b8eb62be`  
		Last Modified: Tue, 15 Nov 2022 22:59:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7bf64971b8ca870b8bc8476ffc783c777f6bb3bb53e50d8e719f1ea1bad697`  
		Last Modified: Wed, 16 Nov 2022 07:04:31 GMT  
		Size: 3.3 MB (3348953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c001071f815bdbd3fc5e231343c0b4b3337b9d339bd507162ce825aa8eff5643`  
		Last Modified: Mon, 21 Nov 2022 19:29:13 GMT  
		Size: 21.1 MB (21096341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c4d15fc7d1e06ddff844be580c929a202aeef96ed8cb426f2e1f60c6291d80`  
		Last Modified: Mon, 21 Nov 2022 19:29:14 GMT  
		Size: 18.2 MB (18220647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6220bf882cf516ac06374d47fe5f7eb9cb8ac7207c16648c87262453bcb5dd`  
		Last Modified: Mon, 21 Nov 2022 19:29:10 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9610156b7a28fe2c40ba7509e651e32b895a71e7c2999362f9d0dcdefefc7830`  
		Last Modified: Mon, 21 Nov 2022 19:29:10 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-bullseye` - linux; arm variant v5

```console
$ docker pull satosa@sha256:191432b034c13284a7a750492dc4bbbaab7cbdab72b127ccdc3276685c0a6277
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.3 MB (374337256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddea723e3d8081cb37968943d59ce80b13516d5314627468f2f689ac477edb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:49:18 GMT
ADD file:1949af7e583a1b54055a421129c32315fc101e53e2cda05da3171ed461bde0a6 in / 
# Tue, 15 Nov 2022 01:49:19 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:45:56 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 07:45:56 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 07:46:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 08:28:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 08:28:59 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 08:51:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 08:51:04 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 08:51:04 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 08:51:04 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:33:16 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:33:16 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:33:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:33:32 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:48:45 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:48:45 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:53:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:53:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:53:25 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:53:26 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:53:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:53:26 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:53:26 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:53:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b56836d864a6d857be3d12242b65962f2a2cf0d77c48cfb85bbbdf9d56a7e93d`  
		Last Modified: Tue, 15 Nov 2022 01:54:26 GMT  
		Size: 28.9 MB (28914126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a6e5b3ab314e2965853a4ddc03100cfb0fd0d2825cdc2fb4f1bc363cca39b9`  
		Last Modified: Tue, 15 Nov 2022 10:08:43 GMT  
		Size: 1.1 MB (1060732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db96a74ae1eb60de22f4973a045a1b638a39090565ee2fdf0d4a8c4319bf21c`  
		Last Modified: Tue, 15 Nov 2022 10:09:24 GMT  
		Size: 12.1 MB (12146339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb7e08f0a09cbc7e1269f3c705f9ff28966afe27388fc990a03c00f3200360a`  
		Last Modified: Tue, 15 Nov 2022 10:09:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdc4079d02fdf319fd5aa22d26a4a8b2ec80e3f8beb0ada18ed0aa2ace5e0d7`  
		Last Modified: Wed, 16 Nov 2022 00:39:40 GMT  
		Size: 3.3 MB (3348246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0106290c3f2418d61678711f86fda97637dff84ccfae811034f743dcae2eb8`  
		Last Modified: Mon, 21 Nov 2022 19:54:08 GMT  
		Size: 22.7 MB (22693132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745925b8b4315a2b9b975665bd6158b73df587417a7fade9559f85ddfc27139d`  
		Last Modified: Mon, 21 Nov 2022 19:54:31 GMT  
		Size: 306.2 MB (306162846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c0f3ca52005fb9ed30e05bac90f93fbd6237467e4145b4950ac388200c78fc`  
		Last Modified: Mon, 21 Nov 2022 19:54:04 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15ae5fb82b045c21046c703a63283b8053930321884f0aa7174a12966b6fb46`  
		Last Modified: Mon, 21 Nov 2022 19:54:04 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-bullseye` - linux; arm variant v7

```console
$ docker pull satosa@sha256:c31d3aa2b933736a4d50e795d7d017bdbe9163970108978759602cc4b09333de
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.1 MB (371088257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d8463fe00f06c45603677eff859db0d7b45fc077a01e06584c25b28d75a300`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 03:43:25 GMT
ADD file:1b5c939bd2a35667d7fc44c3009a56ed92a932f512a73df1617dec6ccbd6e6b1 in / 
# Tue, 15 Nov 2022 03:43:26 GMT
CMD ["bash"]
# Wed, 16 Nov 2022 02:10:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Nov 2022 02:10:52 GMT
ENV LANG=C.UTF-8
# Wed, 16 Nov 2022 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Nov 2022 04:26:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 16 Nov 2022 04:26:07 GMT
ENV PYTHON_VERSION=3.11.0
# Wed, 16 Nov 2022 04:47:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 16 Nov 2022 04:47:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_PIP_VERSION=22.3
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 04:47:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 04:47:40 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:58:12 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:58:13 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 20:02:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 20:02:37 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 20:02:37 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 20:02:38 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 20:02:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 20:02:38 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 20:02:38 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 20:02:38 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:fd18d0201d0ce0c5e103902d894f5d601fc5dde76688aa7dae786840141d23e4`  
		Last Modified: Tue, 15 Nov 2022 03:50:11 GMT  
		Size: 26.6 MB (26576195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f4e2c2480160d1670c2ebb7d1c8290f0a3956265f0069d1de3e5b60d587141`  
		Last Modified: Wed, 16 Nov 2022 08:13:53 GMT  
		Size: 1.0 MB (1042833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9254168af81f2bf98cb621d697e2b624446620a5acce3412a20ed6f6912fd248`  
		Last Modified: Wed, 16 Nov 2022 08:15:35 GMT  
		Size: 11.6 MB (11642276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a40d929533b6fb9173ac38ebf09de1f187f9aa8c6b49de778a38b52abbda11`  
		Last Modified: Wed, 16 Nov 2022 08:15:33 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b04522957691b19b0ac6940e157f56337b27084782602ad4d8a7229397944e1`  
		Last Modified: Wed, 16 Nov 2022 08:15:34 GMT  
		Size: 3.3 MB (3348201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978ebe46f9e524ab17da6008d165ad70ca5187930fb4cd7fc6cd17cccbe7002e`  
		Last Modified: Mon, 21 Nov 2022 20:03:41 GMT  
		Size: 22.4 MB (22430741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa27795d0d8f0524db63e5fbf00dcc9ac44cfeb68c3a66350870d3c3e903fe9`  
		Last Modified: Mon, 21 Nov 2022 20:04:05 GMT  
		Size: 306.0 MB (306036175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5483a349efd69231e68a3b2f9212afd52f92c5498da8c707b5a60f90db6399a`  
		Last Modified: Mon, 21 Nov 2022 20:03:37 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa6d2f8593d4d5bca10332fd90d782e457560c6a50b6fd53614a5eb88d04109`  
		Last Modified: Mon, 21 Nov 2022 20:03:37 GMT  
		Size: 2.1 KB (2144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-bullseye` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:a654eeeefb6f573740cf6dc83bc68eb3ff1ad0e4ab660417964ee9664772c6a9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85480362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa7f1d11b3d6d0006e3d3dce2de48cfc52f63ddd139cfddfd1a79675972969b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:41:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 07:41:31 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 07:41:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 08:34:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 08:34:07 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 08:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 08:47:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 08:47:37 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 08:47:37 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:17:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:17:57 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:18:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:18:07 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:49:25 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:49:25 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:50:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:50:21 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:50:21 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:50:21 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:50:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:50:21 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:50:21 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:50:21 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbd8719487c40bfcc7d42d53f202d1dbbbb7ac0fb4e4919ed791664b7f4e47b`  
		Last Modified: Tue, 15 Nov 2022 10:55:04 GMT  
		Size: 1.1 MB (1065870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb07c67a71797e21118367f8ed3ec8f9561b4e4e3f662aed2467c97a93a6dc3f`  
		Last Modified: Tue, 15 Nov 2022 10:56:03 GMT  
		Size: 12.6 MB (12637055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130567c01926a008d097f8a10e6c4348f8cf6f6bae2df7860e1ebad57caf457d`  
		Last Modified: Tue, 15 Nov 2022 10:56:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad488014eea42b129f9a60d9258bfd09ddf59c75a5ccdc55e196cc0eef88cfe`  
		Last Modified: Wed, 16 Nov 2022 01:26:28 GMT  
		Size: 3.3 MB (3348606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cc72b0c430a3bd0d92649200cd8c6da867ea3a7f33b5066d9b8bae085c587c`  
		Last Modified: Mon, 21 Nov 2022 19:50:50 GMT  
		Size: 21.0 MB (20975486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c84b4c195beedd08e708b18de7f11a9e87d3ac3ef1bed9904140963320cb472`  
		Last Modified: Mon, 21 Nov 2022 19:50:50 GMT  
		Size: 17.4 MB (17380880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15489ffd1801184e8a797e1467fb0a83eec71433d9efe85b7fcc060f9c77547`  
		Last Modified: Mon, 21 Nov 2022 19:50:47 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6345651cb201b249a31896d42f4f630bd5f4ee5dc259842a415b1e1d21bc36ab`  
		Last Modified: Mon, 21 Nov 2022 19:50:47 GMT  
		Size: 2.1 KB (2141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-bullseye` - linux; 386

```console
$ docker pull satosa@sha256:34866c133ed80b3650fcac32e7f67597fa1598e16fc84e51e0e8ee340d0e6ca9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 MB (380177011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25aed64d35227d6dd9deb0905d3a0f76dc6e28a9ce7465ec44f6985baf78563`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:27 GMT
ADD file:608bec4ba3e2543714da4c5158f3c46a168f63ee69ac3f48bff54474ba9a6f27 in / 
# Tue, 15 Nov 2022 01:41:27 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 12:57:10 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 12:57:11 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 12:57:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:13:48 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 14:13:49 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 14:32:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 14:32:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 14:32:38 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 14:32:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:37:29 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:37:29 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:37:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:37:42 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:39:08 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:39:08 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:43:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:43:23 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:43:23 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:43:25 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:43:26 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:43:27 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:43:28 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f6a1e975b34444ecb7c6a2b537403fd6b94d2ff3225944ac2ac3b292466e4078`  
		Last Modified: Tue, 15 Nov 2022 01:47:05 GMT  
		Size: 32.4 MB (32392982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a4ead92cc7eae0396b0fbac1238e0bee3f677740a65a67474e08bcbaa003ba`  
		Last Modified: Tue, 15 Nov 2022 17:38:22 GMT  
		Size: 884.5 KB (884461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd0f4ed85c962a057d2c2667c8b4e1a210aea5e2c9e68520214eb87926f684e`  
		Last Modified: Tue, 15 Nov 2022 19:31:55 GMT  
		Size: 12.7 MB (12683309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72250ba4c687654d3be8943b7bf9591f4dc5de08989c26f5654409682ffbdbfd`  
		Last Modified: Tue, 15 Nov 2022 19:31:53 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ffce336712f2fe573ad63960925a12291df3e7598c36c326698f1308f9caae`  
		Last Modified: Wed, 16 Nov 2022 01:51:48 GMT  
		Size: 3.1 MB (3132128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab52fcbbc37aab1d08731873c11e68396df78043d92d74c7faa4c5b09467c928`  
		Last Modified: Mon, 21 Nov 2022 19:44:19 GMT  
		Size: 24.1 MB (24065495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc904879f9ede6886b46d646fa18a746d32afacfe68d200cbd6259eb315d64a5`  
		Last Modified: Mon, 21 Nov 2022 19:44:46 GMT  
		Size: 307.0 MB (307006821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debe7b65c57d841640da19f01ceedfd6f2d319eabb09c1027621317ab5e75159`  
		Last Modified: Mon, 21 Nov 2022 19:44:15 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ea23efc09b0e6df59a86e0ce421416ed60dbfd3ee8016fdf2d744574b117cd`  
		Last Modified: Mon, 21 Nov 2022 19:44:15 GMT  
		Size: 2.1 KB (2143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-bullseye` - linux; ppc64le

```console
$ docker pull satosa@sha256:aa91656e4b6a0f6b51aa29a1219617190b462ee7f8b0f25fddd786c831f542f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.5 MB (382489126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88774150f37054a63d09106df180126b080812678a23cfb365f6c4c5fcd1ec22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 05:18:45 GMT
ADD file:520926164fdc762143905745329e568c67289232bec450e48645d82a4613dccf in / 
# Tue, 15 Nov 2022 05:18:47 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:06:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 13:06:51 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 13:07:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:38:22 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 14:38:22 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 15:25:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 15:25:30 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 15:25:31 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 15:25:31 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:27:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:27:46 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:28:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:28:07 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:17:24 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:17:25 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:24:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:24:32 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:24:32 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:24:33 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:24:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:24:33 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:24:34 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:24:34 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:c57913b7d0318ef1a47f0348ce54d9865316776aa1ffb2c7871b1473b3d29407`  
		Last Modified: Tue, 15 Nov 2022 05:24:22 GMT  
		Size: 35.3 MB (35285140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa173aadf3e5fa326d1f1b9f9263051781dc9833e8b60e5bb5a9a994739e18ee`  
		Last Modified: Tue, 15 Nov 2022 17:58:02 GMT  
		Size: 1.1 MB (1096202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2c11a6d1874c9a04e310b3de6f884a5db20d8b2819f963dfbb87d255d4041d`  
		Last Modified: Tue, 15 Nov 2022 17:58:54 GMT  
		Size: 13.0 MB (12955764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53510645cb4e75dba43f2960e61295b7e4092e32b65c05d78e4a222a1035b0`  
		Last Modified: Tue, 15 Nov 2022 17:58:50 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76a75d59183d172f23c152a8f9b934d52c2bbe4e381b7d98e6254342b65c9ad`  
		Last Modified: Wed, 16 Nov 2022 07:01:30 GMT  
		Size: 3.3 MB (3349130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789086c936cb86df67a1bcdf02c069f46030c960a874385b1c09458ea09c9e28`  
		Last Modified: Mon, 21 Nov 2022 19:25:29 GMT  
		Size: 23.6 MB (23636418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf604bdc50ad0b740586882da17fa028eb433f3e9291ae1752d62a62443a5dbd`  
		Last Modified: Mon, 21 Nov 2022 19:25:54 GMT  
		Size: 306.2 MB (306154608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24af618620347663fdfc4357acbffd238b3cc0a2d84703ef629fe73ef009c9bf`  
		Last Modified: Mon, 21 Nov 2022 19:25:23 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b025a5ca25095fb82fa5f084b355cf1b4387400fe727ec454daad74044e9445`  
		Last Modified: Mon, 21 Nov 2022 19:25:23 GMT  
		Size: 2.1 KB (2143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-bullseye` - linux; s390x

```console
$ docker pull satosa@sha256:11d52a081306682d815a39f964424df846d178a0cd0e043c4c6392ff3f219e6a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.2 MB (375225534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec1f645b1f322cd61afb287021cc9f964eccaaecf3250c047df64b92f392d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 10:52:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 10:52:16 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 10:52:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 11:31:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 11:31:14 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 11:46:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 11:46:18 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 11:46:19 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 11:46:19 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:47:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:47:51 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:48:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:48:06 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:42:07 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:42:08 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:46:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:46:10 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:46:10 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:46:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:46:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:46:10 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:46:10 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:46:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1487a90d7d45334f92d990a52e5750391ed66b11532972979f0792745cedca`  
		Last Modified: Tue, 15 Nov 2022 13:07:54 GMT  
		Size: 1.1 MB (1077428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81becff7fb0cea099dc76445874abd672598812e9ae8fb990ce90a07971a00c2`  
		Last Modified: Tue, 15 Nov 2022 13:08:34 GMT  
		Size: 12.4 MB (12422163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e82170644b3fad2be2ca3ce0cd517e5487772520f4eccaf5e60ce99b9533cf`  
		Last Modified: Tue, 15 Nov 2022 13:08:32 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8aa6e35e336a7de98329dc7ecba62f34a24d5eacb447feafcaac381b01a578`  
		Last Modified: Wed, 16 Nov 2022 00:58:52 GMT  
		Size: 3.3 MB (3348811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55521d94cc6014114d16684de5cf415a987eb5306bb707b2c9c89612bae7434`  
		Last Modified: Mon, 21 Nov 2022 19:46:42 GMT  
		Size: 21.0 MB (21008499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453920ba520592eb4a4712ce352cacced35e45b4c29dc9ba96af152f4263f10a`  
		Last Modified: Mon, 21 Nov 2022 19:46:54 GMT  
		Size: 307.7 MB (307712990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b654413945b74c59b340cba2b01bbd308650ac51a2cefcaede178af5de4e030`  
		Last Modified: Mon, 21 Nov 2022 19:46:39 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a8d82d6fccb2478507a3f5986cf0cf8538a12e3f01d8780e85ed975218703`  
		Last Modified: Mon, 21 Nov 2022 19:46:40 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.2`

```console
$ docker pull satosa@sha256:920b2db648258e4779443b954cbc17015f3e7feda80d41ee006fdf102363bce8
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

### `satosa:8.2` - linux; amd64

```console
$ docker pull satosa@sha256:2b75f1966b97e958ab7b3edb499a68b28221198f61990a4e20b66bf461a02dfb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87754433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da994718d5841d288b6e518373ab9111b96651fc972c162c8ec1e737bb52fd08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 18:54:42 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 18:54:42 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 18:54:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 20:02:05 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 20:02:05 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 20:16:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 20:16:53 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 20:16:53 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 20:16:53 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:55:31 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:55:32 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:55:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:55:42 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:27:35 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:27:35 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:28:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:28:36 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:28:36 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:28:36 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:28:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:28:36 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:28:36 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:28:36 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00aaacf759c581712fa578a6b4e8e0b9fc780919a5d835a168457b754755644`  
		Last Modified: Tue, 15 Nov 2022 22:58:09 GMT  
		Size: 1.1 MB (1077982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b9691827181afb85e2027be1b34b948a9de4110f0253de4e0c9dfcf1559f7b`  
		Last Modified: Tue, 15 Nov 2022 22:59:24 GMT  
		Size: 12.6 MB (12586017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf69ec4fb1d1d974ad18c827b094bb4a4242791b94344e6f059ed9d0b8eb62be`  
		Last Modified: Tue, 15 Nov 2022 22:59:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7bf64971b8ca870b8bc8476ffc783c777f6bb3bb53e50d8e719f1ea1bad697`  
		Last Modified: Wed, 16 Nov 2022 07:04:31 GMT  
		Size: 3.3 MB (3348953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c001071f815bdbd3fc5e231343c0b4b3337b9d339bd507162ce825aa8eff5643`  
		Last Modified: Mon, 21 Nov 2022 19:29:13 GMT  
		Size: 21.1 MB (21096341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c4d15fc7d1e06ddff844be580c929a202aeef96ed8cb426f2e1f60c6291d80`  
		Last Modified: Mon, 21 Nov 2022 19:29:14 GMT  
		Size: 18.2 MB (18220647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6220bf882cf516ac06374d47fe5f7eb9cb8ac7207c16648c87262453bcb5dd`  
		Last Modified: Mon, 21 Nov 2022 19:29:10 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9610156b7a28fe2c40ba7509e651e32b895a71e7c2999362f9d0dcdefefc7830`  
		Last Modified: Mon, 21 Nov 2022 19:29:10 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2` - linux; arm variant v5

```console
$ docker pull satosa@sha256:191432b034c13284a7a750492dc4bbbaab7cbdab72b127ccdc3276685c0a6277
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.3 MB (374337256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddea723e3d8081cb37968943d59ce80b13516d5314627468f2f689ac477edb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:49:18 GMT
ADD file:1949af7e583a1b54055a421129c32315fc101e53e2cda05da3171ed461bde0a6 in / 
# Tue, 15 Nov 2022 01:49:19 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:45:56 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 07:45:56 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 07:46:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 08:28:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 08:28:59 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 08:51:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 08:51:04 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 08:51:04 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 08:51:04 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:33:16 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:33:16 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:33:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:33:32 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:48:45 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:48:45 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:53:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:53:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:53:25 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:53:26 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:53:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:53:26 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:53:26 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:53:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b56836d864a6d857be3d12242b65962f2a2cf0d77c48cfb85bbbdf9d56a7e93d`  
		Last Modified: Tue, 15 Nov 2022 01:54:26 GMT  
		Size: 28.9 MB (28914126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a6e5b3ab314e2965853a4ddc03100cfb0fd0d2825cdc2fb4f1bc363cca39b9`  
		Last Modified: Tue, 15 Nov 2022 10:08:43 GMT  
		Size: 1.1 MB (1060732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db96a74ae1eb60de22f4973a045a1b638a39090565ee2fdf0d4a8c4319bf21c`  
		Last Modified: Tue, 15 Nov 2022 10:09:24 GMT  
		Size: 12.1 MB (12146339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb7e08f0a09cbc7e1269f3c705f9ff28966afe27388fc990a03c00f3200360a`  
		Last Modified: Tue, 15 Nov 2022 10:09:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdc4079d02fdf319fd5aa22d26a4a8b2ec80e3f8beb0ada18ed0aa2ace5e0d7`  
		Last Modified: Wed, 16 Nov 2022 00:39:40 GMT  
		Size: 3.3 MB (3348246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0106290c3f2418d61678711f86fda97637dff84ccfae811034f743dcae2eb8`  
		Last Modified: Mon, 21 Nov 2022 19:54:08 GMT  
		Size: 22.7 MB (22693132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745925b8b4315a2b9b975665bd6158b73df587417a7fade9559f85ddfc27139d`  
		Last Modified: Mon, 21 Nov 2022 19:54:31 GMT  
		Size: 306.2 MB (306162846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c0f3ca52005fb9ed30e05bac90f93fbd6237467e4145b4950ac388200c78fc`  
		Last Modified: Mon, 21 Nov 2022 19:54:04 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15ae5fb82b045c21046c703a63283b8053930321884f0aa7174a12966b6fb46`  
		Last Modified: Mon, 21 Nov 2022 19:54:04 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2` - linux; arm variant v7

```console
$ docker pull satosa@sha256:c31d3aa2b933736a4d50e795d7d017bdbe9163970108978759602cc4b09333de
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.1 MB (371088257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d8463fe00f06c45603677eff859db0d7b45fc077a01e06584c25b28d75a300`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 03:43:25 GMT
ADD file:1b5c939bd2a35667d7fc44c3009a56ed92a932f512a73df1617dec6ccbd6e6b1 in / 
# Tue, 15 Nov 2022 03:43:26 GMT
CMD ["bash"]
# Wed, 16 Nov 2022 02:10:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Nov 2022 02:10:52 GMT
ENV LANG=C.UTF-8
# Wed, 16 Nov 2022 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Nov 2022 04:26:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 16 Nov 2022 04:26:07 GMT
ENV PYTHON_VERSION=3.11.0
# Wed, 16 Nov 2022 04:47:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 16 Nov 2022 04:47:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_PIP_VERSION=22.3
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 04:47:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 04:47:40 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:58:12 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:58:13 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 20:02:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 20:02:37 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 20:02:37 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 20:02:38 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 20:02:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 20:02:38 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 20:02:38 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 20:02:38 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:fd18d0201d0ce0c5e103902d894f5d601fc5dde76688aa7dae786840141d23e4`  
		Last Modified: Tue, 15 Nov 2022 03:50:11 GMT  
		Size: 26.6 MB (26576195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f4e2c2480160d1670c2ebb7d1c8290f0a3956265f0069d1de3e5b60d587141`  
		Last Modified: Wed, 16 Nov 2022 08:13:53 GMT  
		Size: 1.0 MB (1042833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9254168af81f2bf98cb621d697e2b624446620a5acce3412a20ed6f6912fd248`  
		Last Modified: Wed, 16 Nov 2022 08:15:35 GMT  
		Size: 11.6 MB (11642276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a40d929533b6fb9173ac38ebf09de1f187f9aa8c6b49de778a38b52abbda11`  
		Last Modified: Wed, 16 Nov 2022 08:15:33 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b04522957691b19b0ac6940e157f56337b27084782602ad4d8a7229397944e1`  
		Last Modified: Wed, 16 Nov 2022 08:15:34 GMT  
		Size: 3.3 MB (3348201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978ebe46f9e524ab17da6008d165ad70ca5187930fb4cd7fc6cd17cccbe7002e`  
		Last Modified: Mon, 21 Nov 2022 20:03:41 GMT  
		Size: 22.4 MB (22430741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa27795d0d8f0524db63e5fbf00dcc9ac44cfeb68c3a66350870d3c3e903fe9`  
		Last Modified: Mon, 21 Nov 2022 20:04:05 GMT  
		Size: 306.0 MB (306036175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5483a349efd69231e68a3b2f9212afd52f92c5498da8c707b5a60f90db6399a`  
		Last Modified: Mon, 21 Nov 2022 20:03:37 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa6d2f8593d4d5bca10332fd90d782e457560c6a50b6fd53614a5eb88d04109`  
		Last Modified: Mon, 21 Nov 2022 20:03:37 GMT  
		Size: 2.1 KB (2144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:a654eeeefb6f573740cf6dc83bc68eb3ff1ad0e4ab660417964ee9664772c6a9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85480362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa7f1d11b3d6d0006e3d3dce2de48cfc52f63ddd139cfddfd1a79675972969b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:41:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 07:41:31 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 07:41:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 08:34:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 08:34:07 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 08:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 08:47:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 08:47:37 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 08:47:37 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:17:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:17:57 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:18:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:18:07 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:49:25 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:49:25 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:50:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:50:21 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:50:21 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:50:21 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:50:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:50:21 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:50:21 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:50:21 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbd8719487c40bfcc7d42d53f202d1dbbbb7ac0fb4e4919ed791664b7f4e47b`  
		Last Modified: Tue, 15 Nov 2022 10:55:04 GMT  
		Size: 1.1 MB (1065870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb07c67a71797e21118367f8ed3ec8f9561b4e4e3f662aed2467c97a93a6dc3f`  
		Last Modified: Tue, 15 Nov 2022 10:56:03 GMT  
		Size: 12.6 MB (12637055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130567c01926a008d097f8a10e6c4348f8cf6f6bae2df7860e1ebad57caf457d`  
		Last Modified: Tue, 15 Nov 2022 10:56:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad488014eea42b129f9a60d9258bfd09ddf59c75a5ccdc55e196cc0eef88cfe`  
		Last Modified: Wed, 16 Nov 2022 01:26:28 GMT  
		Size: 3.3 MB (3348606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cc72b0c430a3bd0d92649200cd8c6da867ea3a7f33b5066d9b8bae085c587c`  
		Last Modified: Mon, 21 Nov 2022 19:50:50 GMT  
		Size: 21.0 MB (20975486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c84b4c195beedd08e708b18de7f11a9e87d3ac3ef1bed9904140963320cb472`  
		Last Modified: Mon, 21 Nov 2022 19:50:50 GMT  
		Size: 17.4 MB (17380880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15489ffd1801184e8a797e1467fb0a83eec71433d9efe85b7fcc060f9c77547`  
		Last Modified: Mon, 21 Nov 2022 19:50:47 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6345651cb201b249a31896d42f4f630bd5f4ee5dc259842a415b1e1d21bc36ab`  
		Last Modified: Mon, 21 Nov 2022 19:50:47 GMT  
		Size: 2.1 KB (2141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2` - linux; 386

```console
$ docker pull satosa@sha256:34866c133ed80b3650fcac32e7f67597fa1598e16fc84e51e0e8ee340d0e6ca9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 MB (380177011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25aed64d35227d6dd9deb0905d3a0f76dc6e28a9ce7465ec44f6985baf78563`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:27 GMT
ADD file:608bec4ba3e2543714da4c5158f3c46a168f63ee69ac3f48bff54474ba9a6f27 in / 
# Tue, 15 Nov 2022 01:41:27 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 12:57:10 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 12:57:11 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 12:57:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:13:48 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 14:13:49 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 14:32:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 14:32:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 14:32:38 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 14:32:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:37:29 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:37:29 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:37:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:37:42 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:39:08 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:39:08 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:43:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:43:23 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:43:23 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:43:25 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:43:26 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:43:27 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:43:28 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f6a1e975b34444ecb7c6a2b537403fd6b94d2ff3225944ac2ac3b292466e4078`  
		Last Modified: Tue, 15 Nov 2022 01:47:05 GMT  
		Size: 32.4 MB (32392982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a4ead92cc7eae0396b0fbac1238e0bee3f677740a65a67474e08bcbaa003ba`  
		Last Modified: Tue, 15 Nov 2022 17:38:22 GMT  
		Size: 884.5 KB (884461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd0f4ed85c962a057d2c2667c8b4e1a210aea5e2c9e68520214eb87926f684e`  
		Last Modified: Tue, 15 Nov 2022 19:31:55 GMT  
		Size: 12.7 MB (12683309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72250ba4c687654d3be8943b7bf9591f4dc5de08989c26f5654409682ffbdbfd`  
		Last Modified: Tue, 15 Nov 2022 19:31:53 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ffce336712f2fe573ad63960925a12291df3e7598c36c326698f1308f9caae`  
		Last Modified: Wed, 16 Nov 2022 01:51:48 GMT  
		Size: 3.1 MB (3132128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab52fcbbc37aab1d08731873c11e68396df78043d92d74c7faa4c5b09467c928`  
		Last Modified: Mon, 21 Nov 2022 19:44:19 GMT  
		Size: 24.1 MB (24065495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc904879f9ede6886b46d646fa18a746d32afacfe68d200cbd6259eb315d64a5`  
		Last Modified: Mon, 21 Nov 2022 19:44:46 GMT  
		Size: 307.0 MB (307006821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debe7b65c57d841640da19f01ceedfd6f2d319eabb09c1027621317ab5e75159`  
		Last Modified: Mon, 21 Nov 2022 19:44:15 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ea23efc09b0e6df59a86e0ce421416ed60dbfd3ee8016fdf2d744574b117cd`  
		Last Modified: Mon, 21 Nov 2022 19:44:15 GMT  
		Size: 2.1 KB (2143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2` - linux; ppc64le

```console
$ docker pull satosa@sha256:aa91656e4b6a0f6b51aa29a1219617190b462ee7f8b0f25fddd786c831f542f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.5 MB (382489126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88774150f37054a63d09106df180126b080812678a23cfb365f6c4c5fcd1ec22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 05:18:45 GMT
ADD file:520926164fdc762143905745329e568c67289232bec450e48645d82a4613dccf in / 
# Tue, 15 Nov 2022 05:18:47 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:06:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 13:06:51 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 13:07:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:38:22 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 14:38:22 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 15:25:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 15:25:30 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 15:25:31 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 15:25:31 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:27:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:27:46 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:28:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:28:07 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:17:24 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:17:25 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:24:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:24:32 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:24:32 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:24:33 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:24:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:24:33 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:24:34 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:24:34 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:c57913b7d0318ef1a47f0348ce54d9865316776aa1ffb2c7871b1473b3d29407`  
		Last Modified: Tue, 15 Nov 2022 05:24:22 GMT  
		Size: 35.3 MB (35285140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa173aadf3e5fa326d1f1b9f9263051781dc9833e8b60e5bb5a9a994739e18ee`  
		Last Modified: Tue, 15 Nov 2022 17:58:02 GMT  
		Size: 1.1 MB (1096202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2c11a6d1874c9a04e310b3de6f884a5db20d8b2819f963dfbb87d255d4041d`  
		Last Modified: Tue, 15 Nov 2022 17:58:54 GMT  
		Size: 13.0 MB (12955764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53510645cb4e75dba43f2960e61295b7e4092e32b65c05d78e4a222a1035b0`  
		Last Modified: Tue, 15 Nov 2022 17:58:50 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76a75d59183d172f23c152a8f9b934d52c2bbe4e381b7d98e6254342b65c9ad`  
		Last Modified: Wed, 16 Nov 2022 07:01:30 GMT  
		Size: 3.3 MB (3349130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789086c936cb86df67a1bcdf02c069f46030c960a874385b1c09458ea09c9e28`  
		Last Modified: Mon, 21 Nov 2022 19:25:29 GMT  
		Size: 23.6 MB (23636418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf604bdc50ad0b740586882da17fa028eb433f3e9291ae1752d62a62443a5dbd`  
		Last Modified: Mon, 21 Nov 2022 19:25:54 GMT  
		Size: 306.2 MB (306154608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24af618620347663fdfc4357acbffd238b3cc0a2d84703ef629fe73ef009c9bf`  
		Last Modified: Mon, 21 Nov 2022 19:25:23 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b025a5ca25095fb82fa5f084b355cf1b4387400fe727ec454daad74044e9445`  
		Last Modified: Mon, 21 Nov 2022 19:25:23 GMT  
		Size: 2.1 KB (2143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2` - linux; s390x

```console
$ docker pull satosa@sha256:11d52a081306682d815a39f964424df846d178a0cd0e043c4c6392ff3f219e6a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.2 MB (375225534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec1f645b1f322cd61afb287021cc9f964eccaaecf3250c047df64b92f392d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 10:52:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 10:52:16 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 10:52:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 11:31:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 11:31:14 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 11:46:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 11:46:18 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 11:46:19 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 11:46:19 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:47:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:47:51 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:48:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:48:06 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:42:07 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:42:08 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:46:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:46:10 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:46:10 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:46:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:46:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:46:10 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:46:10 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:46:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1487a90d7d45334f92d990a52e5750391ed66b11532972979f0792745cedca`  
		Last Modified: Tue, 15 Nov 2022 13:07:54 GMT  
		Size: 1.1 MB (1077428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81becff7fb0cea099dc76445874abd672598812e9ae8fb990ce90a07971a00c2`  
		Last Modified: Tue, 15 Nov 2022 13:08:34 GMT  
		Size: 12.4 MB (12422163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e82170644b3fad2be2ca3ce0cd517e5487772520f4eccaf5e60ce99b9533cf`  
		Last Modified: Tue, 15 Nov 2022 13:08:32 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8aa6e35e336a7de98329dc7ecba62f34a24d5eacb447feafcaac381b01a578`  
		Last Modified: Wed, 16 Nov 2022 00:58:52 GMT  
		Size: 3.3 MB (3348811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55521d94cc6014114d16684de5cf415a987eb5306bb707b2c9c89612bae7434`  
		Last Modified: Mon, 21 Nov 2022 19:46:42 GMT  
		Size: 21.0 MB (21008499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453920ba520592eb4a4712ce352cacced35e45b4c29dc9ba96af152f4263f10a`  
		Last Modified: Mon, 21 Nov 2022 19:46:54 GMT  
		Size: 307.7 MB (307712990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b654413945b74c59b340cba2b01bbd308650ac51a2cefcaede178af5de4e030`  
		Last Modified: Mon, 21 Nov 2022 19:46:39 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a8d82d6fccb2478507a3f5986cf0cf8538a12e3f01d8780e85ed975218703`  
		Last Modified: Mon, 21 Nov 2022 19:46:40 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.2-alpine`

```console
$ docker pull satosa@sha256:96837510b982a984c0f69c23c7424082c1030cd0ca1de70f3a1dda2d5e3a9688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `satosa:8.2-alpine` - linux; amd64

```console
$ docker pull satosa@sha256:6e3e4da73ae0c0d1ee3192a90d4e47dd1711df0f3e2d5cda5ec9b5d0146dc48b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c03699dd38f4ddbe3655ace3de96f6a1cef874a71cdabefd8c2f24970096df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:56:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 06:39:07 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 06:39:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 06:57:28 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 06:57:28 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 07:15:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 07:15:59 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 07:15:59 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 07:15:59 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:56:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:56:08 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:56:15 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:56:15 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:22:15 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:22:15 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:22:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:23:00 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:23:00 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:23:00 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:23:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:23:01 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:23:01 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:23:01 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e124a36b9ab9caae9b9b43bffcb6f6d9f126ab89cf2a8b20b9a6f912df03d36`  
		Last Modified: Sat, 12 Nov 2022 07:47:59 GMT  
		Size: 661.8 KB (661831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86456952aa287ca80ac7d7f349dc9edbabda9393ab022d20f2e4c2263cd7d2e7`  
		Last Modified: Sat, 12 Nov 2022 07:48:26 GMT  
		Size: 13.0 MB (12998794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ece9ef7a5797feb2ddaf23aee223848643c0baaedaaa203c721aecb6b272b25`  
		Last Modified: Sat, 12 Nov 2022 07:48:24 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef27b859822294ab1253f8e09a8712d63ea9939eadd1dc4b595d52726c0b020d`  
		Last Modified: Wed, 16 Nov 2022 07:05:43 GMT  
		Size: 3.1 MB (3056443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824935fc626e0971164be442423360798c85d529053e967a909cd1273bda190e`  
		Last Modified: Fri, 18 Nov 2022 18:23:39 GMT  
		Size: 10.9 MB (10872324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fed4aaf1a18111683af619a1e71edd5804307567ed23a83f6f40d15d2794af`  
		Last Modified: Fri, 18 Nov 2022 18:23:41 GMT  
		Size: 17.4 MB (17363712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e090e2c9c7e5d74822d9f71487ec5a71f3058a6f2d8bf756ddaaed8180da06e`  
		Last Modified: Fri, 18 Nov 2022 18:23:38 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41247ef96bde894139c620ba77d7e56bed539612bc8605d4495a7b78bd90ebfb`  
		Last Modified: Fri, 18 Nov 2022 18:23:38 GMT  
		Size: 2.1 KB (2146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2-alpine` - linux; arm variant v6

```console
$ docker pull satosa@sha256:a6fbc6091cf0e1a4e5f6e3d7f2cb1e798e64a2324ff1c80eb9d46b342c11fd39
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327070023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313e9fa4c6d8a5fe836e6b47a9dcef3b27b5b56032c637bb8c15c6c2ecaba99b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:28:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 06:28:49 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 06:28:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 06:55:00 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 06:55:00 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 07:21:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 07:21:39 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 07:21:39 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 07:21:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:41:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:41:32 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:41:39 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:41:39 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:49:39 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:49:39 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:54:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:54:44 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:54:44 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:54:44 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:54:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:54:44 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:54:44 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:54:44 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe974d15ab7b1ace1e4997a68bcfb22f2652af9f902f110d0a90fbdd2ef2053`  
		Last Modified: Sat, 12 Nov 2022 08:03:00 GMT  
		Size: 666.2 KB (666196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69683a8852c8900b94150a78af049bb63d4f73fbdd7239fba1302b9b211ec82`  
		Last Modified: Sat, 12 Nov 2022 08:03:24 GMT  
		Size: 12.5 MB (12545209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63725fb700eaa74dc7942aef8ee5d333eb6b74e224f29ff11f0a997c56208595`  
		Last Modified: Sat, 12 Nov 2022 08:03:22 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012ec3c62fe317e21430242a858a7e489044f55ef1b0398a0c40d9b08e49a357`  
		Last Modified: Wed, 16 Nov 2022 00:46:22 GMT  
		Size: 3.1 MB (3056167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f055f28d65cb7615e57588e003562504a3430b08b6f6e1b13afde191879907f`  
		Last Modified: Fri, 18 Nov 2022 18:55:21 GMT  
		Size: 9.7 MB (9749625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328dee8fb8e4a3a68d2eaea6c4b4eee56bed5bf0e214820a5f81312650be64cf`  
		Last Modified: Fri, 18 Nov 2022 18:55:46 GMT  
		Size: 298.4 MB (298425888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15eaa52f90ffd951ff72991440bbf786b70e29887c6aac6337a8a778504b135e`  
		Last Modified: Fri, 18 Nov 2022 18:55:19 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7997f2f2f20f25fc39c97114744f2d8d8bf61520dcf9641712b83c710b9c87f4`  
		Last Modified: Fri, 18 Nov 2022 18:55:19 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2-alpine` - linux; arm variant v7

```console
$ docker pull satosa@sha256:3bae4cd91de90ed4b33d66d1f77a22cd0b9fcd0ab1b4eaef2cff5417c9275733
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325957233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f631246a1547940b3f84d445fda67d7237809b05753009f90e9037abebd08a84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:12:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 08:12:04 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 08:12:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 08:38:23 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 08:38:23 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 09:08:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 09:08:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 09:08:09 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 09:08:09 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 05:31:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 05:31:37 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 05:31:43 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 05:31:44 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 19:02:52 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 19:02:52 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 19:07:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 19:07:42 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 19:07:42 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 19:07:43 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 19:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 19:07:43 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 19:07:43 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 19:07:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb04c1ebc7f7005f359b85d4698d031de9ca4a4e8bc776ac6faa3f052b3a3f1`  
		Last Modified: Sat, 12 Nov 2022 10:03:05 GMT  
		Size: 659.3 KB (659291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997ef90ff733ebe7a201a71b832a552bd33839b74047f89bc3f1f00139c6e629`  
		Last Modified: Sat, 12 Nov 2022 10:03:50 GMT  
		Size: 12.0 MB (11996460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2e907876797a7e7631369ff616b83ed0b57d0c152d486322351a767e140814`  
		Last Modified: Sat, 12 Nov 2022 10:03:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0291337573b1029d149b2fca6ebe6b0b3601a0d0f5eaecc06c1e75696f8c6731`  
		Last Modified: Wed, 16 Nov 2022 08:16:48 GMT  
		Size: 3.1 MB (3056225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8f69cf77b68a4b6e967edd1ed5cebd3eda7ce3b4c37d3cc3c6c80941a0509`  
		Last Modified: Fri, 18 Nov 2022 19:09:23 GMT  
		Size: 9.5 MB (9499491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63ac0856d1f8f6029e19cbd1091942b95aa2bf50d51d2e6be43d3fbe7f3bb7d`  
		Last Modified: Fri, 18 Nov 2022 19:09:51 GMT  
		Size: 298.3 MB (298315139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8470d03ed17d2c6c783bb46ad242efce0cc3f549f5b98e001e42fda3b56824b8`  
		Last Modified: Fri, 18 Nov 2022 19:09:21 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598946608775d3c0df6899c4da0bfec0d2ef162decc5c884d73764d4a72f6789`  
		Last Modified: Fri, 18 Nov 2022 19:09:21 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2-alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:2c93dd162547b7b44c8202cf0599e16fb7d2a686c396e6130f122c1b3f61dc4e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46167316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4ccc5a457a36ea94161437a8f9f5053f0e75d381326a3d6a0d8e1e91cc02a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:23:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 08:16:58 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 08:16:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 08:35:03 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 08:35:03 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 08:53:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 08:53:19 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 08:53:19 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 08:53:19 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:18:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:18:37 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:18:42 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:18:42 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:48:20 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:48:20 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:49:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:49:01 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:49:01 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:49:01 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:49:01 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:49:01 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:49:01 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e190eeb0612a6514b857c64886ec8f64d8e235210be5682cf6abbc5bd172b135`  
		Last Modified: Sat, 12 Nov 2022 09:21:43 GMT  
		Size: 663.1 KB (663101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4727b51eed627eface71c55490f3017153992b7d9ae395a99b1e11841128d06`  
		Last Modified: Sat, 12 Nov 2022 09:22:08 GMT  
		Size: 13.1 MB (13073328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce34a3004b391575b577e7922f6d501a0b8ba079dc0741b068b86558c26ee4a1`  
		Last Modified: Sat, 12 Nov 2022 09:22:06 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c270266b6f1942f4120af4ec7278184a61adb708209c33c2320154d82f8a31`  
		Last Modified: Wed, 16 Nov 2022 01:27:26 GMT  
		Size: 3.1 MB (3056436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286cee3bdb5335ff6bca12b16beabdce685e5fdb0a9d0561b1e6cb24ba774152`  
		Last Modified: Fri, 18 Nov 2022 18:49:43 GMT  
		Size: 9.7 MB (9699369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fc21cbba39c03767e72e06461ef113f17eae2671200bbff9598e569d7b5be7`  
		Last Modified: Fri, 18 Nov 2022 18:49:45 GMT  
		Size: 17.0 MB (16955466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5513e43b833e2f30026902bd7a4a1af1addd71ecb1736426f8252fc49d442006`  
		Last Modified: Fri, 18 Nov 2022 18:49:43 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed37a61b2c4a8b46b1ab69bf0c36dcccc4b0e44802a41f019fcb2efd750418a3`  
		Last Modified: Fri, 18 Nov 2022 18:49:42 GMT  
		Size: 2.1 KB (2145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2-alpine` - linux; 386

```console
$ docker pull satosa@sha256:2db0679167412bbbf2ab4702b8580f18935847abe845bb15e8472bda6204190d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328240269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9c562b6c31c0440d0e58b8f9b031c6bcbb90cb33beb9032c8b3544236d5c33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:29:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 05:29:12 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 05:29:14 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 05:50:43 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 05:50:44 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 06:11:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 06:11:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 06:11:39 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 06:11:40 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:38:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:38:28 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:38:35 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:38:36 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:43:42 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:43:43 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:47:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:47:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:47:55 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:47:57 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:47:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:47:58 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:47:59 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:48:00 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a152a67ad9fd5011f8da356e104e14cdbd9cd925941bb6c241b50471eef5a520`  
		Last Modified: Sat, 12 Nov 2022 06:51:44 GMT  
		Size: 669.6 KB (669609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81c595fa967dddaa2db39bd0328b1e7e07583641e9870975cc6d7f37a54f069`  
		Last Modified: Sat, 12 Nov 2022 06:52:19 GMT  
		Size: 13.2 MB (13163166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8750f6265e3be5e75d2d9bb8766f7ae3208bd6ec29a99ab721971a438e8692`  
		Last Modified: Sat, 12 Nov 2022 06:52:17 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c32efb655c88520610dfffc30bc04d2a99130cbac9bd50f8f43c0a37aef6d28`  
		Last Modified: Wed, 16 Nov 2022 01:52:46 GMT  
		Size: 3.1 MB (3054164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e426180bebf4c41e9095922812af13b228b8a1891f925b18c6418706d09d589c`  
		Last Modified: Fri, 18 Nov 2022 18:49:32 GMT  
		Size: 10.0 MB (9981921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35638e3376e5dee654e447a8aded8def08d009dc15a9a6492ea89f0f6cf991d`  
		Last Modified: Fri, 18 Nov 2022 18:49:48 GMT  
		Size: 298.6 MB (298551244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed3a4f7081736c94dcc732f68489dc73f4dbfb0033bb1565e56218bf56e0eba`  
		Last Modified: Fri, 18 Nov 2022 18:49:31 GMT  
		Size: 9.4 KB (9437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84eedc2257c4e9334b63cca383a14503a49dcd221ab8e62a83dd2811a1c87895`  
		Last Modified: Fri, 18 Nov 2022 18:49:31 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2-alpine` - linux; ppc64le

```console
$ docker pull satosa@sha256:78f6a669461f794f0b3dd8e4ed981afb6864275142dd4e3e84b2c9d9e502f748
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328360558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c362cb6cae301a29e6e4675274c3ec62a3fab9aa0ca147eb8167fb57c2d3c92e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 09:09:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 09:09:52 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 09:09:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 09:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 09:49:13 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 10:29:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 10:29:46 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 10:29:47 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 10:29:47 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:28:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:28:15 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:28:26 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:28:27 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:25:31 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:25:31 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:33:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:34:00 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:34:01 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:34:01 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:34:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:34:02 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:34:02 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:34:02 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0578c681eac19aa83cc60a5d383147a7c56a35a3ac13286945daa470f25157e`  
		Last Modified: Sat, 12 Nov 2022 11:31:49 GMT  
		Size: 670.3 KB (670297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bcec55fc14204d6d5b10511d2dcb4b565f19ea0c07a815947bf4616259786f`  
		Last Modified: Sat, 12 Nov 2022 11:32:23 GMT  
		Size: 13.3 MB (13307557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd9e47c00af72c31f09498bcdbb9f23c6b599d96b3262a847fd18af79d8ec83`  
		Last Modified: Sat, 12 Nov 2022 11:32:20 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbba60b66096fca5cbb93d7c032bf2aa7755ea3c73fcddca01bb6d3af1fb0f86`  
		Last Modified: Wed, 16 Nov 2022 07:01:58 GMT  
		Size: 3.1 MB (3056418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59aba7b954790c375454d90d43b7e21ef374bf3fc2cfbca50b660cb08066a22b`  
		Last Modified: Fri, 18 Nov 2022 18:35:37 GMT  
		Size: 10.0 MB (9950742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840cb6e59e4841e4831f3736de75cdf2d9a9d41a587a37d4f6eb185bc212f816`  
		Last Modified: Fri, 18 Nov 2022 18:36:05 GMT  
		Size: 298.6 MB (298562127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605fa8f9b6826c59c0ecc11cc54f8a7a6193c33cee3839935c7409ec2c4bd610`  
		Last Modified: Fri, 18 Nov 2022 18:35:34 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f7512564d5a154d9f72c5ff30f44cfb66410e160250b0ffba25e4abaaaacd1`  
		Last Modified: Fri, 18 Nov 2022 18:35:34 GMT  
		Size: 2.2 KB (2151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.2-alpine3.16`

```console
$ docker pull satosa@sha256:96837510b982a984c0f69c23c7424082c1030cd0ca1de70f3a1dda2d5e3a9688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `satosa:8.2-alpine3.16` - linux; amd64

```console
$ docker pull satosa@sha256:6e3e4da73ae0c0d1ee3192a90d4e47dd1711df0f3e2d5cda5ec9b5d0146dc48b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c03699dd38f4ddbe3655ace3de96f6a1cef874a71cdabefd8c2f24970096df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:56:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 06:39:07 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 06:39:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 06:57:28 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 06:57:28 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 07:15:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 07:15:59 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 07:15:59 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 07:15:59 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:56:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:56:08 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:56:15 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:56:15 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:22:15 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:22:15 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:22:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:23:00 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:23:00 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:23:00 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:23:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:23:01 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:23:01 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:23:01 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e124a36b9ab9caae9b9b43bffcb6f6d9f126ab89cf2a8b20b9a6f912df03d36`  
		Last Modified: Sat, 12 Nov 2022 07:47:59 GMT  
		Size: 661.8 KB (661831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86456952aa287ca80ac7d7f349dc9edbabda9393ab022d20f2e4c2263cd7d2e7`  
		Last Modified: Sat, 12 Nov 2022 07:48:26 GMT  
		Size: 13.0 MB (12998794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ece9ef7a5797feb2ddaf23aee223848643c0baaedaaa203c721aecb6b272b25`  
		Last Modified: Sat, 12 Nov 2022 07:48:24 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef27b859822294ab1253f8e09a8712d63ea9939eadd1dc4b595d52726c0b020d`  
		Last Modified: Wed, 16 Nov 2022 07:05:43 GMT  
		Size: 3.1 MB (3056443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824935fc626e0971164be442423360798c85d529053e967a909cd1273bda190e`  
		Last Modified: Fri, 18 Nov 2022 18:23:39 GMT  
		Size: 10.9 MB (10872324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fed4aaf1a18111683af619a1e71edd5804307567ed23a83f6f40d15d2794af`  
		Last Modified: Fri, 18 Nov 2022 18:23:41 GMT  
		Size: 17.4 MB (17363712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e090e2c9c7e5d74822d9f71487ec5a71f3058a6f2d8bf756ddaaed8180da06e`  
		Last Modified: Fri, 18 Nov 2022 18:23:38 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41247ef96bde894139c620ba77d7e56bed539612bc8605d4495a7b78bd90ebfb`  
		Last Modified: Fri, 18 Nov 2022 18:23:38 GMT  
		Size: 2.1 KB (2146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2-alpine3.16` - linux; arm variant v6

```console
$ docker pull satosa@sha256:a6fbc6091cf0e1a4e5f6e3d7f2cb1e798e64a2324ff1c80eb9d46b342c11fd39
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327070023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313e9fa4c6d8a5fe836e6b47a9dcef3b27b5b56032c637bb8c15c6c2ecaba99b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:28:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 06:28:49 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 06:28:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 06:55:00 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 06:55:00 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 07:21:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 07:21:39 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 07:21:39 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 07:21:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:41:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:41:32 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:41:39 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:41:39 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:49:39 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:49:39 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:54:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:54:44 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:54:44 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:54:44 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:54:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:54:44 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:54:44 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:54:44 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe974d15ab7b1ace1e4997a68bcfb22f2652af9f902f110d0a90fbdd2ef2053`  
		Last Modified: Sat, 12 Nov 2022 08:03:00 GMT  
		Size: 666.2 KB (666196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69683a8852c8900b94150a78af049bb63d4f73fbdd7239fba1302b9b211ec82`  
		Last Modified: Sat, 12 Nov 2022 08:03:24 GMT  
		Size: 12.5 MB (12545209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63725fb700eaa74dc7942aef8ee5d333eb6b74e224f29ff11f0a997c56208595`  
		Last Modified: Sat, 12 Nov 2022 08:03:22 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012ec3c62fe317e21430242a858a7e489044f55ef1b0398a0c40d9b08e49a357`  
		Last Modified: Wed, 16 Nov 2022 00:46:22 GMT  
		Size: 3.1 MB (3056167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f055f28d65cb7615e57588e003562504a3430b08b6f6e1b13afde191879907f`  
		Last Modified: Fri, 18 Nov 2022 18:55:21 GMT  
		Size: 9.7 MB (9749625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328dee8fb8e4a3a68d2eaea6c4b4eee56bed5bf0e214820a5f81312650be64cf`  
		Last Modified: Fri, 18 Nov 2022 18:55:46 GMT  
		Size: 298.4 MB (298425888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15eaa52f90ffd951ff72991440bbf786b70e29887c6aac6337a8a778504b135e`  
		Last Modified: Fri, 18 Nov 2022 18:55:19 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7997f2f2f20f25fc39c97114744f2d8d8bf61520dcf9641712b83c710b9c87f4`  
		Last Modified: Fri, 18 Nov 2022 18:55:19 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2-alpine3.16` - linux; arm variant v7

```console
$ docker pull satosa@sha256:3bae4cd91de90ed4b33d66d1f77a22cd0b9fcd0ab1b4eaef2cff5417c9275733
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325957233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f631246a1547940b3f84d445fda67d7237809b05753009f90e9037abebd08a84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:12:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 08:12:04 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 08:12:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 08:38:23 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 08:38:23 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 09:08:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 09:08:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 09:08:09 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 09:08:09 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 05:31:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 05:31:37 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 05:31:43 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 05:31:44 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 19:02:52 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 19:02:52 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 19:07:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 19:07:42 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 19:07:42 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 19:07:43 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 19:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 19:07:43 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 19:07:43 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 19:07:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb04c1ebc7f7005f359b85d4698d031de9ca4a4e8bc776ac6faa3f052b3a3f1`  
		Last Modified: Sat, 12 Nov 2022 10:03:05 GMT  
		Size: 659.3 KB (659291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997ef90ff733ebe7a201a71b832a552bd33839b74047f89bc3f1f00139c6e629`  
		Last Modified: Sat, 12 Nov 2022 10:03:50 GMT  
		Size: 12.0 MB (11996460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2e907876797a7e7631369ff616b83ed0b57d0c152d486322351a767e140814`  
		Last Modified: Sat, 12 Nov 2022 10:03:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0291337573b1029d149b2fca6ebe6b0b3601a0d0f5eaecc06c1e75696f8c6731`  
		Last Modified: Wed, 16 Nov 2022 08:16:48 GMT  
		Size: 3.1 MB (3056225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8f69cf77b68a4b6e967edd1ed5cebd3eda7ce3b4c37d3cc3c6c80941a0509`  
		Last Modified: Fri, 18 Nov 2022 19:09:23 GMT  
		Size: 9.5 MB (9499491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63ac0856d1f8f6029e19cbd1091942b95aa2bf50d51d2e6be43d3fbe7f3bb7d`  
		Last Modified: Fri, 18 Nov 2022 19:09:51 GMT  
		Size: 298.3 MB (298315139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8470d03ed17d2c6c783bb46ad242efce0cc3f549f5b98e001e42fda3b56824b8`  
		Last Modified: Fri, 18 Nov 2022 19:09:21 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598946608775d3c0df6899c4da0bfec0d2ef162decc5c884d73764d4a72f6789`  
		Last Modified: Fri, 18 Nov 2022 19:09:21 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:2c93dd162547b7b44c8202cf0599e16fb7d2a686c396e6130f122c1b3f61dc4e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46167316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4ccc5a457a36ea94161437a8f9f5053f0e75d381326a3d6a0d8e1e91cc02a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:23:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 08:16:58 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 08:16:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 08:35:03 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 08:35:03 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 08:53:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 08:53:19 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 08:53:19 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 08:53:19 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:18:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:18:37 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:18:42 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:18:42 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:48:20 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:48:20 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:49:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:49:01 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:49:01 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:49:01 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:49:01 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:49:01 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:49:01 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e190eeb0612a6514b857c64886ec8f64d8e235210be5682cf6abbc5bd172b135`  
		Last Modified: Sat, 12 Nov 2022 09:21:43 GMT  
		Size: 663.1 KB (663101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4727b51eed627eface71c55490f3017153992b7d9ae395a99b1e11841128d06`  
		Last Modified: Sat, 12 Nov 2022 09:22:08 GMT  
		Size: 13.1 MB (13073328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce34a3004b391575b577e7922f6d501a0b8ba079dc0741b068b86558c26ee4a1`  
		Last Modified: Sat, 12 Nov 2022 09:22:06 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c270266b6f1942f4120af4ec7278184a61adb708209c33c2320154d82f8a31`  
		Last Modified: Wed, 16 Nov 2022 01:27:26 GMT  
		Size: 3.1 MB (3056436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286cee3bdb5335ff6bca12b16beabdce685e5fdb0a9d0561b1e6cb24ba774152`  
		Last Modified: Fri, 18 Nov 2022 18:49:43 GMT  
		Size: 9.7 MB (9699369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fc21cbba39c03767e72e06461ef113f17eae2671200bbff9598e569d7b5be7`  
		Last Modified: Fri, 18 Nov 2022 18:49:45 GMT  
		Size: 17.0 MB (16955466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5513e43b833e2f30026902bd7a4a1af1addd71ecb1736426f8252fc49d442006`  
		Last Modified: Fri, 18 Nov 2022 18:49:43 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed37a61b2c4a8b46b1ab69bf0c36dcccc4b0e44802a41f019fcb2efd750418a3`  
		Last Modified: Fri, 18 Nov 2022 18:49:42 GMT  
		Size: 2.1 KB (2145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2-alpine3.16` - linux; 386

```console
$ docker pull satosa@sha256:2db0679167412bbbf2ab4702b8580f18935847abe845bb15e8472bda6204190d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328240269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9c562b6c31c0440d0e58b8f9b031c6bcbb90cb33beb9032c8b3544236d5c33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:29:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 05:29:12 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 05:29:14 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 05:50:43 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 05:50:44 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 06:11:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 06:11:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 06:11:39 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 06:11:40 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:38:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:38:28 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:38:35 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:38:36 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:43:42 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:43:43 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:47:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:47:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:47:55 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:47:57 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:47:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:47:58 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:47:59 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:48:00 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a152a67ad9fd5011f8da356e104e14cdbd9cd925941bb6c241b50471eef5a520`  
		Last Modified: Sat, 12 Nov 2022 06:51:44 GMT  
		Size: 669.6 KB (669609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81c595fa967dddaa2db39bd0328b1e7e07583641e9870975cc6d7f37a54f069`  
		Last Modified: Sat, 12 Nov 2022 06:52:19 GMT  
		Size: 13.2 MB (13163166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8750f6265e3be5e75d2d9bb8766f7ae3208bd6ec29a99ab721971a438e8692`  
		Last Modified: Sat, 12 Nov 2022 06:52:17 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c32efb655c88520610dfffc30bc04d2a99130cbac9bd50f8f43c0a37aef6d28`  
		Last Modified: Wed, 16 Nov 2022 01:52:46 GMT  
		Size: 3.1 MB (3054164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e426180bebf4c41e9095922812af13b228b8a1891f925b18c6418706d09d589c`  
		Last Modified: Fri, 18 Nov 2022 18:49:32 GMT  
		Size: 10.0 MB (9981921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35638e3376e5dee654e447a8aded8def08d009dc15a9a6492ea89f0f6cf991d`  
		Last Modified: Fri, 18 Nov 2022 18:49:48 GMT  
		Size: 298.6 MB (298551244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed3a4f7081736c94dcc732f68489dc73f4dbfb0033bb1565e56218bf56e0eba`  
		Last Modified: Fri, 18 Nov 2022 18:49:31 GMT  
		Size: 9.4 KB (9437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84eedc2257c4e9334b63cca383a14503a49dcd221ab8e62a83dd2811a1c87895`  
		Last Modified: Fri, 18 Nov 2022 18:49:31 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2-alpine3.16` - linux; ppc64le

```console
$ docker pull satosa@sha256:78f6a669461f794f0b3dd8e4ed981afb6864275142dd4e3e84b2c9d9e502f748
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328360558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c362cb6cae301a29e6e4675274c3ec62a3fab9aa0ca147eb8167fb57c2d3c92e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 09:09:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 09:09:52 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 09:09:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 09:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 09:49:13 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 10:29:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 10:29:46 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 10:29:47 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 10:29:47 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:28:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:28:15 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:28:26 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:28:27 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:25:31 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:25:31 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:33:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:34:00 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:34:01 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:34:01 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:34:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:34:02 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:34:02 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:34:02 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0578c681eac19aa83cc60a5d383147a7c56a35a3ac13286945daa470f25157e`  
		Last Modified: Sat, 12 Nov 2022 11:31:49 GMT  
		Size: 670.3 KB (670297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bcec55fc14204d6d5b10511d2dcb4b565f19ea0c07a815947bf4616259786f`  
		Last Modified: Sat, 12 Nov 2022 11:32:23 GMT  
		Size: 13.3 MB (13307557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd9e47c00af72c31f09498bcdbb9f23c6b599d96b3262a847fd18af79d8ec83`  
		Last Modified: Sat, 12 Nov 2022 11:32:20 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbba60b66096fca5cbb93d7c032bf2aa7755ea3c73fcddca01bb6d3af1fb0f86`  
		Last Modified: Wed, 16 Nov 2022 07:01:58 GMT  
		Size: 3.1 MB (3056418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59aba7b954790c375454d90d43b7e21ef374bf3fc2cfbca50b660cb08066a22b`  
		Last Modified: Fri, 18 Nov 2022 18:35:37 GMT  
		Size: 10.0 MB (9950742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840cb6e59e4841e4831f3736de75cdf2d9a9d41a587a37d4f6eb185bc212f816`  
		Last Modified: Fri, 18 Nov 2022 18:36:05 GMT  
		Size: 298.6 MB (298562127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605fa8f9b6826c59c0ecc11cc54f8a7a6193c33cee3839935c7409ec2c4bd610`  
		Last Modified: Fri, 18 Nov 2022 18:35:34 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f7512564d5a154d9f72c5ff30f44cfb66410e160250b0ffba25e4abaaaacd1`  
		Last Modified: Fri, 18 Nov 2022 18:35:34 GMT  
		Size: 2.2 KB (2151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.2-bullseye`

```console
$ docker pull satosa@sha256:920b2db648258e4779443b954cbc17015f3e7feda80d41ee006fdf102363bce8
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

### `satosa:8.2-bullseye` - linux; amd64

```console
$ docker pull satosa@sha256:2b75f1966b97e958ab7b3edb499a68b28221198f61990a4e20b66bf461a02dfb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87754433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da994718d5841d288b6e518373ab9111b96651fc972c162c8ec1e737bb52fd08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 18:54:42 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 18:54:42 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 18:54:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 20:02:05 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 20:02:05 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 20:16:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 20:16:53 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 20:16:53 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 20:16:53 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:55:31 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:55:32 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:55:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:55:42 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:27:35 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:27:35 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:28:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:28:36 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:28:36 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:28:36 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:28:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:28:36 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:28:36 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:28:36 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00aaacf759c581712fa578a6b4e8e0b9fc780919a5d835a168457b754755644`  
		Last Modified: Tue, 15 Nov 2022 22:58:09 GMT  
		Size: 1.1 MB (1077982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b9691827181afb85e2027be1b34b948a9de4110f0253de4e0c9dfcf1559f7b`  
		Last Modified: Tue, 15 Nov 2022 22:59:24 GMT  
		Size: 12.6 MB (12586017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf69ec4fb1d1d974ad18c827b094bb4a4242791b94344e6f059ed9d0b8eb62be`  
		Last Modified: Tue, 15 Nov 2022 22:59:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7bf64971b8ca870b8bc8476ffc783c777f6bb3bb53e50d8e719f1ea1bad697`  
		Last Modified: Wed, 16 Nov 2022 07:04:31 GMT  
		Size: 3.3 MB (3348953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c001071f815bdbd3fc5e231343c0b4b3337b9d339bd507162ce825aa8eff5643`  
		Last Modified: Mon, 21 Nov 2022 19:29:13 GMT  
		Size: 21.1 MB (21096341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c4d15fc7d1e06ddff844be580c929a202aeef96ed8cb426f2e1f60c6291d80`  
		Last Modified: Mon, 21 Nov 2022 19:29:14 GMT  
		Size: 18.2 MB (18220647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6220bf882cf516ac06374d47fe5f7eb9cb8ac7207c16648c87262453bcb5dd`  
		Last Modified: Mon, 21 Nov 2022 19:29:10 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9610156b7a28fe2c40ba7509e651e32b895a71e7c2999362f9d0dcdefefc7830`  
		Last Modified: Mon, 21 Nov 2022 19:29:10 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2-bullseye` - linux; arm variant v5

```console
$ docker pull satosa@sha256:191432b034c13284a7a750492dc4bbbaab7cbdab72b127ccdc3276685c0a6277
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.3 MB (374337256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddea723e3d8081cb37968943d59ce80b13516d5314627468f2f689ac477edb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:49:18 GMT
ADD file:1949af7e583a1b54055a421129c32315fc101e53e2cda05da3171ed461bde0a6 in / 
# Tue, 15 Nov 2022 01:49:19 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:45:56 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 07:45:56 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 07:46:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 08:28:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 08:28:59 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 08:51:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 08:51:04 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 08:51:04 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 08:51:04 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:33:16 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:33:16 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:33:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:33:32 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:48:45 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:48:45 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:53:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:53:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:53:25 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:53:26 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:53:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:53:26 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:53:26 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:53:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b56836d864a6d857be3d12242b65962f2a2cf0d77c48cfb85bbbdf9d56a7e93d`  
		Last Modified: Tue, 15 Nov 2022 01:54:26 GMT  
		Size: 28.9 MB (28914126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a6e5b3ab314e2965853a4ddc03100cfb0fd0d2825cdc2fb4f1bc363cca39b9`  
		Last Modified: Tue, 15 Nov 2022 10:08:43 GMT  
		Size: 1.1 MB (1060732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db96a74ae1eb60de22f4973a045a1b638a39090565ee2fdf0d4a8c4319bf21c`  
		Last Modified: Tue, 15 Nov 2022 10:09:24 GMT  
		Size: 12.1 MB (12146339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb7e08f0a09cbc7e1269f3c705f9ff28966afe27388fc990a03c00f3200360a`  
		Last Modified: Tue, 15 Nov 2022 10:09:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdc4079d02fdf319fd5aa22d26a4a8b2ec80e3f8beb0ada18ed0aa2ace5e0d7`  
		Last Modified: Wed, 16 Nov 2022 00:39:40 GMT  
		Size: 3.3 MB (3348246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0106290c3f2418d61678711f86fda97637dff84ccfae811034f743dcae2eb8`  
		Last Modified: Mon, 21 Nov 2022 19:54:08 GMT  
		Size: 22.7 MB (22693132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745925b8b4315a2b9b975665bd6158b73df587417a7fade9559f85ddfc27139d`  
		Last Modified: Mon, 21 Nov 2022 19:54:31 GMT  
		Size: 306.2 MB (306162846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c0f3ca52005fb9ed30e05bac90f93fbd6237467e4145b4950ac388200c78fc`  
		Last Modified: Mon, 21 Nov 2022 19:54:04 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15ae5fb82b045c21046c703a63283b8053930321884f0aa7174a12966b6fb46`  
		Last Modified: Mon, 21 Nov 2022 19:54:04 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2-bullseye` - linux; arm variant v7

```console
$ docker pull satosa@sha256:c31d3aa2b933736a4d50e795d7d017bdbe9163970108978759602cc4b09333de
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.1 MB (371088257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d8463fe00f06c45603677eff859db0d7b45fc077a01e06584c25b28d75a300`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 03:43:25 GMT
ADD file:1b5c939bd2a35667d7fc44c3009a56ed92a932f512a73df1617dec6ccbd6e6b1 in / 
# Tue, 15 Nov 2022 03:43:26 GMT
CMD ["bash"]
# Wed, 16 Nov 2022 02:10:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Nov 2022 02:10:52 GMT
ENV LANG=C.UTF-8
# Wed, 16 Nov 2022 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Nov 2022 04:26:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 16 Nov 2022 04:26:07 GMT
ENV PYTHON_VERSION=3.11.0
# Wed, 16 Nov 2022 04:47:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 16 Nov 2022 04:47:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_PIP_VERSION=22.3
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 04:47:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 04:47:40 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:58:12 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:58:13 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 20:02:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 20:02:37 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 20:02:37 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 20:02:38 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 20:02:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 20:02:38 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 20:02:38 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 20:02:38 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:fd18d0201d0ce0c5e103902d894f5d601fc5dde76688aa7dae786840141d23e4`  
		Last Modified: Tue, 15 Nov 2022 03:50:11 GMT  
		Size: 26.6 MB (26576195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f4e2c2480160d1670c2ebb7d1c8290f0a3956265f0069d1de3e5b60d587141`  
		Last Modified: Wed, 16 Nov 2022 08:13:53 GMT  
		Size: 1.0 MB (1042833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9254168af81f2bf98cb621d697e2b624446620a5acce3412a20ed6f6912fd248`  
		Last Modified: Wed, 16 Nov 2022 08:15:35 GMT  
		Size: 11.6 MB (11642276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a40d929533b6fb9173ac38ebf09de1f187f9aa8c6b49de778a38b52abbda11`  
		Last Modified: Wed, 16 Nov 2022 08:15:33 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b04522957691b19b0ac6940e157f56337b27084782602ad4d8a7229397944e1`  
		Last Modified: Wed, 16 Nov 2022 08:15:34 GMT  
		Size: 3.3 MB (3348201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978ebe46f9e524ab17da6008d165ad70ca5187930fb4cd7fc6cd17cccbe7002e`  
		Last Modified: Mon, 21 Nov 2022 20:03:41 GMT  
		Size: 22.4 MB (22430741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa27795d0d8f0524db63e5fbf00dcc9ac44cfeb68c3a66350870d3c3e903fe9`  
		Last Modified: Mon, 21 Nov 2022 20:04:05 GMT  
		Size: 306.0 MB (306036175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5483a349efd69231e68a3b2f9212afd52f92c5498da8c707b5a60f90db6399a`  
		Last Modified: Mon, 21 Nov 2022 20:03:37 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa6d2f8593d4d5bca10332fd90d782e457560c6a50b6fd53614a5eb88d04109`  
		Last Modified: Mon, 21 Nov 2022 20:03:37 GMT  
		Size: 2.1 KB (2144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:a654eeeefb6f573740cf6dc83bc68eb3ff1ad0e4ab660417964ee9664772c6a9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85480362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa7f1d11b3d6d0006e3d3dce2de48cfc52f63ddd139cfddfd1a79675972969b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:41:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 07:41:31 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 07:41:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 08:34:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 08:34:07 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 08:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 08:47:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 08:47:37 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 08:47:37 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:17:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:17:57 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:18:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:18:07 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:49:25 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:49:25 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:50:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:50:21 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:50:21 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:50:21 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:50:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:50:21 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:50:21 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:50:21 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbd8719487c40bfcc7d42d53f202d1dbbbb7ac0fb4e4919ed791664b7f4e47b`  
		Last Modified: Tue, 15 Nov 2022 10:55:04 GMT  
		Size: 1.1 MB (1065870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb07c67a71797e21118367f8ed3ec8f9561b4e4e3f662aed2467c97a93a6dc3f`  
		Last Modified: Tue, 15 Nov 2022 10:56:03 GMT  
		Size: 12.6 MB (12637055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130567c01926a008d097f8a10e6c4348f8cf6f6bae2df7860e1ebad57caf457d`  
		Last Modified: Tue, 15 Nov 2022 10:56:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad488014eea42b129f9a60d9258bfd09ddf59c75a5ccdc55e196cc0eef88cfe`  
		Last Modified: Wed, 16 Nov 2022 01:26:28 GMT  
		Size: 3.3 MB (3348606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cc72b0c430a3bd0d92649200cd8c6da867ea3a7f33b5066d9b8bae085c587c`  
		Last Modified: Mon, 21 Nov 2022 19:50:50 GMT  
		Size: 21.0 MB (20975486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c84b4c195beedd08e708b18de7f11a9e87d3ac3ef1bed9904140963320cb472`  
		Last Modified: Mon, 21 Nov 2022 19:50:50 GMT  
		Size: 17.4 MB (17380880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15489ffd1801184e8a797e1467fb0a83eec71433d9efe85b7fcc060f9c77547`  
		Last Modified: Mon, 21 Nov 2022 19:50:47 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6345651cb201b249a31896d42f4f630bd5f4ee5dc259842a415b1e1d21bc36ab`  
		Last Modified: Mon, 21 Nov 2022 19:50:47 GMT  
		Size: 2.1 KB (2141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2-bullseye` - linux; 386

```console
$ docker pull satosa@sha256:34866c133ed80b3650fcac32e7f67597fa1598e16fc84e51e0e8ee340d0e6ca9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 MB (380177011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25aed64d35227d6dd9deb0905d3a0f76dc6e28a9ce7465ec44f6985baf78563`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:27 GMT
ADD file:608bec4ba3e2543714da4c5158f3c46a168f63ee69ac3f48bff54474ba9a6f27 in / 
# Tue, 15 Nov 2022 01:41:27 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 12:57:10 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 12:57:11 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 12:57:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:13:48 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 14:13:49 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 14:32:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 14:32:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 14:32:38 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 14:32:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:37:29 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:37:29 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:37:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:37:42 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:39:08 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:39:08 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:43:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:43:23 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:43:23 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:43:25 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:43:26 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:43:27 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:43:28 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f6a1e975b34444ecb7c6a2b537403fd6b94d2ff3225944ac2ac3b292466e4078`  
		Last Modified: Tue, 15 Nov 2022 01:47:05 GMT  
		Size: 32.4 MB (32392982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a4ead92cc7eae0396b0fbac1238e0bee3f677740a65a67474e08bcbaa003ba`  
		Last Modified: Tue, 15 Nov 2022 17:38:22 GMT  
		Size: 884.5 KB (884461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd0f4ed85c962a057d2c2667c8b4e1a210aea5e2c9e68520214eb87926f684e`  
		Last Modified: Tue, 15 Nov 2022 19:31:55 GMT  
		Size: 12.7 MB (12683309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72250ba4c687654d3be8943b7bf9591f4dc5de08989c26f5654409682ffbdbfd`  
		Last Modified: Tue, 15 Nov 2022 19:31:53 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ffce336712f2fe573ad63960925a12291df3e7598c36c326698f1308f9caae`  
		Last Modified: Wed, 16 Nov 2022 01:51:48 GMT  
		Size: 3.1 MB (3132128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab52fcbbc37aab1d08731873c11e68396df78043d92d74c7faa4c5b09467c928`  
		Last Modified: Mon, 21 Nov 2022 19:44:19 GMT  
		Size: 24.1 MB (24065495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc904879f9ede6886b46d646fa18a746d32afacfe68d200cbd6259eb315d64a5`  
		Last Modified: Mon, 21 Nov 2022 19:44:46 GMT  
		Size: 307.0 MB (307006821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debe7b65c57d841640da19f01ceedfd6f2d319eabb09c1027621317ab5e75159`  
		Last Modified: Mon, 21 Nov 2022 19:44:15 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ea23efc09b0e6df59a86e0ce421416ed60dbfd3ee8016fdf2d744574b117cd`  
		Last Modified: Mon, 21 Nov 2022 19:44:15 GMT  
		Size: 2.1 KB (2143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2-bullseye` - linux; ppc64le

```console
$ docker pull satosa@sha256:aa91656e4b6a0f6b51aa29a1219617190b462ee7f8b0f25fddd786c831f542f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.5 MB (382489126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88774150f37054a63d09106df180126b080812678a23cfb365f6c4c5fcd1ec22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 05:18:45 GMT
ADD file:520926164fdc762143905745329e568c67289232bec450e48645d82a4613dccf in / 
# Tue, 15 Nov 2022 05:18:47 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:06:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 13:06:51 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 13:07:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:38:22 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 14:38:22 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 15:25:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 15:25:30 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 15:25:31 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 15:25:31 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:27:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:27:46 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:28:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:28:07 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:17:24 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:17:25 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:24:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:24:32 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:24:32 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:24:33 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:24:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:24:33 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:24:34 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:24:34 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:c57913b7d0318ef1a47f0348ce54d9865316776aa1ffb2c7871b1473b3d29407`  
		Last Modified: Tue, 15 Nov 2022 05:24:22 GMT  
		Size: 35.3 MB (35285140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa173aadf3e5fa326d1f1b9f9263051781dc9833e8b60e5bb5a9a994739e18ee`  
		Last Modified: Tue, 15 Nov 2022 17:58:02 GMT  
		Size: 1.1 MB (1096202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2c11a6d1874c9a04e310b3de6f884a5db20d8b2819f963dfbb87d255d4041d`  
		Last Modified: Tue, 15 Nov 2022 17:58:54 GMT  
		Size: 13.0 MB (12955764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53510645cb4e75dba43f2960e61295b7e4092e32b65c05d78e4a222a1035b0`  
		Last Modified: Tue, 15 Nov 2022 17:58:50 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76a75d59183d172f23c152a8f9b934d52c2bbe4e381b7d98e6254342b65c9ad`  
		Last Modified: Wed, 16 Nov 2022 07:01:30 GMT  
		Size: 3.3 MB (3349130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789086c936cb86df67a1bcdf02c069f46030c960a874385b1c09458ea09c9e28`  
		Last Modified: Mon, 21 Nov 2022 19:25:29 GMT  
		Size: 23.6 MB (23636418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf604bdc50ad0b740586882da17fa028eb433f3e9291ae1752d62a62443a5dbd`  
		Last Modified: Mon, 21 Nov 2022 19:25:54 GMT  
		Size: 306.2 MB (306154608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24af618620347663fdfc4357acbffd238b3cc0a2d84703ef629fe73ef009c9bf`  
		Last Modified: Mon, 21 Nov 2022 19:25:23 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b025a5ca25095fb82fa5f084b355cf1b4387400fe727ec454daad74044e9445`  
		Last Modified: Mon, 21 Nov 2022 19:25:23 GMT  
		Size: 2.1 KB (2143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2-bullseye` - linux; s390x

```console
$ docker pull satosa@sha256:11d52a081306682d815a39f964424df846d178a0cd0e043c4c6392ff3f219e6a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.2 MB (375225534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec1f645b1f322cd61afb287021cc9f964eccaaecf3250c047df64b92f392d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 10:52:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 10:52:16 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 10:52:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 11:31:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 11:31:14 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 11:46:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 11:46:18 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 11:46:19 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 11:46:19 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:47:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:47:51 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:48:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:48:06 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:42:07 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:42:08 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:46:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:46:10 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:46:10 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:46:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:46:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:46:10 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:46:10 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:46:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1487a90d7d45334f92d990a52e5750391ed66b11532972979f0792745cedca`  
		Last Modified: Tue, 15 Nov 2022 13:07:54 GMT  
		Size: 1.1 MB (1077428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81becff7fb0cea099dc76445874abd672598812e9ae8fb990ce90a07971a00c2`  
		Last Modified: Tue, 15 Nov 2022 13:08:34 GMT  
		Size: 12.4 MB (12422163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e82170644b3fad2be2ca3ce0cd517e5487772520f4eccaf5e60ce99b9533cf`  
		Last Modified: Tue, 15 Nov 2022 13:08:32 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8aa6e35e336a7de98329dc7ecba62f34a24d5eacb447feafcaac381b01a578`  
		Last Modified: Wed, 16 Nov 2022 00:58:52 GMT  
		Size: 3.3 MB (3348811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55521d94cc6014114d16684de5cf415a987eb5306bb707b2c9c89612bae7434`  
		Last Modified: Mon, 21 Nov 2022 19:46:42 GMT  
		Size: 21.0 MB (21008499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453920ba520592eb4a4712ce352cacced35e45b4c29dc9ba96af152f4263f10a`  
		Last Modified: Mon, 21 Nov 2022 19:46:54 GMT  
		Size: 307.7 MB (307712990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b654413945b74c59b340cba2b01bbd308650ac51a2cefcaede178af5de4e030`  
		Last Modified: Mon, 21 Nov 2022 19:46:39 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a8d82d6fccb2478507a3f5986cf0cf8538a12e3f01d8780e85ed975218703`  
		Last Modified: Mon, 21 Nov 2022 19:46:40 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.2.0`

```console
$ docker pull satosa@sha256:920b2db648258e4779443b954cbc17015f3e7feda80d41ee006fdf102363bce8
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

### `satosa:8.2.0` - linux; amd64

```console
$ docker pull satosa@sha256:2b75f1966b97e958ab7b3edb499a68b28221198f61990a4e20b66bf461a02dfb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87754433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da994718d5841d288b6e518373ab9111b96651fc972c162c8ec1e737bb52fd08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 18:54:42 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 18:54:42 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 18:54:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 20:02:05 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 20:02:05 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 20:16:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 20:16:53 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 20:16:53 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 20:16:53 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:55:31 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:55:32 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:55:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:55:42 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:27:35 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:27:35 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:28:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:28:36 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:28:36 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:28:36 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:28:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:28:36 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:28:36 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:28:36 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00aaacf759c581712fa578a6b4e8e0b9fc780919a5d835a168457b754755644`  
		Last Modified: Tue, 15 Nov 2022 22:58:09 GMT  
		Size: 1.1 MB (1077982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b9691827181afb85e2027be1b34b948a9de4110f0253de4e0c9dfcf1559f7b`  
		Last Modified: Tue, 15 Nov 2022 22:59:24 GMT  
		Size: 12.6 MB (12586017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf69ec4fb1d1d974ad18c827b094bb4a4242791b94344e6f059ed9d0b8eb62be`  
		Last Modified: Tue, 15 Nov 2022 22:59:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7bf64971b8ca870b8bc8476ffc783c777f6bb3bb53e50d8e719f1ea1bad697`  
		Last Modified: Wed, 16 Nov 2022 07:04:31 GMT  
		Size: 3.3 MB (3348953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c001071f815bdbd3fc5e231343c0b4b3337b9d339bd507162ce825aa8eff5643`  
		Last Modified: Mon, 21 Nov 2022 19:29:13 GMT  
		Size: 21.1 MB (21096341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c4d15fc7d1e06ddff844be580c929a202aeef96ed8cb426f2e1f60c6291d80`  
		Last Modified: Mon, 21 Nov 2022 19:29:14 GMT  
		Size: 18.2 MB (18220647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6220bf882cf516ac06374d47fe5f7eb9cb8ac7207c16648c87262453bcb5dd`  
		Last Modified: Mon, 21 Nov 2022 19:29:10 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9610156b7a28fe2c40ba7509e651e32b895a71e7c2999362f9d0dcdefefc7830`  
		Last Modified: Mon, 21 Nov 2022 19:29:10 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0` - linux; arm variant v5

```console
$ docker pull satosa@sha256:191432b034c13284a7a750492dc4bbbaab7cbdab72b127ccdc3276685c0a6277
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.3 MB (374337256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddea723e3d8081cb37968943d59ce80b13516d5314627468f2f689ac477edb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:49:18 GMT
ADD file:1949af7e583a1b54055a421129c32315fc101e53e2cda05da3171ed461bde0a6 in / 
# Tue, 15 Nov 2022 01:49:19 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:45:56 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 07:45:56 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 07:46:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 08:28:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 08:28:59 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 08:51:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 08:51:04 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 08:51:04 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 08:51:04 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:33:16 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:33:16 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:33:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:33:32 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:48:45 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:48:45 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:53:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:53:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:53:25 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:53:26 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:53:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:53:26 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:53:26 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:53:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b56836d864a6d857be3d12242b65962f2a2cf0d77c48cfb85bbbdf9d56a7e93d`  
		Last Modified: Tue, 15 Nov 2022 01:54:26 GMT  
		Size: 28.9 MB (28914126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a6e5b3ab314e2965853a4ddc03100cfb0fd0d2825cdc2fb4f1bc363cca39b9`  
		Last Modified: Tue, 15 Nov 2022 10:08:43 GMT  
		Size: 1.1 MB (1060732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db96a74ae1eb60de22f4973a045a1b638a39090565ee2fdf0d4a8c4319bf21c`  
		Last Modified: Tue, 15 Nov 2022 10:09:24 GMT  
		Size: 12.1 MB (12146339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb7e08f0a09cbc7e1269f3c705f9ff28966afe27388fc990a03c00f3200360a`  
		Last Modified: Tue, 15 Nov 2022 10:09:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdc4079d02fdf319fd5aa22d26a4a8b2ec80e3f8beb0ada18ed0aa2ace5e0d7`  
		Last Modified: Wed, 16 Nov 2022 00:39:40 GMT  
		Size: 3.3 MB (3348246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0106290c3f2418d61678711f86fda97637dff84ccfae811034f743dcae2eb8`  
		Last Modified: Mon, 21 Nov 2022 19:54:08 GMT  
		Size: 22.7 MB (22693132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745925b8b4315a2b9b975665bd6158b73df587417a7fade9559f85ddfc27139d`  
		Last Modified: Mon, 21 Nov 2022 19:54:31 GMT  
		Size: 306.2 MB (306162846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c0f3ca52005fb9ed30e05bac90f93fbd6237467e4145b4950ac388200c78fc`  
		Last Modified: Mon, 21 Nov 2022 19:54:04 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15ae5fb82b045c21046c703a63283b8053930321884f0aa7174a12966b6fb46`  
		Last Modified: Mon, 21 Nov 2022 19:54:04 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0` - linux; arm variant v7

```console
$ docker pull satosa@sha256:c31d3aa2b933736a4d50e795d7d017bdbe9163970108978759602cc4b09333de
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.1 MB (371088257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d8463fe00f06c45603677eff859db0d7b45fc077a01e06584c25b28d75a300`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 03:43:25 GMT
ADD file:1b5c939bd2a35667d7fc44c3009a56ed92a932f512a73df1617dec6ccbd6e6b1 in / 
# Tue, 15 Nov 2022 03:43:26 GMT
CMD ["bash"]
# Wed, 16 Nov 2022 02:10:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Nov 2022 02:10:52 GMT
ENV LANG=C.UTF-8
# Wed, 16 Nov 2022 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Nov 2022 04:26:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 16 Nov 2022 04:26:07 GMT
ENV PYTHON_VERSION=3.11.0
# Wed, 16 Nov 2022 04:47:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 16 Nov 2022 04:47:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_PIP_VERSION=22.3
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 04:47:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 04:47:40 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:58:12 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:58:13 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 20:02:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 20:02:37 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 20:02:37 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 20:02:38 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 20:02:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 20:02:38 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 20:02:38 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 20:02:38 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:fd18d0201d0ce0c5e103902d894f5d601fc5dde76688aa7dae786840141d23e4`  
		Last Modified: Tue, 15 Nov 2022 03:50:11 GMT  
		Size: 26.6 MB (26576195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f4e2c2480160d1670c2ebb7d1c8290f0a3956265f0069d1de3e5b60d587141`  
		Last Modified: Wed, 16 Nov 2022 08:13:53 GMT  
		Size: 1.0 MB (1042833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9254168af81f2bf98cb621d697e2b624446620a5acce3412a20ed6f6912fd248`  
		Last Modified: Wed, 16 Nov 2022 08:15:35 GMT  
		Size: 11.6 MB (11642276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a40d929533b6fb9173ac38ebf09de1f187f9aa8c6b49de778a38b52abbda11`  
		Last Modified: Wed, 16 Nov 2022 08:15:33 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b04522957691b19b0ac6940e157f56337b27084782602ad4d8a7229397944e1`  
		Last Modified: Wed, 16 Nov 2022 08:15:34 GMT  
		Size: 3.3 MB (3348201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978ebe46f9e524ab17da6008d165ad70ca5187930fb4cd7fc6cd17cccbe7002e`  
		Last Modified: Mon, 21 Nov 2022 20:03:41 GMT  
		Size: 22.4 MB (22430741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa27795d0d8f0524db63e5fbf00dcc9ac44cfeb68c3a66350870d3c3e903fe9`  
		Last Modified: Mon, 21 Nov 2022 20:04:05 GMT  
		Size: 306.0 MB (306036175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5483a349efd69231e68a3b2f9212afd52f92c5498da8c707b5a60f90db6399a`  
		Last Modified: Mon, 21 Nov 2022 20:03:37 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa6d2f8593d4d5bca10332fd90d782e457560c6a50b6fd53614a5eb88d04109`  
		Last Modified: Mon, 21 Nov 2022 20:03:37 GMT  
		Size: 2.1 KB (2144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:a654eeeefb6f573740cf6dc83bc68eb3ff1ad0e4ab660417964ee9664772c6a9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85480362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa7f1d11b3d6d0006e3d3dce2de48cfc52f63ddd139cfddfd1a79675972969b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:41:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 07:41:31 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 07:41:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 08:34:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 08:34:07 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 08:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 08:47:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 08:47:37 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 08:47:37 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:17:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:17:57 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:18:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:18:07 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:49:25 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:49:25 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:50:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:50:21 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:50:21 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:50:21 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:50:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:50:21 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:50:21 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:50:21 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbd8719487c40bfcc7d42d53f202d1dbbbb7ac0fb4e4919ed791664b7f4e47b`  
		Last Modified: Tue, 15 Nov 2022 10:55:04 GMT  
		Size: 1.1 MB (1065870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb07c67a71797e21118367f8ed3ec8f9561b4e4e3f662aed2467c97a93a6dc3f`  
		Last Modified: Tue, 15 Nov 2022 10:56:03 GMT  
		Size: 12.6 MB (12637055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130567c01926a008d097f8a10e6c4348f8cf6f6bae2df7860e1ebad57caf457d`  
		Last Modified: Tue, 15 Nov 2022 10:56:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad488014eea42b129f9a60d9258bfd09ddf59c75a5ccdc55e196cc0eef88cfe`  
		Last Modified: Wed, 16 Nov 2022 01:26:28 GMT  
		Size: 3.3 MB (3348606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cc72b0c430a3bd0d92649200cd8c6da867ea3a7f33b5066d9b8bae085c587c`  
		Last Modified: Mon, 21 Nov 2022 19:50:50 GMT  
		Size: 21.0 MB (20975486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c84b4c195beedd08e708b18de7f11a9e87d3ac3ef1bed9904140963320cb472`  
		Last Modified: Mon, 21 Nov 2022 19:50:50 GMT  
		Size: 17.4 MB (17380880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15489ffd1801184e8a797e1467fb0a83eec71433d9efe85b7fcc060f9c77547`  
		Last Modified: Mon, 21 Nov 2022 19:50:47 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6345651cb201b249a31896d42f4f630bd5f4ee5dc259842a415b1e1d21bc36ab`  
		Last Modified: Mon, 21 Nov 2022 19:50:47 GMT  
		Size: 2.1 KB (2141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0` - linux; 386

```console
$ docker pull satosa@sha256:34866c133ed80b3650fcac32e7f67597fa1598e16fc84e51e0e8ee340d0e6ca9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 MB (380177011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25aed64d35227d6dd9deb0905d3a0f76dc6e28a9ce7465ec44f6985baf78563`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:27 GMT
ADD file:608bec4ba3e2543714da4c5158f3c46a168f63ee69ac3f48bff54474ba9a6f27 in / 
# Tue, 15 Nov 2022 01:41:27 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 12:57:10 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 12:57:11 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 12:57:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:13:48 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 14:13:49 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 14:32:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 14:32:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 14:32:38 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 14:32:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:37:29 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:37:29 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:37:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:37:42 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:39:08 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:39:08 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:43:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:43:23 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:43:23 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:43:25 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:43:26 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:43:27 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:43:28 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f6a1e975b34444ecb7c6a2b537403fd6b94d2ff3225944ac2ac3b292466e4078`  
		Last Modified: Tue, 15 Nov 2022 01:47:05 GMT  
		Size: 32.4 MB (32392982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a4ead92cc7eae0396b0fbac1238e0bee3f677740a65a67474e08bcbaa003ba`  
		Last Modified: Tue, 15 Nov 2022 17:38:22 GMT  
		Size: 884.5 KB (884461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd0f4ed85c962a057d2c2667c8b4e1a210aea5e2c9e68520214eb87926f684e`  
		Last Modified: Tue, 15 Nov 2022 19:31:55 GMT  
		Size: 12.7 MB (12683309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72250ba4c687654d3be8943b7bf9591f4dc5de08989c26f5654409682ffbdbfd`  
		Last Modified: Tue, 15 Nov 2022 19:31:53 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ffce336712f2fe573ad63960925a12291df3e7598c36c326698f1308f9caae`  
		Last Modified: Wed, 16 Nov 2022 01:51:48 GMT  
		Size: 3.1 MB (3132128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab52fcbbc37aab1d08731873c11e68396df78043d92d74c7faa4c5b09467c928`  
		Last Modified: Mon, 21 Nov 2022 19:44:19 GMT  
		Size: 24.1 MB (24065495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc904879f9ede6886b46d646fa18a746d32afacfe68d200cbd6259eb315d64a5`  
		Last Modified: Mon, 21 Nov 2022 19:44:46 GMT  
		Size: 307.0 MB (307006821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debe7b65c57d841640da19f01ceedfd6f2d319eabb09c1027621317ab5e75159`  
		Last Modified: Mon, 21 Nov 2022 19:44:15 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ea23efc09b0e6df59a86e0ce421416ed60dbfd3ee8016fdf2d744574b117cd`  
		Last Modified: Mon, 21 Nov 2022 19:44:15 GMT  
		Size: 2.1 KB (2143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0` - linux; ppc64le

```console
$ docker pull satosa@sha256:aa91656e4b6a0f6b51aa29a1219617190b462ee7f8b0f25fddd786c831f542f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.5 MB (382489126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88774150f37054a63d09106df180126b080812678a23cfb365f6c4c5fcd1ec22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 05:18:45 GMT
ADD file:520926164fdc762143905745329e568c67289232bec450e48645d82a4613dccf in / 
# Tue, 15 Nov 2022 05:18:47 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:06:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 13:06:51 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 13:07:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:38:22 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 14:38:22 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 15:25:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 15:25:30 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 15:25:31 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 15:25:31 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:27:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:27:46 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:28:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:28:07 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:17:24 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:17:25 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:24:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:24:32 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:24:32 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:24:33 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:24:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:24:33 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:24:34 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:24:34 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:c57913b7d0318ef1a47f0348ce54d9865316776aa1ffb2c7871b1473b3d29407`  
		Last Modified: Tue, 15 Nov 2022 05:24:22 GMT  
		Size: 35.3 MB (35285140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa173aadf3e5fa326d1f1b9f9263051781dc9833e8b60e5bb5a9a994739e18ee`  
		Last Modified: Tue, 15 Nov 2022 17:58:02 GMT  
		Size: 1.1 MB (1096202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2c11a6d1874c9a04e310b3de6f884a5db20d8b2819f963dfbb87d255d4041d`  
		Last Modified: Tue, 15 Nov 2022 17:58:54 GMT  
		Size: 13.0 MB (12955764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53510645cb4e75dba43f2960e61295b7e4092e32b65c05d78e4a222a1035b0`  
		Last Modified: Tue, 15 Nov 2022 17:58:50 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76a75d59183d172f23c152a8f9b934d52c2bbe4e381b7d98e6254342b65c9ad`  
		Last Modified: Wed, 16 Nov 2022 07:01:30 GMT  
		Size: 3.3 MB (3349130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789086c936cb86df67a1bcdf02c069f46030c960a874385b1c09458ea09c9e28`  
		Last Modified: Mon, 21 Nov 2022 19:25:29 GMT  
		Size: 23.6 MB (23636418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf604bdc50ad0b740586882da17fa028eb433f3e9291ae1752d62a62443a5dbd`  
		Last Modified: Mon, 21 Nov 2022 19:25:54 GMT  
		Size: 306.2 MB (306154608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24af618620347663fdfc4357acbffd238b3cc0a2d84703ef629fe73ef009c9bf`  
		Last Modified: Mon, 21 Nov 2022 19:25:23 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b025a5ca25095fb82fa5f084b355cf1b4387400fe727ec454daad74044e9445`  
		Last Modified: Mon, 21 Nov 2022 19:25:23 GMT  
		Size: 2.1 KB (2143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0` - linux; s390x

```console
$ docker pull satosa@sha256:11d52a081306682d815a39f964424df846d178a0cd0e043c4c6392ff3f219e6a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.2 MB (375225534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec1f645b1f322cd61afb287021cc9f964eccaaecf3250c047df64b92f392d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 10:52:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 10:52:16 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 10:52:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 11:31:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 11:31:14 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 11:46:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 11:46:18 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 11:46:19 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 11:46:19 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:47:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:47:51 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:48:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:48:06 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:42:07 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:42:08 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:46:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:46:10 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:46:10 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:46:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:46:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:46:10 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:46:10 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:46:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1487a90d7d45334f92d990a52e5750391ed66b11532972979f0792745cedca`  
		Last Modified: Tue, 15 Nov 2022 13:07:54 GMT  
		Size: 1.1 MB (1077428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81becff7fb0cea099dc76445874abd672598812e9ae8fb990ce90a07971a00c2`  
		Last Modified: Tue, 15 Nov 2022 13:08:34 GMT  
		Size: 12.4 MB (12422163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e82170644b3fad2be2ca3ce0cd517e5487772520f4eccaf5e60ce99b9533cf`  
		Last Modified: Tue, 15 Nov 2022 13:08:32 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8aa6e35e336a7de98329dc7ecba62f34a24d5eacb447feafcaac381b01a578`  
		Last Modified: Wed, 16 Nov 2022 00:58:52 GMT  
		Size: 3.3 MB (3348811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55521d94cc6014114d16684de5cf415a987eb5306bb707b2c9c89612bae7434`  
		Last Modified: Mon, 21 Nov 2022 19:46:42 GMT  
		Size: 21.0 MB (21008499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453920ba520592eb4a4712ce352cacced35e45b4c29dc9ba96af152f4263f10a`  
		Last Modified: Mon, 21 Nov 2022 19:46:54 GMT  
		Size: 307.7 MB (307712990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b654413945b74c59b340cba2b01bbd308650ac51a2cefcaede178af5de4e030`  
		Last Modified: Mon, 21 Nov 2022 19:46:39 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a8d82d6fccb2478507a3f5986cf0cf8538a12e3f01d8780e85ed975218703`  
		Last Modified: Mon, 21 Nov 2022 19:46:40 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.2.0-alpine`

```console
$ docker pull satosa@sha256:96837510b982a984c0f69c23c7424082c1030cd0ca1de70f3a1dda2d5e3a9688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `satosa:8.2.0-alpine` - linux; amd64

```console
$ docker pull satosa@sha256:6e3e4da73ae0c0d1ee3192a90d4e47dd1711df0f3e2d5cda5ec9b5d0146dc48b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c03699dd38f4ddbe3655ace3de96f6a1cef874a71cdabefd8c2f24970096df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:56:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 06:39:07 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 06:39:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 06:57:28 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 06:57:28 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 07:15:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 07:15:59 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 07:15:59 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 07:15:59 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:56:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:56:08 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:56:15 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:56:15 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:22:15 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:22:15 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:22:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:23:00 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:23:00 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:23:00 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:23:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:23:01 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:23:01 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:23:01 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e124a36b9ab9caae9b9b43bffcb6f6d9f126ab89cf2a8b20b9a6f912df03d36`  
		Last Modified: Sat, 12 Nov 2022 07:47:59 GMT  
		Size: 661.8 KB (661831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86456952aa287ca80ac7d7f349dc9edbabda9393ab022d20f2e4c2263cd7d2e7`  
		Last Modified: Sat, 12 Nov 2022 07:48:26 GMT  
		Size: 13.0 MB (12998794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ece9ef7a5797feb2ddaf23aee223848643c0baaedaaa203c721aecb6b272b25`  
		Last Modified: Sat, 12 Nov 2022 07:48:24 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef27b859822294ab1253f8e09a8712d63ea9939eadd1dc4b595d52726c0b020d`  
		Last Modified: Wed, 16 Nov 2022 07:05:43 GMT  
		Size: 3.1 MB (3056443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824935fc626e0971164be442423360798c85d529053e967a909cd1273bda190e`  
		Last Modified: Fri, 18 Nov 2022 18:23:39 GMT  
		Size: 10.9 MB (10872324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fed4aaf1a18111683af619a1e71edd5804307567ed23a83f6f40d15d2794af`  
		Last Modified: Fri, 18 Nov 2022 18:23:41 GMT  
		Size: 17.4 MB (17363712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e090e2c9c7e5d74822d9f71487ec5a71f3058a6f2d8bf756ddaaed8180da06e`  
		Last Modified: Fri, 18 Nov 2022 18:23:38 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41247ef96bde894139c620ba77d7e56bed539612bc8605d4495a7b78bd90ebfb`  
		Last Modified: Fri, 18 Nov 2022 18:23:38 GMT  
		Size: 2.1 KB (2146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0-alpine` - linux; arm variant v6

```console
$ docker pull satosa@sha256:a6fbc6091cf0e1a4e5f6e3d7f2cb1e798e64a2324ff1c80eb9d46b342c11fd39
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327070023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313e9fa4c6d8a5fe836e6b47a9dcef3b27b5b56032c637bb8c15c6c2ecaba99b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:28:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 06:28:49 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 06:28:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 06:55:00 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 06:55:00 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 07:21:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 07:21:39 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 07:21:39 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 07:21:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:41:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:41:32 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:41:39 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:41:39 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:49:39 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:49:39 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:54:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:54:44 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:54:44 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:54:44 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:54:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:54:44 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:54:44 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:54:44 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe974d15ab7b1ace1e4997a68bcfb22f2652af9f902f110d0a90fbdd2ef2053`  
		Last Modified: Sat, 12 Nov 2022 08:03:00 GMT  
		Size: 666.2 KB (666196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69683a8852c8900b94150a78af049bb63d4f73fbdd7239fba1302b9b211ec82`  
		Last Modified: Sat, 12 Nov 2022 08:03:24 GMT  
		Size: 12.5 MB (12545209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63725fb700eaa74dc7942aef8ee5d333eb6b74e224f29ff11f0a997c56208595`  
		Last Modified: Sat, 12 Nov 2022 08:03:22 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012ec3c62fe317e21430242a858a7e489044f55ef1b0398a0c40d9b08e49a357`  
		Last Modified: Wed, 16 Nov 2022 00:46:22 GMT  
		Size: 3.1 MB (3056167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f055f28d65cb7615e57588e003562504a3430b08b6f6e1b13afde191879907f`  
		Last Modified: Fri, 18 Nov 2022 18:55:21 GMT  
		Size: 9.7 MB (9749625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328dee8fb8e4a3a68d2eaea6c4b4eee56bed5bf0e214820a5f81312650be64cf`  
		Last Modified: Fri, 18 Nov 2022 18:55:46 GMT  
		Size: 298.4 MB (298425888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15eaa52f90ffd951ff72991440bbf786b70e29887c6aac6337a8a778504b135e`  
		Last Modified: Fri, 18 Nov 2022 18:55:19 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7997f2f2f20f25fc39c97114744f2d8d8bf61520dcf9641712b83c710b9c87f4`  
		Last Modified: Fri, 18 Nov 2022 18:55:19 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0-alpine` - linux; arm variant v7

```console
$ docker pull satosa@sha256:3bae4cd91de90ed4b33d66d1f77a22cd0b9fcd0ab1b4eaef2cff5417c9275733
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325957233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f631246a1547940b3f84d445fda67d7237809b05753009f90e9037abebd08a84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:12:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 08:12:04 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 08:12:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 08:38:23 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 08:38:23 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 09:08:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 09:08:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 09:08:09 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 09:08:09 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 05:31:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 05:31:37 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 05:31:43 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 05:31:44 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 19:02:52 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 19:02:52 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 19:07:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 19:07:42 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 19:07:42 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 19:07:43 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 19:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 19:07:43 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 19:07:43 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 19:07:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb04c1ebc7f7005f359b85d4698d031de9ca4a4e8bc776ac6faa3f052b3a3f1`  
		Last Modified: Sat, 12 Nov 2022 10:03:05 GMT  
		Size: 659.3 KB (659291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997ef90ff733ebe7a201a71b832a552bd33839b74047f89bc3f1f00139c6e629`  
		Last Modified: Sat, 12 Nov 2022 10:03:50 GMT  
		Size: 12.0 MB (11996460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2e907876797a7e7631369ff616b83ed0b57d0c152d486322351a767e140814`  
		Last Modified: Sat, 12 Nov 2022 10:03:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0291337573b1029d149b2fca6ebe6b0b3601a0d0f5eaecc06c1e75696f8c6731`  
		Last Modified: Wed, 16 Nov 2022 08:16:48 GMT  
		Size: 3.1 MB (3056225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8f69cf77b68a4b6e967edd1ed5cebd3eda7ce3b4c37d3cc3c6c80941a0509`  
		Last Modified: Fri, 18 Nov 2022 19:09:23 GMT  
		Size: 9.5 MB (9499491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63ac0856d1f8f6029e19cbd1091942b95aa2bf50d51d2e6be43d3fbe7f3bb7d`  
		Last Modified: Fri, 18 Nov 2022 19:09:51 GMT  
		Size: 298.3 MB (298315139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8470d03ed17d2c6c783bb46ad242efce0cc3f549f5b98e001e42fda3b56824b8`  
		Last Modified: Fri, 18 Nov 2022 19:09:21 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598946608775d3c0df6899c4da0bfec0d2ef162decc5c884d73764d4a72f6789`  
		Last Modified: Fri, 18 Nov 2022 19:09:21 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0-alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:2c93dd162547b7b44c8202cf0599e16fb7d2a686c396e6130f122c1b3f61dc4e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46167316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4ccc5a457a36ea94161437a8f9f5053f0e75d381326a3d6a0d8e1e91cc02a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:23:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 08:16:58 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 08:16:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 08:35:03 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 08:35:03 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 08:53:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 08:53:19 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 08:53:19 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 08:53:19 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:18:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:18:37 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:18:42 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:18:42 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:48:20 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:48:20 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:49:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:49:01 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:49:01 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:49:01 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:49:01 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:49:01 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:49:01 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e190eeb0612a6514b857c64886ec8f64d8e235210be5682cf6abbc5bd172b135`  
		Last Modified: Sat, 12 Nov 2022 09:21:43 GMT  
		Size: 663.1 KB (663101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4727b51eed627eface71c55490f3017153992b7d9ae395a99b1e11841128d06`  
		Last Modified: Sat, 12 Nov 2022 09:22:08 GMT  
		Size: 13.1 MB (13073328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce34a3004b391575b577e7922f6d501a0b8ba079dc0741b068b86558c26ee4a1`  
		Last Modified: Sat, 12 Nov 2022 09:22:06 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c270266b6f1942f4120af4ec7278184a61adb708209c33c2320154d82f8a31`  
		Last Modified: Wed, 16 Nov 2022 01:27:26 GMT  
		Size: 3.1 MB (3056436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286cee3bdb5335ff6bca12b16beabdce685e5fdb0a9d0561b1e6cb24ba774152`  
		Last Modified: Fri, 18 Nov 2022 18:49:43 GMT  
		Size: 9.7 MB (9699369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fc21cbba39c03767e72e06461ef113f17eae2671200bbff9598e569d7b5be7`  
		Last Modified: Fri, 18 Nov 2022 18:49:45 GMT  
		Size: 17.0 MB (16955466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5513e43b833e2f30026902bd7a4a1af1addd71ecb1736426f8252fc49d442006`  
		Last Modified: Fri, 18 Nov 2022 18:49:43 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed37a61b2c4a8b46b1ab69bf0c36dcccc4b0e44802a41f019fcb2efd750418a3`  
		Last Modified: Fri, 18 Nov 2022 18:49:42 GMT  
		Size: 2.1 KB (2145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0-alpine` - linux; 386

```console
$ docker pull satosa@sha256:2db0679167412bbbf2ab4702b8580f18935847abe845bb15e8472bda6204190d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328240269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9c562b6c31c0440d0e58b8f9b031c6bcbb90cb33beb9032c8b3544236d5c33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:29:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 05:29:12 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 05:29:14 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 05:50:43 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 05:50:44 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 06:11:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 06:11:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 06:11:39 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 06:11:40 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:38:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:38:28 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:38:35 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:38:36 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:43:42 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:43:43 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:47:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:47:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:47:55 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:47:57 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:47:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:47:58 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:47:59 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:48:00 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a152a67ad9fd5011f8da356e104e14cdbd9cd925941bb6c241b50471eef5a520`  
		Last Modified: Sat, 12 Nov 2022 06:51:44 GMT  
		Size: 669.6 KB (669609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81c595fa967dddaa2db39bd0328b1e7e07583641e9870975cc6d7f37a54f069`  
		Last Modified: Sat, 12 Nov 2022 06:52:19 GMT  
		Size: 13.2 MB (13163166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8750f6265e3be5e75d2d9bb8766f7ae3208bd6ec29a99ab721971a438e8692`  
		Last Modified: Sat, 12 Nov 2022 06:52:17 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c32efb655c88520610dfffc30bc04d2a99130cbac9bd50f8f43c0a37aef6d28`  
		Last Modified: Wed, 16 Nov 2022 01:52:46 GMT  
		Size: 3.1 MB (3054164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e426180bebf4c41e9095922812af13b228b8a1891f925b18c6418706d09d589c`  
		Last Modified: Fri, 18 Nov 2022 18:49:32 GMT  
		Size: 10.0 MB (9981921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35638e3376e5dee654e447a8aded8def08d009dc15a9a6492ea89f0f6cf991d`  
		Last Modified: Fri, 18 Nov 2022 18:49:48 GMT  
		Size: 298.6 MB (298551244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed3a4f7081736c94dcc732f68489dc73f4dbfb0033bb1565e56218bf56e0eba`  
		Last Modified: Fri, 18 Nov 2022 18:49:31 GMT  
		Size: 9.4 KB (9437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84eedc2257c4e9334b63cca383a14503a49dcd221ab8e62a83dd2811a1c87895`  
		Last Modified: Fri, 18 Nov 2022 18:49:31 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0-alpine` - linux; ppc64le

```console
$ docker pull satosa@sha256:78f6a669461f794f0b3dd8e4ed981afb6864275142dd4e3e84b2c9d9e502f748
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328360558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c362cb6cae301a29e6e4675274c3ec62a3fab9aa0ca147eb8167fb57c2d3c92e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 09:09:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 09:09:52 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 09:09:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 09:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 09:49:13 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 10:29:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 10:29:46 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 10:29:47 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 10:29:47 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:28:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:28:15 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:28:26 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:28:27 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:25:31 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:25:31 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:33:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:34:00 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:34:01 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:34:01 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:34:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:34:02 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:34:02 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:34:02 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0578c681eac19aa83cc60a5d383147a7c56a35a3ac13286945daa470f25157e`  
		Last Modified: Sat, 12 Nov 2022 11:31:49 GMT  
		Size: 670.3 KB (670297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bcec55fc14204d6d5b10511d2dcb4b565f19ea0c07a815947bf4616259786f`  
		Last Modified: Sat, 12 Nov 2022 11:32:23 GMT  
		Size: 13.3 MB (13307557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd9e47c00af72c31f09498bcdbb9f23c6b599d96b3262a847fd18af79d8ec83`  
		Last Modified: Sat, 12 Nov 2022 11:32:20 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbba60b66096fca5cbb93d7c032bf2aa7755ea3c73fcddca01bb6d3af1fb0f86`  
		Last Modified: Wed, 16 Nov 2022 07:01:58 GMT  
		Size: 3.1 MB (3056418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59aba7b954790c375454d90d43b7e21ef374bf3fc2cfbca50b660cb08066a22b`  
		Last Modified: Fri, 18 Nov 2022 18:35:37 GMT  
		Size: 10.0 MB (9950742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840cb6e59e4841e4831f3736de75cdf2d9a9d41a587a37d4f6eb185bc212f816`  
		Last Modified: Fri, 18 Nov 2022 18:36:05 GMT  
		Size: 298.6 MB (298562127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605fa8f9b6826c59c0ecc11cc54f8a7a6193c33cee3839935c7409ec2c4bd610`  
		Last Modified: Fri, 18 Nov 2022 18:35:34 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f7512564d5a154d9f72c5ff30f44cfb66410e160250b0ffba25e4abaaaacd1`  
		Last Modified: Fri, 18 Nov 2022 18:35:34 GMT  
		Size: 2.2 KB (2151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.2.0-alpine3.16`

```console
$ docker pull satosa@sha256:96837510b982a984c0f69c23c7424082c1030cd0ca1de70f3a1dda2d5e3a9688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `satosa:8.2.0-alpine3.16` - linux; amd64

```console
$ docker pull satosa@sha256:6e3e4da73ae0c0d1ee3192a90d4e47dd1711df0f3e2d5cda5ec9b5d0146dc48b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c03699dd38f4ddbe3655ace3de96f6a1cef874a71cdabefd8c2f24970096df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:56:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 06:39:07 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 06:39:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 06:57:28 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 06:57:28 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 07:15:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 07:15:59 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 07:15:59 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 07:15:59 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:56:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:56:08 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:56:15 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:56:15 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:22:15 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:22:15 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:22:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:23:00 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:23:00 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:23:00 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:23:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:23:01 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:23:01 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:23:01 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e124a36b9ab9caae9b9b43bffcb6f6d9f126ab89cf2a8b20b9a6f912df03d36`  
		Last Modified: Sat, 12 Nov 2022 07:47:59 GMT  
		Size: 661.8 KB (661831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86456952aa287ca80ac7d7f349dc9edbabda9393ab022d20f2e4c2263cd7d2e7`  
		Last Modified: Sat, 12 Nov 2022 07:48:26 GMT  
		Size: 13.0 MB (12998794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ece9ef7a5797feb2ddaf23aee223848643c0baaedaaa203c721aecb6b272b25`  
		Last Modified: Sat, 12 Nov 2022 07:48:24 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef27b859822294ab1253f8e09a8712d63ea9939eadd1dc4b595d52726c0b020d`  
		Last Modified: Wed, 16 Nov 2022 07:05:43 GMT  
		Size: 3.1 MB (3056443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824935fc626e0971164be442423360798c85d529053e967a909cd1273bda190e`  
		Last Modified: Fri, 18 Nov 2022 18:23:39 GMT  
		Size: 10.9 MB (10872324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fed4aaf1a18111683af619a1e71edd5804307567ed23a83f6f40d15d2794af`  
		Last Modified: Fri, 18 Nov 2022 18:23:41 GMT  
		Size: 17.4 MB (17363712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e090e2c9c7e5d74822d9f71487ec5a71f3058a6f2d8bf756ddaaed8180da06e`  
		Last Modified: Fri, 18 Nov 2022 18:23:38 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41247ef96bde894139c620ba77d7e56bed539612bc8605d4495a7b78bd90ebfb`  
		Last Modified: Fri, 18 Nov 2022 18:23:38 GMT  
		Size: 2.1 KB (2146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0-alpine3.16` - linux; arm variant v6

```console
$ docker pull satosa@sha256:a6fbc6091cf0e1a4e5f6e3d7f2cb1e798e64a2324ff1c80eb9d46b342c11fd39
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327070023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313e9fa4c6d8a5fe836e6b47a9dcef3b27b5b56032c637bb8c15c6c2ecaba99b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:28:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 06:28:49 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 06:28:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 06:55:00 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 06:55:00 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 07:21:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 07:21:39 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 07:21:39 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 07:21:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:41:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:41:32 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:41:39 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:41:39 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:49:39 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:49:39 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:54:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:54:44 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:54:44 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:54:44 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:54:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:54:44 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:54:44 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:54:44 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe974d15ab7b1ace1e4997a68bcfb22f2652af9f902f110d0a90fbdd2ef2053`  
		Last Modified: Sat, 12 Nov 2022 08:03:00 GMT  
		Size: 666.2 KB (666196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69683a8852c8900b94150a78af049bb63d4f73fbdd7239fba1302b9b211ec82`  
		Last Modified: Sat, 12 Nov 2022 08:03:24 GMT  
		Size: 12.5 MB (12545209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63725fb700eaa74dc7942aef8ee5d333eb6b74e224f29ff11f0a997c56208595`  
		Last Modified: Sat, 12 Nov 2022 08:03:22 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012ec3c62fe317e21430242a858a7e489044f55ef1b0398a0c40d9b08e49a357`  
		Last Modified: Wed, 16 Nov 2022 00:46:22 GMT  
		Size: 3.1 MB (3056167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f055f28d65cb7615e57588e003562504a3430b08b6f6e1b13afde191879907f`  
		Last Modified: Fri, 18 Nov 2022 18:55:21 GMT  
		Size: 9.7 MB (9749625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328dee8fb8e4a3a68d2eaea6c4b4eee56bed5bf0e214820a5f81312650be64cf`  
		Last Modified: Fri, 18 Nov 2022 18:55:46 GMT  
		Size: 298.4 MB (298425888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15eaa52f90ffd951ff72991440bbf786b70e29887c6aac6337a8a778504b135e`  
		Last Modified: Fri, 18 Nov 2022 18:55:19 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7997f2f2f20f25fc39c97114744f2d8d8bf61520dcf9641712b83c710b9c87f4`  
		Last Modified: Fri, 18 Nov 2022 18:55:19 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0-alpine3.16` - linux; arm variant v7

```console
$ docker pull satosa@sha256:3bae4cd91de90ed4b33d66d1f77a22cd0b9fcd0ab1b4eaef2cff5417c9275733
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325957233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f631246a1547940b3f84d445fda67d7237809b05753009f90e9037abebd08a84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:12:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 08:12:04 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 08:12:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 08:38:23 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 08:38:23 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 09:08:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 09:08:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 09:08:09 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 09:08:09 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 05:31:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 05:31:37 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 05:31:43 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 05:31:44 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 19:02:52 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 19:02:52 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 19:07:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 19:07:42 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 19:07:42 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 19:07:43 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 19:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 19:07:43 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 19:07:43 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 19:07:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb04c1ebc7f7005f359b85d4698d031de9ca4a4e8bc776ac6faa3f052b3a3f1`  
		Last Modified: Sat, 12 Nov 2022 10:03:05 GMT  
		Size: 659.3 KB (659291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997ef90ff733ebe7a201a71b832a552bd33839b74047f89bc3f1f00139c6e629`  
		Last Modified: Sat, 12 Nov 2022 10:03:50 GMT  
		Size: 12.0 MB (11996460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2e907876797a7e7631369ff616b83ed0b57d0c152d486322351a767e140814`  
		Last Modified: Sat, 12 Nov 2022 10:03:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0291337573b1029d149b2fca6ebe6b0b3601a0d0f5eaecc06c1e75696f8c6731`  
		Last Modified: Wed, 16 Nov 2022 08:16:48 GMT  
		Size: 3.1 MB (3056225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8f69cf77b68a4b6e967edd1ed5cebd3eda7ce3b4c37d3cc3c6c80941a0509`  
		Last Modified: Fri, 18 Nov 2022 19:09:23 GMT  
		Size: 9.5 MB (9499491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63ac0856d1f8f6029e19cbd1091942b95aa2bf50d51d2e6be43d3fbe7f3bb7d`  
		Last Modified: Fri, 18 Nov 2022 19:09:51 GMT  
		Size: 298.3 MB (298315139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8470d03ed17d2c6c783bb46ad242efce0cc3f549f5b98e001e42fda3b56824b8`  
		Last Modified: Fri, 18 Nov 2022 19:09:21 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598946608775d3c0df6899c4da0bfec0d2ef162decc5c884d73764d4a72f6789`  
		Last Modified: Fri, 18 Nov 2022 19:09:21 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:2c93dd162547b7b44c8202cf0599e16fb7d2a686c396e6130f122c1b3f61dc4e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46167316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4ccc5a457a36ea94161437a8f9f5053f0e75d381326a3d6a0d8e1e91cc02a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:23:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 08:16:58 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 08:16:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 08:35:03 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 08:35:03 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 08:53:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 08:53:19 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 08:53:19 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 08:53:19 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:18:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:18:37 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:18:42 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:18:42 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:48:20 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:48:20 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:49:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:49:01 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:49:01 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:49:01 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:49:01 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:49:01 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:49:01 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e190eeb0612a6514b857c64886ec8f64d8e235210be5682cf6abbc5bd172b135`  
		Last Modified: Sat, 12 Nov 2022 09:21:43 GMT  
		Size: 663.1 KB (663101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4727b51eed627eface71c55490f3017153992b7d9ae395a99b1e11841128d06`  
		Last Modified: Sat, 12 Nov 2022 09:22:08 GMT  
		Size: 13.1 MB (13073328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce34a3004b391575b577e7922f6d501a0b8ba079dc0741b068b86558c26ee4a1`  
		Last Modified: Sat, 12 Nov 2022 09:22:06 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c270266b6f1942f4120af4ec7278184a61adb708209c33c2320154d82f8a31`  
		Last Modified: Wed, 16 Nov 2022 01:27:26 GMT  
		Size: 3.1 MB (3056436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286cee3bdb5335ff6bca12b16beabdce685e5fdb0a9d0561b1e6cb24ba774152`  
		Last Modified: Fri, 18 Nov 2022 18:49:43 GMT  
		Size: 9.7 MB (9699369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fc21cbba39c03767e72e06461ef113f17eae2671200bbff9598e569d7b5be7`  
		Last Modified: Fri, 18 Nov 2022 18:49:45 GMT  
		Size: 17.0 MB (16955466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5513e43b833e2f30026902bd7a4a1af1addd71ecb1736426f8252fc49d442006`  
		Last Modified: Fri, 18 Nov 2022 18:49:43 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed37a61b2c4a8b46b1ab69bf0c36dcccc4b0e44802a41f019fcb2efd750418a3`  
		Last Modified: Fri, 18 Nov 2022 18:49:42 GMT  
		Size: 2.1 KB (2145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0-alpine3.16` - linux; 386

```console
$ docker pull satosa@sha256:2db0679167412bbbf2ab4702b8580f18935847abe845bb15e8472bda6204190d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328240269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9c562b6c31c0440d0e58b8f9b031c6bcbb90cb33beb9032c8b3544236d5c33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:29:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 05:29:12 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 05:29:14 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 05:50:43 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 05:50:44 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 06:11:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 06:11:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 06:11:39 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 06:11:40 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:38:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:38:28 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:38:35 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:38:36 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:43:42 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:43:43 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:47:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:47:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:47:55 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:47:57 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:47:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:47:58 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:47:59 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:48:00 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a152a67ad9fd5011f8da356e104e14cdbd9cd925941bb6c241b50471eef5a520`  
		Last Modified: Sat, 12 Nov 2022 06:51:44 GMT  
		Size: 669.6 KB (669609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81c595fa967dddaa2db39bd0328b1e7e07583641e9870975cc6d7f37a54f069`  
		Last Modified: Sat, 12 Nov 2022 06:52:19 GMT  
		Size: 13.2 MB (13163166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8750f6265e3be5e75d2d9bb8766f7ae3208bd6ec29a99ab721971a438e8692`  
		Last Modified: Sat, 12 Nov 2022 06:52:17 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c32efb655c88520610dfffc30bc04d2a99130cbac9bd50f8f43c0a37aef6d28`  
		Last Modified: Wed, 16 Nov 2022 01:52:46 GMT  
		Size: 3.1 MB (3054164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e426180bebf4c41e9095922812af13b228b8a1891f925b18c6418706d09d589c`  
		Last Modified: Fri, 18 Nov 2022 18:49:32 GMT  
		Size: 10.0 MB (9981921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35638e3376e5dee654e447a8aded8def08d009dc15a9a6492ea89f0f6cf991d`  
		Last Modified: Fri, 18 Nov 2022 18:49:48 GMT  
		Size: 298.6 MB (298551244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed3a4f7081736c94dcc732f68489dc73f4dbfb0033bb1565e56218bf56e0eba`  
		Last Modified: Fri, 18 Nov 2022 18:49:31 GMT  
		Size: 9.4 KB (9437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84eedc2257c4e9334b63cca383a14503a49dcd221ab8e62a83dd2811a1c87895`  
		Last Modified: Fri, 18 Nov 2022 18:49:31 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0-alpine3.16` - linux; ppc64le

```console
$ docker pull satosa@sha256:78f6a669461f794f0b3dd8e4ed981afb6864275142dd4e3e84b2c9d9e502f748
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328360558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c362cb6cae301a29e6e4675274c3ec62a3fab9aa0ca147eb8167fb57c2d3c92e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 09:09:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 09:09:52 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 09:09:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 09:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 09:49:13 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 10:29:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 10:29:46 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 10:29:47 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 10:29:47 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:28:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:28:15 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:28:26 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:28:27 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:25:31 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:25:31 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:33:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:34:00 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:34:01 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:34:01 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:34:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:34:02 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:34:02 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:34:02 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0578c681eac19aa83cc60a5d383147a7c56a35a3ac13286945daa470f25157e`  
		Last Modified: Sat, 12 Nov 2022 11:31:49 GMT  
		Size: 670.3 KB (670297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bcec55fc14204d6d5b10511d2dcb4b565f19ea0c07a815947bf4616259786f`  
		Last Modified: Sat, 12 Nov 2022 11:32:23 GMT  
		Size: 13.3 MB (13307557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd9e47c00af72c31f09498bcdbb9f23c6b599d96b3262a847fd18af79d8ec83`  
		Last Modified: Sat, 12 Nov 2022 11:32:20 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbba60b66096fca5cbb93d7c032bf2aa7755ea3c73fcddca01bb6d3af1fb0f86`  
		Last Modified: Wed, 16 Nov 2022 07:01:58 GMT  
		Size: 3.1 MB (3056418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59aba7b954790c375454d90d43b7e21ef374bf3fc2cfbca50b660cb08066a22b`  
		Last Modified: Fri, 18 Nov 2022 18:35:37 GMT  
		Size: 10.0 MB (9950742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840cb6e59e4841e4831f3736de75cdf2d9a9d41a587a37d4f6eb185bc212f816`  
		Last Modified: Fri, 18 Nov 2022 18:36:05 GMT  
		Size: 298.6 MB (298562127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605fa8f9b6826c59c0ecc11cc54f8a7a6193c33cee3839935c7409ec2c4bd610`  
		Last Modified: Fri, 18 Nov 2022 18:35:34 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f7512564d5a154d9f72c5ff30f44cfb66410e160250b0ffba25e4abaaaacd1`  
		Last Modified: Fri, 18 Nov 2022 18:35:34 GMT  
		Size: 2.2 KB (2151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.2.0-bullseye`

```console
$ docker pull satosa@sha256:920b2db648258e4779443b954cbc17015f3e7feda80d41ee006fdf102363bce8
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

### `satosa:8.2.0-bullseye` - linux; amd64

```console
$ docker pull satosa@sha256:2b75f1966b97e958ab7b3edb499a68b28221198f61990a4e20b66bf461a02dfb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87754433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da994718d5841d288b6e518373ab9111b96651fc972c162c8ec1e737bb52fd08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 18:54:42 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 18:54:42 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 18:54:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 20:02:05 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 20:02:05 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 20:16:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 20:16:53 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 20:16:53 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 20:16:53 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:55:31 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:55:32 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:55:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:55:42 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:27:35 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:27:35 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:28:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:28:36 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:28:36 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:28:36 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:28:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:28:36 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:28:36 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:28:36 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00aaacf759c581712fa578a6b4e8e0b9fc780919a5d835a168457b754755644`  
		Last Modified: Tue, 15 Nov 2022 22:58:09 GMT  
		Size: 1.1 MB (1077982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b9691827181afb85e2027be1b34b948a9de4110f0253de4e0c9dfcf1559f7b`  
		Last Modified: Tue, 15 Nov 2022 22:59:24 GMT  
		Size: 12.6 MB (12586017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf69ec4fb1d1d974ad18c827b094bb4a4242791b94344e6f059ed9d0b8eb62be`  
		Last Modified: Tue, 15 Nov 2022 22:59:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7bf64971b8ca870b8bc8476ffc783c777f6bb3bb53e50d8e719f1ea1bad697`  
		Last Modified: Wed, 16 Nov 2022 07:04:31 GMT  
		Size: 3.3 MB (3348953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c001071f815bdbd3fc5e231343c0b4b3337b9d339bd507162ce825aa8eff5643`  
		Last Modified: Mon, 21 Nov 2022 19:29:13 GMT  
		Size: 21.1 MB (21096341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c4d15fc7d1e06ddff844be580c929a202aeef96ed8cb426f2e1f60c6291d80`  
		Last Modified: Mon, 21 Nov 2022 19:29:14 GMT  
		Size: 18.2 MB (18220647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6220bf882cf516ac06374d47fe5f7eb9cb8ac7207c16648c87262453bcb5dd`  
		Last Modified: Mon, 21 Nov 2022 19:29:10 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9610156b7a28fe2c40ba7509e651e32b895a71e7c2999362f9d0dcdefefc7830`  
		Last Modified: Mon, 21 Nov 2022 19:29:10 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0-bullseye` - linux; arm variant v5

```console
$ docker pull satosa@sha256:191432b034c13284a7a750492dc4bbbaab7cbdab72b127ccdc3276685c0a6277
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.3 MB (374337256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddea723e3d8081cb37968943d59ce80b13516d5314627468f2f689ac477edb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:49:18 GMT
ADD file:1949af7e583a1b54055a421129c32315fc101e53e2cda05da3171ed461bde0a6 in / 
# Tue, 15 Nov 2022 01:49:19 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:45:56 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 07:45:56 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 07:46:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 08:28:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 08:28:59 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 08:51:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 08:51:04 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 08:51:04 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 08:51:04 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:33:16 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:33:16 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:33:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:33:32 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:48:45 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:48:45 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:53:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:53:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:53:25 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:53:26 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:53:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:53:26 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:53:26 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:53:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b56836d864a6d857be3d12242b65962f2a2cf0d77c48cfb85bbbdf9d56a7e93d`  
		Last Modified: Tue, 15 Nov 2022 01:54:26 GMT  
		Size: 28.9 MB (28914126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a6e5b3ab314e2965853a4ddc03100cfb0fd0d2825cdc2fb4f1bc363cca39b9`  
		Last Modified: Tue, 15 Nov 2022 10:08:43 GMT  
		Size: 1.1 MB (1060732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db96a74ae1eb60de22f4973a045a1b638a39090565ee2fdf0d4a8c4319bf21c`  
		Last Modified: Tue, 15 Nov 2022 10:09:24 GMT  
		Size: 12.1 MB (12146339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb7e08f0a09cbc7e1269f3c705f9ff28966afe27388fc990a03c00f3200360a`  
		Last Modified: Tue, 15 Nov 2022 10:09:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdc4079d02fdf319fd5aa22d26a4a8b2ec80e3f8beb0ada18ed0aa2ace5e0d7`  
		Last Modified: Wed, 16 Nov 2022 00:39:40 GMT  
		Size: 3.3 MB (3348246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0106290c3f2418d61678711f86fda97637dff84ccfae811034f743dcae2eb8`  
		Last Modified: Mon, 21 Nov 2022 19:54:08 GMT  
		Size: 22.7 MB (22693132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745925b8b4315a2b9b975665bd6158b73df587417a7fade9559f85ddfc27139d`  
		Last Modified: Mon, 21 Nov 2022 19:54:31 GMT  
		Size: 306.2 MB (306162846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c0f3ca52005fb9ed30e05bac90f93fbd6237467e4145b4950ac388200c78fc`  
		Last Modified: Mon, 21 Nov 2022 19:54:04 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15ae5fb82b045c21046c703a63283b8053930321884f0aa7174a12966b6fb46`  
		Last Modified: Mon, 21 Nov 2022 19:54:04 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0-bullseye` - linux; arm variant v7

```console
$ docker pull satosa@sha256:c31d3aa2b933736a4d50e795d7d017bdbe9163970108978759602cc4b09333de
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.1 MB (371088257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d8463fe00f06c45603677eff859db0d7b45fc077a01e06584c25b28d75a300`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 03:43:25 GMT
ADD file:1b5c939bd2a35667d7fc44c3009a56ed92a932f512a73df1617dec6ccbd6e6b1 in / 
# Tue, 15 Nov 2022 03:43:26 GMT
CMD ["bash"]
# Wed, 16 Nov 2022 02:10:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Nov 2022 02:10:52 GMT
ENV LANG=C.UTF-8
# Wed, 16 Nov 2022 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Nov 2022 04:26:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 16 Nov 2022 04:26:07 GMT
ENV PYTHON_VERSION=3.11.0
# Wed, 16 Nov 2022 04:47:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 16 Nov 2022 04:47:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_PIP_VERSION=22.3
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 04:47:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 04:47:40 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:58:12 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:58:13 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 20:02:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 20:02:37 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 20:02:37 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 20:02:38 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 20:02:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 20:02:38 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 20:02:38 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 20:02:38 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:fd18d0201d0ce0c5e103902d894f5d601fc5dde76688aa7dae786840141d23e4`  
		Last Modified: Tue, 15 Nov 2022 03:50:11 GMT  
		Size: 26.6 MB (26576195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f4e2c2480160d1670c2ebb7d1c8290f0a3956265f0069d1de3e5b60d587141`  
		Last Modified: Wed, 16 Nov 2022 08:13:53 GMT  
		Size: 1.0 MB (1042833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9254168af81f2bf98cb621d697e2b624446620a5acce3412a20ed6f6912fd248`  
		Last Modified: Wed, 16 Nov 2022 08:15:35 GMT  
		Size: 11.6 MB (11642276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a40d929533b6fb9173ac38ebf09de1f187f9aa8c6b49de778a38b52abbda11`  
		Last Modified: Wed, 16 Nov 2022 08:15:33 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b04522957691b19b0ac6940e157f56337b27084782602ad4d8a7229397944e1`  
		Last Modified: Wed, 16 Nov 2022 08:15:34 GMT  
		Size: 3.3 MB (3348201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978ebe46f9e524ab17da6008d165ad70ca5187930fb4cd7fc6cd17cccbe7002e`  
		Last Modified: Mon, 21 Nov 2022 20:03:41 GMT  
		Size: 22.4 MB (22430741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa27795d0d8f0524db63e5fbf00dcc9ac44cfeb68c3a66350870d3c3e903fe9`  
		Last Modified: Mon, 21 Nov 2022 20:04:05 GMT  
		Size: 306.0 MB (306036175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5483a349efd69231e68a3b2f9212afd52f92c5498da8c707b5a60f90db6399a`  
		Last Modified: Mon, 21 Nov 2022 20:03:37 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa6d2f8593d4d5bca10332fd90d782e457560c6a50b6fd53614a5eb88d04109`  
		Last Modified: Mon, 21 Nov 2022 20:03:37 GMT  
		Size: 2.1 KB (2144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:a654eeeefb6f573740cf6dc83bc68eb3ff1ad0e4ab660417964ee9664772c6a9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85480362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa7f1d11b3d6d0006e3d3dce2de48cfc52f63ddd139cfddfd1a79675972969b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:41:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 07:41:31 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 07:41:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 08:34:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 08:34:07 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 08:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 08:47:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 08:47:37 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 08:47:37 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:17:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:17:57 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:18:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:18:07 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:49:25 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:49:25 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:50:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:50:21 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:50:21 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:50:21 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:50:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:50:21 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:50:21 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:50:21 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbd8719487c40bfcc7d42d53f202d1dbbbb7ac0fb4e4919ed791664b7f4e47b`  
		Last Modified: Tue, 15 Nov 2022 10:55:04 GMT  
		Size: 1.1 MB (1065870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb07c67a71797e21118367f8ed3ec8f9561b4e4e3f662aed2467c97a93a6dc3f`  
		Last Modified: Tue, 15 Nov 2022 10:56:03 GMT  
		Size: 12.6 MB (12637055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130567c01926a008d097f8a10e6c4348f8cf6f6bae2df7860e1ebad57caf457d`  
		Last Modified: Tue, 15 Nov 2022 10:56:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad488014eea42b129f9a60d9258bfd09ddf59c75a5ccdc55e196cc0eef88cfe`  
		Last Modified: Wed, 16 Nov 2022 01:26:28 GMT  
		Size: 3.3 MB (3348606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cc72b0c430a3bd0d92649200cd8c6da867ea3a7f33b5066d9b8bae085c587c`  
		Last Modified: Mon, 21 Nov 2022 19:50:50 GMT  
		Size: 21.0 MB (20975486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c84b4c195beedd08e708b18de7f11a9e87d3ac3ef1bed9904140963320cb472`  
		Last Modified: Mon, 21 Nov 2022 19:50:50 GMT  
		Size: 17.4 MB (17380880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15489ffd1801184e8a797e1467fb0a83eec71433d9efe85b7fcc060f9c77547`  
		Last Modified: Mon, 21 Nov 2022 19:50:47 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6345651cb201b249a31896d42f4f630bd5f4ee5dc259842a415b1e1d21bc36ab`  
		Last Modified: Mon, 21 Nov 2022 19:50:47 GMT  
		Size: 2.1 KB (2141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0-bullseye` - linux; 386

```console
$ docker pull satosa@sha256:34866c133ed80b3650fcac32e7f67597fa1598e16fc84e51e0e8ee340d0e6ca9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 MB (380177011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25aed64d35227d6dd9deb0905d3a0f76dc6e28a9ce7465ec44f6985baf78563`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:27 GMT
ADD file:608bec4ba3e2543714da4c5158f3c46a168f63ee69ac3f48bff54474ba9a6f27 in / 
# Tue, 15 Nov 2022 01:41:27 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 12:57:10 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 12:57:11 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 12:57:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:13:48 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 14:13:49 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 14:32:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 14:32:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 14:32:38 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 14:32:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:37:29 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:37:29 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:37:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:37:42 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:39:08 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:39:08 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:43:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:43:23 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:43:23 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:43:25 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:43:26 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:43:27 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:43:28 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f6a1e975b34444ecb7c6a2b537403fd6b94d2ff3225944ac2ac3b292466e4078`  
		Last Modified: Tue, 15 Nov 2022 01:47:05 GMT  
		Size: 32.4 MB (32392982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a4ead92cc7eae0396b0fbac1238e0bee3f677740a65a67474e08bcbaa003ba`  
		Last Modified: Tue, 15 Nov 2022 17:38:22 GMT  
		Size: 884.5 KB (884461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd0f4ed85c962a057d2c2667c8b4e1a210aea5e2c9e68520214eb87926f684e`  
		Last Modified: Tue, 15 Nov 2022 19:31:55 GMT  
		Size: 12.7 MB (12683309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72250ba4c687654d3be8943b7bf9591f4dc5de08989c26f5654409682ffbdbfd`  
		Last Modified: Tue, 15 Nov 2022 19:31:53 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ffce336712f2fe573ad63960925a12291df3e7598c36c326698f1308f9caae`  
		Last Modified: Wed, 16 Nov 2022 01:51:48 GMT  
		Size: 3.1 MB (3132128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab52fcbbc37aab1d08731873c11e68396df78043d92d74c7faa4c5b09467c928`  
		Last Modified: Mon, 21 Nov 2022 19:44:19 GMT  
		Size: 24.1 MB (24065495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc904879f9ede6886b46d646fa18a746d32afacfe68d200cbd6259eb315d64a5`  
		Last Modified: Mon, 21 Nov 2022 19:44:46 GMT  
		Size: 307.0 MB (307006821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debe7b65c57d841640da19f01ceedfd6f2d319eabb09c1027621317ab5e75159`  
		Last Modified: Mon, 21 Nov 2022 19:44:15 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ea23efc09b0e6df59a86e0ce421416ed60dbfd3ee8016fdf2d744574b117cd`  
		Last Modified: Mon, 21 Nov 2022 19:44:15 GMT  
		Size: 2.1 KB (2143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0-bullseye` - linux; ppc64le

```console
$ docker pull satosa@sha256:aa91656e4b6a0f6b51aa29a1219617190b462ee7f8b0f25fddd786c831f542f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.5 MB (382489126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88774150f37054a63d09106df180126b080812678a23cfb365f6c4c5fcd1ec22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 05:18:45 GMT
ADD file:520926164fdc762143905745329e568c67289232bec450e48645d82a4613dccf in / 
# Tue, 15 Nov 2022 05:18:47 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:06:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 13:06:51 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 13:07:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:38:22 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 14:38:22 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 15:25:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 15:25:30 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 15:25:31 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 15:25:31 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:27:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:27:46 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:28:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:28:07 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:17:24 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:17:25 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:24:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:24:32 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:24:32 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:24:33 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:24:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:24:33 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:24:34 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:24:34 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:c57913b7d0318ef1a47f0348ce54d9865316776aa1ffb2c7871b1473b3d29407`  
		Last Modified: Tue, 15 Nov 2022 05:24:22 GMT  
		Size: 35.3 MB (35285140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa173aadf3e5fa326d1f1b9f9263051781dc9833e8b60e5bb5a9a994739e18ee`  
		Last Modified: Tue, 15 Nov 2022 17:58:02 GMT  
		Size: 1.1 MB (1096202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2c11a6d1874c9a04e310b3de6f884a5db20d8b2819f963dfbb87d255d4041d`  
		Last Modified: Tue, 15 Nov 2022 17:58:54 GMT  
		Size: 13.0 MB (12955764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53510645cb4e75dba43f2960e61295b7e4092e32b65c05d78e4a222a1035b0`  
		Last Modified: Tue, 15 Nov 2022 17:58:50 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76a75d59183d172f23c152a8f9b934d52c2bbe4e381b7d98e6254342b65c9ad`  
		Last Modified: Wed, 16 Nov 2022 07:01:30 GMT  
		Size: 3.3 MB (3349130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789086c936cb86df67a1bcdf02c069f46030c960a874385b1c09458ea09c9e28`  
		Last Modified: Mon, 21 Nov 2022 19:25:29 GMT  
		Size: 23.6 MB (23636418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf604bdc50ad0b740586882da17fa028eb433f3e9291ae1752d62a62443a5dbd`  
		Last Modified: Mon, 21 Nov 2022 19:25:54 GMT  
		Size: 306.2 MB (306154608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24af618620347663fdfc4357acbffd238b3cc0a2d84703ef629fe73ef009c9bf`  
		Last Modified: Mon, 21 Nov 2022 19:25:23 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b025a5ca25095fb82fa5f084b355cf1b4387400fe727ec454daad74044e9445`  
		Last Modified: Mon, 21 Nov 2022 19:25:23 GMT  
		Size: 2.1 KB (2143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.2.0-bullseye` - linux; s390x

```console
$ docker pull satosa@sha256:11d52a081306682d815a39f964424df846d178a0cd0e043c4c6392ff3f219e6a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.2 MB (375225534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec1f645b1f322cd61afb287021cc9f964eccaaecf3250c047df64b92f392d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 10:52:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 10:52:16 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 10:52:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 11:31:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 11:31:14 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 11:46:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 11:46:18 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 11:46:19 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 11:46:19 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:47:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:47:51 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:48:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:48:06 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:42:07 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:42:08 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:46:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:46:10 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:46:10 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:46:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:46:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:46:10 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:46:10 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:46:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1487a90d7d45334f92d990a52e5750391ed66b11532972979f0792745cedca`  
		Last Modified: Tue, 15 Nov 2022 13:07:54 GMT  
		Size: 1.1 MB (1077428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81becff7fb0cea099dc76445874abd672598812e9ae8fb990ce90a07971a00c2`  
		Last Modified: Tue, 15 Nov 2022 13:08:34 GMT  
		Size: 12.4 MB (12422163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e82170644b3fad2be2ca3ce0cd517e5487772520f4eccaf5e60ce99b9533cf`  
		Last Modified: Tue, 15 Nov 2022 13:08:32 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8aa6e35e336a7de98329dc7ecba62f34a24d5eacb447feafcaac381b01a578`  
		Last Modified: Wed, 16 Nov 2022 00:58:52 GMT  
		Size: 3.3 MB (3348811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55521d94cc6014114d16684de5cf415a987eb5306bb707b2c9c89612bae7434`  
		Last Modified: Mon, 21 Nov 2022 19:46:42 GMT  
		Size: 21.0 MB (21008499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453920ba520592eb4a4712ce352cacced35e45b4c29dc9ba96af152f4263f10a`  
		Last Modified: Mon, 21 Nov 2022 19:46:54 GMT  
		Size: 307.7 MB (307712990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b654413945b74c59b340cba2b01bbd308650ac51a2cefcaede178af5de4e030`  
		Last Modified: Mon, 21 Nov 2022 19:46:39 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a8d82d6fccb2478507a3f5986cf0cf8538a12e3f01d8780e85ed975218703`  
		Last Modified: Mon, 21 Nov 2022 19:46:40 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:alpine`

```console
$ docker pull satosa@sha256:96837510b982a984c0f69c23c7424082c1030cd0ca1de70f3a1dda2d5e3a9688
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
$ docker pull satosa@sha256:6e3e4da73ae0c0d1ee3192a90d4e47dd1711df0f3e2d5cda5ec9b5d0146dc48b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c03699dd38f4ddbe3655ace3de96f6a1cef874a71cdabefd8c2f24970096df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:56:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 06:39:07 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 06:39:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 06:57:28 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 06:57:28 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 07:15:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 07:15:59 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 07:15:59 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 07:15:59 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:56:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:56:08 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:56:15 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:56:15 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:22:15 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:22:15 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:22:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:23:00 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:23:00 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:23:00 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:23:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:23:01 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:23:01 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:23:01 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e124a36b9ab9caae9b9b43bffcb6f6d9f126ab89cf2a8b20b9a6f912df03d36`  
		Last Modified: Sat, 12 Nov 2022 07:47:59 GMT  
		Size: 661.8 KB (661831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86456952aa287ca80ac7d7f349dc9edbabda9393ab022d20f2e4c2263cd7d2e7`  
		Last Modified: Sat, 12 Nov 2022 07:48:26 GMT  
		Size: 13.0 MB (12998794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ece9ef7a5797feb2ddaf23aee223848643c0baaedaaa203c721aecb6b272b25`  
		Last Modified: Sat, 12 Nov 2022 07:48:24 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef27b859822294ab1253f8e09a8712d63ea9939eadd1dc4b595d52726c0b020d`  
		Last Modified: Wed, 16 Nov 2022 07:05:43 GMT  
		Size: 3.1 MB (3056443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824935fc626e0971164be442423360798c85d529053e967a909cd1273bda190e`  
		Last Modified: Fri, 18 Nov 2022 18:23:39 GMT  
		Size: 10.9 MB (10872324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fed4aaf1a18111683af619a1e71edd5804307567ed23a83f6f40d15d2794af`  
		Last Modified: Fri, 18 Nov 2022 18:23:41 GMT  
		Size: 17.4 MB (17363712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e090e2c9c7e5d74822d9f71487ec5a71f3058a6f2d8bf756ddaaed8180da06e`  
		Last Modified: Fri, 18 Nov 2022 18:23:38 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41247ef96bde894139c620ba77d7e56bed539612bc8605d4495a7b78bd90ebfb`  
		Last Modified: Fri, 18 Nov 2022 18:23:38 GMT  
		Size: 2.1 KB (2146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine` - linux; arm variant v6

```console
$ docker pull satosa@sha256:a6fbc6091cf0e1a4e5f6e3d7f2cb1e798e64a2324ff1c80eb9d46b342c11fd39
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327070023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313e9fa4c6d8a5fe836e6b47a9dcef3b27b5b56032c637bb8c15c6c2ecaba99b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:28:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 06:28:49 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 06:28:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 06:55:00 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 06:55:00 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 07:21:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 07:21:39 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 07:21:39 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 07:21:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:41:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:41:32 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:41:39 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:41:39 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:49:39 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:49:39 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:54:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:54:44 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:54:44 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:54:44 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:54:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:54:44 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:54:44 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:54:44 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe974d15ab7b1ace1e4997a68bcfb22f2652af9f902f110d0a90fbdd2ef2053`  
		Last Modified: Sat, 12 Nov 2022 08:03:00 GMT  
		Size: 666.2 KB (666196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69683a8852c8900b94150a78af049bb63d4f73fbdd7239fba1302b9b211ec82`  
		Last Modified: Sat, 12 Nov 2022 08:03:24 GMT  
		Size: 12.5 MB (12545209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63725fb700eaa74dc7942aef8ee5d333eb6b74e224f29ff11f0a997c56208595`  
		Last Modified: Sat, 12 Nov 2022 08:03:22 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012ec3c62fe317e21430242a858a7e489044f55ef1b0398a0c40d9b08e49a357`  
		Last Modified: Wed, 16 Nov 2022 00:46:22 GMT  
		Size: 3.1 MB (3056167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f055f28d65cb7615e57588e003562504a3430b08b6f6e1b13afde191879907f`  
		Last Modified: Fri, 18 Nov 2022 18:55:21 GMT  
		Size: 9.7 MB (9749625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328dee8fb8e4a3a68d2eaea6c4b4eee56bed5bf0e214820a5f81312650be64cf`  
		Last Modified: Fri, 18 Nov 2022 18:55:46 GMT  
		Size: 298.4 MB (298425888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15eaa52f90ffd951ff72991440bbf786b70e29887c6aac6337a8a778504b135e`  
		Last Modified: Fri, 18 Nov 2022 18:55:19 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7997f2f2f20f25fc39c97114744f2d8d8bf61520dcf9641712b83c710b9c87f4`  
		Last Modified: Fri, 18 Nov 2022 18:55:19 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine` - linux; arm variant v7

```console
$ docker pull satosa@sha256:3bae4cd91de90ed4b33d66d1f77a22cd0b9fcd0ab1b4eaef2cff5417c9275733
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325957233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f631246a1547940b3f84d445fda67d7237809b05753009f90e9037abebd08a84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:12:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 08:12:04 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 08:12:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 08:38:23 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 08:38:23 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 09:08:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 09:08:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 09:08:09 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 09:08:09 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 05:31:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 05:31:37 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 05:31:43 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 05:31:44 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 19:02:52 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 19:02:52 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 19:07:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 19:07:42 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 19:07:42 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 19:07:43 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 19:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 19:07:43 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 19:07:43 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 19:07:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb04c1ebc7f7005f359b85d4698d031de9ca4a4e8bc776ac6faa3f052b3a3f1`  
		Last Modified: Sat, 12 Nov 2022 10:03:05 GMT  
		Size: 659.3 KB (659291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997ef90ff733ebe7a201a71b832a552bd33839b74047f89bc3f1f00139c6e629`  
		Last Modified: Sat, 12 Nov 2022 10:03:50 GMT  
		Size: 12.0 MB (11996460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2e907876797a7e7631369ff616b83ed0b57d0c152d486322351a767e140814`  
		Last Modified: Sat, 12 Nov 2022 10:03:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0291337573b1029d149b2fca6ebe6b0b3601a0d0f5eaecc06c1e75696f8c6731`  
		Last Modified: Wed, 16 Nov 2022 08:16:48 GMT  
		Size: 3.1 MB (3056225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8f69cf77b68a4b6e967edd1ed5cebd3eda7ce3b4c37d3cc3c6c80941a0509`  
		Last Modified: Fri, 18 Nov 2022 19:09:23 GMT  
		Size: 9.5 MB (9499491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63ac0856d1f8f6029e19cbd1091942b95aa2bf50d51d2e6be43d3fbe7f3bb7d`  
		Last Modified: Fri, 18 Nov 2022 19:09:51 GMT  
		Size: 298.3 MB (298315139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8470d03ed17d2c6c783bb46ad242efce0cc3f549f5b98e001e42fda3b56824b8`  
		Last Modified: Fri, 18 Nov 2022 19:09:21 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598946608775d3c0df6899c4da0bfec0d2ef162decc5c884d73764d4a72f6789`  
		Last Modified: Fri, 18 Nov 2022 19:09:21 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:2c93dd162547b7b44c8202cf0599e16fb7d2a686c396e6130f122c1b3f61dc4e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46167316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4ccc5a457a36ea94161437a8f9f5053f0e75d381326a3d6a0d8e1e91cc02a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:23:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 08:16:58 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 08:16:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 08:35:03 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 08:35:03 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 08:53:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 08:53:19 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 08:53:19 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 08:53:19 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:18:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:18:37 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:18:42 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:18:42 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:48:20 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:48:20 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:49:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:49:01 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:49:01 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:49:01 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:49:01 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:49:01 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:49:01 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e190eeb0612a6514b857c64886ec8f64d8e235210be5682cf6abbc5bd172b135`  
		Last Modified: Sat, 12 Nov 2022 09:21:43 GMT  
		Size: 663.1 KB (663101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4727b51eed627eface71c55490f3017153992b7d9ae395a99b1e11841128d06`  
		Last Modified: Sat, 12 Nov 2022 09:22:08 GMT  
		Size: 13.1 MB (13073328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce34a3004b391575b577e7922f6d501a0b8ba079dc0741b068b86558c26ee4a1`  
		Last Modified: Sat, 12 Nov 2022 09:22:06 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c270266b6f1942f4120af4ec7278184a61adb708209c33c2320154d82f8a31`  
		Last Modified: Wed, 16 Nov 2022 01:27:26 GMT  
		Size: 3.1 MB (3056436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286cee3bdb5335ff6bca12b16beabdce685e5fdb0a9d0561b1e6cb24ba774152`  
		Last Modified: Fri, 18 Nov 2022 18:49:43 GMT  
		Size: 9.7 MB (9699369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fc21cbba39c03767e72e06461ef113f17eae2671200bbff9598e569d7b5be7`  
		Last Modified: Fri, 18 Nov 2022 18:49:45 GMT  
		Size: 17.0 MB (16955466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5513e43b833e2f30026902bd7a4a1af1addd71ecb1736426f8252fc49d442006`  
		Last Modified: Fri, 18 Nov 2022 18:49:43 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed37a61b2c4a8b46b1ab69bf0c36dcccc4b0e44802a41f019fcb2efd750418a3`  
		Last Modified: Fri, 18 Nov 2022 18:49:42 GMT  
		Size: 2.1 KB (2145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine` - linux; 386

```console
$ docker pull satosa@sha256:2db0679167412bbbf2ab4702b8580f18935847abe845bb15e8472bda6204190d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328240269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9c562b6c31c0440d0e58b8f9b031c6bcbb90cb33beb9032c8b3544236d5c33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:29:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 05:29:12 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 05:29:14 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 05:50:43 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 05:50:44 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 06:11:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 06:11:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 06:11:39 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 06:11:40 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:38:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:38:28 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:38:35 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:38:36 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:43:42 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:43:43 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:47:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:47:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:47:55 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:47:57 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:47:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:47:58 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:47:59 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:48:00 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a152a67ad9fd5011f8da356e104e14cdbd9cd925941bb6c241b50471eef5a520`  
		Last Modified: Sat, 12 Nov 2022 06:51:44 GMT  
		Size: 669.6 KB (669609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81c595fa967dddaa2db39bd0328b1e7e07583641e9870975cc6d7f37a54f069`  
		Last Modified: Sat, 12 Nov 2022 06:52:19 GMT  
		Size: 13.2 MB (13163166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8750f6265e3be5e75d2d9bb8766f7ae3208bd6ec29a99ab721971a438e8692`  
		Last Modified: Sat, 12 Nov 2022 06:52:17 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c32efb655c88520610dfffc30bc04d2a99130cbac9bd50f8f43c0a37aef6d28`  
		Last Modified: Wed, 16 Nov 2022 01:52:46 GMT  
		Size: 3.1 MB (3054164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e426180bebf4c41e9095922812af13b228b8a1891f925b18c6418706d09d589c`  
		Last Modified: Fri, 18 Nov 2022 18:49:32 GMT  
		Size: 10.0 MB (9981921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35638e3376e5dee654e447a8aded8def08d009dc15a9a6492ea89f0f6cf991d`  
		Last Modified: Fri, 18 Nov 2022 18:49:48 GMT  
		Size: 298.6 MB (298551244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed3a4f7081736c94dcc732f68489dc73f4dbfb0033bb1565e56218bf56e0eba`  
		Last Modified: Fri, 18 Nov 2022 18:49:31 GMT  
		Size: 9.4 KB (9437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84eedc2257c4e9334b63cca383a14503a49dcd221ab8e62a83dd2811a1c87895`  
		Last Modified: Fri, 18 Nov 2022 18:49:31 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine` - linux; ppc64le

```console
$ docker pull satosa@sha256:78f6a669461f794f0b3dd8e4ed981afb6864275142dd4e3e84b2c9d9e502f748
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328360558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c362cb6cae301a29e6e4675274c3ec62a3fab9aa0ca147eb8167fb57c2d3c92e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 09:09:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 09:09:52 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 09:09:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 09:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 09:49:13 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 10:29:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 10:29:46 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 10:29:47 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 10:29:47 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:28:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:28:15 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:28:26 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:28:27 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:25:31 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:25:31 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:33:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:34:00 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:34:01 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:34:01 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:34:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:34:02 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:34:02 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:34:02 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0578c681eac19aa83cc60a5d383147a7c56a35a3ac13286945daa470f25157e`  
		Last Modified: Sat, 12 Nov 2022 11:31:49 GMT  
		Size: 670.3 KB (670297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bcec55fc14204d6d5b10511d2dcb4b565f19ea0c07a815947bf4616259786f`  
		Last Modified: Sat, 12 Nov 2022 11:32:23 GMT  
		Size: 13.3 MB (13307557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd9e47c00af72c31f09498bcdbb9f23c6b599d96b3262a847fd18af79d8ec83`  
		Last Modified: Sat, 12 Nov 2022 11:32:20 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbba60b66096fca5cbb93d7c032bf2aa7755ea3c73fcddca01bb6d3af1fb0f86`  
		Last Modified: Wed, 16 Nov 2022 07:01:58 GMT  
		Size: 3.1 MB (3056418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59aba7b954790c375454d90d43b7e21ef374bf3fc2cfbca50b660cb08066a22b`  
		Last Modified: Fri, 18 Nov 2022 18:35:37 GMT  
		Size: 10.0 MB (9950742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840cb6e59e4841e4831f3736de75cdf2d9a9d41a587a37d4f6eb185bc212f816`  
		Last Modified: Fri, 18 Nov 2022 18:36:05 GMT  
		Size: 298.6 MB (298562127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605fa8f9b6826c59c0ecc11cc54f8a7a6193c33cee3839935c7409ec2c4bd610`  
		Last Modified: Fri, 18 Nov 2022 18:35:34 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f7512564d5a154d9f72c5ff30f44cfb66410e160250b0ffba25e4abaaaacd1`  
		Last Modified: Fri, 18 Nov 2022 18:35:34 GMT  
		Size: 2.2 KB (2151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:alpine3.16`

```console
$ docker pull satosa@sha256:96837510b982a984c0f69c23c7424082c1030cd0ca1de70f3a1dda2d5e3a9688
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
$ docker pull satosa@sha256:6e3e4da73ae0c0d1ee3192a90d4e47dd1711df0f3e2d5cda5ec9b5d0146dc48b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c03699dd38f4ddbe3655ace3de96f6a1cef874a71cdabefd8c2f24970096df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:56:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 06:39:07 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 06:39:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 06:57:28 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 06:57:28 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 07:15:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 07:15:59 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 07:15:59 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 07:15:59 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:56:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:56:08 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:56:15 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:56:15 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:22:15 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:22:15 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:22:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:23:00 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:23:00 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:23:00 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:23:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:23:01 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:23:01 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:23:01 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e124a36b9ab9caae9b9b43bffcb6f6d9f126ab89cf2a8b20b9a6f912df03d36`  
		Last Modified: Sat, 12 Nov 2022 07:47:59 GMT  
		Size: 661.8 KB (661831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86456952aa287ca80ac7d7f349dc9edbabda9393ab022d20f2e4c2263cd7d2e7`  
		Last Modified: Sat, 12 Nov 2022 07:48:26 GMT  
		Size: 13.0 MB (12998794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ece9ef7a5797feb2ddaf23aee223848643c0baaedaaa203c721aecb6b272b25`  
		Last Modified: Sat, 12 Nov 2022 07:48:24 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef27b859822294ab1253f8e09a8712d63ea9939eadd1dc4b595d52726c0b020d`  
		Last Modified: Wed, 16 Nov 2022 07:05:43 GMT  
		Size: 3.1 MB (3056443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824935fc626e0971164be442423360798c85d529053e967a909cd1273bda190e`  
		Last Modified: Fri, 18 Nov 2022 18:23:39 GMT  
		Size: 10.9 MB (10872324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fed4aaf1a18111683af619a1e71edd5804307567ed23a83f6f40d15d2794af`  
		Last Modified: Fri, 18 Nov 2022 18:23:41 GMT  
		Size: 17.4 MB (17363712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e090e2c9c7e5d74822d9f71487ec5a71f3058a6f2d8bf756ddaaed8180da06e`  
		Last Modified: Fri, 18 Nov 2022 18:23:38 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41247ef96bde894139c620ba77d7e56bed539612bc8605d4495a7b78bd90ebfb`  
		Last Modified: Fri, 18 Nov 2022 18:23:38 GMT  
		Size: 2.1 KB (2146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine3.16` - linux; arm variant v6

```console
$ docker pull satosa@sha256:a6fbc6091cf0e1a4e5f6e3d7f2cb1e798e64a2324ff1c80eb9d46b342c11fd39
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327070023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313e9fa4c6d8a5fe836e6b47a9dcef3b27b5b56032c637bb8c15c6c2ecaba99b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:28:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 06:28:49 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 06:28:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 06:55:00 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 06:55:00 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 07:21:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 07:21:39 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 07:21:39 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 07:21:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:41:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:41:32 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:41:39 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:41:39 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:49:39 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:49:39 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:54:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:54:44 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:54:44 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:54:44 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:54:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:54:44 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:54:44 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:54:44 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe974d15ab7b1ace1e4997a68bcfb22f2652af9f902f110d0a90fbdd2ef2053`  
		Last Modified: Sat, 12 Nov 2022 08:03:00 GMT  
		Size: 666.2 KB (666196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69683a8852c8900b94150a78af049bb63d4f73fbdd7239fba1302b9b211ec82`  
		Last Modified: Sat, 12 Nov 2022 08:03:24 GMT  
		Size: 12.5 MB (12545209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63725fb700eaa74dc7942aef8ee5d333eb6b74e224f29ff11f0a997c56208595`  
		Last Modified: Sat, 12 Nov 2022 08:03:22 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012ec3c62fe317e21430242a858a7e489044f55ef1b0398a0c40d9b08e49a357`  
		Last Modified: Wed, 16 Nov 2022 00:46:22 GMT  
		Size: 3.1 MB (3056167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f055f28d65cb7615e57588e003562504a3430b08b6f6e1b13afde191879907f`  
		Last Modified: Fri, 18 Nov 2022 18:55:21 GMT  
		Size: 9.7 MB (9749625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328dee8fb8e4a3a68d2eaea6c4b4eee56bed5bf0e214820a5f81312650be64cf`  
		Last Modified: Fri, 18 Nov 2022 18:55:46 GMT  
		Size: 298.4 MB (298425888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15eaa52f90ffd951ff72991440bbf786b70e29887c6aac6337a8a778504b135e`  
		Last Modified: Fri, 18 Nov 2022 18:55:19 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7997f2f2f20f25fc39c97114744f2d8d8bf61520dcf9641712b83c710b9c87f4`  
		Last Modified: Fri, 18 Nov 2022 18:55:19 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine3.16` - linux; arm variant v7

```console
$ docker pull satosa@sha256:3bae4cd91de90ed4b33d66d1f77a22cd0b9fcd0ab1b4eaef2cff5417c9275733
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325957233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f631246a1547940b3f84d445fda67d7237809b05753009f90e9037abebd08a84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:12:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 08:12:04 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 08:12:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 08:38:23 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 08:38:23 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 09:08:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 09:08:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 09:08:09 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 09:08:09 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 05:31:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 05:31:37 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 05:31:43 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 05:31:44 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 19:02:52 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 19:02:52 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 19:07:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 19:07:42 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 19:07:42 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 19:07:43 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 19:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 19:07:43 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 19:07:43 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 19:07:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb04c1ebc7f7005f359b85d4698d031de9ca4a4e8bc776ac6faa3f052b3a3f1`  
		Last Modified: Sat, 12 Nov 2022 10:03:05 GMT  
		Size: 659.3 KB (659291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997ef90ff733ebe7a201a71b832a552bd33839b74047f89bc3f1f00139c6e629`  
		Last Modified: Sat, 12 Nov 2022 10:03:50 GMT  
		Size: 12.0 MB (11996460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2e907876797a7e7631369ff616b83ed0b57d0c152d486322351a767e140814`  
		Last Modified: Sat, 12 Nov 2022 10:03:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0291337573b1029d149b2fca6ebe6b0b3601a0d0f5eaecc06c1e75696f8c6731`  
		Last Modified: Wed, 16 Nov 2022 08:16:48 GMT  
		Size: 3.1 MB (3056225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8f69cf77b68a4b6e967edd1ed5cebd3eda7ce3b4c37d3cc3c6c80941a0509`  
		Last Modified: Fri, 18 Nov 2022 19:09:23 GMT  
		Size: 9.5 MB (9499491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63ac0856d1f8f6029e19cbd1091942b95aa2bf50d51d2e6be43d3fbe7f3bb7d`  
		Last Modified: Fri, 18 Nov 2022 19:09:51 GMT  
		Size: 298.3 MB (298315139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8470d03ed17d2c6c783bb46ad242efce0cc3f549f5b98e001e42fda3b56824b8`  
		Last Modified: Fri, 18 Nov 2022 19:09:21 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598946608775d3c0df6899c4da0bfec0d2ef162decc5c884d73764d4a72f6789`  
		Last Modified: Fri, 18 Nov 2022 19:09:21 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine3.16` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:2c93dd162547b7b44c8202cf0599e16fb7d2a686c396e6130f122c1b3f61dc4e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46167316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4ccc5a457a36ea94161437a8f9f5053f0e75d381326a3d6a0d8e1e91cc02a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:23:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 08:16:58 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 08:16:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 08:35:03 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 08:35:03 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 08:53:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 08:53:19 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 08:53:19 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 08:53:19 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:18:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:18:37 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:18:42 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:18:42 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:48:20 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:48:20 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:49:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:49:01 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:49:01 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:49:01 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:49:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:49:01 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:49:01 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:49:01 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e190eeb0612a6514b857c64886ec8f64d8e235210be5682cf6abbc5bd172b135`  
		Last Modified: Sat, 12 Nov 2022 09:21:43 GMT  
		Size: 663.1 KB (663101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4727b51eed627eface71c55490f3017153992b7d9ae395a99b1e11841128d06`  
		Last Modified: Sat, 12 Nov 2022 09:22:08 GMT  
		Size: 13.1 MB (13073328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce34a3004b391575b577e7922f6d501a0b8ba079dc0741b068b86558c26ee4a1`  
		Last Modified: Sat, 12 Nov 2022 09:22:06 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c270266b6f1942f4120af4ec7278184a61adb708209c33c2320154d82f8a31`  
		Last Modified: Wed, 16 Nov 2022 01:27:26 GMT  
		Size: 3.1 MB (3056436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286cee3bdb5335ff6bca12b16beabdce685e5fdb0a9d0561b1e6cb24ba774152`  
		Last Modified: Fri, 18 Nov 2022 18:49:43 GMT  
		Size: 9.7 MB (9699369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fc21cbba39c03767e72e06461ef113f17eae2671200bbff9598e569d7b5be7`  
		Last Modified: Fri, 18 Nov 2022 18:49:45 GMT  
		Size: 17.0 MB (16955466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5513e43b833e2f30026902bd7a4a1af1addd71ecb1736426f8252fc49d442006`  
		Last Modified: Fri, 18 Nov 2022 18:49:43 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed37a61b2c4a8b46b1ab69bf0c36dcccc4b0e44802a41f019fcb2efd750418a3`  
		Last Modified: Fri, 18 Nov 2022 18:49:42 GMT  
		Size: 2.1 KB (2145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine3.16` - linux; 386

```console
$ docker pull satosa@sha256:2db0679167412bbbf2ab4702b8580f18935847abe845bb15e8472bda6204190d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328240269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9c562b6c31c0440d0e58b8f9b031c6bcbb90cb33beb9032c8b3544236d5c33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:29:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 05:29:12 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 05:29:14 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 05:50:43 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 05:50:44 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 06:11:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 06:11:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 06:11:39 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 06:11:40 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:38:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:38:28 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:38:35 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:38:36 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:43:42 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:43:43 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:47:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:47:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:47:55 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:47:57 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:47:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:47:58 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:47:59 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:48:00 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a152a67ad9fd5011f8da356e104e14cdbd9cd925941bb6c241b50471eef5a520`  
		Last Modified: Sat, 12 Nov 2022 06:51:44 GMT  
		Size: 669.6 KB (669609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81c595fa967dddaa2db39bd0328b1e7e07583641e9870975cc6d7f37a54f069`  
		Last Modified: Sat, 12 Nov 2022 06:52:19 GMT  
		Size: 13.2 MB (13163166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8750f6265e3be5e75d2d9bb8766f7ae3208bd6ec29a99ab721971a438e8692`  
		Last Modified: Sat, 12 Nov 2022 06:52:17 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c32efb655c88520610dfffc30bc04d2a99130cbac9bd50f8f43c0a37aef6d28`  
		Last Modified: Wed, 16 Nov 2022 01:52:46 GMT  
		Size: 3.1 MB (3054164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e426180bebf4c41e9095922812af13b228b8a1891f925b18c6418706d09d589c`  
		Last Modified: Fri, 18 Nov 2022 18:49:32 GMT  
		Size: 10.0 MB (9981921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35638e3376e5dee654e447a8aded8def08d009dc15a9a6492ea89f0f6cf991d`  
		Last Modified: Fri, 18 Nov 2022 18:49:48 GMT  
		Size: 298.6 MB (298551244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed3a4f7081736c94dcc732f68489dc73f4dbfb0033bb1565e56218bf56e0eba`  
		Last Modified: Fri, 18 Nov 2022 18:49:31 GMT  
		Size: 9.4 KB (9437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84eedc2257c4e9334b63cca383a14503a49dcd221ab8e62a83dd2811a1c87895`  
		Last Modified: Fri, 18 Nov 2022 18:49:31 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine3.16` - linux; ppc64le

```console
$ docker pull satosa@sha256:78f6a669461f794f0b3dd8e4ed981afb6864275142dd4e3e84b2c9d9e502f748
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328360558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c362cb6cae301a29e6e4675274c3ec62a3fab9aa0ca147eb8167fb57c2d3c92e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 09:09:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 09:09:52 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 09:09:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 09:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 12 Nov 2022 09:49:13 GMT
ENV PYTHON_VERSION=3.11.0
# Sat, 12 Nov 2022 10:29:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 12 Nov 2022 10:29:46 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 12 Nov 2022 10:29:47 GMT
ENV PYTHON_PIP_VERSION=22.3
# Sat, 12 Nov 2022 10:29:47 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:28:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:28:15 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:28:26 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:28:27 GMT
CMD ["python3"]
# Fri, 18 Nov 2022 18:25:31 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Fri, 18 Nov 2022 18:25:31 GMT
ENV SATOSA_VERSION=8.2.0
# Fri, 18 Nov 2022 18:33:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 18 Nov 2022 18:34:00 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 18 Nov 2022 18:34:01 GMT
WORKDIR /etc/satosa
# Fri, 18 Nov 2022 18:34:01 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 18 Nov 2022 18:34:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Nov 2022 18:34:02 GMT
EXPOSE 8080
# Fri, 18 Nov 2022 18:34:02 GMT
USER satosa:satosa
# Fri, 18 Nov 2022 18:34:02 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0578c681eac19aa83cc60a5d383147a7c56a35a3ac13286945daa470f25157e`  
		Last Modified: Sat, 12 Nov 2022 11:31:49 GMT  
		Size: 670.3 KB (670297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bcec55fc14204d6d5b10511d2dcb4b565f19ea0c07a815947bf4616259786f`  
		Last Modified: Sat, 12 Nov 2022 11:32:23 GMT  
		Size: 13.3 MB (13307557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd9e47c00af72c31f09498bcdbb9f23c6b599d96b3262a847fd18af79d8ec83`  
		Last Modified: Sat, 12 Nov 2022 11:32:20 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbba60b66096fca5cbb93d7c032bf2aa7755ea3c73fcddca01bb6d3af1fb0f86`  
		Last Modified: Wed, 16 Nov 2022 07:01:58 GMT  
		Size: 3.1 MB (3056418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59aba7b954790c375454d90d43b7e21ef374bf3fc2cfbca50b660cb08066a22b`  
		Last Modified: Fri, 18 Nov 2022 18:35:37 GMT  
		Size: 10.0 MB (9950742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840cb6e59e4841e4831f3736de75cdf2d9a9d41a587a37d4f6eb185bc212f816`  
		Last Modified: Fri, 18 Nov 2022 18:36:05 GMT  
		Size: 298.6 MB (298562127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605fa8f9b6826c59c0ecc11cc54f8a7a6193c33cee3839935c7409ec2c4bd610`  
		Last Modified: Fri, 18 Nov 2022 18:35:34 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f7512564d5a154d9f72c5ff30f44cfb66410e160250b0ffba25e4abaaaacd1`  
		Last Modified: Fri, 18 Nov 2022 18:35:34 GMT  
		Size: 2.2 KB (2151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:bullseye`

```console
$ docker pull satosa@sha256:920b2db648258e4779443b954cbc17015f3e7feda80d41ee006fdf102363bce8
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

### `satosa:bullseye` - linux; amd64

```console
$ docker pull satosa@sha256:2b75f1966b97e958ab7b3edb499a68b28221198f61990a4e20b66bf461a02dfb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87754433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da994718d5841d288b6e518373ab9111b96651fc972c162c8ec1e737bb52fd08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 18:54:42 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 18:54:42 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 18:54:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 20:02:05 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 20:02:05 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 20:16:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 20:16:53 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 20:16:53 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 20:16:53 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:55:31 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:55:32 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:55:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:55:42 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:27:35 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:27:35 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:28:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:28:36 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:28:36 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:28:36 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:28:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:28:36 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:28:36 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:28:36 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00aaacf759c581712fa578a6b4e8e0b9fc780919a5d835a168457b754755644`  
		Last Modified: Tue, 15 Nov 2022 22:58:09 GMT  
		Size: 1.1 MB (1077982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b9691827181afb85e2027be1b34b948a9de4110f0253de4e0c9dfcf1559f7b`  
		Last Modified: Tue, 15 Nov 2022 22:59:24 GMT  
		Size: 12.6 MB (12586017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf69ec4fb1d1d974ad18c827b094bb4a4242791b94344e6f059ed9d0b8eb62be`  
		Last Modified: Tue, 15 Nov 2022 22:59:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7bf64971b8ca870b8bc8476ffc783c777f6bb3bb53e50d8e719f1ea1bad697`  
		Last Modified: Wed, 16 Nov 2022 07:04:31 GMT  
		Size: 3.3 MB (3348953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c001071f815bdbd3fc5e231343c0b4b3337b9d339bd507162ce825aa8eff5643`  
		Last Modified: Mon, 21 Nov 2022 19:29:13 GMT  
		Size: 21.1 MB (21096341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c4d15fc7d1e06ddff844be580c929a202aeef96ed8cb426f2e1f60c6291d80`  
		Last Modified: Mon, 21 Nov 2022 19:29:14 GMT  
		Size: 18.2 MB (18220647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6220bf882cf516ac06374d47fe5f7eb9cb8ac7207c16648c87262453bcb5dd`  
		Last Modified: Mon, 21 Nov 2022 19:29:10 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9610156b7a28fe2c40ba7509e651e32b895a71e7c2999362f9d0dcdefefc7830`  
		Last Modified: Mon, 21 Nov 2022 19:29:10 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:bullseye` - linux; arm variant v5

```console
$ docker pull satosa@sha256:191432b034c13284a7a750492dc4bbbaab7cbdab72b127ccdc3276685c0a6277
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.3 MB (374337256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddea723e3d8081cb37968943d59ce80b13516d5314627468f2f689ac477edb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:49:18 GMT
ADD file:1949af7e583a1b54055a421129c32315fc101e53e2cda05da3171ed461bde0a6 in / 
# Tue, 15 Nov 2022 01:49:19 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:45:56 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 07:45:56 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 07:46:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 08:28:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 08:28:59 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 08:51:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 08:51:04 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 08:51:04 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 08:51:04 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:33:16 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:33:16 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:33:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:33:32 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:48:45 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:48:45 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:53:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:53:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:53:25 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:53:26 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:53:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:53:26 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:53:26 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:53:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b56836d864a6d857be3d12242b65962f2a2cf0d77c48cfb85bbbdf9d56a7e93d`  
		Last Modified: Tue, 15 Nov 2022 01:54:26 GMT  
		Size: 28.9 MB (28914126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a6e5b3ab314e2965853a4ddc03100cfb0fd0d2825cdc2fb4f1bc363cca39b9`  
		Last Modified: Tue, 15 Nov 2022 10:08:43 GMT  
		Size: 1.1 MB (1060732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db96a74ae1eb60de22f4973a045a1b638a39090565ee2fdf0d4a8c4319bf21c`  
		Last Modified: Tue, 15 Nov 2022 10:09:24 GMT  
		Size: 12.1 MB (12146339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb7e08f0a09cbc7e1269f3c705f9ff28966afe27388fc990a03c00f3200360a`  
		Last Modified: Tue, 15 Nov 2022 10:09:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdc4079d02fdf319fd5aa22d26a4a8b2ec80e3f8beb0ada18ed0aa2ace5e0d7`  
		Last Modified: Wed, 16 Nov 2022 00:39:40 GMT  
		Size: 3.3 MB (3348246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0106290c3f2418d61678711f86fda97637dff84ccfae811034f743dcae2eb8`  
		Last Modified: Mon, 21 Nov 2022 19:54:08 GMT  
		Size: 22.7 MB (22693132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745925b8b4315a2b9b975665bd6158b73df587417a7fade9559f85ddfc27139d`  
		Last Modified: Mon, 21 Nov 2022 19:54:31 GMT  
		Size: 306.2 MB (306162846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c0f3ca52005fb9ed30e05bac90f93fbd6237467e4145b4950ac388200c78fc`  
		Last Modified: Mon, 21 Nov 2022 19:54:04 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15ae5fb82b045c21046c703a63283b8053930321884f0aa7174a12966b6fb46`  
		Last Modified: Mon, 21 Nov 2022 19:54:04 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:bullseye` - linux; arm variant v7

```console
$ docker pull satosa@sha256:c31d3aa2b933736a4d50e795d7d017bdbe9163970108978759602cc4b09333de
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.1 MB (371088257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d8463fe00f06c45603677eff859db0d7b45fc077a01e06584c25b28d75a300`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 03:43:25 GMT
ADD file:1b5c939bd2a35667d7fc44c3009a56ed92a932f512a73df1617dec6ccbd6e6b1 in / 
# Tue, 15 Nov 2022 03:43:26 GMT
CMD ["bash"]
# Wed, 16 Nov 2022 02:10:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Nov 2022 02:10:52 GMT
ENV LANG=C.UTF-8
# Wed, 16 Nov 2022 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Nov 2022 04:26:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 16 Nov 2022 04:26:07 GMT
ENV PYTHON_VERSION=3.11.0
# Wed, 16 Nov 2022 04:47:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 16 Nov 2022 04:47:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_PIP_VERSION=22.3
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 04:47:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 04:47:40 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:58:12 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:58:13 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 20:02:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 20:02:37 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 20:02:37 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 20:02:38 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 20:02:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 20:02:38 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 20:02:38 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 20:02:38 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:fd18d0201d0ce0c5e103902d894f5d601fc5dde76688aa7dae786840141d23e4`  
		Last Modified: Tue, 15 Nov 2022 03:50:11 GMT  
		Size: 26.6 MB (26576195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f4e2c2480160d1670c2ebb7d1c8290f0a3956265f0069d1de3e5b60d587141`  
		Last Modified: Wed, 16 Nov 2022 08:13:53 GMT  
		Size: 1.0 MB (1042833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9254168af81f2bf98cb621d697e2b624446620a5acce3412a20ed6f6912fd248`  
		Last Modified: Wed, 16 Nov 2022 08:15:35 GMT  
		Size: 11.6 MB (11642276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a40d929533b6fb9173ac38ebf09de1f187f9aa8c6b49de778a38b52abbda11`  
		Last Modified: Wed, 16 Nov 2022 08:15:33 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b04522957691b19b0ac6940e157f56337b27084782602ad4d8a7229397944e1`  
		Last Modified: Wed, 16 Nov 2022 08:15:34 GMT  
		Size: 3.3 MB (3348201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978ebe46f9e524ab17da6008d165ad70ca5187930fb4cd7fc6cd17cccbe7002e`  
		Last Modified: Mon, 21 Nov 2022 20:03:41 GMT  
		Size: 22.4 MB (22430741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa27795d0d8f0524db63e5fbf00dcc9ac44cfeb68c3a66350870d3c3e903fe9`  
		Last Modified: Mon, 21 Nov 2022 20:04:05 GMT  
		Size: 306.0 MB (306036175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5483a349efd69231e68a3b2f9212afd52f92c5498da8c707b5a60f90db6399a`  
		Last Modified: Mon, 21 Nov 2022 20:03:37 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa6d2f8593d4d5bca10332fd90d782e457560c6a50b6fd53614a5eb88d04109`  
		Last Modified: Mon, 21 Nov 2022 20:03:37 GMT  
		Size: 2.1 KB (2144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:bullseye` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:a654eeeefb6f573740cf6dc83bc68eb3ff1ad0e4ab660417964ee9664772c6a9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85480362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa7f1d11b3d6d0006e3d3dce2de48cfc52f63ddd139cfddfd1a79675972969b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:41:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 07:41:31 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 07:41:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 08:34:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 08:34:07 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 08:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 08:47:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 08:47:37 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 08:47:37 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:17:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:17:57 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:18:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:18:07 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:49:25 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:49:25 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:50:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:50:21 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:50:21 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:50:21 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:50:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:50:21 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:50:21 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:50:21 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbd8719487c40bfcc7d42d53f202d1dbbbb7ac0fb4e4919ed791664b7f4e47b`  
		Last Modified: Tue, 15 Nov 2022 10:55:04 GMT  
		Size: 1.1 MB (1065870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb07c67a71797e21118367f8ed3ec8f9561b4e4e3f662aed2467c97a93a6dc3f`  
		Last Modified: Tue, 15 Nov 2022 10:56:03 GMT  
		Size: 12.6 MB (12637055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130567c01926a008d097f8a10e6c4348f8cf6f6bae2df7860e1ebad57caf457d`  
		Last Modified: Tue, 15 Nov 2022 10:56:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad488014eea42b129f9a60d9258bfd09ddf59c75a5ccdc55e196cc0eef88cfe`  
		Last Modified: Wed, 16 Nov 2022 01:26:28 GMT  
		Size: 3.3 MB (3348606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cc72b0c430a3bd0d92649200cd8c6da867ea3a7f33b5066d9b8bae085c587c`  
		Last Modified: Mon, 21 Nov 2022 19:50:50 GMT  
		Size: 21.0 MB (20975486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c84b4c195beedd08e708b18de7f11a9e87d3ac3ef1bed9904140963320cb472`  
		Last Modified: Mon, 21 Nov 2022 19:50:50 GMT  
		Size: 17.4 MB (17380880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15489ffd1801184e8a797e1467fb0a83eec71433d9efe85b7fcc060f9c77547`  
		Last Modified: Mon, 21 Nov 2022 19:50:47 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6345651cb201b249a31896d42f4f630bd5f4ee5dc259842a415b1e1d21bc36ab`  
		Last Modified: Mon, 21 Nov 2022 19:50:47 GMT  
		Size: 2.1 KB (2141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:bullseye` - linux; 386

```console
$ docker pull satosa@sha256:34866c133ed80b3650fcac32e7f67597fa1598e16fc84e51e0e8ee340d0e6ca9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 MB (380177011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25aed64d35227d6dd9deb0905d3a0f76dc6e28a9ce7465ec44f6985baf78563`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:27 GMT
ADD file:608bec4ba3e2543714da4c5158f3c46a168f63ee69ac3f48bff54474ba9a6f27 in / 
# Tue, 15 Nov 2022 01:41:27 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 12:57:10 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 12:57:11 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 12:57:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:13:48 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 14:13:49 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 14:32:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 14:32:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 14:32:38 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 14:32:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:37:29 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:37:29 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:37:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:37:42 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:39:08 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:39:08 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:43:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:43:23 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:43:23 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:43:25 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:43:26 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:43:27 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:43:28 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f6a1e975b34444ecb7c6a2b537403fd6b94d2ff3225944ac2ac3b292466e4078`  
		Last Modified: Tue, 15 Nov 2022 01:47:05 GMT  
		Size: 32.4 MB (32392982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a4ead92cc7eae0396b0fbac1238e0bee3f677740a65a67474e08bcbaa003ba`  
		Last Modified: Tue, 15 Nov 2022 17:38:22 GMT  
		Size: 884.5 KB (884461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd0f4ed85c962a057d2c2667c8b4e1a210aea5e2c9e68520214eb87926f684e`  
		Last Modified: Tue, 15 Nov 2022 19:31:55 GMT  
		Size: 12.7 MB (12683309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72250ba4c687654d3be8943b7bf9591f4dc5de08989c26f5654409682ffbdbfd`  
		Last Modified: Tue, 15 Nov 2022 19:31:53 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ffce336712f2fe573ad63960925a12291df3e7598c36c326698f1308f9caae`  
		Last Modified: Wed, 16 Nov 2022 01:51:48 GMT  
		Size: 3.1 MB (3132128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab52fcbbc37aab1d08731873c11e68396df78043d92d74c7faa4c5b09467c928`  
		Last Modified: Mon, 21 Nov 2022 19:44:19 GMT  
		Size: 24.1 MB (24065495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc904879f9ede6886b46d646fa18a746d32afacfe68d200cbd6259eb315d64a5`  
		Last Modified: Mon, 21 Nov 2022 19:44:46 GMT  
		Size: 307.0 MB (307006821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debe7b65c57d841640da19f01ceedfd6f2d319eabb09c1027621317ab5e75159`  
		Last Modified: Mon, 21 Nov 2022 19:44:15 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ea23efc09b0e6df59a86e0ce421416ed60dbfd3ee8016fdf2d744574b117cd`  
		Last Modified: Mon, 21 Nov 2022 19:44:15 GMT  
		Size: 2.1 KB (2143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:bullseye` - linux; ppc64le

```console
$ docker pull satosa@sha256:aa91656e4b6a0f6b51aa29a1219617190b462ee7f8b0f25fddd786c831f542f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.5 MB (382489126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88774150f37054a63d09106df180126b080812678a23cfb365f6c4c5fcd1ec22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 05:18:45 GMT
ADD file:520926164fdc762143905745329e568c67289232bec450e48645d82a4613dccf in / 
# Tue, 15 Nov 2022 05:18:47 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:06:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 13:06:51 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 13:07:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:38:22 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 14:38:22 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 15:25:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 15:25:30 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 15:25:31 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 15:25:31 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:27:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:27:46 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:28:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:28:07 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:17:24 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:17:25 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:24:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:24:32 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:24:32 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:24:33 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:24:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:24:33 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:24:34 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:24:34 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:c57913b7d0318ef1a47f0348ce54d9865316776aa1ffb2c7871b1473b3d29407`  
		Last Modified: Tue, 15 Nov 2022 05:24:22 GMT  
		Size: 35.3 MB (35285140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa173aadf3e5fa326d1f1b9f9263051781dc9833e8b60e5bb5a9a994739e18ee`  
		Last Modified: Tue, 15 Nov 2022 17:58:02 GMT  
		Size: 1.1 MB (1096202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2c11a6d1874c9a04e310b3de6f884a5db20d8b2819f963dfbb87d255d4041d`  
		Last Modified: Tue, 15 Nov 2022 17:58:54 GMT  
		Size: 13.0 MB (12955764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53510645cb4e75dba43f2960e61295b7e4092e32b65c05d78e4a222a1035b0`  
		Last Modified: Tue, 15 Nov 2022 17:58:50 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76a75d59183d172f23c152a8f9b934d52c2bbe4e381b7d98e6254342b65c9ad`  
		Last Modified: Wed, 16 Nov 2022 07:01:30 GMT  
		Size: 3.3 MB (3349130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789086c936cb86df67a1bcdf02c069f46030c960a874385b1c09458ea09c9e28`  
		Last Modified: Mon, 21 Nov 2022 19:25:29 GMT  
		Size: 23.6 MB (23636418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf604bdc50ad0b740586882da17fa028eb433f3e9291ae1752d62a62443a5dbd`  
		Last Modified: Mon, 21 Nov 2022 19:25:54 GMT  
		Size: 306.2 MB (306154608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24af618620347663fdfc4357acbffd238b3cc0a2d84703ef629fe73ef009c9bf`  
		Last Modified: Mon, 21 Nov 2022 19:25:23 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b025a5ca25095fb82fa5f084b355cf1b4387400fe727ec454daad74044e9445`  
		Last Modified: Mon, 21 Nov 2022 19:25:23 GMT  
		Size: 2.1 KB (2143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:bullseye` - linux; s390x

```console
$ docker pull satosa@sha256:11d52a081306682d815a39f964424df846d178a0cd0e043c4c6392ff3f219e6a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.2 MB (375225534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec1f645b1f322cd61afb287021cc9f964eccaaecf3250c047df64b92f392d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 10:52:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 10:52:16 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 10:52:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 11:31:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 11:31:14 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 11:46:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 11:46:18 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 11:46:19 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 11:46:19 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:47:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:47:51 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:48:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:48:06 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:42:07 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:42:08 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:46:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:46:10 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:46:10 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:46:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:46:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:46:10 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:46:10 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:46:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1487a90d7d45334f92d990a52e5750391ed66b11532972979f0792745cedca`  
		Last Modified: Tue, 15 Nov 2022 13:07:54 GMT  
		Size: 1.1 MB (1077428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81becff7fb0cea099dc76445874abd672598812e9ae8fb990ce90a07971a00c2`  
		Last Modified: Tue, 15 Nov 2022 13:08:34 GMT  
		Size: 12.4 MB (12422163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e82170644b3fad2be2ca3ce0cd517e5487772520f4eccaf5e60ce99b9533cf`  
		Last Modified: Tue, 15 Nov 2022 13:08:32 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8aa6e35e336a7de98329dc7ecba62f34a24d5eacb447feafcaac381b01a578`  
		Last Modified: Wed, 16 Nov 2022 00:58:52 GMT  
		Size: 3.3 MB (3348811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55521d94cc6014114d16684de5cf415a987eb5306bb707b2c9c89612bae7434`  
		Last Modified: Mon, 21 Nov 2022 19:46:42 GMT  
		Size: 21.0 MB (21008499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453920ba520592eb4a4712ce352cacced35e45b4c29dc9ba96af152f4263f10a`  
		Last Modified: Mon, 21 Nov 2022 19:46:54 GMT  
		Size: 307.7 MB (307712990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b654413945b74c59b340cba2b01bbd308650ac51a2cefcaede178af5de4e030`  
		Last Modified: Mon, 21 Nov 2022 19:46:39 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a8d82d6fccb2478507a3f5986cf0cf8538a12e3f01d8780e85ed975218703`  
		Last Modified: Mon, 21 Nov 2022 19:46:40 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:latest`

```console
$ docker pull satosa@sha256:920b2db648258e4779443b954cbc17015f3e7feda80d41ee006fdf102363bce8
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

### `satosa:latest` - linux; amd64

```console
$ docker pull satosa@sha256:2b75f1966b97e958ab7b3edb499a68b28221198f61990a4e20b66bf461a02dfb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87754433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da994718d5841d288b6e518373ab9111b96651fc972c162c8ec1e737bb52fd08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 18:54:42 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 18:54:42 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 18:54:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 20:02:05 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 20:02:05 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 20:16:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 20:16:53 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 20:16:53 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 20:16:53 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:55:31 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:55:32 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:55:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:55:42 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:27:35 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:27:35 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:28:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:28:36 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:28:36 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:28:36 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:28:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:28:36 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:28:36 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:28:36 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00aaacf759c581712fa578a6b4e8e0b9fc780919a5d835a168457b754755644`  
		Last Modified: Tue, 15 Nov 2022 22:58:09 GMT  
		Size: 1.1 MB (1077982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b9691827181afb85e2027be1b34b948a9de4110f0253de4e0c9dfcf1559f7b`  
		Last Modified: Tue, 15 Nov 2022 22:59:24 GMT  
		Size: 12.6 MB (12586017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf69ec4fb1d1d974ad18c827b094bb4a4242791b94344e6f059ed9d0b8eb62be`  
		Last Modified: Tue, 15 Nov 2022 22:59:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7bf64971b8ca870b8bc8476ffc783c777f6bb3bb53e50d8e719f1ea1bad697`  
		Last Modified: Wed, 16 Nov 2022 07:04:31 GMT  
		Size: 3.3 MB (3348953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c001071f815bdbd3fc5e231343c0b4b3337b9d339bd507162ce825aa8eff5643`  
		Last Modified: Mon, 21 Nov 2022 19:29:13 GMT  
		Size: 21.1 MB (21096341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c4d15fc7d1e06ddff844be580c929a202aeef96ed8cb426f2e1f60c6291d80`  
		Last Modified: Mon, 21 Nov 2022 19:29:14 GMT  
		Size: 18.2 MB (18220647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6220bf882cf516ac06374d47fe5f7eb9cb8ac7207c16648c87262453bcb5dd`  
		Last Modified: Mon, 21 Nov 2022 19:29:10 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9610156b7a28fe2c40ba7509e651e32b895a71e7c2999362f9d0dcdefefc7830`  
		Last Modified: Mon, 21 Nov 2022 19:29:10 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:latest` - linux; arm variant v5

```console
$ docker pull satosa@sha256:191432b034c13284a7a750492dc4bbbaab7cbdab72b127ccdc3276685c0a6277
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.3 MB (374337256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddea723e3d8081cb37968943d59ce80b13516d5314627468f2f689ac477edb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:49:18 GMT
ADD file:1949af7e583a1b54055a421129c32315fc101e53e2cda05da3171ed461bde0a6 in / 
# Tue, 15 Nov 2022 01:49:19 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:45:56 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 07:45:56 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 07:46:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 08:28:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 08:28:59 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 08:51:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 08:51:04 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 08:51:04 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 08:51:04 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:33:16 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:33:16 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:33:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:33:32 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:48:45 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:48:45 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:53:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:53:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:53:25 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:53:26 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:53:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:53:26 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:53:26 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:53:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b56836d864a6d857be3d12242b65962f2a2cf0d77c48cfb85bbbdf9d56a7e93d`  
		Last Modified: Tue, 15 Nov 2022 01:54:26 GMT  
		Size: 28.9 MB (28914126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a6e5b3ab314e2965853a4ddc03100cfb0fd0d2825cdc2fb4f1bc363cca39b9`  
		Last Modified: Tue, 15 Nov 2022 10:08:43 GMT  
		Size: 1.1 MB (1060732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db96a74ae1eb60de22f4973a045a1b638a39090565ee2fdf0d4a8c4319bf21c`  
		Last Modified: Tue, 15 Nov 2022 10:09:24 GMT  
		Size: 12.1 MB (12146339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb7e08f0a09cbc7e1269f3c705f9ff28966afe27388fc990a03c00f3200360a`  
		Last Modified: Tue, 15 Nov 2022 10:09:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdc4079d02fdf319fd5aa22d26a4a8b2ec80e3f8beb0ada18ed0aa2ace5e0d7`  
		Last Modified: Wed, 16 Nov 2022 00:39:40 GMT  
		Size: 3.3 MB (3348246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0106290c3f2418d61678711f86fda97637dff84ccfae811034f743dcae2eb8`  
		Last Modified: Mon, 21 Nov 2022 19:54:08 GMT  
		Size: 22.7 MB (22693132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745925b8b4315a2b9b975665bd6158b73df587417a7fade9559f85ddfc27139d`  
		Last Modified: Mon, 21 Nov 2022 19:54:31 GMT  
		Size: 306.2 MB (306162846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c0f3ca52005fb9ed30e05bac90f93fbd6237467e4145b4950ac388200c78fc`  
		Last Modified: Mon, 21 Nov 2022 19:54:04 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15ae5fb82b045c21046c703a63283b8053930321884f0aa7174a12966b6fb46`  
		Last Modified: Mon, 21 Nov 2022 19:54:04 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:latest` - linux; arm variant v7

```console
$ docker pull satosa@sha256:c31d3aa2b933736a4d50e795d7d017bdbe9163970108978759602cc4b09333de
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.1 MB (371088257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d8463fe00f06c45603677eff859db0d7b45fc077a01e06584c25b28d75a300`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 03:43:25 GMT
ADD file:1b5c939bd2a35667d7fc44c3009a56ed92a932f512a73df1617dec6ccbd6e6b1 in / 
# Tue, 15 Nov 2022 03:43:26 GMT
CMD ["bash"]
# Wed, 16 Nov 2022 02:10:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Nov 2022 02:10:52 GMT
ENV LANG=C.UTF-8
# Wed, 16 Nov 2022 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Nov 2022 04:26:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 16 Nov 2022 04:26:07 GMT
ENV PYTHON_VERSION=3.11.0
# Wed, 16 Nov 2022 04:47:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 16 Nov 2022 04:47:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_PIP_VERSION=22.3
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 04:47:27 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 04:47:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 04:47:40 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:58:12 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:58:13 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 20:02:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 20:02:37 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 20:02:37 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 20:02:38 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 20:02:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 20:02:38 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 20:02:38 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 20:02:38 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:fd18d0201d0ce0c5e103902d894f5d601fc5dde76688aa7dae786840141d23e4`  
		Last Modified: Tue, 15 Nov 2022 03:50:11 GMT  
		Size: 26.6 MB (26576195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f4e2c2480160d1670c2ebb7d1c8290f0a3956265f0069d1de3e5b60d587141`  
		Last Modified: Wed, 16 Nov 2022 08:13:53 GMT  
		Size: 1.0 MB (1042833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9254168af81f2bf98cb621d697e2b624446620a5acce3412a20ed6f6912fd248`  
		Last Modified: Wed, 16 Nov 2022 08:15:35 GMT  
		Size: 11.6 MB (11642276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a40d929533b6fb9173ac38ebf09de1f187f9aa8c6b49de778a38b52abbda11`  
		Last Modified: Wed, 16 Nov 2022 08:15:33 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b04522957691b19b0ac6940e157f56337b27084782602ad4d8a7229397944e1`  
		Last Modified: Wed, 16 Nov 2022 08:15:34 GMT  
		Size: 3.3 MB (3348201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978ebe46f9e524ab17da6008d165ad70ca5187930fb4cd7fc6cd17cccbe7002e`  
		Last Modified: Mon, 21 Nov 2022 20:03:41 GMT  
		Size: 22.4 MB (22430741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa27795d0d8f0524db63e5fbf00dcc9ac44cfeb68c3a66350870d3c3e903fe9`  
		Last Modified: Mon, 21 Nov 2022 20:04:05 GMT  
		Size: 306.0 MB (306036175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5483a349efd69231e68a3b2f9212afd52f92c5498da8c707b5a60f90db6399a`  
		Last Modified: Mon, 21 Nov 2022 20:03:37 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa6d2f8593d4d5bca10332fd90d782e457560c6a50b6fd53614a5eb88d04109`  
		Last Modified: Mon, 21 Nov 2022 20:03:37 GMT  
		Size: 2.1 KB (2144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:latest` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:a654eeeefb6f573740cf6dc83bc68eb3ff1ad0e4ab660417964ee9664772c6a9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85480362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa7f1d11b3d6d0006e3d3dce2de48cfc52f63ddd139cfddfd1a79675972969b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:41:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 07:41:31 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 07:41:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 08:34:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 08:34:07 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 08:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 08:47:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 08:47:37 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 08:47:37 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:17:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:17:57 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:18:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:18:07 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:49:25 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:49:25 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:50:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:50:21 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:50:21 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:50:21 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:50:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:50:21 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:50:21 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:50:21 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbd8719487c40bfcc7d42d53f202d1dbbbb7ac0fb4e4919ed791664b7f4e47b`  
		Last Modified: Tue, 15 Nov 2022 10:55:04 GMT  
		Size: 1.1 MB (1065870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb07c67a71797e21118367f8ed3ec8f9561b4e4e3f662aed2467c97a93a6dc3f`  
		Last Modified: Tue, 15 Nov 2022 10:56:03 GMT  
		Size: 12.6 MB (12637055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130567c01926a008d097f8a10e6c4348f8cf6f6bae2df7860e1ebad57caf457d`  
		Last Modified: Tue, 15 Nov 2022 10:56:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad488014eea42b129f9a60d9258bfd09ddf59c75a5ccdc55e196cc0eef88cfe`  
		Last Modified: Wed, 16 Nov 2022 01:26:28 GMT  
		Size: 3.3 MB (3348606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cc72b0c430a3bd0d92649200cd8c6da867ea3a7f33b5066d9b8bae085c587c`  
		Last Modified: Mon, 21 Nov 2022 19:50:50 GMT  
		Size: 21.0 MB (20975486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c84b4c195beedd08e708b18de7f11a9e87d3ac3ef1bed9904140963320cb472`  
		Last Modified: Mon, 21 Nov 2022 19:50:50 GMT  
		Size: 17.4 MB (17380880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15489ffd1801184e8a797e1467fb0a83eec71433d9efe85b7fcc060f9c77547`  
		Last Modified: Mon, 21 Nov 2022 19:50:47 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6345651cb201b249a31896d42f4f630bd5f4ee5dc259842a415b1e1d21bc36ab`  
		Last Modified: Mon, 21 Nov 2022 19:50:47 GMT  
		Size: 2.1 KB (2141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:latest` - linux; 386

```console
$ docker pull satosa@sha256:34866c133ed80b3650fcac32e7f67597fa1598e16fc84e51e0e8ee340d0e6ca9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 MB (380177011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25aed64d35227d6dd9deb0905d3a0f76dc6e28a9ce7465ec44f6985baf78563`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:27 GMT
ADD file:608bec4ba3e2543714da4c5158f3c46a168f63ee69ac3f48bff54474ba9a6f27 in / 
# Tue, 15 Nov 2022 01:41:27 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 12:57:10 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 12:57:11 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 12:57:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:13:48 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 14:13:49 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 14:32:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 14:32:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 14:32:38 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 14:32:39 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 01:37:29 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 01:37:29 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 01:37:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 01:37:42 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:39:08 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:39:08 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:43:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:43:23 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:43:23 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:43:25 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:43:26 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:43:27 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:43:28 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f6a1e975b34444ecb7c6a2b537403fd6b94d2ff3225944ac2ac3b292466e4078`  
		Last Modified: Tue, 15 Nov 2022 01:47:05 GMT  
		Size: 32.4 MB (32392982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a4ead92cc7eae0396b0fbac1238e0bee3f677740a65a67474e08bcbaa003ba`  
		Last Modified: Tue, 15 Nov 2022 17:38:22 GMT  
		Size: 884.5 KB (884461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd0f4ed85c962a057d2c2667c8b4e1a210aea5e2c9e68520214eb87926f684e`  
		Last Modified: Tue, 15 Nov 2022 19:31:55 GMT  
		Size: 12.7 MB (12683309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72250ba4c687654d3be8943b7bf9591f4dc5de08989c26f5654409682ffbdbfd`  
		Last Modified: Tue, 15 Nov 2022 19:31:53 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ffce336712f2fe573ad63960925a12291df3e7598c36c326698f1308f9caae`  
		Last Modified: Wed, 16 Nov 2022 01:51:48 GMT  
		Size: 3.1 MB (3132128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab52fcbbc37aab1d08731873c11e68396df78043d92d74c7faa4c5b09467c928`  
		Last Modified: Mon, 21 Nov 2022 19:44:19 GMT  
		Size: 24.1 MB (24065495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc904879f9ede6886b46d646fa18a746d32afacfe68d200cbd6259eb315d64a5`  
		Last Modified: Mon, 21 Nov 2022 19:44:46 GMT  
		Size: 307.0 MB (307006821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debe7b65c57d841640da19f01ceedfd6f2d319eabb09c1027621317ab5e75159`  
		Last Modified: Mon, 21 Nov 2022 19:44:15 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ea23efc09b0e6df59a86e0ce421416ed60dbfd3ee8016fdf2d744574b117cd`  
		Last Modified: Mon, 21 Nov 2022 19:44:15 GMT  
		Size: 2.1 KB (2143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:latest` - linux; ppc64le

```console
$ docker pull satosa@sha256:aa91656e4b6a0f6b51aa29a1219617190b462ee7f8b0f25fddd786c831f542f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.5 MB (382489126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88774150f37054a63d09106df180126b080812678a23cfb365f6c4c5fcd1ec22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 05:18:45 GMT
ADD file:520926164fdc762143905745329e568c67289232bec450e48645d82a4613dccf in / 
# Tue, 15 Nov 2022 05:18:47 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:06:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 13:06:51 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 13:07:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:38:22 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 14:38:22 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 15:25:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 15:25:30 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 15:25:31 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 15:25:31 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 06:27:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 06:27:46 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 06:28:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 06:28:07 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:17:24 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:17:25 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:24:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:24:32 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:24:32 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:24:33 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:24:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:24:33 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:24:34 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:24:34 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:c57913b7d0318ef1a47f0348ce54d9865316776aa1ffb2c7871b1473b3d29407`  
		Last Modified: Tue, 15 Nov 2022 05:24:22 GMT  
		Size: 35.3 MB (35285140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa173aadf3e5fa326d1f1b9f9263051781dc9833e8b60e5bb5a9a994739e18ee`  
		Last Modified: Tue, 15 Nov 2022 17:58:02 GMT  
		Size: 1.1 MB (1096202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2c11a6d1874c9a04e310b3de6f884a5db20d8b2819f963dfbb87d255d4041d`  
		Last Modified: Tue, 15 Nov 2022 17:58:54 GMT  
		Size: 13.0 MB (12955764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53510645cb4e75dba43f2960e61295b7e4092e32b65c05d78e4a222a1035b0`  
		Last Modified: Tue, 15 Nov 2022 17:58:50 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76a75d59183d172f23c152a8f9b934d52c2bbe4e381b7d98e6254342b65c9ad`  
		Last Modified: Wed, 16 Nov 2022 07:01:30 GMT  
		Size: 3.3 MB (3349130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789086c936cb86df67a1bcdf02c069f46030c960a874385b1c09458ea09c9e28`  
		Last Modified: Mon, 21 Nov 2022 19:25:29 GMT  
		Size: 23.6 MB (23636418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf604bdc50ad0b740586882da17fa028eb433f3e9291ae1752d62a62443a5dbd`  
		Last Modified: Mon, 21 Nov 2022 19:25:54 GMT  
		Size: 306.2 MB (306154608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24af618620347663fdfc4357acbffd238b3cc0a2d84703ef629fe73ef009c9bf`  
		Last Modified: Mon, 21 Nov 2022 19:25:23 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b025a5ca25095fb82fa5f084b355cf1b4387400fe727ec454daad74044e9445`  
		Last Modified: Mon, 21 Nov 2022 19:25:23 GMT  
		Size: 2.1 KB (2143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:latest` - linux; s390x

```console
$ docker pull satosa@sha256:11d52a081306682d815a39f964424df846d178a0cd0e043c4c6392ff3f219e6a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.2 MB (375225534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec1f645b1f322cd61afb287021cc9f964eccaaecf3250c047df64b92f392d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 10:52:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 10:52:16 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 10:52:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 11:31:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 15 Nov 2022 11:31:14 GMT
ENV PYTHON_VERSION=3.11.0
# Tue, 15 Nov 2022 11:46:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 15 Nov 2022 11:46:18 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 15 Nov 2022 11:46:19 GMT
ENV PYTHON_PIP_VERSION=22.3
# Tue, 15 Nov 2022 11:46:19 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.0
# Wed, 16 Nov 2022 00:47:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66030fa03382b4914d4c4d0896961a0bdeeeb274/public/get-pip.py
# Wed, 16 Nov 2022 00:47:51 GMT
ENV PYTHON_GET_PIP_SHA256=1e501cf004eac1b7eb1f97266d28f995ae835d30250bec7f8850562703067dc6
# Wed, 16 Nov 2022 00:48:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 16 Nov 2022 00:48:06 GMT
CMD ["python3"]
# Mon, 21 Nov 2022 19:42:07 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Mon, 21 Nov 2022 19:42:08 GMT
ENV SATOSA_VERSION=8.2.0
# Mon, 21 Nov 2022 19:46:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Mon, 21 Nov 2022 19:46:10 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Mon, 21 Nov 2022 19:46:10 GMT
WORKDIR /etc/satosa
# Mon, 21 Nov 2022 19:46:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Mon, 21 Nov 2022 19:46:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:46:10 GMT
EXPOSE 8080
# Mon, 21 Nov 2022 19:46:10 GMT
USER satosa:satosa
# Mon, 21 Nov 2022 19:46:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1487a90d7d45334f92d990a52e5750391ed66b11532972979f0792745cedca`  
		Last Modified: Tue, 15 Nov 2022 13:07:54 GMT  
		Size: 1.1 MB (1077428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81becff7fb0cea099dc76445874abd672598812e9ae8fb990ce90a07971a00c2`  
		Last Modified: Tue, 15 Nov 2022 13:08:34 GMT  
		Size: 12.4 MB (12422163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e82170644b3fad2be2ca3ce0cd517e5487772520f4eccaf5e60ce99b9533cf`  
		Last Modified: Tue, 15 Nov 2022 13:08:32 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8aa6e35e336a7de98329dc7ecba62f34a24d5eacb447feafcaac381b01a578`  
		Last Modified: Wed, 16 Nov 2022 00:58:52 GMT  
		Size: 3.3 MB (3348811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55521d94cc6014114d16684de5cf415a987eb5306bb707b2c9c89612bae7434`  
		Last Modified: Mon, 21 Nov 2022 19:46:42 GMT  
		Size: 21.0 MB (21008499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453920ba520592eb4a4712ce352cacced35e45b4c29dc9ba96af152f4263f10a`  
		Last Modified: Mon, 21 Nov 2022 19:46:54 GMT  
		Size: 307.7 MB (307712990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b654413945b74c59b340cba2b01bbd308650ac51a2cefcaede178af5de4e030`  
		Last Modified: Mon, 21 Nov 2022 19:46:39 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14a8d82d6fccb2478507a3f5986cf0cf8538a12e3f01d8780e85ed975218703`  
		Last Modified: Mon, 21 Nov 2022 19:46:40 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
