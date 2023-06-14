## `hylang:python3.9-buster`

```console
$ docker pull hylang@sha256:541f6bd8706c80503e0efd77146af3d669377c5acaf2c18dab77c2a429fbdebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:python3.9-buster` - linux; amd64

```console
$ docker pull hylang@sha256:b66ae9fb1bcdc20313d08c95884501a5143679989649f063596eac40ea6d05c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47739804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0d5837dd8a5abcde6d8c3bcf81acd1412db86916fd913ec16f1c31c051c7e6`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:32 GMT
ADD file:2818e508d01da2188fb234b38fb19aa1ea9eeeae92d361ecdf49318d949f51a9 in / 
# Mon, 12 Jun 2023 23:21:32 GMT
CMD ["bash"]
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Jun 2023 16:18:53 GMT
ENV LANG=C.UTF-8
# Tue, 06 Jun 2023 16:18:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jun 2023 16:18:53 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PYTHON_VERSION=3.9.17
# Tue, 06 Jun 2023 16:18:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 06 Jun 2023 16:18:53 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/0d8570dc44796f4369b652222cf176b3db6ac70e/public/get-pip.py
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PYTHON_GET_PIP_SHA256=96461deced5c2a487ddc65207ec5a9cffeca0d34e7af7ea1afc470ff0d746207
# Tue, 06 Jun 2023 16:18:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 06 Jun 2023 16:18:53 GMT
CMD ["python3"]
# Tue, 13 Jun 2023 23:05:50 GMT
ENV HY_VERSION=0.26.0
# Tue, 13 Jun 2023 23:05:50 GMT
ENV HYRULE_VERSION=0.3.0
# Tue, 13 Jun 2023 23:06:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 13 Jun 2023 23:06:04 GMT
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
	-	`sha256:8d53da26040835f622504d7762fad14d226ac414efeb5363f5febebc89ff224d`  
		Last Modified: Tue, 13 Jun 2023 16:49:11 GMT  
		Size: 11.0 MB (11042101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c8c79126f669beec1dcf6f34cd88094471745570c19c29b465dfa7db1fdabd`  
		Last Modified: Tue, 13 Jun 2023 16:49:09 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1c130fa3ec1777a82123374b4c500623959f903c1dd731ee4a83e1f1b38ff2`  
		Last Modified: Tue, 13 Jun 2023 16:49:10 GMT  
		Size: 3.1 MB (3136007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b421a3feee6128b0c44a885bcc4174f1a16aa69f5c5af7c5b51928d25d2b8a`  
		Last Modified: Tue, 13 Jun 2023 23:13:32 GMT  
		Size: 3.6 MB (3641661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-buster` - linux; arm variant v7

```console
$ docker pull hylang@sha256:83c18e777b795f30da9b58da864caf5f9f7a3299bf719afdb7dbcf1e04153a4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42256626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa158147ed729cb8450137f30c8ed134b50d1b57e5bc3997a679200cdcd731d4`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 12 Jun 2023 23:59:19 GMT
ADD file:7b4adc9bf459eb426ed799beabf07a67596899becc5750ea0a430d44d50fb565 in / 
# Mon, 12 Jun 2023 23:59:19 GMT
CMD ["bash"]
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Jun 2023 16:18:53 GMT
ENV LANG=C.UTF-8
# Tue, 06 Jun 2023 16:18:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jun 2023 16:18:53 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PYTHON_VERSION=3.9.17
# Tue, 06 Jun 2023 16:18:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 06 Jun 2023 16:18:53 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/0d8570dc44796f4369b652222cf176b3db6ac70e/public/get-pip.py
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PYTHON_GET_PIP_SHA256=96461deced5c2a487ddc65207ec5a9cffeca0d34e7af7ea1afc470ff0d746207
# Tue, 06 Jun 2023 16:18:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 06 Jun 2023 16:18:53 GMT
CMD ["python3"]
# Wed, 14 Jun 2023 00:54:24 GMT
ENV HY_VERSION=0.26.0
# Wed, 14 Jun 2023 00:54:24 GMT
ENV HYRULE_VERSION=0.3.0
# Wed, 14 Jun 2023 00:54:38 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 14 Jun 2023 00:54:38 GMT
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
	-	`sha256:bfdf325efe819bbc567cb56672cc2909312fa020b8d80ccbcd1ee2d7318cb00d`  
		Last Modified: Tue, 13 Jun 2023 09:00:48 GMT  
		Size: 10.4 MB (10362928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233ab3994dafafc10d36c19c0373f15de049a30ee07f62ed316c71e7dbeabf9e`  
		Last Modified: Tue, 13 Jun 2023 09:00:46 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8b9f5cbd1866417d7d3f1ed6afc00e552fc962ba5639b0ea0166d3c79c2716`  
		Last Modified: Tue, 13 Jun 2023 09:00:48 GMT  
		Size: 3.1 MB (3135387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f997594385aeac0eaa288e80e227affbec1c7eb241be65010f22e99175a96bd`  
		Last Modified: Wed, 14 Jun 2023 00:59:17 GMT  
		Size: 3.6 MB (3641591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-buster` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:d18bc0b5068bd67a22c7fb359dc627dd0f589fc39223b556f351553a351a9901
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46473347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e3d32e77d3a5c97a1f737ff45fb7ff265d0dd6cf9f1ae13c1c471106cf0c7b`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:52 GMT
ADD file:d4a87f28032264e15d38bdd7efb6ffca8deadeb5388758f243e4866b360324c2 in / 
# Mon, 12 Jun 2023 23:40:52 GMT
CMD ["bash"]
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Jun 2023 16:18:53 GMT
ENV LANG=C.UTF-8
# Tue, 06 Jun 2023 16:18:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jun 2023 16:18:53 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PYTHON_VERSION=3.9.17
# Tue, 06 Jun 2023 16:18:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 06 Jun 2023 16:18:53 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/0d8570dc44796f4369b652222cf176b3db6ac70e/public/get-pip.py
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PYTHON_GET_PIP_SHA256=96461deced5c2a487ddc65207ec5a9cffeca0d34e7af7ea1afc470ff0d746207
# Tue, 06 Jun 2023 16:18:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 06 Jun 2023 16:18:53 GMT
CMD ["python3"]
# Tue, 13 Jun 2023 21:30:12 GMT
ENV HY_VERSION=0.26.0
# Tue, 13 Jun 2023 21:30:12 GMT
ENV HYRULE_VERSION=0.3.0
# Tue, 13 Jun 2023 21:30:23 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 13 Jun 2023 21:30:23 GMT
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
	-	`sha256:03b001ef06cfba07019144f7f4db343a9002007cff20d4a6ae6dc0fb095742f1`  
		Last Modified: Tue, 13 Jun 2023 12:54:22 GMT  
		Size: 11.1 MB (11127378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361a81f618250e198664f2dae40e4ed6794adfd9785dad752d3ab134a7017aac`  
		Last Modified: Tue, 13 Jun 2023 12:54:20 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaed1ae01443ee6fcb6800a70c65d65fa2d3755e8deedd6958759ff27b8b22b`  
		Last Modified: Tue, 13 Jun 2023 12:54:21 GMT  
		Size: 3.1 MB (3135719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683eb8d36bc64da6c8228e72034187471d6d7c7dcb381c28d3d04ca0879134c1`  
		Last Modified: Tue, 13 Jun 2023 21:36:55 GMT  
		Size: 3.6 MB (3641542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.9-buster` - linux; 386

```console
$ docker pull hylang@sha256:ae3721a980011b35b70d397634bb8506e8500b538cf88c34f6c6f2929b6e9517
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48526752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8ec57aaef05fb57394fdf47d035cd20d740a41d84338b5efe2bcb5355364f4`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:35 GMT
ADD file:89de6b7378fdf61514133b7bd1ed23bb24397ce045566a30fee2a1347bf6587f in / 
# Mon, 12 Jun 2023 23:40:36 GMT
CMD ["bash"]
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Jun 2023 16:18:53 GMT
ENV LANG=C.UTF-8
# Tue, 06 Jun 2023 16:18:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jun 2023 16:18:53 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PYTHON_VERSION=3.9.17
# Tue, 06 Jun 2023 16:18:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Tue, 06 Jun 2023 16:18:53 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/0d8570dc44796f4369b652222cf176b3db6ac70e/public/get-pip.py
# Tue, 06 Jun 2023 16:18:53 GMT
ENV PYTHON_GET_PIP_SHA256=96461deced5c2a487ddc65207ec5a9cffeca0d34e7af7ea1afc470ff0d746207
# Tue, 06 Jun 2023 16:18:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 06 Jun 2023 16:18:53 GMT
CMD ["python3"]
# Wed, 14 Jun 2023 00:56:15 GMT
ENV HY_VERSION=0.26.0
# Wed, 14 Jun 2023 00:56:15 GMT
ENV HYRULE_VERSION=0.3.0
# Wed, 14 Jun 2023 00:56:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 14 Jun 2023 00:56:32 GMT
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
	-	`sha256:a1ba55f40be75f349171900a9b6eda01507f40f93ea0ab7fcbc6dc5630984db8`  
		Last Modified: Tue, 13 Jun 2023 18:35:42 GMT  
		Size: 11.2 MB (11163417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e326021abc4104e118cee59570ca6e065fa3f308e69b39d82d7b4be049fbb0`  
		Last Modified: Tue, 13 Jun 2023 18:35:40 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc4e4227a4e0cebf39d4ed03b4f8aebafa9ad999b80463e91bb1930d1624c38`  
		Last Modified: Tue, 13 Jun 2023 18:35:41 GMT  
		Size: 3.1 MB (3135715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6231c8b664438a64c24cbc0a87c99dd380df5abf94e577fde3f509f9fd9f5097`  
		Last Modified: Wed, 14 Jun 2023 01:04:23 GMT  
		Size: 3.6 MB (3641636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
