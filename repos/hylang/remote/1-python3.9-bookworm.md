## `hylang:1-python3.9-bookworm`

```console
$ docker pull hylang@sha256:e43f688cc37677f5c4917c4782528661fbf56e8b43ec4bcd5881a5a4dd992968
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
$ docker pull hylang@sha256:c097b6603228b44f5a43f8ac3983d5c84109dd406d9e9ccf3435efa227499e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df9f73aeb1a0c08d4f7fa39460ab8c8e1d4c347e85bcb39499d2b952f479cf4`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d691b80d5159dfbcf2c1daad72a24c0fb9a55b6d90d6a11dcd46384ff1afa64d`  
		Last Modified: Mon, 28 Apr 2025 22:08:08 GMT  
		Size: 3.5 MB (3511561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b1a677eccc72224f1c1f6beece7da2221414861259d64d106a62d9b1f704e0`  
		Last Modified: Mon, 28 Apr 2025 22:08:08 GMT  
		Size: 14.9 MB (14934958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95b45635cb4f373b9afdfb37bc513f1cc179ce6bd32904fb5570188eee2f29`  
		Last Modified: Mon, 28 Apr 2025 22:08:08 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ea230bd323ab6ba9cb1b9760b9195b97b9ff0c1c45300120d92319417419af`  
		Last Modified: Mon, 28 Apr 2025 22:22:04 GMT  
		Size: 3.7 MB (3669943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:e0dc7a0241beec0453a7c7b6079f331063995b56490778e95f9533705c911d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2475159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c40c75475f79cf67166ee440f6ce78fe238afbf2d297f1411ca4e5442101ab8`

```dockerfile
```

-	Layers:
	-	`sha256:8af7b5b5909cfa3be721aa25e672441bbca3a2b882610cf76f825d2fd415ec75`  
		Last Modified: Mon, 28 Apr 2025 22:22:03 GMT  
		Size: 2.5 MB (2465902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c48afde50be8730ba4eff20dbe027feeb4a6f730d03b491c67d02e21854fbf4`  
		Last Modified: Mon, 28 Apr 2025 22:22:03 GMT  
		Size: 9.3 KB (9257 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:093d07ec5bed06561ced682594a1e5ee81659ca3a13115338f122e71f97f3348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46874743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0134c559cb20b45861c6f4c6d3c9ddb4f4c3a78f166de23de00f6561dee5ebfb`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1745798400'
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
	-	`sha256:3bc532ff9d2a2a12c6cfc746359843257a240960865aea7ecb10c71e0b93ec78`  
		Last Modified: Mon, 28 Apr 2025 21:07:56 GMT  
		Size: 25.8 MB (25757836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd3f52acbe9abc4f7abed187506e721554093a556b5a4a20128eb901cf2806e`  
		Last Modified: Tue, 29 Apr 2025 02:34:30 GMT  
		Size: 3.1 MB (3082299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d163d05f2d157a29a752cd246dd1c1706b868655e9e8a638d0f9e1603457db80`  
		Last Modified: Tue, 29 Apr 2025 03:09:08 GMT  
		Size: 14.4 MB (14364325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f620984a865df722ea9f9c3aa28c3f896f8b117f70e87b9e81950d04de3d06`  
		Last Modified: Tue, 29 Apr 2025 03:09:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a4940de7853f12d0a1137c47d17330d270850f83135961e2653c99e80f4e29`  
		Last Modified: Tue, 29 Apr 2025 05:22:21 GMT  
		Size: 3.7 MB (3670034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:41c94a6a5bbadd514dc66777b77a8791bd9197c2fef360ae0c539b71590de75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2478811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5353627f78216eae540ed08fb745dba69e399cd15f9e995e39c70a334908f090`

```dockerfile
```

-	Layers:
	-	`sha256:754dcf5501fc29503492c7cda38aed8935e0235c449b5e4d3a06dd2f192ca111`  
		Last Modified: Tue, 29 Apr 2025 05:22:21 GMT  
		Size: 2.5 MB (2469446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85bb05a3da996005f7804a3d726b66446f8dc05362895708af8fb06d15ce8870`  
		Last Modified: Tue, 29 Apr 2025 05:22:21 GMT  
		Size: 9.4 KB (9365 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:bb053ecb079598d051a8aeaf0e04bdb9e586709f9f165d207f40857eee810a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44477715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38bbbb95f4aa6a1e9b427e0a52a53b25d31f6fc394e6e19231ec08361e214f9`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdeed5e302497b1968de1331044c42bd4d087b1b79f61050b621362a7a36250`  
		Last Modified: Tue, 08 Apr 2025 11:45:37 GMT  
		Size: 2.9 MB (2914846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6567b051cb800c21a399c87b1afa89bc35dfb89f85ce49bbb1800ac937a49d`  
		Last Modified: Wed, 09 Apr 2025 20:55:12 GMT  
		Size: 14.0 MB (13954616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dbc312204af762146c4c93a57be036e886dfb869c2dd755410305683da44d3`  
		Last Modified: Wed, 09 Apr 2025 20:55:11 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e724cc75fe4839084c6ad986e57ec6b262c44a847c5472bf07992a4d374e5c`  
		Last Modified: Wed, 09 Apr 2025 21:38:49 GMT  
		Size: 3.7 MB (3670136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:46d7baa0bde15ac86bf6d4fbba50f60b443cd95ddd5ad2d18073bfe418d31075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2477568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4d42fa19310204596b1d7818bb94d138ce816ade1708fbe47f3b2581f02ca1`

```dockerfile
```

-	Layers:
	-	`sha256:1b47e29fa7d353a828111fa8d4eed762d517ff738f32ee6752d477aadd9db8b1`  
		Last Modified: Wed, 09 Apr 2025 21:38:49 GMT  
		Size: 2.5 MB (2468203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42335de630a8db81687bc4e250a3393443b9fbf12de0ecf63fcc0a29a341aef3`  
		Last Modified: Wed, 09 Apr 2025 21:38:49 GMT  
		Size: 9.4 KB (9365 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:1c18ce7e5cf7cd5edb3caa814b6299d9633e86974e3ea98d957c41f3ff1c95ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49903925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e2b3b0fb747b5de06d30463dc6df166c14fe8c96d950a7e9159c291117a60f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d9a0ac6293889b2e134861072f9099a06d78ca983d7172d7bb8b236008c7c3`  
		Last Modified: Tue, 08 Apr 2025 09:25:55 GMT  
		Size: 3.3 MB (3332082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9e09c11dcc28ed1f853d17d5095a9ba250b731178a2d239b5abdbfb5c4788e`  
		Last Modified: Wed, 09 Apr 2025 23:11:28 GMT  
		Size: 14.8 MB (14835194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59024e03c371a36e3b8f43a806543c68509de3f7a7cccb45eb6d4176dcfed5ff`  
		Last Modified: Wed, 09 Apr 2025 23:11:27 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450e2c1fb5b87e554a1f6ea42a5394b883a1a9d7f1bb18297c613b799b1da8b3`  
		Last Modified: Thu, 10 Apr 2025 01:48:07 GMT  
		Size: 3.7 MB (3670079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:9da95cb737f99d976e010b9b7e8abf112622919862712048a4e4fe906c32fd0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2475632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d09b29578d393daabccc6a117b363c88a5e11b700c708e82c47b34933e50e4`

```dockerfile
```

-	Layers:
	-	`sha256:21fd8a80bfe937ae9e8059fb9a862446d35df72aa27da7dc5ecf2b9adf8a850b`  
		Last Modified: Thu, 10 Apr 2025 01:48:07 GMT  
		Size: 2.5 MB (2466223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb5a5ce09f07c4c99179e1718eda2c1501f1b7075e306a9b083a350714f74b53`  
		Last Modified: Thu, 10 Apr 2025 01:48:06 GMT  
		Size: 9.4 KB (9409 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:1d38f6b8d4199e3419c547402e132a9d123162914014926b2217cc784998c520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51572916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3f78d6a27ae54bdd41d0b7edd28f3791d28414612e71a60b016d3ddac9f064`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f5b12efe7fe8a2688131e57db81a7eb69d5e8bef7d9890993a2c132bd66e36`  
		Last Modified: Mon, 28 Apr 2025 22:02:44 GMT  
		Size: 3.5 MB (3509867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49456289f52ee315317c0eca4369296a867665bf04dbce52129dd83cb1df106e`  
		Last Modified: Mon, 28 Apr 2025 22:02:44 GMT  
		Size: 15.2 MB (15181972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7a8f94a2439c58c22782efa0ba042ad4d295dbcc2533bc91b49e9730d235f7`  
		Last Modified: Mon, 28 Apr 2025 22:02:43 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbf02757655a1a94ebf97476b31dbc59fdcec1f3405388940f48708dfa87a39`  
		Last Modified: Mon, 28 Apr 2025 22:21:34 GMT  
		Size: 3.7 MB (3669962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:dd72d4dbf540854df347c0c84a40cc27d30f362570fb1be0c5aaf1b537af5a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16169a36e02d665a4ecdaf4d81021349dcb9a9e7dde0773cca24bca06523158f`

```dockerfile
```

-	Layers:
	-	`sha256:874ae06972f2c2b4f3d24fb6efd50771b0a2593471d76211fd58863dc410fcae`  
		Last Modified: Mon, 28 Apr 2025 22:21:34 GMT  
		Size: 2.5 MB (2462982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b58aaf2bbf6a836d76b45370cc461e54d34a861013dd89de8db6808b8b2b21b9`  
		Last Modified: Mon, 28 Apr 2025 22:21:34 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bookworm` - linux; mips64le

```console
$ docker pull hylang@sha256:4d5b74493706d96b0276f9da59f8f0409e5e103569ed4ae7a980ebe51a6e28f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49710325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53528d5e894db8be82b81a475c0afca9e80c9d3fc75610b3ace7c46d4952c92d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:c5170849255c666bce01dd02c1afbe442b1ecb682c342680d91dcd7cd477b57d`  
		Last Modified: Tue, 08 Apr 2025 00:23:28 GMT  
		Size: 28.5 MB (28513953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5a5e44b8693293bdeaf4b10f07420287a2c60ed16dcb91ef223e415958a0eb`  
		Last Modified: Wed, 09 Apr 2025 19:05:34 GMT  
		Size: 2.9 MB (2907085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2611a5dd82611c73df6256af0eaee93e5140b8670a402fd7c9eb48879d0063`  
		Last Modified: Wed, 09 Apr 2025 19:05:34 GMT  
		Size: 14.6 MB (14618541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4183414bd87a1c8567fc3130977013a8a7e2c48aefd231b4de1d6003be17b8de`  
		Last Modified: Wed, 09 Apr 2025 19:05:32 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63aed0c75cc84ea1802ab61b3133445c8071fd757905f6b9dcd628570a08e267`  
		Last Modified: Wed, 09 Apr 2025 19:36:55 GMT  
		Size: 3.7 MB (3670495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:396c8078172c6b3e5e34ee8bae06f19838c02e32da3c258994f0117018c59860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56530e0d6325ca0ee2064051bd8c156b7ec7bb279e728954bde0849eedb490c6`

```dockerfile
```

-	Layers:
	-	`sha256:a7d63918626afac9325a0f1ed29d8bc38ae8e31c7a45d2dadb5d4a0f3d98b50b`  
		Last Modified: Wed, 09 Apr 2025 19:36:54 GMT  
		Size: 9.1 KB (9144 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:2cf851dfec41bcb9bde0f28c1d6921ad4b7874bcf81b066e616a5c3920af0c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (54991549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2c3d38b6a6219bfcc37fed699b3f8e60b1541fdfeafcc7da7b223e1b59d08d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14081b1afe897cce9676c9df550a4ef4deae350ae7ce3f01cbaf00ca3d0fc44`  
		Last Modified: Tue, 29 Apr 2025 02:44:59 GMT  
		Size: 3.7 MB (3713706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8fc7d10d63a1e4e234b94efc2d065bb7a65998b15784a605627909dc9ecc91`  
		Last Modified: Tue, 29 Apr 2025 03:18:58 GMT  
		Size: 15.5 MB (15538917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9666187326fa45f8ea1d07124d2b51b9d221f766eef7d9605d126f1b863f2c4c`  
		Last Modified: Tue, 29 Apr 2025 03:18:57 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409429393503ebd3d3540bcc9a02d07d978235cd76b2e5d68dc5e8f74438b92c`  
		Last Modified: Tue, 29 Apr 2025 08:16:02 GMT  
		Size: 3.7 MB (3670234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:926df4ad4aa1ed662da7b16ca2c3b1c2975e37267263f7a6c40746c45071ed06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2479643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53905d822d7fe34c5f5be526dd3864b9368cb15ba68b010d261beb6fe6dbb5bb`

```dockerfile
```

-	Layers:
	-	`sha256:95dead935543d741ced40fb78903a04d990f6c384e8aa584d80a1d032af51df6`  
		Last Modified: Tue, 29 Apr 2025 08:16:01 GMT  
		Size: 2.5 MB (2470318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0b42c8eb3ce759727490eeefb2a88c7605a635b92679930390e111ceb418eaf`  
		Last Modified: Tue, 29 Apr 2025 08:16:01 GMT  
		Size: 9.3 KB (9325 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:b8bc0a29b2a28ee8d2f60e31f0e8537318aa3fdd091ecc8e13722d1ab61e5b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48448988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4820d7840578efedb5dcea13550e899d95388ef846b65413bb619f350b3d83fa`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4bd54a9f3382d42e097f7db7e6c47d5b56175964eb40e170669bc0efc3af66`  
		Last Modified: Tue, 29 Apr 2025 02:08:39 GMT  
		Size: 3.2 MB (3173138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef7d90cc7864d98bc5595b575c0fb1957b97e45474acf014932858a69facb24`  
		Last Modified: Tue, 29 Apr 2025 02:21:45 GMT  
		Size: 14.7 MB (14720791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a81ecbc9012e1b61c899baa7b81208b68b4bfb786a1428480634e136d61294`  
		Last Modified: Tue, 29 Apr 2025 02:21:44 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0619ec721ebbfaf155d35008c1d28a16b77a6a000b5b8c61d2499f3629b4d52`  
		Last Modified: Tue, 29 Apr 2025 05:58:39 GMT  
		Size: 3.7 MB (3669942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:cded4d094e56fa2617a311f98be1f3a820c4943dd96b40c3ea1f0e306654882d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2474867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295f14c579aa38e03619be9d81bc28f1621444af7a0a3d52cd98dd2a3733f7ae`

```dockerfile
```

-	Layers:
	-	`sha256:071c3f616778d4ca60aceb21776dca588613e06413fed1ab6990be49ed71620c`  
		Last Modified: Tue, 29 Apr 2025 05:58:39 GMT  
		Size: 2.5 MB (2465610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2edf756277cd5e7b5228ad8a0c69e4a7f9a73992f1a47d8b80cddd54f76ab588`  
		Last Modified: Tue, 29 Apr 2025 05:58:39 GMT  
		Size: 9.3 KB (9257 bytes)  
		MIME: application/vnd.in-toto+json
