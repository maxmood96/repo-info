## `python:3-bullseye`

```console
$ docker pull python@sha256:27e77d37c246ed79fbaeb3e78c9c20fa5035ac7b849b77c70f93cd9f96195f69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `python:3-bullseye` - linux; amd64

```console
$ docker pull python@sha256:fc62b2818aad8aa5232f3356ea84f2cb8dd44b8c1f14a09f26c29ed9d6c97a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.3 MB (355285582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fcb26a42d667ea5d57fd4d7d1b019ca2fb3717d77c14f87033669cd6577907`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_VERSION=3.13.4
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_SHA256=27b15a797562a2971dce3ffe31bb216042ce0b995b39d768cf15f784cc757365
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8156a957a8b63a670ed89130a2e1eedf5c1b2a939f33a952c4159b4ebcb0a`  
		Last Modified: Tue, 10 Jun 2025 23:36:44 GMT  
		Size: 15.8 MB (15765139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2678613884c2f141cc551880b1a1587f0c890606a900bbac5a1ace2645be657`  
		Last Modified: Wed, 11 Jun 2025 00:02:35 GMT  
		Size: 54.8 MB (54757363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c6624995870ade650aaf0f5b37565d2e41e2500e8105fd69b79900eef086cf`  
		Last Modified: Wed, 11 Jun 2025 02:16:19 GMT  
		Size: 197.1 MB (197142069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf49a485c4478a870cc82137956d90fc64d00ff9bf6f6410e8fc4700fbc3466`  
		Last Modified: Wed, 11 Jun 2025 02:33:41 GMT  
		Size: 6.1 MB (6051913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866a63718b0d1d9f21fa9c1a2fa05a521a041eaafb06f0f77f3c0d95094de932`  
		Last Modified: Wed, 11 Jun 2025 02:33:42 GMT  
		Size: 27.8 MB (27814066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6efd8402fc9369c8ccbae28a70623ab41786624fa6a1c1b3513e8e79b8929c`  
		Last Modified: Wed, 11 Jun 2025 02:33:40 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:03d726e0b66e7b34d999bf4013e6ca232e59da2ae9047df4ea4b7cfc975c2742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15982886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536070ed8d0a1f01fc82e091bf2ec0736243d531b891baa4f9a904c852592e9f`

```dockerfile
```

-	Layers:
	-	`sha256:a67a1d85021263ed9ff9afa489a95554d66f2480369238fb6dca968b6663bc83`  
		Last Modified: Wed, 11 Jun 2025 06:06:42 GMT  
		Size: 16.0 MB (15960389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e02202ad6750cfa5eb2d5af24e15d97bee2df8a551a137d72951e2d7eaba7914`  
		Last Modified: Wed, 11 Jun 2025 06:06:43 GMT  
		Size: 22.5 KB (22497 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; arm variant v7

```console
$ docker pull python@sha256:dc727e34e0be0e2a35d75c1a0f94633b4d499ecfbcb9157520f8a8b1da6c4240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.2 MB (314246963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d52c53bef7c1ef85ac2b9bf987046942f355de3ba2768fd60a21db343b9a91`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_VERSION=3.13.4
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_SHA256=27b15a797562a2971dce3ffe31bb216042ce0b995b39d768cf15f784cc757365
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:2bf062f1f44f96722293994387f4b88016e2f0a9f49c7f09b2ceffefc7717199`  
		Last Modified: Tue, 03 Jun 2025 13:43:06 GMT  
		Size: 49.0 MB (49041988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933c7aef3dae867caad0cbafef5672fb39317c04b3bf8bff0868bf265098c4de`  
		Last Modified: Tue, 03 Jun 2025 14:32:56 GMT  
		Size: 14.9 MB (14880519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0144e65734487c61a592b9ecd7d576c77bc270bd5d65049de36718f77416c6`  
		Last Modified: Tue, 03 Jun 2025 14:32:58 GMT  
		Size: 50.6 MB (50631322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c9ac1f243c709a0fa1779761ca68b4f1c6b9419089c5cd54dcb97bb3d22f54`  
		Last Modified: Tue, 03 Jun 2025 14:33:03 GMT  
		Size: 167.6 MB (167578499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37328008c44539da0fd704fddaaef8972771db035729820129c1d5d064395659`  
		Last Modified: Tue, 03 Jun 2025 14:33:07 GMT  
		Size: 5.5 MB (5461199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b099b327cda6eb1fa437ec94b74d8631388cb6fc72ff7713226b9fb3d4f9370b`  
		Last Modified: Wed, 04 Jun 2025 21:15:37 GMT  
		Size: 26.7 MB (26653187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e7ca3fd73fd72d40e4accae9156f19868ba72af47cc5a4208d5986b59c3817`  
		Last Modified: Wed, 04 Jun 2025 18:14:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:c4225090974ddef1dd69f7051d8d3534719f0465fc38ce6d3b6cb6305bc42c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15491589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52b2b5e8ea853c74960a11cbab5c34f72f65aafb461a5933b22180d47670fbf`

```dockerfile
```

-	Layers:
	-	`sha256:37525206f74855570c65b138ce222e2ec07316c8bb7a5c319e38811cdc7f0718`  
		Last Modified: Wed, 04 Jun 2025 21:07:00 GMT  
		Size: 15.5 MB (15468990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e965c18081d712ee41cb4044a21e4c4944c63f5876af8cf19b7e054d5d7096e`  
		Last Modified: Wed, 04 Jun 2025 21:07:00 GMT  
		Size: 22.6 KB (22599 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; arm64 variant v8

```console
$ docker pull python@sha256:8af5fe55f8abaadaeaa14651eaaae5e1839cecabbda36126f0dbaf47163878df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.4 MB (346371593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ccd16fa5dff7bc02257d31b424e0f3397322fd10860c971460a21c97d1297e`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_VERSION=3.13.4
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_SHA256=27b15a797562a2971dce3ffe31bb216042ce0b995b39d768cf15f784cc757365
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a602f78cf8d696db9521d18affb7ecdb79ff690533efae26e3bdb1544cb1752`  
		Last Modified: Tue, 03 Jun 2025 13:31:09 GMT  
		Size: 15.8 MB (15750382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c1b27af19f7550ac0d9c38bf6bcf26ba7eb53984e7e5e0886342816133c76e`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 54.9 MB (54853236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d0d4413e7427c3ec24a23fc978dced4b2de0294ec9d2e02645e0f62aa2de32`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 190.0 MB (190044698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e858abaa6fd1247545d6d20a95470baebe32096afc7a57d3033ed71ea95404`  
		Last Modified: Wed, 04 Jun 2025 18:12:26 GMT  
		Size: 6.2 MB (6165080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb10576055102ea3da48a1a509a1c8ce78806f4990611441c5cca27220dfb27c`  
		Last Modified: Wed, 04 Jun 2025 18:12:27 GMT  
		Size: 27.3 MB (27310193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2e075d6a39c2e3a6c30c8e07b3b38e0d29ea3629d6663c77249ebfc9281cf6`  
		Last Modified: Wed, 04 Jun 2025 18:12:25 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:8a6212458c645ed6eb7eab17630af2c7dc2403fadc68e1af31caa1e0f06d63d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15694212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5361e49c13ff6ca2d9029a6c42c63119fa3534e5e20405a84d5b8588b99985`

```dockerfile
```

-	Layers:
	-	`sha256:a70313d21a6ac45dcd74a68407351d9d9af7248a18d3c9fa4cb0b0f7cb41fac3`  
		Last Modified: Wed, 04 Jun 2025 18:07:55 GMT  
		Size: 15.7 MB (15671581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b604d8b447ce361eeb0fd9bb8915ada5b0f62c89d7d224d87ae5bc7fd0386f66`  
		Last Modified: Wed, 04 Jun 2025 18:07:56 GMT  
		Size: 22.6 KB (22631 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-bullseye` - linux; 386

```console
$ docker pull python@sha256:0488976ca9bf64675acf3eec1051b797e6716d152d360c544ccf3b19e59d9173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360312865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5429f860bcfef5944a1e7ee57715393b85305d3c2ab5e077229134e651c10042`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_VERSION=3.13.4
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_SHA256=27b15a797562a2971dce3ffe31bb216042ce0b995b39d768cf15f784cc757365
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:e516fc486459913e83d7e1f35cc45b6e3bed5cabe1eab9f1598665e153a14d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 54.7 MB (54690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e7c1ed34c380b4c9e9f08e94b0f7b9bf90a0e8c42de246cb4b2159e2126fef`  
		Last Modified: Wed, 11 Jun 2025 00:00:47 GMT  
		Size: 16.3 MB (16268617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3a34392e433938214bbf2cba34365a474d819c470686803059c6d8390cf680`  
		Last Modified: Wed, 11 Jun 2025 01:13:31 GMT  
		Size: 56.0 MB (56049939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fc14c21031cb8eae2e7bca81acab0fca46817b5d8a4fa7fbfb97ff76557da5`  
		Last Modified: Wed, 11 Jun 2025 02:14:17 GMT  
		Size: 200.0 MB (200041378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34376bfa6eabd8438e76d8b41803d0b53e1f26c431bb68ae57708a6adaabce1b`  
		Last Modified: Wed, 11 Jun 2025 02:36:49 GMT  
		Size: 6.4 MB (6441675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dcfddaf6350a3c710c27dde48d86642303506b0b4437ed4a9e1db5015ed85b`  
		Last Modified: Wed, 11 Jun 2025 02:36:50 GMT  
		Size: 26.8 MB (26820994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb8b7063418af7bd8aec22dbf98c216e1b920d338ff2953f74a271648c425ac`  
		Last Modified: Wed, 11 Jun 2025 02:36:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:d83f596baeabdc70cf62e612e55234d1d9c4ddc8b81ca316da42e5531d2f3deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15970809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b49e4ff127e4fa133ea34d0dda61a53d7a8a93daf14e25790fcdeb38c6350f4`

```dockerfile
```

-	Layers:
	-	`sha256:9b3fabbb7c7e1e02e152cc0e92d457008d63da5b5f4a4edd287c67642321e7d8`  
		Last Modified: Wed, 11 Jun 2025 06:07:18 GMT  
		Size: 15.9 MB (15948348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1018750c57d6a2cb4394ff28e5b758afa7ca4489ee204f14b280fca31cb069fd`  
		Last Modified: Wed, 11 Jun 2025 06:07:19 GMT  
		Size: 22.5 KB (22461 bytes)  
		MIME: application/vnd.in-toto+json
