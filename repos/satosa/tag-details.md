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
$ docker pull satosa@sha256:9838f3edf179af20bee6c8ac3925bd3f36658a0f5862b3385a6c8f5fe2e618cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8` - linux; amd64

```console
$ docker pull satosa@sha256:df7e89152d9cc4909c80222d415a397e9a8c744497036afe3e184f06dad836b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88862529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14675eb83676db6aee0c38ab053b5d50f3a6bef793a282c6c33034b02b85b8a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 14:40:43 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 14:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 14:40:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 14:40:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 14:40:43 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467daa3d4c8b6f3916948d9277922e51161a5d42c977631819a635d2fa9fb32e`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 3.5 MB (3511398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d51d0de90c323e22cf7900a0ee9185e1e3c185b3ed4fecd9202ae1534e60c7`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 11.7 MB (11724854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e6c34f2b20e314d433bf1d444a0c72dc1b27dc93964a4fc102a4dccd25e799`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab50b4ae9438decebef449b4afb727284fe0c8f9198b603c588fea80266eb13`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 1.8 MB (1751083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0db6c6dc89000cc270ec074bf74ed84465d3fd1b31b84cc16de60dcf4879395`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 21.5 MB (21455664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57f345912a7c877e65d8bfc4b29882cb71d9062d398118c452f731fa33ed2dc`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 21.3 MB (21280717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ff5e597a64fb5ca09139b8f7b787223bcd6a34d8c228040d6afe1440477dc7`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd0519cfa116902f9ae050b5fdf0bc57b64a5b5932a15b709fcc2c1951ecfae`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8` - unknown; unknown

```console
$ docker pull satosa@sha256:5c2553b9ff9019842b9134cb7f6cce18e5ad03d85f5c55a6cad7e49beac6ee1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2613369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6aec6c918521cd245227d130ea8626b23153986c281c938525bfcccc1a3f4f`

```dockerfile
```

-	Layers:
	-	`sha256:7e79b6aa88d9313fa3e0221dbd224b5bf6ecf13806da95dd9247c869c98d75cd`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 2.6 MB (2589886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7feca4e51ca18ad4deb21d66b20093be3fc6c01600301d6036157791cce48a8d`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 23.5 KB (23483 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:34f580cda009c649a0081d1dd0149e1d5d02cee4c2544f0929854272eaec8f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88214898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4290484613fdccc82556b42425aa56e356902679ddc288bb26c46b07c14dd461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 14:40:43 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 14:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 14:40:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 14:40:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 14:40:43 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc0bb0f48368309a59f8f76a26a1a2aefa34ff474a1d5fc171b034e954d299b`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 3.3 MB (3331450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbb068a2dcf7bb59fec2a07a7fc7d2d77207313340abb2e7c0010a7660c74e1`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 11.7 MB (11697919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cccda67aa8cce65f16c17702f99d7ae53526c87fe6fd6df833321c206a1915`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31068c739a9608963613c12774e31ba8f0157b299cf8cad529aba9038a3d689d`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 1.8 MB (1751307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc99567289f026c220b3120e68f2d85a71232bbe55438455a3f5e660e87389c`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 21.3 MB (21297890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b36ce4c95930510899b0b5e3794aa799935d3c389646b558a56a26f050775a0`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 21.0 MB (20967460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b6a305f0626446c54a1e5c9a85be45e2c0848d78fffbea4e00d62319e58090`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c81978fdbec654b6eee497a378a0dd8655dab131976c1043e21b9b10947c537`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8` - unknown; unknown

```console
$ docker pull satosa@sha256:47ec55d5a93a25674ccc46b0f4063e4ba39e098ea9cfae20f977e66a0e62e08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2616658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8a53b07362a51d5b4b640abbb68b92b09ec789662505cb6bd7a61909c2f134`

```dockerfile
```

-	Layers:
	-	`sha256:ab5fac2784df8870ecf5b0b5660c59db1821183005268be1c017eefb25d099ea`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 2.6 MB (2592706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c71e017aac0b41e1beff888e67cf43b0fe9f47727a15285186f9f711fb2c4c`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 24.0 KB (23952 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8-alpine`

```console
$ docker pull satosa@sha256:450fe7aed678967f2ecd2c0e9c6332e5e2b100d34adcfa8291ecb0faba12a91d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `satosa:8-alpine` - linux; amd64

```console
$ docker pull satosa@sha256:1d4a2004db2f2160b9293361adbe91483bbbcfafd770c82549d3c79cbd63859d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45787482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c88811c75113b8a4851925e08cc4b50d9514de6e2842e9eaab79c9680a83c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fe8821d8e937f4d18d66ed6c01512319f6369e39501aa040d545cddb26c012`  
		Last Modified: Fri, 06 Sep 2024 23:31:42 GMT  
		Size: 627.9 KB (627915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e73abbe668f9cf00602e624892cee4209b2bea1a95102c68b2057c7e0b3c57`  
		Last Modified: Fri, 06 Sep 2024 23:31:43 GMT  
		Size: 11.5 MB (11499904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd37ef32dbcc8362c68d13269033880dde7e11c41e37de2144c7489fe84d588`  
		Last Modified: Fri, 06 Sep 2024 23:31:42 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e183bebb85d6d6db6d0223f702bb07cfdb79b7f435fb9c1d0e43fb9022370a9`  
		Last Modified: Fri, 06 Sep 2024 23:31:43 GMT  
		Size: 1.7 MB (1673601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b17f050437f188171644ad503679b514d0019bea18044a12242ceb2fe6083e`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 7.4 MB (7409601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d878e1fb4ea01bcb258e5c2cd0eb96217339c4c051c4d4fd643683e476df9a4a`  
		Last Modified: Sat, 07 Sep 2024 00:08:55 GMT  
		Size: 21.1 MB (21144433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14c3f2db0ae337a9fc6e52f90c84de448c365301280a38020a17089961009b5`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f56a48a186a09d5a69eebebecf31b6bb438e02c3867154d01a13a24ca8f659a`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:ce6fd0561adb7c64976cb6fa979b8dc71b67c174924c5359a0d0900f96b5c321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1194106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54d256448b7680b09dce413cbbf5be25b70b9c315cfc9c61333ca2ff946849b`

```dockerfile
```

-	Layers:
	-	`sha256:7e11b81e6a698a0ed5df4bb58d79891397ecfb89a6dd90f7df37c37ef9e5a7a5`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 1.2 MB (1169929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2477e3630694ca6355ede795fa0ca290ddab4bb0ed90194dc82f36e2ab4b2f3b`  
		Last Modified: Sat, 07 Sep 2024 00:08:53 GMT  
		Size: 24.2 KB (24177 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8-alpine` - linux; arm variant v7

```console
$ docker pull satosa@sha256:484750cdfd849cd77669cbe91f573bb799331e79c39145a45324ad01310c2204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72502585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c3b9ea495a1c6906a04b17ae1148f8ec4470b8364642894b5beb7c54dc3c2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aca995c8234bcb8cc3881779eb898cea97d1e1ae8d93dfc03230bc2b72cd58f`  
		Last Modified: Wed, 24 Jul 2024 10:02:21 GMT  
		Size: 628.0 KB (627989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06edd34be8b9ba5da915d801b435bfb90ed4c553da299b2edb6293bbef6cd86a`  
		Last Modified: Wed, 07 Aug 2024 22:21:25 GMT  
		Size: 10.7 MB (10656411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164f482cec3d411bf812c97570ac5c9cd9745c2358cb78bd766f07f01038b63c`  
		Last Modified: Wed, 07 Aug 2024 22:21:24 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00118344aaad7672000a959203f9ded1e7e1c7bffa1433954163611aba69da4`  
		Last Modified: Wed, 04 Sep 2024 06:48:01 GMT  
		Size: 1.7 MB (1673590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c8bf69c8012a63b0b5abd3d4a28a39b1aeaed68ffbefa760be087bdaeb807a`  
		Last Modified: Wed, 04 Sep 2024 08:25:22 GMT  
		Size: 11.3 MB (11271496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1221728f93d4c726ecb0f8bf748430dcadd7eacce6921dab6782a74002a17a`  
		Last Modified: Wed, 04 Sep 2024 08:25:23 GMT  
		Size: 45.3 MB (45333665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1918f04628471e1950a105722a4d0e74f6a5d737e48d3ff39a4c0499d4f802`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3dc36ddb010041b6560916f6d2ecbb8da960fd4b4420d7104cf2e9eae2e8dd6`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 2.1 KB (2148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:9a5e945adbc9012c9125b8e76e839c0211e790b7aadaed484f26c7f84ba22869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1194729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b02d8bf4abbc5d9e84d436d0bae2a84f79699f03a2be8c2ac2699db1204182`

```dockerfile
```

-	Layers:
	-	`sha256:5a0df6ee33dffff152bce8d3422e8602ad36252d7f2461d6fcea1e786db2daf4`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 1.2 MB (1170376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62dc3f905e9f0d597d487f8b3c213c95f3dfd1c6d4ff1c069c332bffa6c46d08`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 24.4 KB (24353 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8-alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e22814a24e95ebc1f3d6544566d145352a96c1792f2365a16b9d306f576611b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47295578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeeb532d9cfb950d8b7acdbdbe8fd94d29d5120bdd40d9cf046295712ca8c1bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564a93de2c7019a622a4491382e14c5bdf5d7c23bd78c6f9f1c699f72e74fce`  
		Last Modified: Wed, 04 Sep 2024 07:31:02 GMT  
		Size: 630.3 KB (630336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24cd4abfec65ee86b6e7bd5861d5543e3da7dafb92f20851aea5357dfa89434`  
		Last Modified: Wed, 04 Sep 2024 07:31:03 GMT  
		Size: 13.7 MB (13656630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce315a403531201e7db80d481aafa278bd2b73b77c24c5dac830b8736ef6a75`  
		Last Modified: Wed, 04 Sep 2024 07:31:02 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40395139ed67e33f42cbd9721d5a74dac2d9917914519da789686e6122be9579`  
		Last Modified: Wed, 04 Sep 2024 07:31:03 GMT  
		Size: 1.7 MB (1673588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f7073db196529ac226fa3fa25afd2cb96c0298b048397af4f32a61c8d163a4`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 7.4 MB (7403230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3182e9cb9a162ad5fc8ed2b1bb93e5ae69b4a371cd40055b321ec73be449e6e`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 20.6 MB (20561012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3016037b2ceaa72afbe6b3af6862693b2d462201dd7491bc761c2dd900b390`  
		Last Modified: Wed, 04 Sep 2024 09:43:16 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35827c7507295d2943fcceceaeada49dfe6114f767c09d53f773d2c8ae0f3163`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 2.1 KB (2141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:0d5ed8afefec0046729989356a966a2baca01f83e0d253ae0cbe857f5b25e911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1192195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb71a3b25a30177e482a159536c84119f4731c59326a0ea5643027d47048bee9`

```dockerfile
```

-	Layers:
	-	`sha256:91aa376b5a5a0351d224b70755bd3f018eda925fbc7d8728275cb741623c08bb`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 1.2 MB (1167548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ddf12d3de38b8098769bbab9786e83ba03071f5f62fc4f03c9a5bbd8a40b9a9`  
		Last Modified: Wed, 04 Sep 2024 09:43:16 GMT  
		Size: 24.6 KB (24647 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8-alpine` - linux; 386

```console
$ docker pull satosa@sha256:2d8cebf9b303562cec2ad131a00c16058682d35e6bd8c8373a6049c2da05fa50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72174501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dca95b05acd6caadc4d2d7296fd8b0f814308a8bb54f679533a64ebab3faef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b2801d1a66d8eb7d37ef8c9bd01ed316e098fb58aca389c7038cf904ab7229`  
		Last Modified: Fri, 06 Sep 2024 23:33:12 GMT  
		Size: 628.4 KB (628417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e8a05a75efec89d800448cf9a90e1fd959a798b05a8f51e395555b1d05c35f`  
		Last Modified: Fri, 06 Sep 2024 23:33:13 GMT  
		Size: 11.7 MB (11692995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5711feaa7d3d84fb482e82165b47257f80cf1c7983ba93ce546895b7d9e28f21`  
		Last Modified: Fri, 06 Sep 2024 23:33:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daa8fc3a87001de1178cb86c2f3a5fb7e0c2b59f148e985334303b078cc6b13`  
		Last Modified: Fri, 06 Sep 2024 23:33:13 GMT  
		Size: 1.7 MB (1673606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7b4e5c3f2ca385e6a13fb3370fe3f6b5b7fbb27b7e78dda4febbba65faa3ae`  
		Last Modified: Sat, 07 Sep 2024 00:14:59 GMT  
		Size: 9.7 MB (9739429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a844ba5a90453d5ad7c35d062ced6e7dd837a85671dba10cf6084eed5bb437c`  
		Last Modified: Sat, 07 Sep 2024 00:15:00 GMT  
		Size: 45.2 MB (45174127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba215f757c4dc05b9334c475e0b248836410f95ca5863da0d003a76632535a1`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 9.9 KB (9920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a6e89a4bf4c06ffa048e8cedd4b46ad59c9488eb85e10ebddda37a91119547`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:5c89fc3ceec355fda8b70edc5043ef7d778ac8a14eeba4292a949b1cb2327e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1196870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64cf3af182ba3581f1e116de5945cb44af88663baf9613093c160e918a42baf`

```dockerfile
```

-	Layers:
	-	`sha256:90b86ed2cf30e8cdaad32f8211994587cdb407caf5196c21249a5f34b13b85dd`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 1.2 MB (1172748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2dc2205c70270528b883f21361c34d7e3293ee05096b63fa6a91d7c0be6ac47`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 24.1 KB (24122 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8-alpine` - linux; ppc64le

```console
$ docker pull satosa@sha256:6eecae17d30f48b03013d1d14a9b85ad3dea43b7923802d32ea3fa169f663479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76592545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caecb8549d9061ef80f72b53699ea19949fb3468ebdd4fb08c708829a1e05b36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459c907a569b15590c9d09d1ce39e44a9fa42640c696731731c52d192bfd1842`  
		Last Modified: Wed, 04 Sep 2024 07:40:49 GMT  
		Size: 630.8 KB (630823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d605ef3d7805437512a36129b9d3fb98ea13cddaf3c648f0147ba73205aa8fb`  
		Last Modified: Wed, 04 Sep 2024 10:52:53 GMT  
		Size: 14.1 MB (14072296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca3a0f938f4ab832be7c9b54e21d39cb0b524c08c9ec96b391064e82e8631d5`  
		Last Modified: Wed, 04 Sep 2024 10:52:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad63210e30ceb3bec53e28d69a992fc0e9f5ba1671edc1342363a34bf791e6a`  
		Last Modified: Wed, 04 Sep 2024 10:52:53 GMT  
		Size: 1.7 MB (1673607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb55fe0b4d5ab4f6e38e6c402bd87fb52c91f2618745b6a66f3ea5180e2ef1a`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 9.9 MB (9918961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807f1e0c89922bd6eb55fe13fd897d48f74a874ef5df95b59aa61c5becac725b`  
		Last Modified: Wed, 04 Sep 2024 11:57:27 GMT  
		Size: 46.9 MB (46921424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f44aa855627fd8f485493cf04a1fe931385ef50ab1e8c0a79039488cf685256`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca0ca3cc5339094abd67f79e15bfea386376d3d2a52bcbbcd606c8d3e08b098`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:b11392488a9554cedf95a8a01fba766787c14030bb9cf5a0ce3e7aba1ae245b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1192698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc0583b84240d78f45aed5c0632d199084849cf2aa75cea1b4fa5d4d7a6d7ee0`

```dockerfile
```

-	Layers:
	-	`sha256:f35c5753ebe494db7b440a6cf4b3dd4bd589e66ec185d01a909e8c1122073457`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 1.2 MB (1168412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:977c5235e7ee7677285f54387c067e63b90071463dba2480f48588b750a682f2`  
		Last Modified: Wed, 04 Sep 2024 11:57:24 GMT  
		Size: 24.3 KB (24286 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8-alpine3.19`

```console
$ docker pull satosa@sha256:450fe7aed678967f2ecd2c0e9c6332e5e2b100d34adcfa8291ecb0faba12a91d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `satosa:8-alpine3.19` - linux; amd64

```console
$ docker pull satosa@sha256:1d4a2004db2f2160b9293361adbe91483bbbcfafd770c82549d3c79cbd63859d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45787482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c88811c75113b8a4851925e08cc4b50d9514de6e2842e9eaab79c9680a83c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fe8821d8e937f4d18d66ed6c01512319f6369e39501aa040d545cddb26c012`  
		Last Modified: Fri, 06 Sep 2024 23:31:42 GMT  
		Size: 627.9 KB (627915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e73abbe668f9cf00602e624892cee4209b2bea1a95102c68b2057c7e0b3c57`  
		Last Modified: Fri, 06 Sep 2024 23:31:43 GMT  
		Size: 11.5 MB (11499904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd37ef32dbcc8362c68d13269033880dde7e11c41e37de2144c7489fe84d588`  
		Last Modified: Fri, 06 Sep 2024 23:31:42 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e183bebb85d6d6db6d0223f702bb07cfdb79b7f435fb9c1d0e43fb9022370a9`  
		Last Modified: Fri, 06 Sep 2024 23:31:43 GMT  
		Size: 1.7 MB (1673601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b17f050437f188171644ad503679b514d0019bea18044a12242ceb2fe6083e`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 7.4 MB (7409601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d878e1fb4ea01bcb258e5c2cd0eb96217339c4c051c4d4fd643683e476df9a4a`  
		Last Modified: Sat, 07 Sep 2024 00:08:55 GMT  
		Size: 21.1 MB (21144433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14c3f2db0ae337a9fc6e52f90c84de448c365301280a38020a17089961009b5`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f56a48a186a09d5a69eebebecf31b6bb438e02c3867154d01a13a24ca8f659a`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-alpine3.19` - unknown; unknown

```console
$ docker pull satosa@sha256:ce6fd0561adb7c64976cb6fa979b8dc71b67c174924c5359a0d0900f96b5c321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1194106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54d256448b7680b09dce413cbbf5be25b70b9c315cfc9c61333ca2ff946849b`

```dockerfile
```

-	Layers:
	-	`sha256:7e11b81e6a698a0ed5df4bb58d79891397ecfb89a6dd90f7df37c37ef9e5a7a5`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 1.2 MB (1169929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2477e3630694ca6355ede795fa0ca290ddab4bb0ed90194dc82f36e2ab4b2f3b`  
		Last Modified: Sat, 07 Sep 2024 00:08:53 GMT  
		Size: 24.2 KB (24177 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8-alpine3.19` - linux; arm variant v7

```console
$ docker pull satosa@sha256:484750cdfd849cd77669cbe91f573bb799331e79c39145a45324ad01310c2204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72502585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c3b9ea495a1c6906a04b17ae1148f8ec4470b8364642894b5beb7c54dc3c2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aca995c8234bcb8cc3881779eb898cea97d1e1ae8d93dfc03230bc2b72cd58f`  
		Last Modified: Wed, 24 Jul 2024 10:02:21 GMT  
		Size: 628.0 KB (627989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06edd34be8b9ba5da915d801b435bfb90ed4c553da299b2edb6293bbef6cd86a`  
		Last Modified: Wed, 07 Aug 2024 22:21:25 GMT  
		Size: 10.7 MB (10656411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164f482cec3d411bf812c97570ac5c9cd9745c2358cb78bd766f07f01038b63c`  
		Last Modified: Wed, 07 Aug 2024 22:21:24 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00118344aaad7672000a959203f9ded1e7e1c7bffa1433954163611aba69da4`  
		Last Modified: Wed, 04 Sep 2024 06:48:01 GMT  
		Size: 1.7 MB (1673590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c8bf69c8012a63b0b5abd3d4a28a39b1aeaed68ffbefa760be087bdaeb807a`  
		Last Modified: Wed, 04 Sep 2024 08:25:22 GMT  
		Size: 11.3 MB (11271496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1221728f93d4c726ecb0f8bf748430dcadd7eacce6921dab6782a74002a17a`  
		Last Modified: Wed, 04 Sep 2024 08:25:23 GMT  
		Size: 45.3 MB (45333665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1918f04628471e1950a105722a4d0e74f6a5d737e48d3ff39a4c0499d4f802`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3dc36ddb010041b6560916f6d2ecbb8da960fd4b4420d7104cf2e9eae2e8dd6`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 2.1 KB (2148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-alpine3.19` - unknown; unknown

```console
$ docker pull satosa@sha256:9a5e945adbc9012c9125b8e76e839c0211e790b7aadaed484f26c7f84ba22869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1194729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b02d8bf4abbc5d9e84d436d0bae2a84f79699f03a2be8c2ac2699db1204182`

```dockerfile
```

-	Layers:
	-	`sha256:5a0df6ee33dffff152bce8d3422e8602ad36252d7f2461d6fcea1e786db2daf4`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 1.2 MB (1170376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62dc3f905e9f0d597d487f8b3c213c95f3dfd1c6d4ff1c069c332bffa6c46d08`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 24.4 KB (24353 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e22814a24e95ebc1f3d6544566d145352a96c1792f2365a16b9d306f576611b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47295578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeeb532d9cfb950d8b7acdbdbe8fd94d29d5120bdd40d9cf046295712ca8c1bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564a93de2c7019a622a4491382e14c5bdf5d7c23bd78c6f9f1c699f72e74fce`  
		Last Modified: Wed, 04 Sep 2024 07:31:02 GMT  
		Size: 630.3 KB (630336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24cd4abfec65ee86b6e7bd5861d5543e3da7dafb92f20851aea5357dfa89434`  
		Last Modified: Wed, 04 Sep 2024 07:31:03 GMT  
		Size: 13.7 MB (13656630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce315a403531201e7db80d481aafa278bd2b73b77c24c5dac830b8736ef6a75`  
		Last Modified: Wed, 04 Sep 2024 07:31:02 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40395139ed67e33f42cbd9721d5a74dac2d9917914519da789686e6122be9579`  
		Last Modified: Wed, 04 Sep 2024 07:31:03 GMT  
		Size: 1.7 MB (1673588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f7073db196529ac226fa3fa25afd2cb96c0298b048397af4f32a61c8d163a4`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 7.4 MB (7403230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3182e9cb9a162ad5fc8ed2b1bb93e5ae69b4a371cd40055b321ec73be449e6e`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 20.6 MB (20561012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3016037b2ceaa72afbe6b3af6862693b2d462201dd7491bc761c2dd900b390`  
		Last Modified: Wed, 04 Sep 2024 09:43:16 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35827c7507295d2943fcceceaeada49dfe6114f767c09d53f773d2c8ae0f3163`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 2.1 KB (2141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-alpine3.19` - unknown; unknown

```console
$ docker pull satosa@sha256:0d5ed8afefec0046729989356a966a2baca01f83e0d253ae0cbe857f5b25e911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1192195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb71a3b25a30177e482a159536c84119f4731c59326a0ea5643027d47048bee9`

```dockerfile
```

-	Layers:
	-	`sha256:91aa376b5a5a0351d224b70755bd3f018eda925fbc7d8728275cb741623c08bb`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 1.2 MB (1167548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ddf12d3de38b8098769bbab9786e83ba03071f5f62fc4f03c9a5bbd8a40b9a9`  
		Last Modified: Wed, 04 Sep 2024 09:43:16 GMT  
		Size: 24.6 KB (24647 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8-alpine3.19` - linux; 386

```console
$ docker pull satosa@sha256:2d8cebf9b303562cec2ad131a00c16058682d35e6bd8c8373a6049c2da05fa50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72174501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dca95b05acd6caadc4d2d7296fd8b0f814308a8bb54f679533a64ebab3faef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b2801d1a66d8eb7d37ef8c9bd01ed316e098fb58aca389c7038cf904ab7229`  
		Last Modified: Fri, 06 Sep 2024 23:33:12 GMT  
		Size: 628.4 KB (628417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e8a05a75efec89d800448cf9a90e1fd959a798b05a8f51e395555b1d05c35f`  
		Last Modified: Fri, 06 Sep 2024 23:33:13 GMT  
		Size: 11.7 MB (11692995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5711feaa7d3d84fb482e82165b47257f80cf1c7983ba93ce546895b7d9e28f21`  
		Last Modified: Fri, 06 Sep 2024 23:33:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daa8fc3a87001de1178cb86c2f3a5fb7e0c2b59f148e985334303b078cc6b13`  
		Last Modified: Fri, 06 Sep 2024 23:33:13 GMT  
		Size: 1.7 MB (1673606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7b4e5c3f2ca385e6a13fb3370fe3f6b5b7fbb27b7e78dda4febbba65faa3ae`  
		Last Modified: Sat, 07 Sep 2024 00:14:59 GMT  
		Size: 9.7 MB (9739429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a844ba5a90453d5ad7c35d062ced6e7dd837a85671dba10cf6084eed5bb437c`  
		Last Modified: Sat, 07 Sep 2024 00:15:00 GMT  
		Size: 45.2 MB (45174127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba215f757c4dc05b9334c475e0b248836410f95ca5863da0d003a76632535a1`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 9.9 KB (9920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a6e89a4bf4c06ffa048e8cedd4b46ad59c9488eb85e10ebddda37a91119547`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-alpine3.19` - unknown; unknown

```console
$ docker pull satosa@sha256:5c89fc3ceec355fda8b70edc5043ef7d778ac8a14eeba4292a949b1cb2327e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1196870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64cf3af182ba3581f1e116de5945cb44af88663baf9613093c160e918a42baf`

```dockerfile
```

-	Layers:
	-	`sha256:90b86ed2cf30e8cdaad32f8211994587cdb407caf5196c21249a5f34b13b85dd`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 1.2 MB (1172748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2dc2205c70270528b883f21361c34d7e3293ee05096b63fa6a91d7c0be6ac47`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 24.1 KB (24122 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8-alpine3.19` - linux; ppc64le

```console
$ docker pull satosa@sha256:6eecae17d30f48b03013d1d14a9b85ad3dea43b7923802d32ea3fa169f663479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76592545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caecb8549d9061ef80f72b53699ea19949fb3468ebdd4fb08c708829a1e05b36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459c907a569b15590c9d09d1ce39e44a9fa42640c696731731c52d192bfd1842`  
		Last Modified: Wed, 04 Sep 2024 07:40:49 GMT  
		Size: 630.8 KB (630823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d605ef3d7805437512a36129b9d3fb98ea13cddaf3c648f0147ba73205aa8fb`  
		Last Modified: Wed, 04 Sep 2024 10:52:53 GMT  
		Size: 14.1 MB (14072296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca3a0f938f4ab832be7c9b54e21d39cb0b524c08c9ec96b391064e82e8631d5`  
		Last Modified: Wed, 04 Sep 2024 10:52:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad63210e30ceb3bec53e28d69a992fc0e9f5ba1671edc1342363a34bf791e6a`  
		Last Modified: Wed, 04 Sep 2024 10:52:53 GMT  
		Size: 1.7 MB (1673607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb55fe0b4d5ab4f6e38e6c402bd87fb52c91f2618745b6a66f3ea5180e2ef1a`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 9.9 MB (9918961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807f1e0c89922bd6eb55fe13fd897d48f74a874ef5df95b59aa61c5becac725b`  
		Last Modified: Wed, 04 Sep 2024 11:57:27 GMT  
		Size: 46.9 MB (46921424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f44aa855627fd8f485493cf04a1fe931385ef50ab1e8c0a79039488cf685256`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca0ca3cc5339094abd67f79e15bfea386376d3d2a52bcbbcd606c8d3e08b098`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-alpine3.19` - unknown; unknown

```console
$ docker pull satosa@sha256:b11392488a9554cedf95a8a01fba766787c14030bb9cf5a0ce3e7aba1ae245b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1192698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc0583b84240d78f45aed5c0632d199084849cf2aa75cea1b4fa5d4d7a6d7ee0`

```dockerfile
```

-	Layers:
	-	`sha256:f35c5753ebe494db7b440a6cf4b3dd4bd589e66ec185d01a909e8c1122073457`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 1.2 MB (1168412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:977c5235e7ee7677285f54387c067e63b90071463dba2480f48588b750a682f2`  
		Last Modified: Wed, 04 Sep 2024 11:57:24 GMT  
		Size: 24.3 KB (24286 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8-bookworm`

```console
$ docker pull satosa@sha256:9838f3edf179af20bee6c8ac3925bd3f36658a0f5862b3385a6c8f5fe2e618cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8-bookworm` - linux; amd64

```console
$ docker pull satosa@sha256:df7e89152d9cc4909c80222d415a397e9a8c744497036afe3e184f06dad836b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88862529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14675eb83676db6aee0c38ab053b5d50f3a6bef793a282c6c33034b02b85b8a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 14:40:43 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 14:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 14:40:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 14:40:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 14:40:43 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467daa3d4c8b6f3916948d9277922e51161a5d42c977631819a635d2fa9fb32e`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 3.5 MB (3511398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d51d0de90c323e22cf7900a0ee9185e1e3c185b3ed4fecd9202ae1534e60c7`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 11.7 MB (11724854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e6c34f2b20e314d433bf1d444a0c72dc1b27dc93964a4fc102a4dccd25e799`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab50b4ae9438decebef449b4afb727284fe0c8f9198b603c588fea80266eb13`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 1.8 MB (1751083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0db6c6dc89000cc270ec074bf74ed84465d3fd1b31b84cc16de60dcf4879395`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 21.5 MB (21455664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57f345912a7c877e65d8bfc4b29882cb71d9062d398118c452f731fa33ed2dc`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 21.3 MB (21280717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ff5e597a64fb5ca09139b8f7b787223bcd6a34d8c228040d6afe1440477dc7`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd0519cfa116902f9ae050b5fdf0bc57b64a5b5932a15b709fcc2c1951ecfae`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:5c2553b9ff9019842b9134cb7f6cce18e5ad03d85f5c55a6cad7e49beac6ee1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2613369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6aec6c918521cd245227d130ea8626b23153986c281c938525bfcccc1a3f4f`

```dockerfile
```

-	Layers:
	-	`sha256:7e79b6aa88d9313fa3e0221dbd224b5bf6ecf13806da95dd9247c869c98d75cd`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 2.6 MB (2589886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7feca4e51ca18ad4deb21d66b20093be3fc6c01600301d6036157791cce48a8d`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 23.5 KB (23483 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8-bookworm` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:34f580cda009c649a0081d1dd0149e1d5d02cee4c2544f0929854272eaec8f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88214898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4290484613fdccc82556b42425aa56e356902679ddc288bb26c46b07c14dd461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 14:40:43 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 14:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 14:40:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 14:40:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 14:40:43 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc0bb0f48368309a59f8f76a26a1a2aefa34ff474a1d5fc171b034e954d299b`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 3.3 MB (3331450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbb068a2dcf7bb59fec2a07a7fc7d2d77207313340abb2e7c0010a7660c74e1`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 11.7 MB (11697919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cccda67aa8cce65f16c17702f99d7ae53526c87fe6fd6df833321c206a1915`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31068c739a9608963613c12774e31ba8f0157b299cf8cad529aba9038a3d689d`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 1.8 MB (1751307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc99567289f026c220b3120e68f2d85a71232bbe55438455a3f5e660e87389c`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 21.3 MB (21297890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b36ce4c95930510899b0b5e3794aa799935d3c389646b558a56a26f050775a0`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 21.0 MB (20967460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b6a305f0626446c54a1e5c9a85be45e2c0848d78fffbea4e00d62319e58090`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c81978fdbec654b6eee497a378a0dd8655dab131976c1043e21b9b10947c537`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:47ec55d5a93a25674ccc46b0f4063e4ba39e098ea9cfae20f977e66a0e62e08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2616658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8a53b07362a51d5b4b640abbb68b92b09ec789662505cb6bd7a61909c2f134`

```dockerfile
```

-	Layers:
	-	`sha256:ab5fac2784df8870ecf5b0b5660c59db1821183005268be1c017eefb25d099ea`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 2.6 MB (2592706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c71e017aac0b41e1beff888e67cf43b0fe9f47727a15285186f9f711fb2c4c`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 24.0 KB (23952 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.4`

```console
$ docker pull satosa@sha256:9838f3edf179af20bee6c8ac3925bd3f36658a0f5862b3385a6c8f5fe2e618cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8.4` - linux; amd64

```console
$ docker pull satosa@sha256:df7e89152d9cc4909c80222d415a397e9a8c744497036afe3e184f06dad836b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88862529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14675eb83676db6aee0c38ab053b5d50f3a6bef793a282c6c33034b02b85b8a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 14:40:43 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 14:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 14:40:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 14:40:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 14:40:43 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467daa3d4c8b6f3916948d9277922e51161a5d42c977631819a635d2fa9fb32e`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 3.5 MB (3511398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d51d0de90c323e22cf7900a0ee9185e1e3c185b3ed4fecd9202ae1534e60c7`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 11.7 MB (11724854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e6c34f2b20e314d433bf1d444a0c72dc1b27dc93964a4fc102a4dccd25e799`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab50b4ae9438decebef449b4afb727284fe0c8f9198b603c588fea80266eb13`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 1.8 MB (1751083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0db6c6dc89000cc270ec074bf74ed84465d3fd1b31b84cc16de60dcf4879395`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 21.5 MB (21455664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57f345912a7c877e65d8bfc4b29882cb71d9062d398118c452f731fa33ed2dc`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 21.3 MB (21280717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ff5e597a64fb5ca09139b8f7b787223bcd6a34d8c228040d6afe1440477dc7`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd0519cfa116902f9ae050b5fdf0bc57b64a5b5932a15b709fcc2c1951ecfae`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4` - unknown; unknown

```console
$ docker pull satosa@sha256:5c2553b9ff9019842b9134cb7f6cce18e5ad03d85f5c55a6cad7e49beac6ee1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2613369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6aec6c918521cd245227d130ea8626b23153986c281c938525bfcccc1a3f4f`

```dockerfile
```

-	Layers:
	-	`sha256:7e79b6aa88d9313fa3e0221dbd224b5bf6ecf13806da95dd9247c869c98d75cd`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 2.6 MB (2589886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7feca4e51ca18ad4deb21d66b20093be3fc6c01600301d6036157791cce48a8d`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 23.5 KB (23483 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.4` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:34f580cda009c649a0081d1dd0149e1d5d02cee4c2544f0929854272eaec8f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88214898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4290484613fdccc82556b42425aa56e356902679ddc288bb26c46b07c14dd461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 14:40:43 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 14:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 14:40:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 14:40:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 14:40:43 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc0bb0f48368309a59f8f76a26a1a2aefa34ff474a1d5fc171b034e954d299b`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 3.3 MB (3331450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbb068a2dcf7bb59fec2a07a7fc7d2d77207313340abb2e7c0010a7660c74e1`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 11.7 MB (11697919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cccda67aa8cce65f16c17702f99d7ae53526c87fe6fd6df833321c206a1915`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31068c739a9608963613c12774e31ba8f0157b299cf8cad529aba9038a3d689d`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 1.8 MB (1751307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc99567289f026c220b3120e68f2d85a71232bbe55438455a3f5e660e87389c`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 21.3 MB (21297890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b36ce4c95930510899b0b5e3794aa799935d3c389646b558a56a26f050775a0`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 21.0 MB (20967460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b6a305f0626446c54a1e5c9a85be45e2c0848d78fffbea4e00d62319e58090`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c81978fdbec654b6eee497a378a0dd8655dab131976c1043e21b9b10947c537`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4` - unknown; unknown

```console
$ docker pull satosa@sha256:47ec55d5a93a25674ccc46b0f4063e4ba39e098ea9cfae20f977e66a0e62e08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2616658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8a53b07362a51d5b4b640abbb68b92b09ec789662505cb6bd7a61909c2f134`

```dockerfile
```

-	Layers:
	-	`sha256:ab5fac2784df8870ecf5b0b5660c59db1821183005268be1c017eefb25d099ea`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 2.6 MB (2592706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c71e017aac0b41e1beff888e67cf43b0fe9f47727a15285186f9f711fb2c4c`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 24.0 KB (23952 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.4-alpine`

```console
$ docker pull satosa@sha256:450fe7aed678967f2ecd2c0e9c6332e5e2b100d34adcfa8291ecb0faba12a91d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `satosa:8.4-alpine` - linux; amd64

```console
$ docker pull satosa@sha256:1d4a2004db2f2160b9293361adbe91483bbbcfafd770c82549d3c79cbd63859d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45787482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c88811c75113b8a4851925e08cc4b50d9514de6e2842e9eaab79c9680a83c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fe8821d8e937f4d18d66ed6c01512319f6369e39501aa040d545cddb26c012`  
		Last Modified: Fri, 06 Sep 2024 23:31:42 GMT  
		Size: 627.9 KB (627915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e73abbe668f9cf00602e624892cee4209b2bea1a95102c68b2057c7e0b3c57`  
		Last Modified: Fri, 06 Sep 2024 23:31:43 GMT  
		Size: 11.5 MB (11499904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd37ef32dbcc8362c68d13269033880dde7e11c41e37de2144c7489fe84d588`  
		Last Modified: Fri, 06 Sep 2024 23:31:42 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e183bebb85d6d6db6d0223f702bb07cfdb79b7f435fb9c1d0e43fb9022370a9`  
		Last Modified: Fri, 06 Sep 2024 23:31:43 GMT  
		Size: 1.7 MB (1673601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b17f050437f188171644ad503679b514d0019bea18044a12242ceb2fe6083e`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 7.4 MB (7409601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d878e1fb4ea01bcb258e5c2cd0eb96217339c4c051c4d4fd643683e476df9a4a`  
		Last Modified: Sat, 07 Sep 2024 00:08:55 GMT  
		Size: 21.1 MB (21144433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14c3f2db0ae337a9fc6e52f90c84de448c365301280a38020a17089961009b5`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f56a48a186a09d5a69eebebecf31b6bb438e02c3867154d01a13a24ca8f659a`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:ce6fd0561adb7c64976cb6fa979b8dc71b67c174924c5359a0d0900f96b5c321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1194106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54d256448b7680b09dce413cbbf5be25b70b9c315cfc9c61333ca2ff946849b`

```dockerfile
```

-	Layers:
	-	`sha256:7e11b81e6a698a0ed5df4bb58d79891397ecfb89a6dd90f7df37c37ef9e5a7a5`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 1.2 MB (1169929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2477e3630694ca6355ede795fa0ca290ddab4bb0ed90194dc82f36e2ab4b2f3b`  
		Last Modified: Sat, 07 Sep 2024 00:08:53 GMT  
		Size: 24.2 KB (24177 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.4-alpine` - linux; arm variant v7

```console
$ docker pull satosa@sha256:484750cdfd849cd77669cbe91f573bb799331e79c39145a45324ad01310c2204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72502585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c3b9ea495a1c6906a04b17ae1148f8ec4470b8364642894b5beb7c54dc3c2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aca995c8234bcb8cc3881779eb898cea97d1e1ae8d93dfc03230bc2b72cd58f`  
		Last Modified: Wed, 24 Jul 2024 10:02:21 GMT  
		Size: 628.0 KB (627989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06edd34be8b9ba5da915d801b435bfb90ed4c553da299b2edb6293bbef6cd86a`  
		Last Modified: Wed, 07 Aug 2024 22:21:25 GMT  
		Size: 10.7 MB (10656411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164f482cec3d411bf812c97570ac5c9cd9745c2358cb78bd766f07f01038b63c`  
		Last Modified: Wed, 07 Aug 2024 22:21:24 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00118344aaad7672000a959203f9ded1e7e1c7bffa1433954163611aba69da4`  
		Last Modified: Wed, 04 Sep 2024 06:48:01 GMT  
		Size: 1.7 MB (1673590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c8bf69c8012a63b0b5abd3d4a28a39b1aeaed68ffbefa760be087bdaeb807a`  
		Last Modified: Wed, 04 Sep 2024 08:25:22 GMT  
		Size: 11.3 MB (11271496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1221728f93d4c726ecb0f8bf748430dcadd7eacce6921dab6782a74002a17a`  
		Last Modified: Wed, 04 Sep 2024 08:25:23 GMT  
		Size: 45.3 MB (45333665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1918f04628471e1950a105722a4d0e74f6a5d737e48d3ff39a4c0499d4f802`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3dc36ddb010041b6560916f6d2ecbb8da960fd4b4420d7104cf2e9eae2e8dd6`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 2.1 KB (2148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:9a5e945adbc9012c9125b8e76e839c0211e790b7aadaed484f26c7f84ba22869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1194729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b02d8bf4abbc5d9e84d436d0bae2a84f79699f03a2be8c2ac2699db1204182`

```dockerfile
```

-	Layers:
	-	`sha256:5a0df6ee33dffff152bce8d3422e8602ad36252d7f2461d6fcea1e786db2daf4`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 1.2 MB (1170376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62dc3f905e9f0d597d487f8b3c213c95f3dfd1c6d4ff1c069c332bffa6c46d08`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 24.4 KB (24353 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.4-alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e22814a24e95ebc1f3d6544566d145352a96c1792f2365a16b9d306f576611b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47295578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeeb532d9cfb950d8b7acdbdbe8fd94d29d5120bdd40d9cf046295712ca8c1bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564a93de2c7019a622a4491382e14c5bdf5d7c23bd78c6f9f1c699f72e74fce`  
		Last Modified: Wed, 04 Sep 2024 07:31:02 GMT  
		Size: 630.3 KB (630336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24cd4abfec65ee86b6e7bd5861d5543e3da7dafb92f20851aea5357dfa89434`  
		Last Modified: Wed, 04 Sep 2024 07:31:03 GMT  
		Size: 13.7 MB (13656630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce315a403531201e7db80d481aafa278bd2b73b77c24c5dac830b8736ef6a75`  
		Last Modified: Wed, 04 Sep 2024 07:31:02 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40395139ed67e33f42cbd9721d5a74dac2d9917914519da789686e6122be9579`  
		Last Modified: Wed, 04 Sep 2024 07:31:03 GMT  
		Size: 1.7 MB (1673588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f7073db196529ac226fa3fa25afd2cb96c0298b048397af4f32a61c8d163a4`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 7.4 MB (7403230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3182e9cb9a162ad5fc8ed2b1bb93e5ae69b4a371cd40055b321ec73be449e6e`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 20.6 MB (20561012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3016037b2ceaa72afbe6b3af6862693b2d462201dd7491bc761c2dd900b390`  
		Last Modified: Wed, 04 Sep 2024 09:43:16 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35827c7507295d2943fcceceaeada49dfe6114f767c09d53f773d2c8ae0f3163`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 2.1 KB (2141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:0d5ed8afefec0046729989356a966a2baca01f83e0d253ae0cbe857f5b25e911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1192195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb71a3b25a30177e482a159536c84119f4731c59326a0ea5643027d47048bee9`

```dockerfile
```

-	Layers:
	-	`sha256:91aa376b5a5a0351d224b70755bd3f018eda925fbc7d8728275cb741623c08bb`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 1.2 MB (1167548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ddf12d3de38b8098769bbab9786e83ba03071f5f62fc4f03c9a5bbd8a40b9a9`  
		Last Modified: Wed, 04 Sep 2024 09:43:16 GMT  
		Size: 24.6 KB (24647 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.4-alpine` - linux; 386

```console
$ docker pull satosa@sha256:2d8cebf9b303562cec2ad131a00c16058682d35e6bd8c8373a6049c2da05fa50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72174501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dca95b05acd6caadc4d2d7296fd8b0f814308a8bb54f679533a64ebab3faef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b2801d1a66d8eb7d37ef8c9bd01ed316e098fb58aca389c7038cf904ab7229`  
		Last Modified: Fri, 06 Sep 2024 23:33:12 GMT  
		Size: 628.4 KB (628417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e8a05a75efec89d800448cf9a90e1fd959a798b05a8f51e395555b1d05c35f`  
		Last Modified: Fri, 06 Sep 2024 23:33:13 GMT  
		Size: 11.7 MB (11692995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5711feaa7d3d84fb482e82165b47257f80cf1c7983ba93ce546895b7d9e28f21`  
		Last Modified: Fri, 06 Sep 2024 23:33:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daa8fc3a87001de1178cb86c2f3a5fb7e0c2b59f148e985334303b078cc6b13`  
		Last Modified: Fri, 06 Sep 2024 23:33:13 GMT  
		Size: 1.7 MB (1673606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7b4e5c3f2ca385e6a13fb3370fe3f6b5b7fbb27b7e78dda4febbba65faa3ae`  
		Last Modified: Sat, 07 Sep 2024 00:14:59 GMT  
		Size: 9.7 MB (9739429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a844ba5a90453d5ad7c35d062ced6e7dd837a85671dba10cf6084eed5bb437c`  
		Last Modified: Sat, 07 Sep 2024 00:15:00 GMT  
		Size: 45.2 MB (45174127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba215f757c4dc05b9334c475e0b248836410f95ca5863da0d003a76632535a1`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 9.9 KB (9920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a6e89a4bf4c06ffa048e8cedd4b46ad59c9488eb85e10ebddda37a91119547`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:5c89fc3ceec355fda8b70edc5043ef7d778ac8a14eeba4292a949b1cb2327e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1196870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64cf3af182ba3581f1e116de5945cb44af88663baf9613093c160e918a42baf`

```dockerfile
```

-	Layers:
	-	`sha256:90b86ed2cf30e8cdaad32f8211994587cdb407caf5196c21249a5f34b13b85dd`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 1.2 MB (1172748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2dc2205c70270528b883f21361c34d7e3293ee05096b63fa6a91d7c0be6ac47`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 24.1 KB (24122 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.4-alpine` - linux; ppc64le

```console
$ docker pull satosa@sha256:6eecae17d30f48b03013d1d14a9b85ad3dea43b7923802d32ea3fa169f663479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76592545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caecb8549d9061ef80f72b53699ea19949fb3468ebdd4fb08c708829a1e05b36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459c907a569b15590c9d09d1ce39e44a9fa42640c696731731c52d192bfd1842`  
		Last Modified: Wed, 04 Sep 2024 07:40:49 GMT  
		Size: 630.8 KB (630823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d605ef3d7805437512a36129b9d3fb98ea13cddaf3c648f0147ba73205aa8fb`  
		Last Modified: Wed, 04 Sep 2024 10:52:53 GMT  
		Size: 14.1 MB (14072296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca3a0f938f4ab832be7c9b54e21d39cb0b524c08c9ec96b391064e82e8631d5`  
		Last Modified: Wed, 04 Sep 2024 10:52:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad63210e30ceb3bec53e28d69a992fc0e9f5ba1671edc1342363a34bf791e6a`  
		Last Modified: Wed, 04 Sep 2024 10:52:53 GMT  
		Size: 1.7 MB (1673607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb55fe0b4d5ab4f6e38e6c402bd87fb52c91f2618745b6a66f3ea5180e2ef1a`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 9.9 MB (9918961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807f1e0c89922bd6eb55fe13fd897d48f74a874ef5df95b59aa61c5becac725b`  
		Last Modified: Wed, 04 Sep 2024 11:57:27 GMT  
		Size: 46.9 MB (46921424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f44aa855627fd8f485493cf04a1fe931385ef50ab1e8c0a79039488cf685256`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca0ca3cc5339094abd67f79e15bfea386376d3d2a52bcbbcd606c8d3e08b098`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:b11392488a9554cedf95a8a01fba766787c14030bb9cf5a0ce3e7aba1ae245b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1192698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc0583b84240d78f45aed5c0632d199084849cf2aa75cea1b4fa5d4d7a6d7ee0`

```dockerfile
```

-	Layers:
	-	`sha256:f35c5753ebe494db7b440a6cf4b3dd4bd589e66ec185d01a909e8c1122073457`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 1.2 MB (1168412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:977c5235e7ee7677285f54387c067e63b90071463dba2480f48588b750a682f2`  
		Last Modified: Wed, 04 Sep 2024 11:57:24 GMT  
		Size: 24.3 KB (24286 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.4-alpine3.19`

```console
$ docker pull satosa@sha256:450fe7aed678967f2ecd2c0e9c6332e5e2b100d34adcfa8291ecb0faba12a91d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `satosa:8.4-alpine3.19` - linux; amd64

```console
$ docker pull satosa@sha256:1d4a2004db2f2160b9293361adbe91483bbbcfafd770c82549d3c79cbd63859d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45787482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c88811c75113b8a4851925e08cc4b50d9514de6e2842e9eaab79c9680a83c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fe8821d8e937f4d18d66ed6c01512319f6369e39501aa040d545cddb26c012`  
		Last Modified: Fri, 06 Sep 2024 23:31:42 GMT  
		Size: 627.9 KB (627915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e73abbe668f9cf00602e624892cee4209b2bea1a95102c68b2057c7e0b3c57`  
		Last Modified: Fri, 06 Sep 2024 23:31:43 GMT  
		Size: 11.5 MB (11499904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd37ef32dbcc8362c68d13269033880dde7e11c41e37de2144c7489fe84d588`  
		Last Modified: Fri, 06 Sep 2024 23:31:42 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e183bebb85d6d6db6d0223f702bb07cfdb79b7f435fb9c1d0e43fb9022370a9`  
		Last Modified: Fri, 06 Sep 2024 23:31:43 GMT  
		Size: 1.7 MB (1673601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b17f050437f188171644ad503679b514d0019bea18044a12242ceb2fe6083e`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 7.4 MB (7409601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d878e1fb4ea01bcb258e5c2cd0eb96217339c4c051c4d4fd643683e476df9a4a`  
		Last Modified: Sat, 07 Sep 2024 00:08:55 GMT  
		Size: 21.1 MB (21144433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14c3f2db0ae337a9fc6e52f90c84de448c365301280a38020a17089961009b5`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f56a48a186a09d5a69eebebecf31b6bb438e02c3867154d01a13a24ca8f659a`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4-alpine3.19` - unknown; unknown

```console
$ docker pull satosa@sha256:ce6fd0561adb7c64976cb6fa979b8dc71b67c174924c5359a0d0900f96b5c321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1194106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54d256448b7680b09dce413cbbf5be25b70b9c315cfc9c61333ca2ff946849b`

```dockerfile
```

-	Layers:
	-	`sha256:7e11b81e6a698a0ed5df4bb58d79891397ecfb89a6dd90f7df37c37ef9e5a7a5`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 1.2 MB (1169929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2477e3630694ca6355ede795fa0ca290ddab4bb0ed90194dc82f36e2ab4b2f3b`  
		Last Modified: Sat, 07 Sep 2024 00:08:53 GMT  
		Size: 24.2 KB (24177 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.4-alpine3.19` - linux; arm variant v7

```console
$ docker pull satosa@sha256:484750cdfd849cd77669cbe91f573bb799331e79c39145a45324ad01310c2204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72502585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c3b9ea495a1c6906a04b17ae1148f8ec4470b8364642894b5beb7c54dc3c2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aca995c8234bcb8cc3881779eb898cea97d1e1ae8d93dfc03230bc2b72cd58f`  
		Last Modified: Wed, 24 Jul 2024 10:02:21 GMT  
		Size: 628.0 KB (627989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06edd34be8b9ba5da915d801b435bfb90ed4c553da299b2edb6293bbef6cd86a`  
		Last Modified: Wed, 07 Aug 2024 22:21:25 GMT  
		Size: 10.7 MB (10656411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164f482cec3d411bf812c97570ac5c9cd9745c2358cb78bd766f07f01038b63c`  
		Last Modified: Wed, 07 Aug 2024 22:21:24 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00118344aaad7672000a959203f9ded1e7e1c7bffa1433954163611aba69da4`  
		Last Modified: Wed, 04 Sep 2024 06:48:01 GMT  
		Size: 1.7 MB (1673590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c8bf69c8012a63b0b5abd3d4a28a39b1aeaed68ffbefa760be087bdaeb807a`  
		Last Modified: Wed, 04 Sep 2024 08:25:22 GMT  
		Size: 11.3 MB (11271496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1221728f93d4c726ecb0f8bf748430dcadd7eacce6921dab6782a74002a17a`  
		Last Modified: Wed, 04 Sep 2024 08:25:23 GMT  
		Size: 45.3 MB (45333665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1918f04628471e1950a105722a4d0e74f6a5d737e48d3ff39a4c0499d4f802`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3dc36ddb010041b6560916f6d2ecbb8da960fd4b4420d7104cf2e9eae2e8dd6`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 2.1 KB (2148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4-alpine3.19` - unknown; unknown

```console
$ docker pull satosa@sha256:9a5e945adbc9012c9125b8e76e839c0211e790b7aadaed484f26c7f84ba22869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1194729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b02d8bf4abbc5d9e84d436d0bae2a84f79699f03a2be8c2ac2699db1204182`

```dockerfile
```

-	Layers:
	-	`sha256:5a0df6ee33dffff152bce8d3422e8602ad36252d7f2461d6fcea1e786db2daf4`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 1.2 MB (1170376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62dc3f905e9f0d597d487f8b3c213c95f3dfd1c6d4ff1c069c332bffa6c46d08`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 24.4 KB (24353 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.4-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e22814a24e95ebc1f3d6544566d145352a96c1792f2365a16b9d306f576611b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47295578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeeb532d9cfb950d8b7acdbdbe8fd94d29d5120bdd40d9cf046295712ca8c1bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564a93de2c7019a622a4491382e14c5bdf5d7c23bd78c6f9f1c699f72e74fce`  
		Last Modified: Wed, 04 Sep 2024 07:31:02 GMT  
		Size: 630.3 KB (630336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24cd4abfec65ee86b6e7bd5861d5543e3da7dafb92f20851aea5357dfa89434`  
		Last Modified: Wed, 04 Sep 2024 07:31:03 GMT  
		Size: 13.7 MB (13656630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce315a403531201e7db80d481aafa278bd2b73b77c24c5dac830b8736ef6a75`  
		Last Modified: Wed, 04 Sep 2024 07:31:02 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40395139ed67e33f42cbd9721d5a74dac2d9917914519da789686e6122be9579`  
		Last Modified: Wed, 04 Sep 2024 07:31:03 GMT  
		Size: 1.7 MB (1673588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f7073db196529ac226fa3fa25afd2cb96c0298b048397af4f32a61c8d163a4`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 7.4 MB (7403230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3182e9cb9a162ad5fc8ed2b1bb93e5ae69b4a371cd40055b321ec73be449e6e`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 20.6 MB (20561012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3016037b2ceaa72afbe6b3af6862693b2d462201dd7491bc761c2dd900b390`  
		Last Modified: Wed, 04 Sep 2024 09:43:16 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35827c7507295d2943fcceceaeada49dfe6114f767c09d53f773d2c8ae0f3163`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 2.1 KB (2141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4-alpine3.19` - unknown; unknown

```console
$ docker pull satosa@sha256:0d5ed8afefec0046729989356a966a2baca01f83e0d253ae0cbe857f5b25e911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1192195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb71a3b25a30177e482a159536c84119f4731c59326a0ea5643027d47048bee9`

```dockerfile
```

-	Layers:
	-	`sha256:91aa376b5a5a0351d224b70755bd3f018eda925fbc7d8728275cb741623c08bb`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 1.2 MB (1167548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ddf12d3de38b8098769bbab9786e83ba03071f5f62fc4f03c9a5bbd8a40b9a9`  
		Last Modified: Wed, 04 Sep 2024 09:43:16 GMT  
		Size: 24.6 KB (24647 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.4-alpine3.19` - linux; 386

```console
$ docker pull satosa@sha256:2d8cebf9b303562cec2ad131a00c16058682d35e6bd8c8373a6049c2da05fa50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72174501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dca95b05acd6caadc4d2d7296fd8b0f814308a8bb54f679533a64ebab3faef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b2801d1a66d8eb7d37ef8c9bd01ed316e098fb58aca389c7038cf904ab7229`  
		Last Modified: Fri, 06 Sep 2024 23:33:12 GMT  
		Size: 628.4 KB (628417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e8a05a75efec89d800448cf9a90e1fd959a798b05a8f51e395555b1d05c35f`  
		Last Modified: Fri, 06 Sep 2024 23:33:13 GMT  
		Size: 11.7 MB (11692995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5711feaa7d3d84fb482e82165b47257f80cf1c7983ba93ce546895b7d9e28f21`  
		Last Modified: Fri, 06 Sep 2024 23:33:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daa8fc3a87001de1178cb86c2f3a5fb7e0c2b59f148e985334303b078cc6b13`  
		Last Modified: Fri, 06 Sep 2024 23:33:13 GMT  
		Size: 1.7 MB (1673606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7b4e5c3f2ca385e6a13fb3370fe3f6b5b7fbb27b7e78dda4febbba65faa3ae`  
		Last Modified: Sat, 07 Sep 2024 00:14:59 GMT  
		Size: 9.7 MB (9739429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a844ba5a90453d5ad7c35d062ced6e7dd837a85671dba10cf6084eed5bb437c`  
		Last Modified: Sat, 07 Sep 2024 00:15:00 GMT  
		Size: 45.2 MB (45174127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba215f757c4dc05b9334c475e0b248836410f95ca5863da0d003a76632535a1`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 9.9 KB (9920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a6e89a4bf4c06ffa048e8cedd4b46ad59c9488eb85e10ebddda37a91119547`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4-alpine3.19` - unknown; unknown

```console
$ docker pull satosa@sha256:5c89fc3ceec355fda8b70edc5043ef7d778ac8a14eeba4292a949b1cb2327e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1196870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64cf3af182ba3581f1e116de5945cb44af88663baf9613093c160e918a42baf`

```dockerfile
```

-	Layers:
	-	`sha256:90b86ed2cf30e8cdaad32f8211994587cdb407caf5196c21249a5f34b13b85dd`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 1.2 MB (1172748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2dc2205c70270528b883f21361c34d7e3293ee05096b63fa6a91d7c0be6ac47`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 24.1 KB (24122 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.4-alpine3.19` - linux; ppc64le

```console
$ docker pull satosa@sha256:6eecae17d30f48b03013d1d14a9b85ad3dea43b7923802d32ea3fa169f663479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76592545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caecb8549d9061ef80f72b53699ea19949fb3468ebdd4fb08c708829a1e05b36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459c907a569b15590c9d09d1ce39e44a9fa42640c696731731c52d192bfd1842`  
		Last Modified: Wed, 04 Sep 2024 07:40:49 GMT  
		Size: 630.8 KB (630823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d605ef3d7805437512a36129b9d3fb98ea13cddaf3c648f0147ba73205aa8fb`  
		Last Modified: Wed, 04 Sep 2024 10:52:53 GMT  
		Size: 14.1 MB (14072296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca3a0f938f4ab832be7c9b54e21d39cb0b524c08c9ec96b391064e82e8631d5`  
		Last Modified: Wed, 04 Sep 2024 10:52:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad63210e30ceb3bec53e28d69a992fc0e9f5ba1671edc1342363a34bf791e6a`  
		Last Modified: Wed, 04 Sep 2024 10:52:53 GMT  
		Size: 1.7 MB (1673607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb55fe0b4d5ab4f6e38e6c402bd87fb52c91f2618745b6a66f3ea5180e2ef1a`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 9.9 MB (9918961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807f1e0c89922bd6eb55fe13fd897d48f74a874ef5df95b59aa61c5becac725b`  
		Last Modified: Wed, 04 Sep 2024 11:57:27 GMT  
		Size: 46.9 MB (46921424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f44aa855627fd8f485493cf04a1fe931385ef50ab1e8c0a79039488cf685256`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca0ca3cc5339094abd67f79e15bfea386376d3d2a52bcbbcd606c8d3e08b098`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4-alpine3.19` - unknown; unknown

```console
$ docker pull satosa@sha256:b11392488a9554cedf95a8a01fba766787c14030bb9cf5a0ce3e7aba1ae245b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1192698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc0583b84240d78f45aed5c0632d199084849cf2aa75cea1b4fa5d4d7a6d7ee0`

```dockerfile
```

-	Layers:
	-	`sha256:f35c5753ebe494db7b440a6cf4b3dd4bd589e66ec185d01a909e8c1122073457`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 1.2 MB (1168412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:977c5235e7ee7677285f54387c067e63b90071463dba2480f48588b750a682f2`  
		Last Modified: Wed, 04 Sep 2024 11:57:24 GMT  
		Size: 24.3 KB (24286 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.4-bookworm`

```console
$ docker pull satosa@sha256:9838f3edf179af20bee6c8ac3925bd3f36658a0f5862b3385a6c8f5fe2e618cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8.4-bookworm` - linux; amd64

```console
$ docker pull satosa@sha256:df7e89152d9cc4909c80222d415a397e9a8c744497036afe3e184f06dad836b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88862529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14675eb83676db6aee0c38ab053b5d50f3a6bef793a282c6c33034b02b85b8a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 14:40:43 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 14:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 14:40:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 14:40:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 14:40:43 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467daa3d4c8b6f3916948d9277922e51161a5d42c977631819a635d2fa9fb32e`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 3.5 MB (3511398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d51d0de90c323e22cf7900a0ee9185e1e3c185b3ed4fecd9202ae1534e60c7`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 11.7 MB (11724854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e6c34f2b20e314d433bf1d444a0c72dc1b27dc93964a4fc102a4dccd25e799`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab50b4ae9438decebef449b4afb727284fe0c8f9198b603c588fea80266eb13`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 1.8 MB (1751083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0db6c6dc89000cc270ec074bf74ed84465d3fd1b31b84cc16de60dcf4879395`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 21.5 MB (21455664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57f345912a7c877e65d8bfc4b29882cb71d9062d398118c452f731fa33ed2dc`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 21.3 MB (21280717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ff5e597a64fb5ca09139b8f7b787223bcd6a34d8c228040d6afe1440477dc7`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd0519cfa116902f9ae050b5fdf0bc57b64a5b5932a15b709fcc2c1951ecfae`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:5c2553b9ff9019842b9134cb7f6cce18e5ad03d85f5c55a6cad7e49beac6ee1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2613369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6aec6c918521cd245227d130ea8626b23153986c281c938525bfcccc1a3f4f`

```dockerfile
```

-	Layers:
	-	`sha256:7e79b6aa88d9313fa3e0221dbd224b5bf6ecf13806da95dd9247c869c98d75cd`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 2.6 MB (2589886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7feca4e51ca18ad4deb21d66b20093be3fc6c01600301d6036157791cce48a8d`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 23.5 KB (23483 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.4-bookworm` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:34f580cda009c649a0081d1dd0149e1d5d02cee4c2544f0929854272eaec8f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88214898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4290484613fdccc82556b42425aa56e356902679ddc288bb26c46b07c14dd461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 14:40:43 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 14:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 14:40:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 14:40:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 14:40:43 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc0bb0f48368309a59f8f76a26a1a2aefa34ff474a1d5fc171b034e954d299b`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 3.3 MB (3331450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbb068a2dcf7bb59fec2a07a7fc7d2d77207313340abb2e7c0010a7660c74e1`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 11.7 MB (11697919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cccda67aa8cce65f16c17702f99d7ae53526c87fe6fd6df833321c206a1915`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31068c739a9608963613c12774e31ba8f0157b299cf8cad529aba9038a3d689d`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 1.8 MB (1751307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc99567289f026c220b3120e68f2d85a71232bbe55438455a3f5e660e87389c`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 21.3 MB (21297890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b36ce4c95930510899b0b5e3794aa799935d3c389646b558a56a26f050775a0`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 21.0 MB (20967460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b6a305f0626446c54a1e5c9a85be45e2c0848d78fffbea4e00d62319e58090`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c81978fdbec654b6eee497a378a0dd8655dab131976c1043e21b9b10947c537`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:47ec55d5a93a25674ccc46b0f4063e4ba39e098ea9cfae20f977e66a0e62e08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2616658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8a53b07362a51d5b4b640abbb68b92b09ec789662505cb6bd7a61909c2f134`

```dockerfile
```

-	Layers:
	-	`sha256:ab5fac2784df8870ecf5b0b5660c59db1821183005268be1c017eefb25d099ea`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 2.6 MB (2592706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c71e017aac0b41e1beff888e67cf43b0fe9f47727a15285186f9f711fb2c4c`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 24.0 KB (23952 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.4.0`

```console
$ docker pull satosa@sha256:9838f3edf179af20bee6c8ac3925bd3f36658a0f5862b3385a6c8f5fe2e618cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8.4.0` - linux; amd64

```console
$ docker pull satosa@sha256:df7e89152d9cc4909c80222d415a397e9a8c744497036afe3e184f06dad836b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88862529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14675eb83676db6aee0c38ab053b5d50f3a6bef793a282c6c33034b02b85b8a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 14:40:43 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 14:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 14:40:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 14:40:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 14:40:43 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467daa3d4c8b6f3916948d9277922e51161a5d42c977631819a635d2fa9fb32e`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 3.5 MB (3511398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d51d0de90c323e22cf7900a0ee9185e1e3c185b3ed4fecd9202ae1534e60c7`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 11.7 MB (11724854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e6c34f2b20e314d433bf1d444a0c72dc1b27dc93964a4fc102a4dccd25e799`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab50b4ae9438decebef449b4afb727284fe0c8f9198b603c588fea80266eb13`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 1.8 MB (1751083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0db6c6dc89000cc270ec074bf74ed84465d3fd1b31b84cc16de60dcf4879395`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 21.5 MB (21455664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57f345912a7c877e65d8bfc4b29882cb71d9062d398118c452f731fa33ed2dc`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 21.3 MB (21280717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ff5e597a64fb5ca09139b8f7b787223bcd6a34d8c228040d6afe1440477dc7`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd0519cfa116902f9ae050b5fdf0bc57b64a5b5932a15b709fcc2c1951ecfae`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4.0` - unknown; unknown

```console
$ docker pull satosa@sha256:5c2553b9ff9019842b9134cb7f6cce18e5ad03d85f5c55a6cad7e49beac6ee1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2613369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6aec6c918521cd245227d130ea8626b23153986c281c938525bfcccc1a3f4f`

```dockerfile
```

-	Layers:
	-	`sha256:7e79b6aa88d9313fa3e0221dbd224b5bf6ecf13806da95dd9247c869c98d75cd`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 2.6 MB (2589886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7feca4e51ca18ad4deb21d66b20093be3fc6c01600301d6036157791cce48a8d`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 23.5 KB (23483 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.4.0` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:34f580cda009c649a0081d1dd0149e1d5d02cee4c2544f0929854272eaec8f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88214898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4290484613fdccc82556b42425aa56e356902679ddc288bb26c46b07c14dd461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 14:40:43 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 14:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 14:40:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 14:40:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 14:40:43 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc0bb0f48368309a59f8f76a26a1a2aefa34ff474a1d5fc171b034e954d299b`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 3.3 MB (3331450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbb068a2dcf7bb59fec2a07a7fc7d2d77207313340abb2e7c0010a7660c74e1`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 11.7 MB (11697919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cccda67aa8cce65f16c17702f99d7ae53526c87fe6fd6df833321c206a1915`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31068c739a9608963613c12774e31ba8f0157b299cf8cad529aba9038a3d689d`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 1.8 MB (1751307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc99567289f026c220b3120e68f2d85a71232bbe55438455a3f5e660e87389c`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 21.3 MB (21297890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b36ce4c95930510899b0b5e3794aa799935d3c389646b558a56a26f050775a0`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 21.0 MB (20967460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b6a305f0626446c54a1e5c9a85be45e2c0848d78fffbea4e00d62319e58090`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c81978fdbec654b6eee497a378a0dd8655dab131976c1043e21b9b10947c537`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4.0` - unknown; unknown

```console
$ docker pull satosa@sha256:47ec55d5a93a25674ccc46b0f4063e4ba39e098ea9cfae20f977e66a0e62e08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2616658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8a53b07362a51d5b4b640abbb68b92b09ec789662505cb6bd7a61909c2f134`

```dockerfile
```

-	Layers:
	-	`sha256:ab5fac2784df8870ecf5b0b5660c59db1821183005268be1c017eefb25d099ea`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 2.6 MB (2592706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c71e017aac0b41e1beff888e67cf43b0fe9f47727a15285186f9f711fb2c4c`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 24.0 KB (23952 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.4.0-alpine`

```console
$ docker pull satosa@sha256:450fe7aed678967f2ecd2c0e9c6332e5e2b100d34adcfa8291ecb0faba12a91d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `satosa:8.4.0-alpine` - linux; amd64

```console
$ docker pull satosa@sha256:1d4a2004db2f2160b9293361adbe91483bbbcfafd770c82549d3c79cbd63859d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45787482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c88811c75113b8a4851925e08cc4b50d9514de6e2842e9eaab79c9680a83c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fe8821d8e937f4d18d66ed6c01512319f6369e39501aa040d545cddb26c012`  
		Last Modified: Fri, 06 Sep 2024 23:31:42 GMT  
		Size: 627.9 KB (627915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e73abbe668f9cf00602e624892cee4209b2bea1a95102c68b2057c7e0b3c57`  
		Last Modified: Fri, 06 Sep 2024 23:31:43 GMT  
		Size: 11.5 MB (11499904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd37ef32dbcc8362c68d13269033880dde7e11c41e37de2144c7489fe84d588`  
		Last Modified: Fri, 06 Sep 2024 23:31:42 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e183bebb85d6d6db6d0223f702bb07cfdb79b7f435fb9c1d0e43fb9022370a9`  
		Last Modified: Fri, 06 Sep 2024 23:31:43 GMT  
		Size: 1.7 MB (1673601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b17f050437f188171644ad503679b514d0019bea18044a12242ceb2fe6083e`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 7.4 MB (7409601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d878e1fb4ea01bcb258e5c2cd0eb96217339c4c051c4d4fd643683e476df9a4a`  
		Last Modified: Sat, 07 Sep 2024 00:08:55 GMT  
		Size: 21.1 MB (21144433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14c3f2db0ae337a9fc6e52f90c84de448c365301280a38020a17089961009b5`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f56a48a186a09d5a69eebebecf31b6bb438e02c3867154d01a13a24ca8f659a`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4.0-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:ce6fd0561adb7c64976cb6fa979b8dc71b67c174924c5359a0d0900f96b5c321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1194106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54d256448b7680b09dce413cbbf5be25b70b9c315cfc9c61333ca2ff946849b`

```dockerfile
```

-	Layers:
	-	`sha256:7e11b81e6a698a0ed5df4bb58d79891397ecfb89a6dd90f7df37c37ef9e5a7a5`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 1.2 MB (1169929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2477e3630694ca6355ede795fa0ca290ddab4bb0ed90194dc82f36e2ab4b2f3b`  
		Last Modified: Sat, 07 Sep 2024 00:08:53 GMT  
		Size: 24.2 KB (24177 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.4.0-alpine` - linux; arm variant v7

```console
$ docker pull satosa@sha256:484750cdfd849cd77669cbe91f573bb799331e79c39145a45324ad01310c2204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72502585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c3b9ea495a1c6906a04b17ae1148f8ec4470b8364642894b5beb7c54dc3c2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aca995c8234bcb8cc3881779eb898cea97d1e1ae8d93dfc03230bc2b72cd58f`  
		Last Modified: Wed, 24 Jul 2024 10:02:21 GMT  
		Size: 628.0 KB (627989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06edd34be8b9ba5da915d801b435bfb90ed4c553da299b2edb6293bbef6cd86a`  
		Last Modified: Wed, 07 Aug 2024 22:21:25 GMT  
		Size: 10.7 MB (10656411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164f482cec3d411bf812c97570ac5c9cd9745c2358cb78bd766f07f01038b63c`  
		Last Modified: Wed, 07 Aug 2024 22:21:24 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00118344aaad7672000a959203f9ded1e7e1c7bffa1433954163611aba69da4`  
		Last Modified: Wed, 04 Sep 2024 06:48:01 GMT  
		Size: 1.7 MB (1673590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c8bf69c8012a63b0b5abd3d4a28a39b1aeaed68ffbefa760be087bdaeb807a`  
		Last Modified: Wed, 04 Sep 2024 08:25:22 GMT  
		Size: 11.3 MB (11271496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1221728f93d4c726ecb0f8bf748430dcadd7eacce6921dab6782a74002a17a`  
		Last Modified: Wed, 04 Sep 2024 08:25:23 GMT  
		Size: 45.3 MB (45333665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1918f04628471e1950a105722a4d0e74f6a5d737e48d3ff39a4c0499d4f802`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3dc36ddb010041b6560916f6d2ecbb8da960fd4b4420d7104cf2e9eae2e8dd6`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 2.1 KB (2148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4.0-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:9a5e945adbc9012c9125b8e76e839c0211e790b7aadaed484f26c7f84ba22869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1194729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b02d8bf4abbc5d9e84d436d0bae2a84f79699f03a2be8c2ac2699db1204182`

```dockerfile
```

-	Layers:
	-	`sha256:5a0df6ee33dffff152bce8d3422e8602ad36252d7f2461d6fcea1e786db2daf4`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 1.2 MB (1170376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62dc3f905e9f0d597d487f8b3c213c95f3dfd1c6d4ff1c069c332bffa6c46d08`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 24.4 KB (24353 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.4.0-alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e22814a24e95ebc1f3d6544566d145352a96c1792f2365a16b9d306f576611b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47295578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeeb532d9cfb950d8b7acdbdbe8fd94d29d5120bdd40d9cf046295712ca8c1bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564a93de2c7019a622a4491382e14c5bdf5d7c23bd78c6f9f1c699f72e74fce`  
		Last Modified: Wed, 04 Sep 2024 07:31:02 GMT  
		Size: 630.3 KB (630336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24cd4abfec65ee86b6e7bd5861d5543e3da7dafb92f20851aea5357dfa89434`  
		Last Modified: Wed, 04 Sep 2024 07:31:03 GMT  
		Size: 13.7 MB (13656630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce315a403531201e7db80d481aafa278bd2b73b77c24c5dac830b8736ef6a75`  
		Last Modified: Wed, 04 Sep 2024 07:31:02 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40395139ed67e33f42cbd9721d5a74dac2d9917914519da789686e6122be9579`  
		Last Modified: Wed, 04 Sep 2024 07:31:03 GMT  
		Size: 1.7 MB (1673588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f7073db196529ac226fa3fa25afd2cb96c0298b048397af4f32a61c8d163a4`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 7.4 MB (7403230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3182e9cb9a162ad5fc8ed2b1bb93e5ae69b4a371cd40055b321ec73be449e6e`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 20.6 MB (20561012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3016037b2ceaa72afbe6b3af6862693b2d462201dd7491bc761c2dd900b390`  
		Last Modified: Wed, 04 Sep 2024 09:43:16 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35827c7507295d2943fcceceaeada49dfe6114f767c09d53f773d2c8ae0f3163`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 2.1 KB (2141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4.0-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:0d5ed8afefec0046729989356a966a2baca01f83e0d253ae0cbe857f5b25e911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1192195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb71a3b25a30177e482a159536c84119f4731c59326a0ea5643027d47048bee9`

```dockerfile
```

-	Layers:
	-	`sha256:91aa376b5a5a0351d224b70755bd3f018eda925fbc7d8728275cb741623c08bb`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 1.2 MB (1167548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ddf12d3de38b8098769bbab9786e83ba03071f5f62fc4f03c9a5bbd8a40b9a9`  
		Last Modified: Wed, 04 Sep 2024 09:43:16 GMT  
		Size: 24.6 KB (24647 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.4.0-alpine` - linux; 386

```console
$ docker pull satosa@sha256:2d8cebf9b303562cec2ad131a00c16058682d35e6bd8c8373a6049c2da05fa50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72174501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dca95b05acd6caadc4d2d7296fd8b0f814308a8bb54f679533a64ebab3faef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b2801d1a66d8eb7d37ef8c9bd01ed316e098fb58aca389c7038cf904ab7229`  
		Last Modified: Fri, 06 Sep 2024 23:33:12 GMT  
		Size: 628.4 KB (628417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e8a05a75efec89d800448cf9a90e1fd959a798b05a8f51e395555b1d05c35f`  
		Last Modified: Fri, 06 Sep 2024 23:33:13 GMT  
		Size: 11.7 MB (11692995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5711feaa7d3d84fb482e82165b47257f80cf1c7983ba93ce546895b7d9e28f21`  
		Last Modified: Fri, 06 Sep 2024 23:33:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daa8fc3a87001de1178cb86c2f3a5fb7e0c2b59f148e985334303b078cc6b13`  
		Last Modified: Fri, 06 Sep 2024 23:33:13 GMT  
		Size: 1.7 MB (1673606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7b4e5c3f2ca385e6a13fb3370fe3f6b5b7fbb27b7e78dda4febbba65faa3ae`  
		Last Modified: Sat, 07 Sep 2024 00:14:59 GMT  
		Size: 9.7 MB (9739429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a844ba5a90453d5ad7c35d062ced6e7dd837a85671dba10cf6084eed5bb437c`  
		Last Modified: Sat, 07 Sep 2024 00:15:00 GMT  
		Size: 45.2 MB (45174127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba215f757c4dc05b9334c475e0b248836410f95ca5863da0d003a76632535a1`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 9.9 KB (9920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a6e89a4bf4c06ffa048e8cedd4b46ad59c9488eb85e10ebddda37a91119547`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4.0-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:5c89fc3ceec355fda8b70edc5043ef7d778ac8a14eeba4292a949b1cb2327e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1196870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64cf3af182ba3581f1e116de5945cb44af88663baf9613093c160e918a42baf`

```dockerfile
```

-	Layers:
	-	`sha256:90b86ed2cf30e8cdaad32f8211994587cdb407caf5196c21249a5f34b13b85dd`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 1.2 MB (1172748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2dc2205c70270528b883f21361c34d7e3293ee05096b63fa6a91d7c0be6ac47`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 24.1 KB (24122 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.4.0-alpine` - linux; ppc64le

```console
$ docker pull satosa@sha256:6eecae17d30f48b03013d1d14a9b85ad3dea43b7923802d32ea3fa169f663479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76592545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caecb8549d9061ef80f72b53699ea19949fb3468ebdd4fb08c708829a1e05b36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459c907a569b15590c9d09d1ce39e44a9fa42640c696731731c52d192bfd1842`  
		Last Modified: Wed, 04 Sep 2024 07:40:49 GMT  
		Size: 630.8 KB (630823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d605ef3d7805437512a36129b9d3fb98ea13cddaf3c648f0147ba73205aa8fb`  
		Last Modified: Wed, 04 Sep 2024 10:52:53 GMT  
		Size: 14.1 MB (14072296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca3a0f938f4ab832be7c9b54e21d39cb0b524c08c9ec96b391064e82e8631d5`  
		Last Modified: Wed, 04 Sep 2024 10:52:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad63210e30ceb3bec53e28d69a992fc0e9f5ba1671edc1342363a34bf791e6a`  
		Last Modified: Wed, 04 Sep 2024 10:52:53 GMT  
		Size: 1.7 MB (1673607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb55fe0b4d5ab4f6e38e6c402bd87fb52c91f2618745b6a66f3ea5180e2ef1a`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 9.9 MB (9918961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807f1e0c89922bd6eb55fe13fd897d48f74a874ef5df95b59aa61c5becac725b`  
		Last Modified: Wed, 04 Sep 2024 11:57:27 GMT  
		Size: 46.9 MB (46921424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f44aa855627fd8f485493cf04a1fe931385ef50ab1e8c0a79039488cf685256`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca0ca3cc5339094abd67f79e15bfea386376d3d2a52bcbbcd606c8d3e08b098`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4.0-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:b11392488a9554cedf95a8a01fba766787c14030bb9cf5a0ce3e7aba1ae245b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1192698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc0583b84240d78f45aed5c0632d199084849cf2aa75cea1b4fa5d4d7a6d7ee0`

```dockerfile
```

-	Layers:
	-	`sha256:f35c5753ebe494db7b440a6cf4b3dd4bd589e66ec185d01a909e8c1122073457`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 1.2 MB (1168412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:977c5235e7ee7677285f54387c067e63b90071463dba2480f48588b750a682f2`  
		Last Modified: Wed, 04 Sep 2024 11:57:24 GMT  
		Size: 24.3 KB (24286 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.4.0-alpine3.19`

```console
$ docker pull satosa@sha256:450fe7aed678967f2ecd2c0e9c6332e5e2b100d34adcfa8291ecb0faba12a91d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `satosa:8.4.0-alpine3.19` - linux; amd64

```console
$ docker pull satosa@sha256:1d4a2004db2f2160b9293361adbe91483bbbcfafd770c82549d3c79cbd63859d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45787482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c88811c75113b8a4851925e08cc4b50d9514de6e2842e9eaab79c9680a83c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fe8821d8e937f4d18d66ed6c01512319f6369e39501aa040d545cddb26c012`  
		Last Modified: Fri, 06 Sep 2024 23:31:42 GMT  
		Size: 627.9 KB (627915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e73abbe668f9cf00602e624892cee4209b2bea1a95102c68b2057c7e0b3c57`  
		Last Modified: Fri, 06 Sep 2024 23:31:43 GMT  
		Size: 11.5 MB (11499904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd37ef32dbcc8362c68d13269033880dde7e11c41e37de2144c7489fe84d588`  
		Last Modified: Fri, 06 Sep 2024 23:31:42 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e183bebb85d6d6db6d0223f702bb07cfdb79b7f435fb9c1d0e43fb9022370a9`  
		Last Modified: Fri, 06 Sep 2024 23:31:43 GMT  
		Size: 1.7 MB (1673601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b17f050437f188171644ad503679b514d0019bea18044a12242ceb2fe6083e`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 7.4 MB (7409601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d878e1fb4ea01bcb258e5c2cd0eb96217339c4c051c4d4fd643683e476df9a4a`  
		Last Modified: Sat, 07 Sep 2024 00:08:55 GMT  
		Size: 21.1 MB (21144433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14c3f2db0ae337a9fc6e52f90c84de448c365301280a38020a17089961009b5`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f56a48a186a09d5a69eebebecf31b6bb438e02c3867154d01a13a24ca8f659a`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4.0-alpine3.19` - unknown; unknown

```console
$ docker pull satosa@sha256:ce6fd0561adb7c64976cb6fa979b8dc71b67c174924c5359a0d0900f96b5c321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1194106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54d256448b7680b09dce413cbbf5be25b70b9c315cfc9c61333ca2ff946849b`

```dockerfile
```

-	Layers:
	-	`sha256:7e11b81e6a698a0ed5df4bb58d79891397ecfb89a6dd90f7df37c37ef9e5a7a5`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 1.2 MB (1169929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2477e3630694ca6355ede795fa0ca290ddab4bb0ed90194dc82f36e2ab4b2f3b`  
		Last Modified: Sat, 07 Sep 2024 00:08:53 GMT  
		Size: 24.2 KB (24177 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.4.0-alpine3.19` - linux; arm variant v7

```console
$ docker pull satosa@sha256:484750cdfd849cd77669cbe91f573bb799331e79c39145a45324ad01310c2204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72502585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c3b9ea495a1c6906a04b17ae1148f8ec4470b8364642894b5beb7c54dc3c2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aca995c8234bcb8cc3881779eb898cea97d1e1ae8d93dfc03230bc2b72cd58f`  
		Last Modified: Wed, 24 Jul 2024 10:02:21 GMT  
		Size: 628.0 KB (627989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06edd34be8b9ba5da915d801b435bfb90ed4c553da299b2edb6293bbef6cd86a`  
		Last Modified: Wed, 07 Aug 2024 22:21:25 GMT  
		Size: 10.7 MB (10656411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164f482cec3d411bf812c97570ac5c9cd9745c2358cb78bd766f07f01038b63c`  
		Last Modified: Wed, 07 Aug 2024 22:21:24 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00118344aaad7672000a959203f9ded1e7e1c7bffa1433954163611aba69da4`  
		Last Modified: Wed, 04 Sep 2024 06:48:01 GMT  
		Size: 1.7 MB (1673590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c8bf69c8012a63b0b5abd3d4a28a39b1aeaed68ffbefa760be087bdaeb807a`  
		Last Modified: Wed, 04 Sep 2024 08:25:22 GMT  
		Size: 11.3 MB (11271496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1221728f93d4c726ecb0f8bf748430dcadd7eacce6921dab6782a74002a17a`  
		Last Modified: Wed, 04 Sep 2024 08:25:23 GMT  
		Size: 45.3 MB (45333665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1918f04628471e1950a105722a4d0e74f6a5d737e48d3ff39a4c0499d4f802`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3dc36ddb010041b6560916f6d2ecbb8da960fd4b4420d7104cf2e9eae2e8dd6`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 2.1 KB (2148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4.0-alpine3.19` - unknown; unknown

```console
$ docker pull satosa@sha256:9a5e945adbc9012c9125b8e76e839c0211e790b7aadaed484f26c7f84ba22869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1194729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b02d8bf4abbc5d9e84d436d0bae2a84f79699f03a2be8c2ac2699db1204182`

```dockerfile
```

-	Layers:
	-	`sha256:5a0df6ee33dffff152bce8d3422e8602ad36252d7f2461d6fcea1e786db2daf4`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 1.2 MB (1170376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62dc3f905e9f0d597d487f8b3c213c95f3dfd1c6d4ff1c069c332bffa6c46d08`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 24.4 KB (24353 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.4.0-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e22814a24e95ebc1f3d6544566d145352a96c1792f2365a16b9d306f576611b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47295578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeeb532d9cfb950d8b7acdbdbe8fd94d29d5120bdd40d9cf046295712ca8c1bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564a93de2c7019a622a4491382e14c5bdf5d7c23bd78c6f9f1c699f72e74fce`  
		Last Modified: Wed, 04 Sep 2024 07:31:02 GMT  
		Size: 630.3 KB (630336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24cd4abfec65ee86b6e7bd5861d5543e3da7dafb92f20851aea5357dfa89434`  
		Last Modified: Wed, 04 Sep 2024 07:31:03 GMT  
		Size: 13.7 MB (13656630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce315a403531201e7db80d481aafa278bd2b73b77c24c5dac830b8736ef6a75`  
		Last Modified: Wed, 04 Sep 2024 07:31:02 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40395139ed67e33f42cbd9721d5a74dac2d9917914519da789686e6122be9579`  
		Last Modified: Wed, 04 Sep 2024 07:31:03 GMT  
		Size: 1.7 MB (1673588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f7073db196529ac226fa3fa25afd2cb96c0298b048397af4f32a61c8d163a4`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 7.4 MB (7403230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3182e9cb9a162ad5fc8ed2b1bb93e5ae69b4a371cd40055b321ec73be449e6e`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 20.6 MB (20561012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3016037b2ceaa72afbe6b3af6862693b2d462201dd7491bc761c2dd900b390`  
		Last Modified: Wed, 04 Sep 2024 09:43:16 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35827c7507295d2943fcceceaeada49dfe6114f767c09d53f773d2c8ae0f3163`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 2.1 KB (2141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4.0-alpine3.19` - unknown; unknown

```console
$ docker pull satosa@sha256:0d5ed8afefec0046729989356a966a2baca01f83e0d253ae0cbe857f5b25e911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1192195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb71a3b25a30177e482a159536c84119f4731c59326a0ea5643027d47048bee9`

```dockerfile
```

-	Layers:
	-	`sha256:91aa376b5a5a0351d224b70755bd3f018eda925fbc7d8728275cb741623c08bb`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 1.2 MB (1167548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ddf12d3de38b8098769bbab9786e83ba03071f5f62fc4f03c9a5bbd8a40b9a9`  
		Last Modified: Wed, 04 Sep 2024 09:43:16 GMT  
		Size: 24.6 KB (24647 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.4.0-alpine3.19` - linux; 386

```console
$ docker pull satosa@sha256:2d8cebf9b303562cec2ad131a00c16058682d35e6bd8c8373a6049c2da05fa50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72174501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dca95b05acd6caadc4d2d7296fd8b0f814308a8bb54f679533a64ebab3faef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b2801d1a66d8eb7d37ef8c9bd01ed316e098fb58aca389c7038cf904ab7229`  
		Last Modified: Fri, 06 Sep 2024 23:33:12 GMT  
		Size: 628.4 KB (628417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e8a05a75efec89d800448cf9a90e1fd959a798b05a8f51e395555b1d05c35f`  
		Last Modified: Fri, 06 Sep 2024 23:33:13 GMT  
		Size: 11.7 MB (11692995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5711feaa7d3d84fb482e82165b47257f80cf1c7983ba93ce546895b7d9e28f21`  
		Last Modified: Fri, 06 Sep 2024 23:33:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daa8fc3a87001de1178cb86c2f3a5fb7e0c2b59f148e985334303b078cc6b13`  
		Last Modified: Fri, 06 Sep 2024 23:33:13 GMT  
		Size: 1.7 MB (1673606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7b4e5c3f2ca385e6a13fb3370fe3f6b5b7fbb27b7e78dda4febbba65faa3ae`  
		Last Modified: Sat, 07 Sep 2024 00:14:59 GMT  
		Size: 9.7 MB (9739429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a844ba5a90453d5ad7c35d062ced6e7dd837a85671dba10cf6084eed5bb437c`  
		Last Modified: Sat, 07 Sep 2024 00:15:00 GMT  
		Size: 45.2 MB (45174127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba215f757c4dc05b9334c475e0b248836410f95ca5863da0d003a76632535a1`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 9.9 KB (9920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a6e89a4bf4c06ffa048e8cedd4b46ad59c9488eb85e10ebddda37a91119547`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4.0-alpine3.19` - unknown; unknown

```console
$ docker pull satosa@sha256:5c89fc3ceec355fda8b70edc5043ef7d778ac8a14eeba4292a949b1cb2327e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1196870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64cf3af182ba3581f1e116de5945cb44af88663baf9613093c160e918a42baf`

```dockerfile
```

-	Layers:
	-	`sha256:90b86ed2cf30e8cdaad32f8211994587cdb407caf5196c21249a5f34b13b85dd`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 1.2 MB (1172748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2dc2205c70270528b883f21361c34d7e3293ee05096b63fa6a91d7c0be6ac47`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 24.1 KB (24122 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.4.0-alpine3.19` - linux; ppc64le

```console
$ docker pull satosa@sha256:6eecae17d30f48b03013d1d14a9b85ad3dea43b7923802d32ea3fa169f663479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76592545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caecb8549d9061ef80f72b53699ea19949fb3468ebdd4fb08c708829a1e05b36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459c907a569b15590c9d09d1ce39e44a9fa42640c696731731c52d192bfd1842`  
		Last Modified: Wed, 04 Sep 2024 07:40:49 GMT  
		Size: 630.8 KB (630823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d605ef3d7805437512a36129b9d3fb98ea13cddaf3c648f0147ba73205aa8fb`  
		Last Modified: Wed, 04 Sep 2024 10:52:53 GMT  
		Size: 14.1 MB (14072296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca3a0f938f4ab832be7c9b54e21d39cb0b524c08c9ec96b391064e82e8631d5`  
		Last Modified: Wed, 04 Sep 2024 10:52:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad63210e30ceb3bec53e28d69a992fc0e9f5ba1671edc1342363a34bf791e6a`  
		Last Modified: Wed, 04 Sep 2024 10:52:53 GMT  
		Size: 1.7 MB (1673607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb55fe0b4d5ab4f6e38e6c402bd87fb52c91f2618745b6a66f3ea5180e2ef1a`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 9.9 MB (9918961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807f1e0c89922bd6eb55fe13fd897d48f74a874ef5df95b59aa61c5becac725b`  
		Last Modified: Wed, 04 Sep 2024 11:57:27 GMT  
		Size: 46.9 MB (46921424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f44aa855627fd8f485493cf04a1fe931385ef50ab1e8c0a79039488cf685256`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca0ca3cc5339094abd67f79e15bfea386376d3d2a52bcbbcd606c8d3e08b098`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4.0-alpine3.19` - unknown; unknown

```console
$ docker pull satosa@sha256:b11392488a9554cedf95a8a01fba766787c14030bb9cf5a0ce3e7aba1ae245b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1192698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc0583b84240d78f45aed5c0632d199084849cf2aa75cea1b4fa5d4d7a6d7ee0`

```dockerfile
```

-	Layers:
	-	`sha256:f35c5753ebe494db7b440a6cf4b3dd4bd589e66ec185d01a909e8c1122073457`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 1.2 MB (1168412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:977c5235e7ee7677285f54387c067e63b90071463dba2480f48588b750a682f2`  
		Last Modified: Wed, 04 Sep 2024 11:57:24 GMT  
		Size: 24.3 KB (24286 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.4.0-bookworm`

```console
$ docker pull satosa@sha256:9838f3edf179af20bee6c8ac3925bd3f36658a0f5862b3385a6c8f5fe2e618cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8.4.0-bookworm` - linux; amd64

```console
$ docker pull satosa@sha256:df7e89152d9cc4909c80222d415a397e9a8c744497036afe3e184f06dad836b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88862529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14675eb83676db6aee0c38ab053b5d50f3a6bef793a282c6c33034b02b85b8a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 14:40:43 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 14:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 14:40:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 14:40:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 14:40:43 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467daa3d4c8b6f3916948d9277922e51161a5d42c977631819a635d2fa9fb32e`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 3.5 MB (3511398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d51d0de90c323e22cf7900a0ee9185e1e3c185b3ed4fecd9202ae1534e60c7`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 11.7 MB (11724854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e6c34f2b20e314d433bf1d444a0c72dc1b27dc93964a4fc102a4dccd25e799`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab50b4ae9438decebef449b4afb727284fe0c8f9198b603c588fea80266eb13`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 1.8 MB (1751083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0db6c6dc89000cc270ec074bf74ed84465d3fd1b31b84cc16de60dcf4879395`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 21.5 MB (21455664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57f345912a7c877e65d8bfc4b29882cb71d9062d398118c452f731fa33ed2dc`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 21.3 MB (21280717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ff5e597a64fb5ca09139b8f7b787223bcd6a34d8c228040d6afe1440477dc7`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd0519cfa116902f9ae050b5fdf0bc57b64a5b5932a15b709fcc2c1951ecfae`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4.0-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:5c2553b9ff9019842b9134cb7f6cce18e5ad03d85f5c55a6cad7e49beac6ee1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2613369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6aec6c918521cd245227d130ea8626b23153986c281c938525bfcccc1a3f4f`

```dockerfile
```

-	Layers:
	-	`sha256:7e79b6aa88d9313fa3e0221dbd224b5bf6ecf13806da95dd9247c869c98d75cd`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 2.6 MB (2589886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7feca4e51ca18ad4deb21d66b20093be3fc6c01600301d6036157791cce48a8d`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 23.5 KB (23483 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.4.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:34f580cda009c649a0081d1dd0149e1d5d02cee4c2544f0929854272eaec8f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88214898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4290484613fdccc82556b42425aa56e356902679ddc288bb26c46b07c14dd461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 14:40:43 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 14:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 14:40:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 14:40:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 14:40:43 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc0bb0f48368309a59f8f76a26a1a2aefa34ff474a1d5fc171b034e954d299b`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 3.3 MB (3331450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbb068a2dcf7bb59fec2a07a7fc7d2d77207313340abb2e7c0010a7660c74e1`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 11.7 MB (11697919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cccda67aa8cce65f16c17702f99d7ae53526c87fe6fd6df833321c206a1915`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31068c739a9608963613c12774e31ba8f0157b299cf8cad529aba9038a3d689d`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 1.8 MB (1751307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc99567289f026c220b3120e68f2d85a71232bbe55438455a3f5e660e87389c`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 21.3 MB (21297890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b36ce4c95930510899b0b5e3794aa799935d3c389646b558a56a26f050775a0`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 21.0 MB (20967460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b6a305f0626446c54a1e5c9a85be45e2c0848d78fffbea4e00d62319e58090`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c81978fdbec654b6eee497a378a0dd8655dab131976c1043e21b9b10947c537`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.4.0-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:47ec55d5a93a25674ccc46b0f4063e4ba39e098ea9cfae20f977e66a0e62e08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2616658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8a53b07362a51d5b4b640abbb68b92b09ec789662505cb6bd7a61909c2f134`

```dockerfile
```

-	Layers:
	-	`sha256:ab5fac2784df8870ecf5b0b5660c59db1821183005268be1c017eefb25d099ea`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 2.6 MB (2592706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c71e017aac0b41e1beff888e67cf43b0fe9f47727a15285186f9f711fb2c4c`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 24.0 KB (23952 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:alpine`

```console
$ docker pull satosa@sha256:450fe7aed678967f2ecd2c0e9c6332e5e2b100d34adcfa8291ecb0faba12a91d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `satosa:alpine` - linux; amd64

```console
$ docker pull satosa@sha256:1d4a2004db2f2160b9293361adbe91483bbbcfafd770c82549d3c79cbd63859d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45787482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c88811c75113b8a4851925e08cc4b50d9514de6e2842e9eaab79c9680a83c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fe8821d8e937f4d18d66ed6c01512319f6369e39501aa040d545cddb26c012`  
		Last Modified: Fri, 06 Sep 2024 23:31:42 GMT  
		Size: 627.9 KB (627915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e73abbe668f9cf00602e624892cee4209b2bea1a95102c68b2057c7e0b3c57`  
		Last Modified: Fri, 06 Sep 2024 23:31:43 GMT  
		Size: 11.5 MB (11499904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd37ef32dbcc8362c68d13269033880dde7e11c41e37de2144c7489fe84d588`  
		Last Modified: Fri, 06 Sep 2024 23:31:42 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e183bebb85d6d6db6d0223f702bb07cfdb79b7f435fb9c1d0e43fb9022370a9`  
		Last Modified: Fri, 06 Sep 2024 23:31:43 GMT  
		Size: 1.7 MB (1673601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b17f050437f188171644ad503679b514d0019bea18044a12242ceb2fe6083e`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 7.4 MB (7409601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d878e1fb4ea01bcb258e5c2cd0eb96217339c4c051c4d4fd643683e476df9a4a`  
		Last Modified: Sat, 07 Sep 2024 00:08:55 GMT  
		Size: 21.1 MB (21144433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14c3f2db0ae337a9fc6e52f90c84de448c365301280a38020a17089961009b5`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f56a48a186a09d5a69eebebecf31b6bb438e02c3867154d01a13a24ca8f659a`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:ce6fd0561adb7c64976cb6fa979b8dc71b67c174924c5359a0d0900f96b5c321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1194106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54d256448b7680b09dce413cbbf5be25b70b9c315cfc9c61333ca2ff946849b`

```dockerfile
```

-	Layers:
	-	`sha256:7e11b81e6a698a0ed5df4bb58d79891397ecfb89a6dd90f7df37c37ef9e5a7a5`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 1.2 MB (1169929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2477e3630694ca6355ede795fa0ca290ddab4bb0ed90194dc82f36e2ab4b2f3b`  
		Last Modified: Sat, 07 Sep 2024 00:08:53 GMT  
		Size: 24.2 KB (24177 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:alpine` - linux; arm variant v7

```console
$ docker pull satosa@sha256:484750cdfd849cd77669cbe91f573bb799331e79c39145a45324ad01310c2204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72502585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c3b9ea495a1c6906a04b17ae1148f8ec4470b8364642894b5beb7c54dc3c2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aca995c8234bcb8cc3881779eb898cea97d1e1ae8d93dfc03230bc2b72cd58f`  
		Last Modified: Wed, 24 Jul 2024 10:02:21 GMT  
		Size: 628.0 KB (627989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06edd34be8b9ba5da915d801b435bfb90ed4c553da299b2edb6293bbef6cd86a`  
		Last Modified: Wed, 07 Aug 2024 22:21:25 GMT  
		Size: 10.7 MB (10656411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164f482cec3d411bf812c97570ac5c9cd9745c2358cb78bd766f07f01038b63c`  
		Last Modified: Wed, 07 Aug 2024 22:21:24 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00118344aaad7672000a959203f9ded1e7e1c7bffa1433954163611aba69da4`  
		Last Modified: Wed, 04 Sep 2024 06:48:01 GMT  
		Size: 1.7 MB (1673590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c8bf69c8012a63b0b5abd3d4a28a39b1aeaed68ffbefa760be087bdaeb807a`  
		Last Modified: Wed, 04 Sep 2024 08:25:22 GMT  
		Size: 11.3 MB (11271496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1221728f93d4c726ecb0f8bf748430dcadd7eacce6921dab6782a74002a17a`  
		Last Modified: Wed, 04 Sep 2024 08:25:23 GMT  
		Size: 45.3 MB (45333665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1918f04628471e1950a105722a4d0e74f6a5d737e48d3ff39a4c0499d4f802`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3dc36ddb010041b6560916f6d2ecbb8da960fd4b4420d7104cf2e9eae2e8dd6`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 2.1 KB (2148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:9a5e945adbc9012c9125b8e76e839c0211e790b7aadaed484f26c7f84ba22869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1194729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b02d8bf4abbc5d9e84d436d0bae2a84f79699f03a2be8c2ac2699db1204182`

```dockerfile
```

-	Layers:
	-	`sha256:5a0df6ee33dffff152bce8d3422e8602ad36252d7f2461d6fcea1e786db2daf4`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 1.2 MB (1170376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62dc3f905e9f0d597d487f8b3c213c95f3dfd1c6d4ff1c069c332bffa6c46d08`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 24.4 KB (24353 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e22814a24e95ebc1f3d6544566d145352a96c1792f2365a16b9d306f576611b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47295578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeeb532d9cfb950d8b7acdbdbe8fd94d29d5120bdd40d9cf046295712ca8c1bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564a93de2c7019a622a4491382e14c5bdf5d7c23bd78c6f9f1c699f72e74fce`  
		Last Modified: Wed, 04 Sep 2024 07:31:02 GMT  
		Size: 630.3 KB (630336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24cd4abfec65ee86b6e7bd5861d5543e3da7dafb92f20851aea5357dfa89434`  
		Last Modified: Wed, 04 Sep 2024 07:31:03 GMT  
		Size: 13.7 MB (13656630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce315a403531201e7db80d481aafa278bd2b73b77c24c5dac830b8736ef6a75`  
		Last Modified: Wed, 04 Sep 2024 07:31:02 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40395139ed67e33f42cbd9721d5a74dac2d9917914519da789686e6122be9579`  
		Last Modified: Wed, 04 Sep 2024 07:31:03 GMT  
		Size: 1.7 MB (1673588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f7073db196529ac226fa3fa25afd2cb96c0298b048397af4f32a61c8d163a4`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 7.4 MB (7403230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3182e9cb9a162ad5fc8ed2b1bb93e5ae69b4a371cd40055b321ec73be449e6e`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 20.6 MB (20561012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3016037b2ceaa72afbe6b3af6862693b2d462201dd7491bc761c2dd900b390`  
		Last Modified: Wed, 04 Sep 2024 09:43:16 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35827c7507295d2943fcceceaeada49dfe6114f767c09d53f773d2c8ae0f3163`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 2.1 KB (2141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:0d5ed8afefec0046729989356a966a2baca01f83e0d253ae0cbe857f5b25e911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1192195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb71a3b25a30177e482a159536c84119f4731c59326a0ea5643027d47048bee9`

```dockerfile
```

-	Layers:
	-	`sha256:91aa376b5a5a0351d224b70755bd3f018eda925fbc7d8728275cb741623c08bb`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 1.2 MB (1167548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ddf12d3de38b8098769bbab9786e83ba03071f5f62fc4f03c9a5bbd8a40b9a9`  
		Last Modified: Wed, 04 Sep 2024 09:43:16 GMT  
		Size: 24.6 KB (24647 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:alpine` - linux; 386

```console
$ docker pull satosa@sha256:2d8cebf9b303562cec2ad131a00c16058682d35e6bd8c8373a6049c2da05fa50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72174501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dca95b05acd6caadc4d2d7296fd8b0f814308a8bb54f679533a64ebab3faef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b2801d1a66d8eb7d37ef8c9bd01ed316e098fb58aca389c7038cf904ab7229`  
		Last Modified: Fri, 06 Sep 2024 23:33:12 GMT  
		Size: 628.4 KB (628417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e8a05a75efec89d800448cf9a90e1fd959a798b05a8f51e395555b1d05c35f`  
		Last Modified: Fri, 06 Sep 2024 23:33:13 GMT  
		Size: 11.7 MB (11692995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5711feaa7d3d84fb482e82165b47257f80cf1c7983ba93ce546895b7d9e28f21`  
		Last Modified: Fri, 06 Sep 2024 23:33:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daa8fc3a87001de1178cb86c2f3a5fb7e0c2b59f148e985334303b078cc6b13`  
		Last Modified: Fri, 06 Sep 2024 23:33:13 GMT  
		Size: 1.7 MB (1673606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7b4e5c3f2ca385e6a13fb3370fe3f6b5b7fbb27b7e78dda4febbba65faa3ae`  
		Last Modified: Sat, 07 Sep 2024 00:14:59 GMT  
		Size: 9.7 MB (9739429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a844ba5a90453d5ad7c35d062ced6e7dd837a85671dba10cf6084eed5bb437c`  
		Last Modified: Sat, 07 Sep 2024 00:15:00 GMT  
		Size: 45.2 MB (45174127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba215f757c4dc05b9334c475e0b248836410f95ca5863da0d003a76632535a1`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 9.9 KB (9920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a6e89a4bf4c06ffa048e8cedd4b46ad59c9488eb85e10ebddda37a91119547`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:5c89fc3ceec355fda8b70edc5043ef7d778ac8a14eeba4292a949b1cb2327e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1196870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64cf3af182ba3581f1e116de5945cb44af88663baf9613093c160e918a42baf`

```dockerfile
```

-	Layers:
	-	`sha256:90b86ed2cf30e8cdaad32f8211994587cdb407caf5196c21249a5f34b13b85dd`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 1.2 MB (1172748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2dc2205c70270528b883f21361c34d7e3293ee05096b63fa6a91d7c0be6ac47`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 24.1 KB (24122 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:alpine` - linux; ppc64le

```console
$ docker pull satosa@sha256:6eecae17d30f48b03013d1d14a9b85ad3dea43b7923802d32ea3fa169f663479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76592545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caecb8549d9061ef80f72b53699ea19949fb3468ebdd4fb08c708829a1e05b36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459c907a569b15590c9d09d1ce39e44a9fa42640c696731731c52d192bfd1842`  
		Last Modified: Wed, 04 Sep 2024 07:40:49 GMT  
		Size: 630.8 KB (630823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d605ef3d7805437512a36129b9d3fb98ea13cddaf3c648f0147ba73205aa8fb`  
		Last Modified: Wed, 04 Sep 2024 10:52:53 GMT  
		Size: 14.1 MB (14072296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca3a0f938f4ab832be7c9b54e21d39cb0b524c08c9ec96b391064e82e8631d5`  
		Last Modified: Wed, 04 Sep 2024 10:52:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad63210e30ceb3bec53e28d69a992fc0e9f5ba1671edc1342363a34bf791e6a`  
		Last Modified: Wed, 04 Sep 2024 10:52:53 GMT  
		Size: 1.7 MB (1673607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb55fe0b4d5ab4f6e38e6c402bd87fb52c91f2618745b6a66f3ea5180e2ef1a`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 9.9 MB (9918961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807f1e0c89922bd6eb55fe13fd897d48f74a874ef5df95b59aa61c5becac725b`  
		Last Modified: Wed, 04 Sep 2024 11:57:27 GMT  
		Size: 46.9 MB (46921424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f44aa855627fd8f485493cf04a1fe931385ef50ab1e8c0a79039488cf685256`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca0ca3cc5339094abd67f79e15bfea386376d3d2a52bcbbcd606c8d3e08b098`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:b11392488a9554cedf95a8a01fba766787c14030bb9cf5a0ce3e7aba1ae245b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1192698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc0583b84240d78f45aed5c0632d199084849cf2aa75cea1b4fa5d4d7a6d7ee0`

```dockerfile
```

-	Layers:
	-	`sha256:f35c5753ebe494db7b440a6cf4b3dd4bd589e66ec185d01a909e8c1122073457`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 1.2 MB (1168412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:977c5235e7ee7677285f54387c067e63b90071463dba2480f48588b750a682f2`  
		Last Modified: Wed, 04 Sep 2024 11:57:24 GMT  
		Size: 24.3 KB (24286 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:alpine3.19`

```console
$ docker pull satosa@sha256:450fe7aed678967f2ecd2c0e9c6332e5e2b100d34adcfa8291ecb0faba12a91d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `satosa:alpine3.19` - linux; amd64

```console
$ docker pull satosa@sha256:1d4a2004db2f2160b9293361adbe91483bbbcfafd770c82549d3c79cbd63859d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45787482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c88811c75113b8a4851925e08cc4b50d9514de6e2842e9eaab79c9680a83c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fe8821d8e937f4d18d66ed6c01512319f6369e39501aa040d545cddb26c012`  
		Last Modified: Fri, 06 Sep 2024 23:31:42 GMT  
		Size: 627.9 KB (627915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e73abbe668f9cf00602e624892cee4209b2bea1a95102c68b2057c7e0b3c57`  
		Last Modified: Fri, 06 Sep 2024 23:31:43 GMT  
		Size: 11.5 MB (11499904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd37ef32dbcc8362c68d13269033880dde7e11c41e37de2144c7489fe84d588`  
		Last Modified: Fri, 06 Sep 2024 23:31:42 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e183bebb85d6d6db6d0223f702bb07cfdb79b7f435fb9c1d0e43fb9022370a9`  
		Last Modified: Fri, 06 Sep 2024 23:31:43 GMT  
		Size: 1.7 MB (1673601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b17f050437f188171644ad503679b514d0019bea18044a12242ceb2fe6083e`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 7.4 MB (7409601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d878e1fb4ea01bcb258e5c2cd0eb96217339c4c051c4d4fd643683e476df9a4a`  
		Last Modified: Sat, 07 Sep 2024 00:08:55 GMT  
		Size: 21.1 MB (21144433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14c3f2db0ae337a9fc6e52f90c84de448c365301280a38020a17089961009b5`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f56a48a186a09d5a69eebebecf31b6bb438e02c3867154d01a13a24ca8f659a`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:alpine3.19` - unknown; unknown

```console
$ docker pull satosa@sha256:ce6fd0561adb7c64976cb6fa979b8dc71b67c174924c5359a0d0900f96b5c321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1194106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54d256448b7680b09dce413cbbf5be25b70b9c315cfc9c61333ca2ff946849b`

```dockerfile
```

-	Layers:
	-	`sha256:7e11b81e6a698a0ed5df4bb58d79891397ecfb89a6dd90f7df37c37ef9e5a7a5`  
		Last Modified: Sat, 07 Sep 2024 00:08:54 GMT  
		Size: 1.2 MB (1169929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2477e3630694ca6355ede795fa0ca290ddab4bb0ed90194dc82f36e2ab4b2f3b`  
		Last Modified: Sat, 07 Sep 2024 00:08:53 GMT  
		Size: 24.2 KB (24177 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:alpine3.19` - linux; arm variant v7

```console
$ docker pull satosa@sha256:484750cdfd849cd77669cbe91f573bb799331e79c39145a45324ad01310c2204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72502585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c3b9ea495a1c6906a04b17ae1148f8ec4470b8364642894b5beb7c54dc3c2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aca995c8234bcb8cc3881779eb898cea97d1e1ae8d93dfc03230bc2b72cd58f`  
		Last Modified: Wed, 24 Jul 2024 10:02:21 GMT  
		Size: 628.0 KB (627989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06edd34be8b9ba5da915d801b435bfb90ed4c553da299b2edb6293bbef6cd86a`  
		Last Modified: Wed, 07 Aug 2024 22:21:25 GMT  
		Size: 10.7 MB (10656411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164f482cec3d411bf812c97570ac5c9cd9745c2358cb78bd766f07f01038b63c`  
		Last Modified: Wed, 07 Aug 2024 22:21:24 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00118344aaad7672000a959203f9ded1e7e1c7bffa1433954163611aba69da4`  
		Last Modified: Wed, 04 Sep 2024 06:48:01 GMT  
		Size: 1.7 MB (1673590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c8bf69c8012a63b0b5abd3d4a28a39b1aeaed68ffbefa760be087bdaeb807a`  
		Last Modified: Wed, 04 Sep 2024 08:25:22 GMT  
		Size: 11.3 MB (11271496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1221728f93d4c726ecb0f8bf748430dcadd7eacce6921dab6782a74002a17a`  
		Last Modified: Wed, 04 Sep 2024 08:25:23 GMT  
		Size: 45.3 MB (45333665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1918f04628471e1950a105722a4d0e74f6a5d737e48d3ff39a4c0499d4f802`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3dc36ddb010041b6560916f6d2ecbb8da960fd4b4420d7104cf2e9eae2e8dd6`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 2.1 KB (2148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:alpine3.19` - unknown; unknown

```console
$ docker pull satosa@sha256:9a5e945adbc9012c9125b8e76e839c0211e790b7aadaed484f26c7f84ba22869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1194729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b02d8bf4abbc5d9e84d436d0bae2a84f79699f03a2be8c2ac2699db1204182`

```dockerfile
```

-	Layers:
	-	`sha256:5a0df6ee33dffff152bce8d3422e8602ad36252d7f2461d6fcea1e786db2daf4`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 1.2 MB (1170376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62dc3f905e9f0d597d487f8b3c213c95f3dfd1c6d4ff1c069c332bffa6c46d08`  
		Last Modified: Wed, 04 Sep 2024 08:25:21 GMT  
		Size: 24.4 KB (24353 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e22814a24e95ebc1f3d6544566d145352a96c1792f2365a16b9d306f576611b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47295578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeeb532d9cfb950d8b7acdbdbe8fd94d29d5120bdd40d9cf046295712ca8c1bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564a93de2c7019a622a4491382e14c5bdf5d7c23bd78c6f9f1c699f72e74fce`  
		Last Modified: Wed, 04 Sep 2024 07:31:02 GMT  
		Size: 630.3 KB (630336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24cd4abfec65ee86b6e7bd5861d5543e3da7dafb92f20851aea5357dfa89434`  
		Last Modified: Wed, 04 Sep 2024 07:31:03 GMT  
		Size: 13.7 MB (13656630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce315a403531201e7db80d481aafa278bd2b73b77c24c5dac830b8736ef6a75`  
		Last Modified: Wed, 04 Sep 2024 07:31:02 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40395139ed67e33f42cbd9721d5a74dac2d9917914519da789686e6122be9579`  
		Last Modified: Wed, 04 Sep 2024 07:31:03 GMT  
		Size: 1.7 MB (1673588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f7073db196529ac226fa3fa25afd2cb96c0298b048397af4f32a61c8d163a4`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 7.4 MB (7403230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3182e9cb9a162ad5fc8ed2b1bb93e5ae69b4a371cd40055b321ec73be449e6e`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 20.6 MB (20561012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3016037b2ceaa72afbe6b3af6862693b2d462201dd7491bc761c2dd900b390`  
		Last Modified: Wed, 04 Sep 2024 09:43:16 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35827c7507295d2943fcceceaeada49dfe6114f767c09d53f773d2c8ae0f3163`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 2.1 KB (2141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:alpine3.19` - unknown; unknown

```console
$ docker pull satosa@sha256:0d5ed8afefec0046729989356a966a2baca01f83e0d253ae0cbe857f5b25e911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1192195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb71a3b25a30177e482a159536c84119f4731c59326a0ea5643027d47048bee9`

```dockerfile
```

-	Layers:
	-	`sha256:91aa376b5a5a0351d224b70755bd3f018eda925fbc7d8728275cb741623c08bb`  
		Last Modified: Wed, 04 Sep 2024 09:43:17 GMT  
		Size: 1.2 MB (1167548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ddf12d3de38b8098769bbab9786e83ba03071f5f62fc4f03c9a5bbd8a40b9a9`  
		Last Modified: Wed, 04 Sep 2024 09:43:16 GMT  
		Size: 24.6 KB (24647 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:alpine3.19` - linux; 386

```console
$ docker pull satosa@sha256:2d8cebf9b303562cec2ad131a00c16058682d35e6bd8c8373a6049c2da05fa50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72174501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3dca95b05acd6caadc4d2d7296fd8b0f814308a8bb54f679533a64ebab3faef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b2801d1a66d8eb7d37ef8c9bd01ed316e098fb58aca389c7038cf904ab7229`  
		Last Modified: Fri, 06 Sep 2024 23:33:12 GMT  
		Size: 628.4 KB (628417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e8a05a75efec89d800448cf9a90e1fd959a798b05a8f51e395555b1d05c35f`  
		Last Modified: Fri, 06 Sep 2024 23:33:13 GMT  
		Size: 11.7 MB (11692995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5711feaa7d3d84fb482e82165b47257f80cf1c7983ba93ce546895b7d9e28f21`  
		Last Modified: Fri, 06 Sep 2024 23:33:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daa8fc3a87001de1178cb86c2f3a5fb7e0c2b59f148e985334303b078cc6b13`  
		Last Modified: Fri, 06 Sep 2024 23:33:13 GMT  
		Size: 1.7 MB (1673606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7b4e5c3f2ca385e6a13fb3370fe3f6b5b7fbb27b7e78dda4febbba65faa3ae`  
		Last Modified: Sat, 07 Sep 2024 00:14:59 GMT  
		Size: 9.7 MB (9739429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a844ba5a90453d5ad7c35d062ced6e7dd837a85671dba10cf6084eed5bb437c`  
		Last Modified: Sat, 07 Sep 2024 00:15:00 GMT  
		Size: 45.2 MB (45174127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba215f757c4dc05b9334c475e0b248836410f95ca5863da0d003a76632535a1`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 9.9 KB (9920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a6e89a4bf4c06ffa048e8cedd4b46ad59c9488eb85e10ebddda37a91119547`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:alpine3.19` - unknown; unknown

```console
$ docker pull satosa@sha256:5c89fc3ceec355fda8b70edc5043ef7d778ac8a14eeba4292a949b1cb2327e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1196870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64cf3af182ba3581f1e116de5945cb44af88663baf9613093c160e918a42baf`

```dockerfile
```

-	Layers:
	-	`sha256:90b86ed2cf30e8cdaad32f8211994587cdb407caf5196c21249a5f34b13b85dd`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 1.2 MB (1172748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2dc2205c70270528b883f21361c34d7e3293ee05096b63fa6a91d7c0be6ac47`  
		Last Modified: Sat, 07 Sep 2024 00:14:58 GMT  
		Size: 24.1 KB (24122 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:alpine3.19` - linux; ppc64le

```console
$ docker pull satosa@sha256:6eecae17d30f48b03013d1d14a9b85ad3dea43b7923802d32ea3fa169f663479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76592545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caecb8549d9061ef80f72b53699ea19949fb3468ebdd4fb08c708829a1e05b36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 17:24:54 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:24:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 17:24:54 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 17:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 17:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:24:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 17:24:54 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 17:24:54 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459c907a569b15590c9d09d1ce39e44a9fa42640c696731731c52d192bfd1842`  
		Last Modified: Wed, 04 Sep 2024 07:40:49 GMT  
		Size: 630.8 KB (630823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d605ef3d7805437512a36129b9d3fb98ea13cddaf3c648f0147ba73205aa8fb`  
		Last Modified: Wed, 04 Sep 2024 10:52:53 GMT  
		Size: 14.1 MB (14072296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca3a0f938f4ab832be7c9b54e21d39cb0b524c08c9ec96b391064e82e8631d5`  
		Last Modified: Wed, 04 Sep 2024 10:52:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad63210e30ceb3bec53e28d69a992fc0e9f5ba1671edc1342363a34bf791e6a`  
		Last Modified: Wed, 04 Sep 2024 10:52:53 GMT  
		Size: 1.7 MB (1673607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb55fe0b4d5ab4f6e38e6c402bd87fb52c91f2618745b6a66f3ea5180e2ef1a`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 9.9 MB (9918961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807f1e0c89922bd6eb55fe13fd897d48f74a874ef5df95b59aa61c5becac725b`  
		Last Modified: Wed, 04 Sep 2024 11:57:27 GMT  
		Size: 46.9 MB (46921424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f44aa855627fd8f485493cf04a1fe931385ef50ab1e8c0a79039488cf685256`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca0ca3cc5339094abd67f79e15bfea386376d3d2a52bcbbcd606c8d3e08b098`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 2.1 KB (2142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:alpine3.19` - unknown; unknown

```console
$ docker pull satosa@sha256:b11392488a9554cedf95a8a01fba766787c14030bb9cf5a0ce3e7aba1ae245b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1192698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc0583b84240d78f45aed5c0632d199084849cf2aa75cea1b4fa5d4d7a6d7ee0`

```dockerfile
```

-	Layers:
	-	`sha256:f35c5753ebe494db7b440a6cf4b3dd4bd589e66ec185d01a909e8c1122073457`  
		Last Modified: Wed, 04 Sep 2024 11:57:25 GMT  
		Size: 1.2 MB (1168412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:977c5235e7ee7677285f54387c067e63b90071463dba2480f48588b750a682f2`  
		Last Modified: Wed, 04 Sep 2024 11:57:24 GMT  
		Size: 24.3 KB (24286 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:bookworm`

```console
$ docker pull satosa@sha256:9838f3edf179af20bee6c8ac3925bd3f36658a0f5862b3385a6c8f5fe2e618cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:bookworm` - linux; amd64

```console
$ docker pull satosa@sha256:df7e89152d9cc4909c80222d415a397e9a8c744497036afe3e184f06dad836b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88862529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14675eb83676db6aee0c38ab053b5d50f3a6bef793a282c6c33034b02b85b8a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 14:40:43 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 14:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 14:40:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 14:40:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 14:40:43 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467daa3d4c8b6f3916948d9277922e51161a5d42c977631819a635d2fa9fb32e`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 3.5 MB (3511398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d51d0de90c323e22cf7900a0ee9185e1e3c185b3ed4fecd9202ae1534e60c7`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 11.7 MB (11724854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e6c34f2b20e314d433bf1d444a0c72dc1b27dc93964a4fc102a4dccd25e799`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab50b4ae9438decebef449b4afb727284fe0c8f9198b603c588fea80266eb13`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 1.8 MB (1751083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0db6c6dc89000cc270ec074bf74ed84465d3fd1b31b84cc16de60dcf4879395`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 21.5 MB (21455664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57f345912a7c877e65d8bfc4b29882cb71d9062d398118c452f731fa33ed2dc`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 21.3 MB (21280717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ff5e597a64fb5ca09139b8f7b787223bcd6a34d8c228040d6afe1440477dc7`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd0519cfa116902f9ae050b5fdf0bc57b64a5b5932a15b709fcc2c1951ecfae`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:5c2553b9ff9019842b9134cb7f6cce18e5ad03d85f5c55a6cad7e49beac6ee1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2613369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6aec6c918521cd245227d130ea8626b23153986c281c938525bfcccc1a3f4f`

```dockerfile
```

-	Layers:
	-	`sha256:7e79b6aa88d9313fa3e0221dbd224b5bf6ecf13806da95dd9247c869c98d75cd`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 2.6 MB (2589886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7feca4e51ca18ad4deb21d66b20093be3fc6c01600301d6036157791cce48a8d`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 23.5 KB (23483 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:bookworm` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:34f580cda009c649a0081d1dd0149e1d5d02cee4c2544f0929854272eaec8f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88214898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4290484613fdccc82556b42425aa56e356902679ddc288bb26c46b07c14dd461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 14:40:43 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 14:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 14:40:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 14:40:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 14:40:43 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc0bb0f48368309a59f8f76a26a1a2aefa34ff474a1d5fc171b034e954d299b`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 3.3 MB (3331450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbb068a2dcf7bb59fec2a07a7fc7d2d77207313340abb2e7c0010a7660c74e1`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 11.7 MB (11697919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cccda67aa8cce65f16c17702f99d7ae53526c87fe6fd6df833321c206a1915`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31068c739a9608963613c12774e31ba8f0157b299cf8cad529aba9038a3d689d`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 1.8 MB (1751307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc99567289f026c220b3120e68f2d85a71232bbe55438455a3f5e660e87389c`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 21.3 MB (21297890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b36ce4c95930510899b0b5e3794aa799935d3c389646b558a56a26f050775a0`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 21.0 MB (20967460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b6a305f0626446c54a1e5c9a85be45e2c0848d78fffbea4e00d62319e58090`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c81978fdbec654b6eee497a378a0dd8655dab131976c1043e21b9b10947c537`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:47ec55d5a93a25674ccc46b0f4063e4ba39e098ea9cfae20f977e66a0e62e08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2616658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8a53b07362a51d5b4b640abbb68b92b09ec789662505cb6bd7a61909c2f134`

```dockerfile
```

-	Layers:
	-	`sha256:ab5fac2784df8870ecf5b0b5660c59db1821183005268be1c017eefb25d099ea`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 2.6 MB (2592706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c71e017aac0b41e1beff888e67cf43b0fe9f47727a15285186f9f711fb2c4c`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 24.0 KB (23952 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:latest`

```console
$ docker pull satosa@sha256:9838f3edf179af20bee6c8ac3925bd3f36658a0f5862b3385a6c8f5fe2e618cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:latest` - linux; amd64

```console
$ docker pull satosa@sha256:df7e89152d9cc4909c80222d415a397e9a8c744497036afe3e184f06dad836b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88862529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14675eb83676db6aee0c38ab053b5d50f3a6bef793a282c6c33034b02b85b8a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 14:40:43 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 14:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 14:40:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 14:40:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 14:40:43 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467daa3d4c8b6f3916948d9277922e51161a5d42c977631819a635d2fa9fb32e`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 3.5 MB (3511398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d51d0de90c323e22cf7900a0ee9185e1e3c185b3ed4fecd9202ae1534e60c7`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 11.7 MB (11724854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e6c34f2b20e314d433bf1d444a0c72dc1b27dc93964a4fc102a4dccd25e799`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab50b4ae9438decebef449b4afb727284fe0c8f9198b603c588fea80266eb13`  
		Last Modified: Wed, 04 Sep 2024 23:19:15 GMT  
		Size: 1.8 MB (1751083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0db6c6dc89000cc270ec074bf74ed84465d3fd1b31b84cc16de60dcf4879395`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 21.5 MB (21455664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57f345912a7c877e65d8bfc4b29882cb71d9062d398118c452f731fa33ed2dc`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 21.3 MB (21280717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ff5e597a64fb5ca09139b8f7b787223bcd6a34d8c228040d6afe1440477dc7`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd0519cfa116902f9ae050b5fdf0bc57b64a5b5932a15b709fcc2c1951ecfae`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:latest` - unknown; unknown

```console
$ docker pull satosa@sha256:5c2553b9ff9019842b9134cb7f6cce18e5ad03d85f5c55a6cad7e49beac6ee1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2613369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6aec6c918521cd245227d130ea8626b23153986c281c938525bfcccc1a3f4f`

```dockerfile
```

-	Layers:
	-	`sha256:7e79b6aa88d9313fa3e0221dbd224b5bf6ecf13806da95dd9247c869c98d75cd`  
		Last Modified: Thu, 05 Sep 2024 00:10:41 GMT  
		Size: 2.6 MB (2589886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7feca4e51ca18ad4deb21d66b20093be3fc6c01600301d6036157791cce48a8d`  
		Last Modified: Thu, 05 Sep 2024 00:10:40 GMT  
		Size: 23.5 KB (23483 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:latest` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:34f580cda009c649a0081d1dd0149e1d5d02cee4c2544f0929854272eaec8f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88214898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4290484613fdccc82556b42425aa56e356902679ddc288bb26c46b07c14dd461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 19 Dec 2023 14:40:43 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 14:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_VERSION=3.12.5
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_PIP_VERSION=24.2
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Tue, 19 Dec 2023 14:40:43 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		--no-setuptools 		--no-wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["python3"]
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENV SATOSA_VERSION=8.4.0
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
WORKDIR /etc/satosa
# Tue, 19 Dec 2023 14:40:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 14:40:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 14:40:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Dec 2023 14:40:43 GMT
USER satosa:satosa
# Tue, 19 Dec 2023 14:40:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc0bb0f48368309a59f8f76a26a1a2aefa34ff474a1d5fc171b034e954d299b`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 3.3 MB (3331450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbb068a2dcf7bb59fec2a07a7fc7d2d77207313340abb2e7c0010a7660c74e1`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 11.7 MB (11697919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cccda67aa8cce65f16c17702f99d7ae53526c87fe6fd6df833321c206a1915`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31068c739a9608963613c12774e31ba8f0157b299cf8cad529aba9038a3d689d`  
		Last Modified: Thu, 05 Sep 2024 17:29:01 GMT  
		Size: 1.8 MB (1751307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc99567289f026c220b3120e68f2d85a71232bbe55438455a3f5e660e87389c`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 21.3 MB (21297890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b36ce4c95930510899b0b5e3794aa799935d3c389646b558a56a26f050775a0`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 21.0 MB (20967460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b6a305f0626446c54a1e5c9a85be45e2c0848d78fffbea4e00d62319e58090`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c81978fdbec654b6eee497a378a0dd8655dab131976c1043e21b9b10947c537`  
		Last Modified: Thu, 05 Sep 2024 21:01:00 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:latest` - unknown; unknown

```console
$ docker pull satosa@sha256:47ec55d5a93a25674ccc46b0f4063e4ba39e098ea9cfae20f977e66a0e62e08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2616658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8a53b07362a51d5b4b640abbb68b92b09ec789662505cb6bd7a61909c2f134`

```dockerfile
```

-	Layers:
	-	`sha256:ab5fac2784df8870ecf5b0b5660c59db1821183005268be1c017eefb25d099ea`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 2.6 MB (2592706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c71e017aac0b41e1beff888e67cf43b0fe9f47727a15285186f9f711fb2c4c`  
		Last Modified: Thu, 05 Sep 2024 21:00:59 GMT  
		Size: 24.0 KB (23952 bytes)  
		MIME: application/vnd.in-toto+json
