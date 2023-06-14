## `hylang:python3.10-buster`

```console
$ docker pull hylang@sha256:1c21e718f9ec5fb04f5b5c4064d294ff1c7f11ccbffa7da964c771811e29f04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:python3.10-buster` - linux; amd64

```console
$ docker pull hylang@sha256:9ab5be450363f43b8b04b8ee76f0cfe00646f0d33ff0ac5c7da5026efe4c48e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48957043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b71619edb31a40de8c44b5d27b5aea59e02fdad27cabf61ce4ba831f74af44`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:32 GMT
ADD file:2818e508d01da2188fb234b38fb19aa1ea9eeeae92d361ecdf49318d949f51a9 in / 
# Mon, 12 Jun 2023 23:21:32 GMT
CMD ["bash"]
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jun 2023 03:49:12 GMT
ENV LANG=C.UTF-8
# Wed, 07 Jun 2023 03:49:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jun 2023 03:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PYTHON_VERSION=3.10.12
# Wed, 07 Jun 2023 03:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 07 Jun 2023 03:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/0d8570dc44796f4369b652222cf176b3db6ac70e/public/get-pip.py
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=96461deced5c2a487ddc65207ec5a9cffeca0d34e7af7ea1afc470ff0d746207
# Wed, 07 Jun 2023 03:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Jun 2023 03:49:12 GMT
CMD ["python3"]
# Tue, 13 Jun 2023 23:05:12 GMT
ENV HY_VERSION=0.26.0
# Tue, 13 Jun 2023 23:05:12 GMT
ENV HYRULE_VERSION=0.3.0
# Tue, 13 Jun 2023 23:05:24 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 13 Jun 2023 23:05:25 GMT
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
	-	`sha256:6903bcecb9721c4ee87e4188b263a0a392a16b2e2813c7a0ed0f9c4416194734`  
		Last Modified: Tue, 13 Jun 2023 16:48:25 GMT  
		Size: 11.5 MB (11501376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2697057e25fe078e5f17bdb522b6a913fc3ce2a041d34d2e4771e0f3ddd3c3f`  
		Last Modified: Tue, 13 Jun 2023 16:48:23 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7d39ff15355e0249529c91607c3e93f107c500b603a0ad75e90c85e4cf43b6`  
		Last Modified: Tue, 13 Jun 2023 16:48:24 GMT  
		Size: 3.4 MB (3370865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fac5f05e15b02b9a6896bd2b37adfeaafb3860deb734a3fe7ba5bdf3d6596c6`  
		Last Modified: Tue, 13 Jun 2023 23:12:55 GMT  
		Size: 4.2 MB (4164768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-buster` - linux; arm variant v7

```console
$ docker pull hylang@sha256:053d2e9a4039b0f734604f626b7077e86fce71cb8f65efaaed42ee72de0a9767
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43486475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980d5386da309fe22891fc8363eed2ecbac40d3f78d39228d0d8274a61a0aa24`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 12 Jun 2023 23:59:19 GMT
ADD file:7b4adc9bf459eb426ed799beabf07a67596899becc5750ea0a430d44d50fb565 in / 
# Mon, 12 Jun 2023 23:59:19 GMT
CMD ["bash"]
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jun 2023 03:49:12 GMT
ENV LANG=C.UTF-8
# Wed, 07 Jun 2023 03:49:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jun 2023 03:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PYTHON_VERSION=3.10.12
# Wed, 07 Jun 2023 03:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 07 Jun 2023 03:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/0d8570dc44796f4369b652222cf176b3db6ac70e/public/get-pip.py
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=96461deced5c2a487ddc65207ec5a9cffeca0d34e7af7ea1afc470ff0d746207
# Wed, 07 Jun 2023 03:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Jun 2023 03:49:12 GMT
CMD ["python3"]
# Wed, 14 Jun 2023 00:53:49 GMT
ENV HY_VERSION=0.26.0
# Wed, 14 Jun 2023 00:53:49 GMT
ENV HYRULE_VERSION=0.3.0
# Wed, 14 Jun 2023 00:54:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 14 Jun 2023 00:54:02 GMT
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
	-	`sha256:ce084b2545cea873005b5089884a44ef43d4df0595cae775531c889342a797b6`  
		Last Modified: Tue, 13 Jun 2023 08:59:56 GMT  
		Size: 10.8 MB (10834588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5990c3363db6f0074a7d0878c427031d2cc197bf6d384c8b924ac2a11b064e5c`  
		Last Modified: Tue, 13 Jun 2023 08:59:54 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782891521f79c2b1172db553bf7afa71062829569d1fd77c0bb04d0da7484327`  
		Last Modified: Tue, 13 Jun 2023 08:59:55 GMT  
		Size: 3.4 MB (3370236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf46ee4bf5f9566a94f95ebe78463fa520d5523c81feabb1b1c0c130d1f287f9`  
		Last Modified: Wed, 14 Jun 2023 00:58:44 GMT  
		Size: 4.2 MB (4164931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-buster` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:673b6766618dc9a5def8055e048aa67002cce462e06589f6156d940f12561170
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47694907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e22a5aca18594b9e1af50811d7feddfe00346490fe4b98c590d54cd267d2f9a`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:52 GMT
ADD file:d4a87f28032264e15d38bdd7efb6ffca8deadeb5388758f243e4866b360324c2 in / 
# Mon, 12 Jun 2023 23:40:52 GMT
CMD ["bash"]
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jun 2023 03:49:12 GMT
ENV LANG=C.UTF-8
# Wed, 07 Jun 2023 03:49:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jun 2023 03:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PYTHON_VERSION=3.10.12
# Wed, 07 Jun 2023 03:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 07 Jun 2023 03:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/0d8570dc44796f4369b652222cf176b3db6ac70e/public/get-pip.py
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=96461deced5c2a487ddc65207ec5a9cffeca0d34e7af7ea1afc470ff0d746207
# Wed, 07 Jun 2023 03:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Jun 2023 03:49:12 GMT
CMD ["python3"]
# Tue, 13 Jun 2023 21:29:42 GMT
ENV HY_VERSION=0.26.0
# Tue, 13 Jun 2023 21:29:42 GMT
ENV HYRULE_VERSION=0.3.0
# Tue, 13 Jun 2023 21:29:53 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 13 Jun 2023 21:29:53 GMT
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
	-	`sha256:0fecbe24af58d3c2efe15b25e254d540af1e144362e497bfca406df71d565f2c`  
		Last Modified: Tue, 13 Jun 2023 12:53:39 GMT  
		Size: 11.6 MB (11590822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd1afb703b36466cb23ef0e488320febbb3b79ea359c76e9ee2abdd431dbfaa`  
		Last Modified: Tue, 13 Jun 2023 12:53:37 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07f336a6b5291a3294d26bee39f7634877e06da801007e8fa001e48587e26ac`  
		Last Modified: Tue, 13 Jun 2023 12:53:38 GMT  
		Size: 3.4 MB (3370555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f212c6fcf261adf80edc1ed562f31244ad6364abc6fba74178fa52c3ac0afb1`  
		Last Modified: Tue, 13 Jun 2023 21:36:25 GMT  
		Size: 4.2 MB (4164820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-buster` - linux; 386

```console
$ docker pull hylang@sha256:9325aafcfa4b18a19cdfe4483680ed0fd0b57a7722645744104c7aed88c78f20
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49743255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1814480e718a4029ec863834ac87ed7becb29d50d20e1077c73a902236ac8a29`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:35 GMT
ADD file:89de6b7378fdf61514133b7bd1ed23bb24397ce045566a30fee2a1347bf6587f in / 
# Mon, 12 Jun 2023 23:40:36 GMT
CMD ["bash"]
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jun 2023 03:49:12 GMT
ENV LANG=C.UTF-8
# Wed, 07 Jun 2023 03:49:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jun 2023 03:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PYTHON_VERSION=3.10.12
# Wed, 07 Jun 2023 03:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 07 Jun 2023 03:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/0d8570dc44796f4369b652222cf176b3db6ac70e/public/get-pip.py
# Wed, 07 Jun 2023 03:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=96461deced5c2a487ddc65207ec5a9cffeca0d34e7af7ea1afc470ff0d746207
# Wed, 07 Jun 2023 03:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 07 Jun 2023 03:49:12 GMT
CMD ["python3"]
# Wed, 14 Jun 2023 00:55:29 GMT
ENV HY_VERSION=0.26.0
# Wed, 14 Jun 2023 00:55:29 GMT
ENV HYRULE_VERSION=0.3.0
# Wed, 14 Jun 2023 00:55:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 14 Jun 2023 00:55:44 GMT
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
	-	`sha256:ff62688675130e69f2ad1f24e66ac69563a642b08a8218ebb1bdb650ca3cf954`  
		Last Modified: Tue, 13 Jun 2023 18:34:53 GMT  
		Size: 11.6 MB (11622008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f2280a4f8145f140ef3eb6bb84996ad6193e76169891366cf5dc1f3e824991`  
		Last Modified: Tue, 13 Jun 2023 18:34:50 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18ca856a86a2a90d5750db34692a3a7eed1963e3f82e77977ca97b147188ebb`  
		Last Modified: Tue, 13 Jun 2023 18:34:52 GMT  
		Size: 3.4 MB (3370568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6f1e0b984aab5dca3c6998ca8145a7f547c20f54e58800e8280dfc467f15e4`  
		Last Modified: Wed, 14 Jun 2023 01:03:52 GMT  
		Size: 4.2 MB (4164695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
