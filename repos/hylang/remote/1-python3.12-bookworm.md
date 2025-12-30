## `hylang:1-python3.12-bookworm`

```console
$ docker pull hylang@sha256:60aa1d9d533afdce2731a0145f485e5c5e9a5ab9663c0d89edd7279d4cac90d1
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

### `hylang:1-python3.12-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:64133f6e0ef6dc0f29c4a8a10fe3fa1ed0520baec213593d1fdd74aaa8c19271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50945770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7f988499287f428010ef0927e23dca3105c1cadd2d58c928026c921c3d410c`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:34:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:34:04 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 23:34:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:34:04 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 23:34:04 GMT
ENV PYTHON_VERSION=3.12.12
# Mon, 08 Dec 2025 23:34:04 GMT
ENV PYTHON_SHA256=fb85a13414b028c49ba18bbd523c2d055a30b56b18b92ce454ea2c51edc656c4
# Mon, 08 Dec 2025 23:43:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 23:43:21 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 23:43:21 GMT
CMD ["python3"]
# Tue, 09 Dec 2025 00:58:34 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 00:58:34 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 00:58:34 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Dec 2025 00:58:34 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24bc3dc4f23685c51879f06c0e553157e8980f01a394e2a288592eba3bddbf2`  
		Last Modified: Mon, 08 Dec 2025 23:43:35 GMT  
		Size: 3.5 MB (3515887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214e476b5e7a9a721ccda18dc4eda68623bd68cfbf87fb5ec37534fefc244a4`  
		Last Modified: Mon, 08 Dec 2025 23:43:35 GMT  
		Size: 13.7 MB (13667535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26e5e7da277de4549af157f67aa7ab1ba03b0cb6005d6407772c282951716df`  
		Last Modified: Mon, 08 Dec 2025 23:43:34 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4586f3006074f13c78f3bbe222fa7cf0b4012ca76e8686186b1ef11aa9971cb1`  
		Last Modified: Tue, 09 Dec 2025 00:58:47 GMT  
		Size: 5.5 MB (5533682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:2d1d2cb277207511fec12215c6796ab8a4e83b8577d1b5e69d3a07d7eeaf5450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2586075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27fd6045a479de1becc4e088dc8a75c09253e2d413ef3cd62b35d0acf9b1a90d`

```dockerfile
```

-	Layers:
	-	`sha256:57f848fdaa4f1e1aade784bafd48519b92f49491b63a9753cf74c79d0bf256e9`  
		Last Modified: Tue, 09 Dec 2025 03:24:42 GMT  
		Size: 2.6 MB (2577981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0408e1ff4fa5a470b0cae874b6f3a027de76cc8c09a33291b5de3166a750707`  
		Last Modified: Tue, 09 Dec 2025 03:24:42 GMT  
		Size: 8.1 KB (8094 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:0392be5b2f1504ed7d4be6cb5642f37384fca450e68f88377ad578937b15049c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47461172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958b270b924bb2fce684f6ad34e8676448035ecfa6455dcb3a513690d281337f`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:49:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:49:38 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:49:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:49:38 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 30 Dec 2025 00:49:38 GMT
ENV PYTHON_VERSION=3.12.12
# Tue, 30 Dec 2025 00:49:38 GMT
ENV PYTHON_SHA256=fb85a13414b028c49ba18bbd523c2d055a30b56b18b92ce454ea2c51edc656c4
# Tue, 30 Dec 2025 01:06:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 30 Dec 2025 01:06:57 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 30 Dec 2025 01:06:57 GMT
CMD ["python3"]
# Tue, 30 Dec 2025 02:01:43 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 02:01:43 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 02:01:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 02:01:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:cdd01b66e4b6599d6f59fe75d883783e8ddfc67db8fda967c6ce250da575cc0b`  
		Last Modified: Mon, 29 Dec 2025 22:25:33 GMT  
		Size: 25.8 MB (25757576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f678ca83ae7536dc952690a82d3014c813a881158c4393a5449319e233066300`  
		Last Modified: Tue, 30 Dec 2025 01:07:13 GMT  
		Size: 3.1 MB (3090746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a26ca93620b1a6f1e4caa2539a97e9006b368673a2572da7b696d5a4d89d2a`  
		Last Modified: Tue, 30 Dec 2025 01:07:13 GMT  
		Size: 13.1 MB (13078813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1558c52728a16f6b248ad423474b049f39a220d13cf2216366e742bfc6450068`  
		Last Modified: Tue, 30 Dec 2025 01:07:11 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2c759824ab95c5228b093e8b523b495d7aff1583d81777aada7c99bd1da6e2`  
		Last Modified: Tue, 30 Dec 2025 02:01:56 GMT  
		Size: 5.5 MB (5533787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:1b4ff08d0a486ff1208cbcc5db69cc4d2a6104d06afcca30314e6fbc3304532b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f849e44e825c45f228b77ee615659c4f24260b54e6d1f1c9ad092f1ffcebd7c`

```dockerfile
```

-	Layers:
	-	`sha256:af7d3473ed4d9e2830ffc20423c74d2eef4592fb7e004569b029b3734adfef98`  
		Last Modified: Tue, 30 Dec 2025 03:20:07 GMT  
		Size: 2.6 MB (2581801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21b9ede189a1677591456d96a7cfc6ada198ba47a1f04517583479e15a594e97`  
		Last Modified: Tue, 30 Dec 2025 03:20:08 GMT  
		Size: 8.2 KB (8173 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:f31e2cc9cfdc2fac88d9e34005b3c0f14eb9b5935d92f869ad524b6114812bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45064139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53215010d04e62feaf494bf33d84efd79749c23612675c57fbdfdadd966a261b`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:55:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:55:24 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 00:55:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:55:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 09 Dec 2025 00:55:24 GMT
ENV PYTHON_VERSION=3.12.12
# Tue, 09 Dec 2025 00:55:24 GMT
ENV PYTHON_SHA256=fb85a13414b028c49ba18bbd523c2d055a30b56b18b92ce454ea2c51edc656c4
# Tue, 09 Dec 2025 01:12:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 09 Dec 2025 01:12:28 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 09 Dec 2025 01:12:28 GMT
CMD ["python3"]
# Tue, 09 Dec 2025 02:26:30 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 02:26:30 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 02:26:30 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Dec 2025 02:26:30 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e12d446114182318769a6ca4adfc14d21fbb73f898de1d765662812d9f21c3a6`  
		Last Modified: Mon, 08 Dec 2025 22:16:03 GMT  
		Size: 23.9 MB (23934020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b48537fc630ffd549f89bf95850f25038721fe70344658d27959687355163a8`  
		Last Modified: Tue, 09 Dec 2025 01:12:41 GMT  
		Size: 2.9 MB (2925464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56aa065e1078d7fc772e17ce6adb7ace46bcd9aa8db74ea60de1b863140abe8e`  
		Last Modified: Tue, 09 Dec 2025 01:12:44 GMT  
		Size: 12.7 MB (12670583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b26593a6e3db4632533f9c4b3d492d2298b87503944c1db438f427f33891c7e`  
		Last Modified: Tue, 09 Dec 2025 01:12:41 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f8ecb24af9b820911e36c0b13903fb862c3cec0716b2ff170120e1062ae1bf`  
		Last Modified: Tue, 09 Dec 2025 02:26:44 GMT  
		Size: 5.5 MB (5533822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:bc810c0f4fad623a3d98ac5d7d877f1119de29889f57df1cef09243ef6ffa09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e334143a78059aacd7616380c54ecdbe25e70ab36ea285f1976350806249ce`

```dockerfile
```

-	Layers:
	-	`sha256:70e908d7f40936b0bf58f817989aea985d5c434714b86e5285aadaa1f9e4c6c1`  
		Last Modified: Tue, 09 Dec 2025 03:24:52 GMT  
		Size: 2.6 MB (2580250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c042523274bf71644a9ec8797758aa0e77f9faa3cc60001fa48ec7e7c61ba7b`  
		Last Modified: Tue, 09 Dec 2025 03:24:53 GMT  
		Size: 8.2 KB (8173 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:481babf9db51c7a810cc025d5ebd8cab081ba747778f26154133ee43f4cc8ac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50581596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec82846af216030d080066d6126950f972b08337d49e50f671b3c252d9d99a9f`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:38:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:38:59 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 23:38:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:38:59 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 23:38:59 GMT
ENV PYTHON_VERSION=3.12.12
# Mon, 08 Dec 2025 23:38:59 GMT
ENV PYTHON_SHA256=fb85a13414b028c49ba18bbd523c2d055a30b56b18b92ce454ea2c51edc656c4
# Mon, 08 Dec 2025 23:50:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 23:50:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 23:50:37 GMT
CMD ["python3"]
# Tue, 09 Dec 2025 00:54:42 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 00:54:42 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 00:54:42 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Dec 2025 00:54:42 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3c710b82ea434a47f7e4d02215f4731589f357784e935ff327d1823f407f4f`  
		Last Modified: Mon, 08 Dec 2025 23:50:55 GMT  
		Size: 3.3 MB (3349144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf964b5626627fd4f5d300995b212e8d028b304256dcfcc4c5e7e7d62ccca8c`  
		Last Modified: Mon, 08 Dec 2025 23:50:55 GMT  
		Size: 13.6 MB (13596245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7101479101ef4bf7b4c288179b682b86ae7d2103bec5972629bf29b6ed8f1183`  
		Last Modified: Mon, 08 Dec 2025 23:50:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ec96d62fedf45154ec6d552503c0f0dfe56980bfd3af6b5cf070e9c6e19bac`  
		Last Modified: Tue, 09 Dec 2025 00:54:54 GMT  
		Size: 5.5 MB (5533729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:7d0aca37485154ef6a92028cf300b31919b89fba429d3e8e40afcf393ed8ae9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2586452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3934168835977cea58da7467b41e040f080d4c9a68dc7bf62e85e0563fe5144`

```dockerfile
```

-	Layers:
	-	`sha256:d0f52789c8812460a3bea24a643afc728f06e47667c63780f11d7a3154e960f0`  
		Last Modified: Tue, 09 Dec 2025 03:24:57 GMT  
		Size: 2.6 MB (2578254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:359a294287fc06da8861cdef492f15df2e5fc58cf8118727a01abe594b31d6d4`  
		Last Modified: Tue, 09 Dec 2025 03:24:58 GMT  
		Size: 8.2 KB (8198 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:e07962b9fcde882da3aecdfc08ff5124b9246ced0b8204a797a0b94e2713eacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52183299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13112807c2560b500860d85d1838ee6e152744dae42d0ab8380d3c4068c3893d`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:01:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:01:55 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:01:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:01:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 30 Dec 2025 00:01:55 GMT
ENV PYTHON_VERSION=3.12.12
# Tue, 30 Dec 2025 00:01:55 GMT
ENV PYTHON_SHA256=fb85a13414b028c49ba18bbd523c2d055a30b56b18b92ce454ea2c51edc656c4
# Tue, 30 Dec 2025 00:13:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 30 Dec 2025 00:13:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 30 Dec 2025 00:13:55 GMT
CMD ["python3"]
# Tue, 30 Dec 2025 01:07:31 GMT
ENV HY_VERSION=1.1.0
# Tue, 30 Dec 2025 01:07:31 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 30 Dec 2025 01:07:31 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 30 Dec 2025 01:07:31 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc7f4f01b6e98d075770b4f9d46c8bb8a6f6c0400886e0772498e07ef376eae`  
		Last Modified: Tue, 30 Dec 2025 00:14:10 GMT  
		Size: 3.5 MB (3516510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe19207939cd52234c830319bad2c0b2485b4637dc59669e6909d2140fe971`  
		Last Modified: Tue, 30 Dec 2025 00:14:10 GMT  
		Size: 13.9 MB (13923092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b881b6772e0b261ee12ea92d4f78837a839f9b72427457d0ab7c44e51a11c145`  
		Last Modified: Tue, 30 Dec 2025 00:14:09 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d586840c57ddc2bb6ae85b71853ed665f7ae45782523a692eacd163f0ad2d2e0`  
		Last Modified: Tue, 30 Dec 2025 01:07:46 GMT  
		Size: 5.5 MB (5533675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:3a5c8f1237da1a3381fc2e7669d151a7847973a821bbf97f993dc23fdd2c0c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2583194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d372a2c6141abc5ec7e7a5357ec1287d95307ab5f48570e25537ac8c4b96ac`

```dockerfile
```

-	Layers:
	-	`sha256:a7fbef0ac2b79f3e04296aa556a0c7e34ec55e851daf412ba6123fcfc9b08f7e`  
		Last Modified: Tue, 30 Dec 2025 03:20:17 GMT  
		Size: 2.6 MB (2575132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0ff4fc705892355de90d175271cd4f88d6155da2d9c31c8352e4000d0f66aec`  
		Last Modified: Tue, 30 Dec 2025 03:20:18 GMT  
		Size: 8.1 KB (8062 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:c01035fe09d464c0b13d306afbd13c3144c9c03fbbb6b57dc7996345f0d27768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55692069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335664a0d64b94cf69bc403d6faec07327a06320d89b2cb7bd447b78faf1e096`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 15:23:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 15:23:37 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 15:23:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 15:23:37 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 09 Dec 2025 15:23:37 GMT
ENV PYTHON_VERSION=3.12.12
# Tue, 09 Dec 2025 15:23:37 GMT
ENV PYTHON_SHA256=fb85a13414b028c49ba18bbd523c2d055a30b56b18b92ce454ea2c51edc656c4
# Tue, 09 Dec 2025 15:43:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 09 Dec 2025 15:43:46 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 09 Dec 2025 15:43:46 GMT
CMD ["python3"]
# Tue, 09 Dec 2025 17:07:52 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 17:07:52 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 17:07:52 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Dec 2025 17:07:52 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf74c700a420a85fddf5b4d8e2e0556f2fee47309b07836ca2dfd7ea17ded58b`  
		Last Modified: Tue, 09 Dec 2025 15:44:36 GMT  
		Size: 3.7 MB (3721191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578f4a306199eca501598e3e6e6151463a4351d60dd5622608b55fa6edc86e95`  
		Last Modified: Tue, 09 Dec 2025 15:44:37 GMT  
		Size: 14.4 MB (14367844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b836fb90cc4cc4847383715404e454f6f92f8bd6f3ce148af91901221a0bb`  
		Last Modified: Tue, 09 Dec 2025 15:44:36 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3c0e151263da6a4b434d73c6f71779138c25db506d4295c4261dd43c928128`  
		Last Modified: Tue, 09 Dec 2025 17:08:14 GMT  
		Size: 5.5 MB (5533940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:2074e08bb05734e659d613bda80ac44de860babc914ee6f5e1d3244e0a114df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2590625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5705a94d7e89ef8b30f199308d799bb45a1c9dfdefb966ef6aba0b1d2f3a25`

```dockerfile
```

-	Layers:
	-	`sha256:611bfb0102e7328a1241372fb5e107b664edca88c69c3ae81700189e42c6f8a9`  
		Last Modified: Tue, 09 Dec 2025 18:18:27 GMT  
		Size: 2.6 MB (2582487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:778bca2eac06e6ad503c1383c739a4be5a196a47c0fe68896f59127ebaa88cfa`  
		Last Modified: Tue, 09 Dec 2025 18:18:28 GMT  
		Size: 8.1 KB (8138 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:d1f62b26dad8c655f81c97bd756e3782b4226d9d52f5a0538d8797cba28d41a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49125483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1ab0f2128e51779af68492f5b8b355683be11b9f3b9ad1d09cfdd64e412df2`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:59:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:59:05 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 00:59:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:59:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 09 Dec 2025 00:59:05 GMT
ENV PYTHON_VERSION=3.12.12
# Tue, 09 Dec 2025 00:59:05 GMT
ENV PYTHON_SHA256=fb85a13414b028c49ba18bbd523c2d055a30b56b18b92ce454ea2c51edc656c4
# Tue, 09 Dec 2025 01:11:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 09 Dec 2025 01:11:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 09 Dec 2025 01:11:07 GMT
CMD ["python3"]
# Tue, 09 Dec 2025 03:01:53 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 03:01:53 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 03:01:53 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Dec 2025 03:01:53 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e888560717625af869ca1af0ba16006b45321d72522dbc01d19b460b27d2a68`  
		Last Modified: Tue, 09 Dec 2025 01:11:26 GMT  
		Size: 3.2 MB (3181817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40caf32ea0c689272259c4f8cdd2f7387ac2dc085179eab83269f003b8cbd15d`  
		Last Modified: Tue, 09 Dec 2025 01:11:27 GMT  
		Size: 13.5 MB (13525021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6aec7f1c4bc1dbcebad4b5f5353aef8c039a78309da80c08d9f707201b8264`  
		Last Modified: Tue, 09 Dec 2025 01:11:26 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1cddd4e05fdc1eb80dd26e30bcc532c2863aa566ce621735ef0772bd0a8494`  
		Last Modified: Tue, 09 Dec 2025 03:02:12 GMT  
		Size: 5.5 MB (5533966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:ef7af46bd5c450e89d7271e008d302c11bfd6ea00f125af3ab0478537c84a216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8eedfe2b9ac8c28130a9de7b86950a5cae0992f8cd387ec9a8a7de553fc11b`

```dockerfile
```

-	Layers:
	-	`sha256:308a91b9a87427336343f760736c9233887508a8731a78e788a5172f4ad9c073`  
		Last Modified: Tue, 09 Dec 2025 18:18:32 GMT  
		Size: 2.6 MB (2574797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2bff329d3a390bf6553c807f267dbcee6c31e718e62cbd295aa06e10454130b`  
		Last Modified: Tue, 09 Dec 2025 18:18:33 GMT  
		Size: 8.1 KB (8094 bytes)  
		MIME: application/vnd.in-toto+json
