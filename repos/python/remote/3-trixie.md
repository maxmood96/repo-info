## `python:3-trixie`

```console
$ docker pull python@sha256:ac6bf6a345348823afe0c5f729e623ac51728e59c0053096aa572d5d915c451f
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

### `python:3-trixie` - linux; amd64

```console
$ docker pull python@sha256:15cfe7526c99021489a9564fa1808413ac88b68ab2bc0ccc7ba34b26718d0d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.8 MB (411820651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fd9a3ce5de4d2b5ac35306a207bf24345ec15006cf91ef7b3458a8f78da7eb`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	apt-get dist-clean # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PYTHON_VERSION=3.13.7
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PYTHON_SHA256=5462f9099dfd30e238def83c71d91897d8caa5ff6ebc7a50f14d4802cdaaa79a
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e4db86de6eba33869491caa7946b80dd71c255f1940e96a9f755cc2b1f3829`  
		Last Modified: Tue, 12 Aug 2025 22:14:12 GMT  
		Size: 25.6 MB (25612940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea45766c6449310ca2fc621a7e00bedb4b9b803a7fbfe2607efce6d2e07e435`  
		Last Modified: Tue, 12 Aug 2025 22:15:03 GMT  
		Size: 67.8 MB (67777316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb1455cf185ce395d378e9a520710caec9909f11d6f9c69d28d3f73c50f2d23`  
		Last Modified: Tue, 12 Aug 2025 22:50:39 GMT  
		Size: 235.8 MB (235800478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d622b1dca92a1bff6997b50744603cfe2c3ff963d49d1d673ba465f4a42c3fcd`  
		Last Modified: Fri, 15 Aug 2025 22:16:47 GMT  
		Size: 6.1 MB (6096774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad72fce423fc3c58b412c53eacabd1610851730252f5ee57525cdb08df25aa36`  
		Last Modified: Fri, 15 Aug 2025 22:16:49 GMT  
		Size: 27.3 MB (27254612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f8f98927f6fd501ce40652d02ecc721a637e1a8b1f8b34ca3543011e99a7ee`  
		Last Modified: Fri, 15 Aug 2025 22:16:46 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-trixie` - unknown; unknown

```console
$ docker pull python@sha256:81b278f1e7a0ae659f9f579ea090609ffebc7db2c880d08523628ea55afd1127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17769170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d155bb9d51dfd26d62b9db2b166766e57699f23cdda614d68726e90ff6d8360`

```dockerfile
```

-	Layers:
	-	`sha256:16b658ee8eaac37d4358faf07c297b5b246a954c656601803d83add2b996e152`  
		Last Modified: Sat, 16 Aug 2025 00:06:34 GMT  
		Size: 17.7 MB (17745551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:758adc61cfb5ab5d7088375e9b23b8eb0035cccd1701c99acea965a4d72ecf32`  
		Last Modified: Sat, 16 Aug 2025 00:06:35 GMT  
		Size: 23.6 KB (23619 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-trixie` - linux; arm variant v5

```console
$ docker pull python@sha256:a5fce64bf63beeda12187b78fadc3419a2006f1d5eee9bbbf4f511753860243d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.3 MB (374332183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f45d8fd0a9fd7224af8452f6b0c57f96d7f4f4316f01095c11295a54c10649`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	apt-get dist-clean # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PYTHON_VERSION=3.13.7
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PYTHON_SHA256=5462f9099dfd30e238def83c71d91897d8caa5ff6ebc7a50f14d4802cdaaa79a
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:49b34b9ef926ce7ed8f011fe61446ff5495accfded522a04a8414730759ac407`  
		Last Modified: Tue, 12 Aug 2025 20:49:02 GMT  
		Size: 47.4 MB (47442425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10345871b22cfbefdba6d9f2d575fe7ebd340d456d55037a519d266903c1f87a`  
		Last Modified: Wed, 13 Aug 2025 00:01:36 GMT  
		Size: 24.3 MB (24338768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08aa2b20bf2d33c358d141989badced2a336e24163718df277bd1fffd0bce46c`  
		Last Modified: Wed, 13 Aug 2025 14:14:52 GMT  
		Size: 65.3 MB (65319013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a918cc6f34461032d9e2cd34bd173bec69c69070075ea1707b4ab36b71c15fb`  
		Last Modified: Wed, 13 Aug 2025 15:07:16 GMT  
		Size: 205.3 MB (205274291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745b3d227d6d2f771385fbc16483519aaa87e372d37bfa8d154aecb4dd73ba13`  
		Last Modified: Wed, 13 Aug 2025 17:56:46 GMT  
		Size: 5.8 MB (5808665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523c00b39b5ae1c30d33544a93247075a4b2aea630c1f6f4d452bfe4faea8ed0`  
		Last Modified: Fri, 15 Aug 2025 23:40:43 GMT  
		Size: 26.1 MB (26148771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb0f7bdea8c82f4031f514dd8df5fbe9b56d56f3cf6d82cb07abec78ef30f3c`  
		Last Modified: Fri, 15 Aug 2025 23:40:42 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-trixie` - unknown; unknown

```console
$ docker pull python@sha256:f1d291b57bd2817b36186c2f3f182fbdf78367d00b8f6b3d0816314149bc5a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17531560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec29ea5ec9929bae3ee053888582ce19d380af56f48e6373b329d29ef4dcf8cf`

```dockerfile
```

-	Layers:
	-	`sha256:7302eb9d9898c15d606a37308d19d699965c182c878dd627ee5bca107af28124`  
		Last Modified: Sat, 16 Aug 2025 00:07:54 GMT  
		Size: 17.5 MB (17507807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54496b836f4dd10a93443492b037258abab474758e5b292542b7681c1ee3c9fa`  
		Last Modified: Sat, 16 Aug 2025 00:07:55 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-trixie` - linux; arm variant v7

```console
$ docker pull python@sha256:3b3eb39afa3b3436a32e5d2cca7d053328cc09365c251fe717ce6c510f7f2521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.5 MB (356489580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b1f798e7343c8c80a4c924394cb60121e8241d82c5d6e00bfa19ea94f62acc`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	apt-get dist-clean # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PYTHON_VERSION=3.13.7
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PYTHON_SHA256=5462f9099dfd30e238def83c71d91897d8caa5ff6ebc7a50f14d4802cdaaa79a
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:58382c67f397ebdc005890f56dc436f7798aeeee2e0d603ba02e89d6243c138b`  
		Last Modified: Tue, 12 Aug 2025 20:51:59 GMT  
		Size: 45.7 MB (45712631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72873bc1bfa1e9338237d9573d1640f6647f61a1636bbd71d8128d16503087`  
		Last Modified: Wed, 13 Aug 2025 00:16:54 GMT  
		Size: 23.6 MB (23613045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe0a58e6c2887b271354fa2e1067ff7e829f063163f76c4a3d4f1da179eb22e`  
		Last Modified: Wed, 13 Aug 2025 06:50:21 GMT  
		Size: 62.7 MB (62718501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec56b61521700d996402c22c24c12a3a452e3a426cc9001df0aa805a0dab6b8`  
		Last Modified: Wed, 13 Aug 2025 15:08:05 GMT  
		Size: 192.8 MB (192840920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8f0d7017d8803ed4b84d5e203d749d9de7d9165d853af4c0e675c4241c9788`  
		Last Modified: Wed, 13 Aug 2025 23:57:16 GMT  
		Size: 5.5 MB (5492621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6dfbb3986235a58b370491541a925feaccd7cc17d57bae3c8198a370d81690`  
		Last Modified: Fri, 15 Aug 2025 23:40:03 GMT  
		Size: 26.1 MB (26111611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae21a747e9eec3d49feece6467c2dfde6f600f1b4822bff2fc71fd406f0ba5b`  
		Last Modified: Fri, 15 Aug 2025 23:40:00 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-trixie` - unknown; unknown

```console
$ docker pull python@sha256:3ac53ddc033744e61040f0045a4849ad8fca1c7c2b5ac704e55f1d151ae48857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17537386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0d266d4b20a69c878bd3008c431bedc13402eeb64a1ae3d936e941556b9049`

```dockerfile
```

-	Layers:
	-	`sha256:b95fd411f68e20f7bd46b2a2619a0006491cbb7266e55860e4946a502bc65bee`  
		Last Modified: Sat, 16 Aug 2025 00:08:11 GMT  
		Size: 17.5 MB (17513633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8546047ca4271e3b806fad123078f103909a17a75b1fbcbb2c72a22c2a3fd66`  
		Last Modified: Sat, 16 Aug 2025 00:08:12 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-trixie` - linux; arm64 variant v8

```console
$ docker pull python@sha256:e5432b269010193f98c0a8a9871c196edf449935848d7ca8eede435b064fdf25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.0 MB (400963419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5a62077b3ba3112433fb0b2d395609252f1432c69edaf4965b8c60ac61d4f3`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	apt-get dist-clean # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PYTHON_VERSION=3.13.7
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PYTHON_SHA256=5462f9099dfd30e238def83c71d91897d8caa5ff6ebc7a50f14d4802cdaaa79a
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9923852056eb09462c3344515191318e7aa33ff28057c946bc41a414ee57df0b`  
		Last Modified: Wed, 13 Aug 2025 07:30:07 GMT  
		Size: 25.0 MB (25014610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcc8bff74cbeacbac9c6869b6a9def273b93cc67de196b347688de2a9185de0`  
		Last Modified: Wed, 13 Aug 2025 15:31:50 GMT  
		Size: 67.6 MB (67593628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997d2d68e2fc83df067d8e29a4a06bab06bb202146e47bac816a352ad1d30c04`  
		Last Modified: Wed, 13 Aug 2025 23:52:34 GMT  
		Size: 226.0 MB (226017512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8022fef72bf61f9f598f33e085eb845cfd6e886fa79f1d57cb219b64197f103`  
		Last Modified: Fri, 15 Aug 2025 23:01:54 GMT  
		Size: 6.2 MB (6202190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e583365591e70cc5c12133f5d6f489e00229c0fa786fcaefa161ff1e7a4b596`  
		Last Modified: Fri, 15 Aug 2025 23:01:55 GMT  
		Size: 26.5 MB (26493626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bad67af72c3141901cb5ebd056a24f734c4b0acccff64c3bb5fdce532d89ea`  
		Last Modified: Fri, 15 Aug 2025 23:01:54 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-trixie` - unknown; unknown

```console
$ docker pull python@sha256:2666d897645f71d7222d7a901a472bb85977d09f6bb11e9ccd65eaf7c67bb039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17853724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647416c5fbad7170d2287e2cba2016f2dd2bc9b54cdf08b5af475d4a4c501f86`

```dockerfile
```

-	Layers:
	-	`sha256:1624e4bcd6546b3dc3eb857bd24261d120e71449b6662e6f0886f9bdd8c5c1d4`  
		Last Modified: Sat, 16 Aug 2025 00:07:20 GMT  
		Size: 17.8 MB (17829923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f8fda65c85609877beba9d9b73d233c3f4c51533769cfa514368411b5120ad1`  
		Last Modified: Sat, 16 Aug 2025 00:07:21 GMT  
		Size: 23.8 KB (23801 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-trixie` - linux; 386

```console
$ docker pull python@sha256:bd5c88005486e760ac35889dfcdb994cb39e0059b49523b83de20da3c47cf836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.0 MB (419985800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a677c739a8a8895b1bf5e7d3fdf55153bd5986dcbc413e3e788258831d6a1`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	apt-get dist-clean # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PYTHON_VERSION=3.13.7
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PYTHON_SHA256=5462f9099dfd30e238def83c71d91897d8caa5ff6ebc7a50f14d4802cdaaa79a
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:3d9f8c7ff550056ffe2cca57d7110ae0306e74220a891574e97ddc10ba49823d`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 50.8 MB (50794258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde29e7bc69fcf496b5e5df92d7d82da6ff9f4877784085c4dcba73f6ee6a1ea`  
		Last Modified: Tue, 12 Aug 2025 21:20:38 GMT  
		Size: 26.8 MB (26772559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd9904337df106e0852d247e06047929e66d5097f2d2c13861e2e31ecc63f4b`  
		Last Modified: Tue, 12 Aug 2025 22:15:57 GMT  
		Size: 69.8 MB (69794753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99aa8af494884aa1d142f9bd1267bf4dbbd07ee9c8d0e78f024adb5f20f72f78`  
		Last Modified: Tue, 12 Aug 2025 23:13:52 GMT  
		Size: 239.9 MB (239887207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7abc0a8715ed3ea8610f1d1cb9bce367c64910da756847961dce6f36777973`  
		Last Modified: Fri, 15 Aug 2025 22:19:34 GMT  
		Size: 6.5 MB (6459398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46089032d859f80eb8881130942bc8662ec0e6243fd1bdb9e23a2fdf94629dcf`  
		Last Modified: Fri, 15 Aug 2025 22:19:38 GMT  
		Size: 26.3 MB (26277369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c344522f98a2e5f488bdeeed48de3d39cd1bcf2a1aa443cb8aad93a7f6bc166`  
		Last Modified: Fri, 15 Aug 2025 22:19:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-trixie` - unknown; unknown

```console
$ docker pull python@sha256:a34120bd19797fb6dde6ea11eab64f637e0baaea274b18ced51eb1e512733f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17738644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0eb139cb4fd168e440363bfe79ef39b15ff659d6cc4d83d7ae2532f12939cf4`

```dockerfile
```

-	Layers:
	-	`sha256:3f78a9cd5a2cf023d0ed4a77b59249320e599db6d51c2463b3935ff883925048`  
		Last Modified: Sat, 16 Aug 2025 00:07:37 GMT  
		Size: 17.7 MB (17715081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ca522f1a896ad65774c79197a23538b3fd3f7a2efd621b6d2873b1d8837d3ab`  
		Last Modified: Sat, 16 Aug 2025 00:07:38 GMT  
		Size: 23.6 KB (23563 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-trixie` - linux; ppc64le

```console
$ docker pull python@sha256:ae8d9b5d0371ef0c12fdd4723f88bb475995ed4763d4d1259d4742a514ffd750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.2 MB (418242605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d341e414f02d299c9a4a58c8cec663c51bfba7f7d623781cfd09751ad9e0fe26`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_VERSION=3.13.6
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_SHA256=17ba5508819d8736a14fbfc47d36e184946a877851b2e9c4b6c43acb44a3b104
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a327675583423e2c44eae4c02a88be15dbeac36073deb88700ba487e0c0e35`  
		Last Modified: Wed, 13 Aug 2025 15:15:16 GMT  
		Size: 27.0 MB (26992868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf20d9e1e5f16d7552d637dd4a12484b22e52928311f81dd13c82b6838c2ae7`  
		Last Modified: Wed, 13 Aug 2025 21:23:59 GMT  
		Size: 73.0 MB (73018659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e609a63b79cb97e868edf62a4c9454838befd7ede70ebc96840a505bc31e1518`  
		Last Modified: Thu, 14 Aug 2025 04:25:41 GMT  
		Size: 231.0 MB (231013234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119bb0022394856e5451a59eff85bc30bd45abbb2934c0890d4db8985b7e9f72`  
		Last Modified: Thu, 14 Aug 2025 14:15:11 GMT  
		Size: 6.8 MB (6826223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b2e0e84bd9f873681f88b6b8fc7e3c7d9aa2ca1f43a509aed7f60be818ce76`  
		Last Modified: Thu, 14 Aug 2025 14:55:10 GMT  
		Size: 27.3 MB (27287987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf571557f1b04035c2539fb698c70116e295844140754f720b788880f2c0ac0`  
		Last Modified: Thu, 14 Aug 2025 14:55:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-trixie` - unknown; unknown

```console
$ docker pull python@sha256:962dde6226536f37dca9c53e09de165ee7025ae6b62017a5a679a12240f86e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17754955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a48ff7159877b83eb7756a0fb19635c18f24a9cc63ec9e7a3e1dbcb21e4b94`

```dockerfile
```

-	Layers:
	-	`sha256:d18c196208d51043e203232e1aeb78f144e2d79f18e0b6f8273dbb2b7a717e61`  
		Last Modified: Thu, 14 Aug 2025 15:09:02 GMT  
		Size: 17.7 MB (17731264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f082bd4bc5bdfbdaeff337237310a6d4819dcbac9165235b55629adc74d0f2`  
		Last Modified: Thu, 14 Aug 2025 15:09:04 GMT  
		Size: 23.7 KB (23691 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-trixie` - linux; s390x

```console
$ docker pull python@sha256:c3125cd1a3208c6223ca462122792852ccb9af83f726423c480d559b6a452840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.4 MB (384373690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34466c14d4686b23ac79d935f59e06ec7eee60c42a2a4d48a43d6a3e5eed961`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_VERSION=3.13.6
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_SHA256=17ba5508819d8736a14fbfc47d36e184946a877851b2e9c4b6c43acb44a3b104
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47181ddd75754adfc74e4f58b4a898ec33ad906976b71219b567efd19470677`  
		Last Modified: Wed, 13 Aug 2025 03:27:04 GMT  
		Size: 26.8 MB (26779580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415f63d435cf750f4bda1af6afa07ce9f812fa19c74e6f9f050da85f47eb36e7`  
		Last Modified: Wed, 13 Aug 2025 17:21:16 GMT  
		Size: 68.6 MB (68619998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0559cbb94826f8b1e5c377d0a644ba7cd24eee336fc5523a414d8ad448427fe2`  
		Last Modified: Wed, 13 Aug 2025 17:19:38 GMT  
		Size: 206.4 MB (206400871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c504590d5599ba0f4b9ab55589ecb14e3a4e56ebf03db4c033e0873a50e301`  
		Last Modified: Wed, 13 Aug 2025 23:51:31 GMT  
		Size: 6.3 MB (6334805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ab3c98d73e5e6468028af2ac8db0b1d5046f536a7f18ec55ed9958ee6b688b`  
		Last Modified: Thu, 14 Aug 2025 00:19:00 GMT  
		Size: 26.9 MB (26893026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a948bd87575ff9b96ce7cfe7236ba40a5e09c33651a7ab0e55f3b49e7bea66`  
		Last Modified: Thu, 14 Aug 2025 00:18:49 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-trixie` - unknown; unknown

```console
$ docker pull python@sha256:be1d2c59cf7b5113ff112b46d13d616f542f72622d6572c30d38b2aaa117b7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17546385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652980219607b46632108b1d2c413a58e89de5da1f8a9374552a0a9e288dcd5c`

```dockerfile
```

-	Layers:
	-	`sha256:f40fac31c2f4f375403c273c3bf523cd24458ee9828049e64f66cbfec4df3465`  
		Last Modified: Thu, 14 Aug 2025 03:07:41 GMT  
		Size: 17.5 MB (17522766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336dc6a30e594e9fce0ae24bd4236c1153bd80f7133b30e645d73d5f1e091267`  
		Last Modified: Thu, 14 Aug 2025 03:07:42 GMT  
		Size: 23.6 KB (23619 bytes)  
		MIME: application/vnd.in-toto+json
