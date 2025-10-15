## `hylang:python3.13`

```console
$ docker pull hylang@sha256:e5d47ef4b8e243064e1e9f38885ce4909f43ae6e0df8fab4e196bcdf1b8fff72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `hylang:python3.13` - linux; amd64

```console
$ docker pull hylang@sha256:6bccb02937a137345fa68f434e4e3e1ca5280d72bf62b922509dca714d6592ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51299000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b9c09bfacb2adefd407e80aec4a9f6f624561e76a81ce8421e8cfc41d9c9af`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PYTHON_VERSION=3.13.8
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PYTHON_SHA256=b9910730526b298299b46b35595ced9055722df60c06ad6301f6a4e2c728a252
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb47ef3fe06b5a7046519c3d2e531efd840040c3f0b6a16aafeac5c1c8095812`  
		Last Modified: Tue, 07 Oct 2025 20:58:06 GMT  
		Size: 4.3 MB (4250333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326ad4d2abf0742bc3cade1f9a8cd94bc113d1e08efac3e44f67fd00fa451b58`  
		Last Modified: Tue, 07 Oct 2025 20:58:06 GMT  
		Size: 11.7 MB (11733812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97385090cab0a6a5b06ddb222eba55e45f5bcf4ca806e77b6ea64c62fec563ad`  
		Last Modified: Tue, 07 Oct 2025 20:58:05 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ee14982b8274498a5fe7ca0c6aaa896c043b8a7962119070428a1efdb4e3f4`  
		Last Modified: Wed, 08 Oct 2025 20:14:12 GMT  
		Size: 5.5 MB (5536839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:fd5769c44c3bef75666f2ba5672cb96742b7b98d160ac90a3a67629a9b503108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2164135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:262b556d983cf6831ea54fcfd4b0c15a23d471373ab7855d95331304149e6690`

```dockerfile
```

-	Layers:
	-	`sha256:f7fdc9ade1a30207bb8acf5d187a02a31da23c45b4648de7c94dae7b3d550f4e`  
		Last Modified: Wed, 08 Oct 2025 23:25:01 GMT  
		Size: 2.2 MB (2154900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da9a2d4846a6208cbda9c514341ce4a4063a03602397ad3254d9e67dcd7c81a0`  
		Last Modified: Wed, 08 Oct 2025 23:25:02 GMT  
		Size: 9.2 KB (9235 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; arm variant v5

```console
$ docker pull hylang@sha256:488af011ea4fb54fc76958d05244f946593224e3f320d1ff228f4ec34c001c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48563531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cdf16e09d36f4458cf0994c40265f01eb72dc629df5aa96e8d3be5032645542`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PYTHON_VERSION=3.13.8
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PYTHON_SHA256=b9910730526b298299b46b35595ced9055722df60c06ad6301f6a4e2c728a252
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a76bb672760fdeddfdb60d25c5f12e0c20a9ee20c104f310d04387c7290d6e`  
		Last Modified: Tue, 07 Oct 2025 20:59:12 GMT  
		Size: 3.6 MB (3648746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be23cd60833e0dd54b8a9f480b1721f082747033358c57be84052529b6363b52`  
		Last Modified: Tue, 07 Oct 2025 20:59:10 GMT  
		Size: 11.4 MB (11431557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b3eeb3d6b88a527d0e65910b1968af1ab3b0dc7e5af82ffb6ea9dbaf8b6388`  
		Last Modified: Tue, 07 Oct 2025 20:59:09 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eded30823e1ace6f916a2cc0c3ca2ce96db36b1917338ef3e1a8425e28d0578`  
		Last Modified: Wed, 08 Oct 2025 20:14:29 GMT  
		Size: 5.5 MB (5536833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:0d54491fcb4cfc781dd7dccfd73ddf0e264a466074a2ea7b65e625dfec7a17fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2167248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e35dcc539c87e8478d9d8afbd89802be6fdb8d0e354193471a3f66f4bff3b94`

```dockerfile
```

-	Layers:
	-	`sha256:2ad85813dfb6bd9a02d3a3556ab27b81880b3b6b54963853aa58584dd3b2278b`  
		Last Modified: Wed, 08 Oct 2025 23:25:09 GMT  
		Size: 2.2 MB (2157901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bff4786a357d799f66c3812d53de848a932c0a9941c3a1c6720f440cabdd8e0`  
		Last Modified: Wed, 08 Oct 2025 23:25:09 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; arm variant v7

```console
$ docker pull hylang@sha256:c35e05f7adcddec573a285fe568d5c711daed99106dab477791298da26ff73b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46351848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d071225bf10a8a59a185c741bef3ad5278c0d4132b336a6b32e6662f0af78bd`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PYTHON_VERSION=3.13.8
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PYTHON_SHA256=b9910730526b298299b46b35595ced9055722df60c06ad6301f6a4e2c728a252
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3171ef823204613137b506831bb121db732fa456cedcd085cd94b28dac4b9ca6`  
		Last Modified: Tue, 07 Oct 2025 20:47:24 GMT  
		Size: 3.5 MB (3450543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca9908e93c3db386dbad55e0d28996447957160db5c042bc8e4d7bc0819ff79`  
		Last Modified: Tue, 07 Oct 2025 21:13:13 GMT  
		Size: 11.2 MB (11151539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b599e82fec3bea9a1328f63c8fe435c84da80f0e8f0d63bd8b2bcd660b8e6d8b`  
		Last Modified: Tue, 07 Oct 2025 21:13:12 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8062327e70f05e6f3524a8ac34b6343a7f90d1c86ed514add3c5854893b33a93`  
		Last Modified: Wed, 08 Oct 2025 20:14:13 GMT  
		Size: 5.5 MB (5536759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:dc460d91d567ba44da83c8a1c699be486ef9a2b1a958d40bf806003faeee741d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c280147b2435b369bad1db48d9150ee5a7a727d094f70c32b2dce4b1041d4f0`

```dockerfile
```

-	Layers:
	-	`sha256:ce20399be7e083c0c84ca99e19ac563cf17bed7d42bfb8a811b09637486ef4a1`  
		Last Modified: Wed, 08 Oct 2025 23:25:13 GMT  
		Size: 2.2 MB (2156354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19763ac2659be5cc592e82bb6df22285bd0c46c610a84543aacceb763ed44e96`  
		Last Modified: Wed, 08 Oct 2025 23:25:14 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:9c2886700744c601cf1102d20d071a656c420c55b6d9e198a0c734b060ff981d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51938623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732a9f97b207db4e36be3b0e56a3482eaf1d69277549077303bbe875453cc7e6`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PYTHON_VERSION=3.13.8
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PYTHON_SHA256=b9910730526b298299b46b35595ced9055722df60c06ad6301f6a4e2c728a252
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb758b7840f502ee4ee98d245a845f5e196a299f09e8a013b7e90da3ce4b386b`  
		Last Modified: Tue, 07 Oct 2025 21:11:40 GMT  
		Size: 4.6 MB (4598128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5066f1e1affbcfeee30d0b7b493d4c24f343b299f72d7e2e695607ece34899`  
		Last Modified: Tue, 07 Oct 2025 21:11:40 GMT  
		Size: 11.7 MB (11662747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c935f3950542a63254f0527cfc6930a7be3dfbcd8143cdefdcbd38a96ec4250b`  
		Last Modified: Tue, 07 Oct 2025 21:11:39 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9fcc95b0fc9adc81a95622b085da995dc5ee610a7c05e6d968205fd3d009151`  
		Last Modified: Wed, 08 Oct 2025 20:14:18 GMT  
		Size: 5.5 MB (5536649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:dddc52784687173297d0704e299ce4b465bdd40d5e81bd3c2919dffb1caba873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2164601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6376814cd705c6fa5d110bf0fd18e57daf6ca4139b8c19e96a77c2c7303f56`

```dockerfile
```

-	Layers:
	-	`sha256:b34dd4a20a7357442b5a6b0798b56ff1e1772c050b1380607318a248791f5267`  
		Last Modified: Wed, 08 Oct 2025 23:25:18 GMT  
		Size: 2.2 MB (2155214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37100eb5243bd239d8c99536f24eca4e6d200c43b27a676db2bb3afddf2745e5`  
		Last Modified: Wed, 08 Oct 2025 23:25:19 GMT  
		Size: 9.4 KB (9387 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; 386

```console
$ docker pull hylang@sha256:b3b0b4fb365bbbcd3ef1409c1c845ae49f8283f3bd971cf648bccc44aaaa93cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52860431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2550df9162ba7d7f452dbf580e127e96dab6ab49334fd0c7adf28ae8cb5ca0b`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PYTHON_VERSION=3.13.8
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PYTHON_SHA256=b9910730526b298299b46b35595ced9055722df60c06ad6301f6a4e2c728a252
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4d757535efd4de079032cb85f2e5ef9ba6da8de4d282459e1380dc79fe0b8b`  
		Last Modified: Tue, 07 Oct 2025 20:51:10 GMT  
		Size: 4.2 MB (4183117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaf37546adb97815894a72a1dc30795c453a7ffed27f4662f43b59cd56b04ab`  
		Last Modified: Tue, 07 Oct 2025 20:51:10 GMT  
		Size: 11.8 MB (11845725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a0f9d0e857230476e5fa17c5461598fa35fdfdfbbf57bf41e48e3542088d34`  
		Last Modified: Tue, 07 Oct 2025 20:51:09 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb54394e414b507dae48696a9a14883d85a9910672363861a19dd1e44a4e0e6`  
		Last Modified: Wed, 08 Oct 2025 20:15:07 GMT  
		Size: 5.5 MB (5536804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:45d9f3d0b14171a33a204d188746ce9a750c181f0a54788f051a270317e7865a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36da58d71905dfd373089b6417bb4288877128ce22102dd57e4e699f8310b888`

```dockerfile
```

-	Layers:
	-	`sha256:3cf5b81108aa552472db1680e0317cdee561ff4482bcd2f9c1987fec2422a2dc`  
		Last Modified: Wed, 08 Oct 2025 23:25:23 GMT  
		Size: 2.2 MB (2152061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6373463bc1f6d02bc6a6848d41dba97617b8dbb761b8213dd46e6f39b04adcdb`  
		Last Modified: Wed, 08 Oct 2025 23:25:24 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; ppc64le

```console
$ docker pull hylang@sha256:179ace74d3960a2e1125f4679ddd70c58b20af808cc3180c96ed532358dc9dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55789590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951fffef643f0b8d4e73b13f187d7e68cc0f723163559b5e434454fac2a8f5de`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PYTHON_VERSION=3.13.8
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PYTHON_SHA256=b9910730526b298299b46b35595ced9055722df60c06ad6301f6a4e2c728a252
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c36134bebf0561b514019e768d85c75ab5aaac0a181f111433350c3c8897ccb`  
		Last Modified: Tue, 07 Oct 2025 20:53:04 GMT  
		Size: 4.5 MB (4518623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba08f7b4093c384e10c21850ffa06597510aa918d3cdcae1c620f278b13e3a8`  
		Last Modified: Tue, 07 Oct 2025 22:18:25 GMT  
		Size: 12.1 MB (12135401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d82895736a538e803fa4c5bf0da6d13029f7a4607fb232e61fbc05cfcf67dc9`  
		Last Modified: Tue, 07 Oct 2025 22:18:24 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead707ea6680ea6bebd8c721626a0f27de61079f678caa587ff6faf0e1f969a2`  
		Last Modified: Tue, 07 Oct 2025 23:18:02 GMT  
		Size: 5.5 MB (5536862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:b9271f52532ad196f09bc5be0c4b76de2500315e526f6a7a39a4208fc4dbed8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2167794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04f8b7d4569fb6285e68d0461c12fca5423ae93ad7bd1ea70258dbdec6ad29e`

```dockerfile
```

-	Layers:
	-	`sha256:416a74184e20d9671cc4156af6a63153e26d58f6939411701f135d57f6fddaa3`  
		Last Modified: Wed, 08 Oct 2025 23:25:28 GMT  
		Size: 2.2 MB (2158491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb5d7478d85167911f46212dc1b7f72b4bd90bb28138165235a833c138866770`  
		Last Modified: Wed, 08 Oct 2025 23:25:29 GMT  
		Size: 9.3 KB (9303 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; riscv64

```console
$ docker pull hylang@sha256:17777adae7f72ffb029010f8d89727d2bf87304cc2918e918a43ca589db44519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49405664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150685afe40ebf9f53ecb7df1a4769456777acab779ac810b8029aa96d00b2d1`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PYTHON_VERSION=3.13.8
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PYTHON_SHA256=b9910730526b298299b46b35595ced9055722df60c06ad6301f6a4e2c728a252
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07881641e691ca6202df8ecc95ec2695a82945f59f23848306c6f524e1ecc797`  
		Last Modified: Wed, 08 Oct 2025 01:45:04 GMT  
		Size: 3.9 MB (3871072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce105971705908bb1453c65462e68f84e91b8d5c0f975c125c54819f73bdf83`  
		Last Modified: Wed, 08 Oct 2025 06:05:31 GMT  
		Size: 11.7 MB (11720748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b95fd166e74ebfab4802e4a11d2a5e858872686e6704fec431e4366e7ef5fb`  
		Last Modified: Wed, 08 Oct 2025 06:05:30 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdc57f77e67dbdca18c47bd73ff94ba35d7eecd50d8b3584a31545adcc699ce`  
		Last Modified: Wed, 08 Oct 2025 10:33:07 GMT  
		Size: 5.5 MB (5538092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:d3d03bad232d1bd830e85a1a84ed805146bf33a907a2043b5e0192c756dfe0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb5eb432eb9e90d9eeb7db44e1d4cdfa631fe8dd211c420e2ab0b3fa360523e`

```dockerfile
```

-	Layers:
	-	`sha256:d9acd8c38d11e0ff8b7cb9e7a5623e2c1fecd774dd23d0fc66ad5489603a2e8a`  
		Last Modified: Wed, 08 Oct 2025 23:25:33 GMT  
		Size: 2.1 MB (2148862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2b3a9d9b017d210131f0188208e3b3657bd7048579dbb239ae979118a9c88c7`  
		Last Modified: Wed, 08 Oct 2025 23:25:34 GMT  
		Size: 9.3 KB (9303 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; s390x

```console
$ docker pull hylang@sha256:acfa55a3b393287f219e6c9173775c4b1f24f99a39a9f60f079bd46a44e800b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51073663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63998d4039509fc05ffd8f6e3dc92aca7f6de64d193de792460c1029f9791250`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PYTHON_VERSION=3.13.8
# Tue, 07 Oct 2025 17:53:11 GMT
ENV PYTHON_SHA256=b9910730526b298299b46b35595ced9055722df60c06ad6301f6a4e2c728a252
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 07 Oct 2025 17:53:11 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7b17702cfe3c7d1897051161ba3ef82e1ffa2added4e44d0b8840676d17148`  
		Last Modified: Tue, 07 Oct 2025 20:56:23 GMT  
		Size: 3.9 MB (3906902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ffbdba5173fc541b9e71954cfd23da4e64dcc216123c71756f1224ca8d295b`  
		Last Modified: Tue, 07 Oct 2025 21:50:04 GMT  
		Size: 11.8 MB (11792786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07856d63cbc53f667e9d10a6541a47b99f9298407e87dcde73f4343fd333fcd5`  
		Last Modified: Tue, 07 Oct 2025 21:50:02 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bf08969ae1ba115aa99638912624753c053d2f6cc759f207834a998c1f7f9f`  
		Last Modified: Tue, 07 Oct 2025 22:39:02 GMT  
		Size: 5.5 MB (5536496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:ab5de7a102074a63a6487f892f24dec9708cde91175f837a2b13447dbedb9bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b731da35e698440723a22ce257097ea5f95018254d66fa8418c029be3b20a971`

```dockerfile
```

-	Layers:
	-	`sha256:12e66b9ad63c537cb42f6c26ac6423d03e317985ab0cbc11723ba008d152b34a`  
		Last Modified: Wed, 08 Oct 2025 23:25:37 GMT  
		Size: 2.2 MB (2156339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8285a7e1f0639f9190e3322980425083c4a475886dc7d74ea269703af219f8a`  
		Last Modified: Wed, 08 Oct 2025 23:25:38 GMT  
		Size: 9.2 KB (9235 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - windows version 10.0.26100.6899; amd64

```console
$ docker pull hylang@sha256:926eb1f9034f6b007693576e20b69d3af817a7de2d96caabcc45eba5db9d78d1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3287800893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e92e23a519ca30915e88ce76189c12970d2a795a1e2e4d39cfb8024360fbac`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:55:20 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 14 Oct 2025 20:55:20 GMT
ENV PYTHON_VERSION=3.13.8
# Tue, 14 Oct 2025 20:55:21 GMT
ENV PYTHON_SHA256=f17f216f057ed805b653f80a607c0d97d52884b4ed00380acabf199f0c025b14
# Tue, 14 Oct 2025 20:55:58 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:55:59 GMT
CMD ["python"]
# Tue, 14 Oct 2025 21:14:59 GMT
ENV HY_VERSION=1.1.0
# Tue, 14 Oct 2025 21:14:59 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 14 Oct 2025 21:17:05 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 14 Oct 2025 21:17:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b31ef2acd9573fa311450133976eaea07e0ccfd74f3de24d672c7bf465eba24`  
		Last Modified: Tue, 14 Oct 2025 20:51:54 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a501a3b214cea57b153540001e56e8f7fe77064199381518da7d30509d86054`  
		Last Modified: Tue, 14 Oct 2025 20:56:16 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbc87b51a61d7a2ed3ab427f91eed401bed1d4b252fc26b167e1f00f1467b65`  
		Last Modified: Tue, 14 Oct 2025 20:56:16 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc726552ac29e4b450cf5b274d56d65e6a27a89211e5d0932d6f337c18392310`  
		Last Modified: Tue, 14 Oct 2025 20:56:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2372e539ae66eed8bcff6c272270633b7c72968515eb3458ec15ab94b3870cfd`  
		Last Modified: Tue, 14 Oct 2025 20:56:22 GMT  
		Size: 58.7 MB (58721895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef79130f817a6156acf2f337b6ebf8a7dc77ece94732988e956f2a6d85f9bf5f`  
		Last Modified: Tue, 14 Oct 2025 20:56:17 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6c4e953a954edcfd2714fc3ff002a80ab00853fd84646bdbf66cb28577233b`  
		Last Modified: Tue, 14 Oct 2025 21:17:18 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88588a9cfea3c5df81c990a156b1eb66546e66cf3126f15395dcd6a1e6e5b369`  
		Last Modified: Tue, 14 Oct 2025 21:17:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eed4ca36c57c3151803e8db32189739d296d998d74fbfcc07e714a602b2c9e4`  
		Last Modified: Tue, 14 Oct 2025 21:17:18 GMT  
		Size: 8.6 MB (8588045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee54cd92f3702fffa30b834961bcd054453c532340dd015972537a768ce2a0d3`  
		Last Modified: Tue, 14 Oct 2025 21:17:17 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.13` - windows version 10.0.20348.4294; amd64

```console
$ docker pull hylang@sha256:645b84f1dfa0925bfc45df27bff6f622603ca9ca958db130b6cad1b5adc50949
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556123599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353d8c023277b0c8a501332066c60f49ef24156eb6425a56a33d278f0a7d2bf3`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:41:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:51:12 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 14 Oct 2025 20:52:23 GMT
ENV PYTHON_VERSION=3.13.8
# Tue, 14 Oct 2025 20:52:24 GMT
ENV PYTHON_SHA256=f17f216f057ed805b653f80a607c0d97d52884b4ed00380acabf199f0c025b14
# Tue, 14 Oct 2025 20:53:05 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:53:06 GMT
CMD ["python"]
# Tue, 14 Oct 2025 21:15:19 GMT
ENV HY_VERSION=1.1.0
# Tue, 14 Oct 2025 21:15:19 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 14 Oct 2025 21:15:52 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 14 Oct 2025 21:15:53 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d69910297fad50ffc461b607623e7deea128c2f2ed652341ab8682223c1249b`  
		Last Modified: Tue, 14 Oct 2025 20:45:19 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3446127170afdeb57742ca016297854803b344289f853d2569ae7f8ad174ec26`  
		Last Modified: Tue, 14 Oct 2025 20:52:15 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d885c5709c87eb38ed5ca551ae478c2acaea0d963e4a04d984584ceea201221f`  
		Last Modified: Tue, 14 Oct 2025 20:53:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240925fe8ea52bbcb89e5be181c9962edf989d50c89b5caa3aa6313792ed85f3`  
		Last Modified: Tue, 14 Oct 2025 20:53:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3090ab8ff77be92d486f4c6349f4734d05c5fb35db552fddf6174cd395903d0d`  
		Last Modified: Tue, 14 Oct 2025 20:53:29 GMT  
		Size: 58.6 MB (58625335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab163e11bec47fdabe60798f58168275e93f8fac8c86ff39a1f9bac32446c266`  
		Last Modified: Tue, 14 Oct 2025 20:53:24 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1376c66b42fa965298026a7da68b08513dc3ee3bb8efeff4993461349ef8f16b`  
		Last Modified: Tue, 14 Oct 2025 21:16:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cbfecb83aa771acaea44711f4294c4140edd575c9e9abd9a0bd606d32082c1a`  
		Last Modified: Tue, 14 Oct 2025 21:16:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8438ac4eb00a3f57fe41c31b942e671990b128b9d07f7b9a4b8c5e8dba36a2f8`  
		Last Modified: Tue, 14 Oct 2025 21:16:11 GMT  
		Size: 8.5 MB (8468721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53da52b7d35e4a03087d2bae85ce240bd2b5317b32f8ea380b00d124ec9c97cd`  
		Last Modified: Tue, 14 Oct 2025 21:16:10 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
