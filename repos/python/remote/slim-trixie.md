## `python:slim-trixie`

```console
$ docker pull python@sha256:aee3b1c52ce756c42ee4ad90437ae49d87fa87fc2f09c17895f098b67f081a8d
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

### `python:slim-trixie` - linux; amd64

```console
$ docker pull python@sha256:2409290aa375de35f6492db84c700067d5c4c2aacfaf770c155d7528fb68bcf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43345220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20872a6793c23eb82b68c1fb90667c110b63587b239891e8f7a5eb53b18667b1`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:57:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:57:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:57:53 GMT
ENV PYTHON_VERSION=3.14.4
# Fri, 08 May 2026 19:57:53 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Fri, 08 May 2026 20:05:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 08 May 2026 20:05:08 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 May 2026 20:05:08 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab80c0b8b94e86367b7670f7b513efd102e283d9cd8de7aa4660999d1e30d97`  
		Last Modified: Fri, 08 May 2026 20:05:16 GMT  
		Size: 1.3 MB (1293092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765e5bc6b73e0d0f223f9d3c00a231903580b2233cf4beb9bba35041519fbd92`  
		Last Modified: Fri, 08 May 2026 20:05:17 GMT  
		Size: 12.3 MB (12271652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cf12ae9d2089e998920c83152f6fd488418715b42de71a60029dee4d9fabfe`  
		Last Modified: Fri, 08 May 2026 20:05:16 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-trixie` - unknown; unknown

```console
$ docker pull python@sha256:f45d1f0a7244b888697ef7d92561bdbedb1282504117713aac8b7e74466710ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2170464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b623ca3206b2832ed7b35ceba8c200dbe712199c2d30efece60bf880411080`

```dockerfile
```

-	Layers:
	-	`sha256:5b31fab810c5c16a7269255d78d686edb291198b046dd97a89150995c08a1f8d`  
		Last Modified: Fri, 08 May 2026 20:05:16 GMT  
		Size: 2.1 MB (2146618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30a534eb1840a1c93dcac1cae3dd3edb756df8867501a55dbdfb9847efe2a54d`  
		Last Modified: Fri, 08 May 2026 20:05:16 GMT  
		Size: 23.8 KB (23846 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-trixie` - linux; arm variant v5

```console
$ docker pull python@sha256:b52c808c7ecceb8d0dd86daf5a55b0a3adc3aee44a233ed9bc47d9104cb0eeb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41174473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42b5f155987944b47f421180903561968136aba643907bd8e51f73947cea23c`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 21:06:35 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 21:06:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:06:35 GMT
ENV PYTHON_VERSION=3.14.4
# Fri, 08 May 2026 21:06:35 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Fri, 08 May 2026 21:16:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 08 May 2026 21:16:49 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 May 2026 21:16:49 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc1c48aa1722f36d3bd1da1009091d2df9cc1e520758fdaad9c37a7d34b7ebf`  
		Last Modified: Fri, 08 May 2026 21:16:57 GMT  
		Size: 1.3 MB (1276185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f579c30f410713936a03c2be62e8c3086be8b687fd7431b3bfe5c9497b3eebd0`  
		Last Modified: Fri, 08 May 2026 21:16:57 GMT  
		Size: 11.9 MB (11949838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00435a715ccc0176aafaff9548081df4ca865784ff9dea00122ad6157070882b`  
		Last Modified: Fri, 08 May 2026 21:16:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-trixie` - unknown; unknown

```console
$ docker pull python@sha256:622c4950f6697dcf4da749ef679bb07496b67eded6c9b9c1636510c93c0f0130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfaefda8b2a7fc442d06ba30cadac400bb7b94856e85778156e7243f67f64c3c`

```dockerfile
```

-	Layers:
	-	`sha256:5c688bf7d17858be01b8f469b6be8d38cdefc5ce9dc0e15fc8f9c57260565351`  
		Last Modified: Fri, 08 May 2026 21:16:57 GMT  
		Size: 2.1 MB (2149619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19c8a05ddb88c92fee182ff59efd5999f93c98aa647b61cf3042fc635f25f9a1`  
		Last Modified: Fri, 08 May 2026 21:16:57 GMT  
		Size: 24.0 KB (23984 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-trixie` - linux; arm variant v7

```console
$ docker pull python@sha256:d4e2c58957aed8d6fe7bb9071d9a88c485c211789bb6c5073797925c9422a29e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39098826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada0e7f91fe1132de24eabae1bfec6c7bbb06af2bc7aac30676392de3a518fd9`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:59:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:59:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:59:59 GMT
ENV PYTHON_VERSION=3.14.4
# Fri, 08 May 2026 19:59:59 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Fri, 08 May 2026 20:11:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 08 May 2026 20:11:08 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 May 2026 20:11:08 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270d396283a9b0f5f1e6e707248f6d275b6bde64e85b784d50f873549e32fcd6`  
		Last Modified: Fri, 08 May 2026 20:11:15 GMT  
		Size: 1.2 MB (1249068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0a221fde3f1a80b6a6de3dfa133473cf2aba70f8fada95994ba712dde1072e`  
		Last Modified: Fri, 08 May 2026 20:11:16 GMT  
		Size: 11.6 MB (11634596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07881dcc6ce3c91278f478f286f6d3d6cff1d40018be8a26537d9e8e67da4918`  
		Last Modified: Fri, 08 May 2026 20:11:14 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-trixie` - unknown; unknown

```console
$ docker pull python@sha256:ed52761589461ced0c1e765ca564fa9fbfd0e27ac31361dcb8cef70493b1a166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e30c49eecf90745105181c4acfeabd694898599b50d723a0b20522f8c8331df`

```dockerfile
```

-	Layers:
	-	`sha256:fb309a57673b104856b40fb0ad6e2cec052c40183c679b2c71b6f31d13aa7197`  
		Last Modified: Fri, 08 May 2026 20:11:15 GMT  
		Size: 2.1 MB (2148072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90ccaef2a43c01e177c5a917d2c358057e84ca60b3b87f954d3e6fe4baabb901`  
		Last Modified: Fri, 08 May 2026 20:11:15 GMT  
		Size: 24.0 KB (23984 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-trixie` - linux; arm64 variant v8

```console
$ docker pull python@sha256:1966fc5ef37f7b8b4907cc8ce0898cf9fa6f64dc0205295da532374e877c3597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43603356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d385202703d2691c1b8c50a5cccaad90410b3e96742c0626f877bf5389da69`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:59:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:59:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:59:38 GMT
ENV PYTHON_VERSION=3.14.4
# Fri, 08 May 2026 19:59:38 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Fri, 08 May 2026 20:07:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 08 May 2026 20:07:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 May 2026 20:07:05 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31c4e147be7a2f1573503ad599786b283b6922f6ac04af2218e8d28be53c7aa`  
		Last Modified: Fri, 08 May 2026 20:07:13 GMT  
		Size: 1.3 MB (1273881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76390185799a5a51b77380c8ce003e85bfd208a1aba79c8a46a47070479d8fe`  
		Last Modified: Fri, 08 May 2026 20:07:13 GMT  
		Size: 12.2 MB (12185583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e86e5ab3004d041099543681b2fa49706acedfc13bff732e895504879438584`  
		Last Modified: Fri, 08 May 2026 20:07:13 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-trixie` - unknown; unknown

```console
$ docker pull python@sha256:2a122ab7f7cee1912fcad7749894bd04e407c08fa20c4ee5102f4d5ceb753b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2170960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1970d5e73d3dba711b7834b2dbb5803163343e0342f8139dec1747181effc464`

```dockerfile
```

-	Layers:
	-	`sha256:c9ae4d9a008669e65fdd1be271dedb8e44fa7cdd85ee1939081433cae03b5f1a`  
		Last Modified: Fri, 08 May 2026 20:07:13 GMT  
		Size: 2.1 MB (2146932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15c7a261ca0e7aa30b2fd90632048e7de5a01ae17cf9612bf9450b00753c0720`  
		Last Modified: Fri, 08 May 2026 20:07:13 GMT  
		Size: 24.0 KB (24028 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-trixie` - linux; 386

```console
$ docker pull python@sha256:87e3ab4b14b23cd6386e8ab38d09684846e1bde6ed3ab9466def0a83ccfc3691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44966797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd169b6e3115edc598efbb57f5d521e5dbc41ca9324b3b69b88fb8214986654`
-	Default Command: `["python3"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:57:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:57:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 01:57:14 GMT
ENV PYTHON_VERSION=3.14.3
# Tue, 07 Apr 2026 01:57:14 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Tue, 07 Apr 2026 02:14:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 07 Apr 2026 02:14:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 07 Apr 2026 02:14:40 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3ad58e7663dac2e874d85633f012dff41d0fc985f7d40eeef495d01a4201e3`  
		Last Modified: Tue, 07 Apr 2026 02:14:47 GMT  
		Size: 1.3 MB (1297206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0272dd4cb7195931b2beb5f7d5e2da6e442a6959e5120a272961a4ab57a2a012`  
		Last Modified: Tue, 07 Apr 2026 02:14:48 GMT  
		Size: 12.4 MB (12378090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96903a511312da826b57d25e208b7d468f2e0e463902203e0ad7b039a3a56cc`  
		Last Modified: Tue, 07 Apr 2026 02:14:47 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-trixie` - unknown; unknown

```console
$ docker pull python@sha256:0983fb5027106604bdebdc5ec22151b6750e16529271d730cb981a0794e884d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2167559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d706bc709696fdd947b6d1f2f23c979de51cf57da0436673182ecaa7bdbbea9f`

```dockerfile
```

-	Layers:
	-	`sha256:cee82911c72a3a98cf844caa1f7ac73d017234073d707ad95af17eee3eadeac0`  
		Last Modified: Tue, 07 Apr 2026 02:14:47 GMT  
		Size: 2.1 MB (2143771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea893f6e58724c0d91116afd534a061603c4a226572ef8f277f70490aaec0cc`  
		Last Modified: Tue, 07 Apr 2026 02:14:47 GMT  
		Size: 23.8 KB (23788 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-trixie` - linux; ppc64le

```console
$ docker pull python@sha256:aaee4a4e069aa17277de3d6065206b0919f851c2d91124895e72a34c02e71883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47598236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760511971869f8c9031ed7268b3f87761aa990d76cda9913807a48c16da3274b`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 05:15:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 05:15:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:15:24 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 22 Apr 2026 05:15:24 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 22 Apr 2026 06:01:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 06:01:54 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 06:01:54 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f111c0180379849c2242c25410e5cfba1da759760c6fd915b382423a79dfeb09`  
		Last Modified: Wed, 22 Apr 2026 05:38:44 GMT  
		Size: 1.3 MB (1320835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c290091f0c19fe00c1215f778cb3a65746a096671294db07b1c01f69d45cb1ba`  
		Last Modified: Wed, 22 Apr 2026 06:02:21 GMT  
		Size: 12.7 MB (12679120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0a482d9841e740618dd9de888a37790e6517a17a81a92bf01a02c87a8e6e97`  
		Last Modified: Wed, 22 Apr 2026 06:02:20 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-trixie` - unknown; unknown

```console
$ docker pull python@sha256:9f0a6d44b663da754fd8ebba93b06215c3db1e6af31d3441668ce2375f1d2793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2174126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5591527bd2f45f28a106098dcf05f0e57b62a236cd1f957c11baf932421a2aef`

```dockerfile
```

-	Layers:
	-	`sha256:d6c4a18dba36baee8010ead96b0dd6efb2957a984e82c0c8874d39470df8bc7e`  
		Last Modified: Wed, 22 Apr 2026 06:02:20 GMT  
		Size: 2.2 MB (2150209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f43f4611986675eed1715802fed0d89cc53a5433adf7c28f2a51881201af17a`  
		Last Modified: Wed, 22 Apr 2026 06:02:20 GMT  
		Size: 23.9 KB (23917 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-trixie` - linux; riscv64

```console
$ docker pull python@sha256:dc688db915f30b545b82b93598aea4114f13c06d145b4ee56281bdc74c217a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41837001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a14de1b6f4b4abd20460c766e633d903a5c7aecfa613d194400dccb49d9ca6e`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 02:19:56 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 02:19:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 24 Apr 2026 02:19:56 GMT
ENV PYTHON_VERSION=3.14.4
# Fri, 24 Apr 2026 02:19:56 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Fri, 24 Apr 2026 05:34:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 24 Apr 2026 05:34:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 24 Apr 2026 05:34:06 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bce0dc49d545c30c4bf27ff3f9b3955e43ea993920b0b092cc45c56722e615`  
		Last Modified: Fri, 24 Apr 2026 03:58:00 GMT  
		Size: 1.3 MB (1260935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dea914d0c50df9327e58be37aa0ddf5ad3cd12db4c581a298eed284dd71706`  
		Last Modified: Fri, 24 Apr 2026 05:35:14 GMT  
		Size: 12.3 MB (12295622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ef74184625974270d8396a7b33ce07d0b1f7b43a58a33496b7d7847f2f49e9`  
		Last Modified: Fri, 24 Apr 2026 05:35:12 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-trixie` - unknown; unknown

```console
$ docker pull python@sha256:882b601969d0e6f934f993d50a81955705c0e41c618ba7e2e6544bb92c8b66c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2164498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818c41534d37f2b398d3edc8e91b5b57ff40b1232d590a8d86e21c14fdd31710`

```dockerfile
```

-	Layers:
	-	`sha256:1007cde9a945da088e661c9c4edcc94e8d6c17a6e9baf53baf6f19f0524fd10e`  
		Last Modified: Fri, 24 Apr 2026 05:35:13 GMT  
		Size: 2.1 MB (2140580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e762a244f1296274ad0d79f9d95be92521d50571d28be801514a8b940d952e87`  
		Last Modified: Fri, 24 Apr 2026 05:35:13 GMT  
		Size: 23.9 KB (23918 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-trixie` - linux; s390x

```console
$ docker pull python@sha256:68015e2276523eb8f8a57ae3649dd7c43342bb667f556dd1230be786652fad6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43464968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfef7b6bdb7409c97260aa9c20f59a68ade7013f083437961be70fd9d9c9b1e`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 21:31:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 21:31:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:31:39 GMT
ENV PYTHON_VERSION=3.14.4
# Fri, 08 May 2026 21:31:39 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Fri, 08 May 2026 21:39:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 08 May 2026 21:39:26 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 May 2026 21:39:26 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086261b25b4ea08c7d835e1e6b9f2b7c015d715ef2653907ec347beeb0d61e9e`  
		Last Modified: Fri, 08 May 2026 21:39:38 GMT  
		Size: 1.3 MB (1305510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4037942c2ecfa215478c3c98dde890f6e78ed70da9f943589994b52f56ca64c5`  
		Last Modified: Fri, 08 May 2026 21:39:38 GMT  
		Size: 12.3 MB (12318861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd48b5450ea01d0a681eecef0e06c4c31af94c3b5aedf4cd0759f256cd643f0`  
		Last Modified: Fri, 08 May 2026 21:39:38 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-trixie` - unknown; unknown

```console
$ docker pull python@sha256:0b91c53a923c63e603a4f6a97f054f6c471b14cc23ac779c8f2fed3bf5752515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2171903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b48cd3641389193bb4d231dedb9d9c6ff69a81fd6d2152f9bc92cf34cd08869`

```dockerfile
```

-	Layers:
	-	`sha256:5c1927ce819e4408e59272910787bd6cd8b1e40277633f5eeb8b75846af4adc8`  
		Last Modified: Fri, 08 May 2026 21:39:38 GMT  
		Size: 2.1 MB (2148057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b8cc4c7a04fde1b47582d296c32b05b905dcb7ec4fba9edc26e958742a042e7`  
		Last Modified: Fri, 08 May 2026 21:39:38 GMT  
		Size: 23.8 KB (23846 bytes)  
		MIME: application/vnd.in-toto+json
