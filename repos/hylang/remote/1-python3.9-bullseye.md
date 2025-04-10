## `hylang:1-python3.9-bullseye`

```console
$ docker pull hylang@sha256:f03ccede4c5d88e7713afc6cb7a78f6c15af46999aedc29be8fd287b6421b340
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

### `hylang:1-python3.9-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:6faf2914ceb5b3639c81edf3fd5111f2c24be900763ee9bfbece723dc6c4b437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49135846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4b1a3dea11fbf3282011b0551564c0f29ec678d37530e1f85affffd8c1355e`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 17:54:43 GMT
ENV LANG=C.UTF-8
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_VERSION=3.9.22
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_SHA256=8c136d199d3637a1fce98a16adc809c1d83c922d02d41f3614b34f8b6e7d38ec
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
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
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63677b18bed1cc0a972436c4b4e6fbe51237a68e8c189de066310bce759087b`  
		Last Modified: Wed, 09 Apr 2025 18:20:50 GMT  
		Size: 1.1 MB (1076265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06feb7a04f5093f2029fc28f2f6b87de205e71ae377884f07bd9cc85581cdff8`  
		Last Modified: Wed, 09 Apr 2025 18:20:50 GMT  
		Size: 14.1 MB (14132032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f5e289f1b27696efa5e812ccbb9e9ab23e7b61ee0d75aa639da4ea5e748f63`  
		Last Modified: Wed, 09 Apr 2025 18:20:49 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a798c492f56c45d13fa33240e0c6849f517aa20d65c979b3a9ab058f040247`  
		Last Modified: Wed, 09 Apr 2025 18:30:22 GMT  
		Size: 3.7 MB (3669880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:5a918aa5ca4760dddecceef22d30eb183b6309a14bd4a0d6d9972b3da91070fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2725094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef98a2ebab3a788a528cc80f6b7f287593d03f037f159d9560c4e93521e9a575`

```dockerfile
```

-	Layers:
	-	`sha256:37b3e1637d2f2b688db7e540b776eec57bdbb9cc9aac0cebdb6bd18f3619a236`  
		Last Modified: Wed, 09 Apr 2025 18:30:21 GMT  
		Size: 2.7 MB (2717078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3660cb0257e65cfe1983b4ba94b5ef0c3083f7c2fcc6881f4aba22f175fab46a`  
		Last Modified: Wed, 09 Apr 2025 18:30:21 GMT  
		Size: 8.0 KB (8016 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:63704c438c439b55dae7d030c6e69920c3ad89863ff21389fbac86a7cdadb106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43582369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a014a300583ea3594e7d98833ef3aaff50a51da2d5a12ae1ebfd6b71df4a3bbc`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 17:54:43 GMT
ENV LANG=C.UTF-8
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_VERSION=3.9.22
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_SHA256=8c136d199d3637a1fce98a16adc809c1d83c922d02d41f3614b34f8b6e7d38ec
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
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
	-	`sha256:bfc445187b87c4f640fe8b85c4ee3c251ce5e7023a5ff0acd053bde1f01e6aaf`  
		Last Modified: Tue, 08 Apr 2025 00:23:52 GMT  
		Size: 25.5 MB (25539135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ecdde7a00ceb13538875d85bc733018169f10be5fffad9b82129f97a9ea64f`  
		Last Modified: Tue, 08 Apr 2025 12:11:33 GMT  
		Size: 1.0 MB (1041642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf250496acba132305accfdae6900819579856f8bb9f73fb0104003856d7af0c`  
		Last Modified: Wed, 09 Apr 2025 21:11:47 GMT  
		Size: 13.3 MB (13331145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed486cdd4db39f66c4f7ab110457cb552455945556674d38c1f62cbbf15c82a`  
		Last Modified: Wed, 09 Apr 2025 21:11:46 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c008456356d6c135c385dcb4498f4a210f6785eb8bdbe1b5bdcfa4b746d32a59`  
		Last Modified: Wed, 09 Apr 2025 22:09:49 GMT  
		Size: 3.7 MB (3670197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:f3383098d80b975c14cc51a36a3c80c1e4b5da5f8d44b329836dd7d4de305e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2727416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391e6d729ab566bf0abddd88b84f959c23cc13b90fe71b6ada71149814ea153b`

```dockerfile
```

-	Layers:
	-	`sha256:4ff98b7a766175d3d39edbb9ccf0d74172abc0e3f2f4e1e65475fba8ff55ccce`  
		Last Modified: Wed, 09 Apr 2025 22:09:49 GMT  
		Size: 2.7 MB (2719323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d33bfa7039f7358434b906d0c647dcad24a6c5a26d1cf334314938acb3f1805`  
		Last Modified: Wed, 09 Apr 2025 22:09:48 GMT  
		Size: 8.1 KB (8093 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:423cc8ae4afceb6759a7b1b55b5b9ca22bb046e54310ea1f45f009144ad5ff84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47626948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f3c3b097dd55e3acd0ab5d82242f9d18025388bb9673bec4ca64b0b5fa42fd`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 17:54:43 GMT
ENV LANG=C.UTF-8
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_VERSION=3.9.22
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_SHA256=8c136d199d3637a1fce98a16adc809c1d83c922d02d41f3614b34f8b6e7d38ec
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
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
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab9c1400414b3d21e6f9400bd67f85d9cf73afd69f2800a10bbfdd6d0d83238`  
		Last Modified: Tue, 08 Apr 2025 09:39:42 GMT  
		Size: 1.1 MB (1064063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a020fc61d0a7a20b4ff4d6b08ac2d9400ef84ffdf369f710c71aa28c921a0de`  
		Last Modified: Wed, 09 Apr 2025 23:23:00 GMT  
		Size: 14.1 MB (14143011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b902ca806abf8765d739f1f50babaedaf69f2e1365774a212c681bf6e83ec408`  
		Last Modified: Wed, 09 Apr 2025 23:22:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c71d018889d9461c8b1cb265c6471119627b3de6e4bbac7ec484698b22a65a`  
		Last Modified: Thu, 10 Apr 2025 01:48:32 GMT  
		Size: 3.7 MB (3670126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:7e5ee2b3b984ce0723844c078da7d6e9ec722d396e37f98896a64798db63c091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2725458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde3ad885847aa376424338ce969fb159b61a5422eef9fb5ae4ff0e2b3986c1d`

```dockerfile
```

-	Layers:
	-	`sha256:1082289bc0862b9572f73a67d07792b8322fc16ce7cc576d57202475684612a2`  
		Last Modified: Thu, 10 Apr 2025 01:48:32 GMT  
		Size: 2.7 MB (2717337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b9142fa3b9f6009589c760d43618d7318a80bfdcc313fff425cc8a7e1b30792`  
		Last Modified: Thu, 10 Apr 2025 01:48:32 GMT  
		Size: 8.1 KB (8121 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:3143ccb43cfa4a3d699d427573d2b9da31336f695d57d711358407e4e9c595ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50185495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a172b3d382ee8a08af7dd4804f0618d555a58933d086e85e17e852b11017bcc`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 17:54:43 GMT
ENV LANG=C.UTF-8
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_VERSION=3.9.22
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_SHA256=8c136d199d3637a1fce98a16adc809c1d83c922d02d41f3614b34f8b6e7d38ec
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
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
	-	`sha256:c7f226a3ed9e3a783e859dc8479e50da2694130147ffb4885645e02664eedbec`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 31.2 MB (31184573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b704a074da2aed9f28d6131b20874b5e4bddb0fc7a9311a1b9bf9af4936148`  
		Last Modified: Wed, 09 Apr 2025 18:23:20 GMT  
		Size: 1.1 MB (1088768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fa6e4a8f1279a234bfe263275b1c49b315fe276714663689e044cf1fbc712a`  
		Last Modified: Wed, 09 Apr 2025 18:23:20 GMT  
		Size: 14.2 MB (14241821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad8847189b0b1af580b4e6aa56911d8db05b61b0e1b88366b1b6886a869ec2f`  
		Last Modified: Wed, 09 Apr 2025 18:23:20 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44d4cb2e189c4e4ea8444511f06efd8910e1e4c542f33f4db3ade020146f6d4`  
		Last Modified: Wed, 09 Apr 2025 18:30:27 GMT  
		Size: 3.7 MB (3670082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:fe20114ff38843249ac2dfbdc9dc1615beb187da4a387260f04139df45c1526b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55b2696745d9db00071853df3a44ee9125aa8d645fc9dc8d32beda60def55ac`

```dockerfile
```

-	Layers:
	-	`sha256:4600ab5e74b2424aabca5cf5a3133e1581aafb1bc7ce5e4e3f7924daa2fc5b74`  
		Last Modified: Wed, 09 Apr 2025 18:30:27 GMT  
		Size: 2.7 MB (2714190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03d37656e7c94ad5e6637ef7117385bcbc229f17388d8f5427c623ca25d1d69f`  
		Last Modified: Wed, 09 Apr 2025 18:30:27 GMT  
		Size: 8.0 KB (7985 bytes)  
		MIME: application/vnd.in-toto+json
