## `hylang:python3.12`

```console
$ docker pull hylang@sha256:1010636b07cdb67ef431037823be7629945cb797185cd06092c3390e2ec7062f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 17
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
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `hylang:python3.12` - linux; amd64

```console
$ docker pull hylang@sha256:a0d1c61c614549bec8ec09d07586c8e9da5a34b25dd1b4e284ddbaca02054467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51016255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99e1f375940c27805682f0371cad6e3bad61e9db0eba6f42e2be99008b57204`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 21:54:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 21:54:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_VERSION=3.12.9
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_SHA256=7220835d9f90b37c006e9842a8dff4580aaca4318674f947302b8d28f3f81112
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9612276b664ecdb44eeeb2891cad88cfd0d48cde3b3bb3d34a377367b2cf1b3`  
		Last Modified: Tue, 08 Apr 2025 01:44:15 GMT  
		Size: 3.5 MB (3511489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b365a43716b1cc8103bfbf60883d4f6b8ff5e1a3fd96794e8158b5ff1a8cc0aa`  
		Last Modified: Tue, 08 Apr 2025 01:44:15 GMT  
		Size: 13.7 MB (13652946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e639439a27133b1b01ef0ea874bb7c33444aed60b797320860c31d1c05a3a3d3`  
		Last Modified: Tue, 08 Apr 2025 01:44:15 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f052b181a5570db0fc26daeff394753ecc0d9790f98ac2f8e0d8fad22508b4b`  
		Last Modified: Tue, 08 Apr 2025 02:22:06 GMT  
		Size: 5.6 MB (5624311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:f7e80ca23c29354ffdfc73c0ecf3ef597a7f60f4dc828332d10b3eb95456c569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e78a741c47e01c1e716372cf50f25ddcdc8d2cf79de65dedacacd8111546f65`

```dockerfile
```

-	Layers:
	-	`sha256:c7f6e38e9ed80e69363e490f4950de5601006a118bf11ced7f570bf484a820cd`  
		Last Modified: Tue, 08 Apr 2025 02:22:06 GMT  
		Size: 2.5 MB (2461130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f40214d3f45218a178d1220f6f2e460968b903a2779eda19c4cde68b67757c3`  
		Last Modified: Tue, 08 Apr 2025 02:22:06 GMT  
		Size: 9.3 KB (9276 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12` - linux; arm variant v5

```console
$ docker pull hylang@sha256:73f4d2b0bccbd01ae04f3465645a1fc34208f5f27b70a31381d4b6a7975a3625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47507126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee96e7a16dcf870966d03fa6bd4ab78351e0e1229a88c256693b3de161e9c29`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 21:54:55 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 21:54:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_VERSION=3.12.9
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_SHA256=7220835d9f90b37c006e9842a8dff4580aaca4318674f947302b8d28f3f81112
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
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
	-	`sha256:87c352465466fcf04c9686fee29c2541af5fc39172801545bb24d9faa8cdeabb`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 25.7 MB (25735853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd964f1cade853cbe41fbbe453799587896be06949cdfdeb24da63c12efbe33c`  
		Last Modified: Tue, 18 Mar 2025 01:35:37 GMT  
		Size: 3.1 MB (3082334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a68359309999894d9743402902a5c2dc3b0becc3caa33349ac184387a0325`  
		Last Modified: Tue, 18 Mar 2025 02:22:55 GMT  
		Size: 13.1 MB (13067279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96b339897554d30595141f578eea32f63ebb76773b50524922bae43e55d2b31`  
		Last Modified: Tue, 18 Mar 2025 02:22:55 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3639062d8ccb528ccc73e998cd57080030f9ab767d95cd9e63cc25846496e6`  
		Last Modified: Wed, 19 Mar 2025 23:06:21 GMT  
		Size: 5.6 MB (5621410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:90f204548e1a6b02f2e0bb5fdd15066d80ba84d02b2fcfa78ab62bcc86145dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60c29b2bb75b002ef8ee75311f43eb8dac71f1aa0c30eb9ccb418a5737327ab`

```dockerfile
```

-	Layers:
	-	`sha256:fcbf6c42f17bbe780b3002666b2020abfbb88d608d085612fd011e0c11e00105`  
		Last Modified: Wed, 19 Mar 2025 23:06:21 GMT  
		Size: 2.5 MB (2463338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d5476c313495f582414c9cd561df797bf59d771fdd4e9fea01fa72d8408e3f1`  
		Last Modified: Wed, 19 Mar 2025 23:06:20 GMT  
		Size: 9.4 KB (9384 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12` - linux; arm variant v7

```console
$ docker pull hylang@sha256:98b3d959763435fb6a669d2c3ffababa2dcccc54e9e71f152cd9b8b5c14001b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45110845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63582a2aba2012ef2351b001d5a6aa838cf9a67ea379ee9d58307a59e27ab62`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 21:54:55 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 21:54:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_VERSION=3.12.9
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_SHA256=7220835d9f90b37c006e9842a8dff4580aaca4318674f947302b8d28f3f81112
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
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
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950e6c7bb7e40a18b5b42fd10ae4ac2dec09ed9938b71640f067f59a58de9e56`  
		Last Modified: Mon, 17 Mar 2025 23:54:48 GMT  
		Size: 2.9 MB (2914816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f247e0b80fabf7637814fb6577d94c62b63fff3a37d449a0ef8fa5c327dad0`  
		Last Modified: Tue, 18 Mar 2025 03:06:39 GMT  
		Size: 12.7 MB (12659337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdf6eff1799dbf4d8b1e8b84a8e98432ba2bf3891c40381f75a7074868f9071`  
		Last Modified: Tue, 18 Mar 2025 03:06:37 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fabdc35fe071d1b66eb684a4d0a25c90f4507c48d9c5ff50dd9845daa850779`  
		Last Modified: Wed, 19 Mar 2025 23:30:05 GMT  
		Size: 5.6 MB (5621354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:ac903609b9452288a5cf7c0b6390560b36bc11bfea07d0a14bd814bc6b3b18e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fbf21d009e1a1a7a581c94d9ce69292f3d02c97139b21915f512b802599602a`

```dockerfile
```

-	Layers:
	-	`sha256:70f85fc49ed3d5b73c3f4e38a787b1087a93923510dde3a7438b42a8b1266167`  
		Last Modified: Wed, 19 Mar 2025 23:30:05 GMT  
		Size: 2.5 MB (2462095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b461c137a37c2c2cc2cf88414eaf1456a451ab18aab9bc383f74f9e91b65c1b`  
		Last Modified: Wed, 19 Mar 2025 23:30:04 GMT  
		Size: 9.4 KB (9383 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:0e2a2b112dfe4f539da723a4f245c5aa93a92e586988142f971c28e69a3c263b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50563933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a20bbcc96541bcade57c892183b0ecdf2f6e6a52173a8e1bec8cf5f723bcebc`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 21:54:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 21:54:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_VERSION=3.12.9
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_SHA256=7220835d9f90b37c006e9842a8dff4580aaca4318674f947302b8d28f3f81112
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f529d1f5c642f942a2f18a72c6b14f378767cdf3f66131f04497701e8361712`  
		Last Modified: Tue, 18 Mar 2025 00:53:49 GMT  
		Size: 3.3 MB (3332047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8de0b27f0d9f5cf579e907dcfbf973bef045401fadcaf904919baee9c911d7`  
		Last Modified: Tue, 18 Mar 2025 01:40:22 GMT  
		Size: 13.6 MB (13566241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442a320f7d25402433ed0567151a9841e2000712cd94c22d2310b39e72899176`  
		Last Modified: Tue, 18 Mar 2025 01:40:21 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cff367ee0903f9a32c68a5fd5b161d621818b7ff7b02d81b740068a115074b`  
		Last Modified: Wed, 19 Mar 2025 23:17:07 GMT  
		Size: 5.6 MB (5621358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:d4a119810bb4b0e2c66ac762cbee60c0506b640499332ccd6b5e98fc859e59b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90966759a2dfbfe70567fc578b5981fa045140314c3a566f83f3de3b6a1ecb4f`

```dockerfile
```

-	Layers:
	-	`sha256:849c89ed2dbb1619380ff08f722a9bc2756442cf1eecf7172cf0244c88a2469a`  
		Last Modified: Wed, 19 Mar 2025 23:17:07 GMT  
		Size: 2.5 MB (2460115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3146d0e4979f9096ea61f0a986ead9d3d067a03ab298e5e9c44691526a29aa73`  
		Last Modified: Wed, 19 Mar 2025 23:17:07 GMT  
		Size: 9.4 KB (9428 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12` - linux; 386

```console
$ docker pull hylang@sha256:28e570ae3a59e566078b748bdaedecefd6cff2da081b2ee54d524c46fe7b628b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52258051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e17e79f456f8e8deec516c24bb3356daf9e719f761ada07f13899c10e2a1e0`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 21:54:55 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 21:54:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_VERSION=3.12.9
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_SHA256=7220835d9f90b37c006e9842a8dff4580aaca4318674f947302b8d28f3f81112
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
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
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9cb20ae44e6296f198b3a66f5e49f9ce9639618b99b718d404aa14dbc3bbb3`  
		Last Modified: Tue, 08 Apr 2025 01:52:11 GMT  
		Size: 3.5 MB (3509839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2c60a20d64354bd3a8804ba6cd529ced847604ccc91e5b7540c6c60cc4b03b`  
		Last Modified: Tue, 08 Apr 2025 01:52:11 GMT  
		Size: 13.9 MB (13912996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1132f66cbbcdba112dab216352acbda1c44d0d710cb0a5e3344468edcf25d4`  
		Last Modified: Tue, 08 Apr 2025 01:52:10 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db750f13db16120aeeefd6678e48333e2065009fafc02a82e4ba00eda55abbba`  
		Last Modified: Tue, 08 Apr 2025 02:22:45 GMT  
		Size: 5.6 MB (5624235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:9a29613968a630f8df83896290ecaa5a63e4e5b41beb4c3160c5465c73116935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7079385951dc4a8c81569202450e41a0ce6a344a0b2279ee83f66d92e0c0bded`

```dockerfile
```

-	Layers:
	-	`sha256:b2896112ec5bc0f5a60ff5e8d0504e0010d979d4775bdfce8e80b7c8ed32af3f`  
		Last Modified: Tue, 08 Apr 2025 02:22:45 GMT  
		Size: 2.5 MB (2458210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca365a45fe884fac976407d6e6748cda264d458cee02eb649d0687526b97f52f`  
		Last Modified: Tue, 08 Apr 2025 02:22:45 GMT  
		Size: 9.2 KB (9223 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12` - linux; ppc64le

```console
$ docker pull hylang@sha256:5e87047227c5208e7a73b900cf549587652f03bcb160e6f67929f81d489fda13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55737079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a3cc6d403b729dea3e7500ac158ad0ab0c5dffa758326910da80d9daf036da`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 21:54:55 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 21:54:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_VERSION=3.12.9
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_SHA256=7220835d9f90b37c006e9842a8dff4580aaca4318674f947302b8d28f3f81112
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
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
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72226155cfbc58eb5364a0683816d321a0bbd79e75f5339e9a5afab1e8ce15e`  
		Last Modified: Tue, 18 Mar 2025 00:41:41 GMT  
		Size: 3.7 MB (3713730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47b69dcff0cf02abf54a6ebfb78757260fc876851f39deb1ac87ceb06231fb4`  
		Last Modified: Tue, 18 Mar 2025 01:33:25 GMT  
		Size: 14.4 MB (14353990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee12c74c40c8e0b5b31a8e967eacf091ef183df49271bae1acc6c68bb882ace`  
		Last Modified: Tue, 18 Mar 2025 01:33:24 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13174f42a1a6029f668f68b934da84852e3d6ff3883cc2477cbe1dda807f5db4`  
		Last Modified: Wed, 19 Mar 2025 23:23:55 GMT  
		Size: 5.6 MB (5621295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:66fa03677c170ea98575c3d1221a3b7c076710150ba84e5d5bf0e54a649935aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2473553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238295ddf467003399d025efd435563aa38a3281b609b4359f698d9bd848707a`

```dockerfile
```

-	Layers:
	-	`sha256:86c7e36758ab00fd8a03a4f11989c92e3dc7daa76124fdcb17bee26be4f15ee1`  
		Last Modified: Wed, 19 Mar 2025 23:23:54 GMT  
		Size: 2.5 MB (2464210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:982e6c72f9e422113ba39294df8bcee8562effada05908edca3f5954b3a41eab`  
		Last Modified: Wed, 19 Mar 2025 23:23:54 GMT  
		Size: 9.3 KB (9343 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12` - linux; s390x

```console
$ docker pull hylang@sha256:c5b094c97c55956f70ba8092245a688cc1f3f482cc122d8007fa022d663e4c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49171859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e595e2f8a5b789d00295ec683122d8f4adb57904b5a8c20ccd0d1bdd6931415`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 21:54:55 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 21:54:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_VERSION=3.12.9
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_SHA256=7220835d9f90b37c006e9842a8dff4580aaca4318674f947302b8d28f3f81112
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
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
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f110cc88d649be2edbbbff23a20b329274e87b9a332feb5da0d2a129b68ad352`  
		Last Modified: Tue, 18 Mar 2025 00:04:04 GMT  
		Size: 3.2 MB (3173191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d41dcd647bf21d02edc06f1464583916b0a598fb28fd34841dcb4edb54743bf`  
		Last Modified: Tue, 18 Mar 2025 05:20:27 GMT  
		Size: 13.5 MB (13516217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea780b239a2134c4b11156951e6ceaebec0177abbe227dafdbb1f734128f8ae`  
		Last Modified: Tue, 18 Mar 2025 05:20:26 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00f6088d7dd4e6cc03749b447e495b7c7fd9571df672e394e2965035fec69a5`  
		Last Modified: Wed, 19 Mar 2025 23:46:51 GMT  
		Size: 5.6 MB (5621142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:7b3a412b557c0a621189ee5f1d9a9a1e65619194582dcd65afd3f6033be55733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffbf93b4ac46347f5918c304e23cfa02ec667049894ef38eb562b6f3dddb6fe`

```dockerfile
```

-	Layers:
	-	`sha256:f403aa89641688d84d90d53eb51b2f04ee76c4c399e3f2a7c55bcbf5643ec80b`  
		Last Modified: Wed, 19 Mar 2025 23:46:51 GMT  
		Size: 2.5 MB (2459502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43ce6066cd2b8a4a693bef0b888dfc5acc14f225abeaf43716261bfc868e77bd`  
		Last Modified: Wed, 19 Mar 2025 23:46:51 GMT  
		Size: 9.3 KB (9276 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12` - windows version 10.0.26100.3476; amd64

```console
$ docker pull hylang@sha256:30b6d286471c67d404835315b9cae46b5bfeacd6738892e9813079e71195d7e8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2977425519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ec2dab804cde36fb62e8066522c7226eee88d59a6b28ed53fc320855889b1f`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:48:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:48:19 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 12 Mar 2025 18:48:20 GMT
ENV PYTHON_VERSION=3.12.9
# Wed, 12 Mar 2025 18:48:21 GMT
ENV PYTHON_SHA256=2a52993092a19cfdffe126e2eeac46a4265e25705614546604ad44988e040c0f
# Wed, 12 Mar 2025 18:48:59 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:48:59 GMT
CMD ["python"]
# Wed, 19 Mar 2025 23:05:20 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 23:05:22 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 23:06:01 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 19 Mar 2025 23:06:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6ab578ec8491b47ec39e11a79eeac738d23b741f5f2d9480e6f8f35366e9c8`  
		Last Modified: Wed, 12 Mar 2025 18:49:05 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095ddf14630b8b7dcff9dbdf09047657aa0f426431be631646cf7a5f04d5b3cc`  
		Last Modified: Wed, 12 Mar 2025 18:49:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6732778a9d15b5ceedc87d2fd5974a16ecc0f3f3aba789df74feeb38c278b2`  
		Last Modified: Wed, 12 Mar 2025 18:49:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab72a92e0ac0561e7ecf182a29d3bd6a8fb17976e172558e51a5fd99ac666fe`  
		Last Modified: Wed, 12 Mar 2025 18:49:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48feb201ade569bac5347a5e18f93cb3c2392d976e9a90a2fdbf31fec8f5557e`  
		Last Modified: Wed, 12 Mar 2025 18:49:09 GMT  
		Size: 60.1 MB (60096959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512c0c087e203eae3cbd53618793e3bc1ce757df8be0d04c962dc392579b9e55`  
		Last Modified: Wed, 12 Mar 2025 18:49:03 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415436b4e30d51281adffbdd9984c4042ec10a08c1ccf0649d86ec8e29b691d3`  
		Last Modified: Wed, 19 Mar 2025 23:06:06 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8141103a38520bae936eda5e70561cc7845328ee46a1f3ebb166a8f013ed4bfa`  
		Last Modified: Wed, 19 Mar 2025 23:06:06 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eabeb709d83505f74f886bd5b526b9f18e66f94e300d9a53bf3a9530319b330`  
		Last Modified: Wed, 19 Mar 2025 23:06:07 GMT  
		Size: 8.7 MB (8670321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea7f874de3cf7a9911c641bc342f73efe32cb27a08aac8ae7ad7e0b9f116e63`  
		Last Modified: Wed, 19 Mar 2025 23:06:06 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.12` - windows version 10.0.20348.3328; amd64

```console
$ docker pull hylang@sha256:dfab68e730502665e186f7665562c68cb946478073f07f582087504dd8191142
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338434036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2bb5342fd8c72103a7e05d5a5eb3633a47950e5b1a51607fee7e25b7fc2c94`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:54:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:54:44 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 12 Mar 2025 18:54:45 GMT
ENV PYTHON_VERSION=3.12.9
# Wed, 12 Mar 2025 18:54:46 GMT
ENV PYTHON_SHA256=2a52993092a19cfdffe126e2eeac46a4265e25705614546604ad44988e040c0f
# Wed, 12 Mar 2025 18:55:31 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:55:32 GMT
CMD ["python"]
# Wed, 19 Mar 2025 23:07:57 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 23:07:58 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 23:08:33 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 19 Mar 2025 23:08:33 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2992cfee4a8a03d26a5f52f0f69acafa648b5757d143d21d98522c887d07c449`  
		Last Modified: Wed, 12 Mar 2025 18:55:35 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f331a3ba5eb9785c558490c986f306f28f3c3385ccac3752b4f053e583a253d`  
		Last Modified: Wed, 12 Mar 2025 18:55:34 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246785186c2ea9d38a2bf7766b1f0a19c5803bb00b953725e1ac7fa17a9aae27`  
		Last Modified: Wed, 12 Mar 2025 18:55:34 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdedecadbaca5b44e37bb50483c44e212efc7b64b5251ddc36c1286354285d3`  
		Last Modified: Wed, 12 Mar 2025 18:55:34 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a043e0a111b1a6b32380df89edc23d32c905c60a14e37372bc9f0088e28e35`  
		Last Modified: Wed, 12 Mar 2025 18:55:39 GMT  
		Size: 59.9 MB (59941957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980de137b96e235773fb475806933aec82fb16e19a7a5b5193ff374c70372e4c`  
		Last Modified: Wed, 12 Mar 2025 18:55:34 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140431ffce7f5993fbe2b40f1dee8e914f1977b4050055aba82dbcb229a644ea`  
		Last Modified: Wed, 19 Mar 2025 23:08:38 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d4af7138df77f57a99d5e020b3cc7b484fc7c60e1284c2b70d17307bfb2f2a`  
		Last Modified: Wed, 19 Mar 2025 23:08:38 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43fab148c3fa6856508865e5951d94d65e3bcaee7b801eaec1ad1f2418d27258`  
		Last Modified: Wed, 19 Mar 2025 23:08:39 GMT  
		Size: 8.5 MB (8540557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4402e057a66720bf694402c3c4d53761f554c4cb528a5f4c8f3bc639d22dd10`  
		Last Modified: Wed, 19 Mar 2025 23:08:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.12` - windows version 10.0.17763.7009; amd64

```console
$ docker pull hylang@sha256:681555c91d4964869c37a024240b0e055b430b11b65ff7f28a58b1aa4a98e73f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2217394770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7491339c4cb6068dfc3dacfe8414a9121e09670974c40f0526fa2b8c954e3e`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:49:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:49:45 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 12 Mar 2025 18:49:45 GMT
ENV PYTHON_VERSION=3.12.9
# Wed, 12 Mar 2025 18:49:46 GMT
ENV PYTHON_SHA256=2a52993092a19cfdffe126e2eeac46a4265e25705614546604ad44988e040c0f
# Wed, 12 Mar 2025 18:50:59 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:51:00 GMT
CMD ["python"]
# Wed, 19 Mar 2025 23:12:09 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 23:12:11 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 23:13:29 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 19 Mar 2025 23:13:30 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc182e7cf13f9e22000cba27deb4457ea1d5d2f34837430884a4792580ec3c56`  
		Last Modified: Wed, 12 Mar 2025 18:51:04 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55898bef7227dc9e811a2ce352d54904c26c465ca3c8e168ab1c4d4bf9eb1923`  
		Last Modified: Wed, 12 Mar 2025 18:51:03 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3900e17be4fadf995bac023c1a2a187794c72ba719a24b98dc7e716da02954`  
		Last Modified: Wed, 12 Mar 2025 18:51:03 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e938bb4969cb839486b1b3ef95e92d3069f16e27e4b701ec9fbf89dfdf908e67`  
		Last Modified: Wed, 12 Mar 2025 18:51:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3297900c2bc8f782af2ef806eb969009c1b54e97da62d46e9c59895bd366b2`  
		Last Modified: Wed, 12 Mar 2025 18:51:08 GMT  
		Size: 58.6 MB (58607213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625a88776fd655768154e0d14b390368d6c1d4fbc6ddbfcde9d96220ddf23b1c`  
		Last Modified: Wed, 12 Mar 2025 18:51:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a948d7a49a9f4444e780394459ab090d72ae50799c35891cb74f6e3fd14c0f`  
		Last Modified: Wed, 19 Mar 2025 23:13:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5543243cf3a120471028f7acd5100efb9a915dc01af45016917a81618ab688`  
		Last Modified: Wed, 19 Mar 2025 23:13:32 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ca64cd1fa1d127dbd66c0a0236aade15bbe63d0ef01a23cd9b72c66c433658`  
		Last Modified: Wed, 19 Mar 2025 23:13:33 GMT  
		Size: 7.1 MB (7142543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9932be5fbf86869878b486387604da597f32fff0422baf74c02f8ec96c66687d`  
		Last Modified: Wed, 19 Mar 2025 23:13:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
