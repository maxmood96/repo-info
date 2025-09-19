## `hylang:python3.14-rc-trixie`

```console
$ docker pull hylang@sha256:6c4a5591f1a79a9ad6e727bed55a6fa7487fbcd6dff908c88a6adfa491c6675e
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

### `hylang:python3.14-rc-trixie` - linux; amd64

```console
$ docker pull hylang@sha256:98c05be79fe24e40601ad2da97fc82414566f75017ce72aca18d5614002c654d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48972272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608c43484ac7b11c936d4766a64364b8e211fd43a3c4ad5ae811e865cb39d49f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.14.0rc3
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=646dc945e49c73a141896deda12d43f3f293fd69426774c16fc43496180e8fcd
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abf1f41fc9aea17d8dcece10938a2973015729a6e000aa9c67749346a70d21f`  
		Last Modified: Thu, 18 Sep 2025 20:18:14 GMT  
		Size: 1.3 MB (1292520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4a03bc3fb562d18d7638064318c2d081501ca9b6ad5610c1e7862af42ab71b`  
		Last Modified: Thu, 18 Sep 2025 20:18:15 GMT  
		Size: 12.2 MB (12152292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ba4c97d3a5211d55f49dc321d5670ecf5ba0db3576fd227d1a6e55878ab5ec`  
		Last Modified: Thu, 18 Sep 2025 20:18:14 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eccfbea5455d7c74b653f1edf37e73e0616a1a513dc4f0cdca9759bacad9728`  
		Last Modified: Thu, 18 Sep 2025 21:11:09 GMT  
		Size: 5.8 MB (5753714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:6938760d038b45d2d7a2465a6362c97f642e718756db0a2f6c441a57aa508ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7451612e8423aaa560b3de253ac7c7f79ddd0ea42e32bfc8fe3a089f3907dbf9`

```dockerfile
```

-	Layers:
	-	`sha256:ff7c0cc5ad5341ae861443aa5da2c7ad5c8f8f3c8956685ade887a4046f0ff8a`  
		Last Modified: Thu, 18 Sep 2025 23:19:33 GMT  
		Size: 2.2 MB (2153628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f7f1b319be8190e859fd01c94ed7302812b734a902a25268301e5a9cad3b31b`  
		Last Modified: Thu, 18 Sep 2025 23:19:34 GMT  
		Size: 8.0 KB (7976 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-trixie` - linux; arm variant v5

```console
$ docker pull hylang@sha256:fa9232f70eebaf2e58e32c5b20ba7e337c4ea84c8450c61be2a8f38a6ab406f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46801409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e882eed424576fcfd5e92dc691feede1440bc4ffd155cda1ea5a06a41a4f3475`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1757289600'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.14.0rc3
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=646dc945e49c73a141896deda12d43f3f293fd69426774c16fc43496180e8fcd
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
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
	-	`sha256:5d61fc20e756831552727f89a087e2b45b07dace604ad2cda0a2afa80ace388d`  
		Last Modified: Mon, 08 Sep 2025 21:13:29 GMT  
		Size: 27.9 MB (27941760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ede9508de272c59801e5199051ae7cc21e049c85cd44600dfcb3b7254d5a7f`  
		Last Modified: Thu, 18 Sep 2025 20:36:26 GMT  
		Size: 1.3 MB (1275434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1f4e64530105ef3cd240580c9c163a8eac304e3aa14cf79ed8b5e400d29408`  
		Last Modified: Thu, 18 Sep 2025 21:10:35 GMT  
		Size: 11.8 MB (11830182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067ef67f3216a7fce89b85b0625339bb52fcdb9fb891121b30e01c042110b69b`  
		Last Modified: Thu, 18 Sep 2025 21:10:33 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9109ef8df89c4fb1ac03680584d34d5a80b8189e437b2c83f05b401ec0cb064`  
		Last Modified: Thu, 18 Sep 2025 21:11:07 GMT  
		Size: 5.8 MB (5753782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:cc9698d1f4621228009c7d891c37506cabf901ab91d4c0e3b304d7b9395adeef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2164653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa75745f6635628c307adeddf1b33ef2da03fa00b4c6f22b6b3fd84f714d6af`

```dockerfile
```

-	Layers:
	-	`sha256:35aed1aa0959309f6f8fdabd8895d027f5ac95b7d163df9b91a35316cd922572`  
		Last Modified: Thu, 18 Sep 2025 23:19:38 GMT  
		Size: 2.2 MB (2156597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35958b5f195dbf3c30f942879da0e20422463f44378202700f81559d2cf76956`  
		Last Modified: Thu, 18 Sep 2025 23:19:39 GMT  
		Size: 8.1 KB (8056 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-trixie` - linux; arm variant v7

```console
$ docker pull hylang@sha256:a7c7e98e41d7a52a2de6324eb1e5eed4208bedd789b3ba7b3dfb1732315fcb10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44738247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ce18f6d63dea9e5c604c52c1a526cde5c39d57c1486649f8a04798f4c501f3`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.14.0rc3
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=646dc945e49c73a141896deda12d43f3f293fd69426774c16fc43496180e8fcd
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
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
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20089cd63e03f595778c6f52df01fb43da558bec67ec672ebf7f68ce3444512f`  
		Last Modified: Thu, 18 Sep 2025 20:22:06 GMT  
		Size: 1.2 MB (1247969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b03c2be4ac9a585c71cee5812bdcdfdbdabcc85db881f9eba7d788e894f2f5c`  
		Last Modified: Thu, 18 Sep 2025 20:22:07 GMT  
		Size: 11.5 MB (11528384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fe1b3a0fc904e61839a426a76fd854ce9fee50f01b30c996447cf03f5cc644`  
		Last Modified: Thu, 18 Sep 2025 20:22:06 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16629846d254c57ea8e444d2c75022f8700b5bc4cd8b1d326c46a81283c86b72`  
		Last Modified: Thu, 18 Sep 2025 21:09:51 GMT  
		Size: 5.8 MB (5753796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:b453ca24d593c6e11a93014ff5aa440f69a92717e14e768c5ab55204ba903c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6638545341d973859b5b63258250f6608dacb3ee126dceeca750f392d4bce8ca`

```dockerfile
```

-	Layers:
	-	`sha256:382c18047a4301832bfbe7d9eddb5950dd849bc8bd0c1eb0913510c710ab95b3`  
		Last Modified: Thu, 18 Sep 2025 23:19:43 GMT  
		Size: 2.2 MB (2155050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95926bcb430205a8c69d91b213291fe75824afda500d204507ca118e4d934aa9`  
		Last Modified: Thu, 18 Sep 2025 23:19:44 GMT  
		Size: 8.1 KB (8056 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-trixie` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:b2288a9cc9c2eca228583a385ec4c4c2b71e9239c868b0d32fb2361621fb7f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49225529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a981b0927aa001786fffb6e54f88ba73bd479f82ca5cbefeada2052c4f5823d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.14.0rc3
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=646dc945e49c73a141896deda12d43f3f293fd69426774c16fc43496180e8fcd
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8910461b9592c41c851fccb2d638e0b38a68dc9f6b85a1720325067bf3e71fa`  
		Last Modified: Thu, 18 Sep 2025 20:18:07 GMT  
		Size: 1.3 MB (1272876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c83553a2f14b24f4f833b9c4d7a35eac3139c4e8fa1412e3c9f8dfecc06200`  
		Last Modified: Thu, 18 Sep 2025 20:18:11 GMT  
		Size: 12.1 MB (12062031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3603d6641968e84b326efde363f741a3d97b75dbad8c08dda909a85770a345f9`  
		Last Modified: Thu, 18 Sep 2025 20:18:07 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1a214a2774e3647f1f33b8adcdff569bacaf972bcf761469d9d3c3716a0a74`  
		Last Modified: Thu, 18 Sep 2025 21:11:50 GMT  
		Size: 5.8 MB (5753740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:c9e421e3072664050a1a0150abfb83c3fcc03d1dfad4812f42b7609cb7aa99c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ceeb2635eb3be7f3be019af6c55ca086835e9f410320fe227083a44f1b681a`

```dockerfile
```

-	Layers:
	-	`sha256:c8166d579e7f102265a8b10608bf8e15af580d7ce8100e8d6b1c29b33a3e6274`  
		Last Modified: Thu, 18 Sep 2025 23:19:48 GMT  
		Size: 2.2 MB (2153894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:691ea99ca492d4819daccb3b152896a1fa0b6060ee0d4c522c86f4300f8f6e20`  
		Last Modified: Thu, 18 Sep 2025 23:19:49 GMT  
		Size: 8.1 KB (8080 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-trixie` - linux; 386

```console
$ docker pull hylang@sha256:a7d998be1f8104963d9abe7d9eba6ea75ec45f3ece98fa8912df3d3cfee9bc1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50617232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6926c5a48b8638124a99a1769549a64d8333ae0c15a858ea4ec5b3c3aac041`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.14.0rc3
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=646dc945e49c73a141896deda12d43f3f293fd69426774c16fc43496180e8fcd
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4240a46283f500f15074b0f10ca16dd88e99e21b61f430be3e9e35ccdec85e`  
		Last Modified: Thu, 18 Sep 2025 20:19:49 GMT  
		Size: 1.3 MB (1296501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db44b9045a94fec945968fdc5d692b74fc9e028be1be1353864fe5b91d87d6c4`  
		Last Modified: Thu, 18 Sep 2025 20:19:52 GMT  
		Size: 12.3 MB (12277002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b417c50346487a00257406db68ab0edfc111ec77fa554a3fe72e23223c8fd15`  
		Last Modified: Thu, 18 Sep 2025 20:19:51 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde1475cfba129052ebe29802c542eb80548684424facd0e4edcf3d74096ccf7`  
		Last Modified: Thu, 18 Sep 2025 21:10:50 GMT  
		Size: 5.8 MB (5753694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:aeccc93dbf46fb1afb5ca33e00df91a247aec6cdf08d53867911870eeff13b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3161ace967a00709bfbf807b091f2ca9bdc264d7b8d65ddfafa7a68802ad2f`

```dockerfile
```

-	Layers:
	-	`sha256:d97dd5c63e402dd32fbd19a51bb946ba43759c9ab5855d48367c7c104c094d4e`  
		Last Modified: Thu, 18 Sep 2025 23:19:53 GMT  
		Size: 2.2 MB (2150809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1478cf00c048fea2b240318558d9e7a2251e74bff73648f989e0c50b7d0d916`  
		Last Modified: Thu, 18 Sep 2025 23:19:53 GMT  
		Size: 7.9 KB (7944 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-trixie` - linux; ppc64le

```console
$ docker pull hylang@sha256:41eb7080f757912d01a9d665599a55bf0f2ef42599b9e9e2df8f1a8151d010f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53230597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04bdadd38967e3aa8d5d9b86d3bb3b10f991e084a163222171a396bcb1498af`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.14.0rc3
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=646dc945e49c73a141896deda12d43f3f293fd69426774c16fc43496180e8fcd
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5679388497b6627cd8430fb41c5fb00021ac67b801aa4c348e05bf79aa63e5b`  
		Last Modified: Thu, 18 Sep 2025 20:26:50 GMT  
		Size: 1.3 MB (1320708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163a44433528fb68180436fd6e2bc49c04c46cc7a9d37586519cb148a00ffb26`  
		Last Modified: Thu, 18 Sep 2025 20:26:59 GMT  
		Size: 12.6 MB (12561476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72102787fadf8bb8d6fdbc5ba2e58970ffe59244a93df1c8758f72a84e81af2a`  
		Last Modified: Thu, 18 Sep 2025 20:26:50 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e89a621ef4896145cf64bdb24297d387f12617ee189850834f6b53588665a6`  
		Last Modified: Thu, 18 Sep 2025 21:21:27 GMT  
		Size: 5.8 MB (5753812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:4cd9bbdc7c6265eef9edbbb3f9779c77fd7e3b780868596a228eb5f7204a655f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7adb6d4f78c91917c74a7ce11cda1a580a6095979a7a9d7ea06e92998454841f`

```dockerfile
```

-	Layers:
	-	`sha256:cb4b96a30da742824321248fb96e11ce6bee7d7f73e72427da7d4982d3f5c2ff`  
		Last Modified: Thu, 18 Sep 2025 23:19:57 GMT  
		Size: 2.2 MB (2157195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d417b0cb704b701e8baa199d178c48935728ea74fbb71094a8790ec5ad9a0eb3`  
		Last Modified: Thu, 18 Sep 2025 23:19:58 GMT  
		Size: 8.0 KB (8020 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-trixie` - linux; riscv64

```console
$ docker pull hylang@sha256:45b567c977c597561672a27966b7e7de2844cc5e6be7689d49c662b13a3879a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47457360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cbbe28e29daa35c9da787adb087b09d10f128af706966d4d569e1a5af00d87`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.14.0rc3
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=646dc945e49c73a141896deda12d43f3f293fd69426774c16fc43496180e8fcd
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
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
	-	`sha256:cbb089cb93d400be63876d795bf4b93760c44709fa7dbdf23f6c42a3cd4f37c7`  
		Last Modified: Fri, 19 Sep 2025 00:02:07 GMT  
		Size: 12.2 MB (12171639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792880b982d9081e96e54955c48320451b4eed16b175dcc2087accce795a1fa7`  
		Last Modified: Fri, 19 Sep 2025 00:02:06 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a1258b0b102fd5b2cfa043052aacf9c90da0d0fa2498bbdae5e41c7ad62cef`  
		Last Modified: Fri, 19 Sep 2025 01:27:58 GMT  
		Size: 5.8 MB (5754367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:432ed42d6493caf4edf5645e0667284cf54d15b8c215cfa87db7fc773072119f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2155586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986fc1c7c275ef4c381b9ce478c3af552905cb8cb89f55cd3f5ee1ee33038087`

```dockerfile
```

-	Layers:
	-	`sha256:5a378a40be6e6d5fc78fdc311893bda3ce4d54a97084a020a3ca8edfb8b4adf1`  
		Last Modified: Fri, 19 Sep 2025 02:18:32 GMT  
		Size: 2.1 MB (2147566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f7802bbeb62409e2ba82bc29c3c2b09fcfca9b5abafae69fb22feae267223cc`  
		Last Modified: Fri, 19 Sep 2025 02:18:32 GMT  
		Size: 8.0 KB (8020 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.14-rc-trixie` - linux; s390x

```console
$ docker pull hylang@sha256:975f11902d737268c6e3fbf330f1b54408e357f7b5e2061f7b31a249c9f61b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49093283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64517cb955959ac85948d7ab52d43f8ebb0110235551578e89e8b2be421797c6`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 Aug 2025 21:03:27 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_VERSION=3.14.0rc3
# Wed, 13 Aug 2025 21:03:27 GMT
ENV PYTHON_SHA256=646dc945e49c73a141896deda12d43f3f293fd69426774c16fc43496180e8fcd
# Wed, 13 Aug 2025 21:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f87dd9cc3688fc5bf8366b09bf31a2e452b21c7bec14488908b5bbda4823ae`  
		Last Modified: Thu, 18 Sep 2025 20:33:53 GMT  
		Size: 1.3 MB (1305071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb8f3ba1c396597c2d6ac2fcdba019597df2f1b0174236e45da77ab68de41d2`  
		Last Modified: Thu, 18 Sep 2025 20:33:58 GMT  
		Size: 12.2 MB (12201363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb36f6009d088e1f3df2149c9ab5311aa38e2bf7f8ca951c0a23f7ce0ec0dce`  
		Last Modified: Thu, 18 Sep 2025 20:33:53 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7381654997a98c19720ffddbe3cad31170f11eabf413ca8f0b20f66e5af592ea`  
		Last Modified: Thu, 18 Sep 2025 21:10:56 GMT  
		Size: 5.8 MB (5753694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.14-rc-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:ea60c12fa54b0b2f824b56e6c43593a03263a2314b7cf5cecdbf77820d438605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d6a2cd78b122e29e4c0a03ed59cee4d1db0ba88dadf51d273975f71658172a`

```dockerfile
```

-	Layers:
	-	`sha256:2e2dc9a4ae15a3b6bd74342823b78e3d8019d504962e334e28997654d62af732`  
		Last Modified: Thu, 18 Sep 2025 23:20:06 GMT  
		Size: 2.2 MB (2155067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56b791410d29a1d369ad2144c71f79d04c48d8a64c74dbc55dd6183951da19b4`  
		Last Modified: Thu, 18 Sep 2025 23:20:07 GMT  
		Size: 8.0 KB (7976 bytes)  
		MIME: application/vnd.in-toto+json
