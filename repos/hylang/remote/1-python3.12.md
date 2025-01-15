## `hylang:1-python3.12`

```console
$ docker pull hylang@sha256:bf936e3847f80508045ea128fee11fbb1eb6af4281c07b3ba902c4c424047c57
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
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `hylang:1-python3.12` - linux; amd64

```console
$ docker pull hylang@sha256:c113ee93d5da8c2cccf066488a065e54c21ed673c922f3366c6c64aff5a7b5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50971527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b2c322c8704a824063206854a7700c4545442cf2b1d4fff51891fd91ba034d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 00:36:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 00:36:05 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_VERSION=3.12.8
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
CMD ["python3"]
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499051ac08b3a334937e7ed829c944091e47d01f2428dbd2d71fb37d5dc05a87`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 3.5 MB (3511532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a8eea45d12c8ebc7133b2db7b6861e900f73b15fff9a94a95d140827ab10ee`  
		Last Modified: Tue, 14 Jan 2025 02:32:13 GMT  
		Size: 13.7 MB (13651884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc54bb88b02b327bcc18f3d5e561c2c77490f91a580d2dcb9d40f3614511bec6`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ea219a60f121230a7edf564a74e5a63ee59529a9bb2b71fe6f2a82b085fc18`  
		Last Modified: Tue, 14 Jan 2025 03:26:02 GMT  
		Size: 5.6 MB (5595444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:92fd4b4b7c1e831cb7d02a5306572d9236755fd0fcefebf03c9848ab97312da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8d6b9c30d41bcd7b1f67c6244048ff0445996e76b307209b0e5537facc92f4`

```dockerfile
```

-	Layers:
	-	`sha256:c4b4ac5782bd398e46aeaffe210c874527ae65a0ecdabee25258db7be2f6e836`  
		Last Modified: Tue, 14 Jan 2025 03:26:02 GMT  
		Size: 2.5 MB (2459768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75a66670506ba4360e2753cd1c2e489bf44159debba4c550fb34100341077595`  
		Last Modified: Wed, 15 Jan 2025 00:18:43 GMT  
		Size: 9.3 KB (9276 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12` - linux; arm variant v5

```console
$ docker pull hylang@sha256:95720d663fec8a9c45a265f685707236c155eadab2cabfc1e651b8ce3d773942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47431824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76498a585608ef0d4faba0322e4fd51d832c0b3bc479447983593ab247fc3412`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 00:36:05 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 00:36:05 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_VERSION=3.12.8
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
CMD ["python3"]
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 01:33:27 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb716453e7f65fe5edf58ffb991f477aad6631af6855b1fbbf63247b2f480eb`  
		Last Modified: Tue, 14 Jan 2025 21:05:47 GMT  
		Size: 3.1 MB (3082269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e1cb7ea5d08ddf3e9446182f7353512de9c0bf77239fcbee948a7d31890804`  
		Last Modified: Tue, 14 Jan 2025 21:06:11 GMT  
		Size: 13.0 MB (13017146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a049cb6dd175689300a5692b3c291f7167f0ae35ba62dae7e86025f97ca1fa2a`  
		Last Modified: Tue, 14 Jan 2025 08:11:07 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59b466bc4db9a05c21627985ce6392594b45bd5596f103411c3b41702310ffb`  
		Last Modified: Tue, 14 Jan 2025 11:12:42 GMT  
		Size: 5.6 MB (5595493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:81b398328d060a028615873cd3ae0fa2dac3ba4dd4365d8317307c8eb07509a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb3ee32ebae1102347ec3a19b1dd5c2d2a98cbc21ea39ec7362953302794346`

```dockerfile
```

-	Layers:
	-	`sha256:af10513f326df3d89feb7c82754f2a9ee6ff817b40bf93560046e6aa00784ff1`  
		Last Modified: Wed, 15 Jan 2025 00:18:45 GMT  
		Size: 2.5 MB (2463312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:930be104d543f44526e32c9d0cc2c738371de2b31b2d34af3daf9edfee220106`  
		Last Modified: Tue, 14 Jan 2025 11:12:41 GMT  
		Size: 9.4 KB (9384 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12` - linux; arm variant v7

```console
$ docker pull hylang@sha256:8f351e197b65b29036f3a92c7c8a8cff88eba0aaf5b135b3fd0ab75533fde043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45023254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97032443bfcc879b3dd6985bedaf32213ab9c98f74a9bdc5282ad4354224322`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 00:36:05 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 00:36:05 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_VERSION=3.12.8
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
CMD ["python3"]
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 20:33:55 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7232d1a962386bbbd1220e29bc109b5a822ab0094e04d1318461e39e2ccf034`  
		Last Modified: Tue, 14 Jan 2025 20:36:59 GMT  
		Size: 2.9 MB (2914918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce66675b8020aca5ead6dfad7fecbc97efc2fbdfb6b82dbcb7bbc67a6567be34`  
		Last Modified: Tue, 14 Jan 2025 20:46:22 GMT  
		Size: 12.6 MB (12598013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83dde6852157e4cd4a081a7e77b72e43fcc99009e1a857bf39a6cf91fb6ecf1`  
		Last Modified: Tue, 14 Jan 2025 20:47:41 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de4ad18b7bc0d98ebfe03d38e79bc9b8e53109da97eb6a133a698b377380fb7`  
		Last Modified: Tue, 14 Jan 2025 21:40:27 GMT  
		Size: 5.6 MB (5595474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:e0003701d3c5baa9fd64806bc4e84f985b6e18f51d6ab35f4a38fde40e212590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0779f107c85e7b7fb68909a588409bda7b4b429aff9ed33465ee29adbe759430`

```dockerfile
```

-	Layers:
	-	`sha256:e94cc8bb9cabb4bb5d5d381f00290709d5652e0db30eec9923ff11d30787dd05`  
		Last Modified: Wed, 15 Jan 2025 00:18:48 GMT  
		Size: 2.5 MB (2462069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce296399c9459cfe28f1aa460b0c1093ef5613251b2deeade8aab151b1aa4def`  
		Last Modified: Wed, 15 Jan 2025 00:18:56 GMT  
		Size: 9.4 KB (9384 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:b6788749425a008575061fbe8782da186c1069d6b2e8f04670f57765adcc2019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50519461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d62b4afdf72329d1903cc116398fb7a0f99950867de45b664717b1ddae4eb4`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 00:36:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 00:36:05 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_VERSION=3.12.8
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
CMD ["python3"]
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02d1a1ced20b0100efa105489794679cd32592b3baa884d7cd0bce963726219`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.3 MB (3332025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b505734ccb3b2e831a9c008786edfb960bd0840be4460816bc170c7f77260aa7`  
		Last Modified: Tue, 14 Jan 2025 20:33:10 GMT  
		Size: 13.6 MB (13550738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64f5fd9b3eb1cbb7b3781b51900c6287dd60108a8947e65f08ff18d464f2799`  
		Last Modified: Tue, 14 Jan 2025 10:20:07 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e71715e0af8522effa17ebec3740972e4627eefbbfa271e50ad8c14e7b16be`  
		Last Modified: Tue, 14 Jan 2025 16:40:19 GMT  
		Size: 5.6 MB (5595417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:c3ca26bf89cc45ed4ae1a445d0e3b57e359f76c8be2d4796303f04d6b26deeb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff4c4a4c154c92db4607f552d9b20c54d2dd98846b0a998e2a408f375ee3f48`

```dockerfile
```

-	Layers:
	-	`sha256:f923ad5e65a30e6b1dc79ed180618d560a737a4b9fdf05e86c1c68c6f04de374`  
		Last Modified: Tue, 14 Jan 2025 16:40:19 GMT  
		Size: 2.5 MB (2460089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50993da0003a86b8db8263ed3f402d287a3a73645e5d121e4f2b6d9401d517f9`  
		Last Modified: Tue, 14 Jan 2025 16:40:19 GMT  
		Size: 9.4 KB (9426 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12` - linux; 386

```console
$ docker pull hylang@sha256:e6fcf555bc128ac5522b2b4c0a5a3987f1868410aa6177ae309fc25b5745c7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52199117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bce5c8dd43342cc7c9b6abc8b6a6fc569d385bf1eec00ceb92ca9b945204cf1`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 00:36:05 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 00:36:05 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_VERSION=3.12.8
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
CMD ["python3"]
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 20:35:48 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4c8f7fe469e257b3be529feac376b4f9b4e300987c5f6090ca47d9d8187a1d`  
		Last Modified: Tue, 14 Jan 2025 20:50:28 GMT  
		Size: 3.5 MB (3509819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1fb2062d3a6cf0b1748ed8528d5210e45e889033534757fea3a936f870fc40`  
		Last Modified: Tue, 14 Jan 2025 22:15:36 GMT  
		Size: 13.9 MB (13906234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f844ab446e44753f9dfe0592a3f19b9e1c48248e356f381da621cbc8960b75ed`  
		Last Modified: Tue, 14 Jan 2025 21:19:50 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b68ff6c23d14988bfe56b2d554df835101a86da2ac0f98eff808fa6b221156`  
		Last Modified: Tue, 14 Jan 2025 03:24:20 GMT  
		Size: 5.6 MB (5595219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:9da7a44e132012aa23a0f410b54bc610d8856b47415f67a104aadc57f83fd97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0957b62c8dcc87d3858b02a2c9dbd4c0d30ca646960de7334b38e6b0e35eef1c`

```dockerfile
```

-	Layers:
	-	`sha256:0e5d42c697ccf58e5bec835199d22df4dc92da10a028556dfe424e8991a2e8a1`  
		Last Modified: Tue, 14 Jan 2025 03:24:19 GMT  
		Size: 2.5 MB (2456848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c2cb0761d87c9e0f8d169e8f21d93df901e5d75ef85c25db26465ec97e18c8`  
		Last Modified: Tue, 14 Jan 2025 03:24:19 GMT  
		Size: 9.2 KB (9224 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12` - linux; ppc64le

```console
$ docker pull hylang@sha256:7223c9242c7d1c3674592fd4dddf0996ac7de6f7ada95ba9ca43a21eee596e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55645980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a869da2c7dce0555c15404e9f3cd808224ddaa05c66bf1a11a5dc5a7acf5fb`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 00:36:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 00:36:05 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_VERSION=3.12.8
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
CMD ["python3"]
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d620252f157554d49441d6f1e5ac06538b432674396ad8fd478c7a96d3549a`  
		Last Modified: Tue, 14 Jan 2025 20:37:03 GMT  
		Size: 3.7 MB (3713734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbd7e8f4a5160e1288862555de341424ee101b42d3b534d1fc569c9e9ee00cc`  
		Last Modified: Tue, 14 Jan 2025 07:46:05 GMT  
		Size: 14.3 MB (14291760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f61a9610c68649af24abaae2388b407c698cdaed44505494dcb059d4fb45384`  
		Last Modified: Tue, 14 Jan 2025 07:46:04 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97a4849db145ad2fc2a332b7d5b8af53bb7b80adaf4f3b2c6bfb2d3c45ab54c`  
		Last Modified: Tue, 14 Jan 2025 13:24:35 GMT  
		Size: 5.6 MB (5595390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:a02df733233f83670b2bab957ff6e3ec2814f1ac6893b26a3f027f47a2c204e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2473527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed40b50e4572873f89414b783f7a94e589042f5d94b0e597026c785a8d1695b`

```dockerfile
```

-	Layers:
	-	`sha256:86f3830e3bbffb2fa228403a6a2c0aa5481d0c60134bf82b164a8d3db47c3fa5`  
		Last Modified: Wed, 15 Jan 2025 00:18:53 GMT  
		Size: 2.5 MB (2464184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c40c10b17c87962f39ed412ed0209c20a70b1673849c847b23e75fa9573cafa`  
		Last Modified: Wed, 15 Jan 2025 00:18:53 GMT  
		Size: 9.3 KB (9343 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12` - linux; s390x

```console
$ docker pull hylang@sha256:c200c278063f36e9cc9eca0cbdd34a1f357215988e53adb910c4219545640a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49091979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351105dea45b34437db6db58cb93cf310c4f795eba3eb2c79ec4aa73aa48f4f4`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 00:36:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 00:36:05 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_VERSION=3.12.8
# Wed, 04 Dec 2024 00:36:05 GMT
ENV PYTHON_SHA256=c909157bb25ec114e5869124cc2a9c4a4d4c1e957ca4ff553f1edc692101154e
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 00:36:05 GMT
CMD ["python3"]
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 20:36:29 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597a9339eb929c2bd88707540b991ffc9a4e9acd8428278be33de51ca2aff7d9`  
		Last Modified: Tue, 14 Jan 2025 07:14:29 GMT  
		Size: 3.2 MB (3173121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e897ab88683be1e8cb89a4f9caf370f96625d32f379fbb3063d0bc67a31120d`  
		Last Modified: Tue, 14 Jan 2025 20:43:31 GMT  
		Size: 13.5 MB (13464567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8f09a2d351212bc5ab18700ff326fd73e7991469b27bfc4bd2a6f8421755e2`  
		Last Modified: Tue, 14 Jan 2025 07:14:29 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08e1cecdeccda6d1dc89731232ad04dd64e1376ecc915c5a70372645fa9403b`  
		Last Modified: Tue, 14 Jan 2025 11:31:34 GMT  
		Size: 5.6 MB (5595304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:4d9a450a1a232c4f6b6b09ce0f3b5837abd58567dc8ebaaf0609d7bc0bd3077e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4006a8be987f7ce95a53e76d993ec9e7bce5082842067d085de3610235824f8d`

```dockerfile
```

-	Layers:
	-	`sha256:5fbb0870e117a64292e486a3b0c1c415f320c9aea101c2aa9288c549d958f5ba`  
		Last Modified: Tue, 14 Jan 2025 11:31:34 GMT  
		Size: 2.5 MB (2459476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a622e3ba23540abedf82e0ac45d162cf7e47bb6492b160e03a31e458baa6a80`  
		Last Modified: Wed, 15 Jan 2025 00:19:02 GMT  
		Size: 9.3 KB (9276 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12` - windows version 10.0.20348.2966; amd64

```console
$ docker pull hylang@sha256:1178a9c0396b1c35d12c1b1e9aa215cde9b6ec2fec7a071a86a896491f86fb25
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2322350536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176cd329819245b0bb5706fdfd9dee31df51c240c1fd619404267fcec54c8520`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:42:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:42:58 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 11 Dec 2024 20:42:59 GMT
ENV PYTHON_VERSION=3.12.8
# Wed, 11 Dec 2024 20:43:00 GMT
ENV PYTHON_SHA256=71bd44e6b0e91c17558963557e4cdb80b483de9b0a0a9717f06cf896f95ab598
# Wed, 11 Dec 2024 20:43:43 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:43:43 GMT
CMD ["python"]
# Thu, 09 Jan 2025 23:10:35 GMT
ENV HY_VERSION=1.0.0
# Thu, 09 Jan 2025 23:10:36 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 09 Jan 2025 23:12:05 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 09 Jan 2025 23:12:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da926f5375939d9dc382c854fc5da819e00a1ff2c7406fcddc8ba05f26ecb34`  
		Last Modified: Wed, 11 Dec 2024 20:43:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f58adc4231c3bbc7df9a3546d8ab43372f4dc9d70529b3c92f3366cb9b3a5db`  
		Last Modified: Wed, 11 Dec 2024 20:43:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fbdbe634f9ad8487a6fa24162448cacc4dc0dfd61ce1c1298c2ac24f78d976`  
		Last Modified: Wed, 11 Dec 2024 20:43:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010caa98cd1cce422bc61b1062237b35a780a9f4ac262cfb1477e4359133b089`  
		Last Modified: Fri, 13 Dec 2024 18:32:59 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2eb60fc7589b6813d8b88bb56a4e9a6557740d9e4a6231cc24b9b00823857d`  
		Last Modified: Fri, 13 Dec 2024 22:14:03 GMT  
		Size: 59.9 MB (59935423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff6b0046ebd10376ac0bf3af702b085b098fab88ae08b318aeee4c0584d4aa7`  
		Last Modified: Fri, 13 Dec 2024 16:26:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76be316adfd0e23ead718839887b77e3dd7cbc27570935a6ce28ca598db93996`  
		Last Modified: Thu, 09 Jan 2025 23:12:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e9d84ccc1b2effc6e1fb269e321f2dfa2d2065c638ae34789fb7e62bb5c4a1`  
		Last Modified: Thu, 09 Jan 2025 23:12:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f623b909728f4cc4807a699e6ef69d2d2920d79a80f16b46c48342368e616e2b`  
		Last Modified: Thu, 09 Jan 2025 23:12:10 GMT  
		Size: 8.5 MB (8531189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064b0f954001b84240261a61efbf65ec580ef9ba3be70b7bdf79116fdacfbe58`  
		Last Modified: Thu, 09 Jan 2025 23:12:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-python3.12` - windows version 10.0.17763.6659; amd64

```console
$ docker pull hylang@sha256:57e48d6c94430756ac289f2f5ddd50b0be01af0b14a9ae39998d3b92cfae3073
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2080052674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2293ae3c18a58b199202f81574781b72bb8543be401d3cb50bee152146a2b833`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:41:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:41:49 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 11 Dec 2024 20:41:50 GMT
ENV PYTHON_VERSION=3.12.8
# Wed, 11 Dec 2024 20:41:50 GMT
ENV PYTHON_SHA256=71bd44e6b0e91c17558963557e4cdb80b483de9b0a0a9717f06cf896f95ab598
# Wed, 11 Dec 2024 20:42:46 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:42:47 GMT
CMD ["python"]
# Thu, 09 Jan 2025 23:10:15 GMT
ENV HY_VERSION=1.0.0
# Thu, 09 Jan 2025 23:10:16 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 09 Jan 2025 23:11:05 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 09 Jan 2025 23:11:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c69b30de0bb94495a01d2ffa3cbe2160d47354a632fa558a9a28bb1f5586a26`  
		Last Modified: Wed, 11 Dec 2024 20:42:53 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3f4905dceffd459d14fbfb30b842c645d5d62e6248061cb2b78399fe229df9`  
		Last Modified: Wed, 11 Dec 2024 20:42:51 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61eb8d3c795404a9cce5e17b329a1d1d8f7e3403af85c201eee41fbf81d3d14`  
		Last Modified: Fri, 13 Dec 2024 17:52:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf845fe8780bfa8b4a27751991a0bc5196b903cf3c58ac13e37e1cf1d0ee557`  
		Last Modified: Sat, 14 Dec 2024 04:10:29 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb2a1b246e83da13677def7201662292fbef830339c769b762c341cc1c5e043`  
		Last Modified: Wed, 11 Dec 2024 20:42:56 GMT  
		Size: 58.7 MB (58732455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf5cf7377be1465e2468dce6ac41ac1f30018149d8eca84eb04e1723195c16f`  
		Last Modified: Wed, 11 Dec 2024 20:42:51 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515a25d4aeed142aa5ff39fa93da2835e91873fccdf31e9ed20613519cdbfea1`  
		Last Modified: Thu, 09 Jan 2025 23:11:09 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5764e89d40950d51d74657905008b79bf76bdbbf3bdb61a0b8df31e368bf10`  
		Last Modified: Thu, 09 Jan 2025 23:11:10 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09b5300e31dd2fd9a471b938a2f8e17e25252cfd5a29b460dba4259b2ec7d6d`  
		Last Modified: Thu, 09 Jan 2025 23:11:11 GMT  
		Size: 7.1 MB (7139631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233a1b829eeffd5e4cc77dd3b39f5cc10177340f268020197af37ecb1e162baf`  
		Last Modified: Thu, 09 Jan 2025 23:11:09 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
