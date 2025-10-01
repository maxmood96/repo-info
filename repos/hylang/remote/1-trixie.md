## `hylang:1-trixie`

```console
$ docker pull hylang@sha256:4c0394efa0791a30032954e4069ebe65f9e95f27b0a551a7ff7867edfa201175
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

### `hylang:1-trixie` - linux; amd64

```console
$ docker pull hylang@sha256:ba2eb4398722bcf0d3f38525ff3a1976b6103f1b24da0e248f0b8f315c2f6855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48342128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29277d407d5c61c3328a92364554fe4b85186a1f4221c8db19b6e2ad2e156da0`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.13.7
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=5462f9099dfd30e238def83c71d91897d8caa5ff6ebc7a50f14d4802cdaaa79a
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["python3"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HY_VERSION=1.1.0
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 13 Aug 2025 21:03:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fd2a94d72338ac6bbe103da6448d7e4cb7e7a29b9f56fa61d307b4395edf86`  
		Last Modified: Tue, 30 Sep 2025 01:29:53 GMT  
		Size: 1.3 MB (1292542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b685f2f76ba4e1e04b26b98a2aca385ea829c3b1ec637fbd82df8755973a60`  
		Last Modified: Tue, 30 Sep 2025 03:35:21 GMT  
		Size: 11.7 MB (11735641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d456e82f89bfe09aec396e93d830ba74fe0257fe2454506902adf46fb4377b3`  
		Last Modified: Tue, 30 Sep 2025 01:29:53 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa638f3de88278e58ecc8a12c4ecc777077aa2120b527624a0ffdf8ad4b4ad7`  
		Last Modified: Tue, 30 Sep 2025 03:36:09 GMT  
		Size: 5.5 MB (5535929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:261a7858668ea3c0a6f385c99f700192b0eb30f6d3af41ccf47e4ef74a46eae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2164017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858c14d8496697683bb6833c95162aeef6eb29a5adc50724ba1ffbb0ca856397`

```dockerfile
```

-	Layers:
	-	`sha256:89c50a46fb4fae8883ae07856c8411766491c1e27e7c1e7717509b1860f1646c`  
		Last Modified: Tue, 30 Sep 2025 20:18:25 GMT  
		Size: 2.2 MB (2154814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdbeb7319f9f40181c3117d0b330a118c76a5db2acc8bcebb3e02fc2314bda57`  
		Last Modified: Tue, 30 Sep 2025 20:18:26 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-trixie` - linux; arm variant v5

```console
$ docker pull hylang@sha256:759ff10ada167579973908f9badd244fe0afb7577ef060fd8deda8adb6819944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46188604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031ae33e7f60b5aa8469984064b79f530e74444388a386859fee15499ba8a3bf`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.13.7
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=5462f9099dfd30e238def83c71d91897d8caa5ff6ebc7a50f14d4802cdaaa79a
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["python3"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HY_VERSION=1.1.0
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 13 Aug 2025 21:03:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec56f5abbace28369c0613a557ad5b9b2fad30e3bdec7b3503874a6e21c98d6e`  
		Last Modified: Tue, 30 Sep 2025 01:37:30 GMT  
		Size: 1.3 MB (1275440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a4ff5048da2d0f9a56c8c573cbc0a73a186409a621a8838c6da24c951b122b`  
		Last Modified: Tue, 30 Sep 2025 01:37:32 GMT  
		Size: 11.4 MB (11430833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd013e914aa79c708905a4b2a8585b18ff1aec42288c42d3af1e4c52a7095772`  
		Last Modified: Tue, 30 Sep 2025 01:37:37 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71826c9d838a5f11278e6d4cb698689bde09e7f1dae27e72dabc32015db15bf1`  
		Last Modified: Tue, 30 Sep 2025 03:03:14 GMT  
		Size: 5.5 MB (5535937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:e7a4cbfbb1b420fb846aff44c2ecec8fab0033e4106420799d15ed349afa1ed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2167130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d20a29e1a4fbfa337e0eaeb4fade856a8eb3a45836e9f5c7e118d2b96f8c54f`

```dockerfile
```

-	Layers:
	-	`sha256:c97f94df382d75e4be65aecf34322d5b8476cbc9520659898d4850b2e783a7ef`  
		Last Modified: Tue, 30 Sep 2025 08:18:53 GMT  
		Size: 2.2 MB (2157815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6aa3db9f2c32f82c65b8d038f7fe12f06fdb0fde34129eab73b95e47c0137b9`  
		Last Modified: Tue, 30 Sep 2025 08:18:53 GMT  
		Size: 9.3 KB (9315 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-trixie` - linux; arm variant v7

```console
$ docker pull hylang@sha256:4a1b33efd4ed37a6f8a20f45b3a16bafe0dc8ee9f0cb6bbc93a7360b87c5bebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44144445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01997a9e719c3439e596b851f2af871ad059ee1805cdfec0055f16402009f29`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.13.7
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=5462f9099dfd30e238def83c71d91897d8caa5ff6ebc7a50f14d4802cdaaa79a
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["python3"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HY_VERSION=1.1.0
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 13 Aug 2025 21:03:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c59eccf883ebcb680e29397ba73dac3f8a418dca52e1d030f6a9ad9d354408`  
		Last Modified: Tue, 30 Sep 2025 02:10:12 GMT  
		Size: 1.2 MB (1247953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a8446a5c6fd2db04a11e2d78b94d90441273b7f0edaf22976157699d8c105b`  
		Last Modified: Tue, 30 Sep 2025 02:10:12 GMT  
		Size: 11.1 MB (11147542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607ca797831cef6f95ca5f4bc511f3bafea6832e0ea47e2565882dd9e0f21714`  
		Last Modified: Tue, 30 Sep 2025 02:10:12 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a941412b68c628f447d5472163b7b3d0f6b5a4a00de5ca3b74a275a2b45fa71`  
		Last Modified: Tue, 30 Sep 2025 03:24:18 GMT  
		Size: 5.5 MB (5535942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:bd0e1c5ce709484c9b4ecceb4c20d0f77f4d024955deed12ff09fd00ae877b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1e31a4bcb0c3cc14623929c3f340a4c5e36366133e4044ae01f70d40ce5249`

```dockerfile
```

-	Layers:
	-	`sha256:34bd91734d88db86b39d3cc437db1900e26b98debdae14c0cb54e6f7eb62851a`  
		Last Modified: Wed, 01 Oct 2025 20:19:45 GMT  
		Size: 2.2 MB (2156268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df6854a8690785c859ca650f79b85b0a3d9403db35ea86bbe5107a9817e2ef71`  
		Last Modified: Wed, 01 Oct 2025 20:19:45 GMT  
		Size: 9.3 KB (9315 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-trixie` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:57a03168a22cd2c427558264be1462d6b7869a2905965934ea67584822aaeff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48615280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b464ee32b19bc58ec8ed37a759dd30c9c4aecfaa1883ca99500831dc6ae3d05f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.13.7
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=5462f9099dfd30e238def83c71d91897d8caa5ff6ebc7a50f14d4802cdaaa79a
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["python3"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HY_VERSION=1.1.0
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 13 Aug 2025 21:03:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d8541dd367f5b0d64f05e4b545d916cdb2b1dde256277aa062ad54c75b7222`  
		Last Modified: Tue, 30 Sep 2025 00:45:09 GMT  
		Size: 1.3 MB (1272858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e440326d8d0b8fdf9f1ce85d6c01a6f1e4bdb0f5df94c06cc52a14f761562f1`  
		Last Modified: Tue, 30 Sep 2025 00:45:10 GMT  
		Size: 11.7 MB (11665386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb6b0ed57a4a78261b9d38e2ae8e77840317eb53f36572adac1ab2ae3c7a99f`  
		Last Modified: Tue, 30 Sep 2025 00:45:09 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11e97d7898b74fd9d220b5d14c9fcac2c762968aa84af9ec04e3bc583a93e76`  
		Last Modified: Tue, 30 Sep 2025 01:24:17 GMT  
		Size: 5.5 MB (5535945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:35b93e1e5d6d5ffac8cc7dca1b2d7d25d58eb99df33ca91ba6c58860d8152233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2164483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851f7528c39f6ed051c6fd6aef36bfc9bdfc34f386b5d7ca5a8601839d01046d`

```dockerfile
```

-	Layers:
	-	`sha256:10c056db44c52185650bf8365f1d03915ad00ea1b3ee0603a0c121eb382b1960`  
		Last Modified: Tue, 30 Sep 2025 11:20:13 GMT  
		Size: 2.2 MB (2155128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9677e0e49c9f9d58984ac2358c101e2e64ef022576393ea5f53dd3564f537f6e`  
		Last Modified: Tue, 30 Sep 2025 11:20:14 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-trixie` - linux; 386

```console
$ docker pull hylang@sha256:66f528ae4c081d243804b77e59a0f2edf183a1380da0e8efb9c4de8850b4cf6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49974686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24478124317015b349a469aa389fa51e9a73b14552760cf34b88805e2ee7582e`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.13.7
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=5462f9099dfd30e238def83c71d91897d8caa5ff6ebc7a50f14d4802cdaaa79a
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["python3"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HY_VERSION=1.1.0
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 13 Aug 2025 21:03:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af07352aa37ea291d9e65f2216ed8d148416d197361299628d8e151ad8defc2e`  
		Last Modified: Tue, 30 Sep 2025 00:42:23 GMT  
		Size: 1.3 MB (1296505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf110630e5c2b1180b93531a201ef11f3dc6667de45d9aefb0d53516c6d5fa1`  
		Last Modified: Tue, 30 Sep 2025 00:42:24 GMT  
		Size: 11.8 MB (11847455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f90563e5acb883b0d062ead1248bc780e58615c40b90febfb244c72f46a4e3`  
		Last Modified: Tue, 30 Sep 2025 00:42:23 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602d415252a447ff1e50dc25770f13bffb4e2a7b10541e3ba2820f0b8505756d`  
		Last Modified: Tue, 30 Sep 2025 01:23:27 GMT  
		Size: 5.5 MB (5535942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:676284f4d3e91f395081a2df82c7a72c5df09fa25ca462690b12d948c662b9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffb912f2341bde8184165e35629a13e905011c36e68e0d49d0d8bd482095d91`

```dockerfile
```

-	Layers:
	-	`sha256:f4b10301eeecff3d214b2151326b7dfc84a7576fb9dc9a39ec2bcd5a211298e5`  
		Last Modified: Wed, 01 Oct 2025 17:26:34 GMT  
		Size: 2.2 MB (2151975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed897c25507f005e69ab58890b364ec3c982911b81e0a2151db9fdc67bc3d905`  
		Last Modified: Wed, 01 Oct 2025 17:26:34 GMT  
		Size: 9.2 KB (9151 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-trixie` - linux; ppc64le

```console
$ docker pull hylang@sha256:6fd3716fc4c7bc3b36081414ed6692af8ce4994212005102679cbe1abc39b30d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52583599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1410ecf0a7386d270dcaf9bafda92308980d71b1fe092204b1e62968989551f8`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.13.7
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=5462f9099dfd30e238def83c71d91897d8caa5ff6ebc7a50f14d4802cdaaa79a
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["python3"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HY_VERSION=1.1.0
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 13 Aug 2025 21:03:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b0bfaf59f87658ddd223362fbb0dd01025ef3bb8eea1e3c7a68aa1ca5146be`  
		Last Modified: Tue, 30 Sep 2025 11:47:07 GMT  
		Size: 1.3 MB (1320787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b07137398cf2e494302c4fdf0a4f586b855cda43d8343066cc887a9638dc7a`  
		Last Modified: Tue, 30 Sep 2025 12:06:26 GMT  
		Size: 12.1 MB (12128038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520ed7fc7b2be2cd9e668ed89ba04a4cce54295b393d9fec19744c895ee57b2b`  
		Last Modified: Tue, 30 Sep 2025 12:06:26 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40cb373637d5f09214675824ee8aca5ac8fda84f6acf36a0c040be91768a5f8`  
		Last Modified: Tue, 30 Sep 2025 22:17:10 GMT  
		Size: 5.5 MB (5536070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:a522927d3fa5a05f066db30046e53bb94cb3ccb1b208705564d9c4b1f13e29b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2167676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a86e5db9c806e52714b894f7a0ae9547d195e124b03b45f34ffe85b128c6ad`

```dockerfile
```

-	Layers:
	-	`sha256:34ae0185c146c8b1d35c126a28322b2f4e40748c923e7f6ccbe3a27351f338cd`  
		Last Modified: Wed, 01 Oct 2025 20:19:53 GMT  
		Size: 2.2 MB (2158405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b4eb583c4e327dbd6480e94e55707b5504f672c1f7d08f4f9200ac4dd983d5a`  
		Last Modified: Wed, 01 Oct 2025 20:19:55 GMT  
		Size: 9.3 KB (9271 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-trixie` - linux; riscv64

```console
$ docker pull hylang@sha256:ca2c14ce84629825a31022290170ceac5c253b5c26b326968e3656043b56a684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46781295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1571965b39a4c3e43e208b3d4f9cd8770a83caa35e26868d2e32e068e5da444`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.13.7
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=5462f9099dfd30e238def83c71d91897d8caa5ff6ebc7a50f14d4802cdaaa79a
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["python3"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HY_VERSION=1.1.0
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 13 Aug 2025 21:03:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ada7e08221c54cf97c5f0d44b9dc8842ce4a65dc672f81530cdbc3d006ca31`  
		Last Modified: Fri, 12 Sep 2025 23:22:34 GMT  
		Size: 1.3 MB (1259725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35261e5de3156a2efeafb9eb025ef46de49249bc5bb2bee31efbff8b9ec80ff4`  
		Last Modified: Sat, 13 Sep 2025 06:24:03 GMT  
		Size: 11.7 MB (11713263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedfae1b06e5837253ab5671912fd2d2585643b876edcf539953dcd0766724f6`  
		Last Modified: Sat, 13 Sep 2025 06:24:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02af8eda285fd1c588dccd301df04b59de5c00abcf61930bcf4c9cc4cf30a279`  
		Last Modified: Mon, 15 Sep 2025 07:24:54 GMT  
		Size: 5.5 MB (5536684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:e469216fe4079a688105821f556ae33d38cd584670521aff536224938562328a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88a7d253c7c490f1279aa4be2df222002e78cff8a6202dce54e268fa0fb80c5`

```dockerfile
```

-	Layers:
	-	`sha256:3be9ee2eea7a23b56511defae172d028be5128673390cfbb1f19f1b2c3101bb1`  
		Last Modified: Mon, 15 Sep 2025 08:18:35 GMT  
		Size: 2.1 MB (2148776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250fa0df27dcdc67a9b42b4e240dcb865a7ab24f0c2241367da0e09600a36c24`  
		Last Modified: Mon, 15 Sep 2025 08:18:36 GMT  
		Size: 9.3 KB (9271 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-trixie` - linux; s390x

```console
$ docker pull hylang@sha256:0a07bcd892e7d708a71f8ca3742480a44f8f0aee828bbf92c9d39a0079c3699b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48463118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d9040634deaaba639e2508db9fe4f5edd2e2ce3a5e00c5a442cec285883160`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.13.7
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=5462f9099dfd30e238def83c71d91897d8caa5ff6ebc7a50f14d4802cdaaa79a
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["python3"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HY_VERSION=1.1.0
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 13 Aug 2025 21:03:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f701a28ec318ac43038df06d954daad1bc9f2b5dc11e5c09e3e06453a1af11`  
		Last Modified: Tue, 30 Sep 2025 11:25:38 GMT  
		Size: 1.3 MB (1305071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5bd9001daa17d85708551f42c6bee5a3bbb79eb7dec7c9b2144ad992e7a762`  
		Last Modified: Tue, 30 Sep 2025 11:45:04 GMT  
		Size: 11.8 MB (11784539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917849674d466aa07e27aa7d2437f7b6fcb6eca2c2ff7c28911453c96cd38f17`  
		Last Modified: Tue, 30 Sep 2025 11:45:04 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe35d5e3f5ef7e4a8f8e097a3f89ffb7ef9a313f1baf8bb99685680b339a6e9`  
		Last Modified: Tue, 30 Sep 2025 19:09:26 GMT  
		Size: 5.5 MB (5536029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:8db0595a25df0b81ee1bc96f767742efdf97e570f9f6cf3ee3f024a2233cfbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5a8924700dbcdaa81da2c722fcc43e5dd07e43f87b2f2889f918cf98dcd106`

```dockerfile
```

-	Layers:
	-	`sha256:d2d6cd4a5c3cc17349cede15bb92b18e157f29e6a89a9d6a58536bc9f4f8d5d0`  
		Last Modified: Wed, 01 Oct 2025 20:20:00 GMT  
		Size: 2.2 MB (2156253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a289a51d742d2ac85c99fbe3948a5067e0a7dc1cabcb6491ded2148df802d71f`  
		Last Modified: Wed, 01 Oct 2025 20:20:01 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.in-toto+json
