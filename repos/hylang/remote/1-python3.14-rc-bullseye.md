## `hylang:1-python3.14-rc-bullseye`

```console
$ docker pull hylang@sha256:2ab8edbbe99d67058a6a04646e68a78bb9aa8f5607e6632e30e042610de4aa56
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
$ docker pull hylang@sha256:f32df73ca60dc9094a4d14d36a05f191c78b028ba0e175ed3055a3522515e405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50411010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e24cf7ac242614031a15b6089a9e8716872aeccbfd7091c7f9d5f73c443906`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Jun 2025 21:00:47 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
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
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46115e567e6a2d67721f56e13271777057b5ac41a0d5809e2cc78637a4bc1ba4`  
		Last Modified: Tue, 01 Jul 2025 02:45:05 GMT  
		Size: 1.1 MB (1077881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9846c9cc470e42d2041a10bc6957c30abe4fae3d63cda05272f8fe5b0e3f4abf`  
		Last Modified: Tue, 01 Jul 2025 03:28:10 GMT  
		Size: 13.2 MB (13235635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c972ee1ff24a3817015d1d8de6157daefb660f3a63f3709db1f544b38c09244c`  
		Last Modified: Tue, 01 Jul 2025 03:28:09 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c88b6cb9fafac8a35b81e85f35319e83c57da5d92ac71dd555c875f39ba967`  
		Last Modified: Tue, 01 Jul 2025 13:22:01 GMT  
		Size: 5.8 MB (5841196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:900bbfe3b6d541d0652e46eb1cfb00e319d9fd1ea8f0e4df4f5df4c72a05a94b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2828502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11755cc0e794635127e30eeffd82c8d5e4e95f7b0b33814414c8c0545b39ea9b`

```dockerfile
```

-	Layers:
	-	`sha256:7a57123e11dbac8bce43d493a6c3ddb9f80adf89f0f51e25b03ccab99bb8409e`  
		Last Modified: Tue, 01 Jul 2025 05:19:58 GMT  
		Size: 2.8 MB (2820501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0418bcde64ae333854dcc805821ea9e931a945cf867c9a962bc45fe534c3c320`  
		Last Modified: Tue, 01 Jul 2025 05:19:59 GMT  
		Size: 8.0 KB (8001 bytes)  
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
		Last Modified: Wed, 18 Jun 2025 21:20:35 GMT  
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
$ docker pull hylang@sha256:c274e6dff7614ed6b3c39eea24a652701566c63fda230b21cc9fe76c21de39f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51524881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054c969660ba9d8c3af632762f5a62052b34dc6a6ea9d7a9c7073ba8bab0e8cd`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Jun 2025 21:00:47 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
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
	-	`sha256:40be1da6146972d9df50a98eef7b5c0f729cd95a3a38782418f354f3b9355a9a`  
		Last Modified: Tue, 01 Jul 2025 01:14:57 GMT  
		Size: 31.2 MB (31189680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a49ed2875b03420a9cd0a125f28045c57612c251609c775b1520aa47fa736d`  
		Last Modified: Tue, 01 Jul 2025 02:47:39 GMT  
		Size: 1.1 MB (1090495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2cc19a10e27c601a1faca00fd726df94e66db7678a42d7d3af1e17600c4d0c`  
		Last Modified: Tue, 01 Jul 2025 02:47:45 GMT  
		Size: 13.4 MB (13403199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87f61bac3bfea6e99c6b3427486774566535f61c63d0ab97fca5f2e26656287`  
		Last Modified: Tue, 01 Jul 2025 02:47:34 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ded2633d0f16da66a0e427c2e563a5e93ffd5bc242da36ebd6c8e19024e5fe2`  
		Last Modified: Tue, 01 Jul 2025 13:22:04 GMT  
		Size: 5.8 MB (5841257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:3a57fbc87824e6ffa72ab64622d9af36ab5b1d3bbd6abc45a41554c455fcecd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2825633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c61e9a72f14f9e9ec540deab4fd8fd1d2456806b3355282631ef11f537bf5f`

```dockerfile
```

-	Layers:
	-	`sha256:14484fcd87ff226bf50599380997f4e05e4cb2176c90f2af3ec1d009b01f9f34`  
		Last Modified: Tue, 01 Jul 2025 05:20:14 GMT  
		Size: 2.8 MB (2817664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba5854051b0a446e1012b45e165bea41dd076169516b7c64db19f5c2126203d2`  
		Last Modified: Tue, 01 Jul 2025 05:20:15 GMT  
		Size: 8.0 KB (7969 bytes)  
		MIME: application/vnd.in-toto+json
