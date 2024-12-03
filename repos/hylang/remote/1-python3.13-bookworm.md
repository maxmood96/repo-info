## `hylang:1-python3.13-bookworm`

```console
$ docker pull hylang@sha256:d8d7faa5e4f5ebbe277dbdf5f0c7e2ade4ddf7ffa03f3251cd1c0e55c84cef93
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

### `hylang:1-python3.13-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:b2b9794770ecfd876bf01b99853fd5eb21c430ed03855b0baa85c1176e673f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49772059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f26cc11052783980250d759b37a7c8bb4390740619aa44ed9d70c93480a935a`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.13.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcccf87d013dafa7f4bd6b72c6c3c1f5a3a347e626690a07568d0a925cfb262e`  
		Last Modified: Tue, 03 Dec 2024 02:29:59 GMT  
		Size: 3.3 MB (3317321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acee09de1c5d11742e97e43b537a9c6dd6ec1346a50b75e9b68f39de44a4216f`  
		Last Modified: Tue, 03 Dec 2024 02:29:59 GMT  
		Size: 12.6 MB (12554630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a576ef79af7ef1fe063c34530a90c344f6d622795c713ff9f2a771f3edc00cee`  
		Last Modified: Tue, 03 Dec 2024 02:29:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6112ce49ca2ba0ced8cb4a05c2f522a5181891daa3d74cc0a2e91b12a1615e27`  
		Last Modified: Tue, 03 Dec 2024 03:26:35 GMT  
		Size: 5.7 MB (5668278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:d103cb4e870cf9a8ba0d4a46e50344470cb2416c21832ddab02e83df8e5e6aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2432399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a87b0208c5806c9e96f3e68f5451497e5f040d53498d4955941b271115747ad`

```dockerfile
```

-	Layers:
	-	`sha256:b54c003e020b18536bc24f254cac5515dd37c05007a3d3a59d3d537426b7cae8`  
		Last Modified: Tue, 03 Dec 2024 03:26:35 GMT  
		Size: 2.4 MB (2420732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44af1a38258d365378efe707b60ced1bc5a4f244c6142d51d50e5e2cb4429ae4`  
		Last Modified: Tue, 03 Dec 2024 03:26:34 GMT  
		Size: 11.7 KB (11667 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:e439f87c0b50cab145f79c596d0475eaeb2bbf160c9e8b3ed79391e6d4857aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46355051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702ff28498a95952a38b955596c8e36d6c078f132c7b45c3587308f3cd07828b`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.13.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:25d432086d20067bebfff2b163f22d49e7da8528782652615fe170bf8c39194d`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 25.8 MB (25754926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5523c22d013c583282bb834c4b12d7cd19ac8c108e2d4f4644f3d0b0600431a`  
		Last Modified: Tue, 03 Dec 2024 06:48:13 GMT  
		Size: 2.9 MB (2889961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf538b3cf74d293053eee6ed53b344c8a235105b00d7d12e8420b4c2b5259136`  
		Last Modified: Tue, 03 Dec 2024 07:08:13 GMT  
		Size: 12.0 MB (12041180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af01669cec838a64d5a56eef3c9bd651177f62f25b00069782bc26323b73a80`  
		Last Modified: Tue, 03 Dec 2024 07:08:12 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6d717ed8ef4e50518f9a906c5a1913bfc50e5db7d555f917295d9079956a85`  
		Last Modified: Tue, 03 Dec 2024 09:53:48 GMT  
		Size: 5.7 MB (5668736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:33a1576802cabe4ebeab5d28632e79c54a0123b9d14da6c861a8c6dc26bbf601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2436170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6cbad372a1ef39e873a3abda660b0541d22bc3ab1aa6196698f73d9757c8ac`

```dockerfile
```

-	Layers:
	-	`sha256:cd4c61a5a4fc75ce4698b135726ea417b6fc5dea882d59f957ad4aad11237f20`  
		Last Modified: Tue, 03 Dec 2024 09:53:48 GMT  
		Size: 2.4 MB (2424331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96472535b9772b69d49ab9f8ffe7452183fa5a25efa90fd482e2ebc1ff607d7c`  
		Last Modified: Tue, 03 Dec 2024 09:53:47 GMT  
		Size: 11.8 KB (11839 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:89719442aad48f0408441b6af9ca5631a14d9ed5e885589955bf0f05b0681684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43987479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31543ff247b3cf25ef1cbcae43281ed0bb455f9af268af2d8cd847c91ab36a3`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.13.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc68b05a34d230d10397365aa4b7199272b81254f15c0d0fc1ba69365b60fb1`  
		Last Modified: Tue, 03 Dec 2024 10:17:29 GMT  
		Size: 2.7 MB (2721167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9e596dea6f4b2f37df30ddfac630d4f6ede7027c51f1a2e505505005a187d3`  
		Last Modified: Tue, 03 Dec 2024 11:00:21 GMT  
		Size: 11.7 MB (11663774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964a5638330a344b0befb2f3bc048415a6a12c64325c87251ea0771d1d7fd275`  
		Last Modified: Tue, 03 Dec 2024 11:00:20 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83dde3f947a4642c67532f784b8b898fd3f724c581ea532c11635271a5beaef0`  
		Last Modified: Tue, 03 Dec 2024 19:40:10 GMT  
		Size: 5.7 MB (5668699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:90919d5d64ac2503390b5bccd1f97a5b46d7785ccff17ea040c6dc708f554389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2434911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85740594a4cc83a423db6444ff644dd57077ddafc5940780ac871b59e34b3eee`

```dockerfile
```

-	Layers:
	-	`sha256:4e35df8db0c8815c18455eb8491f4d02e623c7decb24daa2b51fce7842b3c4be`  
		Last Modified: Tue, 03 Dec 2024 19:40:10 GMT  
		Size: 2.4 MB (2423072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:095ba91071020374a8f77036db2c96c9aff4095663aeec52d28892fdd3c33680`  
		Last Modified: Tue, 03 Dec 2024 19:40:09 GMT  
		Size: 11.8 KB (11839 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:f2dba93c36f52d28131dc875403c0743e2a68c120eee061da5ac3a4031985890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49294109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db01103ff6e4c02e3fdac5e3ec30657c1fd195855a40841e214fbdbb1ff8415e`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.13.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac98cfdb273bf9e7a34bb9745c734d49b1506faa8a5044d29b138548b2c04c7f`  
		Last Modified: Tue, 03 Dec 2024 08:12:50 GMT  
		Size: 3.1 MB (3137743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97fee4b636ac6cbeb4f80a1b121f37e1361739a25bd9bb8dc23155c4f59d7f5`  
		Last Modified: Tue, 03 Dec 2024 08:39:31 GMT  
		Size: 12.4 MB (12428715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374482381e72e7a0a812588414eed066eb54201d3e5df1f9b9ee858ad45cfe17`  
		Last Modified: Tue, 03 Dec 2024 08:39:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b7308f05bda73909e549fc2e8053fd0a0426913b89c8ff217d1f444678203b`  
		Last Modified: Tue, 03 Dec 2024 16:02:19 GMT  
		Size: 5.7 MB (5668592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:d212781de69ca43809cb950c6beb98cb15077f57a23d0c900bb5f80a64dca57c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2433055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e456cf7312eb4fb1062bfe09e5b8fc49e55446b00de2d619e56eebb2560d9a`

```dockerfile
```

-	Layers:
	-	`sha256:0d2323f554086e052a9cf30f6b6df25eac4ee6a8a6a435ed28ca7fdcbae7c21f`  
		Last Modified: Tue, 03 Dec 2024 16:02:19 GMT  
		Size: 2.4 MB (2421140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aff9016c9d3e3abc91f12394a4f23a7243e87e8790be4208250742b0828c5f90`  
		Last Modified: Tue, 03 Dec 2024 16:02:18 GMT  
		Size: 11.9 KB (11915 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:f54b7e7f5ccaea8ca6b01c9cf000b5d4d1f75649ef275c491ea55a7982d88ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50975523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcdfef60f3ab51b0e049606b65f3be7445f33fb2a4776c73222087388fcb963c`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.13.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07acc7c26605f34644b7e09c90895c83eeb51a9452a2b6616b01f9e57f7ba0f1`  
		Last Modified: Tue, 03 Dec 2024 02:45:46 GMT  
		Size: 3.3 MB (3316837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43fedfa38f74217844cea6d05dbc30e8a4c2e51be7ffa1c81947b373026f625`  
		Last Modified: Tue, 03 Dec 2024 02:45:47 GMT  
		Size: 12.8 MB (12784978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b383e2955db716df04aaec3b122d27e4464dfb6d688cf900d672a9a793014f2a`  
		Last Modified: Tue, 03 Dec 2024 02:45:46 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1359b0338603b9f7e0989a7e522ec31752f0d1ce992e3aec071bc3d38dd3cb`  
		Last Modified: Tue, 03 Dec 2024 03:22:43 GMT  
		Size: 5.7 MB (5667972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:9347b4432a5cd167d8b8053b17331d1cda5bf8275767bd9a9b6f9fb602dcfcc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8257ea50141cbe9c7094b0e4f749bca9a1020529ad7f0e5a8ea9b8ce6fbc839`

```dockerfile
```

-	Layers:
	-	`sha256:7ca807ebc58fa736eff90e71b7e42e9440d96707d18a6ad46ab74189a3742f9c`  
		Last Modified: Tue, 03 Dec 2024 03:22:43 GMT  
		Size: 2.4 MB (2417794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a554c00467c362a8ef67687264891680b0507f08721e62142d0654d0d1ebc85`  
		Last Modified: Tue, 03 Dec 2024 03:22:43 GMT  
		Size: 11.6 KB (11575 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:c89a8b2a2087427304c3309225325a1c00ad061b6daeade5376c053c1743d0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54279703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943610d1931dbe98d3184f94161a466354ff167fd8eeb1c8b0501b38a84a55f3`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.13.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34640725679def5c8b7151179bb328099e95eb968613243f6f80826db0643d9`  
		Last Modified: Tue, 03 Dec 2024 06:41:56 GMT  
		Size: 3.5 MB (3520168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f60bd0198258fe910f751f1f84e1a0eebe43f9b32ee79aa437f2a210ac94bf`  
		Last Modified: Tue, 03 Dec 2024 06:59:56 GMT  
		Size: 13.0 MB (13027235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cb14e24059a99dbd2f4810e78ead0bf95ff9b9d3a2c58b7f3c8264c03f69ca`  
		Last Modified: Tue, 03 Dec 2024 06:59:55 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec18133ef99a036e287af7e5d1e76c5feb6bfb8c2e892b4bcf68bcc3ddadb20`  
		Last Modified: Tue, 03 Dec 2024 15:58:04 GMT  
		Size: 5.7 MB (5668786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:d5a221ee03ee95ddacd1feef3593300f7b910755ca526bbc262f02704a24a0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2436924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5144f7d8bae8b0f30eff2bb77d8b0d92ceb86093fbf4b4cf68d9722b9b0e3b54`

```dockerfile
```

-	Layers:
	-	`sha256:1f7b568a029d27fc777f4148259ef3ad2c3697604f2d2f55345d61a03aafaa4d`  
		Last Modified: Tue, 03 Dec 2024 15:58:03 GMT  
		Size: 2.4 MB (2425141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff1b2b19560ecc9014a3e40804e79a110b81b704d9b4ab8b1667f7acd1e60c26`  
		Last Modified: Tue, 03 Dec 2024 15:58:03 GMT  
		Size: 11.8 KB (11783 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:958ec0b88012ed9cbf522a660ee903e9a9a6fba4ff31818657d37e4b9ee4ce84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47868716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272df025b66d652a709606dfd44d2e2e1dd2fb4eee1a77f6f0e442f85ba2517f`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.13.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbdc1d36b76c88548701723e3e88e6f136864a7be1d1c1a505afbeaf2b99bcf`  
		Last Modified: Tue, 03 Dec 2024 06:00:52 GMT  
		Size: 3.0 MB (2980777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab54d9e1b59a6333e572335c6d829709a6608fdfb89756fe67df4f8807b0bf3`  
		Last Modified: Tue, 03 Dec 2024 06:15:21 GMT  
		Size: 12.3 MB (12340283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a86fdd63dd4448a0b8bea3eba3b8714620824f7d759b5c1536adec100521133`  
		Last Modified: Tue, 03 Dec 2024 06:15:20 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78467a2cc117faa7e4e7cacb62a3f680cfa885e00109a07e8ece2ef220075b66`  
		Last Modified: Tue, 03 Dec 2024 10:21:37 GMT  
		Size: 5.7 MB (5668436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:202530f15a1437ccb1f24e75717ae51b42f3d51bfcc6e800350e5838ebebad24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2432116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ef5bc8d78a812a4b3b4e3d829ad4be7f4ecbbff0f163573419c14399ddf619`

```dockerfile
```

-	Layers:
	-	`sha256:f15a283e05907b6c2e19ac6f58fa3bb9854e3ef2cbdbfb1bf369fd0b341d857b`  
		Last Modified: Tue, 03 Dec 2024 10:21:36 GMT  
		Size: 2.4 MB (2420449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d18918bd05ba355ee74588ba56e495804701a1ea5c84aeb77cdb70f08580adc`  
		Last Modified: Tue, 03 Dec 2024 10:21:36 GMT  
		Size: 11.7 KB (11667 bytes)  
		MIME: application/vnd.in-toto+json
