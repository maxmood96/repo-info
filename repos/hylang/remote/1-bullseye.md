## `hylang:1-bullseye`

```console
$ docker pull hylang@sha256:481977c7685503b5fa446bf8787faffae249594482f9769710a630d57870a7b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:1-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:ccb090885bbc7abd4aff3f62506f4a70d4ee7fede003ce88585a3a0fcb0197f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49762114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21de5cf7449b4dcdfef14768b3f1b3e0ba3c8b3af05ad297d747724d070e8c9`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Apr 2025 19:02:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Tue, 08 Apr 2025 19:02:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Apr 2025 19:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Apr 2025 19:02:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Apr 2025 19:02:43 GMT
ENV PYTHON_VERSION=3.13.3
# Tue, 08 Apr 2025 19:02:43 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Tue, 08 Apr 2025 19:02:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Apr 2025 19:02:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Apr 2025 19:02:43 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9783470cfc7dea3c7978b9153f9ba5ceb5b4d725af39a3e3f649d460f0e007`  
		Last Modified: Mon, 28 Apr 2025 22:14:10 GMT  
		Size: 1.1 MB (1076218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f26434336e9d956b8f530eda26dfeb47910942d93838264b3d82fd9eae8e5e`  
		Last Modified: Mon, 28 Apr 2025 22:14:10 GMT  
		Size: 12.8 MB (12762738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f431ef9e9289f64e46d8b3a1b5510d5d930f0e52b757c50adf76123118e0e8`  
		Last Modified: Mon, 28 Apr 2025 22:14:10 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b826c65090dcfc3ae5fac6ffa2dac7dd2dc4d00da32059c8655c60c20471f08`  
		Last Modified: Fri, 09 May 2025 17:34:32 GMT  
		Size: 5.7 MB (5668304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:8a8e787e7da1d7c076a4ca9910c98c120e0500cb5be304b6eec600b3f89017d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb5b5ab9c9e1dc3fca8caec5e08aa0cd153c36b7fcd21b6a499f3c50b455030`

```dockerfile
```

-	Layers:
	-	`sha256:5eb9510ec22992efa3b7dc4a035b46422b78ff6484adbf329580794b6d475f07`  
		Last Modified: Fri, 09 May 2025 17:34:31 GMT  
		Size: 2.7 MB (2713584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c60a0f93e81605516d9b48d3164839635c5360b6d04a53d517ecb2df324f4a1`  
		Last Modified: Fri, 09 May 2025 17:34:31 GMT  
		Size: 9.2 KB (9245 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:4ae8a6e630210302064ba1a0cc71bcd21fd93d76b10055d2026dda0f48ee2e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44215160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e103eadac0b3e57da8e1e43752ef9d55b847fcce6d1e28c60b3e1c75ad8970ba`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Apr 2025 19:02:43 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Tue, 08 Apr 2025 19:02:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Apr 2025 19:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Apr 2025 19:02:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Apr 2025 19:02:43 GMT
ENV PYTHON_VERSION=3.13.3
# Tue, 08 Apr 2025 19:02:43 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Tue, 08 Apr 2025 19:02:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Apr 2025 19:02:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Apr 2025 19:02:43 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:93c17983cb6e26d53fe6219e705b968f8a22ae1b4cb559618bdff5ba501ae39d`  
		Last Modified: Mon, 28 Apr 2025 21:16:22 GMT  
		Size: 25.5 MB (25542427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098cc8ed368864e2d50e9bc3938fb245bd25c463ac61e14a06c8c19d80e699ec`  
		Last Modified: Tue, 29 Apr 2025 06:39:19 GMT  
		Size: 1.0 MB (1041643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccff666d201eae77b51a3c51ca91d0b768190ee96e2c42ae85ff786ec723ff0`  
		Last Modified: Tue, 29 Apr 2025 07:19:19 GMT  
		Size: 12.0 MB (11962513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c7cf5d3a6bd82ce32df9d7491c259a9d7847477c88bfce88803265d95a6ec4`  
		Last Modified: Tue, 29 Apr 2025 07:19:19 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f428f76ccc00505e9cca6975ea3669e0780d467a5c82f8b2911af8938a493ab5`  
		Last Modified: Fri, 09 May 2025 18:38:20 GMT  
		Size: 5.7 MB (5668327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:faff1a853e16ad1b93efe509f2068823d44dff3995b160e5c4f4cb3b748a36d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2725214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cc6cca186a6d4b5e63cdb7c030bd1463a4debbe0301cee4121e50ad79e21e7`

```dockerfile
```

-	Layers:
	-	`sha256:9d2a6361d3bb6172b4f01a689723fcfb1e1ea14c965e9efe340853b96e2141ad`  
		Last Modified: Fri, 09 May 2025 18:38:19 GMT  
		Size: 2.7 MB (2715861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed3d72d215b8808f6200e636ba98a5d235976bec367cc0b7d5592b7272d1eb38`  
		Last Modified: Fri, 09 May 2025 18:38:19 GMT  
		Size: 9.4 KB (9353 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:685614e690fae8246fe1e9a331843e405e2c7509807c512f62df980df90fdf94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48270683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17a91c9d51fa466ae9124e49a5654540e11cfea0607464b06d589f5e4a226cf`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Apr 2025 19:02:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Tue, 08 Apr 2025 19:02:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Apr 2025 19:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Apr 2025 19:02:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Apr 2025 19:02:43 GMT
ENV PYTHON_VERSION=3.13.3
# Tue, 08 Apr 2025 19:02:43 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Tue, 08 Apr 2025 19:02:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Apr 2025 19:02:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Apr 2025 19:02:43 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8e820d8ec519539a3e949b94cbdee98218a5d49aea1dfb3a4e7fe4c0758e95`  
		Last Modified: Tue, 29 Apr 2025 22:25:36 GMT  
		Size: 1.1 MB (1064047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff9367544c4ea4d53ece27f8a445ffb5a08448c9eef34060309c97714e765fa`  
		Last Modified: Tue, 29 Apr 2025 22:51:59 GMT  
		Size: 12.8 MB (12793314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69eb6693e44ae9d4a85aa9653c2e432e43f25a106e4736aaf4e619fa560518a1`  
		Last Modified: Tue, 29 Apr 2025 22:51:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc963ca663beed48242ac3945c5ad2bdccb91c80c2ccab35c3cc2ef5bac64511`  
		Last Modified: Fri, 09 May 2025 18:50:56 GMT  
		Size: 5.7 MB (5668428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:d997824a235efc0635ccb388b058dd752f857d1f8710d8dd1b7e904c38fd4eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2723288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13959d53ca4c196de07ece9ab9109cb1fdec384ca9d16319f2504e7795e6511e`

```dockerfile
```

-	Layers:
	-	`sha256:246957059c9824553e7b4fc1c1f2c71c3768d186aed7331d0f00df778cf41bef`  
		Last Modified: Fri, 09 May 2025 18:50:56 GMT  
		Size: 2.7 MB (2713891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b07832ce087d3bce9eb5e139f895b101882767c7d5207ef6aa0871b6d4473fd`  
		Last Modified: Fri, 09 May 2025 18:50:55 GMT  
		Size: 9.4 KB (9397 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:f14c6eb00c471818f9e1a1be22e4aec5a59af1bd4a0ebe90b4030c13aede252e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50857497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca15d94fc59b83073d7732ad4e1d2e60ac73e5bd82da5d31097d22def0d5761`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Apr 2025 19:02:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Tue, 08 Apr 2025 19:02:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Apr 2025 19:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Apr 2025 19:02:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Apr 2025 19:02:43 GMT
ENV PYTHON_VERSION=3.13.3
# Tue, 08 Apr 2025 19:02:43 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Tue, 08 Apr 2025 19:02:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Apr 2025 19:02:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Apr 2025 19:02:43 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:73bb1b80ecf1f8784ad6f92a35120b6e2306657fc7e8cbaedca1f45900f3d746`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 31.2 MB (31187893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464cbd9f97f03fce6b34d5f997006e1545d8dec35137e2cc8eafc06f9243b083`  
		Last Modified: Mon, 28 Apr 2025 22:26:47 GMT  
		Size: 1.1 MB (1088770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393566571d9e57acbbe5fa35c893c9fba89e424e258ad502fb72e9a202a3f170`  
		Last Modified: Mon, 28 Apr 2025 22:26:48 GMT  
		Size: 12.9 MB (12912233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6537e97df76878b0c7b859ec9ea2400d6300bcfb9a5ad10a7995f4e8b5b7467b`  
		Last Modified: Mon, 28 Apr 2025 22:26:47 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99e83c48e2407a6619f191d948bc4d18ce6dc375591b48277ed64699ece09f5`  
		Last Modified: Fri, 09 May 2025 17:34:25 GMT  
		Size: 5.7 MB (5668351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:cc2716112ce48a748523204289a61927dec727805c1eeddb4e55417b4ba1369b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2719869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23d3c470f85fb74bf57e6a4d361f3046ffd1fb4b16c83c85b2f19c2ec90832a`

```dockerfile
```

-	Layers:
	-	`sha256:38f178fe1f18906cff9ffe4445e1c36816b061e2c0103191f57c03a28dc4eee1`  
		Last Modified: Fri, 09 May 2025 17:34:25 GMT  
		Size: 2.7 MB (2710676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3830b1784740b6cb52c644c40b6a3318f889bc0e50e8756301e6dffd58e040ee`  
		Last Modified: Fri, 09 May 2025 17:34:25 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.in-toto+json
