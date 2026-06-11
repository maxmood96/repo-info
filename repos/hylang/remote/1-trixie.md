## `hylang:1-trixie`

```console
$ docker pull hylang@sha256:509c3ee2531b857778ff539a3220c9f8dc2e2ae67c98558386478bf3d7c7cdb7
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

### `hylang:1-trixie` - linux; amd64

```console
$ docker pull hylang@sha256:709382422e9ad085f7594602668deacd35e0c96947890e71b914662fbb8df75a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52092187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7286671bf0d0c56744ab91322029d236158e8cd7e765ad729647b983f579d7`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Wed, 10 Jun 2026 20:38:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:38:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 10 Jun 2026 20:38:22 GMT
ENV PYTHON_VERSION=3.14.6
# Wed, 10 Jun 2026 20:38:22 GMT
ENV PYTHON_SHA256=143b1dddefaec3bd2e21e3b839b34a2b7fb9842272883c576420d605e9f30c63
# Wed, 10 Jun 2026 20:45:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 10 Jun 2026 20:45:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jun 2026 20:45:55 GMT
CMD ["python3"]
# Wed, 10 Jun 2026 20:59:37 GMT
ENV HY_VERSION=1.3.0
# Wed, 10 Jun 2026 20:59:37 GMT
ENV HYRULE_VERSION=1.1.0
# Wed, 10 Jun 2026 20:59:37 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jun 2026 20:59:37 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be37d830c486da8461cecc8af4382b008ca0ce9689b4ee878d7bbdd7fef4cbf8`  
		Last Modified: Wed, 10 Jun 2026 20:46:03 GMT  
		Size: 4.3 MB (4262148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f0102b8ec8a90db393e9a2ff03f3b92cf046909ccc5a94c297481cd05694fc`  
		Last Modified: Wed, 10 Jun 2026 20:46:03 GMT  
		Size: 12.3 MB (12336112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4001ea6ba59f4895c65ae40f77b17df9fab5102b36a217f10029224e62d73e87`  
		Last Modified: Wed, 10 Jun 2026 20:46:03 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadf8f6d266086dc4287a6e6277a6395694e1e3b5f613a8f81cab67424573112`  
		Last Modified: Wed, 10 Jun 2026 20:59:44 GMT  
		Size: 5.7 MB (5713750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:314de69d5618ac49499d5ffc0cb69273fa0afd92a2bbfb2ee3ea0dd4226e5bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f186deef8bcb56859ae74e5a942b5d33ae4b929f28950c1bb160f212d65b3b96`

```dockerfile
```

-	Layers:
	-	`sha256:bdd3d694cbd2e04df063def86cc7cb7a9acdc369c01be759b463bffb47878d29`  
		Last Modified: Wed, 10 Jun 2026 20:59:44 GMT  
		Size: 2.2 MB (2156691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62a0ba2b9951baa1d5786b6bb8f28c1897f04a9528ee290b0c000fa6b827b505`  
		Last Modified: Wed, 10 Jun 2026 20:59:44 GMT  
		Size: 11.6 KB (11643 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-trixie` - linux; arm variant v5

```console
$ docker pull hylang@sha256:d3448b97ee8213529f79beaa3b533a16ec778af5ea155e775592a019aff6b4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49336804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2d595b8668d145e36739900c60dd2e7df91da8d7dfbb5429f9e41b3124d525`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Wed, 10 Jun 2026 20:40:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:40:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 10 Jun 2026 20:40:33 GMT
ENV PYTHON_VERSION=3.14.6
# Wed, 10 Jun 2026 20:40:33 GMT
ENV PYTHON_SHA256=143b1dddefaec3bd2e21e3b839b34a2b7fb9842272883c576420d605e9f30c63
# Wed, 10 Jun 2026 20:50:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 10 Jun 2026 20:50:57 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jun 2026 20:50:57 GMT
CMD ["python3"]
# Wed, 10 Jun 2026 21:19:55 GMT
ENV HY_VERSION=1.3.0
# Wed, 10 Jun 2026 21:19:55 GMT
ENV HYRULE_VERSION=1.1.0
# Wed, 10 Jun 2026 21:19:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jun 2026 21:19:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65f533a486c27ec4e09f64cedf4c24f235318094728b927cc0cdf6b54c65b12`  
		Last Modified: Wed, 10 Jun 2026 20:51:05 GMT  
		Size: 3.7 MB (3655837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f34defd4dbe8a1a36008f2646bb1b11dab63c40aa300c13d97eee176b4cfad`  
		Last Modified: Wed, 10 Jun 2026 20:51:05 GMT  
		Size: 12.0 MB (12012991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f4ad91e4ada5f53d8d27573e3ea685a36ed73a3548413de870f14b913db310`  
		Last Modified: Wed, 10 Jun 2026 20:51:05 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e186015c06418aafe423f8d9cd505b18aafa38506dfdbf9e024ca1df9b50b6`  
		Last Modified: Wed, 10 Jun 2026 21:20:02 GMT  
		Size: 5.7 MB (5713857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:935a110010107cdb298b2a9bb97f076f50bd1369c8a64788d848b0a680eaf56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2171575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96cdbdb303ac5bc5c8e4db86b7d61c07afbc27f16c136c2c8f2184aa5c062440`

```dockerfile
```

-	Layers:
	-	`sha256:17c1a21723e64478ca02e661bfddc81238a6c62314e7702b192d14e519f451f5`  
		Last Modified: Wed, 10 Jun 2026 21:20:02 GMT  
		Size: 2.2 MB (2159756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58eaa8e8e6f5bbb2f5e89b79aed9b44bd1d9ed467a3148b7d3c22700161a48b4`  
		Last Modified: Wed, 10 Jun 2026 21:20:02 GMT  
		Size: 11.8 KB (11819 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-trixie` - linux; arm variant v7

```console
$ docker pull hylang@sha256:bd4d8b05932b579b1170de6311bcc7104464ace82079b53fa0e8e51310dfe9e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44860168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6c57c44a00b35feaf069fdddff6d6b6fed1cd2d480b223c43286d0c211bf8a`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:48:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:48:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:48:30 GMT
ENV PYTHON_VERSION=3.14.5
# Wed, 20 May 2026 00:48:30 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Wed, 20 May 2026 00:59:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 20 May 2026 00:59:50 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 00:59:50 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:45:28 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:45:28 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:45:28 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:45:28 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9bb2f873b2a38628613ae85598c5e811279dc4d198ad8c328ce5be8557fa31`  
		Last Modified: Wed, 20 May 2026 00:59:57 GMT  
		Size: 1.2 MB (1249140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232dc2b669dfe2c1f293ece8e6ab9da3c3dbbc3e821779f917ca40e786bdbc3b`  
		Last Modified: Wed, 20 May 2026 00:59:58 GMT  
		Size: 11.7 MB (11693170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959a0f0aab1a0b6f1ce2660aee0c74c165eacf8f625b3cdc79264b4f6f11b41b`  
		Last Modified: Wed, 20 May 2026 00:59:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f7b41c528bb226d68cda9373294b77ed453f26d22297a240321333f970c73d`  
		Last Modified: Mon, 08 Jun 2026 22:45:35 GMT  
		Size: 5.7 MB (5711777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:6292ae766ac349e4519291c25096d4897c7fff0e42bc39bbad8cd1a22031eec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2170028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3465e77778e12f8230cff94855b76132e8e22c112bfdc4636e00461e13895163`

```dockerfile
```

-	Layers:
	-	`sha256:d011e28aca91eac6393e8e79ff4003db0ae539ced990a3f7a67a8d170bf8a6cc`  
		Last Modified: Mon, 08 Jun 2026 22:45:35 GMT  
		Size: 2.2 MB (2158209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbf897fb968a8b258994980fffedfde85a76d280a1e268a23aa4f4d5273ae74c`  
		Last Modified: Mon, 08 Jun 2026 22:45:35 GMT  
		Size: 11.8 KB (11819 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-trixie` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:741878e8abb08fab55777b03cf19df81c8839544a0448b067a615cffcae9d350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49383316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d74791919f018d4bf79879b519153203ac860e7881f86de391b40cb13315ef6`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:01:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:01:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 01:01:09 GMT
ENV PYTHON_VERSION=3.14.6
# Thu, 11 Jun 2026 01:01:09 GMT
ENV PYTHON_SHA256=143b1dddefaec3bd2e21e3b839b34a2b7fb9842272883c576420d605e9f30c63
# Thu, 11 Jun 2026 01:08:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 01:08:45 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 01:08:45 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 02:40:43 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 02:40:43 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 02:40:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 02:40:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97b6eb0baf41e8e071245217af2edd0320b77237e74ede5085251d49577742b`  
		Last Modified: Thu, 11 Jun 2026 01:08:53 GMT  
		Size: 1.3 MB (1274110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd0cea519b3ec8c1964679483e8c8da68f3dc77d55f8f323301dc330479485f`  
		Last Modified: Thu, 11 Jun 2026 01:08:54 GMT  
		Size: 12.2 MB (12246817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef566a1a023aad5f4f486511740610bca6b3ac93b0439bfef2684152336bd88c`  
		Last Modified: Thu, 11 Jun 2026 01:08:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861010934b26c0bd227e4bae9027f03728b56a1feffbcb6a15eb1234d1e3e367`  
		Last Modified: Thu, 11 Jun 2026 02:40:50 GMT  
		Size: 5.7 MB (5713610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:3e75cac11716d73568245fa7e93f8e4c652ff5a2491189d17c40284a036999fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5b9faf84ff45541b9303376c93d1a36342e6ef4224d324e9a87cfc63cab139`

```dockerfile
```

-	Layers:
	-	`sha256:61af85a986b4fcb48a5a7052736d15d5811251a757398d3284d081320b1ac9dc`  
		Last Modified: Thu, 11 Jun 2026 02:40:50 GMT  
		Size: 2.2 MB (2157093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a2349fb6a5f3e1d37b188f104bc8129266b4fb3bf9a6efff2fc81a07cd56dbe`  
		Last Modified: Thu, 11 Jun 2026 02:40:50 GMT  
		Size: 11.9 KB (11891 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-trixie` - linux; 386

```console
$ docker pull hylang@sha256:a338c97a32832608c102bd31598a059dd18684cba624620321f44e121c93fbcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50787281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f702befb1aba95e7a3325434d218b512095105a0f83f24ba0b57b4040ddd00b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:56:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:56:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:56:49 GMT
ENV PYTHON_VERSION=3.14.6
# Thu, 11 Jun 2026 00:56:49 GMT
ENV PYTHON_SHA256=143b1dddefaec3bd2e21e3b839b34a2b7fb9842272883c576420d605e9f30c63
# Thu, 11 Jun 2026 01:17:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 01:17:56 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 01:17:56 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 02:39:32 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 02:39:32 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 02:39:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 02:39:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c0793083304481934d46b624a2f0b982b713d34bdda56855232cecc6973414`  
		Last Modified: Thu, 11 Jun 2026 01:18:04 GMT  
		Size: 1.3 MB (1297731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fb484000e3356c68bd6163578441f98bee5ce09aad77db318a9403633c9acd`  
		Last Modified: Thu, 11 Jun 2026 01:18:04 GMT  
		Size: 12.5 MB (12474018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af72c0f1f3a23cea9213fb87d297cb35f145c290308a25e4cf6cc5f8b0155d3`  
		Last Modified: Thu, 11 Jun 2026 01:18:04 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cc2be8f984f646a508d52c649224492bd997bb8a6cf79156ea6f57d0deefa1`  
		Last Modified: Thu, 11 Jun 2026 02:39:39 GMT  
		Size: 5.7 MB (5714088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:e7ca495fd50b72aff0fe78e44a3118187c04b68231829a4473210f607718d07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a4096f21d6cc7db3e78c92096eab4960b543e62801e2a4cda0f3ac3d675dfe`

```dockerfile
```

-	Layers:
	-	`sha256:eeb3d33348d0bdbffea3672b6f7bea81558eb320e353a99b361eff5bbd2172eb`  
		Last Modified: Thu, 11 Jun 2026 02:39:39 GMT  
		Size: 2.2 MB (2153812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98dab86ac8cc719e5438a7969e12abf5a3439f08592e7a4c741c54237f6016eb`  
		Last Modified: Thu, 11 Jun 2026 02:39:39 GMT  
		Size: 11.6 KB (11550 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-trixie` - linux; ppc64le

```console
$ docker pull hylang@sha256:857d829fc298674f842c822c37dd7e0767bb39eba795a0ab6f7247c362c15988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53372687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c5a07a23142186b8a48aa38b9dd5b9bbfd288f102a77cef873d39a5c037617`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 02:52:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 02:52:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:52:51 GMT
ENV PYTHON_VERSION=3.14.5
# Wed, 20 May 2026 02:52:51 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Wed, 20 May 2026 03:37:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 20 May 2026 03:37:56 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 03:37:56 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 23:13:47 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 23:13:47 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 23:13:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 23:13:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bf42993f8ddcb8239db7203cca564245875086e6cd25916329cda86b12722c`  
		Last Modified: Wed, 20 May 2026 03:15:49 GMT  
		Size: 1.3 MB (1321276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e61558d17aebc279e58f876aa2b61163b3ede117292ac23074727cf1af8d4`  
		Last Modified: Wed, 20 May 2026 03:38:10 GMT  
		Size: 12.7 MB (12738775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb72edae4144e59197d9f061944f8463bfa8b05d2af1a5afc3fc8f9a9117ebb`  
		Last Modified: Wed, 20 May 2026 03:38:09 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8347ff83ac48f2360e0bb31642a2457308c64f8b80311347333378f7ab0baed4`  
		Last Modified: Mon, 08 Jun 2026 23:14:03 GMT  
		Size: 5.7 MB (5711933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:f475a8cb37da453adfeb83685610473921ba841f18ac23fd24d37c7830c84dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1923a53abc1f7a35aefc39d5a26f4ec38df6e58829c155989ecc61e5ba4a8dcb`

```dockerfile
```

-	Layers:
	-	`sha256:5b2d71bd3fa8c22f4ff4ebf70922f17860195bc61501b7ce548e3d4743d0488e`  
		Last Modified: Mon, 08 Jun 2026 23:14:02 GMT  
		Size: 2.2 MB (2160330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dfd47fa0eb08fd51b6038c569ce5a74cf79a415c434a1de4f88df94f9eb86e8`  
		Last Modified: Mon, 08 Jun 2026 23:14:02 GMT  
		Size: 11.8 KB (11758 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-trixie` - linux; riscv64

```console
$ docker pull hylang@sha256:27772de0f7f7ba153e402bf4fc6ff3ff6f81461481038cee5c02609151df4ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47589960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccbbcc3d3083807c4a1ccaef8cf18bbf03e8c538dbc186953f6f5a1e7aa71e9f`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 22:49:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 May 2026 22:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 21 May 2026 22:49:23 GMT
ENV PYTHON_VERSION=3.14.5
# Thu, 21 May 2026 22:49:23 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Fri, 22 May 2026 02:09:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 22 May 2026 02:09:02 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 22 May 2026 02:09:02 GMT
CMD ["python3"]
# Tue, 09 Jun 2026 08:33:38 GMT
ENV HY_VERSION=1.3.0
# Tue, 09 Jun 2026 08:33:38 GMT
ENV HYRULE_VERSION=1.1.0
# Tue, 09 Jun 2026 08:33:38 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Jun 2026 08:33:38 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1903f08bd509a376c3c8569e83e6ede0ced718aecf8dc410b5f415b30e27b9ba`  
		Last Modified: Fri, 22 May 2026 00:31:18 GMT  
		Size: 1.3 MB (1261204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1fcb60634edb7295afacb1e8d82788663dc31e4268ec8786c6f060c41f33d6`  
		Last Modified: Fri, 22 May 2026 02:10:09 GMT  
		Size: 12.3 MB (12338128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c90a5c1c7f9c51008262cc1966274d718a7ebfe4189be6ef3a92c2d1f1b187a`  
		Last Modified: Fri, 22 May 2026 02:10:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8dffcea8dcc5059f8efb4744ade7c6e7b3eaaec0e9809651a068738ecccf329`  
		Last Modified: Tue, 09 Jun 2026 08:34:46 GMT  
		Size: 5.7 MB (5712781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:77ca51feb649b236622877966a01fefb745e010cb852ef0ef4564fd26aa646d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2162460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8d0ff9a93cbb977b5eda22e883a04a864fc45da09f3a69f736d61cab6757b4`

```dockerfile
```

-	Layers:
	-	`sha256:8907aa631b14e71c264aecb9c4d9624687ee359ad69a494913b28eab1cbfff01`  
		Last Modified: Tue, 09 Jun 2026 08:34:43 GMT  
		Size: 2.2 MB (2150701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31f95e65b14ad357414ba73898bcbabfa40239951ae593209bd102c6be93583c`  
		Last Modified: Tue, 09 Jun 2026 08:34:38 GMT  
		Size: 11.8 KB (11759 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-trixie` - linux; s390x

```console
$ docker pull hylang@sha256:67d36aeefe8aced9a81b300ba46d8c85b926c72b77153cb88668bd4985a45e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49233928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da29b4e0ffee017f0c3b24a5c3278a8eda0004afe8a422b5fa15bb7dcfc41f0`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:58:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:58:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:58:04 GMT
ENV PYTHON_VERSION=3.14.5
# Wed, 20 May 2026 00:58:04 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Wed, 20 May 2026 01:06:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 20 May 2026 01:06:42 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 01:06:42 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:54:27 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:54:27 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:54:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:54:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d411acf534ef647eede4adcd91ed47b044aed46d5bab39dff8cf46b5c41606`  
		Last Modified: Wed, 20 May 2026 01:06:54 GMT  
		Size: 1.3 MB (1305801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d466ca01a7946f036d78a2ce92c5ea2262bd364cc5afa9f96a961463660e4974`  
		Last Modified: Wed, 20 May 2026 01:06:54 GMT  
		Size: 12.4 MB (12370138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7563e7bf20dca778256ffc3f7aeaddef6c5685202d460d1d13b372df24ed5df4`  
		Last Modified: Wed, 20 May 2026 01:06:54 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4a269000f24395f8e3f628fe9b48916ae355ff0eda10a95d8821cbb0aa39df`  
		Last Modified: Mon, 08 Jun 2026 22:54:42 GMT  
		Size: 5.7 MB (5711815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:73fd1cb4e51b19acb5f32b84b871ad8f64a655271849fbbe625108a18d25019c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91057295d369042efb39e9efee3920e80dfe3ef78d9e93443bf8b3974d5f7f35`

```dockerfile
```

-	Layers:
	-	`sha256:6bea07bb267e78295fb81f6c06bbbeca25caf0bed9de694f437f846bebaace30`  
		Last Modified: Mon, 08 Jun 2026 22:54:41 GMT  
		Size: 2.2 MB (2158130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e8b7d69b0d3d68fef262ca2a09cfc843517bfdcba98c71592f6f0621a390366`  
		Last Modified: Mon, 08 Jun 2026 22:54:41 GMT  
		Size: 11.6 KB (11643 bytes)  
		MIME: application/vnd.in-toto+json
