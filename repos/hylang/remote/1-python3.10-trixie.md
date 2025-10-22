## `hylang:1-python3.10-trixie`

```console
$ docker pull hylang@sha256:2be1246a2cbf6fe638c24bcf07c62fcb586db33a9ea32c9d73de5e34dfc32ebb
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
$ docker pull hylang@sha256:52a41e81e0044bb4b8b58bdb9a0a2f47d06b0f1e5436120470bfcb4e4140c52d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48744920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e7105bf973c3b0b6514298a245ed9c1d248852cae547c1f340e7bf92fb8536`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 19:19:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc665d66e712e17c182277008fb8820d04d1daf02ddd72dc03cad5ce61a4c92`  
		Last Modified: Tue, 21 Oct 2025 02:11:49 GMT  
		Size: 1.3 MB (1292664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e07bd32e322a19461db84fbcad96046830fff3ce826a2a25c568f1ee7097c`  
		Last Modified: Tue, 21 Oct 2025 02:11:49 GMT  
		Size: 13.8 MB (13820388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a29352df11cfa64d30061c8bd8ba24701fc8d9100bd42b62c0d0ea5047ab2b`  
		Last Modified: Tue, 21 Oct 2025 02:11:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56a1bd32435715d73769b5c36a004a0cea497ce02b515032d4db4a569b32922`  
		Last Modified: Tue, 21 Oct 2025 05:03:15 GMT  
		Size: 3.9 MB (3853694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:cec15d3a3a4a081c58f449ad828dcdaa576f116dc166b1e97d4045016bf48ad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb7c944a97fab1cc76d1274bbdf69407d6a12b9de8fd84bf625110fadcac7c3`

```dockerfile
```

-	Layers:
	-	`sha256:58eb0ce60c469810eb7a8058930461a9716ec5bd186ac4b796f7a3dbcdc68058`  
		Last Modified: Tue, 21 Oct 2025 11:18:15 GMT  
		Size: 2.2 MB (2199955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d4cd96707dcb7dae46da1961a6a41fb223e5af0ef694983a776c854d20c173f`  
		Last Modified: Tue, 21 Oct 2025 11:18:16 GMT  
		Size: 9.3 KB (9251 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; arm variant v5

```console
$ docker pull hylang@sha256:aa30c98253d20ea52f627ca34fdf36034728b900cd576531b68b2ef57278f4d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46557135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e5ac6eebe3f745e3fa4294ab224432cc5c29dcae84b6eaea7cb0ae405e99f7`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 19:19:01 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:389bac9f76fa529ccf801fd7c9cb260ecee27d208221c25004185ab22936c4d4`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 27.9 MB (27946283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef63b0e5af46cde2c0a758f830fca35ee0ddd32bbdb3701863ce229f50b92a7`  
		Last Modified: Tue, 21 Oct 2025 03:12:42 GMT  
		Size: 1.3 MB (1275585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f45ff7164ff4a3e45c5e2cee99f2e202881bb0edb7afaa540bf56cf11ee38a6`  
		Last Modified: Tue, 21 Oct 2025 03:12:42 GMT  
		Size: 13.5 MB (13481270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93edc2ce95504120f34d6f8a44e350227393278fa90a5dcc3a3e18498a2c2e19`  
		Last Modified: Tue, 21 Oct 2025 03:12:41 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defe33f73fe459df4c3e068ae3b4695dc1d161bfab41d114baed2692fdbfb974`  
		Last Modified: Tue, 21 Oct 2025 04:29:41 GMT  
		Size: 3.9 MB (3853748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:8d7ddc07c7ea9a1ee9f0568a0389457b9546ea30a9af30859563784c369456db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd9707351fc10506f573371c8cf47c6e1bb54edbb64cae87c656c65a1e54516`

```dockerfile
```

-	Layers:
	-	`sha256:5bb58aefbb8da3458a0e32d43e0358ed860997c4701abf8a88901ae50b373d39`  
		Last Modified: Tue, 21 Oct 2025 08:18:02 GMT  
		Size: 2.2 MB (2202956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da442242e3c6233fb7d05dc85d127577fab67f26937396c2599a97b4dd3cf596`  
		Last Modified: Tue, 21 Oct 2025 08:18:02 GMT  
		Size: 9.4 KB (9363 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; arm variant v7

```console
$ docker pull hylang@sha256:c1f62c1335bb4ef505ae2e21a10a2731644f7c5fd6e75d7602063ae1a5120ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44530418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dd4d66e72ea6bbbe503b4b5531a4641b860cff625ea86b97e678eb10f46c15`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 19:19:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e700df98be6e78aab9ead4375242aa7e453705fe87e3341e08715efd74a134fd`  
		Last Modified: Tue, 21 Oct 2025 03:47:31 GMT  
		Size: 1.2 MB (1248124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5e396b3dcdfb90f255e7cdf31965de0fbef7b08e087c0d5d48151bc4597544`  
		Last Modified: Tue, 21 Oct 2025 03:47:32 GMT  
		Size: 13.2 MB (13215554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af40380a2c0baebbc6926e788a8f200ff1c4cdbaee39172dc5fa69972ab5f429`  
		Last Modified: Tue, 21 Oct 2025 03:47:31 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1304a463bd16fe3826f753eec06cd273fb3dfe9a78e02b9854f63a87cdf98fe`  
		Last Modified: Tue, 21 Oct 2025 04:37:18 GMT  
		Size: 3.9 MB (3853597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:69c6fde51df86a7ce3c4f96549763161af30a388bd934ddf146610f1901d7ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a86b3425bf7b78d643e418f0f8ad3b3bdaf68be72c946730eba4c172b268e2d`

```dockerfile
```

-	Layers:
	-	`sha256:af6bf46dfc27224be39512ede112e2301f9bcd0662a580dac4553412668073b4`  
		Last Modified: Tue, 21 Oct 2025 08:18:06 GMT  
		Size: 2.2 MB (2201409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d68fc8e036b6d9503fa9a3998da00dfb579703f7cd5b2a07f2843c1e25a303f2`  
		Last Modified: Tue, 21 Oct 2025 08:18:06 GMT  
		Size: 9.4 KB (9363 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:65e71d13d91472944f75a5803e94228e16f64ebfb41ea87587c2fe9d3facc196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49044165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1294313b47c6f888b4a686ec15ed543d760eda5b9dcb5aeec4a42ef80fda6aa4`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 19:19:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c901e904088ba15fab1654f3eb8dfbab473700c84cdbb0866ce8f31b9685906d`  
		Last Modified: Tue, 21 Oct 2025 02:18:55 GMT  
		Size: 1.3 MB (1273099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90af7e2724d2ef4d898def30306b377723c0b7179ee859df1ccb41ebf99ea9c9`  
		Last Modified: Tue, 21 Oct 2025 02:18:56 GMT  
		Size: 13.8 MB (13775013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17d065df0479e9e026a501befa3200ba4c68cd46914fa6d9b20a8d275068726`  
		Last Modified: Tue, 21 Oct 2025 02:18:55 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602b1565b0df11606da9508427084d7ce1671852c1500a3f3afd2f0158ddeb7f`  
		Last Modified: Tue, 21 Oct 2025 03:24:15 GMT  
		Size: 3.9 MB (3853676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:cfb50f9297227fc4fa8935480ecdf079d297c651a89e98edfba16e1a8b83cf09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b3fe7088636ccf992142e4e50f79ddf040111067d22ebecf67c827e517f0f5`

```dockerfile
```

-	Layers:
	-	`sha256:2a24e8f4ce745be69ab260ced819d8dafbca9e253e4f3a43e6564769b3c8bab6`  
		Last Modified: Tue, 21 Oct 2025 08:21:08 GMT  
		Size: 2.2 MB (2200269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:add54e82fc7309cf5b7193470b4ceb65bd111baeb66d641252e010a230bbb748`  
		Last Modified: Tue, 21 Oct 2025 08:21:09 GMT  
		Size: 9.4 KB (9403 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; 386

```console
$ docker pull hylang@sha256:4b979c94557aa9fba6102bddfc0f9f9857d7d9032f398273f821d72221a5b9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50296823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c78909e90a3f2ad9366fad2bd04317374d92330629f0bee0445575fb2e05f0`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 19:19:01 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c16a4c4b63d084ae08c5ec6fe25ac02e7e6308f7cc9bf9261a182544050236d`  
		Last Modified: Tue, 21 Oct 2025 02:16:24 GMT  
		Size: 1.3 MB (1296585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7b6a3e637754b84c8e277c72a2ed0e55ddc846e3cfd1b920cbc1a63bd5e7cc`  
		Last Modified: Tue, 21 Oct 2025 02:16:25 GMT  
		Size: 13.9 MB (13851695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41da1154cbd82f3f3e6431eb9c9471ddd41525cf5c2eb128fffa1a473c42104e`  
		Last Modified: Tue, 21 Oct 2025 02:16:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a501891353f33fcab8fdd301c0df23b8327122dbccbe04955aaf766dec4d247d`  
		Last Modified: Tue, 21 Oct 2025 03:18:22 GMT  
		Size: 3.9 MB (3853667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:d3c9917f0fb5fe562b24d9164eb4cf843fa3293d0e3e6162a1c06bf6adbb64cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9a9ec1e214a3eeaf6b3268d51548cce317775a78f80c8c7f758c37dd1f8b32`

```dockerfile
```

-	Layers:
	-	`sha256:d1e9aef373275d1bf4e9d516e8ad545563f5d34d37d3f95bf62693ca74858656`  
		Last Modified: Tue, 21 Oct 2025 11:18:26 GMT  
		Size: 2.2 MB (2197116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:688b2d6cb24763bfc78e24ea5be11746fb236ebea736d4f08ecb1343e2932db8`  
		Last Modified: Tue, 21 Oct 2025 11:18:27 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; ppc64le

```console
$ docker pull hylang@sha256:0ad03069679d8c1ce49b1beef071f091397352a2037689c8e065e5c8efeb9282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52922851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217253b51e973f991f09171e637751ba7022d4dc30c11b4fd30c3098ecc3b1f4`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 19:19:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb558dffcc860262e2beb67e32665bd21619cba0fcdc6a241d92e98e82bc66c3`  
		Last Modified: Tue, 21 Oct 2025 12:43:45 GMT  
		Size: 1.3 MB (1320968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad07372be0406a5df1b6164ed073845d8d3df56330c88dbf4e819f12bffdd84`  
		Last Modified: Tue, 21 Oct 2025 13:52:31 GMT  
		Size: 14.1 MB (14149146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdb0554638a33c54b073eaee9c16a10c8276775a852b61321004e9850b64c3a`  
		Last Modified: Tue, 21 Oct 2025 13:52:29 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a13c135232c98bc4801ee335d3a862fddb5cef0878d596cfd9dbc2d67eb9a1`  
		Last Modified: Tue, 21 Oct 2025 22:04:33 GMT  
		Size: 3.9 MB (3853970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:dad2b5ae3e87fb29b9ea291bb76f3db81aa39505b9a0e26536b36b206b02d994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9419fcf9fc9217a4affae208a67352db323253c6edfad5389ed5a64ec8395cd`

```dockerfile
```

-	Layers:
	-	`sha256:e7e3f59af24985a8cf0d50f6077bac58d736456ac5f8ce82b34236849f371d2f`  
		Last Modified: Tue, 21 Oct 2025 23:17:54 GMT  
		Size: 2.2 MB (2203546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d4d86c9f735c378920bd6aa8c8c7380f8ff63db179cf5a2d15d01982d7c09c1`  
		Last Modified: Tue, 21 Oct 2025 23:17:55 GMT  
		Size: 9.3 KB (9319 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; riscv64

```console
$ docker pull hylang@sha256:f5734d04441c11c9ff18bdaba3434d3ab5dd8022f0ee9f60fd210779d12209c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49744752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be1dc68c741ded7b4fd547e71a910d011364e5a901c7b2bc587fa1d35d79899`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769d6987bfd0545096d164e9a80591a9443ae52e2ff80e6f38eb2fe7fb5b3983`  
		Last Modified: Mon, 13 Oct 2025 17:20:38 GMT  
		Size: 3.9 MB (3871099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8739d1555af86fe84a225cddd2fe3f25f44738c5899610b3a562cbfaedf74828`  
		Last Modified: Tue, 14 Oct 2025 09:00:32 GMT  
		Size: 13.7 MB (13743454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da3a8aa006cb214f7b3cc92e2f743d47e3cb9d89149cdf016be39a07f531d77`  
		Last Modified: Tue, 14 Oct 2025 09:00:31 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5067283cfe8c952c8a3b0fa828865f651d78255f32522ed5ac991050589b42e`  
		Last Modified: Wed, 15 Oct 2025 19:05:12 GMT  
		Size: 3.9 MB (3854447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:33ce48aa8bc679eb6049d4de4b254afcac3cabf7195a45f845add01e230437ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17a179ff2aad405e865d44de89e807b914816f8f4e8749dba81e228291ad7063`

```dockerfile
```

-	Layers:
	-	`sha256:c0e5ed3634d33465c9226658f6436772c7e9971d831d178c3112ea7e4c62ab7d`  
		Last Modified: Wed, 15 Oct 2025 20:17:52 GMT  
		Size: 2.2 MB (2193917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86cba9dfff78526322407c113da94059e5999a3d30a46f606d1af9deb5ae0217`  
		Last Modified: Wed, 15 Oct 2025 20:17:53 GMT  
		Size: 9.3 KB (9318 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; s390x

```console
$ docker pull hylang@sha256:8da17043d56ee48f8b57286cd5f2988e1c9bef65d7ad74118b3e1dd376f882d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51829206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17b18eaf8d2e4ae963ca328335d69314bd33aa97fcac9ba86ab0bac8621f3b1`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706cd0d1bb40e49288b230ac475ead8382abad5121ddda932fdf1897981d475c`  
		Last Modified: Tue, 30 Sep 2025 12:24:45 GMT  
		Size: 1.3 MB (1305117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c428fbde5c07af4958f728e340a7a5612739ec20ddf7f265d0855dc2aea70d`  
		Last Modified: Fri, 10 Oct 2025 04:33:03 GMT  
		Size: 16.8 MB (16832896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e492d6259761063caf486867ddc5d15898db1ed8417d34d7319b4eb72e3befe2`  
		Last Modified: Fri, 10 Oct 2025 04:33:02 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de144df2a850711eb455c1a9d8f79fe675f75a35eb6ac62adb2da447f1a42f8`  
		Last Modified: Fri, 10 Oct 2025 05:48:21 GMT  
		Size: 3.9 MB (3853713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:d680b708f582392acf1befdaa5508f80dc8324234ca5602bbea2ee82a5e20f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7a57daf54356da6da8a85e4203756e84460b6eb0c210b1177a3ea13cdd3aa0`

```dockerfile
```

-	Layers:
	-	`sha256:eba14df145c55ad3a25430ed96ab26dc20da4b3a14a356de02c3cd2b589df621`  
		Last Modified: Fri, 10 Oct 2025 08:17:47 GMT  
		Size: 2.2 MB (2201394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8067dcf07c8a88b5d80af77710292ef1d37ad3ef7b3cb4d7a23b1b3131141b6`  
		Last Modified: Fri, 10 Oct 2025 08:17:48 GMT  
		Size: 9.2 KB (9250 bytes)  
		MIME: application/vnd.in-toto+json
