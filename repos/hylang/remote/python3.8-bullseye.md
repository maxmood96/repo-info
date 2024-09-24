## `hylang:python3.8-bullseye`

```console
$ docker pull hylang@sha256:059bffd9f4e759d94b6a5ecc9d39d1a9c4ab6d45c4eb404175acf73ced19da48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `hylang:python3.8-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:90c2ecf1ba1138a6f2ae24bcd04be2261e819a4dcee735d8203eecd95dd66641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49941436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1eb3edbd04dfa7214d723b721cd03662c83bf8d3899eb539b6b80ceec5782e6`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:09 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 04 Sep 2024 22:31:09 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.8.20
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==57.5.0' 		wheel 	; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Wed, 11 Sep 2024 00:07:32 GMT
ENV HY_VERSION=0.29.0
# Wed, 11 Sep 2024 00:07:32 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 11 Sep 2024 00:07:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Sep 2024 00:07:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614f438044d1315436d66b80e5aa3e11f354c2bc6b69d27f4c7928d1118043f4`  
		Last Modified: Thu, 12 Sep 2024 21:12:48 GMT  
		Size: 1.1 MB (1076297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865ac7b857be2366f8dc11171ee6f6620a404af44aa0f9097fd118682c9f0abc`  
		Last Modified: Thu, 12 Sep 2024 21:12:49 GMT  
		Size: 13.7 MB (13681153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dafcdffc0b9711da80d2aa65a23e55b25b5202e253da6b34f13fa00512aefad`  
		Last Modified: Thu, 12 Sep 2024 21:12:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c197c00adce9c386c991a4dc414fe5b146ef503893d1129009455461ba24c1`  
		Last Modified: Thu, 12 Sep 2024 22:03:29 GMT  
		Size: 3.8 MB (3755059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:eac04792ae2fc419d1a51ac69a16d57660ca9fbe103554d6a79ec7552af9d19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9310698782ff409b187f1d369ab020a41b8529442ac34fd5444d6fa54656beca`

```dockerfile
```

-	Layers:
	-	`sha256:d2d146db9fa5f58d5699066bef18f8a904a10fbec8277990ea27866869c52e05`  
		Last Modified: Thu, 12 Sep 2024 22:03:29 GMT  
		Size: 2.7 MB (2712144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b24848e89362e8727b9ebb7577d123dbb508c0deba18f2ea51c7ee2bc2fb6f8c`  
		Last Modified: Thu, 12 Sep 2024 22:03:28 GMT  
		Size: 7.9 KB (7907 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-bullseye` - linux; arm variant v5

```console
$ docker pull hylang@sha256:450d1c7a7a14ca6065cec44e0a42141a8774bcfb2281cac6fb23415c34d74d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47220426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28ef4b2b94c7c991cc5e65b11ffbd96558a58e01b087f19f95ae156b4a87abc`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:48 GMT
ADD file:b6f3f19f4bd2bf78068380b3cd10d72519ced99a2b5abe830b4729df341dcfdf in / 
# Wed, 04 Sep 2024 21:48:48 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.8.20
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==57.5.0' 		wheel 	; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HY_VERSION=1.0.0
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HYRULE_VERSION=0.7.0
# Mon, 23 Sep 2024 18:27:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 23 Sep 2024 18:27:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c8ed7888c72e20491bc1a05ae8b473757ca4d400de33029eab69bacfb9dd933b`  
		Last Modified: Wed, 04 Sep 2024 21:52:15 GMT  
		Size: 28.9 MB (28924911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97807cce5cf83b1c41b0da06d4fa6f187874b42c006053352ec652b3c623a32f`  
		Last Modified: Thu, 05 Sep 2024 09:39:41 GMT  
		Size: 1.1 MB (1059669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03baad1cdcb5d8bc325411f786480ced24b6723ecc299eefe061a9ae63a0c00d`  
		Last Modified: Fri, 13 Sep 2024 01:22:34 GMT  
		Size: 13.5 MB (13461670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc84cf46786ca7307f7f5e55d80adf5d70285f7149215dabdb5d2f0fdf5f5f4`  
		Last Modified: Fri, 13 Sep 2024 01:22:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496eee97a7fea886dba18bbe206cc56e88e7840cc4e81dd97cdefc17ab8c926d`  
		Last Modified: Tue, 24 Sep 2024 01:06:38 GMT  
		Size: 3.8 MB (3773927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:ef61694d7e71a1e17d92e4a23a356f5281c12b7dc21e770ac08f8867960f297b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1c526bc94f0fc02a6511d23ef8e6d9271c488f1663c61a547960af78e189b7`

```dockerfile
```

-	Layers:
	-	`sha256:4624a4f04d2784bdd9edbda877dca77f434e16935da437e67458ce662cd7e12d`  
		Last Modified: Tue, 24 Sep 2024 01:06:38 GMT  
		Size: 2.7 MB (2712377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0be3e17d5b80b5eeea8baf231dfef868f16d2de330987066ce51b6eeec88f8ce`  
		Last Modified: Tue, 24 Sep 2024 01:06:38 GMT  
		Size: 8.0 KB (7989 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:8dfc025a090ba6b5167892fc08797cb5d9a25bb927c6912c620afee6e0c57c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44463615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:334e4465beebf493b84245fbb1e2287b5ff983b3620f6f5ffe093ed919f2acde`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:29 GMT
ADD file:c451ece1244c14bce110ffbe6906867ce12f8e88234988b0edba91009a9dbbf8 in / 
# Wed, 04 Sep 2024 21:58:30 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.8.20
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==57.5.0' 		wheel 	; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HY_VERSION=1.0.0
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HYRULE_VERSION=0.7.0
# Mon, 23 Sep 2024 18:27:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 23 Sep 2024 18:27:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f572303598915f7fb61cc4b47f7207c9ee64d52b9db5fc03ee133ec2dd679347`  
		Last Modified: Wed, 04 Sep 2024 22:02:25 GMT  
		Size: 26.6 MB (26589615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ada9b92e3358e126c71192e75d247c90ed2887997c765fc6f6225bdcb6315`  
		Last Modified: Thu, 05 Sep 2024 10:40:06 GMT  
		Size: 1.0 MB (1041690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a118ca5b46b58e1d553a76cf0c3e09a87d643b004d3fcc2994066dbff14ca79b`  
		Last Modified: Fri, 13 Sep 2024 03:45:40 GMT  
		Size: 13.1 MB (13058146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dc8b0505fac790a88df23912f4ed57333f95e5bf22b0f881b3d195fc1cb41a`  
		Last Modified: Fri, 13 Sep 2024 03:45:40 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d33fd64ec6ac975ce59f898010be047d8829bdae85b6f28f16d3eea05cc82bf`  
		Last Modified: Tue, 24 Sep 2024 01:37:55 GMT  
		Size: 3.8 MB (3773914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:a65bfb3a9c418db49d30a5e81ec5b3b02cf1199535bbe9f0b8054a9bf1ecd9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f6d7f93622f0111a04f1d2b8720e47822ef2ccb6cdccdbd2165a2060343e16`

```dockerfile
```

-	Layers:
	-	`sha256:1924ec356deeb1c0ef0446a2d778e21a39bc956e7307f5cf32c1dedd2bd03d41`  
		Last Modified: Tue, 24 Sep 2024 01:37:55 GMT  
		Size: 2.7 MB (2714385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69824f814f4b9d811c3fce8b87f6b838020a9c837878d880a81650fc192b16c`  
		Last Modified: Tue, 24 Sep 2024 01:37:55 GMT  
		Size: 8.0 KB (7988 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:3588196c3abc3fbe8420196b85f392a82a715d4f0276c42108007ee7c3d03385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48661838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14baf1397aa067dceacb31a574c842ed1a53815af166d224aab87f1281bb474b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:08 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Wed, 04 Sep 2024 21:40:08 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.8.20
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==57.5.0' 		wheel 	; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Wed, 11 Sep 2024 00:07:32 GMT
ENV HY_VERSION=0.29.0
# Wed, 11 Sep 2024 00:07:32 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 11 Sep 2024 00:07:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Sep 2024 00:07:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff275ee82ea95959886edab86ca2e172e2a861493eeb036e1ff15fff94cd962`  
		Last Modified: Mon, 09 Sep 2024 19:59:18 GMT  
		Size: 1.1 MB (1064111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bab4cd74694d0bfcbc008e3a456efd4f88ed4f82e2b23c17866890df145e086`  
		Last Modified: Fri, 13 Sep 2024 01:47:02 GMT  
		Size: 13.8 MB (13767913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f601dfb69d55774823200e40f9e519581ab0a5cb07b537d6ba075b89818c28f`  
		Last Modified: Fri, 13 Sep 2024 01:47:01 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fd75094fe56f9f98289f7313dcffe79c23f0a45bd573c9a0d9ee0fbdc9502b`  
		Last Modified: Fri, 13 Sep 2024 02:49:01 GMT  
		Size: 3.8 MB (3755198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:b9928249832dd506f31da9019ca5aed9b1d74c3f5e4fac8b708ebabfcd9848da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df6d4941370c8f70e1cd2d77c41e8c213fea969068dc4c8ac8c322f634567ab`

```dockerfile
```

-	Layers:
	-	`sha256:e55cc46e414f4f11eb28f6185d7fd62a42f74fa8de2249c0c469ed4e11722c2f`  
		Last Modified: Fri, 13 Sep 2024 02:49:01 GMT  
		Size: 2.7 MB (2712404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5aef6db3eb7ec89104e3212adfc5beb44a1f1f0baeac18f64a21db50e692050`  
		Last Modified: Fri, 13 Sep 2024 02:49:00 GMT  
		Size: 8.3 KB (8304 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:0b2ec3c478eaada1a49c0844ae05eb89ab0d809beba3adb73cb3df25adb53795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51109703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b26e3cf75049077c693c8d13ae3bfdd6c869144eb9a9e4f8859956d1dded13e`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:56 GMT
ADD file:9177ff00c3abd0afc64f577295a060d88f4daed1042f024f7cfcfcd8cb1da9b8 in / 
# Wed, 04 Sep 2024 22:44:56 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.8.20
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==57.5.0' 		wheel 	; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HY_VERSION=1.0.0
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HYRULE_VERSION=0.7.0
# Mon, 23 Sep 2024 18:27:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 23 Sep 2024 18:27:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2e34c6adf259f6e5265d64b5a01b92c3cc93548f22be8c1ccc578b7e9babb30c`  
		Last Modified: Wed, 04 Sep 2024 22:48:51 GMT  
		Size: 32.4 MB (32413314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12aec421e64f97ddde88fd2e1648d00a2a29f44827fab800f8b01e35b13a75c`  
		Last Modified: Thu, 12 Sep 2024 21:12:50 GMT  
		Size: 1.1 MB (1088845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48de1574b4fa70053d79995bb73e73964442cbab3b474d9906493a036ddd3c8e`  
		Last Modified: Thu, 12 Sep 2024 21:12:50 GMT  
		Size: 13.8 MB (13833476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c73cd316b9294930d8499a2fcc978c32308efc258d92f541cab5c3ce9d0839`  
		Last Modified: Thu, 12 Sep 2024 21:12:50 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7299ec84072ae560925a5983febe38bce2e5d7f8c9a722193128dc46871ed1`  
		Last Modified: Tue, 24 Sep 2024 01:01:56 GMT  
		Size: 3.8 MB (3773818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:02d1eed6ab2ffba73a2f0e6cc15de0728d5259e523ec2507feb9481542c57308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 KB (7650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e02953d2f380923eaf3815891720f8791232639cdc7d4f84f4b673d09c47aa`

```dockerfile
```

-	Layers:
	-	`sha256:d91ee33882dff49f37c08b4fa6bf920c861c19820249d1f9a1ac466839b69414`  
		Last Modified: Tue, 24 Sep 2024 01:01:55 GMT  
		Size: 7.7 KB (7650 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-bullseye` - linux; ppc64le

```console
$ docker pull hylang@sha256:1fd0c72bd2444d078c067545f78361f5677d2a02042fac715ffb4e27bd073c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54188436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53c630a0f1128a288cbfeb2054dddfd6599976bd9f0b22fd74f6d61645b2e02`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:18 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Wed, 04 Sep 2024 22:26:20 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.8.20
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==57.5.0' 		wheel 	; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Wed, 11 Sep 2024 00:07:32 GMT
ENV HY_VERSION=0.29.0
# Wed, 11 Sep 2024 00:07:32 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 11 Sep 2024 00:07:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Sep 2024 00:07:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ed09e059599213eafed1242e45b41ed32b891130d746335276413acba8b50c`  
		Last Modified: Mon, 09 Sep 2024 20:48:05 GMT  
		Size: 1.1 MB (1094944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e036aa900871a95523f49def4cb7242d70765715962fac33fddeadbab5f30`  
		Last Modified: Fri, 13 Sep 2024 05:30:01 GMT  
		Size: 14.0 MB (14038426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e2b099956f0fd8bd74f9533281c0e4313b118d5e160765ac497aae9de9a016`  
		Last Modified: Fri, 13 Sep 2024 05:30:00 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7be0f24d21a11aa75e227880cbd75758491aef93ec8b4af3b5308a60971d793`  
		Last Modified: Fri, 13 Sep 2024 07:53:07 GMT  
		Size: 3.8 MB (3755541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:6524d44e96d6a5766a8e7879a856e8c7c0f9585c1ab6dc51a34ef0f0f2987043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2724484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7b40ce7f4dfb4c22f9779939db3604e4c7481ebba0a27e168a4372c8aff81b`

```dockerfile
```

-	Layers:
	-	`sha256:c0a19b2ff97437cce1e76e2d6d6245f596bb9e6494b7fa7d7282933e3749d85c`  
		Last Modified: Fri, 13 Sep 2024 07:53:07 GMT  
		Size: 2.7 MB (2716521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:777973ff90f1cc6ade7a62ef515461ea0ed307075391ae1058370ce46ceb8a92`  
		Last Modified: Fri, 13 Sep 2024 07:53:07 GMT  
		Size: 8.0 KB (7963 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-bullseye` - linux; s390x

```console
$ docker pull hylang@sha256:72c8d84d8826e3212f84de2e95fabeac57aa189c35dfa1f3b2328c05bcf78445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48138645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69deeb001dcd35986bf21dfcca0922c57213e59c6acb93ef4873fed011de65bb`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Sep 2024 21:43:26 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Wed, 04 Sep 2024 21:43:27 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.8.20
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==57.5.0' 		wheel 	; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Wed, 11 Sep 2024 00:07:32 GMT
ENV HY_VERSION=0.29.0
# Wed, 11 Sep 2024 00:07:32 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 11 Sep 2024 00:07:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Sep 2024 00:07:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d8a01ff18197c4f12057b07e586f1b6d0872734d35c7a51d21280e0d7747a1`  
		Last Modified: Thu, 05 Sep 2024 05:56:20 GMT  
		Size: 1.1 MB (1075828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720e4f2e29d7cf701eebd7a8aae9c340f45333a8d5640a32845b78b67b9bccd6`  
		Last Modified: Fri, 13 Sep 2024 02:14:28 GMT  
		Size: 13.6 MB (13643901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34cce5ad14f9a6342ba65c542211f6ea88d3fdec9c16d12816ea99b5c46e37d`  
		Last Modified: Fri, 13 Sep 2024 02:14:27 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5185beb9fdba89e2afbe26c48920cd844c5ea74c09cdf0852d9deedc6f39c`  
		Last Modified: Fri, 13 Sep 2024 04:05:07 GMT  
		Size: 3.8 MB (3755219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:3b77241e79351f4c326ea59747ec09329236c413e4a365ceb27d006c8f41da85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a31ced85013ffa18be4e3c133192588f40290b6d56a2b1349118095ce51d3e`

```dockerfile
```

-	Layers:
	-	`sha256:e09399d5ca99f5163734cab6014e021e3af9f470dd8e3742460f2a3b46edec57`  
		Last Modified: Fri, 13 Sep 2024 04:05:07 GMT  
		Size: 2.7 MB (2712340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66aafc63d91d1e3a8e3979730b3098ae3866cb7476eb17c45833210e5c134537`  
		Last Modified: Fri, 13 Sep 2024 04:05:07 GMT  
		Size: 7.9 KB (7918 bytes)  
		MIME: application/vnd.in-toto+json
