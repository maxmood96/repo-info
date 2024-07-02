## `hylang:0-python3.8-bullseye`

```console
$ docker pull hylang@sha256:1da8e73543d647ec6d3ffcbe6f30ce025446cbab1a644783b5543dc94b272ebe
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

### `hylang:0-python3.8-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:44a7f3bd53633d176097819b0d531d628ec5d9dd779f31b5bf9a3c8f6a91d57c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50012536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da81363a2322a0ea9411409ef6e1874cf5c45cbedf35875240e7ffb4b1b820ba`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 21 Mar 2024 23:32:08 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.8.19
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc338303f9e7b9483d400b3a657df01ec9a61d93de550ffeb8f3f630a41deaab`  
		Last Modified: Tue, 02 Jul 2024 03:16:11 GMT  
		Size: 1.1 MB (1076292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434e86081504fc67b571ea94535e5946ef07a533db5aeaa1400bd24746340af3`  
		Last Modified: Tue, 02 Jul 2024 03:16:11 GMT  
		Size: 10.8 MB (10828649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fb8a4c8a22758e16e2acca0bb3d697f79e2cba845af46fac9b9712aaf0adb1`  
		Last Modified: Tue, 02 Jul 2024 03:16:11 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91bc1890dccc646c8200f965e053227602382d9c2ad604c663e927dd074d480`  
		Last Modified: Tue, 02 Jul 2024 03:16:11 GMT  
		Size: 2.9 MB (2928971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fa1ac77fd0ca042d5b3c595bf4e3752a8b6efaeb3d1bceb3ae8920a986aa17`  
		Last Modified: Tue, 02 Jul 2024 04:12:04 GMT  
		Size: 3.8 MB (3756108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:334a42e474e5da2ede8e7499a17c2b89249b507bb2e71e97ef4ea5d5d55fe872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ae79d954f47ec7e64e4f0659fa215b8fe2c145396664199e1523714710c3f9`

```dockerfile
```

-	Layers:
	-	`sha256:663705b249da7bc3c35170804e75ddb7793b85bb4af6359b5421e95f629c36dc`  
		Last Modified: Tue, 02 Jul 2024 04:12:04 GMT  
		Size: 2.7 MB (2688464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1977ed9c5528923d5bc39e74ac07029542d643b07934bd9ad205758ec9aa4e2e`  
		Last Modified: Tue, 02 Jul 2024 04:12:04 GMT  
		Size: 8.5 KB (8491 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.8-bullseye` - linux; arm variant v5

```console
$ docker pull hylang@sha256:5f64f38884ff01148bc545a45837248bf6ddec8714ef335f76a7985d9145fa3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47092184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164603a745b026e6c2996d636e4b20e16077c0dae64305211fc192db70663910`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 21 Mar 2024 23:32:08 GMT
ADD file:78cff0ed53bbaaa1d7680e733d50b8fc9042e257b78718ad822f9ac57a5d1dbb in / 
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.8.19
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f8a34d14f57d3fcf2d97b9fc0fb4439a2d00afe9411fdc788629eb4074186288`  
		Last Modified: Thu, 13 Jun 2024 00:52:21 GMT  
		Size: 28.9 MB (28936731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e505440c19d32bf663204471b090b7e317b8d940c84da46a0f0faf45a19a7330`  
		Last Modified: Thu, 27 Jun 2024 02:17:37 GMT  
		Size: 856.1 KB (856101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81cd83052bc523d859203871e0d08963b6b5f4ec3c880cdcea2e4f1d0fcc4e`  
		Last Modified: Thu, 27 Jun 2024 04:20:39 GMT  
		Size: 10.6 MB (10614311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f854af9a05aca6ee5c68bb8a2d3e6abe72291be81f880890d852de3d4a81e824`  
		Last Modified: Thu, 27 Jun 2024 04:20:38 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0514c9ecef9b001a6d8d2f2a7784119dcae67d9003ef2b676368a443c5cfbbd6`  
		Last Modified: Thu, 27 Jun 2024 04:20:39 GMT  
		Size: 2.9 MB (2928582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a9d5481d22a3275eba2e2e83640a0ffcd0d7dbdd2d409820631220f743984b`  
		Last Modified: Thu, 27 Jun 2024 04:53:11 GMT  
		Size: 3.8 MB (3756227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:f44c6a5e57fd61dc3630dd9fa3a41df8f904aa5e128af97308d264669cc35032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a41bd071922b337b741d3441a4f7fc31466c5211f38f120a1204ed436f9465c`

```dockerfile
```

-	Layers:
	-	`sha256:6c6bd7e8ee21c4e6d6083e221157c89e3992d3b411b9e1cab45a4c450f1b0b50`  
		Last Modified: Thu, 27 Jun 2024 04:53:11 GMT  
		Size: 2.7 MB (2688704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3beeefe25506a2dda4084969df9560687b9cb49c4e3de47e6245ba767a8d7cf8`  
		Last Modified: Thu, 27 Jun 2024 04:53:10 GMT  
		Size: 8.6 KB (8576 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.8-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:990494d335d51ab009a1e124638f1b5481fa5fbf634ae0f6577e7388db7afd34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44324127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a301054332b4df6d4c53a0102a6005712e128ec469591b907a0860ead9e1fc8d`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 21 Mar 2024 23:32:08 GMT
ADD file:b23992f77c1f22e7bf9048641d6da1d6ef922d78b4118f6d513e183ae6de7e34 in / 
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.8.19
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4873d96591a32d2d686ff6c86338fc9a63b9d60639482601b5402eb76e56a566`  
		Last Modified: Thu, 13 Jun 2024 01:02:22 GMT  
		Size: 26.6 MB (26594507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46b4de15aaddca66b3a24bc742dfa9cdb649ed0113659185052bfefc9fc109c`  
		Last Modified: Thu, 27 Jun 2024 03:03:21 GMT  
		Size: 837.4 KB (837396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a8aa78fd6a6bbc785fc47cba7b375abdef2f89e6ea27cb75cb79d3f1eb277f`  
		Last Modified: Thu, 27 Jun 2024 06:36:00 GMT  
		Size: 10.2 MB (10207191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11943e27c0e4113eef3a3b6f23d7d710ad76a3cc77a09780f5d862c86297903e`  
		Last Modified: Thu, 27 Jun 2024 06:35:59 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bf32b11b1a52f083db89a865f4af708bbcd80193d4f0873be6adc9d90ddd39`  
		Last Modified: Thu, 27 Jun 2024 06:36:00 GMT  
		Size: 2.9 MB (2928593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e567df39cf6e8a9b374f302453d42c1e380e2befb0f249f0ab4c1a4e7fe9cb`  
		Last Modified: Thu, 27 Jun 2024 07:07:37 GMT  
		Size: 3.8 MB (3756207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:109ebc082c6292a6817c8892d5516fdb5c80bcc43bfbaaff33ab03687f697f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d715bde1f2b79c4edde8b35725399bec04c513c649dcf476534dca19abd37ea`

```dockerfile
```

-	Layers:
	-	`sha256:210f0c728e9c0062c130802f2b9d37423caae44ba7d71a2f63d31a43ce24ef42`  
		Last Modified: Thu, 27 Jun 2024 07:07:37 GMT  
		Size: 2.7 MB (2690712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3388676e2b9292a7ca239a7225e34b9afe0a6d54a68178656f6809b1b8db968`  
		Last Modified: Thu, 27 Jun 2024 07:07:36 GMT  
		Size: 8.6 KB (8577 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.8-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:ef56b97a4078ec266655a60a23e11a670ccc1bba11fddc3979925f5df382bdc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48554073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd578a3692508c3a93a9c9fd7a7450da5fb9bf77748ffbe4dba9175eb158578`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 21 Mar 2024 23:32:08 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.8.19
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aee3611c294e8e92568be7d452b276ef9e65edbf2b4094aff64b5230e5263f5`  
		Last Modified: Thu, 27 Jun 2024 02:03:16 GMT  
		Size: 859.9 KB (859926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e2bc5db963f57692a8d011568ba530d1e3d44ed84b2638e1233e5f4be49a50`  
		Last Modified: Thu, 27 Jun 2024 04:48:18 GMT  
		Size: 10.9 MB (10921865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967b738acd0d400da9b10053c07e1ef87eed604ac61d5df795e704454b5d7bd0`  
		Last Modified: Thu, 27 Jun 2024 04:48:17 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2d3431273ebc8852b0ff818ff040ba37dba5e6b381a95427b5cdd3b0797d7b`  
		Last Modified: Thu, 27 Jun 2024 04:48:18 GMT  
		Size: 2.9 MB (2928917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18560a9f13badd332d4f1c26ebf3432f4273e5d958be585ea8907ee4ac38dc2`  
		Last Modified: Thu, 27 Jun 2024 06:07:21 GMT  
		Size: 3.8 MB (3756160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:8793fb33eda8aa8a48a2a665a7445c0a1093a359d538aba4895ba40166abaa02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f3047b0012d97849b7301c20fd7725aae0c127b2df08b6f4f68d62f663aa7d`

```dockerfile
```

-	Layers:
	-	`sha256:6482b42b794f3b16f2ab61e56850bc6f5ee6a836fcf4b471b9e9d23992089d81`  
		Last Modified: Thu, 27 Jun 2024 06:07:21 GMT  
		Size: 2.7 MB (2688722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5e826514a4b2ac58392240279b0494227cfba922aae86e4ea8cc3fa5c30fd25`  
		Last Modified: Thu, 27 Jun 2024 06:07:20 GMT  
		Size: 8.9 KB (8886 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.8-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:0238f8a9f4f47ed7b2269da96ff72a69e505769cd26df8a197dcfb32b56cd881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51165046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0dc7341464dae23b2c463434133e28e4751a20bd52a84dced7296271917d55`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 21 Mar 2024 23:32:08 GMT
ADD file:82c5579b81dad9a5dff7724fd8e74d225f919e378995a95c9a0a9c17ca55a77a in / 
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.8.19
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1084208571fd0651d255a493f4e05ba8b2b837b52064c5f2f317a2d979e679bc`  
		Last Modified: Tue, 02 Jul 2024 00:43:26 GMT  
		Size: 32.4 MB (32408452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fb53ba9367e82c559bc4f67f5a3e5a4b6fc1338be7526196224fdca02e37c9`  
		Last Modified: Tue, 02 Jul 2024 03:17:07 GMT  
		Size: 1.1 MB (1088852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98136f6765def3b299931ed401337ceb10bb1c751537633311969881f2830e00`  
		Last Modified: Tue, 02 Jul 2024 03:17:07 GMT  
		Size: 11.0 MB (10982990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1336bdb4055b7287d41465a10ff2c9bae93fd4bb8d0dff2ead3a70be47d04f2b`  
		Last Modified: Tue, 02 Jul 2024 03:17:07 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a9f7a731ff71a78a9b811c602e3f986dcef9f7ea46167189a4bdde852b2583`  
		Last Modified: Tue, 02 Jul 2024 03:17:07 GMT  
		Size: 2.9 MB (2928578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a32a3efb15f5d75c634646017f409800176b14aee08e6db6e44e097413158f`  
		Last Modified: Tue, 02 Jul 2024 04:12:09 GMT  
		Size: 3.8 MB (3755943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:86b5497dceadf442782fb58008886871137843ccdbf71d44cbcd8888057885f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f39b7f06cd5a7e1cb623c078c261352989934c8f532bfa4f3650c253f5c4c06`

```dockerfile
```

-	Layers:
	-	`sha256:32a78e0062b9eab8be16db57f6e149948b475dd89ab052310da6d1d766ed154f`  
		Last Modified: Tue, 02 Jul 2024 04:12:09 GMT  
		Size: 2.7 MB (2685570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d7cccfabfdb7ce976ce5a41f80bdb5509c55d913436990a6a38ce5cece494c`  
		Last Modified: Tue, 02 Jul 2024 04:12:09 GMT  
		Size: 8.5 KB (8458 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.8-bullseye` - linux; mips64le

```console
$ docker pull hylang@sha256:f4504af2143028f888554efe0bf845088aaa8b8fc8101f34b4158bb0f729384f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47986526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30efd53d3e07bdcf31f6a819d264249b34897f80c7a40994ca46102493b2d46`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 21 Mar 2024 23:32:08 GMT
ADD file:008c77755df91bc808f2edbc05df1da6419d984abea862dbf73f345500433eb9 in / 
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.8.19
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1b4876387959ae765d8f504e4352c8f85ce0ad5a78eee29be84300f85cfdf0a6`  
		Last Modified: Thu, 13 Jun 2024 01:23:19 GMT  
		Size: 29.7 MB (29651863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2495c50d3aebf6d3d43fd1777c6c7cf4bc46f4a43a70a1439ac38100fb3ae6`  
		Last Modified: Thu, 27 Jun 2024 00:57:44 GMT  
		Size: 846.2 KB (846218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4225599094446f3e284a782ea04f3a4c52676c7a073edcc1dab9759da5fe293d`  
		Last Modified: Thu, 27 Jun 2024 01:50:41 GMT  
		Size: 10.8 MB (10801776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ae435e5344356d7aedc74b1ca687dcb2daed6a1c08bbbd953c408ba91cf533`  
		Last Modified: Thu, 27 Jun 2024 01:50:40 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb23341aea842eb4d3da93c6fc740ff163ace5225a70d78a6553e6d1348c764`  
		Last Modified: Thu, 27 Jun 2024 01:50:40 GMT  
		Size: 2.9 MB (2929657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d693e9a3aa151f48df4fda0f225cebbfe9456083d6e9705ca1562d84cf4f76`  
		Last Modified: Thu, 27 Jun 2024 02:51:59 GMT  
		Size: 3.8 MB (3756780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:9b10d7cbd9f20f410b320c19f7980b66042ed14dbcb0c57fe4eb44d6dc3ef229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 KB (8346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414b898ffd250b19fc7840552521feddc810e0d7062469320df626f025a633de`

```dockerfile
```

-	Layers:
	-	`sha256:90a70014fe7e7c37816eac7ea0218f17b8ccb1ef058bde57eaa7dd4b906f100e`  
		Last Modified: Thu, 27 Jun 2024 02:51:58 GMT  
		Size: 8.3 KB (8346 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.8-bullseye` - linux; ppc64le

```console
$ docker pull hylang@sha256:d1adacf82b73917a583b17fb3835c5f54494123af4e04a65e872641659b3b6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54071030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000e71e46db9bf055a19434a516a1dbf193e0c23e2f52fefb7cdfb05e6cb7bb9`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 21 Mar 2024 23:32:08 GMT
ADD file:a150537fc528657f8fa98f90c4629e38f111c3c3ef60bd40c28205959899c1a3 in / 
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.8.19
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:64741f366161eb41a5c86810e08ceabb9f4e4b69ac16c725aa2d48f19486e1be`  
		Last Modified: Thu, 13 Jun 2024 01:22:19 GMT  
		Size: 35.3 MB (35311302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e719c077e3046e1b649b1b984dc04759c8b233d3a42d27bc96eb5df0da64b7`  
		Last Modified: Thu, 27 Jun 2024 02:53:39 GMT  
		Size: 890.9 KB (890889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ff8c1e10579fef915124864c32d674a73201f30a4844c4eaa3b94f8557fa14`  
		Last Modified: Thu, 27 Jun 2024 06:33:48 GMT  
		Size: 11.2 MB (11183010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f681478cdebe53cf25b5fb07fc99fae7e6c883d2d592c4c58fa0616a57b5eb9`  
		Last Modified: Thu, 27 Jun 2024 06:33:47 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2de7c16f586700551d40bb3d89c91e15174781a66d2f557fb0af63039273705`  
		Last Modified: Thu, 27 Jun 2024 06:33:48 GMT  
		Size: 2.9 MB (2929428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2854693205409e6df3dd033b52dac601043d8aa5cc649e8770e6924552aaf31e`  
		Last Modified: Thu, 27 Jun 2024 07:24:31 GMT  
		Size: 3.8 MB (3756168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:e4af43d9ba45478f15e147095a17816038391c1106e1feb739a06c5a87a603d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2701383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e63698721fb4d6a27aca1d38c667aae203f7d81fc0e7ace84859258b6b0e09b`

```dockerfile
```

-	Layers:
	-	`sha256:4119adf67eae929f7a1253cc26cec9620f90da73e4ff43f3a3c261d8dd24157d`  
		Last Modified: Thu, 27 Jun 2024 07:24:30 GMT  
		Size: 2.7 MB (2692839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:577beea7d4f3ac19bb58f8b9e81db4ce0a823adca176fa2f53a1c24688c43002`  
		Last Modified: Thu, 27 Jun 2024 07:24:30 GMT  
		Size: 8.5 KB (8544 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.8-bullseye` - linux; s390x

```console
$ docker pull hylang@sha256:0787b8989339ee38bb162c40f14eb08221da1c4459e5e3406220499b930b9c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48020720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787c0c02f8d4524f9c8422b960ee04ec9147d83e1990922cc3e1ddd0fd588274`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 21 Mar 2024 23:32:08 GMT
ADD file:dbc45f2c1dc4ae2fcf0e05b8c9401406afd0f7aa3623659e470bb7d0fb97f9ec in / 
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.8.19
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b9966e11fe1c4138e9aa4f0356568463c21e36009b72062413bb596e0e57738f`  
		Last Modified: Thu, 13 Jun 2024 00:48:17 GMT  
		Size: 29.7 MB (29673762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12769d34a44b8035157d8e4a0480b80c76f0ee30afbd65aa1fea0a293229df52`  
		Last Modified: Thu, 27 Jun 2024 01:52:59 GMT  
		Size: 872.3 KB (872284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e595eff28428d2d57f1e248ddc198c5d79e8947735fb2fb3aefa8d28f90d31`  
		Last Modified: Thu, 27 Jun 2024 04:35:53 GMT  
		Size: 10.8 MB (10789665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dcc1beee21d8a7f33d0eb31e8bd001209ae94ef9577b7e249eb23f1a768430`  
		Last Modified: Thu, 27 Jun 2024 04:35:53 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81565b7d8f15acab81eaf7537c408366ce301219afc5a629833c63cdfdb67d3d`  
		Last Modified: Thu, 27 Jun 2024 04:35:53 GMT  
		Size: 2.9 MB (2928716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac565c49558988277c174b4e259a54e9c90c9f2e135bd21db53604134af3472`  
		Last Modified: Thu, 27 Jun 2024 05:05:29 GMT  
		Size: 3.8 MB (3756061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:7b6c7d7157594dbd7a44d44d18e0d070ba8248920f42fd7cce8253af7bc2aae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e162b14552b00e59b7c62a87f690b30ae9c920caee66114d3e743a1395242c84`

```dockerfile
```

-	Layers:
	-	`sha256:26a279fa60939a4cfbf28eb647fe4609664fa5e18d9553e70c27d4846e721812`  
		Last Modified: Thu, 27 Jun 2024 05:05:29 GMT  
		Size: 2.7 MB (2688658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0272b0ee1884c5d24e8a798cacbd688c0a3ef6470b6fb7bc2fc7d3c012ad6e47`  
		Last Modified: Thu, 27 Jun 2024 05:05:28 GMT  
		Size: 8.5 KB (8501 bytes)  
		MIME: application/vnd.in-toto+json
