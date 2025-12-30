## `hylang:1-python3.10-trixie`

```console
$ docker pull hylang@sha256:7121b090a678605b888e91a148383edade64b9f0259369fffedec46b25b8f684
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `hylang:1-python3.10-trixie` - linux; amd64

```console
$ docker pull hylang@sha256:ac6370eb88738459296d1ed3d29db75a0aeb42848d866964680e7c676909b22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50160286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb99218a8f141458ce8d11ce55b135ee2ab7eb5dcf0faa970b717592ba72d6a8`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:36:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:36:07 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 23:36:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 23:36:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Mon, 08 Dec 2025 23:36:07 GMT
ENV PYTHON_VERSION=3.10.19
# Mon, 08 Dec 2025 23:36:07 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Mon, 08 Dec 2025 23:42:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 23:42:08 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 23:42:08 GMT
CMD ["python3"]
# Tue, 09 Dec 2025 00:58:40 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 00:58:40 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 00:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Dec 2025 00:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd9e26f8f287696571eb98b5e10e91211abbc4dd5918c5a2f50d1b697191540`  
		Last Modified: Mon, 08 Dec 2025 23:42:22 GMT  
		Size: 1.3 MB (1292742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004f0aa18a079de0973edc8a53f2397b4fe498cc595e21fb32ab01c89eb00a70`  
		Last Modified: Mon, 08 Dec 2025 23:42:23 GMT  
		Size: 13.8 MB (13820540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bceabe27cdff3949f8ad5eb4db394db5850a5fbc33e0371b4d621298ef7ccb1`  
		Last Modified: Mon, 08 Dec 2025 23:42:21 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8757ec67b949b15670ee7ceca5f6efdf30c28f326a4eeeaf207f0eba5ee72d1f`  
		Last Modified: Tue, 09 Dec 2025 00:58:53 GMT  
		Size: 5.3 MB (5270260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:d7377db0cc3110331bd93f8f83a11b71b18292bd45fab4884be1bf247e153961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9e024530c4b8af6a056a5ea6b7452d421de3df322cb6241b3a5cea2ce77b35`

```dockerfile
```

-	Layers:
	-	`sha256:7df760305f2925ad38941fdbf08bb46c6e025076e2b5b0d5612c4cce921a5f08`  
		Last Modified: Tue, 09 Dec 2025 03:20:04 GMT  
		Size: 2.2 MB (2199949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c366b815b628ab54795177d58ee64321508b582de6ee1a1136fd35f68a3e8719`  
		Last Modified: Tue, 09 Dec 2025 03:20:04 GMT  
		Size: 9.3 KB (9320 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; arm variant v5

```console
$ docker pull hylang@sha256:9a824dd66daab0fb2b04bd67fa52980d959a14a858d211c1146bfa99fe578046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47971350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1ce516f6939b03398f3640d8ce0bae85a13a282830bdb224ce44a3ccad6389`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:59:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:59:43 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:59:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:59:43 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 30 Dec 2025 00:59:43 GMT
ENV PYTHON_VERSION=3.10.19
# Tue, 30 Dec 2025 00:59:43 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Tue, 30 Dec 2025 01:11:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 30 Dec 2025 01:11:03 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 30 Dec 2025 01:11:03 GMT
CMD ["python3"]
# Tue, 30 Dec 2025 02:31:45 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 02:31:45 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 02:31:45 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 02:31:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b6fceedda32396cc5563df6cf7ebff565b34c27c7baf8962fe469415844f22`  
		Last Modified: Tue, 30 Dec 2025 01:11:18 GMT  
		Size: 1.3 MB (1275918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fe8c6a593f995deff18eae72127ca445715c36e7e420abbe6e789fa07287c4`  
		Last Modified: Tue, 30 Dec 2025 01:11:19 GMT  
		Size: 13.5 MB (13480617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c29a594b1ce2ef19c9ae183cd0f396574216aadbd6f15a4cec08889284b2003`  
		Last Modified: Tue, 30 Dec 2025 01:11:18 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c551793b6cbce5cac48e974eed414804d40f21ca49ee4f73d8a10a851dc12c73`  
		Last Modified: Tue, 30 Dec 2025 02:31:58 GMT  
		Size: 5.3 MB (5270420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:a367baca6a8a5e8106220b1f1cf9f87300ae17b275d41645ea1d6b86b881f72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cca4ac65950401a780c4c1cbc804cf47eb94e9894929d4e936b0350aac2ff3c`

```dockerfile
```

-	Layers:
	-	`sha256:1d4e82bd98ea2a3c30d4a79ece05583422441396aeacc774c46dbaf99c9087d6`  
		Last Modified: Tue, 30 Dec 2025 03:19:02 GMT  
		Size: 2.2 MB (2202950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8be156b0a293a3149583def19dc6e73e3e3e26d5ea3c804b465d26ec882779b`  
		Last Modified: Tue, 30 Dec 2025 03:19:03 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; arm variant v7

```console
$ docker pull hylang@sha256:56d80663feaeb3ed60db695d4f9cd941cb2c607187bd645c0b0a928881e84bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45944910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d6b59b68afdc29522febdc932f9d050bf5aec5fd85808334b26707123ad534`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:59:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:59:12 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 00:59:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:59:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 09 Dec 2025 00:59:12 GMT
ENV PYTHON_VERSION=3.10.19
# Tue, 09 Dec 2025 00:59:12 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Tue, 09 Dec 2025 01:10:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 09 Dec 2025 01:10:08 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 09 Dec 2025 01:10:08 GMT
CMD ["python3"]
# Tue, 09 Dec 2025 01:52:33 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 01:52:33 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 01:52:33 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Dec 2025 01:52:33 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efc46b28e3936c0252707981c62d2c124986230b55542697d16409a71f9dc4f`  
		Last Modified: Tue, 09 Dec 2025 01:10:22 GMT  
		Size: 1.2 MB (1248519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265d2167fb5f445bcb6b9c45f1d23fc27a8cae5af90c48e7feac4ac3c62e7b44`  
		Last Modified: Tue, 09 Dec 2025 01:10:23 GMT  
		Size: 13.2 MB (13215720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad903192f6ae2ab6b0372cd6d29b34abf3a6108ab3b9ad6badbfe219a5e88264`  
		Last Modified: Tue, 09 Dec 2025 01:10:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb2ec0e949042161a23cccb955c4946bdc601b0ce39b21676bff3fb06bcc8fe`  
		Last Modified: Tue, 09 Dec 2025 01:52:46 GMT  
		Size: 5.3 MB (5270411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:409c3bcf76f3246242fbf63051d8e392532f44c416ec1cecaf0152c35136bf5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845d61d0f46e2688f950242b5fa95dfcb8d7d4aac5b5018d2083e9e95972dbc5`

```dockerfile
```

-	Layers:
	-	`sha256:36fbb62466029ac3c36daf15be1ac6396af295e2fb0b528d1a1b19b8dc9438af`  
		Last Modified: Tue, 09 Dec 2025 03:20:13 GMT  
		Size: 2.2 MB (2201403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b7612f9574ba83d1e543fb85a0be4d36cb8a0c5a70891a73823e9c377d528ad`  
		Last Modified: Tue, 09 Dec 2025 03:20:14 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:dc9ce860e4fd00d7206ba6d92eeaccabfcfb3ac0933ad06642a0e19dc08f3321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50458099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b5286f065b54b963fcff12f30ec1e5e3d91b12922e22d7ce185d1d561a42f0`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:41:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:41:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 23:41:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 23:41:54 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Mon, 08 Dec 2025 23:41:54 GMT
ENV PYTHON_VERSION=3.10.19
# Mon, 08 Dec 2025 23:41:54 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Mon, 08 Dec 2025 23:49:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 23:49:25 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 23:49:25 GMT
CMD ["python3"]
# Tue, 09 Dec 2025 00:56:40 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 00:56:40 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 00:56:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Dec 2025 00:56:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f3d64adbba0c169b4ca917d3d1c2ab0c09e4e6bc4952320b4ef9e6f816eb2d`  
		Last Modified: Mon, 08 Dec 2025 23:49:39 GMT  
		Size: 1.3 MB (1273741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522f1ca1e675e6707970283c87b89b52cc177a40a0b020724146a6bd396d12bc`  
		Last Modified: Mon, 08 Dec 2025 23:49:40 GMT  
		Size: 13.8 MB (13775161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673544d1656fda8db7cb4d61be7967ed31542944d5e730bb99931b4f32b0d4bc`  
		Last Modified: Mon, 08 Dec 2025 23:49:39 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e50cf7c65a381438c855cbe92c97e486f95a4ff6cef3a03144500b07423cf79`  
		Last Modified: Tue, 09 Dec 2025 00:56:54 GMT  
		Size: 5.3 MB (5270321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:6f4dd29e88726dd7454c4c2b4fbe24a83f711c11724ec41f84c46a97d4a1c8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6775b3a6dca69b4fbf4523e6ebb727b10c84b49a48e62692a8e9742a8d0cb8d0`

```dockerfile
```

-	Layers:
	-	`sha256:18d9ca3348944d6b6314f6e719433d04737eec29ae45de9a8e6d49af3d5fa990`  
		Last Modified: Tue, 09 Dec 2025 03:20:18 GMT  
		Size: 2.2 MB (2200263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d8fd940f79433f1140fd60ea86cce58d539af749186d5443ea90f0010502331`  
		Last Modified: Tue, 09 Dec 2025 03:20:19 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; 386

```console
$ docker pull hylang@sha256:efc6be7fc330b73f4b374db2b434b45cd4bbc69173a38cd892e65049791cc93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51711496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2533d401910aeeeede498de079a72f9393632187dfaeb9b67638a2a008f4d1aa`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:06:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:06:09 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:06:09 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 30 Dec 2025 00:06:09 GMT
ENV PYTHON_VERSION=3.10.19
# Tue, 30 Dec 2025 00:06:09 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Tue, 30 Dec 2025 00:13:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 30 Dec 2025 00:13:44 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 30 Dec 2025 00:13:44 GMT
CMD ["python3"]
# Tue, 30 Dec 2025 01:08:49 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 01:08:49 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 01:08:49 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 01:08:49 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42093768cb272e650817ab231588d3238f5c4171c4ca0a8b1561b8376394ea33`  
		Last Modified: Tue, 30 Dec 2025 00:13:57 GMT  
		Size: 1.3 MB (1296861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e6464e7619c7a284182bed7ca10533d9d1b5e89560c1d58da0f4d90006400`  
		Last Modified: Tue, 30 Dec 2025 00:13:59 GMT  
		Size: 13.9 MB (13851039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4073253e2808a00cb1ff0e4ab5707649844bde8771279d3e8f3b55ff933ea1`  
		Last Modified: Tue, 30 Dec 2025 00:13:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1a01cb400faf9e43341cc827293761ce5190e71d0060ed3724c7b718d4d6e1`  
		Last Modified: Tue, 30 Dec 2025 01:09:03 GMT  
		Size: 5.3 MB (5270248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:8e13f1465b97fe2120cb5faca51b0783c16a056608cd0b4c5807058026c4ca70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1671b2f25d73667d6d0e61fe4f4d268cc0ace540dfabfd355c1ce3e0bd32c4dd`

```dockerfile
```

-	Layers:
	-	`sha256:af556f469e663ae29e72542331de8d5076e502e95c22fe17899fa35ee6ca1069`  
		Last Modified: Tue, 30 Dec 2025 03:19:13 GMT  
		Size: 2.2 MB (2197110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d27a64f94fd0c516367b1870b0f2e53694e1a1c1b5e56f69100d3940f1e4d70`  
		Last Modified: Tue, 30 Dec 2025 03:19:14 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; ppc64le

```console
$ docker pull hylang@sha256:24af0c5471148a858e79f9d0495bf42024986db726064416eaa781d69b94c52d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54336452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe291e1baff6c2759a4aa6683e069a45bc7e6b6decafea12c99f6b8303412d5`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 03:03:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 03:03:53 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 03:03:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 03:03:53 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 09 Dec 2025 03:03:53 GMT
ENV PYTHON_VERSION=3.10.19
# Tue, 09 Dec 2025 03:03:53 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Tue, 09 Dec 2025 03:33:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 09 Dec 2025 03:33:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 09 Dec 2025 03:33:40 GMT
CMD ["python3"]
# Tue, 09 Dec 2025 12:26:37 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 12:26:37 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 12:26:37 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Dec 2025 12:26:37 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b34e25ea380765900def74de050ce393f0ba0ffcdb8f03969296999b9cf87d`  
		Last Modified: Tue, 09 Dec 2025 03:21:53 GMT  
		Size: 1.3 MB (1320591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685e7c33a3a944c2323a3c0b2603a6eb7bf2598440bd4dfb020758972560291b`  
		Last Modified: Tue, 09 Dec 2025 03:34:10 GMT  
		Size: 14.1 MB (14148107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b04d3dc6055818ebce89482e27f131b35d33d88522d2121dbe83687ceab630`  
		Last Modified: Tue, 09 Dec 2025 03:34:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba47f65261e7806a02f68a17bcff38a2685f94a9e7d50132614235e927b05112`  
		Last Modified: Tue, 09 Dec 2025 12:26:59 GMT  
		Size: 5.3 MB (5270615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:7efd9a9c0d1c29f0cbd2cf79b131e9a44b0cbd54dc9346a8540bfa990c018adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd209131c19841188fbe45f768ae7f392ede000a7f4f5da8edcf17107a2db4f`

```dockerfile
```

-	Layers:
	-	`sha256:8b0a16a1016db6ed6fedc107b1ccf0f6bd16b16d742018ec3b44ab8ede693a54`  
		Last Modified: Tue, 09 Dec 2025 15:17:50 GMT  
		Size: 2.2 MB (2203540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:804b0f666313bac1d4092053d5991f10693298731cbd1dc41ac3a1668c3b5ded`  
		Last Modified: Tue, 09 Dec 2025 15:17:51 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; riscv64

```console
$ docker pull hylang@sha256:61abf8a2a708990815fc17e026ff8ff04b7d8a5ec0cee29fcc795e96559dd950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48533487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d022a9ed18c61a2860acd8ea59a14b8ed4b669c5601178644da476c58b37058`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Fri, 12 Dec 2025 17:01:03 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Dec 2025 17:01:03 GMT
ENV LANG=C.UTF-8
# Fri, 12 Dec 2025 17:01:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 12 Dec 2025 17:01:03 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 12 Dec 2025 17:01:03 GMT
ENV PYTHON_VERSION=3.10.19
# Fri, 12 Dec 2025 17:01:03 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Fri, 12 Dec 2025 21:20:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 12 Dec 2025 21:20:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 12 Dec 2025 21:20:47 GMT
CMD ["python3"]
# Sun, 14 Dec 2025 17:12:56 GMT
ENV HY_VERSION=1.1.0
# Sun, 14 Dec 2025 17:12:56 GMT
ENV HYRULE_VERSION=1.0.1
# Sun, 14 Dec 2025 17:12:56 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 14 Dec 2025 17:12:56 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f13f855d7dafc2c6049eda1545f4fb7f0509441af47211c59ec31d8ae5ab6f8`  
		Last Modified: Fri, 12 Dec 2025 18:43:00 GMT  
		Size: 1.3 MB (1259929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96001479c3987dde0eaacab24db3686ffe96550db2f6e134e28ebcd276fde9f`  
		Last Modified: Fri, 12 Dec 2025 21:22:08 GMT  
		Size: 13.7 MB (13728633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9a70935d784587c71d67386f0aebf3e2d88b0a52bcad52df4b825ce454d0a`  
		Last Modified: Fri, 12 Dec 2025 21:22:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69abd391925e92feb7e0d2d6d392e023ed4616c392919cf693b2059317f091b`  
		Last Modified: Sun, 14 Dec 2025 17:14:06 GMT  
		Size: 5.3 MB (5271520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:5d5d3fa6801367ebfa67c1207782fbca7548a12df73f6391fb3dd058cccd5635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f137b44dac054cc6005c5cbc8a19681b971bc0ee47a768bf3f0f6de1988ab293`

```dockerfile
```

-	Layers:
	-	`sha256:e02b5cf09ccf41553a9e1616f5c7bfa53066d74fff1babc92b7ed12ed4e10404`  
		Last Modified: Sun, 14 Dec 2025 18:17:58 GMT  
		Size: 2.2 MB (2193911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36d5e6a9263123f39b602f773d3d19590db58089e01aabfd2efd455aad0206a4`  
		Last Modified: Sun, 14 Dec 2025 18:17:59 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; s390x

```console
$ docker pull hylang@sha256:930514867854d2a13b05d7b17f0b35d13ea5d1f788fcbf4e3f2db7b8fba9d0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50164828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16aa0db6e000fd8bf230580345bbf1989e6b24503c896f5db8024f54552a7cb2`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:58:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:58:55 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 00:58:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:58:55 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 09 Dec 2025 00:58:55 GMT
ENV PYTHON_VERSION=3.10.19
# Tue, 09 Dec 2025 00:58:55 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Tue, 09 Dec 2025 01:19:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 09 Dec 2025 01:19:33 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 09 Dec 2025 01:19:33 GMT
CMD ["python3"]
# Tue, 09 Dec 2025 03:03:10 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 03:03:10 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 03:03:10 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Dec 2025 03:03:10 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a8f946063fe312146d10145c9b2a145f96fe58dda4950829dda78dae99a8ac`  
		Last Modified: Tue, 09 Dec 2025 01:11:20 GMT  
		Size: 1.3 MB (1305171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e18f503eccc3b79502603f61cd8d99188f202cdd2d0683dcc21409f24f78239`  
		Last Modified: Tue, 09 Dec 2025 01:19:52 GMT  
		Size: 13.8 MB (13754568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962ec6fda82e56383fc8118157b23965c05d253a29ed5821d15b0a9cdd2419cc`  
		Last Modified: Tue, 09 Dec 2025 01:19:51 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d44cbd17fec2ff3fb3d984855213b90f9f20488aca62edead4ac8c02c6f415`  
		Last Modified: Tue, 09 Dec 2025 03:03:27 GMT  
		Size: 5.3 MB (5270440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:a9f64251c7ffeaa760b4c38b84b7d0cf599e6e0ad62d4a546516702542a32a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3287eeb2679eed20ddea6a37949af15c08c33c2f4d4ed1f2b2e07f3d9509c8`

```dockerfile
```

-	Layers:
	-	`sha256:73fd5b9e7b4b13c3a5069a7f5db7614979976e024ab82f37df9493de493b7198`  
		Last Modified: Tue, 09 Dec 2025 03:20:47 GMT  
		Size: 2.2 MB (2201388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89f32719e78e3fbe75c1e8b6593deeeb079db56c225af8fef30afe6974ff3084`  
		Last Modified: Tue, 09 Dec 2025 03:20:48 GMT  
		Size: 9.3 KB (9320 bytes)  
		MIME: application/vnd.in-toto+json
