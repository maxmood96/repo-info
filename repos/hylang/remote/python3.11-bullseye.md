## `hylang:python3.11-bullseye`

```console
$ docker pull hylang@sha256:ce9a430501a9440cf3779525305883e75105f1c83c3a9dadee5c3c3b04eba892
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

### `hylang:python3.11-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:b8a8b89778e9337270c83193cc12e4363eba3f66239052e9b81565b8f2b313e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52735475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493ab7d40cb3c3b402af6a3f39182cae53333de12c23871965cdb7028e652f6f`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 22:49:59 GMT
ENV LANG=C.UTF-8
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4839993cd2949e58866f8b820693d4bbe1c749cb85da8c83f630e8aa14266462`  
		Last Modified: Tue, 18 Mar 2025 00:00:04 GMT  
		Size: 871.2 KB (871234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d16b54627905c44e9e9368faa4120c75bd06e960308174b5b41b0035b844cd0`  
		Last Modified: Tue, 18 Mar 2025 00:00:04 GMT  
		Size: 15.4 MB (15405499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a0f782a43531888170d09249617b3ffd01beb79f5bccdc3f77f4f0fdb229a1`  
		Last Modified: Tue, 18 Mar 2025 00:00:04 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595860fbcca3cad700907202fa65fa49234eb85418ed0df95158c5c360ecacd5`  
		Last Modified: Wed, 19 Mar 2025 22:59:05 GMT  
		Size: 6.2 MB (6204656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:def71f74c11af1e9de7cdc30142937517a3561d66810cbad4d7f14bf942c0326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2723209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e2fcbc1376ff852e1abc6d49761c176a2f5bb51b4479e4ee52afc698780564`

```dockerfile
```

-	Layers:
	-	`sha256:9aefa9a60b46e4270f92460c1feaea3f10b62c5b418aaa943e47b62057a948db`  
		Last Modified: Wed, 19 Mar 2025 22:59:05 GMT  
		Size: 2.7 MB (2715182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f283b31ecc1f090cbc4bf527ad66fcd3e242b7fbee715b017b5448fa2bb410e`  
		Last Modified: Wed, 19 Mar 2025 22:59:05 GMT  
		Size: 8.0 KB (8027 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:bd36528541e42a06a015f34c8e5a48169155a8a8726aeef93243100a4a8df1a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47160988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994c64b52c8ce259ed704c9031e25ef0394aa79895daa6d7a6795696ce562df6`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 22:49:59 GMT
ENV LANG=C.UTF-8
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3687c9079028ac9bf763326f4be55b4e440b37b5baf0c4529715d811c7ec1718`  
		Last Modified: Mon, 17 Mar 2025 22:19:22 GMT  
		Size: 25.5 MB (25535344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9ca95477eddfd090309fedee1cacc9293427d5e3660b566a235e06d02971c4`  
		Last Modified: Tue, 18 Mar 2025 00:23:10 GMT  
		Size: 837.0 KB (836960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d609c7e59d1d0e8d56e1fc2a3c12182e9ccbb34adfa3a054fee2d6e6432fdd`  
		Last Modified: Tue, 18 Mar 2025 02:08:14 GMT  
		Size: 14.6 MB (14583701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98586f4bea356b5add6292f462e05decefa2c7849da52d4cc70ddc77743ee247`  
		Last Modified: Tue, 18 Mar 2025 02:08:13 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcd61261cb9376efb00a38787bed305cbf9988b319bd7cfa13e256f6eefbdbd`  
		Last Modified: Wed, 19 Mar 2025 23:33:01 GMT  
		Size: 6.2 MB (6204734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:f6f715cc300074dcd6e1f8b816608b92727cba18599c0c1f1223fee47cce6dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2725529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:279745f168a42cee98e7710c38ade23cbd5541f214434098191fa3b05372e814`

```dockerfile
```

-	Layers:
	-	`sha256:f72f0d4292c5ac9abeb408b62f140ef2dca2cdb41bb7c85d05e60c7a29016c54`  
		Last Modified: Wed, 19 Mar 2025 23:33:00 GMT  
		Size: 2.7 MB (2717427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c5c53e6816b12f2fe1b2d6dda75770ef57590ccf69308791d1f6956dfa31615`  
		Last Modified: Wed, 19 Mar 2025 23:33:00 GMT  
		Size: 8.1 KB (8102 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:58a3476843b83d1cccf0d2ca9ccbea13d51664a435ccbb5919e4fe08dbea4d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51256263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:649da75de489c4a8b42023ac8056ec2884b1f676bf79f84936a103b7edb92865`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 22:49:59 GMT
ENV LANG=C.UTF-8
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae10c5f584ce1b218d2a6a1b0821e6ff0869f199833d1a1bb6b3108bb531994`  
		Last Modified: Mon, 17 Mar 2025 23:36:23 GMT  
		Size: 859.1 KB (859144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b1f365b20d1b5e1e5c5f3262d421b557dc4e30b95b575e59a6eb9e6e29c179`  
		Last Modified: Tue, 18 Mar 2025 02:05:48 GMT  
		Size: 15.4 MB (15446366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0052a6af23fd30a94e7fd3451bcbbc60332c371412e40bc81c4c927ebec17cb`  
		Last Modified: Tue, 18 Mar 2025 02:05:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c298f8d7ea1d9f3be9219c0ad01ceb39d19a1ddfff59c9ac8fdbd988bd5825`  
		Last Modified: Wed, 19 Mar 2025 23:19:34 GMT  
		Size: 6.2 MB (6204580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:8e0ce206da0de62e4b3c414de64e82cbb19bbd1b4090db5b10f05a7130cf4543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2723572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f1e83bec6e3e2651fac53401d8c4c83193ca3743c3eac794c5d350460d2b2a`

```dockerfile
```

-	Layers:
	-	`sha256:fe8a7cd2cfcf11113e119089065d4ac0dbaf56bc7058990af2f6518febf61e6c`  
		Last Modified: Wed, 19 Mar 2025 23:19:33 GMT  
		Size: 2.7 MB (2715441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07d0b9aa96808b2cad8cdaf9c89ec9db89e5ed68ab0c2838302f581d71c7c212`  
		Last Modified: Wed, 19 Mar 2025 23:19:33 GMT  
		Size: 8.1 KB (8131 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:96aa7264ff8b09180942585653f27844e1623f29c7e43d27c1fa9caa90ebe715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53775797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800a2e113137e49280d99b7d652dac56cb5394c306c81517c67cb3622e9d1a7b`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 22:49:59 GMT
ENV LANG=C.UTF-8
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e83ba34877ecae8e583197e97ef35a452a1d1b81c406023bf40d3c79d5ba9025`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 31.2 MB (31180337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9677d5561f3cff9c7c23703eb2a42b531e589a145dffc509d04686c2b9038f`  
		Last Modified: Mon, 17 Mar 2025 23:46:03 GMT  
		Size: 884.1 KB (884063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57cb738d0e562dd249cdd04d71746f30a3d83d5843b3fed9fc0dfa949f5a6026`  
		Last Modified: Mon, 17 Mar 2025 23:46:04 GMT  
		Size: 15.5 MB (15506640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64027a54dcc13318a5112253ae5b802cc6a1094ae6da16d14ba223f059b60817`  
		Last Modified: Mon, 17 Mar 2025 23:46:03 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e07bf62ff6ea400a7cf000cb81ce27b431c296c6a76d95fe03004c10f7741f`  
		Last Modified: Wed, 19 Mar 2025 22:58:54 GMT  
		Size: 6.2 MB (6204508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:b7758982b4ba811823f2872818c8524305ee364dad67a0e96fd84cece800a7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3662fcfd82a5a13604c445c105cddbd053308f217eea6c6b164c43fe1fd6f8a`

```dockerfile
```

-	Layers:
	-	`sha256:ca5002aabccd13b1e4ececfb3d71a2026ce26830f4bb8798edd69493f01e8831`  
		Last Modified: Wed, 19 Mar 2025 22:58:54 GMT  
		Size: 2.7 MB (2712294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c97abb78eb86b6a88c401acc3883bfd000b9766d233655c773872886f07c269`  
		Last Modified: Wed, 19 Mar 2025 22:58:53 GMT  
		Size: 8.0 KB (7995 bytes)  
		MIME: application/vnd.in-toto+json
