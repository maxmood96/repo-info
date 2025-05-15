## `python:bullseye`

```console
$ docker pull python@sha256:25ed8e09377b01040c264c12ce00870b692c00abe2890ffde502e409325f210c
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

### `python:bullseye` - linux; amd64

```console
$ docker pull python@sha256:555b6dc36ec4de8f1b219696d75efe91ade2933b9a73f9226225dc476152d817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355228335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c125e35654d4bb5f936f5d361ebeec01f0d410180808e2a4bd9cc20e233a87a8`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.13.3
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68201ec6e5815a0906ce41187e7e52419a2d2c28d73d199e7612f268f81bbc35`  
		Last Modified: Mon, 28 Apr 2025 22:15:30 GMT  
		Size: 54.8 MB (54756006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ee2c8b84461fce714721ac74cb275f6aaa0de67c2aeaccb8193af9ea8b4d38`  
		Last Modified: Mon, 28 Apr 2025 23:12:29 GMT  
		Size: 197.1 MB (197107708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256942837b658e5ee5479cc15901d076add4b8f1fbc078a86cfd5670139c91f6`  
		Last Modified: Fri, 09 May 2025 23:50:46 GMT  
		Size: 6.1 MB (6051848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf4ceca432fe97cd7ae8ddacb636425c939dbe7fbf374491d1aa8ff4e77484e`  
		Last Modified: Fri, 09 May 2025 23:50:47 GMT  
		Size: 27.8 MB (27801241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583e994615cd3a9101640476b4f7dea179b31056224efc3debdea2d4eb425ebc`  
		Last Modified: Fri, 09 May 2025 23:50:46 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:bullseye` - unknown; unknown

```console
$ docker pull python@sha256:c96dc190223d9578641f5673a79cedddd10aeff50cc18ad413548d7c5d89ffd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15588734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311f011d5c2195a09afff6ad7414f73964b969f22fcedff0544bf3731b91e129`

```dockerfile
```

-	Layers:
	-	`sha256:e60bee7c51249409d8e8299c11958d2d778adbb075a343e4a45d03e8d8833fa7`  
		Last Modified: Fri, 09 May 2025 23:50:46 GMT  
		Size: 15.6 MB (15566237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1463e27063b8804447d6c64ea5903b6c4dab9fe6c8a29fe3d83cb217e53b2b10`  
		Last Modified: Fri, 09 May 2025 23:50:46 GMT  
		Size: 22.5 KB (22497 bytes)  
		MIME: application/vnd.in-toto+json

### `python:bullseye` - linux; arm variant v7

```console
$ docker pull python@sha256:65ba20c9894a67e4a168e8aa7ccf645de9e07f5d743d8f68434ae3a73e670f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.2 MB (314198940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8052c58d940f3a2495efdc07da9d80bb91dc34535ed42ad0cd3c4c8915d14080`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.13.3
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:72fa46f1d669ee2de1ffbc36b654bfe8dd0aad49156f4143a5d9edd3a5c3d559`  
		Last Modified: Mon, 28 Apr 2025 21:16:06 GMT  
		Size: 49.0 MB (49040048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de64850f276e76efd1e91be51cb4b2577218e49bf52707b1bf6de3be76028cd8`  
		Last Modified: Tue, 29 Apr 2025 03:37:44 GMT  
		Size: 14.9 MB (14879026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc4cecedb434598f97e33a3320b6af6e1676388e6c13b31f0aab4b7c9372012`  
		Last Modified: Tue, 29 Apr 2025 13:23:50 GMT  
		Size: 50.6 MB (50625161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce34362265f33a06975f249d19b3ebf3e131e052b1333868e863a53ee816bc45`  
		Last Modified: Tue, 29 Apr 2025 16:46:09 GMT  
		Size: 167.6 MB (167558886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8024284833212ec76fba32d2e679b8955fa71ec7778eeccb09e51bc56792a6`  
		Last Modified: Tue, 29 Apr 2025 23:06:34 GMT  
		Size: 5.5 MB (5461159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde8a2edb607ebc896f1615ed7b61a1cb1b1ccef74b513bbf47cabd2c417034a`  
		Last Modified: Sat, 10 May 2025 02:54:37 GMT  
		Size: 26.6 MB (26634410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddade27d2a7a4a988358706d940d2abf5958a22ac629407ec64375aff58b12f2`  
		Last Modified: Sat, 10 May 2025 02:54:36 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:bullseye` - unknown; unknown

```console
$ docker pull python@sha256:9cf877da76ffe420dcf4d4a00b53f12f2c4b58ba888c0b2b9f1443a0f1c8605a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15389686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64460f35194a16719918871e3afbcfe3d6fbd8a9b7365d6bd9605efad015a7c2`

```dockerfile
```

-	Layers:
	-	`sha256:4342a067512e63f7b128bd618e8fd2b27815aff700851287fbee904f23519ad9`  
		Last Modified: Sat, 10 May 2025 02:54:37 GMT  
		Size: 15.4 MB (15367087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a3440f06da141094a7e3260ebcdfce641f2800b3b2c7cdd524298cf1165bd76`  
		Last Modified: Sat, 10 May 2025 02:54:36 GMT  
		Size: 22.6 KB (22599 bytes)  
		MIME: application/vnd.in-toto+json

### `python:bullseye` - linux; arm64 variant v8

```console
$ docker pull python@sha256:50511f04df6f89023f24d7e960fabf383a245e0c452ffb6ce9fefd49d0c44e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.3 MB (346345518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2612eb1aae838168c25f72fb613e1eaa88943a7bb81736ea28833cbd08a0094`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.13.3
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b10bbe754ef0579f7ae8162881d71484a39910114f01fdcee0bc53987fec1`  
		Last Modified: Tue, 29 Apr 2025 01:47:13 GMT  
		Size: 15.7 MB (15749108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b30b3b7ef57604d52a4f287f3a1202fa7094c2c34ba89e66f13f2ef75a47ae`  
		Last Modified: Tue, 29 Apr 2025 18:37:49 GMT  
		Size: 54.9 MB (54850001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356545a2ed16b26897f2a271b3f4a7d7e64a9bf9bc0c78fdf4f1386401e37428`  
		Last Modified: Wed, 30 Apr 2025 02:18:06 GMT  
		Size: 190.0 MB (190024328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5de4185ab7d55169a47f7428bd1527be6363c73e5c749d2d1311892c48bee97`  
		Last Modified: Wed, 30 Apr 2025 08:59:21 GMT  
		Size: 6.2 MB (6165132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24430a8228979e8a02a0ddca8e09ade561814c1b8f903bee9255fa593ada67d5`  
		Last Modified: Sat, 10 May 2025 01:20:18 GMT  
		Size: 27.3 MB (27310720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f8fed3c2e26c3bdc863eb36869c74c724c7d89ddbcde23e36ee2280055076f`  
		Last Modified: Sat, 10 May 2025 01:20:17 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:bullseye` - unknown; unknown

```console
$ docker pull python@sha256:84637bcbd063079fb6042323b43be891a4ae1e217a83a976761c549215030cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15591149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7653abdf641d93972c5a93b5bbc72e2b24d58a02ee1481ffbd9eaf11b0e2c585`

```dockerfile
```

-	Layers:
	-	`sha256:dd2256698eec1f9aedd6cbb95531a2107c3b1e30b53b488059937edc62d7a891`  
		Last Modified: Sat, 10 May 2025 01:20:17 GMT  
		Size: 15.6 MB (15568518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6d0ffb58701b24d0def4247e17c0122a6e72d27356be14cd81258e0261c4eb`  
		Last Modified: Sat, 10 May 2025 01:20:17 GMT  
		Size: 22.6 KB (22631 bytes)  
		MIME: application/vnd.in-toto+json

### `python:bullseye` - linux; 386

```console
$ docker pull python@sha256:4711b16f0768e5a22e8af18f1800452fd41f40c2d2cae7e6bc5b902a34590822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360271828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034bd82b6a0b958592919927ef657d420dd84c2a34c85c8c3be018c8efd5b007`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.13.3
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:4ef50a397f2c0106a3e44d1d1bae16cf52fb5e7e855c588f4098e281321c3e7b`  
		Last Modified: Mon, 28 Apr 2025 21:08:10 GMT  
		Size: 54.7 MB (54683102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbb48ef4c334135b55fe5dd328911059bfd41eec15edf03ff0ab96ca44fb6a1`  
		Last Modified: Mon, 28 Apr 2025 21:53:52 GMT  
		Size: 16.3 MB (16267399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229f9ff435d5a831802e386be1d29f22419a5d3951a76711fcdfc9f9bad0e6e3`  
		Last Modified: Mon, 28 Apr 2025 22:14:52 GMT  
		Size: 56.0 MB (56047280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ef040f15a9c521f9352beaf246f79eec04035acb8b716f343f27a2aea49563`  
		Last Modified: Mon, 28 Apr 2025 23:12:49 GMT  
		Size: 200.0 MB (200011534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264f373155d6ad62748ba0dd2b5fb930d71381afc34fec4f05aa3c1889e270ad`  
		Last Modified: Fri, 09 May 2025 23:57:53 GMT  
		Size: 6.4 MB (6441542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc628b709ed7dfe57eddb8472bb95521d5fd19d5319cd46019f45e383b93367`  
		Last Modified: Fri, 09 May 2025 23:57:54 GMT  
		Size: 26.8 MB (26820722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21670d87886e54a99e0fbc255cd8282a1b062851634afd16153b9338c0bd3b3`  
		Last Modified: Fri, 09 May 2025 23:57:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:bullseye` - unknown; unknown

```console
$ docker pull python@sha256:6938dc042fefae7726e17540b7ae35b337b6f36e42dbfd41e8f63cca59e61c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15576970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8ca168818877939f509b6aadc0cd522d6e1b3fbe4ea08e8e1c86aac95ceb51`

```dockerfile
```

-	Layers:
	-	`sha256:432501acdeaf6ddba4d928a2033290346f5f29688cc9af7bb6473049b561ee6d`  
		Last Modified: Fri, 09 May 2025 23:57:54 GMT  
		Size: 15.6 MB (15554509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a4e1ca3f1e925834630b712f4a58d2be4a683a51edb4de9463b135d769e1bbe`  
		Last Modified: Fri, 09 May 2025 23:57:53 GMT  
		Size: 22.5 KB (22461 bytes)  
		MIME: application/vnd.in-toto+json
