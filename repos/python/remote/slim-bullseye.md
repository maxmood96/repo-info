## `python:slim-bullseye`

```console
$ docker pull python@sha256:2a20c1f82dae5a97635baa7ab32210efa0684f2677cf4d94a57ca9d86c0d0c6c
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

### `python:slim-bullseye` - linux; amd64

```console
$ docker pull python@sha256:8b59637e793eb5dbb35af19765fa5ff30dbf2785f18e8e3f91e1f6ebe37449c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43841459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3cb2c94780ad49a8d75861a37b58eb906bdbf1bb9057742efa2627a7d32d56`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 18 Oct 2024 23:23:40 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_VERSION=3.13.0
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328edec447c1274d1652ee1c8632c2e515009903cba12836ada5621027817f65`  
		Last Modified: Tue, 03 Dec 2024 02:27:16 GMT  
		Size: 871.2 KB (871219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9bb6772019971021080e658b97cadc22740555d7fa05dde24bdea39687275d`  
		Last Modified: Tue, 03 Dec 2024 02:27:17 GMT  
		Size: 12.7 MB (12717347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bd0dbb69c80c4a3768a3b1931d32c6176037bcd9a1ba4f2bf93d1e3c02975c`  
		Last Modified: Tue, 03 Dec 2024 02:27:16 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:af7da76b428f86d1d06f26c2aacaf390f1f854f0fb3ba42ead6a5668481bdfce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60499c469aea30d7f89b48d58295e781b11eed7d820c56e1b438096caa80e9f`

```dockerfile
```

-	Layers:
	-	`sha256:475fb857250f1e55f7e84bf792a85dd27b104bb07aac0c673dccfbbb1e0fe5a3`  
		Last Modified: Tue, 03 Dec 2024 02:27:16 GMT  
		Size: 2.7 MB (2705275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d1dd4a55e339278d02249c546e676a0ad10da54428a6001d7a7c7a10f344e52`  
		Last Modified: Tue, 03 Dec 2024 02:27:16 GMT  
		Size: 21.3 KB (21337 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-bullseye` - linux; arm variant v7

```console
$ docker pull python@sha256:cc7aff41d49e5ccb1c4d63690fea3e2a06d66ed37cce7ad7fc455571372bf493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39314509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7cb666fb1ebd8d55c9e92b578930eb576d69f688789eafb935aec45b63e305`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 18 Oct 2024 23:23:40 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["bash"]
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_VERSION=3.13.0
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8deebcec1997579aa5e218c8e5912ec0c765c9746854ee19b1146ff54a71e4fd`  
		Last Modified: Wed, 13 Nov 2024 02:08:11 GMT  
		Size: 837.0 KB (837002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838a16b0117eb0e4108273712dda75b981dd7825df59e191d727ff5ef63cbd87`  
		Last Modified: Wed, 13 Nov 2024 03:03:17 GMT  
		Size: 11.9 MB (11868000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b3bdbbf675e9269bb66ebe2a11e921a24c61a5daf12e60b02a348daa9f77de`  
		Last Modified: Wed, 13 Nov 2024 03:03:16 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:b9e842127d9e6709aa072eeef8152aa5d3a9f23a7f5413117cf6431e46a16238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1505e0e9160d23e3780677aba18d884ec5e41b3228913031f1e8203fa851610`

```dockerfile
```

-	Layers:
	-	`sha256:cdcdc3eb46a59bf6ff95c5e605f0805754b6fe8fc4f832f1d6d7002746fb586e`  
		Last Modified: Wed, 13 Nov 2024 03:03:16 GMT  
		Size: 2.7 MB (2709394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a24c68881b5ff95e9a4ace216eef2b822f408c7ff371167e2c63f707138b664a`  
		Last Modified: Wed, 13 Nov 2024 03:03:16 GMT  
		Size: 21.4 KB (21438 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull python@sha256:7972c7a6833b5ad75e3cb8956c7f9ce9ab5649a2e6a0f57330558b93de577c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43685783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2653a5466178b6959cef02db631ad62b159c0d9d7639f9b33f175b63c41f5e25`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 18 Oct 2024 23:23:40 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["bash"]
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_VERSION=3.13.0
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25411f28c67aaa8738cb8af4664785810b6944d306c75a217d77fc60d4e0df25`  
		Last Modified: Tue, 12 Nov 2024 20:40:28 GMT  
		Size: 859.2 KB (859233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20a29182444861be62c0c43c7700a8d27b24da47aa8fc5364ad9800bc744aec`  
		Last Modified: Tue, 12 Nov 2024 21:20:06 GMT  
		Size: 12.7 MB (12734701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec355efb77354f0ee61ea0fce26346e15f8a82a4549d6608a01a6145373e1aa3`  
		Last Modified: Tue, 12 Nov 2024 21:20:05 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:654ebac8d85f860358bd75d963a49faf8eefc787a82a7814c3730611c02c5d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2728879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4a57c0322d1a6bca3dafc18237e6233e0270778175e0775c58c673a4fdfb5a`

```dockerfile
```

-	Layers:
	-	`sha256:61a9c1c24891fa1f1f704a87ed35e1b18de6a07b5ab516fc651cc812d336ae99`  
		Last Modified: Tue, 12 Nov 2024 21:20:05 GMT  
		Size: 2.7 MB (2707408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd9c412b25efaa7f6424dca927567b0aeba421e548f4b4e4c22ae4b9b85dbecc`  
		Last Modified: Tue, 12 Nov 2024 21:20:05 GMT  
		Size: 21.5 KB (21471 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-bullseye` - linux; 386

```console
$ docker pull python@sha256:574e24ef493db8833d410c4fe083623b0ab82ea1d9f691359d5f9fd21b1cefea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44924733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d048fa78ddbf14dce490d0be5d36f8367c23a30628a59c1a45e85255915e3d`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 18 Oct 2024 23:23:40 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_VERSION=3.13.0
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:c321449a7780a0f6febb0c1425384629e366cd30dd2d0d9cab29fc6e33f6955c`  
		Last Modified: Tue, 03 Dec 2024 01:27:12 GMT  
		Size: 31.2 MB (31179058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf59384ac166c1d5a2cde89482adbd2f6650660ba9f8293eb8dccbf2eaee346`  
		Last Modified: Tue, 03 Dec 2024 02:48:21 GMT  
		Size: 884.1 KB (884055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d23df0bf3983c4cfd304d0eb38cacc6f0a62768de3ddf2f2b37d6c6bd847a40`  
		Last Modified: Tue, 03 Dec 2024 02:48:22 GMT  
		Size: 12.9 MB (12861371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861f4af8332eddf68f509efa91dd413649695117f09f9152f9d9ab86f4304f76`  
		Last Modified: Tue, 03 Dec 2024 02:48:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-bullseye` - unknown; unknown

```console
$ docker pull python@sha256:7f3ee5c2eb30afe1f95368e22b3ec35501dc887bd1d1d433c885e085b6ac8a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2723687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4585676775fc872792eb0baf79ab342c1f4f7499b4cf9d8b31d9836f337a08`

```dockerfile
```

-	Layers:
	-	`sha256:caf108dabc18bc254291f3c8baad64de62029b2fedb45d7d2ebc750b58522be4`  
		Last Modified: Tue, 03 Dec 2024 02:48:21 GMT  
		Size: 2.7 MB (2702386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a79109b452247c769f78d1f685acadea8f7acfeb667a5b711e70eb8c03568b2`  
		Last Modified: Tue, 03 Dec 2024 02:48:21 GMT  
		Size: 21.3 KB (21301 bytes)  
		MIME: application/vnd.in-toto+json
