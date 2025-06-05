## `hylang:1-python3.9-bookworm`

```console
$ docker pull hylang@sha256:be890a5f9ffb6cdd59dc71d79434503ce78fddc4f7826f9bc69a5a2e0511c40e
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `hylang:1-python3.9-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:4c3662bd300bd1233f1a0036390fdb544d8e7705113968f9002958b34dd93fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50346657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7702676041ee7a217779b8605c26c6a68d85b1ca591e411bcb10bb1f028332d3`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 04:24:53 GMT
ENV LANG=C.UTF-8
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_VERSION=3.9.23
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_SHA256=61a42919e13d539f7673cf11d1c404380e28e540510860b9d242196e165709c9
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73a592742abbfe5c0cfc80b46c9df7cf9d437a5b2befb649f2e05d6c81e3d8a`  
		Last Modified: Wed, 04 Jun 2025 17:11:34 GMT  
		Size: 3.5 MB (3511863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710d06b8662fc988997562b77420f175c5f9e936db9a21a6068117f862b440d3`  
		Last Modified: Wed, 04 Jun 2025 17:11:36 GMT  
		Size: 14.9 MB (14937198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a36dc9f4d241af26cee9dedbfc1769eedc458583219fbd5da1d595bdb27e3a8`  
		Last Modified: Wed, 04 Jun 2025 17:11:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8aff6af9d8ab893908c2d3c9a1e5c9c33e0c1163a8c91a3211ee95d28ae54`  
		Last Modified: Wed, 04 Jun 2025 21:28:49 GMT  
		Size: 3.7 MB (3672017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:21035e71e04b86bb8933a2f086287dd4ac325a5e1c1031d96b24d1d28a894a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2495864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a948b94f36f9dc552cdd4780fab90221d25441874e0ec9138be1811ff25a033`

```dockerfile
```

-	Layers:
	-	`sha256:f5188ccbc5933004d2305693c63daf089350831f30c5b67adcd120d4a892c2ea`  
		Last Modified: Wed, 04 Jun 2025 23:25:09 GMT  
		Size: 2.5 MB (2486607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5816daace1757f7b15bd4d441b6ab57de0646b2915c9ea99b97cf5e7031f7d08`  
		Last Modified: Wed, 04 Jun 2025 23:25:10 GMT  
		Size: 9.3 KB (9257 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:706e605843aced2d3a5b085b098f21b53d0d19915e51ea7cc25d5c31b3c82f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46879862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b6ca3de66078f4ab9e51d179cec9782b54261ea184cbbf7c8553c99123df84`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 04:24:53 GMT
ENV LANG=C.UTF-8
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_VERSION=3.9.23
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_SHA256=61a42919e13d539f7673cf11d1c404380e28e540510860b9d242196e165709c9
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Tue, 03 Jun 2025 13:33:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dbb1b0ed7af2455215de8a12234a760614bfce24304f66df8e2699b6b0bc7b`  
		Last Modified: Tue, 03 Jun 2025 14:17:56 GMT  
		Size: 3.1 MB (3085107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7422e697f5cad618f927d7fb915f8592d25e808f8bb4f8b94d8e0b347b3e5027`  
		Last Modified: Wed, 04 Jun 2025 19:35:50 GMT  
		Size: 14.4 MB (14365474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4f68c1d4c24afe755e8d8b281ee8c3531d0ae7974a8e8e50c5f49fb4a1717c`  
		Last Modified: Wed, 04 Jun 2025 19:35:48 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffe451dffb6a778af9ac759b4e1c89ca0a2a36812d4b15875bd7e05022a4cd7`  
		Last Modified: Wed, 04 Jun 2025 20:12:44 GMT  
		Size: 3.7 MB (3672135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:784c261fd8c7b8d7b21340b69ad2f3c49844df2cec84ffa36e049452a637aee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2499824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5047df46246c805a705246ad93bf025464bebd916ff87cf06f5a902b218100`

```dockerfile
```

-	Layers:
	-	`sha256:1899cee77d5b033099bd0d83901ac5cef14a2c15029c85b2603cf5619314e75a`  
		Last Modified: Wed, 04 Jun 2025 23:25:14 GMT  
		Size: 2.5 MB (2490459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d9efaf5cb00c547e72d9ba04cb8942857763353f18f74312eb550c239faec34`  
		Last Modified: Wed, 04 Jun 2025 23:25:15 GMT  
		Size: 9.4 KB (9365 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:014b4e42c9c9e1590c6892107f2540385d59a1f58a171e5f7122968d901b3009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44481411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffba8ef042a1e0d6ec4b52ee8ec5aa4be86c4dc85bcbef2b0cbf8a7091c60f7`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 04:24:53 GMT
ENV LANG=C.UTF-8
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_VERSION=3.9.23
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_SHA256=61a42919e13d539f7673cf11d1c404380e28e540510860b9d242196e165709c9
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5aed779e778c4054c34e61c867da804b23413d3f5e1e9c3cbfb6f69e46db8dd`  
		Last Modified: Tue, 03 Jun 2025 13:31:48 GMT  
		Size: 2.9 MB (2919678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeca08acafca28c65f3bf9e0a12d93befea2055112fda4dfb5165a4bae0cb45`  
		Last Modified: Wed, 04 Jun 2025 22:52:35 GMT  
		Size: 14.0 MB (13956459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ae2c965991098b3ced60dfceb8d4baeae0c1b49d5ba7d796cbea87f8640cce`  
		Last Modified: Wed, 04 Jun 2025 22:52:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3c25805034414ef1a4def82b5c7db921913f8a1f0ddf5be440583dee12aace`  
		Last Modified: Wed, 04 Jun 2025 23:25:57 GMT  
		Size: 3.7 MB (3672103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:50ed51d439356d3f0a88d8e28e2db273de54e1faafe8e7bcff81195e724ce90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a0f87f81c5c250642d86d9cc6826bb76c48bd3ae14d07e2a04df748e179616`

```dockerfile
```

-	Layers:
	-	`sha256:70d549ec99a0278c2823d93f129a6d7e1515a52c86b6df30c601560e3c8e83fd`  
		Last Modified: Thu, 05 Jun 2025 02:19:53 GMT  
		Size: 2.5 MB (2488908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f19064d71cdcf1327a9e167451973d6b74d09b72c85ae8c413eac83aa4a5858`  
		Last Modified: Thu, 05 Jun 2025 02:19:54 GMT  
		Size: 9.4 KB (9362 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:801037eeac601494d74cbad9c91e81cac72b5d33fd2cf31a33b7ec32578d30ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49916158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8e4d73e41edbf625de88ec800db3ad3be3239f2575f8c519efc23490b9a7c5`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 04:24:53 GMT
ENV LANG=C.UTF-8
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_VERSION=3.9.23
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_SHA256=61a42919e13d539f7673cf11d1c404380e28e540510860b9d242196e165709c9
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7840cd825272881c40e91120a55b4d26f7e5829aa530409b56fbc4831b2f944c`  
		Last Modified: Wed, 04 Jun 2025 18:35:46 GMT  
		Size: 3.3 MB (3333501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17505ccc358e867fae756b47794e9cc494d4593818c33c2e5e91c94ec9388a53`  
		Last Modified: Wed, 04 Jun 2025 21:03:17 GMT  
		Size: 14.8 MB (14845174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbdd9ef24b8073f9b8789eeb7cf7b69fedb88f8ce6c75a4fefe52cb5a3b842f`  
		Last Modified: Wed, 04 Jun 2025 21:03:16 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7fe0358d1359e87000114fe40f144bda5ddf58fd775b17e15e91fd6702d659`  
		Last Modified: Wed, 04 Jun 2025 21:55:53 GMT  
		Size: 3.7 MB (3671953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:19f307b65075eefe81d1c24b573d380fbf5ff3ce509ee932c4fff7456a816caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2496337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826dc867b7b5a5cb3414c7d89ed45ed9fd59eef2183aa79edd1566e647b75ab3`

```dockerfile
```

-	Layers:
	-	`sha256:d558a638d4411304b5477b323dbbacc9c6754820d09f45f1f83d4ba8cdd5850e`  
		Last Modified: Wed, 04 Jun 2025 23:25:21 GMT  
		Size: 2.5 MB (2486928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c17d5508c7d1bbcecf11f20882b65d0ca8af1f5e39b76e22f6bea6ee3329105`  
		Last Modified: Wed, 04 Jun 2025 23:25:22 GMT  
		Size: 9.4 KB (9409 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:62fc25b7d71ed1dbf0621ab7bcbeb37d920e65a13ae5956bd3cae7809cd0adc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51573613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b8ad76c5c9a2ac1e2cbc22a54d5469e63f1c97daedf1cf8fa534ee200aac40`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 04:24:53 GMT
ENV LANG=C.UTF-8
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_VERSION=3.9.23
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_SHA256=61a42919e13d539f7673cf11d1c404380e28e540510860b9d242196e165709c9
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Tue, 03 Jun 2025 13:37:03 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adeeeacf53ca5da1536937a21fb82ce12bb7fcc07e97a2de6504154b4bfe4da`  
		Last Modified: Wed, 04 Jun 2025 17:13:03 GMT  
		Size: 3.5 MB (3511165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455a90d1bc50e0f326fdc0790e4087d18d8392061cd2f67f897a5d182d6a4e9a`  
		Last Modified: Wed, 04 Jun 2025 17:13:05 GMT  
		Size: 15.2 MB (15182651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0598c1a551677fd16b259feb5441bdb3e21e4a7434fcc7cac51bc653e73bfaad`  
		Last Modified: Wed, 04 Jun 2025 17:12:51 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c22e82033990b573f2a8e5214d1b56a78fea9c4e89a0a435e38395476b8e1c`  
		Last Modified: Thu, 05 Jun 2025 02:02:53 GMT  
		Size: 3.7 MB (3672061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:70c70adfc4935642cce1618c9b933c0ed8eb443445c380282d6e49eeb3e86756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2492943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fcb4302b36ef194a726d2b2328d30bef540c7c84aba94198db06ff5cfd3b8f4`

```dockerfile
```

-	Layers:
	-	`sha256:68d79d6f4386c8125a4ab1b833f02c09458833a2f2fa4c5a8b1981dee4b7936c`  
		Last Modified: Wed, 04 Jun 2025 23:25:26 GMT  
		Size: 2.5 MB (2483738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fdc3918c60ca9e97ac52d5baa46d3a2af3fb6f93902af2b1b687c961e5b91ce`  
		Last Modified: Wed, 04 Jun 2025 23:25:27 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bookworm` - linux; mips64le

```console
$ docker pull hylang@sha256:fec016aee9b264ef258b39ccee104b5673430d2e4ff81ca2ff7b2537a512899a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49713627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f883eeb5692e888ecb9664b64ff33800300756811f146b0b2d3d5f1756c01b`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 04:24:53 GMT
ENV LANG=C.UTF-8
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_VERSION=3.9.23
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_SHA256=61a42919e13d539f7673cf11d1c404380e28e540510860b9d242196e165709c9
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Tue, 03 Jun 2025 13:38:52 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b500706b1904f9eade4bd0d756b7fb8b21d3bb95a0e43bdfe52cf7350b996346`  
		Last Modified: Tue, 03 Jun 2025 21:17:58 GMT  
		Size: 2.9 MB (2909615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7606ac40173ceba8b8f6d1f595527cb93c463e0b2976edd97bf07787b9241188`  
		Last Modified: Wed, 04 Jun 2025 17:57:35 GMT  
		Size: 14.6 MB (14619726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6630036131d036274277d00fdcd9fc03de0ca443431a7df60cb04b1ce539879d`  
		Last Modified: Wed, 04 Jun 2025 17:57:34 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bc6d810538e474042bba1346efd6ab1fe2accee742045463fed5dca40ec6be`  
		Last Modified: Wed, 04 Jun 2025 18:04:30 GMT  
		Size: 3.7 MB (3672188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:2b5eb4a7154e9b2703355b08b395957b37bf404d8f35b5119f5e9a08f2c8a939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaabb507c6866063652de7f655074a781ed3959574549680a77bc9dbba3c976`

```dockerfile
```

-	Layers:
	-	`sha256:07ce001f2e5300928b50706de1580fc76dba371f438fdf2f2ddf6f0f9965468e`  
		Last Modified: Wed, 04 Jun 2025 23:25:31 GMT  
		Size: 9.1 KB (9144 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:02077a5621d7c65748d704bf92e92e8b3d29e6ac9879eca4079b2664785fc75c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (54995543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab388a92d34295e03352a338f5c466f2224c1fc9514848d4699a29696617c02`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 04:24:53 GMT
ENV LANG=C.UTF-8
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_VERSION=3.9.23
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_SHA256=61a42919e13d539f7673cf11d1c404380e28e540510860b9d242196e165709c9
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284fe4671330599295ea2aa5b4306fd8ab83755805e45a47ecd4cd60a67af718`  
		Last Modified: Tue, 03 Jun 2025 13:42:08 GMT  
		Size: 3.7 MB (3716183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45fdd22872594a187ceaf0bca092c87f34f1d6f6da15c48f91a22c4befc9afa`  
		Last Modified: Wed, 04 Jun 2025 20:08:23 GMT  
		Size: 15.5 MB (15540034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9014ebbe2eaf9dc4deacc437b5a7590e0a1c6a10df92df1fba10fc9d42a07f1`  
		Last Modified: Wed, 04 Jun 2025 20:08:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc632d6ccf95921de3c9f4d0311357672bee1afbb4cbf6bcf8d61f8af39a094`  
		Last Modified: Wed, 04 Jun 2025 20:52:16 GMT  
		Size: 3.7 MB (3672165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:552496e5c5adc0df90838bcbfded0ee65287a2c2bc4f87ca589d8765a3a12753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2500460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1adb272866823ed68cda9814f706c17e2fdff0626ef98cd78b08e89c269b30a3`

```dockerfile
```

-	Layers:
	-	`sha256:389b972abcadbc8901466e1af08e40e601b4037751e68fa2d055389c5477f0e6`  
		Last Modified: Wed, 04 Jun 2025 23:25:35 GMT  
		Size: 2.5 MB (2491137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fdac76728c53d24b9dcbad21dedd50b68b2852bcb396419b6c21a2d75b6c506`  
		Last Modified: Wed, 04 Jun 2025 23:25:36 GMT  
		Size: 9.3 KB (9323 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:0591f2c7276cdd26e0bddf89185c9c2a81b54d58685818c273271e613aebecdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48452477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38acf287eb27f0380b3c8565880cf65772168d3cccbce337e9aa0ef09f84a0c`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 04:24:53 GMT
ENV LANG=C.UTF-8
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_VERSION=3.9.23
# Wed, 04 Jun 2025 04:24:53 GMT
ENV PYTHON_SHA256=61a42919e13d539f7673cf11d1c404380e28e540510860b9d242196e165709c9
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 04:24:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d718881e7dc24c84b353b68bbc5ea4d8da2442eab69433253c52d5adf961304f`  
		Last Modified: Tue, 03 Jun 2025 13:42:03 GMT  
		Size: 3.2 MB (3175300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c903d620356d430d5cd04739e772761d4c8f85754df5c7982249c6629719cbde`  
		Last Modified: Wed, 04 Jun 2025 21:16:25 GMT  
		Size: 14.7 MB (14722028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b0584f37a4c8aa4fb0e4d23f3a796afea3fc3cd36e0b9e3a8f05536d33151`  
		Last Modified: Wed, 04 Jun 2025 20:19:52 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b2c7b309c634dab41272bf850a65bcd701f76226d308d4b5c3f0f5107d174d`  
		Last Modified: Wed, 04 Jun 2025 20:54:26 GMT  
		Size: 3.7 MB (3672092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:05fff976e4a0f129fe48fc5ed280d556083ccbaaeb360f432676f7dd7bc621e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2495572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c7be28f13c3283fa7b4a68c92ac4ad5d42fb485c64aa5d04d1b268ab4d8a09`

```dockerfile
```

-	Layers:
	-	`sha256:c593b16e1faec7b3eb407b435e5fbf6ad253d7eca69434179781bb7001b7f83a`  
		Last Modified: Wed, 04 Jun 2025 23:25:40 GMT  
		Size: 2.5 MB (2486315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c94a66d54de69d9e6765a19fcfa5b3a5de28e13585dec3d1dfe6afd6eff6a49`  
		Last Modified: Wed, 04 Jun 2025 23:25:41 GMT  
		Size: 9.3 KB (9257 bytes)  
		MIME: application/vnd.in-toto+json
