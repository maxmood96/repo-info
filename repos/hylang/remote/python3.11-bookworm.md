## `hylang:python3.11-bookworm`

```console
$ docker pull hylang@sha256:655989e66eee05373b24bf6b5be76b794bbfde12de76a3f011855557d998c1ca
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

### `hylang:python3.11-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:8da1c37d63022de9df4f3b0cf3140858a1a1eacaf3785532702a679729fcc6d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54159342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4c2bfa083c4484ce9952f91b60fb16d0c1b90271ed2dca56a530f35c60e56f`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Jun 2025 23:02:53 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 23:02:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_VERSION=3.11.13
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_SHA256=8fb5f9fbc7609fa822cb31549884575db7fd9657cbffb89510b5d7975963a83a
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799440a7bae7c08a5fe9d9e5a1ccd72fc3cbf9d85fa4be450e12b8550175c620`  
		Last Modified: Tue, 10 Jun 2025 23:57:54 GMT  
		Size: 3.5 MB (3511866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9596beeb5a6dc0950529870568799000e8d73fb678969ac2f485005cd5da1087`  
		Last Modified: Tue, 10 Jun 2025 23:57:55 GMT  
		Size: 16.2 MB (16209133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15658014cd85cd0d8b913d50b4388228aebcf0437d43cfb37e8a5177e8b2bcf8`  
		Last Modified: Tue, 10 Jun 2025 23:57:54 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e7710c449a2eb0bcad8f6cc096b6e621c954c541b433dd38f90163604a5e08`  
		Last Modified: Wed, 11 Jun 2025 12:17:52 GMT  
		Size: 6.2 MB (6207966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:a72c79d7aed135c265fd4cb86d9af390cc4f367ca1d1fa8d6f1b7fc10e59472f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61589e6353da0a89f8183f75e9d728ddb72e2c9feb937929c6c3bb170c447817`

```dockerfile
```

-	Layers:
	-	`sha256:9d7fd5b7e1ba1993eea318c2328c30c92626523107030154f69099d313dea2f9`  
		Last Modified: Wed, 11 Jun 2025 02:18:42 GMT  
		Size: 2.6 MB (2580578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d847a32ccb31d47052e93fbb6fc7796e2d18e3f96a44a261fbc503531ddad0`  
		Last Modified: Wed, 11 Jun 2025 02:18:43 GMT  
		Size: 9.3 KB (9277 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:555078e567ade105e3f08e9a2474211a30bc5727c6e882c8e80af3ee0bb3b0f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50674210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64adaab118af5e0dd23b5230e252ca7bc36d2699c81705985a3d2fbf9694a4a4`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Jun 2025 23:02:53 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 23:02:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_VERSION=3.11.13
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_SHA256=8fb5f9fbc7609fa822cb31549884575db7fd9657cbffb89510b5d7975963a83a
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274c2a54502ea49d4bc612db2f6aba89371e788122aac5ec67337a79dd5996c1`  
		Last Modified: Wed, 11 Jun 2025 05:24:38 GMT  
		Size: 3.1 MB (3085118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf19daace2a599ecf075902640246a82c575edba59b00c5b15478ace2e0e4977`  
		Last Modified: Wed, 11 Jun 2025 09:09:57 GMT  
		Size: 15.6 MB (15618500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363d24d7b0b0bf873cd3eeaf39e2216bb8154e4489a5d5554c07d5c41950ef81`  
		Last Modified: Wed, 11 Jun 2025 05:42:26 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8d67042a75baa057f28af04666e98442671ff9c04803a1e7865ddb1178948d`  
		Last Modified: Wed, 11 Jun 2025 09:21:10 GMT  
		Size: 6.2 MB (6207946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:c21bf3a9c057d1a467f7f64a7b660d469c5ec07171f756151dab6a38db768684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2593815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b52bd38e0d04343ee1e5a68ac03b549dc8b7cba4eabad68c44064efe96a695`

```dockerfile
```

-	Layers:
	-	`sha256:0a791544ef1641eb5b0df4409de725560926bb2ffe806f6ca2e0fc9db4d0365b`  
		Last Modified: Wed, 11 Jun 2025 11:18:03 GMT  
		Size: 2.6 MB (2584430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cbbc2c776648e0185f555926cf96205fde92f2e3a8957fbb464f2fc14ec430c`  
		Last Modified: Wed, 11 Jun 2025 11:18:04 GMT  
		Size: 9.4 KB (9385 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:69cc9b4c6098db06cb614f490ace0d254e618afe402ef8c198c35696b0abb404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48264758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b9f906dae3d718b4e58f083327e8e88e63e49bc598e6a327f6b5b2755826a2`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Jun 2025 23:02:53 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 23:02:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_VERSION=3.11.13
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_SHA256=8fb5f9fbc7609fa822cb31549884575db7fd9657cbffb89510b5d7975963a83a
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5212070728c80d1e5fe75008b02832a4de7cb44150b43673dd127709d503f47f`  
		Last Modified: Wed, 11 Jun 2025 08:46:58 GMT  
		Size: 2.9 MB (2919653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6cbdd08d9ca76ff1953736ff38d940532608013450dd1d8a55637850907b4f`  
		Last Modified: Wed, 11 Jun 2025 09:27:42 GMT  
		Size: 15.2 MB (15198019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b15c5779a9b8a0d3710335b95c03f0c4342a27dcfe72670d58a8d6a32b74cb1`  
		Last Modified: Wed, 11 Jun 2025 09:27:38 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a09d43159d34f435fbd72dfeeea78f2509d35efa44c220978290fc0cab29b9`  
		Last Modified: Wed, 11 Jun 2025 15:56:55 GMT  
		Size: 6.2 MB (6208092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:d3d7b9a35997a0dfd18926907dada7212ea6f0226ed748ab6c0955d1fe605ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2592264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936ef9e7d656ca351eac554e360e04f600ffb0a2632896eb1647609753bb116d`

```dockerfile
```

-	Layers:
	-	`sha256:cb46e0ab281dd2ddd71a75e468c707caa8b3377e9579905dcbdcbd29143c553a`  
		Last Modified: Wed, 11 Jun 2025 17:18:05 GMT  
		Size: 2.6 MB (2582879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5af8725647933185e87cf50094868c628ca29689dcda582b5182c05d1ffe04b`  
		Last Modified: Wed, 11 Jun 2025 17:18:05 GMT  
		Size: 9.4 KB (9385 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:31bab15bf7bfa1b352eb8904ffa6497af86763d6c636d1c153f1bf488199a8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53756026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b162b2eda6f78bda7984a7c60d5235e5b7c0d5d3b58f05e6ef8e97ff12a34065`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Jun 2025 23:02:53 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 23:02:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_VERSION=3.11.13
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_SHA256=8fb5f9fbc7609fa822cb31549884575db7fd9657cbffb89510b5d7975963a83a
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6939e8b629d325c16aec26f961a50f26060da987c2aea1eb86a3e7e7e89e9cbd`  
		Last Modified: Wed, 11 Jun 2025 06:43:36 GMT  
		Size: 3.3 MB (3333525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8c9691b884e6163a21e72a30beeeadabe83823b004243097db1e05bdffaef0`  
		Last Modified: Wed, 11 Jun 2025 08:08:01 GMT  
		Size: 16.1 MB (16136606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4185d6dac69afbc3f5b53ff9609983087cfdcee9bb416dec31be456543be16d5`  
		Last Modified: Wed, 11 Jun 2025 06:43:44 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bc0a241ad82552cf2c285f69d8e6e8344716a9eb9434841c54b57a8e2b9553`  
		Last Modified: Wed, 11 Jun 2025 13:17:22 GMT  
		Size: 6.2 MB (6207972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:34c2c34c895c2a4c34d3170d327a293afc4deb60b9be323ba0ef2232456c56b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2590328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5f105a38c6245d815a156f0b93c97b77e7536d21c2450c4956d2d6b202561f`

```dockerfile
```

-	Layers:
	-	`sha256:3e79d77dc2126dcc00587966623fba4a49bc8616b0683ba1a9bea48c0ce9a498`  
		Last Modified: Wed, 11 Jun 2025 14:18:30 GMT  
		Size: 2.6 MB (2580899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5414a2484067ab6d8610adcc56cfbf28a4af62d1fddbb363ee506d1de366eccb`  
		Last Modified: Wed, 11 Jun 2025 14:18:31 GMT  
		Size: 9.4 KB (9429 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:88836ea6b7470257ce19e24337766ff209c7ac0f6be3c2fb4487251ab8f99bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.4 MB (55371486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2900580b51a42f399a54eacaed3d5531041e148937e5528edffc5af17369647b`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Jun 2025 23:02:53 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 23:02:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_VERSION=3.11.13
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_SHA256=8fb5f9fbc7609fa822cb31549884575db7fd9657cbffb89510b5d7975963a83a
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acf364ff01c24636114073de7c1a221476bc20db3f66aa570f8c912ed82dcdf`  
		Last Modified: Tue, 10 Jun 2025 23:53:07 GMT  
		Size: 3.5 MB (3511117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c33aa3057a6190b16731a868653a60831c7f2b4f7b71bb374839c0697902ce`  
		Last Modified: Tue, 10 Jun 2025 23:53:11 GMT  
		Size: 16.4 MB (16439840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e16f0999cb1c44c1efb40ea27f24585781f93af530f71bb92cfe56b52823cd1`  
		Last Modified: Tue, 10 Jun 2025 23:53:08 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1bd19a752511b6cd3adf784ef6c6e0dd6e555981bcee4d7dfa4bda35e0e039`  
		Last Modified: Wed, 11 Jun 2025 01:15:46 GMT  
		Size: 6.2 MB (6207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:407ddaf127013c88972b0e2bea29034932113e09156fe1ce62b0304fa4ca7867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2586934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ea125880c710f5b3b1973eff4db157fd210a201258805e2796eea352a8282d`

```dockerfile
```

-	Layers:
	-	`sha256:5a6b9c30bd493211eaeb2d1f60a83aaf51839553bac2c3e71e9888ec3bdbb5f2`  
		Last Modified: Wed, 11 Jun 2025 02:19:06 GMT  
		Size: 2.6 MB (2577709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:428c6cb80f91f3295eff9137320f60be11187b8ecd03f99204344d547011fe63`  
		Last Modified: Wed, 11 Jun 2025 02:19:07 GMT  
		Size: 9.2 KB (9225 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:c5f44106f4a584f7e157b195cfc5ae0f65934046d0518674f23a21273b3a7697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58836337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5910e5292e2213c07d9a26b5d6d6d9e619225235aa8f8664fad938381bc17ba3`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Jun 2025 23:02:53 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 23:02:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_VERSION=3.11.13
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_SHA256=8fb5f9fbc7609fa822cb31549884575db7fd9657cbffb89510b5d7975963a83a
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d192f9d3086312398012c1f3f413d5ab311dee770705337f38b001ad5e81de79`  
		Last Modified: Wed, 11 Jun 2025 07:02:26 GMT  
		Size: 3.7 MB (3716112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d248015f1764d7cafe6656fea71019f74bf9b0d495be1b95c21323d4fc7e97`  
		Last Modified: Wed, 11 Jun 2025 09:10:33 GMT  
		Size: 16.8 MB (16839051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a62a2ac54bfc3560002fb6002e984b3c5f3e247aeb9a47d0dd8c8de26dab7b`  
		Last Modified: Wed, 11 Jun 2025 07:27:04 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0610be32e71a00f25a575e1ca0610282b4b6cb66b46d040097d10a04bfd04937`  
		Last Modified: Wed, 11 Jun 2025 17:25:23 GMT  
		Size: 6.2 MB (6208129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:942ea7f6d333e41d73b6d5e2f2169de06431a0d9a137d807bb811c6802582cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2594453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcaf03b56426d1d573caa00c52784c724457565f6b2e77463d84a0d48bf82394`

```dockerfile
```

-	Layers:
	-	`sha256:ca1e9b362024e11f27233c5cf56a4c59b882765404a5aefad660b98ace992a38`  
		Last Modified: Wed, 11 Jun 2025 20:18:13 GMT  
		Size: 2.6 MB (2585108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c32383ff2eb6e029490fd8ebd74d48f788eef30d524cb4c474e83f7bbbc578a5`  
		Last Modified: Wed, 11 Jun 2025 20:18:14 GMT  
		Size: 9.3 KB (9345 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:945ad31bccd481dc76f7b92f0e8f9260c93f1ba9aa6a1504d1791e30ceaa6e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52313286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bb2ff577b273046790fe6b1903e8dcf26fba33f80a771e88a02247a58753f3`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Jun 2025 23:02:53 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 23:02:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_VERSION=3.11.13
# Tue, 03 Jun 2025 23:02:53 GMT
ENV PYTHON_SHA256=8fb5f9fbc7609fa822cb31549884575db7fd9657cbffb89510b5d7975963a83a
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 23:02:53 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555924c108a5b072f3541c3f966d0f03ce4a6761b6ac81f9f0dc08ab31745053`  
		Last Modified: Wed, 11 Jun 2025 05:00:38 GMT  
		Size: 3.2 MB (3175305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c416563170f783e366eb770e73c280d8cb694cebac6a6349d68cb7bdade86eb9`  
		Last Modified: Wed, 11 Jun 2025 06:12:07 GMT  
		Size: 16.0 MB (16041789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccd28d34564bece2f2617dbbcd0f509e551149fac1bd0c25423a9d0faad90db`  
		Last Modified: Wed, 11 Jun 2025 05:12:36 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38442ef2edbb47acf8ac54d3ec9c62917ba3d77e5c6df9ab8d472e85a2d9decf`  
		Last Modified: Wed, 11 Jun 2025 09:09:39 GMT  
		Size: 6.2 MB (6208089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:bb40d099d417926b73ebdec9d72e4b06c3b35ed601262db6da8791ede2f7c29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2586671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cfe9cbc65464516a8b74e7694841714178a79df6e1ab09dafc54da659ad82e3`

```dockerfile
```

-	Layers:
	-	`sha256:c65293d7dc7745ab61663dd9a6d2cc2be75e1544ffacc7c8d3c54e81fbcfe4d7`  
		Last Modified: Wed, 11 Jun 2025 11:18:18 GMT  
		Size: 2.6 MB (2577394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1de33ba21dd380bff084f73a0f8ca4186d9f2fac0b7c4aad5a5aaa63e0e542ba`  
		Last Modified: Wed, 11 Jun 2025 11:18:19 GMT  
		Size: 9.3 KB (9277 bytes)  
		MIME: application/vnd.in-toto+json
