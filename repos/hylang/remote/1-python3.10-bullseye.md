## `hylang:1-python3.10-bullseye`

```console
$ docker pull hylang@sha256:21bac58c6d37b27339a9296df34bcb0afb2cde5f77961276c63bcfe7443210cf
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

### `hylang:1-python3.10-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:f16da1ae3d5a2cd1c2d15b0bd7a8f8a87c64f5f08a83ef5a12db6658b0c784f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50147785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20f5f772d4bb31d7603d632d68df4bcce1b3eba6d7e964ce833848419aa2261`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 16:49:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 16:49:14 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PYTHON_VERSION=3.10.16
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PYTHON_SHA256=bfb249609990220491a1b92850a07135ed0831e41738cf681d63cf01b2a8fbd1
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
CMD ["python3"]
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HY_VERSION=1.0.0
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 27 Feb 2025 17:10:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 27 Feb 2025 17:10:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ba1e4baecb5a2ce65aeefa3b98ffc3329b7378cacc465a0e1a215475d734c7`  
		Last Modified: Mon, 17 Mar 2025 23:23:05 GMT  
		Size: 871.2 KB (871240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4abbffb0d510a30d6842966cceea4bf43d40be513bb7862289a1e01ba3d55d0`  
		Last Modified: Mon, 17 Mar 2025 23:23:05 GMT  
		Size: 14.8 MB (14838223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39be85b6e7a369c003113468c88f4fcbde12fa26a1cfc3ba4cc0384e4652c9e`  
		Last Modified: Mon, 17 Mar 2025 23:23:05 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2978b6321d08a2f29affc186d8a5b0e8e489742065b1b20904291940268e9dd7`  
		Last Modified: Tue, 18 Mar 2025 00:25:41 GMT  
		Size: 4.2 MB (4184237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:1806babe9ef87c923939f1c70e2b436309683e4266077a47d53b7d257fd2d047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2723248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68fadd5e153b8df21ccd5f87e6707e00678a31bd42adbdfb43945c9c3390e29b`

```dockerfile
```

-	Layers:
	-	`sha256:4a6e3db9f71fa231495d2ec4e912572193b12d9010d2da3ba511f47378d0a9e8`  
		Last Modified: Tue, 18 Mar 2025 00:25:40 GMT  
		Size: 2.7 MB (2715222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a5593e482e2c83fa397d4735fafafed153b1486d15e249a8b28b5d8ce8cb532`  
		Last Modified: Tue, 18 Mar 2025 00:25:40 GMT  
		Size: 8.0 KB (8026 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:06569a5ef1315d01c8e037052cd8987edc4275256c9e20bdf0292f2e0e6964a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44617645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50eebaedf0f243b88b288cc79d785c55328ff4210725e8c0f46e185009b34db7`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 16:49:14 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 16:49:14 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PYTHON_VERSION=3.10.16
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PYTHON_SHA256=bfb249609990220491a1b92850a07135ed0831e41738cf681d63cf01b2a8fbd1
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
CMD ["python3"]
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HY_VERSION=1.0.0
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 27 Feb 2025 17:10:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 27 Feb 2025 17:10:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b0ca501b624d9dae81049df15e1024733ee21141b25f8ca123d98e0d13df5d12`  
		Last Modified: Tue, 25 Feb 2025 01:31:18 GMT  
		Size: 25.5 MB (25535432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bf10effdbdb43dfe3fb64366fb0a66189ea37984901bc7e709dbf612f77838`  
		Last Modified: Tue, 25 Feb 2025 11:31:54 GMT  
		Size: 836.9 KB (836943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0311d2712b1dc623bd9e1103d7b71342e5ef7c4397a40cede79f6dea46c576`  
		Last Modified: Tue, 25 Feb 2025 12:43:03 GMT  
		Size: 14.1 MB (14060674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85440796190b38e653d71fe5448912a14f1529599bf6a0164bdd872f1c52b20e`  
		Last Modified: Tue, 25 Feb 2025 12:43:02 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3992a6c4aa7cd74cd3c41f9ae5eb171271316315cac00cc8293c90f3970f3f7`  
		Last Modified: Tue, 25 Feb 2025 16:41:56 GMT  
		Size: 4.2 MB (4184346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:06bf9a2cbe88196573748198af97615f480eb6312dad68f4dc5f5221c2706aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2725570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d66b2997fad85fa1d88e86188d92c34f1389f49009a793f6b8c6e5939529c4`

```dockerfile
```

-	Layers:
	-	`sha256:dad9e4133b778fb63c2911d42d76cb9c7e2e41c9bf80eff484b04930f227627a`  
		Last Modified: Thu, 27 Feb 2025 18:19:40 GMT  
		Size: 2.7 MB (2717467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:028aa6578a9ec5b079fccc2978b7f41975bc9265b2855edac555db3456cfcb56`  
		Last Modified: Thu, 27 Feb 2025 18:19:39 GMT  
		Size: 8.1 KB (8103 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:f3b76b91a0015ec858ddf1a1fd074392037e4ec0c1cd748b5b175bf3929f71b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48668481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6171c6713c48ffe99e34e57e4a4fd30efd3d0941a78e43cb2e55ed8ce7a30c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 16:49:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 16:49:14 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PYTHON_VERSION=3.10.16
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PYTHON_SHA256=bfb249609990220491a1b92850a07135ed0831e41738cf681d63cf01b2a8fbd1
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
CMD ["python3"]
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HY_VERSION=1.0.0
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 27 Feb 2025 17:10:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 27 Feb 2025 17:10:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae10c5f584ce1b218d2a6a1b0821e6ff0869f199833d1a1bb6b3108bb531994`  
		Last Modified: Mon, 17 Mar 2025 23:36:23 GMT  
		Size: 859.1 KB (859144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820361266640e7cb252d9341b85d26824512b56a61401d5c82809c8d4a5225dc`  
		Last Modified: Tue, 18 Mar 2025 01:06:59 GMT  
		Size: 14.9 MB (14878994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e984f7b1968962a1ed6891b04342690880d30ea97fa9e579d6c07728f42540`  
		Last Modified: Tue, 18 Mar 2025 01:06:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b00f1f04be7688c20c40dbca9030be39a707ad4405f29ccd141fbc11239ec1`  
		Last Modified: Tue, 18 Mar 2025 09:17:13 GMT  
		Size: 4.2 MB (4184170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:36827aaa71f8391f1d54f66515d63b8dad6ac31254d1c026cce2306cb514f042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2723611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5596a3bcfcdfe07ca6b50a4f43991744b7eab7bc7afb4a6f500620b6dbd53734`

```dockerfile
```

-	Layers:
	-	`sha256:9cf137e16a8f860713b3479b2cbdf32d0a5fa5e939e2dfcb501b3166c7ac8a4d`  
		Last Modified: Tue, 18 Mar 2025 09:17:13 GMT  
		Size: 2.7 MB (2715481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a6b1868552726d4c844a2a556bfee45e6adb84fb20e344cfdf6700cc577909e`  
		Last Modified: Tue, 18 Mar 2025 09:17:12 GMT  
		Size: 8.1 KB (8130 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:dbbddd240c0a76de251115a2c8d524d85c77fbf279d2b3c51ec1689a9972f0dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51205709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357b8e2eedd5f4b15b6f9752deb13dd449a89c7b8fe6dcd0feb139dcb15f8c62`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 16:49:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 16:49:14 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PYTHON_VERSION=3.10.16
# Wed, 04 Dec 2024 16:49:14 GMT
ENV PYTHON_SHA256=bfb249609990220491a1b92850a07135ed0831e41738cf681d63cf01b2a8fbd1
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 16:49:14 GMT
CMD ["python3"]
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HY_VERSION=1.0.0
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 27 Feb 2025 17:10:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 27 Feb 2025 17:10:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e83ba34877ecae8e583197e97ef35a452a1d1b81c406023bf40d3c79d5ba9025`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 31.2 MB (31180337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6070b046ae081b1dbfc4c3e2ba05ebe3e07c2a5fa91820bded9ec82cb58a03`  
		Last Modified: Mon, 17 Mar 2025 23:41:53 GMT  
		Size: 884.0 KB (884045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef75ae9712b9493207d01d38c5190f15e6c790c216250023e7086771a429ea6`  
		Last Modified: Mon, 17 Mar 2025 23:41:54 GMT  
		Size: 15.0 MB (14956969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b903d86899a1f3c9981edb1c31a520313675f4d3d6f0b482ce0dd3f43b883c`  
		Last Modified: Mon, 17 Mar 2025 23:41:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d073ae78c7858ba7e26c68ec525aa26d41fefa74ba2b879ec81adcd4ac29fb2`  
		Last Modified: Tue, 18 Mar 2025 00:24:28 GMT  
		Size: 4.2 MB (4184109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:630df0e21f9e203d268704711d276e32b9e4f3a789fb47c122488bc9c77402cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941f861ba58b098bdce4624f459a95944bbb6a2bc2fb07b4b53d1fe83a446ce7`

```dockerfile
```

-	Layers:
	-	`sha256:46bcf00de7545591607e10a556a39e2da383c58c741e341f8aa317839bb5ca85`  
		Last Modified: Tue, 18 Mar 2025 00:24:28 GMT  
		Size: 2.7 MB (2712334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7aef687e29e5bca449b70919e23ba12df0c69832c34b436a24ce839f64ecd0d`  
		Last Modified: Tue, 18 Mar 2025 00:24:28 GMT  
		Size: 8.0 KB (7995 bytes)  
		MIME: application/vnd.in-toto+json
