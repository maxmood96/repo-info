## `hylang:1-python3.10-bookworm`

```console
$ docker pull hylang@sha256:c0dd55d2b55abe51dfcb21981a57dccb01d88294eef7494a18e22c8c7cbd3b9a
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

### `hylang:1-python3.10-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:b5ac114937572e4f597d649f10ef55932013c394f27b55b6d5bcd37fa7aff392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51380835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6e9f0fa59850af0d79b2841f50f410e53a91e094ab5073050c309ad6f0ec74`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 16:49:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1235d039a7d629d661cd58c84386a20caab12ed3ba2ca999d194fb1055a3113`  
		Last Modified: Tue, 24 Dec 2024 22:25:19 GMT  
		Size: 3.3 MB (3317312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17464c8c9fbfac9efc479940986e26dc06b5d14b5753c16971f6930184b2f42`  
		Last Modified: Tue, 24 Dec 2024 22:25:20 GMT  
		Size: 15.6 MB (15647711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f344618db07e51c52e9a0ca634b057784db11516d257efd7fc211dfe4199bc45`  
		Last Modified: Tue, 24 Dec 2024 22:25:19 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad7bee2d41e7fea7a204e5b0edfa0aa8fa80b01797b3824298d14e6993c9e93`  
		Last Modified: Tue, 24 Dec 2024 23:23:26 GMT  
		Size: 4.2 MB (4183982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:71bd6f1c34af22cc383c7f331b7c55119e701714d36e263abe63003c221a31b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2473882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c3e8a929dab0340ed8b5e365be9d3142eeb77e3c711efff3fd687d5a730c09`

```dockerfile
```

-	Layers:
	-	`sha256:76d3ae4f369fb8cb9fbabcd4c10595454d4ce1c96816f31abc2cb15b7d5de8f2`  
		Last Modified: Tue, 24 Dec 2024 23:23:26 GMT  
		Size: 2.5 MB (2464606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92e766fc30b6cb5d1975a9ace4a4148d05647dc10aa9075db5fb9e48476eaa7e`  
		Last Modified: Tue, 24 Dec 2024 23:23:26 GMT  
		Size: 9.3 KB (9276 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:acb576ea3df876c3091118155d1e013fb83508ca0e83fc9a253740ea47b682c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47928880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702f4da12e9fa3cc949edf809c039308a22096fdb7096963c09397a310eb2e2c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 16:49:14 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
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
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111b7ed7b8c4f71ba5d68ec8c6a875edc28be8a020502bb8c2429c65a97e220b`  
		Last Modified: Wed, 25 Dec 2024 03:34:53 GMT  
		Size: 2.9 MB (2889980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9243fefc77e7741e7e83fbe7686dbcaf6f940462a8a5fcad2fcf3d33c49e2954`  
		Last Modified: Wed, 25 Dec 2024 04:06:03 GMT  
		Size: 15.1 MB (15099498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9e5490591a03d1aa0892c190c0f333aa9ed10c69402e9731f1391aacf18357`  
		Last Modified: Wed, 25 Dec 2024 04:06:02 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970fb2fdb69b9d3722af32c77f77af14ca80092afcb16794fd5f08653c8da6ba`  
		Last Modified: Thu, 09 Jan 2025 22:37:46 GMT  
		Size: 4.2 MB (4184247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:47f90ef6f079dc80e21793c66995371918697d54ae273ca17317d194c07a6836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2477535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbe6eb6f5a10ce592d7690444ee23facdb4fe01e8c41fb2a1d75a8137126953`

```dockerfile
```

-	Layers:
	-	`sha256:bfa7eb8a25689463dfe2ee765b502e1d737936141bbd961f5ad412856fb5f919`  
		Last Modified: Thu, 09 Jan 2025 22:37:46 GMT  
		Size: 2.5 MB (2468150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7573b2198ccea68ac0e53c1e3d3c9d529adf311ce0af2a4d9547655c5af4f055`  
		Last Modified: Thu, 09 Jan 2025 22:37:46 GMT  
		Size: 9.4 KB (9385 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:2e6c7c4e1d27d71772427fecbc4c13b55ea96d96b3cbf145b49d8d1d99fe8c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45526415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8decac436429e0afc13315d48da47ca1d237e5e41e469bea29c633d7fac93b8`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 16:49:14 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
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
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8288f7a601ddb4b02acf714d6ee53ed985f84aef779897e930992d04bb5871`  
		Last Modified: Wed, 25 Dec 2024 07:39:21 GMT  
		Size: 2.7 MB (2721262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a29b2543b052d265f65ba23841ad2ba39795c04f1bcd2e0d26a66e38fd7a9ae`  
		Last Modified: Wed, 25 Dec 2024 08:58:33 GMT  
		Size: 14.7 MB (14686960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e795efd381392a37ca98e5853370e86fbfe3deba4cd7b50267a8b1fa17eaf737`  
		Last Modified: Wed, 25 Dec 2024 08:58:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bca43f549b7faaed99614d452307c664abeaf3ac39fef7258a41218ba6133dc`  
		Last Modified: Thu, 09 Jan 2025 22:58:00 GMT  
		Size: 4.2 MB (4184422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:80ca7aa191ff9c80cdfe33a64ed00f8e75b6014315fe739b9f932a63cfa99f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2476292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09f199e9387874e9ce220fb5368e590f61ed5840a6df028df6502df480488e6`

```dockerfile
```

-	Layers:
	-	`sha256:4bbad2e1e1d815c39a2511b9abec7eac71965b00db12a5ebccc9450f4b7dd095`  
		Last Modified: Thu, 09 Jan 2025 22:58:00 GMT  
		Size: 2.5 MB (2466907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00851d383b6ef998ca04f32870b14ebc854e818611d6af4c1ac4f48d9c9beff4`  
		Last Modified: Thu, 09 Jan 2025 22:58:00 GMT  
		Size: 9.4 KB (9385 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:4613a1721716206ad0462b6295cae71b3b2c6a00e3f79692d3bd2b20cf183572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4f49fde2f44cef083e5bb1e43d39da82fbac7f4773e8b03a118fa4ce56a6a9`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 16:49:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
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
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681f5b8ff8010135c072ddef91d563db5d69c0d0a38d4b6c79ffe3df80338747`  
		Last Modified: Wed, 25 Dec 2024 05:09:45 GMT  
		Size: 3.1 MB (3137729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48319c982223f062c18581253adc4b6815ced4ec4608bc959837393ec204c20e`  
		Last Modified: Wed, 25 Dec 2024 05:55:22 GMT  
		Size: 15.6 MB (15563508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c66f48a80278101f65964f7b8f8a241d53c95c621f0a29f00f7b1bb0a6a188b`  
		Last Modified: Wed, 25 Dec 2024 05:55:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faac004ed28bfeef1e414398e8bce2fa9c7ec17d8450a994cf582d948dff906`  
		Last Modified: Thu, 09 Jan 2025 22:52:52 GMT  
		Size: 4.2 MB (4184126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:c90a84e645a27048ec1775d47f94173a2aaf6fa5cb10f7212b342cd4fd015a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2474356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57dbc4b2e1adf346fe2574d43521bbc85b0a3e3e21d24d37b3f5bfc1fe0e09aa`

```dockerfile
```

-	Layers:
	-	`sha256:e7e779c3e36c39d3cf78b926d11d3d6f5f1da445c25e1c19d3aa20a6e9b08ef7`  
		Last Modified: Thu, 09 Jan 2025 22:52:51 GMT  
		Size: 2.5 MB (2464927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e49f6d109b893bc4eb0289c7706bd3d8700bbed93fca47487a3b05394c6ec3e6`  
		Last Modified: Thu, 09 Jan 2025 22:52:51 GMT  
		Size: 9.4 KB (9429 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:d6a488e2706c552baf6e287386f84d915434a5d882b917fb85306d813a6123e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52598520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed40f6d79eb99b1ec00d3e40ff9631858d82c0d5e71f8339091262ad1bde7892`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 16:49:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
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
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc993ae9ddb48b728ee9ce898de505d167d073a231c23e5bb7eee4ea11a4538`  
		Last Modified: Tue, 24 Dec 2024 22:39:37 GMT  
		Size: 3.3 MB (3316824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c85c52e13712a4798d1841ad2a79cd1bd0e640c46c1112738db316feee508da`  
		Last Modified: Tue, 24 Dec 2024 22:39:38 GMT  
		Size: 15.9 MB (15891945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0dacaf944d975d78db2088c28c9adf034a2e59d57e23e3fbd15bc20ff18c55`  
		Last Modified: Tue, 24 Dec 2024 22:39:37 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4d7509ef65a9f1beed71c53c2d7557556a07dab77f08903d5d7f2ff423271`  
		Last Modified: Thu, 09 Jan 2025 22:30:11 GMT  
		Size: 4.2 MB (4184116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:ac8d9e2d228b4da91cd804b9e77009983dcf455f38397f365b4005982a3a7629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a3e259d84f73b13d97202fa7c04fb9dfc5f14648d53bcb1811f7d0cb67bfcb`

```dockerfile
```

-	Layers:
	-	`sha256:e384a1951ad6a9ef1ab903d7f775b6d86fb5d9a1cb9d1d9d0bfea5fa248b2105`  
		Last Modified: Thu, 09 Jan 2025 22:30:11 GMT  
		Size: 2.5 MB (2461686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:119249c55c562e297c4436cec8828d788e8a5a6c9f8d6de24fbf03f9720bd7af`  
		Last Modified: Thu, 09 Jan 2025 22:30:11 GMT  
		Size: 9.2 KB (9225 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:6a143c146f4eb71230d3389300e3bf7b891c6de512f510a6be42f7e94a22b39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56028531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a501e501bc39730fc78f09fc02854f8db25915d44c93780d23587610019dc4`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 16:49:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
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
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6e349d4e1e3b8d870499c5d0912b4ebab1d2b5b0719c791729a78151ca542e`  
		Last Modified: Wed, 25 Dec 2024 08:15:01 GMT  
		Size: 3.5 MB (3520196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adce7871c11213a22487f06ae10f70d62c11a0a700ddf2ea18bbc48bd523edcb`  
		Last Modified: Wed, 25 Dec 2024 08:42:26 GMT  
		Size: 16.3 MB (16260707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe7445c4ac86fba8125946896445d50b32ddfe03f8e50bd910d2471766f82bc`  
		Last Modified: Wed, 25 Dec 2024 08:42:26 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9c2f482239ed876690504d40b8562277c399f50a16ef513c8f7e91d85b5828`  
		Last Modified: Wed, 25 Dec 2024 12:33:28 GMT  
		Size: 4.2 MB (4184139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:4bffb6552dad8d007f722c9aa9451b79d345fc2cf67e5a6872031cafc4147ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2478367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e494e48787e16b422538768bb75d32bad11d38f235584286eee2dad914e493ca`

```dockerfile
```

-	Layers:
	-	`sha256:9ed32cb585de068da2b18cf6cfb063c40d0abfc0a788e07406ca8c341ccda279`  
		Last Modified: Wed, 25 Dec 2024 12:33:27 GMT  
		Size: 2.5 MB (2469022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2465670f7c6f76cd42d77d2f9ed575e8e00971cdb9301e1748875dbd5f19f9f3`  
		Last Modified: Wed, 25 Dec 2024 12:33:27 GMT  
		Size: 9.3 KB (9345 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:6961cead45ec06feda7239c80832f516801ae34e4d8165770bf9dbb2532e8a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49481996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69cee652e9deee1de3f2eaf5fbe0e891d3bd8c75a7f14baf94c3c741d97f6cd`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 16:49:14 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
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
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f5727225c4ab96795df8153e9d8adc4d25de284322adb4354b0315bdba1fb0`  
		Last Modified: Wed, 25 Dec 2024 02:22:30 GMT  
		Size: 3.0 MB (2980730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cef3ab449b3e8009355d55ba7c5933f560acd8597603768d8d2f87b1b36a629`  
		Last Modified: Wed, 25 Dec 2024 02:44:08 GMT  
		Size: 15.4 MB (15437991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420147f4fb9a36285872d166ae8e99ff1d8d58537b41e5697c32e472663089`  
		Last Modified: Wed, 25 Dec 2024 02:44:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846679ebf5f8b5d57a76b00f4ee88512e5de8df60a7bc7a2057fc1f148774a2a`  
		Last Modified: Thu, 09 Jan 2025 22:58:16 GMT  
		Size: 4.2 MB (4184124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:3137ba3b9c52f64423d3085e69a124becf4b0c38daa2c719ee8037c97f6566dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2473591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d624caab618ef9582efa80f0e2f8f2019652cdd73122f7b8b222401831d9e6`

```dockerfile
```

-	Layers:
	-	`sha256:ee38b77d1dc08a9a80c381a3c3dc66db1c45a421ad53d5d8b5b8408d0eed053c`  
		Last Modified: Thu, 09 Jan 2025 22:58:16 GMT  
		Size: 2.5 MB (2464314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61bce4ea60a10cf9ef9304c8cafdb9234d4f461145757d8aeb3751e53bb162e8`  
		Last Modified: Thu, 09 Jan 2025 22:58:15 GMT  
		Size: 9.3 KB (9277 bytes)  
		MIME: application/vnd.in-toto+json
