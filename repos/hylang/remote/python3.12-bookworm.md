## `hylang:python3.12-bookworm`

```console
$ docker pull hylang@sha256:bb91b98260545f4ff5be6d61cdab837e5db2df97f27cf70ad93c6afb9397cbbc
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

### `hylang:python3.12-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:51ba547fe34bea8b2a020c9da62525890e3e2a7daf7b6b372677bcabfa8f2cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50823205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1c1af1d63b3b5f475dd4cf77fec9ce9d3ea939fa90653bc40c4490cdcd01a5`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:02:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:02:04 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 02:02:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:02:04 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 24 Jun 2026 02:02:04 GMT
ENV PYTHON_VERSION=3.12.13
# Wed, 24 Jun 2026 02:02:04 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Wed, 24 Jun 2026 02:11:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 24 Jun 2026 02:11:39 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 24 Jun 2026 02:11:39 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 02:46:26 GMT
ENV HY_VERSION=1.3.0
# Wed, 24 Jun 2026 02:46:26 GMT
ENV HYRULE_VERSION=1.1.0
# Wed, 24 Jun 2026 02:46:26 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 24 Jun 2026 02:46:26 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03952ff66d70d39109eda6ac3d7b42f9e2cbce89debbfdc3cc784ead9d9e39a3`  
		Last Modified: Wed, 24 Jun 2026 02:11:48 GMT  
		Size: 3.5 MB (3520782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524401bfa9eb171bc5a9ead7585085969746b64cc95623aed9b32072978d931e`  
		Last Modified: Wed, 24 Jun 2026 02:11:49 GMT  
		Size: 13.7 MB (13666970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a056f49ed4fbbe340a316423216b7ea38b1ea463b9cbeb08b392ff69957fe03e`  
		Last Modified: Wed, 24 Jun 2026 02:11:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f738bf69e78b8751e4c9a03586781f3f01f6ff16453a3d92c6552c5ac1426f71`  
		Last Modified: Wed, 24 Jun 2026 02:46:34 GMT  
		Size: 5.4 MB (5397564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:3869abbf41f3c020a3e2a7324ecf84926196755f4b785c83f9f388a86ca0b3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2586121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8219288756b6c4f5dfa35c8ac3618a261c3264b7a685aa74d918c3505f4cafe4`

```dockerfile
```

-	Layers:
	-	`sha256:6b0d2a2ddcd8686b85d323405f9530a3e3a33682bcd1e4d1176a6357882e78a8`  
		Last Modified: Wed, 24 Jun 2026 02:46:33 GMT  
		Size: 2.6 MB (2578027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b0816d690d609192b23e6d3dbc1a7358b83bedf9fe319419f8ca82cb95729ec`  
		Last Modified: Wed, 24 Jun 2026 02:46:33 GMT  
		Size: 8.1 KB (8094 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:feeb42800ab87d23e948234e077e519acdf47b962525a8939a1157c90ad9b094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47345443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823a7de7cd955b763bed04fcabf544f85cf0802e4bc3293e36596dceaba11052`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:46:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:46:40 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:46:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 11 Jun 2026 01:46:40 GMT
ENV PYTHON_VERSION=3.12.13
# Thu, 11 Jun 2026 01:46:40 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Thu, 11 Jun 2026 02:04:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 02:04:17 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 02:04:17 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 03:05:38 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 03:05:38 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 03:05:38 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 03:05:38 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:99eb1512995af32b91c63bcd418e886af77e3c7ca088226161af558763425461`  
		Last Modified: Wed, 10 Jun 2026 23:38:28 GMT  
		Size: 25.8 MB (25773188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0c92df73d09c97efaed359c70865e4affa5b8bf5242254b7ea428625782e86`  
		Last Modified: Thu, 11 Jun 2026 02:04:25 GMT  
		Size: 3.1 MB (3093609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4348600772da3bc7815b19237e84489bb781213a1154ab3fb66076e6f7013cf2`  
		Last Modified: Thu, 11 Jun 2026 02:04:26 GMT  
		Size: 13.1 MB (13080735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b63dd42ed0695c698e5d3494e6203d8e56145b478eb401fdfe61f224a7aa2a`  
		Last Modified: Thu, 11 Jun 2026 02:04:25 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc67dded18f7f58c250a70fb54b9b5354acac6721f74b8a60de48fcb28f3808c`  
		Last Modified: Thu, 11 Jun 2026 03:05:45 GMT  
		Size: 5.4 MB (5397662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:159a36cc30239e5bb5e605303cd74dd398d52cc27bb51783182d800648b5b53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2590021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030aa5260dd87eb6a6d045af392791fedb07ab8ce6999115008702a6a924ddff`

```dockerfile
```

-	Layers:
	-	`sha256:ec83867b9a60a089355070b1a617f38c785fb452349bb9de114cff8fb924786e`  
		Last Modified: Thu, 11 Jun 2026 03:05:45 GMT  
		Size: 2.6 MB (2581847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75711abbd6b70bbb3b4b219b2b5094314b37994d7df8a6927e8538ebc508233d`  
		Last Modified: Thu, 11 Jun 2026 03:05:45 GMT  
		Size: 8.2 KB (8174 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:927a4680b43f13a85dd85698e4c1139044445d158e4b2c72f83e8c1375093b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44943079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0a42820982176cbe6ad36f9cc0a0560014072323e28d1a37173765490c6fbb`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 02:17:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 02:17:37 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:17:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:17:37 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 11 Jun 2026 02:17:37 GMT
ENV PYTHON_VERSION=3.12.13
# Thu, 11 Jun 2026 02:17:37 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Thu, 11 Jun 2026 02:34:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 02:34:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 02:34:59 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 03:25:01 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 03:25:01 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 03:25:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 03:25:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8ae2378435d99f39097aa4fd0d6c58c08445becca3153d53205b2cc5054b09c2`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 23.9 MB (23944473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5140596476841d7fb1f8962ba135bf43dc2aa46b4214b880e136ffe44bdffcfc`  
		Last Modified: Thu, 11 Jun 2026 02:35:07 GMT  
		Size: 2.9 MB (2928774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06b998886dee689807be4460dc0baf66baad034bf5d995f46251a47299fb86d`  
		Last Modified: Thu, 11 Jun 2026 02:35:07 GMT  
		Size: 12.7 MB (12672062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f4a8e0a8c2412ba596d00184f5f08af953c80ba9620e14810d0189403643e7`  
		Last Modified: Thu, 11 Jun 2026 02:35:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd4abe8ca87785d3c7a38c1beea984c37fbe03e591cc855b0f530056854e8f1`  
		Last Modified: Thu, 11 Jun 2026 03:25:08 GMT  
		Size: 5.4 MB (5397521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:d36db3e1b51fd21c3a9281c73d663276f8e61c88deac4c34b7ec70c09685cf3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccddfffe14c7c5de72e31f5c052caffdbcfc20520d127fdc6b696dfb2dd11f8`

```dockerfile
```

-	Layers:
	-	`sha256:7e7ba50723d3eb1bc34a0c800a6d9c21bc0c318a3ab35c64d3257c56e6a88e25`  
		Last Modified: Thu, 11 Jun 2026 03:25:08 GMT  
		Size: 2.6 MB (2580296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8de13d70cb24d612dd5722610e93a564a31eeb8c3ddc731c92d8b33bae62500`  
		Last Modified: Thu, 11 Jun 2026 03:25:08 GMT  
		Size: 8.2 KB (8174 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:09d3a16fd8bad15e4a68bfe7219f79314c2a6e3071e1f8d6e26e06060a57dfb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50470463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a81d19c0d77cd406ed0442afce9f8d0718600446c1d5affd5bfeb0b98dd723`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:05:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:05:57 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 02:05:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:05:57 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 24 Jun 2026 02:05:57 GMT
ENV PYTHON_VERSION=3.12.13
# Wed, 24 Jun 2026 02:05:57 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Wed, 24 Jun 2026 02:18:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 24 Jun 2026 02:18:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 24 Jun 2026 02:18:07 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 03:24:56 GMT
ENV HY_VERSION=1.3.0
# Wed, 24 Jun 2026 03:24:56 GMT
ENV HYRULE_VERSION=1.1.0
# Wed, 24 Jun 2026 03:24:56 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 24 Jun 2026 03:24:56 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc2ae37f25787137249b55623176297c6852f209431d760db99e2748387b109`  
		Last Modified: Wed, 24 Jun 2026 02:18:15 GMT  
		Size: 3.4 MB (3352678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19441c14bf3fd2108c27c7f831c92502faeb5ec51c114be6112b43d7cb052520`  
		Last Modified: Wed, 24 Jun 2026 02:18:16 GMT  
		Size: 13.6 MB (13597358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d10af0b920bff63f165ae53ac3260d7f61c354d2ecf84462ea7c48dcf9f91c0`  
		Last Modified: Wed, 24 Jun 2026 02:18:15 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79ad895f12e9b1c936672188eb96fef0516bf861f84f9db46b29103b4ae3ecc`  
		Last Modified: Wed, 24 Jun 2026 03:25:04 GMT  
		Size: 5.4 MB (5397760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:59652479f15954325b1f074d1ecfc75898678b9b61b47a21be3a9dac7928c240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2586498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb79a29728be01a80697c5972854c606fd8214443b1e7132db7b8a907864a49`

```dockerfile
```

-	Layers:
	-	`sha256:b9ca8a8c3d0695dd17ca992e96c81931182487a86e025234e54bce1d16362b6a`  
		Last Modified: Wed, 24 Jun 2026 03:25:04 GMT  
		Size: 2.6 MB (2578300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fe00f6a8762555c77f3738c99374d0d0d40cd850fa49553c606153d8a9ecf3e`  
		Last Modified: Wed, 24 Jun 2026 03:25:03 GMT  
		Size: 8.2 KB (8198 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:3919ab2845abdba6099aafcb8459c3364e8f5989e5046cf8e23c807cb932f300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52068374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393ed096341486900bb9e546aa5fa86040b7394af2813e4a32662cdf1abe5751`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:58:32 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:58:32 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:58:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:58:32 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 11 Jun 2026 00:58:32 GMT
ENV PYTHON_VERSION=3.12.13
# Thu, 11 Jun 2026 00:58:32 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Thu, 11 Jun 2026 01:10:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 01:10:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 01:10:27 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 02:39:45 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 02:39:45 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 02:39:45 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 02:39:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:707460b758530d4476f3fefff30544db7cf8dbd98838ccc3533bc05e79016be4`  
		Last Modified: Wed, 10 Jun 2026 23:40:00 GMT  
		Size: 29.2 MB (29225762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18b27c859a4b9f05ca7e4a0a96c9ebfe122b6e6213298415fdfb0c5b7d41824`  
		Last Modified: Thu, 11 Jun 2026 01:10:34 GMT  
		Size: 3.5 MB (3521236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05afbaf5c807ba613ed13e5822abaddc4b22a37e78d1316fc130ab1bcb8c346`  
		Last Modified: Thu, 11 Jun 2026 01:10:35 GMT  
		Size: 13.9 MB (13923412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b3a741d56916c16eb1b727d0d8a56708b744e6bb486c96586f4687c1a13618`  
		Last Modified: Thu, 11 Jun 2026 01:10:34 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5509099cd677451338c71f832d3ce0d0c626043a9f9f8d6c70d0078cd77da944`  
		Last Modified: Thu, 11 Jun 2026 02:39:52 GMT  
		Size: 5.4 MB (5397715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:08cbcb6c448083a9fc8afb61ef481807cc5cd13488f72c24401457ae730f7c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2583240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42dfe3c9b62c66a278c4f29d129c554ef883d6fe8dedbd974caa3bc7b16d7774`

```dockerfile
```

-	Layers:
	-	`sha256:f32012f188cc9c0bd67f6bbff8e26621ecb079fd7068404afb6cd46745e11f8c`  
		Last Modified: Thu, 11 Jun 2026 02:39:51 GMT  
		Size: 2.6 MB (2575178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a9f6a82aee4f31badc4da441116af722a8026488bcd9a3ff314f0e3f93d31e3`  
		Last Modified: Thu, 11 Jun 2026 02:39:51 GMT  
		Size: 8.1 KB (8062 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:f7b2766e5fb43f1490f5fd357dfe4e4a902fb5b63145cf24396f1abf1df8f73b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55573187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19847c19a7763a0f4c548b4ed41f524303292928b595962794cdfb638b799c9e`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 08:04:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 08:04:37 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 08:04:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 08:04:37 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 11 Jun 2026 08:04:37 GMT
ENV PYTHON_VERSION=3.12.13
# Thu, 11 Jun 2026 08:04:37 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Thu, 11 Jun 2026 08:24:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 08:24:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 08:24:53 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 12:34:21 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 12:34:21 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 12:34:21 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 12:34:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df23a1d621df44a13c57ed7248157ad455513f239ae5e25e6b29eaead6f702ee`  
		Last Modified: Thu, 11 Jun 2026 08:25:07 GMT  
		Size: 3.7 MB (3725233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b3eb9be153a724b8c68ae96fc1b431c26fbc36d2e1a564971522ac3f6986ab`  
		Last Modified: Thu, 11 Jun 2026 08:25:08 GMT  
		Size: 14.4 MB (14367683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f3598d43e92950f71b3d9a4f225501317274f6432fbdf8aa85f8ed1a5e53cf`  
		Last Modified: Thu, 11 Jun 2026 08:25:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87b8c6e197f7c1b5d0bf81f9c059d5557f746d61622237f94a78664fdde0430`  
		Last Modified: Thu, 11 Jun 2026 12:34:37 GMT  
		Size: 5.4 MB (5398081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:fb00b25b868520b1f69cd6c9d131a812d76f8b9e9a09b3e29474f11ff0c28e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2590671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0d0a5963e6789c2552ee3337cf3ddb714ba90277cff2f6d5699a3621b111ae`

```dockerfile
```

-	Layers:
	-	`sha256:19cfcd5d3944a02f96941b30b45e3f5282744e2d93545cc3eea2bf9b9b19c506`  
		Last Modified: Thu, 11 Jun 2026 12:34:37 GMT  
		Size: 2.6 MB (2582533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e8c65b92d608eabb20b81830cdb0cdb430ee9bba2e0fea738cea34ac2732949`  
		Last Modified: Thu, 11 Jun 2026 12:34:37 GMT  
		Size: 8.1 KB (8138 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:a06368933ad649608ae2ec563f34eec03c27441a6ed3df61855a057b73d72e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48999289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19dc74a16c701c623469a60ab9d99c8abe9748a9916373d97ed714dcf247ece1`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 02:38:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 02:38:27 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:38:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:38:27 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 11 Jun 2026 02:38:27 GMT
ENV PYTHON_VERSION=3.12.13
# Thu, 11 Jun 2026 02:38:27 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Thu, 11 Jun 2026 02:52:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 02:52:42 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 02:52:42 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 04:03:38 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 04:03:38 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 04:03:38 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 04:03:38 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af79bdb71b2537606f616ffffe41e2d11fda0a6c2b10147073c3a3b967b60b7e`  
		Last Modified: Thu, 11 Jun 2026 02:52:55 GMT  
		Size: 3.2 MB (3184065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9e11c9dd2a6f19e4ea2ec911c7e41ee1a438b00ee39aded8241a40e0b409c9`  
		Last Modified: Thu, 11 Jun 2026 02:52:55 GMT  
		Size: 13.5 MB (13523500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03232e70533a23a1994da0a5981b99f21c566c4d0ce685db9912995034398b74`  
		Last Modified: Thu, 11 Jun 2026 02:52:55 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fbea4a8c661c9072aac4e6ac5b9f5d58c6c7851a041e569e494ef3ba6ced0a`  
		Last Modified: Thu, 11 Jun 2026 04:03:50 GMT  
		Size: 5.4 MB (5397967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:16d3c523840d621cfefb7cf8defe608c363231faca36974d9f935f56b06a8bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4157e1396c51a7903eb774fd7a5f796b0d5ad108874d00f2b4796599e292b0b4`

```dockerfile
```

-	Layers:
	-	`sha256:12fa59287a901d8d66e12fb72819c3cb872a42294ead3d97e865c93c805c16e7`  
		Last Modified: Thu, 11 Jun 2026 04:03:49 GMT  
		Size: 2.6 MB (2574843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b22d68cf5b58bc57493dc229f1d0467c236b505a8d97ae8b9f03d10f762789fb`  
		Last Modified: Thu, 11 Jun 2026 04:03:49 GMT  
		Size: 8.1 KB (8094 bytes)  
		MIME: application/vnd.in-toto+json
