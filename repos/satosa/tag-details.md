<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `satosa`

-	[`satosa:8`](#satosa8)
-	[`satosa:8-alpine`](#satosa8-alpine)
-	[`satosa:8-alpine3.19`](#satosa8-alpine319)
-	[`satosa:8-bookworm`](#satosa8-bookworm)
-	[`satosa:8.4`](#satosa84)
-	[`satosa:8.4-alpine`](#satosa84-alpine)
-	[`satosa:8.4-alpine3.19`](#satosa84-alpine319)
-	[`satosa:8.4-bookworm`](#satosa84-bookworm)
-	[`satosa:8.4.0`](#satosa840)
-	[`satosa:8.4.0-alpine`](#satosa840-alpine)
-	[`satosa:8.4.0-alpine3.19`](#satosa840-alpine319)
-	[`satosa:8.4.0-bookworm`](#satosa840-bookworm)
-	[`satosa:alpine`](#satosaalpine)
-	[`satosa:alpine3.19`](#satosaalpine319)
-	[`satosa:bookworm`](#satosabookworm)
-	[`satosa:latest`](#satosalatest)

## `satosa:8`

```console
$ docker pull satosa@sha256:b6fe267decbd467817f653627989f44ba57a506a148d4b9a69eef4b5b3a223c6
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
$ docker pull satosa@sha256:5c32b82a481315407a8213fe68c5484f56208ce09c049e38d59561c73e150d58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90906882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03bfb47ed64e4c5dc1ea893114954587da90fc25a3247e4612f329469038ef9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
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
# Tue, 13 Feb 2024 15:44:32 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 15:44:32 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 15:45:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 15:45:32 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 15:45:32 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 15:45:32 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 15:45:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 15:45:32 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 15:45:32 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 15:45:32 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d1f07906b71fd60ac43c61035514996a8ad8dbfd39d4f570ac5446b064ee5d`  
		Last Modified: Tue, 13 Feb 2024 11:12:54 GMT  
		Size: 3.5 MB (3507732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3e9a37b01a92d059e8ee8ff525a84400222555e33cae231f8b1d788957450d`  
		Last Modified: Tue, 13 Feb 2024 11:13:47 GMT  
		Size: 12.0 MB (11991512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a33514831e0a3ab693884ed9b534dacd5b2c7110c64692812e78da8471d1f0b`  
		Last Modified: Tue, 13 Feb 2024 11:13:44 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959bfd25ad80f8e7023ffd4f70fd6242ee502c15f6671bd4d299d32efc40470`  
		Last Modified: Tue, 13 Feb 2024 11:13:45 GMT  
		Size: 3.0 MB (2978901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbce98668aa61c3d668392a27d1f07962a0b05246e61e0c6fdd02e9ff3b99cb`  
		Last Modified: Tue, 13 Feb 2024 15:46:04 GMT  
		Size: 22.1 MB (22131281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c2e9f06bef4f772530677cf3122ac0560bcd3f06eef8c1b2f5912840640f37`  
		Last Modified: Tue, 13 Feb 2024 15:46:04 GMT  
		Size: 21.2 MB (21161018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0149f2d2741d11c38936bd8be232ff2e6ff77eae0054a9af5021b6a01b736d0d`  
		Last Modified: Tue, 13 Feb 2024 15:46:01 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be0dac7d9ed7489cc123f4313d801f0b415a9231541a419d86ce216c05dcaa0`  
		Last Modified: Tue, 13 Feb 2024 15:46:01 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8` - linux; arm variant v5

```console
$ docker pull satosa@sha256:1b6c034c92c4410286bbe6984a558abeb749173f63a05c4f726f31f72224deb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.3 MB (355333286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111a7bce7a10a698fe50d3fa635c6b80d60abf733457cb11c02b9247ba917a70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 23 May 2023 00:48:41 GMT
ADD file:868f634f5ddb80ed9e9c719ccaf5d564d96fe819f0b000ecc734311baf5da99b in / 
# Tue, 23 May 2023 00:48:42 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:48:42 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 00:48:42 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 00:48:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 May 2023 00:48:42 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 23 May 2023 00:48:42 GMT
ENV PYTHON_VERSION=3.11.3
# Tue, 23 May 2023 00:48:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 23 May 2023 00:48:42 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 23 May 2023 00:48:42 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Tue, 23 May 2023 00:48:42 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Tue, 23 May 2023 00:48:42 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/0d8570dc44796f4369b652222cf176b3db6ac70e/public/get-pip.py
# Tue, 23 May 2023 00:48:42 GMT
ENV PYTHON_GET_PIP_SHA256=96461deced5c2a487ddc65207ec5a9cffeca0d34e7af7ea1afc470ff0d746207
# Tue, 23 May 2023 00:48:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 23 May 2023 00:48:42 GMT
CMD ["python3"]
# Tue, 23 May 2023 13:53:17 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 23 May 2023 13:53:17 GMT
ENV SATOSA_VERSION=8.2.0
# Tue, 23 May 2023 14:00:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 23 May 2023 14:00:59 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 23 May 2023 14:00:59 GMT
WORKDIR /etc/satosa
# Tue, 23 May 2023 14:00:59 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 23 May 2023 14:00:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 May 2023 14:00:59 GMT
EXPOSE 8080
# Tue, 23 May 2023 14:01:00 GMT
USER satosa:satosa
# Tue, 23 May 2023 14:01:00 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:812967ccba449e7a96044b2d48ffc62816b22eb17641844c4dfffbe3b3ec6f21`  
		Last Modified: Tue, 23 May 2023 00:51:19 GMT  
		Size: 28.9 MB (28903411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51c02b84c5d3000cd5fad1db43e5b181925ce65fcba69e5de80cf6f86dcc9dc`  
		Last Modified: Tue, 23 May 2023 06:21:38 GMT  
		Size: 1.1 MB (1059787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6804baecd87d6bf5a0df8a81f53493f3983ccb3fe4f67085cc33df9ad93e424f`  
		Last Modified: Tue, 23 May 2023 06:22:10 GMT  
		Size: 11.7 MB (11656149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee865db702543611a0073c272d69878c889145e3a15f03abea337bb34ff13383`  
		Last Modified: Tue, 23 May 2023 06:22:08 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3582d7038d35bdd999e817a1a2242591a72dafee3b7f9491739f2eded12caa30`  
		Last Modified: Tue, 23 May 2023 06:22:10 GMT  
		Size: 3.4 MB (3371758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c896d763a3a63cb00ddbd5cdcc2e845cc52b26db83ecc4ee8f885eac815ff406`  
		Last Modified: Tue, 23 May 2023 14:01:23 GMT  
		Size: 22.7 MB (22747859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26bbabdb2586558f07ff698b694f7ff5d2ca90ea1434de90862519d78f38b0af`  
		Last Modified: Tue, 23 May 2023 14:01:43 GMT  
		Size: 287.6 MB (287582449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b525758a86a11078bd078050edb0c80f05479b749dc22dc2c288ddf349ad58d3`  
		Last Modified: Tue, 23 May 2023 14:01:19 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b9451dc6448c57bc30ed2831c6dbcddc60410465c75ab640ed583d0aeab80b`  
		Last Modified: Tue, 23 May 2023 14:01:19 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8` - linux; arm variant v7

```console
$ docker pull satosa@sha256:011efe44839fb660c982fc18393018be58964e5d695df1ab75c2c18622830af3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.1 MB (350118406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9003b3a402e803a529aafaa42d3b2b9e77fab05e81b128ad77a21dae037924a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 23 May 2023 00:57:55 GMT
ADD file:dbb95e676c7a9806b1883ebcf4259345159caf22ff7194ba7556ea0b1f78099a in / 
# Tue, 23 May 2023 00:57:56 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:57:56 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 00:57:56 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 00:57:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 May 2023 00:57:56 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 23 May 2023 00:57:56 GMT
ENV PYTHON_VERSION=3.11.3
# Tue, 23 May 2023 00:57:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 23 May 2023 00:57:56 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 23 May 2023 00:57:56 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Tue, 23 May 2023 00:57:56 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Tue, 23 May 2023 00:57:56 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/0d8570dc44796f4369b652222cf176b3db6ac70e/public/get-pip.py
# Tue, 23 May 2023 00:57:56 GMT
ENV PYTHON_GET_PIP_SHA256=96461deced5c2a487ddc65207ec5a9cffeca0d34e7af7ea1afc470ff0d746207
# Tue, 23 May 2023 00:57:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 23 May 2023 00:57:56 GMT
CMD ["python3"]
# Tue, 23 May 2023 11:03:06 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 23 May 2023 11:03:07 GMT
ENV SATOSA_VERSION=8.2.0
# Tue, 23 May 2023 11:08:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 23 May 2023 11:08:21 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 23 May 2023 11:08:22 GMT
WORKDIR /etc/satosa
# Tue, 23 May 2023 11:08:22 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 23 May 2023 11:08:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 May 2023 11:08:23 GMT
EXPOSE 8080
# Tue, 23 May 2023 11:08:23 GMT
USER satosa:satosa
# Tue, 23 May 2023 11:08:24 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a27027e97f260d9b7aac9bae941b44639374700dc4c32cc2e378b189a4ffda88`  
		Last Modified: Tue, 23 May 2023 01:01:46 GMT  
		Size: 26.6 MB (26564635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c18fa1eb965a9cd27f27d4f8153653a65b50942439f8c148cfebd8d30b2fd92`  
		Last Modified: Tue, 23 May 2023 05:27:31 GMT  
		Size: 1.0 MB (1041758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed9b7ddc0308ec6c21e7ce071d1a78403a2ed9e29eb18d1e50e2b432c26e647`  
		Last Modified: Tue, 23 May 2023 05:27:58 GMT  
		Size: 11.2 MB (11225102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c05d200b8453f1780ddda48b62a663eba129701942d7315f7b8709d060874028`  
		Last Modified: Tue, 23 May 2023 05:27:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c39f7290efdd5e658f9589eeafae04e61c38a52c3660114a9af02ac7864cbf`  
		Last Modified: Tue, 23 May 2023 05:27:57 GMT  
		Size: 3.4 MB (3371808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ebb953d507de429bee981b04539b24423058824bd989d591b33a702f5c947a`  
		Last Modified: Tue, 23 May 2023 11:08:49 GMT  
		Size: 22.5 MB (22475194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884723dd7bbba821cc446c78904a20ef101b33b4d450f5afd8ac5a2d449e0988`  
		Last Modified: Tue, 23 May 2023 11:09:19 GMT  
		Size: 285.4 MB (285428033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed31500b36d9c56263ca900c1d1c50fbed84aa05926e66adccfcf085d0e48a5e`  
		Last Modified: Tue, 23 May 2023 11:08:44 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc69d7a6ff1da49d86ac28b19acd7e90b05476c2cc303f4f08457ab9595a980b`  
		Last Modified: Tue, 23 May 2023 11:08:44 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:3a68256b9eab756090fcfd6e0fb01d31474c035065ef89a46fc20a103cfb03cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89982898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a7461963f9363c0e895bb78ed23316e77c1fccaa66569858c0373a613a3da0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
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
# Tue, 12 Mar 2024 13:00:40 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 12 Mar 2024 13:00:40 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 12 Mar 2024 13:01:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 12 Mar 2024 13:01:39 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 12 Mar 2024 13:01:39 GMT
WORKDIR /etc/satosa
# Tue, 12 Mar 2024 13:01:39 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 12 Mar 2024 13:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 13:01:39 GMT
EXPOSE 8080
# Tue, 12 Mar 2024 13:01:39 GMT
USER satosa:satosa
# Tue, 12 Mar 2024 13:01:39 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55af26b7addf6c0f6fe5fed39393a1379356bb864caac1da91a0fd2fa77b911b`  
		Last Modified: Tue, 12 Mar 2024 09:46:35 GMT  
		Size: 3.3 MB (3323852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3caa3c29ca1489fb5a2119be7e582ca42dece866341d3a379b776c5b2c6362b`  
		Last Modified: Tue, 12 Mar 2024 09:47:24 GMT  
		Size: 12.0 MB (11965714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1240f83dd7d124ccb21f022464852fd5587ac77b5e6be447b86db873dc0bf6d`  
		Last Modified: Tue, 12 Mar 2024 09:47:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6318e81a3dccbefef51184e62057428961a21b0cde407673f088ee0f57417ddc`  
		Last Modified: Tue, 12 Mar 2024 09:47:23 GMT  
		Size: 3.0 MB (2979263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1b6451ffebc99e9f0ea5b7dfcb1ae02b45eca810ebc9bbada3dfc6a5005861`  
		Last Modified: Tue, 12 Mar 2024 13:02:09 GMT  
		Size: 22.0 MB (21976035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ab61321e7317b6e6d2219203156533d48070dc964baf5797c21336fd94c513`  
		Last Modified: Tue, 12 Mar 2024 13:02:09 GMT  
		Size: 20.6 MB (20569252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dab6e27ad8fb7aa4c1c72574a8ed2a1d04a5de529a450fb5605b521fe12ba6`  
		Last Modified: Tue, 12 Mar 2024 13:02:06 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf6d0d867f4ba1d51aaba9bf44b27b3936fbc500d13376e4252cdbb8826648e`  
		Last Modified: Tue, 12 Mar 2024 13:02:06 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8` - linux; 386

```console
$ docker pull satosa@sha256:29df1f337d370235279a903eb80322eb9eec3ac134684f701bd59c93d7281437
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.7 MB (488727279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff9657cc4d63a559b1c55d0d689270b3cab3685c02704b1406c3f8d3bb27d29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:56 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Tue, 13 Feb 2024 00:38:56 GMT
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
# Tue, 13 Feb 2024 17:58:09 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 17:58:09 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 18:09:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 18:09:09 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 18:09:09 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 18:09:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 18:09:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 18:09:10 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 18:09:10 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 18:09:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18cc86e13533dd94d2b3a19bfcb8d1ebde259ebc088243e630bf43438b4bb0`  
		Last Modified: Tue, 13 Feb 2024 14:51:20 GMT  
		Size: 3.5 MB (3503117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48b2b4dedbd677d6449d91281ba20d6fe52233483171d23c4296d9fc6d8cb59`  
		Last Modified: Tue, 13 Feb 2024 14:52:23 GMT  
		Size: 12.2 MB (12239206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a65413fe49c71ab3fa6df4fdf4255039158476191db636768837f1e6e8f735`  
		Last Modified: Tue, 13 Feb 2024 14:52:20 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a42bf4645e12370533b1732e65757f2816f1497d63b7f58b12adb1f283696c3`  
		Last Modified: Tue, 13 Feb 2024 14:52:22 GMT  
		Size: 3.0 MB (2978347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2ac513cfa963fa4f372c2e074be3b84b2c51e0b44bc35cce298f09deba2abe`  
		Last Modified: Tue, 13 Feb 2024 18:22:49 GMT  
		Size: 24.2 MB (24203811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580091280836d4f1a1b351ea86e768f03371c70d1bf055b106d9206deae3f257`  
		Last Modified: Tue, 13 Feb 2024 18:23:18 GMT  
		Size: 415.6 MB (415648638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24b0ff82749ad53a37fb38644218e460b515aa025d63420ebb6c720b02ba1a1`  
		Last Modified: Tue, 13 Feb 2024 18:22:43 GMT  
		Size: 10.0 KB (9963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8ea8a78031214f83625ad937146849d4742abbf5ad497ded7e20c73e51dc3c`  
		Last Modified: Tue, 13 Feb 2024 18:22:43 GMT  
		Size: 2.1 KB (2144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8` - linux; ppc64le

```console
$ docker pull satosa@sha256:3ca21f61a53fe5346c76ed4b9351ce8f001d671762a09a9c1107237d507d7925
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.2 MB (491195693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde9ec216fdcaf6771a71bba1c3a946c1400e738a3a3d304194b057d98b2dd5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:03 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Tue, 13 Feb 2024 00:39:05 GMT
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
# Tue, 13 Feb 2024 08:21:36 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 08:21:37 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 08:29:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 08:29:24 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 08:29:25 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 08:29:25 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 08:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 08:29:26 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 08:29:26 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 08:29:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee78f2de2777d7bd5e7363b69080bb1a6394e1cddd1fc2acaa7f608b1d129d7a`  
		Last Modified: Tue, 13 Feb 2024 03:40:38 GMT  
		Size: 3.7 MB (3704538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8cf259e5ab2eafff3461cd2b4fd546d5d20b75f29b62cd7f1efe2cb09905ff`  
		Last Modified: Tue, 13 Feb 2024 03:41:09 GMT  
		Size: 12.6 MB (12602554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7325c8b16dd117cc14e83e03632bfff7d1ff2dd5c50743012aefa3de8b7b2b15`  
		Last Modified: Tue, 13 Feb 2024 03:41:07 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b53c907fc7631d6fac41077df35d1d3a0ece736979014a24f63fa5ca967935c`  
		Last Modified: Tue, 13 Feb 2024 03:41:08 GMT  
		Size: 3.0 MB (2979477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0549feb427d838b6be46181808df359991252c393af2d1bf946f037982b6450b`  
		Last Modified: Tue, 13 Feb 2024 08:38:33 GMT  
		Size: 24.5 MB (24498861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63086daba02a48c5c956598cef502964ec2b7e522483c7ab0ce6bdec980f1ea2`  
		Last Modified: Tue, 13 Feb 2024 08:38:53 GMT  
		Size: 414.3 MB (414279010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1208cb1697601637c58f6636e02d78eb11f3c9066acc050f74644091e9ca9646`  
		Last Modified: Tue, 13 Feb 2024 08:38:29 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922bf6d55eb5cac0384856e8c65367780d6352aa0675e993301e232564115cd5`  
		Last Modified: Tue, 13 Feb 2024 08:38:29 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8` - linux; s390x

```console
$ docker pull satosa@sha256:39a52857d3d3587a0c290bb162869643e8b9238f59ad917118de3baee91ee50d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.2 MB (498229609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83ea5fd0b8ea8f4fc660c3019bc2988cc4386e050e60fc94ae79e6ea783b2cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 01:02:37 GMT
ADD file:2dc5fd465b3cc728990229e12489d68faf8a93e6f574cacdca11cc9bf31f511d in / 
# Tue, 13 Feb 2024 01:02:39 GMT
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
# Fri, 16 Feb 2024 16:03:41 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Fri, 16 Feb 2024 16:03:42 GMT
ENV SATOSA_VERSION=8.4.0
# Fri, 16 Feb 2024 16:09:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 16 Feb 2024 16:09:18 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 16 Feb 2024 16:09:18 GMT
WORKDIR /etc/satosa
# Fri, 16 Feb 2024 16:09:18 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 16 Feb 2024 16:09:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 16:09:18 GMT
EXPOSE 8080
# Fri, 16 Feb 2024 16:09:18 GMT
USER satosa:satosa
# Fri, 16 Feb 2024 16:09:18 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e55f0b78e9a121a048a72242f0aec2a221466b10bedb873c07b73e4b99f873cb`  
		Last Modified: Tue, 13 Feb 2024 01:30:22 GMT  
		Size: 27.5 MB (27488587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3ec7775a265efbf6c384c5d18340a5650c973a50ca2d0e398efd6f07517659`  
		Last Modified: Tue, 13 Feb 2024 11:03:06 GMT  
		Size: 3.2 MB (3166462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082a41a047ff2d36ba555081aeb9a03139eab7b42242dbe438a27a94c51a2118`  
		Last Modified: Fri, 16 Feb 2024 10:40:39 GMT  
		Size: 11.9 MB (11917778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0926d163b9bf2515318962adbb6c235265efae4c566c49f626ddf024df8a42`  
		Last Modified: Fri, 16 Feb 2024 10:40:37 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf892b126232594fc63d047a9f20f7e6170f1e2a219318db54ab08bd0fc07ed`  
		Last Modified: Fri, 16 Feb 2024 10:40:38 GMT  
		Size: 3.0 MB (2978431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4ef25f44b24d50ed7297148115ca7338cfb361dc21d3f50ff822fbe72640c3`  
		Last Modified: Fri, 16 Feb 2024 16:10:46 GMT  
		Size: 23.8 MB (23798204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183d32aa11aa9166c3b9942b91e0c6928610420fb825c3040b4b013e74e74636`  
		Last Modified: Fri, 16 Feb 2024 16:11:02 GMT  
		Size: 428.9 MB (428867797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4adc9965b1ba16dd34f2892e459b028712639a3e92a446b334f71dd3dc941dd`  
		Last Modified: Fri, 16 Feb 2024 16:10:43 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5072cc9e5ef227421d9831c3f457357ca1ca7e2220f50e68b27aebee0bcf6438`  
		Last Modified: Fri, 16 Feb 2024 16:10:43 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8-alpine`

```console
$ docker pull satosa@sha256:5e04caa7a7fd5dfc0e33118b403522944985089b3dc8d3876ca7ee0bffb32d3b
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
$ docker pull satosa@sha256:b6c892a0480ef2f611608277c260c734ea8857698bd61dd64e57ac191af80a89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47166027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe054bc0129c5e7daaba60958ed19cf96cc8937a1ef76ee8b83ccbd25b90cdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Thu, 08 Feb 2024 00:28:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Thu, 08 Feb 2024 00:28:45 GMT
ENV SATOSA_VERSION=8.4.0
# Thu, 08 Feb 2024 00:29:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 08 Feb 2024 00:29:10 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 08 Feb 2024 00:29:10 GMT
WORKDIR /etc/satosa
# Thu, 08 Feb 2024 00:29:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Thu, 08 Feb 2024 00:29:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 00:29:10 GMT
EXPOSE 8080
# Thu, 08 Feb 2024 00:29:10 GMT
USER satosa:satosa
# Thu, 08 Feb 2024 00:29:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca80dc46cecdd1a97787a1dd6f74263b9d2f7b0dd3e2e15c109f5e34848c932`  
		Last Modified: Sat, 27 Jan 2024 07:51:02 GMT  
		Size: 622.1 KB (622150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9e15b6315c34de5c802bdbd343e3ec69bdc4ab870783fc1b9552daaef25e77`  
		Last Modified: Wed, 07 Feb 2024 23:45:23 GMT  
		Size: 11.8 MB (11767542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fd6f3f484fdfccf33965ca0f8807e5078a619803cf638d82bc4a405e91de04`  
		Last Modified: Wed, 07 Feb 2024 23:45:21 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc96b5c1ba465ba27fb55d4766ade8624de4082ac1530b3293ac735ab3ead50`  
		Last Modified: Wed, 07 Feb 2024 23:45:22 GMT  
		Size: 2.7 MB (2696625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7692e7a182f83cff0c00ace6108c6b19e2059f97d2d3aae2480e8eef815237`  
		Last Modified: Thu, 08 Feb 2024 00:29:42 GMT  
		Size: 7.9 MB (7879777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044eb85425384353220c085b958e1f4064080737c8be49f4fa5d4fb9fc427a4a`  
		Last Modified: Thu, 08 Feb 2024 00:29:44 GMT  
		Size: 20.8 MB (20778854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0c0a4c37ce81a2bad65869c10e4226cf2dd90d5dfccc4e9e9973166e1c790c`  
		Last Modified: Thu, 08 Feb 2024 00:29:41 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ceec51a6010f771ca188eb6a330bc23fd71249d03d2014775390fd899cf8ae`  
		Last Modified: Thu, 08 Feb 2024 00:29:41 GMT  
		Size: 2.1 KB (2147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine` - linux; arm variant v6

```console
$ docker pull satosa@sha256:6eb26239e3f9b4f3d182f3a818f91a427134bee51751e0f46a6d7de705c33a28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262100685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806505b83e27f9e7f96da15ce2aec80efe8e44c3206249270279451344a92dd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:11 GMT
ADD file:c5e68ad58a515830d33f20488adffa6af47be2e332543c747b8931cab7444e59 in / 
# Wed, 29 Mar 2023 18:01:11 GMT
CMD ["/bin/sh"]
# Fri, 28 Apr 2023 22:20:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Apr 2023 22:20:40 GMT
ENV LANG=C.UTF-8
# Fri, 28 Apr 2023 22:20:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 28 Apr 2023 22:20:40 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 28 Apr 2023 22:20:40 GMT
ENV PYTHON_VERSION=3.11.3
# Fri, 28 Apr 2023 22:20:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Fri, 28 Apr 2023 22:20:40 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 28 Apr 2023 22:20:40 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Fri, 28 Apr 2023 22:20:40 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 28 Apr 2023 22:20:40 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/0d8570dc44796f4369b652222cf176b3db6ac70e/public/get-pip.py
# Fri, 28 Apr 2023 22:20:40 GMT
ENV PYTHON_GET_PIP_SHA256=96461deced5c2a487ddc65207ec5a9cffeca0d34e7af7ea1afc470ff0d746207
# Fri, 28 Apr 2023 22:20:40 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 28 Apr 2023 22:20:40 GMT
CMD ["python3"]
# Wed, 03 May 2023 01:44:34 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 May 2023 01:44:34 GMT
ENV SATOSA_VERSION=8.2.0
# Wed, 03 May 2023 01:48:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 May 2023 01:49:00 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 May 2023 01:49:00 GMT
WORKDIR /etc/satosa
# Wed, 03 May 2023 01:49:00 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Wed, 03 May 2023 01:49:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 May 2023 01:49:00 GMT
EXPOSE 8080
# Wed, 03 May 2023 01:49:00 GMT
USER satosa:satosa
# Wed, 03 May 2023 01:49:00 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:c4ddbcc13e08e4ef30f810d8afad41fd6994bd8af7d37746d0ea33d8813968fc`  
		Last Modified: Wed, 29 Mar 2023 18:02:04 GMT  
		Size: 2.6 MB (2616846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385377f5c7fdca5ac838685a95def9e8aa4e3fc5a54fda0bae559ae380f7bfb0`  
		Last Modified: Thu, 06 Apr 2023 00:52:56 GMT  
		Size: 666.1 KB (666102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a062a5dc92b567459a8985a9e708c4bdc4f57c647e619977213dba804c1337`  
		Last Modified: Wed, 03 May 2023 01:19:15 GMT  
		Size: 12.2 MB (12205002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de762052920e8d43b210da3385a6cc976e95f5e5fd3af778181fd8895e3da6f`  
		Last Modified: Wed, 03 May 2023 01:19:12 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddfc182f71d9bff7e6d143bea83e1b862220afbb3047c6db2e86027488ff4f4`  
		Last Modified: Wed, 03 May 2023 01:19:14 GMT  
		Size: 3.1 MB (3080436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cde56b6e08c62bde1a810ff349fd49055f567e82dbe397cf7d0543407a9bc3d`  
		Last Modified: Wed, 03 May 2023 01:49:21 GMT  
		Size: 9.8 MB (9792828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197a17b73bc0684ab6bd86cc5fe3498a1a7a7bd83ba298778a064fe323b9d528`  
		Last Modified: Wed, 03 May 2023 01:49:49 GMT  
		Size: 233.7 MB (233727590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8e3b6b13f0dce1e02f922841fb64cf4f2096f1ccfdd3eab8e3b1efca7b2096`  
		Last Modified: Wed, 03 May 2023 01:49:19 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f38952b8a1e8b828b7d1bf9e2daba56ecb11ebb727d63d0ba14d1893ce7fb1`  
		Last Modified: Wed, 03 May 2023 01:49:19 GMT  
		Size: 2.1 KB (2147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine` - linux; arm variant v7

```console
$ docker pull satosa@sha256:523c142c7c6862e72402d75c6c99136d078f1c3bff0832f307c144a87301c563
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159126183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b6e032712d5981488f40cc76e4bd93d0f28b13a6f6c3d58497260a1e5706a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Mon, 04 Mar 2024 00:18:24 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Mon, 04 Mar 2024 00:18:24 GMT
ENV SATOSA_VERSION=8.4.0
# Fri, 08 Mar 2024 16:42:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 08 Mar 2024 16:42:47 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 08 Mar 2024 16:42:48 GMT
WORKDIR /etc/satosa
# Fri, 08 Mar 2024 16:42:48 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 08 Mar 2024 16:42:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Mar 2024 16:42:49 GMT
EXPOSE 8080
# Fri, 08 Mar 2024 16:42:49 GMT
USER satosa:satosa
# Fri, 08 Mar 2024 16:42:49 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3966cfc81792baee0378a9d2d85424676e1972ac6efaf02823ead42801b9b955`  
		Last Modified: Sat, 27 Jan 2024 09:56:47 GMT  
		Size: 622.3 KB (622347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e682fb52211fcfe80358aff5f595fc49d17d84a426dfe07531a831b75feb09`  
		Last Modified: Wed, 07 Feb 2024 22:05:51 GMT  
		Size: 10.9 MB (10921342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d328ac00f385cdf1e967b3563490ef71319627a85149e04464202d4405186633`  
		Last Modified: Wed, 07 Feb 2024 22:05:49 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20df6294d50f788fb5270d7dd1a4482500cab32031d36d7054b0fe2bb9ad3388`  
		Last Modified: Wed, 07 Feb 2024 22:05:53 GMT  
		Size: 2.7 MB (2696693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993adcda16390f9d0b261707cde6cf96b2fbfaf8bb96fa54b01c4a398144f4d5`  
		Last Modified: Fri, 08 Mar 2024 16:43:14 GMT  
		Size: 9.5 MB (9468950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddad33904f84b8f1d9f9858646ed044016f91c329bf6491ddf905a4c9727f3c4`  
		Last Modified: Fri, 08 Mar 2024 16:43:40 GMT  
		Size: 132.5 MB (132485585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6125db7184428846b311e9359eea466b0f60a621909aef263d67072d417e304d`  
		Last Modified: Fri, 08 Mar 2024 16:43:11 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de92b5342a4b1431267ef2960ed4f572083b7e5e4555b301c6074c0af67e9f50`  
		Last Modified: Fri, 08 Mar 2024 16:43:11 GMT  
		Size: 2.2 KB (2154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:4003a283aad4330aff80c41290a82eb0ebffb57a34566aabee96a29175017c66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48517753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e587120d8e54fb5f41c2efd5cae962e6666bfa7c09b7e9d522f9eef79d331bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Wed, 07 Feb 2024 22:11:05 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 07 Feb 2024 22:11:05 GMT
ENV SATOSA_VERSION=8.4.0
# Wed, 07 Feb 2024 22:11:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 07 Feb 2024 22:11:33 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 07 Feb 2024 22:11:33 GMT
WORKDIR /etc/satosa
# Wed, 07 Feb 2024 22:11:34 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Wed, 07 Feb 2024 22:11:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Feb 2024 22:11:34 GMT
EXPOSE 8080
# Wed, 07 Feb 2024 22:11:34 GMT
USER satosa:satosa
# Wed, 07 Feb 2024 22:11:34 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fa4880b84a89cd734aeddf7f4553ca139e4d53722c41c54d930662c13fec8`  
		Last Modified: Sat, 27 Jan 2024 07:25:43 GMT  
		Size: 625.2 KB (625198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e7e2e0a7f3a4af923909dd104860d8fcd4d1f57bb80634083eeda0ba06e36b`  
		Last Modified: Wed, 07 Feb 2024 21:17:32 GMT  
		Size: 11.8 MB (11832383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99284986c3ffad45eb81cc0742b61e60571970e1c03d9069e0aec554fb1bc089`  
		Last Modified: Wed, 07 Feb 2024 21:17:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be93132253eb292b41ae301f69f0d47c791650c493ecd51e34ed720af01910c9`  
		Last Modified: Wed, 07 Feb 2024 21:17:31 GMT  
		Size: 2.7 MB (2696655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb40e308f00eb72552da1c91817c9bd1ee85c9cc0af8aa6b270e4ba38042daf`  
		Last Modified: Wed, 07 Feb 2024 22:12:05 GMT  
		Size: 9.7 MB (9676585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559bbf4aa424865f8954a90d5005b0a7eeb2e7f6f5cf2a650115800ae44371b`  
		Last Modified: Wed, 07 Feb 2024 22:12:07 GMT  
		Size: 20.3 MB (20326868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04661db7e0029a1b22d9c43b808257e317f876d92528b7e314a89ad81990793c`  
		Last Modified: Wed, 07 Feb 2024 22:12:04 GMT  
		Size: 10.0 KB (9960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6b843d24bf6a06297d5bfbd477d65a9ecd573ada69abf6cc16eacd553e82da`  
		Last Modified: Wed, 07 Feb 2024 22:12:04 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine` - linux; 386

```console
$ docker pull satosa@sha256:391327fc04b4f25ff48fffe263ed5109d6cffec480b1e6ed9c8cd6cf3fd25a08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94656588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aba1b5dff88a26ff7c659482a828d40d8d9adc1ff13480e1cad44266f73cdeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 04:08:00 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_VERSION=3.12.1
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
CMD ["python3"]
# Sat, 27 Jan 2024 08:22:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Sat, 27 Jan 2024 08:22:45 GMT
ENV SATOSA_VERSION=8.4.0
# Sat, 27 Jan 2024 08:30:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Sat, 27 Jan 2024 08:30:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Sat, 27 Jan 2024 08:30:26 GMT
WORKDIR /etc/satosa
# Sat, 27 Jan 2024 08:30:26 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:30:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 08:30:26 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 08:30:26 GMT
USER satosa:satosa
# Sat, 27 Jan 2024 08:30:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7840a0a3a40a6b02ee9c509f8552e6bb70f9a8fb94398de1cfd742dc05d6050`  
		Last Modified: Sat, 27 Jan 2024 04:20:57 GMT  
		Size: 622.8 KB (622802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89a6fae803be2815fb73d36002db0a6aa6c6261cb6d1c568c1e00ae02507350`  
		Last Modified: Sat, 27 Jan 2024 04:21:32 GMT  
		Size: 11.9 MB (11929152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d0d6b56ec289e87c9c0271325d2cae165bad58b6190ea25e22cd8299e0c963`  
		Last Modified: Sat, 27 Jan 2024 04:21:29 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ce0078de875cf898e1a8d7656ea15eb2eace9d4a114c658313f5733402e8ba`  
		Last Modified: Sat, 27 Jan 2024 04:21:30 GMT  
		Size: 2.7 MB (2676259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e3b9a523576b9b8f6a758d4dfcd9a5ab83ba3dc460ef410e4b0be5d7f02c5d`  
		Last Modified: Sat, 27 Jan 2024 08:30:54 GMT  
		Size: 9.6 MB (9619654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc02b6f314d5143b4bc8115b6c540646f5deae4b004b585d1a15342ebf610237`  
		Last Modified: Sat, 27 Jan 2024 08:31:05 GMT  
		Size: 66.6 MB (66552282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47f30cea7d9bc3b8100a695fa9f8a41d253b16b3d39b65ec60470bbbdc52768`  
		Last Modified: Sat, 27 Jan 2024 08:30:51 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49df7ef97d6d92a9d16c8cffdfffe18e75f5e9cd3efe35eccc95aa30bc4f1f7`  
		Last Modified: Sat, 27 Jan 2024 08:30:52 GMT  
		Size: 2.1 KB (2147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine` - linux; ppc64le

```console
$ docker pull satosa@sha256:eefaaf894c37cec9de82537d9844a7c6aec372efe493097fcdd99d78ceaa6bc2
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94283311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bc2d6148135e13cd1b75f30a029b33261fdcb1a5d4a90446d48e5902c57d5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 04:08:00 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_VERSION=3.12.1
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
CMD ["python3"]
# Sat, 27 Jan 2024 08:29:57 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Sat, 27 Jan 2024 08:29:58 GMT
ENV SATOSA_VERSION=8.4.0
# Sat, 27 Jan 2024 08:35:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Sat, 27 Jan 2024 08:35:40 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Sat, 27 Jan 2024 08:35:41 GMT
WORKDIR /etc/satosa
# Sat, 27 Jan 2024 08:35:41 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 08:35:42 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 08:35:43 GMT
USER satosa:satosa
# Sat, 27 Jan 2024 08:35:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d49a9cfe46131ab86b7a184f64865c97ae9d291935002bc7c38567ff27bc73`  
		Last Modified: Sat, 27 Jan 2024 06:51:52 GMT  
		Size: 625.6 KB (625581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e5feee510f8a33a7c371811dafb8bfa0914967fb6c7a516d67434cb1bbd204`  
		Last Modified: Sat, 27 Jan 2024 06:52:28 GMT  
		Size: 12.2 MB (12243607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d0977324b0b3dca506e76d3bde6f9ba583b255bb6941a1be3cbd3a73ff8e6f`  
		Last Modified: Sat, 27 Jan 2024 06:52:26 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63e83db5219c14a37c232e666d4337f900b691fb9e37066556b49fcf6223858`  
		Last Modified: Sat, 27 Jan 2024 06:52:27 GMT  
		Size: 2.7 MB (2676106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d565eb92095419ba03c37c05cab7fa100fb04315710cdd16052fdd4026e1ba`  
		Last Modified: Sat, 27 Jan 2024 08:36:06 GMT  
		Size: 9.8 MB (9801173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03bb04d932f9c6684e334ebedaabaef15c5ca10a2039fc7b092a7c560784931e`  
		Last Modified: Sat, 27 Jan 2024 08:36:14 GMT  
		Size: 65.6 MB (65566138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a082af4585697a65565659cfcf6c0f50d7db1bd8691e3ae138bf5217d4f040`  
		Last Modified: Sat, 27 Jan 2024 08:36:04 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3c70f43dc7ba65b86cf51f7fd90190c017be2d0cc2d247dc00cfb5bee93f19`  
		Last Modified: Sat, 27 Jan 2024 08:36:04 GMT  
		Size: 2.1 KB (2148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8-alpine3.19`

```console
$ docker pull satosa@sha256:d6a2f8debb3cfdc184790fb74026c2cbffd7f402a4a65ecb8e082285143d45a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `satosa:8-alpine3.19` - linux; amd64

```console
$ docker pull satosa@sha256:b6c892a0480ef2f611608277c260c734ea8857698bd61dd64e57ac191af80a89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47166027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe054bc0129c5e7daaba60958ed19cf96cc8937a1ef76ee8b83ccbd25b90cdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Thu, 08 Feb 2024 00:28:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Thu, 08 Feb 2024 00:28:45 GMT
ENV SATOSA_VERSION=8.4.0
# Thu, 08 Feb 2024 00:29:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 08 Feb 2024 00:29:10 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 08 Feb 2024 00:29:10 GMT
WORKDIR /etc/satosa
# Thu, 08 Feb 2024 00:29:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Thu, 08 Feb 2024 00:29:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 00:29:10 GMT
EXPOSE 8080
# Thu, 08 Feb 2024 00:29:10 GMT
USER satosa:satosa
# Thu, 08 Feb 2024 00:29:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca80dc46cecdd1a97787a1dd6f74263b9d2f7b0dd3e2e15c109f5e34848c932`  
		Last Modified: Sat, 27 Jan 2024 07:51:02 GMT  
		Size: 622.1 KB (622150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9e15b6315c34de5c802bdbd343e3ec69bdc4ab870783fc1b9552daaef25e77`  
		Last Modified: Wed, 07 Feb 2024 23:45:23 GMT  
		Size: 11.8 MB (11767542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fd6f3f484fdfccf33965ca0f8807e5078a619803cf638d82bc4a405e91de04`  
		Last Modified: Wed, 07 Feb 2024 23:45:21 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc96b5c1ba465ba27fb55d4766ade8624de4082ac1530b3293ac735ab3ead50`  
		Last Modified: Wed, 07 Feb 2024 23:45:22 GMT  
		Size: 2.7 MB (2696625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7692e7a182f83cff0c00ace6108c6b19e2059f97d2d3aae2480e8eef815237`  
		Last Modified: Thu, 08 Feb 2024 00:29:42 GMT  
		Size: 7.9 MB (7879777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044eb85425384353220c085b958e1f4064080737c8be49f4fa5d4fb9fc427a4a`  
		Last Modified: Thu, 08 Feb 2024 00:29:44 GMT  
		Size: 20.8 MB (20778854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0c0a4c37ce81a2bad65869c10e4226cf2dd90d5dfccc4e9e9973166e1c790c`  
		Last Modified: Thu, 08 Feb 2024 00:29:41 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ceec51a6010f771ca188eb6a330bc23fd71249d03d2014775390fd899cf8ae`  
		Last Modified: Thu, 08 Feb 2024 00:29:41 GMT  
		Size: 2.1 KB (2147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine3.19` - linux; arm variant v7

```console
$ docker pull satosa@sha256:523c142c7c6862e72402d75c6c99136d078f1c3bff0832f307c144a87301c563
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159126183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b6e032712d5981488f40cc76e4bd93d0f28b13a6f6c3d58497260a1e5706a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Mon, 04 Mar 2024 00:18:24 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Mon, 04 Mar 2024 00:18:24 GMT
ENV SATOSA_VERSION=8.4.0
# Fri, 08 Mar 2024 16:42:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 08 Mar 2024 16:42:47 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 08 Mar 2024 16:42:48 GMT
WORKDIR /etc/satosa
# Fri, 08 Mar 2024 16:42:48 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 08 Mar 2024 16:42:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Mar 2024 16:42:49 GMT
EXPOSE 8080
# Fri, 08 Mar 2024 16:42:49 GMT
USER satosa:satosa
# Fri, 08 Mar 2024 16:42:49 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3966cfc81792baee0378a9d2d85424676e1972ac6efaf02823ead42801b9b955`  
		Last Modified: Sat, 27 Jan 2024 09:56:47 GMT  
		Size: 622.3 KB (622347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e682fb52211fcfe80358aff5f595fc49d17d84a426dfe07531a831b75feb09`  
		Last Modified: Wed, 07 Feb 2024 22:05:51 GMT  
		Size: 10.9 MB (10921342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d328ac00f385cdf1e967b3563490ef71319627a85149e04464202d4405186633`  
		Last Modified: Wed, 07 Feb 2024 22:05:49 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20df6294d50f788fb5270d7dd1a4482500cab32031d36d7054b0fe2bb9ad3388`  
		Last Modified: Wed, 07 Feb 2024 22:05:53 GMT  
		Size: 2.7 MB (2696693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993adcda16390f9d0b261707cde6cf96b2fbfaf8bb96fa54b01c4a398144f4d5`  
		Last Modified: Fri, 08 Mar 2024 16:43:14 GMT  
		Size: 9.5 MB (9468950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddad33904f84b8f1d9f9858646ed044016f91c329bf6491ddf905a4c9727f3c4`  
		Last Modified: Fri, 08 Mar 2024 16:43:40 GMT  
		Size: 132.5 MB (132485585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6125db7184428846b311e9359eea466b0f60a621909aef263d67072d417e304d`  
		Last Modified: Fri, 08 Mar 2024 16:43:11 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de92b5342a4b1431267ef2960ed4f572083b7e5e4555b301c6074c0af67e9f50`  
		Last Modified: Fri, 08 Mar 2024 16:43:11 GMT  
		Size: 2.2 KB (2154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:4003a283aad4330aff80c41290a82eb0ebffb57a34566aabee96a29175017c66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48517753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e587120d8e54fb5f41c2efd5cae962e6666bfa7c09b7e9d522f9eef79d331bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Wed, 07 Feb 2024 22:11:05 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 07 Feb 2024 22:11:05 GMT
ENV SATOSA_VERSION=8.4.0
# Wed, 07 Feb 2024 22:11:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 07 Feb 2024 22:11:33 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 07 Feb 2024 22:11:33 GMT
WORKDIR /etc/satosa
# Wed, 07 Feb 2024 22:11:34 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Wed, 07 Feb 2024 22:11:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Feb 2024 22:11:34 GMT
EXPOSE 8080
# Wed, 07 Feb 2024 22:11:34 GMT
USER satosa:satosa
# Wed, 07 Feb 2024 22:11:34 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fa4880b84a89cd734aeddf7f4553ca139e4d53722c41c54d930662c13fec8`  
		Last Modified: Sat, 27 Jan 2024 07:25:43 GMT  
		Size: 625.2 KB (625198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e7e2e0a7f3a4af923909dd104860d8fcd4d1f57bb80634083eeda0ba06e36b`  
		Last Modified: Wed, 07 Feb 2024 21:17:32 GMT  
		Size: 11.8 MB (11832383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99284986c3ffad45eb81cc0742b61e60571970e1c03d9069e0aec554fb1bc089`  
		Last Modified: Wed, 07 Feb 2024 21:17:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be93132253eb292b41ae301f69f0d47c791650c493ecd51e34ed720af01910c9`  
		Last Modified: Wed, 07 Feb 2024 21:17:31 GMT  
		Size: 2.7 MB (2696655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb40e308f00eb72552da1c91817c9bd1ee85c9cc0af8aa6b270e4ba38042daf`  
		Last Modified: Wed, 07 Feb 2024 22:12:05 GMT  
		Size: 9.7 MB (9676585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559bbf4aa424865f8954a90d5005b0a7eeb2e7f6f5cf2a650115800ae44371b`  
		Last Modified: Wed, 07 Feb 2024 22:12:07 GMT  
		Size: 20.3 MB (20326868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04661db7e0029a1b22d9c43b808257e317f876d92528b7e314a89ad81990793c`  
		Last Modified: Wed, 07 Feb 2024 22:12:04 GMT  
		Size: 10.0 KB (9960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6b843d24bf6a06297d5bfbd477d65a9ecd573ada69abf6cc16eacd553e82da`  
		Last Modified: Wed, 07 Feb 2024 22:12:04 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine3.19` - linux; 386

```console
$ docker pull satosa@sha256:391327fc04b4f25ff48fffe263ed5109d6cffec480b1e6ed9c8cd6cf3fd25a08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94656588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aba1b5dff88a26ff7c659482a828d40d8d9adc1ff13480e1cad44266f73cdeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 04:08:00 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_VERSION=3.12.1
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
CMD ["python3"]
# Sat, 27 Jan 2024 08:22:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Sat, 27 Jan 2024 08:22:45 GMT
ENV SATOSA_VERSION=8.4.0
# Sat, 27 Jan 2024 08:30:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Sat, 27 Jan 2024 08:30:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Sat, 27 Jan 2024 08:30:26 GMT
WORKDIR /etc/satosa
# Sat, 27 Jan 2024 08:30:26 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:30:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 08:30:26 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 08:30:26 GMT
USER satosa:satosa
# Sat, 27 Jan 2024 08:30:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7840a0a3a40a6b02ee9c509f8552e6bb70f9a8fb94398de1cfd742dc05d6050`  
		Last Modified: Sat, 27 Jan 2024 04:20:57 GMT  
		Size: 622.8 KB (622802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89a6fae803be2815fb73d36002db0a6aa6c6261cb6d1c568c1e00ae02507350`  
		Last Modified: Sat, 27 Jan 2024 04:21:32 GMT  
		Size: 11.9 MB (11929152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d0d6b56ec289e87c9c0271325d2cae165bad58b6190ea25e22cd8299e0c963`  
		Last Modified: Sat, 27 Jan 2024 04:21:29 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ce0078de875cf898e1a8d7656ea15eb2eace9d4a114c658313f5733402e8ba`  
		Last Modified: Sat, 27 Jan 2024 04:21:30 GMT  
		Size: 2.7 MB (2676259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e3b9a523576b9b8f6a758d4dfcd9a5ab83ba3dc460ef410e4b0be5d7f02c5d`  
		Last Modified: Sat, 27 Jan 2024 08:30:54 GMT  
		Size: 9.6 MB (9619654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc02b6f314d5143b4bc8115b6c540646f5deae4b004b585d1a15342ebf610237`  
		Last Modified: Sat, 27 Jan 2024 08:31:05 GMT  
		Size: 66.6 MB (66552282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47f30cea7d9bc3b8100a695fa9f8a41d253b16b3d39b65ec60470bbbdc52768`  
		Last Modified: Sat, 27 Jan 2024 08:30:51 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49df7ef97d6d92a9d16c8cffdfffe18e75f5e9cd3efe35eccc95aa30bc4f1f7`  
		Last Modified: Sat, 27 Jan 2024 08:30:52 GMT  
		Size: 2.1 KB (2147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine3.19` - linux; ppc64le

```console
$ docker pull satosa@sha256:eefaaf894c37cec9de82537d9844a7c6aec372efe493097fcdd99d78ceaa6bc2
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94283311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bc2d6148135e13cd1b75f30a029b33261fdcb1a5d4a90446d48e5902c57d5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 04:08:00 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_VERSION=3.12.1
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
CMD ["python3"]
# Sat, 27 Jan 2024 08:29:57 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Sat, 27 Jan 2024 08:29:58 GMT
ENV SATOSA_VERSION=8.4.0
# Sat, 27 Jan 2024 08:35:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Sat, 27 Jan 2024 08:35:40 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Sat, 27 Jan 2024 08:35:41 GMT
WORKDIR /etc/satosa
# Sat, 27 Jan 2024 08:35:41 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 08:35:42 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 08:35:43 GMT
USER satosa:satosa
# Sat, 27 Jan 2024 08:35:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d49a9cfe46131ab86b7a184f64865c97ae9d291935002bc7c38567ff27bc73`  
		Last Modified: Sat, 27 Jan 2024 06:51:52 GMT  
		Size: 625.6 KB (625581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e5feee510f8a33a7c371811dafb8bfa0914967fb6c7a516d67434cb1bbd204`  
		Last Modified: Sat, 27 Jan 2024 06:52:28 GMT  
		Size: 12.2 MB (12243607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d0977324b0b3dca506e76d3bde6f9ba583b255bb6941a1be3cbd3a73ff8e6f`  
		Last Modified: Sat, 27 Jan 2024 06:52:26 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63e83db5219c14a37c232e666d4337f900b691fb9e37066556b49fcf6223858`  
		Last Modified: Sat, 27 Jan 2024 06:52:27 GMT  
		Size: 2.7 MB (2676106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d565eb92095419ba03c37c05cab7fa100fb04315710cdd16052fdd4026e1ba`  
		Last Modified: Sat, 27 Jan 2024 08:36:06 GMT  
		Size: 9.8 MB (9801173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03bb04d932f9c6684e334ebedaabaef15c5ca10a2039fc7b092a7c560784931e`  
		Last Modified: Sat, 27 Jan 2024 08:36:14 GMT  
		Size: 65.6 MB (65566138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a082af4585697a65565659cfcf6c0f50d7db1bd8691e3ae138bf5217d4f040`  
		Last Modified: Sat, 27 Jan 2024 08:36:04 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3c70f43dc7ba65b86cf51f7fd90190c017be2d0cc2d247dc00cfb5bee93f19`  
		Last Modified: Sat, 27 Jan 2024 08:36:04 GMT  
		Size: 2.1 KB (2148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8-bookworm`

```console
$ docker pull satosa@sha256:c81291396725ec7b05c481c9e767800f9c0a2a5886ba15963999220508cb6c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `satosa:8-bookworm` - linux; amd64

```console
$ docker pull satosa@sha256:5c32b82a481315407a8213fe68c5484f56208ce09c049e38d59561c73e150d58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90906882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03bfb47ed64e4c5dc1ea893114954587da90fc25a3247e4612f329469038ef9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
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
# Tue, 13 Feb 2024 15:44:32 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 15:44:32 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 15:45:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 15:45:32 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 15:45:32 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 15:45:32 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 15:45:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 15:45:32 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 15:45:32 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 15:45:32 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d1f07906b71fd60ac43c61035514996a8ad8dbfd39d4f570ac5446b064ee5d`  
		Last Modified: Tue, 13 Feb 2024 11:12:54 GMT  
		Size: 3.5 MB (3507732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3e9a37b01a92d059e8ee8ff525a84400222555e33cae231f8b1d788957450d`  
		Last Modified: Tue, 13 Feb 2024 11:13:47 GMT  
		Size: 12.0 MB (11991512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a33514831e0a3ab693884ed9b534dacd5b2c7110c64692812e78da8471d1f0b`  
		Last Modified: Tue, 13 Feb 2024 11:13:44 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959bfd25ad80f8e7023ffd4f70fd6242ee502c15f6671bd4d299d32efc40470`  
		Last Modified: Tue, 13 Feb 2024 11:13:45 GMT  
		Size: 3.0 MB (2978901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbce98668aa61c3d668392a27d1f07962a0b05246e61e0c6fdd02e9ff3b99cb`  
		Last Modified: Tue, 13 Feb 2024 15:46:04 GMT  
		Size: 22.1 MB (22131281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c2e9f06bef4f772530677cf3122ac0560bcd3f06eef8c1b2f5912840640f37`  
		Last Modified: Tue, 13 Feb 2024 15:46:04 GMT  
		Size: 21.2 MB (21161018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0149f2d2741d11c38936bd8be232ff2e6ff77eae0054a9af5021b6a01b736d0d`  
		Last Modified: Tue, 13 Feb 2024 15:46:01 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be0dac7d9ed7489cc123f4313d801f0b415a9231541a419d86ce216c05dcaa0`  
		Last Modified: Tue, 13 Feb 2024 15:46:01 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-bookworm` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:3a68256b9eab756090fcfd6e0fb01d31474c035065ef89a46fc20a103cfb03cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89982898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a7461963f9363c0e895bb78ed23316e77c1fccaa66569858c0373a613a3da0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
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
# Tue, 12 Mar 2024 13:00:40 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 12 Mar 2024 13:00:40 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 12 Mar 2024 13:01:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 12 Mar 2024 13:01:39 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 12 Mar 2024 13:01:39 GMT
WORKDIR /etc/satosa
# Tue, 12 Mar 2024 13:01:39 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 12 Mar 2024 13:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 13:01:39 GMT
EXPOSE 8080
# Tue, 12 Mar 2024 13:01:39 GMT
USER satosa:satosa
# Tue, 12 Mar 2024 13:01:39 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55af26b7addf6c0f6fe5fed39393a1379356bb864caac1da91a0fd2fa77b911b`  
		Last Modified: Tue, 12 Mar 2024 09:46:35 GMT  
		Size: 3.3 MB (3323852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3caa3c29ca1489fb5a2119be7e582ca42dece866341d3a379b776c5b2c6362b`  
		Last Modified: Tue, 12 Mar 2024 09:47:24 GMT  
		Size: 12.0 MB (11965714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1240f83dd7d124ccb21f022464852fd5587ac77b5e6be447b86db873dc0bf6d`  
		Last Modified: Tue, 12 Mar 2024 09:47:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6318e81a3dccbefef51184e62057428961a21b0cde407673f088ee0f57417ddc`  
		Last Modified: Tue, 12 Mar 2024 09:47:23 GMT  
		Size: 3.0 MB (2979263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1b6451ffebc99e9f0ea5b7dfcb1ae02b45eca810ebc9bbada3dfc6a5005861`  
		Last Modified: Tue, 12 Mar 2024 13:02:09 GMT  
		Size: 22.0 MB (21976035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ab61321e7317b6e6d2219203156533d48070dc964baf5797c21336fd94c513`  
		Last Modified: Tue, 12 Mar 2024 13:02:09 GMT  
		Size: 20.6 MB (20569252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dab6e27ad8fb7aa4c1c72574a8ed2a1d04a5de529a450fb5605b521fe12ba6`  
		Last Modified: Tue, 12 Mar 2024 13:02:06 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf6d0d867f4ba1d51aaba9bf44b27b3936fbc500d13376e4252cdbb8826648e`  
		Last Modified: Tue, 12 Mar 2024 13:02:06 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-bookworm` - linux; 386

```console
$ docker pull satosa@sha256:29df1f337d370235279a903eb80322eb9eec3ac134684f701bd59c93d7281437
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.7 MB (488727279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff9657cc4d63a559b1c55d0d689270b3cab3685c02704b1406c3f8d3bb27d29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:56 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Tue, 13 Feb 2024 00:38:56 GMT
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
# Tue, 13 Feb 2024 17:58:09 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 17:58:09 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 18:09:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 18:09:09 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 18:09:09 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 18:09:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 18:09:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 18:09:10 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 18:09:10 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 18:09:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18cc86e13533dd94d2b3a19bfcb8d1ebde259ebc088243e630bf43438b4bb0`  
		Last Modified: Tue, 13 Feb 2024 14:51:20 GMT  
		Size: 3.5 MB (3503117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48b2b4dedbd677d6449d91281ba20d6fe52233483171d23c4296d9fc6d8cb59`  
		Last Modified: Tue, 13 Feb 2024 14:52:23 GMT  
		Size: 12.2 MB (12239206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a65413fe49c71ab3fa6df4fdf4255039158476191db636768837f1e6e8f735`  
		Last Modified: Tue, 13 Feb 2024 14:52:20 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a42bf4645e12370533b1732e65757f2816f1497d63b7f58b12adb1f283696c3`  
		Last Modified: Tue, 13 Feb 2024 14:52:22 GMT  
		Size: 3.0 MB (2978347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2ac513cfa963fa4f372c2e074be3b84b2c51e0b44bc35cce298f09deba2abe`  
		Last Modified: Tue, 13 Feb 2024 18:22:49 GMT  
		Size: 24.2 MB (24203811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580091280836d4f1a1b351ea86e768f03371c70d1bf055b106d9206deae3f257`  
		Last Modified: Tue, 13 Feb 2024 18:23:18 GMT  
		Size: 415.6 MB (415648638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24b0ff82749ad53a37fb38644218e460b515aa025d63420ebb6c720b02ba1a1`  
		Last Modified: Tue, 13 Feb 2024 18:22:43 GMT  
		Size: 10.0 KB (9963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8ea8a78031214f83625ad937146849d4742abbf5ad497ded7e20c73e51dc3c`  
		Last Modified: Tue, 13 Feb 2024 18:22:43 GMT  
		Size: 2.1 KB (2144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-bookworm` - linux; ppc64le

```console
$ docker pull satosa@sha256:3ca21f61a53fe5346c76ed4b9351ce8f001d671762a09a9c1107237d507d7925
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.2 MB (491195693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde9ec216fdcaf6771a71bba1c3a946c1400e738a3a3d304194b057d98b2dd5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:03 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Tue, 13 Feb 2024 00:39:05 GMT
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
# Tue, 13 Feb 2024 08:21:36 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 08:21:37 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 08:29:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 08:29:24 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 08:29:25 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 08:29:25 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 08:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 08:29:26 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 08:29:26 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 08:29:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee78f2de2777d7bd5e7363b69080bb1a6394e1cddd1fc2acaa7f608b1d129d7a`  
		Last Modified: Tue, 13 Feb 2024 03:40:38 GMT  
		Size: 3.7 MB (3704538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8cf259e5ab2eafff3461cd2b4fd546d5d20b75f29b62cd7f1efe2cb09905ff`  
		Last Modified: Tue, 13 Feb 2024 03:41:09 GMT  
		Size: 12.6 MB (12602554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7325c8b16dd117cc14e83e03632bfff7d1ff2dd5c50743012aefa3de8b7b2b15`  
		Last Modified: Tue, 13 Feb 2024 03:41:07 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b53c907fc7631d6fac41077df35d1d3a0ece736979014a24f63fa5ca967935c`  
		Last Modified: Tue, 13 Feb 2024 03:41:08 GMT  
		Size: 3.0 MB (2979477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0549feb427d838b6be46181808df359991252c393af2d1bf946f037982b6450b`  
		Last Modified: Tue, 13 Feb 2024 08:38:33 GMT  
		Size: 24.5 MB (24498861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63086daba02a48c5c956598cef502964ec2b7e522483c7ab0ce6bdec980f1ea2`  
		Last Modified: Tue, 13 Feb 2024 08:38:53 GMT  
		Size: 414.3 MB (414279010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1208cb1697601637c58f6636e02d78eb11f3c9066acc050f74644091e9ca9646`  
		Last Modified: Tue, 13 Feb 2024 08:38:29 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922bf6d55eb5cac0384856e8c65367780d6352aa0675e993301e232564115cd5`  
		Last Modified: Tue, 13 Feb 2024 08:38:29 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-bookworm` - linux; s390x

```console
$ docker pull satosa@sha256:39a52857d3d3587a0c290bb162869643e8b9238f59ad917118de3baee91ee50d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.2 MB (498229609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83ea5fd0b8ea8f4fc660c3019bc2988cc4386e050e60fc94ae79e6ea783b2cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 01:02:37 GMT
ADD file:2dc5fd465b3cc728990229e12489d68faf8a93e6f574cacdca11cc9bf31f511d in / 
# Tue, 13 Feb 2024 01:02:39 GMT
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
# Fri, 16 Feb 2024 16:03:41 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Fri, 16 Feb 2024 16:03:42 GMT
ENV SATOSA_VERSION=8.4.0
# Fri, 16 Feb 2024 16:09:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 16 Feb 2024 16:09:18 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 16 Feb 2024 16:09:18 GMT
WORKDIR /etc/satosa
# Fri, 16 Feb 2024 16:09:18 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 16 Feb 2024 16:09:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 16:09:18 GMT
EXPOSE 8080
# Fri, 16 Feb 2024 16:09:18 GMT
USER satosa:satosa
# Fri, 16 Feb 2024 16:09:18 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e55f0b78e9a121a048a72242f0aec2a221466b10bedb873c07b73e4b99f873cb`  
		Last Modified: Tue, 13 Feb 2024 01:30:22 GMT  
		Size: 27.5 MB (27488587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3ec7775a265efbf6c384c5d18340a5650c973a50ca2d0e398efd6f07517659`  
		Last Modified: Tue, 13 Feb 2024 11:03:06 GMT  
		Size: 3.2 MB (3166462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082a41a047ff2d36ba555081aeb9a03139eab7b42242dbe438a27a94c51a2118`  
		Last Modified: Fri, 16 Feb 2024 10:40:39 GMT  
		Size: 11.9 MB (11917778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0926d163b9bf2515318962adbb6c235265efae4c566c49f626ddf024df8a42`  
		Last Modified: Fri, 16 Feb 2024 10:40:37 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf892b126232594fc63d047a9f20f7e6170f1e2a219318db54ab08bd0fc07ed`  
		Last Modified: Fri, 16 Feb 2024 10:40:38 GMT  
		Size: 3.0 MB (2978431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4ef25f44b24d50ed7297148115ca7338cfb361dc21d3f50ff822fbe72640c3`  
		Last Modified: Fri, 16 Feb 2024 16:10:46 GMT  
		Size: 23.8 MB (23798204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183d32aa11aa9166c3b9942b91e0c6928610420fb825c3040b4b013e74e74636`  
		Last Modified: Fri, 16 Feb 2024 16:11:02 GMT  
		Size: 428.9 MB (428867797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4adc9965b1ba16dd34f2892e459b028712639a3e92a446b334f71dd3dc941dd`  
		Last Modified: Fri, 16 Feb 2024 16:10:43 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5072cc9e5ef227421d9831c3f457357ca1ca7e2220f50e68b27aebee0bcf6438`  
		Last Modified: Fri, 16 Feb 2024 16:10:43 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.4`

```console
$ docker pull satosa@sha256:c81291396725ec7b05c481c9e767800f9c0a2a5886ba15963999220508cb6c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `satosa:8.4` - linux; amd64

```console
$ docker pull satosa@sha256:5c32b82a481315407a8213fe68c5484f56208ce09c049e38d59561c73e150d58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90906882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03bfb47ed64e4c5dc1ea893114954587da90fc25a3247e4612f329469038ef9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
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
# Tue, 13 Feb 2024 15:44:32 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 15:44:32 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 15:45:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 15:45:32 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 15:45:32 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 15:45:32 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 15:45:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 15:45:32 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 15:45:32 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 15:45:32 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d1f07906b71fd60ac43c61035514996a8ad8dbfd39d4f570ac5446b064ee5d`  
		Last Modified: Tue, 13 Feb 2024 11:12:54 GMT  
		Size: 3.5 MB (3507732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3e9a37b01a92d059e8ee8ff525a84400222555e33cae231f8b1d788957450d`  
		Last Modified: Tue, 13 Feb 2024 11:13:47 GMT  
		Size: 12.0 MB (11991512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a33514831e0a3ab693884ed9b534dacd5b2c7110c64692812e78da8471d1f0b`  
		Last Modified: Tue, 13 Feb 2024 11:13:44 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959bfd25ad80f8e7023ffd4f70fd6242ee502c15f6671bd4d299d32efc40470`  
		Last Modified: Tue, 13 Feb 2024 11:13:45 GMT  
		Size: 3.0 MB (2978901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbce98668aa61c3d668392a27d1f07962a0b05246e61e0c6fdd02e9ff3b99cb`  
		Last Modified: Tue, 13 Feb 2024 15:46:04 GMT  
		Size: 22.1 MB (22131281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c2e9f06bef4f772530677cf3122ac0560bcd3f06eef8c1b2f5912840640f37`  
		Last Modified: Tue, 13 Feb 2024 15:46:04 GMT  
		Size: 21.2 MB (21161018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0149f2d2741d11c38936bd8be232ff2e6ff77eae0054a9af5021b6a01b736d0d`  
		Last Modified: Tue, 13 Feb 2024 15:46:01 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be0dac7d9ed7489cc123f4313d801f0b415a9231541a419d86ce216c05dcaa0`  
		Last Modified: Tue, 13 Feb 2024 15:46:01 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:3a68256b9eab756090fcfd6e0fb01d31474c035065ef89a46fc20a103cfb03cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89982898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a7461963f9363c0e895bb78ed23316e77c1fccaa66569858c0373a613a3da0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
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
# Tue, 12 Mar 2024 13:00:40 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 12 Mar 2024 13:00:40 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 12 Mar 2024 13:01:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 12 Mar 2024 13:01:39 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 12 Mar 2024 13:01:39 GMT
WORKDIR /etc/satosa
# Tue, 12 Mar 2024 13:01:39 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 12 Mar 2024 13:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 13:01:39 GMT
EXPOSE 8080
# Tue, 12 Mar 2024 13:01:39 GMT
USER satosa:satosa
# Tue, 12 Mar 2024 13:01:39 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55af26b7addf6c0f6fe5fed39393a1379356bb864caac1da91a0fd2fa77b911b`  
		Last Modified: Tue, 12 Mar 2024 09:46:35 GMT  
		Size: 3.3 MB (3323852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3caa3c29ca1489fb5a2119be7e582ca42dece866341d3a379b776c5b2c6362b`  
		Last Modified: Tue, 12 Mar 2024 09:47:24 GMT  
		Size: 12.0 MB (11965714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1240f83dd7d124ccb21f022464852fd5587ac77b5e6be447b86db873dc0bf6d`  
		Last Modified: Tue, 12 Mar 2024 09:47:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6318e81a3dccbefef51184e62057428961a21b0cde407673f088ee0f57417ddc`  
		Last Modified: Tue, 12 Mar 2024 09:47:23 GMT  
		Size: 3.0 MB (2979263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1b6451ffebc99e9f0ea5b7dfcb1ae02b45eca810ebc9bbada3dfc6a5005861`  
		Last Modified: Tue, 12 Mar 2024 13:02:09 GMT  
		Size: 22.0 MB (21976035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ab61321e7317b6e6d2219203156533d48070dc964baf5797c21336fd94c513`  
		Last Modified: Tue, 12 Mar 2024 13:02:09 GMT  
		Size: 20.6 MB (20569252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dab6e27ad8fb7aa4c1c72574a8ed2a1d04a5de529a450fb5605b521fe12ba6`  
		Last Modified: Tue, 12 Mar 2024 13:02:06 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf6d0d867f4ba1d51aaba9bf44b27b3936fbc500d13376e4252cdbb8826648e`  
		Last Modified: Tue, 12 Mar 2024 13:02:06 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4` - linux; 386

```console
$ docker pull satosa@sha256:29df1f337d370235279a903eb80322eb9eec3ac134684f701bd59c93d7281437
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.7 MB (488727279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff9657cc4d63a559b1c55d0d689270b3cab3685c02704b1406c3f8d3bb27d29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:56 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Tue, 13 Feb 2024 00:38:56 GMT
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
# Tue, 13 Feb 2024 17:58:09 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 17:58:09 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 18:09:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 18:09:09 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 18:09:09 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 18:09:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 18:09:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 18:09:10 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 18:09:10 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 18:09:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18cc86e13533dd94d2b3a19bfcb8d1ebde259ebc088243e630bf43438b4bb0`  
		Last Modified: Tue, 13 Feb 2024 14:51:20 GMT  
		Size: 3.5 MB (3503117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48b2b4dedbd677d6449d91281ba20d6fe52233483171d23c4296d9fc6d8cb59`  
		Last Modified: Tue, 13 Feb 2024 14:52:23 GMT  
		Size: 12.2 MB (12239206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a65413fe49c71ab3fa6df4fdf4255039158476191db636768837f1e6e8f735`  
		Last Modified: Tue, 13 Feb 2024 14:52:20 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a42bf4645e12370533b1732e65757f2816f1497d63b7f58b12adb1f283696c3`  
		Last Modified: Tue, 13 Feb 2024 14:52:22 GMT  
		Size: 3.0 MB (2978347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2ac513cfa963fa4f372c2e074be3b84b2c51e0b44bc35cce298f09deba2abe`  
		Last Modified: Tue, 13 Feb 2024 18:22:49 GMT  
		Size: 24.2 MB (24203811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580091280836d4f1a1b351ea86e768f03371c70d1bf055b106d9206deae3f257`  
		Last Modified: Tue, 13 Feb 2024 18:23:18 GMT  
		Size: 415.6 MB (415648638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24b0ff82749ad53a37fb38644218e460b515aa025d63420ebb6c720b02ba1a1`  
		Last Modified: Tue, 13 Feb 2024 18:22:43 GMT  
		Size: 10.0 KB (9963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8ea8a78031214f83625ad937146849d4742abbf5ad497ded7e20c73e51dc3c`  
		Last Modified: Tue, 13 Feb 2024 18:22:43 GMT  
		Size: 2.1 KB (2144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4` - linux; ppc64le

```console
$ docker pull satosa@sha256:3ca21f61a53fe5346c76ed4b9351ce8f001d671762a09a9c1107237d507d7925
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.2 MB (491195693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde9ec216fdcaf6771a71bba1c3a946c1400e738a3a3d304194b057d98b2dd5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:03 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Tue, 13 Feb 2024 00:39:05 GMT
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
# Tue, 13 Feb 2024 08:21:36 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 08:21:37 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 08:29:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 08:29:24 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 08:29:25 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 08:29:25 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 08:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 08:29:26 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 08:29:26 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 08:29:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee78f2de2777d7bd5e7363b69080bb1a6394e1cddd1fc2acaa7f608b1d129d7a`  
		Last Modified: Tue, 13 Feb 2024 03:40:38 GMT  
		Size: 3.7 MB (3704538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8cf259e5ab2eafff3461cd2b4fd546d5d20b75f29b62cd7f1efe2cb09905ff`  
		Last Modified: Tue, 13 Feb 2024 03:41:09 GMT  
		Size: 12.6 MB (12602554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7325c8b16dd117cc14e83e03632bfff7d1ff2dd5c50743012aefa3de8b7b2b15`  
		Last Modified: Tue, 13 Feb 2024 03:41:07 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b53c907fc7631d6fac41077df35d1d3a0ece736979014a24f63fa5ca967935c`  
		Last Modified: Tue, 13 Feb 2024 03:41:08 GMT  
		Size: 3.0 MB (2979477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0549feb427d838b6be46181808df359991252c393af2d1bf946f037982b6450b`  
		Last Modified: Tue, 13 Feb 2024 08:38:33 GMT  
		Size: 24.5 MB (24498861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63086daba02a48c5c956598cef502964ec2b7e522483c7ab0ce6bdec980f1ea2`  
		Last Modified: Tue, 13 Feb 2024 08:38:53 GMT  
		Size: 414.3 MB (414279010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1208cb1697601637c58f6636e02d78eb11f3c9066acc050f74644091e9ca9646`  
		Last Modified: Tue, 13 Feb 2024 08:38:29 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922bf6d55eb5cac0384856e8c65367780d6352aa0675e993301e232564115cd5`  
		Last Modified: Tue, 13 Feb 2024 08:38:29 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4` - linux; s390x

```console
$ docker pull satosa@sha256:39a52857d3d3587a0c290bb162869643e8b9238f59ad917118de3baee91ee50d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.2 MB (498229609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83ea5fd0b8ea8f4fc660c3019bc2988cc4386e050e60fc94ae79e6ea783b2cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 01:02:37 GMT
ADD file:2dc5fd465b3cc728990229e12489d68faf8a93e6f574cacdca11cc9bf31f511d in / 
# Tue, 13 Feb 2024 01:02:39 GMT
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
# Fri, 16 Feb 2024 16:03:41 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Fri, 16 Feb 2024 16:03:42 GMT
ENV SATOSA_VERSION=8.4.0
# Fri, 16 Feb 2024 16:09:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 16 Feb 2024 16:09:18 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 16 Feb 2024 16:09:18 GMT
WORKDIR /etc/satosa
# Fri, 16 Feb 2024 16:09:18 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 16 Feb 2024 16:09:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 16:09:18 GMT
EXPOSE 8080
# Fri, 16 Feb 2024 16:09:18 GMT
USER satosa:satosa
# Fri, 16 Feb 2024 16:09:18 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e55f0b78e9a121a048a72242f0aec2a221466b10bedb873c07b73e4b99f873cb`  
		Last Modified: Tue, 13 Feb 2024 01:30:22 GMT  
		Size: 27.5 MB (27488587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3ec7775a265efbf6c384c5d18340a5650c973a50ca2d0e398efd6f07517659`  
		Last Modified: Tue, 13 Feb 2024 11:03:06 GMT  
		Size: 3.2 MB (3166462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082a41a047ff2d36ba555081aeb9a03139eab7b42242dbe438a27a94c51a2118`  
		Last Modified: Fri, 16 Feb 2024 10:40:39 GMT  
		Size: 11.9 MB (11917778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0926d163b9bf2515318962adbb6c235265efae4c566c49f626ddf024df8a42`  
		Last Modified: Fri, 16 Feb 2024 10:40:37 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf892b126232594fc63d047a9f20f7e6170f1e2a219318db54ab08bd0fc07ed`  
		Last Modified: Fri, 16 Feb 2024 10:40:38 GMT  
		Size: 3.0 MB (2978431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4ef25f44b24d50ed7297148115ca7338cfb361dc21d3f50ff822fbe72640c3`  
		Last Modified: Fri, 16 Feb 2024 16:10:46 GMT  
		Size: 23.8 MB (23798204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183d32aa11aa9166c3b9942b91e0c6928610420fb825c3040b4b013e74e74636`  
		Last Modified: Fri, 16 Feb 2024 16:11:02 GMT  
		Size: 428.9 MB (428867797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4adc9965b1ba16dd34f2892e459b028712639a3e92a446b334f71dd3dc941dd`  
		Last Modified: Fri, 16 Feb 2024 16:10:43 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5072cc9e5ef227421d9831c3f457357ca1ca7e2220f50e68b27aebee0bcf6438`  
		Last Modified: Fri, 16 Feb 2024 16:10:43 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.4-alpine`

```console
$ docker pull satosa@sha256:d6a2f8debb3cfdc184790fb74026c2cbffd7f402a4a65ecb8e082285143d45a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `satosa:8.4-alpine` - linux; amd64

```console
$ docker pull satosa@sha256:b6c892a0480ef2f611608277c260c734ea8857698bd61dd64e57ac191af80a89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47166027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe054bc0129c5e7daaba60958ed19cf96cc8937a1ef76ee8b83ccbd25b90cdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Thu, 08 Feb 2024 00:28:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Thu, 08 Feb 2024 00:28:45 GMT
ENV SATOSA_VERSION=8.4.0
# Thu, 08 Feb 2024 00:29:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 08 Feb 2024 00:29:10 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 08 Feb 2024 00:29:10 GMT
WORKDIR /etc/satosa
# Thu, 08 Feb 2024 00:29:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Thu, 08 Feb 2024 00:29:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 00:29:10 GMT
EXPOSE 8080
# Thu, 08 Feb 2024 00:29:10 GMT
USER satosa:satosa
# Thu, 08 Feb 2024 00:29:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca80dc46cecdd1a97787a1dd6f74263b9d2f7b0dd3e2e15c109f5e34848c932`  
		Last Modified: Sat, 27 Jan 2024 07:51:02 GMT  
		Size: 622.1 KB (622150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9e15b6315c34de5c802bdbd343e3ec69bdc4ab870783fc1b9552daaef25e77`  
		Last Modified: Wed, 07 Feb 2024 23:45:23 GMT  
		Size: 11.8 MB (11767542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fd6f3f484fdfccf33965ca0f8807e5078a619803cf638d82bc4a405e91de04`  
		Last Modified: Wed, 07 Feb 2024 23:45:21 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc96b5c1ba465ba27fb55d4766ade8624de4082ac1530b3293ac735ab3ead50`  
		Last Modified: Wed, 07 Feb 2024 23:45:22 GMT  
		Size: 2.7 MB (2696625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7692e7a182f83cff0c00ace6108c6b19e2059f97d2d3aae2480e8eef815237`  
		Last Modified: Thu, 08 Feb 2024 00:29:42 GMT  
		Size: 7.9 MB (7879777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044eb85425384353220c085b958e1f4064080737c8be49f4fa5d4fb9fc427a4a`  
		Last Modified: Thu, 08 Feb 2024 00:29:44 GMT  
		Size: 20.8 MB (20778854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0c0a4c37ce81a2bad65869c10e4226cf2dd90d5dfccc4e9e9973166e1c790c`  
		Last Modified: Thu, 08 Feb 2024 00:29:41 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ceec51a6010f771ca188eb6a330bc23fd71249d03d2014775390fd899cf8ae`  
		Last Modified: Thu, 08 Feb 2024 00:29:41 GMT  
		Size: 2.1 KB (2147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4-alpine` - linux; arm variant v7

```console
$ docker pull satosa@sha256:523c142c7c6862e72402d75c6c99136d078f1c3bff0832f307c144a87301c563
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159126183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b6e032712d5981488f40cc76e4bd93d0f28b13a6f6c3d58497260a1e5706a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Mon, 04 Mar 2024 00:18:24 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Mon, 04 Mar 2024 00:18:24 GMT
ENV SATOSA_VERSION=8.4.0
# Fri, 08 Mar 2024 16:42:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 08 Mar 2024 16:42:47 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 08 Mar 2024 16:42:48 GMT
WORKDIR /etc/satosa
# Fri, 08 Mar 2024 16:42:48 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 08 Mar 2024 16:42:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Mar 2024 16:42:49 GMT
EXPOSE 8080
# Fri, 08 Mar 2024 16:42:49 GMT
USER satosa:satosa
# Fri, 08 Mar 2024 16:42:49 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3966cfc81792baee0378a9d2d85424676e1972ac6efaf02823ead42801b9b955`  
		Last Modified: Sat, 27 Jan 2024 09:56:47 GMT  
		Size: 622.3 KB (622347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e682fb52211fcfe80358aff5f595fc49d17d84a426dfe07531a831b75feb09`  
		Last Modified: Wed, 07 Feb 2024 22:05:51 GMT  
		Size: 10.9 MB (10921342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d328ac00f385cdf1e967b3563490ef71319627a85149e04464202d4405186633`  
		Last Modified: Wed, 07 Feb 2024 22:05:49 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20df6294d50f788fb5270d7dd1a4482500cab32031d36d7054b0fe2bb9ad3388`  
		Last Modified: Wed, 07 Feb 2024 22:05:53 GMT  
		Size: 2.7 MB (2696693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993adcda16390f9d0b261707cde6cf96b2fbfaf8bb96fa54b01c4a398144f4d5`  
		Last Modified: Fri, 08 Mar 2024 16:43:14 GMT  
		Size: 9.5 MB (9468950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddad33904f84b8f1d9f9858646ed044016f91c329bf6491ddf905a4c9727f3c4`  
		Last Modified: Fri, 08 Mar 2024 16:43:40 GMT  
		Size: 132.5 MB (132485585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6125db7184428846b311e9359eea466b0f60a621909aef263d67072d417e304d`  
		Last Modified: Fri, 08 Mar 2024 16:43:11 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de92b5342a4b1431267ef2960ed4f572083b7e5e4555b301c6074c0af67e9f50`  
		Last Modified: Fri, 08 Mar 2024 16:43:11 GMT  
		Size: 2.2 KB (2154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4-alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:4003a283aad4330aff80c41290a82eb0ebffb57a34566aabee96a29175017c66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48517753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e587120d8e54fb5f41c2efd5cae962e6666bfa7c09b7e9d522f9eef79d331bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Wed, 07 Feb 2024 22:11:05 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 07 Feb 2024 22:11:05 GMT
ENV SATOSA_VERSION=8.4.0
# Wed, 07 Feb 2024 22:11:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 07 Feb 2024 22:11:33 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 07 Feb 2024 22:11:33 GMT
WORKDIR /etc/satosa
# Wed, 07 Feb 2024 22:11:34 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Wed, 07 Feb 2024 22:11:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Feb 2024 22:11:34 GMT
EXPOSE 8080
# Wed, 07 Feb 2024 22:11:34 GMT
USER satosa:satosa
# Wed, 07 Feb 2024 22:11:34 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fa4880b84a89cd734aeddf7f4553ca139e4d53722c41c54d930662c13fec8`  
		Last Modified: Sat, 27 Jan 2024 07:25:43 GMT  
		Size: 625.2 KB (625198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e7e2e0a7f3a4af923909dd104860d8fcd4d1f57bb80634083eeda0ba06e36b`  
		Last Modified: Wed, 07 Feb 2024 21:17:32 GMT  
		Size: 11.8 MB (11832383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99284986c3ffad45eb81cc0742b61e60571970e1c03d9069e0aec554fb1bc089`  
		Last Modified: Wed, 07 Feb 2024 21:17:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be93132253eb292b41ae301f69f0d47c791650c493ecd51e34ed720af01910c9`  
		Last Modified: Wed, 07 Feb 2024 21:17:31 GMT  
		Size: 2.7 MB (2696655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb40e308f00eb72552da1c91817c9bd1ee85c9cc0af8aa6b270e4ba38042daf`  
		Last Modified: Wed, 07 Feb 2024 22:12:05 GMT  
		Size: 9.7 MB (9676585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559bbf4aa424865f8954a90d5005b0a7eeb2e7f6f5cf2a650115800ae44371b`  
		Last Modified: Wed, 07 Feb 2024 22:12:07 GMT  
		Size: 20.3 MB (20326868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04661db7e0029a1b22d9c43b808257e317f876d92528b7e314a89ad81990793c`  
		Last Modified: Wed, 07 Feb 2024 22:12:04 GMT  
		Size: 10.0 KB (9960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6b843d24bf6a06297d5bfbd477d65a9ecd573ada69abf6cc16eacd553e82da`  
		Last Modified: Wed, 07 Feb 2024 22:12:04 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4-alpine` - linux; 386

```console
$ docker pull satosa@sha256:391327fc04b4f25ff48fffe263ed5109d6cffec480b1e6ed9c8cd6cf3fd25a08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94656588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aba1b5dff88a26ff7c659482a828d40d8d9adc1ff13480e1cad44266f73cdeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 04:08:00 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_VERSION=3.12.1
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
CMD ["python3"]
# Sat, 27 Jan 2024 08:22:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Sat, 27 Jan 2024 08:22:45 GMT
ENV SATOSA_VERSION=8.4.0
# Sat, 27 Jan 2024 08:30:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Sat, 27 Jan 2024 08:30:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Sat, 27 Jan 2024 08:30:26 GMT
WORKDIR /etc/satosa
# Sat, 27 Jan 2024 08:30:26 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:30:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 08:30:26 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 08:30:26 GMT
USER satosa:satosa
# Sat, 27 Jan 2024 08:30:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7840a0a3a40a6b02ee9c509f8552e6bb70f9a8fb94398de1cfd742dc05d6050`  
		Last Modified: Sat, 27 Jan 2024 04:20:57 GMT  
		Size: 622.8 KB (622802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89a6fae803be2815fb73d36002db0a6aa6c6261cb6d1c568c1e00ae02507350`  
		Last Modified: Sat, 27 Jan 2024 04:21:32 GMT  
		Size: 11.9 MB (11929152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d0d6b56ec289e87c9c0271325d2cae165bad58b6190ea25e22cd8299e0c963`  
		Last Modified: Sat, 27 Jan 2024 04:21:29 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ce0078de875cf898e1a8d7656ea15eb2eace9d4a114c658313f5733402e8ba`  
		Last Modified: Sat, 27 Jan 2024 04:21:30 GMT  
		Size: 2.7 MB (2676259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e3b9a523576b9b8f6a758d4dfcd9a5ab83ba3dc460ef410e4b0be5d7f02c5d`  
		Last Modified: Sat, 27 Jan 2024 08:30:54 GMT  
		Size: 9.6 MB (9619654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc02b6f314d5143b4bc8115b6c540646f5deae4b004b585d1a15342ebf610237`  
		Last Modified: Sat, 27 Jan 2024 08:31:05 GMT  
		Size: 66.6 MB (66552282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47f30cea7d9bc3b8100a695fa9f8a41d253b16b3d39b65ec60470bbbdc52768`  
		Last Modified: Sat, 27 Jan 2024 08:30:51 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49df7ef97d6d92a9d16c8cffdfffe18e75f5e9cd3efe35eccc95aa30bc4f1f7`  
		Last Modified: Sat, 27 Jan 2024 08:30:52 GMT  
		Size: 2.1 KB (2147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4-alpine` - linux; ppc64le

```console
$ docker pull satosa@sha256:eefaaf894c37cec9de82537d9844a7c6aec372efe493097fcdd99d78ceaa6bc2
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94283311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bc2d6148135e13cd1b75f30a029b33261fdcb1a5d4a90446d48e5902c57d5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 04:08:00 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_VERSION=3.12.1
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
CMD ["python3"]
# Sat, 27 Jan 2024 08:29:57 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Sat, 27 Jan 2024 08:29:58 GMT
ENV SATOSA_VERSION=8.4.0
# Sat, 27 Jan 2024 08:35:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Sat, 27 Jan 2024 08:35:40 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Sat, 27 Jan 2024 08:35:41 GMT
WORKDIR /etc/satosa
# Sat, 27 Jan 2024 08:35:41 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 08:35:42 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 08:35:43 GMT
USER satosa:satosa
# Sat, 27 Jan 2024 08:35:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d49a9cfe46131ab86b7a184f64865c97ae9d291935002bc7c38567ff27bc73`  
		Last Modified: Sat, 27 Jan 2024 06:51:52 GMT  
		Size: 625.6 KB (625581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e5feee510f8a33a7c371811dafb8bfa0914967fb6c7a516d67434cb1bbd204`  
		Last Modified: Sat, 27 Jan 2024 06:52:28 GMT  
		Size: 12.2 MB (12243607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d0977324b0b3dca506e76d3bde6f9ba583b255bb6941a1be3cbd3a73ff8e6f`  
		Last Modified: Sat, 27 Jan 2024 06:52:26 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63e83db5219c14a37c232e666d4337f900b691fb9e37066556b49fcf6223858`  
		Last Modified: Sat, 27 Jan 2024 06:52:27 GMT  
		Size: 2.7 MB (2676106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d565eb92095419ba03c37c05cab7fa100fb04315710cdd16052fdd4026e1ba`  
		Last Modified: Sat, 27 Jan 2024 08:36:06 GMT  
		Size: 9.8 MB (9801173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03bb04d932f9c6684e334ebedaabaef15c5ca10a2039fc7b092a7c560784931e`  
		Last Modified: Sat, 27 Jan 2024 08:36:14 GMT  
		Size: 65.6 MB (65566138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a082af4585697a65565659cfcf6c0f50d7db1bd8691e3ae138bf5217d4f040`  
		Last Modified: Sat, 27 Jan 2024 08:36:04 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3c70f43dc7ba65b86cf51f7fd90190c017be2d0cc2d247dc00cfb5bee93f19`  
		Last Modified: Sat, 27 Jan 2024 08:36:04 GMT  
		Size: 2.1 KB (2148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.4-alpine3.19`

```console
$ docker pull satosa@sha256:d6a2f8debb3cfdc184790fb74026c2cbffd7f402a4a65ecb8e082285143d45a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `satosa:8.4-alpine3.19` - linux; amd64

```console
$ docker pull satosa@sha256:b6c892a0480ef2f611608277c260c734ea8857698bd61dd64e57ac191af80a89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47166027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe054bc0129c5e7daaba60958ed19cf96cc8937a1ef76ee8b83ccbd25b90cdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Thu, 08 Feb 2024 00:28:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Thu, 08 Feb 2024 00:28:45 GMT
ENV SATOSA_VERSION=8.4.0
# Thu, 08 Feb 2024 00:29:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 08 Feb 2024 00:29:10 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 08 Feb 2024 00:29:10 GMT
WORKDIR /etc/satosa
# Thu, 08 Feb 2024 00:29:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Thu, 08 Feb 2024 00:29:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 00:29:10 GMT
EXPOSE 8080
# Thu, 08 Feb 2024 00:29:10 GMT
USER satosa:satosa
# Thu, 08 Feb 2024 00:29:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca80dc46cecdd1a97787a1dd6f74263b9d2f7b0dd3e2e15c109f5e34848c932`  
		Last Modified: Sat, 27 Jan 2024 07:51:02 GMT  
		Size: 622.1 KB (622150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9e15b6315c34de5c802bdbd343e3ec69bdc4ab870783fc1b9552daaef25e77`  
		Last Modified: Wed, 07 Feb 2024 23:45:23 GMT  
		Size: 11.8 MB (11767542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fd6f3f484fdfccf33965ca0f8807e5078a619803cf638d82bc4a405e91de04`  
		Last Modified: Wed, 07 Feb 2024 23:45:21 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc96b5c1ba465ba27fb55d4766ade8624de4082ac1530b3293ac735ab3ead50`  
		Last Modified: Wed, 07 Feb 2024 23:45:22 GMT  
		Size: 2.7 MB (2696625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7692e7a182f83cff0c00ace6108c6b19e2059f97d2d3aae2480e8eef815237`  
		Last Modified: Thu, 08 Feb 2024 00:29:42 GMT  
		Size: 7.9 MB (7879777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044eb85425384353220c085b958e1f4064080737c8be49f4fa5d4fb9fc427a4a`  
		Last Modified: Thu, 08 Feb 2024 00:29:44 GMT  
		Size: 20.8 MB (20778854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0c0a4c37ce81a2bad65869c10e4226cf2dd90d5dfccc4e9e9973166e1c790c`  
		Last Modified: Thu, 08 Feb 2024 00:29:41 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ceec51a6010f771ca188eb6a330bc23fd71249d03d2014775390fd899cf8ae`  
		Last Modified: Thu, 08 Feb 2024 00:29:41 GMT  
		Size: 2.1 KB (2147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4-alpine3.19` - linux; arm variant v7

```console
$ docker pull satosa@sha256:523c142c7c6862e72402d75c6c99136d078f1c3bff0832f307c144a87301c563
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159126183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b6e032712d5981488f40cc76e4bd93d0f28b13a6f6c3d58497260a1e5706a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Mon, 04 Mar 2024 00:18:24 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Mon, 04 Mar 2024 00:18:24 GMT
ENV SATOSA_VERSION=8.4.0
# Fri, 08 Mar 2024 16:42:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 08 Mar 2024 16:42:47 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 08 Mar 2024 16:42:48 GMT
WORKDIR /etc/satosa
# Fri, 08 Mar 2024 16:42:48 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 08 Mar 2024 16:42:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Mar 2024 16:42:49 GMT
EXPOSE 8080
# Fri, 08 Mar 2024 16:42:49 GMT
USER satosa:satosa
# Fri, 08 Mar 2024 16:42:49 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3966cfc81792baee0378a9d2d85424676e1972ac6efaf02823ead42801b9b955`  
		Last Modified: Sat, 27 Jan 2024 09:56:47 GMT  
		Size: 622.3 KB (622347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e682fb52211fcfe80358aff5f595fc49d17d84a426dfe07531a831b75feb09`  
		Last Modified: Wed, 07 Feb 2024 22:05:51 GMT  
		Size: 10.9 MB (10921342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d328ac00f385cdf1e967b3563490ef71319627a85149e04464202d4405186633`  
		Last Modified: Wed, 07 Feb 2024 22:05:49 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20df6294d50f788fb5270d7dd1a4482500cab32031d36d7054b0fe2bb9ad3388`  
		Last Modified: Wed, 07 Feb 2024 22:05:53 GMT  
		Size: 2.7 MB (2696693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993adcda16390f9d0b261707cde6cf96b2fbfaf8bb96fa54b01c4a398144f4d5`  
		Last Modified: Fri, 08 Mar 2024 16:43:14 GMT  
		Size: 9.5 MB (9468950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddad33904f84b8f1d9f9858646ed044016f91c329bf6491ddf905a4c9727f3c4`  
		Last Modified: Fri, 08 Mar 2024 16:43:40 GMT  
		Size: 132.5 MB (132485585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6125db7184428846b311e9359eea466b0f60a621909aef263d67072d417e304d`  
		Last Modified: Fri, 08 Mar 2024 16:43:11 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de92b5342a4b1431267ef2960ed4f572083b7e5e4555b301c6074c0af67e9f50`  
		Last Modified: Fri, 08 Mar 2024 16:43:11 GMT  
		Size: 2.2 KB (2154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:4003a283aad4330aff80c41290a82eb0ebffb57a34566aabee96a29175017c66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48517753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e587120d8e54fb5f41c2efd5cae962e6666bfa7c09b7e9d522f9eef79d331bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Wed, 07 Feb 2024 22:11:05 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 07 Feb 2024 22:11:05 GMT
ENV SATOSA_VERSION=8.4.0
# Wed, 07 Feb 2024 22:11:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 07 Feb 2024 22:11:33 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 07 Feb 2024 22:11:33 GMT
WORKDIR /etc/satosa
# Wed, 07 Feb 2024 22:11:34 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Wed, 07 Feb 2024 22:11:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Feb 2024 22:11:34 GMT
EXPOSE 8080
# Wed, 07 Feb 2024 22:11:34 GMT
USER satosa:satosa
# Wed, 07 Feb 2024 22:11:34 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fa4880b84a89cd734aeddf7f4553ca139e4d53722c41c54d930662c13fec8`  
		Last Modified: Sat, 27 Jan 2024 07:25:43 GMT  
		Size: 625.2 KB (625198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e7e2e0a7f3a4af923909dd104860d8fcd4d1f57bb80634083eeda0ba06e36b`  
		Last Modified: Wed, 07 Feb 2024 21:17:32 GMT  
		Size: 11.8 MB (11832383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99284986c3ffad45eb81cc0742b61e60571970e1c03d9069e0aec554fb1bc089`  
		Last Modified: Wed, 07 Feb 2024 21:17:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be93132253eb292b41ae301f69f0d47c791650c493ecd51e34ed720af01910c9`  
		Last Modified: Wed, 07 Feb 2024 21:17:31 GMT  
		Size: 2.7 MB (2696655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb40e308f00eb72552da1c91817c9bd1ee85c9cc0af8aa6b270e4ba38042daf`  
		Last Modified: Wed, 07 Feb 2024 22:12:05 GMT  
		Size: 9.7 MB (9676585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559bbf4aa424865f8954a90d5005b0a7eeb2e7f6f5cf2a650115800ae44371b`  
		Last Modified: Wed, 07 Feb 2024 22:12:07 GMT  
		Size: 20.3 MB (20326868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04661db7e0029a1b22d9c43b808257e317f876d92528b7e314a89ad81990793c`  
		Last Modified: Wed, 07 Feb 2024 22:12:04 GMT  
		Size: 10.0 KB (9960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6b843d24bf6a06297d5bfbd477d65a9ecd573ada69abf6cc16eacd553e82da`  
		Last Modified: Wed, 07 Feb 2024 22:12:04 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4-alpine3.19` - linux; 386

```console
$ docker pull satosa@sha256:391327fc04b4f25ff48fffe263ed5109d6cffec480b1e6ed9c8cd6cf3fd25a08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94656588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aba1b5dff88a26ff7c659482a828d40d8d9adc1ff13480e1cad44266f73cdeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 04:08:00 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_VERSION=3.12.1
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
CMD ["python3"]
# Sat, 27 Jan 2024 08:22:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Sat, 27 Jan 2024 08:22:45 GMT
ENV SATOSA_VERSION=8.4.0
# Sat, 27 Jan 2024 08:30:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Sat, 27 Jan 2024 08:30:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Sat, 27 Jan 2024 08:30:26 GMT
WORKDIR /etc/satosa
# Sat, 27 Jan 2024 08:30:26 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:30:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 08:30:26 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 08:30:26 GMT
USER satosa:satosa
# Sat, 27 Jan 2024 08:30:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7840a0a3a40a6b02ee9c509f8552e6bb70f9a8fb94398de1cfd742dc05d6050`  
		Last Modified: Sat, 27 Jan 2024 04:20:57 GMT  
		Size: 622.8 KB (622802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89a6fae803be2815fb73d36002db0a6aa6c6261cb6d1c568c1e00ae02507350`  
		Last Modified: Sat, 27 Jan 2024 04:21:32 GMT  
		Size: 11.9 MB (11929152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d0d6b56ec289e87c9c0271325d2cae165bad58b6190ea25e22cd8299e0c963`  
		Last Modified: Sat, 27 Jan 2024 04:21:29 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ce0078de875cf898e1a8d7656ea15eb2eace9d4a114c658313f5733402e8ba`  
		Last Modified: Sat, 27 Jan 2024 04:21:30 GMT  
		Size: 2.7 MB (2676259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e3b9a523576b9b8f6a758d4dfcd9a5ab83ba3dc460ef410e4b0be5d7f02c5d`  
		Last Modified: Sat, 27 Jan 2024 08:30:54 GMT  
		Size: 9.6 MB (9619654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc02b6f314d5143b4bc8115b6c540646f5deae4b004b585d1a15342ebf610237`  
		Last Modified: Sat, 27 Jan 2024 08:31:05 GMT  
		Size: 66.6 MB (66552282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47f30cea7d9bc3b8100a695fa9f8a41d253b16b3d39b65ec60470bbbdc52768`  
		Last Modified: Sat, 27 Jan 2024 08:30:51 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49df7ef97d6d92a9d16c8cffdfffe18e75f5e9cd3efe35eccc95aa30bc4f1f7`  
		Last Modified: Sat, 27 Jan 2024 08:30:52 GMT  
		Size: 2.1 KB (2147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4-alpine3.19` - linux; ppc64le

```console
$ docker pull satosa@sha256:eefaaf894c37cec9de82537d9844a7c6aec372efe493097fcdd99d78ceaa6bc2
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94283311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bc2d6148135e13cd1b75f30a029b33261fdcb1a5d4a90446d48e5902c57d5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 04:08:00 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_VERSION=3.12.1
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
CMD ["python3"]
# Sat, 27 Jan 2024 08:29:57 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Sat, 27 Jan 2024 08:29:58 GMT
ENV SATOSA_VERSION=8.4.0
# Sat, 27 Jan 2024 08:35:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Sat, 27 Jan 2024 08:35:40 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Sat, 27 Jan 2024 08:35:41 GMT
WORKDIR /etc/satosa
# Sat, 27 Jan 2024 08:35:41 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 08:35:42 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 08:35:43 GMT
USER satosa:satosa
# Sat, 27 Jan 2024 08:35:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d49a9cfe46131ab86b7a184f64865c97ae9d291935002bc7c38567ff27bc73`  
		Last Modified: Sat, 27 Jan 2024 06:51:52 GMT  
		Size: 625.6 KB (625581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e5feee510f8a33a7c371811dafb8bfa0914967fb6c7a516d67434cb1bbd204`  
		Last Modified: Sat, 27 Jan 2024 06:52:28 GMT  
		Size: 12.2 MB (12243607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d0977324b0b3dca506e76d3bde6f9ba583b255bb6941a1be3cbd3a73ff8e6f`  
		Last Modified: Sat, 27 Jan 2024 06:52:26 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63e83db5219c14a37c232e666d4337f900b691fb9e37066556b49fcf6223858`  
		Last Modified: Sat, 27 Jan 2024 06:52:27 GMT  
		Size: 2.7 MB (2676106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d565eb92095419ba03c37c05cab7fa100fb04315710cdd16052fdd4026e1ba`  
		Last Modified: Sat, 27 Jan 2024 08:36:06 GMT  
		Size: 9.8 MB (9801173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03bb04d932f9c6684e334ebedaabaef15c5ca10a2039fc7b092a7c560784931e`  
		Last Modified: Sat, 27 Jan 2024 08:36:14 GMT  
		Size: 65.6 MB (65566138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a082af4585697a65565659cfcf6c0f50d7db1bd8691e3ae138bf5217d4f040`  
		Last Modified: Sat, 27 Jan 2024 08:36:04 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3c70f43dc7ba65b86cf51f7fd90190c017be2d0cc2d247dc00cfb5bee93f19`  
		Last Modified: Sat, 27 Jan 2024 08:36:04 GMT  
		Size: 2.1 KB (2148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.4-bookworm`

```console
$ docker pull satosa@sha256:c81291396725ec7b05c481c9e767800f9c0a2a5886ba15963999220508cb6c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `satosa:8.4-bookworm` - linux; amd64

```console
$ docker pull satosa@sha256:5c32b82a481315407a8213fe68c5484f56208ce09c049e38d59561c73e150d58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90906882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03bfb47ed64e4c5dc1ea893114954587da90fc25a3247e4612f329469038ef9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
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
# Tue, 13 Feb 2024 15:44:32 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 15:44:32 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 15:45:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 15:45:32 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 15:45:32 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 15:45:32 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 15:45:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 15:45:32 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 15:45:32 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 15:45:32 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d1f07906b71fd60ac43c61035514996a8ad8dbfd39d4f570ac5446b064ee5d`  
		Last Modified: Tue, 13 Feb 2024 11:12:54 GMT  
		Size: 3.5 MB (3507732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3e9a37b01a92d059e8ee8ff525a84400222555e33cae231f8b1d788957450d`  
		Last Modified: Tue, 13 Feb 2024 11:13:47 GMT  
		Size: 12.0 MB (11991512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a33514831e0a3ab693884ed9b534dacd5b2c7110c64692812e78da8471d1f0b`  
		Last Modified: Tue, 13 Feb 2024 11:13:44 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959bfd25ad80f8e7023ffd4f70fd6242ee502c15f6671bd4d299d32efc40470`  
		Last Modified: Tue, 13 Feb 2024 11:13:45 GMT  
		Size: 3.0 MB (2978901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbce98668aa61c3d668392a27d1f07962a0b05246e61e0c6fdd02e9ff3b99cb`  
		Last Modified: Tue, 13 Feb 2024 15:46:04 GMT  
		Size: 22.1 MB (22131281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c2e9f06bef4f772530677cf3122ac0560bcd3f06eef8c1b2f5912840640f37`  
		Last Modified: Tue, 13 Feb 2024 15:46:04 GMT  
		Size: 21.2 MB (21161018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0149f2d2741d11c38936bd8be232ff2e6ff77eae0054a9af5021b6a01b736d0d`  
		Last Modified: Tue, 13 Feb 2024 15:46:01 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be0dac7d9ed7489cc123f4313d801f0b415a9231541a419d86ce216c05dcaa0`  
		Last Modified: Tue, 13 Feb 2024 15:46:01 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4-bookworm` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:3a68256b9eab756090fcfd6e0fb01d31474c035065ef89a46fc20a103cfb03cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89982898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a7461963f9363c0e895bb78ed23316e77c1fccaa66569858c0373a613a3da0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
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
# Tue, 12 Mar 2024 13:00:40 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 12 Mar 2024 13:00:40 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 12 Mar 2024 13:01:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 12 Mar 2024 13:01:39 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 12 Mar 2024 13:01:39 GMT
WORKDIR /etc/satosa
# Tue, 12 Mar 2024 13:01:39 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 12 Mar 2024 13:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 13:01:39 GMT
EXPOSE 8080
# Tue, 12 Mar 2024 13:01:39 GMT
USER satosa:satosa
# Tue, 12 Mar 2024 13:01:39 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55af26b7addf6c0f6fe5fed39393a1379356bb864caac1da91a0fd2fa77b911b`  
		Last Modified: Tue, 12 Mar 2024 09:46:35 GMT  
		Size: 3.3 MB (3323852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3caa3c29ca1489fb5a2119be7e582ca42dece866341d3a379b776c5b2c6362b`  
		Last Modified: Tue, 12 Mar 2024 09:47:24 GMT  
		Size: 12.0 MB (11965714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1240f83dd7d124ccb21f022464852fd5587ac77b5e6be447b86db873dc0bf6d`  
		Last Modified: Tue, 12 Mar 2024 09:47:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6318e81a3dccbefef51184e62057428961a21b0cde407673f088ee0f57417ddc`  
		Last Modified: Tue, 12 Mar 2024 09:47:23 GMT  
		Size: 3.0 MB (2979263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1b6451ffebc99e9f0ea5b7dfcb1ae02b45eca810ebc9bbada3dfc6a5005861`  
		Last Modified: Tue, 12 Mar 2024 13:02:09 GMT  
		Size: 22.0 MB (21976035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ab61321e7317b6e6d2219203156533d48070dc964baf5797c21336fd94c513`  
		Last Modified: Tue, 12 Mar 2024 13:02:09 GMT  
		Size: 20.6 MB (20569252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dab6e27ad8fb7aa4c1c72574a8ed2a1d04a5de529a450fb5605b521fe12ba6`  
		Last Modified: Tue, 12 Mar 2024 13:02:06 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf6d0d867f4ba1d51aaba9bf44b27b3936fbc500d13376e4252cdbb8826648e`  
		Last Modified: Tue, 12 Mar 2024 13:02:06 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4-bookworm` - linux; 386

```console
$ docker pull satosa@sha256:29df1f337d370235279a903eb80322eb9eec3ac134684f701bd59c93d7281437
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.7 MB (488727279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff9657cc4d63a559b1c55d0d689270b3cab3685c02704b1406c3f8d3bb27d29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:56 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Tue, 13 Feb 2024 00:38:56 GMT
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
# Tue, 13 Feb 2024 17:58:09 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 17:58:09 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 18:09:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 18:09:09 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 18:09:09 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 18:09:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 18:09:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 18:09:10 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 18:09:10 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 18:09:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18cc86e13533dd94d2b3a19bfcb8d1ebde259ebc088243e630bf43438b4bb0`  
		Last Modified: Tue, 13 Feb 2024 14:51:20 GMT  
		Size: 3.5 MB (3503117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48b2b4dedbd677d6449d91281ba20d6fe52233483171d23c4296d9fc6d8cb59`  
		Last Modified: Tue, 13 Feb 2024 14:52:23 GMT  
		Size: 12.2 MB (12239206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a65413fe49c71ab3fa6df4fdf4255039158476191db636768837f1e6e8f735`  
		Last Modified: Tue, 13 Feb 2024 14:52:20 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a42bf4645e12370533b1732e65757f2816f1497d63b7f58b12adb1f283696c3`  
		Last Modified: Tue, 13 Feb 2024 14:52:22 GMT  
		Size: 3.0 MB (2978347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2ac513cfa963fa4f372c2e074be3b84b2c51e0b44bc35cce298f09deba2abe`  
		Last Modified: Tue, 13 Feb 2024 18:22:49 GMT  
		Size: 24.2 MB (24203811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580091280836d4f1a1b351ea86e768f03371c70d1bf055b106d9206deae3f257`  
		Last Modified: Tue, 13 Feb 2024 18:23:18 GMT  
		Size: 415.6 MB (415648638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24b0ff82749ad53a37fb38644218e460b515aa025d63420ebb6c720b02ba1a1`  
		Last Modified: Tue, 13 Feb 2024 18:22:43 GMT  
		Size: 10.0 KB (9963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8ea8a78031214f83625ad937146849d4742abbf5ad497ded7e20c73e51dc3c`  
		Last Modified: Tue, 13 Feb 2024 18:22:43 GMT  
		Size: 2.1 KB (2144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4-bookworm` - linux; ppc64le

```console
$ docker pull satosa@sha256:3ca21f61a53fe5346c76ed4b9351ce8f001d671762a09a9c1107237d507d7925
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.2 MB (491195693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde9ec216fdcaf6771a71bba1c3a946c1400e738a3a3d304194b057d98b2dd5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:03 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Tue, 13 Feb 2024 00:39:05 GMT
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
# Tue, 13 Feb 2024 08:21:36 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 08:21:37 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 08:29:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 08:29:24 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 08:29:25 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 08:29:25 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 08:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 08:29:26 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 08:29:26 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 08:29:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee78f2de2777d7bd5e7363b69080bb1a6394e1cddd1fc2acaa7f608b1d129d7a`  
		Last Modified: Tue, 13 Feb 2024 03:40:38 GMT  
		Size: 3.7 MB (3704538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8cf259e5ab2eafff3461cd2b4fd546d5d20b75f29b62cd7f1efe2cb09905ff`  
		Last Modified: Tue, 13 Feb 2024 03:41:09 GMT  
		Size: 12.6 MB (12602554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7325c8b16dd117cc14e83e03632bfff7d1ff2dd5c50743012aefa3de8b7b2b15`  
		Last Modified: Tue, 13 Feb 2024 03:41:07 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b53c907fc7631d6fac41077df35d1d3a0ece736979014a24f63fa5ca967935c`  
		Last Modified: Tue, 13 Feb 2024 03:41:08 GMT  
		Size: 3.0 MB (2979477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0549feb427d838b6be46181808df359991252c393af2d1bf946f037982b6450b`  
		Last Modified: Tue, 13 Feb 2024 08:38:33 GMT  
		Size: 24.5 MB (24498861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63086daba02a48c5c956598cef502964ec2b7e522483c7ab0ce6bdec980f1ea2`  
		Last Modified: Tue, 13 Feb 2024 08:38:53 GMT  
		Size: 414.3 MB (414279010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1208cb1697601637c58f6636e02d78eb11f3c9066acc050f74644091e9ca9646`  
		Last Modified: Tue, 13 Feb 2024 08:38:29 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922bf6d55eb5cac0384856e8c65367780d6352aa0675e993301e232564115cd5`  
		Last Modified: Tue, 13 Feb 2024 08:38:29 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4-bookworm` - linux; s390x

```console
$ docker pull satosa@sha256:39a52857d3d3587a0c290bb162869643e8b9238f59ad917118de3baee91ee50d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.2 MB (498229609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83ea5fd0b8ea8f4fc660c3019bc2988cc4386e050e60fc94ae79e6ea783b2cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 01:02:37 GMT
ADD file:2dc5fd465b3cc728990229e12489d68faf8a93e6f574cacdca11cc9bf31f511d in / 
# Tue, 13 Feb 2024 01:02:39 GMT
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
# Fri, 16 Feb 2024 16:03:41 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Fri, 16 Feb 2024 16:03:42 GMT
ENV SATOSA_VERSION=8.4.0
# Fri, 16 Feb 2024 16:09:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 16 Feb 2024 16:09:18 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 16 Feb 2024 16:09:18 GMT
WORKDIR /etc/satosa
# Fri, 16 Feb 2024 16:09:18 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 16 Feb 2024 16:09:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 16:09:18 GMT
EXPOSE 8080
# Fri, 16 Feb 2024 16:09:18 GMT
USER satosa:satosa
# Fri, 16 Feb 2024 16:09:18 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e55f0b78e9a121a048a72242f0aec2a221466b10bedb873c07b73e4b99f873cb`  
		Last Modified: Tue, 13 Feb 2024 01:30:22 GMT  
		Size: 27.5 MB (27488587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3ec7775a265efbf6c384c5d18340a5650c973a50ca2d0e398efd6f07517659`  
		Last Modified: Tue, 13 Feb 2024 11:03:06 GMT  
		Size: 3.2 MB (3166462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082a41a047ff2d36ba555081aeb9a03139eab7b42242dbe438a27a94c51a2118`  
		Last Modified: Fri, 16 Feb 2024 10:40:39 GMT  
		Size: 11.9 MB (11917778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0926d163b9bf2515318962adbb6c235265efae4c566c49f626ddf024df8a42`  
		Last Modified: Fri, 16 Feb 2024 10:40:37 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf892b126232594fc63d047a9f20f7e6170f1e2a219318db54ab08bd0fc07ed`  
		Last Modified: Fri, 16 Feb 2024 10:40:38 GMT  
		Size: 3.0 MB (2978431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4ef25f44b24d50ed7297148115ca7338cfb361dc21d3f50ff822fbe72640c3`  
		Last Modified: Fri, 16 Feb 2024 16:10:46 GMT  
		Size: 23.8 MB (23798204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183d32aa11aa9166c3b9942b91e0c6928610420fb825c3040b4b013e74e74636`  
		Last Modified: Fri, 16 Feb 2024 16:11:02 GMT  
		Size: 428.9 MB (428867797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4adc9965b1ba16dd34f2892e459b028712639a3e92a446b334f71dd3dc941dd`  
		Last Modified: Fri, 16 Feb 2024 16:10:43 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5072cc9e5ef227421d9831c3f457357ca1ca7e2220f50e68b27aebee0bcf6438`  
		Last Modified: Fri, 16 Feb 2024 16:10:43 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.4.0`

```console
$ docker pull satosa@sha256:c81291396725ec7b05c481c9e767800f9c0a2a5886ba15963999220508cb6c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `satosa:8.4.0` - linux; amd64

```console
$ docker pull satosa@sha256:5c32b82a481315407a8213fe68c5484f56208ce09c049e38d59561c73e150d58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90906882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03bfb47ed64e4c5dc1ea893114954587da90fc25a3247e4612f329469038ef9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
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
# Tue, 13 Feb 2024 15:44:32 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 15:44:32 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 15:45:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 15:45:32 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 15:45:32 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 15:45:32 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 15:45:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 15:45:32 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 15:45:32 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 15:45:32 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d1f07906b71fd60ac43c61035514996a8ad8dbfd39d4f570ac5446b064ee5d`  
		Last Modified: Tue, 13 Feb 2024 11:12:54 GMT  
		Size: 3.5 MB (3507732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3e9a37b01a92d059e8ee8ff525a84400222555e33cae231f8b1d788957450d`  
		Last Modified: Tue, 13 Feb 2024 11:13:47 GMT  
		Size: 12.0 MB (11991512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a33514831e0a3ab693884ed9b534dacd5b2c7110c64692812e78da8471d1f0b`  
		Last Modified: Tue, 13 Feb 2024 11:13:44 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959bfd25ad80f8e7023ffd4f70fd6242ee502c15f6671bd4d299d32efc40470`  
		Last Modified: Tue, 13 Feb 2024 11:13:45 GMT  
		Size: 3.0 MB (2978901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbce98668aa61c3d668392a27d1f07962a0b05246e61e0c6fdd02e9ff3b99cb`  
		Last Modified: Tue, 13 Feb 2024 15:46:04 GMT  
		Size: 22.1 MB (22131281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c2e9f06bef4f772530677cf3122ac0560bcd3f06eef8c1b2f5912840640f37`  
		Last Modified: Tue, 13 Feb 2024 15:46:04 GMT  
		Size: 21.2 MB (21161018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0149f2d2741d11c38936bd8be232ff2e6ff77eae0054a9af5021b6a01b736d0d`  
		Last Modified: Tue, 13 Feb 2024 15:46:01 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be0dac7d9ed7489cc123f4313d801f0b415a9231541a419d86ce216c05dcaa0`  
		Last Modified: Tue, 13 Feb 2024 15:46:01 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4.0` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:3a68256b9eab756090fcfd6e0fb01d31474c035065ef89a46fc20a103cfb03cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89982898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a7461963f9363c0e895bb78ed23316e77c1fccaa66569858c0373a613a3da0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
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
# Tue, 12 Mar 2024 13:00:40 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 12 Mar 2024 13:00:40 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 12 Mar 2024 13:01:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 12 Mar 2024 13:01:39 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 12 Mar 2024 13:01:39 GMT
WORKDIR /etc/satosa
# Tue, 12 Mar 2024 13:01:39 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 12 Mar 2024 13:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 13:01:39 GMT
EXPOSE 8080
# Tue, 12 Mar 2024 13:01:39 GMT
USER satosa:satosa
# Tue, 12 Mar 2024 13:01:39 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55af26b7addf6c0f6fe5fed39393a1379356bb864caac1da91a0fd2fa77b911b`  
		Last Modified: Tue, 12 Mar 2024 09:46:35 GMT  
		Size: 3.3 MB (3323852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3caa3c29ca1489fb5a2119be7e582ca42dece866341d3a379b776c5b2c6362b`  
		Last Modified: Tue, 12 Mar 2024 09:47:24 GMT  
		Size: 12.0 MB (11965714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1240f83dd7d124ccb21f022464852fd5587ac77b5e6be447b86db873dc0bf6d`  
		Last Modified: Tue, 12 Mar 2024 09:47:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6318e81a3dccbefef51184e62057428961a21b0cde407673f088ee0f57417ddc`  
		Last Modified: Tue, 12 Mar 2024 09:47:23 GMT  
		Size: 3.0 MB (2979263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1b6451ffebc99e9f0ea5b7dfcb1ae02b45eca810ebc9bbada3dfc6a5005861`  
		Last Modified: Tue, 12 Mar 2024 13:02:09 GMT  
		Size: 22.0 MB (21976035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ab61321e7317b6e6d2219203156533d48070dc964baf5797c21336fd94c513`  
		Last Modified: Tue, 12 Mar 2024 13:02:09 GMT  
		Size: 20.6 MB (20569252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dab6e27ad8fb7aa4c1c72574a8ed2a1d04a5de529a450fb5605b521fe12ba6`  
		Last Modified: Tue, 12 Mar 2024 13:02:06 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf6d0d867f4ba1d51aaba9bf44b27b3936fbc500d13376e4252cdbb8826648e`  
		Last Modified: Tue, 12 Mar 2024 13:02:06 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4.0` - linux; 386

```console
$ docker pull satosa@sha256:29df1f337d370235279a903eb80322eb9eec3ac134684f701bd59c93d7281437
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.7 MB (488727279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff9657cc4d63a559b1c55d0d689270b3cab3685c02704b1406c3f8d3bb27d29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:56 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Tue, 13 Feb 2024 00:38:56 GMT
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
# Tue, 13 Feb 2024 17:58:09 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 17:58:09 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 18:09:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 18:09:09 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 18:09:09 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 18:09:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 18:09:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 18:09:10 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 18:09:10 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 18:09:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18cc86e13533dd94d2b3a19bfcb8d1ebde259ebc088243e630bf43438b4bb0`  
		Last Modified: Tue, 13 Feb 2024 14:51:20 GMT  
		Size: 3.5 MB (3503117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48b2b4dedbd677d6449d91281ba20d6fe52233483171d23c4296d9fc6d8cb59`  
		Last Modified: Tue, 13 Feb 2024 14:52:23 GMT  
		Size: 12.2 MB (12239206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a65413fe49c71ab3fa6df4fdf4255039158476191db636768837f1e6e8f735`  
		Last Modified: Tue, 13 Feb 2024 14:52:20 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a42bf4645e12370533b1732e65757f2816f1497d63b7f58b12adb1f283696c3`  
		Last Modified: Tue, 13 Feb 2024 14:52:22 GMT  
		Size: 3.0 MB (2978347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2ac513cfa963fa4f372c2e074be3b84b2c51e0b44bc35cce298f09deba2abe`  
		Last Modified: Tue, 13 Feb 2024 18:22:49 GMT  
		Size: 24.2 MB (24203811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580091280836d4f1a1b351ea86e768f03371c70d1bf055b106d9206deae3f257`  
		Last Modified: Tue, 13 Feb 2024 18:23:18 GMT  
		Size: 415.6 MB (415648638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24b0ff82749ad53a37fb38644218e460b515aa025d63420ebb6c720b02ba1a1`  
		Last Modified: Tue, 13 Feb 2024 18:22:43 GMT  
		Size: 10.0 KB (9963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8ea8a78031214f83625ad937146849d4742abbf5ad497ded7e20c73e51dc3c`  
		Last Modified: Tue, 13 Feb 2024 18:22:43 GMT  
		Size: 2.1 KB (2144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4.0` - linux; ppc64le

```console
$ docker pull satosa@sha256:3ca21f61a53fe5346c76ed4b9351ce8f001d671762a09a9c1107237d507d7925
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.2 MB (491195693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde9ec216fdcaf6771a71bba1c3a946c1400e738a3a3d304194b057d98b2dd5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:03 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Tue, 13 Feb 2024 00:39:05 GMT
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
# Tue, 13 Feb 2024 08:21:36 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 08:21:37 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 08:29:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 08:29:24 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 08:29:25 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 08:29:25 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 08:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 08:29:26 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 08:29:26 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 08:29:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee78f2de2777d7bd5e7363b69080bb1a6394e1cddd1fc2acaa7f608b1d129d7a`  
		Last Modified: Tue, 13 Feb 2024 03:40:38 GMT  
		Size: 3.7 MB (3704538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8cf259e5ab2eafff3461cd2b4fd546d5d20b75f29b62cd7f1efe2cb09905ff`  
		Last Modified: Tue, 13 Feb 2024 03:41:09 GMT  
		Size: 12.6 MB (12602554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7325c8b16dd117cc14e83e03632bfff7d1ff2dd5c50743012aefa3de8b7b2b15`  
		Last Modified: Tue, 13 Feb 2024 03:41:07 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b53c907fc7631d6fac41077df35d1d3a0ece736979014a24f63fa5ca967935c`  
		Last Modified: Tue, 13 Feb 2024 03:41:08 GMT  
		Size: 3.0 MB (2979477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0549feb427d838b6be46181808df359991252c393af2d1bf946f037982b6450b`  
		Last Modified: Tue, 13 Feb 2024 08:38:33 GMT  
		Size: 24.5 MB (24498861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63086daba02a48c5c956598cef502964ec2b7e522483c7ab0ce6bdec980f1ea2`  
		Last Modified: Tue, 13 Feb 2024 08:38:53 GMT  
		Size: 414.3 MB (414279010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1208cb1697601637c58f6636e02d78eb11f3c9066acc050f74644091e9ca9646`  
		Last Modified: Tue, 13 Feb 2024 08:38:29 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922bf6d55eb5cac0384856e8c65367780d6352aa0675e993301e232564115cd5`  
		Last Modified: Tue, 13 Feb 2024 08:38:29 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4.0` - linux; s390x

```console
$ docker pull satosa@sha256:39a52857d3d3587a0c290bb162869643e8b9238f59ad917118de3baee91ee50d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.2 MB (498229609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83ea5fd0b8ea8f4fc660c3019bc2988cc4386e050e60fc94ae79e6ea783b2cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 01:02:37 GMT
ADD file:2dc5fd465b3cc728990229e12489d68faf8a93e6f574cacdca11cc9bf31f511d in / 
# Tue, 13 Feb 2024 01:02:39 GMT
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
# Fri, 16 Feb 2024 16:03:41 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Fri, 16 Feb 2024 16:03:42 GMT
ENV SATOSA_VERSION=8.4.0
# Fri, 16 Feb 2024 16:09:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 16 Feb 2024 16:09:18 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 16 Feb 2024 16:09:18 GMT
WORKDIR /etc/satosa
# Fri, 16 Feb 2024 16:09:18 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 16 Feb 2024 16:09:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 16:09:18 GMT
EXPOSE 8080
# Fri, 16 Feb 2024 16:09:18 GMT
USER satosa:satosa
# Fri, 16 Feb 2024 16:09:18 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e55f0b78e9a121a048a72242f0aec2a221466b10bedb873c07b73e4b99f873cb`  
		Last Modified: Tue, 13 Feb 2024 01:30:22 GMT  
		Size: 27.5 MB (27488587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3ec7775a265efbf6c384c5d18340a5650c973a50ca2d0e398efd6f07517659`  
		Last Modified: Tue, 13 Feb 2024 11:03:06 GMT  
		Size: 3.2 MB (3166462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082a41a047ff2d36ba555081aeb9a03139eab7b42242dbe438a27a94c51a2118`  
		Last Modified: Fri, 16 Feb 2024 10:40:39 GMT  
		Size: 11.9 MB (11917778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0926d163b9bf2515318962adbb6c235265efae4c566c49f626ddf024df8a42`  
		Last Modified: Fri, 16 Feb 2024 10:40:37 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf892b126232594fc63d047a9f20f7e6170f1e2a219318db54ab08bd0fc07ed`  
		Last Modified: Fri, 16 Feb 2024 10:40:38 GMT  
		Size: 3.0 MB (2978431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4ef25f44b24d50ed7297148115ca7338cfb361dc21d3f50ff822fbe72640c3`  
		Last Modified: Fri, 16 Feb 2024 16:10:46 GMT  
		Size: 23.8 MB (23798204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183d32aa11aa9166c3b9942b91e0c6928610420fb825c3040b4b013e74e74636`  
		Last Modified: Fri, 16 Feb 2024 16:11:02 GMT  
		Size: 428.9 MB (428867797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4adc9965b1ba16dd34f2892e459b028712639a3e92a446b334f71dd3dc941dd`  
		Last Modified: Fri, 16 Feb 2024 16:10:43 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5072cc9e5ef227421d9831c3f457357ca1ca7e2220f50e68b27aebee0bcf6438`  
		Last Modified: Fri, 16 Feb 2024 16:10:43 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.4.0-alpine`

```console
$ docker pull satosa@sha256:d6a2f8debb3cfdc184790fb74026c2cbffd7f402a4a65ecb8e082285143d45a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `satosa:8.4.0-alpine` - linux; amd64

```console
$ docker pull satosa@sha256:b6c892a0480ef2f611608277c260c734ea8857698bd61dd64e57ac191af80a89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47166027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe054bc0129c5e7daaba60958ed19cf96cc8937a1ef76ee8b83ccbd25b90cdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Thu, 08 Feb 2024 00:28:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Thu, 08 Feb 2024 00:28:45 GMT
ENV SATOSA_VERSION=8.4.0
# Thu, 08 Feb 2024 00:29:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 08 Feb 2024 00:29:10 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 08 Feb 2024 00:29:10 GMT
WORKDIR /etc/satosa
# Thu, 08 Feb 2024 00:29:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Thu, 08 Feb 2024 00:29:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 00:29:10 GMT
EXPOSE 8080
# Thu, 08 Feb 2024 00:29:10 GMT
USER satosa:satosa
# Thu, 08 Feb 2024 00:29:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca80dc46cecdd1a97787a1dd6f74263b9d2f7b0dd3e2e15c109f5e34848c932`  
		Last Modified: Sat, 27 Jan 2024 07:51:02 GMT  
		Size: 622.1 KB (622150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9e15b6315c34de5c802bdbd343e3ec69bdc4ab870783fc1b9552daaef25e77`  
		Last Modified: Wed, 07 Feb 2024 23:45:23 GMT  
		Size: 11.8 MB (11767542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fd6f3f484fdfccf33965ca0f8807e5078a619803cf638d82bc4a405e91de04`  
		Last Modified: Wed, 07 Feb 2024 23:45:21 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc96b5c1ba465ba27fb55d4766ade8624de4082ac1530b3293ac735ab3ead50`  
		Last Modified: Wed, 07 Feb 2024 23:45:22 GMT  
		Size: 2.7 MB (2696625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7692e7a182f83cff0c00ace6108c6b19e2059f97d2d3aae2480e8eef815237`  
		Last Modified: Thu, 08 Feb 2024 00:29:42 GMT  
		Size: 7.9 MB (7879777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044eb85425384353220c085b958e1f4064080737c8be49f4fa5d4fb9fc427a4a`  
		Last Modified: Thu, 08 Feb 2024 00:29:44 GMT  
		Size: 20.8 MB (20778854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0c0a4c37ce81a2bad65869c10e4226cf2dd90d5dfccc4e9e9973166e1c790c`  
		Last Modified: Thu, 08 Feb 2024 00:29:41 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ceec51a6010f771ca188eb6a330bc23fd71249d03d2014775390fd899cf8ae`  
		Last Modified: Thu, 08 Feb 2024 00:29:41 GMT  
		Size: 2.1 KB (2147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4.0-alpine` - linux; arm variant v7

```console
$ docker pull satosa@sha256:523c142c7c6862e72402d75c6c99136d078f1c3bff0832f307c144a87301c563
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159126183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b6e032712d5981488f40cc76e4bd93d0f28b13a6f6c3d58497260a1e5706a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Mon, 04 Mar 2024 00:18:24 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Mon, 04 Mar 2024 00:18:24 GMT
ENV SATOSA_VERSION=8.4.0
# Fri, 08 Mar 2024 16:42:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 08 Mar 2024 16:42:47 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 08 Mar 2024 16:42:48 GMT
WORKDIR /etc/satosa
# Fri, 08 Mar 2024 16:42:48 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 08 Mar 2024 16:42:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Mar 2024 16:42:49 GMT
EXPOSE 8080
# Fri, 08 Mar 2024 16:42:49 GMT
USER satosa:satosa
# Fri, 08 Mar 2024 16:42:49 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3966cfc81792baee0378a9d2d85424676e1972ac6efaf02823ead42801b9b955`  
		Last Modified: Sat, 27 Jan 2024 09:56:47 GMT  
		Size: 622.3 KB (622347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e682fb52211fcfe80358aff5f595fc49d17d84a426dfe07531a831b75feb09`  
		Last Modified: Wed, 07 Feb 2024 22:05:51 GMT  
		Size: 10.9 MB (10921342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d328ac00f385cdf1e967b3563490ef71319627a85149e04464202d4405186633`  
		Last Modified: Wed, 07 Feb 2024 22:05:49 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20df6294d50f788fb5270d7dd1a4482500cab32031d36d7054b0fe2bb9ad3388`  
		Last Modified: Wed, 07 Feb 2024 22:05:53 GMT  
		Size: 2.7 MB (2696693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993adcda16390f9d0b261707cde6cf96b2fbfaf8bb96fa54b01c4a398144f4d5`  
		Last Modified: Fri, 08 Mar 2024 16:43:14 GMT  
		Size: 9.5 MB (9468950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddad33904f84b8f1d9f9858646ed044016f91c329bf6491ddf905a4c9727f3c4`  
		Last Modified: Fri, 08 Mar 2024 16:43:40 GMT  
		Size: 132.5 MB (132485585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6125db7184428846b311e9359eea466b0f60a621909aef263d67072d417e304d`  
		Last Modified: Fri, 08 Mar 2024 16:43:11 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de92b5342a4b1431267ef2960ed4f572083b7e5e4555b301c6074c0af67e9f50`  
		Last Modified: Fri, 08 Mar 2024 16:43:11 GMT  
		Size: 2.2 KB (2154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4.0-alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:4003a283aad4330aff80c41290a82eb0ebffb57a34566aabee96a29175017c66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48517753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e587120d8e54fb5f41c2efd5cae962e6666bfa7c09b7e9d522f9eef79d331bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Wed, 07 Feb 2024 22:11:05 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 07 Feb 2024 22:11:05 GMT
ENV SATOSA_VERSION=8.4.0
# Wed, 07 Feb 2024 22:11:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 07 Feb 2024 22:11:33 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 07 Feb 2024 22:11:33 GMT
WORKDIR /etc/satosa
# Wed, 07 Feb 2024 22:11:34 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Wed, 07 Feb 2024 22:11:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Feb 2024 22:11:34 GMT
EXPOSE 8080
# Wed, 07 Feb 2024 22:11:34 GMT
USER satosa:satosa
# Wed, 07 Feb 2024 22:11:34 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fa4880b84a89cd734aeddf7f4553ca139e4d53722c41c54d930662c13fec8`  
		Last Modified: Sat, 27 Jan 2024 07:25:43 GMT  
		Size: 625.2 KB (625198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e7e2e0a7f3a4af923909dd104860d8fcd4d1f57bb80634083eeda0ba06e36b`  
		Last Modified: Wed, 07 Feb 2024 21:17:32 GMT  
		Size: 11.8 MB (11832383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99284986c3ffad45eb81cc0742b61e60571970e1c03d9069e0aec554fb1bc089`  
		Last Modified: Wed, 07 Feb 2024 21:17:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be93132253eb292b41ae301f69f0d47c791650c493ecd51e34ed720af01910c9`  
		Last Modified: Wed, 07 Feb 2024 21:17:31 GMT  
		Size: 2.7 MB (2696655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb40e308f00eb72552da1c91817c9bd1ee85c9cc0af8aa6b270e4ba38042daf`  
		Last Modified: Wed, 07 Feb 2024 22:12:05 GMT  
		Size: 9.7 MB (9676585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559bbf4aa424865f8954a90d5005b0a7eeb2e7f6f5cf2a650115800ae44371b`  
		Last Modified: Wed, 07 Feb 2024 22:12:07 GMT  
		Size: 20.3 MB (20326868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04661db7e0029a1b22d9c43b808257e317f876d92528b7e314a89ad81990793c`  
		Last Modified: Wed, 07 Feb 2024 22:12:04 GMT  
		Size: 10.0 KB (9960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6b843d24bf6a06297d5bfbd477d65a9ecd573ada69abf6cc16eacd553e82da`  
		Last Modified: Wed, 07 Feb 2024 22:12:04 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4.0-alpine` - linux; 386

```console
$ docker pull satosa@sha256:391327fc04b4f25ff48fffe263ed5109d6cffec480b1e6ed9c8cd6cf3fd25a08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94656588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aba1b5dff88a26ff7c659482a828d40d8d9adc1ff13480e1cad44266f73cdeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 04:08:00 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_VERSION=3.12.1
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
CMD ["python3"]
# Sat, 27 Jan 2024 08:22:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Sat, 27 Jan 2024 08:22:45 GMT
ENV SATOSA_VERSION=8.4.0
# Sat, 27 Jan 2024 08:30:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Sat, 27 Jan 2024 08:30:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Sat, 27 Jan 2024 08:30:26 GMT
WORKDIR /etc/satosa
# Sat, 27 Jan 2024 08:30:26 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:30:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 08:30:26 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 08:30:26 GMT
USER satosa:satosa
# Sat, 27 Jan 2024 08:30:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7840a0a3a40a6b02ee9c509f8552e6bb70f9a8fb94398de1cfd742dc05d6050`  
		Last Modified: Sat, 27 Jan 2024 04:20:57 GMT  
		Size: 622.8 KB (622802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89a6fae803be2815fb73d36002db0a6aa6c6261cb6d1c568c1e00ae02507350`  
		Last Modified: Sat, 27 Jan 2024 04:21:32 GMT  
		Size: 11.9 MB (11929152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d0d6b56ec289e87c9c0271325d2cae165bad58b6190ea25e22cd8299e0c963`  
		Last Modified: Sat, 27 Jan 2024 04:21:29 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ce0078de875cf898e1a8d7656ea15eb2eace9d4a114c658313f5733402e8ba`  
		Last Modified: Sat, 27 Jan 2024 04:21:30 GMT  
		Size: 2.7 MB (2676259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e3b9a523576b9b8f6a758d4dfcd9a5ab83ba3dc460ef410e4b0be5d7f02c5d`  
		Last Modified: Sat, 27 Jan 2024 08:30:54 GMT  
		Size: 9.6 MB (9619654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc02b6f314d5143b4bc8115b6c540646f5deae4b004b585d1a15342ebf610237`  
		Last Modified: Sat, 27 Jan 2024 08:31:05 GMT  
		Size: 66.6 MB (66552282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47f30cea7d9bc3b8100a695fa9f8a41d253b16b3d39b65ec60470bbbdc52768`  
		Last Modified: Sat, 27 Jan 2024 08:30:51 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49df7ef97d6d92a9d16c8cffdfffe18e75f5e9cd3efe35eccc95aa30bc4f1f7`  
		Last Modified: Sat, 27 Jan 2024 08:30:52 GMT  
		Size: 2.1 KB (2147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4.0-alpine` - linux; ppc64le

```console
$ docker pull satosa@sha256:eefaaf894c37cec9de82537d9844a7c6aec372efe493097fcdd99d78ceaa6bc2
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94283311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bc2d6148135e13cd1b75f30a029b33261fdcb1a5d4a90446d48e5902c57d5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 04:08:00 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_VERSION=3.12.1
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
CMD ["python3"]
# Sat, 27 Jan 2024 08:29:57 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Sat, 27 Jan 2024 08:29:58 GMT
ENV SATOSA_VERSION=8.4.0
# Sat, 27 Jan 2024 08:35:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Sat, 27 Jan 2024 08:35:40 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Sat, 27 Jan 2024 08:35:41 GMT
WORKDIR /etc/satosa
# Sat, 27 Jan 2024 08:35:41 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 08:35:42 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 08:35:43 GMT
USER satosa:satosa
# Sat, 27 Jan 2024 08:35:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d49a9cfe46131ab86b7a184f64865c97ae9d291935002bc7c38567ff27bc73`  
		Last Modified: Sat, 27 Jan 2024 06:51:52 GMT  
		Size: 625.6 KB (625581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e5feee510f8a33a7c371811dafb8bfa0914967fb6c7a516d67434cb1bbd204`  
		Last Modified: Sat, 27 Jan 2024 06:52:28 GMT  
		Size: 12.2 MB (12243607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d0977324b0b3dca506e76d3bde6f9ba583b255bb6941a1be3cbd3a73ff8e6f`  
		Last Modified: Sat, 27 Jan 2024 06:52:26 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63e83db5219c14a37c232e666d4337f900b691fb9e37066556b49fcf6223858`  
		Last Modified: Sat, 27 Jan 2024 06:52:27 GMT  
		Size: 2.7 MB (2676106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d565eb92095419ba03c37c05cab7fa100fb04315710cdd16052fdd4026e1ba`  
		Last Modified: Sat, 27 Jan 2024 08:36:06 GMT  
		Size: 9.8 MB (9801173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03bb04d932f9c6684e334ebedaabaef15c5ca10a2039fc7b092a7c560784931e`  
		Last Modified: Sat, 27 Jan 2024 08:36:14 GMT  
		Size: 65.6 MB (65566138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a082af4585697a65565659cfcf6c0f50d7db1bd8691e3ae138bf5217d4f040`  
		Last Modified: Sat, 27 Jan 2024 08:36:04 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3c70f43dc7ba65b86cf51f7fd90190c017be2d0cc2d247dc00cfb5bee93f19`  
		Last Modified: Sat, 27 Jan 2024 08:36:04 GMT  
		Size: 2.1 KB (2148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.4.0-alpine3.19`

```console
$ docker pull satosa@sha256:d6a2f8debb3cfdc184790fb74026c2cbffd7f402a4a65ecb8e082285143d45a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `satosa:8.4.0-alpine3.19` - linux; amd64

```console
$ docker pull satosa@sha256:b6c892a0480ef2f611608277c260c734ea8857698bd61dd64e57ac191af80a89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47166027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe054bc0129c5e7daaba60958ed19cf96cc8937a1ef76ee8b83ccbd25b90cdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Thu, 08 Feb 2024 00:28:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Thu, 08 Feb 2024 00:28:45 GMT
ENV SATOSA_VERSION=8.4.0
# Thu, 08 Feb 2024 00:29:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 08 Feb 2024 00:29:10 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 08 Feb 2024 00:29:10 GMT
WORKDIR /etc/satosa
# Thu, 08 Feb 2024 00:29:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Thu, 08 Feb 2024 00:29:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 00:29:10 GMT
EXPOSE 8080
# Thu, 08 Feb 2024 00:29:10 GMT
USER satosa:satosa
# Thu, 08 Feb 2024 00:29:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca80dc46cecdd1a97787a1dd6f74263b9d2f7b0dd3e2e15c109f5e34848c932`  
		Last Modified: Sat, 27 Jan 2024 07:51:02 GMT  
		Size: 622.1 KB (622150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9e15b6315c34de5c802bdbd343e3ec69bdc4ab870783fc1b9552daaef25e77`  
		Last Modified: Wed, 07 Feb 2024 23:45:23 GMT  
		Size: 11.8 MB (11767542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fd6f3f484fdfccf33965ca0f8807e5078a619803cf638d82bc4a405e91de04`  
		Last Modified: Wed, 07 Feb 2024 23:45:21 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc96b5c1ba465ba27fb55d4766ade8624de4082ac1530b3293ac735ab3ead50`  
		Last Modified: Wed, 07 Feb 2024 23:45:22 GMT  
		Size: 2.7 MB (2696625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7692e7a182f83cff0c00ace6108c6b19e2059f97d2d3aae2480e8eef815237`  
		Last Modified: Thu, 08 Feb 2024 00:29:42 GMT  
		Size: 7.9 MB (7879777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044eb85425384353220c085b958e1f4064080737c8be49f4fa5d4fb9fc427a4a`  
		Last Modified: Thu, 08 Feb 2024 00:29:44 GMT  
		Size: 20.8 MB (20778854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0c0a4c37ce81a2bad65869c10e4226cf2dd90d5dfccc4e9e9973166e1c790c`  
		Last Modified: Thu, 08 Feb 2024 00:29:41 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ceec51a6010f771ca188eb6a330bc23fd71249d03d2014775390fd899cf8ae`  
		Last Modified: Thu, 08 Feb 2024 00:29:41 GMT  
		Size: 2.1 KB (2147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4.0-alpine3.19` - linux; arm variant v7

```console
$ docker pull satosa@sha256:523c142c7c6862e72402d75c6c99136d078f1c3bff0832f307c144a87301c563
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159126183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b6e032712d5981488f40cc76e4bd93d0f28b13a6f6c3d58497260a1e5706a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Mon, 04 Mar 2024 00:18:24 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Mon, 04 Mar 2024 00:18:24 GMT
ENV SATOSA_VERSION=8.4.0
# Fri, 08 Mar 2024 16:42:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 08 Mar 2024 16:42:47 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 08 Mar 2024 16:42:48 GMT
WORKDIR /etc/satosa
# Fri, 08 Mar 2024 16:42:48 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 08 Mar 2024 16:42:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Mar 2024 16:42:49 GMT
EXPOSE 8080
# Fri, 08 Mar 2024 16:42:49 GMT
USER satosa:satosa
# Fri, 08 Mar 2024 16:42:49 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3966cfc81792baee0378a9d2d85424676e1972ac6efaf02823ead42801b9b955`  
		Last Modified: Sat, 27 Jan 2024 09:56:47 GMT  
		Size: 622.3 KB (622347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e682fb52211fcfe80358aff5f595fc49d17d84a426dfe07531a831b75feb09`  
		Last Modified: Wed, 07 Feb 2024 22:05:51 GMT  
		Size: 10.9 MB (10921342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d328ac00f385cdf1e967b3563490ef71319627a85149e04464202d4405186633`  
		Last Modified: Wed, 07 Feb 2024 22:05:49 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20df6294d50f788fb5270d7dd1a4482500cab32031d36d7054b0fe2bb9ad3388`  
		Last Modified: Wed, 07 Feb 2024 22:05:53 GMT  
		Size: 2.7 MB (2696693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993adcda16390f9d0b261707cde6cf96b2fbfaf8bb96fa54b01c4a398144f4d5`  
		Last Modified: Fri, 08 Mar 2024 16:43:14 GMT  
		Size: 9.5 MB (9468950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddad33904f84b8f1d9f9858646ed044016f91c329bf6491ddf905a4c9727f3c4`  
		Last Modified: Fri, 08 Mar 2024 16:43:40 GMT  
		Size: 132.5 MB (132485585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6125db7184428846b311e9359eea466b0f60a621909aef263d67072d417e304d`  
		Last Modified: Fri, 08 Mar 2024 16:43:11 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de92b5342a4b1431267ef2960ed4f572083b7e5e4555b301c6074c0af67e9f50`  
		Last Modified: Fri, 08 Mar 2024 16:43:11 GMT  
		Size: 2.2 KB (2154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4.0-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:4003a283aad4330aff80c41290a82eb0ebffb57a34566aabee96a29175017c66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48517753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e587120d8e54fb5f41c2efd5cae962e6666bfa7c09b7e9d522f9eef79d331bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Wed, 07 Feb 2024 22:11:05 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 07 Feb 2024 22:11:05 GMT
ENV SATOSA_VERSION=8.4.0
# Wed, 07 Feb 2024 22:11:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 07 Feb 2024 22:11:33 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 07 Feb 2024 22:11:33 GMT
WORKDIR /etc/satosa
# Wed, 07 Feb 2024 22:11:34 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Wed, 07 Feb 2024 22:11:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Feb 2024 22:11:34 GMT
EXPOSE 8080
# Wed, 07 Feb 2024 22:11:34 GMT
USER satosa:satosa
# Wed, 07 Feb 2024 22:11:34 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fa4880b84a89cd734aeddf7f4553ca139e4d53722c41c54d930662c13fec8`  
		Last Modified: Sat, 27 Jan 2024 07:25:43 GMT  
		Size: 625.2 KB (625198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e7e2e0a7f3a4af923909dd104860d8fcd4d1f57bb80634083eeda0ba06e36b`  
		Last Modified: Wed, 07 Feb 2024 21:17:32 GMT  
		Size: 11.8 MB (11832383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99284986c3ffad45eb81cc0742b61e60571970e1c03d9069e0aec554fb1bc089`  
		Last Modified: Wed, 07 Feb 2024 21:17:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be93132253eb292b41ae301f69f0d47c791650c493ecd51e34ed720af01910c9`  
		Last Modified: Wed, 07 Feb 2024 21:17:31 GMT  
		Size: 2.7 MB (2696655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb40e308f00eb72552da1c91817c9bd1ee85c9cc0af8aa6b270e4ba38042daf`  
		Last Modified: Wed, 07 Feb 2024 22:12:05 GMT  
		Size: 9.7 MB (9676585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559bbf4aa424865f8954a90d5005b0a7eeb2e7f6f5cf2a650115800ae44371b`  
		Last Modified: Wed, 07 Feb 2024 22:12:07 GMT  
		Size: 20.3 MB (20326868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04661db7e0029a1b22d9c43b808257e317f876d92528b7e314a89ad81990793c`  
		Last Modified: Wed, 07 Feb 2024 22:12:04 GMT  
		Size: 10.0 KB (9960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6b843d24bf6a06297d5bfbd477d65a9ecd573ada69abf6cc16eacd553e82da`  
		Last Modified: Wed, 07 Feb 2024 22:12:04 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4.0-alpine3.19` - linux; 386

```console
$ docker pull satosa@sha256:391327fc04b4f25ff48fffe263ed5109d6cffec480b1e6ed9c8cd6cf3fd25a08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94656588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aba1b5dff88a26ff7c659482a828d40d8d9adc1ff13480e1cad44266f73cdeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 04:08:00 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_VERSION=3.12.1
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
CMD ["python3"]
# Sat, 27 Jan 2024 08:22:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Sat, 27 Jan 2024 08:22:45 GMT
ENV SATOSA_VERSION=8.4.0
# Sat, 27 Jan 2024 08:30:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Sat, 27 Jan 2024 08:30:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Sat, 27 Jan 2024 08:30:26 GMT
WORKDIR /etc/satosa
# Sat, 27 Jan 2024 08:30:26 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:30:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 08:30:26 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 08:30:26 GMT
USER satosa:satosa
# Sat, 27 Jan 2024 08:30:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7840a0a3a40a6b02ee9c509f8552e6bb70f9a8fb94398de1cfd742dc05d6050`  
		Last Modified: Sat, 27 Jan 2024 04:20:57 GMT  
		Size: 622.8 KB (622802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89a6fae803be2815fb73d36002db0a6aa6c6261cb6d1c568c1e00ae02507350`  
		Last Modified: Sat, 27 Jan 2024 04:21:32 GMT  
		Size: 11.9 MB (11929152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d0d6b56ec289e87c9c0271325d2cae165bad58b6190ea25e22cd8299e0c963`  
		Last Modified: Sat, 27 Jan 2024 04:21:29 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ce0078de875cf898e1a8d7656ea15eb2eace9d4a114c658313f5733402e8ba`  
		Last Modified: Sat, 27 Jan 2024 04:21:30 GMT  
		Size: 2.7 MB (2676259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e3b9a523576b9b8f6a758d4dfcd9a5ab83ba3dc460ef410e4b0be5d7f02c5d`  
		Last Modified: Sat, 27 Jan 2024 08:30:54 GMT  
		Size: 9.6 MB (9619654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc02b6f314d5143b4bc8115b6c540646f5deae4b004b585d1a15342ebf610237`  
		Last Modified: Sat, 27 Jan 2024 08:31:05 GMT  
		Size: 66.6 MB (66552282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47f30cea7d9bc3b8100a695fa9f8a41d253b16b3d39b65ec60470bbbdc52768`  
		Last Modified: Sat, 27 Jan 2024 08:30:51 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49df7ef97d6d92a9d16c8cffdfffe18e75f5e9cd3efe35eccc95aa30bc4f1f7`  
		Last Modified: Sat, 27 Jan 2024 08:30:52 GMT  
		Size: 2.1 KB (2147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4.0-alpine3.19` - linux; ppc64le

```console
$ docker pull satosa@sha256:eefaaf894c37cec9de82537d9844a7c6aec372efe493097fcdd99d78ceaa6bc2
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94283311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bc2d6148135e13cd1b75f30a029b33261fdcb1a5d4a90446d48e5902c57d5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 04:08:00 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_VERSION=3.12.1
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
CMD ["python3"]
# Sat, 27 Jan 2024 08:29:57 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Sat, 27 Jan 2024 08:29:58 GMT
ENV SATOSA_VERSION=8.4.0
# Sat, 27 Jan 2024 08:35:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Sat, 27 Jan 2024 08:35:40 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Sat, 27 Jan 2024 08:35:41 GMT
WORKDIR /etc/satosa
# Sat, 27 Jan 2024 08:35:41 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 08:35:42 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 08:35:43 GMT
USER satosa:satosa
# Sat, 27 Jan 2024 08:35:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d49a9cfe46131ab86b7a184f64865c97ae9d291935002bc7c38567ff27bc73`  
		Last Modified: Sat, 27 Jan 2024 06:51:52 GMT  
		Size: 625.6 KB (625581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e5feee510f8a33a7c371811dafb8bfa0914967fb6c7a516d67434cb1bbd204`  
		Last Modified: Sat, 27 Jan 2024 06:52:28 GMT  
		Size: 12.2 MB (12243607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d0977324b0b3dca506e76d3bde6f9ba583b255bb6941a1be3cbd3a73ff8e6f`  
		Last Modified: Sat, 27 Jan 2024 06:52:26 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63e83db5219c14a37c232e666d4337f900b691fb9e37066556b49fcf6223858`  
		Last Modified: Sat, 27 Jan 2024 06:52:27 GMT  
		Size: 2.7 MB (2676106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d565eb92095419ba03c37c05cab7fa100fb04315710cdd16052fdd4026e1ba`  
		Last Modified: Sat, 27 Jan 2024 08:36:06 GMT  
		Size: 9.8 MB (9801173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03bb04d932f9c6684e334ebedaabaef15c5ca10a2039fc7b092a7c560784931e`  
		Last Modified: Sat, 27 Jan 2024 08:36:14 GMT  
		Size: 65.6 MB (65566138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a082af4585697a65565659cfcf6c0f50d7db1bd8691e3ae138bf5217d4f040`  
		Last Modified: Sat, 27 Jan 2024 08:36:04 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3c70f43dc7ba65b86cf51f7fd90190c017be2d0cc2d247dc00cfb5bee93f19`  
		Last Modified: Sat, 27 Jan 2024 08:36:04 GMT  
		Size: 2.1 KB (2148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:8.4.0-bookworm`

```console
$ docker pull satosa@sha256:c81291396725ec7b05c481c9e767800f9c0a2a5886ba15963999220508cb6c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `satosa:8.4.0-bookworm` - linux; amd64

```console
$ docker pull satosa@sha256:5c32b82a481315407a8213fe68c5484f56208ce09c049e38d59561c73e150d58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90906882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03bfb47ed64e4c5dc1ea893114954587da90fc25a3247e4612f329469038ef9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
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
# Tue, 13 Feb 2024 15:44:32 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 15:44:32 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 15:45:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 15:45:32 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 15:45:32 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 15:45:32 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 15:45:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 15:45:32 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 15:45:32 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 15:45:32 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d1f07906b71fd60ac43c61035514996a8ad8dbfd39d4f570ac5446b064ee5d`  
		Last Modified: Tue, 13 Feb 2024 11:12:54 GMT  
		Size: 3.5 MB (3507732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3e9a37b01a92d059e8ee8ff525a84400222555e33cae231f8b1d788957450d`  
		Last Modified: Tue, 13 Feb 2024 11:13:47 GMT  
		Size: 12.0 MB (11991512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a33514831e0a3ab693884ed9b534dacd5b2c7110c64692812e78da8471d1f0b`  
		Last Modified: Tue, 13 Feb 2024 11:13:44 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959bfd25ad80f8e7023ffd4f70fd6242ee502c15f6671bd4d299d32efc40470`  
		Last Modified: Tue, 13 Feb 2024 11:13:45 GMT  
		Size: 3.0 MB (2978901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbce98668aa61c3d668392a27d1f07962a0b05246e61e0c6fdd02e9ff3b99cb`  
		Last Modified: Tue, 13 Feb 2024 15:46:04 GMT  
		Size: 22.1 MB (22131281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c2e9f06bef4f772530677cf3122ac0560bcd3f06eef8c1b2f5912840640f37`  
		Last Modified: Tue, 13 Feb 2024 15:46:04 GMT  
		Size: 21.2 MB (21161018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0149f2d2741d11c38936bd8be232ff2e6ff77eae0054a9af5021b6a01b736d0d`  
		Last Modified: Tue, 13 Feb 2024 15:46:01 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be0dac7d9ed7489cc123f4313d801f0b415a9231541a419d86ce216c05dcaa0`  
		Last Modified: Tue, 13 Feb 2024 15:46:01 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:3a68256b9eab756090fcfd6e0fb01d31474c035065ef89a46fc20a103cfb03cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89982898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a7461963f9363c0e895bb78ed23316e77c1fccaa66569858c0373a613a3da0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
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
# Tue, 12 Mar 2024 13:00:40 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 12 Mar 2024 13:00:40 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 12 Mar 2024 13:01:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 12 Mar 2024 13:01:39 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 12 Mar 2024 13:01:39 GMT
WORKDIR /etc/satosa
# Tue, 12 Mar 2024 13:01:39 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 12 Mar 2024 13:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 13:01:39 GMT
EXPOSE 8080
# Tue, 12 Mar 2024 13:01:39 GMT
USER satosa:satosa
# Tue, 12 Mar 2024 13:01:39 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55af26b7addf6c0f6fe5fed39393a1379356bb864caac1da91a0fd2fa77b911b`  
		Last Modified: Tue, 12 Mar 2024 09:46:35 GMT  
		Size: 3.3 MB (3323852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3caa3c29ca1489fb5a2119be7e582ca42dece866341d3a379b776c5b2c6362b`  
		Last Modified: Tue, 12 Mar 2024 09:47:24 GMT  
		Size: 12.0 MB (11965714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1240f83dd7d124ccb21f022464852fd5587ac77b5e6be447b86db873dc0bf6d`  
		Last Modified: Tue, 12 Mar 2024 09:47:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6318e81a3dccbefef51184e62057428961a21b0cde407673f088ee0f57417ddc`  
		Last Modified: Tue, 12 Mar 2024 09:47:23 GMT  
		Size: 3.0 MB (2979263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1b6451ffebc99e9f0ea5b7dfcb1ae02b45eca810ebc9bbada3dfc6a5005861`  
		Last Modified: Tue, 12 Mar 2024 13:02:09 GMT  
		Size: 22.0 MB (21976035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ab61321e7317b6e6d2219203156533d48070dc964baf5797c21336fd94c513`  
		Last Modified: Tue, 12 Mar 2024 13:02:09 GMT  
		Size: 20.6 MB (20569252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dab6e27ad8fb7aa4c1c72574a8ed2a1d04a5de529a450fb5605b521fe12ba6`  
		Last Modified: Tue, 12 Mar 2024 13:02:06 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf6d0d867f4ba1d51aaba9bf44b27b3936fbc500d13376e4252cdbb8826648e`  
		Last Modified: Tue, 12 Mar 2024 13:02:06 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4.0-bookworm` - linux; 386

```console
$ docker pull satosa@sha256:29df1f337d370235279a903eb80322eb9eec3ac134684f701bd59c93d7281437
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.7 MB (488727279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff9657cc4d63a559b1c55d0d689270b3cab3685c02704b1406c3f8d3bb27d29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:56 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Tue, 13 Feb 2024 00:38:56 GMT
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
# Tue, 13 Feb 2024 17:58:09 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 17:58:09 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 18:09:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 18:09:09 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 18:09:09 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 18:09:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 18:09:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 18:09:10 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 18:09:10 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 18:09:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18cc86e13533dd94d2b3a19bfcb8d1ebde259ebc088243e630bf43438b4bb0`  
		Last Modified: Tue, 13 Feb 2024 14:51:20 GMT  
		Size: 3.5 MB (3503117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48b2b4dedbd677d6449d91281ba20d6fe52233483171d23c4296d9fc6d8cb59`  
		Last Modified: Tue, 13 Feb 2024 14:52:23 GMT  
		Size: 12.2 MB (12239206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a65413fe49c71ab3fa6df4fdf4255039158476191db636768837f1e6e8f735`  
		Last Modified: Tue, 13 Feb 2024 14:52:20 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a42bf4645e12370533b1732e65757f2816f1497d63b7f58b12adb1f283696c3`  
		Last Modified: Tue, 13 Feb 2024 14:52:22 GMT  
		Size: 3.0 MB (2978347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2ac513cfa963fa4f372c2e074be3b84b2c51e0b44bc35cce298f09deba2abe`  
		Last Modified: Tue, 13 Feb 2024 18:22:49 GMT  
		Size: 24.2 MB (24203811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580091280836d4f1a1b351ea86e768f03371c70d1bf055b106d9206deae3f257`  
		Last Modified: Tue, 13 Feb 2024 18:23:18 GMT  
		Size: 415.6 MB (415648638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24b0ff82749ad53a37fb38644218e460b515aa025d63420ebb6c720b02ba1a1`  
		Last Modified: Tue, 13 Feb 2024 18:22:43 GMT  
		Size: 10.0 KB (9963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8ea8a78031214f83625ad937146849d4742abbf5ad497ded7e20c73e51dc3c`  
		Last Modified: Tue, 13 Feb 2024 18:22:43 GMT  
		Size: 2.1 KB (2144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4.0-bookworm` - linux; ppc64le

```console
$ docker pull satosa@sha256:3ca21f61a53fe5346c76ed4b9351ce8f001d671762a09a9c1107237d507d7925
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.2 MB (491195693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde9ec216fdcaf6771a71bba1c3a946c1400e738a3a3d304194b057d98b2dd5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:03 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Tue, 13 Feb 2024 00:39:05 GMT
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
# Tue, 13 Feb 2024 08:21:36 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 08:21:37 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 08:29:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 08:29:24 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 08:29:25 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 08:29:25 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 08:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 08:29:26 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 08:29:26 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 08:29:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee78f2de2777d7bd5e7363b69080bb1a6394e1cddd1fc2acaa7f608b1d129d7a`  
		Last Modified: Tue, 13 Feb 2024 03:40:38 GMT  
		Size: 3.7 MB (3704538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8cf259e5ab2eafff3461cd2b4fd546d5d20b75f29b62cd7f1efe2cb09905ff`  
		Last Modified: Tue, 13 Feb 2024 03:41:09 GMT  
		Size: 12.6 MB (12602554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7325c8b16dd117cc14e83e03632bfff7d1ff2dd5c50743012aefa3de8b7b2b15`  
		Last Modified: Tue, 13 Feb 2024 03:41:07 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b53c907fc7631d6fac41077df35d1d3a0ece736979014a24f63fa5ca967935c`  
		Last Modified: Tue, 13 Feb 2024 03:41:08 GMT  
		Size: 3.0 MB (2979477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0549feb427d838b6be46181808df359991252c393af2d1bf946f037982b6450b`  
		Last Modified: Tue, 13 Feb 2024 08:38:33 GMT  
		Size: 24.5 MB (24498861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63086daba02a48c5c956598cef502964ec2b7e522483c7ab0ce6bdec980f1ea2`  
		Last Modified: Tue, 13 Feb 2024 08:38:53 GMT  
		Size: 414.3 MB (414279010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1208cb1697601637c58f6636e02d78eb11f3c9066acc050f74644091e9ca9646`  
		Last Modified: Tue, 13 Feb 2024 08:38:29 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922bf6d55eb5cac0384856e8c65367780d6352aa0675e993301e232564115cd5`  
		Last Modified: Tue, 13 Feb 2024 08:38:29 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8.4.0-bookworm` - linux; s390x

```console
$ docker pull satosa@sha256:39a52857d3d3587a0c290bb162869643e8b9238f59ad917118de3baee91ee50d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.2 MB (498229609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83ea5fd0b8ea8f4fc660c3019bc2988cc4386e050e60fc94ae79e6ea783b2cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 01:02:37 GMT
ADD file:2dc5fd465b3cc728990229e12489d68faf8a93e6f574cacdca11cc9bf31f511d in / 
# Tue, 13 Feb 2024 01:02:39 GMT
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
# Fri, 16 Feb 2024 16:03:41 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Fri, 16 Feb 2024 16:03:42 GMT
ENV SATOSA_VERSION=8.4.0
# Fri, 16 Feb 2024 16:09:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 16 Feb 2024 16:09:18 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 16 Feb 2024 16:09:18 GMT
WORKDIR /etc/satosa
# Fri, 16 Feb 2024 16:09:18 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 16 Feb 2024 16:09:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 16:09:18 GMT
EXPOSE 8080
# Fri, 16 Feb 2024 16:09:18 GMT
USER satosa:satosa
# Fri, 16 Feb 2024 16:09:18 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e55f0b78e9a121a048a72242f0aec2a221466b10bedb873c07b73e4b99f873cb`  
		Last Modified: Tue, 13 Feb 2024 01:30:22 GMT  
		Size: 27.5 MB (27488587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3ec7775a265efbf6c384c5d18340a5650c973a50ca2d0e398efd6f07517659`  
		Last Modified: Tue, 13 Feb 2024 11:03:06 GMT  
		Size: 3.2 MB (3166462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082a41a047ff2d36ba555081aeb9a03139eab7b42242dbe438a27a94c51a2118`  
		Last Modified: Fri, 16 Feb 2024 10:40:39 GMT  
		Size: 11.9 MB (11917778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0926d163b9bf2515318962adbb6c235265efae4c566c49f626ddf024df8a42`  
		Last Modified: Fri, 16 Feb 2024 10:40:37 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf892b126232594fc63d047a9f20f7e6170f1e2a219318db54ab08bd0fc07ed`  
		Last Modified: Fri, 16 Feb 2024 10:40:38 GMT  
		Size: 3.0 MB (2978431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4ef25f44b24d50ed7297148115ca7338cfb361dc21d3f50ff822fbe72640c3`  
		Last Modified: Fri, 16 Feb 2024 16:10:46 GMT  
		Size: 23.8 MB (23798204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183d32aa11aa9166c3b9942b91e0c6928610420fb825c3040b4b013e74e74636`  
		Last Modified: Fri, 16 Feb 2024 16:11:02 GMT  
		Size: 428.9 MB (428867797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4adc9965b1ba16dd34f2892e459b028712639a3e92a446b334f71dd3dc941dd`  
		Last Modified: Fri, 16 Feb 2024 16:10:43 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5072cc9e5ef227421d9831c3f457357ca1ca7e2220f50e68b27aebee0bcf6438`  
		Last Modified: Fri, 16 Feb 2024 16:10:43 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:alpine`

```console
$ docker pull satosa@sha256:5e04caa7a7fd5dfc0e33118b403522944985089b3dc8d3876ca7ee0bffb32d3b
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
$ docker pull satosa@sha256:b6c892a0480ef2f611608277c260c734ea8857698bd61dd64e57ac191af80a89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47166027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe054bc0129c5e7daaba60958ed19cf96cc8937a1ef76ee8b83ccbd25b90cdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Thu, 08 Feb 2024 00:28:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Thu, 08 Feb 2024 00:28:45 GMT
ENV SATOSA_VERSION=8.4.0
# Thu, 08 Feb 2024 00:29:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 08 Feb 2024 00:29:10 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 08 Feb 2024 00:29:10 GMT
WORKDIR /etc/satosa
# Thu, 08 Feb 2024 00:29:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Thu, 08 Feb 2024 00:29:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 00:29:10 GMT
EXPOSE 8080
# Thu, 08 Feb 2024 00:29:10 GMT
USER satosa:satosa
# Thu, 08 Feb 2024 00:29:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca80dc46cecdd1a97787a1dd6f74263b9d2f7b0dd3e2e15c109f5e34848c932`  
		Last Modified: Sat, 27 Jan 2024 07:51:02 GMT  
		Size: 622.1 KB (622150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9e15b6315c34de5c802bdbd343e3ec69bdc4ab870783fc1b9552daaef25e77`  
		Last Modified: Wed, 07 Feb 2024 23:45:23 GMT  
		Size: 11.8 MB (11767542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fd6f3f484fdfccf33965ca0f8807e5078a619803cf638d82bc4a405e91de04`  
		Last Modified: Wed, 07 Feb 2024 23:45:21 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc96b5c1ba465ba27fb55d4766ade8624de4082ac1530b3293ac735ab3ead50`  
		Last Modified: Wed, 07 Feb 2024 23:45:22 GMT  
		Size: 2.7 MB (2696625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7692e7a182f83cff0c00ace6108c6b19e2059f97d2d3aae2480e8eef815237`  
		Last Modified: Thu, 08 Feb 2024 00:29:42 GMT  
		Size: 7.9 MB (7879777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044eb85425384353220c085b958e1f4064080737c8be49f4fa5d4fb9fc427a4a`  
		Last Modified: Thu, 08 Feb 2024 00:29:44 GMT  
		Size: 20.8 MB (20778854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0c0a4c37ce81a2bad65869c10e4226cf2dd90d5dfccc4e9e9973166e1c790c`  
		Last Modified: Thu, 08 Feb 2024 00:29:41 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ceec51a6010f771ca188eb6a330bc23fd71249d03d2014775390fd899cf8ae`  
		Last Modified: Thu, 08 Feb 2024 00:29:41 GMT  
		Size: 2.1 KB (2147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine` - linux; arm variant v6

```console
$ docker pull satosa@sha256:6eb26239e3f9b4f3d182f3a818f91a427134bee51751e0f46a6d7de705c33a28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262100685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806505b83e27f9e7f96da15ce2aec80efe8e44c3206249270279451344a92dd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:11 GMT
ADD file:c5e68ad58a515830d33f20488adffa6af47be2e332543c747b8931cab7444e59 in / 
# Wed, 29 Mar 2023 18:01:11 GMT
CMD ["/bin/sh"]
# Fri, 28 Apr 2023 22:20:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Apr 2023 22:20:40 GMT
ENV LANG=C.UTF-8
# Fri, 28 Apr 2023 22:20:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 28 Apr 2023 22:20:40 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 28 Apr 2023 22:20:40 GMT
ENV PYTHON_VERSION=3.11.3
# Fri, 28 Apr 2023 22:20:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Fri, 28 Apr 2023 22:20:40 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 28 Apr 2023 22:20:40 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Fri, 28 Apr 2023 22:20:40 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 28 Apr 2023 22:20:40 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/0d8570dc44796f4369b652222cf176b3db6ac70e/public/get-pip.py
# Fri, 28 Apr 2023 22:20:40 GMT
ENV PYTHON_GET_PIP_SHA256=96461deced5c2a487ddc65207ec5a9cffeca0d34e7af7ea1afc470ff0d746207
# Fri, 28 Apr 2023 22:20:40 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 28 Apr 2023 22:20:40 GMT
CMD ["python3"]
# Wed, 03 May 2023 01:44:34 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 May 2023 01:44:34 GMT
ENV SATOSA_VERSION=8.2.0
# Wed, 03 May 2023 01:48:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 May 2023 01:49:00 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 May 2023 01:49:00 GMT
WORKDIR /etc/satosa
# Wed, 03 May 2023 01:49:00 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Wed, 03 May 2023 01:49:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 May 2023 01:49:00 GMT
EXPOSE 8080
# Wed, 03 May 2023 01:49:00 GMT
USER satosa:satosa
# Wed, 03 May 2023 01:49:00 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:c4ddbcc13e08e4ef30f810d8afad41fd6994bd8af7d37746d0ea33d8813968fc`  
		Last Modified: Wed, 29 Mar 2023 18:02:04 GMT  
		Size: 2.6 MB (2616846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385377f5c7fdca5ac838685a95def9e8aa4e3fc5a54fda0bae559ae380f7bfb0`  
		Last Modified: Thu, 06 Apr 2023 00:52:56 GMT  
		Size: 666.1 KB (666102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a062a5dc92b567459a8985a9e708c4bdc4f57c647e619977213dba804c1337`  
		Last Modified: Wed, 03 May 2023 01:19:15 GMT  
		Size: 12.2 MB (12205002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de762052920e8d43b210da3385a6cc976e95f5e5fd3af778181fd8895e3da6f`  
		Last Modified: Wed, 03 May 2023 01:19:12 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddfc182f71d9bff7e6d143bea83e1b862220afbb3047c6db2e86027488ff4f4`  
		Last Modified: Wed, 03 May 2023 01:19:14 GMT  
		Size: 3.1 MB (3080436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cde56b6e08c62bde1a810ff349fd49055f567e82dbe397cf7d0543407a9bc3d`  
		Last Modified: Wed, 03 May 2023 01:49:21 GMT  
		Size: 9.8 MB (9792828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197a17b73bc0684ab6bd86cc5fe3498a1a7a7bd83ba298778a064fe323b9d528`  
		Last Modified: Wed, 03 May 2023 01:49:49 GMT  
		Size: 233.7 MB (233727590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8e3b6b13f0dce1e02f922841fb64cf4f2096f1ccfdd3eab8e3b1efca7b2096`  
		Last Modified: Wed, 03 May 2023 01:49:19 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f38952b8a1e8b828b7d1bf9e2daba56ecb11ebb727d63d0ba14d1893ce7fb1`  
		Last Modified: Wed, 03 May 2023 01:49:19 GMT  
		Size: 2.1 KB (2147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine` - linux; arm variant v7

```console
$ docker pull satosa@sha256:523c142c7c6862e72402d75c6c99136d078f1c3bff0832f307c144a87301c563
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159126183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b6e032712d5981488f40cc76e4bd93d0f28b13a6f6c3d58497260a1e5706a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Mon, 04 Mar 2024 00:18:24 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Mon, 04 Mar 2024 00:18:24 GMT
ENV SATOSA_VERSION=8.4.0
# Fri, 08 Mar 2024 16:42:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 08 Mar 2024 16:42:47 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 08 Mar 2024 16:42:48 GMT
WORKDIR /etc/satosa
# Fri, 08 Mar 2024 16:42:48 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 08 Mar 2024 16:42:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Mar 2024 16:42:49 GMT
EXPOSE 8080
# Fri, 08 Mar 2024 16:42:49 GMT
USER satosa:satosa
# Fri, 08 Mar 2024 16:42:49 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3966cfc81792baee0378a9d2d85424676e1972ac6efaf02823ead42801b9b955`  
		Last Modified: Sat, 27 Jan 2024 09:56:47 GMT  
		Size: 622.3 KB (622347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e682fb52211fcfe80358aff5f595fc49d17d84a426dfe07531a831b75feb09`  
		Last Modified: Wed, 07 Feb 2024 22:05:51 GMT  
		Size: 10.9 MB (10921342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d328ac00f385cdf1e967b3563490ef71319627a85149e04464202d4405186633`  
		Last Modified: Wed, 07 Feb 2024 22:05:49 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20df6294d50f788fb5270d7dd1a4482500cab32031d36d7054b0fe2bb9ad3388`  
		Last Modified: Wed, 07 Feb 2024 22:05:53 GMT  
		Size: 2.7 MB (2696693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993adcda16390f9d0b261707cde6cf96b2fbfaf8bb96fa54b01c4a398144f4d5`  
		Last Modified: Fri, 08 Mar 2024 16:43:14 GMT  
		Size: 9.5 MB (9468950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddad33904f84b8f1d9f9858646ed044016f91c329bf6491ddf905a4c9727f3c4`  
		Last Modified: Fri, 08 Mar 2024 16:43:40 GMT  
		Size: 132.5 MB (132485585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6125db7184428846b311e9359eea466b0f60a621909aef263d67072d417e304d`  
		Last Modified: Fri, 08 Mar 2024 16:43:11 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de92b5342a4b1431267ef2960ed4f572083b7e5e4555b301c6074c0af67e9f50`  
		Last Modified: Fri, 08 Mar 2024 16:43:11 GMT  
		Size: 2.2 KB (2154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:4003a283aad4330aff80c41290a82eb0ebffb57a34566aabee96a29175017c66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48517753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e587120d8e54fb5f41c2efd5cae962e6666bfa7c09b7e9d522f9eef79d331bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Wed, 07 Feb 2024 22:11:05 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 07 Feb 2024 22:11:05 GMT
ENV SATOSA_VERSION=8.4.0
# Wed, 07 Feb 2024 22:11:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 07 Feb 2024 22:11:33 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 07 Feb 2024 22:11:33 GMT
WORKDIR /etc/satosa
# Wed, 07 Feb 2024 22:11:34 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Wed, 07 Feb 2024 22:11:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Feb 2024 22:11:34 GMT
EXPOSE 8080
# Wed, 07 Feb 2024 22:11:34 GMT
USER satosa:satosa
# Wed, 07 Feb 2024 22:11:34 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fa4880b84a89cd734aeddf7f4553ca139e4d53722c41c54d930662c13fec8`  
		Last Modified: Sat, 27 Jan 2024 07:25:43 GMT  
		Size: 625.2 KB (625198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e7e2e0a7f3a4af923909dd104860d8fcd4d1f57bb80634083eeda0ba06e36b`  
		Last Modified: Wed, 07 Feb 2024 21:17:32 GMT  
		Size: 11.8 MB (11832383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99284986c3ffad45eb81cc0742b61e60571970e1c03d9069e0aec554fb1bc089`  
		Last Modified: Wed, 07 Feb 2024 21:17:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be93132253eb292b41ae301f69f0d47c791650c493ecd51e34ed720af01910c9`  
		Last Modified: Wed, 07 Feb 2024 21:17:31 GMT  
		Size: 2.7 MB (2696655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb40e308f00eb72552da1c91817c9bd1ee85c9cc0af8aa6b270e4ba38042daf`  
		Last Modified: Wed, 07 Feb 2024 22:12:05 GMT  
		Size: 9.7 MB (9676585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559bbf4aa424865f8954a90d5005b0a7eeb2e7f6f5cf2a650115800ae44371b`  
		Last Modified: Wed, 07 Feb 2024 22:12:07 GMT  
		Size: 20.3 MB (20326868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04661db7e0029a1b22d9c43b808257e317f876d92528b7e314a89ad81990793c`  
		Last Modified: Wed, 07 Feb 2024 22:12:04 GMT  
		Size: 10.0 KB (9960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6b843d24bf6a06297d5bfbd477d65a9ecd573ada69abf6cc16eacd553e82da`  
		Last Modified: Wed, 07 Feb 2024 22:12:04 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine` - linux; 386

```console
$ docker pull satosa@sha256:391327fc04b4f25ff48fffe263ed5109d6cffec480b1e6ed9c8cd6cf3fd25a08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94656588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aba1b5dff88a26ff7c659482a828d40d8d9adc1ff13480e1cad44266f73cdeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 04:08:00 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_VERSION=3.12.1
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
CMD ["python3"]
# Sat, 27 Jan 2024 08:22:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Sat, 27 Jan 2024 08:22:45 GMT
ENV SATOSA_VERSION=8.4.0
# Sat, 27 Jan 2024 08:30:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Sat, 27 Jan 2024 08:30:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Sat, 27 Jan 2024 08:30:26 GMT
WORKDIR /etc/satosa
# Sat, 27 Jan 2024 08:30:26 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:30:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 08:30:26 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 08:30:26 GMT
USER satosa:satosa
# Sat, 27 Jan 2024 08:30:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7840a0a3a40a6b02ee9c509f8552e6bb70f9a8fb94398de1cfd742dc05d6050`  
		Last Modified: Sat, 27 Jan 2024 04:20:57 GMT  
		Size: 622.8 KB (622802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89a6fae803be2815fb73d36002db0a6aa6c6261cb6d1c568c1e00ae02507350`  
		Last Modified: Sat, 27 Jan 2024 04:21:32 GMT  
		Size: 11.9 MB (11929152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d0d6b56ec289e87c9c0271325d2cae165bad58b6190ea25e22cd8299e0c963`  
		Last Modified: Sat, 27 Jan 2024 04:21:29 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ce0078de875cf898e1a8d7656ea15eb2eace9d4a114c658313f5733402e8ba`  
		Last Modified: Sat, 27 Jan 2024 04:21:30 GMT  
		Size: 2.7 MB (2676259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e3b9a523576b9b8f6a758d4dfcd9a5ab83ba3dc460ef410e4b0be5d7f02c5d`  
		Last Modified: Sat, 27 Jan 2024 08:30:54 GMT  
		Size: 9.6 MB (9619654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc02b6f314d5143b4bc8115b6c540646f5deae4b004b585d1a15342ebf610237`  
		Last Modified: Sat, 27 Jan 2024 08:31:05 GMT  
		Size: 66.6 MB (66552282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47f30cea7d9bc3b8100a695fa9f8a41d253b16b3d39b65ec60470bbbdc52768`  
		Last Modified: Sat, 27 Jan 2024 08:30:51 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49df7ef97d6d92a9d16c8cffdfffe18e75f5e9cd3efe35eccc95aa30bc4f1f7`  
		Last Modified: Sat, 27 Jan 2024 08:30:52 GMT  
		Size: 2.1 KB (2147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine` - linux; ppc64le

```console
$ docker pull satosa@sha256:eefaaf894c37cec9de82537d9844a7c6aec372efe493097fcdd99d78ceaa6bc2
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94283311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bc2d6148135e13cd1b75f30a029b33261fdcb1a5d4a90446d48e5902c57d5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 04:08:00 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_VERSION=3.12.1
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
CMD ["python3"]
# Sat, 27 Jan 2024 08:29:57 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Sat, 27 Jan 2024 08:29:58 GMT
ENV SATOSA_VERSION=8.4.0
# Sat, 27 Jan 2024 08:35:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Sat, 27 Jan 2024 08:35:40 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Sat, 27 Jan 2024 08:35:41 GMT
WORKDIR /etc/satosa
# Sat, 27 Jan 2024 08:35:41 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 08:35:42 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 08:35:43 GMT
USER satosa:satosa
# Sat, 27 Jan 2024 08:35:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d49a9cfe46131ab86b7a184f64865c97ae9d291935002bc7c38567ff27bc73`  
		Last Modified: Sat, 27 Jan 2024 06:51:52 GMT  
		Size: 625.6 KB (625581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e5feee510f8a33a7c371811dafb8bfa0914967fb6c7a516d67434cb1bbd204`  
		Last Modified: Sat, 27 Jan 2024 06:52:28 GMT  
		Size: 12.2 MB (12243607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d0977324b0b3dca506e76d3bde6f9ba583b255bb6941a1be3cbd3a73ff8e6f`  
		Last Modified: Sat, 27 Jan 2024 06:52:26 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63e83db5219c14a37c232e666d4337f900b691fb9e37066556b49fcf6223858`  
		Last Modified: Sat, 27 Jan 2024 06:52:27 GMT  
		Size: 2.7 MB (2676106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d565eb92095419ba03c37c05cab7fa100fb04315710cdd16052fdd4026e1ba`  
		Last Modified: Sat, 27 Jan 2024 08:36:06 GMT  
		Size: 9.8 MB (9801173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03bb04d932f9c6684e334ebedaabaef15c5ca10a2039fc7b092a7c560784931e`  
		Last Modified: Sat, 27 Jan 2024 08:36:14 GMT  
		Size: 65.6 MB (65566138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a082af4585697a65565659cfcf6c0f50d7db1bd8691e3ae138bf5217d4f040`  
		Last Modified: Sat, 27 Jan 2024 08:36:04 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3c70f43dc7ba65b86cf51f7fd90190c017be2d0cc2d247dc00cfb5bee93f19`  
		Last Modified: Sat, 27 Jan 2024 08:36:04 GMT  
		Size: 2.1 KB (2148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:alpine3.19`

```console
$ docker pull satosa@sha256:d6a2f8debb3cfdc184790fb74026c2cbffd7f402a4a65ecb8e082285143d45a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `satosa:alpine3.19` - linux; amd64

```console
$ docker pull satosa@sha256:b6c892a0480ef2f611608277c260c734ea8857698bd61dd64e57ac191af80a89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47166027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe054bc0129c5e7daaba60958ed19cf96cc8937a1ef76ee8b83ccbd25b90cdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Thu, 08 Feb 2024 00:28:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Thu, 08 Feb 2024 00:28:45 GMT
ENV SATOSA_VERSION=8.4.0
# Thu, 08 Feb 2024 00:29:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 08 Feb 2024 00:29:10 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 08 Feb 2024 00:29:10 GMT
WORKDIR /etc/satosa
# Thu, 08 Feb 2024 00:29:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Thu, 08 Feb 2024 00:29:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 00:29:10 GMT
EXPOSE 8080
# Thu, 08 Feb 2024 00:29:10 GMT
USER satosa:satosa
# Thu, 08 Feb 2024 00:29:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca80dc46cecdd1a97787a1dd6f74263b9d2f7b0dd3e2e15c109f5e34848c932`  
		Last Modified: Sat, 27 Jan 2024 07:51:02 GMT  
		Size: 622.1 KB (622150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9e15b6315c34de5c802bdbd343e3ec69bdc4ab870783fc1b9552daaef25e77`  
		Last Modified: Wed, 07 Feb 2024 23:45:23 GMT  
		Size: 11.8 MB (11767542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fd6f3f484fdfccf33965ca0f8807e5078a619803cf638d82bc4a405e91de04`  
		Last Modified: Wed, 07 Feb 2024 23:45:21 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc96b5c1ba465ba27fb55d4766ade8624de4082ac1530b3293ac735ab3ead50`  
		Last Modified: Wed, 07 Feb 2024 23:45:22 GMT  
		Size: 2.7 MB (2696625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7692e7a182f83cff0c00ace6108c6b19e2059f97d2d3aae2480e8eef815237`  
		Last Modified: Thu, 08 Feb 2024 00:29:42 GMT  
		Size: 7.9 MB (7879777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044eb85425384353220c085b958e1f4064080737c8be49f4fa5d4fb9fc427a4a`  
		Last Modified: Thu, 08 Feb 2024 00:29:44 GMT  
		Size: 20.8 MB (20778854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0c0a4c37ce81a2bad65869c10e4226cf2dd90d5dfccc4e9e9973166e1c790c`  
		Last Modified: Thu, 08 Feb 2024 00:29:41 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ceec51a6010f771ca188eb6a330bc23fd71249d03d2014775390fd899cf8ae`  
		Last Modified: Thu, 08 Feb 2024 00:29:41 GMT  
		Size: 2.1 KB (2147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine3.19` - linux; arm variant v7

```console
$ docker pull satosa@sha256:523c142c7c6862e72402d75c6c99136d078f1c3bff0832f307c144a87301c563
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159126183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b6e032712d5981488f40cc76e4bd93d0f28b13a6f6c3d58497260a1e5706a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Mon, 04 Mar 2024 00:18:24 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Mon, 04 Mar 2024 00:18:24 GMT
ENV SATOSA_VERSION=8.4.0
# Fri, 08 Mar 2024 16:42:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 08 Mar 2024 16:42:47 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 08 Mar 2024 16:42:48 GMT
WORKDIR /etc/satosa
# Fri, 08 Mar 2024 16:42:48 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 08 Mar 2024 16:42:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Mar 2024 16:42:49 GMT
EXPOSE 8080
# Fri, 08 Mar 2024 16:42:49 GMT
USER satosa:satosa
# Fri, 08 Mar 2024 16:42:49 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3966cfc81792baee0378a9d2d85424676e1972ac6efaf02823ead42801b9b955`  
		Last Modified: Sat, 27 Jan 2024 09:56:47 GMT  
		Size: 622.3 KB (622347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e682fb52211fcfe80358aff5f595fc49d17d84a426dfe07531a831b75feb09`  
		Last Modified: Wed, 07 Feb 2024 22:05:51 GMT  
		Size: 10.9 MB (10921342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d328ac00f385cdf1e967b3563490ef71319627a85149e04464202d4405186633`  
		Last Modified: Wed, 07 Feb 2024 22:05:49 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20df6294d50f788fb5270d7dd1a4482500cab32031d36d7054b0fe2bb9ad3388`  
		Last Modified: Wed, 07 Feb 2024 22:05:53 GMT  
		Size: 2.7 MB (2696693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993adcda16390f9d0b261707cde6cf96b2fbfaf8bb96fa54b01c4a398144f4d5`  
		Last Modified: Fri, 08 Mar 2024 16:43:14 GMT  
		Size: 9.5 MB (9468950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddad33904f84b8f1d9f9858646ed044016f91c329bf6491ddf905a4c9727f3c4`  
		Last Modified: Fri, 08 Mar 2024 16:43:40 GMT  
		Size: 132.5 MB (132485585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6125db7184428846b311e9359eea466b0f60a621909aef263d67072d417e304d`  
		Last Modified: Fri, 08 Mar 2024 16:43:11 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de92b5342a4b1431267ef2960ed4f572083b7e5e4555b301c6074c0af67e9f50`  
		Last Modified: Fri, 08 Mar 2024 16:43:11 GMT  
		Size: 2.2 KB (2154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:4003a283aad4330aff80c41290a82eb0ebffb57a34566aabee96a29175017c66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48517753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e587120d8e54fb5f41c2efd5cae962e6666bfa7c09b7e9d522f9eef79d331bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 06:43:27 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_VERSION=3.12.2
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 07 Feb 2024 06:43:27 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 07 Feb 2024 06:43:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Feb 2024 06:43:27 GMT
CMD ["python3"]
# Wed, 07 Feb 2024 22:11:05 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 07 Feb 2024 22:11:05 GMT
ENV SATOSA_VERSION=8.4.0
# Wed, 07 Feb 2024 22:11:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 07 Feb 2024 22:11:33 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 07 Feb 2024 22:11:33 GMT
WORKDIR /etc/satosa
# Wed, 07 Feb 2024 22:11:34 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Wed, 07 Feb 2024 22:11:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Feb 2024 22:11:34 GMT
EXPOSE 8080
# Wed, 07 Feb 2024 22:11:34 GMT
USER satosa:satosa
# Wed, 07 Feb 2024 22:11:34 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fa4880b84a89cd734aeddf7f4553ca139e4d53722c41c54d930662c13fec8`  
		Last Modified: Sat, 27 Jan 2024 07:25:43 GMT  
		Size: 625.2 KB (625198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e7e2e0a7f3a4af923909dd104860d8fcd4d1f57bb80634083eeda0ba06e36b`  
		Last Modified: Wed, 07 Feb 2024 21:17:32 GMT  
		Size: 11.8 MB (11832383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99284986c3ffad45eb81cc0742b61e60571970e1c03d9069e0aec554fb1bc089`  
		Last Modified: Wed, 07 Feb 2024 21:17:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be93132253eb292b41ae301f69f0d47c791650c493ecd51e34ed720af01910c9`  
		Last Modified: Wed, 07 Feb 2024 21:17:31 GMT  
		Size: 2.7 MB (2696655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb40e308f00eb72552da1c91817c9bd1ee85c9cc0af8aa6b270e4ba38042daf`  
		Last Modified: Wed, 07 Feb 2024 22:12:05 GMT  
		Size: 9.7 MB (9676585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559bbf4aa424865f8954a90d5005b0a7eeb2e7f6f5cf2a650115800ae44371b`  
		Last Modified: Wed, 07 Feb 2024 22:12:07 GMT  
		Size: 20.3 MB (20326868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04661db7e0029a1b22d9c43b808257e317f876d92528b7e314a89ad81990793c`  
		Last Modified: Wed, 07 Feb 2024 22:12:04 GMT  
		Size: 10.0 KB (9960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6b843d24bf6a06297d5bfbd477d65a9ecd573ada69abf6cc16eacd553e82da`  
		Last Modified: Wed, 07 Feb 2024 22:12:04 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine3.19` - linux; 386

```console
$ docker pull satosa@sha256:391327fc04b4f25ff48fffe263ed5109d6cffec480b1e6ed9c8cd6cf3fd25a08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94656588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aba1b5dff88a26ff7c659482a828d40d8d9adc1ff13480e1cad44266f73cdeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 04:08:00 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_VERSION=3.12.1
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
CMD ["python3"]
# Sat, 27 Jan 2024 08:22:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Sat, 27 Jan 2024 08:22:45 GMT
ENV SATOSA_VERSION=8.4.0
# Sat, 27 Jan 2024 08:30:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Sat, 27 Jan 2024 08:30:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Sat, 27 Jan 2024 08:30:26 GMT
WORKDIR /etc/satosa
# Sat, 27 Jan 2024 08:30:26 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:30:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 08:30:26 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 08:30:26 GMT
USER satosa:satosa
# Sat, 27 Jan 2024 08:30:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7840a0a3a40a6b02ee9c509f8552e6bb70f9a8fb94398de1cfd742dc05d6050`  
		Last Modified: Sat, 27 Jan 2024 04:20:57 GMT  
		Size: 622.8 KB (622802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89a6fae803be2815fb73d36002db0a6aa6c6261cb6d1c568c1e00ae02507350`  
		Last Modified: Sat, 27 Jan 2024 04:21:32 GMT  
		Size: 11.9 MB (11929152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d0d6b56ec289e87c9c0271325d2cae165bad58b6190ea25e22cd8299e0c963`  
		Last Modified: Sat, 27 Jan 2024 04:21:29 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ce0078de875cf898e1a8d7656ea15eb2eace9d4a114c658313f5733402e8ba`  
		Last Modified: Sat, 27 Jan 2024 04:21:30 GMT  
		Size: 2.7 MB (2676259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e3b9a523576b9b8f6a758d4dfcd9a5ab83ba3dc460ef410e4b0be5d7f02c5d`  
		Last Modified: Sat, 27 Jan 2024 08:30:54 GMT  
		Size: 9.6 MB (9619654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc02b6f314d5143b4bc8115b6c540646f5deae4b004b585d1a15342ebf610237`  
		Last Modified: Sat, 27 Jan 2024 08:31:05 GMT  
		Size: 66.6 MB (66552282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47f30cea7d9bc3b8100a695fa9f8a41d253b16b3d39b65ec60470bbbdc52768`  
		Last Modified: Sat, 27 Jan 2024 08:30:51 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49df7ef97d6d92a9d16c8cffdfffe18e75f5e9cd3efe35eccc95aa30bc4f1f7`  
		Last Modified: Sat, 27 Jan 2024 08:30:52 GMT  
		Size: 2.1 KB (2147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:alpine3.19` - linux; ppc64le

```console
$ docker pull satosa@sha256:eefaaf894c37cec9de82537d9844a7c6aec372efe493097fcdd99d78ceaa6bc2
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94283311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bc2d6148135e13cd1b75f30a029b33261fdcb1a5d4a90446d48e5902c57d5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 04:08:00 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_VERSION=3.12.1
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Wed, 20 Dec 2023 04:08:00 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Wed, 20 Dec 2023 04:08:00 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 20 Dec 2023 04:08:00 GMT
CMD ["python3"]
# Sat, 27 Jan 2024 08:29:57 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Sat, 27 Jan 2024 08:29:58 GMT
ENV SATOSA_VERSION=8.4.0
# Sat, 27 Jan 2024 08:35:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Sat, 27 Jan 2024 08:35:40 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Sat, 27 Jan 2024 08:35:41 GMT
WORKDIR /etc/satosa
# Sat, 27 Jan 2024 08:35:41 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 08:35:42 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 08:35:43 GMT
USER satosa:satosa
# Sat, 27 Jan 2024 08:35:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d49a9cfe46131ab86b7a184f64865c97ae9d291935002bc7c38567ff27bc73`  
		Last Modified: Sat, 27 Jan 2024 06:51:52 GMT  
		Size: 625.6 KB (625581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e5feee510f8a33a7c371811dafb8bfa0914967fb6c7a516d67434cb1bbd204`  
		Last Modified: Sat, 27 Jan 2024 06:52:28 GMT  
		Size: 12.2 MB (12243607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d0977324b0b3dca506e76d3bde6f9ba583b255bb6941a1be3cbd3a73ff8e6f`  
		Last Modified: Sat, 27 Jan 2024 06:52:26 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63e83db5219c14a37c232e666d4337f900b691fb9e37066556b49fcf6223858`  
		Last Modified: Sat, 27 Jan 2024 06:52:27 GMT  
		Size: 2.7 MB (2676106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d565eb92095419ba03c37c05cab7fa100fb04315710cdd16052fdd4026e1ba`  
		Last Modified: Sat, 27 Jan 2024 08:36:06 GMT  
		Size: 9.8 MB (9801173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03bb04d932f9c6684e334ebedaabaef15c5ca10a2039fc7b092a7c560784931e`  
		Last Modified: Sat, 27 Jan 2024 08:36:14 GMT  
		Size: 65.6 MB (65566138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a082af4585697a65565659cfcf6c0f50d7db1bd8691e3ae138bf5217d4f040`  
		Last Modified: Sat, 27 Jan 2024 08:36:04 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3c70f43dc7ba65b86cf51f7fd90190c017be2d0cc2d247dc00cfb5bee93f19`  
		Last Modified: Sat, 27 Jan 2024 08:36:04 GMT  
		Size: 2.1 KB (2148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:bookworm`

```console
$ docker pull satosa@sha256:c81291396725ec7b05c481c9e767800f9c0a2a5886ba15963999220508cb6c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `satosa:bookworm` - linux; amd64

```console
$ docker pull satosa@sha256:5c32b82a481315407a8213fe68c5484f56208ce09c049e38d59561c73e150d58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90906882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03bfb47ed64e4c5dc1ea893114954587da90fc25a3247e4612f329469038ef9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
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
# Tue, 13 Feb 2024 15:44:32 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 15:44:32 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 15:45:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 15:45:32 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 15:45:32 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 15:45:32 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 15:45:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 15:45:32 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 15:45:32 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 15:45:32 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d1f07906b71fd60ac43c61035514996a8ad8dbfd39d4f570ac5446b064ee5d`  
		Last Modified: Tue, 13 Feb 2024 11:12:54 GMT  
		Size: 3.5 MB (3507732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3e9a37b01a92d059e8ee8ff525a84400222555e33cae231f8b1d788957450d`  
		Last Modified: Tue, 13 Feb 2024 11:13:47 GMT  
		Size: 12.0 MB (11991512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a33514831e0a3ab693884ed9b534dacd5b2c7110c64692812e78da8471d1f0b`  
		Last Modified: Tue, 13 Feb 2024 11:13:44 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959bfd25ad80f8e7023ffd4f70fd6242ee502c15f6671bd4d299d32efc40470`  
		Last Modified: Tue, 13 Feb 2024 11:13:45 GMT  
		Size: 3.0 MB (2978901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbce98668aa61c3d668392a27d1f07962a0b05246e61e0c6fdd02e9ff3b99cb`  
		Last Modified: Tue, 13 Feb 2024 15:46:04 GMT  
		Size: 22.1 MB (22131281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c2e9f06bef4f772530677cf3122ac0560bcd3f06eef8c1b2f5912840640f37`  
		Last Modified: Tue, 13 Feb 2024 15:46:04 GMT  
		Size: 21.2 MB (21161018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0149f2d2741d11c38936bd8be232ff2e6ff77eae0054a9af5021b6a01b736d0d`  
		Last Modified: Tue, 13 Feb 2024 15:46:01 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be0dac7d9ed7489cc123f4313d801f0b415a9231541a419d86ce216c05dcaa0`  
		Last Modified: Tue, 13 Feb 2024 15:46:01 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:bookworm` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:3a68256b9eab756090fcfd6e0fb01d31474c035065ef89a46fc20a103cfb03cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89982898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a7461963f9363c0e895bb78ed23316e77c1fccaa66569858c0373a613a3da0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
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
# Tue, 12 Mar 2024 13:00:40 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 12 Mar 2024 13:00:40 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 12 Mar 2024 13:01:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 12 Mar 2024 13:01:39 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 12 Mar 2024 13:01:39 GMT
WORKDIR /etc/satosa
# Tue, 12 Mar 2024 13:01:39 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 12 Mar 2024 13:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 13:01:39 GMT
EXPOSE 8080
# Tue, 12 Mar 2024 13:01:39 GMT
USER satosa:satosa
# Tue, 12 Mar 2024 13:01:39 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55af26b7addf6c0f6fe5fed39393a1379356bb864caac1da91a0fd2fa77b911b`  
		Last Modified: Tue, 12 Mar 2024 09:46:35 GMT  
		Size: 3.3 MB (3323852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3caa3c29ca1489fb5a2119be7e582ca42dece866341d3a379b776c5b2c6362b`  
		Last Modified: Tue, 12 Mar 2024 09:47:24 GMT  
		Size: 12.0 MB (11965714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1240f83dd7d124ccb21f022464852fd5587ac77b5e6be447b86db873dc0bf6d`  
		Last Modified: Tue, 12 Mar 2024 09:47:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6318e81a3dccbefef51184e62057428961a21b0cde407673f088ee0f57417ddc`  
		Last Modified: Tue, 12 Mar 2024 09:47:23 GMT  
		Size: 3.0 MB (2979263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1b6451ffebc99e9f0ea5b7dfcb1ae02b45eca810ebc9bbada3dfc6a5005861`  
		Last Modified: Tue, 12 Mar 2024 13:02:09 GMT  
		Size: 22.0 MB (21976035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ab61321e7317b6e6d2219203156533d48070dc964baf5797c21336fd94c513`  
		Last Modified: Tue, 12 Mar 2024 13:02:09 GMT  
		Size: 20.6 MB (20569252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dab6e27ad8fb7aa4c1c72574a8ed2a1d04a5de529a450fb5605b521fe12ba6`  
		Last Modified: Tue, 12 Mar 2024 13:02:06 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf6d0d867f4ba1d51aaba9bf44b27b3936fbc500d13376e4252cdbb8826648e`  
		Last Modified: Tue, 12 Mar 2024 13:02:06 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:bookworm` - linux; 386

```console
$ docker pull satosa@sha256:29df1f337d370235279a903eb80322eb9eec3ac134684f701bd59c93d7281437
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.7 MB (488727279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff9657cc4d63a559b1c55d0d689270b3cab3685c02704b1406c3f8d3bb27d29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:56 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Tue, 13 Feb 2024 00:38:56 GMT
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
# Tue, 13 Feb 2024 17:58:09 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 17:58:09 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 18:09:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 18:09:09 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 18:09:09 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 18:09:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 18:09:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 18:09:10 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 18:09:10 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 18:09:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18cc86e13533dd94d2b3a19bfcb8d1ebde259ebc088243e630bf43438b4bb0`  
		Last Modified: Tue, 13 Feb 2024 14:51:20 GMT  
		Size: 3.5 MB (3503117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48b2b4dedbd677d6449d91281ba20d6fe52233483171d23c4296d9fc6d8cb59`  
		Last Modified: Tue, 13 Feb 2024 14:52:23 GMT  
		Size: 12.2 MB (12239206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a65413fe49c71ab3fa6df4fdf4255039158476191db636768837f1e6e8f735`  
		Last Modified: Tue, 13 Feb 2024 14:52:20 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a42bf4645e12370533b1732e65757f2816f1497d63b7f58b12adb1f283696c3`  
		Last Modified: Tue, 13 Feb 2024 14:52:22 GMT  
		Size: 3.0 MB (2978347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2ac513cfa963fa4f372c2e074be3b84b2c51e0b44bc35cce298f09deba2abe`  
		Last Modified: Tue, 13 Feb 2024 18:22:49 GMT  
		Size: 24.2 MB (24203811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580091280836d4f1a1b351ea86e768f03371c70d1bf055b106d9206deae3f257`  
		Last Modified: Tue, 13 Feb 2024 18:23:18 GMT  
		Size: 415.6 MB (415648638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24b0ff82749ad53a37fb38644218e460b515aa025d63420ebb6c720b02ba1a1`  
		Last Modified: Tue, 13 Feb 2024 18:22:43 GMT  
		Size: 10.0 KB (9963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8ea8a78031214f83625ad937146849d4742abbf5ad497ded7e20c73e51dc3c`  
		Last Modified: Tue, 13 Feb 2024 18:22:43 GMT  
		Size: 2.1 KB (2144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:bookworm` - linux; ppc64le

```console
$ docker pull satosa@sha256:3ca21f61a53fe5346c76ed4b9351ce8f001d671762a09a9c1107237d507d7925
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.2 MB (491195693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde9ec216fdcaf6771a71bba1c3a946c1400e738a3a3d304194b057d98b2dd5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:03 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Tue, 13 Feb 2024 00:39:05 GMT
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
# Tue, 13 Feb 2024 08:21:36 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 08:21:37 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 08:29:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 08:29:24 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 08:29:25 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 08:29:25 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 08:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 08:29:26 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 08:29:26 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 08:29:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee78f2de2777d7bd5e7363b69080bb1a6394e1cddd1fc2acaa7f608b1d129d7a`  
		Last Modified: Tue, 13 Feb 2024 03:40:38 GMT  
		Size: 3.7 MB (3704538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8cf259e5ab2eafff3461cd2b4fd546d5d20b75f29b62cd7f1efe2cb09905ff`  
		Last Modified: Tue, 13 Feb 2024 03:41:09 GMT  
		Size: 12.6 MB (12602554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7325c8b16dd117cc14e83e03632bfff7d1ff2dd5c50743012aefa3de8b7b2b15`  
		Last Modified: Tue, 13 Feb 2024 03:41:07 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b53c907fc7631d6fac41077df35d1d3a0ece736979014a24f63fa5ca967935c`  
		Last Modified: Tue, 13 Feb 2024 03:41:08 GMT  
		Size: 3.0 MB (2979477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0549feb427d838b6be46181808df359991252c393af2d1bf946f037982b6450b`  
		Last Modified: Tue, 13 Feb 2024 08:38:33 GMT  
		Size: 24.5 MB (24498861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63086daba02a48c5c956598cef502964ec2b7e522483c7ab0ce6bdec980f1ea2`  
		Last Modified: Tue, 13 Feb 2024 08:38:53 GMT  
		Size: 414.3 MB (414279010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1208cb1697601637c58f6636e02d78eb11f3c9066acc050f74644091e9ca9646`  
		Last Modified: Tue, 13 Feb 2024 08:38:29 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922bf6d55eb5cac0384856e8c65367780d6352aa0675e993301e232564115cd5`  
		Last Modified: Tue, 13 Feb 2024 08:38:29 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:bookworm` - linux; s390x

```console
$ docker pull satosa@sha256:39a52857d3d3587a0c290bb162869643e8b9238f59ad917118de3baee91ee50d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.2 MB (498229609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83ea5fd0b8ea8f4fc660c3019bc2988cc4386e050e60fc94ae79e6ea783b2cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 01:02:37 GMT
ADD file:2dc5fd465b3cc728990229e12489d68faf8a93e6f574cacdca11cc9bf31f511d in / 
# Tue, 13 Feb 2024 01:02:39 GMT
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
# Fri, 16 Feb 2024 16:03:41 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Fri, 16 Feb 2024 16:03:42 GMT
ENV SATOSA_VERSION=8.4.0
# Fri, 16 Feb 2024 16:09:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 16 Feb 2024 16:09:18 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 16 Feb 2024 16:09:18 GMT
WORKDIR /etc/satosa
# Fri, 16 Feb 2024 16:09:18 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 16 Feb 2024 16:09:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 16:09:18 GMT
EXPOSE 8080
# Fri, 16 Feb 2024 16:09:18 GMT
USER satosa:satosa
# Fri, 16 Feb 2024 16:09:18 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e55f0b78e9a121a048a72242f0aec2a221466b10bedb873c07b73e4b99f873cb`  
		Last Modified: Tue, 13 Feb 2024 01:30:22 GMT  
		Size: 27.5 MB (27488587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3ec7775a265efbf6c384c5d18340a5650c973a50ca2d0e398efd6f07517659`  
		Last Modified: Tue, 13 Feb 2024 11:03:06 GMT  
		Size: 3.2 MB (3166462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082a41a047ff2d36ba555081aeb9a03139eab7b42242dbe438a27a94c51a2118`  
		Last Modified: Fri, 16 Feb 2024 10:40:39 GMT  
		Size: 11.9 MB (11917778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0926d163b9bf2515318962adbb6c235265efae4c566c49f626ddf024df8a42`  
		Last Modified: Fri, 16 Feb 2024 10:40:37 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf892b126232594fc63d047a9f20f7e6170f1e2a219318db54ab08bd0fc07ed`  
		Last Modified: Fri, 16 Feb 2024 10:40:38 GMT  
		Size: 3.0 MB (2978431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4ef25f44b24d50ed7297148115ca7338cfb361dc21d3f50ff822fbe72640c3`  
		Last Modified: Fri, 16 Feb 2024 16:10:46 GMT  
		Size: 23.8 MB (23798204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183d32aa11aa9166c3b9942b91e0c6928610420fb825c3040b4b013e74e74636`  
		Last Modified: Fri, 16 Feb 2024 16:11:02 GMT  
		Size: 428.9 MB (428867797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4adc9965b1ba16dd34f2892e459b028712639a3e92a446b334f71dd3dc941dd`  
		Last Modified: Fri, 16 Feb 2024 16:10:43 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5072cc9e5ef227421d9831c3f457357ca1ca7e2220f50e68b27aebee0bcf6438`  
		Last Modified: Fri, 16 Feb 2024 16:10:43 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `satosa:latest`

```console
$ docker pull satosa@sha256:b6fe267decbd467817f653627989f44ba57a506a148d4b9a69eef4b5b3a223c6
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
$ docker pull satosa@sha256:5c32b82a481315407a8213fe68c5484f56208ce09c049e38d59561c73e150d58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90906882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03bfb47ed64e4c5dc1ea893114954587da90fc25a3247e4612f329469038ef9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
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
# Tue, 13 Feb 2024 15:44:32 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 15:44:32 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 15:45:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 15:45:32 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 15:45:32 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 15:45:32 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 15:45:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 15:45:32 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 15:45:32 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 15:45:32 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d1f07906b71fd60ac43c61035514996a8ad8dbfd39d4f570ac5446b064ee5d`  
		Last Modified: Tue, 13 Feb 2024 11:12:54 GMT  
		Size: 3.5 MB (3507732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3e9a37b01a92d059e8ee8ff525a84400222555e33cae231f8b1d788957450d`  
		Last Modified: Tue, 13 Feb 2024 11:13:47 GMT  
		Size: 12.0 MB (11991512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a33514831e0a3ab693884ed9b534dacd5b2c7110c64692812e78da8471d1f0b`  
		Last Modified: Tue, 13 Feb 2024 11:13:44 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0959bfd25ad80f8e7023ffd4f70fd6242ee502c15f6671bd4d299d32efc40470`  
		Last Modified: Tue, 13 Feb 2024 11:13:45 GMT  
		Size: 3.0 MB (2978901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbce98668aa61c3d668392a27d1f07962a0b05246e61e0c6fdd02e9ff3b99cb`  
		Last Modified: Tue, 13 Feb 2024 15:46:04 GMT  
		Size: 22.1 MB (22131281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c2e9f06bef4f772530677cf3122ac0560bcd3f06eef8c1b2f5912840640f37`  
		Last Modified: Tue, 13 Feb 2024 15:46:04 GMT  
		Size: 21.2 MB (21161018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0149f2d2741d11c38936bd8be232ff2e6ff77eae0054a9af5021b6a01b736d0d`  
		Last Modified: Tue, 13 Feb 2024 15:46:01 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be0dac7d9ed7489cc123f4313d801f0b415a9231541a419d86ce216c05dcaa0`  
		Last Modified: Tue, 13 Feb 2024 15:46:01 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:latest` - linux; arm variant v5

```console
$ docker pull satosa@sha256:1b6c034c92c4410286bbe6984a558abeb749173f63a05c4f726f31f72224deb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.3 MB (355333286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111a7bce7a10a698fe50d3fa635c6b80d60abf733457cb11c02b9247ba917a70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 23 May 2023 00:48:41 GMT
ADD file:868f634f5ddb80ed9e9c719ccaf5d564d96fe819f0b000ecc734311baf5da99b in / 
# Tue, 23 May 2023 00:48:42 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:48:42 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 00:48:42 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 00:48:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 May 2023 00:48:42 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 23 May 2023 00:48:42 GMT
ENV PYTHON_VERSION=3.11.3
# Tue, 23 May 2023 00:48:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 23 May 2023 00:48:42 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 23 May 2023 00:48:42 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Tue, 23 May 2023 00:48:42 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Tue, 23 May 2023 00:48:42 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/0d8570dc44796f4369b652222cf176b3db6ac70e/public/get-pip.py
# Tue, 23 May 2023 00:48:42 GMT
ENV PYTHON_GET_PIP_SHA256=96461deced5c2a487ddc65207ec5a9cffeca0d34e7af7ea1afc470ff0d746207
# Tue, 23 May 2023 00:48:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 23 May 2023 00:48:42 GMT
CMD ["python3"]
# Tue, 23 May 2023 13:53:17 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 23 May 2023 13:53:17 GMT
ENV SATOSA_VERSION=8.2.0
# Tue, 23 May 2023 14:00:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 23 May 2023 14:00:59 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 23 May 2023 14:00:59 GMT
WORKDIR /etc/satosa
# Tue, 23 May 2023 14:00:59 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 23 May 2023 14:00:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 May 2023 14:00:59 GMT
EXPOSE 8080
# Tue, 23 May 2023 14:01:00 GMT
USER satosa:satosa
# Tue, 23 May 2023 14:01:00 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:812967ccba449e7a96044b2d48ffc62816b22eb17641844c4dfffbe3b3ec6f21`  
		Last Modified: Tue, 23 May 2023 00:51:19 GMT  
		Size: 28.9 MB (28903411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51c02b84c5d3000cd5fad1db43e5b181925ce65fcba69e5de80cf6f86dcc9dc`  
		Last Modified: Tue, 23 May 2023 06:21:38 GMT  
		Size: 1.1 MB (1059787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6804baecd87d6bf5a0df8a81f53493f3983ccb3fe4f67085cc33df9ad93e424f`  
		Last Modified: Tue, 23 May 2023 06:22:10 GMT  
		Size: 11.7 MB (11656149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee865db702543611a0073c272d69878c889145e3a15f03abea337bb34ff13383`  
		Last Modified: Tue, 23 May 2023 06:22:08 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3582d7038d35bdd999e817a1a2242591a72dafee3b7f9491739f2eded12caa30`  
		Last Modified: Tue, 23 May 2023 06:22:10 GMT  
		Size: 3.4 MB (3371758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c896d763a3a63cb00ddbd5cdcc2e845cc52b26db83ecc4ee8f885eac815ff406`  
		Last Modified: Tue, 23 May 2023 14:01:23 GMT  
		Size: 22.7 MB (22747859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26bbabdb2586558f07ff698b694f7ff5d2ca90ea1434de90862519d78f38b0af`  
		Last Modified: Tue, 23 May 2023 14:01:43 GMT  
		Size: 287.6 MB (287582449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b525758a86a11078bd078050edb0c80f05479b749dc22dc2c288ddf349ad58d3`  
		Last Modified: Tue, 23 May 2023 14:01:19 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b9451dc6448c57bc30ed2831c6dbcddc60410465c75ab640ed583d0aeab80b`  
		Last Modified: Tue, 23 May 2023 14:01:19 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:latest` - linux; arm variant v7

```console
$ docker pull satosa@sha256:011efe44839fb660c982fc18393018be58964e5d695df1ab75c2c18622830af3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.1 MB (350118406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9003b3a402e803a529aafaa42d3b2b9e77fab05e81b128ad77a21dae037924a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 23 May 2023 00:57:55 GMT
ADD file:dbb95e676c7a9806b1883ebcf4259345159caf22ff7194ba7556ea0b1f78099a in / 
# Tue, 23 May 2023 00:57:56 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:57:56 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 00:57:56 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 00:57:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 May 2023 00:57:56 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 23 May 2023 00:57:56 GMT
ENV PYTHON_VERSION=3.11.3
# Tue, 23 May 2023 00:57:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 23 May 2023 00:57:56 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 23 May 2023 00:57:56 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Tue, 23 May 2023 00:57:56 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Tue, 23 May 2023 00:57:56 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/0d8570dc44796f4369b652222cf176b3db6ac70e/public/get-pip.py
# Tue, 23 May 2023 00:57:56 GMT
ENV PYTHON_GET_PIP_SHA256=96461deced5c2a487ddc65207ec5a9cffeca0d34e7af7ea1afc470ff0d746207
# Tue, 23 May 2023 00:57:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 23 May 2023 00:57:56 GMT
CMD ["python3"]
# Tue, 23 May 2023 11:03:06 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 23 May 2023 11:03:07 GMT
ENV SATOSA_VERSION=8.2.0
# Tue, 23 May 2023 11:08:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 23 May 2023 11:08:21 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 23 May 2023 11:08:22 GMT
WORKDIR /etc/satosa
# Tue, 23 May 2023 11:08:22 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 23 May 2023 11:08:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 May 2023 11:08:23 GMT
EXPOSE 8080
# Tue, 23 May 2023 11:08:23 GMT
USER satosa:satosa
# Tue, 23 May 2023 11:08:24 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a27027e97f260d9b7aac9bae941b44639374700dc4c32cc2e378b189a4ffda88`  
		Last Modified: Tue, 23 May 2023 01:01:46 GMT  
		Size: 26.6 MB (26564635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c18fa1eb965a9cd27f27d4f8153653a65b50942439f8c148cfebd8d30b2fd92`  
		Last Modified: Tue, 23 May 2023 05:27:31 GMT  
		Size: 1.0 MB (1041758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed9b7ddc0308ec6c21e7ce071d1a78403a2ed9e29eb18d1e50e2b432c26e647`  
		Last Modified: Tue, 23 May 2023 05:27:58 GMT  
		Size: 11.2 MB (11225102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c05d200b8453f1780ddda48b62a663eba129701942d7315f7b8709d060874028`  
		Last Modified: Tue, 23 May 2023 05:27:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c39f7290efdd5e658f9589eeafae04e61c38a52c3660114a9af02ac7864cbf`  
		Last Modified: Tue, 23 May 2023 05:27:57 GMT  
		Size: 3.4 MB (3371808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ebb953d507de429bee981b04539b24423058824bd989d591b33a702f5c947a`  
		Last Modified: Tue, 23 May 2023 11:08:49 GMT  
		Size: 22.5 MB (22475194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884723dd7bbba821cc446c78904a20ef101b33b4d450f5afd8ac5a2d449e0988`  
		Last Modified: Tue, 23 May 2023 11:09:19 GMT  
		Size: 285.4 MB (285428033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed31500b36d9c56263ca900c1d1c50fbed84aa05926e66adccfcf085d0e48a5e`  
		Last Modified: Tue, 23 May 2023 11:08:44 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc69d7a6ff1da49d86ac28b19acd7e90b05476c2cc303f4f08457ab9595a980b`  
		Last Modified: Tue, 23 May 2023 11:08:44 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:latest` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:3a68256b9eab756090fcfd6e0fb01d31474c035065ef89a46fc20a103cfb03cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89982898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a7461963f9363c0e895bb78ed23316e77c1fccaa66569858c0373a613a3da0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
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
# Tue, 12 Mar 2024 13:00:40 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 12 Mar 2024 13:00:40 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 12 Mar 2024 13:01:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 12 Mar 2024 13:01:39 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 12 Mar 2024 13:01:39 GMT
WORKDIR /etc/satosa
# Tue, 12 Mar 2024 13:01:39 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 12 Mar 2024 13:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 13:01:39 GMT
EXPOSE 8080
# Tue, 12 Mar 2024 13:01:39 GMT
USER satosa:satosa
# Tue, 12 Mar 2024 13:01:39 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55af26b7addf6c0f6fe5fed39393a1379356bb864caac1da91a0fd2fa77b911b`  
		Last Modified: Tue, 12 Mar 2024 09:46:35 GMT  
		Size: 3.3 MB (3323852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3caa3c29ca1489fb5a2119be7e582ca42dece866341d3a379b776c5b2c6362b`  
		Last Modified: Tue, 12 Mar 2024 09:47:24 GMT  
		Size: 12.0 MB (11965714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1240f83dd7d124ccb21f022464852fd5587ac77b5e6be447b86db873dc0bf6d`  
		Last Modified: Tue, 12 Mar 2024 09:47:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6318e81a3dccbefef51184e62057428961a21b0cde407673f088ee0f57417ddc`  
		Last Modified: Tue, 12 Mar 2024 09:47:23 GMT  
		Size: 3.0 MB (2979263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1b6451ffebc99e9f0ea5b7dfcb1ae02b45eca810ebc9bbada3dfc6a5005861`  
		Last Modified: Tue, 12 Mar 2024 13:02:09 GMT  
		Size: 22.0 MB (21976035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ab61321e7317b6e6d2219203156533d48070dc964baf5797c21336fd94c513`  
		Last Modified: Tue, 12 Mar 2024 13:02:09 GMT  
		Size: 20.6 MB (20569252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dab6e27ad8fb7aa4c1c72574a8ed2a1d04a5de529a450fb5605b521fe12ba6`  
		Last Modified: Tue, 12 Mar 2024 13:02:06 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf6d0d867f4ba1d51aaba9bf44b27b3936fbc500d13376e4252cdbb8826648e`  
		Last Modified: Tue, 12 Mar 2024 13:02:06 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:latest` - linux; 386

```console
$ docker pull satosa@sha256:29df1f337d370235279a903eb80322eb9eec3ac134684f701bd59c93d7281437
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.7 MB (488727279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff9657cc4d63a559b1c55d0d689270b3cab3685c02704b1406c3f8d3bb27d29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:56 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Tue, 13 Feb 2024 00:38:56 GMT
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
# Tue, 13 Feb 2024 17:58:09 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 17:58:09 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 18:09:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 18:09:09 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 18:09:09 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 18:09:10 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 18:09:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 18:09:10 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 18:09:10 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 18:09:10 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18cc86e13533dd94d2b3a19bfcb8d1ebde259ebc088243e630bf43438b4bb0`  
		Last Modified: Tue, 13 Feb 2024 14:51:20 GMT  
		Size: 3.5 MB (3503117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48b2b4dedbd677d6449d91281ba20d6fe52233483171d23c4296d9fc6d8cb59`  
		Last Modified: Tue, 13 Feb 2024 14:52:23 GMT  
		Size: 12.2 MB (12239206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a65413fe49c71ab3fa6df4fdf4255039158476191db636768837f1e6e8f735`  
		Last Modified: Tue, 13 Feb 2024 14:52:20 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a42bf4645e12370533b1732e65757f2816f1497d63b7f58b12adb1f283696c3`  
		Last Modified: Tue, 13 Feb 2024 14:52:22 GMT  
		Size: 3.0 MB (2978347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2ac513cfa963fa4f372c2e074be3b84b2c51e0b44bc35cce298f09deba2abe`  
		Last Modified: Tue, 13 Feb 2024 18:22:49 GMT  
		Size: 24.2 MB (24203811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580091280836d4f1a1b351ea86e768f03371c70d1bf055b106d9206deae3f257`  
		Last Modified: Tue, 13 Feb 2024 18:23:18 GMT  
		Size: 415.6 MB (415648638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24b0ff82749ad53a37fb38644218e460b515aa025d63420ebb6c720b02ba1a1`  
		Last Modified: Tue, 13 Feb 2024 18:22:43 GMT  
		Size: 10.0 KB (9963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8ea8a78031214f83625ad937146849d4742abbf5ad497ded7e20c73e51dc3c`  
		Last Modified: Tue, 13 Feb 2024 18:22:43 GMT  
		Size: 2.1 KB (2144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:latest` - linux; ppc64le

```console
$ docker pull satosa@sha256:3ca21f61a53fe5346c76ed4b9351ce8f001d671762a09a9c1107237d507d7925
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.2 MB (491195693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde9ec216fdcaf6771a71bba1c3a946c1400e738a3a3d304194b057d98b2dd5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:03 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Tue, 13 Feb 2024 00:39:05 GMT
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
# Tue, 13 Feb 2024 08:21:36 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Tue, 13 Feb 2024 08:21:37 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 13 Feb 2024 08:29:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Tue, 13 Feb 2024 08:29:24 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Tue, 13 Feb 2024 08:29:25 GMT
WORKDIR /etc/satosa
# Tue, 13 Feb 2024 08:29:25 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Tue, 13 Feb 2024 08:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 08:29:26 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 08:29:26 GMT
USER satosa:satosa
# Tue, 13 Feb 2024 08:29:26 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee78f2de2777d7bd5e7363b69080bb1a6394e1cddd1fc2acaa7f608b1d129d7a`  
		Last Modified: Tue, 13 Feb 2024 03:40:38 GMT  
		Size: 3.7 MB (3704538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8cf259e5ab2eafff3461cd2b4fd546d5d20b75f29b62cd7f1efe2cb09905ff`  
		Last Modified: Tue, 13 Feb 2024 03:41:09 GMT  
		Size: 12.6 MB (12602554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7325c8b16dd117cc14e83e03632bfff7d1ff2dd5c50743012aefa3de8b7b2b15`  
		Last Modified: Tue, 13 Feb 2024 03:41:07 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b53c907fc7631d6fac41077df35d1d3a0ece736979014a24f63fa5ca967935c`  
		Last Modified: Tue, 13 Feb 2024 03:41:08 GMT  
		Size: 3.0 MB (2979477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0549feb427d838b6be46181808df359991252c393af2d1bf946f037982b6450b`  
		Last Modified: Tue, 13 Feb 2024 08:38:33 GMT  
		Size: 24.5 MB (24498861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63086daba02a48c5c956598cef502964ec2b7e522483c7ab0ce6bdec980f1ea2`  
		Last Modified: Tue, 13 Feb 2024 08:38:53 GMT  
		Size: 414.3 MB (414279010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1208cb1697601637c58f6636e02d78eb11f3c9066acc050f74644091e9ca9646`  
		Last Modified: Tue, 13 Feb 2024 08:38:29 GMT  
		Size: 10.0 KB (9961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922bf6d55eb5cac0384856e8c65367780d6352aa0675e993301e232564115cd5`  
		Last Modified: Tue, 13 Feb 2024 08:38:29 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:latest` - linux; s390x

```console
$ docker pull satosa@sha256:39a52857d3d3587a0c290bb162869643e8b9238f59ad917118de3baee91ee50d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.2 MB (498229609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83ea5fd0b8ea8f4fc660c3019bc2988cc4386e050e60fc94ae79e6ea783b2cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 13 Feb 2024 01:02:37 GMT
ADD file:2dc5fd465b3cc728990229e12489d68faf8a93e6f574cacdca11cc9bf31f511d in / 
# Tue, 13 Feb 2024 01:02:39 GMT
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
# Fri, 16 Feb 2024 16:03:41 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	;
# Fri, 16 Feb 2024 16:03:42 GMT
ENV SATOSA_VERSION=8.4.0
# Fri, 16 Feb 2024 16:09:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Fri, 16 Feb 2024 16:09:18 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Fri, 16 Feb 2024 16:09:18 GMT
WORKDIR /etc/satosa
# Fri, 16 Feb 2024 16:09:18 GMT
COPY file:c55013587aaf85deb9d4e88a802c99946f6d607afbf641c34429da762c1aa229 in /usr/local/bin/ 
# Fri, 16 Feb 2024 16:09:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 16:09:18 GMT
EXPOSE 8080
# Fri, 16 Feb 2024 16:09:18 GMT
USER satosa:satosa
# Fri, 16 Feb 2024 16:09:18 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:e55f0b78e9a121a048a72242f0aec2a221466b10bedb873c07b73e4b99f873cb`  
		Last Modified: Tue, 13 Feb 2024 01:30:22 GMT  
		Size: 27.5 MB (27488587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3ec7775a265efbf6c384c5d18340a5650c973a50ca2d0e398efd6f07517659`  
		Last Modified: Tue, 13 Feb 2024 11:03:06 GMT  
		Size: 3.2 MB (3166462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082a41a047ff2d36ba555081aeb9a03139eab7b42242dbe438a27a94c51a2118`  
		Last Modified: Fri, 16 Feb 2024 10:40:39 GMT  
		Size: 11.9 MB (11917778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0926d163b9bf2515318962adbb6c235265efae4c566c49f626ddf024df8a42`  
		Last Modified: Fri, 16 Feb 2024 10:40:37 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf892b126232594fc63d047a9f20f7e6170f1e2a219318db54ab08bd0fc07ed`  
		Last Modified: Fri, 16 Feb 2024 10:40:38 GMT  
		Size: 3.0 MB (2978431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4ef25f44b24d50ed7297148115ca7338cfb361dc21d3f50ff822fbe72640c3`  
		Last Modified: Fri, 16 Feb 2024 16:10:46 GMT  
		Size: 23.8 MB (23798204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183d32aa11aa9166c3b9942b91e0c6928610420fb825c3040b4b013e74e74636`  
		Last Modified: Fri, 16 Feb 2024 16:11:02 GMT  
		Size: 428.9 MB (428867797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4adc9965b1ba16dd34f2892e459b028712639a3e92a446b334f71dd3dc941dd`  
		Last Modified: Fri, 16 Feb 2024 16:10:43 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5072cc9e5ef227421d9831c3f457357ca1ca7e2220f50e68b27aebee0bcf6438`  
		Last Modified: Fri, 16 Feb 2024 16:10:43 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
