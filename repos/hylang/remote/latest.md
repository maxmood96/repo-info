## `hylang:latest`

```console
$ docker pull hylang@sha256:2e6dab65d77e4a25bfe88c106f6c84b64bf5602f00d7de7638aaec14e494fefd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `hylang:latest` - linux; amd64

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

### `hylang:latest` - unknown; unknown

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

### `hylang:latest` - linux; arm variant v5

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

### `hylang:latest` - unknown; unknown

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

### `hylang:latest` - linux; arm variant v7

```console
$ docker pull hylang@sha256:8fd7523070f58134d1717b1629c65c642ce0c143ef36ac611686691fc6d0928e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44974127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949cbaa10702f5b0b8234601cec9f8ba84d102d2dec3ace8478724fee188ed61`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["bash"]
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
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c4bfae3208db1cc5e6056b1b437ead34955dc06d861e28ba3a55e24b0f301f`  
		Last Modified: Wed, 13 Nov 2024 01:46:58 GMT  
		Size: 2.9 MB (2914823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06f4b6a431b83dc17644f0fd7cdb4a938941d112cd8b73d34da99ea24db8b9d`  
		Last Modified: Wed, 13 Nov 2024 02:42:17 GMT  
		Size: 11.7 MB (11663486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54010aca04da3581fe07f44ffe67f44ed1da83640f2121fdc7681aee5b50008c`  
		Last Modified: Wed, 13 Nov 2024 02:42:16 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb64a2fd118081291fa01b14f80e444ad6c2ad0f5341b26964b7148f6dc656ef`  
		Last Modified: Wed, 13 Nov 2024 14:47:19 GMT  
		Size: 5.7 MB (5676660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:latest` - unknown; unknown

```console
$ docker pull hylang@sha256:611fc192905c9da9d7fc3f60fcf5b49cf63376d529e3fa5ed8241349ed2d8811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2436159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efea855d7a5da8834c0d052a69d9441ac06369ef9383d57093103d76373c1456`

```dockerfile
```

-	Layers:
	-	`sha256:6526834297edabfe1f3e5d90424316da35e53e9d783ed3fb51639649ddc25935`  
		Last Modified: Wed, 13 Nov 2024 14:47:19 GMT  
		Size: 2.4 MB (2424320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c35753e0b0206c0a13e4aea90622d0019e89680c717b02a77850993d2c72fcc7`  
		Last Modified: Wed, 13 Nov 2024 14:47:19 GMT  
		Size: 11.8 KB (11839 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:latest` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:6a87818aa8ade6ef5358cdf14e744ed0d4839f2ccbae3532b6644a778b0e5668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50595510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b40a30b839626bca420574af896b708bfe53be1a65fbd8414e814a24b05e3e98`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["bash"]
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e91ee31b4ebfcb39ea9ba6ce1a809ecf2cb20e34911e24306f962f7038edfcc`  
		Last Modified: Tue, 12 Nov 2024 20:26:43 GMT  
		Size: 3.3 MB (3332014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7e82f83815d599042146404728cc6e0507b18ad1d6b67319b7e9cd30f25fff`  
		Last Modified: Tue, 12 Nov 2024 21:06:38 GMT  
		Size: 12.4 MB (12429079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce972ab4a43b26d6ae3a965effd4c0401c5d41132676ad6f906957212879974`  
		Last Modified: Tue, 12 Nov 2024 21:06:37 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ca85d9a36f75157831b95685e92af831d68c70eacb1331505df48bf2ecea6e`  
		Last Modified: Wed, 13 Nov 2024 07:19:16 GMT  
		Size: 5.7 MB (5676812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:latest` - unknown; unknown

```console
$ docker pull hylang@sha256:abd037553e3b1e988092e9553ef862432947bad4d0b37d42ec35f0324957c645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2434303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357d94f198aa32fea6064b0939abad6ab9a06e69d93781758c2683b785d0d2af`

```dockerfile
```

-	Layers:
	-	`sha256:cd8c8b4f9b993c5d8509d40ad25626a5eb691173e16b8c58c3238c231fe63593`  
		Last Modified: Wed, 13 Nov 2024 07:19:16 GMT  
		Size: 2.4 MB (2422388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74a9c4e0b9ef395bd8a89c997f4406d1202472fcb372555bb8d85658d117c7bd`  
		Last Modified: Wed, 13 Nov 2024 07:19:15 GMT  
		Size: 11.9 KB (11915 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:latest` - linux; 386

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

### `hylang:latest` - unknown; unknown

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

### `hylang:latest` - linux; ppc64le

```console
$ docker pull hylang@sha256:499065f0ae20bf8935c61026b39fc16a79120807bcde8ea19a790d2c2e5f892a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55542485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352dd7dc72c15d1d7647451b46385216f8a6f183d712afc9a127adefa711cb20`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["bash"]
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
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3763d3cbcc89420e3619a6d313adf9fd5dce8940eb31b61d8544d75a713990ca`  
		Last Modified: Tue, 12 Nov 2024 11:29:49 GMT  
		Size: 3.7 MB (3713651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f31553e39e713cf02a0c0d38e23162f6b9f89369c6fc5c72bcd849cfa3626ad`  
		Last Modified: Tue, 12 Nov 2024 12:04:41 GMT  
		Size: 13.0 MB (13026419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e68ed501c534290430a491c3859e98a6b1e059420174feeab6a4081ce32c55`  
		Last Modified: Tue, 12 Nov 2024 12:04:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e375f7460130d9e8e2e3f9c21e792f958b7c46fa672be4228b5e5454474a1422`  
		Last Modified: Tue, 12 Nov 2024 23:17:09 GMT  
		Size: 5.7 MB (5676813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:latest` - unknown; unknown

```console
$ docker pull hylang@sha256:09e4f692628d942925ab1c608f3c6ec9f0eaa678427347b9f119f0312ee76c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2438170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f3ce1ba3f422b020842406331c297548d982fd7b2b7bb0bef9bd79803d11e9`

```dockerfile
```

-	Layers:
	-	`sha256:16476a4a9fa5077f9fe924296810077e8f79912bd4c4674362a45cb100a535d2`  
		Last Modified: Tue, 12 Nov 2024 23:17:11 GMT  
		Size: 2.4 MB (2426389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f86b6864941d1971c925172315fee3e203bb08428eec1186cfc2572563c97a9`  
		Last Modified: Tue, 12 Nov 2024 23:17:11 GMT  
		Size: 11.8 KB (11781 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:latest` - linux; s390x

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

### `hylang:latest` - unknown; unknown

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

### `hylang:latest` - windows version 10.0.20348.2849; amd64

```console
$ docker pull hylang@sha256:4d8b135b816c875e148c059b8178b7249fb5517cda8dc4b07ed9e8559200c716
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2319759174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d08fba1229212318206eb52f2627b030bd8eccc2d8ccc08862f38befa2e418`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 20:17:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:17:13 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 14 Nov 2024 20:17:13 GMT
ENV PYTHON_VERSION=3.13.0
# Thu, 14 Nov 2024 20:17:14 GMT
ENV PYTHON_SHA256=78156ad0cf0ec4123bfb5333b40f078596ebf15f2d062a10144863680afbdefc
# Thu, 14 Nov 2024 20:17:55 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:17:56 GMT
CMD ["python"]
# Thu, 14 Nov 2024 21:12:15 GMT
ENV HY_VERSION=1.0.0
# Thu, 14 Nov 2024 21:12:16 GMT
ENV HYRULE_VERSION=0.7.0
# Thu, 14 Nov 2024 21:12:49 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 14 Nov 2024 21:12:50 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81c2266e7829c520aa3c90760450f9de85265d31ef76e07c116d21d86cb9d5`  
		Last Modified: Thu, 14 Nov 2024 20:17:59 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bf73e26732f051db38c88937e307507b46733de79214bd6526da79565b0467`  
		Last Modified: Thu, 14 Nov 2024 20:17:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84bd722ec005c4b9a8d4ce74d1547245ee36e178a58fbca74ea8a88b83557a2a`  
		Last Modified: Thu, 14 Nov 2024 20:17:58 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e33fa699c69073e7247ec2d3a42da4118d465f9912cba354ef0845112bcffd`  
		Last Modified: Thu, 14 Nov 2024 20:17:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ee35dfd6d09fa868757d9bc44d68b28573a959fe0a6fe736dc0b05b3a790a5`  
		Last Modified: Thu, 14 Nov 2024 20:18:03 GMT  
		Size: 58.8 MB (58759488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65c7965bd14123d662cc223a68643149c706713ffcb3745193c4f5c3c25c928`  
		Last Modified: Thu, 14 Nov 2024 20:17:58 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e07266d2cea44aecb5d30adb04f6d73c00606280bf31d67d640a3ea87f1fcac`  
		Last Modified: Thu, 14 Nov 2024 21:12:54 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f08dd223ce66d449267fce757e208ffc24005e2e75c5c4e6d59e223af112a86`  
		Last Modified: Thu, 14 Nov 2024 21:12:54 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37d4c55c1255f60be419b629fc03f8f0c77c3d4def3cf2bf0b39ead371b1078`  
		Last Modified: Thu, 14 Nov 2024 21:12:56 GMT  
		Size: 8.5 MB (8505186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774fc1e7a8dee14f85e5c4bfbf68baf93ed53ab298ecefac245c7f698976e1a3`  
		Last Modified: Thu, 14 Nov 2024 21:12:54 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:latest` - windows version 10.0.17763.6532; amd64

```console
$ docker pull hylang@sha256:edcd603cb84f0fc5d27f5121ae355b1838d6b79e8c5a90929daf847cb8f48191
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075407082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0df8fee57532535c0482b33a338388f11d9ba66c69b75faccdd8a07087e8de`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:18:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:18:32 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 14 Nov 2024 20:18:33 GMT
ENV PYTHON_VERSION=3.13.0
# Thu, 14 Nov 2024 20:18:33 GMT
ENV PYTHON_SHA256=78156ad0cf0ec4123bfb5333b40f078596ebf15f2d062a10144863680afbdefc
# Thu, 14 Nov 2024 20:20:18 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:20:19 GMT
CMD ["python"]
# Thu, 14 Nov 2024 21:21:42 GMT
ENV HY_VERSION=1.0.0
# Thu, 14 Nov 2024 21:21:44 GMT
ENV HYRULE_VERSION=0.7.0
# Thu, 14 Nov 2024 21:23:08 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 14 Nov 2024 21:23:09 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33faaaa342cf5ea879707bfd0ec7e1bbf9e55acf595859c29002cda9715d0759`  
		Last Modified: Thu, 14 Nov 2024 20:20:23 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9e048993d10b503629950c8739bcaa886395e07d4c2d631243230cd9aba76e`  
		Last Modified: Thu, 14 Nov 2024 20:20:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e911286c397244c6526ae07c7a27e450803cfb341fcdd0cbb78d3cfae16e84a`  
		Last Modified: Thu, 14 Nov 2024 20:20:22 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeaacbff3cb119c2d8df7a9b839be99cdd3a84a917fa164f9bdaa059c6205565`  
		Last Modified: Thu, 14 Nov 2024 20:20:21 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9c8be745b040cec06d795882cf237a5a0e125713165574534a245acb33b41c`  
		Last Modified: Thu, 14 Nov 2024 20:20:27 GMT  
		Size: 57.6 MB (57595680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f20e1b3af557ac4be54eab69100ce39ba15cc0c1650fe5c0261caf2a4ee292b`  
		Last Modified: Thu, 14 Nov 2024 20:20:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b5b684c8cd7c0fd9cbc0dac4db677b299a73f9a06c8253a8cc2c48b83218ef`  
		Last Modified: Thu, 14 Nov 2024 21:23:12 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b7f8c98afb324ca1c0b23f80e111856cf86887b993f8d0ab7573f86d5c0520`  
		Last Modified: Thu, 14 Nov 2024 21:23:12 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc729ec1d74c0871da42a2ce0dd9d7618daaaf42c49b85eeeaae82a438f08ee`  
		Last Modified: Thu, 14 Nov 2024 21:23:12 GMT  
		Size: 7.1 MB (7147124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fb684e7eb92905544262646dd35b40a5cd4bb6f5b831b64b216241680cb715`  
		Last Modified: Thu, 14 Nov 2024 21:23:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
