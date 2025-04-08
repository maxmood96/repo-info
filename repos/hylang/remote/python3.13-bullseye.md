## `hylang:python3.13-bullseye`

```console
$ docker pull hylang@sha256:f3d32f3d0ec12424d2d52ddc28410157110770b35a26737896393884737c4fd0
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

### `hylang:python3.13-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:5ce84752bbf1bdbefda4ef840ebebf9434fee523ad9f9bd39809023d3a309379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49796293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362948022e02f377085fb9e2d7647de8cf99b929abab0b2d6ac8a3c498251267`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 23:51:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_VERSION=3.13.2
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de88ae1afa229fa9359a1314df064890f3015dc47db4ed27fd303e6df4f81afb`  
		Last Modified: Tue, 08 Apr 2025 01:43:14 GMT  
		Size: 1.1 MB (1076230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d809190c108480d6b998ba1c3f5bb89e20dc0d28b65e0cd98d2ff66bdbcf801`  
		Last Modified: Tue, 08 Apr 2025 01:43:14 GMT  
		Size: 12.8 MB (12754694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187587022ae14a95f4686c18d4a343ae9218032bb5379c9ab89f9a7e8f3ca5e7`  
		Last Modified: Tue, 08 Apr 2025 01:43:13 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6ad311698ecffe29f84ee3ca3368de62f76bf0daab3845f608949496baa568`  
		Last Modified: Tue, 08 Apr 2025 02:22:09 GMT  
		Size: 5.7 MB (5707699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:6e49038aa193a975ba34e4d186fb65ad2a156bb7aca8e2e00aff3b52e63f360c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4b087b6fb8bcee889908595180ee4dc4e659e3f81360da1d7f890fcc0f4306`

```dockerfile
```

-	Layers:
	-	`sha256:3d9a9b066c888189ca65ecbb46160912178139bcdd1432cb5d992458ceee7fb3`  
		Last Modified: Tue, 08 Apr 2025 02:22:09 GMT  
		Size: 2.7 MB (2713530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db91d1a825534123a103c163b3505a656818f1082e493ad62c3a582f5929de26`  
		Last Modified: Tue, 08 Apr 2025 02:22:09 GMT  
		Size: 9.2 KB (9244 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:f9e4350449d0728217c497a7f7639db6cca467fae91a0283c56d6ce3a724043f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44027978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6aebc87cc0796b4011d5e1447b2edb8be38a1440b82780968a16f565dfe9af`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 23:51:20 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_VERSION=3.13.2
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3687c9079028ac9bf763326f4be55b4e440b37b5baf0c4529715d811c7ec1718`  
		Last Modified: Mon, 17 Mar 2025 22:19:22 GMT  
		Size: 25.5 MB (25535344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2472098f339c2b65ac1f01cc9c347f156c8b748a53c02f84fb39dfb959f08b31`  
		Last Modified: Tue, 18 Mar 2025 00:52:20 GMT  
		Size: 836.9 KB (836945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f97a890b55cb9ae1b83acd5961e23f5a471cf0eb4eca266f2d6c1bcf917e2d6`  
		Last Modified: Tue, 18 Mar 2025 03:28:22 GMT  
		Size: 11.9 MB (11949595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd54ce1bcb81773c9f5e30b3ffa202971433f14f026800237cf33894d38eb1d`  
		Last Modified: Tue, 18 Mar 2025 03:28:22 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f38044af5d7ff4cbdd06f927043b324e962d0a4e021db2b219addd7e307548`  
		Last Modified: Wed, 19 Mar 2025 23:28:04 GMT  
		Size: 5.7 MB (5705845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:f7493b558de07614d94304254b4fe75854eed60d0700d7fb62efa19b4fe5f328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2723243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea086b77815c7dbb89d9af637283636c357339e372113f7eb4339289b46a5eab`

```dockerfile
```

-	Layers:
	-	`sha256:3e3580cc79fde3bc400f9e471262f4747166301863408a8c3c8bbd754089df2c`  
		Last Modified: Wed, 19 Mar 2025 23:28:04 GMT  
		Size: 2.7 MB (2713893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75d1c3af398e92b53e58d3c016ebb26e740caaf1d69c607651f93b3480dbf6c1`  
		Last Modified: Wed, 19 Mar 2025 23:28:03 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:cc644c2878b5e37dacaf8a884fb1ecbbcebebf9754379ebd3b78d1c7cfb168fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48093063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da32312166c380eb4b7b2130affb694beb9eab07361d97bb17de3c346439c4f4`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 23:51:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_VERSION=3.13.2
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061c4ed7e226a14984f858fab8d48bd2b7894cc84f65736c63892d15eb807bd2`  
		Last Modified: Tue, 18 Mar 2025 02:20:42 GMT  
		Size: 859.1 KB (859143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fb1b1925de45f3751bf04d440ad5e2085c51e2bad8d8c8b8bac195a89d7af0`  
		Last Modified: Tue, 18 Mar 2025 03:33:22 GMT  
		Size: 12.8 MB (12782190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de27f5aae1dae9347636bcf55c3e028eb0faf07737ee90293e5f2de0a3309966`  
		Last Modified: Tue, 18 Mar 2025 03:33:20 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6b5feed0420988967a9b4fb27705e86610ed66b2f9b805ba321ea85600d906`  
		Last Modified: Wed, 19 Mar 2025 23:15:35 GMT  
		Size: 5.7 MB (5705557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:90ead9b36c6f6b707414e422a8229e2ead46010b0633d245d5320d48a0bd4dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2721317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7431d75ce2ef684556cd000c901af9236a6c33e0fb75e813a81428e762e765b8`

```dockerfile
```

-	Layers:
	-	`sha256:e1d2ebeb49932d90cc0dda5068eb42e2fe300409d510b7fb935b62a039163ab9`  
		Last Modified: Wed, 19 Mar 2025 23:15:34 GMT  
		Size: 2.7 MB (2711923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3ecd32a604104d2077040e20d329ab383799d0082222847d7904bba84a90eaf`  
		Last Modified: Wed, 19 Mar 2025 23:15:34 GMT  
		Size: 9.4 KB (9394 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:274a7562f4339da7322ce4f91244e082a7b64abcc91ede4b7e6c8ecb150e26b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50880015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224f1b1135d3063af9439bae42de9dc3f0397532b30ce16b873a9c7ffae29825`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 23:51:20 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_VERSION=3.13.2
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c7f226a3ed9e3a783e859dc8479e50da2694130147ffb4885645e02664eedbec`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 31.2 MB (31184573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374248f1569281ec7c40e636ecde3ff0a364b71e76250c51f4bf7577353d0377`  
		Last Modified: Tue, 08 Apr 2025 01:56:16 GMT  
		Size: 1.1 MB (1088784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1100e9714a653c26c07e9ceee3c410c833d40d1882754f9b1c3e4eef8d0424b2`  
		Last Modified: Tue, 08 Apr 2025 01:56:17 GMT  
		Size: 12.9 MB (12898776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107a3f0fe407600dce80b201374d7540c9d41953887e2ac7bdef02e5df3ef820`  
		Last Modified: Tue, 08 Apr 2025 01:56:16 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b05a62bb61103220dfa5fa83a173aac761ac5e63c1c5712ad62e99944c00eb`  
		Last Modified: Tue, 08 Apr 2025 02:20:54 GMT  
		Size: 5.7 MB (5707632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:3fdaff44f74fb86368f0ddfbcdcc4e6a2368ac7eea06534c37415638f4e0f636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2719815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47ce0b8169832dc13fc3a0273d205c5021a413df3b33d6b5a278436be6729f9`

```dockerfile
```

-	Layers:
	-	`sha256:8dafb09fe0387b805fd5c775e8ef540f632e491457d611172b8ce8d75b87940a`  
		Last Modified: Tue, 08 Apr 2025 02:20:54 GMT  
		Size: 2.7 MB (2710622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae4fb8f1ff8b1f5c006059922607aab3423bb5231c8d554e3212c7f28bb84b0`  
		Last Modified: Tue, 08 Apr 2025 02:20:54 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.in-toto+json
