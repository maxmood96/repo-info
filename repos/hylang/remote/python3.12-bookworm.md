## `hylang:python3.12-bookworm`

```console
$ docker pull hylang@sha256:3f3f93a4d9a9a3ed64c89024846bdde6d5ec2018ba7527eac91394df6cf72421
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
$ docker pull hylang@sha256:4b07c3cce7cb4abc7bdec2188bbb8c3610d64aa4b0741211b098dc4a34ec9d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50815508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29177d94d62b4e602fe658e76936c51c31dfd7c1c4e6cea7a30b3ab26b41609`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:43:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:43:33 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:43:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:43:33 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 May 2026 23:43:33 GMT
ENV PYTHON_VERSION=3.12.13
# Tue, 19 May 2026 23:43:33 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Tue, 19 May 2026 23:52:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 19 May 2026 23:52:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 May 2026 23:52:20 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:11:55 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:11:55 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:11:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:11:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988ba5750b9a7e94fc9eda0929f56976755ce1115186e927c8bfaa5ab9798e97`  
		Last Modified: Tue, 19 May 2026 23:52:28 GMT  
		Size: 3.5 MB (3519877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a2e613d3a2b1f19d3f89d1e05fee6d93893d4cc3f1240a20d009695c57d4ba`  
		Last Modified: Tue, 19 May 2026 23:52:28 GMT  
		Size: 13.7 MB (13667611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afabb36019431382d3ba4e572413b7fcadd4e212ab25705bbc71cfe69b614ad`  
		Last Modified: Tue, 19 May 2026 23:52:28 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1697f1353912df39a871f260f565faf473623612aeb3e713a6028ca29792ed9f`  
		Last Modified: Wed, 27 May 2026 00:12:02 GMT  
		Size: 5.4 MB (5394227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:8ab2a773f01af3949d8019578a22b6d9de1308fb76ea5550958fc07d85394377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2586103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a876a4cf37c8e7b3b26438f9170481224bfe6a20f4714451dba174291a617a`

```dockerfile
```

-	Layers:
	-	`sha256:5f6ff563e1af50ae92350b91dfe7e95078b28c5718082c142b03860aae3435db`  
		Last Modified: Wed, 27 May 2026 00:12:02 GMT  
		Size: 2.6 MB (2578009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7021b02cbd019f5f905e52fc0518aba2eaac74015601cbda355532de8d032881`  
		Last Modified: Wed, 27 May 2026 00:12:02 GMT  
		Size: 8.1 KB (8094 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:5016d85eb39921fe71945f7e815f59337ef78b535a466ddcf251d280e2895508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47337239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3b69819d5a717875860cd2d330a9495bb63d179e252ea8474e39c115c1f199`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:17:32 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:17:32 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:17:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:17:32 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 May 2026 00:17:32 GMT
ENV PYTHON_VERSION=3.12.13
# Wed, 20 May 2026 00:17:32 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Wed, 20 May 2026 00:35:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 20 May 2026 00:35:09 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 00:35:09 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:10:35 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:10:35 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:10:35 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:10:35 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3e5afa2eeb01167c187727ebcf5bb90554d4e6dd21fe61f1f694b128ceb15ac1`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 25.8 MB (25768291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5200a3960b177d32c4d52109aabba846dd13fc11be68adfe3d4d6214f2db4a82`  
		Last Modified: Wed, 20 May 2026 00:35:18 GMT  
		Size: 3.1 MB (3093137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd6786c92152dffe73308d90d62a82c37231ccfb0067c10a2a0e30dadbcc216`  
		Last Modified: Wed, 20 May 2026 00:35:18 GMT  
		Size: 13.1 MB (13081252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7516a76a36ff1398a0d4b1209e171519e3c19f993a9b7769f8bd69feff52c5`  
		Last Modified: Wed, 20 May 2026 00:35:18 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19946b079394b1668da2a0a118412e60b0c2be6f8c7f7083aa8375276e67fee`  
		Last Modified: Wed, 27 May 2026 00:10:42 GMT  
		Size: 5.4 MB (5394310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:677cf906e7f87dde6b237752f7bbace4f56950bbc7cf47a2097550d701d9ebf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2590002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca23e39c76a9fe6e4833ac8c7cad9fc8ae8620e13c87482a67398b5148f82b8`

```dockerfile
```

-	Layers:
	-	`sha256:0ac240eadae6eae058c95404b1de597c250af248b6ad326e175fed2b674d4351`  
		Last Modified: Wed, 27 May 2026 00:10:42 GMT  
		Size: 2.6 MB (2581829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c782355acfe2587ff769e3e0da4d1f7549a1e22639102501adaba18d745a58f0`  
		Last Modified: Wed, 27 May 2026 00:10:41 GMT  
		Size: 8.2 KB (8173 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:5e7112cbe09e3a0e1a57897c8b5c9c871d7a2388689567bcadc9445486692eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44937443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13a6a545f9fbae334d5e833926d257722e5a15571d29c7c5cd77193827fe8b8`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:52:03 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:52:03 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:52:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:52:03 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 May 2026 00:52:03 GMT
ENV PYTHON_VERSION=3.12.13
# Wed, 20 May 2026 00:52:03 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Wed, 20 May 2026 01:08:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 20 May 2026 01:08:48 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 01:08:48 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:11:39 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:11:39 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:11:39 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:11:39 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:af86988b12731b7fa2ac73fa1c3f6ab4510a6641d04afb18df09600383bc399d`  
		Last Modified: Tue, 19 May 2026 22:36:05 GMT  
		Size: 23.9 MB (23941643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a244aa94780028d8063612dc99530276b93b954b021659cf36b621c49ffcb1e`  
		Last Modified: Wed, 20 May 2026 01:08:56 GMT  
		Size: 2.9 MB (2928562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434e8cc731c97600d88bac1d6fa4e481cb8335a6c7459756fdd6016063502082`  
		Last Modified: Wed, 20 May 2026 01:08:56 GMT  
		Size: 12.7 MB (12672655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2340456cb44358b91b04027a6fc6bfde9e907477f73e534b146658c8af37652`  
		Last Modified: Wed, 20 May 2026 01:08:56 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96717bb20dc01021d61f8059e64d557bd045aabbc8b8b4aff1e8adafc90017e`  
		Last Modified: Wed, 27 May 2026 00:11:46 GMT  
		Size: 5.4 MB (5394333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:569b8cfa26ab49ef51c7b15a417abfc5de11520e50838d2316309e8e473e0138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a416145c88bfaa6a3bca798a9856dc498aa0f44e71e88187ec1342df005819f8`

```dockerfile
```

-	Layers:
	-	`sha256:7785b8d5d37f5e1f111cd695d4c5d3e74098cf689659c5f409d3b07f6cf46c44`  
		Last Modified: Wed, 27 May 2026 00:11:46 GMT  
		Size: 2.6 MB (2580278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd2c567a8619395144aa1e1d6eeafb6b45febc483242b2e6e21c7eba3908cbbc`  
		Last Modified: Wed, 27 May 2026 00:11:46 GMT  
		Size: 8.2 KB (8174 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:b0a26908caf00d8795ba4dc37f6c462b94cbb4338642a17329aa7ed78f7a6255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50458919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80e5198f764eabfc05bfdab53080471a8bbaf3919fa708471fb3b18484fdc1d`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:48:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:48:01 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:48:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:48:01 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 May 2026 23:48:01 GMT
ENV PYTHON_VERSION=3.12.13
# Tue, 19 May 2026 23:48:01 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Tue, 19 May 2026 23:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 19 May 2026 23:59:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 May 2026 23:59:29 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:11:41 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:11:41 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:11:41 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:11:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca322326d18643da145ed52fad22eba23f9c344331bad70514a30f4d17e4ed19`  
		Last Modified: Tue, 19 May 2026 23:59:38 GMT  
		Size: 3.4 MB (3351867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0e6b48e902d579d701d2bc29a3978af06e898b5a3c61f32612c14da12175d4`  
		Last Modified: Tue, 19 May 2026 23:59:38 GMT  
		Size: 13.6 MB (13597408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b667dd5a47567d37d5d56447d8b3d9324da830b4a96acaae9965f91e48df7d73`  
		Last Modified: Tue, 19 May 2026 23:59:37 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbc6e60179678fe0db4a84b484821425e1dbb85d8b0e562064d3c2935f81973`  
		Last Modified: Wed, 27 May 2026 00:11:48 GMT  
		Size: 5.4 MB (5394351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:674f74713c335650e99ec0643e58fa4e4837b3859fe8b60d6ed7e92eda566c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2586479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c130239584d06ac49224c9aefb48202f7588b68150c5d1fe0e6d37702aa2466`

```dockerfile
```

-	Layers:
	-	`sha256:535197acba3e92507fd0e59ba640e2ccb4aeb8fd84b9c2c8cb56b63b7504919a`  
		Last Modified: Wed, 27 May 2026 00:11:48 GMT  
		Size: 2.6 MB (2578282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bea67a28ffea769043d2008eeda359482f7c53f94e091a6f1635d0c85c504f0`  
		Last Modified: Wed, 27 May 2026 00:11:48 GMT  
		Size: 8.2 KB (8197 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:875c600689d4a3a925cb29169aa50273a8fba163dee4acb7ee761927de310bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52057589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6efb84c1867316abf2093c8dce786a70f4624b78da1c9162c2259d90858994`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:38:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:38:40 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:38:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:38:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 May 2026 23:38:40 GMT
ENV PYTHON_VERSION=3.12.13
# Tue, 19 May 2026 23:38:40 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Tue, 19 May 2026 23:49:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 19 May 2026 23:49:56 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 May 2026 23:49:56 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:10:23 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:10:23 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:10:23 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:10:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:408fe432485bb366e9a4871b553de2e6347ca580fe8a5d45c84c87fa58d5e5c7`  
		Last Modified: Tue, 19 May 2026 22:37:12 GMT  
		Size: 29.2 MB (29218601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf83f1080d49423c623385ffdc685085c75317edca0692e03ff9c012db7e0b`  
		Last Modified: Tue, 19 May 2026 23:50:04 GMT  
		Size: 3.5 MB (3520871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a344cb54752f45badb71f99b86426f05f6412f9c9937122d6a78af46d8be60ac`  
		Last Modified: Tue, 19 May 2026 23:50:04 GMT  
		Size: 13.9 MB (13923700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9782ef1fc3ff6e2b8866609e4a0dcce82aef3c648e4155fc1118709be534d804`  
		Last Modified: Tue, 19 May 2026 23:50:04 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77453df62137963dbaf51aa0049fa2c79233f2a90d46280e348806d0320e030`  
		Last Modified: Wed, 27 May 2026 00:10:30 GMT  
		Size: 5.4 MB (5394168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:b6a8188aa882445572f222e33210610ae26ac62788a1bb98e671c486bd6f5a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2583222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912fda3c69af159c48afa99e4078b1653e22629d5d792335d4b85cd193c2a193`

```dockerfile
```

-	Layers:
	-	`sha256:710a66aaef6810188ff26c71a0dd05ee671e8fc444019e0972c564fd62da0603`  
		Last Modified: Wed, 27 May 2026 00:10:30 GMT  
		Size: 2.6 MB (2575160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d311de976ae353cf23722cf909f406b3e1693bd27649f7a5951db7d6160d0f4`  
		Last Modified: Wed, 27 May 2026 00:10:30 GMT  
		Size: 8.1 KB (8062 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:765cfbd7d5bc15d37915606b18295604abc39b0938bafd00a85f7fb0d00242c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55563550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cea513a9fa39b24abdb34a651b5344c94631f5cb51a42229537723bd55f5870`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 04:33:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 04:33:44 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 04:33:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 04:33:44 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 May 2026 04:33:44 GMT
ENV PYTHON_VERSION=3.12.13
# Wed, 20 May 2026 04:33:44 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Wed, 20 May 2026 04:53:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 20 May 2026 04:53:22 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 04:53:22 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:22:41 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:22:41 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:22:41 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:22:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9992109105b99d139cd44d383159fc226ead8096c0467c99111f3a441a0537e2`  
		Last Modified: Wed, 20 May 2026 04:53:37 GMT  
		Size: 3.7 MB (3725057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30cbb01a52b0f9b65113e5c2d64f14920b33c0b9797a261d7a1ef4d39546298`  
		Last Modified: Wed, 20 May 2026 04:53:37 GMT  
		Size: 14.4 MB (14368015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945b04b5746366ec3629286beb43d48c802330774b251d4b6609a6e1b030ba82`  
		Last Modified: Wed, 20 May 2026 04:53:37 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c4d531da3f294dc8275cb29dc3b6f7334dd5acad311788339a80b004905fda`  
		Last Modified: Wed, 27 May 2026 00:23:01 GMT  
		Size: 5.4 MB (5394487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:984e2132e4e67494a956eba4e9d4e8e4ab2939622e0330d67a4ca757bab2c89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2590651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f21cd3e0a0f92f7615971d964cf98d95ee70eed251fc698ef39a62e84cc3d0`

```dockerfile
```

-	Layers:
	-	`sha256:9ed495d49aae140a2e54c6cb64bdc2e3fd9716ae29dab24b6e710714226c9bf5`  
		Last Modified: Wed, 27 May 2026 00:23:01 GMT  
		Size: 2.6 MB (2582515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbdcf5b6648c3070a92f6f82058200cd31b0cee8bfe18fa5653d1450866d0446`  
		Last Modified: Wed, 27 May 2026 00:23:01 GMT  
		Size: 8.1 KB (8136 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:efb32de61c5cc441acd82f9d1110b570dae9158e5a5fa208cd96245515ae7cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48994657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc7ef5b90fd71c16367ac662f85fe9dc4d9f47ff3393c734f7fd55691ec9a91`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:15:32 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:15:32 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 01:15:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:15:32 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 May 2026 01:15:32 GMT
ENV PYTHON_VERSION=3.12.13
# Wed, 20 May 2026 01:15:32 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Wed, 20 May 2026 01:28:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 20 May 2026 01:28:50 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 01:28:50 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:17:25 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:17:25 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:17:25 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:17:25 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908d95ecc58e29f001750d357eea736423e2548d14ad0d284c6c148dd3071050`  
		Last Modified: Wed, 20 May 2026 01:29:03 GMT  
		Size: 3.2 MB (3184031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3831d52a4b9d8ae96e25741f6fbb86f10ad813efa9f180effa31a628a049066b`  
		Last Modified: Wed, 20 May 2026 01:29:03 GMT  
		Size: 13.5 MB (13527164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cf566d4b09b61c05c6671e3b79d675b0b09cbe98a99edfa6979eb14d594cc2`  
		Last Modified: Wed, 20 May 2026 01:29:03 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2403443c7d19cd0ee69bf378e5fc346bccf4214ba5cb596131e673e1e8e124`  
		Last Modified: Wed, 27 May 2026 00:17:45 GMT  
		Size: 5.4 MB (5394616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:e3c3291db308d2a285ede63ef8723aa417295a86c5be621e5a84fa4dafffc9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82aa793c04a0963b3b799bdc64d40f014248901b23e5b938757b3ccda2fc8516`

```dockerfile
```

-	Layers:
	-	`sha256:b005d9bd4baa04316378d549cec0c38b021b0a4ebde59773a537be0745b54faa`  
		Last Modified: Wed, 27 May 2026 00:17:44 GMT  
		Size: 2.6 MB (2574825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09368bb6ca24e6bc7c522dbd1b70788556f91bbfcce9f281bd274ed24d4fc445`  
		Last Modified: Wed, 27 May 2026 00:17:44 GMT  
		Size: 8.1 KB (8094 bytes)  
		MIME: application/vnd.in-toto+json
