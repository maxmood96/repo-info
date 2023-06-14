## `hylang:0-python3.8-buster`

```console
$ docker pull hylang@sha256:79d6d126d483e60b92a71b02798a60b491228dafb129a3d24ebdc51823e0e765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:0-python3.8-buster` - linux; amd64

```console
$ docker pull hylang@sha256:cbe44910d46eefd59b3c2f346e8e7cafadc21790c8a4768933b7cf6dec140bb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49694028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:360b6ad8abf714959a4752c813d714c31f29a7482b885917059451f0e9cd0bd4`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:32 GMT
ADD file:2818e508d01da2188fb234b38fb19aa1ea9eeeae92d361ecdf49318d949f51a9 in / 
# Mon, 12 Jun 2023 23:21:32 GMT
CMD ["bash"]
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Jun 2023 15:50:21 GMT
ENV LANG=C.UTF-8
# Tue, 06 Jun 2023 15:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jun 2023 15:50:21 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PYTHON_VERSION=3.8.17
# Tue, 06 Jun 2023 15:50:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 06 Jun 2023 15:50:21 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/0d8570dc44796f4369b652222cf176b3db6ac70e/public/get-pip.py
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PYTHON_GET_PIP_SHA256=96461deced5c2a487ddc65207ec5a9cffeca0d34e7af7ea1afc470ff0d746207
# Tue, 06 Jun 2023 15:50:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 06 Jun 2023 15:50:21 GMT
CMD ["python3"]
# Tue, 13 Jun 2023 23:06:32 GMT
ENV HY_VERSION=0.26.0
# Tue, 13 Jun 2023 23:06:32 GMT
ENV HYRULE_VERSION=0.3.0
# Tue, 13 Jun 2023 23:06:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 13 Jun 2023 23:06:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8b91b88d557765cd8c6802668755a3f6dc4337b6ce15a17e4857139e5fc964f3`  
		Last Modified: Mon, 12 Jun 2023 23:27:09 GMT  
		Size: 27.1 MB (27138450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824416e234237961c9c5d4f41dfe5b295a3c35a671ee52889bfb08d8e257ec4c`  
		Last Modified: Tue, 13 Jun 2023 16:46:32 GMT  
		Size: 2.8 MB (2781342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f777578c172d018077d3dc22d6654911fff60066097943fe8c4697ecf8aac35`  
		Last Modified: Tue, 13 Jun 2023 16:49:56 GMT  
		Size: 12.9 MB (12889395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbfea27109a8b1136059a7973ccb8243889faf162ebc173a05909dcb0bec03c9`  
		Last Modified: Tue, 13 Jun 2023 16:49:54 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dfcf5deffff3c5d540a8e0d9a18656a4c03637a8b4f4eec1f4a147799c901`  
		Last Modified: Tue, 13 Jun 2023 16:49:55 GMT  
		Size: 3.1 MB (3138389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d21ccf4f3920c05772d6308f36a10af5b6a53c8bcab159c259cf108249aa0d2`  
		Last Modified: Tue, 13 Jun 2023 23:14:03 GMT  
		Size: 3.7 MB (3746208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.8-buster` - linux; arm variant v7

```console
$ docker pull hylang@sha256:3772d8dbc28f68b9d82b4a1c1e9df149324ce38c5f8987de1d1f728c830d1d32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44245042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4589dd287af29e400a13c8dde1fac7e3cd9fd368ca6162dfceb2f7f77cf7af60`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 12 Jun 2023 23:59:19 GMT
ADD file:7b4adc9bf459eb426ed799beabf07a67596899becc5750ea0a430d44d50fb565 in / 
# Mon, 12 Jun 2023 23:59:19 GMT
CMD ["bash"]
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Jun 2023 15:50:21 GMT
ENV LANG=C.UTF-8
# Tue, 06 Jun 2023 15:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jun 2023 15:50:21 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PYTHON_VERSION=3.8.17
# Tue, 06 Jun 2023 15:50:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 06 Jun 2023 15:50:21 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/0d8570dc44796f4369b652222cf176b3db6ac70e/public/get-pip.py
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PYTHON_GET_PIP_SHA256=96461deced5c2a487ddc65207ec5a9cffeca0d34e7af7ea1afc470ff0d746207
# Tue, 06 Jun 2023 15:50:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 06 Jun 2023 15:50:21 GMT
CMD ["python3"]
# Wed, 14 Jun 2023 00:55:02 GMT
ENV HY_VERSION=0.26.0
# Wed, 14 Jun 2023 00:55:02 GMT
ENV HYRULE_VERSION=0.3.0
# Wed, 14 Jun 2023 00:55:18 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 14 Jun 2023 00:55:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:85d92d6815dd0f72c5fb29f89ebf92afb1452a1f015d2e2692e81f89659fb1f5`  
		Last Modified: Tue, 13 Jun 2023 00:05:05 GMT  
		Size: 22.7 MB (22747263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c89d253fe9ee10f39aea82167be0856e7594471be3341dd830d331c93e86af3`  
		Last Modified: Tue, 13 Jun 2023 08:57:59 GMT  
		Size: 2.4 MB (2369214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4347dfde74a9ec9f92f87d50ce70bc016f581f2cc309031818308d3bb1306d11`  
		Last Modified: Tue, 13 Jun 2023 09:01:35 GMT  
		Size: 12.2 MB (12244504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c4a62e6b3f4b713599effce0099f51eb2f2939ae399d246c379f95f4e4a334`  
		Last Modified: Tue, 13 Jun 2023 09:01:33 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2441833c4c829ddcad003aed473b80f8d96349455293c4892bda630861dfbb`  
		Last Modified: Tue, 13 Jun 2023 09:01:34 GMT  
		Size: 3.1 MB (3137708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cfee0151cdf87211783b2fd53186c624ceeeb69cad450cea71bff009bb2ff3`  
		Last Modified: Wed, 14 Jun 2023 00:59:50 GMT  
		Size: 3.7 MB (3746109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.8-buster` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:ce8ccb19919ac3a2b6d9a68153f4af566cc3049008826a2ff30d4f859567498f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48428473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6e2c88e12e6f870bcb359f8dd0aadb6f47c36740b33a0764b57e24ae5e49ae`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:52 GMT
ADD file:d4a87f28032264e15d38bdd7efb6ffca8deadeb5388758f243e4866b360324c2 in / 
# Mon, 12 Jun 2023 23:40:52 GMT
CMD ["bash"]
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Jun 2023 15:50:21 GMT
ENV LANG=C.UTF-8
# Tue, 06 Jun 2023 15:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jun 2023 15:50:21 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PYTHON_VERSION=3.8.17
# Tue, 06 Jun 2023 15:50:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 06 Jun 2023 15:50:21 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/0d8570dc44796f4369b652222cf176b3db6ac70e/public/get-pip.py
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PYTHON_GET_PIP_SHA256=96461deced5c2a487ddc65207ec5a9cffeca0d34e7af7ea1afc470ff0d746207
# Tue, 06 Jun 2023 15:50:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 06 Jun 2023 15:50:21 GMT
CMD ["python3"]
# Tue, 13 Jun 2023 21:30:44 GMT
ENV HY_VERSION=0.26.0
# Tue, 13 Jun 2023 21:30:44 GMT
ENV HYRULE_VERSION=0.3.0
# Tue, 13 Jun 2023 21:30:57 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 13 Jun 2023 21:30:57 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d191be7a3c9fa95847a482db8211b6f85b45096c7817fdad4d7661ee7ff1a421`  
		Last Modified: Mon, 12 Jun 2023 23:45:21 GMT  
		Size: 25.9 MB (25921353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aea17807c4c653827ca820a0526d96552bda685bf29293e8be90d1b05662f6`  
		Last Modified: Tue, 13 Jun 2023 12:51:45 GMT  
		Size: 2.6 MB (2647113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe349e029970270c77c6cc4e8c8159d6390de76a4c30666e585e9ac57e54212`  
		Last Modified: Tue, 13 Jun 2023 12:55:07 GMT  
		Size: 13.0 MB (12975558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7399277d91f4520aebebe70097c48af726818282fbbc79c1fb34b53f088eb090`  
		Last Modified: Tue, 13 Jun 2023 12:55:05 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f10c4cf03d43a7afd688184e68c55cc3adc2049e78dffcc419a28f8ee8ac68`  
		Last Modified: Tue, 13 Jun 2023 12:55:06 GMT  
		Size: 3.1 MB (3138104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966a4764ae1698323a7bd3d54e773143cdb4c7ea995f1e8340637abebacc178b`  
		Last Modified: Tue, 13 Jun 2023 21:37:23 GMT  
		Size: 3.7 MB (3746102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.8-buster` - linux; 386

```console
$ docker pull hylang@sha256:e57cc51a77d094c6a70a4f5de275d6c4d232c6ccfafb90f82288d57933a9c6da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50475300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251a69dc92cc225f2dce3c41044fb03dc8e3093478ad3ceb6596d37335c8f5cf`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:35 GMT
ADD file:89de6b7378fdf61514133b7bd1ed23bb24397ce045566a30fee2a1347bf6587f in / 
# Mon, 12 Jun 2023 23:40:36 GMT
CMD ["bash"]
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Jun 2023 15:50:21 GMT
ENV LANG=C.UTF-8
# Tue, 06 Jun 2023 15:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jun 2023 15:50:21 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PYTHON_VERSION=3.8.17
# Tue, 06 Jun 2023 15:50:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 06 Jun 2023 15:50:21 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/0d8570dc44796f4369b652222cf176b3db6ac70e/public/get-pip.py
# Tue, 06 Jun 2023 15:50:21 GMT
ENV PYTHON_GET_PIP_SHA256=96461deced5c2a487ddc65207ec5a9cffeca0d34e7af7ea1afc470ff0d746207
# Tue, 06 Jun 2023 15:50:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 06 Jun 2023 15:50:21 GMT
CMD ["python3"]
# Wed, 14 Jun 2023 00:57:00 GMT
ENV HY_VERSION=0.26.0
# Wed, 14 Jun 2023 00:57:00 GMT
ENV HYRULE_VERSION=0.3.0
# Wed, 14 Jun 2023 00:57:19 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 14 Jun 2023 00:57:19 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e3832d1e9e7d28b937b10dcb945a700a76b4e3e7cde251e8eff22782e1fa2a55`  
		Last Modified: Mon, 12 Jun 2023 23:47:50 GMT  
		Size: 27.8 MB (27797003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdb1fae98f4389667300e5bedf9ad5de18e07af4d37e9454e407723adb8d3ff`  
		Last Modified: Tue, 13 Jun 2023 18:32:50 GMT  
		Size: 2.8 MB (2788738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0cb0c66dd2cac15d3052edb7bcc9049497f280d321f5ee0c521133d3326191`  
		Last Modified: Tue, 13 Jun 2023 18:36:31 GMT  
		Size: 13.0 MB (13004977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d46a3eb8e8b35d639d1356fab24ed309b6aa537f8a54b9155a6f96095e1bfa1`  
		Last Modified: Tue, 13 Jun 2023 18:36:28 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23e69e331abc0b42b1f2c9fbc3889f805a1290dc8213e3b1fdbd01a3c95bf99`  
		Last Modified: Tue, 13 Jun 2023 18:36:30 GMT  
		Size: 3.1 MB (3138101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debe197510c896cfdf9116de75ff7b39f8f4d1b9aaabccaba3cf0d3ce50cd1fb`  
		Last Modified: Wed, 14 Jun 2023 01:04:55 GMT  
		Size: 3.7 MB (3746238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
