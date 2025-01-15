## `hylang:1-python3.10-bullseye`

```console
$ docker pull hylang@sha256:11b969bb94f6fc257f23f8dea017dd9be53232520cc75f6c0fdc51fc98b85c81
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

### `hylang:1-python3.10-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:fdcfc2b6c9120a9f9a8fc73944ed99e5176997da07644f862aca2c448cef28f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50151491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c4c2c74685d5d9a68d2ffe0b2d3a4153db4c7a6a3b8a4f896ab9e051c9daac`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 16:49:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 16:49:14 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PYTHON_VERSION=3.10.16
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PYTHON_SHA256=bfb249609990220491a1b92850a07135ed0831e41738cf681d63cf01b2a8fbd1
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
CMD ["python3"]
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2423cd12b377542230fa555c39797af2c63448e676e2e9eff4e7df1cf166dbc1`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 871.2 KB (871220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f46495f9a932e021935be03d2bddaaeaaaa9511ebe5bebb7a12fcafbd03f3db`  
		Last Modified: Tue, 14 Jan 2025 20:34:34 GMT  
		Size: 14.8 MB (14843225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949f78b58d7064d9b41dda967ee08fb0d478c5229b1fc7c7950151bde1770883`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac60e8a62ed830e877d5bf06f160c86eb7eb300d20bbbdd1decb9007d1797ca0`  
		Last Modified: Tue, 14 Jan 2025 03:26:08 GMT  
		Size: 4.2 MB (4184131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:89a421e8216e18e0889c9878f77ab5f9f756ab121556e4d3af61f3325e391f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2723248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d473bd48c2904bb97b26b843bd0202c1913ab57f9671f4ecfb452f90c5ba14`

```dockerfile
```

-	Layers:
	-	`sha256:5f4955809d8cdd14b76d7d6b43531734553a04249b4a289989e0e5f9e3fb33fe`  
		Last Modified: Tue, 14 Jan 2025 03:26:08 GMT  
		Size: 2.7 MB (2715222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2222f763fc8b8c95a1024d8eab94ede85f16d9c62cdd515b600dc94a181e8a85`  
		Last Modified: Tue, 14 Jan 2025 03:26:08 GMT  
		Size: 8.0 KB (8026 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:cf4585b4ca660aa67306fc3794b736f01a30e99c31fdeffaa282fae835cffd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44614950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f22b0218bb0b6e6915decb055ecd0d4b30d37bfd5bc15300ca14d62af6cf9c7`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 16:49:14 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 16:49:14 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PYTHON_VERSION=3.10.16
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PYTHON_SHA256=bfb249609990220491a1b92850a07135ed0831e41738cf681d63cf01b2a8fbd1
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
CMD ["python3"]
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0d436ac8a1fac914a00940d8604851d3414adc2ed370af15a8a5e6b319671b5b`  
		Last Modified: Wed, 25 Dec 2024 01:46:39 GMT  
		Size: 25.5 MB (25533937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47488dd222bf1e5ebfc7794093fc1c5a4434399916ad05161646eb1e9437ca64`  
		Last Modified: Wed, 25 Dec 2024 20:36:37 GMT  
		Size: 836.9 KB (836939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1015e5e3bb4d423230f9b9f9698974f4c58416820f3624526d10c815f18654`  
		Last Modified: Thu, 26 Dec 2024 10:39:22 GMT  
		Size: 14.1 MB (14059585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd5d0b8572dc9663b5fb41b239376f65b53dcf46b628a6aa08c5a1707265040`  
		Last Modified: Wed, 25 Dec 2024 15:39:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7a956b88987860d3f6b9cba8320d99cd35f0fd854d97056c0baa939c292a15`  
		Last Modified: Thu, 09 Jan 2025 22:58:34 GMT  
		Size: 4.2 MB (4184240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:4d2ef84982fb6e42bf113df430c8ef6edd6ef3390e19de33f955cfd88a19b5e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2725570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c0570b0c30ff597cb1c5b0fd3ac92d22854b7fd7196ff8c2e44aae24b0bcf3`

```dockerfile
```

-	Layers:
	-	`sha256:59f94fb684d199ab0b55c53aec575f91148289fa3c71cb78e4686254aec45bae`  
		Last Modified: Thu, 09 Jan 2025 22:58:33 GMT  
		Size: 2.7 MB (2717467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe71d1bac65f28e8f94937e358e5e9ea22be3b397d4d5fcf27cc68e25799d663`  
		Last Modified: Thu, 09 Jan 2025 22:58:33 GMT  
		Size: 8.1 KB (8103 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:568ca66c088689f0643195f64dd32be95949e2fda55b3f4d51e0383fe84b8824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48667172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a2536b048ca2ffba023c49553f100de96b5e7d27c5c37c19afe00f131d9fad`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 16:49:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 16:49:14 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PYTHON_VERSION=3.10.16
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PYTHON_SHA256=bfb249609990220491a1b92850a07135ed0831e41738cf681d63cf01b2a8fbd1
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
CMD ["python3"]
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 20:33:33 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64757e3dbded90ef62713320bdf990f6a446c544004f498e303e366605b97b2f`  
		Last Modified: Tue, 14 Jan 2025 10:33:50 GMT  
		Size: 859.2 KB (859151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319aa994348ecb680d4dbb64ce54cc425fccf73dfc26d1f19df12815d84a8af2`  
		Last Modified: Tue, 14 Jan 2025 20:36:56 GMT  
		Size: 14.9 MB (14878645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b529a31adb09e7a8641a296c9446437ab40f5820e9d70416668ec2a074f0f2a`  
		Last Modified: Tue, 14 Jan 2025 11:14:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1eda275a7663970fc72d342d0f2ec491c7cab1e6a4641d99d427c7033addfa1`  
		Last Modified: Tue, 14 Jan 2025 16:42:32 GMT  
		Size: 4.2 MB (4184215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:5895bd330b42dd3f1efb6fc26a0822e5d4dd61111b3b630091686556cb1d79b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2723612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51cb8c0ab94c642315224b6abf4eea65395d5143efdfeadb6ce7f8101260c8aa`

```dockerfile
```

-	Layers:
	-	`sha256:f73c0252239b3af0a6a6af38354137cc4d4bcfb2fd5531f5f5a9a7451933709d`  
		Last Modified: Tue, 14 Jan 2025 16:42:32 GMT  
		Size: 2.7 MB (2715481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49429ef8895f1815f657c6887b3c51697c9aaeb4f28acd34fb60a598e08d7a99`  
		Last Modified: Tue, 14 Jan 2025 16:42:31 GMT  
		Size: 8.1 KB (8131 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:3ae27240fa8394a63605c59f85b3493e4a0045e6f72d1d69c73c9127903e0a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51203964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1acf611728aabb5a534fac1071609161a131ddd709828cd41986669c3fbec900`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 16:49:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 16:49:14 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PYTHON_VERSION=3.10.16
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PYTHON_SHA256=bfb249609990220491a1b92850a07135ed0831e41738cf681d63cf01b2a8fbd1
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
CMD ["python3"]
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 20:37:11 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167f06b004cc155e9ca17d0306fac46bc00cbd6ac07bb0633fd715c9e7c050e7`  
		Last Modified: Tue, 14 Jan 2025 02:47:47 GMT  
		Size: 884.0 KB (884047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1d5ec83e29be9e8c7108099e7e58968c22429aecd6ed30e0998e00504ea679`  
		Last Modified: Tue, 14 Jan 2025 02:47:47 GMT  
		Size: 15.0 MB (14956532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c18e6691d15b87e51a7b608f168506c0f1ea6b9d66ef233c8ffc1b8afa57fe`  
		Last Modified: Tue, 14 Jan 2025 02:47:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3175249c6249061944a0c7574c51dabad79ace99d86ffb690cd27d9886f1efd`  
		Last Modified: Tue, 14 Jan 2025 03:24:59 GMT  
		Size: 4.2 MB (4184108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:71d59cf6335516629f6fea7dd613c7bcc53aa8e3e32eca35c635b99eda65f004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695665f7debefc7050c25e8bdc48b8a26b56d89b3bad1f0d2f92832a74ef5da6`

```dockerfile
```

-	Layers:
	-	`sha256:ab1bf8477a6309a95c3bbe523f5a574f7a92cca73271dff89132683e9a671450`  
		Last Modified: Tue, 14 Jan 2025 03:24:59 GMT  
		Size: 2.7 MB (2712334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:393a3a514238df4656145125f6bb1138464a4ed576b667bbd248013948f8cc8f`  
		Last Modified: Tue, 14 Jan 2025 03:24:59 GMT  
		Size: 8.0 KB (7994 bytes)  
		MIME: application/vnd.in-toto+json
