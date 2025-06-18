## `hylang:1-python3.14-rc-bullseye`

```console
$ docker pull hylang@sha256:38b218c69199594b8df4768268105a60c0c183a1256c1f58c4884ecf96e3729f
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

### `hylang:1-python3.14-rc-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:ad8e1a772708e8c084152d0ea2848dc6cb0e512d867e7328077efa47f237120f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50412128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c368ec4bb9ce06a8d5db2ad7c4bec6c8bfe088ef5ae1c95de8376b9fde3afb3e`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Jun 2025 21:00:47 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_VERSION=3.14.0b3
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_SHA256=c6f48bf51f01f50d87007a445dd7afe4a4c7a87ab482570be924c1ddfd0d3682
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
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
	-	`sha256:3d79ccbe0210f4986821cddffc5c7fc6551d938e282044db7571e448bde1e24a`  
		Last Modified: Tue, 10 Jun 2025 23:27:03 GMT  
		Size: 30.3 MB (30256064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221c766b20176168adaa30f3ba359e53ff22fc3e38c1d067bf0a23d64057c09f`  
		Last Modified: Wed, 18 Jun 2025 17:07:43 GMT  
		Size: 1.1 MB (1077880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ab1956b2bc1187d7cae47c6e711ed4db08b6504b58c034c6184963b10fb229`  
		Last Modified: Wed, 18 Jun 2025 17:07:44 GMT  
		Size: 13.2 MB (13236710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133143f0c2021cdda4bc84de6d99799503c8e5653339e23677be98ea822d0963`  
		Last Modified: Wed, 18 Jun 2025 17:07:43 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b02f593919a45b6572edff3a575f4f1f92f7808f52fc33e1f7a9efbb050ef53`  
		Last Modified: Wed, 18 Jun 2025 17:08:08 GMT  
		Size: 5.8 MB (5841224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:ea5d576398612e3f9775afa0a959547052c5f9a51ee2067c5a16488990bdab6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2828501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47512accdf1d21cdb55336ee5ea8a7ce8bf0c63675a02fdf84a1c82f1fdbf28c`

```dockerfile
```

-	Layers:
	-	`sha256:e29b84885204a9e7be823f183e411ba3cffbc2dd1a7661fda815945668b4f6a0`  
		Last Modified: Wed, 18 Jun 2025 20:19:33 GMT  
		Size: 2.8 MB (2820501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1d564385faed9e90718242b7031547af2d4ea0fab3b604c63448d7cb87b5cb`  
		Last Modified: Wed, 18 Jun 2025 20:19:34 GMT  
		Size: 8.0 KB (8000 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:1908b15124eddb114cd514d55b8d9b05f884f3831271f86d309d5b3c07d4eddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44814026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0375e4cd3e6fbdc7d7ad67398f06397655a9e1a80533d6840a14f0d4e66e7905`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Jun 2025 21:00:47 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_VERSION=3.14.0b3
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_SHA256=c6f48bf51f01f50d87007a445dd7afe4a4c7a87ab482570be924c1ddfd0d3682
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
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
	-	`sha256:254beacf3f323cf99977d539dcb720dc371b362af3a11b68a1c46f29aa86d29f`  
		Last Modified: Tue, 10 Jun 2025 22:48:19 GMT  
		Size: 25.5 MB (25544195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080407019a5dcb8855a7e8215c3bceb518746bb6209631801c2214b4da573cbd`  
		Last Modified: Wed, 11 Jun 2025 07:49:10 GMT  
		Size: 1.0 MB (1042896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a30ab8af229d66c83a0063369d8495e3cb3d1ca6e5c1e48578c5b6c385dc32f`  
		Last Modified: Wed, 18 Jun 2025 18:18:39 GMT  
		Size: 12.4 MB (12385510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b4996e04f94212d900099a6e9162a03848bfec737100ccf2a408d11720bff0`  
		Last Modified: Wed, 18 Jun 2025 18:18:36 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc071515ca6ef5d320264bb098bab1094a845849c30db941ad5ca9d7e3058a2`  
		Last Modified: Wed, 18 Jun 2025 18:11:23 GMT  
		Size: 5.8 MB (5841175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:49ac3512d97d7d2af94bd881ce57a64171ba178c05d16c1c81bb19cadda4f98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2830823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8940cffb57d35d54fab58297da18c11a9c7e40a02247d779c76957fc286c7d9e`

```dockerfile
```

-	Layers:
	-	`sha256:b8c94a80dbb69582aecfe1680afd6770a14d66c9de7a254a540c2b90abbde2f7`  
		Last Modified: Wed, 18 Jun 2025 20:19:43 GMT  
		Size: 2.8 MB (2822746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc79f5f26ecd24399f4bff79a464681941fa7b167f29ba3d96ed5b36b1482129`  
		Last Modified: Wed, 18 Jun 2025 20:19:44 GMT  
		Size: 8.1 KB (8077 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:b5e156e1619fad1047bede7bb397347e481c5ec5904699ad85d652e2cb46cbdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48918340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b92f7014476632be8432e4858469e9110a8c88dd3b7f28c737822bb58a57cbb`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Jun 2025 21:00:47 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_VERSION=3.14.0b3
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_SHA256=c6f48bf51f01f50d87007a445dd7afe4a4c7a87ab482570be924c1ddfd0d3682
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
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
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2756ee3ce24c04f89bc12da8cd6d6417a6af1342c0c845b0d514098b0180fd`  
		Last Modified: Fri, 13 Jun 2025 01:35:30 GMT  
		Size: 1.1 MB (1065724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd64230e86c567ef52e3f6c0bd302985b61332a0748d4b47bf0ba6a6bf7ff28e`  
		Last Modified: Wed, 18 Jun 2025 17:30:38 GMT  
		Size: 13.3 MB (13267080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cad93ca8331b723fd4c17a012c2a34e044b07ef5aa27484c2369087bfc4edac`  
		Last Modified: Wed, 18 Jun 2025 17:30:37 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1363906f0cdedab9fac2e2781243b4f7840bdd6b3bcbf2fbd95eb59c9dd8b956`  
		Last Modified: Wed, 18 Jun 2025 18:08:43 GMT  
		Size: 5.8 MB (5841101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:e882d67d84651381b54ae1ed96c05ac6f03172e233e280407a528fe8143b5a2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2828865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8631b2f91570bf5f6bf35732ac06f8e429fef8ffce99d59a7abac3b71de183be`

```dockerfile
```

-	Layers:
	-	`sha256:7ca45edd4d4f689a0ce7bae933de336a3305a5d504e57175b2762c3bca58b979`  
		Last Modified: Wed, 18 Jun 2025 20:19:48 GMT  
		Size: 2.8 MB (2820760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fead6eedd8107a328ade1bc538017dd188fc657523ac5dc4c4cd651212c2c8b`  
		Last Modified: Wed, 18 Jun 2025 20:19:49 GMT  
		Size: 8.1 KB (8105 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:c57f98fe4c2c3b248845139a977910e54c582cce9142b4e34202cf44c71e2510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51523222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b527724e41ec189dcbd20c8c28b86546aca625b57c5a37259269dd9c2ec1a2ae`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Jun 2025 21:00:47 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_VERSION=3.14.0b3
# Wed, 04 Jun 2025 21:00:47 GMT
ENV PYTHON_SHA256=c6f48bf51f01f50d87007a445dd7afe4a4c7a87ab482570be924c1ddfd0d3682
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
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
	-	`sha256:1294ecac50b0f4fe7018ad5e666e6e3c43bd85fbdc4ff68322834fcc70904e3c`  
		Last Modified: Tue, 10 Jun 2025 23:26:42 GMT  
		Size: 31.2 MB (31189682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710dc4702217c07e3a26fb215eba395fdfa78d7731e690dc13558f714992b635`  
		Last Modified: Wed, 18 Jun 2025 16:55:28 GMT  
		Size: 1.1 MB (1090526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c5d93685a3bb4433d707c3ae357a59c7a53a49fe764a54901d1828498e0aff`  
		Last Modified: Wed, 18 Jun 2025 16:55:30 GMT  
		Size: 13.4 MB (13401611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e991244b71ef273d2768651cdc5457165c56ea7247f472ea2cb236a0af32d6`  
		Last Modified: Wed, 18 Jun 2025 16:55:28 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f492a72ad5d0d208fb60528372f21cc8f16dabcc8b3e9a2f0845d7bf74365b62`  
		Last Modified: Wed, 18 Jun 2025 17:08:30 GMT  
		Size: 5.8 MB (5841153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:6547d725b3e5c5e57371b9be20584bc53379cbee64e0788fdf21494086566594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2825633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110ae2c8ce0328b7f5144fdbfa946270d1d2798e66e6fe43cdeaf2a3ca929870`

```dockerfile
```

-	Layers:
	-	`sha256:90821874f4d6911bad6c9f12346bcf521d3c702a0844380393dca57cce919520`  
		Last Modified: Wed, 18 Jun 2025 20:19:54 GMT  
		Size: 2.8 MB (2817664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9a5c7b25106e38830e5a856f3da636bc2132e19824032eaca9714b8c576fdbd`  
		Last Modified: Wed, 18 Jun 2025 20:19:54 GMT  
		Size: 8.0 KB (7969 bytes)  
		MIME: application/vnd.in-toto+json
