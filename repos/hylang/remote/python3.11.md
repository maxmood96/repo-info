## `hylang:python3.11`

```console
$ docker pull hylang@sha256:c8e1d8be708d93858eb726ab8769b96d1980e04e56e66512ccce132c6920498f
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

### `hylang:python3.11` - linux; amd64

```console
$ docker pull hylang@sha256:0f37b745ca4e3f42b66b3c69af40d950e13956a8395539abd8121f90c9009c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52522003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2befc375034d46af08d89dea033a02f0407a27947ce8d7a0aff743a73bf14af6`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:34:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:34:05 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 23:34:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 23:34:05 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Mon, 08 Dec 2025 23:34:05 GMT
ENV PYTHON_VERSION=3.11.14
# Mon, 08 Dec 2025 23:34:05 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Mon, 08 Dec 2025 23:42:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 23:42:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 23:42:01 GMT
CMD ["python3"]
# Tue, 09 Dec 2025 00:58:47 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 00:58:47 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 00:58:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Dec 2025 00:58:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cf4c3b83019e176aba979aba419d35f56576bbcfc4f7249a1ab1d4b536730b`  
		Last Modified: Mon, 08 Dec 2025 23:42:16 GMT  
		Size: 1.3 MB (1292754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d55cfecf3663813d03c369bcd532b89f41cf07b65d95887ef686538370a747c`  
		Last Modified: Mon, 08 Dec 2025 23:42:17 GMT  
		Size: 14.4 MB (14363455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0cdbca744e7bd0ce0ff6da73b9148829b04309925992954a314ba203f56e99`  
		Last Modified: Mon, 08 Dec 2025 23:42:16 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f5a00765dafdc92f813b5007b5bfebf477da964fb5ed71d918f0787d078758`  
		Last Modified: Tue, 09 Dec 2025 00:59:00 GMT  
		Size: 7.1 MB (7089049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:d103f05df7ad85de9001945682a06d96aee644f70e0712310616bd8be759f220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4097445adc9343ce93bbf36d89e62c6afeb5e0ef4eee61b8211fee815d217db2`

```dockerfile
```

-	Layers:
	-	`sha256:4126c73464ac9f8508039822ff92cd58aced8609d9df96352625d4b82a5962b1`  
		Last Modified: Tue, 09 Dec 2025 03:20:50 GMT  
		Size: 2.2 MB (2199909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e8f9cde1557510398254fe09483a813cdd3babce18e729ae5136e16d39e10bf`  
		Last Modified: Tue, 09 Dec 2025 03:20:50 GMT  
		Size: 9.3 KB (9320 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11` - linux; arm variant v5

```console
$ docker pull hylang@sha256:9ca08d163dc7a1f27c047df39c327d106481d0fc6307a998afeff9bfcd10d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50305622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d170803c6d2435c26884d41b5a3ccf6b7c2d656a23ccb41e85b93e07d3bf9a`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:50:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:50:26 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:50:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:50:26 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 30 Dec 2025 00:50:26 GMT
ENV PYTHON_VERSION=3.11.14
# Tue, 30 Dec 2025 00:50:26 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Tue, 30 Dec 2025 01:08:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 30 Dec 2025 01:08:49 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 30 Dec 2025 01:08:49 GMT
CMD ["python3"]
# Tue, 30 Dec 2025 02:01:38 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 02:01:38 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 02:01:38 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 02:01:38 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3ea114ff713968caef4500307f9da2fa094f6a98221dd9ef815076f1dba856`  
		Last Modified: Tue, 30 Dec 2025 01:09:03 GMT  
		Size: 1.3 MB (1275916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9afd9070fd4a9c381384774b72ed8c3eaeb827cadc705d7fe15cc0d4d75c49`  
		Last Modified: Tue, 30 Dec 2025 01:09:04 GMT  
		Size: 14.0 MB (13996325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1d628ca992944a826b309c6f872e21543944881769b16f624baefd061275c2`  
		Last Modified: Tue, 30 Dec 2025 01:09:02 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c97b20b8bd8876cb7408d074a9ebab99eea4fdf8793db6b66bb49770c8d9e29`  
		Last Modified: Tue, 30 Dec 2025 02:01:52 GMT  
		Size: 7.1 MB (7088985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:bd742bb3176bee982a81c4de48a5bdad277cec9a1e3c09c5644a40bc5a67b6dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ddd06d4c09e8bcd47f5b24d331e43362cbf0b8b8f482c0d8bf5662bfaf9a23`

```dockerfile
```

-	Layers:
	-	`sha256:e83b20426e41e7d3d48f0be8f17b7218c6f2f7755f1b9480f616bdae949e4d1e`  
		Last Modified: Tue, 30 Dec 2025 03:19:29 GMT  
		Size: 2.2 MB (2202910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eddcc7cb2870b4ace76a2cbb39ea555968f2417684b833f5badc9c1edefeb886`  
		Last Modified: Tue, 30 Dec 2025 03:19:30 GMT  
		Size: 9.4 KB (9431 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11` - linux; arm variant v7

```console
$ docker pull hylang@sha256:b461b2eb475a89ba7ce2a22c17ec8feb8799e12f68f312e26f911dc8f78d980c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48277844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af43396b89faae2b526a24c1acbbfd75cd7e8b77d1f609063248075b71f46333`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:27:25 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:27:25 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:27:25 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 30 Dec 2025 01:27:25 GMT
ENV PYTHON_VERSION=3.11.14
# Tue, 30 Dec 2025 01:27:25 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Tue, 30 Dec 2025 01:44:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 30 Dec 2025 01:44:08 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 30 Dec 2025 01:44:08 GMT
CMD ["python3"]
# Tue, 30 Dec 2025 02:44:24 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 02:44:24 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 02:44:24 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 02:44:24 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d2b76b8f6a8928bcd8ff867e5f50f328df18adc3a142cd56ea6d7cbfa2baf8`  
		Last Modified: Tue, 30 Dec 2025 01:44:20 GMT  
		Size: 1.2 MB (1248529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad5b475d6045cb524403a1ee4f7b5e980b81590cce87eae028d95bba8859ee6`  
		Last Modified: Tue, 30 Dec 2025 01:44:22 GMT  
		Size: 13.7 MB (13730090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8134fd1276990f37f9c4dee7b897a964b53c660c77c447576a1b9387b36d1523`  
		Last Modified: Tue, 30 Dec 2025 01:44:20 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2149e39b198f4afc9788574af15c5dea7dd2a2854011511537319e592a59ea91`  
		Last Modified: Tue, 30 Dec 2025 02:44:36 GMT  
		Size: 7.1 MB (7088975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:d06d92bdd0db1bf375d20dad92a07c584778b6c9cd9c88f43b9b2d52033b506b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea95e2ce19bb704910aad68c90d0586556edd93af736159f620640c1ac1c7e7`

```dockerfile
```

-	Layers:
	-	`sha256:95c0bf50c1005918db496c6d5c7bea4a9a7af8f1b851e2aaa4e7c4bb45624085`  
		Last Modified: Tue, 30 Dec 2025 03:22:11 GMT  
		Size: 2.2 MB (2201363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9bc84e26f57ee135e67634a0b33a819def54635e7bffc4d18e22b2f4e590a27`  
		Last Modified: Tue, 30 Dec 2025 03:22:11 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:7dfa317dc05f28c0596186dcb4806f2ad86c3ee2a2ff6c6ea8b9847cf3ba8158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52813750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15aa0ab3a6e2ad88d38b8f920ba1a921ae2b368cf3590da0c06678de2fab9a1`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:39:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:39:16 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 23:39:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 23:39:16 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Mon, 08 Dec 2025 23:39:16 GMT
ENV PYTHON_VERSION=3.11.14
# Mon, 08 Dec 2025 23:39:16 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Mon, 08 Dec 2025 23:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 23:50:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 23:50:27 GMT
CMD ["python3"]
# Tue, 09 Dec 2025 00:54:40 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 00:54:40 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 00:54:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Dec 2025 00:54:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf6e8047453b31b08baebfe66323f7f1fa2be022577fa1f2aed06f5e710d1da`  
		Last Modified: Mon, 08 Dec 2025 23:50:41 GMT  
		Size: 1.3 MB (1273744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa8861819f0519a75b4c22a5f364cab4f4b35968dc06724a58a82d6cc42bf1b`  
		Last Modified: Mon, 08 Dec 2025 23:50:42 GMT  
		Size: 14.3 MB (14312166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913c05e4a1c0a655817e913f334e1402b8f4d5ffc5ecdc8d8981beb71736b143`  
		Last Modified: Mon, 08 Dec 2025 23:50:41 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b1acc616299c2463a0112c2f5b6134e7e805f0dcaefbe06909c5a03976c39f`  
		Last Modified: Tue, 09 Dec 2025 00:55:00 GMT  
		Size: 7.1 MB (7088963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:de2896bac3eddf6f8b267b228428430f33791c4aedd5bd6483138d1103cb2482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c7daafbecb69522e1576ee1769f3322eed4a9936fb615b4f3f480f3c3d7d73`

```dockerfile
```

-	Layers:
	-	`sha256:ebbe8930c238504873b06a731d330ed19aa2f7a97b0deafb56cb1517dd8ba77a`  
		Last Modified: Tue, 09 Dec 2025 03:21:19 GMT  
		Size: 2.2 MB (2200223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3588312a7706cecaa5a7a78705dfacba1c7e5934858014bff5c2949c64060ae2`  
		Last Modified: Tue, 09 Dec 2025 03:21:20 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11` - linux; 386

```console
$ docker pull hylang@sha256:c1864f93c5c6e60d2443a9874de3a05473537af6d73edb622d60eed61baaf4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54081228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787c7c84e661596c39679c20e79140f6641c46cffd9df0c5b7ceaca80a16cba3`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:02:46 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:02:46 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:02:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:02:46 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 30 Dec 2025 00:02:46 GMT
ENV PYTHON_VERSION=3.11.14
# Tue, 30 Dec 2025 00:02:46 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Tue, 30 Dec 2025 00:12:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 30 Dec 2025 00:12:15 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 30 Dec 2025 00:12:15 GMT
CMD ["python3"]
# Tue, 30 Dec 2025 01:08:08 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 01:08:08 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 01:08:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 01:08:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188a9bd0807ee8c19bef1759d90afb5e671eec17e1b5f88e35be21f8f03e4d00`  
		Last Modified: Tue, 30 Dec 2025 00:12:28 GMT  
		Size: 1.3 MB (1296817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e7c3eacd70a235b2274cd17a11748403f8600683cc1caafd6f1b20754dbc53`  
		Last Modified: Tue, 30 Dec 2025 00:12:29 GMT  
		Size: 14.4 MB (14401966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e861afa81eb96497ec0d65c63947c1e91032c6dc1fb3efbacf4b1a3ea0061f`  
		Last Modified: Tue, 30 Dec 2025 00:12:28 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa048361175a279b918f9b496c333e1551914a22b75ca2eca6ef4fc88e93770`  
		Last Modified: Tue, 30 Dec 2025 01:08:22 GMT  
		Size: 7.1 MB (7089096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:f425560faf44730bae2b6ff49092094d0410de764c6465e4aeac64b92549a4a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd30f1f4d5a7e33099e4fb17ea9120bac236d0503169f824fb9262057623e37`

```dockerfile
```

-	Layers:
	-	`sha256:b19fa99ac544143d7ca4584948eddc8d71041a90ef1ce7e7e5275bfb86daaffc`  
		Last Modified: Tue, 30 Dec 2025 03:19:40 GMT  
		Size: 2.2 MB (2197070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4916ca5503182a406bfac7120d8c8eb70f69e882a2f8b1b5770a5d2a4b312086`  
		Last Modified: Tue, 30 Dec 2025 03:19:41 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11` - linux; ppc64le

```console
$ docker pull hylang@sha256:49675845b4c22768558a710e4bd8cd3ba847323582e69caa95c3b10376f5bff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56705355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449a70f3d1e8a45a3a0eeecf233b5bb73211647cfa763112741a903633b9bc29`
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
ENV PYTHON_VERSION=3.11.14
# Tue, 09 Dec 2025 03:03:53 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Tue, 09 Dec 2025 03:33:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 09 Dec 2025 03:33:46 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 09 Dec 2025 03:33:46 GMT
CMD ["python3"]
# Tue, 09 Dec 2025 12:25:53 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 12:25:53 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 12:25:53 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Dec 2025 12:25:53 GMT
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
	-	`sha256:95ceb1a82925411d884e6c11f95003b8a6480c250573db3fa7d2c36acbaaf2f8`  
		Last Modified: Tue, 09 Dec 2025 03:34:11 GMT  
		Size: 14.7 MB (14698266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5b9f892b20fd79467a7698ebf140665adea6e94591ff64fa5066aba7782c05`  
		Last Modified: Tue, 09 Dec 2025 03:34:09 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0f7a0acd05c657bde7a0388db2d6761c4b404ff31243dc1c2206aba0635e4e`  
		Last Modified: Tue, 09 Dec 2025 12:26:15 GMT  
		Size: 7.1 MB (7089359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:f437d5bd7d8f8f5a8f38f2747d3f1bc763d29d8b1a210fdb7b736c061966fb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0f41eba54cad37b8b8e62b7b6c158411b6a9a6862fb6b04e53163894960fb0`

```dockerfile
```

-	Layers:
	-	`sha256:1a2dc59e79a4e5f61e2febd9a2187c7d03d29079a86f2699104479d4e4edfa8b`  
		Last Modified: Tue, 09 Dec 2025 15:18:05 GMT  
		Size: 2.2 MB (2203500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f27efb030fa7d9591f9b5eea0fcd04f0ed527d5fa2e748cab952d7b59bdee579`  
		Last Modified: Tue, 09 Dec 2025 15:18:06 GMT  
		Size: 9.4 KB (9387 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11` - linux; riscv64

```console
$ docker pull hylang@sha256:748f609bb4ba13298d7a61a1b9da741c5b151b6ab4385cd317bc38b512e8a5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50815390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44b0cf7ec071f02ea606b72df278a33b5220ab94e3832792b2acdb63806d04c`
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
ENV PYTHON_VERSION=3.11.14
# Fri, 12 Dec 2025 17:01:03 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Fri, 12 Dec 2025 20:04:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 12 Dec 2025 20:04:28 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 12 Dec 2025 20:04:28 GMT
CMD ["python3"]
# Sun, 14 Dec 2025 17:08:47 GMT
ENV HY_VERSION=1.1.0
# Sun, 14 Dec 2025 17:08:47 GMT
ENV HYRULE_VERSION=1.0.1
# Sun, 14 Dec 2025 17:08:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 14 Dec 2025 17:08:47 GMT
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
	-	`sha256:bc3de216e78467232e446b973a70ca957ce0cae2deb23bf30a9f0d5a83c4d0e2`  
		Last Modified: Fri, 12 Dec 2025 20:05:54 GMT  
		Size: 14.2 MB (14191957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4955b74deefcfac31586911fdd34621740433904e129590d7b222ed1949c21`  
		Last Modified: Fri, 12 Dec 2025 20:05:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de0ef4d110c8d73ec032052cf47e6aee19ee662b93ffc1969c3ca920b553dbc`  
		Last Modified: Sun, 14 Dec 2025 17:10:00 GMT  
		Size: 7.1 MB (7090099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:5594b177c9f8d326cb1406b2ee99c700b847d5bf0120627ca5aef57dc5949064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e773e2b4dedfbef148b4c2bafbce162168033dec1f6db7d2690c02b16ecd7d`

```dockerfile
```

-	Layers:
	-	`sha256:d76fd9772a73c58cde47c3e019c6553b47dfd2a5492a79c4b6beb95970663471`  
		Last Modified: Sun, 14 Dec 2025 18:18:13 GMT  
		Size: 2.2 MB (2193871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b2fe08d0c2b0429b06e22881626d75550bb4adf6aba5d3bf6de1c2cfb73cd89`  
		Last Modified: Sun, 14 Dec 2025 18:18:14 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11` - linux; s390x

```console
$ docker pull hylang@sha256:81761c13c678e56f09d69cc4d645756a874152a95f66a7e0d242acd321823c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52594805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36534403b83c232ddc83f1fde49d23f2b3c75cc1e5412c4a4de3a3f7033d3ea7`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:32:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:32:38 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:32:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:32:38 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 30 Dec 2025 01:32:38 GMT
ENV PYTHON_VERSION=3.11.14
# Tue, 30 Dec 2025 01:32:38 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Tue, 30 Dec 2025 01:47:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 30 Dec 2025 01:47:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 30 Dec 2025 01:47:07 GMT
CMD ["python3"]
# Tue, 30 Dec 2025 03:05:30 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 03:05:30 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 03:05:30 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 03:05:30 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a309564aa467bb8a1a074ae93a88b5cb42de0b4b4ebe7c88554cfaa0bcbf710`  
		Last Modified: Tue, 30 Dec 2025 01:44:41 GMT  
		Size: 1.3 MB (1305186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c56e3a96397815abe1bcdca1ec6b4ebc40c9ee81d4ee7a542768f2477548884`  
		Last Modified: Tue, 30 Dec 2025 01:47:26 GMT  
		Size: 14.4 MB (14365995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d800bf5c26493a97dd54f4bdb23e7724d897d70c6f161ad288e9acdcc71c11`  
		Last Modified: Tue, 30 Dec 2025 01:47:25 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099a8b4eb6136a422cabe7c6542ffab8c3313dbdd1050b1448cab543aeb3750a`  
		Last Modified: Tue, 30 Dec 2025 03:05:46 GMT  
		Size: 7.1 MB (7088955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:f8b7766ab896a8421c114bf4d016ab4cbdae6124e681f88de2f906b68b43c210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8d0fc93bd1b4cf9447be5a5b5ac2afbfe47e0dde1a3a9d33ff70e516d3a711`

```dockerfile
```

-	Layers:
	-	`sha256:8079e9af85dfeabd62f5c4b887d79b5716c3012dfbe5f15c26dab64cffb3e276`  
		Last Modified: Tue, 30 Dec 2025 03:24:48 GMT  
		Size: 2.2 MB (2201348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5343ae4e90ed366f0b79bbc0ca856205963346b314fe25625798acb4fcb56d05`  
		Last Modified: Tue, 30 Dec 2025 03:24:49 GMT  
		Size: 9.3 KB (9319 bytes)  
		MIME: application/vnd.in-toto+json
